---
description: 'Weitere Informationen finden Sie unter: JetOSSnapshotPrepareInstance-Funktion'
title: JetOSSnapshotPrepareInstance-Funktion
TOCTitle: JetOSSnapshotPrepareInstance Function
ms:assetid: b4f06342-633f-47c6-be32-64ec058920fe
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294064(v=EXCHG.10)
ms:contentKeyID: 32765679
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotPrepareInstance
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4997be8f268d676fbd4a164281061b488e948168
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474386"
---
# <a name="jetossnapshotprepareinstance-function"></a>JetOSSnapshotPrepareInstance-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetossnapshotprepareinstance-function"></a>JetOSSnapshotPrepareInstance-Funktion

Die **JetOSSnapshotPrepareInstance-Funktion** wählt eine bestimmte Instanz aus, die Teil der Momentaufnahmesitzung sein soll.

**Windows Vista:** **JetOSSnapshotPrepareInstance** wurde in Windows Vista eingeführt.

```cpp
JET_ERR JET_API JetOSSnapshotPrepareInstance(
  __in          JET_OSSNAPID snapId,
  __in          JET_INSTANCE instance,
  __in          const JET_GRBIT grbit
);
```

### <a name="parameters"></a>Parameter

*snapId*

Der Bezeichner der Momentaufnahmesitzung.

*Instanz*

Die -Instanz, die für diesen Aufruf verwendet wird.

*grbit*

Die Optionen für diesen Aufruf. Dieser Parameter ist für die zukünftige Verwendung reserviert. Der einzige gültige Wert ist 0 (null).

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Der Momentaufnahme-ID-Zeiger <strong>ist NULL,</strong> oder <em>der grbit-Parameter</em> ist ungültig.</p> | 
| <p>JET_errOSSnapshotInvalidSequence</p> | <p>Eine Momentaufnahmesitzung wird bereits erstellt.</p> | 
| <p>JET_errOSSnapshotInvalidSnapId</p> | <p>Der Bezeichner für die Momentaufnahmesitzung ist ungültig.</p> | 



Wenn diese Funktion erfolgreich ist, ist die angegebene Instanz Teil der Momentaufnahmesitzung.

Wenn diese Funktion fehlschlägt, erfolgt keine Änderung des Engine-Zustands.

#### <a name="remarks"></a>Hinweise

Der normale API-Sequenzaufruf [ist: JetOSSnapshotPrepare](./jetossnapshotprepare-function.md), optional gefolgt von einem oder mehr Aufrufen von **JetOSSnapshotPrepareInstance**, gefolgt von [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md). Nachdem der Einfrieren gestartet wurde, kann er mit [JetOSSnapshotThaw beendet werden.](./jetossnapshotthaw-function.md) Nach der Vorbereitung kann die Momentaufnahmesitzung mit [JetOSSnapshotAbort](./jetossnapshotabort-function.md)jederzeit plötzlich beendet werden. Ereignisprotokolleinträge werden für die verschiedenen Schritte der Momentaufnahme generiert.

Wenn **JetOSSnapshotPrepareInstance** zwischen dem Start der Sitzung ([JetOSSnapshotPrepare](./jetossnapshotprepare-function.md)) und dem Fix-Moment ([JetOSSnapshotFreeze)](./jetossnapshotfreeze-function.md)nicht aufgerufen wird, frieren alle ausgeführten Instanzen in der Engine ein und werden Teil der Momentaufnahmesitzung. Dies hat zwei Gründe:

  - Sie vereinfacht den Code für Benutzer, die alle Instanzen wünschen.

  - Sie ermöglicht Abwärtskompatibilität für die Aufrufer der Momentaufnahme-APIs.

#### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008.</p> | | <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | | <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[Fehlerbehandlungsparameter](./error-handling-parameters.md)  
[Erweiterbare Storage Engine-Fehler](./extensible-storage-engine-errors.md)  
[JET_ERR](./jet-err.md)  
[JetOSSnapshotAbort](./jetossnapshotabort-function.md)  
[JetOSSnapshotEnd](./jetossnapshotend-function.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)  
[JetOSSnapshotPrepare](./jetossnapshotprepare-function.md)  
[JetOSSnapshotThaw](./jetossnapshotthaw-function.md)
