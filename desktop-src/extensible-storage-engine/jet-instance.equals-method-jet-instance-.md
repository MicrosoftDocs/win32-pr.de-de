---
description: 'Erfahren Sie mehr über: JET_INSTANCE. Equals-Methode (JET_INSTANCE)'
title: JET_INSTANCE. Equals-Methode (JET_INSTANCE)
TOCTitle: Equals method (JET_INSTANCE)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_INSTANCE.Equals(Microsoft.Isam.Esent.Interop.JET_INSTANCE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_instance.equals(v=EXCHG.10)
ms:contentKeyID: 39512490
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_INSTANCE.Equals
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: dfbafdfdd3a07e9c5911cfefc3e5f7931005ffa508a3e9fcb660f106604877ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118765654"
---
# <a name="jet_instanceequals-method-jet_instance"></a>JET_INSTANCE. Equals-Methode (JET_INSTANCE)

Gibt einen Wert zurück, der angibt, ob diese Instanz gleich einer anderen Instanz ist.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Function Equals ( _
    other As JET_INSTANCE _
) As Boolean
'Usage
Dim instance As JET_INSTANCE
Dim other As JET_INSTANCE
Dim returnValue As Boolean

returnValue = instance.Equals(other)
```

``` csharp
public bool Equals(
    JET_INSTANCE other
)
```

#### <a name="parameters"></a>Parameter

  - Sonstige  
    Typ: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)  
    
    Eine -Instanz, die mit dieser Instanz verglichen werden soll.

#### <a name="return-value"></a>Rückgabewert

Typ: [System.Boolean](/dotnet/api/system.boolean)  
True, wenn die beiden Instanzen gleich sind.  

#### <a name="implements"></a>Implementiert

[IEquatable \<T\> . Equals(T)](/dotnet/api/system.iequatable-1.equals#System_IEquatable_1_Equals__0_)  

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[JET_INSTANCE Struktur](./jet-instance-structure.md)

[JET_INSTANCE-Member](./jet-instance-members.md)

[Equals-Überladung](./jet-instance.equals-method.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
