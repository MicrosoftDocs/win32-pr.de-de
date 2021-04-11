---
description: 'Weitere Informationen finden Sie hier: JET_DBINFOMISC. Gleichheits Methode (JET_DBINFOMISC)'
title: JET_DBINFOMISC. Gleichheits Methode (JET_DBINFOMISC)
TOCTitle: Equals method (JET_DBINFOMISC)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.Equals(Microsoft.Isam.Esent.Interop.JET_DBINFOMISC)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbinfomisc.equals(v=EXCHG.10)
ms:contentKeyID: 39514332
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.Equals
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bbe29fe112b82b5c88673d9301b3feb4b0c94536
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128245"
---
# <a name="jet_dbinfomiscequals-method-jet_dbinfomisc"></a>JET_DBINFOMISC. Gleichheits Methode (JET_DBINFOMISC)

Gibt an, ob das aktuelle Objekt gleich einem anderen Objekt des gleichen Typs ist.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Function Equals ( _
    other As JET_DBINFOMISC _
) As Boolean
'Usage
Dim instance As JET_DBINFOMISC
Dim other As JET_DBINFOMISC
Dim returnValue As Boolean

returnValue = instance.Equals(other)
```

``` csharp
public bool Equals(
    JET_DBINFOMISC other
)
```

#### <a name="parameters"></a>Parameter

  - andere  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_DBINFOMISC](./jet-dbinfomisc-class.md)  
    
    Ein Objekt, das mit diesem Objekt verglichen werden soll.

#### <a name="return-value"></a>Rückgabewert

Typ: [System. Boolean](/dotnet/api/system.boolean)  
True, wenn das aktuelle Objekt gleich dem anderen Parameter ist. andernfalls false.  

#### <a name="implements"></a>Implementiert

[IEquatable \<T\> . Ist gleich(T)](/dotnet/api/system.iequatable-1.equals#System_IEquatable_1_Equals__0_)  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[JET_DBINFOMISC-Klasse](./jet-dbinfomisc-class.md)

[Mitglieder JET_DBINFOMISC](./jet-dbinfomisc-members.md)

[Gleichheits Überladung](./jet-dbinfomisc.equals-method.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
