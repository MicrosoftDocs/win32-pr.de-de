---
description: 'Weitere Informationen zu: SetCurrentIndexGrbit-Enumeration'
title: SetCurrentIndexGrbit-Enumeration
TOCTitle: SetCurrentIndexGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.setcurrentindexgrbit(v=EXCHG.10)
ms:contentKeyID: 39515072
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit
- Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit.MoveFirst
- Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit.NoMove
- Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit.None
- Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit.NoMove
- Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit.MoveFirst
- Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ee060e73208219408b278e325d2ecf21c36e50975fc5d72e7723fab344b9459b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119107264"
---
# <a name="setcurrentindexgrbit-enumeration"></a>SetCurrentIndexGrbit-Enumeration

Optionen für [JetSetCurrentIndex2(JET_SESID, JET_TABLEID, String, SetCurrentIndexGrbit)](./api.jetsetcurrentindex2-method.md) und [JetSetCurrentIndex3(JET_SESID, JET_TABLEID, String, SetCurrentIndexGrbit, Int32).](./api.jetsetcurrentindex3-method.md)

Diese Enumeration enthält ein [FlagsAttribute](/dotnet/api/system.flagsattribute)-Attribut, das eine bitweise Kombination der Memberwerte zulässt.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration SetCurrentIndexGrbit
'Usage
Dim instance As SetCurrentIndexGrbit
```

``` csharp
[FlagsAttribute]
public enum SetCurrentIndexGrbit
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
<td>Standardoptionen. Dies entspricht MoveFirst.</td>
</tr>
<tr class="even">
<td></td>
<td>Movefirst</td>
<td>Gibt an, dass der Cursor am ersten Eintrag des angegebenen Indexes positioniert werden soll. Wenn der aktuelle Index ausgewählt wird, wird diese Option ignoriert.</td>
</tr>
<tr class="odd">
<td></td>
<td>NoMove</td>
<td>Gibt an, dass der Cursor auf dem Indexeintrag des neuen Index positioniert werden soll, der dem Datensatz entspricht, der dem Indexeintrag an der aktuellen Position des Cursors auf dem alten Index zugeordnet ist.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
