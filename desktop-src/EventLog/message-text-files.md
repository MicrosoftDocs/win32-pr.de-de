---
description: Nachrichten werden in einer Meldungs Textdatei definiert. Der Nachrichten Compiler weist jeder Nachricht Zahlen zu und generiert eine C/C++ include-Datei, die von der Anwendung verwendet werden kann, um auf eine Nachricht mithilfe einer symbolischen Konstante zuzugreifen.
ms.assetid: 99fbb3d6-6fde-4162-b0b9-99a1cdf0b8f8
title: Meldungs Text Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e87547f44b0b556df4e3a2ffb67736b950321c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215571"
---
# <a name="message-text-files"></a>Meldungs Text Dateien

Nachrichten werden in einer Meldungs Textdatei definiert. Der Nachrichten Compiler weist jeder Nachricht Zahlen zu und generiert eine C/C++ include-Datei, die von der Anwendung verwendet werden kann, um auf eine Nachricht mithilfe einer symbolischen Konstante zuzugreifen.

Die allgemeine Syntax für-Anweisungen in einer Nachrichten Textdatei lautet wie folgt:

*Schlüsselwort* = *Wert*

Leerzeichen um das Gleichheitszeichen werden ignoriert, und der Wert wird durch Leerzeichen (einschließlich Zeilenumbrüchen) aus dem nächsten Schlüsselwort-Wert-Paar getrennt. Case wird beim Vergleich mit Schlüsselwort Namen ignoriert. Der *Wertteil* kann eine numerische ganzzahlige Konstante mit c/C++-Syntax, ein Symbol Name, der den Regeln für C/C++-Bezeichner folgt, oder ein Dateiname mit maximal 8 Zeichen ohne Zeiträume sein.

Eine Beispiel Nachrichtendatei finden Sie unter [Sample Message Textdatei](sample-message-text-file.md).

## <a name="comments"></a>Kommentare

In der Meldungs Textdatei sind Kommentarzeilen zulässig. Ein Semikolon (;) beginnt einen Kommentar, der am Ende der Zeile endet. Befolgen Sie das Semikolon mit einem einzeiligen C/C++-Kommentar Indikator (//), damit die vom Nachrichten Compiler generierte Header Datei in der Anwendung kompiliert wird.

``` syntax
;// This is a single-line comment.
```

Beginnen Sie für einen Block Kommentar jede Zeile mit einem Semikolon, und platzieren Sie dann einen C/C++ Open Block Comment Indicator (/ \* ) nach dem Semikolon in der ersten Zeile und dem schließende Block Kommentar Indikator ( \* /) nach dem Semikolon in der letzten Zeile.

``` syntax
;/* This is a block comment.
;   It spans multiple lines.
;*/
```

## <a name="header-section"></a>Headerabschnitt

Die Nachrichten Textdatei enthält einen Header, der Namen und sprach Bezeichner für die Verwendung durch die Nachrichten Definitionen im Text der Datei definiert. Der-Header enthält NULL oder mehr der folgenden Anweisungen.



| Anweisungs Syntax                           | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Messageidtypedef =*Typ*                    | Der in der Nachrichten Definition zu verwendende Typ wie folgt: \# define *Name* ((*Type*) 0x *nnnnnnnnnn*)<br/> Der Typ muss groß genug sein, um den gesamten Nachrichten Code, z. b. ein **DWORD**, aufnehmen zu können. Der Typ kann auch ein Typ sein, der im Quellcode der Anwendung definiert ist. Der Standardwert für den *Typ* ist leer, sodass keine Typumwandlung verwendet wird. <br/> Diese Anweisung kann im-Header und so oft wie nötig im Abschnitt Nachrichten Definition angegeben werden.<br/>                                                                                                                  |
| Schwere Amen = (*namens* = *Nummer* \[ :*Name* \] ) | Ein Satz von Namen, die in einer Nachrichten Definition für den Schweregrad zulässig sind. Jeder Schweregrad Name zugeordnet ist eine Zahl, die das Bitmuster bei der nach-links-nach-unten-durch 30 Bits-Struktur dem logischen OR mit den Werten für die Einrichtung und die Nachrichten-ID zum bilden des Nachrichten Codes übergibt. Ein Schweregrad, der nicht in 2 Bits passt, ist ein Fehler. Die Schweregrade können auch symbolische Namen erhalten. Der Standardwert wird wie folgt definiert: severitynames = (Success = 0x0 Information = 0x1 Warning = 0x2 Error = 0x3)<br/>                                                                      |
| *Name* der Netzwerknamen = (Name- = *Nummer* \[ :*Name* \] ) | Ein Satz von Namen, die für die Einrichtungs Werte in einer Nachrichten Definition zulässig sind. Die Zuordnung zu den einzelnen Einrichtungs Namen ist eine Zahl, die das Bitmuster für das logische OR mit den Werten für Schweregrad und Nachrichten-ID zum bilden des Nachrichten Codes ergibt, wenn Sie von 16 Bits nach links verschoben wird. Jeder Einrichtungs Wert, der nicht in 12 Bits passt, ist ein Fehler. Dies ermöglicht 4096-Anlagen Codes. die ersten 256 Codes sind für die Verwendung durch das System reserviert. Die Einrichtungs Codes können auch symbolische Namen erhalten. Der Standardwert wird wie folgt definiert: "", "", "", "".<br/> |
| LanguageNames = (*namens* = *Nummer*:*Dateiname*) | Ein Satz von Namen, die für die sprach Werte in einer Nachrichten Definition zulässig sind. Die Zahl wird als sprach Bezeichner in der Ressourcen Tabelle verwendet. Die angegebene Datei enthält die Meldungen für diese Sprache. Es handelt sich in der Regel um eine vom Nachrichten Compiler generierte bin-Datei.<br/> Ein Beispiel Wert ist: LanguageNames = (English = 0x409: MSG00409)<br/> Eine Liste der Sprachen-IDs finden Sie unter <https://go.microsoft.com/fwlink/p/?linkid=190280> .<br/>                                                                                                                    |
| OutputBase =*Zahl*                        | Ausgabe Basis für die Nachrichten Konstanten, die der Nachrichten Compiler in die Header Datei schreibt. Falls vorhanden, überschreibt dieser Wert den Schalter-d. Diese Zahl kann entweder 10 (Decimal) oder 16 (hexadezimal) sein.                                                                                                                                                                                                                                                                                                                                                                                   |



 

## <a name="message-definitions"></a>Nachrichten Definitionen

Eine Meldungs Textdatei enthält 0 (null) oder mehr Nachrichten Definitionen nach dem Header Abschnitt. In der folgenden Tabelle werden die Nachrichten Definitions Anweisungen beschrieben. Die MessageId-Anweisung markiert den Anfang der Nachrichten Definition. Die Anweisungen für den Schweregrad und den Betrieb sind optional.



| Anweisungs Syntax                  | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MessageId = \[ *Zahl* \| + *Nummer*\] | Der Bezeichner für die Nachricht. Diese Anweisung ist erforderlich, obwohl der Wert optional ist. Wenn kein Wert angegeben wird, ist der verwendete Wert der vorherige Wert für die Einrichtung Plus 1. Wenn der Wert mit einem Pluszeichen angegeben wird, ist der verwendete Wert der vorherige Wert für die-Funktion und die Zahl nach dem Pluszeichen. Jeder angegebene Wert muss in 16 Bits passen. Weitere Informationen zur Art und Weise, in der der Nachrichtenwert aus dem Schweregrad, der Einrichtung und der Meldungs-ID besteht, finden Sie im Diagramm in WinError. h. Diese Header Datei definiert Fehlercodes für das System.<br/> |
| Schweregrad =*Name*                   | Einer der Werte, die von "severitynames" in der Kopfzeile angegeben werden. Diese Anweisung ist optional. Wenn kein Wert angegeben ist, wird der Wert verwendet, der zuletzt für eine Nachrichten Definition angegeben wurde. Der Standardwert für die erste Nachrichten Definition ist. `Severity=Success`<br/>                                                                                                                                                                                                                                                                                               |
| Einrichtung =*Name*                   | Einer der Werte, die von "facilitynames" in der Kopfzeile angegeben werden. Diese Anweisung ist optional. Wenn kein Wert angegeben ist, wird der Wert verwendet, der zuletzt für eine Nachrichten Definition angegeben wurde. Der Standardwert für die erste Nachrichten Definition ist. `Facility=Application`<br/>                                                                                                                                                                                                                                                                                           |
| SymbolicName =*Name*               | Ordnet dem Nachrichten Code eine symbolische Konstante von C/C++ zu. Sie wird in der Nachrichten Definition wie folgt verwendet: \# define *Name* ((*Typ*) 0x *nnnnnnnnnnnn*)<br/>                                                                                                                                                                                                                                                                                                                                                                                                     |
| OutputBase = {*Number*}             | Ausgabe Basis für die Nachrichten Konstanten, die der Nachrichten Compiler in die Header Datei schreibt. Falls vorhanden, überschreibt dieser Wert den Schalter-d. Diese Zahl kann entweder 10 (Decimal) oder 16 (hexadezimal) sein.                                                                                                                                                                                                                                                                                                                                                                 |
| Language =*Name*                   | Einer der Werte, die von LanguageNames in der Kopfzeile angegeben werden. Diese Anweisung ist optional. Wenn kein Wert angegeben ist, wird der Wert verwendet, der zuletzt für eine Nachrichten Definition angegeben wurde. Der Standardwert für die erste Nachrichten Definition lautet wie folgt: `Language=English`<br/>                                                                                                                                                                                                                                                                                   |
| *Meldungs Text*                    | Der Text für die Nachricht. Es ist in der Nachrichten Binärdatei enthalten. Sie ist auch in der Header Datei im Kommentar Block enthalten, der direkt vor der Nachrichten Definition steht.                                                                                                                                                                                                                                                                                                                                                                                        |
| .                                 | Der Nachrichtentext wird durch eine neue Zeile mit einem einzelnen Zeitraum am Anfang der Zeile beendet.                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |



 

Wenn die Nachrichten Definition Nachrichtentext für mehr als eine Sprache enthält, erfordert jede Sprache ihre eigene sprach Anweisung, den Meldungs Text und das Beenden einer neuen Zeile mit einem Zeitraum. Beispiel:

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

Sie können die folgenden Escapesequenzen zum Formatieren von Meldungs Text angeben, der von der Ereignisanzeige oder der Anwendung verwendet werden soll. Das Prozentzeichen (%). beginnt alle Escapesequenzen. Alle anderen Zeichen, die auf ein Prozentzeichen folgen, werden ohne das Prozentzeichen angezeigt.

<dl> <dt>

<span id="_n__format_specifier__"></span><span id="_N__FORMAT_SPECIFIER__"></span>%*n* \[ ! *Format \_* Bezeichner!\]
</dt> <dd>

Beschreibt einen Einfügevorgang. Jede Einfügung ist ein Eintrag im Argument Array in der [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) -Funktion. Der Wert von *n* kann eine Zahl zwischen 1 und 99 sein. Der Formatspezifizierer ist optional. Wenn kein Wert angegeben ist, lautet der Standardwert! s!. Weitere Informationen zum Format Bezeichner finden Sie unter [**wsprintf**](/windows/win32/api/winuser/nf-winuser-wsprintfa).

Der Format Bezeichner kann \* entweder für die Genauigkeit oder die Breite verwendet werden. Wenn angegeben, werden die Einfügungen mit der nummerierten *n*+ 1 und *n*+ 2 verarbeitet.

</dd> <dt>

<span id="_0"></span>%0
</dt> <dd>

Beendet eine Meldungs Textzeile ohne nachfolgende Zeilenumbruch Zeichen. Dies kann verwendet werden, um eine lange Zeile zu erstellen oder eine Eingabe Aufforderungs Meldung ohne nachfolgende Zeilenumbruch Zeichen zu beenden.

</dd> <dt>

<span id="_."></span>%.
</dt> <dd>

Generiert einen einzelnen Zeitraum. Dies kann verwendet werden, um einen Zeitraum am Anfang einer Zeile anzuzeigen, der andernfalls den Nachrichtentext beenden würde.

</dd> <dt>

<span id="__"></span>%!
</dt> <dd>

Generiert ein einzelnes Ausrufezeichen. Dies kann zum Angeben eines Ausrufezeichens unmittelbar nach einer Einfügung verwendet werden.

</dd> <dt>

<span id="__"></span>%%
</dt> <dd>

Generiert ein einzelnes Prozentzeichen.

</dd> <dt>

<span id="_n"></span><span id="_N"></span>% n
</dt> <dd>

Generiert einen harten Zeilenumbruch, wenn er am Ende einer Zeile vorkommt. Dies kann mit [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) verwendet werden, um sicherzustellen, dass die Nachricht einer bestimmten Breite entspricht.

</dd> <dt>

<span id="_b"></span><span id="_B"></span>% b
</dt> <dd>

Generiert ein Leerzeichen. Dies kann verwendet werden, um eine geeignete Anzahl von nachfolgenden Leerzeichen in einer Zeile sicherzustellen.

</dd> <dt>

<span id="_r"></span><span id="_R"></span>% r
</dt> <dd>

Generiert einen fest Wagen Rücklauf ohne nachfolgende Zeilenumbruch Zeichen.

</dd> </dl>

 

