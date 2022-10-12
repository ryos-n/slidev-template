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

* アイコン
* Twitterの連携

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
