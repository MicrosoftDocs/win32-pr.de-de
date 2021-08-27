---
description: Weitere Informationen finden Sie unter JetOSSnapshotEnd-Funktion.
title: JetOSSnapshotEnd-Funktion
TOCTitle: JetOSSnapshotEnd Function
ms:assetid: f7f4db8b-8e40-48d7-bc7b-0c80d0d0f77f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294136(v=EXCHG.10)
ms:contentKeyID: 32765750
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotEnd
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b57528899b8d78ecee31f6dd54c2ac8decece383
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984433"
---
# <a name="jetossnapshotend-function"></a>JetOSSnapshotEnd-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetossnapshotend-function"></a>JetOSSnapshotEnd-Funktion

Die **JetOSSnapshotEnd-Funktion** benachrichtigt die Engine, dass die Momentaufnahmesitzung beendet wurde.

**Windows Vista:****JetOSSnapshotEnd** wird in Windows Vista: eingeführt.  

```cpp
    JET_ERR JET_API JetOSSnapshotEnd(
      __in          const JET_OSSNAPID snapId,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parameter

*snapId*

Der Bezeichner der Momentaufnahmesitzung.

*grbit*

Die Optionen für diesen Aufruf. Dieser Parameter kann eine Kombination der folgenden Werte enthalten.


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>0</p> | <p>Das erfolgreiche Ende der Momentaufnahmesitzung.</p> | 
| <p>JET_bitAbortSnapshot</p> | <p>Die Momentaufnahmesitzung wurde abgebrochen.</p> | 



### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errInvalidGrbit</p> | <p>Eine der angeforderten Optionen ist ungültig, wird falsch verwendet oder nicht implementiert.</p> | 
| <p>JET_errOSSnapshotInvalidSequence</p> | <p>Eine Momentaufnahmesitzung wird bereits erstellt. Dies ist nicht zulässig.</p> | 
| <p>JET_errOSSnapshotInvalidSnapId</p> | <p>Der Bezeichner für die Momentaufnahmesitzung ist ungültig.</p> | 
| <p>JET_errOSSnapshotTimeOut</p> | <p>Für die Momentaufnahmesitzung ist ein internes Timeout aufgetreten, bevor dieser Aufruf aufgetreten ist. Daher wurden die E/A-Vorgänge wieder normal, bevor dieser Aufruf erfolgt ist.</p> | 



Wenn diese Funktion erfolgreich ist, wird eine Momentaufnahmesitzung abgeschlossen, und das normale Engine-Verhalten wird fortgesetzt. Eine neue Momentaufnahmesitzung kann später gestartet werden.

Wenn diese Funktion fehlschlägt, wird der JET_errOSSnapshotTimeOut zurückgegeben, und die aktuelle Momentaufnahmesitzung wird beendet, aber das Einfrieren von E/A-Daten während des Momentaufnahmezeitraums wurde intern nicht beachtet. Bei allen anderen Fehlern wird der Momentaufnahmesitzungsstatus nicht geändert.

#### <a name="remarks"></a>Bemerkungen

Diese Funktion wird nur aufgerufen, wenn [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) mit einem JET_bitContinueAfterThaw.

Die Momentaufnahmesitzung muss abgeschlossen sein, damit die Momentaufnahmeüberprüfung und die Protokoll abgeschnitten werden. Ereignisprotokolleinträge werden für die verschiedenen Schritte der Momentaufnahme generiert.

#### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008.</p> | 
| <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | 
| <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[Fehlerbehandlungsparameter](./error-handling-parameters.md)  
[Erweiterbare Storage Engine-Fehler](./extensible-storage-engine-errors.md)  
[JET_ERR](./jet-err.md)  
[JetOSSnapshotThaw](./jetossnapshotthaw-function.md)
