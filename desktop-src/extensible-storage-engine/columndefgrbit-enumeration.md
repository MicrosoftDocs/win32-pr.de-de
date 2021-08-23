---
description: Weitere Informationen finden Sie unter ColumndefGrbit-Enumeration.
title: ColumndefGrbit-Enumeration
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
ms.openlocfilehash: f2bd26a3dac291d78b101aa56f186d9b31f7a927b1eca3e29febc7773e3c0939
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119042458"
---
# <a name="columndefgrbit-enumeration"></a>ColumndefGrbit-Enumeration

Optionen für die JET_COLUMNDEF Struktur.

Diese Enumeration enthält ein [FlagsAttribute](/dotnet/api/system.flagsattribute)-Attribut, das eine bitweise Kombination der Memberwerte zulässt.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

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
<td>ColumnFixed</td>
<td>Die Spalte wird korrigiert. Es wird immer die gleiche Menge an Speicherplatz in einer Zeile verwendet, unabhängig davon, wie viele Daten in der Spalte gespeichert werden. ColumnFixed kann nicht mit ColumnTagged verwendet werden. Dieses Bit kann nicht mit langen Werten verwendet werden (d. h. JET_coltyp. LongText und JET_coltyp. LongBinary).</td>
</tr>
<tr class="odd">
<td></td>
<td>ColumnTagged</td>
<td>Die Spalte wird markiert. Markierte Spalten nehmen keinen Speicherplatz in der Datenbank ein, wenn sie keine Daten enthalten. Dieses Bit kann nicht mit ColumnFixed verwendet werden.</td>
</tr>
<tr class="even">
<td></td>
<td>ColumnNotNULL</td>
<td>Die Spalte darf nie auf einen NULL-Wert festgelegt werden. Auf Windows XP kann dies nur auf feste Spalten (Bit, Byte, ganze Zahl usw.) angewendet werden.</td>
</tr>
<tr class="odd">
<td></td>
<td>ColumnVersion</td>
<td>Die Spalte ist eine Versionsspalte, die die Version der Zeile angibt. Der Wert dieser Spalte beginnt bei 0 (null) und wird für jedes Update der Zeile automatisch erhöht. Diese Option kann nur auf die JET_coltyp. Lange Spalten. Diese Option kann nicht mit ColumnAutoincrement, ColumnEscrowUpdate oder ColumnTagged verwendet werden.</td>
</tr>
<tr class="even">
<td></td>
<td>ColumnAutoincrement</td>
<td>Die Spalte wird automatisch erhöht. Die Zahl ist eine steigende Zahl, und es ist garantiert, dass sie innerhalb einer Tabelle eindeutig ist. Die Zahlen sind jedoch möglicherweise nicht kontinuierlich. Wenn beispielsweise fünf Zeilen in eine Tabelle eingefügt werden, kann die Spalte für die automatische Inkrementierung die Werte &quot; &quot; { 1, 2, 6, 7, 8 } enthalten. Dieses Bit kann nur für Spalten vom Typ JET_coltyp. Long oder JET_coltyp. Währung.</td>
</tr>
<tr class="odd">
<td></td>
<td>ColumnMultiValued</td>
<td>Die Spalte kann mehrere Werte haben. Einer mehrwertigen Spalte können null, ein oder mehrere Werte zugeordnet sein. Die verschiedenen Werte in einer mehrwertigen Spalte werden durch eine Zahl namens itagSequence-Member identifiziert, die zu verschiedenen Strukturen gehört, einschließlich: JET_RETINFO, JET_SETINFO, JET_SETCOLUMN, JET_RETRIEVECOLUMN und JET_ENUMCOLUMNVALUE. Mehrwertige Spalten müssen mit Tags versehen sein. Das bedeutet, dass es sich nicht um Spalten fester länge oder variabler Länge handelt.</td>
</tr>
<tr class="even">
<td></td>
<td>ColumnEscrowUpdate</td>
<td>Gibt an, dass es sich bei einer Spalte um eine Spalte zum Aktualisieren der Stirnrunzel handelt. Eine Spalte zum Aktualisieren der Stirnrunzeln kann gleichzeitig von verschiedenen Sitzungen mit JetEscrowUpdate aktualisiert werden und behält die Transaktionskonsistenz bei. Eine Spalte zum Aktualisieren der Stirnrunzeln muss auch die folgenden Bedingungen erfüllen: Eine Spalte zum Aktualisieren der Stirnrunzeln kann nur erstellt werden, wenn die Tabelle leer ist. Eine Spalte zum Aktualisieren der Stirnrunzeln muss vom Typ JET_coltypLong. Eine Spalte zum Aktualisieren der Stirnrunzeln muss über einen Standardwert verfügen. JET_bitColumnEscrowUpdate kann nicht in Verbindung mit ColumnTagged, ColumnVersion oder ColumnAutoincrement verwendet werden.</td>
</tr>
<tr class="odd">
<td></td>
<td>ColumnUnversioned</td>
<td>Die Spalte wird in einem ohne Versionsinformationen erstellt. Dies bedeutet, dass andere Transaktionen, die versuchen, eine Spalte mit dem gleichen Namen hinzuzufügen, fehlschlagen. Dieses Bit ist nur bei JetAddColumn nützlich. Sie kann nicht innerhalb einer Transaktion verwendet werden.</td>
</tr>
<tr class="even">
<td></td>
<td>ColumnMaybeNull</td>
<td>Bei einem äußeren Join hat der Vorgang zum Abrufen der Spalte möglicherweise keine Übereinstimmung aus der inneren Tabelle.</td>
</tr>
<tr class="odd">
<td></td>
<td>ColumnUserDefinedDefault</td>
<td>Der Standardwert für eine Spalte wird von einer Rückruffunktion bereitgestellt. Eine Spalte mit einem benutzerdefinierten Standardwert muss eine markierte Spalte sein. Die Angabe JET_bitColumnUserDefinedDefault bedeutet, dass pvDefault auf eine JET_USERDEFINEDDEFAULT-Struktur verweisen muss, und cbDefault muss auf sizeof( JET_USERDEFINEDDEFAULT ) festgelegt werden.</td>
</tr>
<tr class="even">
<td></td>
<td>TTKey</td>
<td>Die Spalte ist eine Schlüsselspalte für die temporäre Tabelle. Die Reihenfolge der Spaltendefinitionen mit dieser Option, die im Eingabearray angegeben ist, bestimmt die Rangfolge der einzelnen Schlüsselspalten für die temporäre Tabelle. Die erste Spaltendefinition im Array, für das diese Option festgelegt ist, ist die wichtigste Schlüsselspalte und so weiter. Wenn mehr Schlüsselspalten angefordert werden, als von der Datenbank-Engine unterstützt werden können, wird diese Option für die nicht unterstützten Schlüsselspalten ignoriert.</td>
</tr>
<tr class="odd">
<td></td>
<td>TTDescending</td>
<td>Die Sortierreihenfolge der Schlüsselspalte für die temporäre Tabelle sollte absteigend und nicht aufsteigend sein. Wenn diese Option ohne TTKey angegeben wird, wird diese Option ignoriert.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)

[ColumnCompressed](./windows7grbits.columncompressed-field.md)
