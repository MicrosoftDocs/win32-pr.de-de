---
description: Der WMI Query Language (WQL) ist eine Teilmenge der American National Standards Institute Structured Query Language (ANSI SQL) &\# 8212; mit geringfügigen Semantik Änderungen. In der folgenden Tabelle werden die WQL-Schlüsselwörter aufgelistet.
ms.assetid: 72a7ec04-9af3-41ae-9189-6e1d46803fa9
ms.tgt_platform: multiple
title: WQL (WMI SQL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87498b6e8e37ab900e21eedf2c15d5cdba9f9bd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215438"
---
# <a name="wql-sql-for-wmi"></a>WQL (WMI SQL)

Der WMI Query Language (WQL) ist eine Teilmenge der American National Standards Institute Structured Query Language (ANSI SQL) mit geringfügigen Semantik Änderungen. In der folgenden Tabelle werden die WQL-Schlüsselwörter aufgelistet.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>WQL-Schlüsselwort</th>
<th>Bedeutung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>AND<br/></td>
<td>Kombiniert zwei boolesche Ausdrücke und gibt <strong>true</strong> zurück, wenn beide Ausdrücke <strong>true</strong>sind.<br/></td>
</tr>
<tr class="even">
<td><a href="associators-of-statement.md">assoziatoren von</a></td>
<td>Ruft alle-Instanzen ab, die einer-Quell Instanz zugeordnet sind.<br/> Verwenden Sie diese Anweisung mit Schema Abfragen und Daten Abfragen.<br/></td>
</tr>
<tr class="odd">
<td><a href="--class-identifier.md">__CLASS</a></td>
<td>Verweist auf die-Klasse des-Objekts in einer Abfrage.<br/></td>
</tr>
<tr class="even">
<td>FROM<br/></td>
<td>Gibt die Klasse an, die die in einer SELECT-Anweisung aufgeführten Eigenschaften enthält. Windows-Verwaltungsinstrumentation (WMI) unterstützt Daten Abfragen von nur einer Klasse gleichzeitig.<br/></td>
</tr>
<tr class="odd">
<td><a href="group-clause.md">Group-Klausel</a></td>
<td>Bewirkt, dass WMI eine Benachrichtigung generiert, um eine Gruppe von Ereignissen darzustellen.<br/> Verwenden Sie diese Klausel mit Ereignis Abfragen.<br/></td>
</tr>
<tr class="even">
<td><a href="having-clause.md">HAVING</a></td>
<td>Filtert die Ereignisse, die während des in der <a href="within-clause.md">within-Klausel</a>angegebenen Gruppierungs Intervalls empfangen werden.<br/></td>
</tr>
<tr class="odd">
<td><a href="wql-operators.md">IS</a></td>
<td>Vergleichs Operator, der mit Not und <strong>null</strong>verwendet wird. Die Syntax für diese Anweisung lautet wie folgt:<br/> ist [NOT] <strong>null</strong><br/> (wobei nicht optional ist)<br/></td>
</tr>
<tr class="even">
<td><a href="wql-operators.md">ISA</a></td>
<td>Operator, der eine Abfrage auf die Unterklassen einer angegebenen Klasse anwendet. Weitere Informationen finden Sie unter <a href="isa-operator-for-event-queries.md">ISA-Operator für Ereignis Abfragen</a>, <a href="isa-operator-for-data-queries.md">ISA-Operator für Daten Abfragen</a>und <a href="isa-operator-for-schema-queries.md">ISA-Operator für Schema Abfragen</a>.<br/></td>
</tr>
<tr class="odd">
<td>Keysonly<br/></td>
<td>Wird in <a href="references-of-statement.md">verweisen von</a> und <a href="associators-of-statement.md">assoziatoren von</a> Abfragen verwendet, um sicherzustellen, dass die resultierenden Instanzen nur mit den Schlüsseln der-Instanzen aufgefüllt werden, wodurch der Aufwand des Aufrufes verringert wird.<br/></td>
</tr>
<tr class="even">
<td><a href="wql-operators.md">LIKE</a></td>
<td>Operator, der bestimmt, ob eine angegebene Zeichenfolge mit einem angegebenen Muster übereinstimmt.<br/></td>
</tr>
<tr class="odd">
<td>NICHT<br/></td>
<td>Vergleichs Operator, der in einer WQL SELECT-Abfrage verwendet, z. b.:<br/>
<pre data-space="preserve"><code>SELECT * FROM meta_class WHERE NOT __class < &quot;Win32&quot; AND NOT __this ISA &quot;Win32_Account&quot;</code></pre></td>
</tr>
<tr class="even">
<td><strong>NULL</strong></td>
<td>Gibt an, dass ein Objekt über keinen explizit zugewiesenen Wert verfügt. <strong>Null</strong> entspricht nicht 0 (null) oder leer.<br/></td>
</tr>
<tr class="odd">
<td>oder<br/></td>
<td>Kombiniert zwei Bedingungen.<br/> Wenn mehr als ein logischer Operator in einer-Anweisung verwendet wird, werden die-oder-Operatoren nach den Operatoren und ausgewertet.<br/></td>
</tr>
<tr class="even">
<td><a href="references-of-statement.md">Verweise auf</a></td>
<td>Ruft alle Assoziations Instanzen ab, die auf eine bestimmte Quell Instanz verweisen. Verwenden Sie diese Anweisung mit Schema-und Daten Abfragen. Die <a href="references-of-statement.md">References of</a> -Anweisung ähnelt den <a href="associators-of-statement.md">assoziatoren der</a> -Anweisung. Endpunkt Instanzen werden jedoch nicht abgerufen. die Zuordnungs Instanzen werden abgerufen.<br/></td>
</tr>
<tr class="odd">
<td>SELECT<br/></td>
<td>Gibt die Eigenschaften an, die in einer Abfrage verwendet werden.<br/> Weitere Informationen finden Sie unter <a href="select-statement-for-data-queries.md">SELECT-Anweisung für Daten Abfragen</a>, <a href="select-statement-for-event-queries.md">SELECT-Anweisung für Ereignis Abfragen</a>oder <a href="select-statement-for-schema-queries.md">SELECT-Anweisung für Schema Abfragen</a>.<br/></td>
</tr>
<tr class="even">
<td><strong>TRUE</strong></td>
<td>Boolescher Operator, der ergibt-1 (minus 1).<br/></td>
</tr>
<tr class="odd">
<td><a href="where-clause.md">WHERE</a></td>
<td>Schränkt den Gültigkeitsbereich einer Daten-, Ereignis-oder Schema Abfrage ein.<br/></td>
</tr>
<tr class="even">
<td><a href="within-clause.md">WITHIN</a></td>
<td>Gibt ein Abruf-oder Gruppierungs Intervall an.<br/> Verwenden Sie diese Klausel mit Ereignis Abfragen.<br/></td>
</tr>
<tr class="odd">
<td>false<br/></td>
<td>Boolescher Operator, der als 0 (null) ausgewertet wird.</td>
</tr>
</tbody>
</table>



 

> [!Note]  
> Wenn Sie ein WQL-Schlüsselwort als Objektnamen verwenden, kann dies zu einer Abfrage führen, die auch dann nicht analysiert werden kann, wenn die Abfrage ohne Fehler kompiliert wird.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WQL-Operatoren](wql-operators.md)
</dt> <dt>

[WQL-unterstützte Datumsformate](wql-supported-date-formats.md)
</dt> <dt>

[Von WQL unterstützte Zeitformate](wql-supported-time-formats.md)
</dt> </dl>

 

 




