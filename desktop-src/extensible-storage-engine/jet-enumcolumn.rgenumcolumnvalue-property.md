---
description: 'Weitere Informationen zu: JET_ENUMCOLUMN.rgEnumColumnValue-Eigenschaft'
title: JET_ENUMCOLUMN.rgEnumColumnValue-Eigenschaft
TOCTitle: 'rgEnumColumnValue property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.rgEnumColumnValue
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumn.rgenumcolumnvalue(v=EXCHG.10)
ms:contentKeyID: 55103505
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.rgEnumColumnValue
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.set_rgEnumColumnValue
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.rgEnumColumnValue
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.get_rgEnumColumnValue
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 32322cf1952b6ce2ff8a3496cd5058e4915d86739c20e6c4baaab9577ed15488
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119617230"
---
# <a name="jet_enumcolumnrgenumcolumnvalue-property"></a>JET_ENUMCOLUMN.rgEnumColumnValue-Eigenschaft

Ruft die Aufzählungsspaltenwerte für die Spalte ab. Dieser Member wird nur verwendet, wenn [err](./jet-enumcolumn.err-property.md) nicht [ColumnSingleValue](./jet-wrn-enumeration.md)ist.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property rgEnumColumnValue As JET_ENUMCOLUMNVALUE()
    Get
    Friend Set
'Usage
Dim instance As JET_ENUMCOLUMN
Dim value As JET_ENUMCOLUMNVALUE()

value = instance.rgEnumColumnValue
```

``` csharp
public JET_ENUMCOLUMNVALUE[] rgEnumColumnValue { get; internal set; }
```

#### <a name="property-value"></a>Eigenschaftswert

Typ: \[\]  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[JET_ENUMCOLUMN-Klasse](./jet-enumcolumn-class.md)

[JET_ENUMCOLUMN-Member](./jet-enumcolumn-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
