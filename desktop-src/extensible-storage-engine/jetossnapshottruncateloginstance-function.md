---
description: 'Weitere Informationen finden Sie unter: JetOSSnapshotTruncateLogInstance-Funktion'
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
ms.openlocfilehash: da5c999f9fcec38878f339cfb2a927c2be2e5b70
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479026"
---
# <a name="jetossnapshottruncateloginstance-function"></a>JetOSSnapshotTruncateLogInstance-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetossnapshottruncateloginstance-function"></a>JetOSSnapshotTruncateLogInstance-Funktion

Die **JetOSSnapshotTruncateLogInstance-Funktion** schneidigt das Protokoll für eine angegebene Instanz während einer Momentaufnahmesitzung ab.

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

Die Optionen für diesen Aufruf. Dieser Parameter kann eine Kombination der folgenden Werte enthalten.

*grbit* kann einen der folgenden Werte haben:


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>JET_bitAllDatabasesSnapshot</p> | <p>Alle Datenbanken sind angefügt, damit die Speicher-Engine das Protokoll abschneiden und berechnen und abschneiden kann.</p> | 
| <p>0 (Null)</p> | <p>Es erfolgt keine Kürzung.</p> | 



### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errInvalidGrbit</p> | <p>Der <em>grbit-Parameter</em> ist ungültig.</p> | 
| <p>JET_errOSSnapshotInvalidSequence</p> | <p>Die Momentaufnahmesitzung befindet sich nicht in dem Zustand, in dem eine Kürzung auftreten kann. Mögliche Ursachen sind:</p><ul><li><p>Der Aufruf wird abgeschlossen, nachdem für die Momentaufnahmesitzung ein Time out durchgeführt wurde.</p></li><li><p>Die Sitzung wurde als Kopiermomentaufnahme angegeben.</p></li></ul> | 



Wenn diese Funktion erfolgreich ist, werden die Protokolldateien für eine oder alle Instanzen, die Teil der Momentaufnahmesitzung sind, nach Möglichkeit abgeschnitten.

#### <a name="remarks"></a>Hinweise

Diese Funktion sollte nur aufgerufen werden, wenn die Momentaufnahme mit der option JET_bitContinueAfterThaw wurde. Andernfalls endet die Momentaufnahmesitzung nach dem Aufruf von [JetOSSnapshotThaw.](./jetossnapshotthaw-function.md)

#### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008.</p> | | <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | | <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[Fehlerbehandlungsparameter](./error-handling-parameters.md)  
[Erweiterbare Storage Engine-Fehler](./extensible-storage-engine-errors.md)  
[JET_ERR](./jet-err.md)  
[JetOSSnapshotEnd](./jetossnapshotend-function.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)  
[JetOSSnapshotPrepare](./jetossnapshotprepare-function.md)  
[JetOSSnapshotThaw](./jetossnapshotthaw-function.md)
