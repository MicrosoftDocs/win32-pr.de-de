---
description: Aufbau
ms.assetid: b5f607b2-9cca-4eef-9c63-d2015bd10469
title: Aufbau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e030e02ab77ec54e1e340d72db7210665d649bfb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346184"
---
# <a name="composition"></a><span data-ttu-id="7049f-103">Aufbau</span><span class="sxs-lookup"><span data-stu-id="7049f-103">Composition</span></span>

> [!Note]  
> <span data-ttu-id="7049f-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="7049f-104">\[Deprecated.</span></span> <span data-ttu-id="7049f-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="7049f-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="7049f-106">Das Kompositions Objekt ist ein Container für Spuren.</span><span class="sxs-lookup"><span data-stu-id="7049f-106">The composition object is a container for tracks.</span></span> <span data-ttu-id="7049f-107">Sie kann auch andere Kompositionen (für die Schachtelung von Spuren), Effekte und Übergänge enthalten.</span><span class="sxs-lookup"><span data-stu-id="7049f-107">It can also hold other compositions (for nesting of tracks), effects, and transitions.</span></span> <span data-ttu-id="7049f-108">Um dieses Objekt zu erstellen, rufen Sie die [**iamtimeline:: erkreateemptynode**](iamtimeline-createemptynode.md) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="7049f-108">To create this object, call the [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) method.</span></span>

<span data-ttu-id="7049f-109">Das Kompositions Objekt macht die folgenden Schnittstellen verfügbar:</span><span class="sxs-lookup"><span data-stu-id="7049f-109">The composition object exposes the following interfaces:</span></span>

-   [<span data-ttu-id="7049f-110">**Iamtimelinecomp**</span><span class="sxs-lookup"><span data-stu-id="7049f-110">**IAMTimelineComp**</span></span>](iamtimelinecomp.md)
-   [<span data-ttu-id="7049f-111">**Iamtimelineeffectable**</span><span class="sxs-lookup"><span data-stu-id="7049f-111">**IAMTimelineEffectable**</span></span>](iamtimelineeffectable.md)
-   [<span data-ttu-id="7049f-112">**Iamtimelineobj**</span><span class="sxs-lookup"><span data-stu-id="7049f-112">**IAMTimelineObj**</span></span>](iamtimelineobj.md)
-   [<span data-ttu-id="7049f-113">**Iamtimelinetransable**</span><span class="sxs-lookup"><span data-stu-id="7049f-113">**IAMTimelineTransable**</span></span>](iamtimelinetransable.md)
-   [<span data-ttu-id="7049f-114">**Iamtimelinevirtualtrack**</span><span class="sxs-lookup"><span data-stu-id="7049f-114">**IAMTimelineVirtualTrack**</span></span>](iamtimelinevirtualtrack.md)

## <a name="related-topics"></a><span data-ttu-id="7049f-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7049f-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7049f-116">Das Zeitachsen Modell</span><span class="sxs-lookup"><span data-stu-id="7049f-116">The Timeline Model</span></span>](the-timeline-model.md)
</dt> <dt>

[<span data-ttu-id="7049f-117">Erstellen einer Zeitachse</span><span class="sxs-lookup"><span data-stu-id="7049f-117">Constructing a Timeline</span></span>](constructing-a-timeline.md)
</dt> </dl>

 

 



