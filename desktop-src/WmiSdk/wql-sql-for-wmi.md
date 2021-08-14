---
description: Die WMI Query Language (WQL) ist eine Teilmenge der American National Standards Institute strukturierte Abfragesprache (ANSI SQL)&8212; mit geringfügigen semantischen \# Änderungen. In der folgenden Tabelle sind die WQL-Schlüsselwörter aufgeführt.
ms.assetid: 72a7ec04-9af3-41ae-9189-6e1d46803fa9
ms.tgt_platform: multiple
title: WQL (WMI SQL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c9a1a3b0db3f383bd8ba44aeb1e433b5aab02b4e9b4773ea221e1a0254ae037
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117738819"
---
# <a name="wql-sql-for-wmi"></a>WQL (WMI SQL)

Die WMI Query Language (WQL) ist eine Teilmenge der American National Standards Institute strukturierte Abfragesprache (ANSI SQL) mit geringfügigen semantischen Änderungen. In der folgenden Tabelle sind die WQL-Schlüsselwörter aufgeführt.



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
<td>Kombiniert zwei boolesche Ausdrücke und gibt <strong>TRUE zurück,</strong> wenn beide Ausdrücke <strong>TRUE sind.</strong><br/></td>
</tr>
<tr class="even">
<td><a href="associators-of-statement.md">ASSOZIATOREN VON</a></td>
<td>Ruft alle Instanzen ab, die einer Quellinstanz zugeordnet sind.<br/> Verwenden Sie diese Anweisung mit Schemaabfragen und Datenabfragen.<br/></td>
</tr>
<tr class="odd">
<td><a href="--class-identifier.md">__CLASS</a></td>
<td>Verweist auf die Klasse des -Objekts in einer Abfrage.<br/></td>
</tr>
<tr class="even">
<td>FROM<br/></td>
<td>Gibt die Klasse an, die die in einer SELECT-Anweisung aufgeführten Eigenschaften enthält. Windows Die Verwaltungsinstrumentation (WMI) unterstützt Datenabfragen von nur einer Klasse gleichzeitig.<br/></td>
</tr>
<tr class="odd">
<td><a href="group-clause.md">GROUP-Klausel</a></td>
<td>Bewirkt, dass WMI eine Benachrichtigung generiert, die eine Gruppe von Ereignissen repräsentiert.<br/> Verwenden Sie diese Klausel mit Ereignisabfragen.<br/></td>
</tr>
<tr class="even">
<td><a href="having-clause.md">HAVING</a></td>
<td>Filtert die Ereignisse, die während des Gruppierungsintervalls empfangen werden, das in der <a href="within-clause.md">WITHIN-Klausel angegeben ist.</a><br/></td>
</tr>
<tr class="odd">
<td><a href="wql-operators.md">IS</a></td>
<td>Vergleichsoperator, der mit NOT und <strong>NULL verwendet wird.</strong> Die Syntax für diese Anweisung ist die folgende:<br/> IS [NOT] <strong>NULL</strong><br/> (wobei NOT optional ist)<br/></td>
</tr>
<tr class="even">
<td><a href="wql-operators.md">ISA</a></td>
<td>Operator, der eine Abfrage auf die Unterklassen einer angegebenen Klasse an wendet. Weitere Informationen finden Sie unter <a href="isa-operator-for-event-queries.md">ISA-Operator für</a>Ereignisabfragen, <a href="isa-operator-for-data-queries.md">ISA-Operator für Datenabfragen</a>und <a href="isa-operator-for-schema-queries.md">ISA-Operator für Schemaabfragen.</a><br/></td>
</tr>
<tr class="odd">
<td>KEYSONLY<br/></td>
<td>Wird in <a href="references-of-statement.md">REFERENCES OF-</a> und <a href="associators-of-statement.md">ASSOCIATORS OF-Abfragen</a> verwendet, um sicherzustellen, dass die resultierenden Instanzen nur mit den Schlüsseln der -Instanzen aufgefüllt werden, wodurch der Aufwand für den Aufruf reduziert wird.<br/></td>
</tr>
<tr class="even">
<td><a href="wql-operators.md">LIKE</a></td>
<td>Operator, der bestimmt, ob eine angegebene Zeichenfolge einem angegebenen Muster entspricht.<br/></td>
</tr>
<tr class="odd">
<td>NICHT<br/></td>
<td>Vergleichsoperator, der in einer WQL SELECT-Abfrage verwendet, z. B.:<br/>
<pre data-space="preserve"><code>SELECT * FROM meta_class WHERE NOT __class < &quot;Win32&quot; AND NOT __this ISA &quot;Win32_Account&quot;</code></pre></td>
</tr>
<tr class="even">
<td><strong>NULL</strong></td>
<td>Gibt an, dass einem Objekt kein explizit zugewiesener Wert zugewiesen ist. <strong>NULL</strong> entspricht nicht null (0) oder leer.<br/></td>
</tr>
<tr class="odd">
<td>oder<br/></td>
<td>Kombiniert zwei Bedingungen.<br/> Wenn mehrere logische Operatoren in einer -Anweisung verwendet werden, werden die OR-Operatoren nach den AND-Operatoren ausgewertet.<br/></td>
</tr>
<tr class="even">
<td><a href="references-of-statement.md">VERWEISE VON</a></td>
<td>Ruft alle Zuordnungsinstanzen ab, die auf eine bestimmte Quellinstanz verweisen. Verwenden Sie diese Anweisung mit Schema- und Datenabfragen. Die <a href="references-of-statement.md">REFERENCES OF-Anweisung</a> ähnelt der <a href="associators-of-statement.md">ASSOCIATORS OF-Anweisung.</a> Endpunktinstanzen werden jedoch nicht abgerufen. Sie ruft die Zuordnungsinstanzen ab.<br/></td>
</tr>
<tr class="odd">
<td>SELECT<br/></td>
<td>Gibt die Eigenschaften an, die in einer Abfrage verwendet werden.<br/> Weitere Informationen finden Sie unter <a href="select-statement-for-data-queries.md">SELECT-Anweisung für Datenabfragen,</a> <a href="select-statement-for-event-queries.md">SELECT-Anweisung für Ereignisabfragen</a>oder <a href="select-statement-for-schema-queries.md">SELECT-Anweisung für Schemaabfragen.</a><br/></td>
</tr>
<tr class="even">
<td><strong>TRUE</strong></td>
<td>Boolescher Operator, der zu -1 (minus 1) ausgewertet wird.<br/></td>
</tr>
<tr class="odd">
<td><a href="where-clause.md">WHERE</a></td>
<td>Eingeengt den Bereich einer Daten-, Ereignis- oder Schemaabfrage.<br/></td>
</tr>
<tr class="even">
<td><a href="within-clause.md">WITHIN</a></td>
<td>Gibt ein Abruf- oder Gruppierungsintervall an.<br/> Verwenden Sie diese Klausel mit Ereignisabfragen.<br/></td>
</tr>
<tr class="odd">
<td>FALSE<br/></td>
<td>Boolescher Operator, der zu 0 (null) ausgewertet wird.</td>
</tr>
</tbody>
</table>



 

> [!Note]  
> Die Verwendung eines WQL-Schlüsselworts als Objektname kann zu einer Abfrage führen, die auch dann nicht analysiert werden kann, wenn die Abfrage ohne Fehler kompiliert wird.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WQL-Operatoren](wql-operators.md)
</dt> <dt>

[Von WQL unterstützte Datumsformate](wql-supported-date-formats.md)
</dt> <dt>

[Von WQL unterstützte Zeitformate](wql-supported-time-formats.md)
</dt> </dl>

 

 




