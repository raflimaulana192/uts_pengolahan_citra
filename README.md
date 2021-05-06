# uts_pengolahan_citra
konversi RGB
![image](https://user-images.githubusercontent.com/56399268/117322038-d7574100-aeb7-11eb-8731-ef7725c7e692.png)

![image](https://user-images.githubusercontent.com/56399268/117322167-f655d300-aeb7-11eb-9c45-e5f0cdab9fdf.png)

kodingnnya yaitu :

[filename, pathname] = uigetfile({'*.png','*.png'});
gambar1 =imread([pathname, filename]);

axes(handles.axes1);
imshow(gambar1);

R = gambar1(:,:,1);
G = gambar1(:,:,2);
B = gambar1(:,:,3);

Red = cat(3,R,G*0,B*0);
Green = cat(3,R*0,G,B*0);
Blue = cat(3,R*0,G*0,B);

axes(handles.axes2);
imshow(Red);

axes(handles.axes3);
imshow(Green);
