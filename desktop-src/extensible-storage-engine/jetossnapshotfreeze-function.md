---
description: 'Weitere Informationen finden Sie unter: JetOSSnapshotFreeze-Funktion'
title: JetOSSnapshotFreeze-Funktion
TOCTitle: JetOSSnapshotFreeze Function
ms:assetid: 8dfbff20-199e-4d89-a33c-ae8e39b11ec1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269332(v=EXCHG.10)
ms:contentKeyID: 32765622
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotFreezeA
- JetOSSnapshotFreezeW
- JetOSSnapshotFreeze
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 854e38f91b894b1f7cc486a15afcfe857aaa31d6
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473966"
---
# <a name="jetossnapshotfreeze-function"></a>JetOSSnapshotFreeze-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetossnapshotfreeze-function"></a>JetOSSnapshotFreeze-Funktion

Die **JetOSSnapshotFreeze-Funktion** startet eine Momentaufnahme. Während die Momentaufnahme in Bearbeitung ist, kann keine Schreib-auf-Datenträger-Aktivität durch die Engine stattfinden.

**Windows XP:****JetOSSnapshotFreeze** wird in Windows XP eingeführt.  

```cpp
    JET_ERR JET_API JetOSSnapshotFreeze(
      __in          const JET_OSSNAPID snapId,
      __out         unsigned long* pcInstanceInfo,
      __out         JET_INSTANCE_INFO** paInstanceInfo,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parameter

*snapId*

Der Bezeichner der Momentaufnahmesitzung.

*pcInstanceInfo*

Die Anzahl der derzeit in der Engine ausgeführten Instanzen, die Teil der Momentaufnahmesitzung sind.

*paInstanceInfo*

Ein Array von -Strukturen, eine für jede ausgeführte Instanz, die Teil der Momentaufnahmesitzung ist, die die Instanz und die Datenbanken beschreibt, die teil davon sind.

*grbit*

Die Optionen für diesen Aufruf. Dieser Parameter ist für die zukünftige Verwendung reserviert, und der einzige unterstützte gültige Wert ist 0.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Die für die Ausgabeparameter bereitgestellten Zeiger sind NULL, die Momentaufnahmesitzung ist ungültig, oder der <em>grbit-Parameter</em> ist ungültig.</p> | 
| <p>JET_errOSSnapshotInvalidSequence</p> | <p>Die Momentaufnahmesitzung befindet sich nicht im entsprechenden Zustand, um ein Einfrieren zu starten (z. B. ist bei dieser Sitzung zuvor ein vorheriger Einfrieren fehlgeschlagen).</p> | 
| <p>JET_errOSSnapshotNotAllowed</p> | <p>Die Engine befindet sich nicht in einem Zustand, in dem eine Momentaufnahme ausgeführt werden kann. Mindestens eine Streamingsicherung wird bereits ausgeführt, oder eine oder mehrere Instanzen werden wiederherstellungsschritte ausgeführt oder werden beendet.</p> | 
| <p>JET_errOSSnapshotInvalidSnapId</p> | <p>Der Bezeichner für die Momentaufnahmesitzung ist ungültig.</p> | 
| <p>JET_errOutOfMemory</p> | <p>Fehler bei der Funktion aufgrund einer nicht genügenden Arbeitsspeicherbedingung.</p> | 
| <p>JET_errOutOfThreads</p> | <p>Fehler bei der Funktion, weil ein neuer Thread, der das Einfrieren durchfing, nicht gestartet werden konnte.</p> | 



Wenn diese Funktion erfolgreich ist, werden keine Schreib-IOs für die Datenbankdateien oder die Protokolldateien ausgegeben, die Teil von instanzen sind, die fixiert sind. Außerdem werden die Instanzinformationen ordnungsgemäß ausgefüllt und müssen später durch Aufrufen von [JetFreeBuffer](./jetfreebuffer-function.md) mit dem Zeiger auf das zurückgegebene Instanzinformationsarray frei werden.

Wenn diese Funktion fehlschlägt, wird die Engine weiterhin normal ausgeführt, während die E/A-Vorgänge wie gewohnt ausgeführt werden. Es ist nicht notwendig, [JetOSSnapshotThaw aufrufen,](./jetossnapshotthaw-function.md) wenn beim Einfrieren ein Fehler auftritt. Außerdem werden die Instanzinformationen nicht ausgefüllt, sodass diese Ressource nicht frei werden muss.

#### <a name="remarks"></a>Hinweise

Während des Einfrierenzeitraums werden keine Schreib-E/A-Dateien für die angefügten Datenbanken oder Transaktionsprotokolle ausgegeben, obwohl möglicherweise Schreib-E/A-Dateien für die temporären Datenbanken oder Streamingdateien ausgegeben werden.

Der Zustand, in dem sich die Datenbanken und die Protokolldateien während des Einfrierens befinden (der Zustand, in dem sich die Dateien in einem Volumemomentaufnahme-Image befinden), ist so, dass eine normale Wiederherstellung möglich ist, wenn diese Dateien später wiederhergestellt werden.

Da während des Einfrierens keine Schreibvorgänge ausgeführt werden, werden normale API-Aufrufe an die Engine für dieses Intervall möglicherweise nicht mehr ausgeführt. Die Clientanwendung muss API-Aufrufe verarbeiten können, die möglicherweise länger dauern als normal, wenn ein Einfrieren auftritt.

Aufgrund der oben beschriebenen möglichen Auswirkungen gibt es ein internes Timeout, nach dem die Momentaufnahmesitzung die Einfrierenphase beendet, auch wenn die APIs, die das Aufsperren oder Abbrechen tun, nicht aufgerufen wurden. Der Wert des Timeouts kann mithilfe des JET_paramOSSnapshotTimeout [geändert](./backup-and-restore-parameters.md) werden. Beachten Sie, dass das typische Einfrierenintervall im Bereich von 10 Sekunden liegt und das Standardzeitüberschreitungsintervall ungefähr 60 Sekunden beträgt.

#### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista oder Windows XP.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008 oder Windows Server 2003.</p> | | <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | | <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Implementiert als <strong>JetOSSnapshotFreezeW</strong> (Unicode) und <strong>JetOSSnapshotFreezeA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_INSTANCE_INFO](./jet-instance-info-structure.md)  
[JET_OSSNAPID](./jet-ossnapid.md)  
[JetOSSnapshotAbort](./jetossnapshotabort-function.md)  
[JetOSSnapshotPrepare](./jetossnapshotprepare-function.md)  
[JetOSSnapshotPrepareInstance](./jetossnapshotprepareinstance-function.md)  
[JetOSSnapshotThaw](./jetossnapshotthaw-function.md)
