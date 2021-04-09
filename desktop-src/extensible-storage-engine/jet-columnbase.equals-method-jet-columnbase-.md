---
description: 'Weitere Informationen finden Sie hier: JET_COLUMNBASE. Gleichheits Methode (JET_COLUMNBASE)'
title: JET_COLUMNBASE. Gleichheits Methode (JET_COLUMNBASE)
TOCTitle: Equals method (JET_COLUMNBASE)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_COLUMNBASE.Equals(Microsoft.Isam.Esent.Interop.JET_COLUMNBASE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columnbase.equals(v=EXCHG.10)
ms:contentKeyID: 55103355
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
ms.openlocfilehash: ada65f03966ebd5f0bf7142d3953117734c2f3cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868963"
---
# <a name="jet_columnbaseequals-method-jet_columnbase"></a>JET_COLUMNBASE. Gleichheits Methode (JET_COLUMNBASE)

Gibt einen Wert zurück, der angibt, ob diese Instanz gleich einer anderen Instanz ist.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Function Equals ( _
    other As JET_COLUMNBASE _
) As Boolean
'Usage
Dim instance As JET_COLUMNBASE
Dim other As JET_COLUMNBASE
Dim returnValue As Boolean

returnValue = instance.Equals(other)
```

``` csharp
public bool Equals(
    JET_COLUMNBASE other
)
```

#### <a name="parameters"></a>Parameter

  - andere  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNBASE](./jet-columnbase-class.md)  
    
    Eine-Instanz, die mit dieser Instanz verglichen werden soll.

#### <a name="return-value"></a>Rückgabewert

Typ: [System. Boolean](/dotnet/api/system.boolean)  
True, wenn die beiden Instanzen gleich sind.  

#### <a name="implements"></a>Implementiert

[IEquatable \<T\> . Ist gleich(T)](/dotnet/api/system.iequatable-1.equals#System_IEquatable_1_Equals__0_)  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[JET_COLUMNBASE-Klasse](./jet-columnbase-class.md)

[Mitglieder JET_COLUMNBASE](./jet-columnbase-members.md)

[Gleichheits Überladung](./jet-columnbase.equals-method.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
