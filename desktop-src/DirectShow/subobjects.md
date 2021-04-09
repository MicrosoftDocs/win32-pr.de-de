---
description: Unter Objekte
ms.assetid: 03cbd590-b573-4a98-9ab7-fe548800cfcb
title: Unter Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad8b427a315231577f1608a168629bc8b77d2cc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867083"
---
# <a name="subobjects"></a><span data-ttu-id="4135b-103">Unter Objekte</span><span class="sxs-lookup"><span data-stu-id="4135b-103">Subobjects</span></span>

<span data-ttu-id="4135b-104">\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]</span><span class="sxs-lookup"><span data-stu-id="4135b-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="4135b-105">Quellen, Effekte und Übergänge verfügen über interne Zeiger auf andere COM-Objekte, die als unter *geordnete* Objekte bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="4135b-105">Sources, effects, and transitions have internal pointers to other COM objects, called *subobjects*.</span></span> <span data-ttu-id="4135b-106">Das untergeordnete Objekt führt die eigentliche Arbeit des-Objekts aus.</span><span class="sxs-lookup"><span data-stu-id="4135b-106">The subobject performs the actual work of the object.</span></span> <span data-ttu-id="4135b-107">Das untergeordnete Objekt einer Quelle ist die Komponente, mit der die Video-oder Audiodaten erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="4135b-107">The subobject of a source is the component that creates the video or audio data.</span></span> <span data-ttu-id="4135b-108">Das untergeordnete Objekt eines Effekts oder Übergangs ist die Komponente, die die Daten transformiert. Beispielsweise werden in einem Videoeffekt die visuellen Effekte im Videostream erstellt.</span><span class="sxs-lookup"><span data-stu-id="4135b-108">The subobject of an effect or transition is the component that transforms the data; for example, in a video effect, it creates the visual effect in the video stream.</span></span>

<span data-ttu-id="4135b-109">Der Typ des untergeordneten Objekts hängt vom Objekttyp ab:</span><span class="sxs-lookup"><span data-stu-id="4135b-109">The type of subobject depends on the type of object:</span></span>

-   <span data-ttu-id="4135b-110">Quelle: jeder DirectShow-Quell Filter oder Parserfilter, der Suchvorgänge unterstützt und ein von der unterstützte Format unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4135b-110">Source: Any DirectShow source filter or parser filter that supports seeking and produces a format that DES supports.</span></span> <span data-ttu-id="4135b-111">Es kann ein komprimiertes Format sein, wenn DirectShow-Filter vorhanden sind, um es zu decodieren.</span><span class="sxs-lookup"><span data-stu-id="4135b-111">It can be a compressed format if DirectShow filters exist to decode it.</span></span>
-   <span data-ttu-id="4135b-112">Auswirkung: bei einem Video werden alle 2D-Eingaben von Microsoft® DirectX® Transform-Objekt.</span><span class="sxs-lookup"><span data-stu-id="4135b-112">Effect: For video, any 2-D one-input Microsoft® DirectX® Transform object.</span></span> <span data-ttu-id="4135b-113">Für Audiodaten wird ein beliebiger DirectShow-audiowirkungs Filter verwendet.</span><span class="sxs-lookup"><span data-stu-id="4135b-113">For audio, any DirectShow audio effect filter.</span></span>
-   <span data-ttu-id="4135b-114">Übergang: bei einem Video handelt es sich um ein beliebiges 2D-DirectX-Transformations Objekt mit zwei Eingaben.</span><span class="sxs-lookup"><span data-stu-id="4135b-114">Transition: For video, any 2-D two-input DirectX Transform object.</span></span> <span data-ttu-id="4135b-115">Das Audioformat unterstützt keine Übergänge.</span><span class="sxs-lookup"><span data-stu-id="4135b-115">Audio does not support transitions.</span></span>

<span data-ttu-id="4135b-116">Gruppen, Kompositionen und Spuren verfügen über keine unter Objekte.</span><span class="sxs-lookup"><span data-stu-id="4135b-116">Groups, compositions, and tracks do not have subobjects.</span></span>

<span data-ttu-id="4135b-117">Der untergeordnete Zeiger wird von der Anwendung nicht direkt festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4135b-117">The application does not directly set the subobject pointer.</span></span> <span data-ttu-id="4135b-118">Bei Effekten und Übergängen Ruft die Anwendung die [**iamtimelineobj:: setsubobjectguid**](iamtimelineobj-setsubobjectguid.md) -Methode auf, um die GUID des unter Objekts anzugeben.</span><span class="sxs-lookup"><span data-stu-id="4135b-118">For effects and transitions, the application calls the [**IAMTimelineObj::SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) method to specify the GUID of the subobject.</span></span> <span data-ttu-id="4135b-119">Bei Quell Objekten Ruft eine Anwendung in der Regel [**iamtimelinesrc:: setmedianame**](iamtimelinesrc-setmedianame.md) auf, um den Namen einer Quelldatei anzugeben.</span><span class="sxs-lookup"><span data-stu-id="4135b-119">For source objects, an application typically calls the [**IAMTimelineSrc::SetMediaName**](iamtimelinesrc-setmedianame.md) to specify the name of a source file.</span></span> <span data-ttu-id="4135b-120">Die **setsubobjectguid** -Methode kann jedoch auch für Quell Objekte verwendet werden, um den Klassen Bezeichner (CLSID) eines Filters anzugeben.</span><span class="sxs-lookup"><span data-stu-id="4135b-120">However, the **SetSubObjectGUID** method can also be used for source objects, to specify the class identifier (CLSID) of a filter.</span></span>

<span data-ttu-id="4135b-121">Weitere Informationen finden Sie unter [Arbeiten mit Quellen](working-with-sources.md) und [Arbeiten mit Effekten und Übergängen](working-with-effects-and-transitions.md).</span><span class="sxs-lookup"><span data-stu-id="4135b-121">For more information, see [Working with Sources](working-with-sources.md) and [Working with Effects and Transitions](working-with-effects-and-transitions.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4135b-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4135b-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4135b-123">Übersicht über die Zeitachsen Komponenten</span><span class="sxs-lookup"><span data-stu-id="4135b-123">Overview of the Timeline Components</span></span>](overview-of-the-timeline-components.md)
</dt> </dl>

 

 



