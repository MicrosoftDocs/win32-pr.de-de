---
description: 'Weitere Informationen finden Sie unter: JET_DBINFOMISC.bkinfoDiffPrev-Eigenschaft'
title: JET_DBINFOMISC.bkinfoDiffPrev-Eigenschaft
TOCTitle: 'bkinfoDiffPrev property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.bkinfoDiffPrev
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbinfomisc.bkinfodiffprev(v=EXCHG.10)
ms:contentKeyID: 39513441
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.bkinfoDiffPrev
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.bkinfoDiffPrev
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.set_bkinfoDiffPrev
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.get_bkinfoDiffPrev
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fec2a5a00ebeb805085daba3b3a707bbe739eba6dbaca3c5945fb49152c7e6c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118980400"
---
# <a name="jet_dbinfomiscbkinfodiffprev-property"></a>JET_DBINFOMISC.bkinfoDiffPrev-Eigenschaft

Ruft Informationen zur letzten erfolgreichen differenziellen Sicherung ab. Zurücksetzen, [wenn bkinfoFullPrev](./jet-dbinfomisc.bkinfofullprev-property.md) festgelegt ist.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property bkinfoDiffPrev As JET_BKINFO
    Get
    Friend Set
'Usage
Dim instance As JET_DBINFOMISC
Dim value As JET_BKINFO

value = instance.bkinfoDiffPrev
```

``` csharp
public JET_BKINFO bkinfoDiffPrev { get; internal set; }
```

#### <a name="property-value"></a>Eigenschaftswert

Typ: [Microsoft.Isam.Esent.Interop.JET_BKINFO](./jet-bkinfo-structure2.md)  

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[JET_DBINFOMISC-Klasse](./jet-dbinfomisc-class.md)

[JET_DBINFOMISC Member](./jet-dbinfomisc-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
