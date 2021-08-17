---
description: Filter für internen Skriptbefehlsrenderer
ms.assetid: 264cc7c3-987c-4832-85a2-087278a4d024
title: Filter für internen Skriptbefehlsrenderer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58ed1afa417b542b0eabbb7c01b8b8d477b8145809da3339e6b6c80d471a71cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117818687"
---
# <a name="internal-script-command-renderer-filter"></a>Filter für internen Skriptbefehlsrenderer

Empfängt Skriptbefehle und verteilt sie an die Anwendung.

Dieser Filter akzeptiert Skriptbefehle in einem von zwei Formaten:

-   MEDIATYPE \_ Text: Jedes Medienbeispiel enthält eine ANSI-Textzeichenfolge.
-   MEDIATYPE \_ ScriptCommand: Jedes Medienbeispiel enthält zwei mit NULL endende Unicode-Zeichenfolgen, die miteinander verkettet sind. Die erste Zeichenfolge beschreibt den Befehlstyp, und die zweite Zeichenfolge ist der Skriptbefehl.

    Wenn der Filter ein Beispiel empfängt, sendet er eine [**EC \_ OLE \_ EVENT-Ereignisbenachrichtigung.**](ec-ole-event.md) Der erste Ereignisparameter ist ein **BSTR** mit dem Befehlstyp oder `Text` , wenn das Format MEDIATYPE Text \_ ist. Der zweite Ereignisparameter ist ein **BSTR** mit dem Skriptbefehl. Die Anwendung kann das Ereignis abrufen und auf den Skriptbefehl reagieren.

Ein Beispiel für die Verwendung dieses Filters finden Sie unter [SAMI (CC) Parser](sami--cc--parser-filter.md).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Filterschnittstellen</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter,</strong></a> <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></td>
</tr>
<tr class="even">
<td>Eingabepinmedientypen</td>
<td><ul>
<li>MEDIATYPE_ScriptCommand, MEDIASUBTYPE_NULL</li>
<li>MEDIATYPE_Text, MEDIASUBTYPE_NULL</li>
</ul></td>
</tr>
<tr class="odd">
<td>Eingabe-Pin-Schnittstellen</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>Medientypen des Ausgabepins</td>
<td>Nicht verfügbar</td>
</tr>
<tr class="odd">
<td>Ausgabe-Pin-Schnittstellen</td>
<td>Nicht verfügbar</td>
</tr>
<tr class="even">
<td>Filtern von CLSID</td>
<td>{48025243-2D39-11CE-875D-00608CB78066}</td>
</tr>
<tr class="odd">
<td>CLSID der Eigenschaftenseite</td>
<td>Keine Eigenschaftenseite</td>
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
<td><a href="filter-categories.md">Filterkategorie</a></td>
<td>CLSID_LegacyAmFilterCategory</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 



