# Media-3D-Pada-P5js
Tugas membuat Media 3D Pada P5js 

function setup() {
  // Membuat canvas 3D
  createCanvas(400, 400, WEBGL);
}

function draw() {
  // Mengatur background
  background(200);

  // Menambahkan pencahayaan
  directionalLight(255, 255, 255, 0.5, 1, -0.5);
  ambientLight(100);

  // Mengatur rotasi objek berdasarkan waktu
  rotateY(frameCount * 0.01);

  // Membuat batang pohon (silinder)
  push();
  fill(139, 69, 19); // Warna cokelat untuk batang pohon
  cylinder(20, 150); // Silinder dengan diameter 20 dan tinggi 150
  pop();

  // Membuat lapisan daun 1 (kerucut bawah)
  push();
  translate(0, -80, 0); // Menggeser ke atas batang
  fill(34, 139, 34); // Warna hijau untuk daun
  cone(70, 100); // Kerucut besar sebagai lapisan bawah daun
  pop();

  // Membuat lapisan daun 2 (kerucut tengah)
  push();
  translate(0, -130, 0); // Menggeser lebih ke atas
  fill(34, 139, 34); // Warna hijau
  cone(50, 80); // Kerucut sedang sebagai lapisan tengah daun
  pop();

  // Membuat lapisan daun 3 (kerucut atas)
  push();
  translate(0, -170, 0); // Menggeser ke atas lebih jauh
  fill(34, 139, 34); // Warna hijau
  cone(30, 60); // Kerucut kecil sebagai lapisan atas daun
  pop();
}
