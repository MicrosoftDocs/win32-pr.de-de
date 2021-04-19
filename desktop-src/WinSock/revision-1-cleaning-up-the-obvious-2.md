---
description: In dieser Version des Beispiel Programms wurden einige offensichtliche Änderungen vorgenommen, die den ersten Schritten bei der Verbesserung der Leistung in Kauf nehmen.
ms.assetid: ef9d594c-31fe-44c0-b707-47c01e2c5bf0
title: 'Revision 1: Bereinigen der offensichtlichen'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 631bea7395000531cce542b41ace3b3aab9afff0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348920"
---
# <a name="revision-one-cleaning-up-the-obvious"></a><span data-ttu-id="4b7bc-103">Revision 1: Bereinigen der offensichtlichen</span><span class="sxs-lookup"><span data-stu-id="4b7bc-103">Revision One: Cleaning up the Obvious</span></span>

<span data-ttu-id="4b7bc-104">In dieser Version des Beispiel Programms wurden einige offensichtliche Änderungen vorgenommen, die den ersten Schritten bei der Verbesserung der Leistung in Kauf nehmen.</span><span class="sxs-lookup"><span data-stu-id="4b7bc-104">In this version of the example program, a few obvious changes have been made that will take initial strides at improving performance.</span></span> <span data-ttu-id="4b7bc-105">Diese Version des Codes ist weit von der Leistungsoptimierung entfernt. es handelt sich jedoch um einen guten inkrementellen Schritt, der die Untersuchung der Auswirkungen von inkrementellen besseren Ansätzen ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="4b7bc-105">This version of the code is far from performance-tuned, but it is a good incremental step that enables examination of the effects of incrementally better approaches.</span></span>

> [!WARNING]
> <span data-ttu-id="4b7bc-106">Dieses Beispiel für die Anwendung bietet absichtlich eine schlechte Leistung, um mit Codeänderungen mögliche Leistungsverbesserungen zu veranschaulichen.</span><span class="sxs-lookup"><span data-stu-id="4b7bc-106">This example of the application provides intentionally poor performance, in order to illustrate performance improvements possible with changes to code.</span></span> <span data-ttu-id="4b7bc-107">Verwenden Sie dieses Codebeispiel nicht in Ihrer Anwendung. Dies dient nur zur Veranschaulichung.</span><span class="sxs-lookup"><span data-stu-id="4b7bc-107">Do not use this code sample in your application; it is for illustration purposes only.</span></span>

 


```C++
#include <windows.h>

BYTE Set(row, col, bAlive)
{
    SOCKET s = socket(...);
    BYTE byRet = 0;
    BYTE tmp[3];
    tmp[0] = (BYTE)row;
    tmp[1] = (BYTE)col;
    tmp[2] = (BYTE)bAlive;
    bind( s, ... );
    connect( s, ... );
    send( s, &tmp, 3 );
    recv( s, &byRet, 1 );
    closesocket( s );
    return byRet;
}
```



## <a name="changes-in-this-version"></a><span data-ttu-id="4b7bc-108">Änderungen in dieser Version</span><span class="sxs-lookup"><span data-stu-id="4b7bc-108">Changes in this Version</span></span>

<span data-ttu-id="4b7bc-109">Diese Version spiegelt die folgenden Änderungen wider:</span><span class="sxs-lookup"><span data-stu-id="4b7bc-109">This version reflects the following changes:</span></span>

-   <span data-ttu-id="4b7bc-110">"Sndbuf = 0" wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="4b7bc-110">Removed SNDBUF=0.</span></span> <span data-ttu-id="4b7bc-111">Die 200 Millisekunden Verzögerungen aufgrund von ungepufferten Sende-und verzögerten Bestätigungen werden entfernt.</span><span class="sxs-lookup"><span data-stu-id="4b7bc-111">The 200 millisecond delays due to unbuffered sends and delayed acknowledgments are removed.</span></span>
-   <span data-ttu-id="4b7bc-112">Das Sende-Send-Receive-Verhalten wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="4b7bc-112">Removed the Send-Send-Receive behavior.</span></span> <span data-ttu-id="4b7bc-113">Diese Änderung beseitigt 200-Millisekunden-Verzögerungen aufgrund von Nagle-und verzögerten ACK-Interaktionen.</span><span class="sxs-lookup"><span data-stu-id="4b7bc-113">This change eliminates 200-millisecond delays due to Nagle and delayed ACK interactions.</span></span>
-   <span data-ttu-id="4b7bc-114">Die Little-d-Annahme wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="4b7bc-114">Removed little-endian assumption.</span></span> <span data-ttu-id="4b7bc-115">Die Bytes sind nun in der richtigen Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="4b7bc-115">The bytes are now in order.</span></span>

## <a name="remaining-problems"></a><span data-ttu-id="4b7bc-116">Verbleibende Probleme</span><span class="sxs-lookup"><span data-stu-id="4b7bc-116">Remaining Problems</span></span>

<span data-ttu-id="4b7bc-117">In dieser Version verbleiben die folgenden Probleme:</span><span class="sxs-lookup"><span data-stu-id="4b7bc-117">In this version, the following problems remain:</span></span>

-   <span data-ttu-id="4b7bc-118">Die Anwendung stellt immer noch eine hohe Verbindung her.</span><span class="sxs-lookup"><span data-stu-id="4b7bc-118">The application is still connect heavy.</span></span> <span data-ttu-id="4b7bc-119">Da die Verzögerungen von 600 MS Millisekunden entfernt werden, erreicht die Anwendung jetzt die 12 Verbindungen pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="4b7bc-119">Since the 600+ millisecond delays are removed, the application now hits the 12 connects-per-second sustained rate.</span></span> <span data-ttu-id="4b7bc-120">Viele gleichzeitige Verbindungen werden nun zu einem Problem.</span><span class="sxs-lookup"><span data-stu-id="4b7bc-120">Many concurrent connections now becomes an issue.</span></span>
-   <span data-ttu-id="4b7bc-121">Die Anwendung ist immer noch FAT. unveränderte Zellen werden weiterhin an den Server weitergegeben.</span><span class="sxs-lookup"><span data-stu-id="4b7bc-121">The application is still fat; unchanged cells are still propagated to the server.</span></span>
-   <span data-ttu-id="4b7bc-122">Die Anwendung weist immer noch ein schlechtes Streaming auf. 3-Byte-Sendungen sind immer noch kleine Sende Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="4b7bc-122">The application still exhibits poor streaming; 3-byte sends are still small sends.</span></span>
-   <span data-ttu-id="4b7bc-123">Die Anwendung sendet jetzt 2 Bytes/RTT, was bei einem direkt verbundenen Ethernet 4 KB/s beträgt.</span><span class="sxs-lookup"><span data-stu-id="4b7bc-123">The application now sends 2 bytes/RTT, which equals 4 KB/s on directly connected Ethernet.</span></span> <span data-ttu-id="4b7bc-124">Dies ist nicht zu schnell, aber die Wartezeit führt wahrscheinlich zunächst zu Problemen.</span><span class="sxs-lookup"><span data-stu-id="4b7bc-124">This is not too fast, but TIME-WAIT will likely cause problems first.</span></span>
-   <span data-ttu-id="4b7bc-125">Der Aufwand liegt bei bis zu 99,3%, was jedoch immer noch keinen guten Verwaltungs Prozentsatz zur Folge hat.</span><span class="sxs-lookup"><span data-stu-id="4b7bc-125">The overhead is down to 99.3%, which is still not a good overhead percentage.</span></span>

## <a name="key-performance-metrics"></a><span data-ttu-id="4b7bc-126">Wichtige Leistungsmetriken</span><span class="sxs-lookup"><span data-stu-id="4b7bc-126">Key Performance Metrics</span></span>

<span data-ttu-id="4b7bc-127">Die folgenden wichtigen Leistungsmetriken werden in Roundtripzeit (RTT), goodput und Protokoll Mehraufwand ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="4b7bc-127">The following key performance metrics are expressed in Round Trip Time (RTT), Goodput, and Protocol Overhead.</span></span> <span data-ttu-id="4b7bc-128">Eine Erläuterung dieser Begriffe finden Sie im Thema zur [Netzwerkterminologie](network-terminology-2.md) .</span><span class="sxs-lookup"><span data-stu-id="4b7bc-128">See the [Network Terminology](network-terminology-2.md) topic for an explanation of these terms.</span></span>

<span data-ttu-id="4b7bc-129">Diese Version reflektiert die folgenden Leistungsmetriken:</span><span class="sxs-lookup"><span data-stu-id="4b7bc-129">This version reflect the following performance metrics:</span></span>

-   <span data-ttu-id="4b7bc-130">Zellzeit – 2 × RTT</span><span class="sxs-lookup"><span data-stu-id="4b7bc-130">Cell Time—2×RTT</span></span>
-   <span data-ttu-id="4b7bc-131">Goodput – 2 Bytes/RTT</span><span class="sxs-lookup"><span data-stu-id="4b7bc-131">Goodput—2 bytes/RTT</span></span>
-   <span data-ttu-id="4b7bc-132">Protokoll Aufwand – 99,3 Prozent</span><span class="sxs-lookup"><span data-stu-id="4b7bc-132">Protocol Overhead—99.3 percent</span></span>

## <a name="related-topics"></a><span data-ttu-id="4b7bc-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4b7bc-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b7bc-134">Verbessern einer langsamen Anwendung</span><span class="sxs-lookup"><span data-stu-id="4b7bc-134">Improving a Slow Application</span></span>](improving-a-slow-application-2.md)
</dt> <dt>

[<span data-ttu-id="4b7bc-135">Netzwerkterminologie</span><span class="sxs-lookup"><span data-stu-id="4b7bc-135">Network Terminology</span></span>](network-terminology-2.md)
</dt> <dt>

[<span data-ttu-id="4b7bc-136">Baselineversion: eine sehr schlechte leistungsfähige Anwendung</span><span class="sxs-lookup"><span data-stu-id="4b7bc-136">The Baseline Version: A Very Poor Performing Application</span></span>](the-baseline-version-a-very-poor-performing-application-2.md)
</dt> <dt>

[<span data-ttu-id="4b7bc-137">Revision 2: Neuentwerfen für eine geringere Anzahl von Verbindungen</span><span class="sxs-lookup"><span data-stu-id="4b7bc-137">Revision 2: Redesigning for Fewer Connects</span></span>](revision-2-redesigning-for-fewer-connects-2.md)
</dt> <dt>

[<span data-ttu-id="4b7bc-138">Revision 3: komprimierte Block-Sendevorgang</span><span class="sxs-lookup"><span data-stu-id="4b7bc-138">Revision 3: Compressed Block Send</span></span>](revision-3-compressed-block-send-2.md)
</dt> <dt>

[<span data-ttu-id="4b7bc-139">Zukünftige Verbesserungen</span><span class="sxs-lookup"><span data-stu-id="4b7bc-139">Future Improvements</span></span>](future-improvements-2.md)
</dt> </dl>

 

 



