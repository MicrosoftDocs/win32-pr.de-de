---
description: Eine ABC-Breite ist ein zusammengesetzter Wert, der durch eine GDI-ABC-Struktur definiert wird. Die -Struktur enthält die Member abcA, abcB und abcC, die dem &\# 0034; Ein&\# 0034;, &\# 0034; B&\# 0034; und &\# 0034; C&\# 0034; Breiten eines Glyphen oder einer Ausführung.
ms.assetid: 48c766e5-a69d-47d2-a885-f24b80e910d8
title: Uniscribe Glossary
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 808ff2e9620810fe2ec344a037437e6ce8d62bff9460a53cf7b777cedc9d46b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146971"
---
# <a name="uniscribe-glossary"></a>Uniscribe Glossary

Eine ABC-Breite ist ein zusammengesetzter Wert, der durch eine [**GDI-ABC-Struktur definiert**](/windows/win32/api/wingdi/ns-wingdi-abc) wird. Die -Struktur enthält die Member **abcA,** **abcB** und **abcC,** die den Breiten "A", "B" und "C" eines [Glyphen](#glyph) oder [ausführen.](#run)

Die Breite "A" ist unterhängend [](#underhang) (positiv; auch als "Padding" bezeichnet) oder überhängen [(negativ)](#overhang) links neben dem Bildschirmäquivalent von Ink, das das Glyphen oder die Ausführung darstellt. Die Breite "B" ist die schwarze Breite, die Breite von der äußersten linken Ink bis zur äußersten rechten Ink-Breite. Die Breite "C" ist rechts neben der Ink-Klasse überhängend.

Die folgende Abbildung zeigt einen italischen Kleinbuchstaben F mit Überhängen links und rechts. Das heißt, die Breite von "A" und "C" ist hier negativ. Eine [Abbildung der](#underhang) positiven Breite von "A" und "C" finden Sie unter Unterhängen.

![Abbildung, die einen italischen Kleinbuchstaben F mit Überhängen links und rechts zeigt.](images/abcwidth.gif)

Wenn zwei oder mehr Glyphen als Einheit angezeigt werden, trägt in der Regel nur das linke Glyph zur Breite "A" der Ausführung bei, und nur das am weitesten rechts stehende Glyph trägt zur Breite "C" der Ausführung bei. Dies ist jedoch keine strikte Regel. Wenn z. B. das erste Glyphe in einer Ausführung ein schmaler Buchstabe ist und das zweite Glyph eine breite diakritische Markierung ist und als separate Glyphen behandelt wird, kann die diakritische Markierung tatsächlich über den Buchstaben hinausgehen.

## <a name="abc-width"></a>ABC-Breite

Eine ABC-Breite ist ein zusammengesetzter Wert, der durch eine [**GDI-ABC-Struktur definiert**](/windows/win32/api/wingdi/ns-wingdi-abc) wird. Die -Struktur enthält die Member **abcA,** **abcB** und **abcC,** die den Breiten "A", "B" und "C" eines [Glyphen](#glyph) oder [ausführen.](#run)

Die Breite "A" ist unterhängend [](#underhang) (positiv; auch als "Padding" bezeichnet) oder überhängen [(negativ)](#overhang) links neben dem Bildschirmäquivalent von Ink, das das Glyphen oder die Ausführung darstellt. Die Breite "B" ist die schwarze Breite, die Breite von der äußersten linken Ink bis zur äußersten rechten Ink-Breite. Die Breite "C" ist rechts neben der Ink-Klasse überhängend.

Die folgende Abbildung zeigt einen italischen Kleinbuchstaben F mit Überhängen links und rechts. Das heißt, die Breite von "A" und "C" ist hier negativ. Eine [Abbildung der](#underhang) positiven Breite von "A" und "C" finden Sie unter Unterhängen.

![Abbildung, die einen italischen Kleinbuchstaben F mit Überhängen links und rechts zeigt.](images/abcwidth.gif)

Wenn zwei oder mehr Glyphen als Einheit angezeigt werden, trägt in der Regel nur das linke Glyph zur Breite "A" der Ausführung bei, und nur das am weitesten rechts stehende Glyph trägt zur Breite "C" der Ausführung bei. Dies ist jedoch keine strikte Regel. Wenn z. B. das erste Glyphe in einer Ausführung ein schmaler Buchstabe ist und das zweite Glyph eine breite diakritische Markierung ist und als separate Glyphen behandelt wird, kann die diakritische Markierung tatsächlich über den Buchstaben hinausgehen.

## <a name="advance-width"></a>Breite nach vorn

Die Breite eines [Glyphens](#glyph) ist die Bewegung in Richtung des Schreibens vom Ausgangspunkt für das Rendern dieses Glyphen bis zum Ausgangspunkt für das Rendern des nächsten Glyphen.

## <a name="bidirectional-stack"></a>bidirektionaler Stapel

Der bidirektionale Stapel ist eine 5-Bit-Ganzzahl, die die Schachtelungsebenen zwischen Text von links nach rechts und von rechts nach links nachverfolgt. Er beginnt immer bei 0 (null) für von links nach rechts. Daher stellen alle werte mit gerader Zahl Text von links nach rechts dar, und alle ungeraden Werte stellen Text von rechts nach links dar. Der bidirektionale Stapel wird im **uBidiLevel-Member** einer [**SCRIPT \_ STATE-Struktur**](/windows/win32/api/usp10/ns-usp10-script_state) dargestellt.

## <a name="bidirectional-text"></a>Bidirektionaler Text

Bidirektionaler Text enthält sowohl von links nach rechts als auch von rechts nach links, aber der Begriff wird manchmal auch lose auf reinen Text von rechts nach links angewendet. Für den text von rechts nach links ist die Verwendung [](#embedding-level) des [bidirektionalen](#bidirectional-stack)Stapels erforderlich, da die Standardeinbettungsebene 0 (null) Text von links nach rechts impliziert.

## <a name="cell-width"></a>Zellenbreite

Eine Anwendung kann den Text für eine Linie rechtfertigen, indem sie die Zellenbreite für bestimmte Glyphen anpasst. Für den textierten Text ist die Zellenbreite für ein Glyph mit der [Vorbreite identisch.](#advance-width)

## <a name="cluster"></a>cluster

Ein Cluster ist die kleinste linguistische Einheit, die gestaltet werden kann. In Sprachen wie Arabisch und vielen der indischen Sprachen hängen die Glyphen, die zum Darstellen der einzelnen Zeichen (Unicode-Codepunkt) verwendet werden, stark von den umgebenden Codepunkten ab, die den Cluster bilden. In diesen Sprachen können Anwendungen Codepunkte nur über den Cluster in entsprechende Glyphen übersetzen. In einigen Skripts, z. B. Devanainnen, kann sich die Reihenfolge der Glyphen innerhalb eines Clusters von der Reihenfolge der entsprechenden Unicode-Codepunkte unterscheiden. Weitere Informationen finden Sie unter [Windows Glyphenverarbeitung](/typography/develop/processing-part1) auf der Microsoft-Website für Typografie.

## <a name="complex-script"></a>Komplexes Skript

Ein komplexes Skript ist [ein Skript](#complex-script) mit einer der folgenden Eigenschaften:

-   Ermöglicht bidirektionales Rendering.
-   Verfügt über eine kontextbezogene Gestaltung.
-   Verfügt über kombinierende Zeichen.
-   Verfügt über spezielle Wortbruch- und Begründungsregeln.
-   Filtert unzulässige Zeichenkombinationen heraus.
-   Wird im Core-Windows nicht unterstützt und erfordert daher möglicherweise einen [Schriftartfallback.](#font-fallback)

In einigen komplexen Skripts kann sich die Reihenfolge der Symbolen von der Reihenfolge der zugrunde liegenden Unicode-Zeichen unterscheiden, die sie darstellen. Weitere [Informationen finden Sie unter](about-complex-scripts.md) Informationen zu komplexen Skripts.

> [!Note]  
> Im Kontext der Typografie ist es manchmal wünschenswert, das lateinische Skript, das beim Schreiben von Englisch verwendet wird, als komplexes Skript zu behandeln. Beispiele hierfür sind das feature "Styleic Alternates", das in der Dokumentation zu [**OPENTYPE \_ FEATURE \_ RECORD**](/windows/desktop/api/Usp10/ns-usp10-opentype_feature_record)beschrieben wird, oderLigaturen wie "fi", bei denen ein einzelnes Glyph zwei oder mehr aufeinander folgende Zeichen darstellt.

 

## <a name="embedding-level"></a>Einbettungsebene

In [bidirektionalem Text](#bidirectional-text)ist die Einbettungsebene der Index des [bidirektionalen Stapels.](#bidirectional-stack)

## <a name="font-fallback"></a>Schriftartfallback

Ein Schriftartfallback ist eine automatisierte Auswahl einer anderen Schriftart als der Schriftart, die vom Benutzer in einer Anwendung ausgewählt wurde. In Uniscribe wird das Schriftartfallback von der [**ScriptStringAnalyse-Funktion**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse) angewendet, wenn sich der text ganz oder teilweise in einem Skript befindet, das die vom Benutzer ausgewählte Schriftart nicht unterstützt.

## <a name="glyph"></a>Symbol

Ein Glyph ist eine einzelne Einheit der Anzeige in einer Schriftart. Für OpenType wird diese Einheit durch eine Gliederung definiert. Für andere Arten von Schriftarten kann sie durch eine Bitmap, eine Reihe von grafischen Befehlen und deren Art definiert werden. Ein Glyphen entspricht nicht unbedingt einem einzelnen Zeichen. Beispielsweise stellt die Fi-Ligatur ("fi") die beiden Zeichen "f" und "i" dar. Das Kleinbuchstabe "o" mit Strichflex und Tilde ("ỗ") besteht in der Regel aus mehreren Glyphen.

## <a name="item"></a>item

Ein Element verfügt über ein [einzelnes Skript und](#complex-script) eine einzelne Richtung. Die [**ScriptItemize-**](/windows/desktop/api/Usp10/nf-usp10-scriptitemize) [**oder ScriptItemizeOpenType-Funktion**](/windows/desktop/api/usp10/nf-usp10-scriptitemizeopentype) kann einen Absatz in Elemente analysieren. Ein Element ist nicht notwendigerweise ein [ausgeführter](#run). Sie kann Zeichen mehrerer Formate enthalten. Element- und Ausführungsinformationen müssen kombiniert werden, um Bereiche [zu bestimmen.](#range)

## <a name="lrm"></a>Lrm

LRM gibt die LINKS-NACH-RECHTS-MARKIERUNG (Unicode-Codepunkt U+200E) an. Diese Markierung gibt an, dass darauf folgende Zeichen in logischer Reihenfolge von links nach rechts gerendert werden sollen.

## <a name="ltr"></a>Ltr

LTR gibt von links nach rechts an.

## <a name="range"></a>range

Ein Bereich ist ein Sonderfall einer [Ausführung.](#run) Er fällt vollständig in ein [Element.](#item) Wenn also ein Element in Läufe zerbrochen wird, ist jede dieser Läufe ein Bereich.

## <a name="rlm"></a>Rlm

RLM gibt die RECHTS-NACH-LINKS-MARKIERUNG (Unicode-Codepunkt U+200F) an. Diese Markierung gibt an, dass zeichen, die ihm folgen, in logischer Reihenfolge von rechts nach links gerendert werden sollen.

## <a name="rtl"></a>RTL

RTL gibt von rechts nach links an.

## <a name="run"></a>Run

Eine Ausführung ist eine Textzeile, die Von Uniscribe gerendert werden kann. It should have a single style, that is, font, size, and color, but can be drawn from a variety of [scripts](#complex-script). Eine Ausführung kann sowohl Inhalt von links nach rechts als auch von rechts nach links enthalten.

## <a name="nads"></a>BEITENS

CODS gibt NATIONAL DIGIT SHAPES an (Unicode-Codepunkt U+206E. Der Begriff gibt an, dass europäische Ziffern (U+0030 bis U+0039) als nationale Ziffern gerendert werden sollen. Weitere [Informationen zu nationalen](digit-shapes.md) Ziffern finden Sie unter Ziffernformen.

## <a name="nods"></a>Nickt

NODS gibt NOMINAL DIGIT SHAPES (Unicode-Codepunkt U+206F) an. Der Begriff gibt an, dass europäische Ziffern (U+0030 bis U+0039) normal und nicht als nationale Ziffern gerendert werden sollen.

## <a name="overhang"></a>Überhang

Der Überhänge ist der Teil der Ink eines Glyphens, der über die [erweiterte Breite](#advance-width) des Glyphen hinausgeht. Die meisten Glyphen (z. B. "H") weisen keinen Überhang auf, da auf beiden Seiten ein wenig Leerraum vorhanden ist, um sie von benachbarten Glyphen zu trennen. Ein Beispiel für ein Glyphen mit Überhängen ist das in diesem Thema verwendete italische "f", um die [ABC-Breite](#abc-width)zu veranschaulichen. Sowohl der obere als auch der untere Rand des italischen "f" überhängen die angrenzenden Glyphen. Overhang entspricht einer negativen Breite von "A" oder "C".

## <a name="padding"></a>Auffüllung

Siehe [underhang](#underhang).

## <a name="script"></a>script

Ein Skript ist ein System geschriebener Sprache, z. B. lateinisches Skript, arabisches Skript, chinesisches Skript. Ein einzelnes Skript kann auf eine oder mehrere menschliche Sprachen angewendet werden. Das Skript hat keine bestimmte Beziehung zu einer Schriftart. Beispielsweise kann das lateinische Skript von der Schriftart Times New Roman oder Arial gleichermaßen gut gerendert werden.

## <a name="underhang"></a>underhang

Der Unterhang ist eine Breite von Leerraum links oder rechts vom durchgezogenen Teil eines Glyphen. Underhang entspricht einer positiven "A"- oder "C"-Breite, wie für [ABC-Breite](#abc-width)beschrieben. Underhang wird manchmal als "Auffüllung" bezeichnet. Die folgende Abbildung zeigt den Unterhang für den Kleinbuchstaben n.

![Abbildung, die den Unterhang für den Kleinbuchstaben n zeigt.](images/underhang.gif)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu Uniscribe](about-uniscribe.md)
</dt> </dl>

 

 
