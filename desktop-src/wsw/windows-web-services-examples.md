---
title: Beispiele für Windows-Webdienste
description: In den folgenden Beispielen wird die Verwendung der Windows-Webdienste-API veranschaulicht.
ms.assetid: 8a557ef0-a88a-4257-a181-57f2dca9022f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e74aec03c4822fb9ba270076b5127dd37d145fb5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106342038"
---
# <a name="windows-web-services-examples"></a>Beispiele für Windows-Webdienste

In den folgenden Beispielen wird die Verwendung der Windows-Webdienste-API veranschaulicht.

-   [Beispiele für Dienst Modelle](service-model-examples.md)
-   [Beispiele für die TCP-Kanal Schicht](tcp-channel-layer-examples.md)
-   [Beispiele für HTTP-Kanal Ebenen](http-channel-layer-examples.md)
-   [Beispiele für UDP-Kanal Ebenen](udp-channel-layer-examples.md)
-   [Beispiele für Named Pipe-Kanal Ebenen](named-pipes-channel-layer-examples.md)
-   [Nachrichtenbeispiele](message-examples.md)
-   [XML-Beispiele](xml-examples.md)
-   [Beispiele für Async-Modelle](async-model-examples.md)
-   [Beispiele für Sicherheits Kanal Ebenen](security-channel-layer-examples.md)
-   [Datei Replikations Beispiele](file-replication-examples.md)

## <a name="service-model-examples"></a>Beispiele für Dienst Modelle

Rechner Dienst: Client: [httpcalculatorclientexample](httpcalculatorclientexample.md), Server: [httpcalculatorserviceexample](httpcalculatorserviceexample.md).

Rechner Dienst mit SSL-Transportsicherheit: Client: [httpcalculatorwithsslclientexample](httpcalculatorwithsslclientexample.md), Server: [httpcalculatorwithsslserviceexample](httpcalculatorwithsslserviceexample.md).

Rechner Dienst mit Benutzername über SSL-Sicherheit im gemischten Modus: Client: [httpcalculatorwithusernameoversslclientexample](httpcalculatorwithusernameoversslclientexample.md), Server: [httpcalculatorwithusernameoversslserviceexample](httpcalculatorwithusernameoversslserviceexample.md).

Rechner Dienst mit Kerberos über SSL-Sicherheit im gemischten Modus: Client: [httpcalculatorwithkerberosoversslclientexample](httpcalculatorwithkerberosoversslclientexample.md), Server: [httpcalculatorwithkerberosoversslserviceexample](httpcalculatorwithkerberosoversslserviceexample.md).

Bestell Dienst: Client: [httppurchaseorderclientexample](httppurchaseorderclientexample.md), Server: [httppurchaseorderserviceexample](httppurchaseorderserviceexample.md).

Bestell Dienst mit SSL-Transportsicherheit: Client: [httppurchaseorderwithsslclientexample](httppurchaseorderwithsslclientexample.md), Server: [httppurchaseorderwithsslserviceexample](httppurchaseorderwithsslserviceexample.md).

Bestell Dienst mit Benutzername über SSL-Sicherheit im gemischten Modus: Client: [httppurchaseorderwithusernameoversslclientexample](httppurchaseorderwithusernameoversslclientexample.md), Server: [httppurchaseorderwithusernameoversslserviceexample](httppurchaseorderwithusernameoversslserviceexample.md).

Bestell Dienst mit Kerberos über SSL-Sicherheit im gemischten Modus: Client: [httppurchaseorderwithkerberosoversslclientexample](httppurchaseorderwithkerberosoversslclientexample.md), Server: [httppurchaseorderwithkerberosoversslserviceexample](httppurchaseorderwithkerberosoversslserviceexample.md).

Nicht typisierter Bestell Dienst: Server: [untypedserviceexample](untypedserviceexample.md). Client: [untypedcliumtexample](untypedclientexample.md)

Sitzungs basierter Rechner: Server: [sessionfullcalculatorserviceexample](sessionfullcalculatorserviceexample.md). Client:[sessionfullcalculatorclieintexample](sessionfullcalculatorclientexample.md).

Rechner, der eine benutzerdefinierte Kanal-und Listenerimplementierung verwendet: Server:[httpcalculatorwithlayeredchannelserviceexample](httpcalculatorwithlayeredchannelserviceexample.md). Client:[httpcalculatorwithlayeredchannelclieintexample](httpcalculatorwithlayeredchannelclientexample.md).

Rechner, der einen codierten Kanal verwendet: Server:[httpcalculatorwithencodecodchannelserviceexample](httpcalculatorwithencodedchannelserviceexample.md). Client:[httpcalculatorwithencodecodchannelclieintexample](httpcalculatorwithencodedchannelclientexample.md).

Dienst, der unformatierte HTTP-Anforderungen (nicht SOAP) verarbeitet: Client:[httprawclientexample](httprawclientexample.md). Server:[httprawserviceexample](httprawserviceexample.md).

Benachrichtigung zum Abbruch des Dienst Vorgangs: Server: [blockingserviceexample](blockingserviceexample.md). Client:[servicecancellationexample](servicecancellationexample.md).

Abbruch aufrufen: Server: [sessionfullcalculatorserviceexample](sessionfullcalculatorserviceexample.md). Client:[callabandonexample](callabandonexample.md).

Erstellen Sie manuell eine Richtlinien Beschreibung, und verwenden Sie Sie zum Erstellen eines Dienst Proxys: [policytemplateexample](policytemplateexample.md).

## <a name="tcp-channel-layer-examples"></a>Beispiele für die TCP-Kanal Schicht

Ein TCP-Beispiel, das Nachrichten mit einem unidirektionalen Muster sendet: Client: [onewaytcpclientexample](onewaytcpclientexample.md), Server: [onewaytcpserverexample](onewaytcpserverexample.md)

Ein TCP-Beispiel, das Nachrichten mit einem Anforderung-Antwort-Muster sendet: Client: [requestreplytcpclientexample](requestreplytcpclientexample.md), Server: [requestreplytcpserverexample](requestreplytcpserverexample.md)

Ein TCP-Streaming-Beispiel: Client: [streamingtcpcliumtexample](streamingtcpclientexample.md), Server: [streamingtcpserverexample](streamingtcpserverexample.md)

Ein Async Streaming TCP-Beispiel: Client: [asyncstreamingtcpclieintexample](asyncstreamingtcpclientexample.md), Server: [asyncstreamingtcpserverexample](asyncstreamingtcpserverexample.md)

## <a name="http-channel-layer-examples"></a>Beispiele für HTTP-Kanal Ebenen

Ein HTTP-Beispiel: Client: [httpclieintexample](httpclientexample.md), Server: [httpserverexample](httpserverexample.md)

Ein HTTP-Beispiel, in dem die Streaming-APIs verwendet werden: Client: [streaminghttpclieintexample](streaminghttpclientexample.md), Server: [streaminghttpserverexample](streaminghttpserverexample.md)

## <a name="udp-channel-layer-examples"></a>Beispiele für UDP-Kanal Ebenen

Ein UDP-Beispiel, das Nachrichten mit einem unidirektionalen Muster sendet: Client: [onewayudpclientexample](onewayudpclientexample.md), Server: [onewayudpserverexample](onewayudpserverexample.md)

Ein UDP-Beispiel, das Nachrichten mit einem Multicast Anforderungs Antwortmuster sendet: Client: [multicastudpclientexample](multicastudpclientexample.md), Server: [multicastudpserverexample](multicastudpserverexample.md) Folgendes ist das gleiche Beispiel, wobei IPv6-Adressierung verwendet wird: Client: [MulticastUdpClientExample6](multicastudpclientexample6.md), Server: [MulticastUdpServerExample6](multicastudpserverexample6.md)

## <a name="named-pipes-channel-layer-examples"></a>Kanalebenenbeispiele für benannte Pipes

Ein Named Pipes-Beispiel, das Nachrichten mit einem Anforderung-Antwort-Muster sendet: Client: [requestreplynamedpipesclientexample](requestreplynamedpipesclientexample.md), Server: [requestreplynamedpipesserverexample](requestreplynamedpipesserverexample.md)

Ein Streaming Named Pipes-Beispiel: Client: [streamingnamedpipesclieintexample](streamingnamedpipesclientexample.md), Server: [streamingnamedpipesserverexample](streamingnamedpipesserverexample.md)

## <a name="message-examples"></a>Nachrichtenbeispiele

Ein Beispiel, in dem benutzerdefinierte Nachrichten Header verwendet werden: [customheaderexample](customheaderexample.md)

Ein Beispiel, das eine Meldung codiert und decodiert: [MessageEncodingExample](messageencodingexample.md)

Ein Beispiel, das eine Nachricht weiterleitet: [forwardmessageexample](forwardmessageexample.md)

## <a name="xml-examples"></a>XML-Beispiele

Ein Beispiel für das Schreiben und Lesen von XML mit einem XML-Puffer " [lesebeschreitexmlexample](readwritexmlexample.md) "

Ein Beispiel für das Schreiben und Lesen von Binärdaten mithilfe von MTOM, wswrite [tebytes](readwritebytesxmlexample.md) , wspushbytes und wspullbytes

Ein Beispiel für die Navigation eines XML-Puffers [navigatexmlexample](navigatexmlexample.md)

Ein Beispiel für das Lesen eines XML-Dokument Knotens nach Knoten " [infoxmlexample](readxmlexample.md) "

Ein Beispiel für das Suchen und Anzeigen eines XML-Attributs "read [attributeexample](readattributeexample.md) "

Ein Beispiel für das Schreiben und Lesen eines Arrays von Elementen " [leseschreitearrayexample](readwritearrayexample.md) "

Ein Beispiel, das ein Element in einen XML-Puffer [insertelementexample](insertelementexample.md) einfügt

Ein Beispiel für die Verwendung einiger XML-Puffer-Hilfsobjekte [xmlbufferexample](xmlbufferexample.md)

Ein Beispiel für das Schreiben und Lesen eines abgeleiteten Typs mithilfe der von wsutil generierten Hilfsfunktionen [derivedtypeexample](derivedtypeexample.md)

## <a name="async-model-examples"></a>Beispiele für Async-Modelle

Ein Beispiel, das das Modell für asynchrone Funktionen veranschaulicht. [Asyncmodelexample](asyncmodelexample.md)

## <a name="security-channel-layer-examples"></a>Beispiele für Sicherheits Kanal Ebenen

Windows-Transportsicherheit über TCP: Client: [requestreplytcpclientwithwindowstransportsecurityexample](requestreplytcpclientwithwindowstransportsecurityexample.md), Server: [requestreplytcpserverwithwindowstransportsecurityexample](requestreplytcpserverwithwindowstransportsecurityexample.md).

Windows-Transportsicherheit über Named Pipes: Client: [requestreplynamedpipesclientwithwindowstransportsecurityexample](requestreplynamedpipesclientwithwindowstransportsecurityexample.md), Server: [requestreplynamedpipesserverwithwindowstransportsecurityexample](requestreplynamedpipesserverwithwindowstransportsecurityexample.md).

SSL-Transportsicherheit: Client: [httpclientwithsslexample](httpclientwithsslexample.md), Server: [httpserverwithsslexample](httpserverwithsslexample.md).

Benutzername über SSL-Sicherheit im gemischten Modus: Client: [httpclientwithusernameoversslexample](httpclientwithusernameoversslexample.md), Server: [httpserverwithusernameoversslexample](httpserverwithusernameoversslexample.md).

Benutzername über SSL-Sicherheit im gemischten Modus: Client: [httpclientwithkerberosoversslexample](httpclientwithkerberosoversslexample.md), Server: [httpserverwithkerberosoversslexample](httpserverwithkerberosoversslexample.md).

## <a name="metadata-example"></a>Metadatenbeispiel

In den folgenden Beispielen wird gezeigt, wie WSDL-und Richtlinien Dokumente verarbeitet werden, mit dem Ziel, Informationen über das von einem Endpunkt unterstützte Protokoll zu extrahieren.

Benutzername über SSL-Sicherheit im gemischten Modus: [MetadataImportWithUsernameOverSslExample](metadataimportwithusernameoversslexample.md). Ausgestelltes Token über SSL-Sicherheit im gemischten Modus: [MetadataImportWithIssuedTokenOverSslExample](metadataimportwithissuedtokenoversslexample.md). X509-Zertifikat über SSL-Sicherheit im gemischten Modus: [MetadataImportWithX509OverSslExample](metadataimportwithx509oversslexample.md).

## <a name="ws-metadata-exchange-example"></a>WS-Metadata Exchange-Beispiel

In den folgenden Beispielen wird gezeigt, wie WS-MetadataExchange auf dem [WS- \_ Dienst \_ Host](ws-service-host.md)aktiviert wird.

TCP-Dienst mit aktiviertem WS-MetadataExchange: [MetadataExchangeSample](metadataexchangesample.md). Der WCF-dienstmonikerclient, der den TCP-Dienst mit aktiviertem WS-MetadataExchange aufruft: [servicemonikersample](servicemonikersample.md).

## <a name="custom-headers-and-service-model"></a>Benutzerdefinierte Header und Dienstmodell

In den folgenden Beispielen wird gezeigt, wie benutzerdefinierte Header mit dem [WS- \_ Dienst \_ Proxy](ws-service-proxy.md) bzw. dem [WS- \_ Dienst \_ Host](ws-service-host.md) verwendet werden.

Client: [httpcustomheaderpurchaseorderclieintexample](httpcustomheaderpurchaseorderclientexample.md), Server: [httpcustomheaderpurchaseorderserviceexample](httpcustomheaderpurchaseorderserviceexample.md).

## <a name="file-replication-sample"></a>Datei Replikations Beispiel

Ein umfassendes Beispiel, das die Implementierung eines Datei Replikations Dienstanbieter veranschaulicht: Tool: [filereptoolexample](filereptoolexample.md), Service: [filerepserviceexample](filerepserviceexample.md).

## <a name="wcf-public-service-interoperation"></a>Interoperabilität mit öffentlichem WCF-Dienst

Ein Windows-Webdienst Client kommuniziert mit einem WCF-Dienst Client: [wcfpublicservicesample](wcfpublicservicesample.md).

## <a name="custom-http-proxy"></a>Benutzerdefinierter HTTP-Proxy

Ein Windows-Webdienst Client kommuniziert mit einem ASMX-TerraService-Dienst unter Verwendung eines benutzerdefinierten Proxy Clients: [asmxterraservicesamplewithcustomproxy](asmxterraservicesamplewithcustomproxy.md)

 

 




