---
description: Appsequence-Informationen, die in WS-Discovery Ankündigungs-und Antwort Nachrichten (Hello, Probe Matches und resolvematches) enthalten sind.
ms.assetid: f54eaa09-7ce8-4948-a0c5-edf2d054f6d5
title: Appsequence-Validierungsregeln
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ea44c1ee2d157608ddd1756e71d7183f310df87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528592"
---
# <a name="appsequence-validation-rules"></a><span data-ttu-id="969fd-103">Appsequence-Validierungsregeln</span><span class="sxs-lookup"><span data-stu-id="969fd-103">AppSequence Validation Rules</span></span>

<span data-ttu-id="969fd-104">Appsequence-Informationen, die in WS-Discovery Ankündigungs-und Antwort Nachrichten ([Hello](hello-message.md), [Probe Matches](probematches-message.md)und [resolvematches](resolvematches-message.md)) enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="969fd-104">AppSequence information contained in WS-Discovery announcement and response messages ([Hello](hello-message.md), [ProbeMatches](probematches-message.md), and [ResolveMatches](resolvematches-message.md)).</span></span> <span data-ttu-id="969fd-105">Diese Informationen werden von WSDAPI verarbeitet und überprüft, bevor diese Nachrichten an Komponenten oberhalb des Stapels weitergeleitet werden (z. b. Netzwerk-Explorer oder eine Anwendung, die WSDAPI aufrufen).</span><span class="sxs-lookup"><span data-stu-id="969fd-105">This information is processed and validated by WSDAPI before these messages are passed on to components above the stack (such as Network Explorer or an application calling into WSDAPI).</span></span>

<span data-ttu-id="969fd-106">Der folgende XML-Code zeigt ein Beispiel für ein appsequence-Element.</span><span class="sxs-lookup"><span data-stu-id="969fd-106">The following XML shows a sample AppSequence element.</span></span> <span data-ttu-id="969fd-107">Das WSD-Präfix verweist auf den-Namespace `https://schemas.xmlsoap.org/ws/2005/04/discovery` .</span><span class="sxs-lookup"><span data-stu-id="969fd-107">The wsd prefix refers to the namespace `https://schemas.xmlsoap.org/ws/2005/04/discovery`.</span></span>

``` syntax
<wsd:AppSequence InstanceId="2"
    SequenceId="urn:uuid:369a7d7b-5f87-48a4-aa9a-189edf2a8772"
    MessageNumber="21">
</wsd:AppSequence>
```

<span data-ttu-id="969fd-108">WSDAPI ignoriert veraltete Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="969fd-108">WSDAPI ignores stale messages.</span></span> <span data-ttu-id="969fd-109">Für jedes Gerät (eindeutig durch die Endpunkt Adresse im SOAP-Text identifiziert) ignoriert WSDAPI alle Nachrichten mit einer appsequence-messagenzahl, die niedriger ist als die letzte angezeigte Meldung.</span><span class="sxs-lookup"><span data-stu-id="969fd-109">For each device (uniquely identified by the Endpoint Address in the SOAP Body), WSDAPI ignores any messages with an AppSequence MessageNumber lower than the last message seen.</span></span>

<span data-ttu-id="969fd-110">WSDAPI ignoriert veraltete xaddr-Ankündigungen.</span><span class="sxs-lookup"><span data-stu-id="969fd-110">WSDAPI ignores stale XAddr announcements.</span></span> <span data-ttu-id="969fd-111">Wenn die appsequence-InstanceId niedriger als die letzte angezeigte instanceId ist, ignoriert WSDAPI die im SOAP-Text angekündigten xaddrs.</span><span class="sxs-lookup"><span data-stu-id="969fd-111">If the AppSequence InstanceId is lower than the last InstanceId seen, WSDAPI ignores the XAddrs advertised in the SOAP body.</span></span> <span data-ttu-id="969fd-112">Wenn die InstanceId gleich der vorherigen ist, aber MetadataVersion niedriger ist als die letzte MetadataVersion, ignoriert WSDAPI die xaddrs.</span><span class="sxs-lookup"><span data-stu-id="969fd-112">Also, if the InstanceId is the same as previous but the MetadataVersion is lower than the last MetadataVersion, WSDAPI ignores the XAddrs.</span></span>

<span data-ttu-id="969fd-113">WSDAPI ignoriert doppelte WS-Discovery Meldungen.</span><span class="sxs-lookup"><span data-stu-id="969fd-113">WSDAPI ignores duplicate WS-Discovery messages.</span></span> <span data-ttu-id="969fd-114">Wenn zwei identische WS-Discovery-Nachrichten an WSDAPI gesendet werden, wird nur der erste empfangene verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="969fd-114">If two identical WS-Discovery messages are sent to WSDAPI, only the first received will be processed.</span></span> <span data-ttu-id="969fd-115">Dies ist in der Regel nur für Anwendungen relevant, die direkt in die [**iwsdiscoverypublisher**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoverypublisher) -oder [**iwsdiscoveryprovider**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoveryprovider) -Schnittstellen aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="969fd-115">This is typically only relevant for applications that call directly into the [**IWSDiscoveryPublisher**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoverypublisher) or [**IWSDiscoveryProvider**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoveryprovider) interfaces.</span></span>

## <a name="related-topics"></a><span data-ttu-id="969fd-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="969fd-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="969fd-117">Ermittlungs-und Metadatenaustausch-Nachrichten Muster</span><span class="sxs-lookup"><span data-stu-id="969fd-117">Discovery and Metadata Exchange Message Patterns</span></span>](discovery-and-metadata-exchange-message-patterns.md)
</dt> </dl>

 

 



