---
description: Weitere Informationen finden Sie in der columnvalueof-Struktur <T> . Length-Eigenschaft
title: Columnvalueobstruct (T). Length-Eigenschaft
TOCTitle: 'Length property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.ColumnValueOfStruct`1.Length
ms:mtpsurl: https://msdn.microsoft.com/library/Dn334225(v=EXCHG.10)
ms:contentKeyID: 55101009
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnValueOfStruct`1.Length
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnValueOfStruct`1.get_Length
- Microsoft.Isam.Esent.Interop.ColumnValueOfStruct`1.Length
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ae3c67ba3dfbdcf8c72e04e75185c835c290e21b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527554"
---
# <a name="columnvalueofstructtlength-property"></a>Columnvalueof-Struktur \<T\> . Length-Eigenschaft

Ruft die Byte Länge eines Spaltenwerts ab, der 0 (null) ist, wenn die Spalte NULL ist. andernfalls entspricht Sie der Größe dieser Spalte mit fester Größe.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Overrides ReadOnly Property Length As Integer
    Get
'Usage
Dim instance As ColumnValueOfStruct
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

[Columnvalueosstruct- \<T\> Klasse](./columnvalueofstruct-t-class.md)

[Columnvalueofstruct \<T\> -Member](./columnvalueofstruct-t-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
