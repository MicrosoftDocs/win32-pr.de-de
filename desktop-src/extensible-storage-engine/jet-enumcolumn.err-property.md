---
description: 'Weitere Informationen finden Sie unter: JET_ENUMCOLUMN.err-Eigenschaft'
title: JET_ENUMCOLUMN.err-Eigenschaft
TOCTitle: 'err property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.err
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumn.err(v=EXCHG.10)
ms:contentKeyID: 55103499
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.err
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.get_err
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.set_err
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.err
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 01e531ae5676883f54d5229512b2b6868907ef8a3cf9d12f2e8584b1e489457a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119617260"
---
# <a name="jet_enumcolumnerr-property"></a>JET_ENUMCOLUMN.err-Eigenschaft

Ruft den Spaltenstatuscode ab, der sich aus der -Enumeration ergibt.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property err As JET_wrn
    Get
    Friend Set
'Usage
Dim instance As JET_ENUMCOLUMN
Dim value As JET_wrn

value = instance.err
```

``` csharp
public JET_wrn err { get; internal set; }
```

#### <a name="property-value"></a>Eigenschaftswert

Typ: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[JET_ENUMCOLUMN-Klasse](./jet-enumcolumn-class.md)

[JET_ENUMCOLUMN Member](./jet-enumcolumn-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)

[ColumnSingleValue](./jet-wrn-enumeration.md)
