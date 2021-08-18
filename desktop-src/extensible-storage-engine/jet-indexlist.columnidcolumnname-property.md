---
description: 'Weitere Informationen finden Sie unter: JET_INDEXLIST.columnidcolumnname-Eigenschaft'
title: JET_INDEXLIST.columnidcolumnname-Eigenschaft
TOCTitle: 'columnidcolumnname property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidcolumnname
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexlist.columnidcolumnname(v=EXCHG.10)
ms:contentKeyID: 55103662
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidcolumnname
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.set_columnidcolumnname
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.get_columnidcolumnname
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidcolumnname
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: af517a86946c6115728f5c53608e8925afd049228c6edfb5f47fb2384a2b99f7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120116040"
---
# <a name="jet_indexlistcolumnidcolumnname-property"></a>JET_INDEXLIST.columnidcolumnname-Eigenschaft

Ruft die Columnid der Spalte in der temporären Tabelle ab, in der das grbit gespeichert wird, das für die indizierte Spalte gilt. Siehe [IndexKeyGrbit](./indexkeygrbit-enumeration.md). Die Spalte ist vom Typ [Text](./jet-coltyp-enumeration.md).

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property columnidcolumnname As JET_COLUMNID
    Get
    Friend Set
'Usage
Dim instance As JET_INDEXLIST
Dim value As JET_COLUMNID

value = instance.columnidcolumnname
```

``` csharp
public JET_COLUMNID columnidcolumnname { get; internal set; }
```

#### <a name="property-value"></a>Eigenschaftswert

Typ: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[JET_INDEXLIST-Klasse](./jet-indexlist-class.md)

[JET_INDEXLIST Member](./jet-indexlist-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
