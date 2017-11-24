This is a basic "back to top" jQuery type function for drupal.

Add the .css to a css or sass file (and include it in the themename.styles.scss file)

Put the image into the themes/themename/image folder

Add the js file to the js folder & reference from the html.tpl.php file, or add :

<script type="text/javascript">
$('body').prepend('<a href="#" class="back-to-top">Back to Top</a>');

var amountScrolled = 300;

$(window).scroll(function() {
  if ( $(window).scrollTop() > amountScrolled ) {
    $('a.back-to-top').fadeIn('slow');
  } else {
    $('a.back-to-top').fadeOut('slow');
  }
});

$('a.back-to-top, a.simple-back-to-top').click(function() {
  $('html, body').animate({
    scrollTop: 0
  }, 700);
  return false;
});

at the bottom , below   <?php print $page_bottom; ?>


