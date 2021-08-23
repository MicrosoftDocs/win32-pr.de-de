---
description: 'Weitere Informationen finden Sie unter: JET_COLUMNCREATE.cbMax-Eigenschaft'
title: JET_COLUMNCREATE.cbMax-Eigenschaft
TOCTitle: 'cbMax property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_COLUMNCREATE.cbMax
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columncreate.cbmax(v=EXCHG.10)
ms:contentKeyID: 55103390
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_COLUMNCREATE.cbMax
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNCREATE.cbMax
- Microsoft.Isam.Esent.Interop.JET_COLUMNCREATE.set_cbMax
- Microsoft.Isam.Esent.Interop.JET_COLUMNCREATE.get_cbMax
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f5f45137a52209f2096fc4f372c7af4b0573945645ecd6ddbe592a2d4770b550
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119780950"
---
# <a name="jet_columncreatecbmax-property"></a>JET_COLUMNCREATE.cbMax-Eigenschaft

Ruft die maximale Länge der Spalte ab oder legt diese fest. Dies ist nur für Spalten vom Typ [Text](./jet-coltyp-enumeration.md), [LongText](./jet-coltyp-enumeration.md), [Binary](./jet-coltyp-enumeration.md) und [LongBinary sinnvoll.](./jet-coltyp-enumeration.md)

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property cbMax As Integer
    Get
    Set
'Usage
Dim instance As JET_COLUMNCREATE
Dim value As Integer

value = instance.cbMax

instance.cbMax = value
```

``` csharp
public int cbMax { get; set; }
```

#### <a name="property-value"></a>Eigenschaftswert

Typ: [System.Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[JET_COLUMNCREATE-Klasse](./jet-columncreate-class.md)

[JET_COLUMNCREATE Member](./jet-columncreate-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
