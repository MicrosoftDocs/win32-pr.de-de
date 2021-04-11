---
description: Weitere Informationen finden Sie in der JET_ENUMCOLUMNID. ColumnID-Eigenschaft.
title: JET_ENUMCOLUMNID. ColumnID-Eigenschaft
TOCTitle: 'columnid property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.columnid
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumnid.columnid(v=EXCHG.10)
ms:contentKeyID: 55103623
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.columnid
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.set_columnid
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.get_columnid
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.columnid
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f1c456a4eb208ba8c9f2ac39ea0b4dad410ee270
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128216"
---
# <a name="jet_enumcolumnidcolumnid-property"></a>JET_ENUMCOLUMNID. ColumnID-Eigenschaft

Ruft die aufzuzählenden Spalten-ID ab oder legt Sie fest.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property columnid As JET_COLUMNID
    Get
    Set
'Usage
Dim instance As JET_ENUMCOLUMNID
Dim value As JET_COLUMNID

value = instance.columnid

instance.columnid = value
```

``` csharp
public JET_COLUMNID columnid { get; set; }
```

#### <a name="property-value"></a>Eigenschaftswert

Typ: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)  

## <a name="remarks"></a>Bemerkungen

Wenn die Spalten-ID 0 (null) ist, wird die Enumeration dieser Spalte übersprungen und ein entsprechender Slot im Ausgabe Array von JET_ENUMCOLUMN Strukturen mit dem Spalten Status JET_wrnColumnSkipped generiert.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[JET_ENUMCOLUMNID-Klasse](./jet-enumcolumnid-class.md)

[Mitglieder JET_ENUMCOLUMNID](./jet-enumcolumnid-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
