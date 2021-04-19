---
description: 'Weitere Informationen finden Sie hier: Server2003Api. jedessnapshotabort-Methode'
title: Server2003Api. jedessnapshotabort-Methode (Microsoft. ISAM. ESENT. Interop. Server2003)
TOCTitle: 'JetOSSnapshotAbort method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Server2003.Server2003Api.JetOSSnapshotAbort(Microsoft.Isam.Esent.Interop.JET_OSSNAPID,Microsoft.Isam.Esent.Interop.Server2003.SnapshotAbortGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.server2003api.jetossnapshotabort(v=EXCHG.10)
ms:contentKeyID: 55104209
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Api.JetOSSnapshotAbort
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Api.JetOSSnapshotAbort
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 44ee61a7c6cff7fe90a77fdaced786532457c132
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347012"
---
# <a name="server2003apijetossnapshotabort-method"></a>Server2003Api. jedessnapshotabort-Methode

Benachrichtigt die Engine, dass Sie normale e/a-Vorgänge fortsetzen kann, nachdem eine Sperrfrist mit einem fehlerhaften Snapshot erreicht wurde.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Sub JetOSSnapshotAbort ( _
    snapid As JET_OSSNAPID, _
    grbit As SnapshotAbortGrbit _
)
'Usage
Dim snapid As JET_OSSNAPID
Dim grbit As SnapshotAbortGrbitServer2003Api.JetOSSnapshotAbort(snapid, _
    grbit)
```

``` csharp
public static void JetOSSnapshotAbort(
    JET_OSSNAPID snapid,
    SnapshotAbortGrbit grbit
)
```

#### <a name="parameters"></a>Parameter

  - snapid  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)  
    
    Der Bezeichner der Momentaufnahme Sitzung.

<!-- end list -->

  - grbit  
    Typ: [Microsoft. ISAM. ESENT. Interop. Server2003. snapshotabortgrbit](./snapshotabortgrbit-enumeration.md)  
    
    Optionen für diesen-Befehl.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Server2003Api-Klasse](./server2003api-class.md)

[Server2003Api-Member](./server2003api-members.md)

[Microsoft. ISAM. ESENT. Interop. Server2003-Namespace](./microsoft.isam.esent.interop.server2003-namespace.md)
