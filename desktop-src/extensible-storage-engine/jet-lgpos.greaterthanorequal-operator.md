---
description: 'Weitere Informationen finden Sie unter: JET_LGPOS. GreaterThanOrEqual-Operator'
title: JET_LGPOS. GreaterThanOrEqual-Operator
TOCTitle: 'GreaterThanOrEqual operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_LGPOS.op_GreaterThanOrEqual(Microsoft.Isam.Esent.Interop.JET_LGPOS,Microsoft.Isam.Esent.Interop.JET_LGPOS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_lgpos.op_greaterthanorequal(v=EXCHG.10)
ms:contentKeyID: 39510730
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_LGPOS.GreaterThanOrEqual
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_LGPOS.GreaterThanOrEqual
- Microsoft.Isam.Esent.Interop.JET_LGPOS.op_GreaterThanOrEqual
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ef9f6835d4c65d08eeb6b3765bd5f2319048986daac439b7b2059b02ecf9735a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119109267"
---
# <a name="jet_lgposgreaterthanorequal-operator"></a>JET_LGPOS. GreaterThanOrEqual-Operator

Bestimmen Sie, ob eine Protokollposition hinter oder gleich einer anderen Protokollposition liegt.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Operator >= ( _
    lhs As JET_LGPOS, _
    rhs As JET_LGPOS _
) As Boolean
'Usage
Dim lhs As JET_LGPOS
Dim rhs As JET_LGPOS
Dim returnValue As Boolean

returnValue = (lhs >= rhs)
```

``` csharp
public static bool operator >=(
    JET_LGPOS lhs,
    JET_LGPOS rhs
)
```

#### <a name="parameters"></a>Parameter

  - Lhs  
    Typ: [Microsoft.Isam.Esent.Interop.JET_LGPOS](./jet-lgpos-structure2.md)  
    
    Die erste zu vergleichende Protokollposition.

<!-- end list -->

  - rhs  
    Typ: [Microsoft.Isam.Esent.Interop.JET_LGPOS](./jet-lgpos-structure2.md)  
    
    Die zweite zu vergleichende Protokollposition.

#### <a name="return-value"></a>Rückgabewert

Typ: [System.Boolean](/dotnet/api/system.boolean)  
True, wenn ls nach oder gleich rhs ist.  

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[JET_LGPOS-Struktur](./jet-lgpos-structure2.md)

[JET_LGPOS Member](./jet-lgpos-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
