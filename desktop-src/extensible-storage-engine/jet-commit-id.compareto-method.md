---
description: Weitere Informationen finden Sie unter JET_COMMIT_ID.CompareTo-Methode.
title: JET_COMMIT_ID.CompareTo-Methode (Microsoft.Isam.Esent.Interop.Windows8)
TOCTitle: 'CompareTo method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.CompareTo(Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.jet_commit_id.compareto(v=EXCHG.10)
ms:contentKeyID: 55104397
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.CompareTo
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.CompareTo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a101cd38eb80598f907068d8fd27d2217ad73db1476dc41d42b2a6caaae3e6ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118766898"
---
# <a name="jet_commit_idcompareto-method"></a>JET_COMMIT_ID.CompareTo-Methode

Gibt einen Wert zurück, der diese Instanz mit einer anderen vergleicht.

**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Function CompareTo ( _
    other As JET_COMMIT_ID _
) As Integer
'Usage
Dim instance As JET_COMMIT_ID
Dim other As JET_COMMIT_ID
Dim returnValue As Integer

returnValue = instance.CompareTo(other)
```

``` csharp
public int CompareTo(
    JET_COMMIT_ID other
)
```

#### <a name="parameters"></a>Parameter

  - Sonstige  
    Typ: [Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)  
    
    Eine -Instanz, die mit dieser Instanz verglichen werden soll.

#### <a name="return-value"></a>Rückgabewert

Typ: [System.Int32](/dotnet/api/system.int32)  
Ein Wert mit Vorzeichen, der die relativen Positionen der -Instanzen darstellt.  

#### <a name="implements"></a>Implementiert

[IComparable \<T\> . CompareTo(T)](/dotnet/api/system.icomparable-1.compareto#System_IComparable_1_CompareTo__0_)  

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[JET_COMMIT_ID-Klasse](./jet-commit-id-class.md)

[JET_COMMIT_ID-Member](./jet-commit-id-members.md)

[Microsoft.Isam.Esent.Interop.Windows8-Namespace](./microsoft.isam.esent.interop.windows8-namespace.md)
