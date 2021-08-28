---
description: Zeilen-21-Decoderfilter
ms.assetid: 48fa5484-1f8c-4133-b2e1-888cb1834402
title: Zeilen-21-Decoderfilter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b0668d4b71b8dcccf4ceacf7f5428fa7a65ad52
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468237"
---
# <a name="line-21-decoder-filter"></a>Zeilen-21-Decoderfilter

Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

Dieser Filter des Line 21-Decoders decodiert Zeilen 21-Daten und zeichnet den Beschriftungstext auf Bitmaps.

Der Eingabepin stellt eine Verbindung mit einem beliebigen Datenanbieter der Zeile 21 her, in der Regel entweder ein DVD-Videodecoder oder der [CC-Decoderfilter.](cc-decoder-filter.md) Der CC-Decoder stellt Daten der Zeile 21 der VBI eines analogen Fernsehsignals bereit. Der Ausgabepin stellt eine Verbindung mit einem sekundären Pin auf dem [Overlay-Mixer](overlay-mixer-filter.md) oder mit einem anderen Videorenderer her, z. B. der VMR.

Dieser Filter akzeptiert Zeilen-21-Daten im Standard-Bytepaarformat oder für DVD als Paket für die gesamte Gruppe von Bildern (GOP). Für jeden GOP im DVD-Videostream kann ein Benutzerdatenpaket vorhanden sein, das die Headerinformationen des jeweiligen GOP und die Daten der Zeile 21 enthält. Das Format der Bytepaare wird im EIA/CEA-608-B-Standard definiert. Weitere Informationen finden Sie in diesem Standard.

Zwei Versionen dieses Filters sind verfügbar:



| Filter            | CLSID                 |
|-------------------|-----------------------|
| Line 21 Decoder   | CLSID \_ Line21Decoder  |
| Zeile 21 Decoder 2 | CLSID \_ Line21Decoder2 |



 

Der Filter der Version 1 wird auf Microsoft® Windows® 98.05.2000 und Windows 2000-Plattformen verwendet. Der Filter der Version 2 ist in Microsoft Windows XP und höher verfügbar und wird immer dann verwendet, wenn sich der Videomischungsrenderer im Diagramm befindet.

Die Informationen in der folgenden Tabelle gelten für beide Versionen des Filters:




| | | Filterschnittstellen | <a href="/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder"><strong>IAMLine21Decoder</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a> | | Eingabepinmedientypen | Haupttyp: MEDIATYPE_AUXLine21DataSubtype:<br /><ul><li>MEDIASUBTYPE_Line21_BytePair (Standardzeile 21)</li><li>MEDIASUBTYPE_Line21_GOPPacket (DVD-Zeile 21)</li></ul>Formattyp: FORMAT_VideoInfo oder GUID_NULL<br /> | | Eingabepinschnittstellen | <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | | Ausgabepinmedientypen | Haupttyp: MEDIATYPE_VideoSubtype:<br /><ul><li>MEDIASUBTYPE_RGB8</li><li>MEDIASUBTYPE_RGB555</li><li>MEDIASUBTYPE_RGB565</li><li>MEDIASUBTYPE_RGB24</li><li>MEDIASUBTYPE_RGB32</li></ul>Formattyp: FORMAT_VideoInfo<br /> | | Ausgabepinschnittstellen | <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | | Filtern von CLSID-| Siehe vorherige Tabelle | | CLSID-| der Eigenschaftenseite Keine | | Ausführbare | qdvd.dll | | <a href="merit.md">|</a> Line 21 Decoder: MERIT_NORMALLine 21 Decoder 2: MERIT_NORMAL + 2<br /> | | <a href="filter-categories.md">| "Filterkategorie"</a> CLSID_LegacyAmFilterCategory | 




 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> <dt>

[Untertitel und Teletext](closed-captions-and-teletext.md)
</dt> <dt>

[KONFIGURATION DES DVD-Filters Graph](dvd-filter-graph-configuration.md)
</dt> </dl>

 

 




