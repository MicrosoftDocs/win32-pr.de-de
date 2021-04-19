---
description: Weitere Informationen finden Sie in der columndefgrbit-Enumeration.
title: Columndefgrbit-Enumeration
TOCTitle: ColumndefGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.ColumndefGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columndefgrbit(v=EXCHG.10)
ms:contentKeyID: 39513005
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnAutoincrement
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.TTKey
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.None
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnUserDefinedDefault
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnMaybeNull
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnMultiValued
- Microsoft.Isam.Esent.Interop.ColumndefGrbit
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnFixed
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnTagged
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnUnversioned
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnEscrowUpdate
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnNotNULL
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnVersion
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.TTDescending
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnNotNULL
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnAutoincrement
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnUnversioned
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnMaybeNull
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnTagged
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.None
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnMultiValued
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.TTDescending
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnEscrowUpdate
- Microsoft.Isam.Esent.Interop.ColumndefGrbit
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnVersion
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnFixed
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnUserDefinedDefault
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.TTKey
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d2c94dcf7d454c5f0ea11fcee0bd46655099dfd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356551"
---
# <a name="columndefgrbit-enumeration"></a>Columndefgrbit-Enumeration

Optionen für die JET_COLUMNDEF Struktur.

Diese Enumeration enthält ein [FlagsAttribute](/dotnet/api/system.flagsattribute)-Attribut, das eine bitweise Kombination der Memberwerte zulässt.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration ColumndefGrbit
'Usage
Dim instance As ColumndefGrbit
```

``` csharp
[FlagsAttribute]
public enum ColumndefGrbit
```

## <a name="members"></a>Member

<table>
<thead>
<tr class="header">
<th></th>
<th>Membername</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td>Keine</td>
<td>Standardoptionen.</td>
</tr>
<tr class="even">
<td></td>
<td>Columnfixed</td>
<td>Die Spalte wird korrigiert. Es wird immer die gleiche Menge an Speicherplatz in einer Zeile verwendet, unabhängig davon, wie viele Daten in der Spalte gespeichert werden. Columnfixed kann nicht mit columntagged verwendet werden. Dieses Bit kann nicht mit langen Werten verwendet werden (d. h. JET_coltyp. LONGTEXT und JET_coltyp. LONGBINARY).</td>
</tr>
<tr class="odd">
<td></td>
<td>Columntagged</td>
<td>Die Spalte wird gekennzeichnet. Markierte Spalten beanspruchen keinen Speicherplatz in der Datenbank, wenn Sie keine Daten enthalten. Dieses Bit kann nicht mit columnfixed verwendet werden.</td>
</tr>
<tr class="even">
<td></td>
<td>Columnnotnull</td>
<td>Die Spalte darf nie auf einen NULL-Wert festgelegt werden. Unter Windows XP kann dies nur auf fixierte Spalten (Bit, Byte, Integer usw.) angewendet werden.</td>
</tr>
<tr class="odd">
<td></td>
<td>Columnversion</td>
<td>Die Spalte ist eine Versions Spalte, die die Version der Zeile angibt. Der Wert dieser Spalte beginnt bei Null und wird für jedes Update in der Zeile automatisch inkrementiert. Diese Option kann nur auf JET_coltyp angewendet werden. Lange Spalten. Diese Option kann nicht mit ' columnautoincrement ', ' columnescrowupdate ' oder ' columntagged ' verwendet werden.</td>
</tr>
<tr class="even">
<td></td>
<td>Columnautoincrement</td>
<td>Die Spalte wird automatisch inkrementiert. Die Zahl ist eine steigende Zahl, die in einer Tabelle garantiert eindeutig ist. Die Zahlen sind jedoch möglicherweise nicht kontinuierlich. Wenn z. b. fünf Zeilen in eine Tabelle eingefügt werden, &quot; kann die AutoIncrement- &quot; Spalte die Werte {1, 2, 6, 7, 8} enthalten. Dieses Bit kann nur für Spalten vom Typ JET_coltyp verwendet werden. Long oder JET_coltyp. Währungs.</td>
</tr>
<tr class="odd">
<td></td>
<td>Columnmultiwertig</td>
<td>Die Spalte kann mehr wertig sein. Für eine mehrwertige Spalte können NULL, ein oder mehrere Werte zugeordnet werden. Die verschiedenen Werte in einer mehrwertigen Spalte werden durch eine Zahl gekennzeichnet, die als itagsequence-Member bezeichnet wird, der zu verschiedenen Strukturen gehört, einschließlich: JET_RETINFO, JET_SETINFO, JET_SETCOLUMN, JET_RETRIEVECOLUMN und JET_ENUMCOLUMNVALUE. Mehrwertige Spalten müssen markierte Spalten sein. Das heißt, Sie können keine Spalten fester Länge oder Spalten mit variabler Länge aufweisen.</td>
</tr>
<tr class="even">
<td></td>
<td>Columnescrowupdate</td>
<td>Gibt an, dass eine Spalte eine Spalte für die hinterlegte Aktualisierung ist. Eine Spalte für das Hinterlegungs Update kann gleichzeitig von verschiedenen Sitzungen mit jetescrowupdate aktualisiert werden und behält die Transaktions Konsistenz bei. Eine Spalte vom Datentyp "hinterlegter" muss auch die folgenden Bedingungen erfüllen: eine Spalte für das hinterlegter-Update kann nur erstellt werden, wenn die Tabelle leer ist. Eine Spalte vom Typ "hinterlegter" muss vom Typ "JET_coltypLong" sein. Eine Spalte für das hinterlegter-Update muss einen Standardwert aufweisen. JET_bitColumnEscrowUpdate kann nicht in Verbindung mit columntagged, columnversion oder columnautoincrement verwendet werden.</td>
</tr>
<tr class="odd">
<td></td>
<td>Columnunversioniert</td>
<td>Die Spalte wird in einem ohne Versionsinformationen erstellt. Dies bedeutet, dass andere Transaktionen, die versuchen, eine Spalte mit demselben Namen hinzuzufügen, fehlschlagen. Dieses Bit ist nur bei jetaddcolumn nützlich. Sie kann nicht innerhalb einer Transaktion verwendet werden.</td>
</tr>
<tr class="even">
<td></td>
<td>Columnmaybenull</td>
<td>Beim äußeren Join weist der Vorgang zum Abrufen von Spalten möglicherweise keine Entsprechung aus der inneren Tabelle auf.</td>
</tr>
<tr class="odd">
<td></td>
<td>Columnuserdefineddefault</td>
<td>Der Standardwert für eine Spalte wird von einer Rückruffunktion bereitgestellt. Eine Spalte, die über einen benutzerdefinierten Standardwert verfügt, muss eine markierte Spalte sein. Das Angeben von JET_bitColumnUserDefinedDefault bedeutet, dass pvdefault auf eine JET_USERDEFINEDDEFAULT Struktur verweisen muss und cbdefault auf sizeof (JET_USERDEFINEDDEFAULT) festgelegt werden muss.</td>
</tr>
<tr class="even">
<td></td>
<td>Ttkey</td>
<td>Die Spalte ist eine Schlüssel Spalte für die temporäre Tabelle. Die Reihenfolge der Spaltendefinitionen, bei denen diese Option im Eingabe Array angegeben ist, bestimmt die Rangfolge der einzelnen Schlüssel Spalten für die temporäre Tabelle. Die erste Spaltendefinition im Array, für die diese Option festgelegt ist, ist die wichtigste Schlüssel Spalte usw. Wenn mehr Schlüssel Spalten angefordert werden, als von der Datenbank-Engine unterstützt werden können, wird diese Option für die nicht supportablen Schlüssel Spalten ignoriert.</td>
</tr>
<tr class="odd">
<td></td>
<td>Absteigend</td>
<td>Die Sortierreihenfolge der Schlüssel Spalte für die temporäre Tabelle sollte absteigend und nicht aufsteigend sein. Wenn diese Option ohne ttkey angegeben wird, wird diese Option ignoriert.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)

[Columncompressed](./windows7grbits.columncompressed-field.md)
