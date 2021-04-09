---
description: 'Weitere Informationen finden Sie hier: JET_COLUMNDEF. Contentequals-Methode'
title: JET_COLUMNDEF. Contentequals-Methode
TOCTitle: 'ContentEquals method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_COLUMNDEF.ContentEquals(Microsoft.Isam.Esent.Interop.JET_COLUMNDEF)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columndef.contentequals(v=EXCHG.10)
ms:contentKeyID: 55103479
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_COLUMNDEF.ContentEquals
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNDEF.ContentEquals
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7f4527edef1fd8567ec3f4973dddc67548e79946
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130181"
---
# <a name="jet_columndefcontentequals-method"></a>JET_COLUMNDEF. Contentequals-Methode

Gibt einen Wert zurück, der angibt, ob diese Instanz gleich einer anderen Instanz ist.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Function ContentEquals ( _
    other As JET_COLUMNDEF _
) As Boolean
'Usage
Dim instance As JET_COLUMNDEF
Dim other As JET_COLUMNDEF
Dim returnValue As Boolean

returnValue = instance.ContentEquals(other)
```

``` csharp
public bool ContentEquals(
    JET_COLUMNDEF other
)
```

#### <a name="parameters"></a>Parameter

  - andere  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNDEF](./jet-columndef-class.md)  
    
    Eine-Instanz, die mit dieser Instanz verglichen werden soll.

#### <a name="return-value"></a>Rückgabewert

Typ: [System. Boolean](/dotnet/api/system.boolean)  
True, wenn die beiden Instanzen gleich sind.  

#### <a name="implements"></a>Implementiert

[Icontentequatable \<T\> . Contentequals (T)](./icontentequatable-t-.contentequals-method.md)  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[JET_COLUMNDEF-Klasse](./jet-columndef-class.md)

[Mitglieder JET_COLUMNDEF](./jet-columndef-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
