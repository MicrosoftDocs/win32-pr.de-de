---
description: 'Weitere Informationen finden Sie hier: JET_RSTINFO. pfnstatus-Eigenschaft'
title: JET_RSTINFO. pfnstatus-Eigenschaft
TOCTitle: 'pfnStatus property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_RSTINFO.pfnStatus
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_rstinfo.pfnstatus(v=EXCHG.10)
ms:contentKeyID: 55103829
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_RSTINFO.pfnStatus
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_RSTINFO.pfnStatus
- Microsoft.Isam.Esent.Interop.JET_RSTINFO.set_pfnStatus
- Microsoft.Isam.Esent.Interop.JET_RSTINFO.get_pfnStatus
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 57b400e91867d4408fcdb93b979d1a39d8e7eb76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344416"
---
# <a name="jet_rstinfopfnstatus-property"></a>JET_RSTINFO. pfnstatus-Eigenschaft

Ruft den Rückruf ab oder legt ihn fest, der die Status Funktion abruft oder festlegt.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property pfnStatus As JET_PFNSTATUS
    Get
    Set
'Usage
Dim instance As JET_RSTINFO
Dim value As JET_PFNSTATUS

value = instance.pfnStatus

instance.pfnStatus = value
```

``` csharp
public JET_PFNSTATUS pfnStatus { get; set; }
```

#### <a name="property-value"></a>Eigenschaftswert

Typ: [Microsoft.ISAM.ESENT.Interop.JET_PFNSTATUS](./jet-pfnstatus-delegate.md)  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[JET_RSTINFO-Klasse](./jet-rstinfo-class.md)

[Mitglieder JET_RSTINFO](./jet-rstinfo-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
