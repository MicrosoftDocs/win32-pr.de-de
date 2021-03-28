---
description: Alle Schriftarten verwenden einen Zeichensatz. Ein Zeichensatz enthält Satzzeichen, Ziffern, groß-und Kleinbuchstaben sowie alle anderen druckbaren Zeichen. Jedes Element eines Zeichensatzes wird durch eine Zahl identifiziert.
ms.assetid: 7989c59e-2ec6-4d1a-bb86-f4037ca32764
title: Von Schriftarten verwendete Zeichensätze
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e33c4c5cc193c4474b39113acdedafec699456e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978800"
---
# <a name="character-sets-used-by-fonts"></a>Von Schriftarten verwendete Zeichensätze

Alle Schriftarten verwenden einen Zeichensatz. Ein Zeichensatz enthält Satzzeichen, Ziffern, groß-und Kleinbuchstaben sowie alle anderen druckbaren Zeichen. Jedes Element eines Zeichensatzes wird durch eine Zahl identifiziert.

Die meisten verwendeten Zeichensätze sind übergeordnete Zeichen des US-ASCII-Zeichensatzes, der Zeichen für die numerischen 96-Werte von 32 bis 127 definiert. Es gibt fünf Hauptgruppen von Zeichensätzen:

-   Windows
-   Unicode
-   OEM (Originalgerätehersteller)
-   Symbol
-   Hersteller spezifisch

## <a name="windows-character-set"></a>Windows-Zeichensatz

Der Windows-Zeichensatz ist der am häufigsten verwendete Zeichensatz. Sie entspricht im Wesentlichen dem ANSI-Zeichensatz. Das leere Zeichen ist das erste Zeichen im Windows-Zeichensatz. Sie hat einen hexadezimalen Wert von 0x20 (Decimal 32). Das letzte Zeichen im Windows-Zeichensatz hat den Hexadezimalwert 0xFF (Decimal 255).

Viele Schriftarten geben ein Standard Zeichen an. Wenn eine Anforderung für ein Zeichen erfolgt, das nicht in der Schriftart enthalten ist, stellt das System dieses Standard Zeichen bereit. Viele Schriftarten, die den Windows-Zeichensatz verwenden, geben den Zeitraum (.) als Standard Zeichen an. TrueType-und OpenType-Schriftarten verwenden normalerweise ein geöffnetes Feld als Standard Zeichen.

Schriftarten verwenden ein Umbruch Zeichen, das als Quad bezeichnet wird, um Wörter zu trennen und Text rechtfertigen. Die meisten Schriftarten, die den Windows-Zeichensatz verwenden, geben an, dass das leere Zeichen als Bruchzeichen dienen soll.

## <a name="unicode-character-set"></a>Unicode-Zeichensatz

Der Windows-Zeichensatz verwendet 8 Bits zur Darstellung der einzelnen Zeichen. Daher ist die maximale Anzahl von Zeichen, die mithilfe von 8 Bits ausgedrückt werden kann, 256 (2 ^ 8). Dies ist in der Regel für westliche Sprachen ausreichend, einschließlich der diakritischen Zeichen, die in Französisch, Deutsch, Spanisch und anderen Sprachen verwendet werden. Allerdings verwenden Ostsprachen Tausende von separaten Zeichen, die nicht mithilfe eines Single-Byte-Codierungs Schemas codiert werden können. Mit der zunehmenden Verbreitung von Computer Commerce wurden Doppelbyte-Codierungs Schemas entwickelt, sodass Zeichen in 8-Bit-, 16-Bit-, 24-Bit-oder 32-Bit-Sequenzen dargestellt werden können. Dies erfordert komplizierte Übergabe Algorithmen. die Verwendung unterschiedlicher Codesets könnte sogar zu unterschiedlichen Ergebnissen auf zwei verschiedenen Computern führen.

Um das Problem mehrerer Codierungs Schemas zu beheben, wurde der Unicode-Standard für die Datendarstellung entwickelt. Ein 16-Bit-Zeichen Codierungsschema (Unicode) kann 65.536 (2 ^ 16) Zeichen darstellen. Dies reicht aus, um heute alle Sprachen in den Computerhandel aufzunehmen, sowie Satzzeichen, mathematische Symbole und Raum für die Erweiterung. Unicode erstellt für jedes Zeichen einen eindeutigen Code, um sicherzustellen, dass die Zeichen Übersetzung immer genau ist.

## <a name="oem-character-set"></a>OEM-Zeichensatz

Der OEM-Zeichensatz wird in der Regel in voll Bild-MS-DOS-Sitzungen für die Bildschirm Anzeige verwendet. Die Zeichen 32 bis 127 sind normalerweise in den Zeichensätzen OEM, US-ASCII und Windows identisch. Die anderen Zeichen im OEM-Zeichensatz (0 bis 31 und 128 bis 255) entsprechen den Zeichen, die in einer-voll Bild-MS-DOS-Sitzung angezeigt werden können. Diese Zeichen unterscheiden sich in der Regel von den Windows-Zeichen.

## <a name="symbol-character-set"></a>Symbol Zeichensatz

Der Symbol Zeichensatz enthält Sonderzeichen, die in der Regel zur Darstellung mathematischer und wissenschaftlicher Formeln verwendet werden.

## <a name="vendor-specific-character-sets"></a>Herstellerspezifische Zeichensätze

Viele Drucker und andere Ausgabegeräte stellen Schriftarten auf Grundlage von Zeichensätzen bereit, die sich vom Windows-und OEM-setset unterscheiden, z. b. der Extended Binary Coded Decimal Interchange Code (EBCDIC)-Zeichensatz. Um einen dieser Zeichensätze zu verwenden, übersetzt der Druckertreiber aus dem Windows-Zeichensatz in den herstellerspezifischen Zeichensatz.

 

 



