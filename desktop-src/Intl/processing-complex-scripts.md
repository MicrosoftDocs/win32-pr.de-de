---
description: Um eine Textgrundstellung anzugeben, kann eine Anwendung eine von zwei Methoden verwenden.
ms.assetid: 1190baed-5959-4f7a-8946-ac3b3da85821
title: Verarbeiten komplexer Skripts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 987c58cd1d6e8979573b47bbf3e2e7ff248617b12907f81ef70761c08403a067
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118390424"
---
# <a name="processing-complex-scripts"></a>Verarbeiten komplexer Skripts

Um eine Textgrundstellung anzugeben, kann eine Anwendung eine von zwei Methoden verwenden. Für eine einfache Implementierung der mehrsprachigen Begründung sollte die Anwendung [**ScriptJustify**](/windows/desktop/api/Usp10/nf-usp10-scriptjustify)aufrufen. Es generiert das Delta-Dxarray, indem kashida, dann Interwordabstand und dann Intercharacterabstand berücksichtigt werden. Zur komplexeren Begründung kann die Anwendung ein aktualisiertes Delta dx-Array mit eigenen Sprachkenntnissen und den informationen generieren, die von [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) im [**SCRIPT \_ DXTTR-Array**](/windows/win32/api/usp10/ns-usp10-script_visattr) abgerufen werden.

Der Begründungsbereich oder die Kashida sollte eingefügt werden, wenn sie durch den **uJustification-Member** von [**SCRIPT \_ CSVTTR**](/windows/win32/api/usp10/ns-usp10-script_visattr)identifiziert wird. Beim Ausführen einer Zeichenübergreifenden Begründung sollte die Anwendung zusätzlichen Platz nur nach Glyphen einfügen, die mit SCRIPT JUSTIFY CHARACTER markiert \_ \_ sind.

Die Anwendung führt die Platzierung von Caretzeichen und Treffertests mithilfe von [**ScriptXtoCP**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp) und [**ScriptCXaX durch.**](/windows/desktop/api/Usp10/nf-usp10-scriptcptox) Weitere Informationen finden Sie unter [Verwalten von Caretplatzierung und Treffertests.](managing-caret-placement-and-hit-testing.md)

Um Breiten auf schriftartunabhängige Weise abzurufen, ruft die Anwendung [**ScriptGetLogicalWidths auf.**](/windows/desktop/api/Usp10/nf-usp10-scriptgetlogicalwidths) Durch Übergeben der logischen Breite an [**ScriptApplyLogicalWidth**](/windows/desktop/api/Usp10/nf-usp10-scriptapplylogicalwidth)kann ein Textblock in den gleichen Grenzen mit akzeptablem Qualitätsverlust erneut angezeigt werden, auch wenn die ursprüngliche Schriftart nicht verfügbar ist. Es generiert ein Array von Glyphenbreiten ([Vorausbreiten](uniscribe-glossary.md)), das für die Übergabe an [**ScriptTextOut**](/windows/desktop/api/Usp10/nf-usp10-scripttextout)geeignet ist. Eine solche Aufzeichnung und erneute Anwendung von Informationen über die breite Breite auf schriftartunabhängige Weise kann in Situationen wie metafiles in einem von der Anwendung definierten Format nützlich sein.

> [!Note]  
> Metadateien unterstützen keine Glyphenindizes. Um in eine erweiterte Metadatei zu schreiben, sollte die Anwendung [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta) verwenden und die logischen Zeichen direkt schreiben. Mit diesem Mechanismus erfolgt die Generierung und Platzierung von Glyphen erst, wenn der Text wiedergegeben wird.

 

Die Anwendung sollte [**ScriptGetFontProperties**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontproperties)aufrufen, um die spezifischen Glyphen abzurufen, die für die Standard-, Leer- und Kashida-Eigenschaft usw. für die aktuelle Schriftart verwendet werden. Um zu bestimmen, welche Zeichen in einer Ausführung von der ausgewählten Schriftart unterstützt werden, ruft die Anwendung [**ScriptGetCMap**](/windows/desktop/api/Usp10/nf-usp10-scriptgetcmap)auf. Zeichen, die nicht verfügbar sind, weisen das Standardglyphen im Glyphenpuffer auf. Beachten Sie, dass diese Methode fehlschlägt, wenn eine Schriftart ein Zeichen mithilfe einer Kombination von Glyphen anstelle eines einzelnen Glyphen rendert. Beispiel: 00C9; LATIN CAPITAL LETTER E WITH LETTER kann mit einem großgeschriebenen E-Glyphen und einem schärferen Glyphen gerendert werden. Um die Schriftartunterstützung für eine Zeichenfolge zu bestimmen, die diese Arten von Codepunkten enthält, kann die Anwendung [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape)aufrufen. Weitere Informationen finden Sie unter [Verwenden von Strukturierungs-Engines.](using-shaping-engines.md)

Die [**ScriptCacheGetHeight-Funktion**](/windows/desktop/api/Usp10/nf-usp10-scriptcachegetheight) gibt die Höhe der Schriftart aus dem Schriftartcache zurück. [**ScriptGetProperties**](/windows/desktop/api/Usp10/nf-usp10-scriptgetproperties) enthält Informationen zur speziellen Verarbeitung, die für alle Skripts erforderlich ist, indiziert nach Skript. Beispielsweise enthält sie die primäre Sprache, die dem Skript zugeordnet ist, Daten, die angeben, ob das Skript numerisch ist, und Daten, die angeben, ob das Skript ein komplexes Skript ist.

[**ScriptGetGlyphABCWidth**](/windows/desktop/api/Usp10/nf-usp10-scriptgetglyphabcwidth) gibt die [ABC-Breite](uniscribe-glossary.md) eines bestimmten Glyphens zurück, was beim Zeichnen von Glyphendiagrammen nützlich sein kann. Sie sollte jedoch nicht für normale komplexe Skripttextformatierungen verwendet werden.

## <a name="related-topics"></a>Verwandte Themen

[Verwenden von Uniscribe](using-uniscribe.md)


 

 
