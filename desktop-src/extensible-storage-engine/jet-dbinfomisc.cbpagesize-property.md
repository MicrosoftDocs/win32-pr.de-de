---
description: 'Weitere Informationen finden Sie unter: JET_DBINFOMISC.cbPageSize-Eigenschaft'
title: JET_DBINFOMISC.cbPageSize-Eigenschaft
TOCTitle: 'cbPageSize property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.cbPageSize
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbinfomisc.cbpagesize(v=EXCHG.10)
ms:contentKeyID: 39512879
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.cbPageSize
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.get_cbPageSize
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.set_cbPageSize
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.cbPageSize
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1a4b72ff96337637c90aaeaa48bfbb344f0d36e9658536cb6efa9c5399741063
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119891420"
---
# <a name="jet_dbinfomisccbpagesize-property"></a>JET_DBINFOMISC.cbPageSize-Eigenschaft

Ruft die Seitengröße der Datenbank ab. Der Wert 0 bedeutet 4 KB Seiten.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property cbPageSize As Integer
    Get
    Friend Set
'Usage
Dim instance As JET_DBINFOMISC
Dim value As Integer

value = instance.cbPageSize
```

``` csharp
public int cbPageSize { get; internal set; }
```

#### <a name="property-value"></a>Eigenschaftswert

Typ: [System.Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[JET_DBINFOMISC-Klasse](./jet-dbinfomisc-class.md)

[JET_DBINFOMISC Member](./jet-dbinfomisc-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
