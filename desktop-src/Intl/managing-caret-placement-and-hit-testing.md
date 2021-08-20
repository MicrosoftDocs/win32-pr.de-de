---
description: Komplexe Skriptsprachen werden von ScriptShape in Cluster unterbrochen. Die Neuanordnung von Zeichen erfolgt immer innerhalb von Clustergrenzen. Die Cluster selbst bewegen sich garantiert in richtung der Leserichtung.
ms.assetid: 50b4b643-af96-4a6f-80f9-27a71ce16b0e
title: Verwalten von Caretplatzierung und Treffertests
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02e1c6d3b9dbd54f3df2b458a3f7473d1021dceafd6772730b8482b06c4e1c4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119788400"
---
# <a name="managing-caret-placement-and-hit-testing"></a>Verwalten von Caretplatzierung und Treffertests

Komplexe Skriptsprachen werden von ScriptShape [in](uniscribe-glossary.md) [**Cluster unterbrochen.**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) Die Neuanordnung von Zeichen erfolgt immer innerhalb von Clustergrenzen. Die Cluster selbst bewegen sich garantiert in richtung der Leserichtung.

Clusterinformationen im logischen Clusterarray werden verwendet, um die Breite eines Clusters von Glyphen gleichmäßig auf die logischen Zeichen zu teilen, die sie darstellen. Beispielsweise ist das Lam-Alef-Glyph in vier Bereiche unterteilt:

-   Die führende Hälfte von lam.
-   Die nachende Hälfte des lam.
-   Die führende Hälfte des Alef.
-   Die nachende Hälfte des Alef.

Konventionen für die Ein caret-Platzierung in Clustern hängen vom Skript ab. Wenn für das arabische Skript die Position des Caretzeichens zwischen einem Basiszeichen und dessen Kombinationsmarkierung festgelegt ist, wird das Caretzeichen in der Mitte des Basiszeichens angezeigt. Für das thailändisch-Skript kann die Ein caret nicht innerhalb eines Clusters positioniert werden. Wenn der Benutzer das Caret-Caret-Strich-Strich-5-Strich-1-Strich-1-Strich-1-0-4-0-1600-000-000-000-000-000-4000-30

Die [**ScriptXtoCP-**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp) und [**ScriptCPtoX-Funktionen**](/windows/desktop/api/Usp10/nf-usp10-scriptcptox) übersetzen zwischen Caretpositionen (in Codepunktoffsets) und x-Positionen (in Pixeln). Die **ScriptXtoCP-Funktion** verfügt über Kenntnisse der Positionskonventionen der Caretstellen der einzelnen Skripts:

-   Für Indien und Thai werden Caretpositionen an Clustergrenzen positioniert.
-   Für Arabisch werden Caretpositionen mit Clustern interpoliert.
-   Für Hebräisch werden in Versionen vor Usp10.dll Version 1.420 Caretpositionen mit Clustern interpoliert. Ab Usp10.dll Version 1.420 werden Caretpositionen an Clustergrenzen ausrichten.

[**Sowohl ScriptXtoCP als**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp) auch [**ScriptCPtoX**](/windows/desktop/api/Usp10/nf-usp10-scriptcptox) funktionieren nur innerhalb von Ausführungen. Die Funktionen erfordern, dass bestimmte Parameter aus früheren Uniscribe-Aufrufen stammen, wie in der folgenden Tabelle gezeigt.



| Parameter                                        | Quelle                                                 |
|--------------------------------------------------|--------------------------------------------------------|
| *Psa*                                            | Wie von [**ScriptItemize zurückgegeben.**](/windows/desktop/api/Usp10/nf-usp10-scriptitemize) |
| *cGlyphspwLogClust*<br/> *psva*<br/> | Wie von [**ScriptShape zurückgegeben.**](/windows/desktop/api/Usp10/nf-usp10-scriptshape)     |
| *piAdvance*                                      | Wie von [**ScriptPlace zurückgegeben.**](/windows/desktop/api/Usp10/nf-usp10-scriptplace)     |



 

Die Anwendung muss die Ausführung einrichten, in der sich ein angegebener Caretoffset oder eine x-Position befindet, bevor die Informationen an [**ScriptCPtoX**](/windows/desktop/api/Usp10/nf-usp10-scriptcptox) oder [**ScriptXtoCP übergeben werden.**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp) Wenn die Anwendung die Breiteninformationen nicht speichern kann, kann sie treffertests und die Ein caretplatzierung durchführen, nachdem die einzelnen Ausführungen angezeigt wurden. Alternativ kann die Anwendung genügend Informationen zwischenspeichern, um Treffertests und die Platzierung von Caretstrichen in der aktuellen Zeile zu durchführen, ohne dass der Absatz erneut verarbeitet werden muss.

[**ScriptXtoCP gibt**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp) einen nachstellenden Edgewert zurück, damit die Anwendung die Seite des Zeichens oder Clusters kennt, auf das der Benutzer geklickt hat. Der Wert ist entweder 0 oder die Breite des Zeichens oder Clusters in Codepunkten. Die zurückgegebene Zeichenposition ist die Position des Zeichens, auf das der Benutzer geklickt hat. Weitere Informationen finden Sie unter [Anzeigen des Caret-Zeichens in bidirektionalen Zeichenfolgen.](displaying-the-caret-in-bidirectional-strings.md)

Für Sprachen wie Thailändisch, für die der Benutzer das Caretzeichen konventionsell nicht in einem Cluster platzieren möchte, legt [**ScriptXtoCP**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp) das flag der nachden Seite auf 0 oder auf die Clusterbreite fest. Für Sprachen wie Arabisch, für die der Benutzer erwartet, dass sie innerhalb eines Clusters bearbeitet werden können, legt **ScriptXtoCP** das Nachseitenflag auf 0 oder 1 fest.

Uniscribe stellt Informationen zu gültigen Caretpositionen im **fCharStop-Member** in den logischen Attributen zur Verfügung, die von ScriptBreak zurückgegeben werden, um die Anwendung beim Einrichten gültiger Positionen für das Caretzeichen bei der Verarbeitung der Pfeiltasten zu [**unterstützen.**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak) **TRUE** wird für die meisten Zeichen und **FALSE für** Interclusterzeichen in Skripts wie Thai zurückgegeben. Die Anwendung sollte den **fNeedsCaretInfo-Wert** in der [**SCRIPT \_ PROPERTIES-Struktur**](/windows/desktop/api/Usp10/ns-usp10-script_properties) für ein Element überprüfen, um zu überprüfen, ob **scriptBreak** zum Überprüfen auf gültige Caretpositionen erforderlich ist. Wenn der **fNeedsCaretInfo-Wert** **FALSE ist,** sind alle Codepunkte gültige Caretpositionen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 




