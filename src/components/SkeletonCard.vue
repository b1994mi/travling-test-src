<template>
  <!-- skeleton card by sheikh005 -->
  <div class="d-flex">
    <div class="rounded-circle overflow-hidden me-3 avatar-size">
      <div class="card__image loading"></div>
    </div>
    <div class="flex-grow-1">
      <div class="card__title loading"></div>
      <div class="card__description loading"></div>
    </div>
  </div>
</template>

<style scoped>
/* Card image loading */
.card__image img {
  width: 100%;
  height: 100%;
}

.card__image.loading {
  height: 300px;
  width: 400px;
}

/* Card title */
.card__title {
  padding: 8px;
  font-size: 22px;
  font-weight: 700;
}

.card__title.loading {
  height: 1rem;
  width: 50%;
  margin: 1rem;
  border-radius: 3px;
}

/* Card description */
.card__description {
  padding: 8px;
  font-size: 16px;
}

.card__description.loading {
  height: 3rem;
  margin: 1rem;
  border-radius: 3px;
}

/* The loading Class */
.loading {
  position: relative;
  background-color: #e2e2e2;
}

/* The moving element */
.loading::after {
  display: block;
  content: "";
  position: absolute;
  width: 100%;
  height: 100%;
  transform: translateX(-100%);
  background: -webkit-gradient(
    linear,
    left top,
    right top,
    from(transparent),
    color-stop(rgba(255, 255, 255, 0.2)),
    to(transparent)
  );

  background: linear-gradient(
    90deg,
    transparent,
    rgba(255, 255, 255, 0.2),
    transparent
  );

  /* Adding animation */
  animation: loading 0.8s infinite;
}

/* Loading Animation */
@keyframes loading {
  100% {
    transform: translateX(100%);
  }
}
</style>