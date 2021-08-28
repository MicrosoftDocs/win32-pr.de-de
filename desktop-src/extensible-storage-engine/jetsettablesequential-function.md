---
description: 'Weitere Informationen zu: JetSetTableSequential-Funktion'
title: JetSetTableSequential-Funktion
TOCTitle: JetSetTableSequential Function
ms:assetid: 874ddd3c-0d69-4d48-b61a-e9e0457426ef
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269323(v=EXCHG.10)
ms:contentKeyID: 32765613
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetTableSequential
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0a8b49b112c9566b15226e8ffd52f4240cff2fb8
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471716"
---
# <a name="jetsettablesequential-function"></a>JetSetTableSequential-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetsettablesequential-function"></a>JetSetTableSequential-Funktion

Die **JetSetTableSequential-Funktion** benachrichtigt die Datenbank-Engine, dass die Anwendung den gesamten aktuellen Index scannt, der einen bestimmten Cursor enthält. Folglich werden die Methoden, die für den Zugriff auf die Indexdaten verwendet werden, optimiert, um dieses Szenario so schnell wie möglich zu gestalten.

**Windows XP:****JetSetTableSequential** wird in Windows XP eingeführt.  

```cpp
    JET_ERR JET_API JetSetTableSequential(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parameter

*sesid*

Die Sitzung, die für diesen Aufruf verwendet werden soll.

*tableid*

Der Cursor, der für diesen Aufruf verwendet werden soll.

*grbit*

Eine Gruppe von Bits, die null oder mehr der folgenden Optionen angeben.


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>JET_bitPrereadForward</p> | <p>Diese Option wird zum Indizierung in Vorwärtsrichtung verwendet.</p><p><strong>Windows 7:</strong><strong>JET_bitPrereadForward</strong> wird in Windows 7 eingeführt.  </p> | 
| <p>JET_bitPrereadBackward</p> | <p>Diese Option wird zum Indizierung in rückwärts gerichteter Richtung verwendet.</p><p><strong>Windows 7:</strong><strong>JET_bitPrereadBackward</strong> wird in Windows 7 eingeführt.  </p> | 



### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errClientRequestToStopJetService</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da alle Aktivitäten auf der -Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufs von <a href="gg269240(v=exchg.10).md">JetStopService</a>in den Stillstand gebracht wurden.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da für die Instanz, die der Sitzung zugeordnet ist, ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen.</p><p><strong>Windows XP:</strong>  Dieser Rückgabewert wird in Windows XP eingeführt.</p> | 
| <p>JET_errNotInitialized</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da ein Wiederherstellungsvorgang für die Instanz ausgeführt wird, die der Sitzung zugeordnet ist.</p> | 
| <p>JET_errTermInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</p> | 



Wenn diese Funktion erfolgreich ausgeführt wird, ist der aktuelle Index des Cursors für eine sequenzielle Überprüfung des gesamten Indexes optimiert. Es erfolgt keine Änderung des Datenbankzustands.

Wenn diese Funktion fehlschlägt, erfolgt keine Änderung an der Konfiguration des Cursors. Es erfolgt keine Änderung des Datenbankzustands.

#### <a name="remarks"></a>Hinweise

Wenn die Anwendung eine bekannte Teilmenge eines Indexes effizient überprüfen muss, wird eine ähnliche Optimierung auch durchgeführt, wenn ein Indexbereich mit [JetSetIndexRange](./jetsetindexrange-function.md)eingerichtet wird. Diese Optimierung ist nur in Windows XP und späteren Versionen verfügbar.

Wenn die Anwendung eine unbekannte Teilmenge eines Indexes effizient überprüfen muss, sollte keine Aktion ausgeführt werden. Die Engine kann das Überprüfungsverhalten automatisch erkennen und ruft Daten im Voraus ab. Dieses Verhalten ist jedoch nicht so aggressiv.

Durch diese Optimierung wird das Scannen des primären Indexes effizient und das Scannen nur der Indexeintragsdaten in einem sekundären Index effizient. Dadurch wird das Scannen eines sekundären Indexes beim Effizienten Abrufen von Datensatzdaten nicht ermöglicht. Dies liegt daran, dass die Engine keine Lese-/Vorlesefunktion für die Datensatzdaten ausführt.

#### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista oder Windows XP.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008 oder Windows Server 2003.</p> | | <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | | <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetSetIndexRange](./jetsetindexrange-function.md)  
[JetStopService](./jetstopservice-function.md)
