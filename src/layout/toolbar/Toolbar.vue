<template>
  <!--begin::Toolbar-->
  <div class="toolbar py-5 py-lg-15" id="kt_toolbar">
    <!--begin::Container-->
    <div
      id="kt_toolbar_container"
      :class="{
        'container-fluid': toolbarWidthFluid,
        'container-xxl': !toolbarWidthFluid,
      }"
      class="d-flex flex-stack flex-wrap">
      <!--begin::Page title-->

      <!--end::Page title-->

      <!--begin::Actions-->
      <div class="d-flex align-items-center py-3 py-md-1">
        <!--begin::Wrapper-->
        <div class="me-4">
          <!--begin::Menu-->


          <Dropdown1></Dropdown1>
          <!--end::Menu-->
        </div>
        <!--end::Wrapper-->

        <!--begin::Button-->

        <!--end::Button-->
      </div>
      <!--end::Actions-->
    </div>
    <!--end::Container-->
  </div>
  <!--end::Toolbar-->
</template>

<script lang="ts">
import { defineComponent } from "vue";
import Dropdown1 from "@/components/dropdown/Dropdown1.vue";
import { toolbarWidthFluid } from "@/core/helpers/config";

export default defineComponent({
  name: "KToolbar",
  props: {
    breadcrumbs: Array,
    title: String,
  },
  components: {
    Dropdown1,
  },
  setup() {
    return {
      toolbarWidthFluid,
    };
  },
});
</script>
