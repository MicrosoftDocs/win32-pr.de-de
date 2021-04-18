---
description: 'Weitere Informationen zu: Debug-Bit-Enumeration'
title: Debug-Enumeration
TOCTitle: DefragGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.DefragGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.defraggrbit(v=EXCHG.10)
ms:contentKeyID: 39516122
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.DefragGrbit
- Microsoft.Isam.Esent.Interop.DefragGrbit.AvailSpaceTreesOnly
- Microsoft.Isam.Esent.Interop.DefragGrbit.BatchStart
- Microsoft.Isam.Esent.Interop.DefragGrbit.BatchStop
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.DefragGrbit
- Microsoft.Isam.Esent.Interop.DefragGrbit.BatchStart
- Microsoft.Isam.Esent.Interop.DefragGrbit.AvailSpaceTreesOnly
- Microsoft.Isam.Esent.Interop.DefragGrbit.BatchStop
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e5da047fbdad20ac40d780dc5b0bba9e986e7672
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350986"
---
# <a name="defraggrbit-enumeration"></a>Debug-Enumeration

Optionen für [jetdefragment (JET_SESID, JET_DBID, String, Int32, Int32, defraggrbit)](./api.jetdefragment-method.md).

Diese Enumeration enthält ein [FlagsAttribute](/dotnet/api/system.flagsattribute)-Attribut, das eine bitweise Kombination der Memberwerte zulässt.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration DefragGrbit
'Usage
Dim instance As DefragGrbit
```

``` csharp
[FlagsAttribute]
public enum DefragGrbit
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
<td>Availspacetreesonly</td>
<td>Zerlegt den verfügbaren Platz Anteil der ESE-Daten Bank Speicher Belegung. Der Daten Bankbereich ist in zwei Typen unterteilt: eigener Speicherplatz und verfügbarer Speicherplatz. Der Speicherplatz ist einer Tabelle oder einem Index zugeordnet, während der verfügbare Speicherplatz für die Verwendung innerhalb der Tabelle bzw. des Indexes bereit ist. Der verfügbare Speicherplatz ist weitaus dynamischer als das Verhalten und erfordert eine Inline Defragmentierung, die nicht dem Besitz des eigenen Speicherplatzes oder der Tabellen-oder Indexdaten entspricht.</td>
</tr>
<tr class="even">
<td></td>
<td>Batchstart</td>
<td>Startet eine neue defragmentierungsaufgabe.</td>
</tr>
<tr class="odd">
<td></td>
<td>Batchstoppt</td>
<td>Beendet eine defragmentierungsaufgabe.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
