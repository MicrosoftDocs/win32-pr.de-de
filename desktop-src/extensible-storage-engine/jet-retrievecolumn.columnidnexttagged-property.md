---
description: Weitere Informationen finden Sie in der JET_RETRIEVECOLUMN. columnidnexttaging-Eigenschaft.
title: JET_RETRIEVECOLUMN. columnidnexttaging (Eigenschaft)
TOCTitle: 'columnidNextTagged property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.columnidNextTagged
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_retrievecolumn.columnidnexttagged(v=EXCHG.10)
ms:contentKeyID: 55103812
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.columnidNextTagged
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.columnidNextTagged
- Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.get_columnidNextTagged
- Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.set_columnidNextTagged
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5b900d03e43f0d7b172b09e0928110222e909df3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129832"
---
# <a name="jet_retrievecolumncolumnidnexttagged-property"></a>JET_RETRIEVECOLUMN. columnidnexttaging (Eigenschaft)

Ruft das ColumnID der markierten Spalte mit mehreren Werten oder einer sparsespalte ab, wenn alle markierten Spalten abgerufen werden, indem 0 als ColumnID übergeben wird.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property columnidNextTagged As JET_COLUMNID
    Get
    Private Set
'Usage
Dim instance As JET_RETRIEVECOLUMN
Dim value As JET_COLUMNID

value = instance.columnidNextTagged
```

``` csharp
public JET_COLUMNID columnidNextTagged { get; private set; }
```

#### <a name="property-value"></a>Eigenschaftswert

Typ: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[JET_RETRIEVECOLUMN-Klasse](./jet-retrievecolumn-class.md)

[Mitglieder JET_RETRIEVECOLUMN](./jet-retrievecolumn-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
