# OpenStreetMap Roads
The package takes an openstreetmap pbf file and converts it to a Trie with all the road network information
It provides an api to then do a fast map matching for any latitude, longitude that comes under the bounding box of the pbf file. 

## Importing and loading the pbf file
from osm_roads.osm_roads import OsmRoads

way_finder = OsmRoads()
way_finder.load_osm_pbf("bengaluru.pbf")

## Search for map matching with latitude and longitude 

way_finder.get_road_type(12.934005898750094, 77.61075025215672)

## Saving the current PBF to a trie 
way_finder.export_trie('bangalore_updated.trie')

## Loading the trie from file 
way_finder.load_trie('bangalore_updated.trie')