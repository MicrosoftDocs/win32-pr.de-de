---
description: Sie können benutzerdefinierte Eingabe Bereiche definieren und zuweisen, indem Sie die Handschrift Syntax für reguläre Ausdrücke verwenden, die von einigen der Handschrift Erkennungsformen von Microsoft interpretiert wird.
ms.assetid: e3afe735-eca8-4fda-bd5b-cc0ab0b6a872
title: Syntax Referenz für reguläre Ausdrücke
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23c0de50ff37795032719d9bc90ee81891324ba9
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "104218933"
---
# <a name="regular-expression-syntax-reference"></a>Syntax Referenz für reguläre Ausdrücke

Sie können benutzerdefinierte Eingabe Bereiche definieren und zuweisen, indem Sie die Handschrift Syntax für reguläre Ausdrücke verwenden, die von einigen der Handschrift Erkennungsformen von Microsoft interpretiert wird. Die Syntax ist eine Teilmenge der [sprach Implementierung für reguläre Ausdrücke](/documentation/?url=%2flibrary%2fcpgenref%2fhtml%2fcpconRegularExpressionsLanguageElements.asp%3fframe%3dtrue) in der .NET Framework.

Es gibt einige Unterschiede bei der Verwendung von Handschrift regulären Ausdrücken und der Art und Weise, wie die anderen Typen von regulären Ausdrücken verwendet werden. Die Handschrift Syntax wird verwendet, um eine exakte Zeichenfolge anzugeben, die mit der Erkennungs-Engine und nicht mit einer Teil Zeichenfolge abgeglichen wird. Beispielsweise würde der reguläre Ausdruck s ( \[ a-z \] +) p Übereinstimmungen für "Suppe", "Ende", "inStep" und "esophagus" zurückgeben. Ein entsprechender Handschrift regulärer Ausdruck, wie z. b. s (! is \_ OneChar) + p, würde z. b. "Suppe" und "beenden", aber nicht "inStep" und "esophagus" entsprechen.

Reguläre Ausdrücke von Handschrift unterstützen keine nicht unterbrechende Leerzeichen in regulären Ausdrücken. Das heißt, Sie können die Entität "nbsp" nicht innerhalb eines regulären Handschrift Ausdrucks verwenden.

In den folgenden Abschnitten wird die Syntax ausführlicher beschrieben.

## <a name="valid-operators"></a>Gültige Operatoren

Die folgenden Operatoren sind für das Erstellen regulärer Ausdrücke zum Definieren von Eingabe Bereichen für Handschrift Erkennungsformen gültig.



| Operator      | BESCHREIBUNG                                                                           |
|---------------|---------------------------------------------------------------------------------------|
| \*<br/> | Der unäre Postfix-Operator, der 0 (null) oder mehr Vorkommen des Operanden bezeichnet.<br/> |
| +<br/>  | Der unäre Postfix-Operator, der ein oder mehrere Vorkommen des Operanden bezeichnet.<br/>  |
| ?<br/>  | Der unäre Postfix-Operator gibt NULL oder ein Vorkommen des Operanden an.<br/>   |
| \|<br/> | Binärer Infix-Operator, der "or" bedeutet.<br/>                                        |
| ()<br/> | Wird zum Gruppieren von Elementen verwendet.<br/>                                                       |



 

Die Microsoft-Implementierung von regulären Ausdrücken für Handschrift Erkennungs Tools ermöglicht wiederholte Anwendungen von Postfix-unären Operatoren. Beispiel: a \* \* = (a \* ) \* = a \* , b? = (b?)? = b? Sie können auch nicht aufeinander folgende Wiederholungen zulassen, z. b \* .: a? \* = ((a \* )?) \* = (a \* ) \* = a \* . Dies unterscheidet sich von .NET Framework regulären Ausdrücken, die nur das zulassen? Operator, der wiederholt werden soll.

Ein weiterer Unterschied von .NET Framework regulären Ausdrücken ist, dass reguläre Handschrift Ausdrücke keinen leeren Ausdruck unterstützen, der mit einem leeren paar Klammern () gekennzeichnet ist.

> [!Note]  
> Für reguläre Handschrift Ausdrücke werden nur Zeichen in der 1252-Codepage unterstützt.

 

## <a name="using-input-scopes"></a>Verwenden von Eingabe Bereichen

Sie können auch den Satz regulärer Eingabe Bereiche verwenden, die als Teil der [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) -Funktion in ihren regulären Ausdrücken definiert sind. Der Wert für month (numerisch) lautet z. b \_ . "Date \_ Month". Die Syntax zum Angeben eines Eingabe Bereichs als Teil eines regulären Ausdrucks besteht darin, dem Enumerationswert des Eingabe Bereichs eine öffnende Klammer und ein Ausrufezeichen (! und eine schließende Klammer) am Ende vorangestellt werden. Beispiel:

(! Ist \_ Datum/ \_ Monat)

Wenn Sie den \_ Standardeingabe Bereich der-Klasse mit einem beliebigen anderen Eingabebereich kombinieren, besteht der Effekt darin, dass die Erkennung entweder jeden einzelnen Ausdruck, der vom Standard Sprachmodell unterstützt wird (z. b. ein Wort aus dem System Wörterbuch oder einem Datum), mit oder ohne Interpunktions Zeichen oder einen beliebigen Wert zurückgeben kann, der dem restlichen regulären Ausdruck entspricht.

> [!Note]  
> Die folgenden [**Member von "**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) " in regulären Ausdrücken werden nicht unterstützt: ist " \_ PhraseList", " \_ RegularExpression", " \_ SRGS", "XML" \_ .

 

## <a name="unsupported-operators"></a>Nicht unterstützte Operatoren

Die folgenden Operatoren für reguläre Ausdrücke werden beim Erstellen von regulären Handschrift Ausdrücken nicht unterstützt.



| Operator                                     | BESCHREIBUNG                                                         |
|----------------------------------------------|---------------------------------------------------------------------|
| .<br/>                                 | Zeit Zeichen.<br/>                                        |
| \[\]<br/>                              | Eckige Klammern. Klammer für das Gruppieren von Elementen verwenden.<br/>     |
| {}<br/>                                | Geschweifte Klammern.<br/>                                          |
| (?\# Kommentar) und \# \[ Kommentar\]<br/> | Kommentare.<br/>                                                |
| $<br/>                                 | Dollar Zeichen.<br/>                                   |
| ^<br/>                                 | Caretzeichen.<br/>                                         |
| -<br/>                                 | Bindestrich. Muss oder ( \| ) alle Sätze von Elementen kombinieren.<br/> |



 

## <a name="escaping-characters"></a>Umwandeln von Zeichen mit Escapezeichen

Gewöhnliche Zeichen, die nicht die in der folgenden Tabelle aufgeführten sind, stimmen mit sich selbst. Das heißt, ein "a" in einem regulären Ausdruck gibt an, dass die Eingabe einem "a" entsprechen soll.

Ein weiterer bedeutender Unterschied beim Schreiben regulärer Ausdrücke ist, dass Sie nur eine begrenzte Anzahl von Zeichen in einem regulären Ausdruck mit Escapezeichen versehen können. In der folgenden Tabelle werden die zulässigen Zeichen, die mit Escapezeichen versehen werden können, beschrieben. Jeder andere Versuch, ein Zeichen mit Escapezeichen zu versehen, führt zu einem Fehler, der von der Erkennung ausgelöst wird.



| Zeichen       |
|-----------------|
| \\\*<br/> |
| \\+<br/>  |
| \\?<br/>  |
| \\(<br/>  |
| \\)<br/>  |
| \\\|<br/> |
| \\\\<br/> |
| \\!<br/>  |
| \\.<br/>  |
| \\\[<br/> |
| \\\]<br/> |
| \\^<br/>  |
| \\{<br/>  |
| \\}<br/>  |
| \\$<br/>  |
| \\\#<br/> |



 

 

 