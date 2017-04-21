Cacao Respuestas 
===============

Cacao Respuestas es una instancia de [Askbot](http://askbot.org/) con ciertas modificaciones disponibles en [este repositorio](https://github.com/CacaoMovil/askbot-devel)

## Como agregar un backend SMS.

Para crear un nuevo backend SMS se debe de agregar una nueva clase que herede de BaseSMSBackend en askbot/utils/sms.py y en esta clase implementar el método *send_sms*.

Posteriormente se tendrá que modificar la funcion *get_sms_backend_client* en el mismo archivo para agregar la llamada hacia el backend pertinente.

Finalmente para que el backend nuevo esté disponible en la configuración se debera de modificar el archivo conf/sms.py para incluirlo en la constante *SMS_BACKEND_CHOICES*. 

## Cambios de CSS

```
    .button {
        background-image: none;
        background-color: #B2BB1E;
        border-radius: 0;
        box-shadow: none;
        text-shadow: 0px 1px 0px rgba(0,0,0,0.5);
        color: #fff;
    }

    .button:hover {
            background-color: #D3D30F;
        background-image: none;
        text-shadow: 0px 1px 0px rgba(255,255,255,1);
        color:#414C00;
    }

    body {
      font-size: 16px;
    }

    #header {
        background: #472A2B;
    }

    #userToolsNav a {
        color: #E7A614;
    }

    #metaNav a {
        color: #E7A614;
    }

    .js-tag {
        margin: 0;
        padding: 0;
        height: auto;
    }

    .js-tag-name {
            background: #eee;
        border: 0;
        border-top: 0;
        outline: 0 !important;
        -webkit-box-shadow: none;
        -moz-box-shadow: none;
        box-shadow: none;
        padding: 5px 10px;
        height: auto;
    }

    ul.tags li {
        margin: 0 5px 5px 0;
        height:auto;
    }

    .short-summary .userinfo {
        padding-bottom: 10px;
        padding-top: 10px;
    }
    .ribbonwrap {
        height: 10px;
        margin-bottom: 20px;
    }
    .ribbon {
        width: 20%;
        float: left;
        height: 100%;
    }
    .grn {
        background: #B2BB1E;
    }
    .bwn {
        background: #472A2B;
    }
    .ylw {
        background: #E7A614;
    }
    .red {
        background: #7C0040;
    }
    .teal {
        background: #00A389;
    }
    #ground {
            background: #472A2B;
            border-top: 0;
        padding: 0;
    }
    #secondaryHeader {
        margin-bottom: 0;
    }

    .tabBar {
        font-size: 16px;
            background-color: #eee;
    }
    .logowrap {
        background: #fff;
        padding: 20px 0;
    }
    #questionCount {
        color: #00A389;
    }
    .short-summary {
            padding: 20px 0 10px 0;
    }

    .short-summary h2 {
        font-size: 22px;
        position:relative;
    }

    .box .contributorback {
        background: transparent;
    }

    .box h2 {
        background: transparent;
        color: #7C0040;
        border-bottom: 3px solid #E7A614;
    }

    #metaNav #navBadges {
        display: none;
    }
    .short-summary .votes, .short-summary .answers, .short-summary .favorites, .short-summary .views {
        margin: 0 5px;
        padding: 10px;
        width: 50px;
        height: 50px;
        border: 0;
    }

    .short-summary h2:before {
            content: "\f059";
        font-family: FontAwesome;
        color: #B2BB1E;
        padding-right: 10px;
    }
    .votes.no-votes {
        background: #E6F6F3;
    }
    .answers.no-answers {
        background: #FDF6E8;
    }
    .views.no-views {
        background: #F2E6EC;
    }
    .votes.some-votes {
        background: #00A389;
    }
    .answers.some-answers {
        background: #E7A614;
    }
    .views.some-views {
        background: #7C0040;
    }

    .some-views span, .some-votes span, .some-answers span, .some-views div, .some-votes div, .some-answers div {
        color:#fff !important;
    }

    body.lang-es .short-summary .counts .answers div, body.lang-es .short-summary .counts .views div, body.lang-es .short-summary .counts .votes div {
        font-size: 12px;
    }

    .copyright {
        color:#7E696A;
    }

    .footer-links a {
        color:#E7A614;
    }

    .powered-link a, .copyright a {
        color:#B2BB1E;
    }

    body {
      font-family: 'Lato', sans-serif;
    }

    input, select, textarea {
      font-family: Trebuchet MS, "segoe ui", Helvetica, Tahoma, Verdana, MingLiu, PMingLiu, 'Lato', sans-serif, sans-serif;
    }

    /* ----- Notify message bar , check blocks/system_messages.html ----- */
    .notify {
      font-family: 'Oswald', sans-serif;
    }
    /* ----- Header, check blocks/header.html ----- */
    #header {
      font-family: 'Oswald', sans-serif;
    }
    #secondaryHeader {
      font-family: 'Oswald', sans-serif;
    }

    #searchBar input.searchInput {
      font-family: 'Lato', sans-serif;
    }

    button,
    input[type="submit"],
    input[type="button"],
    input[type="reset"],
    .button,
    .btn {
      font-family: 'Oswald', sans-serif;
    }

    /* ----- Sidebar Widgets Box, check main_page/sidebar.html or question/sidebar.html ----- */
    .box p {
      font-family: 'Oswald', sans-serif;
    }

    .box h2 {
      font-family: 'Oswald', sans-serif;
    }
    .box h3 {
      font-family: 'Oswald', sans-serif;
    }

    .box label {
      font-family: 'Oswald', sans-serif;
    }

    .box .js-question-follower-count {
      font-family: 'Lato', sans-serif;
    }

    /* ----- Sorting top Tab, check main_page/tab_bar.html ------*/
    .tabBar {
      font-family: 'Lato', sans-serif;
    }
    .rss {
      font-family: 'Lato', sans-serif;
    }
    /* ----- Headline, containing number of questions and tags selected, check main_page/headline.html ----- */
    #questionCount {
      font-family: 'Oswald', sans-serif;
    }
    #listSearchTags {
      font-family: 'Oswald', sans-serif;
    }
    .search-tips {
      font-family: 'Oswald', sans-serif;
    }

    .short-summary h2 {
      font-family: 'Oswald', sans-serif;
    }
    .short-summary .userinfo {
      font-family: 'Lato', sans-serif;
    }

    .short-summary .counts {
      font-family: 'Oswald', sans-serif;
    }
    .short-summary .counts .item-count {
      font-family: 'Oswald', sans-serif;
    }

    .js-tag-name {
      font-family: 'Lato', sans-serif;
    }

    .js-delete-icon {
      font-family: 'Lato', sans-serif;
    }

    /* ----- Ask and Edit Question Form template----- */
    .section-title {
      font-family: 'Oswald', sans-serif;
    }
    .wmd-preview {
      font-family: 'Lato', sans-serif;
    }

    .question-page h1 {
      font-family: 'Oswald', sans-serif;
    }
    .question-page p.rss a {
      font-family: 'Oswald', sans-serif;
    }
    .question-page .post-body {
      font-family: 'Lato', sans-serif;
    }

    .question-page .post-update-info {
      font-family: 'Lato', sans-serif;
    }

    .question-page .post-controls a, .question-page .post-controls span.dropdown-toggle {
      font-family: 'Lato', sans-serif;
    }

    .question-page .post-controls .answer-convert input, .question-page .answer-controls .answer-convert input {
      font-family: 'Lato', sans-serif;
    }

    .question-page #questionCount {
      font-family: 'Oswald', sans-serif;
    }
    .question-page h2.comment-title {
      font-family: 'Oswald', sans-serif;
    }
    .question-page .comments .controls a {
      font-family: 'Lato', sans-serif;
    }
    .question-page .comments textarea {
      font-family: 'Lato', sans-serif;
    }

    .question-page .comments .counter {
      font-family: 'Lato', sans-serif;
    }
    .question-page .comments .comment {
      font-family: 'Lato', sans-serif;
    }

    .question-page .comments .convert-comment input {
      font-family: 'Lato', sans-serif;
    }

    .question-page #fmanswer h2 {
      font-family: 'Oswald', sans-serif;
    }
    .vote-number {
      font-family: 'Oswald', sans-serif;
    }
    .count {
      font-family: 'Oswald', sans-serif;
    }
    .scoreNumber {
      font-family: 'Oswald', sans-serif;
    }
    .vote-count {
      font-family: 'Lato', sans-serif;
    }
    .revision h3 {
      font-family: 'Oswald', sans-serif;
    }
    /* ----- Red Popup notification ----- */
    .vote-notification {
      font-family: 'Lato', sans-serif;
    }
    /* ----- Footer links , check blocks/footer.html----- */
    #ground {
      font-family: 'Oswald', sans-serif;
    }
    .tag-subscriptions .action {
      font-family: 'Oswald', sans-serif;
    }
    /*!
     *  Font Awesome 4.3.0 by @davegandy - http://fontawesome.io - @fontawesome
     *  License - http://fontawesome.io/license (Font: SIL OFL 1.1, CSS: MIT License)
     */
    /* FONT PATH
     * -------------------------- */
    @font-face {
      font-family: 'FontAwesome';
      src: url('/m/default/media/fa-4.3.0/fonts/fontawesome-webfont.eot?v=4.3.0&fd07a52ab766');
      src: url('/m/default/media/fa-4.3.0/fonts/fontawesome-webfont.eot?&fd07a52ab766#iefix&v=4.3.0') format('embedded-opentype'), url('/m/default/media/fa-4.3.0/fonts/fontawesome-webfont.woff2?v=4.3.0&fd07a52ab766') format('woff2'), url('/m/default/media/fa-4.3.0/fonts/fontawesome-webfont.woff?v=4.3.0&fd07a52ab766') format('woff'), url('/m/default/media/fa-4.3.0/fonts/fontawesome-webfont.ttf?v=4.3.0&fd07a52ab766') format('truetype'), url('/m/default/media/fa-4.3.0/fonts/fontawesome-webfont.svg?v=4.3.0&fd07a52ab766#fontawesomeregular') format('svg');
      font-weight: normal;
      font-style: normal;
    }

    .navbar-search .search-query {
      font-family: "Helvetica Neue", Helvetica, 'Lato', sans-serif, sans-serif;
    }

```
