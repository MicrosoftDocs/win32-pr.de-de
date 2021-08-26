---
description: Video Interlacing
ms.assetid: 2911ae57-1703-4a9d-bd33-94af1e0f8804
title: Video Interlacing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 340c727f8faaaf20ff82eff58d0c651601071dea
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474336"
---
# <a name="video-interlacing"></a>Video Interlacing

In diesem Thema wird beschrieben, wie Medienquellen und Decoder mit Interlacing-Videoinhalten umgehen sollten.

Um Interlaced-Videos ordnungsgemäß zu decodieren und zu rendern, sind die folgenden Informationen erforderlich:

-   Progressiv oder Interlacing. Ein Videostream kann progressive Frames, Interlacingframes oder eine Kombination aus beidem enthalten.

-   Felddominanz. Felddominanz beschreibt, welches Feld zuerst angezeigt wird, das obere feld oder das untere Feld.

-   Wiederholen Sie das erste Feld. Dieses Flag wird im 3:2-Pulldown verwendet, wenn der Frame progressiv ist, der Stream jedoch interlaced ist. In diesem Kontext kann das erste Feld das obere oder untere Feld sein.

-   Überlappte Felder oder einzelne Felder. Ein Beispiel kann entweder ein einzelnes Feld oder zwei überlappte Felder enthalten. Wenn ein Beispiel ein einzelnes Feld enthält, ist die Stichprobenhöhe die Hälfte der Framehöhe, da das Beispiel nur die Hälfte der Scanlinien für einen Frame enthält. Überlappte Felder werden empfohlen, sofern die Merkmale des Quellinhalts nichts anderes vorschreiben.

Jedes dieser Merkmale kann sich von einem Beispiel in das nächste ändern. Videokomponenten müssen jedoch etwas über den gesamten Inhalt wissen, bevor das Streaming beginnt. Wenn das Video z. B. als Interlacing angezeigt wird, muss der erweiterte Videorenderer (EVR) Videospeicher für das Deinterlacing reservieren. Wenn es sich bei dem Video um vollständig progressive Frames handelt, kann der EVR die Renderingpipeline optimieren. Das Hinzufügen eines Deinterlacingschritts zur Pipeline erhöht die Renderinglatenz.

Informationen zum Interlacing werden an zwei Stellen gespeichert:

-   Allgemeine Informationen zum Interlacing in einem Stream werden im Medientyp platziert. Weitere Informationen zu Medientypen finden Sie unter [Medientypen.](media-types.md)

-   Informationen, die sich mit den einzelnen Stichproben ändern können, werden im Beispiel als Attribut platziert. Weitere Informationen zu Beispielen finden Sie unter [Medienbeispiele.](media-samples.md)

## <a name="interlace-information-in-the-media-type"></a>Interlace-Informationen im Medientyp

Das [**MF \_ MT \_ INTERLACE \_ MODE-Attribut**](mf-mt-interlace-mode-attribute.md) für den Medientyp beschreibt, wie der Stream als Ganzes verschachtelt wird. Der Wert dieses Attributs ist ein Member der [**MFVideoInterlaceMode-Enumeration.**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideointerlacemode) Ein Videomedientyp sollte immer über dieses Attribut verfügen.

-   Wenn der Stream nur progressive Frames ohne Interlacingframes enthält, verwenden Sie MFVideoInterlace \_ Progressive.
-   Wenn der Stream nur Zwischenebenenframes enthält und jedes Beispiel zwei verschachtelte Felder enthält, verwenden Sie MFVideoInterlace \_ FieldInterleavedUpperFirst oder MFVideoInterlace \_ FieldInterleavedLowerFirst.
-   Wenn der Stream nur Frames mit Interlacing enthält und jedes Beispiel ein einzelnes Feld enthält, verwenden Sie MFVideoInterlace \_ FieldSingleUpper oder MFVideoInterlace \_ FieldSingleLower. Wenn die Felder zwischen oben und unten wechseln, spielt es keine Rolle, welcher dieser beiden Werte verwendet wird. Wenn das Format nur obere oder nur niedrigere Felder enthält, legen Sie den Wert fest, der dem Inhalt entspricht.
-   Wenn der Stream eine Mischung aus Geschachtelten und progressiven Frames enthält oder die Felddominanz wechselt, legen Sie den Medientyp auf MFVideoInterlace \_ MixedInterlaceOrProgressive fest. Verwenden Sie Beispielattribute, um jeden Frame zu beschreiben.

In der folgenden Tabelle wird dieses Attribut zusammengefasst.



| MF \_ MT \_ INTERLACE-MODUS \_                       | Interlaced? | Beispiele                                  | Erstes Feld    |
|-----------------------------------------------|-------------|------------------------------------------|----------------|
| MFVideoInterlace \_ Progressive                 | Nein          | Progressiver Frame                        | Nicht zutreffend |
| MFVideoInterlace \_ FieldInterleavedUpperFirst  | Ja         | Überlappte Felder                       | Erste Obere    |
| MFVideoInterlace \_ FieldInterleavedLowerFirst  | Ja         | Überlappte Felder                       | Lower first    |
| MFVideoInterlace \_ FieldSingleUpper            | Ja         | Einzelfeld                             | Erste Obere    |
| MFVideoInterlace \_ FieldSingleLower            | Ja         | Einzelfeld                             | Lower first    |
| MFVideoInterlace \_ MixedInterlaceOrProgressive | Kann variieren    | Überlappte Felder oder progressive Frames | Kann variieren       |



 

Überlappte Felder und einzelne Felder können nicht gemischt werden. Der Wechsel von einem zum anderen erfordert eine Änderung des Medientyps.

## <a name="interlace-flags-on-samples"></a>Interlace-Flags in Beispielen

Informationen, die sich von einem Beispiel zum nächsten ändern können, werden mithilfe von Beispielattributen angegeben. Verwenden Sie [**die BERDsample-Schnittstelle,**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) um diese Attribute zu erhalten oder zu festlegen.

Alle in diesem Abschnitt aufgeführten Interlacingattribute verfügen über boolesche Werte. Jedes dieser Attribute kann über drei Werte verfügen: **TRUE,** **FALSE** oder nicht festgelegt. Wenn kein Attribut festgelegt ist, wird der Wert vom Medientyp übernommen. Wenn ein Attribut festgelegt ist, überschreibt der Wert den Medientyp. Einige Kombinationen von Flags und Medientypen sind ungültig.




| Attribut | BESCHREIBUNG | 
|-----------|-------------|
| <a href="mfsampleextension-interlaced-attribute.md">MFSampleExtension_Interlaced</a> | True <strong>gibt an,</strong>dass der Frame als Interlacing angezeigt wird. False <strong>gibt an,</strong>dass der Frame progressiv ist.<br /> Legen Sie dieses Attribut für jedes Beispiel fest, wenn der Medientyp MFVideoInterlace_MixedInterlaceOrProgressive.<br /> | 
| <a href="mfsampleextension-bottomfieldfirst-attribute.md">MFSampleExtension_BottomFieldFirst</a> | Die Bedeutung dieses Flags hängt davon ab, ob die Beispiele überlappte Felder oder einzelne Felder enthalten.<br /><ul><li>Überlappte Felder: Bei <strong>TRUE</strong>wird zuerst das untere Feld angezeigt. False <strong>gibt</strong>an, dass das obere Feld zuerst angezeigt wird.<br /></li><li>Einzelne Felder: True <strong>gibt an,</strong>dass das Beispiel ein unteres Feld enthält. False <strong>gibt an,</strong>dass das Beispiel ein oberes Feld enthält.<br /></li></ul>Legen Sie dieses Attribut für jedes Interlace-Beispiel fest, wenn der Medientyp MFVideoInterlace_FieldSingleUpper, MFVideoInterlace_FieldSingleLower oder MFVideoInterlace_MixedInterlaceOrProgressive.<br /> | 
| <a href="mfsampleextension-repeatfirstfield-attribute.md">MFSampleExtension_RepeatFirstField</a> | True <strong>gibt an,</strong>dass das erste Feld wiederholt wird. Wenn <strong>FALSE</strong> oder nicht festgelegt ist, wird das erste Feld nicht wiederholt. | 
| <a href="mfsampleextension-singlefield-attribute.md">MFSampleExtension_SingleField</a> | True <strong>gibt an,</strong>dass das Beispiel ein einzelnes Feld enthält. False <strong>gibt an,</strong>dass das Beispiel überlappte Felder enthält. | 




 

Die folgende Tabelle zeigt, welche Flags je nach Medientyp erforderlich, optional oder unzulässig sind.



| Medientyp         | Verschachtelte Flags                      | BottomFieldFirst-Flag                    | RepeatFirstField-Flag | SingleField-Flag                     |
|--------------------|--------------------------------------|------------------------------------------|-----------------------|--------------------------------------|
| progressiv        | Optional; wenn festgelegt, muss **FALSE** sein. | Legen Sie keinen Wert fest.                              | Legen Sie keinen Wert fest.           | Legen Sie keinen Wert fest.                          |
| Verschachtelte Felder | Optional; wenn festgelegt, muss **TRUE** sein.  | Optional; wenn festgelegt, muss mit dem Medientyp übereinstimmen. | Legen Sie keinen Wert fest.           | Optional; wenn festgelegt, muss **FALSE** sein. |
| Einzelne Felder      | Optional; wenn festgelegt, muss **TRUE** sein.  | Erforderlich.                                | Legen Sie keinen Wert fest.           | Legen Sie auf **TRUE** fest.                     |
| Mixed              | Erforderlich.                            | Erforderlich.                                | Erforderlich.             | Optional; wenn festgelegt, muss **FALSE** sein. |



 

In Fällen, in denen das Attribut optional ist, definiert der Medientyp die Informationen bereits. Es ist gültig, das Attribut so festzulegen, dass es übereinstimmt, aber nicht erforderlich.

Wenn der Medientyp beispielsweise MFVideoInterlace \_ Progressive lautet, bedeutet dies, dass alle Frames im Stream progressiv sind. Daher können Sie entweder das **MFSampleExtension \_ Interlaced-Attribut** auf **FALSE** festlegen oder das Attribut nicht festlegen.

## <a name="recommendations"></a>Empfehlungen

Dieser Abschnitt enthält Empfehlungen für verschiedene Inhaltstypen.

1. Bei dem Video handelt es sich um alle progressiven Frames.

-   Legen Sie den Medientyp auf MFVideoInterlace \_ Progressive fest.

-   Legen Sie das **MFSampleExtension \_ Interlaced-Attribut** nicht fest, oder legen Sie es für jeden Frame auf **FALSE** fest.

-   Legen Sie die Attribute **MFSampleExtension \_ BottomFieldFirst,** **MFSampleExtension \_ RepeatFirstField** oder **MFSampleExtension \_ SingleField** nicht fest.

2. Das Video ist alles übersprungene Felder mit der gleichen Felddominanz. Beispiele enthalten verschachtelte Felder.

-   Legen Sie den Medientyp auf MFVideoInterlace \_ FieldInterleavedUpperFirst oder MFVideoInterlace \_ FieldInterleavedLowerFirst fest.

-   Legen Sie das **MFSampleExtension \_ Interlaced-Attribut** nicht fest, oder legen Sie es für jeden Frame auf **TRUE** fest.

-   Legen Sie nicht das **\_ BottomFieldFirst-Attribut MFSampleExtension** fest, oder legen Sie den Wert für jeden Frame so fest, dass er dem Medientyp entspricht.

-   Legen Sie das **Attribut MFSampleExtension \_ RepeatFirstField** nicht fest, oder legen Sie es für jeden Frame auf **FALSE** fest.

-   Legen Sie das **Attribut MFSampleExtension \_ SingleField** nicht fest, oder legen Sie es für jeden Frame auf **FALSE** fest.

3. Das Video enthält eine Mischung aus übersprungenen und progressiven Frames mit wiederholten Feldern und unterschiedlicher Felddominanz (z. B. DVD-Video).

-   Legen Sie den Medientyp auf MFVideoInterlace \_ MixedInterlaceOrProgressive fest.

-   Legen Sie für jeden Frame die Attribute **MFSampleExtension \_ Interlaced,** **MFSampleExtension \_ BottomFieldFirst** und **MFSampleExtension \_ RepeatFirstField** fest.

-   Legen Sie das **Attribut MFSampleExtension \_ SingleField** nicht fest, oder legen Sie es für jeden Frame auf **FALSE** fest.

4. Das Video ist übersprungen, und die Beispiele enthalten einzelne Felder.

-   Legen Sie den Medientyp auf MFVideoInterlace \_ FieldSingleUpper oder MFVideoInterlace \_ FieldSingleLower fest.

-   Legen Sie auf jedem Frame das **Attribut MFSampleExtension \_ BottomFieldFirst** fest.

-   Legen Sie das **MFSampleExtension \_ Interlaced-Attribut** nicht fest, oder legen Sie es für jeden Frame auf **TRUE** fest.

-   Legen Sie das **Attribut MFSampleExtension \_ RepeatFirstField** nicht fest, oder legen Sie es für jeden Frame auf **FALSE** fest.

-   Legen Sie das **Attribut MFSampleExtension \_ SingleField** nicht fest, oder legen Sie es für jeden Frame auf **TRUE** fest.

Die meisten Videoinhalte fallen in eine dieser Kategorien.

## <a name="mpeg-2-mappings"></a>MPEG-2-Zuordnungen

Verwenden Sie für MPEG-2-Inhalte die folgenden Zuordnungen, um die MPEG-2-Flags in Media Foundation Beispielattribute zu konvertieren.

**\_Bildstruktur**



| Wert         | Beispielattribut                                                                                                        |
|---------------|-------------------------------------------------------------------------------------------------------------------------|
| frame         | **MFSampleExtension \_ SingleField**  =  **FALSE**                                                                          |
| oberes \_ Feld    | **MFSampleExtension \_ SingleField**  =  **TRUE**<br/> **MFSampleExtension \_ BottomFieldFirst**  =  **FALSE**<br/> |
| unteres \_ Feld | **MFSampleExtension \_ SingleField**  =  **TRUE**<br/> **MFSampleExtension \_ BottomFieldFirst**  =  **TRUE**<br/>  |



 

**Progressiver \_ Frame**



| Wert | Beispielattribut                              |
|-------|-----------------------------------------------|
| 0     | **MFSampleExtension \_ Interlaced**  =  **TRUE**  |
| 1     | **MFSampleExtension \_ Interlaced**  =  **FALSE** |



 

**oberstes \_ Feld \_ zuerst**



| Wert | Beispielattribut                                    |
|-------|-----------------------------------------------------|
| 0     | **MFSampleExtension \_ BottomFieldFirst**  =  **TRUE**  |
| 1     | **MFSampleExtension \_ BottomFieldFirst**  =  **FALSE** |



 

**Wiederholen \_ des ersten \_ Felds**



| Wert | Beispielattribut                                    |
|-------|-----------------------------------------------------|
| 0     | **MFSampleExtension \_ RepeatFirstField**  =  **FALSE** |
| 1     | **MFSampleExtension \_ RepeatFirstField**  =  **TRUE**  |



 

## <a name="single-field-samples"></a>beispiele für Single-Field

Wenn der Medientyp MFVideoInterlace \_ FieldSingleUpper oder MFVideoInterlace \_ FieldSingleLower ist, bedeutet dies, dass jedes Beispiel ein einzelnes Feld enthält. Der Medientyp beschreibt jedoch den gesamten Frame. Daher enthält jeder Puffer nur die Hälfte der Im Medientyp angegebenen Feldzeilen. Wenn der Medientyp das Video beispielsweise als 720 × 480 beschreibt, enthält jedes Feld 240 Scanzeilen, und daher enthält jeder Puffer nur 240 Pixelzeilen. Wenn Sie eine Komponente schreiben, die Medientypen mit Einfeldbeispielen akzeptiert, müssen Sie diese Tatsache berücksichtigen, wenn Sie auf die Daten im Puffer zugreifen.

Die gleiche Regel gilt für die geometrische Öffnung[(MF \_ MT GEOMETRIC \_ \_ APERTURE-Attribut)](mf-mt-geometric-aperture-attribute.md) und die minimale Anzeigegeblendung[(MF MT MINIMUM DISPLAY \_ \_ \_ \_ APERTURE-Attribut).](mf-mt-minimum-display-aperture-attribute.md) Diese Bereiche werden in Bezug auf den gesamten Rahmen und nicht auf die einzelnen Felder angegeben.

## <a name="directshow-mappings"></a>DirectShow-Zuordnungen

In DirectShow sind Informationen zum Pro-Sample-Interlacing im **dwTypeSpecificFlags-Member** der **AM \_ SAMPLE2 \_ PROPERTIES-Struktur** enthalten. Die folgende Tabelle zeigt die entsprechenden Attribute für Media Foundation.



| DirectShow-Beispielflag              | Media Foundation Beispielattribut                                                                                                                                                  |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AM \_ VIDEO \_ FLAG \_ INTERLEAVED \_ FRAME | **MFSampleExtension \_ SingleField**  =  **FALSE**.                                                                                                                                    |
| AM \_ VIDEO \_ FLAG \_ FIELD1             | **MFSampleExtension \_ Interlaced**  =  **TRUE**.<br/> **MFSampleExtension \_ SingleField**  =  **TRUE**.<br/> **MFSampleExtension \_ BottomFieldFirst**  =  **FALSE**.<br/> |
| AM \_ VIDEO \_ FLAG \_ FIELD2             | **MFSampleExtension \_ Interlaced**  =  **TRUE**.<br/> **MFSampleExtension \_ SingleField**  =  **TRUE**.<br/> **MFSampleExtension \_ BottomFieldFirst**  =  **TRUE**.<br/>  |
| AM \_ VIDEO \_ FLAG \_ WEAVE              | **MFSampleExtension \_ Interlaced**  =  **FALSE**. (Dieses Flag gibt an, dass der Treiber die beiden Felder nicht deinterlacen soll.)                                                        |
| AM \_ \_ VIDEOFLAG \_ FIELD1FIRST        | **MFSampleExtension \_ BottomFieldFirst**  =  **FALSE**. Wenn der Inhalt übersprungen wird und das AM \_ VIDEO \_ FLAG \_ FIELD1FIRST-Flag nicht vorhanden ist, legen Sie dieses Attribut auf **TRUE** fest.        |
| AM \_ VIDEO \_ FLAG \_ REPEAT \_ FIELD      | **MFSampleExtension \_ RepeatFirstField**  =  **TRUE**. Wenn das FLAG AM \_ VIDEO FLAG REPEAT FIELD nicht vorhanden \_ \_ \_ ist, legen Sie dieses Attribut auf **FALSE** fest.                                    |



 

Wenn das DirectShow-Beispiel keine Beispielflags enthält, verwenden Sie den Wert von **dwInterlaceFlags** aus der **VIDEOINFOHEADER2-Struktur:**



| DirectShow-Interlace-Flag    | Media Foundation Beispielattribut                    |
|------------------------------|------------------------------------------------------|
| AMINTERLACE \_ IsInterlaced    | **MFSampleExtension \_ Interlaced**  =  **TRUE**.        |
| AMINTERLACE \_ 1FieldPerSample | **MFSampleExtension \_ SingleField**  =  **TRUE**.       |
| AMINTERLACE \_ Field1First     | **MFSampleExtension \_ BottomFieldFirst**  =  **FALSE**. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Videomedientypen](video-media-types.md)
</dt> <dt>

[Medientypen](media-types.md)
</dt> </dl>

 

 




