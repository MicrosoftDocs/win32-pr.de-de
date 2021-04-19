---
title: Stichprobenerweiterungstypen
description: Stichprobenerweiterungstypen
ms.assetid: 8de2e003-cb21-4be9-bcde-7f5909b6260a
keywords:
- Windows Media-Format-SDK, Beispiel Erweiterungen
- Advanced Systems Format (ASF), Beispiel Erweiterungen
- ASF (Advanced Systems Format), Beispiel Erweiterungen
- Windows Media-Format-SDK, Dateneinheiten Erweiterungen
- Advanced Systems Format (ASF), Dateneinheiten Erweiterungen
- ASF (Advanced Systems Format), Dateneinheiten Erweiterungen
- Windows Media-Format-SDK, Puffer Eigenschaften
- Advanced Systems Format (ASF), Puffer Eigenschaften
- ASF (Advanced Systems Format), Puffer Eigenschaften
- Beispiel Erweiterungen, Typen
- Dateneinheiten Erweiterungen, Typen
- Puffer Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 972e3da1ecaad277158bb270cc358436f53db9e2
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2020
ms.locfileid: "106342121"
---
# <a name="sample-extension-types"></a>Stichprobenerweiterungstypen

Beispiel Erweiterungen, die auch als Dateneinheiten Erweiterungen (Gebühren) oder Puffer Eigenschaften bezeichnet werden, sind Elemente von Daten, die an die Medien Beispiele im Data-Abschnitt der ASF-Datei angefügt werden. Verschiedene Typen von Beispiel Erweiterungen werden im Windows Media-Format-SDK definiert. Sie können auch eigene Erweiterungs Typen erstellen.

Um Beispiel Erweiterungen zu verwenden, müssen Sie den Erweiterungstyp in den Datenstrom-Konfigurationsdaten des Profils angeben. Aufrufen der [**IWMStreamConfig2:: adddataunitextension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) -Methode zum Konfigurieren eines Datenstroms, um Beispiele mit erweiterten Daten zu akzeptieren.

Einzelne Beispiel Erweiterungen müssen den Eingabe Beispielen hinzugefügt werden, indem die [**INSSBuffer3:: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) -Methode aufgerufen wird. Beim Lesen von Beispielen können Sie die [**INSSBuffer3:: GetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-getproperty) -Methode aufrufen, um die Erweiterungs Daten abzurufen. Sie können auch die Methoden der [**INSSBuffer4**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer4) -Schnittstelle verwenden, um die an eine Stichprobe angefügten dateneinheits-Erweiterungen aufzuzählen.

In der folgenden Tabelle werden die vordefinierten dateneinheits-Erweiterungs Bezeichner aufgelistet, und es werden die Daten beschrieben, die jeweils an Samples angefügt werden.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>GUID der Beispiel Erweiterung</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WM_SampleExtensionGUID_OutputCleanPoint</td>
<td>Die Daten zeigen an, ob das Beispiel ein <a href="wmformat-glossary.md"><em>Cleanpoint</em></a>ist. Der Wert 0 (null) gibt an, dass das Beispiel kein Cleanpoint ist. Ein Wert ungleich 0 (null) gibt an, dass es sich um einen Cleanpoint handelt. Diese Beispiel Daten-Einheits Erweiterung (Due) wird verwendet, um die Bereinigung von cleanpoints beim Schreiben von vorkomprimierten Mediendaten strömen zu verfolgen, die mit Codecs von Drittanbietern codiert wurden.</td>
</tr>
<tr class="even">
<td>WM_SampleExtensionGUID_Timecode</td>
<td>Bei den Daten handelt es sich um eine <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data"><strong>WMT_TIMECODE_EXTENSION_DATA</strong></a> Struktur, die dem Beispiel zugeordnete SMPTE-Zeit Code Daten enthält. Die Größe für diese Fälligkeit ist immer WM_SampleExtension_Timecode_Size, also 14 Bytes.<br/></td>
</tr>
<tr class="odd">
<td>WM_SampleExtensionGUID_FileName</td>
<td>Diese Art von Beispiel Erweiterung wird für Dateistreams verwendet. Die Daten in einem File Stream-Beispiel sind ein Teil einer Datendatei. Die Daten in der Beispiel Erweiterung geben den Namen der Datei an, aus der der Inhalt in der Stichprobe entnommen wurde. Der Dateiname ist eine Zeichenfolge mit breit Zeichen, die den Dateinamen im Name. Extension-Format ohne Pfadinformationen enthält.<br/></td>
</tr>
<tr class="even">
<td>WM_SampleExtensionGUID_ContentType</td>
<td>Die Daten identifizieren den Inhaltstyp, den das Beispiel enthält. Diese Art von Beispiel Erweiterung wird mit Zeilen Sprung-Videostreams verwendet. Bei allen Zeilen Sprung Inhalten wird das WM_CT_INTERLACED-Flag zusammen mit einem bitweisen <strong>or</strong> mit WM_CT_BOTTOM_FIELD_FIRST, WM_CT_TOP_FIELD_FIRST oder WM_CT_REPEAT_FIRST_FIELD verwendet.<br/> Die Feld Reihenfolge wird nicht im Codierungsprozess verwendet, sondern mit den komprimierten Beispielen verwaltet, sodass Sie an die renderinghardware übermittelt werden kann. Durch die Wiedergabe von Zeilen Sprung Inhalt mit der falschen Feld Reihenfolge werden Artefakte wie Motion Jitter im Video eingeführt.<br/> Die Größe für diese Fälligkeit ist immer WM_SampleExtension_ContentType_Size.<br/></td>
</tr>
<tr class="odd">
<td>WM_SampleExtensionGUID_PixelAspectRatio</td>
<td>Die Daten zeigen das Pixel Seitenverhältnis des Inhalts in der Stichprobe an. Dies gilt nur für Videos. Dieser Erweiterungstyp wird verwendet, um das Seitenverhältnis von nicht quadratischen Pixeln zu identifizieren. Weitere Informationen finden <a href="to-read-and-write-video-streams-with-non-square-pixels.md">Sie unter so lesen und schreiben Sie Videostreams mit nicht quadratischen Pixeln</a>.<br/> Seitenverhältnis Werte werden als Wort gespeichert, dessen niedriges Byte der X-Aspekt und dessen hohes Byte der Y-Aspekt ist. Beispielsweise wird 16:9 als 0x0910 gespeichert.<br/> Die Größe für diese Fälligkeit ist immer WM_SampleExtension_PixelAspectRatio_Size, d. h. 2 Bytes.<br/></td>
</tr>
<tr class="even">
<td>WM_SampleExtensionGUID_SampleDuration</td>
<td>Die Daten zeigen die Dauer (in Millisekunden) des im Buffer-Objekt enthaltenen Beispiels an. Wenn bei der Wiedergabe diese Einstellung festgelegt ist, wird Sie vom Reader-Objekt zum Überschreiben des vorhandenen Sample Duration-Werts verwendet. Dieser Wert wird automatisch durch die SDK-Laufzeitkomponenten in Videostreams mit Bitraten von 100 kbit/s oder höher festgelegt, wobei der Aufwand der fälligen Informationen nicht signifikant ist. Sie ist nicht für Streams mit Bitraten unter 100 kbit/s festgelegt. Anwendungen sollten diesen Wert nicht manuell festlegen, da der Writer (bei hochbitrate-Streams) den Wert mit seinen eigenen Daten überschreibt.<br/> Die Größe für diese Fälligkeit ist immer WM_SampleExtension_SampleDuration_Size, d. h. 2 Bytes.<br/></td>
</tr>
<tr class="odd">
<td>WM_SampleExtensionGUID_ChromaLocation</td>
<td>Die Daten geben den Typ der Chroma-Unterstichprobe an, die im I420-Videoformat verwendet wird. Der Wert dieser Erweiterung wird auf einen der folgenden Werte festgelegt:<br/>
<ul>
<li>WM_CL_INTERLACED420</li>
<li>WM_CL_PROGRESSIVE420</li>
</ul>
Diese Dateneinheiten Erweiterung ist im Profil nicht konfiguriert. Es ist in der Beispielausgabe des Decoders enthalten.<br/> Die Größe dieses fälligen ist immer WM_SampleExtension_ChromaLocation_Size, 1 Byte.<br/></td>
</tr>
<tr class="even">
<td>WM_SampleExtensionGUID_ColorSpaceInfo</td>
<td>Die Daten enthalten Informationen über den für den aktuellen Videoframe verwendeten Farbraum. Der Wert dieser Erweiterung ist eine <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_colorspaceinfo_extension_data"><strong>WMT_COLORSPACEINFO_EXTENSION_DATA</strong></a> Struktur.<br/> Diese Dateneinheiten Erweiterung ist im Profil nicht konfiguriert. Es ist in der Beispielausgabe des Decoders enthalten.<br/> Die Größe dieses fälligen ist immer WM_SampleExtension_ColorSpaceInfo_Size, also 3 Bytes.<br/></td>
</tr>
<tr class="odd">
<td>WM_SampleExtensionGUID_UserDataInfo</td>
<td>Bei den Daten handelt es sich um benutzerdefinierte Benutzerdaten. Die ersten vier Bytes der Daten enthalten die Größe der benutzerdefinierten Daten.<br/> Das nächste Byte enthält den Typ der Benutzerdaten, die in der Beispiel Erweiterung bereitgestellt werden. Die folgenden Typen werden unterstützt:<br/>
<ul>
<li>0x1F-Sequenz Ebene-Benutzerdaten</li>
<li>0x1E-Benutzerdaten auf Einstiegspunkt Ebene</li>
<li>0x1D-Benutzerdaten auf Frame-Ebene</li>
<li>0x1C-Benutzerdaten auf Feldebene</li>
<li>0x1B-Benutzerdaten auf Slice-Ebene</li>
</ul>
Die sechsten und nachfolgenden Bytes enthalten die Benutzerdaten. Es gibt so viele Bytes von Benutzerdaten, wie durch die Zahl in den ersten vier Bytes angegeben.<br/> Diese Dateneinheiten Erweiterung ist im Profil nicht konfiguriert. Es ist in den Beispielen enthalten, die vom Decoder ausgegeben werden.<br/></td>
</tr>
<tr class="even">
<td>WM_SampleExtensionGUID_SampleProtectionSalt</td>
<td>Die Daten werden anhand von Stichproben verschlüsselt. Dieser Beispiel Erweiterungstyp wird für Inhalte verwendet, die aus einem nicht-ASF-Dateiformat und einem anderen Rechte Schutzschema als Windows Media DRM importiert werden. Beim Importieren geschützter Inhalte muss jede Stichprobe einen eindeutigen Salt-Inhalt enthalten. In der Regel handelt es sich bei diesem Wert um einen monoton steigenden Leistungswert.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Programmierverzeichnis**](programming-reference.md)
</dt> </dl>

 

 





