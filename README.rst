This view can be used to request layer-map-previews by Id.
Geonode 2.4 normally expects the layer name in URLs

1. Clone app
2. Enable in settings.py
3. Add to geonode/urls.py before layers/ ::
    
    url(r'^layers/(?P<layername>\d+)$', 'geonode.layer_by_id.views.layer_detail', name="layer_detail"),
    
