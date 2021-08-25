---
description: 'Weitere Informationen finden Sie unter: JET_ENUMCOLUMNID.columnid-Eigenschaft.'
title: JET_ENUMCOLUMNID.columnid-Eigenschaft
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
ms.openlocfilehash: 98e8aea385dd124e455d26e809c655b25d513a1a7fc843b8b42c8de395c3241c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119890860"
---
# <a name="jet_enumcolumnidcolumnid-property"></a>JET_ENUMCOLUMNID.columnid-Eigenschaft

Ruft die columnid-ID ab, die aufzählt werden soll, oder legt sie fest.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

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

Typ: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)  

## <a name="remarks"></a>Hinweise

Wenn die Spalten-ID 0 (null) ist, wird die Enumeration dieser Spalte übersprungen, und ein entsprechender Slot im Ausgabearray von JET_ENUMCOLUMN-Strukturen wird mit dem Spaltenzustand JET_wrnColumnSkipped.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[JET_ENUMCOLUMNID-Klasse](./jet-enumcolumnid-class.md)

[JET_ENUMCOLUMNID Member](./jet-enumcolumnid-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
