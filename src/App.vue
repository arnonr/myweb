<template>
  <div id="div-body" :style="styleBody">
    <div id="head">
      <nav class="navbar navbar-expand-lg navbar-dark fixed-top" id="mainNav">
        <div class="container">
          <a class="navbar-brand" href="#page-top"
            ><img src="@/assets/img/logos/logo-1.png" alt="กรมสุขภาพจิต" /><img
              src="@/assets/img/logos/logo-2.png"
              alt="..."
              class="logo-name"
          /></a>

          <button
            class="navbar-toggler"
            type="button"
            data-bs-toggle="collapse"
            data-bs-target="#navbarResponsive"
            aria-controls="navbarResponsive"
            aria-expanded="false"
            aria-label="Toggle navigation"
          >
            Menu
            <i class="fas fa-bars ms-1"></i>
          </button>
          <div class="collapse navbar-collapse" id="navbarResponsive">
            <ul class="navbar-nav text-uppercase ms-auto py-4 py-lg-0">
              <li class="nav-item">
                <router-link to="/" class="nav-link" style="cursor: pointer"
                  >หน้าหลัก</router-link
                >
              </li>
              <li class="nav-item">
                <a class="nav-link" href="#services">บริการ</a>
              </li>
              <li class="nav-item">
                <a class="nav-link" href="#portfolio">ข่าวประชาสัมพันธ์</a>
              </li>
              <li class="nav-item">
                <a class="nav-link" href="#team">กัญชาทางการแพทย์</a>
              </li>
              <li class="nav-item">
                <router-link
                  to="/document"
                  class="nav-link"
                  style="cursor: pointer"
                  >แบบฟอร์ม</router-link
                >
              </li>
              <li class="nav-item">
                <router-link
                  to="/about"
                  class="nav-link"
                  style="cursor: pointer"
                  >เกี่ยวกับเรา</router-link
                >
              </li>
              <li class="nav-item">
                <!-- <a class="nav-link" href="#contact">ติดต่อเรา</a> -->

                <router-link
                  to="/contact"
                  class="nav-link"
                  style="cursor: pointer"
                  >ติดต่อเรา</router-link
                >
              </li>
            </ul>
          </div>
        </div>
      </nav>
    </div>
    <router-view />

    <!-- Footer-->
    <footer class="footer py-4 bg-primary">
      <div class="container">
        <div class="row align-items-center">
          <div class="col-lg-4 text-lg-start text-white">
            Copyright &copy; 2023. ศูนย์สุขภาพจิตที่ 6
          </div>
          <div class="col-lg-4 my-3 my-lg-0">
            <a
              class="btn btn-light btn-social mx-2"
              href="#!"
              aria-label="Twitter"
              ><i class="fab fa-twitter"></i
            ></a>
            <a
              class="btn btn-light btn-social mx-2"
              href="#!"
              aria-label="Facebook"
              ><i class="fab fa-facebook-f"></i
            ></a>
            <a
              class="btn btn-light btn-social mx-2"
              href="#!"
              aria-label="LinkedIn"
              ><i class="fab fa-linkedin-in"></i
            ></a>
          </div>
          <div class="col-lg-4 text-lg-end">
            <!-- <a class="link-dark text-decoration-none me-3 text-white" href="#!"
              >Privacy Policy</a
            >
            <a class="link-dark text-decoration-none text-white" href="#!"
              >Terms of Use</a
            > -->
            <button class="btn-xs ml-3" @click="toggleBody()">grayscale</button>
          </div>

          
        </div>
      </div>
    </footer>
  </div>
</template>

<script>
import { defineComponent, onMounted,ref } from "vue";
export default defineComponent({
  name: "App",
  setup() {
    const styleBody = ref("");

    onMounted(() => {
        if (localStorage.getItem("styleBody") === null) {
            localStorage.setItem("styleBody", '')
        }else{
            styleBody.value = localStorage.getItem("styleBody");
        }
    });

    const toggleBody = () => {
        if (localStorage.getItem("styleBody") == '') {
            localStorage.setItem("styleBody", 'filter: grayscale(100%);')
            styleBody.value = 'filter: grayscale(100%);';
        }else{
            localStorage.setItem("styleBody", '')
            styleBody.value = '';
        }
    }
    

    return {
        toggleBody,
        styleBody
    };
  },
});
</script>

<style>
#app {
  font-family: Prompt, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  /* margin-top: 60px; */
}

</style>
