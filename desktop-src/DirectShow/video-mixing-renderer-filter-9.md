---
description: Video Mischungs-Renderer Filter 9
ms.assetid: 3885cca2-74b1-4066-8ecb-84c9841f9e66
title: Video Mischungs-Renderer Filter 9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8b2576f8c5f1b0f262b83141c14ce4836eecb4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757674"
---
# <a name="video-mixing-renderer-filter-9"></a>Video Mischungs-Renderer Filter 9

In DirectX 9 bietet der Filter Video Mischungs-Renderer 9 (VMR-9) erweiterte videorenderingfunktionen auf allen Plattformen, die von DirectX unterstützt werden. Es ist vollständig in DirectX 9 3D-Funktionen integriert. Beispielsweise können Sie problemlos Videos zu spielen und anderen 3D-Umgebungen hinzufügen oder Videobilder mithilfe der Direct3D-Pixel-Shader und anderer Effekte transformieren.

Dieser Filter unterstützt keine Videoports.

Um die Abwärtskompatibilität zu gewährleisten, ist VMR-9 nicht der Standard-Renderer auf einem System. Wenn Sie diesen Filter verwenden möchten, fügen Sie ihn explizit dem Filter Diagramm hinzu, und konfigurieren Sie ihn, bevor Sie seine Eingabe Pins verbinden. VMR-9 verwendet einen eigenen Satz von Schnittstellen, Strukturen und Enumerationen, die nicht immer mit den entsprechenden Datentypen identisch sind, die mit VMR-7 verwendet werden.

VMR-9 unterstützt bis zu 16 Monitore.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Filter Schnittstellen</td>
<td>VMR-9 unterstützt mehrere verschiedene Renderingmodi. Sie unterstützt abhängig vom Renderingmodus einen anderen Satz von Schnittstellen:<br/>
<ul>
<li>Alle Modi: <a href="/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection"><strong>iamcertifiedoutputprotection</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>iamfilterfehlflags</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>ibasefilter</strong></a>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>imediaposition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>imediaseeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>iqualitycontrol</strong></a>, <a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>iqualprop</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmraspectratiocontrol9"><strong>IVMRAspectRatioControl9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrdeinterlacecontrol9"><strong>IVMRDeinterlaceControl9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9"><strong>IVMRFilterConfig9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9"><strong>IVMRMixerBitmap9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixercontrol9"><strong>IVMRMixerControl9</strong></a></li>
<li>Renderless-Modus: <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatornotify9"> <strong>IVMRSurfaceAllocatorNotify9</strong></a></li>
<li>Fenstermodus: <a href="/windows/desktop/api/Control/nn-control-ibasicvideo"><strong>ibasicvideo</strong></a>, <a href="/windows/desktop/api/Control/nn-control-ibasicvideo2"><strong>IBasicVideo2</strong></a>, <a href="/windows/desktop/api/Control/nn-control-ivideowindow"><strong>IVideoWindow</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmonitorconfig9"><strong>IVMRMonitorConfig9</strong></a></li>
<li>Fensterloser Modus: <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmonitorconfig9"><strong>IVMRMonitorConfig9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9"><strong>IVMRWindowlessControl9</strong></a></li>
</ul>
Um den Renderingmodus festzulegen, nennen Sie <a href="/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode"><strong>IVMRFilterConfig9:: setrenderingmode</strong></a>. Weitere Informationen finden Sie unter <a href="vmr-modes-of-operation.md">VMR-Betriebsmodi</a>.<br/></td>
</tr>
<tr class="even">
<td>Eingabe-PIN-Medientypen</td>
<td>Die Eingabe Pins stellen eine Verbindung mit jedem Typ her, der von der zugrunde liegenden Video Hardware unterstützt wird.</td>
</tr>
<tr class="odd">
<td>PIN-Eingabeschnittstellen</td>
<td><a href="/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator"><strong>Iamvideoaccelerator</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ioverlay"><strong>IOverlay</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>iqualitycontrol</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>ipinconnection</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrvideostreamcontrol9"><strong>IVMRVideoStreamControl9</strong></a></td>
</tr>
<tr class="even">
<td>Ausgabe-PIN-Medientypen</td>
<td>Nicht zutreffend</td>
</tr>
<tr class="odd">
<td>PIN-Schnittstellen</td>
<td>Nicht zutreffend</td>
</tr>
<tr class="even">
<td>CLSID Filtern</td>
<td>CLSID_VideoMixingRenderer9</td>
</tr>
<tr class="odd">
<td>CLSID der Eigenschaften Seite</td>
<td>–</td>
</tr>
<tr class="even">
<td>Ausführbare Datei</td>
<td>Quartz.dll</td>
</tr>
<tr class="odd">
<td><a href="merit.md">Verdienst</a></td>
<td>MERIT_DO_NOT_USE</td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">Filter Kategorie</a></td>
<td>CLSID_LegacyAmFilterCategory</td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Bemerkungen

Eine Anwendung kann ein benutzerdefiniertes zuordnerpräsentatorobjekt bereitstellen, das die folgenden Schnittstellen verfügbar macht:

-   [**IVMRImagePresenter9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenter9)
-   [**IVMRImagePresenterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenterconfig9) (optional)
-   [**IVMRSurfaceAllocator9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocator9)
-   [**IVMRSurfaceAllocatorEx9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatorex9) (optional)
-   [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) (optional)

Weitere Informationen zu benutzerdefinierten Zuweiser finden Sie unter [Bereitstellen eines benutzerdefinierten Allocator-Presenter für VMR-9](supplying-a-custom-allocator-presenter-for-vmr-9.md).

Eine Anwendung kann auch einen benutzerdefinierten Plug-in-Compositor bereitstellen, der die folgende Schnittstelle verfügbar macht:

-   [**IVMRImageCompositor9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagecompositor9)

Um das VMR mit einem benutzerdefinierten Compositor zu konfigurieren, müssen Sie [**IVMRFilterConfig9:: abtimagecompositor**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setimagecompositor)aufrufen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> <dt>

[Verwenden des Video Mischungs Renderers](using-the-video-mixing-renderer.md)
</dt> </dl>

 

 




