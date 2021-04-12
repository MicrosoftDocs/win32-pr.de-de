---
title: Übersicht über die Dienstmodell Ebene
description: Die wwsapi-Dienstmodell-API modelliert die Kommunikation zwischen einem Client und einem Dienst als Methodenaufrufe und nicht als Daten Nachrichten.
ms.assetid: a1ed1e3c-94ae-4383-9251-83caf2e3ebf3
keywords:
- Übersicht über die Dienstmodell Ebene Webdienste für Windows
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c74861f0e2ed13b35e308d1314aec2a33dc28c31
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/12/2021
ms.locfileid: "104351118"
---
# <a name="service-model-layer-overview"></a>Übersicht über die Dienstmodell Ebene

Die wwsapi-Dienstmodell-API modelliert die Kommunikation zwischen einem Client und einem Dienst als Methodenaufrufe und nicht als Daten Nachrichten. Im Gegensatz zur [Kanal Ebene](channel-layer-overview.md), die den herkömmlichen [Nachrichten](message.md) Austausch zwischen Client und Dienst unterstützt, verwaltet das Dienstmodell die Kommunikation automatisch mithilfe eines Dienst Proxys auf dem Client und einem Dienst Host auf dem Dienst. Dies bedeutet, dass der Client generierte Funktionen aufruft und der Server Rückrufe implementiert.


Nehmen Sie beispielsweise einen Rechner Dienst an, der eine Addition und Subtraktion zweier Zahlen ausführt. Addition und Subtraktion sind Vorgänge, die auf natürliche Weise als Methodenaufrufe dargestellt werden.

![Diagramm, das zeigt, wie ein Rechner Dienst mithilfe von Methoden aufrufen für Addition und Subtraktion mit einem Client kommuniziert.](images/servicemodelintro.png)

Das Dienstmodell stellt die Kommunikation zwischen dem Client und dem Dienst als deklarierte Methodenaufrufe dar und verbirgt somit die Kommunikations Details der zugrunde liegenden Kanal Ebene von der Anwendung, sodass der Dienst leichter implementiert werden kann.

## <a name="specifying-a-service"></a>Angeben eines Dienstanbieter

Ein Dienst muss in Bezug auf die Nachrichtenaustausch Muster und seine Netzwerkdaten Darstellung angegeben werden. Für-Dienste wird diese Spezifikation normalerweise als WSDL-und XML-Schema Dokumente bereitgestellt.

Beim WSDL-Dokument handelt es sich um ein XML-Dokument, das die kanalbindung und die Nachrichtenaustausch Muster des Dienstanbieter enthält, während das XML-Schema Dokument ein XML-Dokument ist, das die Datendarstellung der einzelnen Nachrichten definiert.

Für den Rechner Dienst und seine Additions-und Subtraktions Vorgänge könnte das WSDL-Dokument wie im folgenden Beispiel aussehen:

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

Ebenso kann das zugehörige XML-Schema wie folgt definiert werden:

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

## <a name="converting-metadata-to-code"></a>Metadaten werden in Code umgerechnet

Das Dienstmodell stellt den [WsUtil.exe](web-service-compiler-tool.md) als Tool zum Verarbeiten dieser Metadatendokumente bereit und umwandelt eine WSDL-Datei in einen C-Header und Quelldateien.

![Diagramm, das zeigt, wie WsUtil.exe eine WSDL-Datei in einen C-Header und Quelldateien konvertiert.](images/doctotool.png)

Der [WsUtil.exe](web-service-compiler-tool.md) generiert Header und Quellen für die Dienst Implementierung sowie Client seitige Dienst Vorgänge für den Client.

## <a name="calling-the-calculator-service-from-a-client&quot;></a>Aufrufen des Rechner Dienstanbieter von einem Client

Wie bei der Dienst Implementierung muss der Client die generierten Header oder Header einschließen.

``` syntax
#include &quot;CalculatorProxyStub.h&quot;
```

Die Client Anwendung kann nun einen Dienst Proxy erstellen und öffnen, um mit der Kommunikation mit dem Rechner Dienst zu beginnen.

``` syntax
WS_ENDPOINT_ADDRESS address = {0};
WS_STRING uri= WS_STRING_VALUE(L&quot;http://localhost/example");
address.uri = uri;

if (FAILED (hr = WsCreateServiceProxy(WS_CHANNEL_TYPE_REQUEST, WS_HTTP_CHANNEL_BINDING, NULL, NULL, 0, &serviceProxy, error)))
    goto Error;

if (FAILED (hr = WsOpenServiceProxy(serviceProxy, &address, NULL, error)))
    goto Error;
```

Die Anwendung kann den Add-Vorgang für den Rechner Dienst mit folgendem Code aufzurufen:

``` syntax
if (FAILED (hr = DefaultBinding_ICalculator_Add(serviceProxy, heap, 1, 2, &result, NULL, 0, NULL, error)))
    goto Error;
```

Die vollständige Implementierung des Rechner Dienstanbieter finden Sie im Codebeispiel unter [httpcalculatorclientexample](httpcalculatorclientexample.md) .

## <a name="service-model-components"></a>Dienstmodell Komponenten

Die Interaktion der einzelnen wwsapi-Dienstmodell Komponenten innerhalb des Rechner Beispiels sieht wie folgt aus:

-   Vom Client wird ein [Dienst Proxy](service-proxy.md) erstellt und geöffnet.
-   Der Client ruft die Add-Funktion des Dienstanbieter auf und übergibt den Dienst Proxy.
-   Die Nachricht wird gemäß der Serialisierungsmetadaten in den Header-und Quelldateien serialisiert, die vom metadatentool ([WsUtil.exe](web-service-compiler-tool.md)) generiert werden.
-   Die Nachricht wird in den Channel geschrieben und über das Netzwerk an den Dienst übertragen.
-   Auf der Serverseite wird der Dienst innerhalb eines Dienst Hosts gehostet und verfügt über einen Endpunkt, der den ICalculator-Vertrag überwacht.
-   Mithilfe der Dienstmodell Metadaten im Stub deserialisiert der Dienst die Nachricht vom Client und sendet Sie an den Stub.
-   Der serverseitige Dienst ruft die Add-Methode auf und übergibt dabei den Vorgangs Kontext. Dieser Vorgangs Kontext enthält den Verweis auf die eingehende Nachricht.

![Das Diagramm zeigt die Interaktion der einzelnen wwsapi-Dienstmodell Komponenten.](images/servicemodellayout.png)

Komponenten

-   [Dienst Host](service-host.md): hostet einen Dienst.
-   [Dienst Proxy](service-proxy.md): definiert, wie ein Client mit einem Dienst kommuniziert.
-   [Kontext](context.md): Eigenschaften Behälter zum Bereitstellen Zustands spezifischer Informationen für einen Dienst Vorgang.
-   [Vertrag](contract.md): die Schnittstellen Definition eines Dienstanbieter. ICalculator stellt z. b. einen Vertrag für den Rechner Dienst in unserem Beispielcode dar.
-   [WsUtil.exe](web-service-compiler-tool.md): das Dienstmodell-metadatentool zum Erstellen von Proxys und Stubdateien.

 

 




