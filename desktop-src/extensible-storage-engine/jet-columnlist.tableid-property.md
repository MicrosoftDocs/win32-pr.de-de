---
description: 'Weitere Informationen finden Sie hier: JET_COLUMNLIST. TableID-Eigenschaft'
title: JET_COLUMNLIST. TableID-Eigenschaft
TOCTitle: 'tableid property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_COLUMNLIST.tableid
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columnlist.tableid(v=EXCHG.10)
ms:contentKeyID: 55103528
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_COLUMNLIST.tableid
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNLIST.get_tableid
- Microsoft.Isam.Esent.Interop.JET_COLUMNLIST.tableid
- Microsoft.Isam.Esent.Interop.JET_COLUMNLIST.set_tableid
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0eb1c2338fca9a1ce503033b83a9c134a08d6a9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217559"
---
# <a name="jet_columnlisttableid-property"></a>JET_COLUMNLIST. TableID-Eigenschaft

Ruft TableID der temporären Tabelle ab. Dies sollte geschlossen werden, wenn die Tabelle nicht mehr benötigt wird.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property tableid As JET_TABLEID
    Get
    Friend Set
'Usage
Dim instance As JET_COLUMNLIST
Dim value As JET_TABLEID

value = instance.tableid
```

``` csharp
public JET_TABLEID tableid { get; internal set; }
```

#### <a name="property-value"></a>Eigenschaftswert

Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[JET_COLUMNLIST-Klasse](./jet-columnlist-class.md)

[Mitglieder JET_COLUMNLIST](./jet-columnlist-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
