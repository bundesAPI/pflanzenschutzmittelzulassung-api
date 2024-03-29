# pflanzenschutzmittelzulassung
No description provided (generated by Openapi Generator https://github.com/openapitools/openapi-generator)

This Python package is automatically generated by the [OpenAPI Generator](https://openapi-generator.tech) project:

- API version: 1.0.0
- Package version: 0.1.0
- Build package: org.openapitools.codegen.languages.PythonClientCodegen

## Requirements.

Python >= 3.6

## Installation & Usage
### pip install

```sh
pip install deutschland[pflanzenschutzmittelzulassung]
```

### poetry install

```sh
poetry add deutschland -E pflanzenschutzmittelzulassung
```

### Setuptools

Install via [Setuptools](http://pypi.python.org/pypi/setuptools).

```sh
python setup.py install --user
```
(or `sudo python setup.py install` to install the package for all users)

## Usage

Import the package:
```python
from deutschland import pflanzenschutzmittelzulassung
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```python

import time
from deutschland import pflanzenschutzmittelzulassung
from pprint import pprint
from deutschland.pflanzenschutzmittelzulassung.api import default_api
from deutschland.pflanzenschutzmittelzulassung.model.adresse_get200_response import AdresseGet200Response
from deutschland.pflanzenschutzmittelzulassung.model.antrag_get200_response import AntragGet200Response
from deutschland.pflanzenschutzmittelzulassung.model.auflage_redu_get200_response import AuflageReduGet200Response
from deutschland.pflanzenschutzmittelzulassung.model.auflagen_get200_response import AuflagenGet200Response
from deutschland.pflanzenschutzmittelzulassung.model.awg_aufwand_get200_response import AwgAufwandGet200Response
from deutschland.pflanzenschutzmittelzulassung.model.awg_bem_get200_response import AwgBemGet200Response
from deutschland.pflanzenschutzmittelzulassung.model.awg_get200_response import AwgGet200Response
from deutschland.pflanzenschutzmittelzulassung.model.awg_kultur_get200_response import AwgKulturGet200Response
from deutschland.pflanzenschutzmittelzulassung.model.awg_partner_aufwand_get200_response import AwgPartnerAufwandGet200Response
from deutschland.pflanzenschutzmittelzulassung.model.awg_partner_get200_response import AwgPartnerGet200Response
from deutschland.pflanzenschutzmittelzulassung.model.awg_schadorg_get200_response import AwgSchadorgGet200Response
from deutschland.pflanzenschutzmittelzulassung.model.awg_verwendungszweck_get200_response import AwgVerwendungszweckGet200Response
from deutschland.pflanzenschutzmittelzulassung.model.awg_wartezeit_ausg_kultur_get200_response import AwgWartezeitAusgKulturGet200Response
from deutschland.pflanzenschutzmittelzulassung.model.awg_wartezeit_get200_response import AwgWartezeitGet200Response
from deutschland.pflanzenschutzmittelzulassung.model.awg_zeitpunkt_get200_response import AwgZeitpunktGet200Response
from deutschland.pflanzenschutzmittelzulassung.model.awg_zulassung_get200_response import AwgZulassungGet200Response
from deutschland.pflanzenschutzmittelzulassung.model.ghs_gefahrenhinweise_get200_response import GhsGefahrenhinweiseGet200Response
from deutschland.pflanzenschutzmittelzulassung.model.ghs_gefahrensymbole_get200_response import GhsGefahrensymboleGet200Response
from deutschland.pflanzenschutzmittelzulassung.model.ghs_sicherheitshinweise_get200_response import GhsSicherheitshinweiseGet200Response
from deutschland.pflanzenschutzmittelzulassung.model.ghs_signalwoerter_get200_response import GhsSignalwoerterGet200Response
from deutschland.pflanzenschutzmittelzulassung.model.hinweis_get200_response import HinweisGet200Response
from deutschland.pflanzenschutzmittelzulassung.model.kode_get200_response import KodeGet200Response
from deutschland.pflanzenschutzmittelzulassung.model.kodeliste_feldname_get200_response import KodelisteFeldnameGet200Response
from deutschland.pflanzenschutzmittelzulassung.model.kodeliste_get200_response import KodelisteGet200Response
from deutschland.pflanzenschutzmittelzulassung.model.kultur_gruppe_get200_response import KulturGruppeGet200Response
from deutschland.pflanzenschutzmittelzulassung.model.mittel_abgelaufen_get200_response import MittelAbgelaufenGet200Response
from deutschland.pflanzenschutzmittelzulassung.model.mittel_abpackung_get200_response import MittelAbpackungGet200Response
from deutschland.pflanzenschutzmittelzulassung.model.mittel_gefahren_symbol_get200_response import MittelGefahrenSymbolGet200Response
from deutschland.pflanzenschutzmittelzulassung.model.mittel_get200_response import MittelGet200Response
from deutschland.pflanzenschutzmittelzulassung.model.mittel_vertrieb_get200_response import MittelVertriebGet200Response
from deutschland.pflanzenschutzmittelzulassung.model.mittel_wirkbereich_get200_response import MittelWirkbereichGet200Response
from deutschland.pflanzenschutzmittelzulassung.model.parallelimport_abgelaufen_get200_response import ParallelimportAbgelaufenGet200Response
from deutschland.pflanzenschutzmittelzulassung.model.schadorg_gruppe_get200_response import SchadorgGruppeGet200Response
from deutschland.pflanzenschutzmittelzulassung.model.staerkung_get200_response import StaerkungGet200Response
from deutschland.pflanzenschutzmittelzulassung.model.stand_get200_response import StandGet200Response
from deutschland.pflanzenschutzmittelzulassung.model.wirkstoff_gehalt_get200_response import WirkstoffGehaltGet200Response
from deutschland.pflanzenschutzmittelzulassung.model.wirkstoff_get200_response import WirkstoffGet200Response
from deutschland.pflanzenschutzmittelzulassung.model.zusatzstoff_get200_response import ZusatzstoffGet200Response
# Defining the host is optional and defaults to https://psm-api.bvl.bund.de/ords/psm/api-v1
# See configuration.py for a list of all supported configuration parameters.
configuration = pflanzenschutzmittelzulassung.Configuration(
    host = "https://psm-api.bvl.bund.de/ords/psm/api-v1"
)



# Enter a context with an instance of the API client
with pflanzenschutzmittelzulassung.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = default_api.DefaultApi(api_client)
    adresse_nr = "adresse_nr_example" # str | Implicit parameter (optional)

    try:
        api_response = api_instance.adresse_get(adresse_nr=adresse_nr)
        pprint(api_response)
    except pflanzenschutzmittelzulassung.ApiException as e:
        print("Exception when calling DefaultApi->adresse_get: %s\n" % e)
```

## Documentation for API Endpoints

All URIs are relative to *https://psm-api.bvl.bund.de/ords/psm/api-v1*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*DefaultApi* | [**adresse_get**](docs/DefaultApi.md#adresse_get) | **GET** /adresse/ | 
*DefaultApi* | [**antrag_get**](docs/DefaultApi.md#antrag_get) | **GET** /antrag/ | 
*DefaultApi* | [**auflage_redu_get**](docs/DefaultApi.md#auflage_redu_get) | **GET** /auflage_redu/ | 
*DefaultApi* | [**auflagen_get**](docs/DefaultApi.md#auflagen_get) | **GET** /auflagen/ | 
*DefaultApi* | [**awg_aufwand_get**](docs/DefaultApi.md#awg_aufwand_get) | **GET** /awg_aufwand/ | 
*DefaultApi* | [**awg_bem_get**](docs/DefaultApi.md#awg_bem_get) | **GET** /awg_bem/ | 
*DefaultApi* | [**awg_get**](docs/DefaultApi.md#awg_get) | **GET** /awg/ | 
*DefaultApi* | [**awg_kultur_get**](docs/DefaultApi.md#awg_kultur_get) | **GET** /awg_kultur/ | 
*DefaultApi* | [**awg_partner_aufwand_get**](docs/DefaultApi.md#awg_partner_aufwand_get) | **GET** /awg_partner_aufwand/ | 
*DefaultApi* | [**awg_partner_get**](docs/DefaultApi.md#awg_partner_get) | **GET** /awg_partner/ | 
*DefaultApi* | [**awg_schadorg_get**](docs/DefaultApi.md#awg_schadorg_get) | **GET** /awg_schadorg/ | 
*DefaultApi* | [**awg_verwendungszweck_get**](docs/DefaultApi.md#awg_verwendungszweck_get) | **GET** /awg_verwendungszweck/ | 
*DefaultApi* | [**awg_wartezeit_ausg_kultur_get**](docs/DefaultApi.md#awg_wartezeit_ausg_kultur_get) | **GET** /awg_wartezeit_ausg_kultur/ | 
*DefaultApi* | [**awg_wartezeit_get**](docs/DefaultApi.md#awg_wartezeit_get) | **GET** /awg_wartezeit/ | 
*DefaultApi* | [**awg_zeitpunkt_get**](docs/DefaultApi.md#awg_zeitpunkt_get) | **GET** /awg_zeitpunkt/ | 
*DefaultApi* | [**awg_zulassung_get**](docs/DefaultApi.md#awg_zulassung_get) | **GET** /awg_zulassung/ | 
*DefaultApi* | [**ghs_gefahrenhinweise_get**](docs/DefaultApi.md#ghs_gefahrenhinweise_get) | **GET** /ghs_gefahrenhinweise/ | 
*DefaultApi* | [**ghs_gefahrensymbole_get**](docs/DefaultApi.md#ghs_gefahrensymbole_get) | **GET** /ghs_gefahrensymbole/ | 
*DefaultApi* | [**ghs_sicherheitshinweise_get**](docs/DefaultApi.md#ghs_sicherheitshinweise_get) | **GET** /ghs_sicherheitshinweise/ | 
*DefaultApi* | [**ghs_signalwoerter_get**](docs/DefaultApi.md#ghs_signalwoerter_get) | **GET** /ghs_signalwoerter/ | 
*DefaultApi* | [**hinweis_get**](docs/DefaultApi.md#hinweis_get) | **GET** /hinweis/ | 
*DefaultApi* | [**kode_get**](docs/DefaultApi.md#kode_get) | **GET** /kode/ | 
*DefaultApi* | [**kodeliste_feldname_get**](docs/DefaultApi.md#kodeliste_feldname_get) | **GET** /kodeliste_feldname/ | 
*DefaultApi* | [**kodeliste_get**](docs/DefaultApi.md#kodeliste_get) | **GET** /kodeliste/ | 
*DefaultApi* | [**kultur_gruppe_get**](docs/DefaultApi.md#kultur_gruppe_get) | **GET** /kultur_gruppe/ | 
*DefaultApi* | [**mittel_abgelaufen_get**](docs/DefaultApi.md#mittel_abgelaufen_get) | **GET** /mittel_abgelaufen/ | 
*DefaultApi* | [**mittel_abpackung_get**](docs/DefaultApi.md#mittel_abpackung_get) | **GET** /mittel_abpackung/ | 
*DefaultApi* | [**mittel_gefahren_symbol_get**](docs/DefaultApi.md#mittel_gefahren_symbol_get) | **GET** /mittel_gefahren_symbol/ | 
*DefaultApi* | [**mittel_get**](docs/DefaultApi.md#mittel_get) | **GET** /mittel/ | 
*DefaultApi* | [**mittel_vertrieb_get**](docs/DefaultApi.md#mittel_vertrieb_get) | **GET** /mittel_vertrieb/ | 
*DefaultApi* | [**mittel_wirkbereich_get**](docs/DefaultApi.md#mittel_wirkbereich_get) | **GET** /mittel_wirkbereich/ | 
*DefaultApi* | [**parallelimport_abgelaufen_get**](docs/DefaultApi.md#parallelimport_abgelaufen_get) | **GET** /parallelimport_abgelaufen/ | 
*DefaultApi* | [**parallelimport_gueltig_get**](docs/DefaultApi.md#parallelimport_gueltig_get) | **GET** /parallelimport_gueltig/ | 
*DefaultApi* | [**schadorg_gruppe_get**](docs/DefaultApi.md#schadorg_gruppe_get) | **GET** /schadorg_gruppe/ | 
*DefaultApi* | [**staerkung_get**](docs/DefaultApi.md#staerkung_get) | **GET** /staerkung/ | 
*DefaultApi* | [**staerkung_vertrieb_get**](docs/DefaultApi.md#staerkung_vertrieb_get) | **GET** /staerkung_vertrieb/ | 
*DefaultApi* | [**stand_get**](docs/DefaultApi.md#stand_get) | **GET** /stand/ | 
*DefaultApi* | [**wirkstoff_gehalt_get**](docs/DefaultApi.md#wirkstoff_gehalt_get) | **GET** /wirkstoff_gehalt/ | 
*DefaultApi* | [**wirkstoff_get**](docs/DefaultApi.md#wirkstoff_get) | **GET** /wirkstoff/ | 
*DefaultApi* | [**zusatzstoff_get**](docs/DefaultApi.md#zusatzstoff_get) | **GET** /zusatzstoff/ | 
*DefaultApi* | [**zusatzstoff_vertrieb_get**](docs/DefaultApi.md#zusatzstoff_vertrieb_get) | **GET** /zusatzstoff_vertrieb/ | 


## Documentation For Models

 - [AdresseGet200Response](docs/AdresseGet200Response.md)
 - [AdresseGet200ResponseItemsInner](docs/AdresseGet200ResponseItemsInner.md)
 - [AntragGet200Response](docs/AntragGet200Response.md)
 - [AntragGet200ResponseItemsInner](docs/AntragGet200ResponseItemsInner.md)
 - [AuflageReduGet200Response](docs/AuflageReduGet200Response.md)
 - [AuflageReduGet200ResponseItemsInner](docs/AuflageReduGet200ResponseItemsInner.md)
 - [AuflagenGet200Response](docs/AuflagenGet200Response.md)
 - [AuflagenGet200ResponseItemsInner](docs/AuflagenGet200ResponseItemsInner.md)
 - [AwgAufwandGet200Response](docs/AwgAufwandGet200Response.md)
 - [AwgAufwandGet200ResponseItemsInner](docs/AwgAufwandGet200ResponseItemsInner.md)
 - [AwgBemGet200Response](docs/AwgBemGet200Response.md)
 - [AwgBemGet200ResponseItemsInner](docs/AwgBemGet200ResponseItemsInner.md)
 - [AwgGet200Response](docs/AwgGet200Response.md)
 - [AwgGet200ResponseItemsInner](docs/AwgGet200ResponseItemsInner.md)
 - [AwgKulturGet200Response](docs/AwgKulturGet200Response.md)
 - [AwgKulturGet200ResponseItemsInner](docs/AwgKulturGet200ResponseItemsInner.md)
 - [AwgPartnerAufwandGet200Response](docs/AwgPartnerAufwandGet200Response.md)
 - [AwgPartnerAufwandGet200ResponseItemsInner](docs/AwgPartnerAufwandGet200ResponseItemsInner.md)
 - [AwgPartnerGet200Response](docs/AwgPartnerGet200Response.md)
 - [AwgPartnerGet200ResponseItemsInner](docs/AwgPartnerGet200ResponseItemsInner.md)
 - [AwgSchadorgGet200Response](docs/AwgSchadorgGet200Response.md)
 - [AwgSchadorgGet200ResponseItemsInner](docs/AwgSchadorgGet200ResponseItemsInner.md)
 - [AwgVerwendungszweckGet200Response](docs/AwgVerwendungszweckGet200Response.md)
 - [AwgVerwendungszweckGet200ResponseItemsInner](docs/AwgVerwendungszweckGet200ResponseItemsInner.md)
 - [AwgWartezeitAusgKulturGet200Response](docs/AwgWartezeitAusgKulturGet200Response.md)
 - [AwgWartezeitAusgKulturGet200ResponseItemsInner](docs/AwgWartezeitAusgKulturGet200ResponseItemsInner.md)
 - [AwgWartezeitGet200Response](docs/AwgWartezeitGet200Response.md)
 - [AwgWartezeitGet200ResponseItemsInner](docs/AwgWartezeitGet200ResponseItemsInner.md)
 - [AwgZeitpunktGet200Response](docs/AwgZeitpunktGet200Response.md)
 - [AwgZeitpunktGet200ResponseItemsInner](docs/AwgZeitpunktGet200ResponseItemsInner.md)
 - [AwgZulassungGet200Response](docs/AwgZulassungGet200Response.md)
 - [AwgZulassungGet200ResponseItemsInner](docs/AwgZulassungGet200ResponseItemsInner.md)
 - [DATE](docs/DATE.md)
 - [GhsGefahrenhinweiseGet200Response](docs/GhsGefahrenhinweiseGet200Response.md)
 - [GhsGefahrenhinweiseGet200ResponseItemsInner](docs/GhsGefahrenhinweiseGet200ResponseItemsInner.md)
 - [GhsGefahrensymboleGet200Response](docs/GhsGefahrensymboleGet200Response.md)
 - [GhsGefahrensymboleGet200ResponseItemsInner](docs/GhsGefahrensymboleGet200ResponseItemsInner.md)
 - [GhsSicherheitshinweiseGet200Response](docs/GhsSicherheitshinweiseGet200Response.md)
 - [GhsSicherheitshinweiseGet200ResponseItemsInner](docs/GhsSicherheitshinweiseGet200ResponseItemsInner.md)
 - [GhsSignalwoerterGet200Response](docs/GhsSignalwoerterGet200Response.md)
 - [GhsSignalwoerterGet200ResponseItemsInner](docs/GhsSignalwoerterGet200ResponseItemsInner.md)
 - [HinweisGet200Response](docs/HinweisGet200Response.md)
 - [HinweisGet200ResponseItemsInner](docs/HinweisGet200ResponseItemsInner.md)
 - [KodeGet200Response](docs/KodeGet200Response.md)
 - [KodeGet200ResponseItemsInner](docs/KodeGet200ResponseItemsInner.md)
 - [KodelisteFeldnameGet200Response](docs/KodelisteFeldnameGet200Response.md)
 - [KodelisteFeldnameGet200ResponseItemsInner](docs/KodelisteFeldnameGet200ResponseItemsInner.md)
 - [KodelisteGet200Response](docs/KodelisteGet200Response.md)
 - [KodelisteGet200ResponseItemsInner](docs/KodelisteGet200ResponseItemsInner.md)
 - [KulturGruppeGet200Response](docs/KulturGruppeGet200Response.md)
 - [KulturGruppeGet200ResponseItemsInner](docs/KulturGruppeGet200ResponseItemsInner.md)
 - [MittelAbgelaufenGet200Response](docs/MittelAbgelaufenGet200Response.md)
 - [MittelAbgelaufenGet200ResponseItemsInner](docs/MittelAbgelaufenGet200ResponseItemsInner.md)
 - [MittelAbpackungGet200Response](docs/MittelAbpackungGet200Response.md)
 - [MittelAbpackungGet200ResponseItemsInner](docs/MittelAbpackungGet200ResponseItemsInner.md)
 - [MittelGefahrenSymbolGet200Response](docs/MittelGefahrenSymbolGet200Response.md)
 - [MittelGefahrenSymbolGet200ResponseItemsInner](docs/MittelGefahrenSymbolGet200ResponseItemsInner.md)
 - [MittelGet200Response](docs/MittelGet200Response.md)
 - [MittelGet200ResponseItemsInner](docs/MittelGet200ResponseItemsInner.md)
 - [MittelVertriebGet200Response](docs/MittelVertriebGet200Response.md)
 - [MittelVertriebGet200ResponseItemsInner](docs/MittelVertriebGet200ResponseItemsInner.md)
 - [MittelWirkbereichGet200Response](docs/MittelWirkbereichGet200Response.md)
 - [MittelWirkbereichGet200ResponseItemsInner](docs/MittelWirkbereichGet200ResponseItemsInner.md)
 - [ParallelimportAbgelaufenGet200Response](docs/ParallelimportAbgelaufenGet200Response.md)
 - [ParallelimportAbgelaufenGet200ResponseItemsInner](docs/ParallelimportAbgelaufenGet200ResponseItemsInner.md)
 - [SchadorgGruppeGet200Response](docs/SchadorgGruppeGet200Response.md)
 - [SchadorgGruppeGet200ResponseItemsInner](docs/SchadorgGruppeGet200ResponseItemsInner.md)
 - [StaerkungGet200Response](docs/StaerkungGet200Response.md)
 - [StaerkungGet200ResponseItemsInner](docs/StaerkungGet200ResponseItemsInner.md)
 - [StandGet200Response](docs/StandGet200Response.md)
 - [StandGet200ResponseItemsInner](docs/StandGet200ResponseItemsInner.md)
 - [WirkstoffGehaltGet200Response](docs/WirkstoffGehaltGet200Response.md)
 - [WirkstoffGehaltGet200ResponseItemsInner](docs/WirkstoffGehaltGet200ResponseItemsInner.md)
 - [WirkstoffGet200Response](docs/WirkstoffGet200Response.md)
 - [WirkstoffGet200ResponseItemsInner](docs/WirkstoffGet200ResponseItemsInner.md)
 - [ZusatzstoffGet200Response](docs/ZusatzstoffGet200Response.md)
 - [ZusatzstoffGet200ResponseItemsInner](docs/ZusatzstoffGet200ResponseItemsInner.md)


## Documentation For Authorization

 All endpoints do not require authorization.

## Author

kontakt@bund.dev


## Notes for Large OpenAPI documents
If the OpenAPI document is large, imports in pflanzenschutzmittelzulassung.apis and pflanzenschutzmittelzulassung.models may fail with a
RecursionError indicating the maximum recursion limit has been exceeded. In that case, there are a couple of solutions:

Solution 1:
Use specific imports for apis and models like:
- `from deutschland.pflanzenschutzmittelzulassung.api.default_api import DefaultApi`
- `from deutschland.pflanzenschutzmittelzulassung.model.pet import Pet`

Solution 2:
Before importing the package, adjust the maximum recursion limit as shown below:
```
import sys
sys.setrecursionlimit(1500)
from deutschland import pflanzenschutzmittelzulassung
from deutschland.pflanzenschutzmittelzulassung.apis import *
from deutschland.pflanzenschutzmittelzulassung.models import *
```

