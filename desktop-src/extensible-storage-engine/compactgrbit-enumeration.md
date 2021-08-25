---
description: 'Weitere Informationen zu: CompactGrbit-Enumeration'
title: CompactGrbit-Enumeration
TOCTitle: CompactGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.CompactGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.compactgrbit(v=EXCHG.10)
ms:contentKeyID: 39509676
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.CompactGrbit
- Microsoft.Isam.Esent.Interop.CompactGrbit.None
- Microsoft.Isam.Esent.Interop.CompactGrbit.Stats
- Microsoft.Isam.Esent.Interop.CompactGrbit.Repair
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.CompactGrbit.Repair
- Microsoft.Isam.Esent.Interop.CompactGrbit.Stats
- Microsoft.Isam.Esent.Interop.CompactGrbit
- Microsoft.Isam.Esent.Interop.CompactGrbit.None
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a85f3298e4127a35acd5a39839f788fc404269f80a07463bde1417dc04f7fe16
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119976540"
---
# <a name="compactgrbit-enumeration"></a>CompactGrbit-Enumeration

Optionen für [JetCompact(JET_SESID, String, String, JET_PFNSTATUS, JET_CONVERT, CompactGrbit)](./api.jetcompact-method.md).

Diese Enumeration enthält ein [FlagsAttribute](/dotnet/api/system.flagsattribute)-Attribut, das eine bitweise Kombination der Memberwerte zulässt.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration CompactGrbit
'Usage
Dim instance As CompactGrbit
```

``` csharp
[FlagsAttribute]
public enum CompactGrbit
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
<td>Stats</td>
<td>Bewirkt, dass JetCompact Statistiken für die Quelldatenbank in eine Datei mit dem Namen DFRGINFO.TXT. Zu den Statistiken gehören der Name jeder Tabelle in der Quelldatenbank, die Anzahl der Zeilen in jeder Tabelle, die Gesamtgröße in Bytes aller Zeilen in jeder Tabelle, die Gesamtgröße in Bytes aller Spalten vom Typ <a href="hh577895(v=exchg.10).md">LongText</a> oder <a href="hh577895(v=exchg.10).md">LongBinary,</a> die groß genug waren, um getrennt vom Datensatz gespeichert zu werden, die Anzahl der gruppierten Indexblattseiten und die Anzahl der Blattseiten mit langen Werten. Darüber hinaus werden zusammenfassende Statistiken, einschließlich der Größe der Quelldatenbank, der Zieldatenbank, der für die Datenbankkomp compaction erforderlichen Zeit und des temporären Datenbankspeicherplatzes, ebenfalls gedumpt.</td>
</tr>
<tr class="odd">
<td></td>
<td>Reparieren</td>
<td><strong>Veraltet.</strong> Wird verwendet, wenn bekannt ist, dass die Quelldatenbank beschädigt ist. Sie ermöglicht eine ganze Reihe neuer Verhaltensweisen, die so viele Daten wie möglich aus der Quelldatenbank speichern sollen. JetCompact mit dieser Option gibt möglicherweise <a href="hh564840(v=exchg.10).md">Success</a> zurück, kopiert aber nicht alle in der Quelldatenbank erstellten Daten. Daten, die sich in beschädigten Teilen der Quelldatenbank befanden, werden übersprungen.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
