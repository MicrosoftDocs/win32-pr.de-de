---
description: 'Erfahren Sie mehr über: JET_HANDLE. Equals-Methode (Objekt)'
title: JET_HANDLE. Equals-Methode (Objekt)
TOCTitle: Equals method (Object)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_HANDLE.Equals(System.Object)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_handle.equals(v=EXCHG.10)
ms:contentKeyID: 39515621
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_HANDLE.Equals
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ccc0d0eb5bbfc1955a3e9a793886dc2c49f91363ae5e0820879895a861d0a8c9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119362200"
---
# <a name="jet_handleequals-method-object"></a>JET_HANDLE. Equals-Methode (Objekt)

Gibt einen Wert zurück, der angibt, ob diese Instanz gleich einer anderen Instanz ist.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Overrides Function Equals ( _
    obj As Object _
) As Boolean
'Usage
Dim instance As JET_HANDLE
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
    
    Ein Objekt, das mit dieser Instanz verglichen werden soll.

#### <a name="return-value"></a>Rückgabewert

Typ: [System.Boolean](/dotnet/api/system.boolean)  
True, wenn die beiden Instanzen gleich sind.  

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[JET_HANDLE-Struktur](./jet-handle-structure.md)

[JET_HANDLE-Member](./jet-handle-members.md)

[Equals-Überladung](./jet-handle.equals-method.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
