---
description: 'Weitere Informationen finden Sie hier: JET_SETCOLUMN. Contentequals-Methode'
title: JET_SETCOLUMN. Contentequals-Methode
TOCTitle: 'ContentEquals method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_SETCOLUMN.ContentEquals(Microsoft.Isam.Esent.Interop.JET_SETCOLUMN)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_setcolumn.contentequals(v=EXCHG.10)
ms:contentKeyID: 55103936
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SETCOLUMN.ContentEquals
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SETCOLUMN.ContentEquals
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 489d42a72033ba942a359d8f3244b154dae9e3c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041643"
---
# <a name="jet_setcolumncontentequals-method"></a>JET_SETCOLUMN. Contentequals-Methode

Gibt einen Wert zurück, der angibt, ob diese Instanz gleich einer anderen Instanz ist.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Function ContentEquals ( _
    other As JET_SETCOLUMN _
) As Boolean
'Usage
Dim instance As JET_SETCOLUMN
Dim other As JET_SETCOLUMN
Dim returnValue As Boolean

returnValue = instance.ContentEquals(other)
```

``` csharp
public bool ContentEquals(
    JET_SETCOLUMN other
)
```

#### <a name="parameters"></a>Parameter

  - andere  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_SETCOLUMN](./jet-setcolumn-class.md)  
    
    Eine-Instanz, die mit dieser Instanz verglichen werden soll.

#### <a name="return-value"></a>Rückgabewert

Typ: [System. Boolean](/dotnet/api/system.boolean)  
True, wenn die beiden Instanzen gleich sind.  

#### <a name="implements"></a>Implementiert

[Icontentequatable \<T\> . Contentequals (T)](./icontentequatable-t-.contentequals-method.md)  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[JET_SETCOLUMN-Klasse](./jet-setcolumn-class.md)

[Mitglieder JET_SETCOLUMN](./jet-setcolumn-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
