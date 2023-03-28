var scene = new THREE.Scene();
var camera = new THREE.PerspectiveCamera(45, window.innerWidth / window.innerHeight, 0.1, 1000);
var renderer = new THREE.WebGLRenderer();
var cubeGeometry = new THREE.BoxGeometry(4, 4, 4);
var planeMaterial = new THREE.MeshBasicMaterial({
color: 0xAAAAAA
});
var cubeMaterial = new THREE.MeshLambertMaterial({
color: 0xFF0000
});
var cubeGeometry = new THREE.BoxGeometry(4, 4, 4);
var cubeMaterial = new THREE.MeshLambertMaterial({
color: 0xFF0000
});
var cube = new THREE.Mesh(cubeGeometry, cubeMaterial);
var sphereGeometry = new THREE.SphereGeometry(4, 20, 20);
var planeGeometry = new THREE.PlaneGeometry(60, 20);
var spotLight = new THREE.SpotLight(0xFFFFFF);
const clock = new THREE.clock();

**开启阴影**

```
renderer.shadowMap.enabled = true;
plane.receiveShadow = true;
cube.castShadow = true;
sphere.castShadow = true;
spotLight.castShadow = true;
```
