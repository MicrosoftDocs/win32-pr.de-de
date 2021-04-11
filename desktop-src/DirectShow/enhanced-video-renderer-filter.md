---
description: Der EVR-Filter (Enhanced Video Renderer) ist ein Video-Mixer und Renderer mit 16 Kanälen. Sie verfügt über die gleichen Kernfunktionen und das Plug-in-Modell wie die Media Foundation EVR-Medien Senke.
ms.assetid: ead99cb3-2be2-42c6-ac22-be0c2ddf28d5
title: Erweiterter Videorendererfilter
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ba6e7c14386ea37424364274263859844182ed7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104041214"
---
# <a name="enhanced-video-renderer-filter"></a><span data-ttu-id="b4d2b-104">Erweiterter Videorendererfilter</span><span class="sxs-lookup"><span data-stu-id="b4d2b-104">Enhanced Video Renderer Filter</span></span>

> [!Note]  
> <span data-ttu-id="b4d2b-105">Dieses Thema gilt für Windows Vista und höher.</span><span class="sxs-lookup"><span data-stu-id="b4d2b-105">This topic applies to Windows Vista and later.</span></span>

 

<span data-ttu-id="b4d2b-106">Der EVR-Filter (Enhanced Video Renderer) ist ein Video-Mixer und Renderer mit 16 Kanälen.</span><span class="sxs-lookup"><span data-stu-id="b4d2b-106">The Enhanced Video Renderer (EVR) filter is a 16-channel video mixer and renderer.</span></span> <span data-ttu-id="b4d2b-107">Sie verfügt über die gleichen Kernfunktionen und das Plug-in-Modell wie die Media Foundation EVR-Medien Senke.</span><span class="sxs-lookup"><span data-stu-id="b4d2b-107">It has the same core functionality and plug-in model as the Media Foundation EVR media sink.</span></span>

<span data-ttu-id="b4d2b-108">Der DirectShow-EVR-Filter ist in der Media Foundation SDK-Dokumentation dokumentiert. Weitere Informationen finden Sie unter [Enhanced Video Renderer](../medfound/enhanced-video-renderer.md).</span><span class="sxs-lookup"><span data-stu-id="b4d2b-108">The DirectShow EVR filter is documented in the Media Foundation SDK documentation; for more information, see [Enhanced Video Renderer](../medfound/enhanced-video-renderer.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b4d2b-109">Filter Schnittstellen (über <strong>QueryInterface</strong>)</span><span class="sxs-lookup"><span data-stu-id="b4d2b-109">Filter Interfaces (through <strong>QueryInterface</strong>)</span></span></td>
<td><span data-ttu-id="b4d2b-110">DirectShow-Schnittstellen:</span><span class="sxs-lookup"><span data-stu-id="b4d2b-110">DirectShow interfaces:</span></span>
<ul>
<li><span data-ttu-id="b4d2b-111"><a href="/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection"><strong>Iamcertifiedoutputprotection</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4d2b-111"><a href="/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection"><strong>IAMCertifiedOutputProtection</strong></a></span></span></li>
<li><span data-ttu-id="b4d2b-112"><a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>Iamfilterfehlflags</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4d2b-112"><a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags</strong></a></span></span></li>
<li><span data-ttu-id="b4d2b-113"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>Ibasefilter</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4d2b-113"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></li>
<li><span data-ttu-id="b4d2b-114"><a href="ikspropertyset.md"><strong>"Ikspropertyset"</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4d2b-114"><a href="ikspropertyset.md"><strong>IKsPropertySet</strong></a></span></span></li>
<li><span data-ttu-id="b4d2b-115"><a href="/windows/desktop/api/Strmif/nn-strmif-imediaeventsink"><strong>Imediaeventsink</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4d2b-115"><a href="/windows/desktop/api/Strmif/nn-strmif-imediaeventsink"><strong>IMediaEventSink</strong></a></span></span></li>
<li><span data-ttu-id="b4d2b-116"><a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>Imediaseeking</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4d2b-116"><a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></span></span></li>
<li><span data-ttu-id="b4d2b-117"><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>Iqualitycontrol</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4d2b-117"><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></li>
<li><span data-ttu-id="b4d2b-118"><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>Iqualprop</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4d2b-118"><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a></span></span></li>
</ul>
<span data-ttu-id="b4d2b-119">Media Foundation-Schnittstellen:</span><span class="sxs-lookup"><span data-stu-id="b4d2b-119">Media Foundation interfaces:</span></span><br/>
<ul>
<li><span data-ttu-id="b4d2b-120"><a href="/windows/desktop/api/evr/nn-evr-ievrfilterconfig"><strong>Ievrfilterconfig</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4d2b-120"><a href="/windows/desktop/api/evr/nn-evr-ievrfilterconfig"><strong>IEVRFilterConfig</strong></a></span></span></li>
<li><span data-ttu-id="b4d2b-121"><a href="/windows/desktop/api/mfidl/nn-mfidl-imfgetservice"><strong>IMF-Dienst</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4d2b-121"><a href="/windows/desktop/api/mfidl/nn-mfidl-imfgetservice"><strong>IMFGetService</strong></a></span></span></li>
<li><span data-ttu-id="b4d2b-122"><a href="/windows/desktop/api/evr/nn-evr-imfvideopositionmapper"><strong>IMF videopositionmapper</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4d2b-122"><a href="/windows/desktop/api/evr/nn-evr-imfvideopositionmapper"><strong>IMFVideoPositionMapper</strong></a></span></span></li>
<li><span data-ttu-id="b4d2b-123"><a href="/windows/desktop/api/evr/nn-evr-imfvideorenderer"><strong>Imsvideorenderer</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4d2b-123"><a href="/windows/desktop/api/evr/nn-evr-imfvideorenderer"><strong>IMFVideoRenderer</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b4d2b-124">Eingabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="b4d2b-124">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="b4d2b-125">Variable, abhängig vom Grafiktreiber.</span><span class="sxs-lookup"><span data-stu-id="b4d2b-125">Variable, depending on the graphics driver.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b4d2b-126">Eingabe-PIN-Schnittstellen (über <strong>QueryInterface</strong>)</span><span class="sxs-lookup"><span data-stu-id="b4d2b-126">Input Pin Interfaces (through <strong>QueryInterface</strong>)</span></span></td>
<td><span data-ttu-id="b4d2b-127">DirectShow-Schnittstellen:</span><span class="sxs-lookup"><span data-stu-id="b4d2b-127">DirectShow interfaces:</span></span>
<ul>
<li><span data-ttu-id="b4d2b-128"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4d2b-128"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></span></span></li>
<li><span data-ttu-id="b4d2b-129"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4d2b-129"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></span></span></li>
<li><span data-ttu-id="b4d2b-130"><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>Iqualitycontrol</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4d2b-130"><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></li>
</ul>
<span data-ttu-id="b4d2b-131">Media Foundation-Schnittstellen:</span><span class="sxs-lookup"><span data-stu-id="b4d2b-131">Media Foundation interfaces:</span></span><br/>
<ul>
<li><span data-ttu-id="b4d2b-132"><a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration"><strong>Idirectxvideomemoryconfiguration</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4d2b-132"><a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration"><strong>IDirectXVideoMemoryConfiguration</strong></a></span></span></li>
<li><span data-ttu-id="b4d2b-133"><a href="/windows/desktop/api/evr9/nn-evr9-ievrvideostreamcontrol"><strong>Ievrvideostreamcontrol</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4d2b-133"><a href="/windows/desktop/api/evr9/nn-evr9-ievrvideostreamcontrol"><strong>IEVRVideoStreamControl</strong></a></span></span></li>
<li><span data-ttu-id="b4d2b-134"><a href="/windows/desktop/api/mfidl/nn-mfidl-imfgetservice"><strong>IMF-Dienst</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4d2b-134"><a href="/windows/desktop/api/mfidl/nn-mfidl-imfgetservice"><strong>IMFGetService</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b4d2b-135">Ausgabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="b4d2b-135">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="b4d2b-136">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="b4d2b-136">Not applicable.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b4d2b-137">PIN-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="b4d2b-137">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="b4d2b-138">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="b4d2b-138">Not applicable.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b4d2b-139">CLSID Filtern</span><span class="sxs-lookup"><span data-stu-id="b4d2b-139">Filter CLSID</span></span></td>
<td><span data-ttu-id="b4d2b-140">CLSID_EnhancedVideoRenderer</span><span class="sxs-lookup"><span data-stu-id="b4d2b-140">CLSID_EnhancedVideoRenderer</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b4d2b-141">Ausführbare Datei</span><span class="sxs-lookup"><span data-stu-id="b4d2b-141">Executable</span></span></td>
<td><span data-ttu-id="b4d2b-142">evr.dll</span><span class="sxs-lookup"><span data-stu-id="b4d2b-142">evr.dll</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b4d2b-143"><a href="merit.md">Verdienst</a></span><span class="sxs-lookup"><span data-stu-id="b4d2b-143"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="b4d2b-144">MERIT_DO_NOT_USE</span><span class="sxs-lookup"><span data-stu-id="b4d2b-144">MERIT_DO_NOT_USE</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b4d2b-145"><a href="filter-categories.md">Filter Kategorie</a></span><span class="sxs-lookup"><span data-stu-id="b4d2b-145"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="b4d2b-146">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="b4d2b-146">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="b4d2b-147">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b4d2b-147">Remarks</span></span>

<span data-ttu-id="b4d2b-148">Zusätzlich zu den Schnittstellen, die über **QueryInterface** verfügbar gemacht werden, macht der EVR andere Schnittstellen über die [**imfgetservice:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) -Methode verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b4d2b-148">In addition to the interfaces exposed through **QueryInterface**, the EVR exposes other interfaces through the [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) method.</span></span> <span data-ttu-id="b4d2b-149">Einige dieser Schnittstellen werden von dem EVR Presenter oder dem EVR-Mixer implementiert, nicht von dem EVR selbst.</span><span class="sxs-lookup"><span data-stu-id="b4d2b-149">Some of these interfaces are implemented by the EVR presenter or the EVR mixer, rather than the EVR itself.</span></span> <span data-ttu-id="b4d2b-150">Wenn die Anwendung einen benutzerdefinierten Presenter oder Mixer auf dem EVR festlegt, machen die benutzerdefinierten Versionen möglicherweise einen anderen Satz von Schnittstellen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b4d2b-150">If the application sets a custom presenter or mixer on the EVR, the custom versions might expose a different set of interfaces.</span></span>



| <span data-ttu-id="b4d2b-151">Object</span><span class="sxs-lookup"><span data-stu-id="b4d2b-151">Object</span></span>     | <span data-ttu-id="b4d2b-152">Dienst Bezeichner</span><span class="sxs-lookup"><span data-stu-id="b4d2b-152">Service Identifier</span></span>                                              | <span data-ttu-id="b4d2b-153">Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="b4d2b-153">Interfaces</span></span>                                                                                                                                                                                                                                                                                                     |
|------------|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4d2b-154">EVR-Filter</span><span class="sxs-lookup"><span data-stu-id="b4d2b-154">EVR filter</span></span> | <span data-ttu-id="b4d2b-155">Mr- \_ Video- \_ Rendering- \_ Dienst (Abfrage EVR oder Presenter)</span><span class="sxs-lookup"><span data-stu-id="b4d2b-155">MR\_VIDEO\_RENDER\_SERVICE(Queries EVR or presenter)</span></span><br/> | [<span data-ttu-id="b4d2b-156">**IMF videoabviceid**</span><span class="sxs-lookup"><span data-stu-id="b4d2b-156">**IMFVideoDeviceID**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)<br/> [<span data-ttu-id="b4d2b-157">**IMF videodisplaycontrol**</span><span class="sxs-lookup"><span data-stu-id="b4d2b-157">**IMFVideoDisplayControl**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol)<br/> [<span data-ttu-id="b4d2b-158">**IMF videopositionmapper**</span><span class="sxs-lookup"><span data-stu-id="b4d2b-158">**IMFVideoPositionMapper**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper)<br/> [<span data-ttu-id="b4d2b-159">**IMF videopresenter**</span><span class="sxs-lookup"><span data-stu-id="b4d2b-159">**IMFVideoPresenter**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideopresenter)<br/>                                                          |
| <span data-ttu-id="b4d2b-160">EVR-Filter</span><span class="sxs-lookup"><span data-stu-id="b4d2b-160">EVR filter</span></span> | <span data-ttu-id="b4d2b-161">Mr- \_ Video \_ Beschleunigungs \_ Dienst (Abfrage Presenter)</span><span class="sxs-lookup"><span data-stu-id="b4d2b-161">MR\_VIDEO\_ACCELERATION\_SERVICE(Queries presenter)</span></span><br/>  | [<span data-ttu-id="b4d2b-162">**IDirect3DDeviceManager9**</span><span class="sxs-lookup"><span data-stu-id="b4d2b-162">**IDirect3DDeviceManager9**</span></span>](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9)                                                                                                                                                                                                                                                      |
| <span data-ttu-id="b4d2b-163">EVR-Filter</span><span class="sxs-lookup"><span data-stu-id="b4d2b-163">EVR filter</span></span> | <span data-ttu-id="b4d2b-164">Mr- \_ Video- \_ Mixer- \_ Dienst (Queries-Mixer)</span><span class="sxs-lookup"><span data-stu-id="b4d2b-164">MR\_VIDEO\_MIXER\_SERVICE(Queries mixer)</span></span><br/>             | [<span data-ttu-id="b4d2b-165">**IMF videoabviceid**</span><span class="sxs-lookup"><span data-stu-id="b4d2b-165">**IMFVideoDeviceID**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)<br/> [<span data-ttu-id="b4d2b-166">**IMF videomixerbitmap**</span><span class="sxs-lookup"><span data-stu-id="b4d2b-166">**IMFVideoMixerBitmap**</span></span>](/windows/desktop/api/evr9/nn-evr9-imfvideomixerbitmap)<br/> [<span data-ttu-id="b4d2b-167">**IMF videomixercontrol**</span><span class="sxs-lookup"><span data-stu-id="b4d2b-167">**IMFVideoMixerControl**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideomixercontrol)<br/> [<span data-ttu-id="b4d2b-168">**IMF videopositionmapper**</span><span class="sxs-lookup"><span data-stu-id="b4d2b-168">**IMFVideoPositionMapper**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper)<br/> [<span data-ttu-id="b4d2b-169">**IMF videoprocessor**</span><span class="sxs-lookup"><span data-stu-id="b4d2b-169">**IMFVideoProcessor**</span></span>](/windows/desktop/api/evr9/nn-evr9-imfvideoprocessor)<br/> |
| <span data-ttu-id="b4d2b-170">Eingabe Pins</span><span class="sxs-lookup"><span data-stu-id="b4d2b-170">Input pins</span></span> | <span data-ttu-id="b4d2b-171">Mr- \_ Video \_ Beschleunigungs \_ Dienst</span><span class="sxs-lookup"><span data-stu-id="b4d2b-171">MR\_VIDEO\_ACCELERATION\_SERVICE</span></span>                                | [<span data-ttu-id="b4d2b-172">**Idirectxvideomemoryconfiguration**</span><span class="sxs-lookup"><span data-stu-id="b4d2b-172">**IDirectXVideoMemoryConfiguration**</span></span>](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration)                                                                                                                                                                                                                                    |



 

<span data-ttu-id="b4d2b-173">Der EVR kann bis zu 16 Videostreams mischen.</span><span class="sxs-lookup"><span data-stu-id="b4d2b-173">The EVR can mix up to 16 video streams.</span></span> <span data-ttu-id="b4d2b-174">Der erste Eingabedaten Strom (PIN 0) wird als *Verweis Datenstrom* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="b4d2b-174">The first input stream (pin 0) is called the *reference stream*.</span></span> <span data-ttu-id="b4d2b-175">Der Verweis Datenstrom wird immer zuerst in der z-Reihenfolge angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b4d2b-175">The reference stream always appears first in the z-order.</span></span> <span data-ttu-id="b4d2b-176">Alle zusätzlichen Streams werden als Substreams bezeichnet und werden oberhalb des Verweis Datenstroms gemischt.</span><span class="sxs-lookup"><span data-stu-id="b4d2b-176">Any additional streams are called substreams, and are mixed on top of the reference stream.</span></span> <span data-ttu-id="b4d2b-177">Die Anwendung kann die z-Reihenfolge der untergeordneten Datenströme ändern, aber kein untergeordneter Stream kann in der z-Reihenfolge angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="b4d2b-177">The application can change the z-order of the substreams, but no substream can be first in the z-order.</span></span>

<span data-ttu-id="b4d2b-178">Der Grafiktreiber bestimmt, welche Videoformate unterstützt werden, aber in der Regel sind Sie auf Folgendes beschränkt:</span><span class="sxs-lookup"><span data-stu-id="b4d2b-178">The graphics driver determines which video formats are supported, but typically they are limited to the following:</span></span>

-   <span data-ttu-id="b4d2b-179">Verweis Datenstrom: progressiv oder Zeilen Sprung-YUV ohne pro Pixel Alpha (z. b. NV12 oder im YUY2); oder progressiv RGB.</span><span class="sxs-lookup"><span data-stu-id="b4d2b-179">Reference stream: Progressive or interlaced YUV with no per-pixel alpha (such as NV12 or YUY2); or progressive RGB.</span></span>
-   <span data-ttu-id="b4d2b-180">Unter Ströme: Progressive YUV mit pro Pixel-Alpha, wie z. b. ayuv oder AI44.</span><span class="sxs-lookup"><span data-stu-id="b4d2b-180">Substreams: Progressive YUV with per-pixel-alpha, such as AYUV or AI44.</span></span>

<span data-ttu-id="b4d2b-181">Die verfügbaren substreamformate können vom Format des Verweis Datenstroms abhängen.</span><span class="sxs-lookup"><span data-stu-id="b4d2b-181">The available substream formats might depend on the format of the reference stream.</span></span>

<span data-ttu-id="b4d2b-182">Der EVR leitet Seek-Befehle durch Upstream durch PIN 0 weiter.</span><span class="sxs-lookup"><span data-stu-id="b4d2b-182">The EVR forwards seek commands upstream through pin 0.</span></span> <span data-ttu-id="b4d2b-183">Die untergeordneten Datenstrom-Pins leiten keine Seek-Befehle weiter.</span><span class="sxs-lookup"><span data-stu-id="b4d2b-183">The substream pins do not forward seek commands.</span></span> <span data-ttu-id="b4d2b-184">Der Quell-oder Splitter Filter ist dafür verantwortlich, dass die untergeordneten Datenströme mit dem Verweisstream synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="b4d2b-184">It is the responsibility of the source or splitter filter to keep the substreams synchronized with the reference stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4d2b-185">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b4d2b-185">Requirements</span></span>



| <span data-ttu-id="b4d2b-186">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b4d2b-186">Requirement</span></span> | <span data-ttu-id="b4d2b-187">Wert</span><span class="sxs-lookup"><span data-stu-id="b4d2b-187">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b4d2b-188">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b4d2b-188">Minimum supported client</span></span><br/> | <span data-ttu-id="b4d2b-189">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b4d2b-189">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b4d2b-190">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b4d2b-190">Minimum supported server</span></span><br/> | <span data-ttu-id="b4d2b-191">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b4d2b-191">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b4d2b-192">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b4d2b-192">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4d2b-193">DirectShow-Filter</span><span class="sxs-lookup"><span data-stu-id="b4d2b-193">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

