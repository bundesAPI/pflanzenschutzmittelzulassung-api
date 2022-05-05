# pflanzenschutzmittelzulassung.DefaultApi

All URIs are relative to *https://psm-api.bvl.bund.de/ords/psm/api-v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**adresse_get**](DefaultApi.md#adresse_get) | **GET** /adresse/ | 
[**antrag_get**](DefaultApi.md#antrag_get) | **GET** /antrag/ | 
[**auflage_redu_get**](DefaultApi.md#auflage_redu_get) | **GET** /auflage_redu/ | 
[**auflagen_get**](DefaultApi.md#auflagen_get) | **GET** /auflagen/ | 
[**awg_aufwand_get**](DefaultApi.md#awg_aufwand_get) | **GET** /awg_aufwand/ | 
[**awg_bem_get**](DefaultApi.md#awg_bem_get) | **GET** /awg_bem/ | 
[**awg_get**](DefaultApi.md#awg_get) | **GET** /awg/ | 
[**awg_kultur_get**](DefaultApi.md#awg_kultur_get) | **GET** /awg_kultur/ | 
[**awg_partner_aufwand_get**](DefaultApi.md#awg_partner_aufwand_get) | **GET** /awg_partner_aufwand/ | 
[**awg_partner_get**](DefaultApi.md#awg_partner_get) | **GET** /awg_partner/ | 
[**awg_schadorg_get**](DefaultApi.md#awg_schadorg_get) | **GET** /awg_schadorg/ | 
[**awg_verwendungszweck_get**](DefaultApi.md#awg_verwendungszweck_get) | **GET** /awg_verwendungszweck/ | 
[**awg_wartezeit_ausg_kultur_get**](DefaultApi.md#awg_wartezeit_ausg_kultur_get) | **GET** /awg_wartezeit_ausg_kultur/ | 
[**awg_wartezeit_get**](DefaultApi.md#awg_wartezeit_get) | **GET** /awg_wartezeit/ | 
[**awg_zeitpunkt_get**](DefaultApi.md#awg_zeitpunkt_get) | **GET** /awg_zeitpunkt/ | 
[**awg_zulassung_get**](DefaultApi.md#awg_zulassung_get) | **GET** /awg_zulassung/ | 
[**ghs_gefahrenhinweise_get**](DefaultApi.md#ghs_gefahrenhinweise_get) | **GET** /ghs_gefahrenhinweise/ | 
[**ghs_gefahrensymbole_get**](DefaultApi.md#ghs_gefahrensymbole_get) | **GET** /ghs_gefahrensymbole/ | 
[**ghs_sicherheitshinweise_get**](DefaultApi.md#ghs_sicherheitshinweise_get) | **GET** /ghs_sicherheitshinweise/ | 
[**ghs_signalwoerter_get**](DefaultApi.md#ghs_signalwoerter_get) | **GET** /ghs_signalwoerter/ | 
[**hinweis_get**](DefaultApi.md#hinweis_get) | **GET** /hinweis/ | 
[**kode_get**](DefaultApi.md#kode_get) | **GET** /kode/ | 
[**kodeliste_feldname_get**](DefaultApi.md#kodeliste_feldname_get) | **GET** /kodeliste_feldname/ | 
[**kodeliste_get**](DefaultApi.md#kodeliste_get) | **GET** /kodeliste/ | 
[**kultur_gruppe_get**](DefaultApi.md#kultur_gruppe_get) | **GET** /kultur_gruppe/ | 
[**mittel_abgelaufen_get**](DefaultApi.md#mittel_abgelaufen_get) | **GET** /mittel_abgelaufen/ | 
[**mittel_abpackung_get**](DefaultApi.md#mittel_abpackung_get) | **GET** /mittel_abpackung/ | 
[**mittel_gefahren_symbol_get**](DefaultApi.md#mittel_gefahren_symbol_get) | **GET** /mittel_gefahren_symbol/ | 
[**mittel_get**](DefaultApi.md#mittel_get) | **GET** /mittel/ | 
[**mittel_vertrieb_get**](DefaultApi.md#mittel_vertrieb_get) | **GET** /mittel_vertrieb/ | 
[**mittel_wirkbereich_get**](DefaultApi.md#mittel_wirkbereich_get) | **GET** /mittel_wirkbereich/ | 
[**parallelimport_abgelaufen_get**](DefaultApi.md#parallelimport_abgelaufen_get) | **GET** /parallelimport_abgelaufen/ | 
[**parallelimport_gueltig_get**](DefaultApi.md#parallelimport_gueltig_get) | **GET** /parallelimport_gueltig/ | 
[**schadorg_gruppe_get**](DefaultApi.md#schadorg_gruppe_get) | **GET** /schadorg_gruppe/ | 
[**staerkung_get**](DefaultApi.md#staerkung_get) | **GET** /staerkung/ | 
[**staerkung_vertrieb_get**](DefaultApi.md#staerkung_vertrieb_get) | **GET** /staerkung_vertrieb/ | 
[**stand_get**](DefaultApi.md#stand_get) | **GET** /stand/ | 
[**wirkstoff_gehalt_get**](DefaultApi.md#wirkstoff_gehalt_get) | **GET** /wirkstoff_gehalt/ | 
[**wirkstoff_get**](DefaultApi.md#wirkstoff_get) | **GET** /wirkstoff/ | 
[**zusatzstoff_get**](DefaultApi.md#zusatzstoff_get) | **GET** /zusatzstoff/ | 
[**zusatzstoff_vertrieb_get**](DefaultApi.md#zusatzstoff_vertrieb_get) | **GET** /zusatzstoff_vertrieb/ | 


# **adresse_get**
> InlineResponse200 adresse_get()



Liefert eine Liste aller Adressen und Namen von Vertriebsfirmen/Antragstellern/Importeuren von Pflanzenschutzmitteln.                       Optional kann nur nach einer Adresse gesucht werden, wenn die entsprechende {adresse_nr} gegeben wird.                       Der Paramter ist optional; werden keine Parameter Ã¼bergeben, enthÃ¤lt die RÃ¼ckgabe alle EintrÃ¤ge.      {adresse_nr} ist der eindeutige Identifizierer fÃ¼r eine Adresse und damit eine/n Vertriebsfirma/Antragsteller/Importeur. Nummer mit bis zu 38 Ziffern, Bsp: 10784.  Wenn auf andere Parameter gefiltert oder Teilabfragen gestellt werden sollen, kÃ¶nnen gesonderte Filtermethoden verwendet werden. Siehe dazu Abschnitt &quot;*JSON Queries*&quot; in der oberen allgemeinen API Beschreibung

### Example


```python
import time
from deutschland import pflanzenschutzmittelzulassung
from deutschland.pflanzenschutzmittelzulassung.api import default_api
from deutschland.pflanzenschutzmittelzulassung.model.inline_response200 import InlineResponse200
from pprint import pprint
# Defining the host is optional and defaults to https://psm-api.bvl.bund.de/ords/psm/api-v1
# See configuration.py for a list of all supported configuration parameters.
configuration = pflanzenschutzmittelzulassung.Configuration(
    host = "https://psm-api.bvl.bund.de/ords/psm/api-v1"
)


# Enter a context with an instance of the API client
with pflanzenschutzmittelzulassung.ApiClient() as api_client:
    # Create an instance of the API class
    api_instance = default_api.DefaultApi(api_client)
    adresse_nr = "adresse_nr_example" # str | Implicit parameter (optional)

    # example passing only required values which don't have defaults set
    # and optional values
    try:
        api_response = api_instance.adresse_get(adresse_nr=adresse_nr)
        pprint(api_response)
    except pflanzenschutzmittelzulassung.ApiException as e:
        print("Exception when calling DefaultApi->adresse_get: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **adresse_nr** | **str**| Implicit parameter | [optional]

### Return type

[**InlineResponse200**](InlineResponse200.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The queried record. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **antrag_get**
> InlineResponse2001 antrag_get()



Liefert die ZulassungsantrÃ¤ge und Antragsteller zu aktuell gÃ¼ltigen Pflanzenschutzmitteln (im Endpunkt /mittel).                       Optional kann nach der Antragnummer {antragnr}, dem Antragsteller {antragsteller_nr} und/oder der Kennnummer des Mittels gefiltert werden.                       Die Paramter sind optional; werden keine Parameter Ã¼bergeben, enthÃ¤lt die RÃ¼ckgabe alle EintrÃ¤ge.      Der eindeutige Identifizierer setzt sich zusammen aus {antragnr} und {kennr}.     {antragnr} ist die Nummer des Antrags. Zeichenfolge aus zwei Zeichen, Bsp: 00.     {antragsteller_nr} ist die Nummer des Antragstellers, referenziert aus dem /adresse Endpunkt. Zahl aus maximal 22 Ziffern, Bsp: 10091.     {kennr} ist die Kennummer eines Pflanzenschutzmittels, referenziert aus dem /mittel Endpunkt. Zeichenkette aus neun Zeichen, Bsp: 005632-60.  Wenn auf andere Parameter gefiltert oder Teilabfragen gestellt werden sollen, kÃ¶nnen gesonderte Filtermethoden verwendet werden. Siehe dazu Abschnitt &quot;*JSON Queries*&quot; in der oberen allgemeinen API Beschreibung

### Example


```python
import time
from deutschland import pflanzenschutzmittelzulassung
from deutschland.pflanzenschutzmittelzulassung.api import default_api
from deutschland.pflanzenschutzmittelzulassung.model.inline_response2001 import InlineResponse2001
from pprint import pprint
# Defining the host is optional and defaults to https://psm-api.bvl.bund.de/ords/psm/api-v1
# See configuration.py for a list of all supported configuration parameters.
configuration = pflanzenschutzmittelzulassung.Configuration(
    host = "https://psm-api.bvl.bund.de/ords/psm/api-v1"
)


# Enter a context with an instance of the API client
with pflanzenschutzmittelzulassung.ApiClient() as api_client:
    # Create an instance of the API class
    api_instance = default_api.DefaultApi(api_client)
    antragnr = "antragnr_example" # str | Implicit parameter (optional)
    antragsteller_nr = "antragsteller_nr_example" # str | Implicit parameter (optional)
    kennr = "kennr_example" # str | Implicit parameter (optional)

    # example passing only required values which don't have defaults set
    # and optional values
    try:
        api_response = api_instance.antrag_get(antragnr=antragnr, antragsteller_nr=antragsteller_nr, kennr=kennr)
        pprint(api_response)
    except pflanzenschutzmittelzulassung.ApiException as e:
        print("Exception when calling DefaultApi->antrag_get: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **antragnr** | **str**| Implicit parameter | [optional]
 **antragsteller_nr** | **str**| Implicit parameter | [optional]
 **kennr** | **str**| Implicit parameter | [optional]

### Return type

[**InlineResponse2001**](InlineResponse2001.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The queried record. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **auflage_redu_get**
> InlineResponse2002 auflage_redu_get()



Liefert eine Liste der Auflagen mit reduzierten AbstÃ¤nden bei verwendeten GerÃ¤ten verschiedener Abdriftminderungsklassen.                       Optional kann nach einer Auflagennummer {auflagenr} gefiltert werden.                       Der Paramter ist optional; werden keine Parameter Ã¼bergeben, enthÃ¤lt die RÃ¼ckgabe alle EintrÃ¤ge.      Der eindeutige Identifizierer wird gebildet aus allen Attributen dieses Endpunkts.     {auflagenr} ist die Nummer einer Auflage, referenziert aus dem /auflagen Endpunkt. Ziffernfolge, Bsp: 49804321.  Wenn auf andere Parameter gefiltert oder Teilabfragen gestellt werden sollen, kÃ¶nnen gesonderte Filtermethoden verwendet werden. Siehe dazu Abschnitt &quot;*JSON Queries*&quot; in der oberen allgemeinen API Beschreibung

### Example


```python
import time
from deutschland import pflanzenschutzmittelzulassung
from deutschland.pflanzenschutzmittelzulassung.api import default_api
from deutschland.pflanzenschutzmittelzulassung.model.inline_response2002 import InlineResponse2002
from pprint import pprint
# Defining the host is optional and defaults to https://psm-api.bvl.bund.de/ords/psm/api-v1
# See configuration.py for a list of all supported configuration parameters.
configuration = pflanzenschutzmittelzulassung.Configuration(
    host = "https://psm-api.bvl.bund.de/ords/psm/api-v1"
)


# Enter a context with an instance of the API client
with pflanzenschutzmittelzulassung.ApiClient() as api_client:
    # Create an instance of the API class
    api_instance = default_api.DefaultApi(api_client)
    auflagenr = "auflagenr_example" # str | Implicit parameter (optional)

    # example passing only required values which don't have defaults set
    # and optional values
    try:
        api_response = api_instance.auflage_redu_get(auflagenr=auflagenr)
        pprint(api_response)
    except pflanzenschutzmittelzulassung.ApiException as e:
        print("Exception when calling DefaultApi->auflage_redu_get: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **auflagenr** | **str**| Implicit parameter | [optional]

### Return type

[**InlineResponse2002**](InlineResponse2002.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The queried record. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **auflagen_get**
> InlineResponse2003 auflagen_get()



Liefert die Liste aller gesetzlichen Auflagen zu Mitteln und Anwendungen.                       Optional kann nach Auflagennummer {auflagenr}, der Ebene {ebene} und/oder eines Auflagenkodes {auflage} gefiltert werden.                       Die Paramter sind optional; werden keine Parameter Ã¼bergeben, enthÃ¤lt die RÃ¼ckgabe alle EintrÃ¤ge.      {auflagenr} ist der eindeutige Identifizierer einer Auflage. Ziffernfolge, Bsp: 49747804.     {auflage} ist der Kode einer Auflage. Der entsprechende Kode Text kann im /kode Endpunkt angefragt werden. Zeichenkette aus maximal 20 Zeichen, Bsp: WMA.     {ebene} ist entweder die Kennnummer eines Mittels (kennr im /mittel Endpunkt, 9 Zeichen) oder der Identifizierer einer Anwendung (awg_id im /awg Endpunkt, 16 Zeichen). Zeichenkette aus maximal 16 Zeichen, Bsp: 024366-00 oder 005190-00/00-004.  Wenn auf andere Parameter gefiltert oder Teilabfragen gestellt werden sollen, kÃ¶nnen gesonderte Filtermethoden verwendet werden. Siehe dazu Abschnitt &quot;*JSON Queries*&quot; in der oberen allgemeinen API Beschreibung

### Example


```python
import time
from deutschland import pflanzenschutzmittelzulassung
from deutschland.pflanzenschutzmittelzulassung.api import default_api
from deutschland.pflanzenschutzmittelzulassung.model.inline_response2003 import InlineResponse2003
from pprint import pprint
# Defining the host is optional and defaults to https://psm-api.bvl.bund.de/ords/psm/api-v1
# See configuration.py for a list of all supported configuration parameters.
configuration = pflanzenschutzmittelzulassung.Configuration(
    host = "https://psm-api.bvl.bund.de/ords/psm/api-v1"
)


# Enter a context with an instance of the API client
with pflanzenschutzmittelzulassung.ApiClient() as api_client:
    # Create an instance of the API class
    api_instance = default_api.DefaultApi(api_client)
    auflage = "auflage_example" # str | Implicit parameter (optional)
    auflagenr = "auflagenr_example" # str | Implicit parameter (optional)
    ebene = "ebene_example" # str | Implicit parameter (optional)

    # example passing only required values which don't have defaults set
    # and optional values
    try:
        api_response = api_instance.auflagen_get(auflage=auflage, auflagenr=auflagenr, ebene=ebene)
        pprint(api_response)
    except pflanzenschutzmittelzulassung.ApiException as e:
        print("Exception when calling DefaultApi->auflagen_get: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **auflage** | **str**| Implicit parameter | [optional]
 **auflagenr** | **str**| Implicit parameter | [optional]
 **ebene** | **str**| Implicit parameter | [optional]

### Return type

[**InlineResponse2003**](InlineResponse2003.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The queried record. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **awg_aufwand_get**
> InlineResponse2005 awg_aufwand_get()



Liefert eine Zuordnung von Anwendungen ({awg_id}) auf vorgeschriebene AufwÃ¤nde/Mengen von Pflanzenschutzmittel und Wasser bei dieser Anwendung.                       Optional kann auf einzelnde Anwendungen per {awg_id} gefiltert werden.                       Der Paramter ist optional; werden keine Parameter Ã¼bergeben, enthÃ¤lt die RÃ¼ckgabe alle EintrÃ¤ge.      Der eindeutige Identifizierer bestimmt sich aus der awg_id, der aufwandbedingung und der sortier_nr.     {awg_id} ist der Identifizierer einer Anwendung, referenziert aus dem Endpunkt /awg. Zeichenfolge aus 16 Zeichen, Bsp: 024785-63/00-002.  Wenn auf andere Parameter gefiltert oder Teilabfragen gestellt werden sollen, kÃ¶nnen gesonderte Filtermethoden verwendet werden. Siehe dazu Abschnitt &quot;*JSON Queries*&quot; in der oberen allgemeinen API Beschreibung

### Example


```python
import time
from deutschland import pflanzenschutzmittelzulassung
from deutschland.pflanzenschutzmittelzulassung.api import default_api
from deutschland.pflanzenschutzmittelzulassung.model.inline_response2005 import InlineResponse2005
from pprint import pprint
# Defining the host is optional and defaults to https://psm-api.bvl.bund.de/ords/psm/api-v1
# See configuration.py for a list of all supported configuration parameters.
configuration = pflanzenschutzmittelzulassung.Configuration(
    host = "https://psm-api.bvl.bund.de/ords/psm/api-v1"
)


# Enter a context with an instance of the API client
with pflanzenschutzmittelzulassung.ApiClient() as api_client:
    # Create an instance of the API class
    api_instance = default_api.DefaultApi(api_client)
    awg_id = "awg_id_example" # str | Implicit parameter (optional)

    # example passing only required values which don't have defaults set
    # and optional values
    try:
        api_response = api_instance.awg_aufwand_get(awg_id=awg_id)
        pprint(api_response)
    except pflanzenschutzmittelzulassung.ApiException as e:
        print("Exception when calling DefaultApi->awg_aufwand_get: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **awg_id** | **str**| Implicit parameter | [optional]

### Return type

[**InlineResponse2005**](InlineResponse2005.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The queried record. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **awg_bem_get**
> InlineResponse2006 awg_bem_get()



Liefert eine Liste von Bemerkungen/ErlÃ¤uterungen zu Anwendungen. (&quot;Auflage&quot; hat in diesem Endpunkt KEINE Verbindung zum Endpunkt /auflage!)                       Optional kann nach einzelnen Anwendungen ({awg_id}) gefiltert werden.                       Der Paramter ist optional; werden keine Parameter Ã¼bergeben, enthÃ¤lt die RÃ¼ckgabe alle EintrÃ¤ge.      Der eindeutige Identifizierer bestimmt sich aus der awg_id und der auflage_bem.     {awg_id} ist der Identifizierer einer Anwendung, referenziert aus dem Endpunkt /awg. Zeichenfolge aus 16 Zeichen, Bsp: 034210-64/00-007.  Wenn auf andere Parameter gefiltert oder Teilabfragen gestellt werden sollen, kÃ¶nnen gesonderte Filtermethoden verwendet werden. Siehe dazu Abschnitt &quot;*JSON Queries*&quot; in der oberen allgemeinen API Beschreibung

### Example


```python
import time
from deutschland import pflanzenschutzmittelzulassung
from deutschland.pflanzenschutzmittelzulassung.api import default_api
from deutschland.pflanzenschutzmittelzulassung.model.inline_response2006 import InlineResponse2006
from pprint import pprint
# Defining the host is optional and defaults to https://psm-api.bvl.bund.de/ords/psm/api-v1
# See configuration.py for a list of all supported configuration parameters.
configuration = pflanzenschutzmittelzulassung.Configuration(
    host = "https://psm-api.bvl.bund.de/ords/psm/api-v1"
)


# Enter a context with an instance of the API client
with pflanzenschutzmittelzulassung.ApiClient() as api_client:
    # Create an instance of the API class
    api_instance = default_api.DefaultApi(api_client)
    awg_id = "awg_id_example" # str | Implicit parameter (optional)

    # example passing only required values which don't have defaults set
    # and optional values
    try:
        api_response = api_instance.awg_bem_get(awg_id=awg_id)
        pprint(api_response)
    except pflanzenschutzmittelzulassung.ApiException as e:
        print("Exception when calling DefaultApi->awg_bem_get: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **awg_id** | **str**| Implicit parameter | [optional]

### Return type

[**InlineResponse2006**](InlineResponse2006.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The queried record. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **awg_get**
> InlineResponse2004 awg_get()



Liefert eine Liste aller zugelassenen Anwendungen. Eine Anwendung beinhaltet ein angewendetes Mittel, eine Kultur, dessen Wachstumsstadium und einen Schadorganismus. Kultur und Schadorganismus kÃ¶nnen Ã¼ber die Endpunkte /awg_kultur und /awg_schadorg abgerufen werden.                       Optional kann die ID der Anwendung {awg_id} und/oder die Kennnummer eines Mittels {kennr} Ã¼bergeben werden, um die Ergebnisse zu filtern.                       Die Paramter sind optional; werden keine Parameter Ã¼bergeben, enthÃ¤lt die RÃ¼ckgabe alle EintrÃ¤ge.      {awg_id} ist der eindeutige Identifizierer einer Anwendung. Zeichenfolge aus 16 Zeichen, Bsp: 007472-60/01-012.     {kennr} ist die Kennummer des Mittels auf das sich die Anwendung bezieht, referenziert aus dem /mittel Endpunkt. Zeichenfolge aus 9 Zeichen, Bsp: 007472-60.  Wenn auf andere Parameter gefiltert oder Teilabfragen gestellt werden sollen, kÃ¶nnen gesonderte Filtermethoden verwendet werden. Siehe dazu Abschnitt &quot;*JSON Queries*&quot; in der oberen allgemeinen API Beschreibung

### Example


```python
import time
from deutschland import pflanzenschutzmittelzulassung
from deutschland.pflanzenschutzmittelzulassung.api import default_api
from deutschland.pflanzenschutzmittelzulassung.model.inline_response2004 import InlineResponse2004
from pprint import pprint
# Defining the host is optional and defaults to https://psm-api.bvl.bund.de/ords/psm/api-v1
# See configuration.py for a list of all supported configuration parameters.
configuration = pflanzenschutzmittelzulassung.Configuration(
    host = "https://psm-api.bvl.bund.de/ords/psm/api-v1"
)


# Enter a context with an instance of the API client
with pflanzenschutzmittelzulassung.ApiClient() as api_client:
    # Create an instance of the API class
    api_instance = default_api.DefaultApi(api_client)
    awg_id = "awg_id_example" # str | Implicit parameter (optional)
    kennr = "kennr_example" # str | Implicit parameter (optional)

    # example passing only required values which don't have defaults set
    # and optional values
    try:
        api_response = api_instance.awg_get(awg_id=awg_id, kennr=kennr)
        pprint(api_response)
    except pflanzenschutzmittelzulassung.ApiException as e:
        print("Exception when calling DefaultApi->awg_get: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **awg_id** | **str**| Implicit parameter | [optional]
 **kennr** | **str**| Implicit parameter | [optional]

### Return type

[**InlineResponse2004**](InlineResponse2004.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The queried record. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **awg_kultur_get**
> InlineResponse2007 awg_kultur_get()



Liefert eine Zuordnung von Anwendungen zu Kulturen. Wenn das Feld &quot;ausgenommen&quot; &quot;J&quot; beinhaltet, bildet die in &quot;kultur&quot; angegebene Kultur eine Ausnahme und ist nicht in der Anwendung enthalten.                             Optional kann nach einzelnen Anwendungen ({awg_id}) gefiltert werden.                             Der Paramter ist optional; werden keine Parameter Ã¼bergeben, enthÃ¤lt die RÃ¼ckgabe alle EintrÃ¤ge.      Der eindeutige Identifizierer bestimmt sich aus der awg_id und der kultur.     {awg_id} ist der Identifizierer einer Anwendung, referenziert aus dem Endpunkt /awg. Zeichenfolge aus 16 Zeichen, Bsp: 042688-00/00-001.  Wenn auf andere Parameter gefiltert oder Teilabfragen gestellt werden sollen, kÃ¶nnen gesonderte Filtermethoden verwendet werden. Siehe dazu Abschnitt &quot;*JSON Queries*&quot; in der oberen allgemeinen API Beschreibung

### Example


```python
import time
from deutschland import pflanzenschutzmittelzulassung
from deutschland.pflanzenschutzmittelzulassung.api import default_api
from deutschland.pflanzenschutzmittelzulassung.model.inline_response2007 import InlineResponse2007
from pprint import pprint
# Defining the host is optional and defaults to https://psm-api.bvl.bund.de/ords/psm/api-v1
# See configuration.py for a list of all supported configuration parameters.
configuration = pflanzenschutzmittelzulassung.Configuration(
    host = "https://psm-api.bvl.bund.de/ords/psm/api-v1"
)


# Enter a context with an instance of the API client
with pflanzenschutzmittelzulassung.ApiClient() as api_client:
    # Create an instance of the API class
    api_instance = default_api.DefaultApi(api_client)
    awg_id = "awg_id_example" # str | Implicit parameter (optional)

    # example passing only required values which don't have defaults set
    # and optional values
    try:
        api_response = api_instance.awg_kultur_get(awg_id=awg_id)
        pprint(api_response)
    except pflanzenschutzmittelzulassung.ApiException as e:
        print("Exception when calling DefaultApi->awg_kultur_get: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **awg_id** | **str**| Implicit parameter | [optional]

### Return type

[**InlineResponse2007**](InlineResponse2007.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The queried record. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **awg_partner_aufwand_get**
> InlineResponse2009 awg_partner_aufwand_get()



Liefert die Zuordnung von Anwendungen zu einem Partnermittel inklusive dem maximalen Aufwand.                             Optional kann nach einer Anwendung {awg_id} gefiltert werden.                             Der Paramter ist optional; werden keine Parameter Ã¼bergeben, enthÃ¤lt die RÃ¼ckgabe alle EintrÃ¤ge.       Der eindeutige Identifizierer bestimmt sich aus der awg_id, der aufwandbedingung und der partner_kennr.     {awg_id} ist der Identifizierer einer Anwendung, referenziert aus dem Endpunkt /awg. Zeichenfolge aus 16 Zeichen, Bsp: 024366-00/02-005.  Wenn auf andere Parameter gefiltert oder Teilabfragen gestellt werden sollen, kÃ¶nnen gesonderte Filtermethoden verwendet werden. Siehe dazu Abschnitt &quot;*JSON Queries*&quot; in der oberen allgemeinen API Beschreibung

### Example


```python
import time
from deutschland import pflanzenschutzmittelzulassung
from deutschland.pflanzenschutzmittelzulassung.api import default_api
from deutschland.pflanzenschutzmittelzulassung.model.inline_response2009 import InlineResponse2009
from pprint import pprint
# Defining the host is optional and defaults to https://psm-api.bvl.bund.de/ords/psm/api-v1
# See configuration.py for a list of all supported configuration parameters.
configuration = pflanzenschutzmittelzulassung.Configuration(
    host = "https://psm-api.bvl.bund.de/ords/psm/api-v1"
)


# Enter a context with an instance of the API client
with pflanzenschutzmittelzulassung.ApiClient() as api_client:
    # Create an instance of the API class
    api_instance = default_api.DefaultApi(api_client)
    awg_id = "awg_id_example" # str | Implicit parameter (optional)

    # example passing only required values which don't have defaults set
    # and optional values
    try:
        api_response = api_instance.awg_partner_aufwand_get(awg_id=awg_id)
        pprint(api_response)
    except pflanzenschutzmittelzulassung.ApiException as e:
        print("Exception when calling DefaultApi->awg_partner_aufwand_get: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **awg_id** | **str**| Implicit parameter | [optional]

### Return type

[**InlineResponse2009**](InlineResponse2009.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The queried record. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **awg_partner_get**
> InlineResponse2008 awg_partner_get()



Liefert die Zuordnung von Anwendungen zu Partnermitteln, die gemeinsam verwendet werden dÃ¼rfen, zum Beipiel als Tankmischungen.                             Optional kann auf eine Anwendung {awg_id} gefiltert werden.                             Der Parameter ist optional; werden keine Parameter Ã¼bergeben, enthÃ¤lt die RÃ¼ckgabe alle EintrÃ¤ge.      Der eindeutige Identifizierer bestimmt sich aus der awg_id und der partner_kennr.     {awg_id} ist der Identifizierer einer Anwendung, referenziert aus dem Endpunkt /awg. Zeichenfolge aus 16 Zeichen, Bsp: 034078-00/01-003.  Wenn auf andere Parameter gefiltert oder Teilabfragen gestellt werden sollen, kÃ¶nnen gesonderte Filtermethoden verwendet werden. Siehe dazu Abschnitt &quot;*JSON Queries*&quot; in der oberen allgemeinen API Beschreibung

### Example


```python
import time
from deutschland import pflanzenschutzmittelzulassung
from deutschland.pflanzenschutzmittelzulassung.api import default_api
from deutschland.pflanzenschutzmittelzulassung.model.inline_response2008 import InlineResponse2008
from pprint import pprint
# Defining the host is optional and defaults to https://psm-api.bvl.bund.de/ords/psm/api-v1
# See configuration.py for a list of all supported configuration parameters.
configuration = pflanzenschutzmittelzulassung.Configuration(
    host = "https://psm-api.bvl.bund.de/ords/psm/api-v1"
)


# Enter a context with an instance of the API client
with pflanzenschutzmittelzulassung.ApiClient() as api_client:
    # Create an instance of the API class
    api_instance = default_api.DefaultApi(api_client)
    awg_id = "awg_id_example" # str | Implicit parameter (optional)

    # example passing only required values which don't have defaults set
    # and optional values
    try:
        api_response = api_instance.awg_partner_get(awg_id=awg_id)
        pprint(api_response)
    except pflanzenschutzmittelzulassung.ApiException as e:
        print("Exception when calling DefaultApi->awg_partner_get: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **awg_id** | **str**| Implicit parameter | [optional]

### Return type

[**InlineResponse2008**](InlineResponse2008.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The queried record. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **awg_schadorg_get**
> InlineResponse20010 awg_schadorg_get()



Liefert eine Zuordnung von Anwendungen zu Schadorganismen. Wenn das Feld &quot;ausgenommen&quot; &quot;J&quot; beinhaltet, bildet der in &quot;schadorg&quot; angegebene Schadorganismus eine Ausnahme und ist nicht in der Anwendung enthalten.                             Optional kann nach einzelnen Anwendungen ({awg_id}) gefiltert werden.                             Der Paramter ist optional; werden keine Parameter Ã¼bergeben, enthÃ¤lt die RÃ¼ckgabe alle EintrÃ¤ge.      Der eindeutige Identifizierer bestimmt sich aus der awg_id und dem schadorg.     {awg_id} ist der Identifizierer einer Anwendung, referenziert aus dem Endpunkt /awg. Zeichenfolge aus 16 Zeichen, Bsp: 043099-63/00-007.  Wenn auf andere Parameter gefiltert oder Teilabfragen gestellt werden sollen, kÃ¶nnen gesonderte Filtermethoden verwendet werden. Siehe dazu Abschnitt &quot;*JSON Queries*&quot; in der oberen allgemeinen API Beschreibung

### Example


```python
import time
from deutschland import pflanzenschutzmittelzulassung
from deutschland.pflanzenschutzmittelzulassung.api import default_api
from deutschland.pflanzenschutzmittelzulassung.model.inline_response20010 import InlineResponse20010
from pprint import pprint
# Defining the host is optional and defaults to https://psm-api.bvl.bund.de/ords/psm/api-v1
# See configuration.py for a list of all supported configuration parameters.
configuration = pflanzenschutzmittelzulassung.Configuration(
    host = "https://psm-api.bvl.bund.de/ords/psm/api-v1"
)


# Enter a context with an instance of the API client
with pflanzenschutzmittelzulassung.ApiClient() as api_client:
    # Create an instance of the API class
    api_instance = default_api.DefaultApi(api_client)
    awg_id = "awg_id_example" # str | Implicit parameter (optional)

    # example passing only required values which don't have defaults set
    # and optional values
    try:
        api_response = api_instance.awg_schadorg_get(awg_id=awg_id)
        pprint(api_response)
    except pflanzenschutzmittelzulassung.ApiException as e:
        print("Exception when calling DefaultApi->awg_schadorg_get: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **awg_id** | **str**| Implicit parameter | [optional]

### Return type

[**InlineResponse20010**](InlineResponse20010.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The queried record. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **awg_verwendungszweck_get**
> InlineResponse20011 awg_verwendungszweck_get()



Liefert die Zuordnung der Anwendungen zu Verwendungszwecken des assoziierten Mittels. Welcher Verwendng die behandelte Kultur also zugefÃ¼hrt werden darf. Kodiert Ã¼ber Kodeliste 31, einzusehen Ã¼ber den Endpunkt /kode.                             Optional kann auf eine Anwendung {awg_id} gefiltert werden.                             Der Paramter ist optional; werden keine Parameter Ã¼bergeben enthÃ¤lt die RÃ¼ckgabe alle EintrÃ¤ge.      Der eindeutige Identifizierer bestimmt sich aus allen Attributen des Endpunkts.     {awg_id} ist der Identifizierer einer Anwendung, referenziert aus dem Endpunkt /awg. Zeichenfolge aus 16 Zeichen, Bsp: 024436-63/00-069.  Wenn auf andere Parameter gefiltert oder Teilabfragen gestellt werden sollen, kÃ¶nnen gesonderte Filtermethoden verwendet werden. Siehe dazu Abschnitt &quot;*JSON Queries*&quot; in der oberen allgemeinen API Beschreibung

### Example


```python
import time
from deutschland import pflanzenschutzmittelzulassung
from deutschland.pflanzenschutzmittelzulassung.api import default_api
from deutschland.pflanzenschutzmittelzulassung.model.inline_response20011 import InlineResponse20011
from pprint import pprint
# Defining the host is optional and defaults to https://psm-api.bvl.bund.de/ords/psm/api-v1
# See configuration.py for a list of all supported configuration parameters.
configuration = pflanzenschutzmittelzulassung.Configuration(
    host = "https://psm-api.bvl.bund.de/ords/psm/api-v1"
)


# Enter a context with an instance of the API client
with pflanzenschutzmittelzulassung.ApiClient() as api_client:
    # Create an instance of the API class
    api_instance = default_api.DefaultApi(api_client)
    awg_id = "awg_id_example" # str | Implicit parameter (optional)

    # example passing only required values which don't have defaults set
    # and optional values
    try:
        api_response = api_instance.awg_verwendungszweck_get(awg_id=awg_id)
        pprint(api_response)
    except pflanzenschutzmittelzulassung.ApiException as e:
        print("Exception when calling DefaultApi->awg_verwendungszweck_get: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **awg_id** | **str**| Implicit parameter | [optional]

### Return type

[**InlineResponse20011**](InlineResponse20011.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The queried record. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **awg_wartezeit_ausg_kultur_get**
> InlineResponse20013 awg_wartezeit_ausg_kultur_get()



Liefert die Zuordnung von Anwendungswartezeiten auf Kulturen, die fÃ¼r diese Wartezeit ausgenommen sind. Die Wartezeit fÃ¼r die Ã¼brigen Kulturen kann im Endpunkt /awg_wartezeit abgerufen werden.                             Optional kann nach der Wartezeit ID {awg_wartezeit_nr} oder der Kultur {kultur} gefiltert werden.                             Die Paramter sind optional; werden keine Parameter Ã¼bergeben, enthÃ¤lt die RÃ¼ckgabe alle EintrÃ¤ge.      Der eindeutige Identifizierer bestimmt sich aus sÃ¤mtlichen Attributen des Endpunkts.     {awg_wartezeit_nr} ist der Identifizierer der Zuordnung einer Anwendung zu einer Wartezeit aus dem Endpunkt /awg_wartezeit. Ziffernfolge aus maximal 38 Ziffern, Bsp: 129281.     {kultur} ist der Kode der behandelten Kultur, referenziert aus dem Endpunkt /kultur_gruppe. Zeichenfolge aus maximal 20 Zeichen, Bsp: VIOWH.  Wenn auf andere Parameter gefiltert oder Teilabfragen gestellt werden sollen, kÃ¶nnen gesonderte Filtermethoden verwendet werden. Siehe dazu Abschnitt &quot;*JSON Queries*&quot; in der oberen allgemeinen API Beschreibung

### Example


```python
import time
from deutschland import pflanzenschutzmittelzulassung
from deutschland.pflanzenschutzmittelzulassung.api import default_api
from deutschland.pflanzenschutzmittelzulassung.model.inline_response20013 import InlineResponse20013
from pprint import pprint
# Defining the host is optional and defaults to https://psm-api.bvl.bund.de/ords/psm/api-v1
# See configuration.py for a list of all supported configuration parameters.
configuration = pflanzenschutzmittelzulassung.Configuration(
    host = "https://psm-api.bvl.bund.de/ords/psm/api-v1"
)


# Enter a context with an instance of the API client
with pflanzenschutzmittelzulassung.ApiClient() as api_client:
    # Create an instance of the API class
    api_instance = default_api.DefaultApi(api_client)
    awg_wartezeit_nr = "awg_wartezeit_nr_example" # str | Implicit parameter (optional)
    kultur = "kultur_example" # str | Implicit parameter (optional)

    # example passing only required values which don't have defaults set
    # and optional values
    try:
        api_response = api_instance.awg_wartezeit_ausg_kultur_get(awg_wartezeit_nr=awg_wartezeit_nr, kultur=kultur)
        pprint(api_response)
    except pflanzenschutzmittelzulassung.ApiException as e:
        print("Exception when calling DefaultApi->awg_wartezeit_ausg_kultur_get: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **awg_wartezeit_nr** | **str**| Implicit parameter | [optional]
 **kultur** | **str**| Implicit parameter | [optional]

### Return type

[**InlineResponse20013**](InlineResponse20013.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The queried record. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **awg_wartezeit_get**
> InlineResponse20012 awg_wartezeit_get()



Liefert die Zuordnung von Anwendungen zu Wartezeiten in Tagen fÃ¼r eine bestimmte Kultur, bis die Anwendung erneut durchgefÃ¼hrt werden kann. Ausgenommene Kulturen sind Ã¼ber den Endpunkt /awg_wartezeit_ausg_kultur abzurufen. Genutzt wird fÃ¼r die Bemerkungen Kodeliste 89, dekodierbar Ã¼ber den Endpunkt /kode.                             Optional kann nach der Wartezeit ID {awg_wartezeit_nr}, der Anwendungs ID {awg_id} oder der Kultur {kultur} gefiltert werden.                             Die Paramter sind optional; werden keine Parameter Ã¼bergeben, enthÃ¤lt die RÃ¼ckgabe alle EintrÃ¤ge.      {awg_wartezeit_nr} ist der eindeutige Identifizierer der Zuordnung einer Anwendung zu einer Wartezeit. Ziffernfolge aus maximal 38 Ziffern, Bsp: 151592.     {awg_id} ist der Identifizierer einer Anwendung, referenziert aus dem Endpunkt /awg. Zeichenfolge aus 16 Zeichen, Bsp: 033274-64/02-001.     {kultur} ist der Kode der behandelten Kultur, referenziert aus dem Endpunkt /kultur_gruppe. Zeichenfolge aus maximal 20 Zeichen, Bsp: FRAAN.  Wenn auf andere Parameter gefiltert oder Teilabfragen gestellt werden sollen, kÃ¶nnen gesonderte Filtermethoden verwendet werden. Siehe dazu Abschnitt &quot;*JSON Queries*&quot; in der oberen allgemeinen API Beschreibung

### Example


```python
import time
from deutschland import pflanzenschutzmittelzulassung
from deutschland.pflanzenschutzmittelzulassung.api import default_api
from deutschland.pflanzenschutzmittelzulassung.model.inline_response20012 import InlineResponse20012
from pprint import pprint
# Defining the host is optional and defaults to https://psm-api.bvl.bund.de/ords/psm/api-v1
# See configuration.py for a list of all supported configuration parameters.
configuration = pflanzenschutzmittelzulassung.Configuration(
    host = "https://psm-api.bvl.bund.de/ords/psm/api-v1"
)


# Enter a context with an instance of the API client
with pflanzenschutzmittelzulassung.ApiClient() as api_client:
    # Create an instance of the API class
    api_instance = default_api.DefaultApi(api_client)
    awg_id = "awg_id_example" # str | Implicit parameter (optional)
    awg_wartezeit_nr = "awg_wartezeit_nr_example" # str | Implicit parameter (optional)
    kultur = "kultur_example" # str | Implicit parameter (optional)

    # example passing only required values which don't have defaults set
    # and optional values
    try:
        api_response = api_instance.awg_wartezeit_get(awg_id=awg_id, awg_wartezeit_nr=awg_wartezeit_nr, kultur=kultur)
        pprint(api_response)
    except pflanzenschutzmittelzulassung.ApiException as e:
        print("Exception when calling DefaultApi->awg_wartezeit_get: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **awg_id** | **str**| Implicit parameter | [optional]
 **awg_wartezeit_nr** | **str**| Implicit parameter | [optional]
 **kultur** | **str**| Implicit parameter | [optional]

### Return type

[**InlineResponse20012**](InlineResponse20012.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The queried record. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **awg_zeitpunkt_get**
> InlineResponse20014 awg_zeitpunkt_get()



Liefert die Zuordnung von Anwendungen zu Zeitpunkten. Es kann mehrere Zeitpunkte pro Anwendung geben, die Ã¼ber das Feld &quot;operand_zu_vorher&quot; aneinandergefÃ¼gt werden in der Reihenfolge nach &quot;sortier_nr&quot;. Die Zeitpunkte sind Ã¼ber Kodeliste 30 kodiert, die Ã¼ber den Endpunkt /kode dekodiert werden kÃ¶nnen.                             Optional kann auf eine Anwendung {awg_id} gefiltert werden.                             Der Paramter ist optional; werden keine Parameter Ã¼bergeben, enthÃ¤lt die RÃ¼ckgabe alle EintrÃ¤ge.      Der eindeutige Identifizierer bestimmt sich aus der awg_id, und dem zeitpunkt.     {awg_id} ist der Identifizierer einer Anwendung, referenziert aus dem Endpunkt /awg. Zeichenfolge aus 16 Zeichen, Bsp: 024560-64/04-025.  Wenn auf andere Parameter gefiltert oder Teilabfragen gestellt werden sollen, kÃ¶nnen gesonderte Filtermethoden verwendet werden. Siehe dazu Abschnitt &quot;*JSON Queries*&quot; in der oberen allgemeinen API Beschreibung

### Example


```python
import time
from deutschland import pflanzenschutzmittelzulassung
from deutschland.pflanzenschutzmittelzulassung.api import default_api
from deutschland.pflanzenschutzmittelzulassung.model.inline_response20014 import InlineResponse20014
from pprint import pprint
# Defining the host is optional and defaults to https://psm-api.bvl.bund.de/ords/psm/api-v1
# See configuration.py for a list of all supported configuration parameters.
configuration = pflanzenschutzmittelzulassung.Configuration(
    host = "https://psm-api.bvl.bund.de/ords/psm/api-v1"
)


# Enter a context with an instance of the API client
with pflanzenschutzmittelzulassung.ApiClient() as api_client:
    # Create an instance of the API class
    api_instance = default_api.DefaultApi(api_client)
    awg_id = "awg_id_example" # str | Implicit parameter (optional)

    # example passing only required values which don't have defaults set
    # and optional values
    try:
        api_response = api_instance.awg_zeitpunkt_get(awg_id=awg_id)
        pprint(api_response)
    except pflanzenschutzmittelzulassung.ApiException as e:
        print("Exception when calling DefaultApi->awg_zeitpunkt_get: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **awg_id** | **str**| Implicit parameter | [optional]

### Return type

[**InlineResponse20014**](InlineResponse20014.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The queried record. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **awg_zulassung_get**
> InlineResponse20015 awg_zulassung_get()



Liefert die Zuordnung von Anwendungen zu ihrem Zulassungsende.                             Optional kann nach deiner Anwendung {awg_id} gefiltert werden.                             Der Paramter ist optional; werden keine Parameter Ã¼bergeben, enthÃ¤lt die RÃ¼ckgabe alle EintrÃ¤ge.      {awg_id} ist der eindeutige Identifizierer einer Anwendung, referenziert aus dem Endpunkt /awg. Zeichenfolge aus 16 Zeichen, Bsp: 026865-00/00-002.  Wenn auf andere Parameter gefiltert oder Teilabfragen gestellt werden sollen, kÃ¶nnen gesonderte Filtermethoden verwendet werden. Siehe dazu Abschnitt &quot;*JSON Queries*&quot; in der oberen allgemeinen API Beschreibung

### Example


```python
import time
from deutschland import pflanzenschutzmittelzulassung
from deutschland.pflanzenschutzmittelzulassung.api import default_api
from deutschland.pflanzenschutzmittelzulassung.model.inline_response20015 import InlineResponse20015
from pprint import pprint
# Defining the host is optional and defaults to https://psm-api.bvl.bund.de/ords/psm/api-v1
# See configuration.py for a list of all supported configuration parameters.
configuration = pflanzenschutzmittelzulassung.Configuration(
    host = "https://psm-api.bvl.bund.de/ords/psm/api-v1"
)


# Enter a context with an instance of the API client
with pflanzenschutzmittelzulassung.ApiClient() as api_client:
    # Create an instance of the API class
    api_instance = default_api.DefaultApi(api_client)
    awg_id = "awg_id_example" # str | Implicit parameter (optional)

    # example passing only required values which don't have defaults set
    # and optional values
    try:
        api_response = api_instance.awg_zulassung_get(awg_id=awg_id)
        pprint(api_response)
    except pflanzenschutzmittelzulassung.ApiException as e:
        print("Exception when calling DefaultApi->awg_zulassung_get: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **awg_id** | **str**| Implicit parameter | [optional]

### Return type

[**InlineResponse20015**](InlineResponse20015.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The queried record. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **ghs_gefahrenhinweise_get**
> InlineResponse20016 ghs_gefahrenhinweise_get()



Liefert eine Zuordnung von Mitteln zu ihren Gefahrenhinweisen. Die Gefahrenhinweise verwenden die Kodeliste 70 und kÃ¶nnen dekodiert werden Ã¼ber den Endpunkt /kode.                             Optional kann auf ein Mittel {kennr} gefiltert werden.                             Die Hinweise entspringen dem &quot;Global harmonisierten System zur Einstufung und Kennzeichnung von Chemikalien&quot;, kurz GHS.                             Der Paramter ist optional; werden keine Parameter Ã¼bergeben, enthÃ¤lt die RÃ¼ckgabe alle EintrÃ¤ge.      Der eindeutige Identifizierer bestimmt sich aus allen Attributen des Endpunkts.     {kennr} ist die Kennummer eines Mittels, referenziert aus dem Endpunkt /mittel. Zeichenfolge aus 9 Zeichen, Bsp: 024780-67.  Wenn auf andere Parameter gefiltert oder Teilabfragen gestellt werden sollen, kÃ¶nnen gesonderte Filtermethoden verwendet werden. Siehe dazu Abschnitt &quot;*JSON Queries*&quot; in der oberen allgemeinen API Beschreibung

### Example


```python
import time
from deutschland import pflanzenschutzmittelzulassung
from deutschland.pflanzenschutzmittelzulassung.api import default_api
from deutschland.pflanzenschutzmittelzulassung.model.inline_response20016 import InlineResponse20016
from pprint import pprint
# Defining the host is optional and defaults to https://psm-api.bvl.bund.de/ords/psm/api-v1
# See configuration.py for a list of all supported configuration parameters.
configuration = pflanzenschutzmittelzulassung.Configuration(
    host = "https://psm-api.bvl.bund.de/ords/psm/api-v1"
)


# Enter a context with an instance of the API client
with pflanzenschutzmittelzulassung.ApiClient() as api_client:
    # Create an instance of the API class
    api_instance = default_api.DefaultApi(api_client)
    kennr = "kennr_example" # str | Implicit parameter (optional)

    # example passing only required values which don't have defaults set
    # and optional values
    try:
        api_response = api_instance.ghs_gefahrenhinweise_get(kennr=kennr)
        pprint(api_response)
    except pflanzenschutzmittelzulassung.ApiException as e:
        print("Exception when calling DefaultApi->ghs_gefahrenhinweise_get: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **kennr** | **str**| Implicit parameter | [optional]

### Return type

[**InlineResponse20016**](InlineResponse20016.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The queried record. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **ghs_gefahrensymbole_get**
> InlineResponse20017 ghs_gefahrensymbole_get()



Liefert eine Zuordnung von Mitteln zu ihren Gefahrensymbolen. Die Gefahrensymbole verwenden die Kodeliste 40 und kÃ¶nnen dekodiert werden Ã¼ber den Endpunkt /kode.                             Optional kann auf ein Mittel {kennr} gefiltert werden.                             Die Symbole entspringen dem &quot;Global harmonisierten System zur Einstufung und Kennzeichnung von Chemikalien&quot;, kurz GHS.                             Der Paramter ist optional; werden keine Parameter Ã¼bergeben, enthÃ¤lt die RÃ¼ckgabe alle EintrÃ¤ge.      Der eindeutige Identifizierer bestimmt sich aus allen Attributen des Endpunkts.     {kennr} ist die Kennummer eines Mittels, referenziert aus dem Endpunkt /mittel. Zeichenfolge aus 9 Zeichen, Bsp: 026557-00.  Wenn auf andere Parameter gefiltert oder Teilabfragen gestellt werden sollen, kÃ¶nnen gesonderte Filtermethoden verwendet werden. Siehe dazu Abschnitt &quot;*JSON Queries*&quot; in der oberen allgemeinen API Beschreibung

### Example


```python
import time
from deutschland import pflanzenschutzmittelzulassung
from deutschland.pflanzenschutzmittelzulassung.api import default_api
from deutschland.pflanzenschutzmittelzulassung.model.inline_response20017 import InlineResponse20017
from pprint import pprint
# Defining the host is optional and defaults to https://psm-api.bvl.bund.de/ords/psm/api-v1
# See configuration.py for a list of all supported configuration parameters.
configuration = pflanzenschutzmittelzulassung.Configuration(
    host = "https://psm-api.bvl.bund.de/ords/psm/api-v1"
)


# Enter a context with an instance of the API client
with pflanzenschutzmittelzulassung.ApiClient() as api_client:
    # Create an instance of the API class
    api_instance = default_api.DefaultApi(api_client)
    kennr = "kennr_example" # str | Implicit parameter (optional)

    # example passing only required values which don't have defaults set
    # and optional values
    try:
        api_response = api_instance.ghs_gefahrensymbole_get(kennr=kennr)
        pprint(api_response)
    except pflanzenschutzmittelzulassung.ApiException as e:
        print("Exception when calling DefaultApi->ghs_gefahrensymbole_get: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **kennr** | **str**| Implicit parameter | [optional]

### Return type

[**InlineResponse20017**](InlineResponse20017.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The queried record. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **ghs_sicherheitshinweise_get**
> InlineResponse20018 ghs_sicherheitshinweise_get()



Liefert eine Zuordnung von Mitteln zu ihren Sicherheitshinweisen. Die Sicherheitshinweise verwenden die Kodeliste 71 und kÃ¶nnen dekodiert werden Ã¼ber den Endpunkt /kode.                             Optional kann auf ein Mittel {kennr} gefiltert werden.                             Die Hinweise entspringen dem &quot;Global harmonisierten System zur Einstufung und Kennzeichnung von Chemikalien&quot;, kurz GHS.                             Der Paramter ist optional; werden keine Parameter Ã¼bergeben, enthÃ¤lt die RÃ¼ckgabe alle EintrÃ¤ge.      Der eindeutige Identifizierer bestimmt sich aus allen Attributen des Endpunkts.     {kennr} ist die Kennummer eines Mittels, referenziert aus dem Endpunkt /mittel. Zeichenfolge aus 9 Zeichen, Bsp: 024350-61.  Wenn auf andere Parameter gefiltert oder Teilabfragen gestellt werden sollen, kÃ¶nnen gesonderte Filtermethoden verwendet werden. Siehe dazu Abschnitt &quot;*JSON Queries*&quot; in der oberen allgemeinen API Beschreibung

### Example


```python
import time
from deutschland import pflanzenschutzmittelzulassung
from deutschland.pflanzenschutzmittelzulassung.api import default_api
from deutschland.pflanzenschutzmittelzulassung.model.inline_response20018 import InlineResponse20018
from pprint import pprint
# Defining the host is optional and defaults to https://psm-api.bvl.bund.de/ords/psm/api-v1
# See configuration.py for a list of all supported configuration parameters.
configuration = pflanzenschutzmittelzulassung.Configuration(
    host = "https://psm-api.bvl.bund.de/ords/psm/api-v1"
)


# Enter a context with an instance of the API client
with pflanzenschutzmittelzulassung.ApiClient() as api_client:
    # Create an instance of the API class
    api_instance = default_api.DefaultApi(api_client)
    kennr = "kennr_example" # str | Implicit parameter (optional)

    # example passing only required values which don't have defaults set
    # and optional values
    try:
        api_response = api_instance.ghs_sicherheitshinweise_get(kennr=kennr)
        pprint(api_response)
    except pflanzenschutzmittelzulassung.ApiException as e:
        print("Exception when calling DefaultApi->ghs_sicherheitshinweise_get: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **kennr** | **str**| Implicit parameter | [optional]

### Return type

[**InlineResponse20018**](InlineResponse20018.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The queried record. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **ghs_signalwoerter_get**
> InlineResponse20019 ghs_signalwoerter_get()



Liefert eine Zuordnung von Mitteln zu ihren SignalwÃ¶rtern. Die SignalwÃ¶rter verwenden die Kodeliste 76 und kÃ¶nnen dekodiert werden Ã¼ber den Endpunkt /kode.                             Optional kann auf ein Mittel {kennr} gefiltert werden.                             Die WÃ¶rter entspringen dem &quot;Global harmonisierten System zur Einstufung und Kennzeichnung von Chemikalien&quot;, kurz GHS.                             Der Paramter ist optional; werden keine Parameter Ã¼bergeben, enthÃ¤lt die RÃ¼ckgabe alle EintrÃ¤ge.      Der eindeutige Identifizierer bestimmt sich aus allen Attributen des Endpunkts.     {kennr} ist die Kennummer eines Mittels, referenziert aus dem Endpunkt /mittel. Zeichenfolge aus 9 Zeichen, Bsp: 008263-00.  Wenn auf andere Parameter gefiltert oder Teilabfragen gestellt werden sollen, kÃ¶nnen gesonderte Filtermethoden verwendet werden. Siehe dazu Abschnitt &quot;*JSON Queries*&quot; in der oberen allgemeinen API Beschreibung

### Example


```python
import time
from deutschland import pflanzenschutzmittelzulassung
from deutschland.pflanzenschutzmittelzulassung.api import default_api
from deutschland.pflanzenschutzmittelzulassung.model.inline_response20019 import InlineResponse20019
from pprint import pprint
# Defining the host is optional and defaults to https://psm-api.bvl.bund.de/ords/psm/api-v1
# See configuration.py for a list of all supported configuration parameters.
configuration = pflanzenschutzmittelzulassung.Configuration(
    host = "https://psm-api.bvl.bund.de/ords/psm/api-v1"
)


# Enter a context with an instance of the API client
with pflanzenschutzmittelzulassung.ApiClient() as api_client:
    # Create an instance of the API class
    api_instance = default_api.DefaultApi(api_client)
    kennr = "kennr_example" # str | Implicit parameter (optional)

    # example passing only required values which don't have defaults set
    # and optional values
    try:
        api_response = api_instance.ghs_signalwoerter_get(kennr=kennr)
        pprint(api_response)
    except pflanzenschutzmittelzulassung.ApiException as e:
        print("Exception when calling DefaultApi->ghs_signalwoerter_get: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **kennr** | **str**| Implicit parameter | [optional]

### Return type

[**InlineResponse20019**](InlineResponse20019.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The queried record. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **hinweis_get**
> InlineResponse20020 hinweis_get()



Liefert eine Zuordnung von Ebenen (Mitteln und Anwendungen) zu Hinweisen. Die Hinweise verwenden die Kodeliste 74 und kÃ¶nnen dekodiert werden Ã¼ber den Endpunkt /kode.                             Optional kann nach einer Ebene {ebene} (einem Mittel/einer Anwendung) gefiltert werden.                             Der Paramter ist optional; werden keine Parameter Ã¼bergeben enthÃ¤lt die RÃ¼ckgabe alle EintrÃ¤ge.      Der eindeutige Identifizierer bestimmt sich aus der {ebene} und dem hinweis.     {ebene} ist entweder die Kennnummer eines Mittels (kennr im /mittel Endpunkt, 9 Zeichen) oder der Identifizierer einer Anwendung (awg_id im /awg Endpunkt, 16 Zeichen). Zeichenkette aus maximal 16 Zeichen, Bsp: 027821-61.  Wenn auf andere Parameter gefiltert oder Teilabfragen gestellt werden sollen, kÃ¶nnen gesonderte Filtermethoden verwendet werden. Siehe dazu Abschnitt &quot;*JSON Queries*&quot; in der oberen allgemeinen API Beschreibung

### Example


```python
import time
from deutschland import pflanzenschutzmittelzulassung
from deutschland.pflanzenschutzmittelzulassung.api import default_api
from deutschland.pflanzenschutzmittelzulassung.model.inline_response20020 import InlineResponse20020
from pprint import pprint
# Defining the host is optional and defaults to https://psm-api.bvl.bund.de/ords/psm/api-v1
# See configuration.py for a list of all supported configuration parameters.
configuration = pflanzenschutzmittelzulassung.Configuration(
    host = "https://psm-api.bvl.bund.de/ords/psm/api-v1"
)


# Enter a context with an instance of the API client
with pflanzenschutzmittelzulassung.ApiClient() as api_client:
    # Create an instance of the API class
    api_instance = default_api.DefaultApi(api_client)
    ebene = "ebene_example" # str | Implicit parameter (optional)

    # example passing only required values which don't have defaults set
    # and optional values
    try:
        api_response = api_instance.hinweis_get(ebene=ebene)
        pprint(api_response)
    except pflanzenschutzmittelzulassung.ApiException as e:
        print("Exception when calling DefaultApi->hinweis_get: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ebene** | **str**| Implicit parameter | [optional]

### Return type

[**InlineResponse20020**](InlineResponse20020.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The queried record. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **kode_get**
> InlineResponse20021 kode_get()



Liefert die Zuordnung von Kodes, Kodelisten und Sprache auf den Kodetext. Verwendet zur Dekodierung verschiedener Kodes aus anderen Tabellen.                             Optional kann auf einen Kode, die dazugehÃ¶rige Kodeliste und/oder eine Sprache gefiltert werden.                             Die Paramter sind optional; werden keine Parameter Ã¼bergeben, enthÃ¤lt die RÃ¼ckgabe alle EintrÃ¤ge.      Der eindeutige Identifizierer bestimmt sich aus dem {kode}, der {kodeliste} und der {sprache}.     {kode} ist ein Kode, der in anderen Tabellen als Kodierung fÃ¼r Werte verwendet wird. Zeichenkette aus maximal 20 Zeichen, Bsp: ASPOF.     {kodeliste} ist die Nummer der Liste, der der ensprechende Kode entnommen ist. Die Bedeutung der Liste kann dem Endpoint /kodeliste entnommen werden. Ziffernfolge aus maximal 3 Ziffern, Bsp: 948.     {sprache} ist die Sprache in der der Kodetext geliefert werden soll. Aktuell bereitgestellt werden DE, GB und teilweise VA (Latein). Zeichenkette aus maximal 20 Zeichen, Bsp: DE.  Wenn auf andere Parameter gefiltert oder Teilabfragen gestellt werden sollen, kÃ¶nnen gesonderte Filtermethoden verwendet werden. Siehe dazu Abschnitt &quot;*JSON Queries*&quot; in der oberen allgemeinen API Beschreibung

### Example


```python
import time
from deutschland import pflanzenschutzmittelzulassung
from deutschland.pflanzenschutzmittelzulassung.api import default_api
from deutschland.pflanzenschutzmittelzulassung.model.inline_response20021 import InlineResponse20021
from pprint import pprint
# Defining the host is optional and defaults to https://psm-api.bvl.bund.de/ords/psm/api-v1
# See configuration.py for a list of all supported configuration parameters.
configuration = pflanzenschutzmittelzulassung.Configuration(
    host = "https://psm-api.bvl.bund.de/ords/psm/api-v1"
)


# Enter a context with an instance of the API client
with pflanzenschutzmittelzulassung.ApiClient() as api_client:
    # Create an instance of the API class
    api_instance = default_api.DefaultApi(api_client)
    kode = "kode_example" # str | Implicit parameter (optional)
    kodeliste = "kodeliste_example" # str | Implicit parameter (optional)
    sprache = "sprache_example" # str | Implicit parameter (optional)

    # example passing only required values which don't have defaults set
    # and optional values
    try:
        api_response = api_instance.kode_get(kode=kode, kodeliste=kodeliste, sprache=sprache)
        pprint(api_response)
    except pflanzenschutzmittelzulassung.ApiException as e:
        print("Exception when calling DefaultApi->kode_get: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **kode** | **str**| Implicit parameter | [optional]
 **kodeliste** | **str**| Implicit parameter | [optional]
 **sprache** | **str**| Implicit parameter | [optional]

### Return type

[**InlineResponse20021**](InlineResponse20021.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The queried record. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **kodeliste_feldname_get**
> InlineResponse20023 kodeliste_feldname_get()



Liefert eine Zuordnung von Kodelistennummer auf die Tabelle und das Feld in dem diese Kodeliste verwendet wird.                             Optional kann nach Kodelistennummer {kodeliste} und/oder Tabellennamen {tabelle} und/oder Spaltennamen {feldname} gefiltert werden.                             Die Paramter sind optional; werden keine Parameter Ã¼bergeben, enthÃ¤lt die RÃ¼ckgabe alle EintrÃ¤ge.      Der eindeutige Identifizierer bestimmt sich aus der {tabelle}, der {kodeliste} und dem {feldname}.     {tabelle} ist der Name einer Tabelle, in der eine Kodeliste verwendet wird. Zeichenkette aus maximal 30 Zeichen, Bsp: ADRESSE.     {kodeliste} ist die Nummer der Liste, die in der Spalte verwendet wird. Ziffernfolge aus maximal 3 Ziffern, Bsp: 3.     {feldname} ist der Name der Spalte, in der eine Kodeliste verwendet wird. Zeichenkette aus maximal 30 Zeichen, Bsp: LAND.  Wenn auf andere Parameter gefiltert oder Teilabfragen gestellt werden sollen, kÃ¶nnen gesonderte Filtermethoden verwendet werden. Siehe dazu Abschnitt &quot;*JSON Queries*&quot; in der oberen allgemeinen API Beschreibung

### Example


```python
import time
from deutschland import pflanzenschutzmittelzulassung
from deutschland.pflanzenschutzmittelzulassung.api import default_api
from deutschland.pflanzenschutzmittelzulassung.model.inline_response20023 import InlineResponse20023
from pprint import pprint
# Defining the host is optional and defaults to https://psm-api.bvl.bund.de/ords/psm/api-v1
# See configuration.py for a list of all supported configuration parameters.
configuration = pflanzenschutzmittelzulassung.Configuration(
    host = "https://psm-api.bvl.bund.de/ords/psm/api-v1"
)


# Enter a context with an instance of the API client
with pflanzenschutzmittelzulassung.ApiClient() as api_client:
    # Create an instance of the API class
    api_instance = default_api.DefaultApi(api_client)
    feldname = "feldname_example" # str | Implicit parameter (optional)
    kodeliste = "kodeliste_example" # str | Implicit parameter (optional)
    tabelle = "tabelle_example" # str | Implicit parameter (optional)

    # example passing only required values which don't have defaults set
    # and optional values
    try:
        api_response = api_instance.kodeliste_feldname_get(feldname=feldname, kodeliste=kodeliste, tabelle=tabelle)
        pprint(api_response)
    except pflanzenschutzmittelzulassung.ApiException as e:
        print("Exception when calling DefaultApi->kodeliste_feldname_get: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **feldname** | **str**| Implicit parameter | [optional]
 **kodeliste** | **str**| Implicit parameter | [optional]
 **tabelle** | **str**| Implicit parameter | [optional]

### Return type

[**InlineResponse20023**](InlineResponse20023.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The queried record. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **kodeliste_get**
> InlineResponse20022 kodeliste_get()



Liefert eine Auflistung der Kodelisten inklusive dem Listennamen, also der testlichen Beschreibung wofÃ¼r die Liste steht.                             Optional kann nut auf eine Kodeliste {kodeliste} gefiltert werden.                             Die Paramter sind optional; werden keine Parameter Ã¼bergeben, enthÃ¤lt die RÃ¼ckgabe alle EintrÃ¤ge.      {kodeliste} ist der eindeutige Identifizierer der Liste. Ziffernfolge aus maximal 3 Ziffern, Bsp: 3.  Wenn auf andere Parameter gefiltert oder Teilabfragen gestellt werden sollen, kÃ¶nnen gesonderte Filtermethoden verwendet werden. Siehe dazu Abschnitt &quot;*JSON Queries*&quot; in der oberen allgemeinen API Beschreibung

### Example


```python
import time
from deutschland import pflanzenschutzmittelzulassung
from deutschland.pflanzenschutzmittelzulassung.api import default_api
from deutschland.pflanzenschutzmittelzulassung.model.inline_response20022 import InlineResponse20022
from pprint import pprint
# Defining the host is optional and defaults to https://psm-api.bvl.bund.de/ords/psm/api-v1
# See configuration.py for a list of all supported configuration parameters.
configuration = pflanzenschutzmittelzulassung.Configuration(
    host = "https://psm-api.bvl.bund.de/ords/psm/api-v1"
)


# Enter a context with an instance of the API client
with pflanzenschutzmittelzulassung.ApiClient() as api_client:
    # Create an instance of the API class
    api_instance = default_api.DefaultApi(api_client)
    kodeliste = "kodeliste_example" # str | Implicit parameter (optional)

    # example passing only required values which don't have defaults set
    # and optional values
    try:
        api_response = api_instance.kodeliste_get(kodeliste=kodeliste)
        pprint(api_response)
    except pflanzenschutzmittelzulassung.ApiException as e:
        print("Exception when calling DefaultApi->kodeliste_get: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **kodeliste** | **str**| Implicit parameter | [optional]

### Return type

[**InlineResponse20022**](InlineResponse20022.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The queried record. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **kultur_gruppe_get**
> InlineResponse20024 kultur_gruppe_get()



Liefert eine Liste der Kulturen und der korrespondierenden Kulturgruppe. Der Enpunkt ist eine ReprÃ¤sentation einer Baumstruktur. kultur_gruppe ist dabei ein Parent, dem das Child kultur zugeordnet ist. Eine Kulturgruppe kann mehrere Kulturen als Children besitzen, eine Kultur kann mehrere Parents haben. Da der Baum mehrere Stufen hat, stehen einige Kulturen als Child (kultur) UND als Parent (kultur_gruppe) in unterschiedlichen Zeilen.                             Optional kann auf eine Kultur {kultur} oder eine Kulturgruppe {kultur_gruppe} gefiltert werden.                             Bei einer Ã¼bergebenen {kultur} enthÃ¤lt die RÃ¼ckgabe nur die direkten Parents, also Kulturgruppen zu der korrepondierenden Kultur.                             Bei einer Ã¼bergebenen {kultur_gruppe} enthÃ¤lt die RÃ¼ckgabe nur die direkten Children, also Kulturen zu der korrepondierenden Kulturgruppe.                             Die Paramter sind optional; werden keine Parameter Ã¼bergeben, enthÃ¤lt die RÃ¼ckgabe alle EintrÃ¤ge.      Der eindeutige Identifizierer bestimmt sich aus der {kultur}, und der {kultur_gruppe}.     {kultur} ist der Kode einer Kultur (Child). Zeichenkette aus maximal 20 Zeichen, Bsp: CAFPA.     {kulturgruppe} ist der Kode der Kulturgruppe der zugeordneten Kultur (Parent). Zeichenkette aus maximal 20 Zeichen, Bsp: NNNZT.  Wenn auf andere Parameter gefiltert oder Teilabfragen gestellt werden sollen, kÃ¶nnen gesonderte Filtermethoden verwendet werden. Siehe dazu Abschnitt &quot;*JSON Queries*&quot; in der oberen allgemeinen API Beschreibung

### Example


```python
import time
from deutschland import pflanzenschutzmittelzulassung
from deutschland.pflanzenschutzmittelzulassung.api import default_api
from deutschland.pflanzenschutzmittelzulassung.model.inline_response20024 import InlineResponse20024
from pprint import pprint
# Defining the host is optional and defaults to https://psm-api.bvl.bund.de/ords/psm/api-v1
# See configuration.py for a list of all supported configuration parameters.
configuration = pflanzenschutzmittelzulassung.Configuration(
    host = "https://psm-api.bvl.bund.de/ords/psm/api-v1"
)


# Enter a context with an instance of the API client
with pflanzenschutzmittelzulassung.ApiClient() as api_client:
    # Create an instance of the API class
    api_instance = default_api.DefaultApi(api_client)
    kultur = "kultur_example" # str | Implicit parameter (optional)
    kultur_gruppe = "kultur_gruppe_example" # str | Implicit parameter (optional)

    # example passing only required values which don't have defaults set
    # and optional values
    try:
        api_response = api_instance.kultur_gruppe_get(kultur=kultur, kultur_gruppe=kultur_gruppe)
        pprint(api_response)
    except pflanzenschutzmittelzulassung.ApiException as e:
        print("Exception when calling DefaultApi->kultur_gruppe_get: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **kultur** | **str**| Implicit parameter | [optional]
 **kultur_gruppe** | **str**| Implicit parameter | [optional]

### Return type

[**InlineResponse20024**](InlineResponse20024.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The queried record. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **mittel_abgelaufen_get**
> InlineResponse20026 mittel_abgelaufen_get()



Liefert eine Liste der abgelaufenen Pflanzenschutzmittel, inklusive Aufbrauchfrist. Weitere Informationen sind nur unter den Endpunkten /wirkstoff und /wirkstoff_gehalt enthalten. Andere Referenzen wurden entfernt.                           Optional kann auf eine Kennummer {kennr} gefiltert werden.                           Der Paramter ist optional; werden keine Parameter Ã¼bergeben, enthÃ¤lt die RÃ¼ckgabe alle EintrÃ¤ge.          {kennr} ist der eindeutige Identifizierer, die Kennummer eines abgelaufenen Mittels. Zeichenkette aus 9 Zeichen, Bsp: 050023-61.  Wenn auf andere Parameter gefiltert oder Teilabfragen gestellt werden sollen, kÃ¶nnen gesonderte Filtermethoden verwendet werden. Siehe dazu Abschnitt &quot;*JSON Queries*&quot; in der oberen allgemeinen API Beschreibung

### Example


```python
import time
from deutschland import pflanzenschutzmittelzulassung
from deutschland.pflanzenschutzmittelzulassung.api import default_api
from deutschland.pflanzenschutzmittelzulassung.model.inline_response20026 import InlineResponse20026
from pprint import pprint
# Defining the host is optional and defaults to https://psm-api.bvl.bund.de/ords/psm/api-v1
# See configuration.py for a list of all supported configuration parameters.
configuration = pflanzenschutzmittelzulassung.Configuration(
    host = "https://psm-api.bvl.bund.de/ords/psm/api-v1"
)


# Enter a context with an instance of the API client
with pflanzenschutzmittelzulassung.ApiClient() as api_client:
    # Create an instance of the API class
    api_instance = default_api.DefaultApi(api_client)
    kennr = "kennr_example" # str | Implicit parameter (optional)

    # example passing only required values which don't have defaults set
    # and optional values
    try:
        api_response = api_instance.mittel_abgelaufen_get(kennr=kennr)
        pprint(api_response)
    except pflanzenschutzmittelzulassung.ApiException as e:
        print("Exception when calling DefaultApi->mittel_abgelaufen_get: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **kennr** | **str**| Implicit parameter | [optional]

### Return type

[**InlineResponse20026**](InlineResponse20026.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The queried record. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **mittel_abpackung_get**
> InlineResponse20027 mittel_abpackung_get()



Liefert eine Liste der Packungsinformationen fÃ¼r Mittel.                           Optional kann auf die Kennummer eines Mittels {kennr} gefiltert werden.                           Der Paramter ist optional; werden keine Parameter Ã¼bergeben, enthÃ¤lt die RÃ¼ckgabe alle EintrÃ¤ge.          Der eindeutige Identifizierer setzt sich aus allen Attributen des Endpunkts zusammen.         {kennr} ist die Kennummer eines Mittels, referenziert aus dem Endpunkt /mittel. Zeichenkette aus 9 Zeichen, Bsp: 033274-64.  Wenn auf andere Parameter gefiltert oder Teilabfragen gestellt werden sollen, kÃ¶nnen gesonderte Filtermethoden verwendet werden. Siehe dazu Abschnitt &quot;*JSON Queries*&quot; in der oberen allgemeinen API Beschreibung

### Example


```python
import time
from deutschland import pflanzenschutzmittelzulassung
from deutschland.pflanzenschutzmittelzulassung.api import default_api
from deutschland.pflanzenschutzmittelzulassung.model.inline_response20027 import InlineResponse20027
from pprint import pprint
# Defining the host is optional and defaults to https://psm-api.bvl.bund.de/ords/psm/api-v1
# See configuration.py for a list of all supported configuration parameters.
configuration = pflanzenschutzmittelzulassung.Configuration(
    host = "https://psm-api.bvl.bund.de/ords/psm/api-v1"
)


# Enter a context with an instance of the API client
with pflanzenschutzmittelzulassung.ApiClient() as api_client:
    # Create an instance of the API class
    api_instance = default_api.DefaultApi(api_client)
    kennr = "kennr_example" # str | Implicit parameter (optional)

    # example passing only required values which don't have defaults set
    # and optional values
    try:
        api_response = api_instance.mittel_abpackung_get(kennr=kennr)
        pprint(api_response)
    except pflanzenschutzmittelzulassung.ApiException as e:
        print("Exception when calling DefaultApi->mittel_abpackung_get: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **kennr** | **str**| Implicit parameter | [optional]

### Return type

[**InlineResponse20027**](InlineResponse20027.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The queried record. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **mittel_gefahren_symbol_get**
> InlineResponse20028 mittel_gefahren_symbol_get()



Liefert eine Zuordnung von Mitteln zu Gefahrensymbolen.                           Optional kann auf eine Mittel Kennummer {kennr} gefiltert werden.                           Die Paramter sind optional; werden keine Parameter Ã¼bergeben, enthÃ¤lt die RÃ¼ckgabe alle EintrÃ¤ge.          Der eindeutige Identifizierer setzt sich aus der {kennr} und dem gefahren_symbol zusammen.         {kennr} ist die Kennummer eines Mittels, referenziert aus dem Endpunkt /mittel. Zeichenkette aus 9 Zeichen, Bsp: 006978-00.  Wenn auf andere Parameter gefiltert oder Teilabfragen gestellt werden sollen, kÃ¶nnen gesonderte Filtermethoden verwendet werden. Siehe dazu Abschnitt &quot;*JSON Queries*&quot; in der oberen allgemeinen API Beschreibung

### Example


```python
import time
from deutschland import pflanzenschutzmittelzulassung
from deutschland.pflanzenschutzmittelzulassung.api import default_api
from deutschland.pflanzenschutzmittelzulassung.model.inline_response20028 import InlineResponse20028
from pprint import pprint
# Defining the host is optional and defaults to https://psm-api.bvl.bund.de/ords/psm/api-v1
# See configuration.py for a list of all supported configuration parameters.
configuration = pflanzenschutzmittelzulassung.Configuration(
    host = "https://psm-api.bvl.bund.de/ords/psm/api-v1"
)


# Enter a context with an instance of the API client
with pflanzenschutzmittelzulassung.ApiClient() as api_client:
    # Create an instance of the API class
    api_instance = default_api.DefaultApi(api_client)
    kennr = "kennr_example" # str | Implicit parameter (optional)

    # example passing only required values which don't have defaults set
    # and optional values
    try:
        api_response = api_instance.mittel_gefahren_symbol_get(kennr=kennr)
        pprint(api_response)
    except pflanzenschutzmittelzulassung.ApiException as e:
        print("Exception when calling DefaultApi->mittel_gefahren_symbol_get: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **kennr** | **str**| Implicit parameter | [optional]

### Return type

[**InlineResponse20028**](InlineResponse20028.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The queried record. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **mittel_get**
> InlineResponse20025 mittel_get()



Liefert eine Liste aller zugelassenen Pflanzeschutzmittel.                           Optional kann auf eine Zulassungsnummer/Kennummer {kennr} gefiltert werden.                           Der Paramter ist optional; werden keine Parameter Ã¼bergeben, enthÃ¤lt die RÃ¼ckgabe alle EintrÃ¤ge.          {kennr} ist der eindeutige Identifizierer, die Kennummer/Zulassungsnummer eines Mittels. Zeichenkette aus 9 Zeichen, Bsp: 024213-73.  Wenn auf andere Parameter gefiltert oder Teilabfragen gestellt werden sollen, kÃ¶nnen gesonderte Filtermethoden verwendet werden. Siehe dazu Abschnitt &quot;*JSON Queries*&quot; in der oberen allgemeinen API Beschreibung

### Example


```python
import time
from deutschland import pflanzenschutzmittelzulassung
from deutschland.pflanzenschutzmittelzulassung.api import default_api
from deutschland.pflanzenschutzmittelzulassung.model.inline_response20025 import InlineResponse20025
from pprint import pprint
# Defining the host is optional and defaults to https://psm-api.bvl.bund.de/ords/psm/api-v1
# See configuration.py for a list of all supported configuration parameters.
configuration = pflanzenschutzmittelzulassung.Configuration(
    host = "https://psm-api.bvl.bund.de/ords/psm/api-v1"
)


# Enter a context with an instance of the API client
with pflanzenschutzmittelzulassung.ApiClient() as api_client:
    # Create an instance of the API class
    api_instance = default_api.DefaultApi(api_client)
    kennr = "kennr_example" # str | Implicit parameter (optional)

    # example passing only required values which don't have defaults set
    # and optional values
    try:
        api_response = api_instance.mittel_get(kennr=kennr)
        pprint(api_response)
    except pflanzenschutzmittelzulassung.ApiException as e:
        print("Exception when calling DefaultApi->mittel_get: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **kennr** | **str**| Implicit parameter | [optional]

### Return type

[**InlineResponse20025**](InlineResponse20025.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The queried record. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **mittel_vertrieb_get**
> InlineResponse20029 mittel_vertrieb_get()



Liefert die Zuordnung von Mitteln zu Vetriebsfirmen dieser Mittel.                           Optional kann auf ein Mittel {kennr} oder eine Vertriebsfirma {vertriebsfirma_nr} gefiltert werden.          Der eindeutige Identifizierer setzt sich aus der{kennr} und der {vertriebsfirma_nr} zusammen.         {kennr} ist die Kennummer eines Mittels, referenziert aus dem Endpunkt /mittel. Zeichenkette aus 9 Zeichen, Bsp: 00A502-00.         {vertriebsfirma_nr} ist die Nummer der Vertriebsfirma, referenziert aus dem Endpunkt /adresse. Ziffernfolge aus maximal 22 Ziffern, Bsp: 11281.  Wenn auf andere Parameter gefiltert oder Teilabfragen gestellt werden sollen, kÃ¶nnen gesonderte Filtermethoden verwendet werden. Siehe dazu Abschnitt &quot;*JSON Queries*&quot; in der oberen allgemeinen API Beschreibung

### Example


```python
import time
from deutschland import pflanzenschutzmittelzulassung
from deutschland.pflanzenschutzmittelzulassung.api import default_api
from deutschland.pflanzenschutzmittelzulassung.model.inline_response20029 import InlineResponse20029
from pprint import pprint
# Defining the host is optional and defaults to https://psm-api.bvl.bund.de/ords/psm/api-v1
# See configuration.py for a list of all supported configuration parameters.
configuration = pflanzenschutzmittelzulassung.Configuration(
    host = "https://psm-api.bvl.bund.de/ords/psm/api-v1"
)


# Enter a context with an instance of the API client
with pflanzenschutzmittelzulassung.ApiClient() as api_client:
    # Create an instance of the API class
    api_instance = default_api.DefaultApi(api_client)
    kennr = "kennr_example" # str | Implicit parameter (optional)
    vertriebsfirma_nr = "vertriebsfirma_nr_example" # str | Implicit parameter (optional)

    # example passing only required values which don't have defaults set
    # and optional values
    try:
        api_response = api_instance.mittel_vertrieb_get(kennr=kennr, vertriebsfirma_nr=vertriebsfirma_nr)
        pprint(api_response)
    except pflanzenschutzmittelzulassung.ApiException as e:
        print("Exception when calling DefaultApi->mittel_vertrieb_get: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **kennr** | **str**| Implicit parameter | [optional]
 **vertriebsfirma_nr** | **str**| Implicit parameter | [optional]

### Return type

[**InlineResponse20029**](InlineResponse20029.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The queried record. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **mittel_wirkbereich_get**
> InlineResponse20030 mittel_wirkbereich_get()



Liefert eine Liste von Zuordnungen von Mitteln zu Wirkbereichen. Die konkreten Anwendungen sind abgebildet in Endpunkt /awg. Das Feld &quot;wirkungsbereich&quot; nutzt die Kodeliste 21, die Ã¼ber den Endpunkt /kode dekodiert werden kann.                           Optional kann auf ein Mittel {kennr} oder einen  Wirkungsbereich {wirkungsbereich} gefiltert werden.                           Die Paramter sind optional; werden keine Parameter Ã¼bergeben, enthÃ¤lt die RÃ¼ckgabe alle EintrÃ¤ge.          Der eindeutige Identifizierer setzt sich aus der {kennr} und dem {wirkungsbreich} zusammen.         {kennr} ist die Kennummer eines Mittels, referenziert aus dem Endpunkt /mittel. Zeichenkette aus 9 Zeichen, Bsp: 006335-00.         {wirkungsbereich} ist der Kode fÃ¼r den Wirkungsbereich eines Mittels. Die Dekodierung lÃ¤uft Ã¼ber den Endpunkt /kode. Zeichenfolge aus 20 Zeichen, Bsp: F.  Wenn auf andere Parameter gefiltert oder Teilabfragen gestellt werden sollen, kÃ¶nnen gesonderte Filtermethoden verwendet werden. Siehe dazu Abschnitt &quot;*JSON Queries*&quot; in der oberen allgemeinen API Beschreibung

### Example


```python
import time
from deutschland import pflanzenschutzmittelzulassung
from deutschland.pflanzenschutzmittelzulassung.api import default_api
from deutschland.pflanzenschutzmittelzulassung.model.inline_response20030 import InlineResponse20030
from pprint import pprint
# Defining the host is optional and defaults to https://psm-api.bvl.bund.de/ords/psm/api-v1
# See configuration.py for a list of all supported configuration parameters.
configuration = pflanzenschutzmittelzulassung.Configuration(
    host = "https://psm-api.bvl.bund.de/ords/psm/api-v1"
)


# Enter a context with an instance of the API client
with pflanzenschutzmittelzulassung.ApiClient() as api_client:
    # Create an instance of the API class
    api_instance = default_api.DefaultApi(api_client)
    kennr = "kennr_example" # str | Implicit parameter (optional)
    wirkungsbereich = "wirkungsbereich_example" # str | Implicit parameter (optional)

    # example passing only required values which don't have defaults set
    # and optional values
    try:
        api_response = api_instance.mittel_wirkbereich_get(kennr=kennr, wirkungsbereich=wirkungsbereich)
        pprint(api_response)
    except pflanzenschutzmittelzulassung.ApiException as e:
        print("Exception when calling DefaultApi->mittel_wirkbereich_get: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **kennr** | **str**| Implicit parameter | [optional]
 **wirkungsbereich** | **str**| Implicit parameter | [optional]

### Return type

[**InlineResponse20030**](InlineResponse20030.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The queried record. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **parallelimport_abgelaufen_get**
> InlineResponse20031 parallelimport_abgelaufen_get()



Liefert eine Liste der abgelaufenen Parallelimporte (Mittel aus anderen LÃ¤ndern die identisch sind zu in Deutschland zugelassenen Mitteln) zu ihren Referenzmitteln.                           Optional kann auf ein Referenzmittel {pi_referenz_kennr} oder einen Importeur {importeur_nr) gefiltert werden.                           Die Paramter sind optional; werden keine Parameter Ã¼bergeben, enthÃ¤lt die RÃ¼ckgabe alle EintrÃ¤ge.          Der eindeutige Identifizierer setzt sich aus allen Attributen des Endpunktes zusammen.         {pi_referenz_kennr} ist die Kennummer eines Mittels, referenziert aus dem Endpunkt /mittel. Zeichenkette aus 9 Zeichen, Bsp: 006768-00.         {importeur_nr} ist die Nummer des Importeurs, referenziert wird die adresse_nr des Endpunktes /adresse. Zeichenfolge aus 20 Zeichen, Bsp: 12158.  Wenn auf andere Parameter gefiltert oder Teilabfragen gestellt werden sollen, kÃ¶nnen gesonderte Filtermethoden verwendet werden. Siehe dazu Abschnitt &quot;*JSON Queries*&quot; in der oberen allgemeinen API Beschreibung

### Example


```python
import time
from deutschland import pflanzenschutzmittelzulassung
from deutschland.pflanzenschutzmittelzulassung.api import default_api
from deutschland.pflanzenschutzmittelzulassung.model.inline_response20031 import InlineResponse20031
from pprint import pprint
# Defining the host is optional and defaults to https://psm-api.bvl.bund.de/ords/psm/api-v1
# See configuration.py for a list of all supported configuration parameters.
configuration = pflanzenschutzmittelzulassung.Configuration(
    host = "https://psm-api.bvl.bund.de/ords/psm/api-v1"
)


# Enter a context with an instance of the API client
with pflanzenschutzmittelzulassung.ApiClient() as api_client:
    # Create an instance of the API class
    api_instance = default_api.DefaultApi(api_client)
    importeur_nr = "importeur_nr_example" # str | Implicit parameter (optional)
    pi_referenz_kennr = "pi_referenz_kennr_example" # str | Implicit parameter (optional)

    # example passing only required values which don't have defaults set
    # and optional values
    try:
        api_response = api_instance.parallelimport_abgelaufen_get(importeur_nr=importeur_nr, pi_referenz_kennr=pi_referenz_kennr)
        pprint(api_response)
    except pflanzenschutzmittelzulassung.ApiException as e:
        print("Exception when calling DefaultApi->parallelimport_abgelaufen_get: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **importeur_nr** | **str**| Implicit parameter | [optional]
 **pi_referenz_kennr** | **str**| Implicit parameter | [optional]

### Return type

[**InlineResponse20031**](InlineResponse20031.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The queried record. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **parallelimport_gueltig_get**
> InlineResponse20031 parallelimport_gueltig_get()



Liefert eine Liste der gÃ¼ltigen Parallelimporte (Mittel aus anderen LÃ¤ndern die identisch sind zu in Deutschland zugelassenen Mitteln) zu ihren Referenzmitteln.                           Optional kann auf ein Referenzmittel {pi_referenz_kennr} oder einen Importeur {importeur_nr) gefiltert werden.                           Die Paramter sind optional; werden keine Parameter Ã¼bergeben, enthÃ¤lt die RÃ¼ckgabe alle EintrÃ¤ge.          Der eindeutige Identifizierer setzt sich aus allen Attributen des Endpunktes zusammen.         {pi_referenz_kennr} ist die Kennummer eines Mittels, referenziert aus dem Endpunkt /mittel. Zeichenkette aus 9 Zeichen, Bsp: 006767-00.         {importeur_nr} ist die Nummer des Importeurs, referenziert wird die adresse_nr des Endpunktes /adresse. Zeichenfolge aus 20 Zeichen, Bsp: 12158.  Wenn auf andere Parameter gefiltert oder Teilabfragen gestellt werden sollen, kÃ¶nnen gesonderte Filtermethoden verwendet werden. Siehe dazu Abschnitt &quot;*JSON Queries*&quot; in der oberen allgemeinen API Beschreibung

### Example


```python
import time
from deutschland import pflanzenschutzmittelzulassung
from deutschland.pflanzenschutzmittelzulassung.api import default_api
from deutschland.pflanzenschutzmittelzulassung.model.inline_response20031 import InlineResponse20031
from pprint import pprint
# Defining the host is optional and defaults to https://psm-api.bvl.bund.de/ords/psm/api-v1
# See configuration.py for a list of all supported configuration parameters.
configuration = pflanzenschutzmittelzulassung.Configuration(
    host = "https://psm-api.bvl.bund.de/ords/psm/api-v1"
)


# Enter a context with an instance of the API client
with pflanzenschutzmittelzulassung.ApiClient() as api_client:
    # Create an instance of the API class
    api_instance = default_api.DefaultApi(api_client)
    importeur_nr = "importeur_nr_example" # str | Implicit parameter (optional)
    pi_referenz_kennr = "pi_referenz_kennr_example" # str | Implicit parameter (optional)

    # example passing only required values which don't have defaults set
    # and optional values
    try:
        api_response = api_instance.parallelimport_gueltig_get(importeur_nr=importeur_nr, pi_referenz_kennr=pi_referenz_kennr)
        pprint(api_response)
    except pflanzenschutzmittelzulassung.ApiException as e:
        print("Exception when calling DefaultApi->parallelimport_gueltig_get: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **importeur_nr** | **str**| Implicit parameter | [optional]
 **pi_referenz_kennr** | **str**| Implicit parameter | [optional]

### Return type

[**InlineResponse20031**](InlineResponse20031.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The queried record. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **schadorg_gruppe_get**
> InlineResponse20033 schadorg_gruppe_get()



Liefert eine Liste der Schadorganismen und der korrespondierenden Schadorganismengruppe. Der Enpunkt ist eine ReprÃ¤sentation einer Baumstruktur. schadorg_gruppe ist dabei ein Parent, dem das Child schadorg zugeordnet ist. Eine Schagorganismusgruppe kann mehrere Schadorganismen als Children besitzen, ein Schadorganismus kann mehrere Parents haben. Da der Baum mehrere Stufen hat, stehen einige Schadorganismen als Child (schadorg) UND als Parent (schadorg_gruppe) in unterschiedlichen Zeilen.                           Optional kann auf einen Schadorganismus {schadorg} oder eine Schadorganismusgruppe {schadorg_gruppe} gefiltert werden.                           Bei einer Ã¼bergebenen {schadorg} enthÃ¤lt die RÃ¼ckgabe nur die direkten Parents, also Schadorganismusgruppen zum korrepondierenden Schadorganismus.                           Bei einer Ã¼bergebenen {schadorg_gruppe} enthÃ¤lt die RÃ¼ckgabe nur die direkten Children, also Schadorganismen zu der korrepondierenden Schadorganismusgruppe.                           Die Paramter sind optional; werden keine Parameter Ã¼bergeben, enthÃ¤lt die RÃ¼ckgabe alle EintrÃ¤ge.          Der eindeutige Identifizierer bestimmt sich aus dem {schadorg}, und der {schadorg_gruppe}.         {schadorg} ist der Kode eines Schadorganismus. (Child). Zeichenkette aus maximal 20 Zeichen, Bsp: BRORM.         {schadorg_gruppe} ist der Kode der Schdorganismusgruppe des zugeordneten Schadorganismus. (Parent). Zeichenkette aus maximal 20 Zeichen, Bsp: TTTMM.  Wenn auf andere Parameter gefiltert oder Teilabfragen gestellt werden sollen, kÃ¶nnen gesonderte Filtermethoden verwendet werden. Siehe dazu Abschnitt &quot;*JSON Queries*&quot; in der oberen allgemeinen API Beschreibung

### Example


```python
import time
from deutschland import pflanzenschutzmittelzulassung
from deutschland.pflanzenschutzmittelzulassung.api import default_api
from deutschland.pflanzenschutzmittelzulassung.model.inline_response20033 import InlineResponse20033
from pprint import pprint
# Defining the host is optional and defaults to https://psm-api.bvl.bund.de/ords/psm/api-v1
# See configuration.py for a list of all supported configuration parameters.
configuration = pflanzenschutzmittelzulassung.Configuration(
    host = "https://psm-api.bvl.bund.de/ords/psm/api-v1"
)


# Enter a context with an instance of the API client
with pflanzenschutzmittelzulassung.ApiClient() as api_client:
    # Create an instance of the API class
    api_instance = default_api.DefaultApi(api_client)
    schadorg = "schadorg_example" # str | Implicit parameter (optional)
    schadorg_gruppe = "schadorg_gruppe_example" # str | Implicit parameter (optional)

    # example passing only required values which don't have defaults set
    # and optional values
    try:
        api_response = api_instance.schadorg_gruppe_get(schadorg=schadorg, schadorg_gruppe=schadorg_gruppe)
        pprint(api_response)
    except pflanzenschutzmittelzulassung.ApiException as e:
        print("Exception when calling DefaultApi->schadorg_gruppe_get: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **schadorg** | **str**| Implicit parameter | [optional]
 **schadorg_gruppe** | **str**| Implicit parameter | [optional]

### Return type

[**InlineResponse20033**](InlineResponse20033.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The queried record. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **staerkung_get**
> InlineResponse20034 staerkung_get()



Liefert eine Liste von zugelassenen StÃ¤rkungsmitteln.                           Optional kann auf die Kennummer des StÃ¤rkungsmittels {kennr} und/oder den Anstragsteller {antragsteller_nr} gefiltert werden.                           Die Paramter sind optional; werden keine Parameter Ã¼bergeben, enthÃ¤lt die RÃ¼ckgabe alle EintrÃ¤ge.          {kennr} ist der eindeutige Identifizierer, die Kennummer einer StÃ¤rkung, referenziert aus dem Endpunkt /mittel. Zeichenkette aus 9 Zeichen, Bsp: 025125-00.         {antragsteller_nr} ist die Nummer des Antragstellers, referenziert wird die adresse_nr des Endpunktes /adresse. Zeichenfolge aus 20 Zeichen, Bsp: 10612.  Wenn auf andere Parameter gefiltert oder Teilabfragen gestellt werden sollen, kÃ¶nnen gesonderte Filtermethoden verwendet werden. Siehe dazu Abschnitt &quot;*JSON Queries*&quot; in der oberen allgemeinen API Beschreibung

### Example


```python
import time
from deutschland import pflanzenschutzmittelzulassung
from deutschland.pflanzenschutzmittelzulassung.api import default_api
from deutschland.pflanzenschutzmittelzulassung.model.inline_response20034 import InlineResponse20034
from pprint import pprint
# Defining the host is optional and defaults to https://psm-api.bvl.bund.de/ords/psm/api-v1
# See configuration.py for a list of all supported configuration parameters.
configuration = pflanzenschutzmittelzulassung.Configuration(
    host = "https://psm-api.bvl.bund.de/ords/psm/api-v1"
)


# Enter a context with an instance of the API client
with pflanzenschutzmittelzulassung.ApiClient() as api_client:
    # Create an instance of the API class
    api_instance = default_api.DefaultApi(api_client)
    antragsteller_nr = "antragsteller_nr_example" # str | Implicit parameter (optional)
    kennr = "kennr_example" # str | Implicit parameter (optional)

    # example passing only required values which don't have defaults set
    # and optional values
    try:
        api_response = api_instance.staerkung_get(antragsteller_nr=antragsteller_nr, kennr=kennr)
        pprint(api_response)
    except pflanzenschutzmittelzulassung.ApiException as e:
        print("Exception when calling DefaultApi->staerkung_get: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **antragsteller_nr** | **str**| Implicit parameter | [optional]
 **kennr** | **str**| Implicit parameter | [optional]

### Return type

[**InlineResponse20034**](InlineResponse20034.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The queried record. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **staerkung_vertrieb_get**
> InlineResponse20029 staerkung_vertrieb_get()



Liefert eine Zuordnung von StÃ¤rungsmitteln auf die Vertriebsfirmen der StÃ¤rkungsmittel.                           Optional kann auf die Kennummer des StÃ¤rkungsmittels {kennr} und/oder die Vertriebsfirma {vertriebsfirma_nr} gefiltert werden.                           Die Paramter sind optional; werden keine Parameter Ã¼bergeben, enthÃ¤lt die RÃ¼ckgabe alle EintrÃ¤ge.      {kennr] ist der eindeutige Identifizierer, die Kennummer einer StÃ¤rkung, referenziert aus dem Endpunkt /mittel. Zeichenkette aus 9 Zeichen, Bsp: 007713-00.     {vertriebsfirma_nr} ist die Nummer der Vertriebsfirma, referenziert wird die adresse_nr des Endpunktes /adresse. Zeichenfolge aus 20 Zeichen, Bsp: 12791.  Wenn auf andere Parameter gefiltert oder Teilabfragen gestellt werden sollen, kÃ¶nnen gesonderte Filtermethoden verwendet werden. Siehe dazu Abschnitt &quot;*JSON Queries*&quot; in der oberen allgemeinen API Beschreibung

### Example


```python
import time
from deutschland import pflanzenschutzmittelzulassung
from deutschland.pflanzenschutzmittelzulassung.api import default_api
from deutschland.pflanzenschutzmittelzulassung.model.inline_response20029 import InlineResponse20029
from pprint import pprint
# Defining the host is optional and defaults to https://psm-api.bvl.bund.de/ords/psm/api-v1
# See configuration.py for a list of all supported configuration parameters.
configuration = pflanzenschutzmittelzulassung.Configuration(
    host = "https://psm-api.bvl.bund.de/ords/psm/api-v1"
)


# Enter a context with an instance of the API client
with pflanzenschutzmittelzulassung.ApiClient() as api_client:
    # Create an instance of the API class
    api_instance = default_api.DefaultApi(api_client)
    kennr = "kennr_example" # str | Implicit parameter (optional)
    vertriebsfirma_nr = "vertriebsfirma_nr_example" # str | Implicit parameter (optional)

    # example passing only required values which don't have defaults set
    # and optional values
    try:
        api_response = api_instance.staerkung_vertrieb_get(kennr=kennr, vertriebsfirma_nr=vertriebsfirma_nr)
        pprint(api_response)
    except pflanzenschutzmittelzulassung.ApiException as e:
        print("Exception when calling DefaultApi->staerkung_vertrieb_get: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **kennr** | **str**| Implicit parameter | [optional]
 **vertriebsfirma_nr** | **str**| Implicit parameter | [optional]

### Return type

[**InlineResponse20029**](InlineResponse20029.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The queried record. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **stand_get**
> InlineResponse20036 stand_get()



Liefert das Release-Datum fÃ¼r den aktuellen Datenbestand. Das heiÃŸt, das Datum an dem die Daten das letzte Mal aktualisiert wurden.  Wenn auf andere Parameter gefiltert oder Teilabfragen gestellt werden sollen, kÃ¶nnen gesonderte Filtermethoden verwendet werden. Siehe dazu Abschnitt &quot;*JSON Queries*&quot; in der oberen allgemeinen API Beschreibung

### Example


```python
import time
from deutschland import pflanzenschutzmittelzulassung
from deutschland.pflanzenschutzmittelzulassung.api import default_api
from deutschland.pflanzenschutzmittelzulassung.model.inline_response20036 import InlineResponse20036
from pprint import pprint
# Defining the host is optional and defaults to https://psm-api.bvl.bund.de/ords/psm/api-v1
# See configuration.py for a list of all supported configuration parameters.
configuration = pflanzenschutzmittelzulassung.Configuration(
    host = "https://psm-api.bvl.bund.de/ords/psm/api-v1"
)


# Enter a context with an instance of the API client
with pflanzenschutzmittelzulassung.ApiClient() as api_client:
    # Create an instance of the API class
    api_instance = default_api.DefaultApi(api_client)

    # example, this endpoint has no required or optional parameters
    try:
        api_response = api_instance.stand_get()
        pprint(api_response)
    except pflanzenschutzmittelzulassung.ApiException as e:
        print("Exception when calling DefaultApi->stand_get: %s\n" % e)
```


### Parameters
This endpoint does not need any parameter.

### Return type

[**InlineResponse20036**](InlineResponse20036.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The queried record. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **wirkstoff_gehalt_get**
> InlineResponse20038 wirkstoff_gehalt_get()



Liefert eine Zuordnung der Mittel und des korrespondierenden Wirkstoffgehalts.                             Optional kann auf die Nummer eines Wirkstoffes {wirknr} und/oder eines Mittels {kennr} gefiltert werden.                             Die Paramter sind optional; werden keine Parameter Ã¼bergeben, enthÃ¤lt die RÃ¼ckgabe alle EintrÃ¤ge.      Der eindeutige Identifizierer setzt sich zusammen aus der {wirknr}, der {kennr} und der wirkvar.     {wirknr} ist die Nummer des Wirkstoffes, referenziert aus dem Endpunkt /wirkstoff. Zeichenkette aus maximal 4 Zeichen, Bsp: 0875.     {kennr} ist die Kennummer eines Mittels, referenziert aus dem Endpunkt /mittel. Zeichenkette aus 9 Zeichen, Bsp: 024994-00.  Wenn auf andere Parameter gefiltert oder Teilabfragen gestellt werden sollen, kÃ¶nnen gesonderte Filtermethoden verwendet werden. Siehe dazu Abschnitt &quot;*JSON Queries*&quot; in der oberen allgemeinen API Beschreibung

### Example


```python
import time
from deutschland import pflanzenschutzmittelzulassung
from deutschland.pflanzenschutzmittelzulassung.api import default_api
from deutschland.pflanzenschutzmittelzulassung.model.inline_response20038 import InlineResponse20038
from pprint import pprint
# Defining the host is optional and defaults to https://psm-api.bvl.bund.de/ords/psm/api-v1
# See configuration.py for a list of all supported configuration parameters.
configuration = pflanzenschutzmittelzulassung.Configuration(
    host = "https://psm-api.bvl.bund.de/ords/psm/api-v1"
)


# Enter a context with an instance of the API client
with pflanzenschutzmittelzulassung.ApiClient() as api_client:
    # Create an instance of the API class
    api_instance = default_api.DefaultApi(api_client)
    kennr = "kennr_example" # str | Implicit parameter (optional)
    wirknr = "wirknr_example" # str | Implicit parameter (optional)

    # example passing only required values which don't have defaults set
    # and optional values
    try:
        api_response = api_instance.wirkstoff_gehalt_get(kennr=kennr, wirknr=wirknr)
        pprint(api_response)
    except pflanzenschutzmittelzulassung.ApiException as e:
        print("Exception when calling DefaultApi->wirkstoff_gehalt_get: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **kennr** | **str**| Implicit parameter | [optional]
 **wirknr** | **str**| Implicit parameter | [optional]

### Return type

[**InlineResponse20038**](InlineResponse20038.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The queried record. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **wirkstoff_get**
> InlineResponse20037 wirkstoff_get()



Liefert eine Liste von zugelassenen Wirkstoffen.                             Optional kann auf einen Wirkstoff anhand der korrespondierenden Wirknummer {wirknr} gefiltert werden.                             Der Paramter ist optional; werden keine Parameter Ã¼bergeben, enthÃ¤lt die RÃ¼ckgabe alle EintrÃ¤ge.      {wirknr} ist der eindeutige Identifizierer des Wirkstoffes. Zeichenkette aus maximal 4 Zeichen, Bsp: 1122.  Wenn auf andere Parameter gefiltert oder Teilabfragen gestellt werden sollen, kÃ¶nnen gesonderte Filtermethoden verwendet werden. Siehe dazu Abschnitt &quot;*JSON Queries*&quot; in der oberen allgemeinen API Beschreibung

### Example


```python
import time
from deutschland import pflanzenschutzmittelzulassung
from deutschland.pflanzenschutzmittelzulassung.api import default_api
from deutschland.pflanzenschutzmittelzulassung.model.inline_response20037 import InlineResponse20037
from pprint import pprint
# Defining the host is optional and defaults to https://psm-api.bvl.bund.de/ords/psm/api-v1
# See configuration.py for a list of all supported configuration parameters.
configuration = pflanzenschutzmittelzulassung.Configuration(
    host = "https://psm-api.bvl.bund.de/ords/psm/api-v1"
)


# Enter a context with an instance of the API client
with pflanzenschutzmittelzulassung.ApiClient() as api_client:
    # Create an instance of the API class
    api_instance = default_api.DefaultApi(api_client)
    wirknr = "wirknr_example" # str | Implicit parameter (optional)

    # example passing only required values which don't have defaults set
    # and optional values
    try:
        api_response = api_instance.wirkstoff_get(wirknr=wirknr)
        pprint(api_response)
    except pflanzenschutzmittelzulassung.ApiException as e:
        print("Exception when calling DefaultApi->wirkstoff_get: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **wirknr** | **str**| Implicit parameter | [optional]

### Return type

[**InlineResponse20037**](InlineResponse20037.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The queried record. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **zusatzstoff_get**
> InlineResponse20039 zusatzstoff_get()



Liefert eine Liste der Zusatzstoffe zu Mitteln.                             Optional kann auf die Nummer des Zusatzstoffes {:kennr} oder die Nummer eines Antragstellers {antragsteller_nr} gefiltert werden.                             Die Paramter sind optional; werden keine Parameter Ã¼bergeben, enthÃ¤lt die RÃ¼ckgabe alle EintrÃ¤ge.      {kennr} ist der eindeutige Identifizierer, die Kennummer des Zusatzstoffes. Zeichenfolge aus 9 Zeichen, Bsp: 008339-00.     {antragsteller_nr} ist die Nummer des Antragsstellers, referenziert wird die adresse_nr des Endpunktes /adresse. Ziffernfolge aus maximal 22 Ziffern, Bsp: 12051.  Wenn auf andere Parameter gefiltert oder Teilabfragen gestellt werden sollen, kÃ¶nnen gesonderte Filtermethoden verwendet werden. Siehe dazu Abschnitt &quot;*JSON Queries*&quot; in der oberen allgemeinen API Beschreibung

### Example


```python
import time
from deutschland import pflanzenschutzmittelzulassung
from deutschland.pflanzenschutzmittelzulassung.api import default_api
from deutschland.pflanzenschutzmittelzulassung.model.inline_response20039 import InlineResponse20039
from pprint import pprint
# Defining the host is optional and defaults to https://psm-api.bvl.bund.de/ords/psm/api-v1
# See configuration.py for a list of all supported configuration parameters.
configuration = pflanzenschutzmittelzulassung.Configuration(
    host = "https://psm-api.bvl.bund.de/ords/psm/api-v1"
)


# Enter a context with an instance of the API client
with pflanzenschutzmittelzulassung.ApiClient() as api_client:
    # Create an instance of the API class
    api_instance = default_api.DefaultApi(api_client)
    antragsteller_nr = "antragsteller_nr_example" # str | Implicit parameter (optional)
    kennr = "kennr_example" # str | Implicit parameter (optional)

    # example passing only required values which don't have defaults set
    # and optional values
    try:
        api_response = api_instance.zusatzstoff_get(antragsteller_nr=antragsteller_nr, kennr=kennr)
        pprint(api_response)
    except pflanzenschutzmittelzulassung.ApiException as e:
        print("Exception when calling DefaultApi->zusatzstoff_get: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **antragsteller_nr** | **str**| Implicit parameter | [optional]
 **kennr** | **str**| Implicit parameter | [optional]

### Return type

[**InlineResponse20039**](InlineResponse20039.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The queried record. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **zusatzstoff_vertrieb_get**
> InlineResponse20029 zusatzstoff_vertrieb_get()



Liefert eine Zuordnung von Zusatzstoffen auf die Vertriebsfirmen der Zusatzstoffe.                             Optional kann auf die Kennummer des Zusatzstoffes {kennr} und/oder die Vertriebsfirma {vertriebsfirma_nr} gefiltert werden.                             Die Paramter sind optional; werden keine Parameter Ã¼bergeben, enthÃ¤lt die RÃ¼ckgabe alle EintrÃ¤ge.      Der eindeutige Identifizierer setzt sich zusammen aus allen Attributen des Endpunkts.     {kennr} ist die Kennummer des Zusatzstoffes, referenziert aus dem Endpunkt /zusatzstoff. Zeichenkette aus 9 Zeichen, Bsp: 005697-00.     {vertriebsfirma_nr} ist die Nummer der Vertriebsfirma, referenziert wird die adresse_nr des Endpunktes /adresse. Ziffernfolge aus maximal 22 Ziffern, Bsp: 10799.  Wenn auf andere Parameter gefiltert oder Teilabfragen gestellt werden sollen, kÃ¶nnen gesonderte Filtermethoden verwendet werden. Siehe dazu Abschnitt &quot;*JSON Queries*&quot; in der oberen allgemeinen API Beschreibung

### Example


```python
import time
from deutschland import pflanzenschutzmittelzulassung
from deutschland.pflanzenschutzmittelzulassung.api import default_api
from deutschland.pflanzenschutzmittelzulassung.model.inline_response20029 import InlineResponse20029
from pprint import pprint
# Defining the host is optional and defaults to https://psm-api.bvl.bund.de/ords/psm/api-v1
# See configuration.py for a list of all supported configuration parameters.
configuration = pflanzenschutzmittelzulassung.Configuration(
    host = "https://psm-api.bvl.bund.de/ords/psm/api-v1"
)


# Enter a context with an instance of the API client
with pflanzenschutzmittelzulassung.ApiClient() as api_client:
    # Create an instance of the API class
    api_instance = default_api.DefaultApi(api_client)
    kennr = "kennr_example" # str | Implicit parameter (optional)
    vertriebsfirma_nr = "vertriebsfirma_nr_example" # str | Implicit parameter (optional)

    # example passing only required values which don't have defaults set
    # and optional values
    try:
        api_response = api_instance.zusatzstoff_vertrieb_get(kennr=kennr, vertriebsfirma_nr=vertriebsfirma_nr)
        pprint(api_response)
    except pflanzenschutzmittelzulassung.ApiException as e:
        print("Exception when calling DefaultApi->zusatzstoff_vertrieb_get: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **kennr** | **str**| Implicit parameter | [optional]
 **vertriebsfirma_nr** | **str**| Implicit parameter | [optional]

### Return type

[**InlineResponse20029**](InlineResponse20029.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The queried record. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

