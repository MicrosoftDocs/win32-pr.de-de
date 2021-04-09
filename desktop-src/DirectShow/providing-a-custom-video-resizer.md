---
description: Bereitstellen eines benutzerdefinierten Videos zum Ändern der Größe
ms.assetid: 4009f93f-cd50-440f-b943-7e3700e0e2cb
title: Bereitstellen eines benutzerdefinierten Videos zum Ändern der Größe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5247727cf16ef3c94a699db2907ff240b1d8a289
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124106"
---
# <a name="providing-a-custom-video-resizer"></a><span data-ttu-id="3f149-103">Bereitstellen eines benutzerdefinierten Videos zum Ändern der Größe</span><span class="sxs-lookup"><span data-stu-id="3f149-103">Providing a Custom Video Resizer</span></span>

<span data-ttu-id="3f149-104">\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]</span><span class="sxs-lookup"><span data-stu-id="3f149-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

> [!Note]  
> <span data-ttu-id="3f149-105">Für dieses Feature ist DirectX 9,0 oder höher erforderlich.</span><span class="sxs-lookup"><span data-stu-id="3f149-105">This feature requires DirectX 9.0 or later.</span></span>

 

<span data-ttu-id="3f149-106">Wenn [DirectShow-Bearbeitungs Dienste](directshow-editing-services.md) (von) die Größe eines Video Quell Clips ändern, ist das Standardverhalten eine *StretchBlt*, die schnell, aber nicht mit Antialiasing versehen ist.</span><span class="sxs-lookup"><span data-stu-id="3f149-106">When [DirectShow Editing Services](directshow-editing-services.md) (DES) resizes a video source clip, the default behavior is a *StretchBlt*, which is fast but not anti-aliased.</span></span> <span data-ttu-id="3f149-107">Sie können das Größen Änderungs Verhalten ändern, indem Sie eine benutzerdefinierte resialisierung als DirectShow-Transformations Filter implementieren.</span><span class="sxs-lookup"><span data-stu-id="3f149-107">You can change the resizing behavior by implementing a custom resizer as a DirectShow transform filter.</span></span> <span data-ttu-id="3f149-108">Der Filter muss die Schnittstelle [**iresize**](iresize.md) verfügbar machen, die es ermöglicht, die Videogröße für die Eingabe und die Ausgabe anzugeben.</span><span class="sxs-lookup"><span data-stu-id="3f149-108">The filter must expose the [**IResize**](iresize.md) interface, which enables DES to specify the input and output video size.</span></span> <span data-ttu-id="3f149-109">Weitere Informationen zum Schreiben eines Transformations Filters finden Sie unter [Schreiben von Transformations Filtern](writing-transform-filters.md).</span><span class="sxs-lookup"><span data-stu-id="3f149-109">For information about writing a transform filter, see [Writing Transform Filters](writing-transform-filters.md).</span></span> <span data-ttu-id="3f149-110">Die **ctransformfilter** -Basisklasse wird als Ausgangspunkt empfohlen.</span><span class="sxs-lookup"><span data-stu-id="3f149-110">The **CTransformFilter** base class is recommended as the starting point.</span></span> <span data-ttu-id="3f149-111">Beachten Sie beim Implementieren des Filters Folgendes:</span><span class="sxs-lookup"><span data-stu-id="3f149-111">When you implement the filter, note the following:</span></span>

-   <span data-ttu-id="3f149-112">Unterstützung der **iresize** -Schnittstelle für den Filter (nicht die Pins).</span><span class="sxs-lookup"><span data-stu-id="3f149-112">Support the **IResize** interface on the filter (not the pins).</span></span>
-   <span data-ttu-id="3f149-113">Der Filter sollte nur [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) -Formate ( \_ Video Info Format) akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="3f149-113">The filter should accept only [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) formats (FORMAT\_VideoInfo).</span></span> <span data-ttu-id="3f149-114">Ablehnen anderer Format Typen.</span><span class="sxs-lookup"><span data-stu-id="3f149-114">Reject other format types.</span></span>
-   <span data-ttu-id="3f149-115">Das Videoformat von des kann ein beliebiger nicht komprimierter RGB-Typ sein, einschließlich 32-Bit-RGB mit Alpha (mediasubtype \_ ARGB32).</span><span class="sxs-lookup"><span data-stu-id="3f149-115">The video format from DES may be any uncompressed RGB type, including 32-bit RGB with alpha (MEDIASUBTYPE\_ARGB32).</span></span> <span data-ttu-id="3f149-116">Der Filter kann Formate mit **biheight** < 0 (null) auf sichere Weise ablehnen.</span><span class="sxs-lookup"><span data-stu-id="3f149-116">Your filter can safely reject formats with **biHeight** < 0.</span></span>
-   <span data-ttu-id="3f149-117">Bevor die Renderingengine die Ausgabepin des Filters verbindet, wird [**iresize::p UT \_ mediaType**](iresize-put-mediatype.md) aufgerufen, um den Ausgabetyp festzulegen.</span><span class="sxs-lookup"><span data-stu-id="3f149-117">Before the Render Engine connects the filter's output pin, it calls [**IResize::put\_MediaType**](iresize-put-mediatype.md) to set the output type.</span></span> <span data-ttu-id="3f149-118">Es kann auch " [**iresize::p UT \_ size**](iresize-put-size.md) " aufgerufen werden, um die Ausgabegröße anzupassen.</span><span class="sxs-lookup"><span data-stu-id="3f149-118">It may also call [**IResize::put\_Size**](iresize-put-size.md) to adjust the output size.</span></span> <span data-ttu-id="3f149-119">Diese beiden Methoden können beliebig oft in beliebiger Reihenfolge aufgerufen werden, bevor die Ausgabe-PIN verbunden wird.</span><span class="sxs-lookup"><span data-stu-id="3f149-119">It can call these two methods in any order, any number of times, before it connects the output pin.</span></span>
-   <span data-ttu-id="3f149-120">Nachdem die Renderingengine eine Verbindung mit der Ausgabe-PIN hergestellt hat, kann Sie die **Put- \_ Größe** erneut</span><span class="sxs-lookup"><span data-stu-id="3f149-120">After the Render Engine connects the output pin, it might call **put\_Size** again.</span></span> <span data-ttu-id="3f149-121">Der Filter für die Größenänderung sollte die Ausgabe-PIN erneut mit der neuen Größe verbinden.</span><span class="sxs-lookup"><span data-stu-id="3f149-121">The resizer filter should reconnect its output pin with the new size.</span></span>
-   <span data-ttu-id="3f149-122">Strecken Sie in der [**ctransformfilter:: Transform**](ctransformfilter-transform.md) -Methode des Filters das Eingabe Video auf die Ausgabegröße.</span><span class="sxs-lookup"><span data-stu-id="3f149-122">Inside the filter's [**CTransformFilter::Transform**](ctransformfilter-transform.md) method, stretch the input video to the output size.</span></span>
-   <span data-ttu-id="3f149-123">Der Filter sollte niemals das Diskontinuität-Flag für das Ausgabe Beispiel festlegen oder einen Medientyp an das Ausgabe Beispiel anfügen.</span><span class="sxs-lookup"><span data-stu-id="3f149-123">Your filter should never set the discontinuity flag on the output sample, or attach a media type to the output sample.</span></span>
-   <span data-ttu-id="3f149-124">Implementieren Sie die **IPersistStream** -Schnittstelle, um den Status des Filters in einer GraphEdit-Datei (grf-Datei) zu speichern.</span><span class="sxs-lookup"><span data-stu-id="3f149-124">To save the filter's state in a GraphEdit (.grf) file, implement the **IPersistStream** interface.</span></span> <span data-ttu-id="3f149-125">(Dies ist optional, aber zum Testen hilfreich.)</span><span class="sxs-lookup"><span data-stu-id="3f149-125">(This is optional, but useful for testing.)</span></span>

<span data-ttu-id="3f149-126">Um den Filter zum Ändern der Größe zu verwenden, muss der Filter als COM-Objekt im System des Benutzers registriert werden.</span><span class="sxs-lookup"><span data-stu-id="3f149-126">To use the resizer filter, the filter must be registered as a COM object on the user's system.</span></span> <span data-ttu-id="3f149-127">Bevor die Anwendung das Videoprojekt rendert, Fragen Sie die Rendering-Engine nach der [**IRenderEngine2**](irenderengine2.md) -Schnittstelle ab, und nennen Sie [**IRenderEngine2:: setresizerguid**](irenderengine2-setresizerguid.md) mit der CLSID des resizerfilterfilters.</span><span class="sxs-lookup"><span data-stu-id="3f149-127">Before the application renders the video project, query the Render Engine for the [**IRenderEngine2**](irenderengine2.md) interface and call [**IRenderEngine2::SetResizerGUID**](irenderengine2-setresizerguid.md) with the CLSID of the resizer filter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3f149-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3f149-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3f149-129">Rendern eines Projekts</span><span class="sxs-lookup"><span data-stu-id="3f149-129">Rendering a Project</span></span>](rendering-a-project.md)
</dt> </dl>

 

 



