<template>
  <div class="okendo-widget-container">
    <div id="oke-reviews-widget"
      data-oke-reviews-widget
      :data-oke-reviews-product-id="'shopify-' + productId">
    </div>;
  </div>
</template>

<script>
export default {
  name: 'Review',
  props: {
    productId: String
  },
  mounted: function () {
    const reviewsWidget = window.document.querySelector('#oke-reviews-widget')
    window.okendoInitApi.initReviewsWidget(reviewsWidget)
  }
}
</script>

<style>
.okendo-widget-container {
  max-width: 960px;
  padding: 0 1em;
  margin: 5em auto;
}

.okeReviews .okeReviews-reviewsWidget-header-controls-writeReview {
    visibility: visible;
}

.okeReviews .okeReviews-reviewsWidget.is-okeReviews-empty {
    display: block;
}
</style>
