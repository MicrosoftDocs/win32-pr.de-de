---
description: Renderer Filter für internen Skript Befehl
ms.assetid: 264cc7c3-987c-4832-85a2-087278a4d024
title: Renderer Filter für internen Skript Befehl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b241643d991e9348015dc51ea5b2f1c4875f079d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521595"
---
# <a name="internal-script-command-renderer-filter"></a>Renderer Filter für internen Skript Befehl

Empfängt Skript Befehle und sendet Sie an die Anwendung.

Dieser Filter akzeptiert Skript Befehle in einem von zwei Formaten:

-   MediaType \_ Text: jedes Medien Beispiel enthält eine ANSI-Text Zeichenfolge.
-   MediaType \_ ScriptCommand: jedes Medien Beispiel enthält zwei mit NULL endenden Unicode-Zeichen folgen, die zusammen verkettet sind. Die erste Zeichenfolge beschreibt den Befehlstyp, und die zweite Zeichenfolge ist der Skript Befehl.

    Wenn der Filter ein Beispiel empfängt, sendet er eine Ereignis Benachrichtigung für das [**EC- \_ OLE- \_ Ereignis**](ec-ole-event.md) . Der erste Ereignis Parameter ist ein **BSTR** mit dem Befehlstyp oder, `Text` Wenn das Format MediaType \_ Text ist. Der zweite Ereignis Parameter ist ein **BSTR** mit dem Skript Befehl. Die Anwendung kann das Ereignis abrufen und auf den Skript Befehl reagieren.

Ein Beispiel für die Verwendung dieses Filters finden Sie unter [Sami (CC)-Parser](sami--cc--parser-filter.md).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Filter Schnittstellen</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>Ibasefilter</strong></a>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>imediaposition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>imediaseeking</strong></a></td>
</tr>
<tr class="even">
<td>Eingabe-PIN-Medientypen</td>
<td><ul>
<li>MEDIATYPE_ScriptCommand MEDIASUBTYPE_NULL</li>
<li>MEDIATYPE_Text MEDIASUBTYPE_NULL</li>
</ul></td>
</tr>
<tr class="odd">
<td>PIN-Eingabeschnittstellen</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>iqualitycontrol</strong></a></td>
</tr>
<tr class="even">
<td>Ausgabe-PIN-Medientypen</td>
<td>Nicht verfügbar</td>
</tr>
<tr class="odd">
<td>PIN-Schnittstellen</td>
<td>Nicht verfügbar</td>
</tr>
<tr class="even">
<td>CLSID Filtern</td>
<td>{48025243-2d39-11CE-875d-00608cb78066}</td>
</tr>
<tr class="odd">
<td>CLSID der Eigenschaften Seite</td>
<td>Keine Eigenschaften Seite</td>
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



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 



