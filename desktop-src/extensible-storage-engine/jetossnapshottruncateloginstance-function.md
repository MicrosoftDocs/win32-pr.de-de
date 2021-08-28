---
description: 'Weitere Informationen zu: JetOSSnapshotTruncateLogInstance-Funktion'
title: JetOSSnapshotTruncateLogInstance-Funktion
TOCTitle: JetOSSnapshotTruncateLogInstance Function
ms:assetid: ddc51957-5b89-4abf-9193-c34ef626a63e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294115(v=EXCHG.10)
ms:contentKeyID: 32765729
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotTruncateLogInstance
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0986633a450052431dfcef1426488dddc0417d33
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988443"
---
# <a name="jetossnapshottruncateloginstance-function"></a>JetOSSnapshotTruncateLogInstance-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetossnapshottruncateloginstance-function"></a>JetOSSnapshotTruncateLogInstance-Funktion

Die **JetOSSnapshotTruncateLogInstance-Funktion** schneidet das Protokoll für eine angegebene Instanz während einer Momentaufnahmesitzung ab.

**Windows Vista:****JetOSSnapshotTruncateLogInstance** wird in Windows Vista eingeführt.  

```cpp
    JET_ERR JET_API JetOSSnapshotTruncateLogInstance(
      __in          const JET_OSSNAPID snapId,
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

Die Optionen für diesen Aufruf. Dieser Parameter kann eine Kombination der folgenden Werte aufweisen.

*grbit* kann einer der folgenden Werte sein:


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
| <p>JET_errOSSnapshotInvalidSequence</p> | <p>Die Momentaufnahmesitzung befindet sich nicht in dem Zustand, in dem eine Kürzung erfolgen kann. Mögliche Ursachen sind:</p><ul><li><p>Der Aufruf wird abgeschlossen, nachdem für die Momentaufnahmesitzung ein Timetimetime ausgegeben wurde.</p></li><li><p>Die Sitzung wurde als Kopiermomentaufnahme angegeben.</p></li></ul> | 



Wenn diese Funktion erfolgreich ausgeführt wird, werden die Protokolldateien für eine oder alle Instanzen, die Teil der Momentaufnahmesitzung sind, nach Möglichkeit abgeschnitten.

#### <a name="remarks"></a>Bemerkungen

Diese Funktion sollte nur aufgerufen werden, wenn die Momentaufnahme mit der Option JET_bitContinueAfterThaw erstellt wurde. Andernfalls wird die Momentaufnahmesitzung nach dem Aufruf von [JetOSSnapshotThaw](./jetossnapshotthaw-function.md)beendet.

#### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008.</p> | 
| <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | 
| <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[Fehlerbehandlungsparameter](./error-handling-parameters.md)  
[Erweiterbare Storage-Engine-Fehler](./extensible-storage-engine-errors.md)  
[JET_ERR](./jet-err.md)  
[JetOSSnapshotEnd](./jetossnapshotend-function.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)  
[JetOSSnapshotPrepare](./jetossnapshotprepare-function.md)  
[JetOSSnapshotThaw](./jetossnapshotthaw-function.md)
