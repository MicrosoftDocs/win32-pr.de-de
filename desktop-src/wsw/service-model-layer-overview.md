---
title: Übersicht über die Dienstmodellebene
description: Die WWSAPI-Dienstmodell-API modelliert die Kommunikation zwischen einem Client und einem Dienst als Methodenaufrufe und nicht als Datennachrichten.
ms.assetid: a1ed1e3c-94ae-4383-9251-83caf2e3ebf3
keywords:
- Service Model Layer Overview Web Services for Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b182678568c7825cbf0b18bbbfd132dd5287d3f05b9ae6a372e6e5c70cd06d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962954"
---
# <a name="service-model-layer-overview"></a>Übersicht über die Dienstmodellebene

Die WWSAPI-Dienstmodell-API modelliert die Kommunikation zwischen einem Client und einem Dienst als Methodenaufrufe und nicht als Datennachrichten. Im Gegensatz zur [Kanalebene,](channel-layer-overview.md)die einen herkömmlicheren [Nachrichtenaustausch](message.md) zwischen Client und Dienst unterstützt, verwaltet das Dienstmodell die Kommunikation automatisch über einen Dienstproxy auf dem Client und einen Diensthost im Dienst. Dies bedeutet, dass der Client generierte Funktionen aufruft und der Server Rückrufe implementiert.


Betrachten Sie beispielsweise einen Rechnerdienst, der Addition und Subtraktion für zwei Zahlen ausführt. Addition und Subtraktion sind Vorgänge, die auf natürliche Weise als Methodenaufrufe dargestellt werden.

![Diagramm, das zeigt, wie ein Rechnerdienst mit einem Client über Methodenaufrufe zur Addition und Subtraktion kommuniziert.](images/servicemodelintro.png)

Das Dienstmodell stellt die Kommunikation zwischen Client und Dienst als deklarierte Methodenaufrufe dar und verbirgt daher die Kommunikationsdetails der zugrunde liegenden Kanalebene aus der Anwendung, sodass der Dienst einfacher implementiert werden kann.

## <a name="specifying-a-service"></a>Angeben eines Diensts

Ein Dienst muss in Bezug auf seine Nachrichtenaustauschmuster und seine Netzwerkdatendarstellung angegeben werden. Für Dienste wird diese Spezifikation in der Regel als WSDL- und XML-Schemadokumente bereitgestellt.

Das WSDL-Dokument ist ein XML-Dokument, das die Kanalbindung und die Nachrichtenaustauschmuster des Diensts enthält, während das XML-Schemadokument ein XML-Dokument ist, das die Datendarstellung der einzelnen Nachrichten definiert.

Für den Rechnerdienst und seine Additions- und Subtraktionsvorgänge könnte das WSDL-Dokument wie im folgenden Beispiel aussehen:

``` syntax
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" 
xmlns:wsu="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-utility-1.0.xsd" 
xmlns:soapenc="http://schemas.xmlsoap.org/soap/encoding/" xmlns:tns="http://Example.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:wsp="http://schemas.xmlsoap.org/ws/2004/09/policy" 
xmlns:wsap="http://schemas.xmlsoap.org/ws/2004/08/addressing/policy" xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
xmlns:msc="http://schemas.microsoft.com/ws/2005/12/wsdl/contract" xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" 
xmlns:soap12="http://schemas.xmlsoap.org/wsdl/soap12/" xmlns:wsa10="http://www.w3.org/2005/08/addressing" 
xmlns:wsx="http://schemas.xmlsoap.org/ws/2004/09/mex" targetNamespace="http://Example.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:portType name="ICalculator">
  <wsdl:operation name="Add">
   <wsdl:input wsaw:Action="http://Example.org/ICalculator/Add" 
   message="tns:ICalculator_Add_InputMessage" />
   <wsdl:output wsaw:Action="http://Example.org/ICalculator/AddResponse" 
   message="tns:ICalculator_Add_OutputMessage" />
  </wsdl:operation>
 </wsdl:portType>
</wsdl:definitions>
```

Ebenso kann das XML-Schema wie folgt definiert werden:

``` syntax
<xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
 <xs:element name="Add">
  <xs:complexType>
   <xs:sequence>
    <xs:element minOccurs="0" name="a" type="xs:int" />
    <xs:element minOccurs="0" name="b" type="xs:int" />
   </xs:sequence>
  </xs:complexType>
 </xs:element>
 <xs:element name="AddResponse">
  <xs:complexType>
   <xs:sequence>
    <xs:element minOccurs="0" name="result" type="xs:int" 
    />
   </xs:sequence>
  </xs:complexType>
 </xs:element>
</xs:schema> 
```

## <a name="converting-metadata-to-code"></a>Konvertieren von Metadaten in Code

Das Dienstmodell stellt die [WsUtil.exe](web-service-compiler-tool.md) als Tool zum Verarbeiten dieser Metadatendokumente bereit und konvertiert eine WSDL-Datei in einen C-Header und Quelldateien.

![Diagramm, das zeigt, wie WsUtil.exe eine WSDL-Datei in einen C-Header und Quelldateien konvertiert.](images/doctotool.png)

Der [WsUtil.exe](web-service-compiler-tool.md) generiert Header und Quellen für die Dienstimplementierungen sowie clientseitige Dienstvorgänge für den Client.

## <a name="calling-the-calculator-service-from-a-client"></a>Aufrufen des Rechnerdiensts von einem Client

Wie bei der Dienstimplementierungen muss der Client die generierten Header oder Header enthalten.

``` syntax
#include "CalculatorProxyStub.h"
```

Nun kann die Clientanwendung einen Dienstproxy erstellen und öffnen, um mit der Kommunikation mit dem Rechnerdienst zu beginnen.

``` syntax
WS_ENDPOINT_ADDRESS address = {0};
WS_STRING uri= WS_STRING_VALUE(L"http://localhost/example");
address.uri = uri;

if (FAILED (hr = WsCreateServiceProxy(WS_CHANNEL_TYPE_REQUEST, WS_HTTP_CHANNEL_BINDING, NULL, NULL, 0, &serviceProxy, error)))
    goto Error;

if (FAILED (hr = WsOpenServiceProxy(serviceProxy, &address, NULL, error)))
    goto Error;
```

Die Anwendung kann den Add-Vorgang für den Rechnerdienst mit dem folgenden Code aufrufen:

``` syntax
if (FAILED (hr = DefaultBinding_ICalculator_Add(serviceProxy, heap, 1, 2, &result, NULL, 0, NULL, error)))
    goto Error;
```

Eine vollständige Implementierung des Rechnerdiensts finden Sie im Codebeispiel unter [HttpCalculatorClientExample.](httpcalculatorclientexample.md)

## <a name="service-model-components"></a>Dienstmodellkomponenten

Die Interaktion der einzelnen WWSAPI-Dienstmodellkomponenten im Rechnerbeispiel sieht wie folgt aus:

-   Der Client erstellt einen [Dienstproxy](service-proxy.md) und öffnet ihn.
-   Der Client ruft die Add-Funktion des Diensts auf und übergibt den Dienstproxy.
-   Die Nachricht wird gemäß den Serialisierungsmetadaten in den Header- und Quelldateien serialisiert, die vom Metadatentool ([WsUtil.exe](web-service-compiler-tool.md)) generiert werden.
-   Die Nachricht wird in den Kanal geschrieben und über das Netzwerk an den Dienst übertragen.
-   Auf serverseitiger Seite wird der Dienst auf einem Diensthost gehostet und verfügt über einen Endpunkt, der auf den ICalculator-Vertrag lauscht.
-   Mithilfe der Dienstmodellmetadaten im Stub deserialisiert der Dienst die Nachricht vom Client und verteilt sie an den Stub.
-   Der serverseitige Dienst ruft die Add-Methode auf und übergibt sie an den Vorgangskontext. Dieser Vorgangskontext enthält den Verweis auf die eingehende Nachricht.

![Diagramm, das die Interaktion der einzelnen WWSAPI-Dienstmodellkomponenten zeigt.](images/servicemodellayout.png)

Komponenten

-   [Diensthost:](service-host.md)Hostet einen Dienst.
-   [Dienstproxy:](service-proxy.md)Definiert, wie ein Client mit einem Dienst kommuniziert.
-   [Kontext:](context.md)Eigenschaftenbehälter zum Verfügbarmachen zustandsspezifischer Informationen für einen Dienstvorgang.
-   [Contract:](contract.md)Die Schnittstellendefinition eines Diensts. Beispielsweise stellt ICalculator einen Vertrag für den Rechnerdienst in unserem Beispielcode dar.
-   [WsUtil.exe: ](web-service-compiler-tool.md)Das Dienstmodellmetadatentool zum Generieren von Proxys und Stubs.

 

 




