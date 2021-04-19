---
description: Video-Interlacing
ms.assetid: 2911ae57-1703-4a9d-bd33-94af1e0f8804
title: Video-Interlacing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec10f49ef21f3701f85467a3f4a1c4b08d69df72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348850"
---
# <a name="video-interlacing"></a>Video-Interlacing

In diesem Thema wird beschrieben, wie Medienquellen und Decoder Zeilen Sprung Videoinhalte verarbeiten sollten.

Zum Decodieren und Rendering von verschachtelten Videos sind folgende Informationen erforderlich:

-   Progressiv oder Zeilen Sprung. Ein Videostream kann progressive Frames, Zeilen Sprung Rahmen oder eine Kombination aus beidem enthalten.

-   Feld Dominanz. Die Feld Dominanz beschreibt, welches Feld zuerst, das obere Feld oder das untere Feld angezeigt wird.

-   Wiederholen Sie das erste Feld. Dieses Flag wird in 3:2 Pulldown verwendet, wenn der Frame progressiv ist, der Stream jedoch mit Zeilen Sprung versehen ist. In diesem Kontext kann das erste Feld das obere oder untere Feld sein.

-   Verschachtelte Felder oder ein einzelnes Feld. Ein Beispiel kann entweder ein einzelnes Feld oder zwei verschachtelte Felder enthalten. Wenn ein Beispiel ein einzelnes Feld enthält, ist die Stichproben Höhe die Hälfte der Rahmenhöhe, da das Beispiel nur die Hälfte der Überprüfungs Linien für einen Frame enthält. Verschachtelte Felder werden empfohlen, es sei denn, die Eigenschaften des Quell Inhalts werden anderweitig empfohlen.

Alle diese Merkmale können von einem Beispiel in das nächste geändert werden. Videokomponenten müssen jedoch etwas über den gesamten Inhalt wissen, bevor das Streaming beginnt. Wenn das Video z. b. Zeilen Sprung ist, muss der erweiterte Videorenderer (EVR) Videospeicher für das Deinterlacing reservieren. Wenn das Video vollständig progressive Frames ist, kann der EVR die Renderingpipeline optimieren. Das Hinzufügen eines Deinterlacing-Schritts zur Pipeline erhöht die Renderingleistung.

Informationen über das Zeilen Sprung werden an zwei Stellen gespeichert:

-   Allgemeine Informationen über die Überlappung in einem Stream werden in den Medientyp eingefügt. Weitere Informationen zu Medientypen finden Sie unter [Medientypen](media-types.md).

-   Informationen, die sich bei jeder Stichprobe ändern können, werden im Beispiel als Attribut abgelegt. Weitere Informationen zu Beispielen finden Sie unter [Medien Beispiele](media-samples.md).

## <a name="interlace-information-in-the-media-type"></a>Interlace-Informationen im Medientyp

Das [**MF \_ MT \_ Interlace \_ Mode**](mf-mt-interlace-mode-attribute.md) -Attribut für den Medientyp beschreibt, wie der Datenstrom als Ganzes mit Zeilen Sprung versehen wird. Der Wert dieses Attributs ist ein Member der [**mfvideointerlacemode**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideointerlacemode) -Enumeration. Ein Video Medientyp sollte immer über dieses Attribut verfügen.

-   Wenn der Stream nur progressive Frames ohne Zeilen Sprung enthält, verwenden Sie MF videointerlace \_ progressiv.
-   Wenn der Stream nur Zeilen Sprung Rahmen enthält und jedes Beispiel zwei verschachtelte Felder enthält, verwenden Sie MF videointerlace \_ fieldinterleavedupperfirst oder MF videointerlace \_ fieldinterleavedlowerfirst.
-   Wenn der Stream nur verschachtelte Rahmen enthält und jedes Beispiel ein einzelnes Feld enthält, verwenden Sie MF videointerlace \_ fieldsingleupperoder MF videointerlace \_ fieldsinglelower. Wenn die Felder zwischen Groß und unten wechseln, spielt es keine Rolle, welche dieser beiden Werte verwendet werden. Wenn das Format nur obere Felder oder nur untere Felder enthält, legen Sie den Wert fest, der dem Inhalt entspricht.
-   Wenn der Stream eine Mischung aus Zeilen Sprung-und progressivem Rahmen enthält oder die Feld Dominanz wechselt, legen Sie den Medientyp auf mfvideointerlace \_ mixedinterlaceorprogressive fest. Verwenden Sie Beispiel Attribute, um die einzelnen Frames zu beschreiben.

In der folgenden Tabelle wird dieses Attribut zusammengefasst.



| MF- \_ MT- \_ Interlace- \_ Modus                       | Zeilen Sprung? | Beispiele                                  | Erstes Feld    |
|-----------------------------------------------|-------------|------------------------------------------|----------------|
| MF videointerlace \_ progressiv                 | Nein          | Progressiver Frame                        | Nicht verfügbar |
| MF-Interlace \_ fieldinterleavedupperfirst  | Ja         | Verschachtelte Felder                       | Obere erste    |
| MF-Interlace \_ fieldinterleavedlowerfirst  | Ja         | Verschachtelte Felder                       | Zuerst unten    |
| MF-Interlace \_ fieldsingleupper            | Ja         | Einzelfeld                             | Obere erste    |
| MF-Interlace \_ fieldsinglelower            | Ja         | Einzelfeld                             | Zuerst unten    |
| MF videointerlace \_ mixedinterlaceorprogressiv | Kann variieren    | Verschachtelte Felder oder progressive Frames | Kann variieren       |



 

Verschachtelte Felder und einzelne Felder können nicht gemischt werden. Der Wechsel von einem zu einem anderen erfordert eine Änderung des Medientyps.

## <a name="interlace-flags-on-samples"></a>Interlace-Flags für Beispiele

Informationen, die sich von einem Beispiel in das nächste ändern können, werden mithilfe von Beispiel Attributen angegeben. Verwenden Sie die [**imfsample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) -Schnittstelle, um diese Attribute zu erhalten oder festzulegen.

Alle in diesem Abschnitt aufgeführten Zeilen Sprung-Attribute verfügen über boolesche Werte. Tatsächlich kann jedes dieser Attribute über drei Werte verfügen: **true**, **false** oder nicht festgelegt. Wenn ein Attribut nicht festgelegt ist, wird der Wert aus dem Medientyp entnommen. Wenn ein Attribut festgelegt ist, überschreibt der Wert den Medientyp. Einige Kombinationen von Flags und Medientypen sind ungültig.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Attribut</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mfsampleextension-interlaced-attribute.md">MFSampleExtension_Interlaced</a></td>
<td><strong>True</strong>gibt an, dass der Frame mit Zeilen Sprung verknüpft ist. <strong>False</strong>gibt an, dass der Frame progressiv ist.<br/> Legen Sie dieses Attribut für jedes Beispiel fest, wenn der Medientyp MFVideoInterlace_MixedInterlaceOrProgressive ist.<br/></td>
</tr>
<tr class="even">
<td><a href="mfsampleextension-bottomfieldfirst-attribute.md">MFSampleExtension_BottomFieldFirst</a></td>
<td>Die Bedeutung dieses Flags hängt davon ab, ob die Beispiele verschachtelte Felder oder einzelne Felder enthalten.<br/>
<ul>
<li>Verschachtelte Felder: <strong>true</strong>gibt an, dass das untere Feld zuerst ist. Wenn <strong>false</strong>, wird das obere Feld zuerst angezeigt.<br/></li>
<li>Einzelne Felder: Wenn <strong>true</strong>, enthält das Beispiel ein niedrigeres Feld. <strong>False</strong>gibt an, dass das Beispiel ein oberes Feld enthält.<br/></li>
</ul>
Legen Sie dieses Attribut für jedes damit-Beispiel fest, wenn der Medientyp MFVideoInterlace_FieldSingleUpper, MFVideoInterlace_FieldSingleLower oder MFVideoInterlace_MixedInterlaceOrProgressive ist.<br/></td>
</tr>
<tr class="odd">
<td><a href="mfsampleextension-repeatfirstfield-attribute.md">MFSampleExtension_RepeatFirstField</a></td>
<td><strong>True</strong>gibt an, dass das erste Feld wiederholt wird. Wenn <strong>false</strong> oder nicht festgelegt ist, wird das erste Feld nicht wiederholt.</td>
</tr>
<tr class="even">
<td><a href="mfsampleextension-singlefield-attribute.md">MFSampleExtension_SingleField</a></td>
<td><strong>True</strong>gibt an, dass das Beispiel ein einzelnes Feld enthält. Wenn der Wert <strong>false</strong>ist, enthält das Beispiel verschachtelte Felder.</td>
</tr>
</tbody>
</table>



 

In der folgenden Tabelle wird basierend auf dem Medientyp angezeigt, welche Flags erforderlich, optional oder nicht zulässig sind.



| Medientyp         | Zeilen Sprung-Flag                      | Bottomfieldfirst-Flag                    | Repeatfirstfield-Flag | Singlefield-Flag                     |
|--------------------|--------------------------------------|------------------------------------------|-----------------------|--------------------------------------|
| progressiv        | Optionale Wenn festgelegt, muss den Wert **false** aufweisen. | Legen Sie keinen Wert fest.                              | Legen Sie keinen Wert fest.           | Legen Sie keinen Wert fest.                          |
| Verschachtelte Felder | Optionale Wenn festgelegt, muss **true** sein.  | Optionale Wenn festgelegt, muss dem Medientyp entsprechen. | Legen Sie keinen Wert fest.           | Optionale Wenn festgelegt, muss den Wert **false** aufweisen. |
| Einzelne Felder      | Optionale Wenn festgelegt, muss **true** sein.  | Erforderlich.                                | Legen Sie keinen Wert fest.           | Auf " **true**" festgelegt.                     |
| Mixed              | Erforderlich.                            | Erforderlich.                                | Erforderlich.             | Optionale Wenn festgelegt, muss den Wert **false** aufweisen. |



 

In Fällen, in denen das Attribut optional ist, definiert der Medientyp bereits die Informationen. Es ist zulässig, das-Attribut auf eine Entsprechung festzulegen, jedoch nicht erforderlich.

Wenn der Medientyp z. b. "MF videointerlace \_ progressiv" ist, bedeutet dies, dass alle Frames im Stream progressiv sind. Daher können Sie entweder das **\_ Interlacing-Attribut "mfsampleextension** " auf " **false**" festlegen oder das Attribut nicht festlegen.

## <a name="recommendations"></a>Empfehlungen

Dieser Abschnitt enthält Empfehlungen für verschiedene Inhaltstypen.

1. Das Video ist alle progressiven Frames.

-   Legen Sie den Medientyp auf mfvideointerlace \_ progressiv fest.

-   Legen Sie das **\_ Interlacing-Attribut "mfsampleextension** " nicht fest, oder legen Sie es für jeden Frame auf " **false** " fest.

-   Legen Sie die ' **MF SampleExtension '-Attribute ' \_ bottomfieldfirst**', ' **MF SampleExtension ' \_ repeatfirstfield**' oder ' **MF Sample Extension \_** ' nicht fest.

2. Das Video stellt alle Zeilen Sprung Felder mit der gleichen Feld Dominanz dar. Beispiele enthalten verschachtelte Felder.

-   Legen Sie den Medientyp auf mfvideointerlace \_ fieldinterleavedupperfirst oder mfvideointerlace \_ fieldinterleavedlowerfirst fest.

-   Legen Sie das **\_ Interlacing-Attribut "mfsampleextension** " nicht fest, oder legen Sie es für jeden Frame auf " **true** " fest.

-   Legen Sie das Attribut " **mfsampleextension \_ bottomfieldfirst** " nicht fest, oder legen Sie den Wert für jeden Frame entsprechend dem Medientyp fest.

-   Legen Sie das Attribut " **\_ repeatfirstfield" der mfsampleextension** nicht fest, oder legen Sie es für jeden Frame auf " **false** " fest.

-   Legen Sie das **\_ Singlefield-Attribut "mfsampleextension** " nicht fest, oder legen Sie es für jeden Frame auf " **false** " fest.

3. Das Video enthält eine Mischung aus Zeilen Sprung-und progressivem Rahmen mit wiederholten Feldern und abweichender Feld Dominanz (z. b. DVD-Video).

-   Legen Sie den Medientyp auf mfvideointerlace \_ mixedinterlaceorprogressive fest.

-   Legen Sie in jedem Frame die Attribute **mfsampleextension \_ Interlacing**, **mfsampleextension \_ bottomfieldfirst** und **mfsampleextension \_ repeatfirstfield** fest.

-   Legen Sie das **\_ Singlefield-Attribut "mfsampleextension** " nicht fest, oder legen Sie es für jeden Frame auf " **false** " fest.

4. Das Video ist Zeilen Sprung, und die Beispiele enthalten einzelne Felder.

-   Legen Sie den Medientyp auf mfvideointerlace \_ fieldsingleupperoder mfvideointerlace \_ fieldsinglelower fest.

-   Legen Sie in jedem Frame das Attribut " **mfsampleextension \_ bottomfieldfirst** " fest.

-   Legen Sie das **\_ Interlacing-Attribut "mfsampleextension** " nicht fest, oder legen Sie es für jeden Frame auf " **true** " fest.

-   Legen Sie das Attribut " **\_ repeatfirstfield" der mfsampleextension** nicht fest, oder legen Sie es für jeden Frame auf " **false** " fest.

-   Legen Sie das **\_ Singlefield-Attribut "mfsampleextension** " nicht fest, oder legen Sie es für jeden Frame auf " **true** " fest.

Die meisten Videoinhalte fallen in eine dieser Kategorien.

## <a name="mpeg-2-mappings"></a>MPEG-2-Zuordnungen

Verwenden Sie für MPEG-2-Inhalte die folgenden Zuordnungen, um die MPEG-2-Flags in Media Foundation Beispiel Attribute zu konvertieren.

**Bild \_ Struktur**



| Wert         | Sample-Attribut                                                                                                        |
|---------------|-------------------------------------------------------------------------------------------------------------------------|
| frame         | **MF Sample Extension \_ Singlefield**  =  **false**                                                                          |
| Oberstes \_ Feld    | **MF Sample Extension \_ Singlefield**  =  **true**<br/> **MF Sample Extension \_ Bottomfieldfirst**  =  **false**<br/> |
| Unteres \_ Feld | **MF Sample Extension \_ Singlefield**  =  **true**<br/> **MF Sample Extension \_ Bottomfieldfirst**  =  **true**<br/>  |



 

**progressiver \_ Frame**



| Wert | Sample-Attribut                              |
|-------|-----------------------------------------------|
| 0     | **MF Sample Extension \_** Zeilen Sprung  =  **true**  |
| 1     | **MF Sample Extension \_** Zeilen Sprung  =  **false** |



 

**Oberstes \_ Feld \_ zuerst**



| Wert | Sample-Attribut                                    |
|-------|-----------------------------------------------------|
| 0     | **MF Sample Extension \_ Bottomfieldfirst**  =  **true**  |
| 1     | **MF Sample Extension \_ Bottomfieldfirst**  =  **false** |



 

**\_erstes \_ Feld wiederholen**



| Wert | Sample-Attribut                                    |
|-------|-----------------------------------------------------|
| 0     | **MF Sample Extension \_ Repeatfirstfield**  =  **false** |
| 1     | **MF Sample Extension \_ Repeatfirstfield**  =  **true**  |



 

## <a name="single-field-samples"></a>Single-Field Beispiele

Wenn der Medientyp MF videointerlace \_ fieldsingleupperor MF videointerlace \_ fieldsinglelower ist, bedeutet dies, dass jedes Beispiel ein einzelnes Feld enthält. Der Medientyp beschreibt jedoch den gesamten Frame. Daher enthält jeder Puffer nur die Hälfte der Anzahl der Feld Zeilen, die im Medientyp angegeben werden. Wenn der Medientyp z. b. das Video als 720 × 480 beschreibt, enthält jedes Feld 240 Scan Zeilen, und jeder Puffer enthält daher nur 240 Zeilen von Pixeln. Wenn Sie eine Komponente schreiben, die Medientypen mit Einzel Feld Beispielen annimmt, müssen Sie diese Tatsache berücksichtigen, wenn Sie auf die Daten im Puffer zugreifen.

Die gleiche Regel gilt für den geometrischen Aperture ("[MF \_ MT \_ geometrischen \_ Aperture](mf-mt-geometric-aperture-attribute.md) "-Attribut) und die minimale Anzeige Öffnung ("MF MT"-Attribut der[ \_ \_ minimalen \_ Anzeige \_ Öffnung](mf-mt-minimum-display-aperture-attribute.md) ). Diese Regionen werden in Bezug auf den gesamten Frame und nicht auf die einzelnen Felder angegeben.

## <a name="directshow-mappings"></a>DirectShow-Zuordnungen

In DirectShow ist das Sample-Zeilen Sprung-Element im **dwtypespecificflags** -Member der **am \_ SAMPLE2 \_ Properties** -Struktur enthalten. In der folgenden Tabelle werden die entsprechenden Attribute für Media Foundation angezeigt.



| DirectShow-beispielflag              | Media Foundation Sample-Attribut                                                                                                                                                  |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| überlappenden Frame mit dem \_ \_ videolflag \_ \_ | **MF Sample Extension \_ Singlefield**  =  **false**.                                                                                                                                    |
| AM \_ - \_ videoflag \_ FIELD1             | **MF Sample Extension \_** Zeilen Sprung "  =  **true**".<br/> **MF Sample Extension \_ Singlefield**  =  **true**.<br/> **MF Sample Extension \_ Bottomfieldfirst**  =  **false**.<br/> |
| AM \_ - \_ videoflag \_ FIELD2             | **MF Sample Extension \_** Zeilen Sprung "  =  **true**".<br/> **MF Sample Extension \_ Singlefield**  =  **true**.<br/> **MF Sample Extension \_ Bottomfieldfirst**  =  **true**.<br/>  |
| AM \_ - \_ videoflag \_              | **MF Sample Extension \_** Zeilen Sprung  =  **false**. (Dieses Flag gibt an, dass der Treiber die beiden Felder nicht deinstalversien sollte.)                                                        |
| AM \_ - \_ videoflag \_ FIELD1FIRST        | **MF Sample Extension \_ Bottomfieldfirst**  =  **false**. Wenn der Inhalt mit Zeilen Sprung versehen ist und das Flag "am \_ Video \_ Flag \_ FIELD1FIRST" nicht vorhanden ist, legen Sie dieses Attribut auf " **true**" fest.        |
| \_ \_ \_ Textfeld zum Wiederholen von \_ textflags      | **MF Sample Extension \_ Repeatfirstfield**  =  **true**. \_ \_ \_ \_ Legen Sie dieses Attribut auf " **false**" fest, wenn das Feld Flag zum Wiederholen des Felds mit der Markierung nicht vorhanden ist                                    |



 

Wenn das DirectShow-Beispiel keine beispielflags enthält, verwenden Sie den Wert von **dwinterlaceflags** aus der **VIDEOINFOHEADER2** -Struktur:



| DirectShow-damit-Flag    | Media Foundation Sample-Attribut                    |
|------------------------------|------------------------------------------------------|
| Aminterlace \_ isinterschnür    | **MF Sample Extension \_** Zeilen Sprung "  =  **true**".        |
| Aminterlace \_ 1fieldpersample | **MF Sample Extension \_ Singlefield**  =  **true**.       |
| Aminterlace \_ Field1First     | **MF Sample Extension \_ Bottomfieldfirst**  =  **false**. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Video Medientypen](video-media-types.md)
</dt> <dt>

[Medientypen](media-types.md)
</dt> </dl>

 

 




