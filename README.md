# animated-ripplebutton

A simple animated ripple button component, It can be easily modified and used for your project, A complete guide about how to build this project from scratch is covered in this [Youtube video](https://www.youtube.com/)

## Changing the defualt ripple color

The default ripple color can be changed by modifying the --desired-color variable. as shown here, the desire color was changed from tomato to blue. you can consider copying this variable to your variable list if you have them declared somewhere in y0our project before

```css
:root {
  --desired-color: blue;
}
```

## Creating and adding more custom ripples

To add more ripples we only need to modify the ripple animation and add more box-shadow values to the original, and increase the spread value to be higher than any declared previously, you can do this as many times as needed
<br>
Note: doing this will increase the ripple area and you might need to use a larger margin or spacing between this element and others

#### Two (2) Ripple | 20px spread increase

```css
:root {
  --desired-color: tomato;
}

@keyframes ripple {
  0% {
    box-shadow: 0 0 0 0 var(--desired-color), 0 0 0 0 var(--desired-color);
  }

  100% {
    box-shadow: 0 0 0 20px rgba(0, 0, 0, 0), 0 0 0 40px rgba(0, 0, 0, 0);
  }
}
```

#### Three (3) Ripple | 20px spread increase

```css
:root {
  --desired-color: tomato;
}

@keyframes ripple {
  0% {
    box-shadow: 0 0 0 0 var(--desired-color), 0 0 0 0 var(--desired-color),
      0 0 0 0 var(--desired-color);
  }

  100% {
    box-shadow: 0 0 0 20px rgba(0, 0, 0, 0), 0 0 0 40px rgba(0, 0, 0, 0),
      0 0 0 60px rgba(0, 0, 0, 0);
  }
}
```

#### Four (4) Ripple | 20px spread increase

```css
:root {
  --desired-color: tomato;
}

@keyframes ripple {
  0% {
    box-shadow: 0 0 0 0 var(--desired-color), 0 0 0 0 var(--desired-color),
      0 0 0 0 var(--desired-color), 0 0 0 0 var(--desired-color);
  }

  100% {
    box-shadow: 0 0 0 20px rgba(0, 0, 0, 0), 0 0 0 40px rgba(0, 0, 0, 0),
      0 0 0 60px rgba(0, 0, 0, 0), 0 0 0 60px rgba(0, 0, 0, 0);
  }
}
```

## Using multiple colors

To add more colors, you simply need to add more color variables and change the default declaration to include those variables, as shown below

```css
:root {
  --desired-color: red;
  --desired-color2: orange;
  --desired-color3: yellow;
}

@keyframes ripple {
  0% {
    box-shadow: 0 0 0 0 var(--desired-color), 0 0 0 0 var(--desired-color2),
      0 0 0 0 var(--desired-color3);
  }

  100% {
    box-shadow: 0 0 0 20px rgba(0, 0, 0, 0), 0 0 0 40px rgba(0, 0, 0, 0),
      0 0 0 60px rgba(0, 0, 0, 0);
  }
}
```

Noticed we also updated our fall back box shadow to carry the same number of desired box shadows and the third(3rd) value in this case was given a higher spread value.

## License

Animated ripple button is licensed under the [MIT license](http://opensource.org/licenses/MIT).
