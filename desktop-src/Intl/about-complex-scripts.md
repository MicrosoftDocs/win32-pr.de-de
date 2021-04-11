---
description: Bei einem komplexen Skript handelt es sich um ein Skript, für das der fcomplex-Member der Skript \_ Eigenschaften auf true festgelegt ist. In diesem Thema werden die Eigenschaften erläutert, die möglicherweise in einem komplexen Skript vorhanden sind.
ms.assetid: bceeb0d6-bda3-43bf-984e-87fbfb327578
title: Informationen zu komplexen Skripts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edb1929a58e7810fb51bcb2b7a6bf9d5a762282e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042545"
---
# <a name="about-complex-scripts"></a>Informationen zu komplexen Skripts

Bei einem [komplexen Skript](uniscribe-glossary.md) handelt es sich um ein Skript, für das der **fcomplex** -Member der [**Skript \_ Eigenschaften**](/windows/desktop/api/Usp10/ns-usp10-script_properties) auf **true** festgelegt ist. In diesem Thema werden die Eigenschaften erläutert, die möglicherweise in einem komplexen Skript vorhanden sind.

## <a name="bidirectional-rendering"></a>Bidirektionales Rendering

Bidirektionales Rendering ist die Behandlung von Text, der sowohl von links nach rechts und von rechts nach links liest. Bei der bidirektionalen Darstellung von Arabisch ist die Standard Leserichtung für Text z. b. von rechts nach links, aber für einige Zahlen von links nach rechts. Die Verarbeitung eines komplexen Skripts muss den Unterschied zwischen der logischen Reihenfolge (Keystroke) und der visuellen Reihenfolge der Symbole berücksichtigen. Außerdem muss bei der Verarbeitung der Caretzeichen und Treffer Tests ordnungsgemäß behandelt werden. Die Zuordnung zwischen Bildschirmposition und Zeichen Index erfordert ein Verständnis der Layoutalgorithmen für die jeweilige Anzeige, z. b. die Auswahl von Text-oder Caretzeichen.

## <a name="contextual-shaping"></a>Kontextabhängige Strukturierung

In der kontextbezogenen Strukturierung ändern Skript Zeichen die Form abhängig von den Zeichen, die Sie umschließen. Eine solche Strukturierung findet in einem englischen, kursiven schreiben statt, wenn eine Form vom Typ "l" vom Typ "l" abhängig von dem vorangestellenden Zeichen geändert wird, z. b. "a" (mit niedriger Verbindung mit "l") oder "o" (mit hoher Verbindung). Arabisch ist beispielsweise ein Skript, das die Kontext Bildung veranschaulicht.

## <a name="combining-characters"></a>Kombinieren von Zeichen

Das Kombinieren von Zeichen, auch als "Ligaturen" bezeichnet, sind Zeichen, die beim Platzieren in ein Zeichen eingebunden werden. Arabisch ist ein Skript, das viele kombinierte Zeichen enthält. Ein Beispiel für die Kombination von Zeichen ist "a", gefolgt von "Kombinieren von Grab", bei dem die gerenderte Darstellung "a" ist. Der Unicode-Stream "U + 0061 U + 0300" erfordert einige Verarbeitungsschritte, um sicherzustellen, dass das "kombinierte Grab" ordnungsgemäß über "a" positioniert ist.

## <a name="specialized-word-break-and-justification"></a>Spezialisierte Wort Umbruch und-Begründung

Einige Skripts, z. b. Thai, haben komplexe Regeln für das Aufteilen von Wörtern zwischen Zeilen oder das rechtfertigen von Text in einer Zeile.

## <a name="filtering-for-illegal-character-combinations"></a>Filtern nach unzulässigen Zeichenkombinationen

Ein komplexes Skript, z. b. Thai, kann unzulässige Zeichenkombinationen herausfiltern, wenn eine Sprache bestimmte Zeichenkombinationen nicht zulässt.

## <a name="font-fallback"></a>Schriftart-Fallback

Bei einem Schriftart Fall Back handelt es sich um die automatisierte Auswahl einer anderen Schriftart als der vom Benutzer ausgewählten Schriftart. In uniwriter wird das Schriftart-Fall Back von der [**scriptstringanalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse) -Funktion angewendet, wenn sich der gesamte Text oder ein Teil des Texts in einem Skript befindet, das von der vom Benutzer ausgewählten Schriftart nicht unterstützt wird. Weitere Informationen finden Sie unter [using Font Fallback](using-font-fallback.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu uniscri](about-uniscribe.md)
</dt> </dl>

 

 



