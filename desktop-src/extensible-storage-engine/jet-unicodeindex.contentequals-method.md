---
description: 'Erfahren Sie mehr über: JET_UNICODEINDEX. ContentEquals-Methode'
title: JET_UNICODEINDEX. ContentEquals-Methode
TOCTitle: 'ContentEquals method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_UNICODEINDEX.ContentEquals(Microsoft.Isam.Esent.Interop.JET_UNICODEINDEX)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_unicodeindex.contentequals(v=EXCHG.10)
ms:contentKeyID: 55103987
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_UNICODEINDEX.ContentEquals
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_UNICODEINDEX.ContentEquals
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cdba8d4c1d524f00f5aa399d2fceac9ddbe57b3c7837243be08e001fec2672e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118979029"
---
# <a name="jet_unicodeindexcontentequals-method"></a>JET_UNICODEINDEX. ContentEquals-Methode

Gibt einen Wert zurück, der angibt, ob diese Instanz gleich einer anderen Instanz ist.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Function ContentEquals ( _
    other As JET_UNICODEINDEX _
) As Boolean
'Usage
Dim instance As JET_UNICODEINDEX
Dim other As JET_UNICODEINDEX
Dim returnValue As Boolean

returnValue = instance.ContentEquals(other)
```

``` csharp
public bool ContentEquals(
    JET_UNICODEINDEX other
)
```

#### <a name="parameters"></a>Parameter

  - Sonstige  
    Typ: [Microsoft.Isam.Esent.Interop.JET_UNICODEINDEX](./jet-unicodeindex-class.md)  
    
    Eine -Instanz, die mit dieser Instanz verglichen werden soll.

#### <a name="return-value"></a>Rückgabewert

Typ: [System.Boolean](/dotnet/api/system.boolean)  
True, wenn die beiden Instanzen gleich sind.  

#### <a name="implements"></a>Implementiert

[IContentEquatable \<T\> . ContentEquals(T)](./icontentequatable-t-.contentequals-method.md)  

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[JET_UNICODEINDEX-Klasse](./jet-unicodeindex-class.md)

[JET_UNICODEINDEX-Member](./jet-unicodeindex-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
