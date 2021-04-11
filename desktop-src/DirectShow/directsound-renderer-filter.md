---
description: DirectSound-rendererfilter
ms.assetid: ec6cc790-8c1f-4de4-a7ca-a7073894380e
title: DirectSound-rendererfilter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae932340ea22213e0f9d7234599742d74208f632
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123505"
---
# <a name="directsound-renderer-filter"></a>DirectSound-rendererfilter

Mit diesem Filter wird Audio mithilfe von DirectSound gerendert. Dieser Filter ist derzeit der Standardaudiorenderer für Wellenform Sound.

Zusätzlich zu den grundlegenden Sound Rendering-Funktionen kann dieser Filter DirectSound-API-Aufrufe verarbeiten. Verwenden Sie die [**iamdirectsound**](/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound) -Methoden, um das Fenster festzulegen und abzurufen, das die Audiowiedergabe behandelt. Der DirectSound-audiorenderer ist der standardaudiorenderingfilter für DirectShow.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Filter Schnittstellen</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iamaudiorendererstats"><strong>Iamaudiorendererstats</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamclockslave"><strong>iamclockslave</strong></a>, <a href="/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound"><strong>iamdirectsound</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol"><strong>iamresourcecontrol</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>ibasefilter</strong></a>, <a href="/windows/desktop/api/Control/nn-control-ibasicaudio"><strong>ibasicaudio</strong></a>, <strong>IDirectSound3DBuffer</strong>, <strong>IDirectSound3dListener</strong>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>imediaposition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>imediaseeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>iqualitycontrol</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ireferenceclock"><strong>IReferenceClock</strong></a></td>
</tr>
<tr class="even">
<td>Eingabe-PIN-Medientypen</td>
<td>Haupttyp: MEDIATYPE_AudioSubtypes:<br/>
<ul>
<li>MEDIASUBTYPE_PCM</li>
<li>MEDIASUBTYPE_IEEE_FLOAT</li>
<li>MEDIASUBTYPE_DOLBY_AC3_SPDIF</li>
<li>MEDIASUBTYPE_RAW_SPORT</li>
<li>MEDIASUBTYPE_SPDIF_TAG_241h</li>
<li>MEDIASUBTYPE_DRM_Audio</li>
</ul>
Formattyp: FORMAT_WaveFormatEx<br/></td>
</tr>
<tr class="odd">
<td>PIN-Eingabeschnittstellen</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>ipinconnection</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>iqualitycontrol</strong></a></td>
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
<td>CLSID_DSoundRender</td>
</tr>
<tr class="odd">
<td>CLSID der Eigenschaften Seite</td>
<td>CLSID_AudioProperties CLSID_AudioRendererAdvancedProperties</td>
</tr>
<tr class="even">
<td>Ausführbare Datei</td>
<td>quartz.dll</td>
</tr>
<tr class="odd">
<td><a href="merit.md">Verdienst</a></td>
<td>MERIT_PREFERRED</td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">Filter Kategorie</a></td>
<td>CLSID_AudioRendererCategory</td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Bemerkungen

Dieser Filter fungiert als Wrapper für ein Audiogerät. Um die auf dem System des Benutzers verfügbaren Audiogeräte aufzulisten, verwenden Sie die [**ikreatedevenum**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum) -Schnittstelle mit der Kategorie audiorenderer (CLSID \_ audiorenderercategory). Für jedes Audiogerät enthält die Kategorie audiorenderer zwei Filter Instanzen. Eine dieser Funktionen entspricht dem DirectSound-Renderer, der andere entspricht dem Filter für [audiorenderer (waveout)](audio-renderer--waveout--filter.md) . Die DirectSound-Instanz hat den anzeigen Amen "DirectSound: *DeviceName*", wobei " *DeviceName* " der Name des Geräts ist. Die waveout-Instanz hat den anzeigen Amen " *DeviceName*".

Die Kategorie audiorenderer enthält zwei zusätzliche Filter Instanzen mit dem Namen "Standard-DirectSound-Gerät" und "standardmäßige Wellen Gerät". Diese entsprechen dem Standard-Audiogerät, das der Benutzer über die Systemsteuerung ausgewählt hat. Sie sind tatsächlich Zuordnungen zu einem der im vorherigen Abschnitt beschriebenen Paare. Wenn das System beispielsweise über zwei Audiogeräte (Gerät A und Gerät B) verfügt, enthält die Kategorie audiorenderer Folgendes:

-   Gerät A
-   DirectSound: Gerät A
-   Gerät B
-   DirectSound: Gerät B
-   DirectSound-Standardgerät
-   Standardmäßiges Wellen Gerät

Wenn der Benutzergerät a als Standardgerät ausgewählt hat, entspricht "Standard-DirectSound-Gerät" "DirectSound: Device a" und "standardmäßige Wellen Gerät" dem Gerät "a". Wenn der Benutzergerät B als Standardgerät auswählt, ändern sich diese Zuordnungen.

"DirectSound-Standardgerät" ist einem bevorzugten Verdienst zugewiesen \_ . Die anderen haben einen Verdienst, der \_ \_ nicht verwendet werden kann \_ . Daher wählt Intelligent Connect immer das standardmäßige DirectSound-Gerät aus.

Der DirectSound-rendererfilter unterstützt 3D-Sound durch die DirectSound **IDirectSound3DBuffer** -und **IDirectSound3dListener** -Schnittstellen. Sie können den Filter auch nach den aktuellen Versionen dieser Schnittstellen Abfragen, **IDirectSound3DBuffer8** und **IDirectSound3dListener8**. Führen Sie das Diagramm aus, bevor Sie Methoden für diese Schnittstellen aufrufen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 




