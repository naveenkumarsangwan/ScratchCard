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
    


License
-------

    Copyright 2017 Niks

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
