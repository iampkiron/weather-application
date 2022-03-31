<template>
  <div>
    <ul class="city-selector">
      <li
        @click="selectCity(city)"
        :class="{ isSelected: city.selected }"
        v-for="city in cities"
        :key="city.code"
      >
        {{ city.label }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "citySelector",
  data() {
    return {
      cities: [
        { code: "SEOUL", label: "서울", selected: false },
        { code: "TOKYO", label: "도쿄", selected: false },
      ],
    };
  },
  methods: {
    selectCity(city) {
      city.selected = !city.selected;
      this.$emit("selectCity", city);
    },
  },
};
</script>

<style scoped>
.city-selector {
  display: grid;
  grid-template-columns: repeat(5, 1fr);
}
.city-selector li {
  display: flex;
  justify-content: center;
  align-items: center;
  border: 0.05em solid #dfe4ea;
  padding: 0.3em;
  cursor: pointer;
}
.isSelected {
  background: #dfe4ea;
}
</style>
