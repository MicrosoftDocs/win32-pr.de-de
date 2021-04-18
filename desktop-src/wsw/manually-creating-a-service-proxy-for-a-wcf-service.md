---
title: Manuelles Erstellen eines Dienst Proxys für einen WCF-Dienst
description: Die einfachste Möglichkeit zum Erstellen eines Client Dienst Proxys für einen Windows Communication Foundation (WCF)-Dienst befindet sich auf der Dienstmodell Ebene mit dem wsutil-Tool, wie im Thema Erstellen eines Clients beschrieben.
ms.assetid: ef545090-382b-44bd-b7ab-f5a285b6e202
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e061fda95298986ee6336dee0662d80c89a0a5a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337796"
---
# <a name="manually-creating-a-service-proxy-for-a-wcf-service"></a>Manuelles Erstellen eines Dienst Proxys für einen WCF-Dienst

Die einfachste Möglichkeit zum Erstellen eines Client Dienst Proxys für einen Windows Communication Foundation (WCF)-Dienst befindet sich auf der [Dienstmodell](service-model-layer-overview.md) Ebene mit dem wsutil-Tool, wie im Thema [Erstellen eines Clients](creating-a-client.md) beschrieben. Falls erforderlich, können Sie einen Dienst Proxy jedoch auch manuell erstellen. Diese API enthält eine [**wscreateserviceproxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) -Funktion zum Erstellen des Dienst Proxys sowie Strukturen, Enumerationen usw., um die Eigenschaften festzulegen, die für die Zusammenarbeit mit WCF erforderlich sind.

WCF bietet eine Reihe von Standard Bindungen, die jeweils auf ein bestimmtes Verwendungs Szenario abzielen. Die Bindung des Dienstanbieter, mit dem Sie eine Verbindung herstellen möchten, bestimmt wiederum, welche Channeleigenschaften Sie für Ihren Dienst Proxy für die Kommunikation mit dem Dienst anpassen müssen.

## <a name="creating-a-service-proxy-for-wcfs-wshttpbinding"></a>Erstellen eines Dienst Proxys für die WSHttpBinding von WCF

WSHttpBinding ist für das Hauptszenario der Internet-Webdienste. Es verwendet die neuere SOAP-Version 1,2 und WS-Addressing Version 1,0 und ermöglicht eine Vielzahl von Sicherheitseinstellungen über die öffentlichen http-und HTTPS-Transporte. Wwsapi verfügt nicht über eine Entsprechung von "WSHttpBinding" (oder eine der WCF-Standard Bindungen), aber da die standardmäßige SOAP-Version, WS-Addressing Version und das Codierungsformat mit denen in wsHttpBinding übereinstimmen, ist das Erstellen eines Dienst Proxys für einen Dienst, der die WSHttpBinding verwendet, unkompliziert. Wenn Sie z. b. einen Dienst Proxy für die Kommunikation mit einem WSHttpBinding-Endpunkt ohne Sicherheit erstellen möchten, können Sie einfach Code wie den folgenden Code Ausschnitt verwenden (Variablen Deklaration und Heap-und Fehler Erstellung werden weggelassen). Beachten Sie, dass im Aufrufen der [**wscreateserviceproxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) -Funktion keine Kanaleigenschaften oder Sicherheits Beschreibung angegeben ist.


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



Die-Funktion erstellt den Dienst Proxy und gibt einen Zeiger darauf im *Service Proxy* -Parameter (&Proxy im obigen Funktionsaufrufen) zurück.

## <a name="creating-a-service-proxy-for-wcfs-basichttpbinding"></a>Erstellen eines Dienst Proxys für die BasicHttpBinding von WCF

Wenn Sie einen Dienst Proxy für einen WCF-Dienst, der eine basicHttpBinding-Bindung verwendet, manuell erstellen, müssen Sie jedoch die SOAP-Version und WS-Addressing Eigenschaften des Kanals festlegen. Der Grund hierfür ist, dass wwsapi standardmäßig SOAP-Version 1,2 und WS-Addressing 1,0 verwendet. Die BasicHttpBinding von WCF hingegen verwendet SOAP-Version 1,1 und keine WS-Adressierung.

Zum Festlegen der SOAP-Version und der WS-Addrssing Eigenschaften des Kanals deklarieren Sie ein Array von [**WS- \_ \_ channeleigenschaftenstrukturen**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property) , die die Channeleigenschaften und die zugehörigen Informationen enthalten sollen.


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



Übergeben Sie dann das Array der Channeleigenschaften (channelproperties) und die Anzahl der Eigenschaften (channelpropertycount) an den [**wscreateserviceproxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) (oder an [**wscreatechannel**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannel) , wenn Sie auf der Kanal Ebene arbeiten).


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



Das Array, das Sie zum Speichern der Eigenschaften deklariert haben, wird in **wscreateserviceproxy** kopiert. Daher können Sie den Speicher für das Eigenschafts Array sofort nach dem Aufrufen der Funktion freigeben. Wenn Sie den Arbeitsspeicher aus dem Stapel zuordnen (wie z. b. den obigen Code Ausschnitt), können Sie auch direkt nach dem-Befehl von der-Funktion zurückgeben.

## <a name="other-bindings"></a>Andere Bindungen

Außerdem bietet wwsapi Mechanismen zum Erstellen von Dienst Proxys für die Kommunikation mit WCF-Diensten mit anderen Bindungen, wie z. b. NetTcpBinding und WSFederationHttpBinding. Viele dieser Bindungen erfordern das Festlegen zusätzlicher Channeleigenschaften, z. b. Sicherheits Deskriptoren. Beispiele, die die Verwendung anderer Bindungen veranschaulichen, finden Sie im Abschnitt [Beispiele für Windows-Webdienste](windows-web-services-examples.md), insbesondere in den Beispielen für die [TCP-channelschicht](tcp-channel-layer-examples.md), Beispiele für die [http-Kanal Schicht](http-channel-layer-examples.md)und [Beispiele für Sicherheits Kanal Ebenen](security-channel-layer-examples.md) .

 

 




