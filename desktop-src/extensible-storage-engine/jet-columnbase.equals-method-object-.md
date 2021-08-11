---
description: 'Weitere Informationen finden Sie unter: JET_COLUMNBASE. Equals-Methode (Objekt)'
title: JET_COLUMNBASE. Equals-Methode (Objekt)
TOCTitle: Equals method (Object)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_COLUMNBASE.Equals(System.Object)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columnbase.equals(v=EXCHG.10)
ms:contentKeyID: 55103438
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNBASE.Equals
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2bff106c0988fa60b5d6d2ae45b5d132e6e4e22ff9ac387c217e192b1d9f0a0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118255096"
---
# <a name="jet_columnbaseequals-method-object"></a>JET_COLUMNBASE. Equals-Methode (Objekt)

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
Dim instance As JET_COLUMNBASE
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
TRUE, wenn die beiden Instanzen gleich sind.  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[JET_COLUMNBASE-Klasse](./jet-columnbase-class.md)

[JET_COLUMNBASE Member](./jet-columnbase-members.md)

[Equals-Überladung](./jet-columnbase.equals-method.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
