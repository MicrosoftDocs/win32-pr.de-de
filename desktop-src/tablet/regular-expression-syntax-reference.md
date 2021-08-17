---
description: Sie können benutzerdefinierte Eingabebereich definieren und zuweisen, indem Sie die Handschriftsyntax für reguläre Ausdrücke verwenden, die von einigen der Microsoft-Handschrifterkennungen verstanden wird.
ms.assetid: e3afe735-eca8-4fda-bd5b-cc0ab0b6a872
title: Referenz zur Syntax regulärer Ausdrücke
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33f09bbf81f86e3609f745358f0b18e35cf3f4712f3b1770fb3eb9c8becebc99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118715530"
---
# <a name="regular-expression-syntax-reference"></a>Referenz zur Syntax regulärer Ausdrücke

Sie können benutzerdefinierte Eingabebereich definieren und zuweisen, indem Sie die Handschriftsyntax für reguläre Ausdrücke verwenden, die von einigen der Microsoft-Handschrifterkennungen verstanden wird. Die Syntax ist eine Teilmenge der [Sprachimplementierung](/documentation/?url=%2flibrary%2fcpgenref%2fhtml%2fcpconRegularExpressionsLanguageElements.asp%3fframe%3dtrue) für reguläre Ausdrücke im .NET Framework.

Es gibt einige Unterschiede in der Art und Weise, wie das Handschriften von regulären Ausdrücken verwendet wird, und der Art und Weise, wie die anderen Typen von regulären Ausdrücken verwendet werden. Die Handschriftsyntax wird verwendet, um eine genaue Zeichenfolge anzugeben, die von der Erkennungs-Engine und nicht als Unterzeichenfolge übereinstimmen wird. Beispielsweise würde der reguläre Ausdruck s( a-z +)p Übereinstimmungen für \[ \] "darstellung", "stop", "instep" und "esoungus" zurückgeben. Ein äquivalenter regulärer Handschriftausdruck wie s(!IS \_ ONECHAR)+p würde dagegen mit "darstellung" und "stop" übereinstimmen, aber nicht mit "instep" und "esochous".

Das Handschriften regulärer Ausdrücke unterstützt keine Leerzeichen in regulären Ausdrücken. Das heißt, Sie können die Entität "nbsp" nicht in einem handschriftlichen regulären Ausdruck verwenden.

In den folgenden Abschnitten wird die Syntax ausführlicher beschrieben.

## <a name="valid-operators"></a>Gültige Operatoren

Die folgenden Operatoren sind zum Erstellen regulärer Ausdrücke gültig, um Eingabebereich für Handschrifterkennungen zu definieren.



| Operator      | Beschreibung                                                                           |
|---------------|---------------------------------------------------------------------------------------|
| \*<br/> | Unärer Postfixoperator, der null oder mehr Vorkommen des Operanden ankn.)<br/> |
| +<br/>  | Ein unärer Postfixoperator, der ein oder mehrere Vorkommen des Operanden bezeichnet.<br/>  |
| ?<br/>  | Ein unärer Postfixoperator, der null oder ein Vorkommen des Operanden andezifizieren kann.<br/>   |
| \|<br/> | Binärer Infixoperator, der "or" bedeutet.<br/>                                        |
| ()<br/> | Wird zum Gruppen von Elementen verwendet.<br/>                                                       |



 

Die Microsoft-Implementierung regulärer Ausdrücke für Handschrifterkennungen ermöglicht wiederholte Anwendungen unärer Postfixoperatoren. Beispiel: a \* \* = (a \* ) = a , \* \* b?? = (b?)? = b?. Sie ermöglichen auch nicht aufeinander folgende Wiederholungen, z.B.: a \* ? \* = ((a \* )?) \* = (a ) = a \* \* \* . Dies ist anders als .NET Framework Regulären Ausdrücken, die nur zulassen? -Operator, der wiederholt werden soll.

Ein weiterer Unterschied .NET Framework regulären Ausdrücken ist, dass das Handschriften regulärer Ausdrücke keinen leeren Ausdruck unterstützt, der mit einem leeren Paar von Klammern () gekennzeichnet ist.

> [!Note]  
> Nur Zeichen in der Codepage 1252 werden für das Handschriften regulärer Ausdrücke unterstützt.

 

## <a name="using-input-scopes"></a>Verwenden von Eingabebereich

Sie können auch den Satz regulärer Eingabebereich verwenden, die als Teil der [**SetInputScope-Funktion**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) in Ihren regulären Ausdrücken definiert sind. Der Wert für Month (numerisch) ist beispielsweise IS \_ DATE \_ MONTH. Die Syntax zum Angeben eines Eingabebereichs als Teil eines regulären Ausdrucks besteht im Vorziehen des aufzählten Werts des Eingabebereichs mit einer offenen Klammer und einem Ausrufezeichen (!), und platzieren Sie am Ende eine schließende Klammer. Beispiel:

(!IS \_ DATE \_ MONTH)

Wenn Sie den IS DEFAULT-Eingabebereich kombinieren, indem Sie ihn mit einem anderen Eingabebereich verknüpfen, hat dies den Effekt, dass die Erkannten entweder einen beliebigen einzelnen Ausdruck zurückgeben können, den das Standardsprachmodell unterstützt (z. B. ein Wort aus dem Systemwörterbuch oder ein Datum) mit oder ohne Interpunktion oder einen beliebigen Wert, der dem Rest des regulären Ausdrucks entspricht, der an die Erkennende übergeben \_ wird.

> [!Note]  
> Die folgenden Elemente von [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) werden in regulären Ausdrücken nicht unterstützt: IS \_ PHRASELIST, IS \_ REGULAREXPRESSION, IS \_ SRGS, IS \_ XML.

 

## <a name="unsupported-operators"></a>Nicht unterstützte Operatoren

Die folgenden Operatoren für reguläre Ausdrücke werden beim Erstellen von handschriftlichen regulären Ausdrücken nicht unterstützt.



| Operator                                     | Beschreibung                                                         |
|----------------------------------------------|---------------------------------------------------------------------|
| .<br/>                                 | Periodenzeichen.<br/>                                        |
| \[\]<br/>                              | Eckige Klammern. Verwenden Sie Klammern zum Gruppieren von Elementen.<br/>     |
| {}<br/>                                | Eckige Klammern.<br/>                                          |
| (?\# kommentar) und \# \[ comment\]<br/> | Kommentare.<br/>                                                |
| $<br/>                                 | Dollarzeichen.<br/>                                   |
| ^<br/>                                 | Caretzeichen.<br/>                                         |
| -<br/>                                 | Bindestrich. Muss OR ( \| ) alle Sätze von Elementen zusammen haben.<br/> |



 

## <a name="escaping-characters"></a>Umwandeln von Zeichen mit Escapezeichen

Normale Zeichen, die nicht in der folgenden Tabelle enthalten sind, passen sich selbst an. Das bedeutet, dass ein "a" in einem regulären Ausdruck angibt, dass die Eingabe mit einem "a" übereinstimmen soll.

Ein weiterer signifikanter Unterschied beim Schreiben von handschriftlichen regulären Ausdrücken ist, dass Sie nur einen begrenzten Satz von Zeichen innerhalb eines regulären Ausdrucks mit Escapezeichen vermausen können. In der folgenden Tabelle werden die zulässigen Zeichen beschrieben, die mit Escapezeichen dargestellt werden können. Jeder andere Versuch, ein Zeichen mit Escapezeichen zu escapen, führt dazu, dass ein Fehler von der -Erkannten ausgelöst wird.



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



 

 

 