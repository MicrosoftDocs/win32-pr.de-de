---
description: Eine Anwendung kann eine von zwei Methoden verwenden, um die Textausrichtung bereitzustellen.
ms.assetid: 1190baed-5959-4f7a-8946-ac3b3da85821
title: Verarbeiten komplexer Skripts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87bea5b75e87afc4177b03c03f4263ba2592a0e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041691"
---
# <a name="processing-complex-scripts"></a>Verarbeiten komplexer Skripts

Eine Anwendung kann eine von zwei Methoden verwenden, um die Textausrichtung bereitzustellen. Für eine einfache Implementierung der mehrsprachigen Begründung sollte die Anwendung [**scriptrecht**](/windows/desktop/api/Usp10/nf-usp10-scriptjustify)nennen. Er generiert das Delta-DX-Array, indem er Kashida, den Abstand zwischen den Wort interwörtern und den intercharacter-Abstand berücksichtigt. Für eine anspruchsvollere Begründung kann die Anwendung ein aktualisiertes Delta-DX-Array generieren, das das eigene Sprachwissen und die von [**scriptshape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) abgerufenen Informationen im [**Skript " \_ visattr**](/windows/win32/api/usp10/ns-usp10-script_visattr) "-Array verwendet.

Es sollte ein Ausrichtungstyp oder ein Kashida eingefügt werden, wenn er vom Benutzer **definierten Member von** [**Skript " \_ visattr**](/windows/win32/api/usp10/ns-usp10-script_visattr)" identifiziert wird Bei der Durchführung der Zeichen übergreifenden Ausrichtung sollte die Anwendung zusätzlichen Leerraum erst einfügen, nachdem Symbole mit dem Zeichen "Skript rechtfertigen" gekennzeichnet wurden \_ \_ .

Die Anwendung führt die Platzierung von Caretzeichen und Treffer Tests mithilfe von [**scriptxeincp**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp) und [**scriptcptox**](/windows/desktop/api/Usp10/nf-usp10-scriptcptox)durch. Weitere Informationen finden Sie unter [Verwalten der Platzierung von Caretzeichen und Treffer Tests](managing-caret-placement-and-hit-testing.md).

Um breiten auf Schriftart unabhängige Weise zu erhalten, ruft die Anwendung [**scriptgetlogicalbreiten**](/windows/desktop/api/Usp10/nf-usp10-scriptgetlogicalwidths)auf. Durch die Übergabe der logischen Breite an [**scriptapplylogicalwidth**](/windows/desktop/api/Usp10/nf-usp10-scriptapplylogicalwidth)kann ein TextBlock in denselben Grenzen mit akzepziellem Verlust der Qualität erneut angezeigt werden, auch wenn die ursprüngliche Schriftart nicht verfügbar ist. Es generiert ein Array von Symbol breiten ([voraus Breite](uniscribe-glossary.md)), die für die Übergabe an [**scripttextout**](/windows/desktop/api/Usp10/nf-usp10-scripttextout)geeignet sind. Das Aufzeichnen und erneute Anwenden von Informationen zur vorab Breite auf Schriftart unabhängige Weise kann in Situationen nützlich sein, in denen ein Anwendungs definiertes Format vorliegt.

> [!Note]  
> Metadateien unterstützen keine Glyphe-Indizes. Zum Schreiben in eine erweiterte Metadatei sollte die Anwendung [**exttextout**](/windows/win32/api/wingdi/nf-wingdi-exttextouta) verwenden und die logischen Zeichen direkt schreiben. Mithilfe dieses Mechanismus werden das Generieren und Platzieren von Symbolen erst nach dem Wiedergeben des Texts angezeigt.

 

Zum Abrufen der spezifischen Symbole, die für die Standard-, Leerzeichen, Kashida usw. für die aktuelle Schriftart verwendet werden, sollte die Anwendung [**scriptgetfontproperties**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontproperties)aufrufen. Wenn Sie bestimmen möchten, welche Zeichen in einer Testlauf von der ausgewählten Schriftart unterstützt werden, ruft die Anwendung [**scriptgetcmap**](/windows/desktop/api/Usp10/nf-usp10-scriptgetcmap)auf. Zeichen, die nicht verfügbar sind, haben das Standard Symbol im Symbol Puffer. Beachten Sie, dass diese Methode fehlschlägt, wenn eine Schriftart ein Zeichen mit einer Kombination von Symbolen anstelle eines einzelnen Symbols rendert. Beispielsweise 00c9; Der lateinische Großbuchstabe E mit dem akuten kann mithilfe eines Großbuchstaben und eines akuten Symbols gerendert werden. Zum Ermitteln der Schriftart Unterstützung für eine Zeichenfolge, die diese Arten von Code Punkten enthält, kann die Anwendung [**scriptshape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape)aufruft. Weitere Informationen finden Sie unter [verwenden](using-shaping-engines.md)von Strukturierungs Modulen.

Die [**scriptcachegetheight**](/windows/desktop/api/Usp10/nf-usp10-scriptcachegetheight) -Funktion gibt die Höhe der Schriftart aus dem Schriftart Cache zurück. [**Scriptgetproperties**](/windows/desktop/api/Usp10/nf-usp10-scriptgetproperties) enthält Informationen zur speziellen Verarbeitung, die für alle Skripts erforderlich ist, die durch das Skript indiziert werden. Sie enthält beispielsweise die dem Skript zugeordnete primäre Sprache, Daten, die angeben, ob das Skript numerisch ist, und Daten, die angeben, ob das Skript ein komplexes Skript ist.

[**Scriptgetglyphabcwidth**](/windows/desktop/api/Usp10/nf-usp10-scriptgetglyphabcwidth) gibt die [ABC-Breite](uniscribe-glossary.md) eines bestimmten Symbols zurück, was für das Zeichnen von Symbol Diagrammen nützlich sein kann. Es sollte jedoch nicht für die normale Formatierung komplexer Skript Text verwendet werden.

## <a name="related-topics"></a>Verwandte Themen

[Verwenden von uniscri](using-uniscribe.md)


 

 
