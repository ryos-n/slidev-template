---
theme: apple-basic
title: SlidevのMarkdown記法サンプル
background: './background.jpg'
---

---
layout: intro-image
image: './background.jpg'
---

<div class="absolute top-10">
<img src="python2.jpeg" class="circle" />
  <span class="font-700">
    ryos
  </span>

</div>

<div class="absolute bottom-10">
  <h1>Slidevについて</h1>
  <p>Slidevで快適な資料作りは実現できるか🤔</p>
</div>

<style>
  .circle {
    border-radius: 50%;
    width: 36px;
    height: 36px;
    object-fit: cover;
    border: 1px solid #999;
    padding: 1px;
  }
</style>


---
layout: image-right
image: 'background_sub_1.jpg'
---

# アジェンダ

* クリックアニメーション
* モーション
* アイコン
* Twitterの連携

---

## クリックアニメーション

<div class="grid grid-cols-[50%,50%] gap-1"><div>

```markdown
<div v-click>Tailwindとは</div>
```

<div>▶︎をクリックすると表示</div>
<br>
<div v-click>Tailwindとは</div>
<br>

```markdown
<v-clicks>

- CSSのフレームワーク
- 1つのクラス名は1つのstyleに対応
- 作る人によって異なるデザインになる
- レスポンシブ対応が楽

</v-clicks>

```
<div>▶︎をクリックすると順番に表示</div>

<v-clicks>

- CSSのフレームワーク
- 1つのクラス名は1つのstyleに対応
- 作る人によって異なるデザインになる
- レスポンシブ対応が楽

</v-clicks>
</div><div>

```markdown
<div v-click>Tailwindのチートシートはこちら</div>
<a v-after href="https://flowbite.com/tools/tailwind-cheat-sheet/">Tailwind CSS Cheat Sheet</a>
```
<div>▶︎をクリックすると同時に表示</div>
<br>
<div v-click>Tailwindのチートシートはこちら</div>
<a v-after href="https://flowbite.com/tools/tailwind-cheat-sheet/">Tailwind CSS Cheat Sheet</a>

`v-after` は `v-click`をトリガーに実行される
<!-- <div v-click-hide>Hello</div> -->
<!-- <div class="slidev-vclick-target slidev-vclick-hidden">Text</div> -->
その他のクリックアニメーションは[こちら](https://sli.dev/guide/animations.html)

</div></div>

---
preload: false
---
## モーション


<div class="grid grid-cols-[50%,50%] gap-1"><div>
```markdown
<div v-motion
    :initial="{ opacity: 0, y: 100 }"
    :enter="{ opacity: 1, y: 0, scale: 1 }">
    ↑↑下から上のモーション↑↑
</div>
```
<br>

<div
    v-motion
    :initial="{ opacity: 0, y: 100 }"
    :enter="{ opacity: 1, y: 0 }">
↑↑下から上のモーション↑↑
</div>
<br>
<br>
<br>

詳しくは[@vueuse/motion](https://motion.vueuse.org/)

</div><div>
```markdown
<div
  v-motion
  :initial="{
    y: 100,
    opacity: 0,
  }"
  :enter="{
    y: 0,
    opacity: 1,
    transition: {
      y: {
        delay: 1600,
      },
      opacity: {
        duration: 1600,
      },
    },
  }"
>組み合わせるとこういうこともできます</div>
```

<div
  v-motion
  :initial="{
    y: 60,
    opacity: 0,
  }"
  :enter="{
    y: 10,
    opacity: 1,
    transition: {
      y: {
        delay: 1600,
      },
      opacity: {
        duration: 1600,
      },
    },
  }"
>組み合わせるとこういうこともできます</div>

</div></div>
---

## アイコン

`{collection-name}-{icon-name}`でアイコンを指定できます。

```markdown
<logos-aws-lambda/>
```

利用可能なアイコンは[Icônes](https://icones.js.org/)から探せます。

<br>
<div class="grid grid-cols-[30%,70%] gap-1"><div>
私の好きなAWSサービス
<logos-aws class="text-xl"/>

</div><div>
<div class="grid grid-cols-[30%,30%,30%] gap-1"><div>
<logos:aws-api-gateway class="text-8xl m-20 animate-bounce"/>
</div><div>
<logos-aws-lambda class="text-8xl m-20 animate-spin"/>
</div><div>
<logos:aws-dynamodb class="text-8xl m-20 animate-ping"/>
</div></div>

</div></div>

---

## Twitterの連携


```markdown
<Tweet id="1329048290977955840"/>

```

<div class="grid grid-cols-[60%,40%] gap-4">

<div>
<Tweet id="1329048290977955840"/>
</div>

<div>


</div>

</div>
---
