---
description: 'Weitere Informationen finden Sie hier: vistaapi. jedessnapshottruneureloginstance-Methode'
title: Vistaapi. jedessnapshottruneureloginstance-Methode (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: 'JetOSSnapshotTruncateLogInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotTruncateLogInstance(Microsoft.Isam.Esent.Interop.JET_OSSNAPID,Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.Vista.SnapshotTruncateLogGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetossnapshottruncateloginstance(v=EXCHG.10)
ms:contentKeyID: 55104197
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotTruncateLogInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotTruncateLogInstance
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 75d694629585a730f5c1c7b9b08bb7b06e735cb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869128"
---
# <a name="vistaapijetossnapshottruncateloginstance-method"></a>Vistaapi. jedessnapshottruneureloginstance-Methode

Verkürzt das Protokoll für eine angegebene-Instanz während einer Momentaufnahme Sitzung.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Sub JetOSSnapshotTruncateLogInstance ( _
    snapshot As JET_OSSNAPID, _
    instance As JET_INSTANCE, _
    grbit As SnapshotTruncateLogGrbit _
)
'Usage
Dim snapshot As JET_OSSNAPID
Dim instance As JET_INSTANCE
Dim grbit As SnapshotTruncateLogGrbitVistaApi.JetOSSnapshotTruncateLogInstance(snapshot, _
    instance, grbit)
```

``` csharp
public static void JetOSSnapshotTruncateLogInstance(
    JET_OSSNAPID snapshot,
    JET_INSTANCE instance,
    SnapshotTruncateLogGrbit grbit
)
```

#### <a name="parameters"></a>Parameter

  - Momentaufnahme  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)  
    
    Der Momentaufnahme Bezeichner.

<!-- end list -->

  - instance  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)  
    
    Die-Instanz, für die das Protokoll abgeschnitten werden soll.

<!-- end list -->

  - grbit  
    Typ: [Microsoft. ISAM. ESENT. Interop. Vista. snapshottruneureloggrbit](./snapshottruncateloggrbit-enumeration.md)  
    
    Optionen für diesen-Befehl.

## <a name="remarks"></a>Bemerkungen

Diese Funktion sollte nur aufgerufen werden, wenn die Momentaufnahme mit der Option [continueafterthaw](./vistagrbits.continueafterthaw-field.md) erstellt wurde. Andernfalls wird die Momentaufnahme Sitzung nach dem Aufrufe von [jedessnapshotthaw (JET_OSSNAPID, snapshotthawgrbit)](./api.jetossnapshotthaw-method.md)beendet.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Vistaapi-Klasse](./vistaapi-class.md)

[Vistaapi-Member](./vistaapi-members.md)

[Microsoft. ISAM. ESENT. Interop. Vista-Namespace](./microsoft.isam.esent.interop.vista-namespace.md)
