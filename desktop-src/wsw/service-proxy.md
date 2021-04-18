---
title: Dienst Proxy
description: Bei einem Dienst Proxy handelt es sich um den Client seitigen Proxy für einen Dienst.
ms.assetid: e1a5bf5e-dbc1-43e3-981b-7db4caa08bdc
keywords:
- Dienst Proxy-Webdienste für Windows
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ac82509fa155084cbb4ca3e6b9437728c6f853a
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/12/2021
ms.locfileid: "106361113"
---
# <a name="service-proxy"></a>Dienst Proxy

Bei einem Dienst Proxy handelt es sich um den Client seitigen Proxy für einen Dienst. Der Dienst Proxy ermöglicht Anwendungen das Senden und empfangen von [Nachrichten](message.md) über einen [Kanal](channel.md) als Methodenaufrufe.

Dienst Proxys werden bei Bedarf erstellt, geöffnet, zum aufzurufen eines Dienstanbieter verwendet und geschlossen, wenn Sie nicht mehr benötigt werden. Alternativ kann eine Anwendung einen Dienst Proxy wieder verwenden, um wiederholt eine Verbindung zum gleichen Dienst herzustellen, ohne Zeit und Ressourcen zu verwenden, die für die mehrmalige Initialisierung eines Dienst Proxys erforderlich sind. Das folgende Diagramm veranschaulicht den Fluss der möglichen Zustände des Dienst Proxys und der Funktionsaufrufe oder Ereignisse, die von einem Zustand zu einem anderen geleitet werden.

![Das Diagramm zeigt die Dienst Proxy Zustände und die Funktionsaufrufe oder Ereignisse, die von einem Zustand zu einem anderen geführt haben.](images/serviceproxystates.png)

Diese Dienst Proxy Zustände werden in der WS- [**\_ Dienst- \_ Proxy \_ Zustands**](/windows/desktop/api/WebServices/ne-webservices-ws_service_proxy_state) Enumeration aufgelistet.

Wie das obige Diagramm und der folgende Code veranschaulichen, wird ein Dienst Proxy durch einen Aufrufen der [**wscreateserviceproxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) -Funktion erstellt. Als Parameter für diesen Befehl stellt wwsapi die folgenden Enumerationen bereit:

-   [**WS \_ - \_ Kanaltyp**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type)
-   [**WS- \_ Kanal \_ Bindung**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)

Außerdem akzeptiert es optionale Parameter unter Verwendung der folgenden Datentypen:

-   [**WS- \_ Proxy- \_ Eigenschaften- \_ ID**](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id)
-   [**WS- \_ Sicherheits \_ Beschreibung**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description)

Wenn der Dienst Proxy erstellt wurde, gibt die **wscreateserviceproxy** -Funktion einen Verweis auf den Dienst Proxy ( [WS- \_ Dienst \_ Proxy](ws-service-proxy.md)) über einen out-Parameter zurück.

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

Beim Erstellen des Dienst Proxys kann die Anwendung den Dienst Proxy für die Kommunikation mit einem Dienst öffnen, indem Sie die [**wsopenserviceproxy**](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy) -Funktion aufrufen und eine [**Adress**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) Struktur mit der Netzwerkadresse des Dienst Endpunkts übergibt, mit dem eine Verbindung hergestellt werden soll.

``` syntax
WS_ENDPOINT_ADDRESS address = {0};
address.uri.chars = "net.tcp://localhost/example";
address.uri.length = wcslen("net.tcp://localhost/example";);
hr = WsOpenServiceProxy(serviceProxy, &address, NULL, error);
```

Wenn der Dienst Proxy geöffnet wurde, kann er von der Anwendung verwendet werden, um Aufrufe an den Dienst durchführen.

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

Wenn die Anwendung den Dienst Proxy nicht mehr benötigt, wird der Dienst Proxy durch Aufrufen der [**wscloseserviceproxy**](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy) -Funktion geschlossen. Außerdem wird der zugehörige Speicher durch Aufrufen von [**wsfreeserviceproxy**](/windows/desktop/api/WebServices/nf-webservices-wsfreeserviceproxy)freigegeben.

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

## <a name="reusing-the-service-proxy"></a>Wieder verwenden des Dienst Proxys

Alternativ kann eine Anwendung nach dem Aufrufen von [**wscloseserviceproxy**](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy) den Dienst Proxy wieder verwenden, indem Sie die [**wsresetserviceproxy**](/windows/desktop/api/WebServices/nf-webservices-wsresetserviceproxy) -Funktion aufruft.

``` syntax
hr = WsResetServiceProxy(
    serviceProxy, 
    error);
```

Weitere Informationen zur Verwendung von Dienst Proxys in verschiedenen Kontexten finden Sie in den folgenden Themen:

-   [Dienst Proxy und-Sitzungen](service-proxy-and-sessions.md)
-   [Dienst Vorgang](service-operation.md)
-   [Client seitige Dienst Vorgänge](client-side-service-operations.md)
-   [Httpcalculatorclieintexample](httpcalculatorclientexample.md)

### <a name="security"></a>Sicherheit

Beachten Sie die folgenden Überlegungen zum Anwendungs Entwurf, wenn Sie die wwsapi-Dienst Proxy-API verwenden:

-   Der Dienst Proxy führt keine Überprüfung der Daten über die grundlegenden Profile 2,0-Validierung und XML-Serialisierung hinaus aus. Die Anwendung ist dafür verantwortlich, die Daten zu überprüfen, die in den Parametern enthalten sind, die Sie als Teil des Aufrufens erhalten.
-   Das Konfigurieren der maximalen Anzahl ausstehender Aufrufe für den Dienst Proxy mithilfe des [**WS- \_ \_ proxyeigenschafts- \_ ID**](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id) -Enumerationswerts **WS \_ Proxy \_ Eigenschaft \_ Max \_ ausstehende \_ Aufrufe** bietet Schutz vor einem Server mit langsamer Ausführung. Der Standardwert ist 100. Anwendungen müssen bei der Änderung der Standardeinstellungen vorsichtig sein.
-   Der Dienst Proxy bietet keine Sicherheitsgarantien, die über diejenigen hinausgehen, die in der [**WS- \_ Sicherheits \_ Beschreibungs**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) Struktur für die Kommunikation mit dem Server angegeben sind.
-   Achten Sie darauf, wenn Sie die Standardwerte für nach [richten](message.md) und [Kanäle](channel.md) auf dem Dienst Proxy ändern. Lesen Sie die Sicherheitsüberlegungen in Bezug auf Nachrichten und Kanäle, bevor Sie die zugehörigen Eigenschaften ändern.
-   Der Dienst Proxy verschlüsselt alle Anmelde Informationen, die er im Arbeitsspeicher speichert.

Die folgenden API-Elemente beziehen sich auf Dienst Proxys.

| Rückruf                                                          | BESCHREIBUNG                                                                                                                     |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [**WS- \_ Proxy \_ Nachrichten \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_proxy_message_callback) | Wird aufgerufen, wenn die Header der Eingabe Nachricht über gesendet werden oder wenn ein Ausgabe Nachrichten Header soeben empfangen wird. |



 



| Enumeration                                                 | Beschreibung                                                                               |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [**WS- \_ Aufrufe- \_ Eigenschaften- \_ ID**](/windows/desktop/api/WebServices/ne-webservices-ws_call_property_id)       | Listet optionale Parameter zum Konfigurieren eines Aufrufens für einen Client seitigen Dienst Vorgang auf. |
| [**WS- \_ Proxy- \_ Eigenschaften- \_ ID**](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id)     | Listet optionale Parameter zum Konfigurieren des Dienst Proxys auf.                         |
| [**WS- \_ Dienst \_ Proxy \_ Status**](/windows/desktop/api/WebServices/ne-webservices-ws_service_proxy_state) | Der Status des Dienst Proxys.                                                           |



 



| Funktion                                                       | BESCHREIBUNG                                                                       |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [**Wsabandoncall**](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall)                         | Bricht einen angegebenen-Rückruf für einen angegebenen Dienst Proxy ab.                           |
| [**Wsabortserviceproxy**](/windows/desktop/api/WebServices/nf-webservices-wsabortserviceproxy)             | Bricht alle ausstehenden Eingaben und Ausgaben für einen angegebenen Dienst Proxy ab.                |
| [**Wscall**](/windows/desktop/api/WebServices/nf-webservices-wscall)                                       | Nur intern. Serialisiert Argumente in eine Nachricht und sendet Sie über den Kanal. |
| [**Wscloseserviceproxy**](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy)             | Schließt einen Dienst Proxy für die Kommunikation.                                         |
| [**Wscreateserviceproxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy)           | Erstellt einen Dienst Proxy.                                                          |
| [**Wsfreeserviceproxy**](/windows/desktop/api/WebServices/nf-webservices-wsfreeserviceproxy)               | Gibt den einem Dienst Proxy zugeordneten Arbeitsspeicher frei.                              |
| [**Wsgetserviceproxyproperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetserviceproxyproperty) | Ruft eine angegebene Dienst Proxy Eigenschaft ab.                                     |
| [**Wsopeinserviceproxy**](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy)               | Öffnet einen Dienst Proxy für einen Dienst Endpunkt.                                      |
| [**Wsresetserviceproxy**](/windows/desktop/api/WebServices/nf-webservices-wsresetserviceproxy)             | Setzt den Dienst Proxy zurück.                                                             |



 



| Handle                                     | BESCHREIBUNG                                       |
|--------------------------------------------|---------------------------------------------------|
| [WS- \_ Dienst \_ Proxy](ws-service-proxy.md) | Ein nicht transparenter Typ, der zum Verweisen auf einen Dienst Proxy verwendet wird. |



 



| Struktur                                         | BESCHREIBUNG                 |
|---------------------------------------------------|-----------------------------|
| [**WS \_ - \_ aufrufeigenschaft**](/windows/desktop/api/WebServices/ns-webservices-ws_call_property)    | Gibt eine-aufrufeigenschaft an.  |
| [**WS \_ Proxy- \_ Eigenschaft**](/windows/desktop/api/WebServices/ns-webservices-ws_proxy_property). | Gibt eine Proxy Eigenschaft an. |



 

 

 




