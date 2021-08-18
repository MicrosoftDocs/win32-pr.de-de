---
description: Weitere Informationen finden Sie unter ColumnStream.Seek-Methode.
title: ColumnStream.Seek-Methode
TOCTitle: 'Seek method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.ColumnStream.Seek(System.Int64,System.IO.SeekOrigin)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnstream.seek(v=EXCHG.10)
ms:contentKeyID: 55100949
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnStream.Seek
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnStream.Seek
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 883739bed33c17877dc86c33670233aab1afc67e9348009bb11c4e67ab27011c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119738190"
---
# <a name="columnstreamseek-method"></a>ColumnStream.Seek-Methode

Legt die Position im aktuellen Stream fest.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Overrides Function Seek ( _
    offset As Long, _
    origin As SeekOrigin _
) As Long
'Usage
Dim instance As ColumnStream
Dim offset As Long
Dim origin As SeekOrigin
Dim returnValue As Long

returnValue = instance.Seek(offset, origin)
```

``` csharp
public override long Seek(
    long offset,
    SeekOrigin origin
)
```

#### <a name="parameters"></a>Parameter

  - offset  
    Typ: [System.Int64](/dotnet/api/system.int64)  
    
    Byteoffset relativ zum Ursprungsparameter.

<!-- end list -->

  - Origin  
    Typ: [System.IO.SeekOrigin](/dotnet/api/system.io.seekorigin)  
    
    Ein SeekOrigin-Zeichen, das den Verweispunkt für die neue Position angibt.

#### <a name="return-value"></a>Rückgabewert

Typ: [System.Int64](/dotnet/api/system.int64)  
Die neue Position im aktuellen Stream.  

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[ColumnStream-Klasse](./columnstream-class.md)

[ColumnStream-Elemente](./columnstream-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
