---
description: 'Weitere Informationen finden Sie unter: VistaApi.JetOSSnapshotTruncateLogInstance-Methode'
title: VistaApi.JetOSSnapshotTruncateLogInstance-Methode (Microsoft.Isam.Esent.Interop.Vista)
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
ms.openlocfilehash: 00a30d604aa57aeaff1d97ca8f92397d6919a769f9416eb504b2d22abe186f96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119471220"
---
# <a name="vistaapijetossnapshottruncateloginstance-method"></a>VistaApi.JetOSSnapshotTruncateLogInstance-Methode

Schneidt das Protokoll für eine angegebene Instanz während einer Momentaufnahmesitzung ab.

**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

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
    Typ: [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)  
    
    Der Momentaufnahmebezeichner.

<!-- end list -->

  - instance  
    Typ: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)  
    
    Die Instanz, für die das Protokoll abgeschnitten werden soll.

<!-- end list -->

  - grbit  
    Typ: [Microsoft.Isam.Esent.Interop.Vista.SnapshotTruncateLogGrbit](./snapshottruncateloggrbit-enumeration.md)  
    
    Optionen für diesen Aufruf.

## <a name="remarks"></a>Hinweise

Diese Funktion sollte nur aufgerufen werden, wenn die Momentaufnahme mit der [Option ContinueAfterThaw erstellt](./vistagrbits.continueafterthaw-field.md) wurde. Andernfalls endet die Momentaufnahmesitzung nach dem Aufruf von [JetOSSnapshotThaw(JET_OSSNAPID, SnapshotThawGrbit).](./api.jetossnapshotthaw-method.md)

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[VistaApi-Klasse](./vistaapi-class.md)

[VistaApi-Member](./vistaapi-members.md)

[Microsoft.Isam.Esent.Interop.Vista-Namespace](./microsoft.isam.esent.interop.vista-namespace.md)
