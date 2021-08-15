---
description: 'Weitere Informationen zu: BytesColumnValue.Length-Eigenschaft'
title: BytesColumnValue.Length-Eigenschaft
TOCTitle: 'Length property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.BytesColumnValue.Length
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.bytescolumnvalue.length(v=EXCHG.10)
ms:contentKeyID: 55107234
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.BytesColumnValue.Length
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.BytesColumnValue.Length
- Microsoft.Isam.Esent.Interop.BytesColumnValue.get_Length
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3951ae20cd8094f543bcb86e1ca9d748f0bb0a601b31beb0f857d3e4e9d5e441
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117901961"
---
# <a name="bytescolumnvaluelength-property"></a>BytesColumnValue.Length-Eigenschaft

Ruft die Bytelänge eines Spaltenwerts ab, der 0 (null) ist, wenn die Spalte NULL ist, andernfalls entspricht sie der tatsächlichen Länge des Bytearrays.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Overrides ReadOnly Property Length As Integer
    Get
'Usage
Dim instance As BytesColumnValue
Dim value As Integer

value = instance.Length
```

``` csharp
public override int Length { get; }
```

#### <a name="property-value"></a>Eigenschaftswert

Typ: [System.Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[BytesColumnValue-Klasse](./bytescolumnvalue-class.md)

[BytesColumnValue-Member](./bytescolumnvalue-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
