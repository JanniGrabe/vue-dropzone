<template>
  <aside class="sidebar">
    <h1>
      <a class="app-name-link" data-nosearch="" href="/vue-dropzone/docs/dist/"><img :src="require('../assets/vue2-dropzone1.png').default"></a>
    </h1>

    <hr class="border">
    <div class="sidebar-nav">
      <ul>
        <li v-for="section in sections" :key="section.title">
          <p>{{ section.title}}</p>
          <ul>
            <router-link v-for="page in section.pages" :to="page.to" active-class="active" :key="page.title">
              <li>
                <a>{{page.title}}</a>
              </li>
            </router-link>
          </ul>
        </li>
        <li>
          <a href="https://github.com/rowanwins/vue-dropzone">
            <button class="sideBtn github">
              <i class="fa fa-github fa-2x" aria-hidden="true"></i>
              <span>GITHUB</span>
            </button>
          </a>
        </li>
        <li>
          <a href="https://www.worldvision.com.au/give/donate/make-a-general-donation">
            <img src="https://www.dropbox.com/s/f6086lensozvp9i/cause.jpg?dl=1">
          </a>
        </li>
      </ul>
    </div>
  </aside>
</template>

<script>
export default {
  data() {
    return {
      sections: [
        {
          title: 'Getting started',
          pages: [{ to: 'installation', title: 'Installation & Usage' }]
        },
        {
          title: 'Documentation',
          pages: [
            { to: '/props', title: 'Props' },
            { to: '/events', title: 'Events' },
            { to: '/methods', title: 'Methods' }
          ]
        },
        {
          title: 'Demos',
          pages: [
            { to: '/demo', title: 'Basic Demo' },
            { to: '/iconDemo', title: 'Adding Icons' },
            { to: '/custom-html', title: 'Custom HTML via Slots' },
            { to: '/manual', title: 'Manually Load Files' },
            { to: '/additionalParams', title: 'Sending Additional Params' },
            { to: '/custom-preview', title: 'Custom Styling' },
            { to: '/aws-s3-upload', title: 'AWS S3 Upload' }
          ]
        }
      ]
    };
  }
};
</script>

<style>
.border {
  border: none;
  border-bottom: 1px solid rgba(0, 0, 0, 0.07);
}

.sidebar li {
  margin: 2px 0 2px 15px;
}

.sideBtn {
  cursor: pointer;
  transition: 0.3s;
  padding: 10px;
  margin: 20px 0px;
}

.github {
  background: #747b8b;
  padding: 10px 48px;
  margin: 40px 0px;
}

.github:hover {
  background: #00b782;
}

.sidebar .sideBtn a {
  color: white;
  letter-spacing: 0.1rem;
}

.cause .sideBtn a {
  font-weight: 500;
}

.sidebar .github a {
  font-weight: 700;
}

.sidebar .sideBtn a:hover {
  text-decoration: none;
}

.fa {
  vertical-align: middle;
  margin-right: 10px;
}

.center-c {
  display: flex;
  align-items: center;
  justify-content: center;
}
</style>
