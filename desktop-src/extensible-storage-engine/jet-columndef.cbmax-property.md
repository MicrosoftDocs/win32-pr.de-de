---
description: 'Weitere Informationen zu: JET_COLUMNDEF.cbMax-Eigenschaft'
title: JET_COLUMNDEF.cbMax-Eigenschaft
TOCTitle: 'cbMax property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_COLUMNDEF.cbMax
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columndef.cbmax(v=EXCHG.10)
ms:contentKeyID: 55103491
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_COLUMNDEF.cbMax
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNDEF.cbMax
- Microsoft.Isam.Esent.Interop.JET_COLUMNDEF.get_cbMax
- Microsoft.Isam.Esent.Interop.JET_COLUMNDEF.set_cbMax
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 760d55f40eb6c95e432e72b7dac412d2f8d912a9736acffcacba9d25804fb53c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119112399"
---
# <a name="jet_columndefcbmax-property"></a>JET_COLUMNDEF.cbMax-Eigenschaft

Ruft die maximale Länge der Spalte ab oder legt sie fest. Dies ist nur für Spalten vom Typ [Text](./jet-coltyp-enumeration.md), [LongText](./jet-coltyp-enumeration.md), [Binary](./jet-coltyp-enumeration.md) und [LongBinary](./jet-coltyp-enumeration.md)sinnvoll.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property cbMax As Integer
    Get
    Set
'Usage
Dim instance As JET_COLUMNDEF
Dim value As Integer

value = instance.cbMax

instance.cbMax = value
```

``` csharp
public int cbMax { get; set; }
```

#### <a name="property-value"></a>Eigenschaftswert

Typ: [System.Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[JET_COLUMNDEF-Klasse](./jet-columndef-class.md)

[JET_COLUMNDEF-Member](./jet-columndef-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
