# Frost componets
A collection of components built with AlpineJS and Tailwind for use with the Frost Starter Kit made available to Statamic.

The components are using my own adoption of the ABEM styling convention.
- [ABEM pattern library](https://imarc-boilerplate.netlify.app/pattern-library/docs/abem.html)
- [Css tricks writing on the topic of ABEM](https://css-tricks.com/abem-useful-adaptation-bem/)


## How to use
Even though the intention of these components are to be distributed with the frost starter kit, they can be used in other scenarios as well.

To use them in other scenarios, you need tailwind setup. Then include the correct tailwind plugin from this repository to your configuration file. 

Copy the markup into your html file and make sure you import the component to your javascript file.

## Components
### Hamburger
```
<button title="close mobile navigation" x-data="{'open':false}" class="c-hamburger" :class="{'-active':open}"
  type="button" @click="open = !open">
  <span class="c-hamburger__line -top"></span>
  <span class="c-hamburger__line -center"></span>
  <span class="c-hamburger__line -bottom"></span>
</button>
```
### Scroller
A horizontal scroll component which supports scrolling different html elements across the screen.

#### Html markup
Simply copy and paste the following to your website.

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

### Navigation
```
<div x-data="navigation" class="c-navigation">

    <div class="c-navigation__logo">
      <svg class="w-full h-full" width="404" height="172" viewBox="0 0 404 172" fill="none" xmlns="http://www.w3.org/2000/svg">
        <path d="M20.647 46.3077V57.0292H38.5712V58.8541H20.647V171.088H4.76468V58.8541H0V57.0292H4.76468V46.3077C4.76468 29.7312 8.31929 17.9452 15.4285 10.9496C22.5377 3.80196 34.0334 0.152085 49.9157 0V1.82494C39.4788 1.97701 31.9914 5.55084 27.4536 12.5464C22.9159 19.3899 20.647 30.6437 20.647 46.3077Z" fill="black"/>
        <path d="M97.8692 66.8382V62.0478C91.0625 64.7852 84.8608 70.336 79.2642 78.7003C73.6676 86.9125 70.7181 94.6684 70.4155 101.968V171.088H54.5333V57.0292H70.4155V93.2997C72.8357 84.4792 77.4491 76.191 84.2558 68.435C91.0625 60.527 98.7767 56.4209 107.399 56.1167H108.306C111.331 56.1167 113.827 57.1813 115.793 59.3104C117.911 61.2874 118.97 63.7966 118.97 66.8382C118.97 69.8798 117.911 72.389 115.793 74.3661C113.827 76.3431 111.331 77.3316 108.306 77.3316C105.281 77.3316 102.785 76.3431 100.819 74.3661C98.8524 72.389 97.8692 69.8798 97.8692 66.8382Z" fill="black"/>
        <path d="M180.76 172C164.878 172 151.945 167.438 141.962 158.313C131.979 149.188 126.987 135.121 126.987 116.111C126.987 97.1017 132.13 82.3501 142.416 71.8568C152.853 61.3634 166.012 56.1167 181.895 56.1167C197.928 56.1167 210.936 60.6791 220.92 69.8037C230.903 78.9284 235.894 92.9956 235.894 112.005C235.894 131.015 230.676 145.767 220.239 156.26C209.953 166.753 196.794 172 180.76 172ZM182.348 57.9416C170.853 57.9416 161.323 63.1123 153.76 73.4536C146.197 83.6428 142.416 97.9381 142.416 116.34C142.416 134.589 145.895 148.124 152.853 156.944C159.811 165.765 169.037 170.175 180.533 170.175C192.029 170.175 201.558 165.08 209.121 154.891C216.684 144.55 220.466 130.255 220.466 112.005C220.466 93.6039 216.987 79.9929 210.029 71.1724C203.071 62.3519 193.844 57.9416 182.348 57.9416Z" fill="black"/>
        <path d="M315.768 65.0133C313.348 63.0363 309.415 61.3634 303.97 59.9947C298.676 58.626 294.668 57.9416 291.945 57.9416C289.222 57.9416 287.634 57.9416 287.18 57.9416C279.012 58.0937 273.113 60.2228 269.483 64.3289C265.853 68.2829 264.037 72.7692 264.037 77.7878C264.037 82.8064 265.626 87.0646 268.802 90.5623C271.979 93.908 275.911 96.5694 280.6 98.5464C285.441 100.371 290.584 102.5 296.029 104.934C301.626 107.367 306.768 109.876 311.457 112.462C316.298 114.895 320.306 118.545 323.483 123.411C326.659 128.126 328.247 134.057 328.247 141.204C328.247 148.352 325.751 154.435 320.76 159.454C315.768 164.472 310.172 167.818 303.97 169.491C297.92 171.164 291.34 172 284.231 172C268.802 172 257.231 168.578 249.517 161.735L250.878 160.366C253.903 163.256 258.365 165.613 264.264 167.438C270.315 169.263 276.138 170.175 281.735 170.175C290.659 170.175 297.995 167.742 303.743 162.875C309.642 157.857 312.592 151.698 312.592 144.398C312.592 136.946 310.399 131.015 306.012 126.605C301.626 122.042 296.256 118.545 289.903 116.111C283.701 113.526 277.424 111.017 271.071 108.584C264.718 105.998 259.348 102.5 254.962 98.0902C250.575 93.5279 248.382 88.2812 248.382 82.3501C248.382 76.4191 249.743 71.6287 252.466 67.9788C255.189 64.1768 258.819 61.5155 263.357 59.9947C271.071 57.4094 278.785 56.1167 286.5 56.1167C299.508 56.1167 309.642 58.55 316.903 63.4165L315.768 65.0133Z" fill="black"/>
        <path d="M344.101 58.8541V57.0292H348.866V34.2175H364.748V57.0292H399.462V58.8541H364.748V141.889C364.748 151.774 365.807 158.921 367.925 163.332C370.193 167.742 374.807 169.947 381.765 169.947C388.874 169.947 396.059 168.502 403.319 165.613L404 167.438C396.437 170.327 387.74 171.772 377.908 171.772C368.227 171.772 360.967 169.795 356.126 165.841C351.286 161.735 348.866 153.675 348.866 141.66V58.8541H344.101Z" fill="black"/>
        </svg>          
    </div>

    <div class="c-navigation__wrapper">
      
      <ul class="c-navigation__desktopNav">
        <li>item</li>
        <li>item</li>
        <li>item</li>
        <li>item</li>
      </ul>
      
      <div class="c-navigation__hamburgerWrapper">
        <button type="button" title="close mobile navigation" class="c-hamburger" :class="{'-active':open}" type="button"
          @click="onToggle">
          <span class="c-hamburger__line -top"></span>
          <span class="c-hamburger__line -center"></span>
          <span class="c-hamburger__line -bottom"></span>
        </button>
      </div>
    </div>


  <template x-teleport="body">

    <div x-show="open" x-ref="overlay" class="c-mobileNav"  
      x-transition:enter="transition ease-out duration-[500ms]"
      x-transition:enter-start="-translate-x-full opacity-0" 
      x-transition:enter-end="translate-x-0 opacity-100"
      x-transition:leave="transition ease-in duration-[300ms] " 
      x-transition:leave-start="translate-x-0 opacity-100"
      x-transition:leave-end="-translate-x-full opacity-0" >

      <div class="c-mobileNav__inner">

        <ul >
          <li>
            <a class="text-lg" href="/"  @click.prevent="onNavigation">Home</a>
          </li>
          <li>
            <a class="text-lg" href="/"  @click.prevent="onNavigation">Away</a>
          </li>
        </ul>

        <div x-ref="socialMediaLinks" class="c-mobileNav__socialMedia" x-show="showSocialMediaLinks"
          x-transition:enter="transition ease-out duration-[500ms]"
          x-transition:enter-start="translate-y-24 opacity-0" x-transition:enter-end="translate-y-0 opacity-100"
          x-transition:leave="transition ease-in duration-[0ms]" x-transition:leave-start="translate-y-0 opacity-100"
          x-transition:leave-end="translate-y-24l opacity-0">
          <ul class="c-mobileNav__socialMediaList">
            <li>Icon</li>
            <li>Icon</li>
            <li>Icon</li>
          </ul>
        </div>

      </div>

    </div>
  </template>

</div>
```