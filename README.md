# Simple Alphabet Indexer Recycler view
Simple Alphabet Index Recycler view is a library for indexing the recycler view list by selecting a letter. 

### Dependencies
Add it in your root build.gradle at the end of repositories:
```
allprojects {
    repositories {
	...
	maven { url 'https://jitpack.io' }
    }
}
```

Add the dependency in your application build.gradle file
```
dependencies {
    compile 'com.github.mnhmasum:SimpleAlphabetIndexer:1.0'
}

```

### XML
```
<com.masum.atoz.indexer.SimpleAlphabetIndexerView
    android:id="@+id/alphabetIndexerView"
    android:layout_width="match_parent"
    android:layout_height="match_parent"/>

```

### JAVA
```
SimpleAlphabetIndexerView simpleAlphabetIndexerView = (SimpleAlphabetIndexerView) findViewById(R.id.alphabetIndexerView);
        simpleAlphabetIndexerView.setAdapter(mAdapter);
        simpleAlphabetIndexerView.addListener(new OnSelectLetter() {
            @Override
            public void onSelectLetter(String letter) {
                Toast.makeText(MainActivity.this, letter, Toast.LENGTH_SHORT).show();
                // do something with the selected letter
            }
        });

```
### To change the Indexer view background color
```
simpleAlphabetIndexerView.setBackgroundColor(getResources().getColor(R.color.colorPrimaryDark));
```
### To change letters font color
```
simpleAlphabetIndexerView.setLetterFontColor(getResources().getColor(R.color.white))
```

