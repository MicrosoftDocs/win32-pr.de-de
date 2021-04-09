---
description: 'Weitere Informationen finden Sie hier: conditionalcolumngrbit-Enumeration'
title: Conditionalcolumngrbit-Enumeration
TOCTitle: ConditionalColumnGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.ConditionalColumnGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.conditionalcolumngrbit(v=EXCHG.10)
ms:contentKeyID: 39513009
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ConditionalColumnGrbit
- Microsoft.Isam.Esent.Interop.ConditionalColumnGrbit.ColumnMustBeNonNull
- Microsoft.Isam.Esent.Interop.ConditionalColumnGrbit.ColumnMustBeNull
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ConditionalColumnGrbit.ColumnMustBeNull
- Microsoft.Isam.Esent.Interop.ConditionalColumnGrbit
- Microsoft.Isam.Esent.Interop.ConditionalColumnGrbit.ColumnMustBeNonNull
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 82828df5d5a25dac08a2a8ab560225456f075a34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959153"
---
# <a name="conditionalcolumngrbit-enumeration"></a>Conditionalcolumngrbit-Enumeration

Optionen für die JET_CONDITIONALCOLUMN Struktur.

Diese Enumeration enthält ein [FlagsAttribute](/dotnet/api/system.flagsattribute)-Attribut, das eine bitweise Kombination der Memberwerte zulässt.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration ConditionalColumnGrbit
'Usage
Dim instance As ConditionalColumnGrbit
```

``` csharp
[FlagsAttribute]
public enum ConditionalColumnGrbit
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
<td>Columnmustbenull</td>
<td>Die Spalte muss NULL sein, damit ein Index Eintrag im Index angezeigt wird.</td>
</tr>
<tr class="even">
<td></td>
<td>Columnmustbenonnull</td>
<td>Die Spalte darf nicht NULL sein, damit ein Index Eintrag im Index angezeigt wird.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
