---
description: 'Weitere Informationen finden Sie unter: JET_ENUMCOLUMN.cbData-Eigenschaft'
title: JET_ENUMCOLUMN.cbData-Eigenschaft
TOCTitle: 'cbData property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.cbData
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumn.cbdata(v=EXCHG.10)
ms:contentKeyID: 55103617
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.cbData
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.cbData
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.set_cbData
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.get_cbData
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e8a1674c4b4c47d6f6a1fa07b06806cd5202db95eb789e499485936ba438dcec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118766006"
---
# <a name="jet_enumcolumncbdata-property"></a>JET_ENUMCOLUMN.cbData-Eigenschaft

Ruft die Größe des Werts ab, der für die Spalte aufzählt wurde. Dieser Member wird nur verwendet, [wenn err](./jet-enumcolumn.err-property.md) gleich [ColumnSingleValue ist.](./jet-wrn-enumeration.md)

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property cbData As Integer
    Get
    Friend Set
'Usage
Dim instance As JET_ENUMCOLUMN
Dim value As Integer

value = instance.cbData
```

``` csharp
public int cbData { get; internal set; }
```

#### <a name="property-value"></a>Eigenschaftswert

Typ: [System.Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[JET_ENUMCOLUMN-Klasse](./jet-enumcolumn-class.md)

[JET_ENUMCOLUMN Member](./jet-enumcolumn-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
