---
description: 'Erfahren Sie mehr über: JET_OSSNAPID. Gleichheitsoperator'
title: JET_OSSNAPID. Gleichheitsoperator
TOCTitle: 'Equality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_OSSNAPID.op_Equality(Microsoft.Isam.Esent.Interop.JET_OSSNAPID,Microsoft.Isam.Esent.Interop.JET_OSSNAPID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_ossnapid.op_equality(v=EXCHG.10)
ms:contentKeyID: 39513985
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_OSSNAPID.Equality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_OSSNAPID.op_Equality
- Microsoft.Isam.Esent.Interop.JET_OSSNAPID.Equality
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5512a41505d9af0a995e0f2dcf16662bfd6abe4e9ba1cf79c21a1265d95bce48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119107684"
---
# <a name="jet_ossnapidequality-operator"></a>JET_OSSNAPID. Gleichheitsoperator

Bestimmt, ob zwei angegebene Instanzen von JET_OSSNAPID gleich sind.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Operator = ( _
    lhs As JET_OSSNAPID, _
    rhs As JET_OSSNAPID _
) As Boolean
'Usage
Dim lhs As JET_OSSNAPID
Dim rhs As JET_OSSNAPID
Dim returnValue As Boolean

returnValue = (lhs = rhs)
```

``` csharp
public static bool operator ==(
    JET_OSSNAPID lhs,
    JET_OSSNAPID rhs
)
```

#### <a name="parameters"></a>Parameter

  - Lhs  
    Typ: [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)  
    
    Die erste zu vergleichende Instanz.

<!-- end list -->

  - rhs  
    Typ: [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)  
    
    Die zweite zu vergleichende Instanz.

#### <a name="return-value"></a>Rückgabewert

Typ: [System.Boolean](/dotnet/api/system.boolean)  
True, wenn die beiden Instanzen gleich sind.  

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[JET_OSSNAPID-Struktur](./jet-ossnapid-structure.md)

[JET_OSSNAPID-Member](./jet-ossnapid-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
