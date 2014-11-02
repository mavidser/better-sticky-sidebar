$(document).ready(function () {
  $(".table-cell-container").height($(window).height());
});

$(window).resize(function () {
  $(".table-cell-container").height($(window).height());
  overflow = $(window).height() - $('#sidebarInner').height();
});

$( "#login-login" ).click(function(event) {
  event.preventDefault();
  $( "#alert-login" ).css( "opacity","1");
  $( "#alert-login" ).css( "top","20px");
  $( "#alert-register" ).css( "opacity","1");
  $( "#alert-register" ).css( "top","20px");
});

$( ".login-alert-close" ).click(function(event) {
  event.preventDefault();
  $( "#alert-login" ).css( "opacity","0");
  $( "#alert-login" ).css( "top","-60px");
  $( "#alert-register" ).css( "opacity","0");
  $( "#alert-register" ).css( "top","-60px");
});

$( "#register-next" ).click(function(event) {
  event.preventDefault();
  $( ".register-form-1" ).css( "margin-top","-"+$( $(".register-form-1" ).height())[0]+"px");
  $( ".register-form-1" ).css( "opacity","0");
  setTimeout(function(){$( ".register-form-1" ).css( "display","none");},500);
  $( ".register-form-2" ).css( "display","block");
  $( ".register-form-2" ).css( "margin-top","0px");
  $( ".register-form-2" ).css( "opacity","1");
});

var element                 = $('#sidebarInner');
    previousScroll          = 0,
    topOffset               = 10,
    bottomOffset            = 10,
    threshold               = element.offset().top,
    previousScrollDirection = 1,
    fixed                   = 0,
    overflow                = $(this).height() - element.height();

$(window).scroll(function(){
  var currentScroll         = $(this).scrollTop(),
      currentScrollBottom   = currentScroll + $(this).height(),
      elementBottom         = element.offset().top + element.height(),
      scrollDifference      = currentScroll - previousScroll,
      scrollDirection       = scrollDifference?scrollDifference<0?-1:1:0,
      topBorderGap          = element.offset().top - currentScroll,
      bottomBorderGap       = currentScrollBottom - elementBottom;

  if(currentScroll > threshold - topOffset) {
    if(previousScrollDirection != scrollDirection && fixed==1) {
      directionChange(scrollDirection,currentScroll - topBorderGap);
    }
    else if (topBorderGap > topOffset && scrollDirection == -1) {
      element.css('top',topOffset).css('position','fixed');
      fixed=1;
    }
    else if(bottomBorderGap > bottomOffset && scrollDirection == 1) {
      element.css('top',overflow-bottomOffset).css('position','fixed');
      fixed=1;
    }
  }
  else {
    element.css('top',0).css('position','relative');
    fixed=0;
  }

  previousScroll = currentScroll;
  previousScrollDirection = scrollDirection;
});

function directionChange (newDirection,offset) {
  if(newDirection==1) {
    element.css('position','relative').css('top',offset-threshold);
  }
  else {
    var top = overflow + $(this).scrollTop() - threshold;
    element.css('position','relative').css('top',top); 
  }
  fixed=0;
}

