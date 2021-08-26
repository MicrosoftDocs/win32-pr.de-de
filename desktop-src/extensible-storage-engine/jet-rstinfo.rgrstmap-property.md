---
description: 'Weitere Informationen zu: JET_RSTINFO.rgrstmap-Eigenschaft'
title: JET_RSTINFO.rgrstmap-Eigenschaft
TOCTitle: 'rgrstmap property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_RSTINFO.rgrstmap
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_rstinfo.rgrstmap(v=EXCHG.10)
ms:contentKeyID: 55103890
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_RSTINFO.rgrstmap
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_RSTINFO.get_rgrstmap
- Microsoft.Isam.Esent.Interop.JET_RSTINFO.set_rgrstmap
- Microsoft.Isam.Esent.Interop.JET_RSTINFO.rgrstmap
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 39b49cd465fe76a4bbd9a2da23fcf9a885f41c9cb5672169d359bd6099b204ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119967585"
---
# <a name="jet_rstinforgrstmap-property"></a>JET_RSTINFO.rgrstmap-Eigenschaft

Ruft das Array von [JET_RSTMAP](./jet-rstmap-class.md) Strukturen ab oder legt dieses fest.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property rgrstmap As JET_RSTMAP()
    Get
    Set
'Usage
Dim instance As JET_RSTINFO
Dim value As JET_RSTMAP()

value = instance.rgrstmap

instance.rgrstmap = value
```

``` csharp
public JET_RSTMAP[] rgrstmap { get; set; }
```

#### <a name="property-value"></a>Eigenschaftswert

Typ: \[\]  

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[JET_RSTINFO-Klasse](./jet-rstinfo-class.md)

[JET_RSTINFO-Member](./jet-rstinfo-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
