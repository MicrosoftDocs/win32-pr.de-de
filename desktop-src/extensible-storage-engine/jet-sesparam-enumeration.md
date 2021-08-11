---
description: 'Weitere Informationen zu: JET_sesparam-Enumeration'
title: JET_sesparam-Enumeration (Microsoft.Isam.Esent.Interop.Windows8)
TOCTitle: JET_sesparam enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Windows8.JET_sesparam
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.jet_sesparam(v=EXCHG.10)
ms:contentKeyID: 55104452
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.JET_sesparam
- Microsoft.Isam.Esent.Interop.Windows8.JET_sesparam.Base
- Microsoft.Isam.Esent.Interop.Windows8.JET_sesparam.CommitDefault
- Microsoft.Isam.Esent.Interop.Windows8.JET_sesparam.CommitGenericContext
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.JET_sesparam.Base
- Microsoft.Isam.Esent.Interop.Windows8.JET_sesparam.CommitGenericContext
- Microsoft.Isam.Esent.Interop.Windows8.JET_sesparam.CommitDefault
- Microsoft.Isam.Esent.Interop.Windows8.JET_sesparam
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7866fa72df1beadf7cd06d61cfe60b2f1ca31a9feabb4412903186eeeeb80748
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118253638"
---
# <a name="jet_sesparam-enumeration"></a>JET_sesparam-Enumeration

ESENT-Sitzungsparameter.

**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Enumeration JET_sesparam
'Usage
Dim instance As JET_sesparam
```

``` csharp
public enum JET_sesparam
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
<td>Basis</td>
<td>Dieser Parameter ist nicht für die Verwendung vorgesehen.</td>
</tr>
<tr class="even">
<td></td>
<td>CommitDefault</td>
<td>Dieser Parameter legt die Grbits für commit fest. Er entspricht funktional dem Systemparameter JET_param.CommitDefault, wenn er mit einer -Instanz und einer sesid verwendet wird.</td>
</tr>
<tr class="odd">
<td></td>
<td>CommitGenericContext</td>
<td>Dieser Parameter legt einen benutzerspezifischen Commitkontext fest, der beim Commit im Transaktionsprotokoll auf Ebene 0 platziert wird.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Microsoft.Isam.Esent.Interop.Windows8-Namespace](./microsoft.isam.esent.interop.windows8-namespace.md)
