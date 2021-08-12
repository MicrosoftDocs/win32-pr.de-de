---
description: 'Erfahren Sie mehr über: IContentEquatable <T> . ContentEquals-Methode'
title: IContentEquatable(T). ContentEquals-Methode
TOCTitle: 'ContentEquals method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.IContentEquatable`1.ContentEquals(`0)
ms:mtpsurl: https://msdn.microsoft.com/library/Hh538970(v=EXCHG.10)
ms:contentKeyID: 39509953
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.IContentEquatable`1.ContentEquals
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.IContentEquatable`1.ContentEquals
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9cee5c5cce2d915b8afb99c794b005b815e696e8488055e385cb49cdfe1ce024
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118256060"
---
# <a name="icontentequatabletcontentequals-method"></a>IContentEquatable \<T\> . ContentEquals-Methode

Gibt einen Wert zurück, der angibt, ob diese Instanz gleich einer anderen Instanz ist.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Function ContentEquals ( _
    other As T _
) As Boolean
'Usage
Dim instance As IContentEquatable
Dim other As T
Dim returnValue As Boolean

returnValue = instance.ContentEquals(other)
```

``` csharp
bool ContentEquals(
    T other
)
```

#### <a name="parameters"></a>Parameter

  - Sonstige  
    Typ: [T](./icontentequatable-t-interface.md)  
    
    Eine -Instanz, die mit dieser Instanz verglichen werden soll.

#### <a name="return-value"></a>Rückgabewert

Typ: [System.Boolean](/dotnet/api/system.boolean)  
True, wenn die beiden Instanzen gleich sind.  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[IContentEquatable-Schnittstelle \<T\>](./icontentequatable-t-interface.md)

[IContentEquatable-Member \<T\>](./icontentequatable-t-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
