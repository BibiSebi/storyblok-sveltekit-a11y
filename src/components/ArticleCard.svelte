<script>
	import { storyblokEditable } from '@storyblok/svelte';
	export let article;
	export let slug;
</script>

<a href="/{slug}" class="w-full h-full bg-[#f7f6fd] rounded-[5px] text-center border-2 border-transparent overflow-hidden hover:shadow-2xl hover:border-[#50b0ae] transition">
<article
	use:storyblokEditable={article}
>
    <img
      src="{article.image.filename}/m/600x0"
      alt={article.image.alt}
      class="w-full h-48 xl:h-72 object-cover pointer-events-none"
    />
    <div class="p-4">
      <h3 class="text-xl text-[#1d243d] font-bold mb-3">
        {article.title}
      </h3>
      <p class="line-clamp-4">
        {article.teaser}
      </p>

    </div>
</article>
</a>

