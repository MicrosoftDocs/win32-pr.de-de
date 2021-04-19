---
description: 'Weitere Informationen finden Sie hier: objectinfogrbit-Enumeration'
title: Objectinfogrbit-Enumeration
TOCTitle: ObjectInfoGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.ObjectInfoGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.objectinfogrbit(v=EXCHG.10)
ms:contentKeyID: 39516208
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ObjectInfoGrbit
- Microsoft.Isam.Esent.Interop.ObjectInfoGrbit.Bookmark
- Microsoft.Isam.Esent.Interop.ObjectInfoGrbit.Rollback
- Microsoft.Isam.Esent.Interop.ObjectInfoGrbit.Updatable
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ObjectInfoGrbit.Bookmark
- Microsoft.Isam.Esent.Interop.ObjectInfoGrbit.Rollback
- Microsoft.Isam.Esent.Interop.ObjectInfoGrbit.Updatable
- Microsoft.Isam.Esent.Interop.ObjectInfoGrbit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4028a2a337b32394029960e45bb0e485c2b6b705
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349889"
---
# <a name="objectinfogrbit-enumeration"></a>Objectinfogrbit-Enumeration

Tabellen Optionen, die in [JET_OBJECTINFO](./jet-objectinfo-class.md)verwendet werden.

Diese Enumeration enthält ein [FlagsAttribute](/dotnet/api/system.flagsattribute)-Attribut, das eine bitweise Kombination der Memberwerte zulässt.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration ObjectInfoGrbit
'Usage
Dim instance As ObjectInfoGrbit
```

``` csharp
[FlagsAttribute]
public enum ObjectInfoGrbit
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
<td>Lesezeichen</td>
<td>Die Tabelle kann Lesezeichen enthalten.</td>
</tr>
<tr class="even">
<td></td>
<td>Rollback</td>
<td>Für die Tabelle kann ein Rollback ausgeführt werden.</td>
</tr>
<tr class="odd">
<td></td>
<td>Aktualisierbar</td>
<td>Die Tabelle kann aktualisiert werden.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
