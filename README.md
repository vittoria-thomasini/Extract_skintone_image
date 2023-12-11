# IDENTIFICAÇÃO E EXTRAÇÃO DE TOM DE PELE UTILIZANDO K-MEANS

## Objetivos

Com o propósito de identificar subtons de pele utilizando técnicas de inteligência artificial, foram estabelecidos alguns objetivos.

### OBJETIVOS GERAIS
O objetivo principal deste trabalho é desenvolver um modelo de identificação e classificação de tons e subtons de pele humana em imagens, utilizando a escala Monk Skin Tone como métrica de identificação da cor dominante. Este modelo pode ser usado em futuras aplicações que permitam aos usuários identificarem seu tom de pele, com objetivo de ajudá-lo a escolher produtos de maquiagem, como a base.

### OBJETIVOS ESPECÍFICOS
Para a plena consecução do objetivo principal, os seguintes objetivos específicos são definidos:
– realizar uma pesquisa bibliográfica sobre o tema proposto;
– identificar a técnica adequada de machine learning a ser aplicada;
– obter e tratar as imagens utilizando a biblioteca de manipulação de imagens
OpenCV;
– segmentar as imagens para extrair informações da imagem relevantes para
classificação de tons da pele;
– desenvolver algoritmos de identificação da escala de tons a partir da extração da
cor dominante da pele;
– classificar o tom dominante identificado conforme a paleta de Monk;
– validar a classificação do tom dominante identificado conforme a paleta de Monk.
 

## Justificativa

A motivação para o desenvolvimento do trabalho reside na problemática que muitos consumidores têm em identificar o próprio tom de pele e conseguir identificar no mercado de cosméticos um produto que tenha um tom que combine com o seu. Atualmente, muito se fala de diversidade e inclusão na indústria de cosméticos e, por isso, cada vez mais marcas estão desenvolvendo cartelas com faixas de cores mais amplas.
No mercado de varejo entende-se que estratégias que auxiliam os clientes a executarem tarefas que entregam valor e reconhecimento pessoal são mais eficazes para fidelizar o cliente (JAIN; BHATTI, 2010). Pensando nesta questão, e com a crescente demanda de personalização, com a tecnologia tornando-se uma ferramenta, a fim de estimular a experiência dos consumidores, o projeto propõe o estudo e a prototipação de um modelo de identificação e classificação do tom de pele, utilizando técnicas de inteligência artificial, para auxiliar os consumidores a identificarem o seu próprio tom de pele.
Existem diversas abordagens para detecção de pele, mas poucos estudos se dedicam a estudar os tons de pele em si. A maioria dos estudos abrange melhores abordagens para a detecção de pele voltada ao reconhecimento facial. Por isso, o desenvolvimento deste trabalho focaliza a identificação de tons de pele, com a menor interferência possível de condições de iluminação e fundo, assim como a influência da região dos olhos, boca, nariz e cabelos.
Diversas aplicações poderão usar os resultados da detecção e classificação de tom de pele, principalmente voltados à indústria da beleza, por profissionais da área de visagismo, maquiadores, pesquisadores sociais, entre outros.

## Exemplo de resultado
Original Image 

![image](https://github.com/vittoria-thomasini/Extract_skintone_image/assets/53311902/0f5dffcc-0478-42da-99c2-dd007708d5b4)

Gray Image

![image](https://github.com/vittoria-thomasini/Extract_skintone_image/assets/53311902/06718bbc-b63e-4194-af73-c1e37a4c2599)

Face

![image](https://github.com/vittoria-thomasini/Extract_skintone_image/assets/53311902/0f1209dd-e40f-4591-aaf5-7b0e984a6321)

Remove Eye

![image](https://github.com/vittoria-thomasini/Extract_skintone_image/assets/53311902/10f2e63a-9606-40b2-9714-c3ee61825877)

Remove Mouth

![image](https://github.com/vittoria-thomasini/Extract_skintone_image/assets/53311902/3d02a48b-7b03-48c7-a581-a7df3203a40b)

Remove Nose

![image](https://github.com/vittoria-thomasini/Extract_skintone_image/assets/53311902/043c8943-b659-403c-8906-9a30ab96999d)

Image result on HSV

![image](https://github.com/vittoria-thomasini/Extract_skintone_image/assets/53311902/a3ce7100-1041-4a13-9323-384875cff595)

Image thresholding
![image](https://github.com/vittoria-thomasini/Extract_skintone_image/assets/53311902/62d5950d-17bd-417d-8469-8e02bf094604)

Color Bar:

![image](https://github.com/vittoria-thomasini/Extract_skintone_image/assets/53311902/37c4936e-6c52-4d27-8763-6c582299f009)

Dominant Color:  {'cluster_index': 7, 'color': [195.0480949406607, 142.58525921299145, 126.40287320424756], 'color_percentage': 0.17665164339892273}

CIELab:  [135 128 128]

MST Classification:  1

Subject:  subject_16

Pose : facing_camera

Light: well_lit

Distance RGB List:  [147.75728773974615, 136.71422558783874, 133.0929989660338, 103.71331427561492, 55.76047947100978, 55.99849949141663, 101.58161472419432, 146.17039748036723, 186.18331309212283, 209.76924346901913]

Minimun RGB : 55.76047947100978

RGB MST Classification Found: 5

Classification RGB:  147.75728773974615

Distance CIELab List: [40.54972950357521, 40.89993405677667, 42.78354714488424, 44.70979322274493, 46.88442095056724, 57.65049753494448, 65.50271878732414, 76.21706110186337, 87.41093222700634, 94.73423169780044]

Mininun CIELab:  40.54972950357521

CIELab MST Classification Found: 1

Expected Distance RGB: 147.01028087111263

Expected Distance CIELab: 40.77005064388297

Accuracy RGB: 8.1

Accuracy CIELab: 100.0
