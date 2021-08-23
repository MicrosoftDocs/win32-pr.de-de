---
description: Ein komplexes Skript ist ein Skript, für das der fComplex-Member von SCRIPT \_ PROPERTIES auf TRUE festgelegt ist. In diesem Thema werden die Eigenschaften eines komplexen Skripts beschrieben.
ms.assetid: bceeb0d6-bda3-43bf-984e-87fbfb327578
title: Informationen zu komplexen Skripts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1e865b7638419178e3339169e56e8ceb111bcc65b925d9c337b5b71d0341827
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119520650"
---
# <a name="about-complex-scripts"></a>Informationen zu komplexen Skripts

Ein [komplexes Skript](uniscribe-glossary.md) ist ein Skript, für das **der fComplex-Member** von [**SCRIPT \_ PROPERTIES**](/windows/desktop/api/Usp10/ns-usp10-script_properties) auf **TRUE festgelegt ist.** In diesem Thema werden die Eigenschaften eines komplexen Skripts beschrieben.

## <a name="bidirectional-rendering"></a>Bidirektionales Rendering

Bidirektionales Rendering ist die Verarbeitung von Text, der sowohl von links nach rechts als auch von rechts nach links liest. Beim bidirektionalen Rendering von Arabisch ist die Standardleserichtung für Text beispielsweise von rechts nach links, aber für einige Zahlen von links nach rechts. Bei der Verarbeitung eines komplexen Skripts muss der Unterschied zwischen der logischen Reihenfolge (Tastatureingabe) und der visuellen Reihenfolge der Glyphen berücksichtigt werden. Darüber hinaus muss die Verarbeitung mit Caretbewegungen und Treffertests ordnungsgemäß umgehen. Die Zuordnung zwischen bildschirmposition und einem Zeichenindex erfordert ein Verständnis der Layoutalgorithmen für die bestimmte Anzeige, z. B. die Auswahl der Text- oder Caretanzeige.

## <a name="contextual-shaping"></a>Kontextbezogenes Gestalten

Bei der kontextbezogenen Gestaltung ändern Skriptzeichen die Form abhängig von den Zeichen, die sie umschließen. Eine solche Formung erfolgt beim englischsprachigen cursive Writing, wenn ein klein geschriebenes "l" die Form abhängig von dem Zeichen ändert, das ihm voran steht, z. B. ein "a" (verbindet sich niedrig mit dem "l") oder ein "o" (verbindet hoch). Arabisch ist z. B. ein Skript, das eine kontextbezogene Gestaltung auf zeigt.

## <a name="combining-characters"></a>Kombinieren von Zeichen

Kombinierende Zeichen, die auch als "Ligaturen" bezeichnet werden, sind Zeichen, die zu einem Zeichen kombiniert werden, wenn sie zusammen platziert werden. Arabisch ist ein Skript mit vielen kombinierenden Zeichen. Ein Beispiel für die Verwendung der Kombination von Zeichen ist das "a", gefolgt von "kombinierenden Darstellungen", für die die gerenderte Darstellung "änder" ist. Der Unicode-Stream "U+0061 U+0300" erfordert einige Verarbeitungen, um sicherzustellen, dass die "kombinierende Zeichenfolge" ordnungsgemäß über dem "a" positioniert ist.

## <a name="specialized-word-break-and-justification"></a>Spezialisierte Wörterbruch und Begründung

Einige Skripts, z. B. Thailändisch, verfügen über komplexe Regeln zum Teilen von Wörtern zwischen Zeilen oder zum Rechtfertigen von Text in einer Zeile.

## <a name="filtering-for-illegal-character-combinations"></a>Filtern nach unzulässigen Zeichenkombinationen

Ein komplexes Skript, z. B. Thailändisch, kann unzulässige Zeichenkombinationen herausfiltern, wenn eine Sprache bestimmte Zeichenkombinationen nicht zulädt.

## <a name="font-fallback"></a>Schriftartfallback

Ein Schriftartfallback ist die automatisierte Auswahl einer anderen Schriftart als der vom Benutzer ausgewählten Schriftart. In Uniscribe wird das Schriftartfallback von der [**ScriptStringAnalyse-Funktion**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse) angewendet, wenn sich der text ganz oder teilweise in einem Skript befindet, das die vom Benutzer ausgewählte Schriftart nicht unterstützt. Weitere Informationen finden Sie unter [Verwenden des Schriftartfallbacks.](using-font-fallback.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu Uniscribe](about-uniscribe.md)
</dt> </dl>

 

 



