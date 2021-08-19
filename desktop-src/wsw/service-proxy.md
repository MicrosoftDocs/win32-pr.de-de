---
title: Dienstproxy
description: Ein Dienstproxy ist der clientseitige Proxy für einen Dienst.
ms.assetid: e1a5bf5e-dbc1-43e3-981b-7db4caa08bdc
keywords:
- Dienstproxywebdienste für Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ff23349545c47dde2a54ea0b0911d3f792f21778f5053628929d3a98c69b0f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026183"
---
# <a name="service-proxy"></a>Dienstproxy

Ein Dienstproxy ist der clientseitige Proxy für einen Dienst. Mit dem Dienstproxy können Anwendungen [](message.md) Nachrichten über einen Kanal als [Methodenaufrufe](channel.md) senden und empfangen.

Dienstproxies werden nach Bedarf erstellt, geöffnet, zum Aufrufen eines Diensts verwendet und geschlossen, wenn sie nicht mehr benötigt werden. Alternativ kann eine Anwendung einen Dienstproxy wiederverwenden, um wiederholt eine Verbindung mit demselben Dienst herzustellen, ohne dass zeit- und ressourcenaufwand für die mehrmalse Initialisierung eines Dienstproxys erforderlich ist. Das folgende Diagramm veranschaulicht den Ablauf der möglichen Zustände des Dienstproxys und der Funktionsaufrufe oder Ereignisse, die von einem Zustand in einen anderen führen.

![Diagramm: Dienstproxystatus und Funktionsaufrufe oder Ereignisse, die von einem Zustand in einen anderen führen](images/serviceproxystates.png)

Diese Dienstproxyzustände werden in der [**WS \_ SERVICE \_ PROXY \_ STATE-Enumeration**](/windows/desktop/api/WebServices/ne-webservices-ws_service_proxy_state) aufgelistet.

Wie das obige Diagramm und der folgende Code veranschaulichen, wird ein Dienstproxy durch einen Aufruf der [**WsCreateServiceProxy-Funktion**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) erstellt. Als Parameter für diesen Aufruf bietet WWSAPI die folgenden Enumerationen:

-   [**\_WS-KANALTYP \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type)
-   [**\_WS-KANALBINDUNG \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)

Außerdem werden optionale Parameter mit den folgenden Datentypen akzeptiert:

-   [**\_ \_ WS-PROXY-EIGENSCHAFTEN-ID \_**](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id)
-   [**\_WS-SICHERHEITSBESCHREIBUNG \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description)

Wenn der Dienstproxy erstellt wurde, gibt die **WsCreateServiceProxy-Funktion** einen Verweis auf den [Dienstproxy WS \_ SERVICE \_ PROXY](ws-service-proxy.md)über einen out-Parameter zurück.

``` syntax
WS_SERVICE_PROXY* serviceProxy = NULL;
hr = WsCreateServiceProxy (
    WS_TCP_CHANNEL_BINDING, 
    WS_CHANNEL_TYPE_DUPLEX_SESSION, 
    NULL, 
    NULL, 
    0, 
    NULL,
    0,
    &serviceProxy, 
    error);
```

Wenn der Dienstproxy erstellt wurde, kann die Anwendung den Dienstproxy für die Kommunikation mit einem [](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) Dienst öffnen, indem die [**WsOpenServiceProxy-Funktion**](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy) aufruft und eine Adressstruktur mit der Netzwerkadresse des Dienstendpunkts übergeben wird, mit dem eine Verbindung hergestellt werden soll.

``` syntax
WS_ENDPOINT_ADDRESS address = {0};
address.uri.chars = "net.tcp://localhost/example";
address.uri.length = wcslen("net.tcp://localhost/example";);
hr = WsOpenServiceProxy(serviceProxy, &address, NULL, error);
```

Wenn der Dienstproxy geöffnet wurde, kann die Anwendung ihn verwenden, um Aufrufe an den Dienst zu tätigen.

``` syntax
hr = Add(
    serviceProxy, 
    1, 
    2, 
    &result, 
    NULL, 
    0, 
    NULL, 
    error);
```

Wenn die Anwendung den Dienstproxy nicht mehr benötigt, wird der Dienstproxy durch Aufrufen der [**WsCloseServiceProxy-Funktion**](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy) geschlossen. Außerdem wird der zugeordnete Arbeitsspeicher durch Aufrufen von [**WsFreeServiceProxy frei.**](/windows/desktop/api/WebServices/nf-webservices-wsfreeserviceproxy)

``` syntax
hr = WsCloseServiceProxy(
    serviceProxy, 
    NULL, 
    error);
```

``` syntax
hr = WsFreeServiceProxy(
    serviceProxy, 
    error);
```

## <a name="reusing-the-service-proxy"></a>Wiederverwendung des Dienstproxys

Alternativ kann eine Anwendung nach dem Aufruf von [**WsCloseServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy) den Dienstproxy wiederverwenden, indem sie die [**WsResetServiceProxy-Funktion**](/windows/desktop/api/WebServices/nf-webservices-wsresetserviceproxy) aufruft.

``` syntax
hr = WsResetServiceProxy(
    serviceProxy, 
    error);
```

Weitere Informationen zur Verwendung von Dienstproxies in verschiedenen Kontexten finden Sie in den folgenden Themen:

-   [Dienstproxy und Sitzungen](service-proxy-and-sessions.md)
-   [Dienstvorgang](service-operation.md)
-   [Clientseitige Dienstvorgänge](client-side-service-operations.md)
-   [HttpCalculatorClientExample](httpcalculatorclientexample.md)

### <a name="security"></a>Sicherheit

Die folgenden Überlegungen zum Anwendungsentwurf sollten bei verwendung der WWSAPI-Dienstproxy-API sorgfältig beachtet werden:

-   Der Dienstproxy führt keine Überprüfung der Daten aus, die über die Überprüfung des Basisprofils 2.0 und die XML-Serialisierung hinausgehen. Die Anwendung ist dafür verantwortlich, die Daten zu überprüfen, die in den Parametern enthalten sind, die sie im Rahmen des Aufrufs zurückerzieht.
-   Das Konfigurieren der maximalen Anzahl ausstehender Aufrufe auf dem Dienstproxy mithilfe des [**WS \_ PROXY PROPERTY \_ ID-Enumerationswerts \_**](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id) **WS PROXY \_ PROPERTY MAX \_ PENDING \_ \_ \_ CALLS** bietet Schutz vor einem langsam ausgeführten Server. Der Standardwert ist 100. Anwendungen müssen bei der Änderung der Standardwerte vorsichtig sein.
-   Der Dienstproxy bietet keine Sicherheitsgarantien, die über die in der [**WS \_ SECURITY \_ DESCRIPTION-Struktur**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) für die Kommunikation mit dem Server angegebenen Sicherheitsgarantien hinausgehen.
-   Gehen Sie beim Ändern der [Nachrichten- und](message.md) [Kanaleinstellungen](channel.md) auf dem Dienstproxy mit Vorsicht vor. Lesen Sie die Sicherheitsüberlegungen im Zusammenhang mit Nachrichten und Kanälen, bevor Sie eine der zugehörigen Eigenschaften ändern.
-   Der Dienstproxy verschlüsselt alle Anmeldeinformationen, die er im Arbeitsspeicher speichert.

Die folgenden API-Elemente beziehen sich auf Dienstproxies.

| Rückruf                                                          | Beschreibung                                                                                                                     |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [**\_ \_ WS-PROXYNACHRICHTENRÜCKRUF \_**](/windows/desktop/api/WebServices/nc-webservices-ws_proxy_message_callback) | Wird aufgerufen, wenn die Header der Eingabenachricht gesendet werden oder wenn gerade ein Ausgabenachrichtenheader empfangen wird. |



 



| Enumeration                                                 | Beschreibung                                                                               |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [**\_EIGENSCHAFTEN-ID DES WS-AUFRUFS \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_call_property_id)       | Enumeriert optionale Parameter zum Konfigurieren eines Aufrufs für einen clientseitigen Dienstvorgang. |
| [**\_ \_ WS-PROXY-EIGENSCHAFTEN-ID \_**](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id)     | Enumeriert optionale Parameter für die Konfiguration des Dienstproxys.                         |
| [**\_ \_ WS-DIENSTPROXYSTATUS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_service_proxy_state) | Der Status des Dienstproxys.                                                           |



 



| Funktion                                                       | Beschreibung                                                                       |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [**WsAbcall**](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall)                         | Verabbruch eines angegebenen Aufrufs für einen angegebenen Dienstproxy.                           |
| [**WsAbortServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsabortserviceproxy)             | Bricht alle ausstehenden Eingaben und Ausgaben für einen angegebenen Dienstproxy ab.                |
| [**WsCall**](/windows/desktop/api/WebServices/nf-webservices-wscall)                                       | Nur intern. Serialisiert Argumente in eine Nachricht und sendet sie über den Kanal. |
| [**WsCloseServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy)             | Schließt einen Dienstproxy für die Kommunikation.                                         |
| [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy)           | Erstellt einen Dienstproxy.                                                          |
| [**WsFreeServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsfreeserviceproxy)               | Gibt den einem Dienstproxy zugeordneten Arbeitsspeicher frei.                              |
| [**WsGetServiceProxyProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetserviceproxyproperty) | Ruft eine angegebene Dienstproxyeigenschaft ab.                                     |
| [**WsOpenServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy)               | Öffnet einen Dienstproxy für einen Dienstendpunkt.                                      |
| [**WsResetServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsresetserviceproxy)             | Setzt den Dienstproxy zurück.                                                             |



 



| Handle                                     | Beschreibung                                       |
|--------------------------------------------|---------------------------------------------------|
| [\_WS-DIENSTPROXY \_](ws-service-proxy.md) | Ein nicht transparenter Typ, der verwendet wird, um auf einen Dienstproxy zu verweisen. |



 



| Struktur                                         | Beschreibung                 |
|---------------------------------------------------|-----------------------------|
| [**\_WS-AUFRUFEIGENSCHAFT \_**](/windows/desktop/api/WebServices/ns-webservices-ws_call_property)    | Gibt eine Aufrufeigenschaft an.  |
| [**WS \_ \_PROXY-EIGENSCHAFT**](/windows/desktop/api/WebServices/ns-webservices-ws_proxy_property). | Gibt eine Proxyeigenschaft an. |



 

 

 




