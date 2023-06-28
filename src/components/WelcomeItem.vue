<template>
  <div class="item">
    <i>
      <slot name="icon"></slot>
    </i>
  </div>
</template>

<style scoped>
.item {
  margin-top: 4rem;
  display: flex;
  justify-content: center;
  align-items: center;
}

.details {
  flex: 1;
  margin-left: 1rem;
}

i {
  display: flex;
  place-items: center;
  place-content: center;
  width: 32px;
  height: 32px;

  color: var(--color-text);
}

@media (min-width: 1024px) {
  .item {
    margin-top: 2rem;
  }

  i {
    top: calc(50% - 25px);
    border: 1px solid var(--color-border);
    background: var(--color-background);
    border-radius: 8px;
    width: 50px;
    height: 50px;
  }

  .item:first-of-type:before {
    display: none;
  }

  .item:last-of-type:after {
    display: none;
  }
}
</style>
