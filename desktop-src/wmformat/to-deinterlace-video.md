---
title: So deinterlace video
description: So deinterlace video
ms.assetid: 60e6af09-fde1-4e4a-b54c-4923c0549b6b
keywords:
- Windows Media Format SDK,deinterlaced video
- Windows Media Format SDK,inverse telecine
- Windows Medienformat-SDK, Telecine
- Advanced Systems Format (ASF), Deinterlaced-Video
- ASF (Advanced Systems Format), Deinterlaced-Video
- Advanced Systems Format (ASF), inverse Telecine
- ASF (Advanced Systems Format), inverse Telecine
- Advanced Systems Format (ASF), telecine
- ASF (Advanced Systems Format), telecine
- Deinterlaced-Video
- inverse Telecine,about
- telecine,about
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4d327ba19ea471f1594410913ebb58f3ac1cfebe048ac418abc7141c1fbee3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118699957"
---
# <a name="to-deinterlace-video"></a>So deinterlace video

Einige Videoquellen, z. B. Videoaufnahmekarten, liefern Videodaten für die Interlaced-Anzeige. Jeder Frame von Interlacingvideos besteht aus zwei Feldern. Das obere Feld enthält die erste Zeile des Videos und jede andere Zeile danach. Das untere Feld enthält die zweite Zeile des Videos und jede andere Zeile danach. Ein Feld enthält also alle gleichmäßig nummerierten Zeilen, das andere alle ungeraden nummerierten Zeilen. Die Felder, aus denen sich ein Frame zusammenbildet, stellen geringfügig unterschiedliche Präsentationszeiten dar, sodass sie bei Überlappung kein statisches Bild bilden.

Wenn Sie Videos auf einem Computermonitor anzeigen möchten, sollte jeder Frame des Videos als ein Bild angezeigt werden  (diese Methode zum Anzeigen des Videos wird als progressives Video bezeichnet. Wenn Sie interlaced video progressiv anzeigen, sehen die Frames aufgrund des Zeitunterschieds zwischen den beiden Feldern möglicherweise nicht richtig aus. Der Windows Media Video-Codec und der Windows Media Video Advanced Profile-Codec unterstützen beide eine Vorverarbeitungsfunktion, die Zwischeninhalte in progressive Frames konvertiert.

Um das Codec-Deinterlace-Eingabevideo zu erhalten, rufen Sie [**die IWMWriterAdvanced2::SetInputSetting-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) auf. Die zu verwendende Einstellung ist g \_ wszDeinterlaceMode. Legen Sie den Deinterlacingmodus auf einen der folgenden Werte fest.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Wert</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WM_DM_NOTINTERLACED</td>
<td>Die Eingabe ist progressiv. Verwenden Sie diese Einstellung, um das Deinterlacing zu beenden, wenn Sie zuvor den Deinterlacingmodus auf einen anderen Wert festgelegt haben.</td>
</tr>
<tr class="even">
<td>WM_DM_DEINTERLACE_NORMAL</td>
<td>Wählen Sie diesen Modus aus, um die gleichmäßigen und ungeraden Felder eines Verschachtelungsrahmens (mithilfe eines Mechanismus zur Bewegungskompensation) zu mischen. Vorteile:<br/>
<ul>
<li>Die Interlace-Artefakte der progressiven Anzeige werden erheblich reduziert.</li>
<li>Der Windows Media Video-Codec erzeugt komprimiertes Video mit höherer Qualität.</li>
</ul></td>
</tr>
<tr class="odd">
<td>WM_DM_DEINTERLACE_HALFSIZE</td>
<td>Wählen Sie diesen Modus aus, wenn die Ausgabeauflösung halb oder kleiner als die Eingabeauflösung ist. Verwenden Sie diesen Modus beispielsweise, wenn die Auflösung des Eingabevideos 640 x 480 Pixel beträgt und die Auflösung des Ausgabevideos 320 x 240 Pixel beträgt. Vorteile:<br/>
<ul>
<li>Die Interlace-Artefakte der progressiven Anzeige werden erheblich reduziert.</li>
</ul></td>
</tr>
<tr class="even">
<td>WM_DM_DEINTERLACE_HALFSIZEDOUBLERATE</td>
<td>Wählen Sie diesen Modus aus, wenn die Ausgabeauflösung halb oder kleiner als die Eingabeauflösung und die Ausgabebildrate <a href="wmformat-glossary.md"><em>doppelt</em></a> so hoch ist. Verwenden Sie diesen Modus beispielsweise, wenn die Auflösung des Eingabevideos 640 x 480 Pixel bei 30 Interlaced Frames/s beträgt und die Ausgabevideoauflösung 320 x 240 Pixel bei 60 Frames/s beträgt. Vorteile:<br/>
<ul>
<li>Dies erzeugt progressive Frames von hoher Qualität, da jedes Feld in einen Frame konvertiert wird und daher keine Informationen gemischt werden müssen.</li>
<li>Die vollständige Bewegung der verschachtelten Felder wird erfasst.</li>
</ul></td>
</tr>
<tr class="odd">
<td>WM_DM_DEINTERLACE_INVERSETELECINE</td>
<td>Wählen Sie diesen Modus aus, um telered 30 Frames/Sek. Video in die 24 Frames/Sek. des ursprünglichen Videos zu konvertieren. Vorteile:<br/>
<ul>
<li>Die Komprimierungsqualität verbessert sich erheblich, da nur 24 Frames/s anstelle von 30 Frames/s codiert werden müssen.</li>
<li>Da das Ergebnis progressiv ist, werden die gleichen Komprimierungs- und Anzeigevorteile des Deinterlacings realisiert.</li>
</ul></td>
</tr>
<tr class="even">
<td>WM_DM_DEINTERLACE_VERTICALHALFSIZEDOUBLERATE</td>
<td>Wählen Sie diesen Modus aus, wenn die vertikale Ausgabeauflösung halb oder kleiner als die vertikale Auflösung der Eingabe ist und die Ausgabebildrate <a href="wmformat-glossary.md"><em>doppelt</em></a> so hoch ist. Die vertikale Videoauflösung der Eingabe beträgt z. B. 640 x 480 Pixel bei 30 Interlacingframes/s, und die vertikale Ausgabevideoauflösung beträgt 320 x 240 Pixel bei 60 Frames/s. Vorteile:<br/>
<ul>
<li>Dies erzeugt progressive Frames von hoher Qualität, da jedes Feld in einen Frame konvertiert wird und daher keine Informationen gemischt werden müssen.</li>
<li>Die vollständige Bewegung der verschachtelten Felder wird erfasst.</li>
</ul></td>
</tr>
</tbody>
</table>



 

Legen Sie für gemischten Inhalt den Deinterlacingmodus nach Bedarf fest, bevor Sie Beispiele eines neuen Typs übergeben. Um beispielsweise mit der Codierung mit progressiver Eingabe zu beginnen, müssen Sie keinen Deinterlacingmodus festlegen. Wenn einige Beispiele dann ein normales Deinterlacing erfordern, müssen Sie den Deinterlacingmodus auf WM \_ DM \_ DEINTERLACE \_ NORMAL festlegen. Um dann zusätzliche progressive Beispiele zu verarbeiten, müssen Sie den Deinterlacingmodus auf WM \_ DM \_ NOTINTERLACED festlegen.

## <a name="inverse-telecine-settings"></a>Inverse Telecine-Einstellungen

Eine Beschreibung von inversem Telecine finden Sie unter [To Use Inverse Telecine (So verwenden Sie Inverse Telecine).](to-use-inverse-telecine.md)

Wenn Sie den Deinterlacingmodus auf WM DM DEINTERLACE INVERSETELECINE festlegen, können Sie das Telecinemuster des ersten Eingabeframes angeben, indem Sie \_ \_ \_ [**IWMWriterAdvanced2::SetInputSetting aufrufen.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) Die zu verwendende Einstellung ist g \_ wszInitialPatternForInverseTelecine. Legen Sie das ursprüngliche Muster auf einen der folgenden Werte fest.



| Wert                                              | Beschreibung                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WM \_ DM DEAKTIVIERT DEN \_ \_ \_ EINHEITLICHEN \_ MODUS                | Gibt an, dass das Eingabemedium den Telecine-Prozess durchgegangen ist, die Frames jedoch nicht mehr in einem vorhersagbaren Muster liegen. Dies gibt in der Regel an, dass die Medien nach der Telecineverarbeitung bearbeitet wurden. Wenn Sie diese Einstellung verwenden, versucht der Codec, die ursprünglichen Frames selbst zu rekonstruieren. |
| WM \_ DM \_ IT \_ FIRST \_ FRAME \_ IN \_ CLIP \_ IS \_ AA \_ TOP    | Gibt an, dass das oberste Feld des AA-Frames das erste Beispiel ist.                                                                                                                                                                                                                                             |
| WM \_ DM \_ IT \_ FIRST \_ FRAME \_ IN \_ CLIP \_ IS \_ BB \_ TOP    | Gibt an, dass das obere Feld des BB-Rahmens das erste Beispiel ist.                                                                                                                                                                                                                                             |
| WM \_ DM \_ IT \_ FIRST \_ FRAME \_ IN \_ CLIP \_ IS \_ BC \_ TOP    | Gibt an, dass das obere Feld des BC-Rahmens das erste Beispiel ist.                                                                                                                                                                                                                                             |
| WM \_ DM \_ IT \_ FIRST \_ FRAME \_ IN \_ CLIP \_ IS \_ CD \_ TOP    | Gibt an, dass das obere Feld des CD-Frames das erste Beispiel ist.                                                                                                                                                                                                                                             |
| WM \_ DM \_ IT \_ FIRST \_ FRAME \_ IN \_ CLIP \_ IS \_ DD \_ TOP    | Gibt an, dass das obere Feld des DD-Frames das erste Beispiel ist.                                                                                                                                                                                                                                             |
| WM \_ DM \_ IT \_ FIRST \_ FRAME \_ IN \_ CLIP \_ IS \_ AA \_ BOTTOM | Gibt an, dass das untere Feld des AA-Frames das erste Beispiel ist.                                                                                                                                                                                                                                          |
| WM \_ DM \_ IT \_ FIRST \_ FRAME \_ IN \_ CLIP \_ IS \_ BB \_ BOTTOM | Gibt an, dass das untere Feld des BB-Rahmens das erste Beispiel ist.                                                                                                                                                                                                                                          |
| WM \_ DM \_ IT \_ FIRST \_ FRAME \_ IN \_ CLIP \_ IS \_ BC \_ BOTTOM | Gibt an, dass das untere Feld des BC-Rahmens das erste Beispiel ist.                                                                                                                                                                                                                                          |
| WM \_ DM \_ IT \_ FIRST \_ FRAME \_ IN \_ CLIP \_ IS \_ CD \_ BOTTOM | Gibt an, dass das untere Feld des CD-Frames das erste Beispiel ist.                                                                                                                                                                                                                                          |
| WM \_ DM \_ IT \_ FIRST \_ FRAME \_ IN \_ CLIP \_ IS \_ DD \_ BOTTOM | Gibt an, dass das untere Feld des DD-Frames das erste Beispiel ist.                                                                                                                                                                                                                                          |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erweiterte Themen**](advanced-topics.md)
</dt> </dl>

 

 





