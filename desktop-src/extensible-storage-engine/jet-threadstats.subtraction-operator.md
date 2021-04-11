---
description: 'Weitere Informationen finden Sie hier: JET_THREADSTATS. Subtraktions Operator'
title: JET_THREADSTATS. Subtraktions Operator (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: 'Subtraction operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.op_Subtraction(Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS,Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats.op_subtraction(v=EXCHG.10)
ms:contentKeyID: 39512217
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Subtraction
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.op_Subtraction
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Subtraction
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5a41455f05b91a582a1d8aae824ca5b426628cf1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214387"
---
# <a name="jet_threadstatssubtraction-operator"></a>JET_THREADSTATS. Subtraktions Operator

Berechnen Sie den Unterschied in den Statistiken zwischen zwei JET_THREADSTATS Strukturen.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Operator - ( _
    t1 As JET_THREADSTATS, _
    t2 As JET_THREADSTATS _
) As JET_THREADSTATS
'Usage
Dim t1 As JET_THREADSTATS
Dim t2 As JET_THREADSTATS
Dim returnValue As JET_THREADSTATS

returnValue = (t1 - t2)
```

``` csharp
public static JET_THREADSTATS operator -(
    JET_THREADSTATS t1,
    JET_THREADSTATS t2
)
```

#### <a name="parameters"></a>Parameter

  - t1  
    Typ: [Microsoft.ISAM.ESENT.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)  
    
    Der erste JET_THREADSTATS.

<!-- end list -->

  - T2  
    Typ: [Microsoft.ISAM.ESENT.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)  
    
    Der zweite JET_THREADSTATS.

#### <a name="return-value"></a>Rückgabewert

Typ: [Microsoft.ISAM.ESENT.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)  
Eine JET_THREADSTATS, die den Unterschied in den Statistiken zwischen T1 und T2 enthält.  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[JET_THREADSTATS Struktur](./jet-threadstats-structure2.md)

[Mitglieder JET_THREADSTATS](./jet-threadstats-members.md)

[Microsoft. ISAM. ESENT. Interop. Vista-Namespace](./microsoft.isam.esent.interop.vista-namespace.md)
