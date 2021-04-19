---
description: Die Baselineversion einer sehr schlechten Leistung in Windows Sockets (Winsock).
ms.assetid: 923884c4-f1bd-4f72-983e-6158f368e0dd
title: 'Baselineversion: eine sehr schlechte leistungsfähige Anwendung'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7c094be5fd5cf6e3b9eaeb07c7ff38880e651dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373083"
---
# <a name="the-baseline-version-a-very-poor-performing-application"></a><span data-ttu-id="d9ea1-103">Baselineversion: eine sehr schlechte leistungsfähige Anwendung</span><span class="sxs-lookup"><span data-stu-id="d9ea1-103">The Baseline Version: A Very Poor Performing Application</span></span>

<span data-ttu-id="d9ea1-104">Das anfängliche, schlechte Codebeispiel, das zum Berechnen der Updates verwendet wird, lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="d9ea1-104">The initial, poor performing code sample used to calculate the updates is as follows:</span></span>

> [!Note]  
> <span data-ttu-id="d9ea1-105">Der Einfachheit halber gibt es in den folgenden Beispielen keine Fehlerbehandlung.</span><span class="sxs-lookup"><span data-stu-id="d9ea1-105">For simplicity, there is no error handling in the following examples.</span></span> <span data-ttu-id="d9ea1-106">Alle Produktionsanwendungen überprüfen immer Rückgabewerte.</span><span class="sxs-lookup"><span data-stu-id="d9ea1-106">Any production application always checks return values.</span></span>

 

> [!WARNING]
> <span data-ttu-id="d9ea1-107">Die ersten Beispiele der Anwendung sorgen für eine absichtlich schlechte Leistung, um mit Codeänderungen mögliche Leistungsverbesserungen zu veranschaulichen.</span><span class="sxs-lookup"><span data-stu-id="d9ea1-107">The first few examples of the application provide intentionally poor performance, in order to illustrate performance improvements possible with changes to code.</span></span> <span data-ttu-id="d9ea1-108">Verwenden Sie diese Codebeispiele nicht in Ihrer Anwendung. Sie dienen nur zur Veranschaulichung.</span><span class="sxs-lookup"><span data-stu-id="d9ea1-108">Do not use these code samples in your application; they are for illustration purposes only.</span></span>

 


```C++
#include <windows.h>

BOOL Map[ROWS][COLS];

void LifeUpdate()
{
    ComputeNext( Map );
    for( int i = 0 ; i < ROWS ; ++i )     //serialized
        for( int j = 0 ; j < COLS ; ++j )
            Set( i, j, Map[i][j] );    //chatty
}

BYTE Set(row, col, bAlive)
{
    SOCKET s = socket(...);
    BYTE byRet = 0;
    setsockopt( s, SO_SNDBUF, &Zero, sizeof(int) );
    bind( s, ... );
    connect( s, ... );
    send( s, &row, 1 );
    send( s, &col, 1 );
    send( s, &bAlive, 1 );
    recv( s, &byRet, 1 );
    closesocket( s );
    return byRet;
}
```



<span data-ttu-id="d9ea1-109">In diesem Zustand hat die Anwendung eine möglichst schlechteste Netzwerkleistung.</span><span class="sxs-lookup"><span data-stu-id="d9ea1-109">In this state, the application has the worst possible network performance.</span></span> <span data-ttu-id="d9ea1-110">Folgende Probleme sind in dieser Version der Beispielanwendung zu finden:</span><span class="sxs-lookup"><span data-stu-id="d9ea1-110">The problems with this version of the sample application include:</span></span>

-   <span data-ttu-id="d9ea1-111">Die Anwendung ist unterteilt.</span><span class="sxs-lookup"><span data-stu-id="d9ea1-111">The application is chatty.</span></span> <span data-ttu-id="d9ea1-112">Jede Transaktion ist zu klein – die Zellen müssen nicht nacheinander aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="d9ea1-112">Each transaction is too small — cells do not need to be updated one by one.</span></span>
-   <span data-ttu-id="d9ea1-113">Die Transaktionen werden streng serialisiert, auch wenn die Zellen gleichzeitig aktualisiert werden könnten.</span><span class="sxs-lookup"><span data-stu-id="d9ea1-113">The transactions are strictly serialized, even though the cells could be updated concurrently.</span></span>
-   <span data-ttu-id="d9ea1-114">Der Sendepuffer ist auf NULL festgelegt, und die Anwendung verursacht eine Verzögerung von 200 Millisekunden für jede Sende – dreimal pro Zelle.</span><span class="sxs-lookup"><span data-stu-id="d9ea1-114">The send buffer is set to zero, and the application incurs a 200-millisecond delay for each send — three times per cell.</span></span>
-   <span data-ttu-id="d9ea1-115">Die Anwendung stellt eine hohe Verbindung her und stellt für jede Zelle eine Verbindung her.</span><span class="sxs-lookup"><span data-stu-id="d9ea1-115">The application is very connect heavy, connecting once for each cell.</span></span> <span data-ttu-id="d9ea1-116">Anwendungen sind aufgrund des Zeit warte Zustands in der Anzahl der Verbindungen pro Sekunde für ein bestimmtes Ziel beschränkt, dies ist jedoch kein Problem, da jede Transaktion mehr als 600 Millisekunden benötigt.</span><span class="sxs-lookup"><span data-stu-id="d9ea1-116">Applications are limited in the number of connections per second for a given destination because of TIME-WAIT state, but that is not an issue here, since each transaction takes over 600 milliseconds.</span></span>
-   <span data-ttu-id="d9ea1-117">Die Anwendung ist FAT. viele Transaktionen haben keine Auswirkung auf den Serverstatus, da viele Zellen nicht von Update zum Update geändert werden.</span><span class="sxs-lookup"><span data-stu-id="d9ea1-117">The application is fat; many transactions have no effect on the server state, because many cells do not change from update to update.</span></span>
-   <span data-ttu-id="d9ea1-118">Die Anwendung zeigt ein schlechtes Streaming an. kleine Sende Vorgänge beanspruchen viel CPU und RAM.</span><span class="sxs-lookup"><span data-stu-id="d9ea1-118">The application exhibits poor streaming; small sends consume a lot of CPU and RAM.</span></span>
-   <span data-ttu-id="d9ea1-119">Die Anwendung setzt eine Little-Endian-Darstellung für Ihre Sendungen voraus.</span><span class="sxs-lookup"><span data-stu-id="d9ea1-119">The application assumes little-endian representation for its sends.</span></span> <span data-ttu-id="d9ea1-120">Dies ist eine natürliche Annahme für die aktuelle Windows-Plattform, kann aber für lang gelebten Code gefährlich sein.</span><span class="sxs-lookup"><span data-stu-id="d9ea1-120">This is a natural assumption for the current Windows platform, but can be dangerous for long-lived code.</span></span>

## <a name="key-performance-metrics"></a><span data-ttu-id="d9ea1-121">Wichtige Leistungsmetriken</span><span class="sxs-lookup"><span data-stu-id="d9ea1-121">Key Performance Metrics</span></span>

<span data-ttu-id="d9ea1-122">Die folgenden Leistungsmetriken werden in Roundtripzeit (RTT), goodput und Protokoll Mehraufwand ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="d9ea1-122">The following performance metrics are expressed in Round Trip Time (RTT), Goodput, and Protocol Overhead.</span></span> <span data-ttu-id="d9ea1-123">Eine Erläuterung dieser Begriffe finden Sie im Thema zur [Netzwerkterminologie](network-terminology-2.md) .</span><span class="sxs-lookup"><span data-stu-id="d9ea1-123">See the [Network Terminology](network-terminology-2.md) topic for an explanation of these terms.</span></span>

-   <span data-ttu-id="d9ea1-124">Zellzeit, Netzwerk Zeit für das Update einer einzelnen Zelle, erfordert 4 \* RTT + 600 Millisekunden für Nagle und verzögerte ACK-Interaktionen.</span><span class="sxs-lookup"><span data-stu-id="d9ea1-124">Cell time, network time for a single cell update, requires 4\*RTT + 600 milliseconds for Nagle and delayed ACK interactions.</span></span>
-   <span data-ttu-id="d9ea1-125">Goodput ist kleiner als 6 Bytes.</span><span class="sxs-lookup"><span data-stu-id="d9ea1-125">Goodput is less than 6 bytes.</span></span>
-   <span data-ttu-id="d9ea1-126">Der Protokoll Mehraufwand beträgt 99,6%.</span><span class="sxs-lookup"><span data-stu-id="d9ea1-126">Protocol Overhead is 99.6%.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d9ea1-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d9ea1-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d9ea1-128">Verbessern einer langsamen Anwendung</span><span class="sxs-lookup"><span data-stu-id="d9ea1-128">Improving a Slow Application</span></span>](improving-a-slow-application-2.md)
</dt> <dt>

[<span data-ttu-id="d9ea1-129">Netzwerkterminologie</span><span class="sxs-lookup"><span data-stu-id="d9ea1-129">Network Terminology</span></span>](network-terminology-2.md)
</dt> <dt>

[<span data-ttu-id="d9ea1-130">Revision 1: Bereinigen der offensichtlichen</span><span class="sxs-lookup"><span data-stu-id="d9ea1-130">Revision 1: Cleaning up the Obvious</span></span>](revision-1-cleaning-up-the-obvious-2.md)
</dt> <dt>

[<span data-ttu-id="d9ea1-131">Revision 2: Neuentwerfen für eine geringere Anzahl von Verbindungen</span><span class="sxs-lookup"><span data-stu-id="d9ea1-131">Revision 2: Redesigning for Fewer Connects</span></span>](revision-2-redesigning-for-fewer-connects-2.md)
</dt> <dt>

[<span data-ttu-id="d9ea1-132">Revision 3: komprimierte Block-Sendevorgang</span><span class="sxs-lookup"><span data-stu-id="d9ea1-132">Revision 3: Compressed Block Send</span></span>](revision-3-compressed-block-send-2.md)
</dt> <dt>

[<span data-ttu-id="d9ea1-133">Zukünftige Verbesserungen</span><span class="sxs-lookup"><span data-stu-id="d9ea1-133">Future Improvements</span></span>](future-improvements-2.md)
</dt> </dl>

 

 



