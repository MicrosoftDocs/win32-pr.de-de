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
# <a name="manually-creating-a-service-proxy-for-a-wcf-service"></a><span data-ttu-id="61f4f-103">Manuelles Erstellen eines Dienst Proxys für einen WCF-Dienst</span><span class="sxs-lookup"><span data-stu-id="61f4f-103">Manually Creating a Service Proxy for a WCF Service</span></span>

<span data-ttu-id="61f4f-104">Die einfachste Möglichkeit zum Erstellen eines Client Dienst Proxys für einen Windows Communication Foundation (WCF)-Dienst befindet sich auf der [Dienstmodell](service-model-layer-overview.md) Ebene mit dem wsutil-Tool, wie im Thema [Erstellen eines Clients](creating-a-client.md) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="61f4f-104">The easiest way to create a client service proxy for a Windows Communication Foundation (WCF) service is at the [Service Model](service-model-layer-overview.md) layer with the WsUtil tool, as described in the [Creating a Client](creating-a-client.md) topic.</span></span> <span data-ttu-id="61f4f-105">Falls erforderlich, können Sie einen Dienst Proxy jedoch auch manuell erstellen.</span><span class="sxs-lookup"><span data-stu-id="61f4f-105">However, if necessary, you can also create a service proxy manually.</span></span> <span data-ttu-id="61f4f-106">Diese API enthält eine [**wscreateserviceproxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) -Funktion zum Erstellen des Dienst Proxys sowie Strukturen, Enumerationen usw., um die Eigenschaften festzulegen, die für die Zusammenarbeit mit WCF erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="61f4f-106">This API includes a [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) function for creating the service proxy as well as structures, enumerations, and so on for setting the properties necessary to interoperate with WCF.</span></span>

<span data-ttu-id="61f4f-107">WCF bietet eine Reihe von Standard Bindungen, die jeweils auf ein bestimmtes Verwendungs Szenario abzielen.</span><span class="sxs-lookup"><span data-stu-id="61f4f-107">WCF provides a number of standard bindings, each targeting a specific usage scenario.</span></span> <span data-ttu-id="61f4f-108">Die Bindung des Dienstanbieter, mit dem Sie eine Verbindung herstellen möchten, bestimmt wiederum, welche Channeleigenschaften Sie für Ihren Dienst Proxy für die Kommunikation mit dem Dienst anpassen müssen.</span><span class="sxs-lookup"><span data-stu-id="61f4f-108">Which binding the service you are trying to connect to uses, in turn, determines which channel properties you need to customize for your service proxy to communicate with the service.</span></span>

## <a name="creating-a-service-proxy-for-wcfs-wshttpbinding"></a><span data-ttu-id="61f4f-109">Erstellen eines Dienst Proxys für die WSHttpBinding von WCF</span><span class="sxs-lookup"><span data-stu-id="61f4f-109">Creating a Service Proxy for WCF's WSHttpBinding</span></span>

<span data-ttu-id="61f4f-110">WSHttpBinding ist für das Hauptszenario der Internet-Webdienste.</span><span class="sxs-lookup"><span data-stu-id="61f4f-110">WSHttpBinding is for the mainline Internet web services scenario.</span></span> <span data-ttu-id="61f4f-111">Es verwendet die neuere SOAP-Version 1,2 und WS-Addressing Version 1,0 und ermöglicht eine Vielzahl von Sicherheitseinstellungen über die öffentlichen http-und HTTPS-Transporte.</span><span class="sxs-lookup"><span data-stu-id="61f4f-111">It uses the newer SOAP version 1.2 and WS-Addressing version 1.0 and enables a wide range of security settings over the public HTTP and HTTPS transports.</span></span> <span data-ttu-id="61f4f-112">Wwsapi verfügt nicht über eine Entsprechung von "WSHttpBinding" (oder eine der WCF-Standard Bindungen), aber da die standardmäßige SOAP-Version, WS-Addressing Version und das Codierungsformat mit denen in wsHttpBinding übereinstimmen, ist das Erstellen eines Dienst Proxys für einen Dienst, der die WSHttpBinding verwendet, unkompliziert.</span><span class="sxs-lookup"><span data-stu-id="61f4f-112">WWSAPI does not have an equivalent of the WSHttpBinding (or any of the WCF standard bindings, for that matter), but since its default SOAP version, WS-Addressing version, and encoding format match those in WSHttpBinding, creating a service proxy for a service that uses the WSHttpBinding is straightforward.</span></span> <span data-ttu-id="61f4f-113">Wenn Sie z. b. einen Dienst Proxy für die Kommunikation mit einem WSHttpBinding-Endpunkt ohne Sicherheit erstellen möchten, können Sie einfach Code wie den folgenden Code Ausschnitt verwenden (Variablen Deklaration und Heap-und Fehler Erstellung werden weggelassen).</span><span class="sxs-lookup"><span data-stu-id="61f4f-113">For example, to create a service proxy to talk to a WSHttpBinding endpoint without security, you can simply use code like following snippet (variable declaration, and heap and error creation are omitted).</span></span> <span data-ttu-id="61f4f-114">Beachten Sie, dass im Aufrufen der [**wscreateserviceproxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) -Funktion keine Kanaleigenschaften oder Sicherheits Beschreibung angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="61f4f-114">Notice that no channel properties or security description is specified in the call to the [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) function.</span></span>


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



<span data-ttu-id="61f4f-115">Die-Funktion erstellt den Dienst Proxy und gibt einen Zeiger darauf im *Service Proxy* -Parameter (&Proxy im obigen Funktionsaufrufen) zurück.</span><span class="sxs-lookup"><span data-stu-id="61f4f-115">The function creates the service proxy and returns a pointer to it in the *serviceProxy* parameter (&proxy in the function call above).</span></span>

## <a name="creating-a-service-proxy-for-wcfs-basichttpbinding"></a><span data-ttu-id="61f4f-116">Erstellen eines Dienst Proxys für die BasicHttpBinding von WCF</span><span class="sxs-lookup"><span data-stu-id="61f4f-116">Creating a Service Proxy for WCF's BasicHttpBinding</span></span>

<span data-ttu-id="61f4f-117">Wenn Sie einen Dienst Proxy für einen WCF-Dienst, der eine basicHttpBinding-Bindung verwendet, manuell erstellen, müssen Sie jedoch die SOAP-Version und WS-Addressing Eigenschaften des Kanals festlegen.</span><span class="sxs-lookup"><span data-stu-id="61f4f-117">When you manually create a service proxy for a WCF service that uses a BasicHttpBinding binding, however, it is necessary to set the SOAP version and WS-Addressing properties of the channel.</span></span> <span data-ttu-id="61f4f-118">Der Grund hierfür ist, dass wwsapi standardmäßig SOAP-Version 1,2 und WS-Addressing 1,0 verwendet.</span><span class="sxs-lookup"><span data-stu-id="61f4f-118">This is because WWSAPI defaults to SOAP version 1.2 and WS-Addressing 1.0.</span></span> <span data-ttu-id="61f4f-119">Die BasicHttpBinding von WCF hingegen verwendet SOAP-Version 1,1 und keine WS-Adressierung.</span><span class="sxs-lookup"><span data-stu-id="61f4f-119">WCF's BasicHttpBinding, on the other hand, uses SOAP version 1.1 and no WS-Addressing.</span></span>

<span data-ttu-id="61f4f-120">Zum Festlegen der SOAP-Version und der WS-Addrssing Eigenschaften des Kanals deklarieren Sie ein Array von [**WS- \_ \_ channeleigenschaftenstrukturen**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property) , die die Channeleigenschaften und die zugehörigen Informationen enthalten sollen.</span><span class="sxs-lookup"><span data-stu-id="61f4f-120">To set the SOAP version and WS-Addrssing properties of the channel, declare an array of [**WS\_CHANNEL\_PROPERTY**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property) structures to hold the channel properties and related information.</span></span>


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



<span data-ttu-id="61f4f-121">Übergeben Sie dann das Array der Channeleigenschaften (channelproperties) und die Anzahl der Eigenschaften (channelpropertycount) an den [**wscreateserviceproxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) (oder an [**wscreatechannel**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannel) , wenn Sie auf der Kanal Ebene arbeiten).</span><span class="sxs-lookup"><span data-stu-id="61f4f-121">Then pass the array of channel properties (channelProperties) and the count of properties (channelPropertyCount) to the [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) (or [**WsCreateChannel**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannel) if you are working at channel layer).</span></span>


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



<span data-ttu-id="61f4f-122">Das Array, das Sie zum Speichern der Eigenschaften deklariert haben, wird in **wscreateserviceproxy** kopiert. Daher können Sie den Speicher für das Eigenschafts Array sofort nach dem Aufrufen der Funktion freigeben.</span><span class="sxs-lookup"><span data-stu-id="61f4f-122">The array you declared to hold the properties is copied in **WsCreateServiceProxy**, and as a result, you can free the memory for the property array immediately after calling the function.</span></span> <span data-ttu-id="61f4f-123">Wenn Sie den Arbeitsspeicher aus dem Stapel zuordnen (wie z. b. den obigen Code Ausschnitt), können Sie auch direkt nach dem-Befehl von der-Funktion zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="61f4f-123">Also, if you allocate the memory from the stack (like the code snippet above), you can also return from the function immediately after the call.</span></span>

## <a name="other-bindings"></a><span data-ttu-id="61f4f-124">Andere Bindungen</span><span class="sxs-lookup"><span data-stu-id="61f4f-124">Other Bindings</span></span>

<span data-ttu-id="61f4f-125">Außerdem bietet wwsapi Mechanismen zum Erstellen von Dienst Proxys für die Kommunikation mit WCF-Diensten mit anderen Bindungen, wie z. b. NetTcpBinding und WSFederationHttpBinding.</span><span class="sxs-lookup"><span data-stu-id="61f4f-125">In addition, WWSAPI provides mechanisms for creating service proxies to communicate with WCF services using other bindings, such as NetTcpBinding and WSFederationHttpBinding.</span></span> <span data-ttu-id="61f4f-126">Viele dieser Bindungen erfordern das Festlegen zusätzlicher Channeleigenschaften, z. b. Sicherheits Deskriptoren.</span><span class="sxs-lookup"><span data-stu-id="61f4f-126">Many of these binding require setting additional channel properties, such as security descriptors.</span></span> <span data-ttu-id="61f4f-127">Beispiele, die die Verwendung anderer Bindungen veranschaulichen, finden Sie im Abschnitt [Beispiele für Windows-Webdienste](windows-web-services-examples.md), insbesondere in den Beispielen für die [TCP-channelschicht](tcp-channel-layer-examples.md), Beispiele für die [http-Kanal Schicht](http-channel-layer-examples.md)und [Beispiele für Sicherheits Kanal Ebenen](security-channel-layer-examples.md) .</span><span class="sxs-lookup"><span data-stu-id="61f4f-127">For examples that illustrate using other bindings, see the [Windows Web Services Examples](windows-web-services-examples.md), section, in particular the [TCP Channel Layer Examples](tcp-channel-layer-examples.md), [HTTP Channel Layer Examples](http-channel-layer-examples.md), and [Security Channel Layer Examples](security-channel-layer-examples.md) subsections.</span></span>

 

 




