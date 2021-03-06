# OpenStreetMap Indoor Mapping browser.

A javascript application to display rooms in a building.

### Status

This a fork from [yarl/osmtools-indoor](https://github.com/yarl/osmtools-indoor) in order to simplify and expand it.

The main objective is to have a self-contained, client application to display building's insides from OpenStreetMap.

This is curently being worked on by students on behalf of [LIFL](http://www.lifl.fr), which should use this application for its buildings soon.

### Advantages

- no PHP
- vertical_passage support
- simpler navigation
- better zoom support
- ??

### How it works?

Displayed data are taken 'live' from OSM database is using [Overpass API](http://wiki.openstreetmap.org/wiki/Overpass_API). It's working worldwide.

It uses [Leaflet](http://leafletjs.com/), an excellent map display library, quite a lot.
 
### How to map a building?

In order to render building outline on the map, relation of building should have a way (role 'outer') with tags building='yes' and level='0'. The relation itself should have tag type='building' and contain subrelations representing building's levels.

Relation of level should have tag type='level' and contain ways - rooms. Each room should be a member of proper level with role 'buildingpart' and should contain tag buildingpart='room'.

For more information please take a look at OSM [wiki page](http://wiki.openstreetmap.org/wiki/IndoorOSM#The_Model_.2F_Tagging_Schema).

### License

    Copyright (C) 2012-2013 Yarl (yarl@o2.pl)

    This program is free software: you can redistribute it and/or modify
    it under the terms of the GNU General Public License as published by
    the Free Software Foundation, either version 3 of the License, or
    (at your option) any later version.

    This program is distributed in the hope that it will be useful,
    but WITHOUT ANY WARRANTY; without even the implied warranty of
    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
    GNU General Public License for more details.

    You should have received a copy of the GNU General Public License
    along with this program.  If not, see <http://www.gnu.org/licenses/>.
