# GEE
Open Sentinel Images
var radar = ee.ImageCollection ('COPERNICUS/S1_GRD')
//'COPERNICUS/S1_GRD' Abrir toda as imagens das Imagens do Sentinel 1 - RADAR.
.filter(ee.Filter.listContains('transmitterReceiverPolarisation', 'VV'))
.filter(ee.Filter.listContains('transmitterReceiverPolarisation', 'VH'))
//Incluir Polarização das cenas
Map.addLayer(radar), {min:-36.4993324, max:-4.4172, band: 'VV'};

//Para abrir uma imagem apenas
var radar = ee.Image('COPERNICUS/S1_GRD/S1A_IW_GRDH_1SDV_20171201T080058_20171201T080123_019506_0211A6_C7B7')
//ID 'COPERNICUS/S1_GRD/S1A_IW_GRDH_1SDV_20171201T080058_20171201T080123_019506_0211A6_C7B7'
Map.addLayer(radar), {min:-36.4993324, max:-4.4172, band: 'VV'};
