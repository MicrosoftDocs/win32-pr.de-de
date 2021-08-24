---
description: 'Weitere Informationen finden Sie unter: JET_DBINFOMISC. Equals-Methode (Objekt)'
title: JET_DBINFOMISC. Equals-Methode (Objekt)
TOCTitle: Equals method (Object)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.Equals(System.Object)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbinfomisc.equals(v=EXCHG.10)
ms:contentKeyID: 39513216
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.Equals
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 46be2130cbb57cc216f570e944d6959ae355780134f90bc94101d01d6f38bb16
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119617600"
---
# <a name="jet_dbinfomiscequals-method-object"></a>JET_DBINFOMISC. Equals-Methode (Objekt)

Bestimmt, ob das [angegebene Objekt](/dotnet/api/system.object) gleich dem aktuellen [Object ist.](/dotnet/api/system.object)

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Overrides Function Equals ( _
    obj As Object _
) As Boolean
'Usage
Dim instance As JET_DBINFOMISC
Dim obj As Object
Dim returnValue As Boolean

returnValue = instance.Equals(obj)
```

``` csharp
public override bool Equals(
    Object obj
)
```

#### <a name="parameters"></a>Parameter

  - obj  
    Typ: [System.Object](/dotnet/api/system.object)  
    
    Das [Objekt,](/dotnet/api/system.object) das mit dem aktuellen Objekt verglichen [werden soll.](/dotnet/api/system.object)

#### <a name="return-value"></a>Rückgabewert

Typ: [System.Boolean](/dotnet/api/system.boolean)  
TRUE, wenn das [angegebene Objekt](/dotnet/api/system.object) gleich dem aktuellen [Object ist;](/dotnet/api/system.object) andernfalls FALSE.  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[JET_DBINFOMISC-Klasse](./jet-dbinfomisc-class.md)

[JET_DBINFOMISC Member](./jet-dbinfomisc-members.md)

[Equals-Überladung](./jet-dbinfomisc.equals-method.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
