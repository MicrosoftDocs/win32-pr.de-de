---
description: 'Weitere Informationen finden Sie unter: JetOSSnapshotGetFreezeInfo-Funktion'
title: JetOSSnapshotGetFreezeInfo-Funktion
TOCTitle: JetOSSnapshotGetFreezeInfo Function
ms:assetid: b94eaf91-7407-4c62-ab1e-3249ad076c1a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294070(v=EXCHG.10)
ms:contentKeyID: 32765685
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotGetFreezeInfo
- JetOSSnapshotGetFreezeInfoA
- JetOSSnapshotGetFreezeInfoW
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e737d6fe31dde43eeba7526e740ec096db20abc9
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466207"
---
# <a name="jetossnapshotgetfreezeinfo-function"></a>JetOSSnapshotGetFreezeInfo-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetossnapshotgetfreezeinfo-function"></a>JetOSSnapshotGetFreezeInfo-Funktion

Die **JetOSSnapshotGetFreezeInfo-Funktion** ruft die Liste der Instanzen und Datenbanken ab, die zu einem bestimmten Zeitpunkt Teil der Momentaufnahmesitzung sind.

**Windows Vista:****JetOSSnapshotGetFreezeInfo** wird in Windows Vista eingeführt.  

```cpp
    JET_ERR JET_API JetOSSnapshotGetFreezeInfo(
      __in          const JET_OSSNAPID snapId,
      __out         unsigned long* pcInstanceInfo,
      __out         JET_INSTANCE_INFO** paInstanceInfo,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parameter

*snapId*

Der Bezeichner der momentaufnahmesitzung, die gestartet werden soll.

*pcInstanceInfo*

Die Anzahl der derzeit ausgeführten Instanzen, die Teil der Momentaufnahmesitzung sind.

*paInstanceInfo*

Ein Array von -Strukturen, eine für jede ausgeführte Instanz, die die Instanz und die Datenbanken beschreibt, die teil davon sind.

*grbit*

Die Optionen für diesen Aufruf. Dieser Parameter ist für die zukünftige Verwendung reserviert. Der einzige gültige Wert ist 0 (null).

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errOutOfMemory</p> | <p>Fehler bei der Funktion aufgrund einer nicht genügenden Arbeitsspeicherbedingung.</p> | 
| <p>JET_errInvalidParameter</p> | <p><em>pcInstanceInfo</em> oder <em>paInstanceInfo</em> ist <strong>NULL.</strong></p> | 
| <p>JET_errOSSnapshotInvalidSnapId</p> | <p>Der Bezeichner für die Momentaufnahmesitzung ist ungültig.</p> | 
| <p>JET_errOSSnapshotInvalidSequence</p> | <p>Eine Momentaufnahmesitzung wird nicht in Bearbeitung.</p> | 



Wenn diese Funktion erfolgreich ausgeführt wird, werden die Instanzinformationen ordnungsgemäß ausgefüllt und müssen später durch Aufrufen von [JetFreeBuffer](./jetfreebuffer-function.md) mit dem Zeiger auf das zurückgegebene Instanzinformationsarray frei werden.

Wenn diese Funktion fehlschlägt, erfolgt keine Änderung des Engine-Zustands.

#### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008.</p> | | <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | | <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Implementiert als <strong>JetOSSnapshotGetFreezeInfoW</strong> (Unicode) und <strong>JetOSSnapshotGetFreezeInfoA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Weitere Informationen

[Fehlerbehandlungsparameter](./error-handling-parameters.md)  
[Erweiterbare Storage Engine-Fehler](./extensible-storage-engine-errors.md)  
[JET_ERR](./jet-err.md)  
[JetFreeBuffer](./jetfreebuffer-function.md)  
[JetOSSnapshotAbort](./jetossnapshotabort-function.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)  
[JetOSSnapshotThaw](./jetossnapshotthaw-function.md)
