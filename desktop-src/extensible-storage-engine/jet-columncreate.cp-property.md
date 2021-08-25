---
description: 'Weitere Informationen zu: JET_COLUMNCREATE.cp-Eigenschaft'
title: JET_COLUMNCREATE.cp-Eigenschaft
TOCTitle: 'cp property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_COLUMNCREATE.cp
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columncreate.cp(v=EXCHG.10)
ms:contentKeyID: 55103400
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_COLUMNCREATE.cp
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNCREATE.get_cp
- Microsoft.Isam.Esent.Interop.JET_COLUMNCREATE.set_cp
- Microsoft.Isam.Esent.Interop.JET_COLUMNCREATE.cp
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: baf182b1e53de4131c773e05ee75577cb5d5f5d6c3fc7be9b138ae3bd672c75c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119945780"
---
# <a name="jet_columncreatecp-property"></a>JET_COLUMNCREATE.cp-Eigenschaft

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
Dim instance As JET_COLUMNCREATE
Dim value As JET_CP

value = instance.cp

instance.cp = value
```

``` csharp
public JET_CP cp { get; set; }
```

#### <a name="property-value"></a>Eigenschaftswert

Typ: [Microsoft.Isam.Esent.Interop.JET_CP](./jet-cp-enumeration.md)  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[JET_COLUMNCREATE-Klasse](./jet-columncreate-class.md)

[JET_COLUMNCREATE-Member](./jet-columncreate-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
