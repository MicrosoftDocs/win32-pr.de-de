---
description: 'Weitere Informationen zu: columnstream. Seek-Methode'
title: Columnstream. Seek-Methode
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
ms.openlocfilehash: d5489bb0ee9a4a1550166e14a945a2a6d58c45af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527560"
---
# <a name="columnstreamseek-method"></a>Columnstream. Seek-Methode

Legt die Position im aktuellen Stream fest.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

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
    Typ: [System. Int64](/dotnet/api/system.int64)  
    
    Byte Offset relativ zum Ursprungs Parameter.

<!-- end list -->

  - Origin  
    Typ: [System. IO. SeekOrigin](/dotnet/api/system.io.seekorigin)  
    
    Ein SeekOrigin, der den Bezugspunkt für die neue Position angibt.

#### <a name="return-value"></a>Rückgabewert

Typ: [System. Int64](/dotnet/api/system.int64)  
Die neue Position im aktuellen Stream.  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Columnstream-Klasse](./columnstream-class.md)

[Columnstream-Member](./columnstream-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
