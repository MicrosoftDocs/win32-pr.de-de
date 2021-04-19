---
description: 'Weitere Informationen finden Sie hier: JET_OBJECTLIST. TableID-Eigenschaft'
title: JET_OBJECTLIST. TableID-Eigenschaft
TOCTitle: 'tableid property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_OBJECTLIST.tableid
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_objectlist.tableid(v=EXCHG.10)
ms:contentKeyID: 55103778
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_OBJECTLIST.tableid
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_OBJECTLIST.set_tableid
- Microsoft.Isam.Esent.Interop.JET_OBJECTLIST.tableid
- Microsoft.Isam.Esent.Interop.JET_OBJECTLIST.get_tableid
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 080d6bd1c46f86d0bb1ab780da2e44a7eb8ae6f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353517"
---
# <a name="jet_objectlisttableid-property"></a>JET_OBJECTLIST. TableID-Eigenschaft

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
Dim instance As JET_OBJECTLIST
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

[JET_OBJECTLIST-Klasse](./jet-objectlist-class.md)

[Mitglieder JET_OBJECTLIST](./jet-objectlist-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
