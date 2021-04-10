---
description: 'Weitere Informationen finden Sie hier: idlegrbit-Enumeration'
title: Idlegrbit-Enumeration
TOCTitle: IdleGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.IdleGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.idlegrbit(v=EXCHG.10)
ms:contentKeyID: 39514282
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.IdleGrbit
- Microsoft.Isam.Esent.Interop.IdleGrbit.Compact
- Microsoft.Isam.Esent.Interop.IdleGrbit.FlushBuffers
- Microsoft.Isam.Esent.Interop.IdleGrbit.GetStatus
- Microsoft.Isam.Esent.Interop.IdleGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.IdleGrbit.Compact
- Microsoft.Isam.Esent.Interop.IdleGrbit.FlushBuffers
- Microsoft.Isam.Esent.Interop.IdleGrbit
- Microsoft.Isam.Esent.Interop.IdleGrbit.None
- Microsoft.Isam.Esent.Interop.IdleGrbit.GetStatus
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f02937241066762b6d711d89e62e67cfed9f41f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215056"
---
# <a name="idlegrbit-enumeration"></a>Idlegrbit-Enumeration

Optionen für [jetidle (JET_SESID, idlegrbit)](./api.jetidle-method.md).

Diese Enumeration enthält ein [FlagsAttribute](/dotnet/api/system.flagsattribute)-Attribut, das eine bitweise Kombination der Memberwerte zulässt.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration IdleGrbit
'Usage
Dim instance As IdleGrbit
```

``` csharp
[FlagsAttribute]
public enum IdleGrbit
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
<td>Flushbuffers</td>
<td>Löst die Bereinigung des Versionsspeicher aus.</td>
</tr>
<tr class="odd">
<td></td>
<td>Kompakt</td>
<td>Für die zukünftige Verwendung reserviert. Wenn dieses Flag angegeben wird, gibt die API <a href="hh564840(v=exchg.10).md">invalidgrbit</a>zurück.</td>
</tr>
<tr class="even">
<td></td>
<td>GetStatus</td>
<td>Gibt <a href="hh557250(v=exchg.10).md">idlefull</a> zurück, wenn der Versionsspeicher größer als der Halbwert ist.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
