---
description: 'Weitere Informationen zu: jetinit-Funktion'
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
ms.openlocfilehash: 308c012bc5eb144e0ac0d608c64d63ccf39aeca1
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "104356216"
---
# <a name="jetinit-function"></a>JetInit-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetinit-function"></a>JetInit-Funktion

Die **jetinit** -Funktion versetzt die Datenbank-Engine in einen Zustand, in dem Sie die Anwendungs Verwendung von Datenbankdateien unterstützen kann. Die Engine muss für die Initialisierung mit [jetsetsystemparameter](./jetsetsystemparameter-function.md)bereits ordnungsgemäß konfiguriert sein. Die Daten Bank Absturz Wiederherstellung wird automatisch als Teil des Initialisierungs Prozesses ausgeführt.

```cpp
JET_ERR JET_API JetInit(
  __in_out_opt  JET_INSTANCE* pinstance
);
```

### <a name="parameters"></a>Parameter

*pinstance*

Die-Instanz, die für diesen Befehl verwendet werden soll.

Für Windows 2000 wird dieser Parameter ignoriert und sollte immer NULL sein.

Für Windows XP und spätere Versionen hängt die Verwendung dieses Parameters vom Betriebsmodus der Engine ab. Wenn die Engine im Legacy Modus betrieben wird (Windows 2000-Kompatibilitätsmodus), in dem nur eine Instanz unterstützt wird, kann dieser Parameter entweder NULL sein, oder er kann auf einen gültigen Ausgabepuffer festgelegt werden, der das globale Instanzhandle zurückgibt, das als Nebeneffekt der Initialisierung erstellt wurde. Dieser Ausgabepuffer muss auf NULL oder JET_instanceNil festgelegt werden. Dieser Instanzhandle kann dann an jede andere Funktion weitergegeben werden, die eine-Instanz verwendet. Wenn die Engine im Modus für mehrere Instanzen ausgeführt wird, muss dieser Parameter auf einen gültigen Eingabepuffer festgelegt werden, der das Instanzhandle enthält, das von der initialisierten [jetkreateinstance](./jetcreateinstance-function.md) -Funktions Instanz zurückgegeben wird.


#### <a name="remarks"></a>Bemerkungen

Eine Instanz muss mit einem **calltinit** -Namen initialisiert werden, bevor Sie von einem anderen als [jetsetsystemparameter](./jetsetsystemparameter-function.md)verwendet werden kann.

Eine Instanz wird durch einen-Rückruf der [jetterm](./jetterm-function.md) -Funktion zerstört, auch wenn diese Instanz nicht mit **jetinit** initialisiert wurde. Eine Instanz ist die Wiederherstellbarkeits Einheit für die Datenbank-Engine. Er steuert den Lebenszyklus aller Dateien, mit denen die Integrität der Daten in einem Satz von Datenbankdateien geschützt wird. Diese Dateien enthalten die Prüf Punkt Datei und die Transaktionsprotokoll Dateien.

Die maximale Anzahl von Instanzen, die zu einem beliebigen Zeitpunkt erstellt werden können, wird durch [JET_paramMaxInstances](./resource-parameters.md)gesteuert, der durch einen Aufruf von [jetsetsystemparameter](./jetsetsystemparameter-function.md)konfiguriert werden kann. Wenn die Datenbank-Engine zum ersten Mal initialisiert wird, erstellt **jetinit** einen anfänglichen Satz von Dateien, um diese Instanz zu unterstützen. Diese Dateien enthalten eine Prüf Punkt Datei (mit dem Namen) \<[JET_paramBaseName](./transaction-log-parameters.md)\> . CHK), eine Reihe von reservierten Transaktionsprotokoll Dateien (mit dem Namen RES1. Log und RES2. Log), eine anfängliche Transaktionsprotokoll Datei (mit dem Namen) \<[JET_paramBaseName](./transaction-log-parameters.md)\> . Log) und eine temporäre Datenbankdatei (benannt nach [JET_paramTempPath](./temporary-database-parameters.md)). Wenn [JET_paramRecovery](./transaction-log-parameters.md) auf "Off" festgelegt ist, werden die Prüf Punkt Datei und die Protokolldateien nicht erstellt. Wenn [JET_paramMaxTemporaryTables](./temporary-database-parameters.md) auf NULL festgelegt ist, wird die temporäre Datenbankdatei nicht erstellt. Diese Dateien stellen den Speicherbedarf einer Instanz auf einem Datenträger dar und müssen mit Bedacht verwaltet werden. Wenn diese Dateien einzeln oder in Bezug auf einen anderen beschädigt werden, gehen die Daten, die in den Datenbanken gespeichert sind, die der Instanz zugeordnet sind, möglicherweise verloren.

Wenn die Datenbank-Engine mit einem vorhandenen Satz von Transaktionsprotokoll Dateien initialisiert wird, werden diese Dateien überprüft, um festzustellen, ob die vorherige Inkarnation der Instanz durch einen Absturz verursacht wurde. Wenn ein Absturz erkannt wird, wird automatisch die Wiederherstellung von Abstürzen ausgeführt. Bei diesem Vorgang werden die Datenbanken, die während der vorherigen Inkarnation der Engine an die Instanz angefügt sind, rekonstruiert und die Änderungen in den Datenbankdateien wieder hergestellt. Das Ergebnis sind Datenbanken, die Transaktions konsistent sind. Dieser Vorgang kann einige Zeit in Anspruch nehmen, wenn die Anzahl der Transaktionsprotokoll Dateien, die für die Datenbanken wiedergegeben werden sollen, sehr groß ist.

Aufgrund der Tatsache, dass **jetinit** die Wiederherstellung von Abstürzen ausführt, ist es möglich, dass im Falle eines Fehlers fast jeder Datenbank-Engine-Fehler zurückgegeben wird. In der Praxis werden die meisten Fehler in der Bereitstellung in zwei Kategorien unterteilt: Daten Beschädigung und Datei Misswirtschaft. Daten Beschädigungen werden am häufigsten in den folgenden oder ähnlichen Fehlern angezeigt:

  - JET_errReadVerifyFailure

  - JET_errLogFileCorrupt

  - JET_errCheckpointCorrupt

Diese Fehler werden fast immer durch Hardwareprobleme verursacht und können daher nicht vermieden werden. Die Datei Misswirtschaft wird am häufigsten in den folgenden oder ähnlichen Fehlern angezeigt:

  - JET_errMissingLogFile

  - JET_errAttachedDatabaseMismatch

  - JET_errDatabaseSharingViolation

  - JET_errInvalidLogSequence

Wenn die Wiederherstellung für eine Gruppe von Protokollen ausgeführt wird, für die nicht alle Datenbanken vorhanden sind (was den Fehler JET_errAttachedDatabaseMismatch unter normalen Umständen zurückgibt), und der Client wünscht, dass die Wiederherstellung trotz fehlender Datenbanken fortgesetzt wird, kann die JET_ bitreplayignoremissingdb verwendet werden, um die Wiederherstellung der verfügbaren Datenbanken fortzusetzen. Diese Fehler können von der Anwendung verhindert werden. Die Anwendung muss darauf achten, das Repository dieser Dateien vor der Bearbeitung durch externe Kräfte wie z. b. den Benutzer oder andere Anwendungen zu schützen. Wenn die Anwendung eine Instanz vollständig zerstören möchte, müssen alle Dateien, die der Instanz zugeordnet sind, gelöscht werden. Hierzu gehören die Prüf Punkt Datei, die Transaktionsprotokoll Dateien und alle Datenbankdateien, die an die Instanz angefügt sind.

Die **jetinit** -Funktion verhält sich in Bezug auf die Datenbankdateien, die an die Instanz angefügt sind, zwischen Windows 2000 und neueren Versionen anders.

**Windows 2000:**  In Windows 2000 bleibt jede Datenbank, die während einer früheren Inkarnation dieser Instanz an die Instanz angefügt ist, nach der erfolgreichen Ausführung von **jetinit** an die Instanz angefügt. Es ist nicht erforderlich, [jetattachdatabase](./jetattachdatabase-function.md) nach **jetinit** aufzurufen, um den späteren Datenbankzugriff zu gewährleisten. Wenn die [jetattachdatabase](./jetattachdatabase-function.md) -Funktion nach der **jetinit** -Funktion aufgerufen wird, wird die JET_wrnDatabaseAttached Warnung zurückgegeben. Diese Warnung gibt an, dass die Daten Bank Anlage beibehalten wurde und ignoriert werden kann.

**Windows XP:**  In Windows XP und späteren Versionen werden alle Datenbanken von **jetinit** automatisch von der Instanz getrennt. Dies bedeutet, dass [jetattachdatabase](./jetattachdatabase-function.md) in diesem Fall immer nach **jetinit** aufgerufen werden muss.

Jede Anwendung, die für die Ausführung unter Windows 2000 und späteren Versionen geschrieben wird, muss [jetattachdatabase](./jetattachdatabase-function.md) nach **jetinit** immer anrufen. Wenn die Anwendung unter Windows 2000 ausgeführt wird, muss Sie in einigen Fällen JET_wrnDatabaseAttached erwarten. Weitere Informationen finden Sie unter [jetattachdatabase](./jetattachdatabase-function.md) .

#### <a name="requirements"></a>Anforderungen

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>In "ESENT. h" deklariert.</p></td>
</tr>
<tr class="even">
<td><p><strong>Bibliothek</strong></p></td>
<td><p>Verwenden Sie ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>Erfordert ESENT.dll.</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Weitere Informationen

[Extensible Storage Engine-Dateien](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_paramMaxTemporaryTables](./temporary-database-parameters.md)  
[JET_paramRecovery](./transaction-log-parameters.md)  
[Jetattachdatabase](./jetattachdatabase-function.md)  
[Jetkreateingestance](./jetcreateinstance-function.md)  
[JetInit3](./jetinit3-function.md)  
[Jetsetsystemparameter](./jetsetsystemparameter-function.md)
