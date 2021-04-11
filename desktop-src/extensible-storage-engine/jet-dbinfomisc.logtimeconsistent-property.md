---
description: 'Weitere Informationen finden Sie hier: JET_DBINFOMISC. logtimekonsistente-Eigenschaft'
title: JET_DBINFOMISC. logtimekonsistente-Eigenschaft
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
ms.openlocfilehash: d46302373df17e147095c5ac5c37f02ffef1eb4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128233"
---
# <a name="jet_dbinfomisclogtimeconsistent-property"></a>JET_DBINFOMISC. logtimekonsistente-Eigenschaft

Ruft den Zeitpunkt ab, zu dem die Datenbank konsistent gemacht wurde. Dieser Wert ist NULL, wenn die Datenbank inkonsistent ist.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

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

Typ: [Microsoft.ISAM.ESENT.Interop.JET_LOGTIME](./jet-logtime-structure2.md)  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[JET_DBINFOMISC-Klasse](./jet-dbinfomisc-class.md)

[Mitglieder JET_DBINFOMISC](./jet-dbinfomisc-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
