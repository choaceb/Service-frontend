<template>
  <div class="chatbot-button">
    <a href="">
      <img
        src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAJAAAACQCAYAAADnRuK4AAAAAXNSR0IArs4c6QAAAERlWElmTU0AKgAAAAgAAYdpAAQAAAABAAAAGgAAAAAAA6ABAAMAAAABAAEAAKACAAQAAAABAAAAkKADAAQAAAABAAAAkAAAAAA/PwqIAAAITElEQVR4Ae2da4hVVRTHHSujyMrsIQY1ZIWWWVr2LinKtBchYvQy+lCRX6LoW30qxS9RIUUPqSSKwkLTniAlPRAjzaInmB8mwkgdy0eSpk6/pXdg5s49d849d+199733v2Exc8/ee+21fuc/++x7zr53hgxREQEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAERSI1AR2oBDRZPT0/PKbS5HBuHnVGykfw8ChuODcNSLnsIbie2A+vGfsXWYz9jX3Z0dHTxs2lK8gJCMIdC8xpsFnYV1om1cjEBrcQWYysQ1N6Uk01WQAjnNMA9iN2OHZ8yxICxbcH3W9gzCGlDwHEKu05OQAhnAtk8hs3ADimcWWt13E86S7B5COnblFJLRkAIx2aZudi92NCUICUUiwnpZexRhLQ5hbiSEBDiuQUYr2LHpgClCWLYRoz3IKKljY61oX/pCGcoNg8INj1LPPnVcIwxg918Y5i/m3/Lhs1AJH4c6byJTfVPq608riDb25iN7JZA9NIQASGeiWRqs05n9Ixbc8Au0pqBiL6JnV50ASGes0hyFWbTsIofAVsXXYaIfvRzObinqAJCPCcR0mqsc/DQ1KIAAZuJLkJEfxboW6hLtAUY4jmCCJdjnYUiVac8BE6l0XuwPjJPY482UQREQjbO69iFHkHLR1UCk6l9o8S8akOPyigCItDHMbuzrBKHgN1XeyLGUMHXQPwlnEciX2P2UFQlHoF9DDWZ9dC6kEMGnYEQjz3LWohJPCHPYmXfB9iXzkHlFg5HgwqI+O7ELnCIUy6KETifbncV65qvV7BLWEn5vxDG6flCUatABGwbyFguZUH2FYWcge4gcIknkCpqcDuGtranKkgJKaAHgkQsp0UIBDsXQS5hXL7GkqXt8VVJh8A4LmO2pHAtoWag2a5RypkHgSDnJJSApnlkLB+uBKa7eis5c7+EcfmyrambMHffIQC0kc8ecj2Ry5ht1HcrIWagKUQn8bidIjdHdk7s3LiWEAIa7xqhnHkSOMfTmfkKIaBx3kHKnxsBe3fsWkI8ozrTNcLqzv6m+inMNqnZR4UnYXOws7F6yu90fhpbU3JiWyQewk4uvS7643s6PoetxYZjF2OPYLY/PEaJeW6K5cMiuguLUdYwyOjyKDl2OLawjgDep++A7bZ2DPuwDr8v0ndYhXhHcfyrOvzW0rWrfPzkXpPN1loyKth2F/3sixUqFuqGYd8V8L2RPpmzAXUjsT8K+LVYBoinN3jqxmA7C/ittcvW3jG9foZYA9nUHLos4+3o+qxBqLNvwFiQVV/l+Cv0zYRMXTd9F1Xpn1W1oBRTxXrq7IHnsoqVvgfdz00IAYVYV5VjXFt+oMLrPG3Ku+Xp07suKu9b7XUevzE+kuP+RD6EgKqB9Ko7OoejPG3K3eTpk6dNEb/DyzsFeL3d22ezCujSHCDytCl3k6dPnjblfi8pP1DhdZ42FbrVdMjeqaZdal3V1dH+piwS+ByNFVnM76Gf7eGuWKibiFmbWovFMrqiUw5SN71WhwXbf54VQ9HjzToDWb6LgDijPHGO2T2gD7AR5XU5Xh9Gm6X4uKK8LceutDrM2tRaLBa7PWCfyu1XOHYzB17rdzDcC/ftHO7PrABiD+1illUMZjcSd2KTsKlY5ltm6vIU+x6eT7HeBbPdSLwaq5fXbnx8jNmi2tY8diNxgFg5Fqo8zDs+u0HqVuoFMiCQBghoQAw6kElgCgJyvYxJQJmsW67iHzIagYD+88ysmddAnhzawddn3uIxaBJQO0jnYI72BsC96BLmjjRJh7uIahQzkPt9IM1ASZ5v96DeDiEei1IzkPu5Ss6h3VY5FwHZXiT3ohnIHWlyDt8JJR7LVDNQcufbNSB7+m6zz0+uXvs40wzUB0YL/vpkSPEYL81ALaiaUkq24W4CAvo3ZIqagULSbZxvey54a2jxWHoSUONOcqiR9+F4FuJZF2qAvn4loL40WuP3OYjno1ipSECxSMcZZz7ieSnOUAdH0SI6Ju2wYy3E/f0IKOp+LM1AYU9qDO+2Sc2Ec19s8VhyMT6CEwNiu47RReIzEU7vzsnoHDQDRUfuNqAtlCc1UjyWiQTkdj6jOdrCSPYFEjcgnq3RRs0YSJewDDAJHrYtqc9jcxHOtlTik4BSORPZcWyk6lnsBYTzV3azxtRIQI3hPtio3TRYgi3GViIcu7ucZJGAGn9a7PPqGzD7Xm37jNsX2A+Ixj6blnxpZgH9Bl17+2rgbTFp07uZ7f9Nudh9G1vP2APPboSyOeVgB4utmQRkX2f3LmZT++pmBz/YiWnbevtkqmPZj69l2I1YvR9Xbttz0lSJO4lnL37s/36Ob6rkFWz9BBwEtBIf7l9HW39m8hCFQB0C2kTf2VGC1CDpEigooE/od0K6WSmyaARqFJAtkudj9g9iVUTgwNe15dXQbhrOFDMR6Ecgp3rsi8Kn9euoFyJgBHIIaAdt3P/tkOi3CAHEYZemrGL3d65vkVSVRggCCKTaPw6xjVAqIpBNAAFdlzH9zM3upRoR6EMAAV2LrcK2Y6uxu/tU61cREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAERcCXwP6RdxSpH8+94AAAAAElFTkSuQmCC"
      />
    </a>
  </div>
</template>
<script>
export default {
  name: 'ChabotButton',
  props: {},
  data: function() {
    return {
      buttonActive: false,
      IMG_SRC:
        'data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAJAAAACQCAYAAADnRuK4AAAAAXNSR0IArs4c6QAAAERlWElmTU0AKgAAAAgAAYdpAAQAAAABAAAAGgAAAAAAA6ABAAMAAAABAAEAAKACAAQAAAABAAAAkKADAAQAAAABAAAAkAAAAAA/PwqIAAAITElEQVR4Ae2da4hVVRTHHSujyMrsIQY1ZIWWWVr2LinKtBchYvQy+lCRX6LoW30qxS9RIUUPqSSKwkLTniAlPRAjzaInmB8mwkgdy0eSpk6/pXdg5s49d849d+199733v2Exc8/ee+21fuc/++x7zr53hgxREQEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAERSI1AR2oBDRZPT0/PKbS5HBuHnVGykfw8ChuODcNSLnsIbie2A+vGfsXWYz9jX3Z0dHTxs2lK8gJCMIdC8xpsFnYV1om1cjEBrcQWYysQ1N6Uk01WQAjnNMA9iN2OHZ8yxICxbcH3W9gzCGlDwHEKu05OQAhnAtk8hs3ADimcWWt13E86S7B5COnblFJLRkAIx2aZudi92NCUICUUiwnpZexRhLQ5hbiSEBDiuQUYr2LHpgClCWLYRoz3IKKljY61oX/pCGcoNg8INj1LPPnVcIwxg918Y5i/m3/Lhs1AJH4c6byJTfVPq608riDb25iN7JZA9NIQASGeiWRqs05n9Ixbc8Au0pqBiL6JnV50ASGes0hyFWbTsIofAVsXXYaIfvRzObinqAJCPCcR0mqsc/DQ1KIAAZuJLkJEfxboW6hLtAUY4jmCCJdjnYUiVac8BE6l0XuwPjJPY482UQREQjbO69iFHkHLR1UCk6l9o8S8akOPyigCItDHMbuzrBKHgN1XeyLGUMHXQPwlnEciX2P2UFQlHoF9DDWZ9dC6kEMGnYEQjz3LWohJPCHPYmXfB9iXzkHlFg5HgwqI+O7ELnCIUy6KETifbncV65qvV7BLWEn5vxDG6flCUatABGwbyFguZUH2FYWcge4gcIknkCpqcDuGtranKkgJKaAHgkQsp0UIBDsXQS5hXL7GkqXt8VVJh8A4LmO2pHAtoWag2a5RypkHgSDnJJSApnlkLB+uBKa7eis5c7+EcfmyrambMHffIQC0kc8ecj2Ry5ht1HcrIWagKUQn8bidIjdHdk7s3LiWEAIa7xqhnHkSOMfTmfkKIaBx3kHKnxsBe3fsWkI8ozrTNcLqzv6m+inMNqnZR4UnYXOws7F6yu90fhpbU3JiWyQewk4uvS7643s6PoetxYZjF2OPYLY/PEaJeW6K5cMiuguLUdYwyOjyKDl2OLawjgDep++A7bZ2DPuwDr8v0ndYhXhHcfyrOvzW0rWrfPzkXpPN1loyKth2F/3sixUqFuqGYd8V8L2RPpmzAXUjsT8K+LVYBoinN3jqxmA7C/ittcvW3jG9foZYA9nUHLos4+3o+qxBqLNvwFiQVV/l+Cv0zYRMXTd9F1Xpn1W1oBRTxXrq7IHnsoqVvgfdz00IAYVYV5VjXFt+oMLrPG3Ku+Xp07suKu9b7XUevzE+kuP+RD6EgKqB9Ko7OoejPG3K3eTpk6dNEb/DyzsFeL3d22ezCujSHCDytCl3k6dPnjblfi8pP1DhdZ42FbrVdMjeqaZdal3V1dH+piwS+ByNFVnM76Gf7eGuWKibiFmbWovFMrqiUw5SN71WhwXbf54VQ9HjzToDWb6LgDijPHGO2T2gD7AR5XU5Xh9Gm6X4uKK8LceutDrM2tRaLBa7PWCfyu1XOHYzB17rdzDcC/ftHO7PrABiD+1illUMZjcSd2KTsKlY5ltm6vIU+x6eT7HeBbPdSLwaq5fXbnx8jNmi2tY8diNxgFg5Fqo8zDs+u0HqVuoFMiCQBghoQAw6kElgCgJyvYxJQJmsW67iHzIagYD+88ysmddAnhzawddn3uIxaBJQO0jnYI72BsC96BLmjjRJh7uIahQzkPt9IM1ASZ5v96DeDiEei1IzkPu5Ss6h3VY5FwHZXiT3ohnIHWlyDt8JJR7LVDNQcufbNSB7+m6zz0+uXvs40wzUB0YL/vpkSPEYL81ALaiaUkq24W4CAvo3ZIqagULSbZxvey54a2jxWHoSUONOcqiR9+F4FuJZF2qAvn4loL40WuP3OYjno1ipSECxSMcZZz7ieSnOUAdH0SI6Ju2wYy3E/f0IKOp+LM1AYU9qDO+2Sc2Ec19s8VhyMT6CEwNiu47RReIzEU7vzsnoHDQDRUfuNqAtlCc1UjyWiQTkdj6jOdrCSPYFEjcgnq3RRs0YSJewDDAJHrYtqc9jcxHOtlTik4BSORPZcWyk6lnsBYTzV3azxtRIQI3hPtio3TRYgi3GViIcu7ucZJGAGn9a7PPqGzD7Xm37jNsX2A+Ixj6blnxpZgH9Bl17+2rgbTFp07uZ7f9Nudh9G1vP2APPboSyOeVgB4utmQRkX2f3LmZT++pmBz/YiWnbevtkqmPZj69l2I1YvR9Xbttz0lSJO4lnL37s/36Ob6rkFWz9BBwEtBIf7l9HW39m8hCFQB0C2kTf2VGC1CDpEigooE/od0K6WSmyaARqFJAtkudj9g9iVUTgwNe15dXQbhrOFDMR6Ecgp3rsi8Kn9euoFyJgBHIIaAdt3P/tkOi3CAHEYZemrGL3d65vkVSVRggCCKTaPw6xjVAqIpBNAAFdlzH9zM3upRoR6EMAAV2LrcK2Y6uxu/tU61cREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAEREAERcCXwP6RdxSpH8+94AAAAAElFTkSuQmCC'
    };
  },
  created: function() {
    window.addEventListener('scroll', this.removeButton);
  },
  methods: {
    // removeButton() {
    //   const scrollY = window.screenY;
    //   return (this.buttonActive = !this.buttonActive);
    // }
  }
};
</script>
<style scoped lang="scss">
.chatbot-button {
  background-color: black;
  border-radius: 100%;
  padding: 1px;

  a {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 52px;
    height: 52px;
    img {
      width: 75%;
    }
  }
}
</style>
