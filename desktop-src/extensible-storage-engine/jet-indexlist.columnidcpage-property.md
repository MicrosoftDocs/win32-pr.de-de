---
description: 'Weitere Informationen finden Sie unter: JET_INDEXLIST.columnidcPage-Eigenschaft'
title: JET_INDEXLIST.columnidcPage-Eigenschaft
TOCTitle: 'columnidcPage property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidcPage
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexlist.columnidcpage(v=EXCHG.10)
ms:contentKeyID: 55103616
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidcPage
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.set_columnidcPage
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.get_columnidcPage
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidcPage
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 969562ad81147178470e531da0cb1669e32709f3624c4d25fe5ea7f6bce68e95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119109815"
---
# <a name="jet_indexlistcolumnidcpage-property"></a>JET_INDEXLIST.columnidcPage-Eigenschaft

Ruft die columnid der Spalte in der temporären Tabelle ab, in der die Anzahl der Seiten im Index gespeichert wird. Dieser Wert ist nicht aktuell und wird nur durch "Api.JetComputeStats" aktualisiert. Die Spalte ist vom Typ [Long.](./jet-coltyp-enumeration.md)

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property columnidcPage As JET_COLUMNID
    Get
    Friend Set
'Usage
Dim instance As JET_INDEXLIST
Dim value As JET_COLUMNID

value = instance.columnidcPage
```

``` csharp
public JET_COLUMNID columnidcPage { get; internal set; }
```

#### <a name="property-value"></a>Eigenschaftswert

Typ: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)  

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[JET_INDEXLIST-Klasse](./jet-indexlist-class.md)

[JET_INDEXLIST Member](./jet-indexlist-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
