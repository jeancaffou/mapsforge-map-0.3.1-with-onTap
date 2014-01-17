mapsforge-map-0.3.1-with-onTap
==============================

Since this is only a commited patch taken from **[here](https://code.google.com/p/mapsforge/issues/attachmentText?id=336&aid=3360005000&name=TouchEventHandler-r2106.patch&token=0P8mhXQZw5JU8cyFmuognsDiuWE%3A1389987593337)**, the thing to notice is this:
> onTap = ovl.getClass().getMethod("onTap", GeoPoint.class, MapView.class);

Therefore, implementing an onTap() method in an Overlay item should yield expected results.

Example:
```
public abstract class ResponsiveOverlay implements Overlay {
	
	public void onTap(GeoPoint geoPoint) {

	}
	// ...
}
