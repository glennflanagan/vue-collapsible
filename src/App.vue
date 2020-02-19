<template>
  <div id="app">
    <Collapsible class="example-collapsible">
      <!-- <div slot="trigger">
        Trigger
      </div>-->
      <div id="example">
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Amet nesciunt
          neque rem at corporis deserunt fugiat? Amet placeat ab commodi culpa.
          Optio voluptatem aperiam atque aut omnis odio tenetur esse nostrum
          quod culpa. Consequatur accusamus illum temporibus earum. Laudantium
          aliquam culpa expedita, animi facere dolorem explicabo quasi
          excepturi? Illo unde nostrum sint odit officiis molestiae ad omnis
          dolores suscipit labore, odio laboriosam aut necessitatibus officia
          itaque? Earum aut eligendi rem placeat aspernatur optio quasi illo
          culpa iure delectus neque, laudantium architecto magnam ratione
          tempore est facilis ex sint, amet, et incidunt nobis similique vero!
          Nam, itaque, aliquam neque perferendis dolores assumenda doloremque
          perspiciatis necessitatibus odio fugiat minus? Maiores, perspiciatis?
          Voluptate consectetur nemo temporibus adipisci quasi corporis,
          eveniet, ullam atque recusandae facere minus animi maxime tempore quis
          ipsam cum nihil harum dolorum amet. Expedita commodi consequatur
          reprehenderit porro libero quidem velit, harum in, possimus maiores
          culpa, nemo exercitationem accusantium temporibus? Voluptates vero
          eligendi, fugiat eos nostrum repudiandae ex fuga pariatur accusamus
          nemo dolore provident at doloremque rem veniam a aut sed excepturi!
          Ipsum illo quae, quidem deserunt possimus eius tempora facere maxime
          voluptate in maiores molestiae similique quos nulla inventore
          quibusdam praesentium molestias aliquam labore ut odit quod
          voluptatibus eum accusamus.
        </p>
      </div>
    </Collapsible>

    <Collapsible
      class="example-collapsible"
      openLabel="Custom open label"
      closedLabel="Custom closed label"
      :isOpen="false"
    >
      <div id="example2">
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Amet nesciunt
          neque rem at corporis deserunt fugiat? Amet placeat ab commodi culpa.
          Optio voluptatem aperiam atque aut omnis odio tenetur esse nostrum
          quod culpa. Consequatur accusamus illum temporibus earum. Laudantium
          aliquam culpa expedita, animi facere dolorem explicabo quasi
          excepturi? Illo unde nostrum sint odit officiis molestiae ad omnis
          dolores suscipit labore, odio laboriosam aut necessitatibus officia
          itaque? Earum aut eligendi rem placeat aspernatur optio quasi illo
          culpa iure delectus neque, laudantium architecto magnam ratione
          tempore est facilis ex sint, amepora facere maxime voluptate in
          maiores molestiae similique quos nulla inventore quibusdam praesentium
          molestias aliquam labore ut odit quod voluptatibus eum accusamus.
        </p>
      </div>
    </Collapsible>

    <Collapsible class="example-collapsible">
      <div slot="trigger">
        <div class="customTrigger">
          <h2>Custom open trigger element</h2>
          <Icon />
        </div>
      </div>

      <div slot="closedTrigger">
        <div class="customTrigger">
          <h2>Custom closed trigger element</h2>
          <Icon />
        </div>
      </div>

      <div id="example2">
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Amet nesciunt
          neque rem at corporis deserunt fugiat? Amet placeat ab commodi culpa.
          Optio voluptatem aperiam atque aut omnis odio tenetur esse nostrum
          quod culpa. Consequatur accusamus illum temporibus earum. Laudantium
          aliquam culpa expedita, animi facere dolorem explicabo quasi
          excepturi? Illo unde nostrum sint odit officiis molestiae ad omnis
          dolores suscipit labore, odio laboriosam aut necessitatibus officia
          itaque? Earum aut eligendi rem placeat aspernatur optio quasi illo
          culpa iure delectus neque, laudantium architecto magnam ratione
          tempore est facilis ex sint, amepora facere maxime voluptate in
          maiores molestiae similique quos nulla inventore quibusdam praesentium
          molestias aliquam labore ut odit quod voluptatibus eum accusamus.
        </p>
      </div>
    </Collapsible>

    <button @click="collapsibleIsOpen = !collapsibleIsOpen">
      Trigger collapsible programatically
    </button>

    <Collapsible
      class="example-collapsible"
      :isOpen="collapsibleIsOpen"
      :onCollapse="handleCollapse"
    >
      <div slot="trigger">
        <div class="customTrigger">
          <h2>Custom open trigger element</h2>
          <Icon />
        </div>
      </div>

      <div slot="closedTrigger">
        <div class="customTrigger">
          <h2>Custom closed trigger element</h2>
          <Icon />
        </div>
      </div>

      <div id="example2">
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Amet nesciunt
          neque rem at corporis deserunt fugiat? Amet placeat ab commodi culpa.
          Optio voluptatem aperiam atque aut omnis odio tenetur esse nostrum
          quod culpa. Consequatur accusamus illum temporibus earum. Laudantium
          aliquam culpa expedita, animi facere dolorem explicabo quasi
          excepturi? Illo unde nostrum sint odit officiis molestiae ad omnis
          dolores suscipit labore, odio laboriosam aut necessitatibus officia
          itaque? Earum aut eligendi rem placeat aspernatur optio quasi illo
          culpa iure delectus neque, laudantium architecto magnam ratione
          tempore est facilis ex sint, amepora facere maxime voluptate in
          maiores molestiae similique quos nulla inventore quibusdam praesentium
          molestias aliquam labore ut odit quod voluptatibus eum accusamus.
        </p>
      </div>
    </Collapsible>
  </div>
</template>

<script>
import Collapsible from './components/Collapsible.vue';
import Icon from './components/Icon';

export default {
  name: 'App',
  data() {
    return {
      collapsibleIsOpen: false,
    };
  },
  methods: {
    handleCollapse(open) {
      this.collapsibleIsOpen = open;
    },
  },
  components: {
    Collapsible,
    Icon,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: left;
  color: #2c3e50;
  margin-top: 60px;
  max-width: 1024px;
  margin-left: auto;
  margin-right: auto;
}

*,
*::after,
*::before {
  box-sizing: border-box;
}

.example-collapsible {
  margin: 30px 0;
}

.example-collapsible .Collapsible__contentInner {
  padding: 20px;
}

.example-collapsible .Collapsible__trigger {
  padding: 10px 20px;
  border: 2px solid aquamarine;
}
.example-collapsible .Collapsible__trigger {
  padding: 10px 20px;
  border: 2px solid aquamarine;
}

.example-collapsible .Collapsible__content {
  border: 2px solid aquamarine;
  border-top: 0;
}

.example-collapsible .Collapsible__content--closed {
  border: 0;
}

.customTrigger {
  display: grid;
  grid-template-columns: auto 20px;
  align-items: center;
}

.customTrigger svg {
  display: block;
  width: 100%;
  height: auto;
}

.customTrigger h2 {
  margin: 0;
  font-size: 16px;
}
</style>
