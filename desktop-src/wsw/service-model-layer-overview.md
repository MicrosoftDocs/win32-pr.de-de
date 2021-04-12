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
# <a name="service-model-layer-overview"></a><span data-ttu-id="78132-106">Übersicht über die Dienstmodell Ebene</span><span class="sxs-lookup"><span data-stu-id="78132-106">Service Model Layer Overview</span></span>

<span data-ttu-id="78132-107">Die wwsapi-Dienstmodell-API modelliert die Kommunikation zwischen einem Client und einem Dienst als Methodenaufrufe und nicht als Daten Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="78132-107">The WWSAPI Service Model API models the communication between a client and a service as method calls, rather than as data messages.</span></span> <span data-ttu-id="78132-108">Im Gegensatz zur [Kanal Ebene](channel-layer-overview.md), die den herkömmlichen [Nachrichten](message.md) Austausch zwischen Client und Dienst unterstützt, verwaltet das Dienstmodell die Kommunikation automatisch mithilfe eines Dienst Proxys auf dem Client und einem Dienst Host auf dem Dienst.</span><span class="sxs-lookup"><span data-stu-id="78132-108">In contrast to the [channel layer](channel-layer-overview.md), which supports more traditional [message](message.md) exchanges between client and service, the Service Model automatically manages communication by means of a service proxy on the client and a service host on the service.</span></span> <span data-ttu-id="78132-109">Dies bedeutet, dass der Client generierte Funktionen aufruft und der Server Rückrufe implementiert.</span><span class="sxs-lookup"><span data-stu-id="78132-109">This means that the client calls generated functions and the server implements callbacks.</span></span>


<span data-ttu-id="78132-110">Nehmen Sie beispielsweise einen Rechner Dienst an, der eine Addition und Subtraktion zweier Zahlen ausführt.</span><span class="sxs-lookup"><span data-stu-id="78132-110">For example, consider a calculator service which performs addition and subtraction on two numbers.</span></span> <span data-ttu-id="78132-111">Addition und Subtraktion sind Vorgänge, die auf natürliche Weise als Methodenaufrufe dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="78132-111">Addition and subtraction are operations naturally represented as method calls.</span></span>

![Diagramm, das zeigt, wie ein Rechner Dienst mithilfe von Methoden aufrufen für Addition und Subtraktion mit einem Client kommuniziert.](images/servicemodelintro.png)

<span data-ttu-id="78132-113">Das Dienstmodell stellt die Kommunikation zwischen dem Client und dem Dienst als deklarierte Methodenaufrufe dar und verbirgt somit die Kommunikations Details der zugrunde liegenden Kanal Ebene von der Anwendung, sodass der Dienst leichter implementiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="78132-113">The service model represents the communication between client and the service as declared method calls, and so conceals the communication details of the underlying channel layer from the application, making the service easier to implement.</span></span>

## <a name="specifying-a-service"></a><span data-ttu-id="78132-114">Angeben eines Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="78132-114">Specifying a Service</span></span>

<span data-ttu-id="78132-115">Ein Dienst muss in Bezug auf die Nachrichtenaustausch Muster und seine Netzwerkdaten Darstellung angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="78132-115">A service must be specified in terms of its message exchange patterns as well as its network data representation.</span></span> <span data-ttu-id="78132-116">Für-Dienste wird diese Spezifikation normalerweise als WSDL-und XML-Schema Dokumente bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="78132-116">For services, this specification is usually provided as WSDL and XML schema documents.</span></span>

<span data-ttu-id="78132-117">Beim WSDL-Dokument handelt es sich um ein XML-Dokument, das die kanalbindung und die Nachrichtenaustausch Muster des Dienstanbieter enthält, während das XML-Schema Dokument ein XML-Dokument ist, das die Datendarstellung der einzelnen Nachrichten definiert.</span><span class="sxs-lookup"><span data-stu-id="78132-117">The WSDL document is an XML document which contains the channel binding and the message exchange patterns of the service, whereas the XML schema document is an XML document that defines the data representation of the individual messages.</span></span>

<span data-ttu-id="78132-118">Für den Rechner Dienst und seine Additions-und Subtraktions Vorgänge könnte das WSDL-Dokument wie im folgenden Beispiel aussehen:</span><span class="sxs-lookup"><span data-stu-id="78132-118">For the calculator service and its addition and subtraction operations, the WSDL document might look like the following example:</span></span>

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

<span data-ttu-id="78132-119">Ebenso kann das zugehörige XML-Schema wie folgt definiert werden:</span><span class="sxs-lookup"><span data-stu-id="78132-119">Likewise, its XML schema can be defined as follows:</span></span>

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

## <a name="converting-metadata-to-code"></a><span data-ttu-id="78132-120">Metadaten werden in Code umgerechnet</span><span class="sxs-lookup"><span data-stu-id="78132-120">Converting Metadata to Code</span></span>

<span data-ttu-id="78132-121">Das Dienstmodell stellt den [WsUtil.exe](web-service-compiler-tool.md) als Tool zum Verarbeiten dieser Metadatendokumente bereit und umwandelt eine WSDL-Datei in einen C-Header und Quelldateien.</span><span class="sxs-lookup"><span data-stu-id="78132-121">The service model provides the [WsUtil.exe](web-service-compiler-tool.md) as a tool to process these metadata documents, converting a WSDL file into a C header and source files.</span></span>

![Diagramm, das zeigt, wie WsUtil.exe eine WSDL-Datei in einen C-Header und Quelldateien konvertiert.](images/doctotool.png)

<span data-ttu-id="78132-123">Der [WsUtil.exe](web-service-compiler-tool.md) generiert Header und Quellen für die Dienst Implementierung sowie Client seitige Dienst Vorgänge für den Client.</span><span class="sxs-lookup"><span data-stu-id="78132-123">The [WsUtil.exe](web-service-compiler-tool.md) generates header and sources for service implementation as well as client-side service operations for the client .</span></span>

## <a name="calling-the-calculator-service-from-a-client"></a><span data-ttu-id="78132-124">Aufrufen des Rechner Dienstanbieter von einem Client</span><span class="sxs-lookup"><span data-stu-id="78132-124">Calling the Calculator Service From a Client</span></span>

<span data-ttu-id="78132-125">Wie bei der Dienst Implementierung muss der Client die generierten Header oder Header einschließen.</span><span class="sxs-lookup"><span data-stu-id="78132-125">As with the service implementation, the client must include the generated header or headers.</span></span>

``` syntax
#include "CalculatorProxyStub.h"
```

<span data-ttu-id="78132-126">Die Client Anwendung kann nun einen Dienst Proxy erstellen und öffnen, um mit der Kommunikation mit dem Rechner Dienst zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="78132-126">Now, The client application can create and open a service proxy to begin communication with the calculator service.</span></span>

``` syntax
WS_ENDPOINT_ADDRESS address = {0};
WS_STRING uri= WS_STRING_VALUE(L"http://localhost/example");
address.uri = uri;

if (FAILED (hr = WsCreateServiceProxy(WS_CHANNEL_TYPE_REQUEST, WS_HTTP_CHANNEL_BINDING, NULL, NULL, 0, &serviceProxy, error)))
    goto Error;

if (FAILED (hr = WsOpenServiceProxy(serviceProxy, &address, NULL, error)))
    goto Error;
```

<span data-ttu-id="78132-127">Die Anwendung kann den Add-Vorgang für den Rechner Dienst mit folgendem Code aufzurufen:</span><span class="sxs-lookup"><span data-stu-id="78132-127">The application can call the Add operation on the calculator service with the following code:</span></span>

``` syntax
if (FAILED (hr = DefaultBinding_ICalculator_Add(serviceProxy, heap, 1, 2, &result, NULL, 0, NULL, error)))
    goto Error;
```

<span data-ttu-id="78132-128">Die vollständige Implementierung des Rechner Dienstanbieter finden Sie im Codebeispiel unter [httpcalculatorclientexample](httpcalculatorclientexample.md) .</span><span class="sxs-lookup"><span data-stu-id="78132-128">Please refer to the code example at [HttpCalculatorClientExample](httpcalculatorclientexample.md) for full implementation of the calculator service.</span></span>

## <a name="service-model-components"></a><span data-ttu-id="78132-129">Dienstmodell Komponenten</span><span class="sxs-lookup"><span data-stu-id="78132-129">Service Model Components</span></span>

<span data-ttu-id="78132-130">Die Interaktion der einzelnen wwsapi-Dienstmodell Komponenten innerhalb des Rechner Beispiels sieht wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="78132-130">The interaction of the individual WWSAPI Service Model components within the Calculator example is as follows:</span></span>

-   <span data-ttu-id="78132-131">Vom Client wird ein [Dienst Proxy](service-proxy.md) erstellt und geöffnet.</span><span class="sxs-lookup"><span data-stu-id="78132-131">The client creates a [service proxy](service-proxy.md) and opens it.</span></span>
-   <span data-ttu-id="78132-132">Der Client ruft die Add-Funktion des Dienstanbieter auf und übergibt den Dienst Proxy.</span><span class="sxs-lookup"><span data-stu-id="78132-132">The client calls the Add function of the service, and passes in the service proxy.</span></span>
-   <span data-ttu-id="78132-133">Die Nachricht wird gemäß der Serialisierungsmetadaten in den Header-und Quelldateien serialisiert, die vom metadatentool ([WsUtil.exe](web-service-compiler-tool.md)) generiert werden.</span><span class="sxs-lookup"><span data-stu-id="78132-133">The message is serialized according to the serialization metadata in the header and source files generated by the metadata tool ([WsUtil.exe](web-service-compiler-tool.md)).</span></span>
-   <span data-ttu-id="78132-134">Die Nachricht wird in den Channel geschrieben und über das Netzwerk an den Dienst übertragen.</span><span class="sxs-lookup"><span data-stu-id="78132-134">The message is written to the channel and is transmitted over the network to the service.</span></span>
-   <span data-ttu-id="78132-135">Auf der Serverseite wird der Dienst innerhalb eines Dienst Hosts gehostet und verfügt über einen Endpunkt, der den ICalculator-Vertrag überwacht.</span><span class="sxs-lookup"><span data-stu-id="78132-135">On the server side, the service is hosted inside a service host, and has an endpoint listening for the ICalculator contract.</span></span>
-   <span data-ttu-id="78132-136">Mithilfe der Dienstmodell Metadaten im Stub deserialisiert der Dienst die Nachricht vom Client und sendet Sie an den Stub.</span><span class="sxs-lookup"><span data-stu-id="78132-136">Using the Service Model metadata in the stub, the service deserializes the message from the client and dispatches it to the stub.</span></span>
-   <span data-ttu-id="78132-137">Der serverseitige Dienst ruft die Add-Methode auf und übergibt dabei den Vorgangs Kontext.</span><span class="sxs-lookup"><span data-stu-id="78132-137">The server-side service calls the Add method, passing it the operation context.</span></span> <span data-ttu-id="78132-138">Dieser Vorgangs Kontext enthält den Verweis auf die eingehende Nachricht.</span><span class="sxs-lookup"><span data-stu-id="78132-138">This operation context contains the reference to the incoming message.</span></span>

![Das Diagramm zeigt die Interaktion der einzelnen wwsapi-Dienstmodell Komponenten.](images/servicemodellayout.png)

<span data-ttu-id="78132-140">Komponenten</span><span class="sxs-lookup"><span data-stu-id="78132-140">Components</span></span>

-   <span data-ttu-id="78132-141">[Dienst Host](service-host.md): hostet einen Dienst.</span><span class="sxs-lookup"><span data-stu-id="78132-141">[Service host](service-host.md): Hosts a service.</span></span>
-   <span data-ttu-id="78132-142">[Dienst Proxy](service-proxy.md): definiert, wie ein Client mit einem Dienst kommuniziert.</span><span class="sxs-lookup"><span data-stu-id="78132-142">[Service proxy](service-proxy.md): Defines how a client communicates with a service.</span></span>
-   <span data-ttu-id="78132-143">[Kontext](context.md): Eigenschaften Behälter zum Bereitstellen Zustands spezifischer Informationen für einen Dienst Vorgang.</span><span class="sxs-lookup"><span data-stu-id="78132-143">[Context](context.md): Property bag for making state-specific information available to a service operation.</span></span>
-   <span data-ttu-id="78132-144">[Vertrag](contract.md): die Schnittstellen Definition eines Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="78132-144">[Contract](contract.md): The interface definition of a service.</span></span> <span data-ttu-id="78132-145">ICalculator stellt z. b. einen Vertrag für den Rechner Dienst in unserem Beispielcode dar.</span><span class="sxs-lookup"><span data-stu-id="78132-145">For example, ICalculator represents a contract for the calculator service in our example code.</span></span>
-   <span data-ttu-id="78132-146">[WsUtil.exe](web-service-compiler-tool.md): das Dienstmodell-metadatentool zum Erstellen von Proxys und Stubdateien.</span><span class="sxs-lookup"><span data-stu-id="78132-146">[WsUtil.exe](web-service-compiler-tool.md): The Service Model metadata tool for generating proxies and stubs.</span></span>

 

 




