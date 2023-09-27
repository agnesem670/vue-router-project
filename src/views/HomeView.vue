<template>
  <div class="home">
    <h1>Home</h1>
    <PostList :posts="posts" />
  </div>
</template>

<script>
import PostList from '@/components/PostList.vue';
import { ref } from 'vue';

export default {
  name: 'HomeView',
  components: { PostList },
  setup() {
    const posts = ref([
      {
        title: 'welcome to the blog',
        body: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Suscipit facere vitae dolore rem at a aut magni dicta, nisi quos laborum. Expedita delectus, excepturi quasi nulla dolorem iste optio labore nobis tempora blanditiis alias, at rem numquam fugiat ducimus molestiae ex ipsam laborum quia? Dignissimos animi fugit voluptas eveniet beatae!',
        id: 1
      },
      {
        title: 'top 5 css tips',
        body: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Suscipit facere vitae dolore rem at a aut magni dicta, nisi quos laborum. Expedita delectus, excepturi quasi nulla dolorem iste optio labore nobis tempora blanditiis alias, at rem numquam fugiat ducimus molestiae ex ipsam laborum quia? Dignissimos animi fugit voluptas eveniet beatae!',
        id: 2
      },
    ]);
    return { posts };
  },
  components: { PostList }
}
</script>


