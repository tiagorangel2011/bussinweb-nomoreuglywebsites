<style>
.ExampleDiv {
  background-color: #0276ff;
  width: 150px;
  height: 50px;
  text-align: center;
  margin: 10px;
  color: white;
}
</style>

Making a better website
=========================


## 1. No More Bright Colors
Bright colors with bright text, such as <span class="unstyled" style="color: white; background-color: yellow;">Yellow with white text</span> or dark colors with dark text, such as <span class="unstyled" style="background-color: blue;">blue with black text</span>, can really make a website unattractive.

If you wanted white text, you could use <span class="unstyled" style="color: white; background-color: darkblue;">Dark Blue With White</span>, or <span style="background-color: yellow;">Yellow with black</span>, but beware: to much yellow can make a website hurt the viewers eyes, and dark blue with white can also look bad.

So for a light-themed website, you would want something like <span class="unstyled" style="background-color: #0276ff;"><b>#0276ff</b> with white text</span>, is way less harsh then some of the other things we have talked about.
      
## 2. No More Straight Edges
Let's say you have a fun DIV element with text in the center:

<div class="ExampleDiv unstyled">
  My #0276ff Background!
</div>

This already looks great, but we can make it better with the `border-radius:` CSS Element. If we set the border radius to 10px, or DIV element looks like such:
    
<div class="ExampleDiv unstyled" style="border-radius: 10px;">
  My #0276ff Background!
</div>

Much better! Just for fun, let's set it to <b>100%</b>...

<div class="ExampleDiv unstyled" style="border-radius: 100%;">
  My #0276ff Background!
</div>

Ewww....... So keep it small, ranging from 3px - 10px for rounded edges!

**Note:** If you have a div that's a perfect square, then using `border-radius: 100%` is ok.

## 3. No More Default Buttons
So, we don't want default buttons like [un]<button>this</button>[/un] because they are kind of basic and pretty ugly. Now, if we took our element, it could already be a button:

<div class="ExampleDiv unstyled" style="border-radius: 10px;" onclick="alert('Never gonna give you up')">Me? A button?</div>
          
(belive it or not, that actually does something when clicked... we'll get to better styling later)

But still, screen readers and such would not be able to focus into the button in this case. So let's go back to the default button and add a event listener - onclick to it.

    <button onclick="alert('Never gonna give you up')">Click me</button>
**Result:** [un]<button class="unstyled" onclick="alert('Never gonna give you up')">Click me</button>[/un]

Ok, but that still looks pretty bad. So let's style it a bit!

```
<style>
button {
  background-color: #0276ff;
  border-radius: 4px;
  border: none;
  color: #fff;
  cursor: pointer;
  font-size: 16px;
  font-weight: 700;
  line-height: 1.5;
  padding: 9px 20px 8px;
}

button:hover,
button:focus {
  opacity: .75;
}
</style>

<button onclick="alert('Never gonna give you up')">Click me</button>
```
<style>
.btn_init {
  background-color: #0276ff;
  border-radius: 4px;
  border: none;
  color: #fff;
  font-size: 16px;
  font-weight: 700;
  line-height: 1.5;
  padding: 9px 20px 8px;
}

.btn_init:hover,
.btn_init:focus {
  opacity: .75;
}
</style>

**Result:** [un]<button class="btn_init unstyled" onclick="alert('Never gonna give you up')" style="cursor: default;">Click me</button>[/un]

That is actually pretty good, but if we use <code>cursor: pointer</code> CSS element, it will be even better, as when hovering the button the mouse will actually switch to a hand:

[un]<button class="btn_init unstyled" style="cursor: pointer" onclick="alert('Never gonna give you up')">Click me</button>[/un]

You can find other nice, fancy buttons that you can just copy-paste [here](https://getcssscan.com/css-buttons-examples).

**Tip:** Don't overcomplicate it unless you know exactly what you're doing. Don't make the button spin. Don't add a weird background. Don't use a weird box shadow.

<footer>
This page is not complete. There will be more soon with more code.
</footer>