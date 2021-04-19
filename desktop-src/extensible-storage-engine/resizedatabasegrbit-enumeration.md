---
description: 'Weitere Informationen finden Sie hier: resizedatabasegrbit-Enumeration'
title: Resizedatabasegrbit-Enumeration (Microsoft. ISAM. ESENT. Interop. Windows8)
TOCTitle: ResizeDatabaseGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Windows8.ResizeDatabaseGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.resizedatabasegrbit(v=EXCHG.10)
ms:contentKeyID: 55104329
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.ResizeDatabaseGrbit
- Microsoft.Isam.Esent.Interop.Windows8.ResizeDatabaseGrbit.None
- Microsoft.Isam.Esent.Interop.Windows8.ResizeDatabaseGrbit.OnlyGrow
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.ResizeDatabaseGrbit.None
- Microsoft.Isam.Esent.Interop.Windows8.ResizeDatabaseGrbit
- Microsoft.Isam.Esent.Interop.Windows8.ResizeDatabaseGrbit.OnlyGrow
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 51d703f96882136e2b88f1a2df37609573c725e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362518"
---
# <a name="resizedatabasegrbit-enumeration"></a>Resizedatabasegrbit-Enumeration

Optionen für [jetresizedatabase (JET_SESID, JET_DBID, Int32, Int32, resizedatabasegrbit)](./windows8api.jetresizedatabase-method.md).

Diese Enumeration enthält ein [FlagsAttribute](/dotnet/api/system.flagsattribute)-Attribut, das eine bitweise Kombination der Memberwerte zulässt.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration ResizeDatabaseGrbit
'Usage
Dim instance As ResizeDatabaseGrbit
```

``` csharp
[FlagsAttribute]
public enum ResizeDatabaseGrbit
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
<td>Keine Option.</td>
</tr>
<tr class="even">
<td></td>
<td>Onlygrow</td>
<td>Vergrößern Sie nur die Datenbank. Wenn der Größenänderung die Datenbank verkleinern würde, führen Sie keine Aktion aus.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Microsoft. ISAM. ESENT. Interop. Windows8-Namespace](./microsoft.isam.esent.interop.windows8-namespace.md)
