---
description: 'Weitere Informationen finden Sie unter: JET_INDEXLIST. columnidlcmapflags-Eigenschaft'
title: JET_INDEXLIST. columnidlcmapflags (Eigenschaft)
TOCTitle: 'columnidLCMapFlags property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidLCMapFlags
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexlist.columnidlcmapflags(v=EXCHG.10)
ms:contentKeyID: 55103667
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidLCMapFlags
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.set_columnidLCMapFlags
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.get_columnidLCMapFlags
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidLCMapFlags
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d5479bda4a0b4f4b802ae42221f5bbd9879c94c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866844"
---
# <a name="jet_indexlistcolumnidlcmapflags-property"></a>JET_INDEXLIST. columnidlcmapflags (Eigenschaft)

Ruft das ColumnID der Spalte in der temporären Tabelle ab, in der die Unicode-normalisierungs Flags für den Index gespeichert werden. Die Spalte ist vom Typ [Long](./jet-coltyp-enumeration.md).

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property columnidLCMapFlags As JET_COLUMNID
    Get
    Friend Set
'Usage
Dim instance As JET_INDEXLIST
Dim value As JET_COLUMNID

value = instance.columnidLCMapFlags
```

``` csharp
public JET_COLUMNID columnidLCMapFlags { get; internal set; }
```

#### <a name="property-value"></a>Eigenschaftswert

Typ: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[JET_INDEXLIST-Klasse](./jet-indexlist-class.md)

[Mitglieder JET_INDEXLIST](./jet-indexlist-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
