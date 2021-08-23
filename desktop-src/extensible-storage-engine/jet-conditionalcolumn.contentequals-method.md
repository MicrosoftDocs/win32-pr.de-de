---
description: 'Erfahren Sie mehr über: JET_CONDITIONALCOLUMN. ContentEquals-Methode'
title: JET_CONDITIONALCOLUMN. ContentEquals-Methode
TOCTitle: 'ContentEquals method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_CONDITIONALCOLUMN.ContentEquals(Microsoft.Isam.Esent.Interop.JET_CONDITIONALCOLUMN)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_conditionalcolumn.contentequals(v=EXCHG.10)
ms:contentKeyID: 55103531
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_CONDITIONALCOLUMN.ContentEquals
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_CONDITIONALCOLUMN.ContentEquals
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3ed50b5951cb255fcdc21854df6bcd0a3865e8efc54f8d9587454c3abc434b9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118766557"
---
# <a name="jet_conditionalcolumncontentequals-method"></a>JET_CONDITIONALCOLUMN. ContentEquals-Methode

Gibt einen Wert zurück, der angibt, ob diese Instanz gleich einer anderen Instanz ist.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Function ContentEquals ( _
    other As JET_CONDITIONALCOLUMN _
) As Boolean
'Usage
Dim instance As JET_CONDITIONALCOLUMN
Dim other As JET_CONDITIONALCOLUMN
Dim returnValue As Boolean

returnValue = instance.ContentEquals(other)
```

``` csharp
public bool ContentEquals(
    JET_CONDITIONALCOLUMN other
)
```

#### <a name="parameters"></a>Parameter

  - Sonstige  
    Typ: [Microsoft.Isam.Esent.Interop.JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-class.md)  
    
    Eine -Instanz, die mit dieser Instanz verglichen werden soll.

#### <a name="return-value"></a>Rückgabewert

Typ: [System.Boolean](/dotnet/api/system.boolean)  
True, wenn die beiden Instanzen gleich sind.  

#### <a name="implements"></a>Implementiert

[IContentEquatable \<T\> . ContentEquals(T)](./icontentequatable-t-.contentequals-method.md)  

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[JET_CONDITIONALCOLUMN-Klasse](./jet-conditionalcolumn-class.md)

[JET_CONDITIONALCOLUMN-Member](./jet-conditionalcolumn-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
