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
# <a name="enhanced-video-renderer-filter"></a>Erweiterter Videorendererfilter

> [!Note]  
> Dieses Thema gilt für Windows Vista und höher.

 

Der EVR-Filter (Enhanced Video Renderer) ist ein Video-Mixer und Renderer mit 16 Kanälen. Sie verfügt über die gleichen Kernfunktionen und das Plug-in-Modell wie die Media Foundation EVR-Medien Senke.

Der DirectShow-EVR-Filter ist in der Media Foundation SDK-Dokumentation dokumentiert. Weitere Informationen finden Sie unter [Enhanced Video Renderer](../medfound/enhanced-video-renderer.md).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Filter Schnittstellen (über <strong>QueryInterface</strong>)</td>
<td>DirectShow-Schnittstellen:
<ul>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection"><strong>Iamcertifiedoutputprotection</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>Iamfilterfehlflags</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>Ibasefilter</strong></a></li>
<li><a href="ikspropertyset.md"><strong>"Ikspropertyset"</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-imediaeventsink"><strong>Imediaeventsink</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>Imediaseeking</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>Iqualitycontrol</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>Iqualprop</strong></a></li>
</ul>
Media Foundation-Schnittstellen:<br/>
<ul>
<li><a href="/windows/desktop/api/evr/nn-evr-ievrfilterconfig"><strong>Ievrfilterconfig</strong></a></li>
<li><a href="/windows/desktop/api/mfidl/nn-mfidl-imfgetservice"><strong>IMF-Dienst</strong></a></li>
<li><a href="/windows/desktop/api/evr/nn-evr-imfvideopositionmapper"><strong>IMF videopositionmapper</strong></a></li>
<li><a href="/windows/desktop/api/evr/nn-evr-imfvideorenderer"><strong>Imsvideorenderer</strong></a></li>
</ul></td>
</tr>
<tr class="even">
<td>Eingabe-PIN-Medientypen</td>
<td>Variable, abhängig vom Grafiktreiber.</td>
</tr>
<tr class="odd">
<td>Eingabe-PIN-Schnittstellen (über <strong>QueryInterface</strong>)</td>
<td>DirectShow-Schnittstellen:
<ul>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>Iqualitycontrol</strong></a></li>
</ul>
Media Foundation-Schnittstellen:<br/>
<ul>
<li><a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration"><strong>Idirectxvideomemoryconfiguration</strong></a></li>
<li><a href="/windows/desktop/api/evr9/nn-evr9-ievrvideostreamcontrol"><strong>Ievrvideostreamcontrol</strong></a></li>
<li><a href="/windows/desktop/api/mfidl/nn-mfidl-imfgetservice"><strong>IMF-Dienst</strong></a></li>
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
<td>CLSID_EnhancedVideoRenderer</td>
</tr>
<tr class="odd">
<td>Ausführbare Datei</td>
<td>evr.dll</td>
</tr>
<tr class="even">
<td><a href="merit.md">Verdienst</a></td>
<td>MERIT_DO_NOT_USE</td>
</tr>
<tr class="odd">
<td><a href="filter-categories.md">Filter Kategorie</a></td>
<td>CLSID_LegacyAmFilterCategory</td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Bemerkungen

Zusätzlich zu den Schnittstellen, die über **QueryInterface** verfügbar gemacht werden, macht der EVR andere Schnittstellen über die [**imfgetservice:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) -Methode verfügbar. Einige dieser Schnittstellen werden von dem EVR Presenter oder dem EVR-Mixer implementiert, nicht von dem EVR selbst. Wenn die Anwendung einen benutzerdefinierten Presenter oder Mixer auf dem EVR festlegt, machen die benutzerdefinierten Versionen möglicherweise einen anderen Satz von Schnittstellen verfügbar.



| Object     | Dienst Bezeichner                                              | Schnittstellen                                                                                                                                                                                                                                                                                                     |
|------------|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| EVR-Filter | Mr- \_ Video- \_ Rendering- \_ Dienst (Abfrage EVR oder Presenter)<br/> | [**IMF videoabviceid**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)<br/> [**IMF videodisplaycontrol**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol)<br/> [**IMF videopositionmapper**](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper)<br/> [**IMF videopresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter)<br/>                                                          |
| EVR-Filter | Mr- \_ Video \_ Beschleunigungs \_ Dienst (Abfrage Presenter)<br/>  | [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9)                                                                                                                                                                                                                                                      |
| EVR-Filter | Mr- \_ Video- \_ Mixer- \_ Dienst (Queries-Mixer)<br/>             | [**IMF videoabviceid**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)<br/> [**IMF videomixerbitmap**](/windows/desktop/api/evr9/nn-evr9-imfvideomixerbitmap)<br/> [**IMF videomixercontrol**](/windows/desktop/api/evr/nn-evr-imfvideomixercontrol)<br/> [**IMF videopositionmapper**](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper)<br/> [**IMF videoprocessor**](/windows/desktop/api/evr9/nn-evr9-imfvideoprocessor)<br/> |
| Eingabe Pins | Mr- \_ Video \_ Beschleunigungs \_ Dienst                                | [**Idirectxvideomemoryconfiguration**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration)                                                                                                                                                                                                                                    |



 

Der EVR kann bis zu 16 Videostreams mischen. Der erste Eingabedaten Strom (PIN 0) wird als *Verweis Datenstrom* bezeichnet. Der Verweis Datenstrom wird immer zuerst in der z-Reihenfolge angezeigt. Alle zusätzlichen Streams werden als Substreams bezeichnet und werden oberhalb des Verweis Datenstroms gemischt. Die Anwendung kann die z-Reihenfolge der untergeordneten Datenströme ändern, aber kein untergeordneter Stream kann in der z-Reihenfolge angegeben werden.

Der Grafiktreiber bestimmt, welche Videoformate unterstützt werden, aber in der Regel sind Sie auf Folgendes beschränkt:

-   Verweis Datenstrom: progressiv oder Zeilen Sprung-YUV ohne pro Pixel Alpha (z. b. NV12 oder im YUY2); oder progressiv RGB.
-   Unter Ströme: Progressive YUV mit pro Pixel-Alpha, wie z. b. ayuv oder AI44.

Die verfügbaren substreamformate können vom Format des Verweis Datenstroms abhängen.

Der EVR leitet Seek-Befehle durch Upstream durch PIN 0 weiter. Die untergeordneten Datenstrom-Pins leiten keine Seek-Befehle weiter. Der Quell-oder Splitter Filter ist dafür verantwortlich, dass die untergeordneten Datenströme mit dem Verweisstream synchronisiert werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

