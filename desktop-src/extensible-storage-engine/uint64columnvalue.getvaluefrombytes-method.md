---
description: 'Weitere Informationen finden Sie unter: UInt64ColumnValue.GetValueFromBytes-Methode'
title: UInt64ColumnValue.GetValueFromBytes-Methode
TOCTitle: 'GetValueFromBytes method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.UInt64ColumnValue.GetValueFromBytes(System.Byte[],System.Int32,System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.uint64columnvalue.getvaluefrombytes(v=EXCHG.10)
ms:contentKeyID: 55104084
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.UInt64ColumnValue.GetValueFromBytes
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.UInt64ColumnValue.GetValueFromBytes
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f34d5b8a96e8c838176f099112371ccb736248e794678c145a24a0f57a67d29c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118978300"
---
# <a name="uint64columnvaluegetvaluefrombytes-method"></a>UInt64ColumnValue.GetValueFromBytes-Methode

Decodieren Sie die Daten mit den aus ESENT abgerufenen Daten, und legen Sie den Wert im ColumnValue-Objekt fest.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Protected Overrides Sub GetValueFromBytes ( _
    value As Byte(), _
    startIndex As Integer, _
    count As Integer, _
    err As Integer _
)
'Usage
Dim value As Byte()
Dim startIndex As Integer
Dim count As Integer
Dim err As Integer

Me.GetValueFromBytes(value, startIndex, _
    count, err)
```

``` csharp
protected override void GetValueFromBytes(
    byte[] value,
    int startIndex,
    int count,
    int err
)
```

#### <a name="parameters"></a>Parameter

  - value  
    Typ: \[\]  
    
    Ein Bytearray.

<!-- end list -->

  - startIndex  
    Typ: [System.Int32](/dotnet/api/system.int32)  
    
    Die Anfangsposition innerhalb der Bytes.

<!-- end list -->

  - count  
    Typ: [System.Int32](/dotnet/api/system.int32)  
    
    Die Anzahl der zu decodierenden Bytes.

<!-- end list -->

  - Err  
    Typ: [System.Int32](/dotnet/api/system.int32)  
    
    Der von ESENT zurückgegebene Fehler.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[UInt64ColumnValue-Klasse](./uint64columnvalue-class.md)

[UInt64ColumnValue-Member](./uint64columnvalue-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
