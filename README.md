# Android-app
Straight path
/**
 * This function assumes logger is an instance of AppEventsLogger and has been
 * created using AppEventsLogger.newLogger() call.
 */
public void logAddedToCartEvent (String contentData, String contentId, String contentType, String currency, double price) {
    Bundle params = new Bundle();
    params.putString(AppEventsConstants.EVENT_PARAM_CONTENT, contentData);
    params.putString(AppEventsConstants.EVENT_PARAM_CONTENT_ID, contentId);
    params.putString(AppEventsConstants.EVENT_PARAM_CONTENT_TYPE, contentType);
    params.putString(AppEventsConstants.EVENT_PARAM_CURRENCY, currency);
    logger.logEvent(AppEventsConstants.EVENT_NAME_ADDED_TO_CART, price, params);
}
