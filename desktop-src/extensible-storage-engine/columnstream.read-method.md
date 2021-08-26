---
description: 'Weitere Informationen finden Sie unter: ColumnStream.Read-Methode'
title: ColumnStream.Read-Methode
TOCTitle: 'Read method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.ColumnStream.Read(System.Byte[],System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnstream.read(v=EXCHG.10)
ms:contentKeyID: 55100988
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnStream.Read
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnStream.Read
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 34c2bd13a2cc436ea192433e4f70098e328d1658a484c5dca9b092fe18f99a50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119976622"
---
# <a name="columnstreamread-method"></a>ColumnStream.Read-Methode

Liest eine Bytesequenz aus dem aktuellen Stream und setzt die Position in diesem Stream um die Anzahl der gelesenen Bytes nach vorn.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Overrides Function Read ( _
    buffer As Byte(), _
    offset As Integer, _
    count As Integer _
) As Integer
'Usage
Dim instance As ColumnStream
Dim buffer As Byte()
Dim offset As Integer
Dim count As Integer
Dim returnValue As Integer

returnValue = instance.Read(buffer, offset, _
    count)
```

``` csharp
public override int Read(
    byte[] buffer,
    int offset,
    int count
)
```

#### <a name="parameters"></a>Parameter

  - Puffer  
    Typ: \[\]  
    
    Der Puffer, in den gelesen werden soll.

<!-- end list -->

  - offset  
    Typ: [System.Int32](/dotnet/api/system.int32)  
    
    Der Offset im Puffer, in den gelesen werden soll.

<!-- end list -->

  - count  
    Typ: [System.Int32](/dotnet/api/system.int32)  
    
    Die Anzahl der zu lesenden Bytes.

#### <a name="return-value"></a>Rückgabewert

Typ: [System.Int32](/dotnet/api/system.int32)  
Die Anzahl der in den Puffer gelesenen Bytes.  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[ColumnStream-Klasse](./columnstream-class.md)

[ColumnStream-Member](./columnstream-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
