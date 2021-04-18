---
description: Microsoft-Netzwerkmonitor 3 (NetMon) ist ein Paket Analysetool, das zum Überprüfen des Netzwerkverkehrs verwendet wird.
ms.assetid: 015a6a6d-9e07-4f22-b931-dcce77051bef
title: Herunterladen von Netmon und Beispiel-DPWS-Filtern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47790b26164ec0ed2792d1d1e1f2ad4ba5d77d38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343817"
---
# <a name="downloading-netmon-and-sample-dpws-filters"></a><span data-ttu-id="984ee-103">Herunterladen von Netmon und Beispiel-DPWS-Filtern</span><span class="sxs-lookup"><span data-stu-id="984ee-103">Downloading Netmon and Sample DPWS Filters</span></span>

<span data-ttu-id="984ee-104">Microsoft-Netzwerkmonitor 3 (NetMon) ist ein Paket Analysetool, das zum Überprüfen des Netzwerkverkehrs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="984ee-104">Microsoft Network Monitor 3 (Netmon) is a packet analyzer used to inspect network traffic.</span></span> <span data-ttu-id="984ee-105">NetMon muss heruntergeladen werden, bevor die Schritte zur Problembehandlung bei der [Überprüfung von Netzwerk Ablauf Verfolgungen für UDP-WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md) und untersuchen [von Netzwerk Ablauf Verfolgungen für den HTTP-Metadatenaustausch](inspecting-network-traces-for-http-metadata-exchange.md) befolgt werden können</span><span class="sxs-lookup"><span data-stu-id="984ee-105">Netmon must be downloaded before the troubleshooting steps given in [Inspecting Network Traces for UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md) and [Inspecting Network Traces for HTTP Metadata Exchange](inspecting-network-traces-for-http-metadata-exchange.md) can be followed.</span></span> <span data-ttu-id="984ee-106">Nachdem Netmon heruntergeladen wurde, können DPWS-Filter verwendet werden, um den relevanten Datenverkehr zu isolieren.</span><span class="sxs-lookup"><span data-stu-id="984ee-106">After Netmon has been downloaded, DPWS filters can be used to help isolate traffic of interest.</span></span>

## <a name="downloading-netmon"></a><span data-ttu-id="984ee-107">NetMon wird heruntergeladen</span><span class="sxs-lookup"><span data-stu-id="984ee-107">Downloading Netmon</span></span>

<span data-ttu-id="984ee-108">Um Netmon herunterzuladen, navigieren Sie zu [Microsoft-Netzwerkmonitor](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=983b941d-06cb-4658-b7f6-3088333d062f) , und befolgen Sie die Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="984ee-108">To download Netmon, go to [Microsoft Network Monitor](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=983b941d-06cb-4658-b7f6-3088333d062f) and follow the instructions.</span></span> <span data-ttu-id="984ee-109">Weitere Informationen zu Netmon finden Sie unter "Informationen zu Netzwerkmonitor 3,0" in der Hilfe-und Support Knowledge Base unter [https://support.microsoft.com/kb/933741](https://support.microsoft.com/kb/933741) .</span><span class="sxs-lookup"><span data-stu-id="984ee-109">For more information about Netmon, see "Information about Network Monitor 3.0" in the Help and Support Knowledge Base at [https://support.microsoft.com/kb/933741](https://support.microsoft.com/kb/933741).</span></span>

## <a name="sample-dpws-filters"></a><span data-ttu-id="984ee-110">Beispiel-DPWS-Filter</span><span class="sxs-lookup"><span data-stu-id="984ee-110">Sample DPWS Filters</span></span>

<span data-ttu-id="984ee-111">Manchmal müssen WS-Discovery-und Metadatenaustausch-Problembehandlung in einem ausgelasteten Netzwerk stattfinden.</span><span class="sxs-lookup"><span data-stu-id="984ee-111">Sometimes, WS-Discovery and metadata exchange troubleshooting must take place on a busy network.</span></span> <span data-ttu-id="984ee-112">Die Beispiel Filter können verwendet werden, um die NetMon-Ausgabe auf den gewünschten Datenverkehr zu beschränken.</span><span class="sxs-lookup"><span data-stu-id="984ee-112">The sample filters can be used to help limit the Netmon output to traffic of interest.</span></span> <span data-ttu-id="984ee-113">Weitere Informationen zur Verwendung von Netmon-Filtern finden Sie unter [https://support.microsoft.com/kb/933741](https://support.microsoft.com/kb/933741) .</span><span class="sxs-lookup"><span data-stu-id="984ee-113">For more information about using Netmon filters, see [https://support.microsoft.com/kb/933741](https://support.microsoft.com/kb/933741).</span></span>

<span data-ttu-id="984ee-114">Das folgende Beispiel zeigt einen Filter, der die Ausgabe auf den gesamten Broadcast WS-Discovery-Datenverkehr beschränkt.</span><span class="sxs-lookup"><span data-stu-id="984ee-114">The following example shows a filter that limits output to all broadcast WS-Discovery traffic.</span></span>

> [!Note]  
> <span data-ttu-id="984ee-115">Dieser Filter erfasst keinen Datenverkehr von Stapeln, die nicht auf Multicast-WS-Discovery Meldungen reagieren, die von Port 3702 stammen.</span><span class="sxs-lookup"><span data-stu-id="984ee-115">This filter does not capture traffic from stacks that do not respond to multicast WS-Discovery messages that originate at port 3702.</span></span> <span data-ttu-id="984ee-116">Wenn ein solcher Stapel verwendet wird, muss dieser Beispiel Filter vor der Verwendung geändert werden.</span><span class="sxs-lookup"><span data-stu-id="984ee-116">If such a stack is being used, then this sample filter must be modified before use.</span></span>

 

``` syntax
// All broadcast WS-Discovery traffic
UDP.Port == 3702
```

<span data-ttu-id="984ee-117">Das folgende Beispiel zeigt einen Filter, der die Ausgabe auf HTTP-Nachrichten einschränkt, die an WSDAPI-Stapel am Standardport gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="984ee-117">The following example shows a filter that limits output to HTTP messages sent to WSDAPI stacks on the default port.</span></span>

> [!Note]  
> <span data-ttu-id="984ee-118">Dienste können relevante HTTP-Nachrichten von anderen Ports als 5357 senden.</span><span class="sxs-lookup"><span data-stu-id="984ee-118">Services may send relevant HTTP messages from ports other than 5357.</span></span> <span data-ttu-id="984ee-119">Wenn der Datenverkehr von anderen Ports von Interesse ist, muss dieser Beispiel Filter vor der Verwendung geändert werden.</span><span class="sxs-lookup"><span data-stu-id="984ee-119">If traffic from other ports is of interest, then this sample filter must be modified before use.</span></span>

 

``` syntax
// HTTP messages sent to WSDAPI stacks on default port
TCP.Port == 5357
```

<span data-ttu-id="984ee-120">Das folgende Beispiel zeigt einen Filter, der die Ausgabe auf IPv4-Multicast Datenverkehr beschränkt.</span><span class="sxs-lookup"><span data-stu-id="984ee-120">The following example shows a filter that limits output to IPv4 multicast traffic.</span></span>

``` syntax
// All IPv4 multicast traffic
IPv4.DestinationAddress == 239.255.255.250
```

<span data-ttu-id="984ee-121">Das folgende Beispiel zeigt einen Filter, der die Ausgabe auf IPv6-Multicast Datenverkehr beschränkt.</span><span class="sxs-lookup"><span data-stu-id="984ee-121">The following example shows a filter that limits output to IPv6 multicast traffic.</span></span>

``` syntax
// All IPv6 multicast traffic
IPv6.DestinationAddress == FF02::C
```

<span data-ttu-id="984ee-122">Einige Filter können kombiniert werden, um die Ergebnisse weiter einzuschränken.</span><span class="sxs-lookup"><span data-stu-id="984ee-122">Some filters can be combined to further limit results.</span></span> <span data-ttu-id="984ee-123">Das folgende Beispiel zeigt einen Filter, der die Ausgabe auf IPv4-Multicast WS-Discovery-Datenverkehr beschränkt.</span><span class="sxs-lookup"><span data-stu-id="984ee-123">The following example shows a filter that limits output to IPv4 multicast WS-Discovery traffic.</span></span>

``` syntax
// All IPv4 multicast WS-Discovery traffic
UDP.Port==3702 && IPv4.DestinationAddress=239.255.255.250
```

<span data-ttu-id="984ee-124">Wenn diese Filter verwendet werden, kann relevanter Datenverkehr aus den Netmon-Ergebnissen ausgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="984ee-124">When these filters are used, relevant traffic may be excluded from the Netmon results.</span></span> <span data-ttu-id="984ee-125">Ein Ausschluss kann auftreten, wenn sich Dienste an anderen Ports als den Standardports (5357/5358) befinden und wenn ein DPWS-Stapel nicht auf Nachrichten mit dem Standardport antwortet.</span><span class="sxs-lookup"><span data-stu-id="984ee-125">Exclusion can occur when services reside at ports other than the default ports (5357/5358) and when a DPWS stack does not respond to messages using the default port.</span></span> <span data-ttu-id="984ee-126">In diesen Fällen müssen die Filter vor der Verwendung geändert werden.</span><span class="sxs-lookup"><span data-stu-id="984ee-126">In these cases, the filters must be modified before use.</span></span>

## <a name="related-topics"></a><span data-ttu-id="984ee-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="984ee-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="984ee-128">WSDAPI-Diagnose Prozeduren</span><span class="sxs-lookup"><span data-stu-id="984ee-128">WSDAPI Diagnostic Procedures</span></span>](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[<span data-ttu-id="984ee-129">Ersten Schritte mit der WSDAPI-Problembehandlung</span><span class="sxs-lookup"><span data-stu-id="984ee-129">Getting Started with WSDAPI Troubleshooting</span></span>](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



