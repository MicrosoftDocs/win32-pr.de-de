---
title: Dienst Host
description: Der Dienst Host ist die Laufzeitumgebung zum Hosten eines Diensts in einem Prozess.
ms.assetid: 42e4d24d-5611-4561-b874-6dc3f3f88c73
keywords:
- Dienst Host-Webdienste für Windows
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0170f7dc0dfda99887b7d11d68d073517e0eb85f
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/12/2021
ms.locfileid: "106371818"
---
# <a name="service-host"></a>Dienst Host

Der Dienst Host ist die Laufzeitumgebung zum Hosten eines Diensts in einem Prozess.


Ein Dienst kann einen oder mehrere Endpunkte innerhalb eines Dienst Hosts konfigurieren.

![Diagramm, das die Struktur eines Dienst Hosts mit einem Dienst Endpunkt anzeigt.](images/servicehost.png)

## <a name="creating-a-service-host"></a>Erstellen eines Dienst Hosts

Vor dem Erstellen eines Dienst Hosts muss ein Dienst seine Endpunkte definieren. Ein Endpunkt im Dienst Host wird in der [**WS- \_ dienstend \_**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) Punkt Struktur angegeben und durch die folgenden Informationen definiert:

-   Eine Adresse, bei der es sich um den physischen URI handelt, auf dem der Dienst gehostet wird.
-   Eine [**WS \_ - \_ Kanaltyp**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) -Struktur, die den Typ des zugrunde liegenden Kanals für den Endpunkt angibt.
-   Eine [**WS- \_ Kanal \_ Bindungs**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) Struktur, die die Bindung des Kanals angibt.
-   Eine [**WS- \_ Sicherheits \_ Beschreibungs**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) Struktur, die die Sicherheits Beschreibung für den Endpunkt enthält.
-   Eine [**WS- \_ Dienst \_ Vertrags**](/windows/desktop/api/WebServices/ns-webservices-ws_service_contract) Struktur, die den [Dienstvertrag](contract.md) für den Endpunkt darstellt.
-   Eine [**WS- \_ Dienst- \_ Sicherheits \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback) Struktur, die eine Autorisierungs Rückruffunktion für den Endpunkt angibt.
-   Eine Eigenschaften Struktur des [**WS- \_ Dienst \_ Endpunkts \_**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint_property) , die ein Array von dienstend Punkt Eigenschaften enthält.

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

Für SOAP über UDP werden nur unidirektionale Verträge unterstützt, die durch die [**WS- \_ UDP- \_ \_ channelbindung**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) in der **WS- \_ \_ channelbindungsenumeration** dargestellt werden.

Nachdem ein Endpunkt definiert wurde, kann er an die [**wscreateservicehost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) -Funktion übergeben werden, die ein Array von Zeigern auf [**WS- \_ dienstend \_**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) Punkt Strukturen annimmt.

``` syntax
HRESULT hr = WsCreateServiceHost (serviceEndpoints, 1, NULL, 0, &host, error);
```

Eine Anwendung kann optional ein Array von [**Dienst Eigenschaften**](/windows/desktop/api/WebServices/ns-webservices-ws_service_property) für [**wscreateservicehost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) bereitstellen, um benutzerdefinierte Einstellungen auf dem Dienst Host zu konfigurieren.

Eine Anwendung öffnet den Dienst Host, um mit der Annahme von Client Anforderungen zu beginnen.

``` syntax
WsOpenServiceHost(serviceHost, NULL, NULL);
```

Nach dem Öffnen des Dienst Hosts kann die Anwendung ihn schließen, wenn keine weiteren Vorgänge vorhanden sind, die dies erfordern. Beachten Sie, dass dadurch keine Ressourcen freigegeben werden und dass Sie mit einem nachfolgenden Aufrufen von [**wsresetservicehost**](/windows/desktop/api/WebServices/nf-webservices-wsresetservicehost)erneut geöffnet werden kann.

``` syntax
WsCloseServiceHost(serviceHost, NULL, NULL);
```

Nach dem Schließen des Dienst Hosts kann eine Anwendung den Dienst Host für die Wiederverwendung zurücksetzen.

``` syntax
WsResetServiceHost(serviceHost, NULL);
```

Wenn die Anwendung mit dem Dienst Host ausgeführt wird, können die Ressourcen, die dem Dienst Host zugeordnet sind, durch Aufrufen der [**wsfreeservicehost**](/windows/desktop/api/WebServices/nf-webservices-wsfreeservicehost) -Funktion freigegeben werden. Beachten Sie, dass [**wscloseservicehost**](/windows/desktop/api/WebServices/nf-webservices-wscloseservicehost) aufgerufen werden muss, bevor diese Funktion aufgerufen wird.

``` syntax
WsFreeServiceHost(serviceHost, NULL);
```

Informationen zum Anfügen eines benutzerdefinierten Zustands an den Dienst Host finden Sie unter [Benutzer Host Status](user-host-state.md) .

Informationen zur Autorisierung in einem Dienst Host für einen bestimmten Endpunkt finden Sie unter [Dienst Autorisierung](service-authorization.md).

Weitere Informationen zum Implementieren von Dienst Vorgängen und Dienstverträgen für einen Dienst finden Sie in den Themen zu [Dienst Vorgängen](server-side-service-operations.md) und [Dienst](contract.md)Verträgen.

## <a name="security"></a>Sicherheit

Eine Anwendung kann die folgenden Eigenschaften verwenden, um die Menge der Ressourcen zu steuern, die der Dienst Host für die Anwendung bereitstellt:

-   [**WS \_ Dienst \_ Endpunkt \_ Eigenschaft \_ Max. \_ Annahme von \_ Kanälen**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),
-   [**WS \_ maximale Parallelität der Dienst \_ Endpunkt \_ Eigenschaft \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),
-   [**WS \_ \_ \_ \_ Maximale \_ Kanäle für Dienst Endpunkt Eigenschaft**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),
-   [**WS \_ \_ \_ \_ \_ \_ Maximale \_ Größe für den eigenschaftenheap des Dienst Endpunkts**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id)
-   [**WS \_ \_Maximale Anzahl \_ von \_ \_ aufrufspooleigenschaften \_ \_ für Dienst Endpunkt**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),
-   [**WS \_ \_ \_ \_ Maximale \_ \_ \_ channelpoolgröße des Dienst Endpunkts**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id).

Für jede dieser Eigenschaften werden sichere Standardwerte ausgewählt. eine Anwendung muss sorgfältig sein, wenn Sie diese Eigenschaften ändern möchte. Zusätzlich zu den oben erwähnten Eigenschaften können auch [Kanal](channel.md)-, [Listener](listener.md) -und [Nachrichten](message.md) spezifische Eigenschaften von der Anwendung geändert werden. Beachten Sie die Sicherheitsüberlegungen dieser Komponenten, bevor Sie diese Einstellungen ändern.

Außerdem sollten die folgenden Überlegungen zum Anwendungs Entwurf sorgfältig ausgewertet werden, wenn die wwsapi-Dienst Host-API verwendet wird:

-   Bei der Verwendung von Mex sollten Anwendungen darauf achten, keine sensiblen Daten offenzulegen. Wenn die Art der Daten, die durch MEX verfügbar gemacht werden, vertraulich ist, kann die Anwendung den MEX-Endpunkt mit einer sicheren Bindung konfigurieren, die mindestens eine Authentifizierung erfordert, und die Autorisierung als Teil des Endpunkts mithilfe des [**WS- \_ Dienst \_ Sicherheits \_ Rückrufs**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback)implementieren.
-   In der Standardeinstellung werden umfangreiche Fehlerinformationen durch Fehler auf Dienst Host über die [**WS- \_ Dienst \_ Eigenschaft \_ Fehler \_ Offenlegungs**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) Eigenschaft deaktiviert. Es ist nach dem Ermessen der Anwendung, umfangreiche Fehlerinformationen als Teil des Fehlers zu senden. Dies kann jedoch zur Offenlegung von Informationen führen. Daher wird empfohlen, dass diese Einstellung nur für Debugszenarien geändert wird.
-   Neben der Überprüfung, die für das Basisprofil 2,0 und die XML-Serialisierung ausgeführt wird, führt der Dienst Host keine Überprüfung des Daten Inhalts aus, der als Teil der Dienst Vorgangs Parameter Es liegt in der Verantwortung der Anwendung, alle Parameter Validierungen eigenständig auszuführen.
-   Die Autorisierung ist nicht als Teil des Dienst Hosts implementiert. Anwendungen können jedoch mithilfe der [**WS- \_ Sicherheits \_ Beschreibung**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) und des [**WS- \_ Dienst \_ Sicherheits \_ Rückrufs**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback)Ihr eigenes Autorisierungs Schema implementieren.
-   Es liegt in der Verantwortung der Anwendung, sichere Bindungen für ihren Endpunkt zu verwenden. Der Dienst Host bietet keine Sicherheitsfunktionen, die über die Konfiguration des Endpunkts hinausgehen.

Die folgenden API-Elemente werden mit dem Dienst Host verwendet.

| Rückruf                                                                             | BESCHREIBUNG                                                                     |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [**WS- \_ Dienst \_ Annahme- \_ Kanal \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_service_accept_channel_callback) | Wird aufgerufen, wenn ein Kanal für einen Endpunkt Listener durch den Dienst Host akzeptiert wird. |
| [**WS- \_ Dienst- \_ Schluss \_ Kanal \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_service_close_channel_callback)   | Wird aufgerufen, wenn ein Kanal an einem Endpunkt geschlossen oder abgebrochen wird.                     |



 



| Enumeration                                                                    | Beschreibung                                                                                 |
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [**Eigenschaften-ID für WS- \_ Dienst \_ Endpunkt \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id) | Optionale Parameter zum Konfigurieren eines [**WS- \_ Dienst \_ Endpunkts**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint). |
| [**Status des WS- \_ Dienst \_ Hosts \_**](/windows/desktop/api/WebServices/ne-webservices-ws_service_host_state)                      | Die Zustände, in denen sich ein Dienst Host befinden kann.                                                   |
| [**WS- \_ Dienst- \_ Eigenschaften- \_ ID**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id)                    | Optionale Parameter zum Konfigurieren des Dienst Hosts.                                       |



 



| Funktion                                                     | BESCHREIBUNG                                                                                  |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**Wsabortservicehost**](/windows/desktop/api/WebServices/nf-webservices-wsabortservicehost)             | Unterbricht und beendet die aktuellen Vorgänge auf dem Dienst Host.                          |
| [**Wscloseservicehost**](/windows/desktop/api/WebServices/nf-webservices-wscloseservicehost)             | Schließt alle Listener, sodass keine neuen Kanäle vom Client akzeptiert werden.                   |
| [**Wscreateservicehost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost)           | Erstellt einen Dienst Host.                                                                      |
| [**Wsfreeservicehost**](/windows/desktop/api/WebServices/nf-webservices-wsfreeservicehost)               | Gibt den einem Dienst Host Objekt zugeordneten Arbeitsspeicher frei.                                   |
| [**Wsgetservicehostproperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetservicehostproperty) | Ruft eine angegebene Dienst Host Eigenschaft ab.                                                 |
| [**Wsopeinservicehost**](/windows/desktop/api/WebServices/nf-webservices-wsopenservicehost)               | Öffnet einen Dienst Host für die Kommunikation und startet die Listener für alle Endpunkte.        |
| [**Wsresetservicehost**](/windows/desktop/api/WebServices/nf-webservices-wsresetservicehost)             | Setzt den Dienst Host für die Wiederverwendung zurück und setzt den zugrunde liegenden Kanal und die Listener für die Wiederverwendung zurück. |



 



| Handle                                       | BESCHREIBUNG                                      |
|----------------------------------------------|--------------------------------------------------|
| [**WS- \_ Dienst \_ Host**](ws-service-host.md) | Ein nicht transparenter Typ, der zum Verweisen auf einen Dienst Host verwendet wird. |



 



| Struktur                                                                              | BESCHREIBUNG                                                                     |
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [**WS- \_ Dienst \_ Endpunkt**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint)                                   | Stellt einen einzelnen Endpunkt auf einem Dienst Host dar.                            |
| [**Eigenschaft des WS- \_ Dienst \_ Endpunkts \_**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint_property)                | Gibt eine Dienst spezifische Einstellung an.                                           |
| [**WS- \_ Dienst \_ Eigenschaft**](/windows/desktop/api/WebServices/ns-webservices-ws_service_property)                                   | Gibt eine Dienst spezifische Einstellung an.                                           |
| [**WS- \_ Dienst \_ Eigenschaft \_ Accept \_ Callback**](/windows/desktop/api/WebServices/ns-webservices-ws_service_property_accept_callback) | Gibt den Rückruf an, der aufgerufen wird, wenn ein Kanal erfolgreich akzeptiert wird. |
| [**Rückruf für die WS- \_ Dienst \_ Eigenschaft \_ Close \_**](/windows/desktop/api/WebServices/ns-webservices-ws_service_property_close_callback)   | Gibt den Rückruf an, der aufgerufen wird, wenn ein Kanal im Begriff ist, geschlossen zu werden.    |



 

 

 




