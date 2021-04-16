---
description: Nicht quadratische Vermischung
ms.assetid: 8d27a921-5638-43ac-807d-e3bd7b9b2de8
title: Nicht quadratische Vermischung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79d23f423f0dbe19f1ff0ba35c44f8fd2f8732bc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522051"
---
# <a name="non-square-mixing"></a><span data-ttu-id="fa9ab-103">Nicht quadratische Vermischung</span><span class="sxs-lookup"><span data-stu-id="fa9ab-103">Non-Square Mixing</span></span>

<span data-ttu-id="fa9ab-104">Dieses Thema gilt für Windows XP Service Pack 2 oder höher.</span><span class="sxs-lookup"><span data-stu-id="fa9ab-104">This topic applies to Windows XP Service Pack 2 or later.</span></span>

<span data-ttu-id="fa9ab-105">Wenn VMR-9 zwei oder mehr Streams kombiniert, gibt es zwei Punkte, an denen die Skalierung stattfinden kann: Wenn der Mixer die Eingabestreams zusammensetzt und der zuordnerpresenter das zusammengesetzte Bild rendert.</span><span class="sxs-lookup"><span data-stu-id="fa9ab-105">When the VMR-9 mixes two or more streams, there are two points where scaling can occur: When the mixer composites the input streams, and when the allocator-presenter renders the composited image.</span></span>

![VMR-Mischungs Vorgänge](images/vmr-nonsquare-mixing.png)

<span data-ttu-id="fa9ab-107">In früheren Versionen von VMR-9 wurden die Eingabedaten Ströme stets mithilfe eines quadratischen (1:1) Pixel Seitenverhältnisses (par) zusammengesetzt, auch wenn nur ein einzelner Videostream vorhanden war.</span><span class="sxs-lookup"><span data-stu-id="fa9ab-107">Previous versions of the VMR-9 always composited the input streams using a square (1:1) pixel aspect ratio (PAR), even when there was only a single video stream.</span></span> <span data-ttu-id="fa9ab-108">Wenn der Eingabedaten Strom nicht quadratische Pixel enthielt, verursachte dies einen unnötigen Skalierungs Vorgang.</span><span class="sxs-lookup"><span data-stu-id="fa9ab-108">If the input stream had non-square pixels, this caused an unnecessary scaling operation.</span></span> <span data-ttu-id="fa9ab-109">Die Skalierung sollte so weit wie möglich vermieden werden, da Sie die endgültige Bildqualität beeinträchtigt.</span><span class="sxs-lookup"><span data-stu-id="fa9ab-109">Scaling should be avoided as much as possible, of course, because it degrades the final image quality.</span></span>

<span data-ttu-id="fa9ab-110">Ab Windows XP Service Pack 2 unterstützt VMR-9 zwei verschiedene Möglichkeiten, um das Problem der doppelten Skalierung zu vermeiden:</span><span class="sxs-lookup"><span data-stu-id="fa9ab-110">Starting in Windows XP Service Pack 2, the VMR-9 supports two different ways to avoid the problem of double scaling:</span></span>

-   <span data-ttu-id="fa9ab-111">Implementieren Sie einen benutzerdefinierten Zuweiser und unterstützen Sie die [**IVMRSurfaceAllocatorEx9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatorex9) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="fa9ab-111">Implement a custom allocator-presenter and support the [**IVMRSurfaceAllocatorEx9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatorex9) interface.</span></span>
-   <span data-ttu-id="fa9ab-112">Verwenden Sie den nicht quadratischen Mischungs Modus.</span><span class="sxs-lookup"><span data-stu-id="fa9ab-112">Use non-square mixing mode.</span></span>

<span data-ttu-id="fa9ab-113">In diesem Abschnitt wird der nicht quadratische Mischungs Modus beschrieben.</span><span class="sxs-lookup"><span data-stu-id="fa9ab-113">This section describes non-square mixing mode.</span></span> <span data-ttu-id="fa9ab-114">Beide Verfahren können von Anwendungen kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="fa9ab-114">Applications can combine both techniques.</span></span>

<span data-ttu-id="fa9ab-115">**Funktionsweise der nicht quadratischen Vermischung**</span><span class="sxs-lookup"><span data-stu-id="fa9ab-115">**How Non-Square Mixing Works**</span></span>

<span data-ttu-id="fa9ab-116">Im nicht quadratischen Mischungs Modus wählt VMR-9 einen Eingabedaten Strom als Zielgröße und par aus.</span><span class="sxs-lookup"><span data-stu-id="fa9ab-116">In non-square mixing mode, the VMR-9 selects one input stream to be the target size and PAR.</span></span> <span data-ttu-id="fa9ab-117">Der Mixer von VMR skaliert das Video nicht aus diesem Stream oder aus anderen Streams mit der gleichen Bildgröße und dem gleichen Wert.</span><span class="sxs-lookup"><span data-stu-id="fa9ab-117">The VMR's mixer does not scale the video from that stream or from any other streams with the same image size and PAR.</span></span> <span data-ttu-id="fa9ab-118">Datenströme mit einer anderen Größe oder einem anderen Seitenverhältnis werden so skaliert, dass Sie mit der Ziel Größe übereinstimmen, die der Größe des endgültigen Ausgabe Bilds entspricht.</span><span class="sxs-lookup"><span data-stu-id="fa9ab-118">Streams with a different size or aspect ratio are scaled to match the target PAR and letterboxed to fit the final output image size.</span></span>

<span data-ttu-id="fa9ab-119">Die Auswahl der Streams hängt vom aktuellen Mischungs Modus ab:</span><span class="sxs-lookup"><span data-stu-id="fa9ab-119">The choice of streams depends on the current mixing mode:</span></span>

-   <span data-ttu-id="fa9ab-120">Der YUV-Mischungs Modus ist auf einen Videodaten Strom auf Pin 0 beschränkt.</span><span class="sxs-lookup"><span data-stu-id="fa9ab-120">YUV mixing mode is restricted to one video stream on pin 0.</span></span> <span data-ttu-id="fa9ab-121">(Die anderen Pins können über untergeordnete oder geschlossene Beschriftungs Datenströme verfügen.) Daher wählt VMR-9 immer Pin 0 für die zielbildgröße und-Größe aus.</span><span class="sxs-lookup"><span data-stu-id="fa9ab-121">(The other pins may have subpicture or closed caption streams.) Therefore, the VMR-9 always selects pin 0 for the target image size and PAR.</span></span>
-   <span data-ttu-id="fa9ab-122">Im RGB-Mischungs Modus wählt der VMR den Stream mit der größten Bildgröße aus.</span><span class="sxs-lookup"><span data-stu-id="fa9ab-122">In RGB mixing mode, the VMR selects the stream with the largest image size.</span></span> <span data-ttu-id="fa9ab-123">Wenn mehr als ein Wert vorhanden ist, wählt er den Wert mit der höchsten z-Reihenfolge aus. und wenn immer noch eine Verknüpfung vorhanden ist, wird der Stream mit der niedrigsten PIN-Nummer ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="fa9ab-123">If there is more than one, it selects the one with the highest z-order; and if there is still a tie, it selects the stream with the lowest pin number.</span></span>

<span data-ttu-id="fa9ab-124">**Beispiele für Vorgänge**</span><span class="sxs-lookup"><span data-stu-id="fa9ab-124">**Examples of Operation**</span></span>

<span data-ttu-id="fa9ab-125">**1. Beispiel:**</span><span class="sxs-lookup"><span data-stu-id="fa9ab-125">**Example 1.**</span></span> <span data-ttu-id="fa9ab-126">Stream 0 ist 720 x 480 Pixel mit einem Bildseiten Verhältnis von 16:9.</span><span class="sxs-lookup"><span data-stu-id="fa9ab-126">Stream 0 is 720 x 480 pixels with a picture aspect ratio of 16:9.</span></span> <span data-ttu-id="fa9ab-127">Stream 1 ist ein 640 x 480 Pixel mit einem Bildseiten Verhältnis von 4:3.</span><span class="sxs-lookup"><span data-stu-id="fa9ab-127">Stream 1 is a 640 x 480 pixels with a picture aspect ratio of 4:3.</span></span>

<span data-ttu-id="fa9ab-128">In diesem Beispiel hat Stream 0 die größte Bildgröße. Daher wählt VMR diesen Stream aus, unabhängig vom RGB-Mischungs Modus oder dem yub-Mischungs Modus.</span><span class="sxs-lookup"><span data-stu-id="fa9ab-128">In this example, stream 0 has the largest image size, so the VMR chooses this stream, regardless of RGB mixing mode or YUB mixing mode.</span></span> <span data-ttu-id="fa9ab-129">Die par ist 32:27 (16:9/720:480). das bedeutet, dass das Bild horizontal durch dieses Verhältnis gestreckt werden muss, um das richtige 16:9 Bildseiten Verhältnis zu schaffen.</span><span class="sxs-lookup"><span data-stu-id="fa9ab-129">The PAR is 32:27 (16:9 / 720:480), meaning the image must be stretched horizontally by this ratio to produce the correct 16:9 picture aspect ratio.</span></span>

<span data-ttu-id="fa9ab-130">Um dem Zielwert zu entsprechen, skaliert der VMR-Mixer den Stream 1 mit dem umgekehrten Verhältnis (27:32), was zu einem 540 x 480-Bild führt.</span><span class="sxs-lookup"><span data-stu-id="fa9ab-130">To match the target PAR, the VMR mixer scales stream 1 by the inverse ratio (27:32), resulting in a 540 x 480 image.</span></span> <span data-ttu-id="fa9ab-131">Die beiden Streams werden dann auf eine Oberfläche zusammengesetzt.</span><span class="sxs-lookup"><span data-stu-id="fa9ab-131">The two streams are then composited onto one surface.</span></span> <span data-ttu-id="fa9ab-132">Um das resultierende Bild ordnungsgemäß anzuzeigen, muss der zuordnerpräsentator das Bild horizontal Strecken, um das Seitenverhältnis von 16:9 Bild anzupassen.</span><span class="sxs-lookup"><span data-stu-id="fa9ab-132">To display the resulting image correctly, the allocator presenter must stretch the image horizontally to fit the 16:9 picture aspect ratio.</span></span>

![Beispiel 1.](images/vmr-nonsquare-mixing2.png)

<span data-ttu-id="fa9ab-134">**2. Beispiel:**</span><span class="sxs-lookup"><span data-stu-id="fa9ab-134">**Example 2.**</span></span> <span data-ttu-id="fa9ab-135">Stream 0 ist 720 x 480 Pixel mit einem Bildseiten Verhältnis von 16:9.</span><span class="sxs-lookup"><span data-stu-id="fa9ab-135">Stream 0 is 720 x 480 pixels with a picture aspect ratio of 16:9.</span></span> <span data-ttu-id="fa9ab-136">Stream 1 ist ein 1024 x 768 Pixel mit einem Bildseiten Verhältnis von 4:3.</span><span class="sxs-lookup"><span data-stu-id="fa9ab-136">Stream 1 is a 1024 x 768 pixels with a picture aspect ratio of 4:3.</span></span>

<span data-ttu-id="fa9ab-137">Wenn VMR-9 den YUV-Mischungs Modus verwendet, wählt er immer Stream 0 aus.</span><span class="sxs-lookup"><span data-stu-id="fa9ab-137">If the VMR-9 is using YUV mixing mode, it always selects stream 0.</span></span> <span data-ttu-id="fa9ab-138">Daher wird der Stream 1 auf 540 x 480 Pixel gestreckt, sodass er mit dem par von Stream 0 übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="fa9ab-138">Therefore, it stretches stream 1 to 540 x 480 pixels, to match the PAR of stream 0.</span></span>

<span data-ttu-id="fa9ab-139">Wenn VMR-9 den RGB-Mischungs Modus verwendet, wählt er Stream 1 als Ziel aus, da dieser Stream die größte Bildgröße aufweist.</span><span class="sxs-lookup"><span data-stu-id="fa9ab-139">If the VMR-9 is using RGB mixing mode, it selects stream 1 as the target, because that stream has the largest image size.</span></span> <span data-ttu-id="fa9ab-140">Der Stream 0 wird auf eine Bildgröße von 1024 x 576 Pixel gestreckt.</span><span class="sxs-lookup"><span data-stu-id="fa9ab-140">It stretches stream 0 to an image size of 1024 x 576 pixels.</span></span> <span data-ttu-id="fa9ab-141">Beachten Sie, dass das zusammengesetzte Image in diesem Fall ein par von 1:1 hat, sodass der Zuordnungs-Presenter nicht für nicht quadratische Pixel korrekt ist.</span><span class="sxs-lookup"><span data-stu-id="fa9ab-141">Note that in this case, the composited image has a PAR of 1:1, so the allocator-presenter does not have to correct for non-square pixels.</span></span> <span data-ttu-id="fa9ab-142">(Möglicherweise muss das Video nach wie vor für das Ziel Rechteck gestreckt werden.)</span><span class="sxs-lookup"><span data-stu-id="fa9ab-142">(It might still need to stretch the video to account for the destination rectangle.)</span></span>

<span data-ttu-id="fa9ab-143">**Verwenden des nicht quadratischen Mischungs Modus**</span><span class="sxs-lookup"><span data-stu-id="fa9ab-143">**Using Non-Square Mixing Mode**</span></span>

<span data-ttu-id="fa9ab-144">Der nicht quadratische Mischungs Modus wird empfohlen, wenn eine der folgenden Bedingungen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="fa9ab-144">Non-square mixing mode is recommended if either of the following conditions are true:</span></span>

-   <span data-ttu-id="fa9ab-145">Die Anwendung sendet nie mehr als einen Videodaten Strom an VMR-9.</span><span class="sxs-lookup"><span data-stu-id="fa9ab-145">Your application never sends more than one video stream to the VMR-9.</span></span>
-   <span data-ttu-id="fa9ab-146">Ihre Anwendung rendert DVD-, Fernseh-oder MS-DVR-Dateien.</span><span class="sxs-lookup"><span data-stu-id="fa9ab-146">Your application renders DVD, television, or ms-dvr files.</span></span> <span data-ttu-id="fa9ab-147">Sie sollten in diesem Fall auch den YUV-Mischungs Modus verwenden, wenn er von der Grafikhardware unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="fa9ab-147">You should also use YUV mixing mode in this case, if the graphics hardware supports it.</span></span>

<span data-ttu-id="fa9ab-148">Wenn Ihre Anwendung mehrere Videostreams mit unterschiedlichen Bildgrößen oder Pixel Seitenverhältnissen kombiniert, wird der standardmäßige quadratische Mischungs Modus empfohlen.</span><span class="sxs-lookup"><span data-stu-id="fa9ab-148">If your application mixes multiple video streams that may have varying image sizes or pixel aspect ratios, the default square mixing mode is recommended.</span></span>

<span data-ttu-id="fa9ab-149">Um den nicht quadratischen Mischungs Modus zu konfigurieren, muss das Filter Diagramm angehalten werden, und alle Eingabe Pins sind auf VMR-9 getrennt.</span><span class="sxs-lookup"><span data-stu-id="fa9ab-149">To configure non-square mixing mode, the filter graph must be stopped and all input pins disconnected on the VMR-9.</span></span> <span data-ttu-id="fa9ab-150">Rufen Sie dann [**IVMRMixerControl9:: setmixingprefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs) mit dem MixerPref9 \_ nonsquaremischungsflag auf:</span><span class="sxs-lookup"><span data-stu-id="fa9ab-150">Then call [**IVMRMixerControl9::SetMixingPrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs) with the MixerPref9\_NonSquareMixing flag:</span></span>


```C++
DWORD dwPrefs;
pMixControl->GetMixingPrefs(&dwPrefs);  
dwPrefs |= MixerPref9_NonSquareMixing;
pMixControl->SetMixingPrefs(dwPrefs);
```



> [!Note]  
> <span data-ttu-id="fa9ab-151">Wenn Sie das MixerPref9 \_ nonsquaremischungsflag mit dem MixerPref9 \_ arsexory-Flag kombinieren, ignoriert VMR-9 das MixerPref9 \_ arsexory-Flag.</span><span class="sxs-lookup"><span data-stu-id="fa9ab-151">If you combine the MixerPref9\_NonSquareMixing flag with the MixerPref9\_ARAdjustXorY flag, the VMR-9 ignores the MixerPref9\_ARAdjustXorY flag.</span></span>

 

<span data-ttu-id="fa9ab-152">Wenn Ihre Anwendung einen benutzerdefinierten zuordnerpräsentator mit einem nicht quadratischen Mischungs Modus verwendet, beachten Sie, dass das zusammengesetzte Bild möglicherweise eine nicht quadratische par-ID hat.</span><span class="sxs-lookup"><span data-stu-id="fa9ab-152">If your application uses a custom allocator-presenter with non-square mixing mode, be aware that the composited image may have a non-square PAR.</span></span> <span data-ttu-id="fa9ab-153">Der zuordnerpräsentator muss das Bild auf einen quadratischen (1:1) par skalieren.</span><span class="sxs-lookup"><span data-stu-id="fa9ab-153">The allocator-presenter must scale the image to a square (1:1) PAR.</span></span>

<span data-ttu-id="fa9ab-154">**Statische Bitmaps**</span><span class="sxs-lookup"><span data-stu-id="fa9ab-154">**Static Bitmaps**</span></span>

<span data-ttu-id="fa9ab-155">Wenn Sie die [**IVMRMixerBitmap9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9) -Schnittstelle verwenden, um eine statische Bitmap in das Video zu mischen, sollten Sie die Bitmap als zweiten Videostream für den VMR-Mischungs Modus in Erwägung ziehen.</span><span class="sxs-lookup"><span data-stu-id="fa9ab-155">If you use the [**IVMRMixerBitmap9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9) interface to blend a static bitmap onto the video, you should consider the bitmap to be a second video stream for purposes of the VMR mixing mode.</span></span>

<span data-ttu-id="fa9ab-156">Die Bitmap wird von VMR als identisch mit dem Ziel behandelt.</span><span class="sxs-lookup"><span data-stu-id="fa9ab-156">The VMR treats the bitmap as having the same PAR as the target.</span></span> <span data-ttu-id="fa9ab-157">Die Bitmap wird nicht skaliert, um das Pixel Seitenverhältnis des Ziels anzupassen.</span><span class="sxs-lookup"><span data-stu-id="fa9ab-157">It does not scale the bitmap to adjust for the target's pixel aspect ratio.</span></span> <span data-ttu-id="fa9ab-158">In der Standardkonfiguration von VMR hat das Ziel eine 1:1-Entsprechung, die den meisten Bitmaps entspricht.</span><span class="sxs-lookup"><span data-stu-id="fa9ab-158">In the VMR's default configuration, the target has a 1:1 PAR, which matches most bitmaps.</span></span> <span data-ttu-id="fa9ab-159">Im nicht quadratischen Mischungs Modus hat das Ziel möglicherweise nicht eckige Pixel.</span><span class="sxs-lookup"><span data-stu-id="fa9ab-159">In non-square mixing mode, the target might have non-square pixels.</span></span> <span data-ttu-id="fa9ab-160">Um sicherzustellen, dass die Bitmap ordnungsgemäß angezeigt wird, sollte die Anwendung ein Bild bereitstellen, dessen par der Ziel-par entspricht.</span><span class="sxs-lookup"><span data-stu-id="fa9ab-160">To ensure that the bitmap is displayed correctly, the application should supply an image whose PAR matches the target PAR.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fa9ab-161">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fa9ab-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa9ab-162">Verwenden des VMR-Mischungs Modus</span><span class="sxs-lookup"><span data-stu-id="fa9ab-162">Using VMR Mixing Mode</span></span>](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



