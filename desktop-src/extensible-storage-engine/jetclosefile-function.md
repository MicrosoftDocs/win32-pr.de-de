---
description: Weitere Informationen finden Sie unter JetCloseFile-Funktion.
title: JetCloseFile-Funktion
TOCTitle: JetCloseFile Function
ms:assetid: e8930915-8102-44b0-ae42-abedbd3e0512
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294127(v=EXCHG.10)
ms:contentKeyID: 32765741
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCloseFile
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ad8f40f53ec23a5a555efeb270370d384d6dc9a6
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122989053"
---
# <a name="jetclosefile-function"></a>JetCloseFile-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetclosefile-function"></a>JetCloseFile-Funktion

Die **JetCloseFile-Funktion** schließt eine Datei, die mit [JetOpenFile](./jetopenfile-function.md) geöffnet wurde, nachdem die Daten aus dieser Datei mit [JetReadFile extrahiert wurden.](./jetreadfile-function.md)

```cpp
    JET_ERR JET_API JetCloseFile(
      __in          JET_HANDLE hfFile
    );
```

### <a name="parameters"></a>Parameter

*hfFile*

Das Handle der zu lesenden Datei.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Es ist nicht möglich, den Vorgang abschließen, da alle Aktivitäten auf der -Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufs von <a href="gg269240(v=exchg.10).md">JetStopService beendet wurden.</a></p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da für die der Sitzung zugeordnete Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen.</p><p>Dieser Fehler wird nur von xp Windows und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Einer der bereitgestellten Parameter enthielt einen unerwarteten Wert oder einen Wert, der in Kombination mit dem Wert eines anderen Parameters nicht sinnvoll war. Dies kann für <strong>JetCloseFile passieren,</strong> wenn:</p><ul><li><p>Das angegebene Instanzhand handle ist ungültig (Windows XP und spätere Versionen).</p></li><li><p>Das angegebene Dateihand handle ist ungültig.</p></li></ul> | 
| <p>JET_errNoBackup</p> | <p>Der Vorgang ist fehlgeschlagen, da keine externe Sicherung durchgeführt wird.</p> | 
| <p>JET_errNotInitialized</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz noch nicht initialisiert wurde.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da ein Wiederherstellungsvorgang für die -Instanz durchgeführt wird, die der Sitzung zugeordnet ist.</p> | 
| <p>JET_errRunningInMultiInstanceMode</p> | <p>Der Vorgang ist fehlgeschlagen, weil versucht wurde, die Engine im Legacymodus (Windows 2000-Kompatibilitätsmodus) zu verwenden, bei dem nur eine Instanz unterstützt wird, wenn tatsächlich bereits mehrere Instanzen vorhanden sind.</p> | 
| <p>JET_errTermInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz heruntergefahren wird.</p> | 



Bei Erfolg wird das Dateihand handle geschlossen. Wenn eine Datenbankdatei geschlossen wurde, wird die zugeordnete Datenbankpatchdatei (sofern vorhanden) zerstört.

Bei einem Fehler erfolgt keine Änderung.

#### <a name="remarks"></a>Bemerkungen

Die Datenbank-Engine unterstützt derzeit nur eine geöffnete Datei über [JetOpenFile.](./jetopenfile-function.md) Wenn ein Dateihand handle mit [JetOpenFile](./jetopenfile-function.md) geöffnet wird, muss es mit **JetCloseFile** geschlossen werden, bevor eine andere Datei geöffnet werden kann.

#### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | 
| <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_HANDLE](./jet-handle.md)  
[JetOpenFile](./jetopenfile-function.md)  
[JetReadFile](./jetreadfile-function.md)  
[JetStopService](./jetstopservice-function.md)
