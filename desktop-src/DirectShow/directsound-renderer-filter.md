---
description: DirectSound-Rendererfilter
ms.assetid: ec6cc790-8c1f-4de4-a7ca-a7073894380e
title: DirectSound-Rendererfilter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b601c0e85169857cd628b3b3e55b5c00af8ea11
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481576"
---
# <a name="directsound-renderer-filter"></a>DirectSound-Rendererfilter

Dieser Filter rendert Audio mit DirectSound. Dieser Filter ist derzeit der Standardaudiorenderer für Waveform-Sound.

Zusätzlich zu den grundlegenden Soundrenderingfunktionen kann dieser Filter DirectSound-API-Aufrufe verarbeiten. Verwenden Sie die [**IAMDirectSound-Methoden,**](/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound) um das Fenster festzulegen und abzurufen, das die Soundwiedergabe verarbeitet. Der DirectSound-Audiorenderer ist der Standardfilter für das Audiorendering für DirectShow.




| | | Filterschnittstellen | <a href="/windows/desktop/api/Strmif/nn-strmif-iamaudiorendererstats"><strong>IAMAudioRendererStats,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iamclockslave"><strong>IAMClockSlave,</strong></a> <a href="/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound"><strong>IAMDirectSound,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol"><strong>IAMResourceControl,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter,</strong></a> <a href="/windows/desktop/api/Control/nn-control-ibasicaudio"><strong>IBasicAudio,</strong></a> <strong>IDirectSound3DBuffer,</strong> <strong>IDirectSound3dListener,</strong> <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ireferenceclock"><strong>IReferenceClock</strong></a> | | Eingabepinmedientypen | Haupttyp: MEDIATYPE_AudioSubtypes:<br /><ul><li>MEDIASUBTYPE_PCM</li><li>MEDIASUBTYPE_IEEE_FLOAT</li><li>MEDIASUBTYPE_DOLBY_AC3_SPDIF</li><li>MEDIASUBTYPE_RAW_SPORT</li><li>MEDIASUBTYPE_SPDIF_TAG_241h</li><li>MEDIASUBTYPE_DRM_Audio</li></ul>Formattyp: FORMAT_WaveFormatEx<br /> | | Eingabepinschnittstellen | <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>IPinConnection,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | | Ausgabepinmedientypen | Nicht zutreffend. | | Ausgabepinschnittstellen | Nicht zutreffend. | | Filtern von CLSID-| CLSID_DSoundRender | | CLSID-| der Eigenschaftenseite CLSID_AudioProperties, CLSID_AudioRendererAdvancedProperties | | Ausführbare | quartz.dll | | <a href="merit.md">|</a> MERIT_PREFERRED | | <a href="filter-categories.md">| "Filterkategorie"</a> CLSID_AudioRendererCategory | 




 

## <a name="remarks"></a>Hinweise

Dieser Filter fungiert als Wrapper für ein Audiogerät. Um die auf dem System des Benutzers verfügbaren Audiogeräte aufzuzählen, verwenden Sie die [**ICreateDevEnum-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum) mit der Audiorendererkategorie (CLSID \_ AudioRendererCategory). Für jedes Audiogerät enthält die Audiorendererkategorie zwei Filterinstanzen. Eine davon entspricht dem DirectSound-Renderer und die andere dem [Filter Audio Renderer (WaveOut).](audio-renderer--waveout--filter.md) Die DirectSound-Instanz hat den Anzeigenamen "DirectSound: *DeviceName",* wobei *DeviceName* der Name des Geräts ist. Die WaveOut-Instanz hat den Anzeigenamen *DeviceName*.

Die Audiorendererkategorie enthält zwei zusätzliche Filterinstanzen mit den Namen "Default DirectSound Device" und "Default WaveOut Device". Diese entsprechen dem Standard-Soundgerät, das vom Benutzer über die Systemsteuerung ausgewählt wurde. Sie sind tatsächlich Zuordnungen zu einem der im vorherigen Absatz beschriebenen Paare. Wenn das System beispielsweise über zwei Audiogeräte verfügt: Gerät A und Gerät B, enthält die Kategorie Audiorenderer Folgendes:

-   Gerät A
-   DirectSound: Gerät A
-   Gerät B
-   DirectSound: Gerät B
-   DirectSound-Standardgerät
-   WaveOut-Standardgerät

Wenn der Benutzer Gerät A als Standardgerät ausgewählt hat, entspricht "DirectSound-Standardgerät" "DirectSound: Gerät A" und "Default WaveOut Device" "Device A". Wenn der Benutzer Gerät B als Standardgerät auswählt, ändern sich diese Zuordnungen.

"Default DirectSound Device" wird ein Leistungswert von PREFER \_ PREFERRED zugewiesen. Die anderen haben sich für DIE VERWENDUNG VON "USE \_ \_ DO NOT \_ USE" (NICHT VERWENDEN) eingesetzt. Daher wählt Intelligent Verbinden immer das DirectSound-Standardgerät aus.

Der Filter DirectSound Renderer unterstützt 3D-Sound über die Schnittstellen DirectSound **IDirectSound3DBuffer** und **IDirectSound3dListener.** Sie können auch den Filter für die aktuellen Versionen dieser Schnittstellen abfragen: **IDirectSound3DBuffer8** und **IDirectSound3dListener8.** Führen Sie das Diagramm aus, bevor Sie Methoden für diese Schnittstellen aufrufen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 




