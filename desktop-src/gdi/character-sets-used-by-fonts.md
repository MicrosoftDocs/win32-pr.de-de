---
description: Alle Schriftarten verwenden einen Zeichensatz. Ein Zeichensatz enthält Satzzeichen, Ziffern, Groß- und Kleinbuchstaben sowie alle anderen druckbaren Zeichen. Jedes Element eines Zeichensatzes wird durch eine Zahl identifiziert.
ms.assetid: 7989c59e-2ec6-4d1a-bb86-f4037ca32764
title: Von Schriftarten verwendete Zeichensätze
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4ec30a82c08a0b9ac1162034b6308bb68ff7dc1c6469e5e73bad2838b528eef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119779360"
---
# <a name="character-sets-used-by-fonts"></a>Von Schriftarten verwendete Zeichensätze

Alle Schriftarten verwenden einen Zeichensatz. Ein Zeichensatz enthält Satzzeichen, Ziffern, Groß- und Kleinbuchstaben sowie alle anderen druckbaren Zeichen. Jedes Element eines Zeichensatzes wird durch eine Zahl identifiziert.

Die meisten verwendeten Zeichensätze sind Obermengen des US-ASCII-Zeichensatzes, der Zeichen für die 96 numerischen Werte von 32 bis 127 definiert. Es gibt fünf Hauptgruppen von Zeichensätzen:

-   Windows
-   Unicode
-   OEM (Originalgerätehersteller)
-   Symbol
-   Herstellerspezifisch

## <a name="windows-character-set"></a>Windows Zeichensatz

Der Windows Zeichensatz ist der am häufigsten verwendete Zeichensatz. Sie entspricht im Wesentlichen dem ANSI-Zeichensatz. Das leere Zeichen ist das erste Zeichen im Windows Zeichensatzes. Er hat den Hexadezimalwert 0x20 (Dezimalzahl 32). Das letzte Zeichen im Windows Zeichensatzes weist den Hexadezimalwert 0xFF (Dezimalzahl 255) auf.

Viele Schriftarten geben ein Standardzeichen an. Wenn eine Anforderung für ein Zeichen gestellt wird, das nicht in der Schriftart enthalten ist, stellt das System dieses Standardzeichen bereit. Viele Schriftarten, die den Windows Zeichensatz verwenden, geben den Punkt (.) als Standardzeichen an. TrueType- und OpenType-Schriftarten verwenden in der Regel ein offenes Feld als Standardzeichen.

Schriftarten verwenden ein Haltezeichen, das als Quad bezeichnet wird, um Wörter zu trennen und Text zu rechtfertigen. Die meisten Schriftarten, die den Windows Zeichensatz verwenden, geben an, dass das leere Zeichen als Haltezeichen dient.

## <a name="unicode-character-set"></a>Unicode-Zeichensatz

Der Windows Zeichensatz verwendet 8 Bits, um jedes Zeichen darzustellen. daher beträgt die maximale Anzahl von Zeichen, die mit 8 Bits ausgedrückt werden können, 256 (2^8). Dies ist in der Regel für die älteren Sprachen ausreichend, einschließlich der diakritischen Markierungen, die in Französisch, Deutsch, Spanisch und anderen Sprachen verwendet werden. Die einheitlichen Sprachen verwenden jedoch Tausende von separaten Zeichen, die nicht mithilfe eines Codierungsschemas mit einem Byte codiert werden können. Mit der zunehmenden Verbreitung von Computerhandel wurden Double-Byte-Codierungsschemas entwickelt, sodass Zeichen in 8-Bit-, 16-Bit-, 24-Bit- oder 32-Bit-Sequenzen dargestellt werden konnten. Dies erfordert komplizierte Übergabealgorithmen. dennoch kann die Verwendung verschiedener Codesätze zu völlig unterschiedlichen Ergebnissen auf zwei verschiedenen Computern führen.

Um das Problem mehrerer Codierungsschemas zu beheben, wurde der Unicode-Standard für die Datendarstellung entwickelt. Ein 16-Bit-Zeichencodierungsschema, Unicode, kann 65.536 (2^16) Zeichen darstellen. Dies reicht aus, um heute alle Sprachen im Computerhandel sowie Interpunktionszeichen, mathematische Symbole und Erweiterungsmöglichkeiten einzubeziehen. Unicode richtet einen eindeutigen Code für jedes Zeichen ein, um sicherzustellen, dass die Zeichenübersetzung immer genau ist.

## <a name="oem-character-set"></a>OEM-Zeichensatz

Der OEM-Zeichensatz wird in der Regel in MS-DOS-Vollbildsitzungen für die Bildschirmanzeige verwendet. Die Zeichen 32 bis 127 sind im OEM-, US-ASCII- und Windows Zeichensätzen in der Regel identisch. Die anderen Zeichen im OEM-Zeichensatz (0 bis 31 und 128 bis 255) entsprechen den Zeichen, die in einer MS-DOS-Vollbildsitzung angezeigt werden können. Diese Zeichen unterscheiden sich im Allgemeinen von den Windows Zeichen.

## <a name="symbol-character-set"></a>Symbolzeichensatz

Der Zeichensatz Symbol enthält Sonderzeichen, die normalerweise zur Darstellung mathematischer und wissenschaftlicher Formeln verwendet werden.

## <a name="vendor-specific-character-sets"></a>Herstellerspezifische Zeichensätze

Viele Drucker und andere Ausgabegeräte stellen Schriftarten bereit, die auf Zeichensätzen basieren, die sich von den Windows- und OEM-Sätzen unterscheiden, z. B. dem Extended Binary Coded Decimal Interchange Code (EBCDIC) Zeichensatz. Um einen dieser Zeichensätze zu verwenden, übersetzt der Druckertreiber aus dem Windows Zeichensatzes in den herstellerspezifischen Zeichensatz.

 

 



