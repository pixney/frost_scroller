# Frost componets

## Scroller
``` 
<div x-cloak x-data="scroller" @resize.window="onWindowResize" @load.window="onDocumentLoad" class="c-scroller" :class="{'-ready':ready}">
  <ul class="c-scroller__list -original">
    <li class="c-scroller__item -original pr-8">
      <p>
        I am text and can be <strong>bold</strong> and conatain contain images or other html elments <button
        class="bg-slate-500 text-white p-2 py-1 mx-4 rounded-md">like a button</button>
      </p>
    </li>
  </ul>
</div>
```