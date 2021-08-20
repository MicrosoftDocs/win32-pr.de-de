---
description: 'Weitere Informationen finden Sie unter: JET_SESID. Gleichheitsoperator'
title: JET_SESID. Gleichheitsoperator
TOCTitle: 'Equality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_SESID.op_Equality(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_SESID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_sesid.op_equality(v=EXCHG.10)
ms:contentKeyID: 39511173
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SESID.Equality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SESID.Equality
- Microsoft.Isam.Esent.Interop.JET_SESID.op_Equality
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5d6137ad066dd92afdce6dcf41e748ca34b3c17d4a52d437781fda69c5c6d851
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119945350"
---
# <a name="jet_sesidequality-operator"></a>JET_SESID. Gleichheitsoperator

Bestimmt, ob zwei angegebene Instanzen JET_SESID gleich sind.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Operator = ( _
    lhs As JET_SESID, _
    rhs As JET_SESID _
) As Boolean
'Usage
Dim lhs As JET_SESID
Dim rhs As JET_SESID
Dim returnValue As Boolean

returnValue = (lhs = rhs)
```

``` csharp
public static bool operator ==(
    JET_SESID lhs,
    JET_SESID rhs
)
```

#### <a name="parameters"></a>Parameter

  - Lhs  
    Typ: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Die erste zu vergleichende Instanz.

<!-- end list -->

  - rhs  
    Typ: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Die zweite zu vergleichende Instanz.

#### <a name="return-value"></a>Rückgabewert

Typ: [System.Boolean](/dotnet/api/system.boolean)  
TRUE, wenn die beiden Instanzen gleich sind.  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[JET_SESID-Struktur](./jet-sesid-structure.md)

[JET_SESID Member](./jet-sesid-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
