<template>
  <div class="item">
    <div class="item-body">
      <slot />
    </div>
    <div class="item-footer">
      <slot name="footer" />
    </div>
  </div>
</template>

<script>
export default {
  name: 'TextureItem',
}
</script>

<style lang="stylus">
.item
  display block
  background #EFF1F0
  box-shadow 0 1px 1px rgba(0, 0, 0, 0.1)
  border-radius 2px
  float left
  position relative
  margin-right 20px
  margin-bottom 20px
  cursor pointer
  width 210px
  height 196px
  transition box-shadow 0.1s ease-in-out 0s

.item-body
  height 166px

  img
    max-width 100%
    margin-left 30px
    margin-top 16px
    width 150px

@media (max-width: 756px)
  .item
    width 45%
    margin-right 5%

  .item-body > img
    margin-left 25%

  .texture-name
    width 65%

@media (max-width: 520px)
  .item
    width 100%

  .item-body > img
    margin-left 30%

  .texture-name
    width 80%

.item:hover
  box-shadow 0 6px 12px rgba(0, 0, 0, 0.175)

.item-selected
  box-shadow 0 6px 12px rgba(0, 0, 0, 0.175)

.item-footer
  background #50b3ec
  color #fff
  font-size 16px
  height 30px
  padding 3px 8px

  .more
    float right
    margin-left 6px
    margin-right 3px
    color #fff

  .more:hover
    color #dadada

  small
    font-size 50%
</style>
