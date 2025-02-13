# -Redu-o-de-Dimensionalidade-em-Imagens-para-Redes-Neurais

Aqui está um exemplo de como você pode implementar a transformação de uma imagem colorida para níveis de cinza e depois binarizá-la usando Scilab: 

// Carregar a imagem colorida
image_path = "sua_imagem_colorida.jpg";
color_image = imread(image_path);

// Converter a imagem para níveis de cinza
grayscale_image = rgb2gray(color_image);

// Salvar a imagem em níveis de cinza
imwrite(grayscale_image, "imagem_em_escala_de_cinza.jpg");

// Definir o valor de limiar para binarização
threshold = 128;

// Binarizar a imagem
binary_image = grayscale_image > threshold;

// Converter valores binários para 0 e 255
binary_image = binary_image * 255;

// Salvar a imagem binarizada
imwrite(binary_image, "imagem_binarizada.jpg");

// Exibir as imagens
figure();
subplot(1,3,1); imshow(color_image); title("Imagem Colorida");
subplot(1,3,2); imshow(grayscale_image); title("Imagem em Escala de Cinza");
subplot(1,3,3); imshow(binary_image); title("Imagem Binarizada");
