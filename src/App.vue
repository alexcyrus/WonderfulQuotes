<template>
    <div class="container">
        <app-new-quote @quoteAdded="newQuote"></app-new-quote>
        <app-quote-grid :quotes="quotes"></app-quote-grid>
    </div>
</template>

<script>
import QuoteGrid from './components/QuoteGrid.vue';
import NewQuote from './components/NewQuote.vue';

export default {
    data: function() {
        return {
            quotes: [
                "A random quote"
            ],
            maxQuotes: 10
        }
    },
    methods: {
        newQuote() {
            this.quotes.push(quote);
        }
    },
    components: {
        appQuoteGrid: QuoteGrid,
        appNewQuote: NewQuote
    }
}
</script>

<style>
</style>
