---
description: Nachrichten werden in einer Nachrichtentextdatei definiert. Der Nachrichtencompiler weist jeder Nachricht Zahlen zu und generiert eine C/C++-Includedatei, mit der die Anwendung mithilfe einer symbolischen Konstante auf eine Nachricht zugreifen kann.
ms.assetid: 99fbb3d6-6fde-4162-b0b9-99a1cdf0b8f8
title: Meldungstextdateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 818210cfe58fb8eafe939c70a2a57b358e306bb9bc072a64abebbec5ca41c266
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118151476"
---
# <a name="message-text-files"></a>Meldungstextdateien

Nachrichten werden in einer Nachrichtentextdatei definiert. Der Nachrichtencompiler weist jeder Nachricht Zahlen zu und generiert eine C/C++-Includedatei, mit der die Anwendung mithilfe einer symbolischen Konstante auf eine Nachricht zugreifen kann.

Die allgemeine Syntax für Anweisungen in einer Meldungstextdatei lautet wie folgt:

*Schlüsselwort* = *wert*

Leerzeichen um das Gleichheitszeichen werden ignoriert, und der Wert wird durch Leerzeichen (einschließlich Zeilenumbrüchen) vom nächsten Schlüsselwort-Wert-Paar getrennt. Der Fall wird beim Vergleich mit Schlüsselwortnamen ignoriert. Der *Wertteil* kann eine numerische ganzzahlige Konstante mit C/C++-Syntax, ein Symbolname, der den Regeln für C/C++-Bezeichner folgt, oder ein Dateiname mit maximal 8 Zeichen ohne Punkt sein.

Eine Beispielmeldungsdatei finden Sie unter [Beispielnachrichten-Textdatei.](sample-message-text-file.md)

## <a name="comments"></a>Kommentare

Kommentarzeilen sind in der Meldungstextdatei zulässig. Ein Semikolon (;) beginnt einen Kommentar, der am Ende der Zeile endet. Folgen Sie dem Semikolon mit einem einzeiligen C/C++-Kommentarindikator (/),damit die vom Nachrichtencompiler generierte Headerdatei in Ihrer Anwendung kompiliert wird.

``` syntax
;// This is a single-line comment.
```

Beginnen Sie bei einem Blockkommentar jede Zeile mit einem Semikolon, und platzieren Sie dann einen C/C++-Indikator für offene \* Blockkommentare (/) nach dem Semikolon in der ersten Zeile und den Schließen-Blockkommentarindikator ( \* /) nach dem Semikolon in der letzten Zeile.

``` syntax
;/* This is a block comment.
;   It spans multiple lines.
;*/
```

## <a name="header-section"></a>Headerabschnitt

Die Meldungstextdatei enthält einen Header, der Namen und Sprachbezeichner für die Verwendung durch die Nachrichtendefinitionen im Text der Datei definiert. Der Header enthält 0 (null) oder mehr der folgenden Anweisungen.



| Anweisungssyntax                           | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MessageIdTypedef=*type*                    | Typ, der in der Nachrichtendefinition wie folgt verwendet werden soll: \# define *name* ((*typ*)0x *nnnnnnnn )*<br/> Der Typ muss groß genug sein, um den gesamten Nachrichtencode aufnehmen zu können, z. B. ein **DWORD-**. Der Typ kann auch ein typ sein, der im Quellcode der Anwendung definiert ist. Der Standardwert für *type* ist leer, sodass keine Typcasting verwendet wird. <br/> Diese Anweisung kann im -Header und so oft wie nötig im Nachrichtendefinitionsabschnitt angegeben werden.<br/>                                                                                                                  |
| SeverityNames=(*name* = *number* \[ :*name* \] ) | Eine Gruppe von Namen, die für den Schweregrad in einer Nachrichtendefinition zulässig sind. Jedem Schweregradnamen ist eine Zahl zugeordnet, die, wenn sie um 30 Bits nach links verschoben wird, das Bitmuster für logical-OR mit der Einrichtung und den Nachrichten-ID-Werten zum Bilden des Nachrichtencodes angibt. Jeder Schweregradwert, der nicht in 2 Bits passt, ist ein Fehler. Die Schweregradcodes können ebenfalls symbolische Namen erhalten. Der Standardwert ist wie folgt definiert: SeverityNames=( Success=0x0 Informational=0x1 Warning=0x2 Error=0x3)<br/>                                                                      |
| FacilityNames=( = *Namesnummer* \[ :*Name* \] ) | Ein Satz von Namen, die für die Einrichtungswerte in einer Nachrichtendefinition zulässig sind. Jedem Einrichtungsnamen ist eine Zahl zugeordnet, die, wenn sie um 16 Bits nach links verschoben wird, das Bitmuster logischem OR mit dem Schweregrad und den Nachrichten-ID-Werten zum Bilden des Nachrichtencodes angibt. Jeder Einrichtungswert, der nicht in 12 Bits passt, ist ein Fehler. Dies ermöglicht 4.096 Einrichtungscodes. die ersten 256 Codes sind für die Systemverwendung reserviert. Den Einrichtungscodes können auch symbolische Namen gegeben werden. Der Standardwert ist wie folgt definiert: FacilityNames=( System=0x0FF Application=0xFFF)<br/> |
| LanguageNames=( = *Namesnummer*:*Dateiname*) | Gruppe von Namen, die für die Sprachwerte in einer Nachrichtendefinition zulässig sind. Die Zahl wird als Sprachbezeichner in der Ressourcentabelle verwendet. Die angegebene Datei enthält die Nachrichten für diese Sprache. Es handelt sich in der Regel um eine BIN-Datei, die vom Nachrichtencompiler generiert wird.<br/> Ein Beispielwert ist: LanguageNames=(English=0x409:MSG00409)<br/> Eine Liste der Sprachbezeichner finden Sie unter <https://go.microsoft.com/fwlink/p/?linkid=190280> .<br/>                                                                                                                    |
| OutputBase=*number*                        | Ausgaberadix für die Nachrichtenkonstanten, die der Nachrichtencompiler in die Headerdatei schreibt. Falls vorhanden, überschreibt dieser Wert den Schalter -d. Diese Zahl kann entweder 10 (dezimal) oder 16 (hexadezimal) sein.                                                                                                                                                                                                                                                                                                                                                                                   |



 

## <a name="message-definitions"></a>Nachrichtendefinitionen

Eine Meldungstextdatei enthält 0 (null) oder mehr Nachrichtendefinitionen, die dem Headerabschnitt folgen. In der folgenden Tabelle werden die Meldungsdefinitionsanweisungen beschrieben. Die MessageId-Anweisung markiert den Anfang der Nachrichtendefinition. Die Anweisungen "Severity" und "Facility" sind optional.



| Anweisungssyntax                  | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MessageId= \[ *Number* \| + *number*\] | Bezeichner für die Nachricht. Diese Anweisung ist erforderlich, obwohl der Wert optional ist. Wenn kein Wert angegeben wird, ist der verwendete Wert der vorherige Wert für die Einrichtung plus ein Wert. Wenn der Wert mit einem Pluszeichen angegeben wird, ist der verwendete Wert der vorherige Wert für die Einrichtung sowie die Zahl nach dem Pluszeichen. Jeder angegebene Wert muss in 16 Bits passen. Weitere Informationen dazu, wie der Nachrichtenwert aus Schweregrad, Einrichtung und Nachrichten-ID gebildet wird, finden Sie im Diagramm in Winerror.h. Diese Headerdatei definiert Fehlercodes für das System.<br/> |
| Severity=*name*                   | Einer der Von SeverityNames im Header angegebenen Werte. Diese Anweisung ist optional. Wenn kein Wert angegeben wird, ist der verwendete Wert der wert, der zuletzt für eine Nachrichtendefinition angegeben wurde. Der Standardwert für die erste Nachrichtendefinition ist `Severity=Success`<br/>                                                                                                                                                                                                                                                                                               |
| Facility=*name*                   | Einer der von FacilityNames im Header angegebenen Werte. Diese Anweisung ist optional. Wenn kein Wert angegeben wird, ist der verwendete Wert der wert, der zuletzt für eine Nachrichtendefinition angegeben wurde. Der Standardwert für die erste Nachrichtendefinition ist `Facility=Application`<br/>                                                                                                                                                                                                                                                                                           |
| SymbolicName=*name*               | Ordnet dem Nachrichtencode eine symbolische C/C++-Konstante zu. Sie wird in der Nachrichtendefinition wie folgt verwendet: \# define *name* ((*typ*)0x *nnnnnnnn )*<br/>                                                                                                                                                                                                                                                                                                                                                                                                     |
| OutputBase={*number*}             | Ausgaberadix für die Nachrichtenkonstanten, die der Nachrichtencompiler in die Headerdatei schreibt. Falls vorhanden, überschreibt dieser Wert den Schalter -d. Diese Zahl kann entweder 10 (dezimal) oder 16 (hexadezimal) sein.                                                                                                                                                                                                                                                                                                                                                                 |
| Language=*name*                   | Einer der Von LanguageNames im Header angegebenen Werte. Diese Anweisung ist optional. Wenn kein Wert angegeben wird, ist der verwendete Wert der wert, der zuletzt für eine Nachrichtendefinition angegeben wurde. Die Standardeinstellung für die erste Nachrichtendefinition lautet wie folgt: `Language=English`<br/>                                                                                                                                                                                                                                                                                   |
| *Meldungstext*                    | Text für die Nachricht. Sie ist in der Nachrichtenbinärdatei enthalten. Sie ist auch in der Headerdatei im Kommentarblock enthalten, der direkt vor der Nachrichtendefinition steht.                                                                                                                                                                                                                                                                                                                                                                                        |
| .                                 | Der Nachrichtentext wird durch eine neue Zeile beendet, die einen einzelnen Punkt am Anfang der Zeile enthält.                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |



 

Wenn die Nachrichtendefinition Nachrichtentext für mehrere Sprachen enthält, erfordert jede Sprache eine eigene Language-Anweisung, einen eigenen Nachrichtentext und das Beenden einer neuen Zeile mit einem Punkt. Beispiel:

``` syntax
MessageId=0x1
Severity=Error
Facility=Runtime
SymbolicName=MSG_BAD_COMMAND
Language=English
You have chosen an incorrect command.
.

Language=Japanese
<Japanese message string goes here>
.
```

Sie können die folgenden Escapesequenzen zum Formatieren von Meldungstext für die Verwendung durch die Ereignisanzeige oder Ihre Anwendung angeben. Das Prozentzeichen (%) beginnt mit allen Escapesequenzen. Alle anderen Zeichen, die auf ein Prozentzeichen folgen, werden ohne das Prozentzeichen angezeigt.

<dl> <dt>

<span id="_n__format_specifier__"></span><span id="_N__FORMAT_SPECIFIER__"></span>%*n* \[ ! *\_ Formatbezeichner*!\]
</dt> <dd>

Beschreibt eine Einfügung. Jede Einfügung ist ein Eintrag im Arguments-Array in der [**FormatMessage-Funktion.**](/windows/desktop/api/winbase/nf-winbase-formatmessage) Der Wert *n* kann eine Zahl zwischen 1 und 99 sein. Der Formatbezeichner ist optional. Wenn kein Wert angegeben wird, ist der Standardwert !s!. Informationen zum Formatbezeichner finden Sie unter [**wsprintf**](/windows/win32/api/winuser/nf-winuser-wsprintfa).

Der Formatbezeichner kann entweder \* für die Genauigkeit oder die Breite verwenden. Wenn angegeben, werden Einfügungen mit der Nummer *n*+1 und *n*+2 verwendet.

</dd> <dt>

<span id="_0"></span>%0
</dt> <dd>

Beendet eine Meldungstextzeile ohne ein nachstehend neues Zeilenumbruchzeichen. Dies kann verwendet werden, um eine lange Zeile zu erstellen oder eine Eingabeaufforderungsnachricht ohne nachstehend ein Zeilenumbruchzeichen zu beenden.

</dd> <dt>

<span id="_."></span>%.
</dt> <dd>

Generiert einen einzelnen Zeitraum. Dies kann verwendet werden, um einen Zeitraum am Anfang einer Zeile anzuzeigen, der andernfalls den Meldungstext beenden würde.

</dd> <dt>

<span id="__"></span>%!
</dt> <dd>

Generiert ein einzelnes Ausrufezeichen. Dies kann verwendet werden, um ein Ausrufezeichen unmittelbar nach einem Einfügezeichen anzugeben.

</dd> <dt>

<span id="__"></span>%%
</dt> <dd>

Generiert ein einzelnes Prozentzeichen.

</dd> <dt>

<span id="_n"></span><span id="_N"></span>%n
</dt> <dd>

Generiert einen harte Zeilenumbruch, wenn er am Ende einer Zeile auftritt. Dies kann mit [**FormatMessage verwendet**](/windows/desktop/api/winbase/nf-winbase-formatmessage) werden, um sicherzustellen, dass die Nachricht eine bestimmte Breite hat.

</dd> <dt>

<span id="_b"></span><span id="_B"></span>%b
</dt> <dd>

Generiert ein Leerzeichen. Dies kann verwendet werden, um eine angemessene Anzahl von nachstellenden Leerzeichen in einer Zeile sicherzustellen.

</dd> <dt>

<span id="_r"></span><span id="_R"></span>%r
</dt> <dd>

Generiert eine harter Wagenrücklaufrücklauf ohne ein nachlaufendes Neulinienzeichen.

</dd> </dl>

 

