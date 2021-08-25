---
description: Weitere Informationen finden Sie unter ColumnValueOfStruct. <T> Length-Eigenschaft
title: ColumnValueOfStruct(T). Length-Eigenschaft
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
ms.openlocfilehash: adbd9a120fca578d2908ec1e98f467c6ce622dbcb16095653a08b81be35c4985
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120066930"
---
# <a name="columnvalueofstructtlength-property"></a>ColumnValueOfStruct \<T\> . Length-Eigenschaft

Ruft die Bytelänge eines Spaltenwerts ab, der 0 (null) ist, wenn die Spalte NULL ist, andernfalls entspricht sie der Größe für diese Spalte mit fester Größe.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

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

Typ: [System.Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[ColumnValueOfStruct-Klasse \<T\>](./columnvalueofstruct-t-class.md)

[ColumnValueOfStruct-Elemente \<T\>](./columnvalueofstruct-t-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
