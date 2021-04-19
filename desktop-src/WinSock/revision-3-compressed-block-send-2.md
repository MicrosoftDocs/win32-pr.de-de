---
description: In dieser Version der Anwendung wird ein komprimierter Block zum Senden der Daten verwendet. Diese Änderung führt zu einer erheblichen Verbesserung der Leistung.
ms.assetid: 3f0a129b-5b67-4334-a0aa-cd80ee7018b9
title: 'Revision 3: komprimierte Block-Sendevorgang'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 657579406ed31fce08239c518a6910f525219fdf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348306"
---
# <a name="revision-three-compressed-block-send"></a><span data-ttu-id="8e226-104">Revision 3: komprimierte Block-Sendevorgang</span><span class="sxs-lookup"><span data-stu-id="8e226-104">Revision Three: Compressed Block Send</span></span>

<span data-ttu-id="8e226-105">In dieser Version der Anwendung wird ein komprimierter Block zum Senden der Daten verwendet.</span><span class="sxs-lookup"><span data-stu-id="8e226-105">In this version of the application, a compressed block send of the data is used.</span></span> <span data-ttu-id="8e226-106">Diese Änderung führt zu einer erheblichen Verbesserung der Leistung.</span><span class="sxs-lookup"><span data-stu-id="8e226-106">This change results in significant performance improvement.</span></span>


```C++
BYTE tmp[3*ROWS*COLS];
FIELD Old = Map;
ComputeNext( Map );
n=Compact(Map,Old,tmp);
bind( s, ... );
connect( s, ... );
send( s, tmp, 3*n );
//can't do recv(s,tmp,n)
for(int i=0; i < n; )
    recv( s, tmp+i, n-i );
closesocket( s );
```



## <a name="changes-in-this-version"></a><span data-ttu-id="8e226-107">Änderungen in dieser Version</span><span class="sxs-lookup"><span data-stu-id="8e226-107">Changes in this Version</span></span>

<span data-ttu-id="8e226-108">Diese Version spiegelt die folgenden Änderungen wider:</span><span class="sxs-lookup"><span data-stu-id="8e226-108">This version reflects the following changes:</span></span>

-   <span data-ttu-id="8e226-109">Zell Aktualisierungen werden nicht mehr serialisiert.</span><span class="sxs-lookup"><span data-stu-id="8e226-109">Cell updates are no longer serialized.</span></span>
-   <span data-ttu-id="8e226-110">Da ein Block-Sendevorgang verwendet wird, ist die Anwendung nicht mehr im Kopf.</span><span class="sxs-lookup"><span data-stu-id="8e226-110">Since a block send is used, the application is no longer chatty.</span></span>
-   <span data-ttu-id="8e226-111">Die Datenkomprimierung wird verwendet, was zu einer weniger FAT-Anwendung führt.</span><span class="sxs-lookup"><span data-stu-id="8e226-111">Data compression is used, resulting in a less fat application.</span></span>

<span data-ttu-id="8e226-112">Es gibt immer noch ein Problem mit dieser Version der Anwendung. das Risiko eines Deadlocks besteht darin, dass ein großer Sendevorgang ohne empfangene Vorgänge verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8e226-112">There is still an issue with this version of the application; the risk of deadlock exists since a large send is used with no receives.</span></span> <span data-ttu-id="8e226-113">Der Server sendet pro 3 empfangener Bytes ein Byte.</span><span class="sxs-lookup"><span data-stu-id="8e226-113">The server sends one byte for every 3 bytes received.</span></span> <span data-ttu-id="8e226-114">Dies kann zu einem Deadlock führen, wenn die Empfangs Puffergröße für diese Beispielanwendung weniger als 1000 Bytes beträgt.</span><span class="sxs-lookup"><span data-stu-id="8e226-114">This could cause a deadlock if the receive buffer size is less than 1000 bytes for this sample application.</span></span>

## <a name="key-performance-metrics"></a><span data-ttu-id="8e226-115">Wichtige Leistungsmetriken</span><span class="sxs-lookup"><span data-stu-id="8e226-115">Key Performance Metrics</span></span>

<span data-ttu-id="8e226-116">Die folgenden Leistungsmetriken werden in Roundtripzeit (RTT), goodput und Protokoll Mehraufwand ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="8e226-116">The following performance metrics are expressed in Round Trip Time (RTT), Goodput, and Protocol Overhead.</span></span> <span data-ttu-id="8e226-117">Eine Erläuterung dieser Begriffe finden Sie im Thema zur [Netzwerkterminologie](network-terminology-2.md) .</span><span class="sxs-lookup"><span data-stu-id="8e226-117">See the [Network Terminology](network-terminology-2.md) topic for an explanation of these terms.</span></span>

<span data-ttu-id="8e226-118">Diese Version reflektiert die folgenden Leistungsmetriken:</span><span class="sxs-lookup"><span data-stu-id="8e226-118">This version reflects the following performance metrics:</span></span>

-   <span data-ttu-id="8e226-119">Zellzeit –. 002 \* RTT</span><span class="sxs-lookup"><span data-stu-id="8e226-119">Cell Time — .002\*RTT</span></span>
-   <span data-ttu-id="8e226-120">Goodput – 2 Kilobyte/RTT</span><span class="sxs-lookup"><span data-stu-id="8e226-120">Goodput — 2 Kilobytes/RTT</span></span>
-   <span data-ttu-id="8e226-121">Protokoll Aufwand – 14%</span><span class="sxs-lookup"><span data-stu-id="8e226-121">Protocol Overhead — 14%</span></span>

<span data-ttu-id="8e226-122">Der mehr Aufwand von 14% beträgt 6% von den Ethernet-Headern und die anderen 8% vom Start bis zum Start der Verbindung.</span><span class="sxs-lookup"><span data-stu-id="8e226-122">Of the 14% overhead, 6% is from the Ethernet headers and the other 8% is from the connection startup and teardown.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8e226-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8e226-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8e226-124">Verbessern einer langsamen Anwendung</span><span class="sxs-lookup"><span data-stu-id="8e226-124">Improving a Slow Application</span></span>](improving-a-slow-application-2.md)
</dt> <dt>

[<span data-ttu-id="8e226-125">Netzwerkterminologie</span><span class="sxs-lookup"><span data-stu-id="8e226-125">Network Terminology</span></span>](network-terminology-2.md)
</dt> <dt>

[<span data-ttu-id="8e226-126">Baselineversion: eine sehr schlechte leistungsfähige Anwendung</span><span class="sxs-lookup"><span data-stu-id="8e226-126">The Baseline Version: A Very Poor Performing Application</span></span>](the-baseline-version-a-very-poor-performing-application-2.md)
</dt> <dt>

[<span data-ttu-id="8e226-127">Revision 1: Bereinigen der offensichtlichen</span><span class="sxs-lookup"><span data-stu-id="8e226-127">Revision 1: Cleaning up the Obvious</span></span>](revision-1-cleaning-up-the-obvious-2.md)
</dt> <dt>

[<span data-ttu-id="8e226-128">Revision 2: Neuentwerfen für eine geringere Anzahl von Verbindungen</span><span class="sxs-lookup"><span data-stu-id="8e226-128">Revision 2: Redesigning for Fewer Connects</span></span>](revision-2-redesigning-for-fewer-connects-2.md)
</dt> <dt>

[<span data-ttu-id="8e226-129">Zukünftige Verbesserungen</span><span class="sxs-lookup"><span data-stu-id="8e226-129">Future Improvements</span></span>](future-improvements-2.md)
</dt> </dl>

 

 



