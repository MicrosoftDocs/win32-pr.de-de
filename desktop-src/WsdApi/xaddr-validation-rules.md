---
description: Transport Adressen (xaddrs), die in Probe Matches-und resolvematches-Meldungen enthalten sind, unterliegen der grundlegenden Validierung, bevor WSDAPI eine HTTP-Nachricht sendet, z. b. eine metadatenanforderung.
ms.assetid: 6b5139b5-aa31-42bc-a281-8784006edfbe
title: Xaddr-Validierungsregeln
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc91ce8a0e1bba267ea92fa79a6680b481297f24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215303"
---
# <a name="xaddr-validation-rules"></a><span data-ttu-id="fe5f9-103">Xaddr-Validierungsregeln</span><span class="sxs-lookup"><span data-stu-id="fe5f9-103">XAddr Validation Rules</span></span>

<span data-ttu-id="fe5f9-104">Transport Adressen (xaddrs), die in [Probe Matches](probematches-message.md) -und [resolvematches](resolvematches-message.md) -Meldungen enthalten sind, unterliegen der grundlegenden Validierung, bevor WSDAPI eine HTTP-Nachricht sendet, z. b. eine metadatenanforderung.</span><span class="sxs-lookup"><span data-stu-id="fe5f9-104">Transport addresses (XAddrs) included in [ProbeMatches](probematches-message.md) and [ResolveMatches](resolvematches-message.md) messages are subject to basic validation before WSDAPI sends an HTTP message, such as a metadata request.</span></span>

<span data-ttu-id="fe5f9-105">Dadurch wird sichergestellt, dass sich die xaddrs im gleichen Subnetz wie der Client befinden.</span><span class="sxs-lookup"><span data-stu-id="fe5f9-105">This is in order to ensure that the XAddrs are on the same subnet as the client.</span></span>

<span data-ttu-id="fe5f9-106">Der folgende XML-Code zeigt ein xaddrs-Beispiel Element.</span><span class="sxs-lookup"><span data-stu-id="fe5f9-106">The following XML shows a sample XAddrs element.</span></span> <span data-ttu-id="fe5f9-107">Das WSD-Präfix verweist auf den-Namespace `https://schemas.xmlsoap.org/ws/2005/04/discovery` .</span><span class="sxs-lookup"><span data-stu-id="fe5f9-107">The wsd prefix refers to the namespace `https://schemas.xmlsoap.org/ws/2005/04/discovery`.</span></span>

``` syntax
<wsd:XAddrs>
    https://192.168.0.2:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
</wsd:XAddrs>
```

<span data-ttu-id="fe5f9-108">Alle folgenden Bedingungen müssen erfüllt sein, damit die HTTP-Nachricht über das Netzwerk gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="fe5f9-108">All of the following conditions must be met before the HTTP message will go out over the wire.</span></span>

-   <span data-ttu-id="fe5f9-109">Xaddrs muss eine HTTP-oder HTTPS-Adresse sein.</span><span class="sxs-lookup"><span data-stu-id="fe5f9-109">XAddrs must be HTTP or HTTPS addresses.</span></span> <span data-ttu-id="fe5f9-110">Xaddrs anderer Schemas werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="fe5f9-110">XAddrs of other schemes are ignored.</span></span>
-   <span data-ttu-id="fe5f9-111">Wenn HTTPS-xaddrs vorhanden sind, müssen alle xaddrs HTTPS lauten.</span><span class="sxs-lookup"><span data-stu-id="fe5f9-111">If any HTTPS XAddrs are present, all XAddrs must be HTTPS.</span></span> <span data-ttu-id="fe5f9-112">Xaddr-Abschnitte, die sowohl HTTP-als auch HTTPS-Adressen enthalten, werden vollständig ignoriert.</span><span class="sxs-lookup"><span data-stu-id="fe5f9-112">XAddr sections which include both HTTP and HTTPS addresses are completely ignored.</span></span> <span data-ttu-id="fe5f9-113">Außerdem muss die Endpunkt Adresse des Geräts exakt mit den HTTPS-xaddrs übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="fe5f9-113">Additionally, the device's endpoint address must match the HTTPS XAddrs exactly.</span></span>
-   <span data-ttu-id="fe5f9-114">Xaddrs müssen IP-Adressen oder Hostnamen sein, die über DNS aufgelöst werden können.</span><span class="sxs-lookup"><span data-stu-id="fe5f9-114">XAddrs must be IP addresses or hostnames resolvable through DNS.</span></span> <span data-ttu-id="fe5f9-115">Normalerweise werden IP-Adressen verwendet.</span><span class="sxs-lookup"><span data-stu-id="fe5f9-115">Usually, IP addresses are used.</span></span>
-   <span data-ttu-id="fe5f9-116">Mindestens eine IP-Adresse, die in den xaddrs enthalten ist (oder die IP-Adresse, die von einem in den xaddrs enthaltenen Hostnamen aufgelöst wurde), muss sich im gleichen Subnetz befinden wie der Adapter, über den die [Probe Matches](probematches-message.md) -oder [resolvematches](resolvematches-message.md) -Nachricht empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="fe5f9-116">At least one IP address included in the XAddrs (or IP address resolved from a hostname included in the XAddrs) must be on the same subnet as the adapter over which the [ProbeMatches](probematches-message.md) or [ResolveMatches](resolvematches-message.md) message was received.</span></span>
-   <span data-ttu-id="fe5f9-117">Auf die Adresse und den Port, die in der ersten xaddr angegeben sind, muss zugegriffen werden können.</span><span class="sxs-lookup"><span data-stu-id="fe5f9-117">The address and port specified in the first XAddr must be accessible.</span></span> <span data-ttu-id="fe5f9-118">WSDAPI versucht, eine Verbindung mit dieser Adresse herzustellen, wenn eine HTTP-Verbindung hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="fe5f9-118">WSDAPI attempts to connect to this address when establishing an HTTP connection.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fe5f9-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fe5f9-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe5f9-120">Probe Matches</span><span class="sxs-lookup"><span data-stu-id="fe5f9-120">ProbeMatches</span></span>](probematches-message.md)
</dt> <dt>

[<span data-ttu-id="fe5f9-121">Resolvematches</span><span class="sxs-lookup"><span data-stu-id="fe5f9-121">ResolveMatches</span></span>](resolvematches-message.md)
</dt> <dt>

[<span data-ttu-id="fe5f9-122">Ermittlungs-und Metadatenaustausch-Nachrichten Muster</span><span class="sxs-lookup"><span data-stu-id="fe5f9-122">Discovery and Metadata Exchange Message Patterns</span></span>](discovery-and-metadata-exchange-message-patterns.md)
</dt> </dl>

 

 



