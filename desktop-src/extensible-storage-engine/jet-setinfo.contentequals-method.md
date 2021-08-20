---
description: 'Weitere Informationen finden Sie unter: JET_SETINFO. ContentEquals-Methode'
title: JET_SETINFO. ContentEquals-Methode
TOCTitle: 'ContentEquals method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_SETINFO.ContentEquals(Microsoft.Isam.Esent.Interop.JET_SETINFO)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_setinfo.contentequals(v=EXCHG.10)
ms:contentKeyID: 55103913
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SETINFO.ContentEquals
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SETINFO.ContentEquals
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2cebf96a77bb88bda982f1333d86bdc5905f6d38937db1b66102e645682e33e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117892715"
---
# <a name="jet_setinfocontentequals-method"></a>JET_SETINFO. ContentEquals-Methode

Gibt einen Wert zurück, der angibt, ob diese Instanz gleich einer anderen Instanz ist.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Function ContentEquals ( _
    other As JET_SETINFO _
) As Boolean
'Usage
Dim instance As JET_SETINFO
Dim other As JET_SETINFO
Dim returnValue As Boolean

returnValue = instance.ContentEquals(other)
```

``` csharp
public bool ContentEquals(
    JET_SETINFO other
)
```

#### <a name="parameters"></a>Parameter

  - Andere  
    Typ: [Microsoft.Isam.Esent.Interop.JET_SETINFO](./jet-setinfo-class.md)  
    
    Eine -Instanz, die mit dieser Instanz verglichen werden soll.

#### <a name="return-value"></a>Rückgabewert

Typ: [System.Boolean](/dotnet/api/system.boolean)  
TRUE, wenn die beiden Instanzen gleich sind.  

#### <a name="implements"></a>Implementiert

[IContentEquatable \<T\> . ContentEquals(T)](./icontentequatable-t-.contentequals-method.md)  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[JET_SETINFO-Klasse](./jet-setinfo-class.md)

[JET_SETINFO Mitglieder](./jet-setinfo-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
