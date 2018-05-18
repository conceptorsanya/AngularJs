# AngularJs
This repo contains AngularJs files
<!-- view.html -->
<div
  file-upload
  action='/api/v1/serie/image/{{ main.serie.id }}'
  btn-class='btn btn-small'
  btn-label="Choose Image"
  input-name="image"
  on-success='serieImageUploaded(responseText)'
  progress-class='btn btn-small'></div>
// ctrl.js
$scope.serieImageUploaded = function (resp) {
  var data = angular.fromJson(resp);
  $scope.main.serie.image = data.serie.image;
  $scope.main.serie.banner_tile_image = data.serie.banner_tile_image;
}
