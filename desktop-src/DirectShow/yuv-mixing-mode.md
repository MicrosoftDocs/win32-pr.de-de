---
description: YUV-Mischungs Modus
ms.assetid: 296b1d96-1824-4000-8bec-158925555177
title: YUV-Mischungs Modus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faf4ca6b1ba5317145c410d6e5b899c7cf264f82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867484"
---
# <a name="yuv-mixing-mode"></a><span data-ttu-id="d6fc5-103">YUV-Mischungs Modus</span><span class="sxs-lookup"><span data-stu-id="d6fc5-103">YUV Mixing Mode</span></span>

<span data-ttu-id="d6fc5-104">Dieses Thema gilt für Windows XP Service Pack 2 oder höher.</span><span class="sxs-lookup"><span data-stu-id="d6fc5-104">This topic applies to Windows XP Service Pack 2 or later.</span></span>

<span data-ttu-id="d6fc5-105">Ab Windows XP Service Pack 2 unterstützt VMR einen Mischungs Modus mit dem Namen YUV-Mischungs Modus.</span><span class="sxs-lookup"><span data-stu-id="d6fc5-105">Starting in Windows XP Service Pack 2, the VMR supports a mixing mode called YUV mixing mode.</span></span> <span data-ttu-id="d6fc5-106">Dieser Modus ist am nützlichsten für erweiterte TV-oder DVD-Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="d6fc5-106">This mode is most useful for advanced TV or DVD applications.</span></span> <span data-ttu-id="d6fc5-107">Es wird ein Teil der Leistungsfähigkeit des VMR-Mischers eingesetzt, um eine bessere Leistung auf Low-End-Grafikhardware zu erzielen</span><span class="sxs-lookup"><span data-stu-id="d6fc5-107">It trades some of the power of the VMR mixer for better performance on low end graphics hardware that uses a unified memory architecture design.</span></span> <span data-ttu-id="d6fc5-108">Der YUV-Mischungs Modus wird sowohl für VMR-7 als auch für VMR-9 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d6fc5-108">YUV mixing mode is supported on both the VMR-7 and VMR-9.</span></span>

<span data-ttu-id="d6fc5-109">**Vorteile**</span><span class="sxs-lookup"><span data-stu-id="d6fc5-109">**Advantages**</span></span>

<span data-ttu-id="d6fc5-110">Der YUV-Mischungs Modus bietet mehrere Vorteile im Zusammenhang mit der Renderingleistung im ursprünglichen RGB-Mischungs Modus, der von der VMR</span><span class="sxs-lookup"><span data-stu-id="d6fc5-110">YUV mixing mode has several advantages relating to rendering performance over the original RGB mixing mode supported by the VMR:</span></span>

-   <span data-ttu-id="d6fc5-111">Wenn sich der VMR im YUV-Mischungs Modus befindet, werden alle Vorgänge zum Aufheben der Interlacing-und Videodaten Strom Komposition in einem YUV-Farbraum ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d6fc5-111">When the VMR is in YUV mixing mode, all de-interlacing and video stream composition operations are performed in YUV color space.</span></span> <span data-ttu-id="d6fc5-112">YUV-Oberflächen erfordern normalerweise zwischen 50% und 60% weniger Speicherbandbreite als äquivalente RGB-Oberflächen.</span><span class="sxs-lookup"><span data-stu-id="d6fc5-112">YUV surfaces typically require from 50% to 60% less memory bandwidth than equivalent RGB surfaces.</span></span>
-   <span data-ttu-id="d6fc5-113">Die Deinterlacing-und Datenstrom Komposition erfolgt durch einen einzelnen-Befehl des Grafik Treibers.</span><span class="sxs-lookup"><span data-stu-id="d6fc5-113">The deinterlacing and stream composition are performed by a single call to the graphics driver.</span></span> <span data-ttu-id="d6fc5-114">Der Treiber kann die multitexturierungsfunktionen der Grafikhardware verwenden, was zu zusätzlichen Einsparungen bei der Speicherbandbreite führt.</span><span class="sxs-lookup"><span data-stu-id="d6fc5-114">The driver can use the graphics hardware's multi-texturing capabilities, resulting in additional memory bandwidth savings.</span></span>

<span data-ttu-id="d6fc5-115">Obwohl jede Video Anwendung den YUV-Mischungs Modus verwenden kann, ist Sie in erster Linie für zwei Arten von Videowiedergabe Anwendungen gedacht:</span><span class="sxs-lookup"><span data-stu-id="d6fc5-115">Although any video application can use YUV mixing mode, it is primarily intended for two types of video playback application:</span></span>

1.  <span data-ttu-id="d6fc5-116">TV-Anwendungen, die Untertitel oder Teletext anzeigen.</span><span class="sxs-lookup"><span data-stu-id="d6fc5-116">TV applications that display closed captions or teletext.</span></span>
2.  <span data-ttu-id="d6fc5-117">DVD-Anwendungen zeigen DVD-subbilddaten oder Untertitel an.</span><span class="sxs-lookup"><span data-stu-id="d6fc5-117">DVD applications display DVD subpicture data or closed captions.</span></span>

<span data-ttu-id="d6fc5-118">**Einschränkungen**</span><span class="sxs-lookup"><span data-stu-id="d6fc5-118">**Restrictions**</span></span>

<span data-ttu-id="d6fc5-119">Eine Reihe von Einschränkungen werden von der VMR erzwungen, wenn Sie in den YUV-Mischungs Modus versetzt wird:</span><span class="sxs-lookup"><span data-stu-id="d6fc5-119">A number of restrictions are enforced by the VMR when it is put into YUV mixing mode:</span></span>

-   <span data-ttu-id="d6fc5-120">Stream 0 (der mit der Eingabe-PIN "0" verbundene Stream) kann progressiv oder Zeilen Sprung sein. alle anderen Streams müssen progressiv sein.</span><span class="sxs-lookup"><span data-stu-id="d6fc5-120">Stream 0 (the stream connected to Input Pin 0) can be progressive or interlaced; all other streams must be progressive.</span></span>
-   <span data-ttu-id="d6fc5-121">GUID \_ NULL (Weave-Modus) ist für Stream 0 nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="d6fc5-121">GUID\_NULL (weave mode) is not allowed for stream 0.</span></span>
-   <span data-ttu-id="d6fc5-122">Das Debuggen "deinterlacepref" \_ kann nicht als Fall Back Modus verwendet werden, da dadurch verhindert werden kann, dass ein deinterlace-Gerät erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="d6fc5-122">DeinterlacePref\_Weave cannot be used as a fallback mode because this could prevent a de-interlace device from being created.</span></span> <span data-ttu-id="d6fc5-123">Der YUV-Mischungs Modus erfordert ein Deinterlacing-Gerät, auch wenn das eingehende Video nicht mit Zeilen Sprung verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="d6fc5-123">YUV mixing mode requires a deinterlace device even if the incoming video is not interlaced.</span></span>
-   <span data-ttu-id="d6fc5-124">Es können keine Änderungen an dem planaren Alpha-Wert vorgenommen werden, der mit den einzelnen VMR-Eingabedaten strömen verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="d6fc5-124">No changes can be made to the planar alpha value associated with each VMR input stream.</span></span>
-   <span data-ttu-id="d6fc5-125">Der Benutzer kann die Z-Reihenfolge der verbundenen Videostreams nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="d6fc5-125">The user cannot alter the Z-order of the connected video streams.</span></span> <span data-ttu-id="d6fc5-126">Die standardmäßige Z-Reihenfolge wird aus der PIN-Reihenfolge entnommen.</span><span class="sxs-lookup"><span data-stu-id="d6fc5-126">The default Z-order is taken from the pin order.</span></span>
-   <span data-ttu-id="d6fc5-127">Die Farb Erstellung wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d6fc5-127">Color keying is not supported.</span></span>
-   <span data-ttu-id="d6fc5-128">Die Eingabe-PIN 0 muss den Videostream erhalten.</span><span class="sxs-lookup"><span data-stu-id="d6fc5-128">Input pin 0 must receive the video stream.</span></span>
-   <span data-ttu-id="d6fc5-129">Die anderen Eingabe Pins können nur Video-substreamdaten empfangen, z. b. DVD-Untertitel, Untertitel oder Teletext.</span><span class="sxs-lookup"><span data-stu-id="d6fc5-129">The other inputs pins can only receive video sub-stream data such as DVD sub-picture, closed captions or teletext.</span></span>
-   <span data-ttu-id="d6fc5-130">Die anderen Eingabe Pins können nur Pixel übergreifende Alpha YUV-Formate wie z. b. ayuv, AI44 und IA44 akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="d6fc5-130">The other inputs pins can only accept per-pixel alpha YUV formats, such as AYUV, AI44 and IA44.</span></span>
-   <span data-ttu-id="d6fc5-131">Keiner der Eingabe Pins von VMR kann RGB-Formate annehmen.</span><span class="sxs-lookup"><span data-stu-id="d6fc5-131">None of the VMR's input pins can accept any RGB formats.</span></span>
-   <span data-ttu-id="d6fc5-132">Die von der Anwendung bereitgestellten Bitmap-Bilder können nicht mehr mit dem Video kombiniert werden, bevor die Darstellung der Anzeige angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d6fc5-132">Application supplied bitmap images can no longer be combined with the video prior to presentation to the display.</span></span>
-   <span data-ttu-id="d6fc5-133">Einzelne untergeordnete Datenströme können nicht horizontal oder vertikal mithilfe der Funktionen des VMR-Mischers "Ausgabe Rechteck" invertiert werden.</span><span class="sxs-lookup"><span data-stu-id="d6fc5-133">Individual sub-streams cannot be inverted horizontally or vertically using the VMR's mixer "output rectangle" functions.</span></span> <span data-ttu-id="d6fc5-134">Die Neupositionierung und Neudimensionierung von Datenströmen wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d6fc5-134">"Normal" stream re-positioning and re-sizing is supported.</span></span>
-   <span data-ttu-id="d6fc5-135">Die Hintergrundfarbe für das Mischen (angegeben durch [**ivmrmixercontrol:: setbackgroundclr**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setbackgroundclr)) ist nach wie vor im RGB-Farbraum angegeben, ebenso wie im RGB-Mischungs Modus.</span><span class="sxs-lookup"><span data-stu-id="d6fc5-135">The mixing background color (specified by [**IVMRMixerControl::SetBackgroundClr**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setbackgroundclr)) is still specified in the RGB color space, just as in RGB mixing mode.</span></span>

<span data-ttu-id="d6fc5-136">**Configuration**</span><span class="sxs-lookup"><span data-stu-id="d6fc5-136">**Configuration**</span></span>

<span data-ttu-id="d6fc5-137">Anwendungen müssen VMR explizit so konfigurieren, dass Sie den YUV-Mischungs Modus nutzen. der ursprüngliche RGB-Mischungs Modus bleibt der standardmäßige Mischungs Modus.</span><span class="sxs-lookup"><span data-stu-id="d6fc5-137">Applications must explicitly configure the VMR to take advantage of YUV mixing mode; the original RGB mixing mode remains the default mixing mode.</span></span> <span data-ttu-id="d6fc5-138">Um den YUV-Mischungs Modus in VMR-7 zu aktivieren, rufen Sie [**ivmrmixercontrol:: setmixingprefs**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setoutputrect) mit dem Flag mixerpref \_ rendertargetyuv auf.</span><span class="sxs-lookup"><span data-stu-id="d6fc5-138">To enable YUV mixing mode in the VMR-7, call [**IVMRMixerControl::SetMixingPrefs**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setoutputrect) with the MixerPref\_RenderTargetYUV flag.</span></span> <span data-ttu-id="d6fc5-139">Dieser Rückruf muss erfolgen, bevor eine der VMR-Eingabe Pins verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="d6fc5-139">This call must be made before any of the VMR's input pins are connected.</span></span> <span data-ttu-id="d6fc5-140">Um den YUV-Mischungs Modus in VMR-9 zu aktivieren, rufen Sie [**IVMRMixerControl9:: setmixingprefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs) mit dem MixerPref9 \_ rendertargetyuv-Flag auf.</span><span class="sxs-lookup"><span data-stu-id="d6fc5-140">To enable YUV mixing mode in the VMR-9, call [**IVMRMixerControl9::SetMixingPrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs) with the MixerPref9\_RenderTargetYUV flag.</span></span>

<span data-ttu-id="d6fc5-141">Die einzige Möglichkeit, zu bestimmen, ob VMR-7 den neuen YUV-Mischungs Modus unterstützt, besteht darin, den VMR in diesem Modus festzulegen.</span><span class="sxs-lookup"><span data-stu-id="d6fc5-141">The only way to determine if the VMR-7 supports the new YUV mixing mode is to try setting the VMR into that mode.</span></span> <span data-ttu-id="d6fc5-142">Wenn der-Vorgang erfolgreich ist, können Sie den VMR bei Bedarf weiterhin in den RGB-Mischungs Modus versetzen.</span><span class="sxs-lookup"><span data-stu-id="d6fc5-142">If the call succeeds, you can still put the VMR back into RGB mixing mode if necessary.</span></span> <span data-ttu-id="d6fc5-143">Nachdem Sie den YUV-Mischungs Modus festgelegt haben, kann der VMR nur wieder in den RGB-Mischungs Modus geändert werden, nachdem alle Eingabe Pins getrennt wurden.</span><span class="sxs-lookup"><span data-stu-id="d6fc5-143">After it is set into YUV mixing mode, the VMR can only be changed back to RGB mixing mode after all input pins have been disconnected.</span></span>

<span data-ttu-id="d6fc5-144">Im YUV-Mischungs Modus können Sie die Auslastung der Grafikverarbeitungseinheit (GPU) verringern, indem Sie die folgenden Flags in der **setmixingprefs** -Methode anwenden:</span><span class="sxs-lookup"><span data-stu-id="d6fc5-144">In YUV mixing mode, you can reduce the load on the graphics processing unit (GPU) by applying the following flags in the **SetMixingPrefs** method:</span></span>



| <span data-ttu-id="d6fc5-145">Flag</span><span class="sxs-lookup"><span data-stu-id="d6fc5-145">Flag</span></span>                                                                                 | <span data-ttu-id="d6fc5-146">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d6fc5-146">Description</span></span>                                                      |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span data-ttu-id="d6fc5-147">VMR-7: mixerpref \_ dynamicswitchumbobvmr-9: MixerPref9 \_ dynamicswitchto Bob</span><span class="sxs-lookup"><span data-stu-id="d6fc5-147">VMR-7: MixerPref\_DynamicSwitchToBOBVMR-9: MixerPref9\_DynamicSwitchToBOB</span></span><br/> | <span data-ttu-id="d6fc5-148">Wechseln Sie zu Bob Deinterlacing.</span><span class="sxs-lookup"><span data-stu-id="d6fc5-148">Switch to bob deinterlacing.</span></span>                                     |
| <span data-ttu-id="d6fc5-149">VMR-7: mixerpref \_ DynamicDecimateBy2VMR-9: mixerpref \_ DynamicDecimateBy2</span><span class="sxs-lookup"><span data-stu-id="d6fc5-149">VMR-7: MixerPref\_DynamicDecimateBy2VMR-9: MixerPref\_DynamicDecimateBy2</span></span><br/>  | <span data-ttu-id="d6fc5-150">Dezimieren Sie das Bild mit dem Faktor 2 horizontal und vertikal.</span><span class="sxs-lookup"><span data-stu-id="d6fc5-150">Decimate the image by a factor of 2 horizontally and vertically.</span></span> |



 

<span data-ttu-id="d6fc5-151">Sie können diese Flags hinzufügen oder entfernen, während das Filter Diagramm ausgeführt wird. die Änderung wird angewendet, wenn der VMR-Mixer den nächsten Videoframe verfasst.</span><span class="sxs-lookup"><span data-stu-id="d6fc5-151">You can add or remove these flags while the filter graph is running; the change is applied when the VMR mixer composes the next video frame.</span></span> <span data-ttu-id="d6fc5-152">Die Flags schließen sich nicht gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="d6fc5-152">The flags are not mutually exclusive.</span></span> <span data-ttu-id="d6fc5-153">Durch diese Einstellungen wird die Qualität des Abbilds reduziert, sodass Sie diese nur dann anwenden können, wenn die Videoqualität weniger wichtig ist – z. b. Wenn Videos in einem kleinen Teil der Benutzeroberfläche abgespielt werden.</span><span class="sxs-lookup"><span data-stu-id="d6fc5-153">These settings reduce the quality of the image, so typically you would apply them only when video quality is less important — for example, if video is playing in a small portion of the user interface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d6fc5-154">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d6fc5-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d6fc5-155">Verwenden des VMR-Mischungs Modus</span><span class="sxs-lookup"><span data-stu-id="d6fc5-155">Using VMR Mixing Mode</span></span>](using-vmr-mixing-mode.md)
</dt> </dl>

 

 




