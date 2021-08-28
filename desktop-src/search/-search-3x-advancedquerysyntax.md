---
description: Erweiterte Abfragesyntax (Advanced Query Syntax, AQS) ist die Standardabfragesyntax, die von Windows Search verwendet wird, um den Index abfragt und Suchparameter zu verfeinern und zu verfeinern.
ms.assetid: 76e33903-d063-48c0-9afe-912c3daa8237
title: Programmgesteuertes Verwenden der erweiterten Abfragesyntax
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ebde3119199d84f67315c2db73343d5dffc58ad
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880697"
---
# <a name="using-advanced-query-syntax-programmatically"></a>Programmgesteuertes Verwenden der erweiterten Abfragesyntax

Erweiterte Abfragesyntax (Advanced Query Syntax, AQS) ist die Standardabfragesyntax, die von Windows Search verwendet wird, um den Index abfragt und Suchparameter zu verfeinern und zu verfeinern. AQS wird von Entwicklern verwendet, um Abfragen programmgesteuert zu erstellen (und von Benutzern, um ihre Suchparameter ein schmaler zu machen). Canonical AQS wurde in Windows 7 eingeführt und muss in Windows 7 und höher verwendet werden, um AQS-Abfragen programmgesteuert zu generieren.

Dieses Thema ist wie folgt organisiert:

-   [Informationen zur erweiterten Abfragesyntax](#about-advanced-query-syntax)
    -   [Beispiele](#examples)
    -   [Eigenschaften](#properties)
-   [Schlüsselwortnutzung in lokalen Sprachen](#keyword-use-in-local-languages)
-   [Kanonische erweiterte Abfragesyntax in Windows 7](#canonical-advanced-query-syntax-in-windows-7)
    -   [Beispiele](#examples)
    -   [Abfrageoperatoren](#query-operators)
    -   [Abfragewerte](#query-values)
-   [Bereichseinschränkungen](#scope-restrictions)
-   [Weitere Ressourcen](#additional-resources)
-   [Zugehörige Themen](#related-topics)

## <a name="about-advanced-query-syntax"></a>Informationen zur erweiterten Abfragesyntax

Eine Abfrage besteht aus grundlegenden Abfragen, die mit AND, OR und NOT verbunden sind, wie in der folgenden Beispielsyntax gezeigt:

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
> Bei AQS wird die Groß-/Kleinschreibung nicht beachtet, mit Ausnahme von AND, OR und NOT, die in Großbuchstaben geschrieben werden müssen.

 

Wenn eine Abfrage über zwei oder mehr Verwendungen von AND oder OR verfügt, werden sie von links nach rechts gebunden, unabhängig davon, ob es sich um AND oder OR handelt. Das heißt, die Abfrage "apple AND pear OR plum" wird so interpretiert, als wäre sie als "(Apple AND Pear) OR plum" geschrieben, und die Abfrage "apple OR pear AND plum" wird so interpretiert, als wäre sie als "(apple OR pear) AND plum" geschrieben. Wenn also ein Dokument das Wort plum enthält, aber weder Apple noch Pear, gibt die erste Abfrage es zurück, die zweite Abfrage jedoch nicht. Daher wird empfohlen, explizite Klammern für jede Abfrage zu verwenden, die AND und OR mischen, um Fehler oder Fehlinterpretationen zu vermeiden.

Eine einfache Abfrage sucht nach Elementen, die eine Einschränkung für eine Eigenschaft erfüllen. Der einzige erforderliche Teil einer einfachen Abfrage ist die Einschränkung oder der Suchwert. Wenn Sie keine Eigenschaft angeben, Windows alle Eigenschaften durchsucht. &lt;restr &gt; stellt die Sucheinschränkung dar.

Die folgenden Formulare für eine einfache Abfrage sind gültig:

``` syntax
<basic query> ::=
     <prop>:<basic restr>
| <restr>
```

Eine Eigenschaft wird durch ein Schlüsselwort wie author oder size oder durch einen kanonischen Eigenschaftennamen wie [System.DateModified festgelegt.](../properties/props-system-datemodified.md) Gültige Formulare für eine Eigenschaft sind:

``` syntax
<prop> ::= 
     <canonical property name>
| <property label in UI language>
```

Ein Operator gibt einen Vorgang an, z. B. < oder =. Eine Liste der gültigen Operatoren finden Sie im Abschnitt Abfrageoperatoren weiter unten in diesem Thema.

Eine grundlegende Einschränkung ist eine einfache Einschränkung für eine Eigenschaft, die ohne Klammern geschrieben werden kann:

``` syntax
<basic restr> ::=
     <value>
| <op><value>
| NOT <basic restr>
| ( <restr> )
```

Eine Einschränkung ist ein Suchwert, z. B. ein Zahlenwert oder ein Zeichenfolgenwert, optional mit einem Operator. Gültige Formulare für eine Einschränkung sind:

``` syntax
<restr> ::=
    <basic restr>
| <restr> AND <restr>
| <restr> <restr>      // Same as <restr> AND <restr>
| <restr> OR <restr>
```

Wenn Sie keinen Operator angeben, wählt Windows Search den am besten geeigneten Operator für Ihre Abfrage aus:

-   Für eine Zeichenfolgeneigenschaft wird der OPERATOR COP \_ WORD \_ STARTSWITH $< angenommen.
-   Für alle anderen Eigenschaften wird der OPERATOR COP \_ EQUAL = angenommen.

Für die programmgesteuerte Verwendung von AQS wird empfohlen, immer über einen expliziten Operator zu verfügen. Das gültige Formular zum Durchsuchen eines einfachen Wert- oder Wertbereichs lautet wie folgt:

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

Eine Abfrage, die nach einem Dokument sucht, das die phase "last quarter" enthält, die von Theresa oder Lee erstellt wurde und im Ordner MyDocs gespeichert wurde, kombiniert drei grundlegende Abfragen wie folgt:

``` syntax
"last quarter" author:(theresa OR lee) folder:MyDocs
```

Die drei grundlegenden Abfragen sind:

-   "Letztes Quartal"
-   author:(theresa OR lee)
-   folder:MyDocs

Eine grundlegende Abfrage, die kanonische Syntax verwendet, ist:

``` syntax
System.Size:>1kb
```

### <a name="properties"></a>Eigenschaften

Auf Eigenschaften wird durch ein Schlüsselwort verwiesen, bei dem es sich um einen kanonischen Eigenschaftsnamen in Windows 7 und höher handelt. AQS in der Windows-Benutzeroberfläche kann die Bezeichnung anstelle des kanonischen Eigenschaftennamens verwenden, z. B. author anstelle von [System.Author.](../properties/props-system-author.md) In Windows Vista und früher war es möglich, englische Bezeichnungen unabhängig von der Benutzeroberflächensprache zu verwenden. In Windows 7 und höher erkennt Windows Search Schlüsselwörter nur in der aktuellen Standardsprache der Benutzeroberfläche.

### <a name="support-for-custom-properties"></a>Unterstützung für benutzerdefinierte Eigenschaften

In Windows Vista und früher waren benutzerdefinierte Eigenschaften in AQS nicht verfügbar. In Windows 7 und höher funktioniert AQS mit benutzerdefinierten Eigenschaften, die beim Eigenschaftensystem registriert sind. Weitere Informationen zum Erstellen benutzerdefinierter Eigenschaften finden Sie unter [Eigenschaftensystem](../properties/building-property-handlers.md).

### <a name="datetime-properties-in-windows-8"></a>DateTime-Eigenschaften in Windows 8

Ab Windows 8 unterstützen DateTime-Eigenschaften (z. B. [System.DateModified)](../properties/props-system-datemodified.md)das kanonische Datums- und Uhrzeitformat, das von [ISO-8601](https://www.w3.org/TR/NOTE-datetime)angegeben wird, optional einschließlich der UTC-Zeitzone.

-   **Windows 8 und früher, Datum/Uhrzeit ohne UTC-Zeitzone:** *YYYY* - *MM* - *DDThh*:*mm*:*ss*

    Dieses Format gibt eine lokale Zeit an, unabhängig vom Benutzer- oder System-Locale.

-   **Windows 8, Datum/Uhrzeit mit UTC-Zeitzone:** *YYYY* - *MM* - *DDThh*:*mm*:*ssTZD*

    Dieses Format gibt eine Uhrzeit in der angegebenen UTC-Zeitzone an.

## <a name="keyword-use-in-local-languages"></a>Schlüsselwortnutzung in lokalen Sprachen

In Windows 7 und höher funktionieren mnemonische Schlüsselwörter nur in der Systemsprache, z. B. deutsche Schlüsselwörter nur unter einem deutschen Betriebssystem und englische Schlüsselwörter nur unter einem englischen Betriebssystem. [System.Author](../properties/props-system-author.md) ist ein kanonisches Schlüsselwort, und der mnemonische Wert für die System.Author-Eigenschaft ist beispielsweise Author. Die Einführung kanonischer Schlüsselwörter gleicht die Tatsache aus, dass englische mnemonische Schlüsselwörter nicht mehr auf allen Betriebssystemen unabhängig von der Sprache allgemein erkannt werden, wie dies in Windows Vista und früher der Fall war.

> [!Note]  
> In Windows 7 und höher erkennt Windows Search Schlüsselwörter nur in der aktuellen Standardsprache und nicht in Englisch, es sei denn, Englisch ist die aktuelle Standardsprache. Es wird empfohlen, dass Entwickler immer kanonische Syntax verwenden, damit ihre Anwendung keine Sprachprobleme mit Schlüsselwörtern hat.

 

## <a name="canonical-advanced-query-syntax-in-windows-7"></a>Kanonische erweiterte Abfragesyntax in Windows 7

Kanonische Syntax wurde für Schlüsselwörter in Windows 7 eingeführt. Ein Beispiel für eine Abfrage mit einer kanonischen Eigenschaft ist `System.Message.FromAddress:=me@microsoft.com` . Beim Codieren von Abfragen in Anwendungen, die Windows 7 und höher ausgeführt werden, müssen Sie kanonische Syntax verwenden, um AQS-Abfragen programmgesteuert zu generieren. Wenn Sie keine kanonische Syntax verwenden und Ihre Anwendung in einem Anderen als der Sprache im Anwendungscode in einem Anderen als der Sprache der Benutzeroberfläche bereitgestellt wird, werden Ihre Abfragen nicht ordnungsgemäß interpretiert.

Die Konventionen für kanonische Schlüsselwortsyntax lauten wie folgt:

-   Die kanonische Syntax für eine Eigenschaft ist ihr kanonischer Name, z. `System.Photo.LightSource` B. . Bei kanonischen Namen wird die Kleinschreibung nicht beachtet.
-   Die kanonische Syntax für die booleschen Operatoren besteht aus den Schlüsselwörtern AND, OR und NOT in Großbuchstaben.
-   Die Operatoren <, >, =usw. sind nicht lokalisiert und daher auch Teil der kanonischen Syntax.
-   Wenn eine Eigenschaft über aufzählte Werte oder Bereiche mit den Namen N₁ bis Nk verfügt, ist die kanonische Syntax für den I-Wert oder -Bereich der kanonische Name für P, gefolgt vom Zeichen , gefolgt von `P`  \# N<sub>I,</sub>wie im folgenden Beispiel veranschaulicht:
    -   `System.Photo.LightSource#Daylight`, `System.Photo.LightSource#StandardA` usw.
-   Für einen definierten semantischen Typ T mit Werten oder Bereichen mit den Namen N₁ bis Nk ist die kanonische Syntax für den I. Wert oder Bereich der kanonische Name für T, gefolgt von dem Zeichen , gefolgt von \# N<sub>I,</sub>wie im folgenden Beispiel veranschaulicht:
    -   `System.Devices.LaunchDeviceStageFromExplorer:=System.StructuredQueryType.Boolean#True`
-   Bei Literalwerten wie Wörtern oder Ausdrücken ist die kanonische Syntax mit der regulären Syntax identisch. Beispiele für Abfragen mit Literalwerten in kanonischer Syntax sind:
    -   `System.Author:sanjay`
    -   `System.Keywords:"Animal"`
    -   `System.FileCount:>100`

> [!Note]  
> Es gibt keine kanonische Syntax für Zahlen in Windows 7 und höher. Da Gleitkommaformate je nach Gebiet variieren, wird die Verwendung einer kanonischen Abfrage, die eine Gleitkommakonstu umfasst, nicht unterstützt. Ganzzahlige Konstanten können dagegen nur mit Ziffern geschrieben werden (keine Trennzeichen für Tausende) und können sicher in kanonischen Abfragen in Windows 7 und höher verwendet werden.

 

### <a name="examples"></a>Beispiele

Die folgende Tabelle enthält einige Beispiele für kanonische Eigenschaften und die Syntax für deren Verwendung.



| Typ der kanonischen Eigenschaft | Beispiel                                                                                     | Syntax                                                                                                                                                                                                                                                  |
|----------------------------|---------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Zeichenfolgenwert               | [System.Author](../properties/props-system-author.md)<br/>    | Der Zeichenfolgenwert wird in der author-Eigenschaft gesucht: <br/>`System.Author:Jacobs`                                                                                                                                                              |
| Enumerationsbereich          | [System.Priority](../properties/props-system-priority.md)             | Die priority-Eigenschaft kann einen numerischen Wertbereich haben:<br/>`System.Priority:System.Priority#High`                                                                                                                                                |
| Boolean                    | [System.IsDeleted](../properties/props-system-isdeleted.md)<br/> | Boolesche Werte können mit jeder booleschen Eigenschaft verwendet werden:<br/>`System.IsDeleted:System.StructuredQueryType.Boolean#True`Und `System.IsDeleted:System.StructuredQueryType.Boolean#False`                                                             |
| Numerisch                  | [System.Size](../properties/props-system-size.md)<br/>      | Es ist nicht möglich, eine kanonische Abfrage, die eine Gleitkommakonstante umfasst, sicher zu schreiben, da Gleitkommaformate zwischen Gebietsschemas variieren. Ganze Zahlen müssen ohne Trennzeichen für Tausende geschrieben werden. Beispiel:<br/>`System.Size:<12345` |



 

Weitere Informationen zu kanonischen Eigenschaften und zum Eigenschaftensystem im Allgemeinen finden Sie unter [Systemeigenschaften.](../properties/props.md) Alternativ können Sie auch auf die öffentlichen Headerdateien verweisen.

### <a name="query-operators"></a>Abfrageoperatoren

Wenn die Eigenschaft p mehrere Werte für ein Element enthält, gibt eine AQS-Abfrage für p: &lt; restr &gt; das Element zurück, wenn &lt; restr für mindestens einen der &gt; -Werte **true** ist. ( &lt; Restr &gt; stellt eine Einschränkung dar.)

Die in der folgenden Tabelle aufgeführte Syntax besteht aus einem Operator, einem Operatorsymbol, einem Beispiel und einer Beispielbeschreibung. Der Operator und das Symbol können in jeder Sprache verwendet und in jeder Abfrage enthalten sein. Verwenden Sie nicht die \_ COP IMPLICIT- oder COP \_ APPLICATION \_ SPECIFIC-Operatoren. Einige der Operatoren verfügen über austauschbare Symbole.



<table>
<colgroup>
<col  />
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Operator</th>
<th>Symbol</th>
<th>Beispiel</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>COP_EQUAL</td>
<td>=<br/></td>
<td>System.FileExtension:= &quot;.txt&quot;<br/></td>
<td>Der Wert ist die Zeichenfolge &quot; <em>.txt</em> &quot; .<br/></td>
</tr>
<tr class="even">
<td>COP_NOTEQUAL</td>
<td>≠<br/> -<br/> &lt;&gt;<br/> NICHT<br/> - -<br/></td>
<td>System.Kind:≠picture<br/> System.Photo.DateTaken:-[]¹<br/> System.Kind: &lt; &gt; picture<br/> System.Kind:NOT-Bild<br/> System.Kind:- -picture<br/></td>
<td>Die <a href="/windows/desktop/properties/props-system-kind">System.Kind-Eigenschaft</a> ist kein Bild.<br/> Die <a href="/windows/desktop/properties/props-system-photo-datetaken">System.Photo.DateTaken-Eigenschaft</a> verfügt über einen -Wert.<br/> Die <a href="/windows/desktop/properties/props-system-kind">System.Kind-Eigenschaft</a> ist kein Bild. <br/> Die <a href="/windows/desktop/properties/props-system-kind">System.Kind-Eigenschaft</a> ist kein Bild. <br/> Doppelte NOT-Operatoren, die auf dieselbe Eigenschaft angewendet werden, brechen nicht ab. Daher entspricht System.Kind:- -picture System.Kind:-picture und System.Kind:NOT picture.<br/></td>
</tr>
<tr class="odd">
<td>COP_LESSTHAN</td>
<td>&lt;<br/></td>
<td>System.Size: &lt; 1 KB<br/></td>
<td>Dieser Wert ist kleiner als <em>1 KB.</em><br/></td>
</tr>
<tr class="even">
<td>COP_GREATERTHAN</td>
<td>&gt;<br/></td>
<td>System.ItemDate: &gt; System.StructuredQueryType.DateTime#Today<br/></td>
<td>Dieser Wert ist größer als <em>heute.</em><br/></td>
</tr>
<tr class="odd">
<td>COP_LESSTHANOREQUAL</td>
<td>&lt;=<br/> ≤<br/></td>
<td>System.Size: &lt; =1 KB<br/></td>
<td>Dieser Wert ist kleiner oder gleich <em>1 KB.</em><br/></td>
</tr>
<tr class="even">
<td>COP_GREATERTHANOREQUAL</td>
<td>&gt;=<br/> ≥<br/></td>
<td>System.Size: &gt; =1 KB<br/></td>
<td>Dieser Wert ist gleich oder größer als <em>1 KB.</em><br/></td>
</tr>
<tr class="odd">
<td>COP_VALUE_STARTSWITH</td>
<td>~&lt;<br/></td>
<td>System.FileName:~ &lt; &quot; C++-Einführung&quot;<br/></td>
<td>Sucht Elemente, bei denen der Dateiname mit den Zeichen &quot; <em>C++-Primer</em> &quot; beginnt.<br/></td>
</tr>
<tr class="even">
<td>COP_VALUE_ENDSWITH</td>
<td>~&gt;<br/></td>
<td>System.Photo.CameraModel:~ &gt; nicht<br/></td>
<td>Sucht Nach Elementen, bei denen der Eigenschaftswert mit den Zeichen <em>endet,</em>die nicht sind.<br/></td>
</tr>
<tr class="odd">
<td>COP_VALUE_CONTAINS</td>
<td>~=<br/> ~~<br/></td>
<td>System.Subject.~=round <br/> System.Search.Autosummary:~~round<br/></td>
<td>Sucht eine Nachricht, die diese Zeichenfolge im Betreff enthält und &quot; z. B.<em>g-Rundungsregeln</em> &quot; entspricht.<br/> Sucht alle Elemente mit einem Autoummary, das die Zeichen <em>rundt.</em><br/></td>
</tr>
<tr class="even">
<td>COP_VALUE_NOTCONTAINS</td>
<td>~!<br/></td>
<td>System.Author:~! &quot; Sanjay&quot;<br/></td>
<td>Sucht Nach Autoren, die nicht über die Zeichensequenz &quot; <em>sjay</em> &quot; verfügen.<br/></td>
</tr>
<tr class="odd">
<td>COP_DOSWILDCARDS</td>
<td>~ <br/></td>
<td>System.FileName:~ &quot; Mic?osoft W*d&quot;<br/></td>
<td>Sucht Dateien, bei denen der Dateiname mit <em>Mic</em>beginnt, gefolgt von einem Zeichen, gefolgt von <em>osoft w,</em>gefolgt von allen Zeichen, die mit <em>d</em>enden. <br/> Mit dem Zeichen „?“ und *-Zeichen werden nicht wörtlich interpretiert und funktionieren wie Platzhalterzeichen im DOS-Stil:<br/>
<ul>
<li>? entspricht einem beliebigen Zeichen.</li>
<li>* entspricht 0 (null) oder mehr beliebigen Zeichen.</li>
</ul></td>
</tr>
<tr class="even">
<td>COP_WORD_EQUAL</td>
<td>$=<br/> $$<br/></td>
<td>System.StructuredQuery.Virtual.From:$= &quot; S !"&quot;<br/></td>
<td>Für Windows 7 und höher. Sucht in allen From-Eigenschaften nach dem Ausdruck &quot; <em>SfloyEss.</em> &quot; Auf das Wort <em>Sjay</em> muss das Wort <em>Solls</em>folgen.<br/></td>
</tr>
<tr class="odd">
<td>COP_WORD_STARTSWITH</td>
<td>$<<br/></td>
<td>System.Author:$<&quot;San&quot; System.Filename:$<&quot;Micro Exe&quot;<br/></td>
<td>Für Windows 7 und höher. Sucht nach jedem Element, bei dem Author ein Wort enthält, das mit den Zeichen &quot; <em>San</em> &quot; beginnt.<br/> Sucht eine beliebige Datei, in der der Dateiname ein Wort enthält, das mit <em>micro</em>beginnt, gefolgt von einem Wort, das mit <em>exe</em>beginnt.<br/></td>
</tr>
</tbody>
</table>



 

¹ Leere eckige Klammern ( \[ \] ) geben "kein Wert" an.

Für Zeichenfolgeneigenschaften ist der Standardvorgang entweder COP \_ WORD STARTS WITH oder COP WORD \_ \_ \_ \_ EQUAL.

### <a name="query-values"></a>Abfragewerte

In der folgenden Tabelle sind nützliche Beispiele dafür aufgeführt, wie Abfragewerte eingeschränkt werden können.



<table>
<colgroup>
<col  />
<col  />
<col  />
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
<td>Eine beliebige Zeichenfolge, nach der gesucht werden kann. Die Zeichenfolge darf keine Leerzeichen oder Zeichenkombinationen enthalten, die Teil der Syntax sind. In diesem Beispiel wird nach einem Wort gesucht, das mit <em>auto</em>beginnt.<br/></td>
</tr>
<tr class="even">
<td>Zeichenfolge in Anführungszeichen &quot;&quot;</td>
<td>&quot;Schlussfolgerungen: gültig &quot; &quot; Das blaue &quot; &quot; &quot; &quot; Team&quot;<br/></td>
<td>Eine beliebige Sequenz von Zeichen. Die Zeichenfolge wird nicht als Teil der Syntax interpretiert.<br/> Anführungszeichen können in eine Abfrage eingefügt werden, wenn sie verdoppelt werden. In diesem Beispiel wird nach <em>Das &quot; blaue &quot; Team</em>gesucht.<br/></td>
</tr>
<tr class="odd">
<td>Integer</td>
<td>5678<br/></td>
<td>Verwenden Sie nur Ziffern für ganze Zahlen. Verwenden Sie keine Trennzeichen für Tausende.<br/></td>
</tr>
<tr class="even">
<td>Gleitkommazahl</td>
<td>5678.1234<br/></td>
<td>Da Gleitkommaformate zwischen Gebietsschemas variieren, kann eine kanonische Abfrage keine Gleitkommakonstante verwenden. Die Verwendung kanonischer Syntax mit Gleitkommazahlen ist nicht lokalisierungssicher. <br/></td>
</tr>
<tr class="odd">
<td>Boolescher <strong>Wert true</strong> / <strong>false</strong></td>
<td>System.IsRead:=System.StructuredQueryType.Boolean#True<br/> System.IsEncrypted:-System.StructuredQueryType.Boolean#False<br/></td>
<td>Der <strong>boolesche</strong> TRUE-Wert.<br/> Der <strong></strong> boolesche FALSE-Wert.<br/></td>
</tr>
<tr class="even">
<td>[]</td>
<td>System.Keywords:=[]<br/></td>
<td>Leere eckige Klammern geben an, dass kein Wert vorhanden ist. In diesem Beispiel werden alle Elemente gefunden, die nicht markiert wurden. <br/></td>
</tr>
<tr class="odd">
<td>Absolute Datumsangaben</td>
<td>System.ItemDate:26.1.2010<br/> SystemDateModified 15.10.2002 19:00 Uhr<br/></td>
<td>Sucht Elemente mit dem Datum 26. Januar 2010.<br/> Sucht elemente, die am 15. Oktober 2002 zwischen den Stunden 19:00:00 und 19:00:59 geändert wurden. <br/>
<blockquote>
[!Note]<br />
Da Datumsformate (z. B. Gleitkommaformate) zwischen Gebietsschemas variieren, wird die Verwendung kanonischer Syntax mit absoluten Datumsangaben nicht unterstützt und ist nicht lokalisierungssicher.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>Relative Datumsangaben</td>
<td>System.ItemDate:System.StructuredQueryType.DateTime#Today<br/> System.DateAcquired:System.StructuredQueryType.DateTime#NextMonth<br/> System.Message.DateReceived:System.StructuredQueryType.DateTime#LastYear<br/></td>
<td>Sucht Nach Elementen mit dem heutigen Datum.<br/> Sucht Elemente mit einem Datum im nächsten Monat.<br/> Sucht Elemente mit einem Datum im letzten Jahr.<br/>
<blockquote>
[!Note]<br />
Zusätzlich zur Suche nach bestimmten Datums- und Datumsbereichen erkennt AQS relative Datumswerte (z. B. <em>heute</em>, <em>morgen</em>, <em>nextweek</em>, <em>nextmonth</em>) und day (z. B. <em>Dienstag</em> oder <em>Montag). Mittwoch</em>und Monat (<em>Februar</em>).
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>..</td>
<td>System.ItemDate:11/05/04...11/10/04 System.Size:5kb.. 10 KB<br/></td>
<td>Doppelte Zeiträume geben einen Wertbereich an. Sucht Elemente mit einem Datum zwischen dem 04.05.11 und dem 10.11.04 einschließlich.<br/> Sucht Elemente zwischen 5 und 10 KB.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="scope-restrictions"></a>Bereichseinschränkungen

Benutzer können den Umfang ihrer Suchvorgänge auf bestimmte Ordner oder Datenspeicher beschränken. Wenn Sie beispielsweise mehrere E-Mail-Konten verwenden und eine Abfrage entweder auf Microsoft Outlook oder Microsoft Outlook Express beschränken möchten, können Sie `System.Search.Store:mapi` `System.Search.Store:oe` oder verwenden. Die folgende Tabelle zeigt einige Beispiele für die Einschränkung einer Suche nach Datenspeicher.



| Einschränken der Suche nach Datenspeicher  | Stichwort | Beispiel                                     |
|--------------------------------|---------|---------------------------------------------|
| Dateien                          | file    | System.Search. Store:file                    |
| Outlook                        | Mapi    | System.Search. Store:mapi                    |
| Outlook Express                | oe      | System.Search. Store:oe                      |
| Offlinedateien                  | Csc     | System.Search. Store:csc                     |
| Bestimmter Ordner auf dem lokalen Laufwerk | folder  | System.ItemFolderNameDisplay:C:" \\ MyFolder" |



 

## <a name="additional-resources"></a>Zusätzliche Ressourcen

-   In Windows 7 und höher kann eine Kontextmenüoption abhängig davon verfügbar sein, ob eine AQS-Bedingung erfüllt ist. Weitere Informationen finden Sie unter "Getting Dynamic Behavior for Static Verbs by Using Advanced Query Syntax" (Abrufen von dynamischem Verhalten für statische Verben mithilfe der erweiterten Abfragesyntax) unter [Erstellen von Kontextmenühandlern.](../shell/context-menu-handlers.md)
-   AQS-Abfragen können auf bestimmte Dateitypen beschränkt werden, die als Dateitypen bezeichnet werden. Weitere Informationen finden Sie unter [Dateitypen und Zuordnungen.](../shell/fa-intro.md) Eine Referenzdokumentation zu Eigenschaften finden Sie unter [System.Kind](../properties/props-system-kind.md)und [System.KindText](../properties/props-system-kindtext.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programm gesteuertes Abfragen des Indexes](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[Verwenden von SQL und AQS-Ansätzen zum Abfragen des Index](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[Abfragen des Index mit ISearchQueryHelper](-search-3x-wds-qryidx-searchqueryhelper.md)
</dt> <dt>

[Abfragen des Indexes mit dem search-ms-Protokoll](-search-3x-wds-qryidx-searchms.md)
</dt> <dt>

[Abfragen des Index mit Windows Search-SQL syntax](-search-sql-windowssearch-entry.md)
</dt> </dl>

 

 
