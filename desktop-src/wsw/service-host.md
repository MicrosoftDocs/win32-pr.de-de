---
title: Diensthost
description: Der Diensthost ist die Laufzeitumgebung zum Hosten eines Diensts innerhalb eines Prozesses.
ms.assetid: 42e4d24d-5611-4561-b874-6dc3f3f88c73
keywords:
- Diensthostwebdienste für Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff3a09a41714ce80402c5430e6849988ae86163770af7ae3eb060fdd7925e861
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119838665"
---
# <a name="service-host"></a>Diensthost

Der Diensthost ist die Laufzeitumgebung zum Hosten eines Diensts innerhalb eines Prozesses.


Ein Dienst kann einen oder mehrere Endpunkte innerhalb eines Diensthosts konfigurieren.

![Diagramm, das die Struktur eines Diensthosts zeigt, der einen Dienstendpunkt enthält.](images/servicehost.png)

## <a name="creating-a-service-host"></a>Erstellen eines Diensthosts

Vor dem Erstellen eines Diensthosts muss ein Dienst seine Endpunkte definieren. Ein Endpunkt im Diensthost wird in der [**WS \_ SERVICE \_ ENDPOINT-Struktur**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) angegeben und durch die folgenden Informationen definiert:

-   Eine Adresse, bei der es sich um den physischen URI handelt, unter dem der Dienst gehostet wird.
-   Eine [**WS \_ CHANNEL \_ TYPE-Struktur,**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) die den Typ des zugrunde liegenden Kanals für den Endpunkt angibt.
-   Eine [**\_ WS-KANALBINDUNGsstruktur, \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) die die Bindung des Kanals angibt.
-   Eine [**WS \_ SECURITY \_ DESCRIPTION-Struktur,**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) die die Sicherheitsbeschreibung für den Endpunkt enthält.
-   Eine [**WS \_ SERVICE \_ CONTRACT-Struktur,**](/windows/desktop/api/WebServices/ns-webservices-ws_service_contract) die den [Dienstvertrag für](contract.md) den Endpunkt darstellt.
-   Eine [**WS \_ SERVICE SECURITY \_ \_ CALLBACK-Struktur,**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback) die eine Autorisierungsrückruffunktion für den Endpunkt angibt.
-   Eine [**WS \_ SERVICE ENDPOINT \_ \_ PROPERTY-Struktur,**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint_property) die ein Array von Dienstendpunkteigenschaften enthält.

``` syntax
WS_SERVICE_ENDPOINT serviceEndpoint = {0};
const WS_SERVICE_ENDPOINT* serviceEndpoints[1];
serviceEndpoints[0] = &serviceEndpoint;
WS_STRING url = WS_STRING_VALUE(L"net.tcp://+/Example");

// Method based service contract for the service
static WS_SERVICE_CONTRACT calculatorContract = 
{
    &calculatorContractDescription, // comes from a generated header.
    NULL,
    &calculatorFunctions, // specified by the application
};

serviceEndpoint.address.url = &url;
serviceEndpoint.binding.channelBinding =  WS_TCP_CHANNEL_BINDING; 
serviceEndpoint.contract = &calculatorContract;  
serviceEndpoint.channelType = WS_CHANNEL_TYPE_DUPLEX_SESSION; 
serviceEndpoint.authorizationCallback = AuthorizationCallback; // Authorization callback.
```

Für SOAP über UDP, dargestellt durch [**\_ WS-UDP-KANALBINDUNG \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) in der WS-KANALBINDUNGsenumeration, werden nur **\_ \_ one-way-Verträge** unterstützt.

Nachdem ein Endpunkt definiert wurde, kann er an die [**WsCreateServiceHost-Funktion**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) übergeben werden, die ein Array von Zeigern auf [**WS \_ SERVICE \_ ENDPOINT-Strukturen**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) verwendet.

``` syntax
HRESULT hr = WsCreateServiceHost (serviceEndpoints, 1, NULL, 0, &host, error);
```

Eine Anwendung kann optional ein [](/windows/desktop/api/WebServices/ns-webservices-ws_service_property) Array von Diensteigenschaften für [**WsCreateServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) bereitstellen, um benutzerdefinierte Einstellungen auf dem Diensthost zu konfigurieren.

Eine Anwendung öffnet den Diensthost, um mit dem Akzeptieren von Clientanforderungen zu beginnen.

``` syntax
WsOpenServiceHost(serviceHost, NULL, NULL);
```

Nach dem Öffnen des Diensthosts kann die Anwendung ihn schließen, wenn keine vorgänge mehr erforderlich sind. Beachten Sie, dass die Ressourcen nicht freigegeben werden und mit einem nachfolgenden Aufruf von [**WsResetServiceHost erneut geöffnet werden können.**](/windows/desktop/api/WebServices/nf-webservices-wsresetservicehost)

``` syntax
WsCloseServiceHost(serviceHost, NULL, NULL);
```

Nach dem Schließen des Diensthosts kann eine Anwendung den Diensthost zur Wiederverwendung zurücksetzen.

``` syntax
WsResetServiceHost(serviceHost, NULL);
```

Wenn die Anwendung mit dem Diensthost fertig ist, kann sie die dem Diensthost zugeordneten Ressourcen durch Aufrufen der [**WsFreeServiceHost-Funktion frei**](/windows/desktop/api/WebServices/nf-webservices-wsfreeservicehost) geben. Beachten [**Sie, dass WsCloseServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscloseservicehost) aufgerufen werden muss, bevor diese Funktion aufgerufen wird.

``` syntax
WsFreeServiceHost(serviceHost, NULL);
```

Informationen zum Anfügen eines benutzerdefinierten Zustands an den Diensthost finden Sie unter [Benutzerhoststatus.](user-host-state.md)

Informationen zur Autorisierung in einem Diensthost für einen bestimmten Endpunkt finden Sie unter [Dienstautorisierung.](service-authorization.md)

Informationen zum Implementieren von Dienstvorgängen und Dienstverträgen für einen Dienst finden Sie in den Themen [Dienstvorgänge](server-side-service-operations.md) [und Dienstverträge.](contract.md)

## <a name="security"></a>Sicherheit

Eine Anwendung kann die folgenden Eigenschaften verwenden, um die Menge der Ressourcen zu steuern, die der Diensthost im Auftrag der Anwendung zuweist:

-   [**WS \_ SERVICE \_ ENDPOINT PROPERTY MAX \_ \_ \_ ACCEPTING \_ CHANNELS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),
-   [**WS \_ SERVICE \_ ENDPOINT PROPERTY MAX \_ \_ \_ CONCURRENCY**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),
-   [**WS \_ SERVICE \_ ENDPOINT PROPERTY MAX \_ \_ \_ CHANNELS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),
-   [**WS \_ SERVICE \_ ENDPOINT PROPERTY BODY \_ \_ \_ HEAP MAX \_ \_ SIZE**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),
-   [**WS \_ SERVICE \_ ENDPOINT PROPERTY MAX CALL POOL \_ \_ \_ \_ \_ SIZE**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),
-   [**WS \_ SERVICE \_ ENDPOINT PROPERTY MAX CHANNEL POOL \_ \_ \_ \_ \_ SIZE**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id).

Für jede dieser Eigenschaften werden sichere Standardwerte ausgewählt. Eine Anwendung muss vorsichtig sein, wenn sie diese Eigenschaften ändern möchte. Neben den oben genannten Eigenschaften können [kanal-,](channel.md) [listener-](listener.md) und [nachrichtenspezifische](message.md) Eigenschaften auch von der Anwendung geändert werden. Lesen Sie die Sicherheitsüberlegungen dieser Komponenten, bevor Sie eine dieser Einstellungen ändern.

Darüber hinaus sollten die folgenden Überlegungen zum Anwendungsentwurf sorgfältig ausgewertet werden, wenn die WWSAPI-Diensthost-API verwendet wird:

-   Bei der Verwendung von MEX sollten Anwendungen darauf achten, keine vertraulichen Daten offen zu legen. Wenn die Art der über MEX verfügbar gemachten Daten vertraulich ist, können Anwendungen den MEX-Endpunkt mit einer sicheren Bindung konfigurieren, die mindestens eine Authentifizierung erfordert, und die Autorisierung als Teil des Endpunkts mithilfe des [**WS \_ SERVICE SECURITY \_ \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback)implementieren.
-   Standardmäßig sind umfangreiche Fehlerinformationen durch Fehler auf dem Diensthost durch die [**WS \_ SERVICE PROPERTY \_ FAULT \_ \_ DISCLOSURE-Eigenschaft**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) deaktiviert. Es liegt im Ermessen der Anwendung, umfangreiche Fehlerinformationen als Teil des Fehlers zu senden. Dies kann jedoch zur Offenlegung von Informationen führen. Daher wird empfohlen, diese Einstellung nur für Debugszenarien zu ändern.
-   Neben der Überprüfung, die für Basic Profile 2.0 und die XML-Serialisierung ausgeführt wird, führt der Diensthost keine Überprüfung des Dateninhalts durch, der als Teil der Dienstvorgangsparameter empfangen wurde. Es liegt in der Verantwortung der Anwendung, alle Parametervalidierungen selbst durchzuführen.
-   Die Autorisierung wird nicht als Teil des Diensthosts implementiert. Anwendungen können jedoch ihr eigenes Autorisierungsschema mit [**WS \_ SECURITY \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) und [**dem WS SERVICE SECURITY \_ \_ \_ CALLBACK implementieren.**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback)
-   Es liegt in der Verantwortung der Anwendung, sichere Bindungen an ihrem Endpunkt zu verwenden. Der Diensthost bietet keine Sicherheit, die über das hinaus geht, was auf dem Endpunkt konfiguriert ist.

Die folgenden API-Elemente werden mit dem Diensthost verwendet.

| Rückruf                                                                             | Beschreibung                                                                     |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [**WS \_ SERVICE \_ ACCEPT \_ CHANNEL \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_service_accept_channel_callback) | Wird aufgerufen, wenn ein Kanal auf einem Endpunktlistener vom Diensthost akzeptiert wird. |
| [**WS \_ SERVICE \_ CLOSE \_ CHANNEL \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_service_close_channel_callback)   | Wird aufgerufen, wenn ein Kanal an einem Endpunkt geschlossen oder abgebrochen wird.                     |



 



| Enumeration                                                                    | Beschreibung                                                                                 |
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [**\_EIGENSCHAFTEN-ID DES WS-DIENSTENDPUNKTS \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id) | Optionale Parameter zum Konfigurieren eines [**\_ WS-DIENSTENDPUNKTs. \_**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) |
| [**\_ \_ WS-DIENSTHOSTSTATUS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_service_host_state)                      | Die Zustände, in denen sich ein Diensthost sein kann.                                                   |
| [**\_ \_ WS-DIENST-EIGENSCHAFTEN-ID \_**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id)                    | Optionale Parameter zum Konfigurieren des Diensthosts.                                       |



 



| Funktion                                                     | Beschreibung                                                                                  |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**WsAbortServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsabortservicehost)             | Unterbricht und beendet aktuelle Vorgänge auf dem Diensthost.                          |
| [**WsCloseServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscloseservicehost)             | Schließt alle Listener, sodass keine neuen Kanäle vom Client akzeptiert werden.                   |
| [**WsCreateServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost)           | Erstellt einen Diensthost.                                                                      |
| [**WsFreeServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsfreeservicehost)               | Gibt den einem Diensthostobjekt zugeordneten Arbeitsspeicher frei.                                   |
| [**WsGetServiceHostProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetservicehostproperty) | Ruft eine angegebene Diensthosteigenschaft ab.                                                 |
| [**WsOpenServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsopenservicehost)               | Öffnet einen Diensthost für die Kommunikation und startet die Listener auf allen Endpunkten.        |
| [**WsResetServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsresetservicehost)             | Setzt den Diensthost für die Wiederverwendung zurück und setzt den zugrunde liegenden Kanal und die Listener zur Wiederverwendung zurück. |



 



| Handle                                       | Beschreibung                                      |
|----------------------------------------------|--------------------------------------------------|
| [**\_WS-DIENSTHOST \_**](ws-service-host.md) | Ein nicht transparenter Typ, der verwendet wird, um auf einen Diensthost zu verweisen. |



 



| Struktur                                                                              | Beschreibung                                                                     |
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [**\_WS-DIENSTENDPUNKT \_**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint)                                   | Stellt einen einzelnen Endpunkt auf einem Diensthost dar.                            |
| [**\_ \_ WS-DIENSTENDPUNKTEIGENSCHAFT \_**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint_property)                | Gibt eine dienstspezifische Einstellung an.                                           |
| [**\_WS-DIENSTEIGENSCHAFT \_**](/windows/desktop/api/WebServices/ns-webservices-ws_service_property)                                   | Gibt eine dienstspezifische Einstellung an.                                           |
| [**WS \_ SERVICE PROPERTY ACCEPT CALLBACK (RÜCKRUF DER WS-DIENSTEIGENSCHAFT \_ \_ \_ ANNEHMEN)**](/windows/desktop/api/WebServices/ns-webservices-ws_service_property_accept_callback) | Gibt den Rückruf an, der aufgerufen wird, wenn ein Kanal erfolgreich akzeptiert wird. |
| [**RÜCKRUF ZUM SCHLIEßEN \_ DER WS-DIENSTEIGENSCHAFT \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_service_property_close_callback)   | Gibt den Rückruf an, der aufgerufen wird, wenn ein Kanal geschlossen werden soll.    |



 

 

 




