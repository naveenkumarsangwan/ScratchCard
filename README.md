# Android Scratchcard
Custom Scratchcard View for Android

       
How to use
-----
**Step 1:** add this to your xml:
```xml
 <RelativeLayout
        android:layout_width="match_parent"
        android:layout_height="match_parent">

        <TextView
            android:id="@+id/textView"
            android:layout_width="240dp"
            android:layout_height="150dp"
            android:layout_centerInParent="true"
            android:text="YOU EARNED 20" />
  
        <in.niks.helpers.ScratchCard
            android:id="@+id/scratchCard"
            android:layout_width="240dp"
            android:layout_height="150dp"
            android:layout_centerInParent="true"/>

    </RelativeLayout>
```
**Step 2:** implement setOnScratchListener to Play with Listener.
```java
private ScratchCard mScratchCard;

.....
    
mScratchCard = (ScratchCard) findViewById(R.id.scratchCard);
mScratchCard.setOnScratchListener(new ScratchCard.OnScratchListener() {
    @Override
    public void onScratch(ScratchCard scratchCard, float visiblePercent) {
         if (visiblePercent > 0.3) {
             mScratchCard.setVisibility(View.GONE);
             Toast.makeText(MainActivity.this, "Content Visible", Toast.LENGTH_SHORT).show();
          }
     }
});
    



