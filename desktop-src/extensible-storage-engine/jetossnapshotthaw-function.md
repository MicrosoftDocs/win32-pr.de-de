---
description: 'Weitere Informationen zu: JetOSSnapshotThaw-Funktion'
title: JetOSSnapshotThaw-Funktion
TOCTitle: JetOSSnapshotThaw Function
ms:assetid: 3b001113-6299-4082-ab15-461f2e33e996
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269229(v=EXCHG.10)
ms:contentKeyID: 32765531
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotThaw
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d9be4bcff435fe30186b3b7585c79e3066987cc5
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479056"
---
# <a name="jetossnapshotthaw-function"></a>JetOSSnapshotThaw-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetossnapshotthaw-function"></a>JetOSSnapshotThaw-Funktion

Die **JetOSSnapshotThaw-Funktion** benachrichtigt die Engine, dass sie den normalen E/A-Betrieb nach einem Einfrierenszeitraum und einer erfolgreichen Momentaufnahme fortsetzen kann.

**Windows XP:****JetOSSnapshotThaw** wurde in Windows XP eingeführt.  

```cpp
    JET_ERR JET_API JetOSSnapshotThaw(
      __in          const JET_OSSNAPID snapId,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parameter

*snapId*

Der Bezeichner der Momentaufnahmesitzung.

*grbit*

Dieser Parameter ist für die zukünftige Verwendung reserviert, und der einzige gültige unterstützte Wert ist 0.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Die Momentaufnahmesitzung ist ungültig, oder der <em>grbit-Parameter</em> ist ungültig.</p> | 
| <p>JET_errOSSnapshotTimeOut</p> | <p>Die Momentaufnahmesitzung hatte vor diesem Aufruf ein internes Timeout. Folglich wurden E/A-Vorgänge wieder normalisiert, bevor dieser Aufruf durchgeführt wurde.</p> | 
| <p>JET_errOSSnapshotInvalidSnapId</p> | <p>Der Bezeichner für die Momentaufnahmesitzung ist ungültig.</p> | 



Wenn diese Funktion erfolgreich ausgeführt wird, wird eine Momentaufnahmesitzung beendet, und das normale Engine-Verhalten wird fortgesetzt. Eine neue Momentaufnahmesitzung kann später gestartet werden.

Wenn diese Funktion fehlschlägt, wird die aktuelle Momentaufnahmesitzung beendet, aber das Einfrieren von IOs während des Momentaufnahmezeitraums wurde intern nicht berücksichtigt.

#### <a name="remarks"></a>Hinweise

Ereignisprotokolleinträge werden für die verschiedenen Schritte der Momentaufnahme generiert.

#### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista oder Windows XP.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008 oder Windows Server 2003.</p> | | <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | | <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_OSSNAPID](./jet-ossnapid.md)  
[JetOSSnapshotAbort](./jetossnapshotabort-function.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)  
[JetOSSnapshotPrepare](./jetossnapshotprepare-function.md)
