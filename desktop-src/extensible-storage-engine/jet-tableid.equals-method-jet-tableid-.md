---
description: 'Weitere Informationen finden Sie unter: JET_TABLEID. Equals-Methode (JET_TABLEID)'
title: JET_TABLEID. Equals-Methode (JET_TABLEID)
TOCTitle: Equals method (JET_TABLEID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_TABLEID.Equals(Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_tableid.equals(v=EXCHG.10)
ms:contentKeyID: 39514708
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_TABLEID.Equals
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f4c794e07efd291ddbf75ce5ab697d61f9ebed0db5a3e5ce66aef561fe91fc26
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119890000"
---
# <a name="jet_tableidequals-method-jet_tableid"></a>JET_TABLEID. Equals-Methode (JET_TABLEID)

Gibt einen Wert zurück, der angibt, ob diese Instanz gleich einer anderen Instanz ist.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Function Equals ( _
    other As JET_TABLEID _
) As Boolean
'Usage
Dim instance As JET_TABLEID
Dim other As JET_TABLEID
Dim returnValue As Boolean

returnValue = instance.Equals(other)
```

``` csharp
public bool Equals(
    JET_TABLEID other
)
```

#### <a name="parameters"></a>Parameter

  - Sonstige  
    Typ: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Eine -Instanz, die mit dieser Instanz verglichen werden soll.

#### <a name="return-value"></a>Rückgabewert

Typ: [System.Boolean](/dotnet/api/system.boolean)  
TRUE, wenn die beiden Instanzen gleich sind.  

#### <a name="implements"></a>Implementiert

[IEquatable \<T\> . Equals(T)](/dotnet/api/system.iequatable-1.equals#System_IEquatable_1_Equals__0_)  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[JET_TABLEID-Struktur](./jet-tableid-structure.md)

[JET_TABLEID Mitglieder](./jet-tableid-members.md)

[Equals-Überladung](./jet-tableid.equals-method.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
