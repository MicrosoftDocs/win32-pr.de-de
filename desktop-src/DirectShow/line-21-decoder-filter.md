---
description: Zeilen-21-Decoderfilter
ms.assetid: 48fa5484-1f8c-4133-b2e1-888cb1834402
title: Zeilen-21-Decoderfilter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9951cd8e6093131d45597d1a89c32c36222eb20a
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122986463"
---
# <a name="line-21-decoder-filter"></a>Zeilen-21-Decoderfilter

Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

Dieser Line 21-Decoderfilter decodiert Daten aus Zeile 21 und zeichnet den Beschriftungstext auf Bitmaps.

Der Eingabepin stellt eine Verbindung mit einem beliebigen Datenanbieter der Zeile 21 (in der Regel entweder mit einem DVD-Videodecoder oder dem [CC-Decoderfilter)](cc-decoder-filter.md) sicher. Der CC-Decoder stellt Zeilen 21-Daten aus der VBI eines analogen Fernsehsignals zurEntbindung. Der Ausgabepin stellt eine Verbindung mit einem sekundären Pin auf dem [Overlay-Mixer](overlay-mixer-filter.md) oder mit einem anderen Videorenderer, z. B. dem VMR, wieder.

Dieser Filter akzeptiert Zeilen 21-Daten im Standard-Bytepaarformat oder bei DVD als Paket für die gesamte Bildgruppe (GOP). Für jeden GOP im DVD-Videostream kann ein Benutzerdatenpaket mit den Headerinformationen und Den 21-Daten dieses GOP enthalten sein. Das Format der Bytepaare ist im EIA/CEA-608-B-Standard definiert. Weitere Informationen finden Sie in diesem Standard.

Es sind zwei Versionen dieses Filters verfügbar:



| Filtern            | CLSID                 |
|-------------------|-----------------------|
| Line 21-Decoder   | CLSID \_ Line21Decoder  |
| Zeile 21 Decoder 2 | CLSID \_ Line21Decoder2 |



 

Der Filter der Version 1 wird auf Microsoft® Windows® 95/98/Me- und Windows 2000-Plattformen verwendet. Der Filter der Version 2 ist in Microsoft Windows XP und höher verfügbar und wird immer dann verwendet, wenn sich der Renderer für das Mischen von Videos im Diagramm befindet.

Die Informationen in der folgenden Tabelle gelten für beide Versionen des Filters:




| Bezeichnung | Wert |
|--------|-------|
| Filterschnittstellen | <a href="/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder"><strong>IAMLine21Decoder,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"> <strong>IBaseFilter</strong></a> | 
| Eingabepin-Medientypen | Haupttyp: MEDIATYPE_AUXLine21DataSubtype:<br /><ul><li>MEDIASUBTYPE_Line21_BytePair (Standardzeile 21)</li><li>MEDIASUBTYPE_Line21_GOPPacket (DVD-Zeile 21)</li></ul>Formattyp: FORMAT_VideoInfo oder GUID_NULL<br /> | 
| Eingabepinschnittstellen | <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | 
| Ausgabepin-Medientypen | Haupttyp: MEDIATYPE_VideoSubtype:<br /><ul><li>MEDIASUBTYPE_RGB8</li><li>MEDIASUBTYPE_RGB555</li><li>MEDIASUBTYPE_RGB565</li><li>MEDIASUBTYPE_RGB24</li><li>MEDIASUBTYPE_RGB32</li></ul>Formattyp: FORMAT_VideoInfo<br /> | 
| Ausgabe-PIN-Schnittstellen | <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | 
| Filtern der CLSID | Siehe vorherige Tabelle | 
| Eigenschaftenseite CLSID | Keine | 
| Ausführbare Datei | qdvd.dll | 
| <a href="merit.md">Verdienst</a> | Zeile 21-Decoder: MERIT_NORMALLine 21-Decoder 2: MERIT_NORMAL + 2<br /> | 
| <a href="filter-categories.md">Filterkategorie</a> | CLSID_LegacyAmFilterCategory | 




 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> <dt>

[Untertitel und Teletext](closed-captions-and-teletext.md)
</dt> <dt>

[DVD-Filter Graph Konfiguration](dvd-filter-graph-configuration.md)
</dt> </dl>

 

 




