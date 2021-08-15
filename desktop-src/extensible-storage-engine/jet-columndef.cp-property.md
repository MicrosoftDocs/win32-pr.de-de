---
description: 'Weitere Informationen zu: JET_COLUMNDEF.cp-Eigenschaft'
title: JET_COLUMNDEF.cp-Eigenschaft
TOCTitle: 'cp property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_COLUMNDEF.cp
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columndef.cp(v=EXCHG.10)
ms:contentKeyID: 55103411
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_COLUMNDEF.cp
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNDEF.get_cp
- Microsoft.Isam.Esent.Interop.JET_COLUMNDEF.set_cp
- Microsoft.Isam.Esent.Interop.JET_COLUMNDEF.cp
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d82fea1a486d7e4797e2a359b6290e7c845f346e9ea8dc02843d6be57747edc7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118487080"
---
# <a name="jet_columndefcp-property"></a>JET_COLUMNDEF.cp-Eigenschaft

Ruft die Codepage der Spalte ab oder legt diese fest. Dies ist nur für Spalten vom Typ [Text](./jet-coltyp-enumeration.md) und [LongText](./jet-coltyp-enumeration.md)sinnvoll.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property cp As JET_CP
    Get
    Set
'Usage
Dim instance As JET_COLUMNDEF
Dim value As JET_CP

value = instance.cp

instance.cp = value
```

``` csharp
public JET_CP cp { get; set; }
```

#### <a name="property-value"></a>Eigenschaftswert

Typ: [Microsoft.Isam.Esent.Interop.JET_CP](./jet-cp-enumeration.md)  

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[JET_COLUMNDEF-Klasse](./jet-columndef-class.md)

[JET_COLUMNDEF-Member](./jet-columndef-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
