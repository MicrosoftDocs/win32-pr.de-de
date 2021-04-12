---
description: Weitere Informationen finden Sie in der Eigenschaft bytescolumnvalue. length.
title: Bytescolumnvalue. length (Eigenschaft)
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
ms.openlocfilehash: f49b38cdab8d5e4a7b3554651a7dc2f97f651b59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348378"
---
# <a name="bytescolumnvaluelength-property"></a>Bytescolumnvalue. length (Eigenschaft)

Ruft die Byte Länge eines Spaltenwerts ab, der 0 (null) ist, wenn die Spalte NULL ist, andernfalls entspricht der tatsächlichen Länge des Byte Arrays.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

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

Typ: [System. Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Bytescolumnvalue-Klasse](./bytescolumnvalue-class.md)

[Bytescolumnvalue-Member](./bytescolumnvalue-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
