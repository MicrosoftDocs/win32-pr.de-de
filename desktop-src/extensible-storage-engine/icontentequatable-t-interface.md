---
description: 'Weitere Informationen finden Sie unter: icontentequatable <T> Interface'
title: Icontentequatable (T)-Schnittstelle
TOCTitle: IContentEquatable(T) interface
ms:assetid: T:Microsoft.Isam.Esent.Interop.IContentEquatable`1
ms:mtpsurl: https://msdn.microsoft.com/library/Hh578046(v=EXCHG.10)
ms:contentKeyID: 39511318
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.IContentEquatable`1
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.IContentEquatable`1
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 02e237714f020f5bafa3ce8b7465f1c8e2615c01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345208"
---
# <a name="icontentequatablet-interface"></a>Icontentequatable- \<T\> Schnittstelle

Eine Schnittstelle für Objekte, deren Inhalt miteinander verglichen werden kann. Dies sollte für Gleichheits Vergleiche bei änderbaren Verweis Objekten verwendet werden, bei denen das Überschreiben von "gleich" () und "GetHashCode ()" keine gute Idee ist.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Interface IContentEquatable(Of T)
'Usage
Dim instance As IContentEquatable(Of T)
```

``` csharp
public interface IContentEquatable<T>
```

#### <a name="type-parameters"></a>Typparameter

  - T  
    Der Typ der Objekte, die zusammen geschrieben werden sollen.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Icontentequatable \<T\> -Member](./icontentequatable-t-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
