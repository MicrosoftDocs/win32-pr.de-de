---
description: In dieser Revision wird die Beispielanwendung neu gestaltet, um unnötige Verbindungen auszuschließen.
ms.assetid: 0db6ded4-0a59-454e-824e-8cd7f0dc9fec
title: 'Revision 2: Neuentwerfen für eine geringere Anzahl von Verbindungen'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae8d5a8c8648f43f9ddac93c9d17f667b4b97011
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131028"
---
# <a name="revision-two-redesigning-for-fewer-connects"></a><span data-ttu-id="36f68-103">Revision 2: Neuentwerfen für eine geringere Anzahl von Verbindungen</span><span class="sxs-lookup"><span data-stu-id="36f68-103">Revision Two: Redesigning for Fewer Connects</span></span>

<span data-ttu-id="36f68-104">In dieser Revision wird die Beispielanwendung neu gestaltet, um unnötige Verbindungen auszuschließen.</span><span class="sxs-lookup"><span data-stu-id="36f68-104">In this revision, the sample application is redesigned to eliminate unnecessary connects.</span></span>

> [!WARNING]
> <span data-ttu-id="36f68-105">Diese Anwendungsbeispiele sorgen auch für eine absichtlich schlechte Leistung, um mit Codeänderungen mögliche Leistungsverbesserungen zu veranschaulichen.</span><span class="sxs-lookup"><span data-stu-id="36f68-105">This examples of the application also provide intentionally poor performance, in order to illustrate performance improvements possible with changes to code.</span></span> <span data-ttu-id="36f68-106">Verwenden Sie dieses Codebeispiel nicht in Ihrer Anwendung. Dies dient nur zur Veranschaulichung.</span><span class="sxs-lookup"><span data-stu-id="36f68-106">Do not use this code sample in your application; it is for illustration purposes only.</span></span>

 


```C++
ComputeNext( Map );
bind( s, ... );
connect( s, ... );
for(int i=0 ; i < ROWS ; ++i)
  for(int j=0 ; j < COLS ; ++j)
  {
    BYTE tmp[3];
    tmp[0] = i;
    tmp[1] = j;
    tmp[2] = Map[i][j];
    send( s, tmp, 3 );
    recv( s, &byRet, 1 );
  }
closesocket( s );
```



## <a name="remaining-problems"></a><span data-ttu-id="36f68-107">Verbleibende Probleme</span><span class="sxs-lookup"><span data-stu-id="36f68-107">Remaining Problems</span></span>

<span data-ttu-id="36f68-108">Durch die Änderungen in Revision 2 wurde die Anwendung neu gestaltet, sodass nur eine Verbindung pro Update hergestellt werden konnte.</span><span class="sxs-lookup"><span data-stu-id="36f68-108">The changes in Revision Two redesigned the application to make only one connect per update.</span></span> <span data-ttu-id="36f68-109">Die Anwendung beinhaltet weiterhin folgende Leistungsprobleme:</span><span class="sxs-lookup"><span data-stu-id="36f68-109">The application still includes the following performance issues:</span></span>

-   <span data-ttu-id="36f68-110">Die Anwendung wird immer noch serialisiert und ist unterteilt.</span><span class="sxs-lookup"><span data-stu-id="36f68-110">The application is still serialized and chatty.</span></span>
-   <span data-ttu-id="36f68-111">Die Anwendung hat immer noch ein FAT-Design. Es gibt viele Sende Vorgänge, für die in diesem Entwurf kein Vorgang erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="36f68-111">The application still has a fat design; there are many sends that require no operation in this design.</span></span>
-   <span data-ttu-id="36f68-112">Die Sende Vorgänge sind immer noch nur 3 Bytes, was zu einem schlechten Streaming gehört.</span><span class="sxs-lookup"><span data-stu-id="36f68-112">The sends are still only 3 bytes, which is poor streaming.</span></span>

## <a name="key-performance-metrics"></a><span data-ttu-id="36f68-113">Wichtige Leistungsmetriken</span><span class="sxs-lookup"><span data-stu-id="36f68-113">Key Performance Metrics</span></span>

<span data-ttu-id="36f68-114">Die folgenden Leistungsmetriken werden in Roundtripzeit (RTT), goodput und Protokoll Mehraufwand ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="36f68-114">The following performance metrics are expressed in Round Trip Time (RTT), Goodput, and Protocol Overhead.</span></span> <span data-ttu-id="36f68-115">Eine Erläuterung dieser Begriffe finden Sie im Thema zur [Netzwerkterminologie](network-terminology-2.md) .</span><span class="sxs-lookup"><span data-stu-id="36f68-115">See the [Network Terminology](network-terminology-2.md) topic for an explanation of these terms.</span></span>

<span data-ttu-id="36f68-116">Diese Version reflektiert die folgenden Leistungsmetriken:</span><span class="sxs-lookup"><span data-stu-id="36f68-116">This version reflects the following performance metrics:</span></span>

-   <span data-ttu-id="36f68-117">Zellzeit – 1 \* RTT</span><span class="sxs-lookup"><span data-stu-id="36f68-117">Cell Time — 1\*RTT</span></span>
-   <span data-ttu-id="36f68-118">Goodput – 4 Bytes/RTT</span><span class="sxs-lookup"><span data-stu-id="36f68-118">Goodput — 4 bytes/RTT</span></span>
-   <span data-ttu-id="36f68-119">Protokoll Aufwand – 96,8%</span><span class="sxs-lookup"><span data-stu-id="36f68-119">Protocol Overhead — 96.8%</span></span>

## <a name="related-topics"></a><span data-ttu-id="36f68-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="36f68-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="36f68-121">Verbessern einer langsamen Anwendung</span><span class="sxs-lookup"><span data-stu-id="36f68-121">Improving a Slow Application</span></span>](improving-a-slow-application-2.md)
</dt> <dt>

[<span data-ttu-id="36f68-122">Netzwerkterminologie</span><span class="sxs-lookup"><span data-stu-id="36f68-122">Network Terminology</span></span>](network-terminology-2.md)
</dt> <dt>

[<span data-ttu-id="36f68-123">Baselineversion: eine sehr schlechte leistungsfähige Anwendung</span><span class="sxs-lookup"><span data-stu-id="36f68-123">The Baseline Version: A Very Poor Performing Application</span></span>](the-baseline-version-a-very-poor-performing-application-2.md)
</dt> <dt>

[<span data-ttu-id="36f68-124">Revision 1: Bereinigen der offensichtlichen</span><span class="sxs-lookup"><span data-stu-id="36f68-124">Revision 1: Cleaning up the Obvious</span></span>](revision-1-cleaning-up-the-obvious-2.md)
</dt> <dt>

[<span data-ttu-id="36f68-125">Revision 3: komprimierte Block-Sendevorgang</span><span class="sxs-lookup"><span data-stu-id="36f68-125">Revision 3: Compressed Block Send</span></span>](revision-3-compressed-block-send-2.md)
</dt> <dt>

[<span data-ttu-id="36f68-126">Zukünftige Verbesserungen</span><span class="sxs-lookup"><span data-stu-id="36f68-126">Future Improvements</span></span>](future-improvements-2.md)
</dt> </dl>

 

 



