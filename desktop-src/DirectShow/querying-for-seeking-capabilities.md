---
description: Abfragen der Suchfunktionen
ms.assetid: d1d8c708-75f2-4dc7-a33a-8dd2cea0ee00
title: Abfragen der Suchfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2aa763ab11267da0a9a13a920285491d83273a8d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860393"
---
# <a name="querying-for-seeking-capabilities"></a><span data-ttu-id="c5230-103">Abfragen der Suchfunktionen</span><span class="sxs-lookup"><span data-stu-id="c5230-103">Querying for Seeking Capabilities</span></span>

<span data-ttu-id="c5230-104">Microsoft® DirectShow® unterstützt das Suchen über die [**imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="c5230-104">Microsoft® DirectShow® supports seeking through the [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface.</span></span> <span data-ttu-id="c5230-105">Der Filter Graph-Manager macht diese Schnittstelle verfügbar, aber die Suchfunktion wird immer durch Filter im Diagramm implementiert.</span><span class="sxs-lookup"><span data-stu-id="c5230-105">The Filter Graph Manager exposes this interface, but the seeking functionality is always implemented by filters in the graph.</span></span>

<span data-ttu-id="c5230-106">Für einige Daten kann kein Seeding durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c5230-106">Some data cannot be seeked.</span></span> <span data-ttu-id="c5230-107">Beispielsweise können Sie keinen livevideostream von einer Kamera aus suchen.</span><span class="sxs-lookup"><span data-stu-id="c5230-107">For example, you cannot seek a live video stream from a camera.</span></span> <span data-ttu-id="c5230-108">Wenn ein Datenstrom durchsuchbar ist, gibt es jedoch unterschiedliche Typen, die er unterstützen kann.</span><span class="sxs-lookup"><span data-stu-id="c5230-108">If a stream is seekable, however, there are various types of seeking it might support.</span></span> <span data-ttu-id="c5230-109">Dazu gehören:</span><span class="sxs-lookup"><span data-stu-id="c5230-109">These include:</span></span>

-   <span data-ttu-id="c5230-110">Suchen einer beliebigen Position im Stream.</span><span class="sxs-lookup"><span data-stu-id="c5230-110">Seeking to an arbitrary position in the stream.</span></span>
-   <span data-ttu-id="c5230-111">Die Dauer des Streams wird abgerufen.</span><span class="sxs-lookup"><span data-stu-id="c5230-111">Retrieving the duration of the stream.</span></span>
-   <span data-ttu-id="c5230-112">Abrufen der aktuellen Position innerhalb des Streams.</span><span class="sxs-lookup"><span data-stu-id="c5230-112">Retrieving the current position within the stream.</span></span>
-   <span data-ttu-id="c5230-113">Spielen in umgekehrter Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="c5230-113">Playing in reverse.</span></span>

<span data-ttu-id="c5230-114">Die **imediaseeking** -Schnittstelle definiert einen Satz von Flags, [**\_ sucht nach \_ Such \_ Funktionen**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities), die die möglichen Suchfunktionen beschreiben.</span><span class="sxs-lookup"><span data-stu-id="c5230-114">The **IMediaSeeking** interface defines a set of flags, [**AM\_SEEKING\_SEEKING\_CAPABILITIES**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities), that describe the possible seeking capabilities.</span></span> <span data-ttu-id="c5230-115">Um die Funktionen des Streams abzurufen, rufen Sie die [**imediaseeking:: getfunktionalitäten**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="c5230-115">To retrieve the stream's capabilities, call the [**IMediaSeeking::GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) method.</span></span> <span data-ttu-id="c5230-116">Die-Methode gibt eine bitweise Kombination von-Flags zurück.</span><span class="sxs-lookup"><span data-stu-id="c5230-116">The method returns a bitwise combination of flags.</span></span> <span data-ttu-id="c5230-117">Die Anwendung kann Sie mit dem &-Operator (bitweiser **and-** Operator) testen.</span><span class="sxs-lookup"><span data-stu-id="c5230-117">The application can test them using the & (bitwise **AND**) operator.</span></span> <span data-ttu-id="c5230-118">Der folgende Code überprüft beispielsweise, ob das Diagramm an einer beliebigen Position suchen kann:</span><span class="sxs-lookup"><span data-stu-id="c5230-118">For example, the following code checks whether the graph can seek to an arbitrary position:</span></span>


```C++
DWORD dwCap = 0;
HRESULT hr = pSeek->GetCapabilities(&dwCap);
if (AM_SEEKING_CanSeekAbsolute & dwCap)
{
    // Graph can seek to absolute positions.
}
```



 

 



