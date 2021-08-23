---
description: Weitere Informationen finden Sie unter EndExternalBackupGrbit-Enumeration.
title: EndExternalBackupGrbit-Enumeration
TOCTitle: EndExternalBackupGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.endexternalbackupgrbit(v=EXCHG.10)
ms:contentKeyID: 39516835
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit
- Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit.Abort
- Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit.None
- Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit.Normal
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit
- Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit.Abort
- Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit.None
- Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit.Normal
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4e18f6ef200481c6f2b22fe229a9e5b0ebc5cbf9d9936b33ad373d93ef19b40c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119669930"
---
# <a name="endexternalbackupgrbit-enumeration"></a>EndExternalBackupGrbit-Enumeration

Optionen für [JetEndExternalBackupInstance(JET_INSTANCE)](./api.jetendexternalbackupinstance-method.md).

Diese Enumeration enthält ein [FlagsAttribute](/dotnet/api/system.flagsattribute)-Attribut, das eine bitweise Kombination der Memberwerte zulässt.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration EndExternalBackupGrbit
'Usage
Dim instance As EndExternalBackupGrbit
```

``` csharp
[FlagsAttribute]
public enum EndExternalBackupGrbit
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
<td>Normal</td>
<td>Die Clientanwendung hat die Sicherung vollständig abgeschlossen und endet normal.</td>
</tr>
<tr class="odd">
<td></td>
<td>Abbrechen</td>
<td>Die Clientanwendung bricht die Sicherung ab.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
