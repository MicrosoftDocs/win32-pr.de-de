---
description: 'Weitere Informationen finden Sie unter: JET_DBINFOMISC.logtimeConsistent-Eigenschaft.'
title: JET_DBINFOMISC.logtimeConsistent-Eigenschaft
TOCTitle: 'logtimeConsistent property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.logtimeConsistent
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbinfomisc.logtimeconsistent(v=EXCHG.10)
ms:contentKeyID: 39513228
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.logtimeConsistent
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.logtimeConsistent
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.get_logtimeConsistent
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.set_logtimeConsistent
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c7f8a8db663dca151d1d2e8e46512ee44fe97074f906ae657af3e1fa2803bbda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118486213"
---
# <a name="jet_dbinfomisclogtimeconsistent-property"></a>JET_DBINFOMISC.logtimeConsistent-Eigenschaft

Ruft den Zeitpunkt ab, zu dem die Datenbank konsistent wurde. Dieser Wert ist NULL, wenn die Datenbank inkonsistent ist.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property logtimeConsistent As JET_LOGTIME
    Get
    Friend Set
'Usage
Dim instance As JET_DBINFOMISC
Dim value As JET_LOGTIME

value = instance.logtimeConsistent
```

``` csharp
public JET_LOGTIME logtimeConsistent { get; internal set; }
```

#### <a name="property-value"></a>Eigenschaftswert

Typ: [Microsoft.Isam.Esent.Interop.JET_LOGTIME](./jet-logtime-structure2.md)  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[JET_DBINFOMISC-Klasse](./jet-dbinfomisc-class.md)

[JET_DBINFOMISC Member](./jet-dbinfomisc-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
