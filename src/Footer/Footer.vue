<template>
  <div class="Footer">

    <div class="LogoContainer">
      <a href="#Intro" class="LogoLink">
        <Logo
          :size="150" />
      </a>
    </div>

    <div class="SocialLinks">
      <a class="SocialIcon Icon-Github" href="https://github.com/JSConfArmenia/" target="_blank"></a>
      <a class="SocialIcon Icon-Facebook" href="https://www.facebook.com/jsconf.am/" target="_blank"></a>
      <a class="SocialIcon Icon-Twitter" href="https://twitter.com/JSConfAM" target="_blank"></a>
      <a class="SocialIcon Icon-Instagram" href="https://www.instagram.com/jsconf.am/" target="_blank"></a>
      <a class="SocialIcon Icon-YouTube" href="https://www.youtube.com/channel/UCkzEOKU959F6_T0OaQBH4VQ/featured" target="_blank"></a>
      <a class="SocialIcon Icon-Telegram" href="https://t.me/jsconfarmenia" target="_blank"></a>
    </div>

    <!-- <div class="PressRelease">
      Press Release
      <a href="/Press-Release-EN.pdf" target="_blank">En</a> |
      <a href="/Press-Release-AM.pdf" target="_blank">Am</a>
    </div> -->

    <p class="Credits">
      Coded in Vue.js by <a href="https://github.com/modularcoder" target="_blank">@modularcoder</a> and
      <a href="https://github.com/JSConfArmenia/conf-21/graphs/contributors" target="_blank">others</a>.
    </p>

    <div class="FooterBgLeft"></div>
  </div>
</template>

<script>
import Logo from '../_common/Logo/Logo.vue';

export default {
  components: {
    Logo,
  },
};
</script>

<style scoped lang="scss">
.Footer {
  min-height: 600px;
  display: flex;
  align-items: center;
  justify-content: flex-end;
  flex-direction: column;
  position: relative;
}

.FooterBgLeft {
  position: absolute;
  left: 0;
  bottom: 0;
  width: 100%;
  height: 100%;
  background-image: url('./FooterBgLeft.svg');
  background-repeat: no-repeat;
  background-size: cover;
  z-index: -1;
}

.LogoContainer {
  margin: 20px 0;
}

.SocialLinks {
  display: flex;
  margin-bottom: 15px;
}

.SocialIcon {
  background: center;
  width: 32px;
  height: 32px;
  margin: 3px;
  padding: 5px;
  background-repeat: no-repeat;
  background-size: 20px;
  background-position: center;
  display: block;
  position: relative;
  overflow: hidden;

  &:after {
    content: " ";
    display: block;
    background-color: #91919145;
    position: absolute;
    transition: all .2s ease;
    top: 100%;
    left: 0;
    width: 100%;
    height: 100%;
  }

  &.active,
  &:hover {
    &:after {
      top: 0;
    }
  }
}

.Icon-Github {
  background-image: url('./github.png');
}

.Icon-Twitter {
  background-image: url('./twitter.png');
}

.Icon-Facebook {
  background-image: url('./facebook.png');
  background-size: 12px;
}

.Icon-Instagram {
  background-image: url('./instagram.png');
}

.Icon-YouTube {
  background-image: url('./youtube.png');
}

.Icon-Telegram {
  background-image: url('./telegram.png');
}
.Credits {
  margin: 20px;
  font-size: .8em;
}

a:not(.LogoLink):not(.SocialIcon) {
  text-decoration: underline;
  color: inherit;
  font-weight: bold;
}

@media (max-width: 500px) {
  .Footer {
    min-height: 500px;
  }

  .FooterBgLeft {
    background-color: #ffe549;
  }
}

</style>
