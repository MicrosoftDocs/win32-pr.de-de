---
description: 'Weitere Informationen finden Sie hier: JET_COMMIT_ID. Gleichheits Operator'
title: JET_COMMIT_ID. Equality-Operator (Microsoft. ISAM. ESENT. Interop. Windows8)
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
ms.openlocfilehash: 36815693c078146faec7d604dd28e5d74d475af2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527452"
---
# <a name="jet_commit_idequality-operator"></a>JET_COMMIT_ID. Equality-Operator

Stellen Sie fest, ob eine comentschärd gleich einer anderen comentschärd ist.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

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

  - LHS  
    Typ: [Microsoft.ISAM.ESENT.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)  
    
    Die erste zu vergleichende comentschärd.

<!-- end list -->

  - rhs  
    Typ: [Microsoft.ISAM.ESENT.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)  
    
    Die zweite zu vergleichende comentschärd.

#### <a name="return-value"></a>Rückgabewert

Typ: [System. Boolean](/dotnet/api/system.boolean)  
"True", wenn "LHS" gleich "RHS" ist.  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[JET_COMMIT_ID-Klasse](./jet-commit-id-class.md)

[Mitglieder JET_COMMIT_ID](./jet-commit-id-members.md)

[Microsoft. ISAM. ESENT. Interop. Windows8-Namespace](./microsoft.isam.esent.interop.windows8-namespace.md)
