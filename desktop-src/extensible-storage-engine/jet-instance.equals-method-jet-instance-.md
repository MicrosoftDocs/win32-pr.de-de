---
description: 'Weitere Informationen finden Sie hier: JET_INSTANCE. Gleichheits Methode (JET_INSTANCE)'
title: JET_INSTANCE. Gleichheits Methode (JET_INSTANCE)
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
ms.openlocfilehash: be4f2a172da5fc0d7670e7e87464eac04df3cfa3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217254"
---
# <a name="jet_instanceequals-method-jet_instance"></a>JET_INSTANCE. Gleichheits Methode (JET_INSTANCE)

Gibt einen Wert zurück, der angibt, ob diese Instanz gleich einer anderen Instanz ist.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

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

  - andere  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)  
    
    Eine-Instanz, die mit dieser Instanz verglichen werden soll.

#### <a name="return-value"></a>Rückgabewert

Typ: [System. Boolean](/dotnet/api/system.boolean)  
True, wenn die beiden Instanzen gleich sind.  

#### <a name="implements"></a>Implementiert

[IEquatable \<T\> . Ist gleich(T)](/dotnet/api/system.iequatable-1.equals#System_IEquatable_1_Equals__0_)  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[JET_INSTANCE Struktur](./jet-instance-structure.md)

[Mitglieder JET_INSTANCE](./jet-instance-members.md)

[Gleichheits Überladung](./jet-instance.equals-method.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
