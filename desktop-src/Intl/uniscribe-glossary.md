---
description: Eine ABC-Breite ist ein zusammengesetzter Wert, der durch eine GDI-ABC-Struktur definiert wird. Die Struktur enthält die Member ABCA, abcb und abcc entsprechend der &\# 0034; A&\# 0034;, &\# 0034; B&\# 0034;, und &\# 0034; C&\# 0034; Breite eines Symbols oder ausführen.
ms.assetid: 48c766e5-a69d-47d2-a885-f24b80e910d8
title: Glossar für uniscri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e154e65c103ce6e4287ac8aa2e76e0be4206f9fd
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "104316724"
---
# <a name="uniscribe-glossary"></a>Glossar für uniscri

Eine ABC-Breite ist ein zusammengesetzter Wert, der durch eine GDI- [**ABC**](/windows/win32/api/wingdi/ns-wingdi-abc) -Struktur definiert wird. Die Struktur enthält die Member **ABCA**, **abcb** und **ABCC**, die den breiten "a", "B" und "C [" eines Symbols entsprechen oder](#glyph) [ausgeführt](#run)werden.

Die Breite "A" ist nicht mehr [vorhanden (positiv](#underhang) , wird auch als "Auffüll Zeichen" bezeichnet) oder [überlastet](#overhang) (negativ) links neben dem Bildschirm auf dem Bildschirm, das das Symbol oder den Testlauf darstellt. Die Breite "B" ist die schwarze Breite, die Breite von der äußersten linken Handschrift zur rechten Handschrift. Die Breite "C" ist auf der rechten Seite der frei Hand Eingabe überlastet.

In der folgenden Abbildung wird eine kursiv Formatierung in Kleinbuchstaben dargestellt, bei der sowohl Links als auch rechts überlastet sind. Das heißt, die breiten "A" und "C" sind hier negativ. Eine Abbildung der positiven "A"-und "C"-breiten finden Sie [unter unterb](#underhang) .

![die Abbildung zeigt eine kursiv Formatierung in Kleinbuchstaben mit einem Überlauf sowohl auf der linken Seite als auch auf der rechten Seite.](images/abcwidth.gif)

Wenn zwei oder mehr Symbole als Einheit angezeigt werden, trägt in der Regel nur das ganz links äußere Symbol zur "a"-Breite des Testlaufs bei, und nur das äußteste Symbol trägt zur "C"-Breite der Testlauf bei. Dabei handelt es sich jedoch nicht um eine strikte Regel. Wenn z. b. das erste Symbol in einer Testlauf einen schmalen Buchstaben und das zweite Symbol ein breites diakritisches Zeichen ist und als separate Symbole behandelt werden, kann das diakritische Zeichen tatsächlich über den Buchstaben hinausgehen.

## <a name="abc-width"></a>ABC-Breite

Eine ABC-Breite ist ein zusammengesetzter Wert, der durch eine GDI- [**ABC**](/windows/win32/api/wingdi/ns-wingdi-abc) -Struktur definiert wird. Die Struktur enthält die Member **ABCA**, **abcb** und **ABCC**, die den breiten "a", "B" und "C [" eines Symbols entsprechen oder](#glyph) [ausgeführt](#run)werden.

Die Breite "A" ist nicht mehr [vorhanden (positiv](#underhang) , wird auch als "Auffüll Zeichen" bezeichnet) oder [überlastet](#overhang) (negativ) links neben dem Bildschirm auf dem Bildschirm, das das Symbol oder den Testlauf darstellt. Die Breite "B" ist die schwarze Breite, die Breite von der äußersten linken Handschrift zur rechten Handschrift. Die Breite "C" ist auf der rechten Seite der frei Hand Eingabe überlastet.

In der folgenden Abbildung wird eine kursiv Formatierung in Kleinbuchstaben dargestellt, bei der sowohl Links als auch rechts überlastet sind. Das heißt, die breiten "A" und "C" sind hier negativ. Eine Abbildung der positiven "A"-und "C"-breiten finden Sie [unter unterb](#underhang) .

![die Abbildung zeigt eine kursiv Formatierung in Kleinbuchstaben mit einem Überlauf sowohl auf der linken Seite als auch auf der rechten Seite.](images/abcwidth.gif)

Wenn zwei oder mehr Symbole als Einheit angezeigt werden, trägt in der Regel nur das ganz links äußere Symbol zur "a"-Breite des Testlaufs bei, und nur das äußteste Symbol trägt zur "C"-Breite der Testlauf bei. Dabei handelt es sich jedoch nicht um eine strikte Regel. Wenn z. b. das erste Symbol in einer Testlauf einen schmalen Buchstaben und das zweite Symbol ein breites diakritisches Zeichen ist und als separate Symbole behandelt werden, kann das diakritische Zeichen tatsächlich über den Buchstaben hinausgehen.

## <a name="advance-width"></a>Erweiterte Breite

Die erweiterte [Breite eines Symbols ist die](#glyph) Verschiebung in Richtung des Schreibvorgangs vom Startpunkt aus, um dieses Symbol an den Ausgangspunkt zum Rendern des nächsten Symbols zu rendern.

## <a name="bidirectional-stack"></a>bidirektionaler Stapel

Der bidirektionale Stapel ist eine 5-Bit-Ganzzahl, die Schachtelungs Ebenen zwischen von links nach rechts und von rechts nach links gerichteten Text nachverfolgt. Sie beginnt immer bei Null für von links nach rechts. Daher stellen alle gerade nummerierten Werte den Text von links nach rechts dar, und alle ungeraden Werte stellen Text von rechts nach links dar. Der bidirektionale Stapel wird im **ubidilevel** -Member einer [**Skript \_ Zustands**](/windows/win32/api/usp10/ns-usp10-script_state) Struktur dargestellt.

## <a name="bidirectional-text"></a>bidirektionaler Text

Der bidirektionale Text enthält sowohl von links nach rechts und von rechts nach links. der Begriff wird jedoch manchmal auch locker auf den reinen Text von rechts nach links angewendet. Für den Text von rechts nach links ist die Verwendung des [bidirektionalen Stapels](#bidirectional-stack)erforderlich, da der standardmäßige [Einbettungs Grad](#embedding-level) NULL den Text von links nach rechts impliziert.

## <a name="cell-width"></a>Zellen Breite

Eine Anwendung kann Text rechtfertigen, damit Sie in eine Linie passt, indem die Zellen Breite für bestimmte Symbole angepasst wird. Bei nicht ungerechtfertigtem Text ist die Zellen Breite für ein Symbol mit der entsprechenden [Vorlauf Breite](#advance-width)identisch.

## <a name="cluster"></a>cluster

Ein Cluster ist die kleinste linguistische Einheit, die strukturiert werden kann. In Sprachen wie Arabisch und vielen der indic-Sprachen sind die Symbole, die zur Darstellung der einzelnen Zeichen verwendet werden (Unicode-Codepunkt), stark von den umgebenden Code Punkten abhängig, die den Cluster bilden. In diesen Sprachen können Anwendungen Code Punkte nur durch die Betrachtung des Clusters in geeignete Symbole übersetzen. In einigen Skripts, wie z. b. Devanagari, kann die Reihenfolge der Symbole in einem Cluster von der Reihenfolge der entsprechenden Unicode-Code Punkte abweichen. Weitere Informationen finden Sie unter [Windows-Glyphe-Verarbeitung](/typography/develop/processing-part1) auf der Microsoft Typografiewebsite.

## <a name="complex-script"></a>komplexes Skript

Bei einem komplexen Skript handelt es sich um ein [Skript](#complex-script) mit einer der folgenden Eigenschaften:

-   Ermöglicht bidirektionales Rendering.
-   Hat kontextabhängige Strukturierung.
-   Weist kombinierte Zeichen auf.
-   Verfügt über spezielle Regeln für Wörter Trennung und Ausrichtung.
-   Filtert ungültige Zeichenkombinationen.
-   Wird in den Windows-Kern Schriftarten nicht unterstützt und erfordert daher möglicherweise einen [Schriftart Fall Back](#font-fallback).

In einigen komplexen Skripts kann sich die Reihenfolge der Symbole erheblich von der Reihenfolge der zugrunde liegenden Unicode-Zeichen unterscheiden, die Sie darstellen. Weitere Details finden Sie unter [Informationen zu komplexen Skripts](about-complex-scripts.md) .

> [!Note]  
> Im Zusammenhang mit der Typografie ist es manchmal wünschenswert, das lateinische Skript zu verarbeiten, das beim Schreiben von Englisch als komplexes Skript verwendet wird. Beispiele hierfür sind das in der Dokumentation von [**OpenType- \_ \_ featuredatensatz**](/windows/desktop/api/Usp10/ns-usp10-opentype_feature_record)beschriebene Feature "Stilvarianten" oder Ligaturen, wie z. b. "Fi", bei denen ein einzelnes Symbol zwei oder mehr aufeinander folgende Zeichen darstellt.

 

## <a name="embedding-level"></a>Einbettungs Ebene

In [bidirektionalem Text](#bidirectional-text)ist die Einbettungs Ebene der Index des [bidirektionalen Stapels](#bidirectional-stack).

## <a name="font-fallback"></a>Schriftart-Fall Back

Bei einem Schriftart Fall Back handelt es sich um eine automatisierte Auswahl einer anderen Schriftart als der Schriftart, die der Benutzer in einer Anwendung ausgewählt hat. In uniwriter wird das Schriftart-Fall Back von der [**scriptstringanalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse) -Funktion angewendet, wenn sich der gesamte Text oder ein Teil des Texts in einem Skript befindet, das von der vom Benutzer ausgewählten Schriftart nicht unterstützt wird.

## <a name="glyph"></a>Symbol

Ein Glyphe ist eine einzelne Anzeigeeinheit in einer Schriftart. Für OpenType wird diese Einheit durch eine Gliederung definiert. Bei anderen Arten von Schriftarten kann Sie durch eine Bitmap, eine Reihe von Grafik Befehlen und ähnliches definiert werden. Ein Symbol entspricht nicht notwendigerweise einem einzelnen Zeichen. Beispielsweise stellt "Fi" Ligaturen ("Fi") die beiden Zeichen "f" und "i" dar. Der Vietnamese-"o" in der Groß-/Kleinschreibung ist in der Regel aus mehreren Symbolen zusammengesetzt.

## <a name="item"></a>item

Ein Element verfügt über ein einzelnes [Skript](#complex-script) und eine Richtung. Die [**scriptitemize**](/windows/desktop/api/Usp10/nf-usp10-scriptitemize) -oder [**scriptitemizeopentype**](/windows/desktop/api/usp10/nf-usp10-scriptitemizeopentype) -Funktion kann einen Absatz in Elemente analysieren. Ein Element ist nicht notwendigerweise ein [Testlauf](#run). Sie kann Zeichen mehrerer Stile enthalten. Element-und laufinformationen müssen kombiniert werden, um [Bereiche](#range)zu bestimmen.

## <a name="lrm"></a>LRM

LRM gibt die Markierung von links nach rechts an (Unicode-Codepunkt U + 200E). Diese Markierung gibt an, dass die Zeichen in der logischen Reihenfolge von links nach rechts gerendert werden sollen.

## <a name="ltr"></a>Ltr

Ltr gibt von links nach rechts an.

## <a name="range"></a>range

Ein Bereich ist ein Sonderfall einer [Testlauf](#run). Sie liegt vollständig innerhalb eines [Elements](#item). Wenn ein Element in Ausführungen unterteilt wird, ist jeder dieser Ausführungen ein Bereich.

## <a name="rlm"></a>RLM

RLM gibt die rechts-nach-links-Markierung an (Unicode-Codepunkt U + 200F). Diese Markierung gibt an, dass die Zeichen in der logischen Reihenfolge von rechts nach links gerendert werden sollen.

## <a name="rtl"></a>RTL

RTL gibt von rechts nach links an.

## <a name="run"></a>Run

Ein Run ist ein Textabschnitt für das Rendering von uniwriter. Sie sollte einen einzelnen Stil aufweisen, d. h. Schriftart, Größe und Farbe, kann jedoch aus einer Vielzahl von [Skripts](#complex-script)gezeichnet werden. Ein Testlauf kann sowohl von links nach rechts und von rechts nach links und von rechts nach Links enthalten.

## <a name="nads"></a>NADS

NADS gibt nationale Ziffern Formen an (Unicode-Codepunkt U + 206E. Der Begriff gibt an, dass die europäischen Ziffern (u + 0030 bis u + 0039) als nationale Ziffern gerendert werden sollen. Weitere Erörterung von nationalen Ziffern finden Sie unter [Ziffern Formen](digit-shapes.md) .

## <a name="nods"></a>Knoten

Nods gibt nominale Ziffern Formen an (Unicode-Codepunkt U + 206F). Der Begriff gibt an, dass die europäischen Ziffern (u + 0030 bis u + 0039) normal gerendert werden sollen, nicht als nationale Ziffern.

## <a name="overhang"></a>hinausragen

Der über Hang ist der Teil der frei Hand Eingabe eines Symbols, das die erweiterte [Breite](#advance-width) des Symbols überschreitet. Die meisten Symbole (z. b. "H") sind nicht überlastet, da auf beiden Seiten ein wenig Leerraum vorhanden ist, um Sie von angrenzenden Symbolen zu trennen. Ein Beispiel für ein Symbol mit hinausragen ist das kursiv "f", das in diesem Thema zum Veranschaulichen der [ABC-Breite](#abc-width)verwendet wird. Sowohl der obere als auch der untere Teil der kursiv Formatierung "f" überschreiten die angrenzenden Symbole. Die Überschreibung entspricht der negativen Breite "a" oder "C".

## <a name="padding"></a>Auffüllung

Siehe [Unteres](#underhang).

## <a name="script"></a>script

Bei einem Skript handelt es sich um ein System von geschriebener Sprache, z. b. lateinische Skripts, Arabische Skripts und Chinesisch. Ein einzelnes Skript kann für eine oder mehrere menschliche Sprachen gelten. Das Skript hat keine besondere Beziehung zu einer Schriftart. Beispielsweise kann das lateinische Skript gleichermaßen gut gerendert werden, und zwar in der Schriftart New Roman oder Arial.

## <a name="underhang"></a>unter hängen

Der Unterraum ist eine Breite von Leerraum links oder rechts vom Solid-Teil eines Symbols. Underhing entspricht der positiven Breite "a" oder "C", wie für die [ABC-Breite](#abc-width)beschrieben. Unter hängen wird manchmal als "Padding" bezeichnet. In der folgenden Abbildung wird der unter Absturz für den Kleinbuchstaben n gezeigt.

![Abbildung, die den unter Absturz für den Kleinbuchstaben n anzeigt.](images/underhang.gif)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu uniscri](about-uniscribe.md)
</dt> </dl>

 

 
