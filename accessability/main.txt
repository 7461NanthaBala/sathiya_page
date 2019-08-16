$(document).ready(function() {
  $(".skiplink").focusin(function(){
     $(this).css("position","static");
  })
   $(".skiplink").focusout(function(){
     $(this).css("position","absolute");
  })

  $("#searchForRetailers").keyup(function() {
  
    
    var filter = $(this).val();
  
    $(".retail").each(function() {
     
      if (
        $(this)
          .attr('alt')
          .indexOf(filter) < 0
      ) {
        $(this).fadeOut(2000);

       
      } else {
        $(this).show();
      }
    });
  });
});
