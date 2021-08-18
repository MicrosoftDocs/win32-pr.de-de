---
description: 'Weitere Informationen finden Sie unter: JET_RECORDLIST.columnidBookmark-Eigenschaft'
title: JET_RECORDLIST.columnidBookmark-Eigenschaft
TOCTitle: 'columnidBookmark property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_RECORDLIST.columnidBookmark
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_recordlist.columnidbookmark(v=EXCHG.10)
ms:contentKeyID: 55103827
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_RECORDLIST.columnidBookmark
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_RECORDLIST.get_columnidBookmark
- Microsoft.Isam.Esent.Interop.JET_RECORDLIST.set_columnidBookmark
- Microsoft.Isam.Esent.Interop.JET_RECORDLIST.columnidBookmark
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0122462a3d809b59e4b3b17d5ecf82e342fac06267da7aae2875407b69b44deb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119730410"
---
# <a name="jet_recordlistcolumnidbookmark-property"></a>JET_RECORDLIST.columnidBookmark-Eigenschaft

Ruft die Columnid der Spalte in der temporären Tabelle ab, in der das Lesezeichen des Datensatzes gespeichert wird. Die Spalte ist vom Typ JET_coltyp. Text.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property columnidBookmark As JET_COLUMNID
    Get
    Friend Set
'Usage
Dim instance As JET_RECORDLIST
Dim value As JET_COLUMNID

value = instance.columnidBookmark
```

``` csharp
public JET_COLUMNID columnidBookmark { get; internal set; }
```

#### <a name="property-value"></a>Eigenschaftswert

Typ: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)  

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[JET_RECORDLIST-Klasse](./jet-recordlist-class.md)

[JET_RECORDLIST Member](./jet-recordlist-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
