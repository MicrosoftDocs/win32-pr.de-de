---
description: Weitere Informationen finden Sie in der JET_INDEXLIST. columnidicolumn-Eigenschaft.
title: JET_INDEXLIST. columnidicolumn (Eigenschaft)
TOCTitle: 'columnidiColumn property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidiColumn
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexlist.columnidicolumn(v=EXCHG.10)
ms:contentKeyID: 55103664
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidiColumn
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.get_columnidiColumn
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidiColumn
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.set_columnidiColumn
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2759c04b60c15d5786306ec536c7eddb89b02172
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352443"
---
# <a name="jet_indexlistcolumnidicolumn-property"></a>JET_INDEXLIST. columnidicolumn (Eigenschaft)

Ruft das ColumnID der Spalte in der temporären Tabelle ab, in der der Index von dieser Spalte im Index Schlüssel gespeichert wird. Die Spalte ist vom Typ [Long](./jet-coltyp-enumeration.md).

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property columnidiColumn As JET_COLUMNID
    Get
    Friend Set
'Usage
Dim instance As JET_INDEXLIST
Dim value As JET_COLUMNID

value = instance.columnidiColumn
```

``` csharp
public JET_COLUMNID columnidiColumn { get; internal set; }
```

#### <a name="property-value"></a>Eigenschaftswert

Typ: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[JET_INDEXLIST-Klasse](./jet-indexlist-class.md)

[Mitglieder JET_INDEXLIST](./jet-indexlist-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
