---
description: Weitere Informationen finden Sie in der JET_SETCOLUMN. err-Eigenschaft.
title: JET_SETCOLUMN. err-Eigenschaft
TOCTitle: 'err property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_SETCOLUMN.err
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_setcolumn.err(v=EXCHG.10)
ms:contentKeyID: 55107684
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SETCOLUMN.err
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SETCOLUMN.err
- Microsoft.Isam.Esent.Interop.JET_SETCOLUMN.get_err
- Microsoft.Isam.Esent.Interop.JET_SETCOLUMN.set_err
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: afb84b4b8cbeda5f5686e953dd6e7b51e9bacbc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958797"
---
# <a name="jet_setcolumnerr-property"></a>JET_SETCOLUMN. err-Eigenschaft

Ruft den vom Vorgang zum Festlegen der Spalte zurückgegebenen Fehlercode oder die Warnung ab.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property err As JET_wrn
    Get
    Friend Set
'Usage
Dim instance As JET_SETCOLUMN
Dim value As JET_wrn

value = instance.err
```

``` csharp
public JET_wrn err { get; internal set; }
```

#### <a name="property-value"></a>Eigenschaftswert

Typ: [Microsoft.ISAM.ESENT.Interop.JET_wrn](./jet-wrn-enumeration.md)  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[JET_SETCOLUMN-Klasse](./jet-setcolumn-class.md)

[Mitglieder JET_SETCOLUMN](./jet-setcolumn-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
