---
description: MPEG-2-Splitter
ms.assetid: 06704a5a-e7ae-4187-ae36-32512d951aaf
title: MPEG-2-Splitter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0f04062660df7711a573dd17deb82f90897454a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104213959"
---
# <a name="mpeg-2-splitter"></a>MPEG-2-Splitter

Ab Microsoft® Windows® XP ist der MPEG-2-Splitter Filter veraltet. Verwenden Sie stattdessen den [MPEG-2-Demultiplexer](mpeg-2-demultiplexer.md) .

Verwenden Sie auf früheren Plattformen den MPEG-2-Splitter für MPEG-2-Programm Datenströme, die im Pullmodus übermittelt wurden und mindestens einen der folgenden Streamtypen enthalten: MPEG-2-Video; MPEG-2-Audiodatei; Nach Definition für DVD-Video codierte AC3-Audiodaten oder PCM-Audiocodierung gemäß Definition für DVD-Video. Dieser Filter analysiert die Streams, erstellt eine Ausgabe-PIN für jeden Stream und gibt die komprimierten MPEG-Audiodaten oder Video Pakete an einen MPEG-2-Decoderfilter aus.

Verwenden Sie für Programm-und Transportstreams, die im Pushmodus übermittelt werden, den [MPEG-2-Demultiplexer](mpeg-2-demultiplexer.md)auf allen Plattformen.

> [!Note]  
> Der MPEG-2-Splitter unterstützt keine Frame genaue Suche.

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Filter Schnittstellen</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>Ibasefilter</strong></a>, <strong>ISpecifyPropertyPages</strong>, <a href="/previous-versions/windows/desktop/api/Amparse/nn-amparse-iamparse"><strong>iamprose</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamselect"><strong>iamstreamselect</strong></a></td>
</tr>
<tr class="even">
<td>Eingabe-PIN-Medientypen</td>
<td><ul>
<li>MEDIATYPE_Stream MEDIASUBTYPE_MPEG2_PROGRAM</li>
<li>MEDIATYPE_Stream MEDIASUBTYPE_MPEG1_Video</li>
<li>MEDIATYPE_Stream MEDIASUBTYPE_NULL</li>
</ul></td>
</tr>
<tr class="odd">
<td>PIN-Eingabeschnittstellen</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>iqualitycontrol</strong></a></td>
</tr>
<tr class="even">
<td>Ausgabe-PIN-Medientypen</td>
<td>Hängt vom Streamtyp ab. Siehe <a href="mpeg-2-splitter-media-types.md">MPEG-2-Splitter Medientypen</a></td>
</tr>
<tr class="odd">
<td>PIN-Schnittstellen</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"> <strong>imediaseeking</strong></a></td>
</tr>
<tr class="even">
<td>CLSID Filtern</td>
<td>CLSID_MMSPLITTER</td>
</tr>
<tr class="odd">
<td>CLSID der Eigenschaften Seite</td>
<td>Nicht verfügbar</td>
</tr>
<tr class="even">
<td>Ausführbare Datei</td>
<td>mpg2splt.ax</td>
</tr>
<tr class="odd">
<td><a href="merit.md">Verdienst</a></td>
<td>MERIT_NORMAL + 1</td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">Filter Kategorie</a></td>
<td>CLSID_AudioInputDeviceCategory</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> <dt>

[Verwenden des MPEG-2-Splitters](using-the-mpeg-2-splitter.md)
</dt> </dl>

 

 



