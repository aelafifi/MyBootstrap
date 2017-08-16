# MyBootstrap
General purpose CSS classes for aspectratio, padding, margin, and dimensions, ...etc

## General Classes:
* rtl, ltr
* cover, contain
* valign-top, valign-bottom, valign-middle

#### Example:
```html
<div class="rtl">
    This will be right-to-left<br/>
    <img src="..." width="100" height="100" class="contain" />
</div>
```

## Aspect Ratio:

.ratio-X: aspect-ratio of the element = 100:X

X = {5, 10, 15, ... 200}

##### Special Classes:

* .ratio-16-9
* .ratio-3-2

#### Example:

```html
<div class="profile-picture ratio-100">
    <!-- Square Div (aspect-ratio = 100:100) -->
    <img src="..." class="cover" /> <!--{ .cover: found in General Classes section }-->
</div>
```

```html
<div class="slider ratio-50">
    <!-- aspect-ratio = 100:50 = 2:1 -->
    ...
</div>
```

```html
<div class="slider ratio-16:9">
    <!-- aspect-ratio = 16:9 (special `ratio` class) -->
    ...
</div>
```

#### Take Care:

The element with the `ratio-X` class is `{ position: relative; }` and the direct child of it is `{ position: absolute; }` and it fills the parent one with the class `ratio-X`. If you want to customize (width, height, margin, padding) it's good to do it for 3rd level element, something like that:

```html
<div class="ratio-X"><!-- Size Wrapper -->
    <div><!-- Sized DIV -->
        <div class="your-custom-class-here">...</div>
    </div>
</div>
```

## Padding:

* pX: padding (all)
* phX: padding (horizontal)
* pvX: padding (vertical)
* ptX: padding (top)
* pbX: padding (bottom)
* plX: padding (left)
* prX: padding (right)

X = {0, 5, 10, 15, ... 120}

#### Example:
```html
<div class="ph30 pv15">
    Horizontal Padding: 30px;
    Vertical Padding:   15px;
</div>
```

## Margin:

Same as padding

* mX, mhX, mvX, mtX, mbX, mlX, mrX

## Margin Out:

Same as padding and margin, but values are in negative

* moX, mohX, movX, motX, mobX, molX, morX

#### Example:
```html
<div class="mot15">
    margin-top: (-)15px;
</div>
```

## Dimensions:

* .wX   : width = X
* .hX   : height = X
* .sqrX : width & height = X (Square)
* .wpX  : width = X% (Width in Percentage)
* .hpX  : height = X% (Height in Percentage)

X = {0, 5, 10, ... 200}

#### Example:

```html
<div class="wp50">
    Width = 50%
</div>

<div class="sqr70">
    Width = Height = 70px
</div>

And so on...
```

## License

Copyright 2017 Ahmed S. El-Afifi <ahmed.s.elafifi@gmail.com>

Licensed under the MIT License
