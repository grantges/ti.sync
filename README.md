

[ti-badge]: http://www-static.appcelerator.com/badges/titanium-git-badge-sq.png
[alloy-badge]:http://www-static.appcelerator.com/badges/alloy-git-badge-sq.png
[alloy]:http://www.appcelerator.com/alloy/
[ti]: http://www.appcelerator.com/titanium/
[acs]:http://docs.appcelerator.com/cloud/latest/
[appc_studio]:http://docs.appcelerator.com/platform/latest/#!/guide/Studio
[ti_studio]:http://docs.appcelerator.com/titanium/latest/#!/guide/Studio
[gittio-badge]: http://gitt.io/badge.png
[gittio-page]: http://gitt.io/component/it.smc.navitems

Ti.Sync [![Built for Titanium SDK][ti-badge]][ti] [![Built for Alloy][alloy-badge]][alloy] 
=======

Keeping data in sync between multiple clients and backend datasources can be a major pain

* local caching
* client wins
* server wins
* what about a merge?

**Ti.Sync** is a framework for easily developing [Alloy][alloy] sync adapters for local and remote data management. Leveraging the underlying [Backbone](http://www.backbonejs.org) concepts, the goal of this project is to incorporate the functionality of the sync adapter into the core ti.sync.js file. This would include client side caching, network event monitoring, push / pull of data etc while abstracting the actual connectivity to the remote data sources through a standardized interface layer.

The end result allows the developer to quickly connect to other datasources without having to rebuild the complexities of the managing the data locally.

## Key Features

* Flexible framework for rapidly building Backbone sync adapters for Appcelerator Titanium applications using the Alloy framework.
* Leverage the Alloy model system to interact with remote data
* Offline Cache of remote data
* Policy Management for data synchronization
    * Client Wins
    * Server Wins
    * Latest Timestamp Wins


## Installation & Usage

### Step 1 - Download the Code
Clone or download this repository to your local machine, then copy the `ti.sync.js` file and the `connectors` folder into your projects assets folder under `app/assets/alloy/sync`. By default, Ti.Sync comes with a prebuilt connector for [Appcelerator Cloud Services (ACS)][acs]. This connector is found in the connectors folder. Any additional connectors you build should be referenced from this folder.

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
                      |-acs.js    <-- Appcelerator Cloud Services Connector

~~~

### Step 2 - Create an Alloy Model

From within [Titanium Stuio][ti_studio] or [Appcelerator Studio][appc_studio] open your Project


