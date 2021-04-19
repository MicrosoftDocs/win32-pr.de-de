---
description: 'Weitere Informationen finden Sie hier: JET_LGPOS. LessThanOrEqual-Operator'
title: JET_LGPOS. LessThanOrEqual-Operator
TOCTitle: 'LessThanOrEqual operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_LGPOS.op_LessThanOrEqual(Microsoft.Isam.Esent.Interop.JET_LGPOS,Microsoft.Isam.Esent.Interop.JET_LGPOS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_lgpos.op_lessthanorequal(v=EXCHG.10)
ms:contentKeyID: 39510104
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_LGPOS.LessThanOrEqual
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_LGPOS.LessThanOrEqual
- Microsoft.Isam.Esent.Interop.JET_LGPOS.op_LessThanOrEqual
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 57eb2f9383b218409ebee927cc4d6ad1283f3e8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366069"
---
# <a name="jet_lgposlessthanorequal-operator"></a>JET_LGPOS. LessThanOrEqual-Operator

Bestimmen Sie, ob eine Protokoll Position vor oder gleich einer anderen Protokoll Position ist.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Operator <= ( _
    lhs As JET_LGPOS, _
    rhs As JET_LGPOS _
) As Boolean
'Usage
Dim lhs As JET_LGPOS
Dim rhs As JET_LGPOS
Dim returnValue As Boolean

returnValue = (lhs <= rhs)
```

``` csharp
public static bool operator <=(
    JET_LGPOS lhs,
    JET_LGPOS rhs
)
```

#### <a name="parameters"></a>Parameter

  - LHS  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_LGPOS](./jet-lgpos-structure2.md)  
    
    Die erste zu vergleichende Protokoll Position.

<!-- end list -->

  - rhs  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_LGPOS](./jet-lgpos-structure2.md)  
    
    Die zweite Protokoll Position, die verglichen werden soll.

#### <a name="return-value"></a>Rückgabewert

Typ: [System. Boolean](/dotnet/api/system.boolean)  
True, wenn LHS vor oder gleich RHS ist.  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[JET_LGPOS Struktur](./jet-lgpos-structure2.md)

[Mitglieder JET_LGPOS](./jet-lgpos-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
