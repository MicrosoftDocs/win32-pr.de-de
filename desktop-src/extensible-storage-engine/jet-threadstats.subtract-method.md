---
description: 'Weitere Informationen finden Sie unter: JET_THREADSTATS. Subtrahieren der Methode'
title: JET_THREADSTATS. Subtrahieren der Methode (Microsoft.Isam.Esent.Interop.Vista)
TOCTitle: 'Subtract method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Subtract(Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS,Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats.subtract(v=EXCHG.10)
ms:contentKeyID: 39514465
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Subtract
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Subtract
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 443e572afd80b3af28e2a88f84880e8679e8e462b0a7f7540e4a277cfa759941
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118251769"
---
# <a name="jet_threadstatssubtract-method"></a>JET_THREADSTATS. Subtrahieren der Methode

Berechnen Sie die Differenz in Statistiken zwischen zwei JET_THREADSTATS Strukturen.

**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Function Subtract ( _
    t1 As JET_THREADSTATS, _
    t2 As JET_THREADSTATS _
) As JET_THREADSTATS
'Usage
Dim t1 As JET_THREADSTATS
Dim t2 As JET_THREADSTATS
Dim returnValue As JET_THREADSTATS

returnValue = JET_THREADSTATS.Subtract(t1, t2)
```

``` csharp
public static JET_THREADSTATS Subtract(
    JET_THREADSTATS t1,
    JET_THREADSTATS t2
)
```

#### <a name="parameters"></a>Parameter

  - t1  
    Typ: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)  
    
    Die erste JET_THREADSTATS.

<!-- end list -->

  - t2  
    Typ: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)  
    
    Der zweite JET_THREADSTATS.

#### <a name="return-value"></a>Rückgabewert

Typ: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)  
Ein JET_THREADSTATS, der den Unterschied in den Statistiken zwischen t1 und t2 enthält.  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[JET_THREADSTATS-Struktur](./jet-threadstats-structure2.md)

[JET_THREADSTATS Member](./jet-threadstats-members.md)

[Microsoft.Isam.Esent.Interop.Vista-Namespace](./microsoft.isam.esent.interop.vista-namespace.md)
