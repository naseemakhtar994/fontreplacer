#Font Replacer

Change all text in your android application with selected font

Usage
=====
Put your font (.ttf) file in assets folder.

On your Application class, add this line inside onCreate():

```
Replacer replacer = FontReplacer.Build(getApplicationContext());
replacer.setDefaultFont("myfont.ttf");
replacer.setBoldFont("myfont-bold.ttf");
...
replacer.setThinFont("myfont-thin.ttf");
replacer.setLightFont("myfont-light.ttf");
...
replacer.applyFont();
```

On xml layout, change the font family properties with "sans-serif" to use selected light/medium/thin font:
```
<TextView
   android:id="@+id/text"
   android:layout_width="wrap_content"
   android:layout_height="wrap_content"
   android:textStyle="bold"
   android:text="This is medium bold font"
   android:fontFamily="sans-serif-medium"
/>
```

If you want to use your default font to another code, just use:

```
Typeface font = FontReplacer.getDefaultFont();
yourview.setTypeface(font);
```

