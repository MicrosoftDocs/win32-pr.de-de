---
description: Die Erweiterte Abfrage Syntax (AQS) ist die Standard Abfrage Syntax, die von Windows Search verwendet wird, um den Index abzufragen und Suchparameter zu verfeinern und einzuschränken.
ms.assetid: 76e33903-d063-48c0-9afe-912c3daa8237
title: Programm gesteuertes verwenden der erweiterten Abfrage Syntax
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc8fa69a5a5ccaa37b84a10abd367e5a29656455
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345673"
---
# <a name="using-advanced-query-syntax-programmatically"></a>Programm gesteuertes verwenden der erweiterten Abfrage Syntax

Die Erweiterte Abfrage Syntax (AQS) ist die Standard Abfrage Syntax, die von Windows Search verwendet wird, um den Index abzufragen und Suchparameter zu verfeinern und einzuschränken. AQS wird von Entwicklern verwendet, um Abfragen Programm gesteuert zu erstellen (und von Benutzern, um Ihre Suchparameter einzuschränken). Kanonische AQS wurde in Windows 7 eingeführt und muss in Windows 7 und höher zum programmgesteuerten Generieren von AQS-Abfragen verwendet werden.

Dieses Thema ist wie folgt organisiert:

-   [Informationen zur erweiterten Abfrage Syntax](#about-advanced-query-syntax)
    -   [Beispiele](#examples)
    -   [Eigenschaften](#properties)
-   [Schlüsselwort Verwendung in lokalen Sprachen](#keyword-use-in-local-languages)
-   [Kanonische Erweiterte Abfrage Syntax in Windows 7](#canonical-advanced-query-syntax-in-windows-7)
    -   [Beispiele](#examples)
    -   [Abfrage Operatoren](#query-operators)
    -   [Abfrage Werte](#query-values)
-   [Bereichs Einschränkungen](#scope-restrictions)
-   [Weitere Ressourcen](#additional-resources)
-   [Zugehörige Themen](#related-topics)

## <a name="about-advanced-query-syntax"></a>Informationen zur erweiterten Abfrage Syntax

Eine Abfrage besteht aus grundlegenden Abfragen, die mit and, or und Not verbunden sind, wie in der folgenden Beispiel Syntax gezeigt:

``` syntax
<query> ::=
     <basic query>
| ( <query> )
| <query> AND <query>  
| <query> <query>    // Same as <query> AND <query>
| <query> OR <query> 
| NOT <query>
```

> [!Note]  
> Bei AQS wird die Groß-/Kleinschreibung nicht beachtet, mit Ausnahme von and, or, und Not, das in Großbuchstaben vorliegen muss.

 

Wenn eine Abfrage zwei oder mehr Verwendungen von and oder or aufweist, werden Sie von links nach rechts gebunden, unabhängig davon, ob es sich um and oder or handelt. Das heißt, die Abfrage "Apple und Birnen oder Plum" wird so interpretiert, als ob Sie als "(Apple, Birne) oder Plum" geschrieben wäre, und die Abfrage "Apple", "PEAR" und "Plum" wird so interpretiert, als ob Sie als "(Apple oder Birne) und Plum" geschrieben wäre. Wenn ein Dokument das Wort Plum, aber weder Apple noch Birnen enthält, gibt die erste Abfrage es zurück, die zweite Abfrage jedoch nicht. Daher wird empfohlen, dass Sie für jede Abfrage, die and und or kombiniert, explizite Klammern verwenden, um Fehler oder Fehlinterpretationen zu vermeiden.

Eine grundlegende Abfrage sucht nach Elementen, die eine Einschränkung für eine Eigenschaft erfüllen. Der einzige erforderliche Teil einer grundlegenden Abfrage ist der Einschränkungs-oder Suchwert. Wenn Sie keine Eigenschaft angeben, durchsucht Windows Search alle Eigenschaften. <restr> stellt die Such Einschränkung dar.

Die folgenden Formulare für eine einfache Abfrage sind gültig:

``` syntax
<basic query> ::=
     <prop>:<basic restr>
| <restr>
```

Eine Eigenschaft wird durch ein Schlüsselwort wie "Author" oder "size" oder durch einen kanonischen Eigenschaftsnamen wie " [System. DateModified](../properties/props-system-datemodified.md)" angegeben. Gültige Formulare für eine Eigenschaft sind wie folgt:

``` syntax
<prop> ::= 
     <canonical property name>
| <property label in UI language>
```

Ein Operator gibt einen Vorgang an, z. b. < oder =. Eine Liste gültiger Operatoren finden Sie im Abschnitt Abfrage Operatoren weiter unten in diesem Thema.

Eine grundlegende Einschränkung ist eine einfache Einschränkung für eine Eigenschaft, die ohne Klammern geschrieben werden kann:

``` syntax
<basic restr> ::=
     <value>
| <op><value>
| NOT <basic restr>
| ( <restr> )
```

Eine Einschränkung ist ein Suchwert, z. b. ein Zahlenwert oder ein Zeichen folgen Wert, optional mit einem-Operator. Gültige Formulare für eine Einschränkung lauten wie folgt:

``` syntax
<restr> ::=
    <basic restr>
| <restr> AND <restr>
| <restr> <restr>      // Same as <restr> AND <restr>
| <restr> OR <restr>
```

Wenn Sie keinen Operator angeben, wählt Windows Search den am besten geeigneten Operator für die Abfrage aus:

-   Für eine Zeichen folgen Eigenschaft wird der COP \_ Word- \_ Operator StartWith $< angenommen.
-   Für alle anderen Eigenschaften wird der COP \_ EQUAL =-Operator angenommen.

Für die programmgesteuerte Verwendung von AQS wird empfohlen, dass Sie immer über einen expliziten Operator verfügen. Das gültige Formular für die Suche nach einem einfachen Wert oder Wertebereich lautet wie folgt:

``` syntax
<value> ::=
    <simplevalue>
| <simplevalue> .. <simplevalue>
```

Ein einfacher Wert kann aus einem der folgenden Typen bestehen:

``` syntax
<simplevalue> ::=
  []         // No value, or a null value
| <word>     // A sequence of characters without whitespace
| <number>   // An integer or a floating point number
| <datetime> // A relative date, or an absolute date and/or time
| <Boolean>
| "..."      // A phrase
| <enumeration range>
```

### <a name="examples"></a>Beispiele

Eine Abfrage, die nach einem Dokument mit der von Theresa oder Lee erstellten Phase "Letztes Quartal" sucht und im Ordner "MyDocs" gespeichert wurde, kombiniert drei grundlegende Abfragen wie folgt:

``` syntax
"last quarter" author:(theresa OR lee) folder:MyDocs
```

Die drei grundlegenden Abfragen lauten:

-   "Letztes Quartal"
-   Autor: (Theresa oder Lee)
-   Ordner: MyDocs

Eine einfache Abfrage, die kanonische Syntax verwendet, lautet:

``` syntax
System.Size:>1kb
```

### <a name="properties"></a>Eigenschaften

Auf Eigenschaften wird durch ein Schlüsselwort verwiesen, das in Windows 7 und höher als kanonischer Eigenschaftsname dienen kann. AQS in der Windows-Benutzeroberfläche kann die Bezeichnung anstelle des kanonischen Eigenschaften namens verwenden, z. b. "Author" anstelle von " [System. Author](../properties/props-system-author.md)". In Windows Vista und früheren Versionen war es möglich, englische Bezeichnungen unabhängig von der Benutzeroberflächen Sprache zu verwenden. In Windows 7 und höher erkennt Windows Search Schlüsselwörter nur in der aktuellen Standardsprache der Benutzeroberfläche.

### <a name="support-for-custom-properties"></a>Unterstützung für benutzerdefinierte Eigenschaften

In Windows Vista und früheren Versionen waren benutzerdefinierte Eigenschaften in AQS nicht verfügbar. In Windows 7 und höher funktioniert AQS mit benutzerdefinierten Eigenschaften, die im-Eigenschaften System registriert sind. Weitere Informationen zum Erstellen von benutzerdefinierten Eigenschaften finden Sie unter Eigenschaften [System](../properties/building-property-handlers.md).

### <a name="datetime-properties-in-windows-8"></a>DateTime-Eigenschaften in Windows 8

Ab Windows 8 unterstützen DateTime-Eigenschaften (z. b [. System. DateModified](../properties/props-system-datemodified.md)) das in [ISO-8601](https://www.w3.org/TR/NOTE-datetime)angegebene kanonische Datums-und Uhrzeit Format, optional einschließlich der UTC-Zeitzone.

-   **Windows 8 und früher, Datum/Uhrzeit ohne UTC-Zeitzone:** *yyyy* - *mm* - *ddThh*:*mm*:*SS*

    Dieses Format gibt eine lokale Uhrzeit an, unabhängig vom Benutzer-oder System Gebiets Schema.

-   **Windows 8, Datum und Uhrzeit mit UTC-Zeitzone:** *yyyy* - *mm* - *ddThh*:*mm*:*sstzd*

    Dieses Format gibt eine Uhrzeit in der angegebenen UTC-Zeitzone an.

## <a name="keyword-use-in-local-languages"></a>Schlüsselwort Verwendung in lokalen Sprachen

In Windows 7 und höher funktionieren mnetmonische Schlüsselwörter nur in der Systemsprache, wie z. b. deutschen Schlüsselwörtern nur auf einem deutschen Betriebssystem und englischen Schlüsselwörtern nur in einem englischen Betriebssystem. [System. Author](../properties/props-system-author.md) ist ein kanonisches Schlüsselwort, und der mnetmonische Wert für die System. Author-Eigenschaft ist beispielsweise Author. Durch die Einführung von kanonischen Schlüsselwörtern wird die Tatsache kompensiert, dass englische mmaische Schlüsselwörter nicht mehr universell auf allen Betriebssystemen erkannt werden, und zwar unabhängig von der Sprache, wie es in Windows Vista und früheren Versionen der Fall war.

> [!Note]  
> In Windows 7 und höher erkennt Windows Search Schlüsselwörter nur in der aktuellen Standardsprache und nicht in englischer Sprache, es sei denn, English ist die aktuelle Standardsprache. Es wird empfohlen, dass Entwickler immer eine kanonische Syntax verwenden, damit Ihre Anwendung keine Sprachprobleme mit Schlüsselwörtern hat.

 

## <a name="canonical-advanced-query-syntax-in-windows-7"></a>Kanonische Erweiterte Abfrage Syntax in Windows 7

Die kanonische Syntax wurde für Schlüsselwörter in Windows 7 eingeführt. Ein Beispiel für eine Abfrage mit einer kanonischen-Eigenschaft ist `System.Message.FromAddress:=me@microsoft.com` . Beim Codieren von Abfragen in Anwendungen, die unter Windows 7 und höher ausgeführt werden, müssen Sie kanonische Syntax verwenden, um AQS-Abfragen Programm gesteuert zu generieren. Wenn Sie keine kanonische Syntax verwenden und die Anwendung in einer Gebiets Schema-oder Benutzeroberflächen Sprache bereitgestellt wird, die sich von der Sprache im Anwendungscode unterscheidet, werden die Abfragen nicht ordnungsgemäß interpretiert.

Die Konventionen für die kanonische Schlüsselwort Syntax lauten wie folgt:

-   Die kanonische Syntax für eine Eigenschaft ist Ihr kanonischer Name, z `System.Photo.LightSource` . b.. Kanonische Namen beachten die Groß-/Kleinschreibung nicht.
-   Die kanonische Syntax für die booleschen Operatoren besteht aus den Schlüsselwörtern and, or und Not in Großbuchstaben.
-   Die Operatoren <, >, = usw., werden nicht lokalisiert und sind daher auch Teil der kanonischen Syntax.
-   Wenn eine Eigenschaft `P` Werte oder Bereiche mit dem Namen N ₁ bis NK aufzählt, ist die kanonische Syntax für den *I* Th-Wert oder-Bereich der kanonische Name für P, gefolgt vom Zeichen gefolgt von \# n <sub>I</sub>, wie im folgenden Beispiel gezeigt:
    -   `System.Photo.LightSource#Daylight`, `System.Photo.LightSource#StandardA` usw.
-   Für einen definierten Semantik Typ t mit Werten oder Bereichen mit dem Namen N ₁ bis NK ist die kanonische Syntax für den *I* Th-Wert oder-Bereich der kanonische Name für t, gefolgt vom Zeichen gefolgt von \# n <sub>I</sub>, wie im folgenden Beispiel gezeigt:
    -   `System.Devices.LaunchDeviceStageFromExplorer:=System.StructuredQueryType.Boolean#True`
-   Bei Literalwerten wie Wörtern oder Ausdrücken ist die kanonische Syntax die gleiche wie die reguläre Syntax. Beispiele für Abfragen mit Literalwerten in kanonischer Syntax:
    -   `System.Author:sanjay`
    -   `System.Keywords:"Animal"`
    -   `System.FileCount:>100`

> [!Note]  
> Es gibt keine kanonische Syntax für Zahlen in Windows 7 und höher. Da Gleit Komma Formate sich zwischen den Gebiets Schemata unterscheiden, wird die Verwendung einer kanonischen Abfrage, die eine Gleit Komma Konstante einschließt, nicht unterstützt. Ganzzahlige Konstanten hingegen können nur mit Ziffern (keine Trennzeichen für Tausende) geschrieben werden und können in kanonischen Abfragen in Windows 7 und höher sicher verwendet werden.

 

### <a name="examples"></a>Beispiele

In der folgenden Tabelle sind einige Beispiele für kanonische Eigenschaften und die Syntax für deren Verwendung aufgeführt.



| Typ der kanonischen Eigenschaft | Beispiel                                                                                     | Syntax                                                                                                                                                                                                                                                  |
|----------------------------|---------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Zeichenfolgenwert               | [System.Author](../properties/props-system-author.md)<br/>    | Der Zeichen folgen Wert wird in der Author-Eigenschaft nach gesucht: <br/>`System.Author:Jacobs`                                                                                                                                                              |
| Enumerationsbereich          | [System. Priority](../properties/props-system-priority.md)             | Die Priority-Eigenschaft kann einen numerischen Wertebereich aufweisen:<br/>`System.Priority:System.Priority#High`                                                                                                                                                |
| Boolean                    | [System. IsDeleted](../properties/props-system-isdeleted.md)<br/> | Boolesche Werte können mit jeder booleschen Eigenschaft verwendet werden:<br/>`System.IsDeleted:System.StructuredQueryType.Boolean#True` und `System.IsDeleted:System.StructuredQueryType.Boolean#False`                                                             |
| Numerisch                  | [System. Size](../properties/props-system-size.md)<br/>      | Es ist nicht möglich, eine kanonische Abfrage, die eine Gleit Komma Konstante umfasst, sicher zu schreiben, da Gleit Komma Formate sich zwischen den Gebiets Schemata unterscheiden. Ganze Zahlen müssen ohne Trennzeichen für Tausende geschrieben werden. Beispiel:<br/>`System.Size:<12345` |



 

Weitere Informationen über kanonische Eigenschaften und das Eigenschaften System finden Sie unter [Systemeigenschaften](../properties/props.md). Alternativ dazu können Sie auch die öffentlichen Header Dateien lesen.

### <a name="query-operators"></a>Abfrageoperatoren

Wenn eine Eigenschaft, p, mehrere Werte für ein Element aufweist, gibt eine AQS-Abfrage für p: <restr> das Element zurück, wenn <restr> für mindestens einen der Werte **true** ist. ( <restr> stellt eine Einschränkung dar.)

Die in der folgenden Tabelle aufgeführte Syntax besteht aus einem Operator, einem Operator Symbol, einem Beispiel und einer Beispiel Beschreibung. Der Operator und das Symbol können in jeder beliebigen Sprache verwendet und in beliebige Abfragen eingeschlossen werden. Verwenden Sie nicht die entsprechenden Cop- \_ oder Cop- \_ Anwendungs \_ spezifischen Operatoren. Einige der Operatoren verfügen über austauschbare Symbole.



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Operator</th>
<th>Symbol</th>
<th>Beispiel</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>COP_EQUAL</td>
<td>=<br/></td>
<td>System. File Extension: = &quot; . txt&quot;<br/></td>
<td>Der Wert ist "String &quot; <em>. txt</em>" &quot; .<br/></td>
</tr>
<tr class="even">
<td>COP_NOTEQUAL</td>
<td>≠<br/> -<br/> &lt;&gt;<br/> NICHT<br/> - -<br/></td>
<td>System. Kind: ≠-Bild<br/> System. Photo. DateTaken:-[] ¹<br/> System. Kind: &lt; &gt; Bild<br/> System. Kind: nicht Bild<br/> System. Kind:--Bild<br/></td>
<td>Die <a href="/windows/desktop/properties/props-system-kind">System. Kind</a> -Eigenschaft ist kein Bild.<br/> Die <a href="/windows/desktop/properties/props-system-photo-datetaken">System. Photo. DateTaken</a> -Eigenschaft weist einen Wert auf.<br/> Die <a href="/windows/desktop/properties/props-system-kind">System. Kind</a> -Eigenschaft ist kein Bild. <br/> Die <a href="/windows/desktop/properties/props-system-kind">System. Kind</a> -Eigenschaft ist kein Bild. <br/> Doppelte not-Operatoren, die auf dieselbe Eigenschaft angewendet werden, werden nicht abgebrochen. Daher ist System. Kind:--Picture Äquivalent zu System. Kind:-Picture und System. Kind: Not Picture.<br/></td>
</tr>
<tr class="odd">
<td>COP_LESSTHAN</td>
<td>&lt;<br/></td>
<td>System. size: &lt; 1 KB<br/></td>
<td>Dieser Wert ist kleiner als <em>1 KB</em>.<br/></td>
</tr>
<tr class="even">
<td>COP_GREATERTHAN</td>
<td>&gt;<br/></td>
<td>System. itemdate: &gt; System. structuredquerytype. DateTime # heute<br/></td>
<td>Dieser Wert ist größer als <em>heute</em>.<br/></td>
</tr>
<tr class="odd">
<td>COP_LESSTHANOREQUAL</td>
<td>&lt;=<br/> ≤<br/></td>
<td>System. size: &lt; = 1 KB<br/></td>
<td>Dieser Wert ist kleiner oder gleich <em>1 KB</em>.<br/></td>
</tr>
<tr class="even">
<td>COP_GREATERTHANOREQUAL</td>
<td>&gt;=<br/> ≥<br/></td>
<td>System. size: &gt; = 1 KB<br/></td>
<td>Dieser Wert ist gleich oder größer als <em>1 KB</em>.<br/></td>
</tr>
<tr class="odd">
<td>COP_VALUE_STARTSWITH</td>
<td>~&lt;<br/></td>
<td>System. filename: ~ &lt; &quot; C++ Primer&quot;<br/></td>
<td>Sucht nach Elementen, bei denen der Dateiname mit den Zeichen &quot; <em>C++ "Primer</em>" beginnt &quot; .<br/></td>
</tr>
<tr class="even">
<td>COP_VALUE_ENDSWITH</td>
<td>~&gt;<br/></td>
<td>System. Photo. CameraModel: ~ &gt; Non<br/></td>
<td>Sucht nach Elementen, bei denen der Eigenschafts Wert mit den Zeichen <em>nicht</em>endet.<br/></td>
</tr>
<tr class="odd">
<td>COP_VALUE_CONTAINS</td>
<td>~=<br/> ~~<br/></td>
<td>System. Subject. ~ = Round <br/> System. search. autosummary: ~ ~ Round<br/></td>
<td>Sucht eine Meldung, die diese Zeichenfolge im Betreff hat, und entspricht &quot; z. b. g-<em>runden</em> Regeln &quot; .<br/> Sucht alle Elemente mit einer autosummary, die die Zeichen <em>Runde</em>enthält.<br/></td>
</tr>
<tr class="even">
<td>COP_VALUE_NOTCONTAINS</td>
<td>~!<br/></td>
<td>System. Author: ~! &quot; Sanjay&quot;<br/></td>
<td>Sucht Autoren, die nicht über die Zeichenfolge &quot; <em>Sanjay</em> verfügen &quot; .<br/></td>
</tr>
<tr class="odd">
<td>COP_DOSWILDCARDS</td>
<td>~ <br/></td>
<td>System. filename: ~ &quot; MIC? osoft W * d&quot;<br/></td>
<td>Sucht nach Dateien, bei denen der Dateiname mit <em>MIC</em>beginnt, gefolgt von einem Zeichen, gefolgt von <em>osoft w</em>, gefolgt von allen Zeichen, die mit <em>d</em>enden. <br/> Mit dem Zeichen „?“ und * Zeichen werden nicht buchstäblich interpretiert und funktionieren wie Platzhalter Zeichen im DOS-Stil:<br/>
<ul>
<li>? entspricht einem beliebigen Zeichen.</li>
<li>* entspricht 0 (null) oder mehr beliebigen Zeichen.</li>
</ul></td>
</tr>
<tr class="even">
<td>COP_WORD_EQUAL</td>
<td>$=<br/> $$<br/></td>
<td>System. StructuredQuery. Virtual. from: $ = &quot; Sanjay Jacobs&quot;<br/></td>
<td>Für Windows 7 und höher. Sucht den Ausdruck &quot; <em>Sanjay Jacobs</em> &quot; in allen Eigenschaften. Auf das Wort <em>Sanjay</em> muss das Wort <em>Jacobs</em>folgen.<br/></td>
</tr>
<tr class="odd">
<td>COP_WORD_STARTSWITH</td>
<td>$<<br/></td>
<td>System. Author: $<&quot;San&quot; System.Filename:$<&quot;Micro Exe&quot;<br/></td>
<td>Für Windows 7 und höher. Sucht nach jedem Element, bei dem der Autor ein Wort enthält, das mit den Zeichen &quot; <em>San</em>beginnt &quot; .<br/> Findet eine beliebige Datei, in der der Dateiname ein Wort enthält, das mit <em>Micro</em>beginnt, gefolgt von einem Wort, das mit <em>exe</em>beginnt.<br/></td>
</tr>
</tbody>
</table>



 

¹ leere eckige Klammern ( \[ \] ) kennzeichnen "kein Wert".

Für Zeichen folgen Eigenschaften ist der Standard Vorgang entweder Cop \_ Word \_ beginnt \_ mit oder Cop \_ Word \_ gleich.

### <a name="query-values"></a>Abfrage Werte

In der folgenden Tabelle sind nützliche Beispiele für die Einschränkung von Abfrage Werten aufgeführt.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Wert/Symbol</th>
<th>Beispiele</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>String</td>
<td>auto<br/></td>
<td>Eine beliebige Sequenz von Zeichen, nach denen gesucht werden kann. Die Zeichenfolge darf keine Leerzeichen oder Zeichenkombinationen enthalten, die Teil der Syntax sind. Dieses Beispiel sucht nach einem Wort, das mit " <em>Auto</em>" beginnt.<br/></td>
</tr>
<tr class="even">
<td>Zeichenfolge in Zeichen &quot;&quot;</td>
<td>&quot;Schlussfolgerungen: gültiges &quot; &quot; &quot; &quot; blaues &quot; &quot; Team&quot;<br/></td>
<td>Eine beliebige Sequenz von Zeichen. Die Zeichenfolge wird nicht als Teil der Syntax interpretiert.<br/> Anführungszeichen können in eine Abfrage eingeschlossen werden, wenn Sie verdoppelt werden. Dieses Beispiel sucht nach <em>dem &quot; blauen &quot; Team</em>.<br/></td>
</tr>
<tr class="odd">
<td>Integer</td>
<td>5678<br/></td>
<td>Verwenden Sie nur Ziffern für ganze Zahlen. Verwenden Sie keine Trennzeichen für Tausender.<br/></td>
</tr>
<tr class="even">
<td>Gleitkommazahl</td>
<td>5678,1234<br/></td>
<td>Da Gleit Komma Formate sich zwischen den Gebiets Schemata unterscheiden, kann eine kanonische Abfrage keine Gleit Komma Konstante verwenden. Die Verwendung von kanonischer Syntax mit Gleit Komma Zahlen ist nicht Lokalisierungs sicher. <br/></td>
</tr>
<tr class="odd">
<td>Boolescher Wert <strong>true</strong> / <strong>false</strong></td>
<td>System. isread: = System. structuredquerytype. Boolean # true<br/> System. isverschlüsselte:-System. structuredquerytype. Boolean # false<br/></td>
<td>Der <strong>echte</strong> boolesche Wert.<br/> Der boolesche Wert <strong>false</strong> .<br/></td>
</tr>
<tr class="even">
<td>[]</td>
<td>System. Keywords: = []<br/></td>
<td>Leere eckige Klammern kennzeichnen, dass kein Wert vorhanden ist. In diesem Beispiel werden alle Elemente gesucht, die nicht markiert wurden. <br/></td>
</tr>
<tr class="odd">
<td>Absolute Datumsangaben</td>
<td>System. itemdate: 1/26/2010<br/> Systemdatemodified 10/15/2002 19:00<br/></td>
<td>Sucht nach Elementen mit dem Datum 26. Januar 2010.<br/> Ermittelt Elemente, die am 15. Oktober 2002 zwischen den Stunden 19:00:00 und 19:00:59 geändert wurden. <br/>
<blockquote>
[!Note]<br />
Da Datumsformate (z. b. Gleit Komma Formate) zwischen Gebiets Schemata variieren, wird die Verwendung von kanonischer Syntax mit absoluten Datumsangaben nicht unterstützt und ist nicht Lokalisierungs sicher.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>Relative Datumsangaben</td>
<td>System. itemdate: System. structuredquerytype. DateTime # heute<br/> System. dateerworbener Name: System. structuredquerytype. DateTime # nextmonth<br/> System. Message. DateReceived: System. structuredquerytype. DateTime # lastYear<br/></td>
<td>Sucht nach Elementen mit dem heutigen Datum.<br/> Findet Elemente mit einem Datum im nächsten Monat.<br/> Findet Elemente mit einem Datum im letzten Jahr.<br/>
<blockquote>
[!Note]<br />
Neben der Suche nach bestimmten Datums-und Datumsbereichen werden von AQS relative Datumswerte (z. b. <em>heute</em>, <em>Morgen</em>, <em>nextweek</em>, <em>nextmonth</em>) und Day (z. b. <em>Dienstag</em> oder Montag) erkannt <em>. Mittwoch</em>) und Monat (<em>Februar</em>).
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>..</td>
<td>System. itemdate: 11/05/04.. 11/10/04 System. size: 5 KB. 10 KB<br/></td>
<td>Doppelte Zeiträume geben einen Wertebereich an. Sucht nach Elementen, deren Datum zwischen 11/05/04 und 11/10/04 (einschließlich) liegt.<br/> Sucht nach Elementen zwischen 5 und 10 KB.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="scope-restrictions"></a>Bereichs Einschränkungen

Benutzer können den Suchbereich auf bestimmte Ordner Speicherorte oder Datenspeicher beschränken. Wenn Sie z. b. mehrere e-Mail-Konten verwenden und eine Abfrage entweder auf Microsoft Outlook oder Microsoft Outlook Express beschränken möchten, können Sie `System.Search.Store:mapi` oder verwenden `System.Search.Store:oe` . In der folgenden Tabelle finden Sie einige Beispiele für die Einschränkung einer Suche nach Datenspeicher.



| Einschränken der Suche nach Datenspeicher  | Schlüsselwort | Beispiel                                     |
|--------------------------------|---------|---------------------------------------------|
| Dateien                          | file    | System. search. Store: Datei                    |
| Outlook                        | MAPI    | System. search. Store: MAPI                    |
| Outlook Express                | oe      | System. search. Store: OE                      |
| Offlinedateien                  | CSC     | System. search. Store: CSC                     |
| Bestimmter Ordner auf lokalem Laufwerk | folder  | System. itemfoldernamedisplay: C: " \\ MyFolder" |



 

## <a name="additional-resources"></a>Weitere Ressourcen

-   In Windows 7 und höher kann eine Kontextmenü Option basierend darauf verfügbar sein, ob eine AQS-Bedingung erfüllt ist. Weitere Informationen finden Sie unter "erzielen von dynamischen Verhalten bei statischen Verben mithilfe der erweiterten Abfrage Syntax" unter [Erstellen von Kontextmenü Handlern](../shell/context-menu-handlers.md).
-   AQS-Abfragen können auf bestimmte Typen von Dateien beschränkt werden, die als Dateitypen bezeichnet werden. Weitere Informationen finden Sie unter [Dateitypen und Zuordnungen](../shell/fa-intro.md). Informationen zur Eigenschafts Referenz Dokumentation finden Sie unter [System. Kind](../properties/props-system-kind.md)und [System. kindtext](../properties/props-system-kindtext.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programm gesteuertes Abfragen des Indexes](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[Verwenden von SQL-und AQS-Ansätzen zum Abfragen des Indexes](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[Abfragen des Indexes mit isearchqueryhelper](-search-3x-wds-qryidx-searchqueryhelper.md)
</dt> <dt>

[Abfragen des Indexes mit dem Search-MS-Protokoll](-search-3x-wds-qryidx-searchms.md)
</dt> <dt>

[Abfragen des Indexes mit der SQL-Syntax von Windows Search](-search-sql-windowssearch-entry.md)
</dt> </dl>

 

 
