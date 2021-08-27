---
description: 'Weitere Informationen zu: JetOSSnapshotPrepare-Funktion'
title: JetOSSnapshotPrepare-Funktion
TOCTitle: JetOSSnapshotPrepare Function
ms:assetid: 364cbcba-7ddb-4748-8417-e885a5984b0d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269224(v=EXCHG.10)
ms:contentKeyID: 32765526
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotPrepare
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 010cafd19ffde09b3083dd3cb6e6a69fa2268f11
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470327"
---
# <a name="jetossnapshotprepare-function"></a>JetOSSnapshotPrepare-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetossnapshotprepare-function"></a>JetOSSnapshotPrepare-Funktion

Die **JetOSSnapshotPrepare-Funktion** beginnt mit den Vorbereitungen für eine Momentaufnahmesitzung. Eine Momentaufnahmesitzung ist ein kurzes Zeitintervall, in dem die Engine keine Schreib-IOs auf den Datenträger ausgibt, sodass die Engine an einer Volumemomentaufnahmesitzung teilnehmen kann (wenn sie von einem Momentaufnahmewriter gesteuert wird).

**Windows XP:****JetOSSnapshotPrepare** wird in Windows XP eingeführt.  

```cpp
    JET_ERR JET_API JetOSSnapshotPrepare(
      __out         JET_OSSNAPID* psnapId,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parameter

*psnapId*

Der Bezeichner der Momentaufnahmesitzung, die gestartet werden soll.

*grbit*

Die Optionen für diesen Aufruf. Dieser Parameter kann eine Kombination der folgenden Werte aufweisen.


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>0</p> | <p>Normale Momentaufnahme.</p> | 
| <p>JET_bitIncrementalSnapshot</p> | <p>Es werden nur Protokolldateien verwendet.</p> | 
| <p>JET_bitCopySnapshot</p> | <p>Eine Kopiermomentaufnahme (normal oder inkrementell) ohne Protokollkürzung.</p> | 
| <p>JET_bitContinueAfterThaw</p> | <p>Die Momentaufnahmesitzung tritt nach <a href="gg269229(v=exchg.10).md">JetOSSnapshotThaw</a> auf und erfordert einen <a href="gg294136(v=exchg.10).md">JetOSSnapshotEnd-Funktionsaufruf.</a></p> | 
| <p>JET_bitExplicitPrepare</p> | <p>Standardmäßig werden keine Instanzen vorbereitet.</p><p><strong>Windows 7:</strong>  JET_bitExplicitPrepare wird in Windows 7 eingeführt.</p> | 



### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Der Momentaufnahme-ID-Zeiger ist NULL, oder der <em>grbit-Parameter</em> ist ungültig.</p> | 
| <p>JET_errOSSnapshotInvalidSequence</p> | <p>Eine Momentaufnahmesitzung wird bereits ausgeführt, und es ist nicht zulässig, dass der Vorgang zu einem bestimmten Zeitpunkt mehr als eine Momentaufnahmesitzung hat.</p> | 



Wenn diese Funktion erfolgreich ist, kann eine Momentaufnahmesitzung jederzeit mit der E/A-Fixierungsphase gestartet werden. Der Bezeichner für die Sitzung wird zurückgegeben und muss in den nachfolgenden Aufrufen für die Momentaufnahmesitzung verwendet werden.

Die ausgeführten Instanzen der Engine werden jetzt als Teil der Momentaufnahmesitzung betrachtet.

**Windows Vista:**  Um eine andere Teilmenge von Instanzen anzugeben, kann [JetOSSnapshotPrepareInstance](./jetossnapshotprepareinstance-function.md) aufgerufen werden.

Der normale API-Sequenzaufruf lautet: **JetOSSnapshotPrepare**, optional gefolgt von einem oder mehreren Aufrufen von [JetOSSnapshotPrepareInstance](./jetossnapshotprepareinstance-function.md)und dann von [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md). Sobald das Einfrieren gestartet wurde, kann es mit [JetOSSnapshotThaw](./jetossnapshotthaw-function.md)beendet werden. Die Momentaufnahmesitzung kann jederzeit nach der Vorbereitung mit [JetOSSnapshotAbort](./jetossnapshotabort-function.md)plötzlich beendet werden.

Wenn JET_bitContinueAfterThaw nach [JetOSSnapshotThaw](./jetossnapshotthaw-function.md)angegeben wird, bleibt die Momentaufnahmesitzung erhalten (obwohl die E/A fortgesetzt wird). Dadurch wird eine Überprüfung der Momentaufnahme aktiviert, und bei Bedarf wird die Protokollkürzung mitHilfe von [JetOSSnapshotTruncateLog](./jetossnapshottruncatelog-function.md) aktiviert, und es ist ein Aufruf von [JetOSSnapshotEnd](./jetossnapshotend-function.md)erforderlich.

Wenn diese Funktion fehlschlägt, erfolgt keine Änderung des Engine-Zustands.

#### <a name="remarks"></a>Hinweise

Ereignisprotokolleinträge werden für die verschiedenen Schritte der Momentaufnahme generiert.

#### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista oder Windows XP.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008 oder Windows Server 2003.</p> | | <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | | <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_OSSNAPID](./jet-ossnapid.md)  
[JetOSSnapshotAbort](./jetossnapshotabort-function.md)  
[JetOSSnapshotEnd](./jetossnapshotend-function.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)  
[JetOSSnapshotPrepareInstance](./jetossnapshotprepareinstance-function.md)  
[JetOSSnapshotThaw](./jetossnapshotthaw-function.md)  
[JetOSSnapshotTruncateLog](./jetossnapshottruncatelog-function.md)
