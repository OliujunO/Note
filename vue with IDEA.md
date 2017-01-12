1. **Use Vue.js plugin**.

**UPDATE**: Both plugins have own problems atm

- [vue-for-idea](https://github.com/henjue/vue-for-idea) has weird [side-effects](https://github.com/henjue/vue-for-idea/issues/46) (hiding `node_modules` from project view);
- [John Kelly's Vue.js plugin](https://github.com/postalservice14/vuejs-plugin) force you to use special declarations for ES6 and scss, sass (see deprecated section below)

> You can install it via `Settings(Preferences)` => `Plugins` => `Browse repositories` => (search for) "vue"

choose one or both: "Vue.js" or "vue-for-idea". It's up to you.

1. **Set "Javascript Language Version" to ES6**.

> Open `Settings(Preferences)` => `Language & Frameworks` => `JavaScript`. Set `Javascript Language Version` to `ECMAcript6`
>
> [https://github.com/postalservice14/vuejs-plugin](https://github.com/postalservice14/vuejs-plugin)

1. **Improve HTML-tag's attributes highlighting**

> Open `Settings(Preferences)` => `Editor` => `Inspection` => `HTML` => select `Unknown HTML tag attributes` => click `Custom HTML tag attributes`. Add your attributes.

For example, my list:

> v-on,v-on:click,v-on:change,v-on:focus,v-on:blur,v-on:keyup,:click,@click,v-model,v-text,v-bind,:disabled,@submit,v-class,:class,v-if,:value,v-for,scoped,@click.prevent,number,:readonly,@input,@click,v-show,v-else,readonly,v-link,:title,:for,tab-index,:name,:id,:checked,transition,@submit.prevent,autocapitalize,autocorrect,slot,v-html,:style

P.S. For more full list of custom tags check [@Alex's](http://stackoverflow.com/a/40097776/930170) answer below

P.P.S. Actually it's should work in more common way:

> Open `Settings(Preferences)` => `Languages & Frameworks` => `Javascript` => `Libraries` => click `Add` (after this you should set path to the `vue.js`. You can dowmload it with npm or whatever)

(More info in this answer: [http://stackoverflow.com/a/28903910/930170](http://stackoverflow.com/a/28903910/930170))

But I didn't get success with that.

1. **Enable Node.js Coding Assistance:**

Open `Settings(Preferences)` => `Languages & Frameworks` => `Node.js and NPM`

> If "Node.js core library is not enabled", click button `Enabled`

------

**DEPRECATED** (may be required if you don't use vue-plugins for IDE):

1. **Make \*.vue files to be recognized as a html-flies**.

> Open `Settings(Preferences)` => `Editor` =>`File Types` find `HTML` in `Recognized File Types`, then add `*.vue` as a new Registered Patterns.

1. **Improve ES6 highlight**.

> In each `vue` file with tag:
>
> ```
>     <script type="text/babel">
>         // your code here...
>     </script>
>
> ```

(This is would help to recognise constructions like `setTimeout(() => {console.log(1) }, 100)`)

1. **Improve styles highlight**. (sass, scss, etc)

> In each `vue` file with tag:
>
> ```
>     <style lang="sass" rel="stylesheet/sass">
>         // your style here...
>     </style>
>
> ```

For `scss` it's gonna be ``

------

**UPD**: The steps below are not so trusted, they *may* helps, or may not, some of them I didn't check personally, or I didn't catch is any effect exist or not.

1. **Import TextMate Bundle functionality**.

> [https://www.jetbrains.com/help/phpstorm/2016.1/textmate-bundles.html?origin=old_help](https://www.jetbrains.com/help/phpstorm/2016.1/textmate-bundles.html?origin=old_help)

1. **Import TypeScript tables for vue**.

> Open `Settings(Preferences)` => `Language & Frameworks` => `JavaScript` => `Libraries`. Click`Download`, Switch to `TypeScript community stubs`. And download all tabs with `vue` word.
>
> Example: [https://youtu.be/4mKiGkokyx8?t=84](https://youtu.be/4mKiGkokyx8?t=84) (from 1:24)

------

**UPD2:** For **more info** check the issue at github: [https://github.com/vuejs/vue-syntax-highlight/issues/3](https://github.com/vuejs/vue-syntax-highlight/issues/3)