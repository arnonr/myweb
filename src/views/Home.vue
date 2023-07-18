<template>
  <div class="home">
    <!-- Masthead-->
    <header class="masthead">
      <div class="container">
        <div class="masthead-subheading">ศูนย์สุขภาพจิตที่ 6</div>
        <div class="masthead-heading text-uppercase">.......</div>
        <a class="btn btn-success btn-xl text-uppercase" href="#services"
          >บริการประชาชน</a
        >
      </div>
    </header>

    <!-- Services-->
    <section class="page-section" id="services">
      <div class="container">
        <div class="text-center">
          <h2 class="section-heading text-uppercase">บริการ</h2>
          <h3 class="section-subheading text-muted">
            Lorem ipsum dolor sit amet consectetur.
          </h3>
        </div>
        <div class="row text-center">
          <div class="col-md-4">
            <span class="fa-stack fa-4x">
              <i class="fas fa-circle fa-stack-2x text-primary"></i>
              <i class="fas fa-shopping-cart fa-stack-1x fa-inverse"></i>
            </span>
            <h4 class="my-3">ให้คำปรึกษา</h4>
            <p class="text-muted">
              Lorem ipsum dolor sit amet, consectetur adipisicing elit. Minima
              maxime quam architecto quo inventore harum ex magni, dicta
              impedit.
            </p>
          </div>
          <div class="col-md-4">
            <span class="fa-stack fa-4x">
              <i class="fas fa-circle fa-stack-2x text-danger"></i>
              <i class="fas fa-laptop fa-stack-1x fa-inverse"></i>
            </span>
            <h4 class="my-3">ตรวจสุขภาพจิตใจ</h4>
            <p class="text-muted">
              Lorem ipsum dolor sit amet, consectetur adipisicing elit. Minima
              maxime quam architecto quo inventore harum ex magni, dicta
              impedit.
            </p>
          </div>
          <div class="col-md-4">
            <span class="fa-stack fa-4x">
              <i class="fas fa-circle fa-stack-2x text-success"></i>
              <i class="fas fa-lock fa-stack-1x fa-inverse"></i>
            </span>
            <h4 class="my-3">ติชม</h4>
            <p class="text-muted">
              Lorem ipsum dolor sit amet, consectetur adipisicing elit. Minima
              maxime quam architecto quo inventore harum ex magni, dicta
              impedit.
            </p>
          </div>
        </div>
      </div>
    </section>
    <!-- Portfolio Grid-->
    <section class="page-section bg-light" id="portfolio">
      <div class="container">
        <div class="text-center">
          <h2 class="section-heading text-uppercase">ข่าวประชาสัมพันธ์</h2>
          <h3 class="section-subheading text-muted">
            Lorem ipsum dolor sit amet consectetur.
          </h3>
        </div>
        <div class="row">
          <div class="col-lg-4 col-sm-6 mb-4" v-for="nw in news" :key="nw.id">
            <div class="card">
              <img
                :src="nw.image"
                class="card-img-top"
                alt="..."
                style="height:260px;"
              />
              <div class="card-body text-start" style="min-height:200px">
                <h5 class="card-title">
                  {{ nw.title }}
                </h5>
                <p class="card-text"></p>
                <a href="#!" class="btn btn-info">อ่านต่อ</a>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Team-->
    <section class="page-section bg-light" id="team">
      <div class="container">
        <div class="text-center">
          <h2 class="section-heading text-uppercase">บุคลากร</h2>
          <h3 class="section-subheading text-muted">
            Lorem ipsum dolor sit amet consectetur.
          </h3>
        </div>
        <div class="row">
          <div class="col-lg-4">
            <div class="team-member">
              <img
                class="mx-auto rounded-circle"
                src="@/assets/img/team/1.jpg"
                alt="..."
              />
              <h4>Parveen Anand</h4>
              <p class="text-muted">Lead Designer</p>
              <a
                class="btn btn-dark btn-social mx-2"
                href="#!"
                aria-label="Parveen Anand Twitter Profile"
                ><i class="fab fa-twitter"></i
              ></a>
              <a
                class="btn btn-dark btn-social mx-2"
                href="#!"
                aria-label="Parveen Anand Facebook Profile"
                ><i class="fab fa-facebook-f"></i
              ></a>
              <a
                class="btn btn-dark btn-social mx-2"
                href="#!"
                aria-label="Parveen Anand LinkedIn Profile"
                ><i class="fab fa-linkedin-in"></i
              ></a>
            </div>
          </div>
          <div class="col-lg-4">
            <div class="team-member">
              <img
                class="mx-auto rounded-circle"
                src="@/assets/img/team/2.jpg"
                alt="..."
              />
              <h4>Diana Petersen</h4>
              <p class="text-muted">Lead Marketer</p>
              <a
                class="btn btn-dark btn-social mx-2"
                href="#!"
                aria-label="Diana Petersen Twitter Profile"
                ><i class="fab fa-twitter"></i
              ></a>
              <a
                class="btn btn-dark btn-social mx-2"
                href="#!"
                aria-label="Diana Petersen Facebook Profile"
                ><i class="fab fa-facebook-f"></i
              ></a>
              <a
                class="btn btn-dark btn-social mx-2"
                href="#!"
                aria-label="Diana Petersen LinkedIn Profile"
                ><i class="fab fa-linkedin-in"></i
              ></a>
            </div>
          </div>
          <div class="col-lg-4">
            <div class="team-member">
              <img
                class="mx-auto rounded-circle"
                src="@/assets/img/team/3.jpg"
                alt="..."
              />
              <h4>Larry Parker</h4>
              <p class="text-muted">Lead Developer</p>
              <a
                class="btn btn-dark btn-social mx-2"
                href="#!"
                aria-label="Larry Parker Twitter Profile"
                ><i class="fab fa-twitter"></i
              ></a>
              <a
                class="btn btn-dark btn-social mx-2"
                href="#!"
                aria-label="Larry Parker Facebook Profile"
                ><i class="fab fa-facebook-f"></i
              ></a>
              <a
                class="btn btn-dark btn-social mx-2"
                href="#!"
                aria-label="Larry Parker LinkedIn Profile"
                ><i class="fab fa-linkedin-in"></i
              ></a>
            </div>
          </div>
        </div>
        <div class="row">
          <div class="col-lg-8 mx-auto text-center">
            <p class="large text-muted">
              Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aut
              eaque, laboriosam veritatis, quos non quis ad perspiciatis, totam
              corporis ea, alias ut unde.
            </p>
          </div>
        </div>
      </div>
    </section>
    <!-- Clients-->
    <div class="py-5">
      <div class="container">
        <div class="row align-items-center">
          <div class="col-md-3 col-sm-6 my-3">
            <a href="https://dmh.go.th/"
              ><img
                class="img-fluid img-brand d-block mx-auto"
                src="@/assets/img/logos/logo-1.png"
                alt="..."
                aria-label="Microsoft Logo"
            /></a>
          </div>
          <div class="col-md-3 col-sm-6 my-3">
            <a href="#!"
              ><img
                class="img-fluid img-brand d-block mx-auto"
                src="@/assets/img/logos/logo-2.png"
                alt="..."
                aria-label="Google Logo"
            /></a>
          </div>
          <div class="col-md-3 col-sm-6 my-3">
            <a href="https://dmh.go.th/"
              ><img
                class="img-fluid img-brand d-block mx-auto"
                src="@/assets/img/logos/logo-1.png"
                alt="..."
                aria-label="Microsoft Logo"
            /></a>
          </div>
          <div class="col-md-3 col-sm-6 my-3">
            <a href="#!"
              ><img
                class="img-fluid img-brand d-block mx-auto"
                src="@/assets/img/logos/logo-2.png"
                alt="..."
                aria-label="Google Logo"
            /></a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { defineComponent, ref, onMounted } from "vue";
import axios from "axios";

// export default {
//   name: "homeItem",
// };

export default defineComponent({
  name: "homeItem",
  setup() {
    onMounted(() => {});

    const news = ref([]);

    async function getRandomUser() {
      try {
        const data = await axios.get(
            "https://gnews.io/api/v4/search?q=example&lang=th&country=th&max=6&apikey=748487b92e72ff359748e9454c5363fb"
        //   "https://random-data-api.com/api/v2/users?size=5"
        );
        console.log(data);
        news.value = data.data.articles;
        news.value.forEach((element) => {
          console.log(element.title);
        });
      } catch (err) {
        console.log("error: ", err);
      }
    }

    getRandomUser();

    return {
        news
    };
  },
});
</script>

<style scoped>
header.masthead {
  background-image: url("@/assets/img/header-bg-1.jpg");
}
</style>
