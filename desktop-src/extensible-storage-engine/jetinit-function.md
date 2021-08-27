---
description: Weitere Informationen finden Sie unter JetInit-Funktion.
title: JetInit-Funktion
TOCTitle: JetInit Function
ms:assetid: b7f78cca-7268-4045-bda2-20746b1d6370
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294068(v=EXCHG.10)
ms:contentKeyID: 32765683
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetInit
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d074e07dec88bf0b33ec56b1391986758fbd388c
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984533"
---
# <a name="jetinit-function"></a>JetInit-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetinit-function"></a>JetInit-Funktion

Die **JetInit-Funktion** versetzt die Datenbank-Engine in einen Zustand, in dem sie die Anwendungsnutzung von Datenbankdateien unterstützen kann. Die Engine muss bereits ordnungsgemäß für die Initialisierung mit [JetSetSystemParameter konfiguriert sein.](./jetsetsystemparameter-function.md) Die Datenbankabsturzwiederherstellung wird automatisch als Teil des Initialisierungsprozesses ausgeführt.

```cpp
JET_ERR JET_API JetInit(
  __in_out_opt  JET_INSTANCE* pinstance
);
```

### <a name="parameters"></a>Parameter

*Pinstance*

Die -Instanz, die für diesen Aufruf verwendet werden soll.

Für Windows 2000 wird dieser Parameter ignoriert und sollte immer NULL sein.

Bei Windows XP und späteren Versionen hängt die Verwendung dieses Parameters vom Betriebsmodus der Engine ab. Wenn die Engine im Legacymodus (Windows 2000-Kompatibilitätsmodus) ausgeführt wird, in dem nur eine Instanz unterstützt wird, kann dieser Parameter entweder NULL sein oder auf einen gültigen Ausgabepuffer festgelegt werden, der das globale Instanzhand handle zurückgibt, das als Nebeneffekt der Initialisierung erstellt wurde. Dieser Ausgabepuffer muss auf NULL oder JET_instanceNil. Dieses Instanzhand handle kann dann an jede andere Funktion übergeben werden, die eine -Instanz verwendet. Wenn die Engine im Modus mit mehreren Instanzen ausgeführt wird, muss dieser Parameter auf einen gültigen Eingabepuffer festgelegt werden, der das Instanzhandl enthält, das von der [initialisierten JetCreateInstance-Funktionsinstanz](./jetcreateinstance-function.md) zurückgegeben wird.


#### <a name="remarks"></a>Bemerkungen

Eine -Instanz muss mit einem Aufruf von **JetInit** initialisiert werden, bevor sie von etwas anderem als [JetSetSystemParameter verwendet werden kann.](./jetsetsystemparameter-function.md)

Eine -Instanz wird durch einen Aufruf der [JetTerm-Funktion](./jetterm-function.md) zerstört, auch wenn diese Instanz nie mit **JetInit initialisiert wurde.** Eine -Instanz ist die Einheit der Wiederherstellbarkeit für die Datenbank-Engine. Sie steuert den Lebenszyklus aller Dateien, die zum Schutz der Integrität der Daten in einer Gruppe von Datenbankdateien verwendet werden. Zu diesen Dateien gehören die Prüfpunktdatei und die Transaktionsprotokolldateien.

Die maximale Anzahl von Instanzen, die zu einem beliebigen Zeitpunkt erstellt werden können, wird durch [JET_paramMaxInstances](./resource-parameters.md)gesteuert, die durch einen Aufruf von [JetSetSystemParameter konfiguriert werden kann.](./jetsetsystemparameter-function.md) Wenn die Datenbank-Engine zum ersten Mal initialisiert wird, erstellt **JetInit** einen anfänglichen Satz von Dateien zur Unterstützung dieser Instanz. Diese Dateien enthalten eine Prüfpunktdatei (mit dem Namen \<[JET_paramBaseName](./transaction-log-parameters.md)\> ). CHK), eine Gruppe reservierter Transaktionsprotokolldateien (mit dem Namen RES1. LOG und RES2. LOG), eine anfängliche Transaktionsprotokolldatei (mit dem Namen \<[JET_paramBaseName](./transaction-log-parameters.md)\> ). LOG) und eine temporäre Datenbankdatei (benannt nach [JET_paramTempPath](./temporary-database-parameters.md)). Wenn [JET_paramRecovery](./transaction-log-parameters.md) auf "Aus" festgelegt ist, werden die Prüfpunktdatei und die Protokolldateien nicht erstellt. Wenn [JET_paramMaxTemporaryTables](./temporary-database-parameters.md) auf 0 (null) festgelegt ist, wird die temporäre Datenbankdatei nicht erstellt. Diese Dateien stellen die auf dem Datenträger einer Instanz dar und müssen mit Vorsicht verwaltet werden. Wenn diese Dateien einzeln oder in Bezug aufeinander beschädigt sind, gehen die daten, die in den datenbanken gespeichert sind, die der Instanz zugeordnet sind, möglicherweise verloren.

Wenn die Datenbank-Engine mit einem vorhandenen Satz von Transaktionsprotokolldateien initialisiert wird, werden diese Dateien überprüft, um zu überprüfen, ob die vorherige Incarnation der Instanz nach einem Absturz kam. Wenn ein Absturz erkannt wird, wird automatisch die Wiederherstellung des Absturzes durchgeführt. Bei diesem Vorgang werden die Datenbanken rekonstruiert, die während der vorherigen Inkarnation der Engine an die Instanz angefügt wurden, und die Änderungen werden in den Datenbankdateien gespeichert. Das Ergebnis sind Datenbanken, die transaktions konsistent sind. Dieser Prozess kann einige Zeit in Dauern dauern, wenn die Anzahl der Transaktionsprotokolldateien, die für die Datenbanken wiedergegeben werden, groß ist.

Aufgrund der Tatsache, dass **JetInit** eine Absturzwiederherstellung durchführt, ist es möglich, dass im Falle eines Fehlers fast jeder Datenbank-Engine-Fehler zurückgegeben wird. In der Praxis fallen die meisten Fehler, die bei der Bereitstellung auftreten, in zwei Kategorien: Datenbeschädigung und Dateifehlverwaltung. Datenbeschädigungen treten am häufigsten in den folgenden oder ähnlichen Fehlern auf:

  - JET_errReadVerifyFailure

  - JET_errLogFileCorrupt

  - JET_errCheckpointCorrupt

Diese Fehler werden fast immer durch Hardwareprobleme verursacht und können daher nicht vermieden werden. Die Fehlverwaltung von Dateien wird sich am häufigsten in den folgenden oder ähnlichen Fehlern manifestieren:

  - JET_errMissingLogFile

  - JET_errAttachedDatabaseMismatch

  - JET_errDatabaseSharingViolation

  - JET_errInvalidLogSequence

Wenn die Wiederherstellung für eine Gruppe von Protokollen ausgeführt wird, für die nicht alle Datenbanken vorhanden sind (wodurch unter normalen Umständen der Fehler JET_errAttachedDatabaseMismatch zurückgegeben wird) und der Client die Wiederherstellung trotz fehlender Datenbanken fortsetzen möchte, kann die JET_ bitReplayIgnoreMissingDB verwendet werden, um die Wiederherstellung für die verfügbaren Datenbanken fortzufahren. Diese Fehler können von der Anwendung verhindert werden. Die Anwendung muss darauf achten, das Repository dieser Dateien vor manipulation durch externe Erzwingungen wie den Benutzer oder andere Anwendungen zu schützen. Wenn die Anwendung eine Instanz vollständig zerstören möchte, müssen alle der Instanz zugeordneten Dateien gelöscht werden. Dazu gehören die Prüfpunktdatei, die Transaktionsprotokolldateien und alle Datenbankdateien, die an die Instanz angefügt sind.

Die **JetInit-Funktion** verhält sich in Bezug auf Datenbankdateien, die an die -Instanz angefügt sind, zwischen Windows 2000 und späteren Versionen unterschiedlich.

**Windows 2000:**  In Windows 2000 bleibt jede Datenbank, die während einer vorherigen Inkarnation dieser Instanz an die Instanz angefügt wurde, an die Instanz angefügt, nachdem **JetInit** erfolgreich abgeschlossen wurde. Es ist nicht erforderlich, [JetAttachDatabase nach](./jetattachdatabase-function.md) **JetInit aufzurufen,** um späteren Datenbankzugriff zu schützen. Wenn die [JetAttachDatabase-Funktion](./jetattachdatabase-function.md) nach der **JetInit-Funktion** aufgerufen wird, JET_wrnDatabaseAttached Warnung zurückgegeben. Diese Warnung gibt an, dass die Datenbankanlage beibehalten wurde und ignoriert werden kann.

**Windows XP:**  In Windows XP und späteren Versionen werden alle Datenbanken automatisch von der -Instanz durch **JetInit getrennt.** Dies bedeutet, [dass JetAttachDatabase](./jetattachdatabase-function.md) in diesem Fall immer nach **JetInit** aufgerufen werden muss.

Jede Anwendung, die für die Ausführung in Windows 2000 und in späteren Releases geschrieben wurde, muss [immer JetAttachDatabase](./jetattachdatabase-function.md) nach **JetInit aufrufen.** Wenn die Anwendung auf Windows 2000 ausgeführt wird, muss sie in einigen Fällen mit JET_wrnDatabaseAttached rechnen. Weitere Informationen finden Sie unter [JetAttachDatabase.](./jetattachdatabase-function.md)

#### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | 
| <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[Erweiterbare Storage-Engine-Dateien](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_paramMaxTemporaryTables](./temporary-database-parameters.md)  
[JET_paramRecovery](./transaction-log-parameters.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit3](./jetinit3-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)
