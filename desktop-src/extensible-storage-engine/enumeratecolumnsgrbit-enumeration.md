---
description: Weitere Informationen finden Sie unter EnumerateColumnsGrbit-Enumeration.
title: EnumerateColumnsGrbit-Enumeration
TOCTitle: EnumerateColumnsGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.enumeratecolumnsgrbit(v=EXCHG.10)
ms:contentKeyID: 39516754
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateCompressOutput
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateCopy
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateIgnoreDefault
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.None
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateTaggedOnly
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumeratePresenceOnly
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateCompressOutput
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateIgnoreDefault
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.None
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateCopy
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumeratePresenceOnly
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateTaggedOnly
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6267bb254101d4c470b3e496e2996a97edc3b817f226e1c78cc226237e56a9b8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119366330"
---
# <a name="enumeratecolumnsgrbit-enumeration"></a>EnumerateColumnsGrbit-Enumeration

Optionen für JetEnumerateColumns.

Diese Enumeration enthält ein [FlagsAttribute](/dotnet/api/system.flagsattribute)-Attribut, das eine bitweise Kombination der Memberwerte zulässt.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration EnumerateColumnsGrbit
'Usage
Dim instance As EnumerateColumnsGrbit
```

``` csharp
[FlagsAttribute]
public enum EnumerateColumnsGrbit
```

## <a name="members"></a>Member

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
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
<td>EnumerateCompressOutput</td>
<td>Beim Aufzählen von Spaltenwerten können alle Spalten, für die alle Werte abgerufen werden und die nur einen Nicht-NULL-Spaltenwert haben, in einem komprimierten Format zurückgegeben werden. Der Status für solche Spalten wird auf <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a> festgelegt, und die Größe des Spaltenwerts und der Arbeitsspeicher, der den Spaltenwert enthält, werden direkt in der JET_ENUMCOLUMN <a href="dn335081(v=exchg.10).md">zurückgegeben.</a> Es ist nicht garantiert, dass alle berechtigten Spalten auf diese Weise komprimiert werden. Weitere <a href="dn335081(v=exchg.10).md">JET_ENUMCOLUMN</a> finden Sie unter .</td>
</tr>
<tr class="odd">
<td></td>
<td>EnumerateCopy</td>
<td>Diese Option gibt an, dass die geänderten Spaltenwerte des Datensatzes und nicht die ursprünglichen Spaltenwerte aufzählt werden sollen. Wenn ein Spaltenwert nicht geändert wurde, wird der ursprüngliche Spaltenwert aufzählt. Auf diese Weise kann ein Spaltenwert, der noch nicht eingefügt oder aktualisiert wurde, beim Einfügen oder Aktualisieren eines Datensatzes aufzählt werden.
<p>Diese Option ist identisch mit <a href="hh578120(v=exchg.10).md">RetrieveCopy.</a></p></td>
</tr>
<tr class="even">
<td></td>
<td>EnumerateIgnoreDefault</td>
<td>Wenn eine bestimmte Spalte nicht im Datensatz vorhanden ist, wird kein Spaltenwert zurückgegeben. Normalerweise wird in diesem Fall der Standardwert für die Spalte zurückgegeben, sofern dieser enthalten ist. Es ist garantiert, dass, wenn die Spalte auf einen anderen Wert als den Standardwert festgelegt ist, dieser andere Wert zurückgegeben wird (d. h., wenn eine Spalte mit einem Standardwert explizit auf NULL festgelegt ist, wird ein NULL-Wert als Wert für diese Spalte zurückgegeben). Auch wenn diese Option angefordert wird, ist es weiterhin möglich, einen Spaltenwert zu sehen, der dem Standardwert entspricht. Es wird kein Aufwand unternommen, Spaltenwerte zu entfernen, die mit ihren Standardwerten übereinstimmen. Beachten Sie, dass diese Option die Ausgabe von <a href="dn292148(v=exchg.10).md">JetEnumerateColumns(JET_SESID, JET_TABLEID, Int32, [], Int32, [], JET_PFNREALLOC, IntPtr, Int32, EnumerateColumnsGrbit)</a> beeinflusst, wenn sie mit EnumeratePresenceOnly oder EnumerateTaggedOnly verwendet wird.</td>
</tr>
<tr class="odd">
<td></td>
<td>EnumeratePresenceOnly</td>
<td>Wenn ein Nicht-NULL-Wert für die angeforderte Spalte oder den angeforderten Spaltenwert vorhanden ist, werden die zugeordneten Daten nicht zurückgegeben. Stattdessen wird der zugeordnete Status für diesen Spalten- oder Spaltenwert auf <a href="hh557250(v=exchg.10).md">ColumnPresent festgelegt.</a> Wenn der Spalten- oder Spaltenwert NULL ist, wird <a href="hh557250(v=exchg.10).md">ColumnNull</a> wie gewohnt zurückgegeben.</td>
</tr>
<tr class="even">
<td></td>
<td>EnumerateTaggedOnly</td>
<td>Beim Aufzählen aller Spaltenwerte im Datensatz (z. B. wenn numColumnids null ist), werden nur markierte Spaltenwerte zurückgegeben. Diese Option ist beim Aufzählen eines bestimmten Arrays von Spalten-IDs nicht zulässig.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)

[EnumerateIgnoreUserDefinedDefault](./server2003grbits.enumerateignoreuserdefineddefault-field.md)

[EnumerateInRecordOnly](./windows7grbits.enumerateinrecordonly-field.md)
