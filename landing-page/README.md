### RetinaJS

    - Thêm data-rjs="3" trong element cần retina
        * <img src="/images/my_image.png" data-rjs="/images/2x/my_image.png" />
        * <div style="background: url(my_image.png);" data-rjs="3" />
        * <div style="background: url(my_image.png);" data-rjs="3" />
    - Thêm trong js để apply cho element nào.
        * retinajs();
        * retinajs( $('img') );
        
    - Ví dụ về CSS
    
```bash

#logo {
  background: url("my_image.png") center center no-repeat;
  background-size: 100px 50px;
}

@media all and (-webkit-min-device-pixel-ratio: 1.5),
       all and (-o-min-device-pixel-ratio: 3 / 2),
       all and (min--moz-device-pixel-ratio: 1.5),
       all and (min-device-pixel-ratio: 1.5) {
  #item {
    background: url("my_image@2x.png") center center no-repeat;
    background-size: 100px 50px;
  }
}

@media (-webkit-min-device-pixel-ratio: 2), (min-resolution: 192dpi) {
  #item {
    background: url("my_image@2x.png") center center no-repeat;
    background-size: 100px 50px;
  }
}

@media (-webkit-min-device-pixel-ratio: 3), (min-resolution: 288dpi) {
  #item {
    background: url("my_image@3x.png") center center no-repeat;
    background-size: 100px 50px;
  }
}

```