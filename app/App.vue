<template>
  <Page>
    <ActionBar :title="navbarTitle"/>
    <GridLayout rows="auto, auto">
      <HelloWorld :msg="msg"/>
    </GridLayout>
  </Page>
</template>
<script>
  import HelloWorld from '~/components/HelloWorld';

  const { VUE_APP_MODE, VUE_APP_PLATFORM } = process.env;

  console.info("------ENV21-------",process.env)

  export default {
    components: {
      HelloWorld,
    },
    data() {
      return {
        navbarTitle: `App.vue`,
        msg: "WTF21",
      };
    },
    methods: {
    }
  };
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style web>
  @import '~styles/style-one';

  .w-page {
    height: 100%;
    width: 100%;
  }
</style>
<style native>
  @import '~styles/style-one';
</style>
