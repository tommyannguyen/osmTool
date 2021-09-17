# code
./osmconvert vietnam-latest.osm.pbf -o=vietnam-latest.o5m

./osmfilter vietnam-latest.o5m --keep="addr:country= and addr:city= and addr:street=" --ignore-dependencies --drop-relations --drop-ways | osmconverter - --csv="@oname @id @lon @lat addr:country addr:city addr:street" >> streets.csv

# install
Supported input and output formats are .osm format and .o5m format. To allow fast data processing, it is recommended to use .o5m format at least for input. The program osmconvert will help you converting other formats to .o5m. For example: ./osmconvert file.pbf -o=file.o5m

https://wiki.openstreetmap.org/wiki/Osmfilter