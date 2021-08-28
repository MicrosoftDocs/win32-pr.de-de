---
description: DirectSound-Rendererfilter
ms.assetid: ec6cc790-8c1f-4de4-a7ca-a7073894380e
title: DirectSound-Rendererfilter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efc1dbd6fc39e7e102cbcd5d25075be6bf86bcc8
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983843"
---
# <a name="directsound-renderer-filter"></a>DirectSound-Rendererfilter

Dieser Filter rendert Audio mit DirectSound. Dieser Filter ist derzeit der Standardaudiorenderer für Waveform-Sound.

Zusätzlich zu den grundlegenden Soundrenderingfunktionen kann dieser Filter DirectSound-API-Aufrufe verarbeiten. Verwenden Sie die [**IAMDirectSound-Methoden,**](/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound) um das Fenster für die Soundwiedergabe zu festlegen und abzurufen. Der DirectSound-Audiorenderer ist der Standardfilter für das Audiorendering für DirectShow.




| Bezeichnung | Wert |
|--------|-------|
| Filterschnittstellen | <a href="/windows/desktop/api/Strmif/nn-strmif-iamaudiorendererstats"><strong>IAMAudioRendererStats</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamclockslave"><strong>IAMClockSklave</strong></a>, <a href="/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound"><strong>IAMDirectSound</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol"><strong>IAMResourceControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Control/nn-control-ibasicaudio"><strong>IBasicAudio</strong></a>, <strong>IDirectSound3DBuffer</strong>, <strong>IDirectSound3dListener</strong>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ireferenceclock"><strong>IReferenceClock</strong></a> | 
| Eingabepin-Medientypen | Haupttyp: MEDIATYPE_AudioSubtypes:<br /><ul><li>MEDIASUBTYPE_PCM</li><li>MEDIASUBTYPE_IEEE_FLOAT</li><li>MEDIASUBTYPE_DOLBY_AC3_SPDIF</li><li>MEDIASUBTYPE_RAW_SPORT</li><li>MEDIASUBTYPE_SPDIF_TAG_241h</li><li>MEDIASUBTYPE_DRM_Audio</li></ul>Formattyp: FORMAT_WaveFormatEx<br /> | 
| Eingabepinschnittstellen | <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>IPinConnection</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | 
| Ausgabepin-Medientypen | Nicht zutreffend | 
| Ausgabe-PIN-Schnittstellen | Nicht zutreffend | 
| Filtern der CLSID | CLSID_DSoundRender | 
| Eigenschaftenseite CLSID | CLSID_AudioProperties, CLSID_AudioRendererAdvancedProperties | 
| Ausführbare Datei | quartz.dll | 
| <a href="merit.md">Verdienst</a> | MERIT_PREFERRED | 
| <a href="filter-categories.md">Filterkategorie</a> | CLSID_AudioRendererCategory | 




 

## <a name="remarks"></a>Bemerkungen

Dieser Filter fungiert als Wrapper für ein Audiogerät. Verwenden Sie zum Aufzählen der auf dem System des Benutzers verfügbaren Audiogeräte die [**ICreateDevEnum-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum) mit der Audiorendererkategorie (CLSID \_ AudioRendererCategory). Für jedes Audiogerät enthält die Kategorie des Audiorenderers zwei Filterinstanzen. Eine davon entspricht dem DirectSound-Renderer, die andere dem Filter [Audiorenderer (WaveOut).](audio-renderer--waveout--filter.md) Die DirectSound-Instanz hat den Benutzerfreundlichen Namen "DirectSound: *DeviceName",* wobei *DeviceName* der Name des Geräts ist. Die WaveOut-Instanz hat den Benutzerfreundlichen *Namen DeviceName.*

Die Kategorie "Audiorenderer" enthält zwei zusätzliche Filterinstanzen namens "Default DirectSound Device" und "Default WaveOut Device". Diese entsprechen dem Standardklanggerät, das vom Benutzer über die Systemsteuerung. Sie sind tatsächlich Zuordnungen zu einem der im vorherigen Absatz beschriebenen Paare. Wenn das System beispielsweise über zwei Audiogeräte verfügt: Gerät A und Gerät B, enthält die Kategorie des Audiorenderers Folgendes:

-   Gerät A
-   DirectSound: Gerät A
-   Gerät B
-   DirectSound: Gerät B
-   DirectSound-Standardgerät
-   WaveOut-Standardgerät

Wenn der Benutzer Gerät A als Standardgerät ausgewählt hat, entspricht "DirectSound-Standardgerät" "DirectSound: Gerät A", und "Standard-WaveOut-Gerät" entspricht "Gerät A". Wenn der Benutzer Gerät B als Standardgerät auswählt, ändern sich diese Zuordnungen.

"Default DirectSound Device" (DirectSound-Standardgerät) ist ein Vorteil von PREFERRED \_ PREFERRED zugewiesen. Die anderen haben sich für DIE VERWENDUNG VON NICHT \_ \_ \_ VERWENDET. Daher wählt Intelligent Verbinden immer das DirectSound-Standardgerät aus.

Der DirectSound-Rendererfilter unterstützt 3D-Sound über die DirectSound **IDirectSound3DBuffer-** und **IDirectSound3dListener-Schnittstellen.** Sie können den Filter auch nach den aktuellen Versionen dieser Schnittstellen abfragen: **IDirectSound3DBuffer8** und **IDirectSound3dListener8.** Führen Sie das Diagramm aus, bevor Sie Methoden für diese Schnittstellen aufrufen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 




