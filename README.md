#create Random Points in GEE

var puntosSNG= ee.FeatureCollection.randomPoints(geometry,1000)
Map.addLayer (puntosSNG);
Export.table.toAsset({
  collection:puntosSNG,
  description:'exportarAssets',
  assetId:'puntosSNG'
});
