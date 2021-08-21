---
description: Weitere Informationen finden Sie unter UpdateGrbit-Enumeration.
title: UpdateGrbit-Enumeration (Microsoft.Isam.Esent.Interop.Server2003)
TOCTitle: UpdateGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.updategrbit(v=EXCHG.10)
ms:contentKeyID: 39514938
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit
- Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit.CheckESE97Compatibility
- Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit
- Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit.None
- Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit.CheckESE97Compatibility
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d78d4d4321831d682f9e3da11ab694e7ac1cc5dab05050e86e59e0765099e97e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118070477"
---
# <a name="updategrbit-enumeration"></a>UpdateGrbit-Enumeration

Optionen für [JetUpdate2(JET_SESID, JET_TABLEID, , \[ \] Int32, Int32, UpdateGrbit)](./server2003api.jetupdate2-method.md).

Diese Enumeration enthält ein [FlagsAttribute](/dotnet/api/system.flagsattribute)-Attribut, das eine bitweise Kombination der Memberwerte zulässt.

**Namespace:**  [Microsoft.Isam.Esent.Interop.Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration UpdateGrbit
'Usage
Dim instance As UpdateGrbit
```

``` csharp
[FlagsAttribute]
public enum UpdateGrbit
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
<td>CheckESE97Kompatibilität</td>
<td><strong>Veraltet.</strong> Dieses Flag bewirkt, dass das Update einen Fehler zurück gibt, wenn das Update in der Windows 2000-Version von ESE nicht möglich gewesen wäre, die eine geringere maximale Anzahl von mehrwertigen Spalteninstanzen in jedem Datensatz erzwungen hat als spätere Versionen von ESE. Dies ist nur für Anwendungen wichtig, die Daten zwischen anwendungen replizieren möchten, die auf Windows 2000 gehostet werden, und Anwendungen, die unter Windows 2003 oder höher von ESE gehostet werden. Dies sollte für die meisten Anwendungen nicht erforderlich sein.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[Microsoft.Isam.Esent.Interop.Server2003-Namespace](./microsoft.isam.esent.interop.server2003-namespace.md)
