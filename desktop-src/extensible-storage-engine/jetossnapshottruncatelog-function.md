---
description: 'Weitere Informationen zu: JetOSSnapshotTruncateLog-Funktion'
title: JetOSSnapshotTruncateLog-Funktion
TOCTitle: JetOSSnapshotTruncateLog Function
ms:assetid: 3df8f5b2-8083-49b7-a325-fd13187f785c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269231(v=EXCHG.10)
ms:contentKeyID: 32765533
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotTruncateLog
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: adda7e97fd9a8e1a65740f4fb82c22b52cfad979
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472506"
---
# <a name="jetossnapshottruncatelog-function"></a>JetOSSnapshotTruncateLog-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetossnapshottruncatelog-function"></a>JetOSSnapshotTruncateLog-Funktion

Die **JetOSSnapshotTruncateLog-Funktion** ermöglicht die Protokollkürzung für alle Instanzen, die Teil der Momentaufnahmesitzung sind.

**Windows Vista:****JetOSSnapshotTruncateLog** wird in Windows Vista eingeführt.  

```cpp
    JET_ERR JET_API JetOSSnapshotTruncateLog(
      __in          const JET_OSSNAPID snapId,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parameter

*snapId*

Der Bezeichner der Momentaufnahmesitzung.

*grbit*

Die Optionen für diesen Aufruf. Dieser Parameter kann eine Kombination der folgenden Werte aufweisen.


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>JET_bitAllDatabasesSnapshot</p> | <p>Alle Datenbanken sind angefügt, damit die Speicher-Engine die Protokollkürzung berechnen und durchführen kann.</p> | 
| <p>0 (Null)</p> | <p>Es erfolgt keine Kürzung.</p> | 



### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errInvalidGrbit</p> | <p>Der <em>grbit-Parameter</em> ist ungültig.</p> | 
| <p>JET_errOSSnapshotInvalidSequence</p> | <p>Die Momentaufnahmesitzung befindet sich nicht in dem Zustand, in dem eine Kürzung erfolgen kann. Mögliche Ursachen sind:</p><ul><li><p>Der Aufruf erfolgt nach dem Time out der Momentaufnahmesitzung.</p></li><li><p>Die Sitzung wurde als Kopiermomentaufnahme angegeben.</p></li></ul> | 



Bei Erfolg werden die Protokolldateien für eine oder alle Instanzen, die Teil der Momentaufnahmesitzung sind, nach Möglichkeit abgeschnitten.

#### <a name="remarks"></a>Hinweise

Diese Funktion sollte nur aufgerufen werden, wenn die Momentaufnahme mit der Option JET_bitContinueAfterThaw erstellt wurde. Andernfalls wäre die Momentaufnahmesitzung nach dem [JetOSSnapshotThaw-Aufruf](./jetossnapshotthaw-function.md) beendet worden.

#### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008.</p> | | <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | | <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[Fehlerbehandlungsparameter](./error-handling-parameters.md)  
[Erweiterbare Storage-Engine-Fehler](./extensible-storage-engine-errors.md)  
[JET_ERR](./jet-err.md)  
[JetOSSnapshotEnd](./jetossnapshotend-function.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)  
[JetOSSnapshotPrepare](./jetossnapshotprepare-function.md)  
[JetOSSnapshotThaw](./jetossnapshotthaw-function.md)
