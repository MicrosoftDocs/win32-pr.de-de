---
title: Begründung, Kerning und Abstand
description: Ab Windows 8 bietet DirectWrite eine Reihe von Features, mit denen Sie die grundlegenden typografischen, Layout-und Abstands Features steuern können, wie z. b. Zeichenabstand, paar Kerning und Begründung.
ms.assetid: A5397132-0806-4842-8B82-E17925FBBBA9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17cc915922d0dbadb45bf47f223df83a25414daf
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729832"
---
# <a name="justification-kerning-and-spacing"></a>Begründung, Kerning und Abstand

Ab Windows 8 bietet [DirectWrite](direct-write-portal.md) eine Reihe von Features, mit denen Sie die grundlegenden typografischen, Layout-und Abstands Features steuern können, wie z. b. Zeichenabstand, paar Kerning und Begründung.

## <a name="character-spacing"></a>Zeichenabstand

Zeichen Abstände, auch als "Nachverfolgung" bezeichnet, sind der Abstand zwischen Zeichen in einer Textform.

Im folgenden finden Sie ein Beispiel für die Nachverfolgung. In der ersten Zeile wird keine Nachverfolgung auf den Text angewendet. Die zweite Zeile erhöht den Zeichenabstand, und die dritte Zeile verringert den Zeichenabstand.

![drei Beispiele für denselben Text ohne Nachverfolgung, mehr Abstand und weniger Abstände.](images/spacing.png)

Ab Windows 8 werden diese Methoden von [DirectWrite](direct-write-portal.md) hier hinzugefügt, um den Abstand der Zeichen im Text zu steuern.

Wenn Sie das [DirectWrite](direct-write-portal.md) -Layout verwenden, können Sie zu diesem Zweck die [**IDWriteTextLayout1:: getcharakterispacing**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextlayout1-getcharacterspacing) -Methode und die [**IDWriteTextLayout1:: setcharakterispacing**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextlayout1-setcharacterspacing) -Methode verwenden.

Verwenden Sie die [**getcharacter Spacing**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextlayout1-getcharacterspacing) -Methode, um den aktuellen Zeichenabstand zu bestimmen, und gibt das aktuelle Zeichen, den Abstand vor und nach dem Zeichen, die minimale erweiterte Breite und eine [**dwrite- \_ Text \_ Bereichs**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) Struktur zurück, die Informationen über die Anfangsposition und die Länge des verbleibenden Texts enthält.

Verwenden Sie [**setcharakterispacing**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextlayout1-setcharacterspacing) für eine [**DWriteTextLayout1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextlayout1) -Schnittstelle, um Ihren eigenen Zeichenabstand auf den Text im Layout anzuwenden. Die **setcharacter Spacing** -Methode nimmt den gewünschten Speicherplatz vor und nach dem-Zeichen, den minimal zulässigen Minimalwert und einen [**dwrite- \_ Text \_ Bereich**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) , der den Bereich definiert, der den Abstand anwendet.

Wenn Sie ein benutzerdefiniertes Layout verwenden, unterstützt [DirectWrite](direct-write-portal.md) das Festlegen des Zeichen Abstands mit [**IDWriteTextAnalyzer1:: applycharacters Spacing**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-applycharacterspacing). Verwenden Sie diese Methode, wenn Sie ein benutzerdefiniertes Text Layout benötigen, um die erweiterte Kontrolle über das Layout zu haben. Diese Methode ermöglicht es Ihnen, **applycharakterispacing** mit dem führenden und nachfolgenden Abstand, der minimalen Vorlauf Breite, der Länge der Cluster Zuordnung, der Anzahl von Symbolen, der Zuordnung von Zeichen Bereichen zu Glyphen und der Vordergrund Breite jedes Symbols anzugeben, wenn Sie ein benutzerdefiniertes Layout verwenden. Die-Methode gibt die geänderten Symbol Fortschritte und eine [**dwrite- \_ Glyphe- \_ Offset**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_offset) -Enumeration mit den neuen Offsets an den Ursprung jedes Symbols zurück.

## <a name="kerning"></a>Unterschneidungen

Bei der kernung handelt es sich um die Anpassung des kontextbezogenen Abstands zwischen Paaren oder wenigen Buchstaben. Der bestimmte Abstand zwischen Zeichensätzen kann die Lesbarkeit erhöhen und das Aussehen von Text verbessern. Der entscheidende Unterschied zwischen dem Zwischenspeicher und dem Zeichenabstand ist die Tatsache, dass der Buchstabe für den Text des Texts agnostisch ist, während die kerung in bestimmten Situationen zwischen bestimmten Zeichen Paaren, wie in der Schriftart definiert, verwendet wird.

Das Image ist ein Beispiel für die Kerning. Das Wort "Avatar" in der obersten Zeile ist kerned, damit das Wort natürlicher aussieht. Wie Sie in den roten Feldern um die Zeichen sehen können, wird zwischen den ersten vier Buchstaben mehr Abstand angewendet, während R am Ende mehr Platz aufweist. Der ursprüngliche Text ohne Unterschneidungen befindet sich in der zweiten Zeile. Durch die Unterschneidungen in diesem Beispiel wird das Wort besser lesbar und natürlicher.

![ein Beispiel für dasselbe Wort mit und ohne angewendetes keror.](images/kerning.png)

Das Zeichen wechselt zwischen Zeichen Paaren, die in der Tabelle "Kerns" in der Tabelle "Kerns" gespeichert werden, und [DirectWrite](direct-write-portal.md) analysiert diese Tabelle und gibt die Informationen über die kernungs-APIs an Sie zurück.

Wenn Sie wissen möchten, ob eine Schriftart paar Kerten unterstützt, können Sie die [**IDWriteFontFace1:: haskerningpaars**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefontface1-haskerningpairs) -Methode verwenden. Diese Methode gibt den booleschen Wert 1 zurück, wenn die Schriftart das Senden von Paaren unterstützt.

Der [**IDWriteFontFace1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1) verfügt auch über eine-Methode, die es Ihnen ermöglicht, Zugriff auf die Einstellungen für das Unterschneidungen-Paar für Glyphe-Indizes zu erhalten. [**Getkerningpiradjustments**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefontface1-getkerningpairadjustments) ermöglicht die Eingabe eines Arrays von Glyphe-Indizes, und [DirectWrite](direct-write-portal.md) gibt ein Array von vorab Anpassungen der Glyphe zurück. Wenn eine Schriftart die Tabelle "Kerns" nicht unterstützt, gibt die Methode Nullen für die vorab Anpassungen der Glyphe zurück.

Wenn Sie das [DirectWrite](direct-write-portal.md) -Layout verwenden, gibt es zwei Methoden an der [**IDWriteTextLayout1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextlayout1) -Schnittstelle, die es Ihnen ermöglichen, die paar-Unterschneidungen-Vorgänge festzulegen und mehr über das Kernen von Paaren im Layout zu erfahren. Die [**setpairren**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextlayout1-setpairkerning) -Methode übernimmt eine boolesche Darstellung, unabhängig davon, ob das keror-paar aktiviert werden soll, und ein [**dwrite- \_ Text \_ Bereich**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) , der den Textbereich definiert, auf den Sie angewendet werden soll. Wenn Sie erfahren möchten, ob für einen Textbereich paar-kertevorgänge aktiviert sind, können Sie die [**getpairren**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextlayout1-getpairkerning) -Methode verwenden, die die aktuelle Position annimmt und einen booleschen Wert zurückgibt, der entspricht, ob die paar-Unterschneidungen aktiviert ist, und den Textbereich, auf den die Einstellung für die Einstellung angewendet wird.

## <a name="justification"></a>Begründung

Die Begründung ist der Prozess der Ausrichtung von Text, sodass er den gesamten Raum innerhalb einer Spalte durch Erhöhen der Fortschritte zwischen Zeichen oder Symbol Clustern oder durch Hinzufügen von rechtfertigen Zeichen zum Erreichen desselben Effekts füllt. Im Allgemeinen wird dies erreicht, indem festgelegt wird, wo einer Textzeile Platz hinzugefügt werden muss, und in diese wichtigen Verkaufschancen eingefügt werden müssen. Diese Abstands Elemente können sich auch unterscheiden, und in lateinischen Skripts wird Text durch Erhöhen der Fortschritts Breite zwischen Elementen, während der Text auf Arabisch mit einem Kashida-Element bündig ausgerichtet wird. Hier ist ein Beispiel für das arabische und das lateinische Skript, das sowohl gerechtfertigt als auch nicht gerechtfertigt ist.

![ein Beispiel für das arabische und das lateinische Skript, das sowohl gerechtfertigt als auch nicht gerechtfertigt ist.](images/justification.png)

Ab Windows 8 verfügt [DirectWrite](direct-write-portal.md) über eine Reihe von Methoden, mit denen Sie Text in ihren apps rechtfertigen können.

Es gibt einen zusätzlichen Wert in der Enumeration der [**dwrite- \_ Text \_ Ausrichtung**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment) . Sie können die [**SetTextAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment) -Methode verwenden und die Ausrichtung auf die **Ausrichtung der dwrite- \_ Text \_ Ausrichtung \_** übergeben. [DirectWrite](direct-write-portal.md) rechtfertigt den Text und fügt das entsprechende Anweisungs Zeichen für das Skript ein.

Wenn Sie ein benutzerdefiniertes Layout verwenden, stehen eine Reihe von Methoden zur Verfügung, sodass Sie die Begründung nutzen können. [DirectWrite](direct-write-portal.md) verfügt über drei Methoden in der [**IDWriteTextAnalyzer1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1) -Schnittstelle, die Sie verwenden können, um einem benutzerdefinierten Layout eine Begründung hinzuzufügen.

Die erste Methode ist " [**getrecht cationopportunities**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-getjustificationopportunities)", die den Text annimmt, den Sie rechtfertigen möchten, und eine [**dwrite- \_ begrün dungs \_**](/windows/win32/api/Dwrite_1/ns-dwrite_1-dwrite_justification_opportunity) Struktur zurückgibt, die beschreibt, wo dem Text rechtfertigen Zeichen hinzugefügt werden können.

Die zweite Funktion ist " [**justifyglyphadvances**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-justifyglyphadvances)", die ein Array von Symbol Vorschritten rechtfertigt, sodass Sie an die Linienbreite angepasst werden. Diese Methode nimmt die von [**getrecht cationopportunity**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-getjustificationopportunities) generierte opportunitätenstruktur der [**dwrite- \_ Begründung \_**](/windows/win32/api/Dwrite_1/ns-dwrite_1-dwrite_justification_opportunity) , das Symbol erweitert und das Symbol Offsets an. Anschließend werden die fertigen Symbol Fortschritte und eine [**dwrite- \_ Glyphe- \_ Offset**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_offset) -Enumeration generiert, die die kompensierten Glyphe-Offsets enthält.

Die dritte Funktion ist " [**getrechtedglyphs**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-getjustifiedglyphs)", die die neuen Symbole für komplexe Skripts füllt, wobei die Ausrichtung den Fortschritt für Symbole erhöht. **Getcompliedglyphs** muss nur aufgerufen werden, wenn das Skript über ein bestimmtes, von [**getscriptproperties**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-getscriptproperties)zurück gegebenes rechtzeitiges Zeichen verfügt. Bei dieser Methode werden Informationen über die Schriftart, die Länge des Texts, die EM-Größe der Glyphen, das Skript des Texts, die Anzahl der Symbole, die Cluster Zuordnung, das ursprüngliche Symbol für das durchsetzen/Offsets, das Symbol für erweiterte Symbole/Offsets und die Symbol Eigenschaften berücksichtigt. Die-Methode gibt die tatsächliche Glyphe, die aktualisierte Cluster Zuordnung, aktualisierte Glyphe-Indizes mit eingefügten Symbol Erstellungs Symbolen, aktualisierte Symbol Offsets und aktualisierte Symbol Fortschritte zurück.

 

 