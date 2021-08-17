---
description: 'Weitere Informationen zu: JET_COMMIT_ID.Equality-Operator'
title: JET_COMMIT_ID.Equality-Operator (Microsoft.Isam.Esent.Interop.Windows8)
TOCTitle: 'Equality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.op_Equality(Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID,Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.jet_commit_id.op_equality(v=EXCHG.10)
ms:contentKeyID: 55104297
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.Equality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.op_Equality
- Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.Equality
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6fb259e54141e3e94e6ee106724e4e737334519398c42ceb11c86026417407db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119112369"
---
# <a name="jet_commit_idequality-operator"></a>JET_COMMIT_ID.Equality-Operator

Bestimmen Sie, ob eine commitid gleich einer anderen commitid ist.

**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Operator = ( _
    lhs As JET_COMMIT_ID, _
    rhs As JET_COMMIT_ID _
) As Boolean
'Usage
Dim lhs As JET_COMMIT_ID
Dim rhs As JET_COMMIT_ID
Dim returnValue As Boolean

returnValue = (lhs = rhs)
```

``` csharp
public static bool operator ==(
    JET_COMMIT_ID lhs,
    JET_COMMIT_ID rhs
)
```

#### <a name="parameters"></a>Parameter

  - Lhs  
    Typ: [Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)  
    
    Die erste zu vergleichende commitid.

<!-- end list -->

  - rhs  
    Typ: [Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)  
    
    Die zweite zu vergleichende commitid.

#### <a name="return-value"></a>Rückgabewert

Typ: [System.Boolean](/dotnet/api/system.boolean)  
True, wenn "ls" kommt, ist gleich "rhs".  

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[JET_COMMIT_ID-Klasse](./jet-commit-id-class.md)

[JET_COMMIT_ID-Member](./jet-commit-id-members.md)

[Microsoft.Isam.Esent.Interop.Windows8-Namespace](./microsoft.isam.esent.interop.windows8-namespace.md)
