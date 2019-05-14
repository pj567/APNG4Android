# APNG&Webp4Android
* Support APNG & Animated Webp
* Implement play control
* Fast Decode
* Low memory usage
* No temporary files generated
* Support still image
* Lightweight implementation
## 使用示例
```java
// Load from asset file
AssetStreamLoader assetLoader = new AssetStreamLoader(context, "wheel.png");
 
 
// Load form Resource
ResourceStreamLoader resourceLoader = new ResourceStreamLoader(context, R.drawable.sample);
 
 
// Load from file
FileStreamLoader fileLoader = new FileStreamLoader("/sdcard/Pictures/1.webp");
 
 
// Create APNG Drawable
APNGDrawable apngDrawable = new APNGDrawable(assetLoader);

//Create Animated webp drawable
WebPDrawable webpDrawable = new WebPDrawable(assetLoader);
 
// Auto play
imageView.setImageDrawable(apngDrawable);
 
 
// Not needed.default controlled by content
apngDrawable.setLoopLimit(10);
 
 
// Implement Animatable2Compat
drawable.registerAnimationCallback(new Animatable2Compat.AnimationCallback() {
    @Override
    public void onAnimationStart(Drawable drawable) {
        super.onAnimationStart(drawable);
    }
});
```
