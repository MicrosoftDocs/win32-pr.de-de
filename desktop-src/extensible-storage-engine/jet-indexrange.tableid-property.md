---
description: 'Weitere Informationen finden Sie hier: JET_INDEXRANGE. TableID-Eigenschaft'
title: JET_INDEXRANGE. TableID-Eigenschaft
TOCTitle: 'tableid property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_INDEXRANGE.tableid
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexrange.tableid(v=EXCHG.10)
ms:contentKeyID: 55103657
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXRANGE.tableid
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXRANGE.tableid
- Microsoft.Isam.Esent.Interop.JET_INDEXRANGE.set_tableid
- Microsoft.Isam.Esent.Interop.JET_INDEXRANGE.get_tableid
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: afd5c9401b3b0284f463aa1dbd6676440fd64b1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357914"
---
# <a name="jet_indexrangetableid-property"></a>JET_INDEXRANGE. TableID-Eigenschaft

Ruft den Cursor ab oder legt ihn fest, der den Index Bereich enthält. Der Cursor muss über einen Index Bereich verfügen, der mit jetsetindexrange festgelegt ist.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property tableid As JET_TABLEID
    Get
    Set
'Usage
Dim instance As JET_INDEXRANGE
Dim value As JET_TABLEID

value = instance.tableid

instance.tableid = value
```

``` csharp
public JET_TABLEID tableid { get; set; }
```

#### <a name="property-value"></a>Eigenschaftswert

Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[JET_INDEXRANGE-Klasse](./jet-indexrange-class.md)

[Mitglieder JET_INDEXRANGE](./jet-indexrange-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
