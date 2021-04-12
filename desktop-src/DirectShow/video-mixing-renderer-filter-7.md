---
description: Video Mischungs-Renderer Filter 7
ms.assetid: c83e6c50-76f2-4aeb-944b-5b244c6bf776
title: Video Mischungs-Renderer Filter 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14e396e15189e89dcebde69fb513419df340ab09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527812"
---
# <a name="video-mixing-renderer-filter-7"></a>Video Mischungs-Renderer Filter 7

Dieses Thema gilt für Windows XP oder höher.

In Windows XP und höher ist der Video Mischungs-Renderer 7 (VMR-7) der Standardvideorenderer. Sie wird als "VMR-7" bezeichnet, da intern DirectDraw 7 verwendet wird. In DirectX 9 ist ein ähnlicher, aber separater Filter (VMR-9) für die erneute Verteilung auf nicht-XP-Systemen verfügbar. VMR-9 verwendet Direct3D 9.

> [!Note]  
> VMR ist unter Windows XP und höher verfügbar. Es ist nicht über die Redistributable von DirectX oder frühere Versionen von Windows verfügbar. In den meisten Szenarien sollten Anwendungen den [Video Mischungs-Renderer 9](video-mixing-renderer-filter-9.md)verwenden.

 

Zu den Features der VMR gehören:

-   Echte Alpha Mischung von bis zu 16 Eingabedaten strömen
-   Zugriff auf das zusammengesetzte Image, bevor es gerendert wird
-   Ein Plug-in-Modell, das Drittanbietern das Implementieren von benutzerdefinierten Video Effekten ermöglicht.
-   Unterstützung für bis zu 15 Monitore.

Während der Diagramm Erstellung unter Windows XP und höher verwendet der Filter Graph-Manager nicht die älteren Videorenderer oder Überlagerungs Filter Filter, es sei denn, die Anwendung erstellt Sie explizit und fügt Sie dem Diagramm hinzu.

Weitere Informationen finden Sie unter [using the Video mischungsrenderer](using-the-video-mixing-renderer.md).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Filter Schnittstellen</td>
<td>Alle Modi:
<ul>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection"><strong>Iamcertifiedoutputprotection</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>Iamfilterfehlflags</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>Ibasefilter</strong></a></li>
<li><a href="ikspropertyset.md"><strong>"Ikspropertyset"</strong></a></li>
<li><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>Imediaposition</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>Imediaseeking</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>Iqualitycontrol</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>Iqualprop</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmraspectratiocontrol"><strong>Ivmraspectratiocontrol</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrdeinterlacecontrol"><strong>Ivmrdeinterlacecontrol</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrfilterconfig"><strong>Ivmrfilterconfig</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixerbitmap"><strong>Ivmrmixerbitmap</strong></a></li>
</ul>
Fenstermodus:<br/>
<ul>
<li><a href="/windows/desktop/api/Control/nn-control-ibasicvideo"><strong>Ibasicvideo</strong></a></li>
<li><a href="/windows/desktop/api/Control/nn-control-ibasicvideo2"><strong>IBasicVideo2</strong></a></li>
<li><a href="/windows/desktop/api/Control/nn-control-ivideowindow"><strong>IVideoWindow</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmonitorconfig"><strong>Ivmrmonitorconfig</strong></a></li>
</ul>
Fensterloser Modus:<br/>
<ul>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol"><strong>Ivmrwindowlesscontrol</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmonitorconfig"><strong>Ivmrmonitorconfig</strong></a></li>
</ul>
Modus für renderlos:<br/>
<ul>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocatornotify"><strong>Ivmrsurfacezuweisung</strong></a></li>
</ul>
Mischmodus:<br/>
<ul>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol"><strong>Ivmrmixercontrol</strong></a></li>
</ul>
Informationen zu den verschiedenen VMR-7-Modi finden Sie unter <a href="vmr-modes-of-operation.md">VMR-Betriebsmodi</a>.<br/></td>
</tr>
<tr class="even">
<td>Eingabe-PIN-Medientypen</td>
<td>Haupttyp: MEDIATYPE_VideoSubtype: hängt von der Grafikhardware ab. Muss ein unkomprimiertes Video sein.<br/></td>
</tr>
<tr class="odd">
<td>PIN-Eingabeschnittstellen</td>
<td><ul>
<li><a href="/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator"><strong>Iamvideoaccelerator</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ioverlay"><strong>IOverlay</strong></a> (siehe Hinweise)</li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>Ipinconnection</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>Iqualitycontrol</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrvideostreamcontrol"><strong>Ivmrvideostreamcontrol</strong></a></li>
</ul></td>
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
<td>Diesem Filter sind zwei CLSIDs zugeordnet:
<ul>
<li>CLSID_VideoMixingRenderer: erstellt VMR-7. Wenn nicht genügend Systemressourcen vorhanden sind, um VMR-7 zu erstellen, tritt beim Aufrufen von <strong>CoCreateInstance</strong> ein Fehler auf.</li>
<li>CLSID_VideoRendererDefault: erstellt VMR-7, wenn Systemressourcen verfügbar sind, oder erstellt andernfalls den alten <a href="video-renderer-filter.md">Videorendererfilter</a> .</li>
</ul>
Verwenden Sie CLSID_VideoMixingRenderer, wenn Sie die spezifischen Funktionen von VMR-7 benötigen. Andernfalls verwenden Sie CLSID_VideoRendererDefault, was fast sicher ist, dass kein Fehler auftritt, da Sie auf den alten Videorendererfilter zurückgreift.<br/></td>
</tr>
<tr class="odd">
<td>CLSID der Eigenschaften Seite</td>
<td>Nicht zutreffend</td>
</tr>
<tr class="even">
<td>Ausführbare Datei</td>
<td>Quartz.dll</td>
</tr>
<tr class="odd">
<td><a href="merit.md">Verdienst</a></td>
<td>MERIT_PREFERRED + 1</td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">Filter Kategorie</a></td>
<td>CLSID_LegacyAmFilterCategory</td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Bemerkungen

Die Eingabe-PIN macht die **IOverlay** -Schnittstelle nur verfügbar, wenn sich der VMR-7-Filter im Fenstermodus befindet. Die einzige **IOverlay** -Methode, die die PIN implementiert, ist **getwindowhandle**, die einer Anwendung das Abrufen eines Handles für das Videofenster des Filters ermöglicht. Alle anderen **IOverlay** -Methoden geben E \_ notimpl zurück. Im fensterlosen Modus erstellt der Filter kein Videofenster, sodass die PIN die Schnittstelle nicht verfügbar macht.

Eine Anwendung kann ein benutzerdefiniertes zuordnerpräsentatorobjekt bereitstellen, das die folgenden Schnittstellen verfügbar macht:

-   [**Ivmrimagepresenter**](/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenter)
-   [**Ivmrimagepresenterconfig**](/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenterconfig) (optional)
-   [**Ivmrmonitorconfig**](/windows/desktop/api/Strmif/nn-strmif-ivmrmonitorconfig) (optional)
-   [**Ivmrsurfacezucator**](/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocator)
-   [**Ivmrwindowlesscontrol**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) (optional)

Weitere Informationen zu benutzerdefinierten Zuweiser finden Sie unter [Bereitstellen eines benutzerdefinierten Allocator-Presenter für VMR-7](supplying-a-custom-allocator-presenter-for-vmr-7.md).

Eine Anwendung kann auch einen benutzerdefinierten Plug-in-Compositor bereitstellen, der die folgende Schnittstelle verfügbar macht:

-   [**Ivmrimagecompositor**](/windows/desktop/api/Strmif/nn-strmif-ivmrimagecompositor)

Um das VMR mit einem benutzerdefinierten Compositor zu konfigurieren, nennen Sie [**ivmrfilterconfig:: abtimagecompositor**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setimagecompositor).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 




