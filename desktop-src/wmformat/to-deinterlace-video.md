---
title: Zum deinterlace-Video
description: Zum deinterlace-Video
ms.assetid: 60e6af09-fde1-4e4a-b54c-4923c0549b6b
keywords:
- Windows Media-Format-SDK, Deinterlacing-Video
- SDK für Windows Media-Format, Inverse Telecine
- Windows Media-Format-SDK, telecine
- Advanced Systems Format (ASF), Deinterlacing-Video
- ASF (Advanced Systems Format), Deinterlacing-Video
- Advanced Systems Format (ASF), Inverse Telecine
- ASF (Advanced Systems Format), Inverse Telecine
- Advanced Systems Format (ASF), telecine
- ASF (Advanced Systems Format), telecine
- Deinterlacing-Video
- Inverse Telecine, Informationen zu
- Telecine, Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 580b8425e5807fefdfa889fcd08deedb4143cf39
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104038570"
---
# <a name="to-deinterlace-video"></a>Zum deinterlace-Video

Einige Videoquellen, z. b. Video Erfassungs Karten, liefern Videodaten für die Zeilen Sprung Anzeige. Jeder Frame mit Zeilen Sprung Video besteht aus zwei Feldern. Das oberste Feld enthält die erste Zeile des Videos und anschließend jede andere Zeile. Das untere Feld enthält die zweite Zeile des Videos und anschließend jede andere Zeile. Ein Feld enthält also alle gerade nummerierten Zeilen, das andere enthält alle ungeraden nummerierten Zeilen. Die Felder, die einen Frame bilden, stellen etwas andere Präsentations Zeiten dar, sodass Sie bei überlappenden Daten kein statisches Bild bilden.

Wenn Sie ein Video auf einem Computermonitor anzeigen möchten, sollte jeder Frame des Videos als ein Bild angezeigt werden (diese Methode zum Anzeigen eines gesamten Frame Bilds wird als *progressives* Video bezeichnet). Wenn Sie das Video mit Zeilen Sprung progressiv anzeigen, werden die Frames aufgrund des Zeitunterschieds zwischen den beiden Feldern möglicherweise nicht richtig angezeigt. Der Windows Media Video Codec und der Windows Media Video Advanced Profile Codec unterstützen beide eine Vorverarbeitungs Funktion, mit der Zeilen Sprung Inhalte in progressive Frames konvertiert werden.

Um das Eingabe Video "Codec Deinterlacing" zu erhalten, geben Sie die [**IWMWriterAdvanced2::**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) *-Methode ein. Die zu verwendende Einstellung ist g \_ wszdeinterlacemode. Legen Sie den Deinterlacing-Modus auf einen der folgenden Werte fest.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Wert</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WM_DM_NOTINTERLACED</td>
<td>Die Eingabe ist progressiv. Verwenden Sie diese Einstellung, um Deinterlacing zu beenden, wenn Sie zuvor den Deinterlacing-Modus auf einen anderen Wert festgelegt haben.</td>
</tr>
<tr class="even">
<td>WM_DM_DEINTERLACE_NORMAL</td>
<td>Wählen Sie diesen Modus aus, um die geraden und ungeraden Felder eines Zeilen Sprung Rahmens (mit einem Bewegungs Kompensationsmechanismus) zu mischen. Davon<br/>
<ul>
<li>Die interspitze Artefakte der progressiven Anzeige werden erheblich reduziert.</li>
<li>Der Windows Media Video Codec erzeugt komprimierte Videos mit höherer Qualität.</li>
</ul></td>
</tr>
<tr class="odd">
<td>WM_DM_DEINTERLACE_HALFSIZE</td>
<td>Wählen Sie diesen Modus aus, wenn die Ausgabeauflösung die Hälfte oder weniger der Eingabe Auflösung ist. Verwenden Sie diesen Modus z. b., wenn die Eingabe Videoauflösung 640 x 480 Pixel und die Ausgabevideo Auflösung 320 x 240 Pixel ist. Davon<br/>
<ul>
<li>Die interspitze Artefakte der progressiven Anzeige werden erheblich reduziert.</li>
</ul></td>
</tr>
<tr class="even">
<td>WM_DM_DEINTERLACE_HALFSIZEDOUBLERATE</td>
<td>Wählen Sie diesen Modus aus, wenn die Ausgabeauflösung die Hälfte oder weniger der Eingabe Auflösung und die Ausgabe <a href="wmformat-glossary.md"><em>Frame Rate</em></a> doppelt so hoch ist. Verwenden Sie diesen Modus z. b., wenn die Eingabe Videoauflösung 640 x 480 Pixel bei 30 überschneidenden Frames/Sek. und die Ausgabevideo Auflösung 320 x 240 Pixel bei 60 Frames/Sek. Davon<br/>
<ul>
<li>Dies erzeugt progressive Frames mit hoher Qualität, da jedes Feld in einen Frame konvertiert wird, sodass keine Informationen in die Mischung einbezogen werden müssen.</li>
<li>Die vollständige Bewegung der Zeilen Sprung Felder wird aufgezeichnet.</li>
</ul></td>
</tr>
<tr class="odd">
<td>WM_DM_DEINTERLACE_INVERSETELECINE</td>
<td>Wählen Sie diesen Modus aus, um ein Video mit einer Textliste von 30 Frames/s in die 24 Frames/Sek. des ursprünglichen Films zu konvertieren. Davon<br/>
<ul>
<li>Die Komprimierungs Qualität verbessert sich erheblich, da nur 24 Frames/Sek. anstelle von 30 Frames/Sek. erforderlich sind.</li>
<li>Da das Ergebnis progressiv ist, werden die gleichen Komprimierungs-und Anzeige Vorteile von Deinterlacing erkannt.</li>
</ul></td>
</tr>
<tr class="even">
<td>WM_DM_DEINTERLACE_VERTICALHALFSIZEDOUBLERATE</td>
<td>Wählen Sie diesen Modus aus, wenn die vertikale Ausgabeauflösung mindestens die Hälfte der Eingabe vertikalen Auflösung und die Ausgabe <a href="wmformat-glossary.md"><em>Frame Rate</em></a> doppelt so hoch ist. Beispielsweise ist die Eingabe vertikale Videoauflösung 640 x 480 Pixel bei 30 Zeilen Sprung Bildern/Sek. und die vertikale Ausgabe des vertikalen Videos beträgt 320 x 240 Pixel bei 60 Frames/Sek. Davon<br/>
<ul>
<li>Dies erzeugt progressive Frames mit hoher Qualität, da jedes Feld in einen Frame konvertiert wird, sodass keine Informationen in die Mischung einbezogen werden müssen.</li>
<li>Die vollständige Bewegung der Zeilen Sprung Felder wird aufgezeichnet.</li>
</ul></td>
</tr>
</tbody>
</table>



 

Legen Sie für gemischten Inhalt den Deinterlacing-Modus nach Bedarf fest, bevor Sie die Beispiele eines neuen Typs übergeben. Wenn Sie z. b. die Codierung mit progressiver Eingabe starten möchten, müssen Sie keinen Deinterlacing-Modus festlegen. Wenn einige Beispiele ein normales Deinterlacing erfordern, müssen Sie den Deinterlacing-Modus auf WM \_ DM \_ deinterlace \_ Normal festlegen. Um zusätzliche Progressive Beispiele zu verarbeiten, müssen Sie den Deinterlacing-Modus auf WM \_ DM \_ notinterlacing festlegen.

## <a name="inverse-telecine-settings"></a>Umgekehrte telecine-Einstellungen

Eine Beschreibung der Inverse Telecine finden [Sie unter So verwenden Sie die umgekehrte telecine](to-use-inverse-telecine.md).

Wenn Sie den Deinterlacing-Modus auf WM \_ DM \_ deinterlace \_ inversetelecine festgelegt haben, können Sie das telecine-Muster des ersten Eingabe Rahmens durch Aufrufen von [**IWMWriterAdvanced2:: setinputsetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting)angeben. Die zu verwendende Einstellung ist g \_ wszinitialpatternforinvertartelecine. Legen Sie das Anfangs Muster auf einen der folgenden Werte fest.



| Wert                                              | BESCHREIBUNG                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WM- \_ DM- \_ Aktivierung ( \_ \_ kohärenter \_ Modus)                | Gibt an, dass die Eingabemedien den telecine-Prozess durchlaufen haben, die Rahmen jedoch nicht mehr in einem vorhersagbaren Muster vorliegen. Dies weist normalerweise darauf hin, dass das Medium nach der telecine-Verarbeitung bearbeitet wurde. Wenn Sie diese Einstellung verwenden, versucht der Codec, die ursprünglichen Frames eigenständig zu rekonstruieren. |
| WM \_ DM \_ \_ der erste \_ Frame \_ in \_ Clip \_ ist \_ AA \_ Top    | Gibt an, dass das oberste Feld des AA-Frames das erste Beispiel ist.                                                                                                                                                                                                                                             |
| WM \_ DM \_ \_ der erste \_ Frame \_ in \_ Clip \_ ist \_ BB \_ Top    | Gibt an, dass das oberste Feld des BB-Frames das erste Beispiel ist.                                                                                                                                                                                                                                             |
| WM \_ DM \_ \_ der erste \_ Frame \_ in \_ Clip \_ ist \_ BC \_ Top    | Gibt an, dass das oberste Feld des BC-Frames das erste Beispiel ist.                                                                                                                                                                                                                                             |
| WM \_ DM \_ \_ der erste \_ Frame \_ in \_ Clip \_ ist \_ CD \_ Top    | Gibt an, dass das oberste Feld des CD-Frames das erste Beispiel ist.                                                                                                                                                                                                                                             |
| WM \_ DM \_ \_ der erste \_ Frame \_ in \_ Clip \_ ist \_ DD \_ Top    | Gibt an, dass das oberste Feld des DD-Frames das erste Beispiel ist.                                                                                                                                                                                                                                             |
| WM \_ DM \_ \_ der erste \_ Frame \_ in \_ Clip \_ ist \_ AA \_ unten | Gibt an, dass das untere Feld des AA-Frames das erste Beispiel ist.                                                                                                                                                                                                                                          |
| WM \_ DM \_ \_ der erste \_ Frame \_ in \_ Clip \_ ist \_ BB \_ unten | Gibt an, dass das untere Feld des BB-Frames das erste Beispiel ist.                                                                                                                                                                                                                                          |
| WM \_ DM \_ \_ der erste \_ Frame \_ in \_ Clip \_ ist \_ BC \_ Bottom | Gibt an, dass das untere Feld des BC-Frames das erste Beispiel ist.                                                                                                                                                                                                                                          |
| WM \_ DM \_ \_ der erste \_ Frame \_ in \_ Clip \_ ist \_ CD \_ unten | Gibt an, dass das untere Feld des CD-Frames das erste Beispiel ist.                                                                                                                                                                                                                                          |
| WM \_ DM \_ \_ der erste \_ Frame \_ im \_ Clip \_ ist \_ TT \_ unten | Gibt an, dass das untere Feld des DD-Frames das erste Beispiel ist.                                                                                                                                                                                                                                          |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erweiterte Themen**](advanced-topics.md)
</dt> </dl>

 

 





