---
description: 'Weitere Informationen zu: JetCloseFileInstance-Funktion'
title: JetCloseFileInstance-Funktion
TOCTitle: JetCloseFileInstance Function
ms:assetid: 64a38655-b128-453b-9593-46032bd6c470
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269270(v=EXCHG.10)
ms:contentKeyID: 32765572
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCloseFileInstance
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d837d1932559c39d6a3b249f934ef77cc56de11a
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122982978"
---
# <a name="jetclosefileinstance-function"></a>JetCloseFileInstance-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetclosefileinstance-function"></a>JetCloseFileInstance-Funktion

Die **JetCloseFileInstance-Funktion** schließt eine Datei, die mit [JetOpenFileInstance](./jetopenfileinstance-function.md) geöffnet wurde, nachdem die Daten aus dieser Datei mit [JetReadFileInstance](./jetreadfileinstance-function.md)extrahiert wurden.

**Windows XP: JetCloseFileInstance** wird in Windows XP eingeführt.

```cpp
    JET_ERR JET_API JetCloseFileInstance(
      __in          JET_INSTANCE instance,
      __in          JET_HANDLE hfFile
    );
```

### <a name="parameters"></a>Parameter

*Instanz*

Die -Instanz, die für diesen Aufruf verwendet werden soll.

Für Windows 2000 ist die API-Variante, die diesen Parameter akzeptiert, nicht verfügbar, da nur eine Instanz unterstützt wird. Die Verwendung dieser globalen Instanz wird in diesem Fall impliziert.

Für Windows XP und höhere Versionen kann die API-Variante, die diesen Parameter nicht akzeptiert, nur aufgerufen werden, wenn sich die Engine im Legacymodus befindet (Windows Kompatibilitätsmodus 2000), in dem nur eine Instanz unterstützt wird. Andernfalls schlägt der Vorgang mit JET_errRunningInMultiInstanceMode fehl.

*hfFile*

Das Handle der zu lesenden Datei.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, als Ergebnis eines Aufrufs von <a href="gg294108(v=exchg.10).md">JetStopServiceInstance</a>aufgetreten sind.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da für die instanz, die der Sitzung zugeordnet ist, ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen.</p><p>Dieser Fehler wird nur von Windows XP und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Einer der bereitgestellten Parameter enthielt einen unerwarteten Wert, oder die Kombination mehrerer Parameterwerte führte zu einem unerwarteten Ergebnis. Dies kann für <strong>JetCloseFileInstance</strong> passieren, wenn:</p><ul><li><p>Das angegebene Instanzhandle ist ungültig (Windows XP und spätere Versionen).</p></li><li><p>Das angegebene Dateihandle ist ungültig.</p></li></ul> | 
| <p>JET_errNoBackup</p> | <p>Fehler beim Vorgang, weil keine externe Sicherung ausgeführt wird.</p> | 
| <p>JET_errNotInitialized</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da die der Sitzung zugeordnete Instanz noch nicht initialisiert wurde.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da ein Wiederherstellungsvorgang für die Instanz ausgeführt wird, die der Sitzung zugeordnet ist.</p> | 
| <p>JET_errRunningInMultiInstanceMode</p> | <p>Fehler beim Vorgang, weil versucht wurde, die Engine im Legacymodus (Windows 2000-Kompatibilitätsmodus) zu verwenden, wobei nur eine Instanz unterstützt wird, wenn tatsächlich bereits mehrere Instanzen vorhanden sind.</p> | 
| <p>JET_errTermInProgress</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da die der Sitzung zugeordnete Instanz heruntergefahren wird.</p> | 



Bei Erfolg wird das Dateihandle geschlossen. Wenn eine Datenbankdatei geschlossen wurde, wird die zugeordnete Datenbankpatchdatei (falls vorhanden) zerstört.

Bei einem Fehler erfolgt keine Änderung.

#### <a name="remarks"></a>Bemerkungen

Die Datenbank-Engine unterstützt derzeit nur jeweils eine geöffnete Datei über [JetOpenFileInstance.](./jetopenfileinstance-function.md) Wenn ein Dateihandle mit [JetOpenFileInstance](./jetopenfileinstance-function.md) geöffnet wird, muss es mithilfe von **JetCloseFileInstance** geschlossen werden, bevor eine andere Datei geöffnet werden kann.

#### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista oder Windows XP.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008 oder Windows Server 2003.</p> | 
| <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | 
| <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_HANDLE](./jet-handle.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetOpenFileInstance](./jetopenfileinstance-function.md)  
[JetReadFileInstance](./jetreadfileinstance-function.md)  
[JetStopServiceInstance](./jetstopserviceinstance-function.md)
