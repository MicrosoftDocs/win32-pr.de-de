---
title: Begründung, Kerning und Abstand
description: Ab Windows 8 bietet DirectWrite eine Reihe von Features, mit denen Sie grundlegende Typografie-, Layout- und Abstandsfeatures steuern können, z. B. Zeichenabstand, Kerningpaare und Begründung.
ms.assetid: A5397132-0806-4842-8B82-E17925FBBBA9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fdd82e201429adb62e687021f003d7d5d6bedcd228c3102f448b04d1f079f71
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119632635"
---
# <a name="justification-kerning-and-spacing"></a>Begründung, Kerning und Abstand

Ab Windows 8 bietet [DirectWrite](direct-write-portal.md) eine Reihe von Features, mit denen Sie grundlegende Typografie-, Layout- und Abstandsfeatures steuern können, z. B. Zeichenabstand, Kopplung von Kerning und Begründung.

## <a name="character-spacing"></a>Zeichenabstand

Zeichenabstand, auch als "Nachverfolgung" bezeichnet, ist der Abstand zwischen Zeichen in einer Ausführung von Text.

Hier ist ein Beispiel für die Nachverfolgung. Die erste Zeile wendet keine Nachverfolgung auf den Text an. Die zweite Zeile erhöht den Zeichenabstand, und die dritte Zeile verringert den Zeichenabstand.

![drei Beispiele für denselben Text ohne Nachverfolgung, mehr Abstand und weniger Abstand.](images/spacing.png)

Ab Windows 8 [werden DirectWrite](direct-write-portal.md) Methoden hier eingefügt, um den Abstand von Zeichen in Ihrem Text zu steuern.

Wenn Sie das [DirectWrite-Layout](direct-write-portal.md) verwenden, können Sie für diesen Zweck die Methoden [**IDWriteTextLayout1::GetCharacterSpacing**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextlayout1-getcharacterspacing) und [**IDWriteTextLayout1::SetCharacterSpacing**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextlayout1-setcharacterspacing) verwenden.

Verwenden Sie die [**GetCharacterSpacing-Methode,**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextlayout1-getcharacterspacing) um den aktuellen Zeichenabstand zu bestimmen, und gibt das aktuelle Zeichen, den Abstand vor und nach dem Zeichen, die minimale Breite und eine [**DWRITE \_ TEXT \_ RANGE-Struktur**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) zurück, die Informationen zur Anfangsposition und Länge des verbleibenden Texts enthält.

Verwenden Sie [**setCharacterSpacing**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextlayout1-setcharacterspacing) auf einer [**DWriteTextLayout1-Schnittstelle,**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextlayout1) um ihren eigenen Zeichenabstand auf den Text im Layout anzuwenden. Die **SetCharacterSpacing-Methode** nimmt die Menge an Speicherplatz ein, die Sie vor und nach dem Zeichen wünschen, den minimal zulässigen Fortschritt und einen [**\_ DWRITE-TEXTBEREICH, \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) der den Bereich definiert, in dem der Abstand angewendet werden soll.

Wenn Sie ein benutzerdefiniertes Layout verwenden, [bietet DirectWrite](direct-write-portal.md) Unterstützung für das Festlegen des Zeichenabstands mit [**IDWriteTextAnalyzer1::ApplyCharacterSpacing**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-applycharacterspacing). Verwenden Sie diese Methode, wenn Sie ein benutzerdefiniertes Textlayout benötigen, um erweiterte Kontrolle über Das Layout zu erhalten. Mit dieser Methode können Sie **ApplyCharacterSpacing** mit dem führenden und dem folgenden Abstand, der minimalen Fortschrittsbreite, der Länge der Clusterzuordnung, der Anzahl von Glyphen, der Zuordnung von Zeichenbereichen zu Glyphen und der Vorbreite der einzelnen Glyphen bereitstellen, wenn Sie ein benutzerdefiniertes Layout verwenden. Die -Methode gibt die geänderten Glyphen-Fortschritte und eine [**DWRITE \_ GLYPH \_ OFFSET-Enumeration**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_offset) mit den neuen Offsets zum Ursprung der einzelnen Glyphen zurück.

## <a name="kerning"></a>Kerning

Kerning ist die kontextbezogene Abstandsanpassung zwischen Paaren oder Triplets von Buchstaben. Ein bestimmter Abstand zwischen Zeichensätzen kann die Lesbarkeit erhöhen und den Text besser aussehen lassen. Der wichtige Unterschied zwischen Kerning und Zeichenabstand besteht in der Tatsache, dass der Abstand von Buchstaben unabhängig vom Text ist, in dem sie leerzeichen, während Kerning in bestimmten Situationen zwischen bestimmten Zeichenpaaren verwendet wird, die in der Schriftart definiert sind.

Das Bild ist ein Beispiel für Kerning. Das Wort AVATAR in der oberen Zeile ist kerngestrichen, um das Wort natürlicher aussehen zu lassen. Wie Sie in den roten Feldern um die Zeichen sehen können, wird zwischen den ersten vier Buchstaben mehr Abstand angewendet, während R am Ende mehr Platz davor hat. Der ursprüngliche Text ohne Kerning befindet sich in der zweiten Zeile. Das Kerning in diesem Beispiel macht das Wort lesbarer und natürlicher.

![Ein Beispiel für das gleiche Wort mit und ohne angewendetes Kerning.](images/kerning.png)

Das Zeichen wird zwischen Zeichenpaaren, in denen die Kerne der Schriftart in der Kerntabelle gespeichert [sind,](direct-write-portal.md) und DirectWrite diese Tabelle analysiert und die Informationen über die Kerning-APIs an Sie zurückgibt.

Wenn Sie wissen möchten, ob eine Schriftart Paarkerning unterstützt, können Sie die [**IDWriteFontFace1::HasKerningPairs-Methode**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefontface1-haskerningpairs) verwenden. Diese Methode gibt den BOOL-Wert 1 zurück, wenn die Schriftart Kerningpaare unterstützt.

[**IdWriteFontFace1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1) verfügt auch über eine -Methode, mit der Sie Zugriff auf die Anpassungen des Kerningpaars für Glyphenindizes erhalten. [**Mit GetKerningPairAdjustments**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefontface1-getkerningpairadjustments) können Sie ein Array von Glyphenindizes eingeben, [und](direct-write-portal.md) DirectWrite ein Array von Glyphenvorrückanpassungen zurückgibt. Wenn eine Schriftart die Kerntabelle nicht unterstützt, gibt die Methode Nullen für die glyphenvoraufgesetzten Anpassungen zurück.

Wenn Sie das [DirectWrite-Layout](direct-write-portal.md) verwenden, gibt es zwei Methoden auf der [**IDWriteTextLayout1-Schnittstelle,**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextlayout1) mit denen Sie Das paarweisen Kerning festlegen und mehr über das Kerning von Paaren im Layout erfahren können. Die [**SetPairKerning-Methode**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextlayout1-setpairkerning) nimmt eine boolesche Darstellung davon an, ob Das Paarkerning aktiviert werden soll, und einen [**DWRITE \_ TEXT \_ RANGE,**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) der den Textbereich definiert, auf den es angewendet werden soll. Wenn Sie erfahren möchten, ob die Paarkerningfunktion für einen Textbereich aktiviert ist, können Sie die [**GetPairKerning-Methode**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextlayout1-getpairkerning) verwenden, die die aktuelle Position übernimmt und einen Bool zurückgibt, der entspricht, ob paarweises Kerning aktiviert ist, und den Textbereich, für den die Kerningeinstellung gilt.

## <a name="justification"></a>Begründung

Die Begründung ist der Prozess der Ausrichtung von Text, sodass er alle Leerzeichen innerhalb einer Spalte ausfüllt, indem die Fortschritte zwischen Zeichen oder Glyphenclustern erhöht oder Begründungszeichen hinzugefügt werden, um denselben Effekt zu erzielen. Im Allgemeinen wird dies erreicht, indem bestimmt wird, wo einer Textzeile Leerzeichen hinzugefügt werden müssen, und Abstandszeichen in diesen Breaking Opportunities eingefügt werden. Diese Abstandselemente können sich auch unterscheiden. In lateinischen Skripts wird Text durch eine Erhöhung der Vorbreiten zwischen Elementen gerechtfertigt, während text auf Arabisch mit einer Kashida gerechtfertigt wird. Im Folgenden finden Sie ein Beispiel für arabische und lateinische Skripts, die sowohl gerechtfertigt als auch nicht gerechtfertigt sind.

![Ein Beispiel für arabische und lateinische Skripts, die sowohl gerechtfertigt als auch nicht gerechtfertigt sind.](images/justification.png)

Ab Windows 8 [verfügt DirectWrite](direct-write-portal.md) über eine Reihe von Methoden, mit denen Sie Text in Ihren Apps rechtfertigen können.

Die [**DWRITE \_ TEXT \_ ALIGNMENT-Enumeration**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment) enthält einen zusätzlichen Wert. Sie können die [**SetTextAlignment-Methode**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment) verwenden und die **DWRITE \_ TEXT ALIGNMENT \_ \_ JUSTIFICATIOND-Konstante** übergeben [und DirectWrite](direct-write-portal.md) den Text rechtfertigen und das entsprechende Begründungszeichen für das Skript einfügen.

Wenn Sie ein benutzerdefiniertes Layout verwenden, stehen eine Reihe von Methoden zur Verfügung, damit Sie die Begründung nutzen können. [DirectWrite](direct-write-portal.md) verfügt über drei Methoden auf der [**IDWriteTextAnalyzer1-Schnittstelle,**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1) mit denen Sie einem benutzerdefinierten Layout eine Begründung hinzufügen können.

Die erste Methode ist [**GetJustificationOpportunities,**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-getjustificationopportunities)die den Text eingibt, den Sie rechtfertigen möchten, und gibt eine [**DWRITE \_ JUSTIFICATION \_ OPPORTUNITY-Struktur**](/windows/win32/api/Dwrite_1/ns-dwrite_1-dwrite_justification_opportunity) zurück, die angibt, wo Begründungszeichen hinzugefügt werden können, um den Text zu rechtfertigen.

Die zweite Funktion ist [**JustifyGlyphAdvances,**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-justifyglyphadvances)die ein Array von Glyphen-Fortschritten so gerechtfertigt, dass sie der Linienbreite passen. Diese Methode verwendet die [**DWRITE \_ JUSTIFICATION \_ OPPORTUNITY-Struktur,**](/windows/win32/api/Dwrite_1/ns-dwrite_1-dwrite_justification_opportunity) die [**GetJustificationOpportunities**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-getjustificationopportunities) generiert, die Glyphenvergrößerung und die Glyphenoffsets. Anschließend werden die gerechtfertigten Glyphenvorkungen und eine [**DWRITE \_ GLYPH \_ OFFSET-Enumeration**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_offset) generiert, die die gerechtfertigten Glyphenoffsets enthält.

Die dritte Funktion ist [**GetJustifiedGlyphs,**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-getjustifiedglyphs)die die neuen Glyphen für komplexe Skripts ausfüllt, bei denen die Begründung die Fortschritte bei Glyphen erhöht hat. **GetJustifiedGlyphs** muss nur aufgerufen werden, wenn das Skript über ein bestimmtes Begründungszeichen verfügt, wie von [**GetScriptProperties zurückgegeben.**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-getscriptproperties) Diese Methode übernimmt Informationen zur Schriftart, Länge des Texts, Emgröße der Glyphen, Skript des Texts, Anzahl von Glyphen, Clusterzuordnung, ursprünglichen Glyphenvor- und -offsets, gerechtfertigten Glyphenvor- und -offsets und Glypheneigenschaften. Die -Methode gibt die tatsächliche Anzahl von Glyphen, die aktualisierte Clusterzuordnung, aktualisierte Glyphenindizes mit eingefügten Begründungs-Glyphen, aktualisierte Glyphenoffsets und aktualisierte Glyphenvorrückungen zurück.

 

 