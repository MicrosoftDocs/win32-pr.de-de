---
description: 'Weitere Informationen finden Sie unter: JET_ERRINFOBASIC. ContentEquals-Methode'
title: JET_ERRINFOBASIC. ContentEquals-Methode (Microsoft.Isam.Esent.Interop.Windows8)
TOCTitle: 'ContentEquals method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.JET_ERRINFOBASIC.ContentEquals(Microsoft.Isam.Esent.Interop.Windows8.JET_ERRINFOBASIC)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.jet_errinfobasic.contentequals(v=EXCHG.10)
ms:contentKeyID: 55104306
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRINFOBASIC.ContentEquals
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRINFOBASIC.ContentEquals
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b86417db68b6e538e9a3a5ab4300a5f31fb0a2138d7158490c18d5877009c422
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119362410"
---
# <a name="jet_errinfobasiccontentequals-method"></a>JET_ERRINFOBASIC. ContentEquals-Methode

Gibt einen Wert zurück, der angibt, ob diese Instanz gleich einer anderen Instanz ist.

**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Function ContentEquals ( _
    other As JET_ERRINFOBASIC _
) As Boolean
'Usage
Dim instance As JET_ERRINFOBASIC
Dim other As JET_ERRINFOBASIC
Dim returnValue As Boolean

returnValue = instance.ContentEquals(other)
```

``` csharp
public bool ContentEquals(
    JET_ERRINFOBASIC other
)
```

#### <a name="parameters"></a>Parameter

  - Sonstige  
    Typ: [Microsoft.Isam.Esent.Interop.Windows8.JET_ERRINFOBASIC](./jet-errinfobasic-class.md)  
    
    Eine -Instanz, die mit dieser Instanz verglichen werden soll.

#### <a name="return-value"></a>Rückgabewert

Typ: [System.Boolean](/dotnet/api/system.boolean)  
TRUE, wenn die beiden Instanzen gleich sind.  

#### <a name="implements"></a>Implementiert

[IContentEquatable \<T\> . ContentEquals(T)](./icontentequatable-t-.contentequals-method.md)  

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[JET_ERRINFOBASIC-Klasse](./jet-errinfobasic-class.md)

[JET_ERRINFOBASIC Mitglieder](./jet-errinfobasic-members.md)

[Microsoft.Isam.Esent.Interop.Windows8-Namespace](./microsoft.isam.esent.interop.windows8-namespace.md)
