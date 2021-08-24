---
description: 'Weitere Informationen finden Sie unter: JET_INDEXLIST.columnidcEntry-Eigenschaft'
title: JET_INDEXLIST.columnidcEntry-Eigenschaft
TOCTitle: 'columnidcEntry property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidcEntry
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexlist.columnidcentry(v=EXCHG.10)
ms:contentKeyID: 55103597
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidcEntry
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.set_columnidcEntry
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidcEntry
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.get_columnidcEntry
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fda8bbf01d20fae6c09415796b04b6a3e1e8372033fa00f3728699a4bd8aeb46
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119604040"
---
# <a name="jet_indexlistcolumnidcentry-property"></a>JET_INDEXLIST.columnidcEntry-Eigenschaft

Ruft die columnid der Spalte in der temporären Tabelle ab, in der die Anzahl der Einträge im Index gespeichert wird. Dieser Wert ist nicht aktuell und wird nur durch "Api.JetComputeStats" aktualisiert. Die Spalte ist vom Typ [Long.](./jet-coltyp-enumeration.md)

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property columnidcEntry As JET_COLUMNID
    Get
    Friend Set
'Usage
Dim instance As JET_INDEXLIST
Dim value As JET_COLUMNID

value = instance.columnidcEntry
```

``` csharp
public JET_COLUMNID columnidcEntry { get; internal set; }
```

#### <a name="property-value"></a>Eigenschaftswert

Typ: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[JET_INDEXLIST-Klasse](./jet-indexlist-class.md)

[JET_INDEXLIST Mitglieder](./jet-indexlist-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
