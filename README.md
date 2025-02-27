<!DOCTYPE html>
<html lang="en">
  <head>

    <meta charset="UTF-8">

    <title>{Title}{block:PostSummary} &mdash; {PostSummary}{/block:PostSummary}</title>

    {block:Description}
    <meta name="description" content="{MetaDescription}">
    {/block:Description}

    <link rel="shortcut icon" href="{Favicon}">
    <link rel="apple-touch-icon" href="{PortraitURL-128}">
    <link rel="alternate" type="application/rss+xml" href="{RSS}">
    <link href='https://fonts.googleapis.com/css?family=Montserrat:400,700' rel='stylesheet' type='text/css'>
    <link href='https://fonts.googleapis.com/css?family=Merriweather:400,700,400italic' rel='stylesheet' type='text/css'>

    <!--[if lt IE 9]>
    <script src="https://html5shim.googlecode.com/svn/trunk/html5.js"></script>
    <![endif]-->

    <!-- Options -->
    <meta name="color:Background" content="#FFFFFF">
    <meta name="color:Body Text" content="#999999">
    <meta name="color:Links" content="#333333">
    <meta name="color:Title" content="#333333">
    <meta name="color:Meta" content="#CCCCCC">
    <meta name="color:Dividers" content="#F2F2F2">
    <meta name="image:Logo" content="">
    <meta name="select:Page Width" content="500px" title="Standard">
    <meta name="select:Page Width" content="700px" title="Wide">
    <meta name="if:Show Date" content="1">
    <meta name="if:Show Note Count" content="1">
    <meta name="if:Infinite Scroll" content="1">
    <meta name="if:Show Like Reblog Buttons" content="1">
    <meta name="text:Google Analytics ID" content="" />

    <style type="text/css">

      html {
        background-color: {color:Background};
            -webkit-font-smoothing: antialiased;
      }
      body {
        color: {color:Body Text};
        font-family: 'Helvetica Neue', "Arial", sans-serif;
        font-size: 12px;
        line-height:1.8em;
      }
      h1, h2, h3, h4, h5 {
        font-family: 'Montserrat', 'Helvetica Neue', "Arial", sans-serif;
        font-weight: 400;
      }
      h1 {
        font-size: 48px;
        line-height: 48px;
      }
      h2 {
        font-size: 32px;
        line-height: 38px;
      }
      h3 {
        font-size: 22px;
        line-height: 28px;
      }
      a:link, a:visited {
        color: {color:Links};
        text-decoration: none;
      }
      a:hover, a:active {
        text-decoration: underline;
      }
      hr {
        border:0 #aaa solid;
        border-top-width:1px;
        clear:both;
        height:0;
      }
      ol {
        list-style:decimal;
      }
      ul {
        list-style:disc;
        margin-left:0px;
      }
      li {
        margin-left:0px;
      }
      p, dl, hr, h1, h2, h3, h4, h5, h6, ol, ul, pre, table, address, fieldset {
        margin: 0 0 15px 0;
      }
      .wrapper {
        max-width: 500px;
        max-width:{select:Page Width}!important;
        margin: 0 auto;
        padding: 0 20px;
      }
      .header {
        margin:0 auto;
      }
      .logotitle {
        margin: 50px 0;
      }
      .logo {
        text-align: center;
      }
      .title {
        text-align: center;
        text-transform: uppercase;
        font-size: 24px;
        font-weight: 100;
        letter-spacing: 5px;
        font-family: 'Montserrat', 'Helvetica Neue', "Arial", sans-serif;
      }
      .title a {
        color: {color:Title};
      }
      .description {
        text-align: center;
        padding: 20px 0 20px 0;
        border-top: 2px solid {color:Dividers};
      }
      .nav {
        display:block;
        list-style: none;
        padding: 20px 0;
        margin: 0;
        text-align: center;
        font-size: 15px;
        text-transform: uppercase;
        font-weight: 700;
        border-top: 2px solid {color:Dividers};
        border-bottom: 2px solid {color:Dividers};
        font-family: 'Montserrat', 'Helvetica Neue', "Arial", sans-serif;
      }
      .nav li {
        margin: 10px;
        display: inline;
      }
      .posts {
        padding-top: 60px;
      }
      iframe {
        max-width: 100%;
      }
      .tumblr_video_container {
        width: 100% !important;
        height: 100% !important;
      }
      .header-posts {
        padding: 0;
      }
      .meta {
        display: block;
        height:14px;
        line-height:1em;
        font-family: 'Montserrat', 'Helvetica Neue', "Arial", sans-serif;
        padding-bottom:60px;
        margin-top: 10px;
        font-size:15px;
        color: {color:Meta};
        text-transform: uppercase;
        border-bottom: 2px solid {color:Dividers};
      }
      .meta a {
        color: {color:Meta};
      }
      .date {
        margin-right: 20px;
      }
      .quote {
        font-size: 30px;
        font-family: 'Merriweather', serif;
        letter-spacing: -1px;
        line-height: 1.2em;
        padding-bottom: 10px;
      }
      blockquote {
        margin-left: 20px;
        padding-left: 15px;
        border-left: 3px {color:Body Text} solid;
      }
      .chat {
        list-style: none;
        padding: 0;
      }
      .tags {
        display: block;
        list-style: none;
        padding: 0;
        margin: 10px 0 0 0;
      }
      .tags a {
        color: {color:Meta};
      }
      .tags ul {
        list-style-type: none;
        display:inline;
        margin: 0;
        padding: 0;
      }
      .tags li {
        margin: 0;
        padding-right: 10px;
        display:inline;
      }
      .footer {
        text-align: center;
        padding-bottom: 25px;
        padding-top: 40px;
      }
      .notes {
        border-bottom: 2px solid {color:Dividers};
        list-style: none;
        padding: 20px 0 50px 0;
        margin: 30px 0 0 0;
        line-height: 2.2em;
      }
      .notes li {
        margin: 0;
      }
      .notes .avatar {
        margin: 0 5px 0 0;
        position: relative;
        top: 5px;
      }
      .notes blockquote {
        margin: 10px 0 0 35px;
        padding-left: 10px;
        border-left: 2px solid {color:Body Text};
      }
      .media {
        margin-bottom: 20px;
      }
      .posts img {
        width: 100%;
      }
      {block:IfInfiniteScroll}
      #infscr-loading, .pagination {
        display: none !important;
      }
      {/block:IfInfiniteScroll}
     .pagination {
        text-align: center;
        font-weight:700;
        border-bottom: 2px solid {color:Dividers};
      }
      .pagination ul {
        list-style: none;
        padding: 10px 15px;
        margin: 10px 0;
      }
      .pagination li {
        margin: 0 2px 0 2px;
        display: inline;
      }
      #pagination a:link, #pageNav a:visited {
        padding: 0;
        margin: 0 2px;
        text-decoration: none;
      }
      #pagination a:hover, #pageNav a:active, #pageNav a.active:link, #pageNav a.active:visited {
        text-decoration: underline;
      }
      #older:after {
        content: " Â»";
      }
      #newer:before {
        content: "Â« ";
      }
      .datenotes {
        float: left;
      }
      .like-button {
        display: inline-block;
        float: right;
        padding: 3px 0 0 10px;
      }
      .reblog-button {
        display: inline-block;
        float: right;
        padding: 3px 0 0 0;
      }
      #install-btn {
        position:fixed;
        bottom: 0px;
        right:6px
      }
      .animated {
        -webkit-animation-fill-mode: both;
        -moz-animation-fill-mode: both;
        -ms-animation-fill-mode: both;
        -o-animation-fill-mode: both;
        animation-fill-mode: both;
        -webkit-animation-duration: 1s;
        -moz-animation-duration: 1s;
        -ms-animation-duration: 1s;
        -o-animation-duration: 1s;
        animation-duration: 1s;
      }
      .animated.hinge {
        -webkit-animation-duration: 1s;
        -moz-animation-duration: 1s;
        -ms-animation-duration: 1s;
        -o-animation-duration: 1s;
        animation-duration: 1s;
      }
      @-webkit-keyframes fadeInDown {
        0% {
          opacity: 0;
          -webkit-transform: translateY(-20px);
        }
        100% {
          opacity: 1;
          -webkit-transform: translateY(0);
        }
      }
      @-moz-keyframes fadeInDown {
        0% {
          opacity: 0;
          -moz-transform: translateY(-20px);
        }
        100% {
          opacity: 1;
          -moz-transform: translateY(0);
        }
      }
      @-o-keyframes fadeInDown {
        0% {
          opacity: 0;
          -o-transform: translateY(-20px);
        }
        100% {
          opacity: 1;
          -o-transform: translateY(0);
        }
      }
      @keyframes fadeInDown {
        0% {
          opacity: 0;
          transform: translateY(-20px);
        }
        100% {
          opacity: 1;
          transform: translateY(0);
        }
      }
      .fadeInDown {
        -webkit-animation-name: fadeInDown;
        -moz-animation-name: fadeInDown;
        -o-animation-name: fadeInDown;
        animation-name: fadeInDown;
      }

    </style>

    <style>{CustomCSS}</style>

  </head>

  <body>

    <div class="wrapper">

      <div class="header">

        <div class="logotitle animated fadeInDown">

          {block:IfLogoImage}
          <div class="logo">
            <a href="/">
              <img src="{image:Logo}" alt={Title}">
            </a>
          </div>
          {/block:IfLogoImage}

          {block:IfNotLogoImage}
          <div class="title">
            <a href="/">{Title}</a>
          </div>
          {/block:IfNotLogoImage}

        </div>

        {block:Description}
        <div class="description">{Description}</div>
        {block:Description}

        <ul class="nav">

          {block:HasPages}
          {block:Pages}
          <li><a href="{URL}">{Label}</a></li>
          {block:Pages}
          {/block:HasPages}

          {block:AskEnabled}
          <li><a href="/ask">Ask</a></li>
          {/block:AskEnabled}

          {block:SubmissionsEnabled}
          <li><a href="/submit">Submit</a></li>
          {/block:SubmissionsEnabled}

          <li><a href="/archive">Twitter</a></li>
          <li><a href="/random">Get KCH</a></li>
          <li><a href="{RSS}">Stake</a></li>

        </ul>

    
        </a>

        <div class="autopagerize_page_element">

          {block:Posts}

          <div class="post" id="{PostID}">

            <div class="posts">

              {block:Photo}
              <div class="media">
            
                <img src="{PhotoURL-HighRes}" alt="{PhotoAlt}" />
               
              </div>
              {block:Caption}
              <div class="photoCaption">{Caption}</div>
              {/block:Caption}
              {/block:Photo}

              {block:Photoset}
              <div class="media">{Photoset}</div>
              {block:Caption}
              <div class="caption">{Caption}</div>
              {/block:Caption}
              {/block:Photoset}

              {block:Audio}
              <div class="audioleft">
                <div class="audioc">
                  <div class="audio">{AudioPlayerBlack}</div>
                </div>
              </div>
              <div class="audioright">
                <div class="audioCaption">
                  {block:Artist}<b>{Artist}</b>{/block:Artist}
                  <p>&mdash;{block:TrackName}{TrackName}{/block:TrackName}</p>
                </div>
              </div>
              <div class="audioClear"></div>
              <div class="audioContainer">
                {block:Caption}{Caption}{/block:Caption}
              </div>
              {/block:Audio}

              {block:Video}
              <div class="js-media media">{Video-700}</div>
              {block:Caption}
              <div>{Caption}</div>
              {/block:Caption}
              {/block:Video}

              {block:Answer}
              <h3>{Asker} asked: {Question}</h3>
              {Answer}
              {/block:Answer}
            </div>

            <div class="header-posts">

              {block:Text}
              {block:Title}
              <h2><a href="{Permalink}">{Title}</a></h2>
              {/block:Title}
              {Body}
              {/block:Text}

              {block:Link}
              <h2><a href="{URL}" {Target}>{Name} &rarr;</a></h2>
              {block:Description}
              <div>{Description}</div>
              {/block:Description}
              {/block:Link}

              {block:Quote}
              <div class="quote">{Quote}</div>
              {block:Source}
              <div id="quoteSource"><p>&mdash; {Source}</p></div>
              {/block:Source}
              {/block:Quote}

              {block:Chat}
              {block:Title}
              <h2>{Title}</h2>
              {/block:Title}
              <ul class="chat">
                {block:Lines}
                <li>{block:Label}<strong>{Label}</strong>{/block:Label} {Line}</li>
                {/block:Lines}
              </ul>
              {/block:Chat}

            </div>

            {block:HasTags}
            <ul class="tags">
              {block:Tags}
              <li><a href="{TagURL}">#{Tag}</a></li>
              {/block:Tags}
            </ul>
            {/block:HasTags}

            <div class="meta">
              <div class="datenotes">

            
          </div>

          {block:PostNotes}
          {PostNotes}
          {/block:PostNotes}

        </div>
        {/block:Posts}

      </div>

      {block:Pagination}
      <div class="pagination">

        <ul class="clearfix">
          {block:PreviousPage}
          <li><a href="{PreviousPage}" id="newer">Newer</a></li>
          {/block:PreviousPage}
          {block:JumpPagination length="10"}
          {block:CurrentPage}
          <li><a href="{URL}" class="active">{PageNumber}</a></li>
          {/block:CurrentPage}
          {block:JumpPage}
          <li><a href="{URL}">{PageNumber}</a></li>
          {/block:JumpPage}
          {/block:JumpPagination}
          {block:NextPage}
          <li><a href="{NextPage}" id="older">Older</a></li>
          {/block:NextPage}
        </ul>

      </div>
      {/block:Pagination}

      <div class="footer">
        © {CopyrightYears} - {Title} - Keep Calm and Hold <br> <strong><p>
      </div>

    </div>

    <script src="https://ajax.googleapis.com/ajax/libs/jquery/1.9.1/jquery.min.js"></script>
    <script src="https://static.tumblr.com/t8k4hxe/WK1mslt6q/jquery.fitvids.js"></script>

    <script>

      $('.js-media').fitVids({ customSelector: 'iframe' });

    </script>

    {block:IfInfiniteScroll}
    {block:IndexPage}
    <script src="https://static.tumblr.com/pqftzxm/Utcnytumt/jquery.infinitescroll.min.js"></script>
    <script>
      (function () {

        $('.autopagerize_page_element').infinitescroll({
          navSelector: '.pagination',
          nextSelector: '.pagination #older',
          itemSelector: '.post',
          bufferPx: 600
        }, function (newElements) {
          var $newElems = $(newElements).css({
            opacity: 0
          });
          var $newElemsIDs = $newElems.map(function () {
            return this.id;
          }).get();
          $newElems.find('.js-media').fitVids({ customSelector: 'iframe' });
          Tumblr.LikeButton.get_status_by_post_ids($newElemsIDs);
          $newElems.animate({
            opacity: 1
          });
        });

      })();
    </script>
    {/block:IndexPage}
    {/block:IfInfiniteScroll}

    {block:IfGoogleAnalyticsID}
    <script>
      var _gaq=[['_setAccount','{text:Google Analytics ID}'],['_trackPageview']];
      (function(d,t){var g=d.createElement(t),s=d.getElementsByTagName(t)[0];
      g.src=('https:'==location.protocol?'//ssl':'//www')+'.google-analytics.com/ga.js';
      s.parentNode.insertBefore(g,s)}(document,'script'));
    </script>
    {/block:IfGoogleAnalyticsID}

  </body>
</html>
