

[ti-badge]: http://www-static.appcelerator.com/badges/titanium-git-badge-sq.png
[alloy-badge]:http://www-static.appcelerator.com/badges/alloy-git-badge-sq.png
[alloy]:http://www.appcelerator.com/alloy/
[ti]: http://www.appcelerator.com/titanium/
[gittio-badge]: http://gitt.io/badge.png
[gittio-page]: http://gitt.io/component/it.smc.navitems

Ti.Sync [![Built for Titanium SDK][ti-badge]][ti] [![Built for Alloy][alloy-badge]][alloy] 
=======

Keeping data in sync between multiple clients and backend datasources can be a major pain

* client wins
* server wins
* what about a merge?

**Ti.Sync** is a framework for easily developing [![Alloy][alloy]] sync adapters for local and remote data management. Leveraging the underlying [Backbone](http://www.backbonejs.org) concepts, the goal of this project is to incorporate the functionality of the sync adapter into the core ti.sync.js file. This would include client side caching, network event monitoring, push / pull of data etc while abstracting the actual connectivity to the remote data sources through a standardized interface layer.

The end result allows the developer to quickly connect to other datasources without having to rebuilt the complexities of the managing the data locally.



Usage
=====

Copy the `ti.sync.js` file into your projects assets folder under `app/assets/alloy/sync`. By default, the Ti.Sync comes with a prebuilt adapter for [Appcelerator Cloud Services (ACS)](http://docs.appcelerator.com/cloud/latest/)

~~~

MyProject
  |
  |-app
     |
     |-assets
          |
          |-alloy
              |
              |-sync
                  |
                  |-ti.sync.js    <-- Location of the backbone sync adapter
                  |
                  |-connectors    <-- Folder for any associated remote datasources connectors
                      |
                      |-acs.js

~~~




