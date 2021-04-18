---
description: 'Weitere Informationen finden Sie hier: enumeratecolumnsgrbit-Enumeration'
title: Enumeratecolumnsgrbit-Enumeration
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
ms.openlocfilehash: 5e27e6810b37b513d550bbafce509b2815ccea2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352353"
---
# <a name="enumeratecolumnsgrbit-enumeration"></a>Enumeratecolumnsgrbit-Enumeration

Optionen für jetenreeratecolumschlag.

Diese Enumeration enthält ein [FlagsAttribute](/dotnet/api/system.flagsattribute)-Attribut, das eine bitweise Kombination der Memberwerte zulässt.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

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
<td>Enumeratecompressoutput</td>
<td>Beim Aufzählen von Spaltenwerten können alle Spalten, für die wir alle Werte abrufen und nur einen nicht-NULL-Spaltenwert aufweisen, in einem komprimierten Format zurückgegeben werden. Der Status dieser Spalten wird auf <a href="hh557250(v=exchg.10).md">columnsinglevalue</a> festgelegt, und die Größe des Spaltenwerts und der Arbeitsspeicher, der den Spaltenwert enthält, werden direkt in der <a href="dn335081(v=exchg.10).md">JET_ENUMCOLUMN</a> Struktur zurückgegeben. Es ist nicht sichergestellt, dass alle berechtigten Spalten auf diese Weise komprimiert werden. Weitere Informationen finden Sie unter <a href="dn335081(v=exchg.10).md">JET_ENUMCOLUMN</a> .</td>
</tr>
<tr class="odd">
<td></td>
<td>Enumeratecopy</td>
<td>Diese Option gibt an, dass die geänderten Spaltenwerte des Datensatzes anstelle der ursprünglichen Spaltenwerte aufgezählt werden sollen. Wenn ein Spaltenwert nicht geändert wurde, wird der ursprüngliche Spaltenwert aufgelistet. Auf diese Weise kann ein Spaltenwert, der noch nicht eingefügt oder aktualisiert wurde, beim Einfügen oder Aktualisieren eines Datensatzes aufgezählt werden.
<p>Diese Option ist mit " <a href="hh578120(v=exchg.10).md">retrievecopy</a>" identisch.</p></td>
</tr>
<tr class="even">
<td></td>
<td>Enumerateignoredefault</td>
<td>Wenn eine bestimmte Spalte nicht im Datensatz vorhanden ist, wird kein Spaltenwert zurückgegeben. Normalerweise würde der Standardwert für die Spalte, sofern vorhanden, in diesem Fall zurückgegeben werden. Wenn die Spalte auf einen anderen Wert als den Standardwert festgelegt ist, wird ein anderer Wert zurückgegeben (d. h., wenn eine Spalte mit einem Standardwert explizit auf NULL festgelegt ist, wird ein NULL-Wert als Wert für diese Spalte zurückgegeben). Auch wenn diese Option angefordert wird, ist es weiterhin möglich, einen Spaltenwert anzuzeigen, der dem Standardwert entspricht. Es wird nicht versucht, Spaltenwerte zu entfernen, die ihren Standardwerten entsprechen. Beachten Sie, dass sich diese Option auf die Ausgabe von <a href="dn292148(v=exchg.10).md">jetenumeratecolumns (JET_SESID JET_TABLEID, Int32, [], Int32, [], JET_PFNREALLOC, IntPtr, Int32, enumeratecolumnsgrbit)</a> auswirkt, wenn Sie mit enumeratepresenceonly oder enumeratetaggedonly verwendet wird.</td>
</tr>
<tr class="odd">
<td></td>
<td>Enumeratepresenceonly</td>
<td>Wenn ein nicht-NULL-Wert für den angeforderten Spalten-oder Spaltenwert vorhanden ist, werden die zugehörigen Daten nicht zurückgegeben. Stattdessen wird der zugehörige Status für diesen Spalten-oder Spaltenwert auf <a href="hh557250(v=exchg.10).md">columnpresent</a>festgelegt. Wenn der Spalten-oder Spaltenwert NULL ist, wird <a href="hh557250(v=exchg.10).md">columnnull</a> wie gewohnt zurückgegeben.</td>
</tr>
<tr class="even">
<td></td>
<td>Enumeratetaggedonly</td>
<td>Wenn alle Spaltenwerte im Datensatz aufgelistet werden (z. b. wenn numcolumnids NULL ist), werden nur markierte Spaltenwerte zurückgegeben. Diese Option ist beim Auflisten eines bestimmten Arrays von Spalten-IDs nicht zulässig.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)

[Enumerateignoreuserdefineddefault](./server2003grbits.enumerateignoreuserdefineddefault-field.md)

[Enumerateingerecordonly](./windows7grbits.enumerateinrecordonly-field.md)
