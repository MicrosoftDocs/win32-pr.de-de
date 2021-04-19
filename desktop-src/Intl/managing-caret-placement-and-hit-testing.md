---
description: Komplexe Skriptsprachen werden von scriptshape in Cluster unterteilt. Die Neuanordnen von Zeichen erfolgt immer innerhalb von Cluster Grenzen. Es ist garantiert, dass die Cluster selbst in der Richtung der Lesefolge fortgeführt werden.
ms.assetid: 50b4b643-af96-4a6f-80f9-27a71ce16b0e
title: Verwalten der Platzierung von Caretzeichen und Treffer Tests
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60396a668c89f7392b28adde0bb123060bf50348
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348841"
---
# <a name="managing-caret-placement-and-hit-testing"></a>Verwalten der Platzierung von Caretzeichen und Treffer Tests

Komplexe Skriptsprachen werden von [**scriptshape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape)in [Cluster](uniscribe-glossary.md) unterteilt. Die Neuanordnen von Zeichen erfolgt immer innerhalb von Cluster Grenzen. Es ist garantiert, dass die Cluster selbst in der Richtung der Lesefolge fortgeführt werden.

Cluster Informationen im Array logischer Cluster werden verwendet, um die Breite eines Clusters von Symbolen gleichmäßig auf die logischen Zeichen zu verteilen, die Sie darstellen. Beispielsweise ist das Symbol "Lam Alef" in vier Bereiche unterteilt:

-   Die führende Hälfte der Lam.
-   Die nachfolgende Hälfte des Lam.
-   Die führende Hälfte von Alef.
-   Die nachfolgende Hälfte der Alef.

Konventionen für die Platzierung von Caretzeichen innerhalb von Clustern sind vom Skript abhängig. Wenn für das Arabische Skript die Position der Einfügemarke zwischen einem Basiszeichen und der zugehörigen Markierung festgelegt ist, wird die Einfügemarke in der Mitte des Basis Zeichens angezeigt. Für das thailändische Skript kann die Einfügemarke nicht innerhalb eines Clusters positioniert werden. Wenn der Benutzer also die Einfügemarke verschiebt, muss sich die Anwendung hinter allen Symbolen befinden, aus denen der Cluster besteht.

Die Funktionen [**scriptxycp**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp) und [**scriptcptox**](/windows/desktop/api/Usp10/nf-usp10-scriptcptox) übersetzen zwischen Caretzeichen (in Code Punkt Offsets) und x-Positionen (in Pixel). Die **scriptxtoicp** -Funktion kennt die Positions Konventionen der Einfügemarke der einzelnen Skripts:

-   Für indische und Thai werden Einfügepositionen an Cluster Grenzen ausgerichtet.
-   Bei Arabisch werden Caretzeichen mit Clustern interpoliert.
-   Bei Hebräisch werden in Versionen vor Usp10.dll, Version 1,420, Einfügepositionen mit Clustern interpoliert. Beginnend mit Usp10.dll, Version 1,420, werden Einfügepositionen an Cluster Grenzen ausgerichtet.

[**Scriptxtcp**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp) und [**scriptcptox**](/windows/desktop/api/Usp10/nf-usp10-scriptcptox) funktionieren nur innerhalb von Ausführungen. Die Funktionen erfordern, dass bestimmte Parameter aus früheren uniscrietaufrufen stammen, wie in der folgenden Tabelle dargestellt.



| Parameter                                        | `Source`                                                 |
|--------------------------------------------------|--------------------------------------------------------|
| *PSA*                                            | Wie von [**scriptitemize**](/windows/desktop/api/Usp10/nf-usp10-scriptitemize)zurückgegeben. |
| *cglyphspwlogclust*<br/> *psva*<br/> | Wie von [**scriptshape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape)zurückgegeben.     |
| *piadvance*                                      | Wie von [**scriptplace**](/windows/desktop/api/Usp10/nf-usp10-scriptplace)zurückgegeben.     |



 

Die Anwendung muss den Testlauf einrichten, in dem eine bestimmte Einfügemarke oder x-Position vor dem übergeben der Informationen an [**scriptcptox**](/windows/desktop/api/Usp10/nf-usp10-scriptcptox) oder [**scriptxtocp**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp)liegt. Wenn die Anwendung die breiten Informationen nicht speichert, kann Sie nach dem Anzeigen der einzelnen Testlauf die Treffer Tests und die Platzierung der Einfügemarke durchführen. Als Alternative kann die Anwendung genug Informationen zwischenspeichern, um Treffer Tests und einfügeplatzierung in der aktuellen Zeile zu erreichen, ohne dass der Absatz verarbeitet werden muss.

[**Scriptxescp**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp) gibt einen nachfolgenden Edge-Wert zurück, sodass die Anwendung die Seite des Zeichens oder Clusters kennt, auf die der Benutzer geklickt hat. Der Wert ist entweder 0 oder die Breite des Zeichens oder Clusters in Code Punkten. Die zurückgegebene Zeichenposition ist die Position des Zeichens, auf das der Benutzer geklickt hat. Weitere Informationen finden Sie unter Anzeigen der Einfügemarke [in bidirektionalen](displaying-the-caret-in-bidirectional-strings.md)Zeichen folgen.

Für Sprachen wie z. b. Thai, bei denen der Benutzer die Einfügemarke nicht in einem Cluster platzieren will, legt [**scriptxdecp**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp) das Flag der nachfolgenden Seite auf 0 oder die Cluster Breite fest. Für Sprachen, wie z. b. Arabisch, für die der Benutzer die Bearbeitung innerhalb eines Clusters erwartet, legt **scriptxescp** das Flag für die nachfolgende Seite auf 0 oder auf 1 fest.

Damit die Anwendung bei der Verarbeitung der Pfeiltasten gültige Speicherorte für die Einfügemarke festlegt, stellt uniscriinformationen zu gültigen Einfügepositionen im **fcharstoppmember** in den von [**scriptbreak**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak)zurückgegebenen logischen Attributen bereit. " **True** " wird für die meisten Zeichen und " **false** " für Austausch Zeichen in Skripts wie "Thai" zurückgegeben. Die Anwendung sollte den **fneedscaretinfo** -Wert in der [**Skript \_ Eigenschaften**](/windows/desktop/api/Usp10/ns-usp10-script_properties) Struktur für ein Element überprüfen, um festzustellen, ob es erforderlich ist, **scriptbreak** aufzurufen, um nach gültigen Einfügepositionen zu suchen. Wenn der **fneedscaretinfo** -Wert " **false**" lautet, sind alle Code Punkte gültige Einfügemarke.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von uniscri](using-uniscribe.md)
</dt> </dl>

 

 




