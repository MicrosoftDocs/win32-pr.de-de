---
description: Zeilen 21-Decoderfilter
ms.assetid: 48fa5484-1f8c-4133-b2e1-888cb1834402
title: Zeilen 21-Decoderfilter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 839a6ff8e77f4815b74f5de65b8f0e2a565cdc2a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106344318"
---
# <a name="line-21-decoder-filter"></a>Zeilen 21-Decoderfilter

Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

Dieser Zeile 21-Decoderfilter decodiert Daten der Zeile 21 und zeichnet den Beschriftungs Text auf Bitmaps.

Die eingabepin stellt eine Verbindung mit einem beliebigen Zeilen 21-Datenanbieter her, in der Regel entweder ein DVD-Video Decoder oder der [CC-Decoder](cc-decoder-filter.md) Der CC-Decoder stellt Zeilen 21-Daten aus der VBI eines analogen Fernsehsignals bereit. Die Ausgabepin stellt eine Verbindung mit einer sekundären PIN auf dem [Overlay-Mixer](overlay-mixer-filter.md) oder einem anderen Videorenderer her, z. b. VMR.

Dieser Filter akzeptiert Zeile 21-Daten im Standard Byte-paar-Format oder als Paket für die ganze Gruppe von Bildern (GOP) als Paket. Für jeden GOP im DVD-Videodaten Strom kann ein Benutzerdaten Paket vorhanden sein, das über die Header Informationen des jeweiligen GOP und die Zeile 21 verfügt. Das Format der Byte-Paare wird im Standardwert von "EIA/CEA-608-B" definiert. Weitere Informationen finden Sie unter diesem Standard.

Zwei Versionen dieses Filters sind verfügbar:



| Filter            | CLSID                 |
|-------------------|-----------------------|
| Zeile 21-Decoder   | CLSID- \_ Line21Decoder  |
| Zeile 21-Decoder 2 | CLSID- \_ Line21Decoder2 |



 

Der Filter Version 1 wird auf den Plattformen Microsoft® Windows® 95/98/Me und Windows 2000 verwendet. Der Filter Version 2 ist in Microsoft Windows XP und höher verfügbar und wird immer dann verwendet, wenn der Video Mischungs-Renderer im Diagramm angezeigt wird.

Die Informationen in der folgenden Tabelle gelten für beide Versionen des Filters:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Filter Schnittstellen</td>
<td><a href="/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder"><strong>IAMLine21Decoder</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"> <strong>ibasefilter</strong></a></td>
</tr>
<tr class="even">
<td>Eingabe-PIN-Medientypen</td>
<td>Haupttyp: MEDIATYPE_AUXLine21DataSubtype:<br/>
<ul>
<li>MEDIASUBTYPE_Line21_BytePair (Standardzeile 21)</li>
<li>MEDIASUBTYPE_Line21_GOPPacket (DVD-Zeile 21)</li>
</ul>
Formattyp: FORMAT_VideoInfo oder GUID_NULL<br/></td>
</tr>
<tr class="odd">
<td>PIN-Eingabeschnittstellen</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>iqualitycontrol</strong></a></td>
</tr>
<tr class="even">
<td>Ausgabe-PIN-Medientypen</td>
<td>Haupttyp: MEDIATYPE_VideoSubtype:<br/>
<ul>
<li>MEDIASUBTYPE_RGB8</li>
<li>MEDIASUBTYPE_RGB555</li>
<li>MEDIASUBTYPE_RGB565</li>
<li>MEDIASUBTYPE_RGB24</li>
<li>MEDIASUBTYPE_RGB32</li>
</ul>
Formattyp: FORMAT_VideoInfo<br/></td>
</tr>
<tr class="odd">
<td>PIN-Schnittstellen</td>
<td><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>Imediaposition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>imediaseeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>iqualitycontrol</strong></a></td>
</tr>
<tr class="even">
<td>CLSID Filtern</td>
<td>Siehe vorherige Tabelle</td>
</tr>
<tr class="odd">
<td>CLSID der Eigenschaften Seite</td>
<td>Keine</td>
</tr>
<tr class="even">
<td>Ausführbare Datei</td>
<td>qdvd.dll</td>
</tr>
<tr class="odd">
<td><a href="merit.md">Verdienst</a></td>
<td>Zeile 21-Decoder: MERIT_NORMALLine 21 Decoder 2: MERIT_NORMAL + 2<br/></td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">Filter Kategorie</a></td>
<td>CLSID_LegacyAmFilterCategory</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> <dt>

[Untertitel und Teletext](closed-captions-and-teletext.md)
</dt> <dt>

[Konfiguration des DVD-Filter Diagramms](dvd-filter-graph-configuration.md)
</dt> </dl>

 

 




