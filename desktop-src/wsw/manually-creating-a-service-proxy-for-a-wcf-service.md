---
title: Manuelles Erstellen eines Dienstproxys für einen WCF-Dienst
description: Die einfachste Möglichkeit zum Erstellen eines Clientdienstproxys für einen WCF-Dienst (Windows Communication Foundation) ist die Dienstmodellebene mit dem WsUtil-Tool, wie im Thema Erstellen eines Clients beschrieben.
ms.assetid: ef545090-382b-44bd-b7ab-f5a285b6e202
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33133ae48dee89e72871712d445453e237116f6f1fa08cf66a76381ea8d3d424
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119927250"
---
# <a name="manually-creating-a-service-proxy-for-a-wcf-service"></a>Manuelles Erstellen eines Dienstproxys für einen WCF-Dienst

Die einfachste Möglichkeit zum Erstellen eines Clientdienstproxys für einen WCF-Dienst (Windows Communication Foundation) ist die [Dienstmodellebene](service-model-layer-overview.md) mit dem WsUtil-Tool, wie im Thema [Erstellen eines Clients](creating-a-client.md) beschrieben. Bei Bedarf können Sie jedoch auch manuell einen Dienstproxy erstellen. Diese API enthält eine [**WsCreateServiceProxy-Funktion**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) zum Erstellen des Dienstproxys sowie Strukturen, Enumerationen usw. zum Festlegen der Eigenschaften, die für die Interoperabilität mit WCF erforderlich sind.

WCF stellt eine Reihe von Standardbindungen bereit, die jeweils auf ein bestimmtes Verwendungsszenario ausgerichtet sind. Welche Bindung der Dienst verwendet, mit dem Sie eine Verbindung herstellen möchten, bestimmt wiederum, welche Kanaleigenschaften Sie anpassen müssen, damit Ihr Dienstproxy mit dem Dienst kommunizieren kann.

## <a name="creating-a-service-proxy-for-wcfs-wshttpbinding"></a>Erstellen eines Dienstproxys für WSHttpBinding von WCF

WSHttpBinding ist für das Hauptszenario für Internetwebdienste vorgesehen. Sie verwendet die neuere SOAP-Version 1.2 und WS-Addressing Version 1.0 und ermöglicht eine Vielzahl von Sicherheitseinstellungen über die öffentlichen HTTP- und HTTPS-Transporte. WWSAPI verfügt nicht über eine Entsprechung von WSHttpBinding (oder einer der WCF-Standardbindungen), aber da die SOAP-Standardversion, WS-Addressing Version und das Codierungsformat mit denen in WSHttpBinding übereinstimmen, ist das Erstellen eines Dienstproxys für einen Dienst, der WSHttpBinding verwendet, einfach. Wenn Sie beispielsweise einen Dienstproxy erstellen möchten, um ohne Sicherheit mit einem WSHttpBinding-Endpunkt zu kommunizieren, können Sie einfach Code wie den folgenden Codeausschnitt verwenden (Variablendeklaration und Heap- und Fehlererstellung werden weggelassen). Beachten Sie, dass im Aufruf der [**WsCreateServiceProxy-Funktion**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) keine Kanaleigenschaften oder Sicherheitsbeschreibungen angegeben sind.


```C++
// Create the proxy

hr = WsCreateServiceProxy(
        WS_CHANNEL_TYPE_REQUEST, 
        WS_HTTP_CHANNEL_BINDING, 
        NULL, // security description
        NULL, // proxy properties
        0, // proxy property count
        NULL, // channel properties
        0, // channel property count
        &proxy, 
        error);
```



Die Funktion erstellt den Dienstproxy und gibt im *parameter serviceProxy* einen Zeiger darauf zurück (&Proxy im obigen Funktionsaufruf).

## <a name="creating-a-service-proxy-for-wcfs-basichttpbinding"></a>Erstellen eines Dienstproxys für basicHttpBinding von WCF

Wenn Sie manuell einen Dienstproxy für einen WCF-Dienst erstellen, der eine BasicHttpBinding-Bindung verwendet, müssen Sie jedoch die SOAP-Version und WS-Addressing Eigenschaften des Kanals festlegen. Dies liegt daran, dass WWSAPI standardmäßig SOAP-Version 1.2 und WS-Addressing 1.0 verwendet. Die BasicHttpBinding von WCF verwendet dagegen SOAP-Version 1.1 und keine WS-Adressierung.

Um die SOAP-Version und WS-Addrssing Eigenschaften des Kanals festzulegen, deklarieren Sie ein Array von [**WS \_ CHANNEL \_ PROPERTY-Strukturen,**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property) das die Kanaleigenschaften und zugehörigen Informationen enthalten soll.


```
WS_CHANNEL_PROPERTY channelProperties[4]; // Array to hold up to 4 channel properties

ULONG channelPropertyCount = 0; // Count of properties set
 
WS_ENVELOPE_VERSION soapVersion = WS_ENVELOPE_VERSION_SOAP_1_1; // Set required SOAP version
channelProperties[channelPropertyCount].id = WS_CHANNEL_PROPERTY_ENVELOPE_VERSION; // Type of first channel property
channelProperties[channelPropertyCount].value = &soapVersion; // Address of the SOAP version value
channelProperties[channelPropertyCount].valueSize = sizeof(soapVersion); // Size of the value
channelPropertyCount++; // Increment property count
 
WS_ADDRESSING_VERSION addressingVersion = WS_ADDRESSING_VERSION_TRANSPORT; // Set required WS-Addressing value
channelProperties[channelPropertyCount].id = WS_CHANNEL_PROPERTY_ADDRESSING_VERSION; // Type of second channel property
channelProperties[channelPropertyCount].value = &addressingVersion ; // Address of the WS-Addressing value
channelProperties[channelPropertyCount].valueSize = sizeof(addressingVersion ); // Size of the value
channelPropertyCount++; // Increment property count
 
// add more channel properties here

```



Übergeben Sie dann das Array der Kanaleigenschaften (channelProperties) und die Anzahl der Eigenschaften (channelPropertyCount) an [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) (oder [**WsCreateChannel,**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannel) wenn Sie auf Kanalebene arbeiten).


```
// Create the proxy

hr = WsCreateServiceProxy(
        WS_CHANNEL_TYPE_REQUEST, 
        WS_HTTP_CHANNEL_BINDING, 
        NULL, // security description
        NULL, // proxy properties
        0, // proxy property count
        channelProperties, // channel properties
        channelPropertyCount, // channel property count
        &proxy, 
        error);
```



Das Array, das Sie zum Speichern der Eigenschaften deklariert haben, wird in **WsCreateServiceProxy** kopiert. Daher können Sie den Arbeitsspeicher für das Eigenschaftenarray sofort nach dem Aufruf der Funktion freigeben. Wenn Sie den Arbeitsspeicher aus dem Stapel zuordnen (wie im obigen Codeausschnitt), können Sie auch direkt nach dem Aufruf von der Funktion zurückgeben.

## <a name="other-bindings"></a>Andere Bindungen

Darüber hinaus bietet WWSAPI Mechanismen zum Erstellen von Dienstproxys für die Kommunikation mit WCF-Diensten mithilfe anderer Bindungen wie NetTcpBinding und WSFederationHttpBinding. Viele dieser Bindungen erfordern das Festlegen zusätzlicher Kanaleigenschaften, z. B. Sicherheitsbeschreibungen. Beispiele, die die Verwendung anderer Bindungen veranschaulichen, finden Sie im Abschnitt [beispiele für Windows Webdienste,](windows-web-services-examples.md)insbesondere die Unterabschnitte [TCP-Kanalebenenbeispiele,](tcp-channel-layer-examples.md) [BEISPIELE FÜR HTTP-Kanalebene](http-channel-layer-examples.md)und [Beispiele für Sicherheitskanalebenen.](security-channel-layer-examples.md)

 

 




