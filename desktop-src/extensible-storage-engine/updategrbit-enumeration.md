---
description: 'Weitere Informationen finden Sie hier: updategrbit-Enumeration'
title: Updategrbit-Enumeration (Microsoft. ISAM. ESENT. Interop. Server2003)
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
ms.openlocfilehash: e27809ef16fb00fd538e4c37826d10fefa3b396c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526792"
---
# <a name="updategrbit-enumeration"></a>Updategrbit-Enumeration

Optionen für [JetUpdate2 (JET_SESID, JET_TABLEID, \[ \] , Int32, Int32, updategrbit)](./server2003api.jetupdate2-method.md).

Diese Enumeration enthält ein [FlagsAttribute](/dotnet/api/system.flagsattribute)-Attribut, das eine bitweise Kombination der Memberwerte zulässt.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

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
<td>CheckESE97Compatibility</td>
<td><strong>Veraltet.</strong> Dieses Flag bewirkt, dass das Update einen Fehler zurückgibt, wenn das Update in der Windows 2000-Version von ESE nicht möglich wäre, was eine geringere maximale Anzahl von mehrwertigen Spalten Instanzen in jedem Datensatz erzwungen hat als spätere Versionen von ESE. Dies ist nur für Anwendungen wichtig, die Daten zwischen Anwendungen replizieren möchten, die unter Windows 2000 gehostet werden, und Anwendungen, die unter Windows 2003 oder höheren Versionen von ESE gehostet werden. Dies sollte für die meisten Anwendungen nicht erforderlich sein.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Microsoft. ISAM. ESENT. Interop. Server2003-Namespace](./microsoft.isam.esent.interop.server2003-namespace.md)
