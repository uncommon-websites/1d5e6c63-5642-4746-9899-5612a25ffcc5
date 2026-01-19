<script lang="ts">
    import ProductCard from './ProductCard.svelte';

    const products = [
        {
            badge: "Most Popular",
            code: "BB-01",
            title: "Custom Knitted Blanket",
            image: "/generated/image-a-stack-of-neatly-folded-colorful-custom-1768850712750-3.webp", 
            price: "Custom Quote"
        },
        {
            badge: "New",
            code: "BB-02",
            title: "Eco-Recycled Series",
            image: "https://images.unsplash.com/photo-1580302200322-2246319ad449?q=80&w=500&auto=format&fit=crop", 
            price: "Custom Quote"
        },
        {
            badge: "Premium",
            code: "BB-03",
            title: "Heritage Knit Throw",
            image: "https://images.unsplash.com/photo-1528906374430-ba5c685c1baf?q=80&w=500&auto=format&fit=crop",
            price: "Custom Quote"
        },
        {
            badge: "Institutional",
            code: "BB-04",
            title: "University Alumni Knit",
            image: "https://images.unsplash.com/photo-1543157145-f78c636d023d?q=80&w=500&auto=format&fit=crop",
            price: "Custom Quote"
        }
    ];
</script>

<section class="bg-black py-24">
    <div class="container mx-auto px-6 md:px-12">
        <div class="flex flex-col md:flex-row justify-between items-end mb-16 text-white">
            <div class="max-w-xl">
                <h2 class="text-4xl md:text-[44px] leading-tight font-medium tracking-tight mb-6">Knitted with purpose. Built for brands.</h2>
                <p class="text-[17px] text-white/80 font-light max-w-md leading-relaxed">We transform your brand identity into high-quality, fully custom blankets manufactured with 100% recycled materials in the USA.</p>
            </div>
            <a href="/" class="hidden md:inline-flex items-center text-[13px] font-bold border-b border-white/30 pb-0.5 hover:border-white transition-colors mt-6 md:mt-0 tracking-wide uppercase">
                View All Options <span class="ml-2">→</span>
            </a>
        </div>

        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-4">
            {#each products as product}
                <ProductCard {...product} isDark={true} />
            {/each}
        </div>

        <div class="mt-12 text-center md:hidden">
            <a href="/" class="inline-flex items-center text-[13px] font-bold border-b border-white/30 pb-0.5 hover:border-white transition-colors text-white tracking-wide uppercase">
                Shop All <span class="ml-2">→</span>
            </a>
        </div>
    </div>
</section>
