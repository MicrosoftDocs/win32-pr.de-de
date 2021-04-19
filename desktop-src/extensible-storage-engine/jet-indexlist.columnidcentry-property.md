---
description: Weitere Informationen finden Sie in der JET_INDEXLIST. columnidcentry-Eigenschaft.
title: JET_INDEXLIST. columnidcentry-Eigenschaft
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
ms.openlocfilehash: 49f3a2a8c22a869cd70a40da72b3e2915caa638c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349366"
---
# <a name="jet_indexlistcolumnidcentry-property"></a>JET_INDEXLIST. columnidcentry-Eigenschaft

Ruft das ColumnID der Spalte in der temporären Tabelle ab, in der die Anzahl der Einträge im Index gespeichert wird. Dieser Wert ist nicht aktuell und wird nur von "API. jetcomputestats" aktualisiert. Die Spalte ist vom Typ [Long](./jet-coltyp-enumeration.md).

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

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

Typ: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[JET_INDEXLIST-Klasse](./jet-indexlist-class.md)

[Mitglieder JET_INDEXLIST](./jet-indexlist-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
