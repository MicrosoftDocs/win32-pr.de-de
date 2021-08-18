---
description: Weitere Informationen zur ColumnStream.Position-Eigenschaft
title: ColumnStream.Position-Eigenschaft
TOCTitle: 'Position property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.ColumnStream.Position
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnstream.position(v=EXCHG.10)
ms:contentKeyID: 55100958
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnStream.Position
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnStream.get_Position
- Microsoft.Isam.Esent.Interop.ColumnStream.set_Position
- Microsoft.Isam.Esent.Interop.ColumnStream.Position
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0f5a3709224e2c231ea35b53d2af823d19ec083974a0fbb4acd7a124d35153f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118982630"
---
# <a name="columnstreamposition-property"></a>ColumnStream.Position-Eigenschaft

Ruft die aktuelle Position im Stream ab oder legt diese fest.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Overrides Property Position As Long
    Get
    Set
'Usage
Dim instance As ColumnStream
Dim value As Long

value = instance.Position

instance.Position = value
```

``` csharp
public override long Position { get; set; }
```

#### <a name="property-value"></a>Eigenschaftswert

Typ: [System.Int64](/dotnet/api/system.int64)  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[ColumnStream-Klasse](./columnstream-class.md)

[ColumnStream-Member](./columnstream-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
