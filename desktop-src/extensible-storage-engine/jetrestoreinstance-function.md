---
description: Weitere Informationen finden Sie unter JetRestoreInstance-Funktion.
title: JetRestoreInstance-Funktion
TOCTitle: JetRestoreInstance Function
ms:assetid: 7ba2b6ee-96f5-44c5-9842-5e58580f60f1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269306(v=EXCHG.10)
ms:contentKeyID: 32765597
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRestoreInstanceW
- JetRestoreInstance
- JetRestoreInstanceA
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 700cbb29fe34700da953df5a20aa94d5a2df4a06
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985663"
---
# <a name="jetrestoreinstance-function"></a>JetRestoreInstance-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetrestoreinstance-function"></a>JetRestoreInstance-Funktion

Die **JetRestoreInstance-Funktion** stellt eine Streamingsicherung einer Instanz einschließlich aller angefügten Datenbanken wieder her. Sie ist für die Verwendung mit einer Sicherung konzipiert, die mit der [JetBackupInstance-Funktion erstellt](./jetbackupinstance-function.md) wurde. Dies ist die einfachste und am meisten gekapselte Wiederherstellungsfunktion.

**Windows XP:****JetRestoreInstance** wird in Windows XP eingeführt.  

```cpp
    JET_ERR JET_API JetRestoreInstance(
      __in          JET_INSTANCE instance,
      __in          JET_PCSTR sz,
      __in_opt      JET_PCSTR szDest,
      __in          JET_PFNSTATUS pfn
    );
```

### <a name="parameters"></a>Parameter

*Instanz*

Gibt die -Instanz an, die für diesen Aufruf verwendet werden soll.

Bei Windows XP und späteren Versionen hängt die Verwendung dieses Parameters vom Betriebsmodus der Engine ab. Wenn die Engine im Legacymodus (Windows 2000-Kompatibilitätsmodus) ausgeführt wird, in dem nur eine Instanz unterstützt wird, kann dieser Parameter entweder NULL sein oder auf einen gültigen Ausgabepuffer mit NULL oder JET_instanceNil festgelegt werden, der das globale Instanzhand handle zurückgibt, das als Nebeneffekt der Initialisierung erstellt wurde. Dieses Instanzhand handle kann dann an jede andere API übergeben werden, die eine -Instanz verwendet. Wenn die Engine im Modus mit mehreren Instanzen ausgeführt wird, muss dieser Parameter auf einen gültigen Eingabepuffer festgelegt werden, der das Instanzhandl enthält, das von [JetCreateInstance](./jetcreateinstance-function.md) zurückgegeben wird, das initialisiert wird.

*Sz*

Der Ordner, in dem sich die Sicherung befindet. Die Sicherung sollte mithilfe der [JetBackup-APIs](./jetbackup-function.md) generiert worden sein.

*szDest*

Name des Ordners, in den die Datenbankdateien aus dem Sicherungssatz kopiert und wiederhergestellt werden. Wenn dies auf NULL festgelegt ist (was für den legacy [JetRestore](./jetrestore-function.md)der Fall ist), werden die Datenbankdateien kopiert und am ursprünglichen Speicherort wiederhergestellt.

*pfn*

Der optionale Zeiger auf die Funktion, die als Benachrichtigungsinformationen zum Fortschritt des Wiederherstellungsvorgang aufgerufen wird.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errAlreadyInitialized</p> | <p>Fehler beim Vorgang, da die Engine bereits für diese Instanz initialisiert wurde.</p> | 
| <p>JET_errInvalidLogSequence</p> | <p>Der Satz von Protokolldateien aus dem Sicherungssatz und aus dem aktuellen Protokollpfad ist nicht übereinstimmend.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Einer der bereitgestellten Parameter enthielt einen unerwarteten Wert oder einen Wert, der in Kombination mit dem Wert eines anderen Parameters nicht sinnvoll war. Dieser Fehler wird von <strong>JetRestoreInstance</strong> zurückgegeben, wenn sich die Engine im Modus mit mehreren Instanzen befindet und Pinstance auf eine ungültige Instanz Windows XP und späteren Releases verweist.</p> | 
| <p>JET_errInvalidPath</p> | <p>Fehler beim Vorgang, weil einige der bereitgestellten Pfade ungültig sind (Sicherungspfad, Zielpfad, Protokoll- oder Systempfad für die Instanz).</p> | 
| <p>JET_errPageSizeMismatch</p> | <p>Fehler beim Vorgang, da die Engine so konfiguriert ist, dass eine Datenbankseitengröße (mit <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> für <a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize)</a>verwendet wird, die nicht der Datenbankseitengröße entspricht, die zum Erstellen der Transaktionsprotokolldateien oder der den Transaktionsprotokolldateien zugeordneten Datenbanken verwendet wird.</p> | 
| <p>JET_errRunningInMultiInstanceMode</p> | <p>Fehler beim Vorgang, da die Parameter den Einzelinstanzmodus implizierten (Windows 2000-Kompatibilitätsmodus), und die Engine sich bereits im Modus mit mehreren Instanzen befindet.</p> | 



Bei Erfolg werden Datenbankdateien aus dem Sicherungssatz an ihrem Speicherort wiederhergestellt, und die Wiederherstellung wird so ausgeführt, dass sich die Datenbanken in einem sauberen Transaktionskonsistenzzustand befinden. Bei der Wiederherstellung werden die Protokolldateien aus dem Sicherungssatz und die Protokolldateien aus dem Protokollpfad wiedergegeben, sofern solche Dateien vorhanden sind. Diese Wiederherstellung führt zu Änderungen an der Prüfpunktdatei, den Transaktionsprotokolldateien und allen Datenbanken, auf die von diesen Transaktionsprotokolldateien verwiesen wird.

Bei einem Fehler verbleibt die Instanz in einem nicht initialisierten Zustand. Der Status der Transaktionsprotokolldateien und aller Datenbanken, auf die von diesen Transaktionsprotokolldateien verwiesen wird, wurde wahrscheinlich beim Versuch geändert, die Wiederherstellung zu initialisieren und die Datenbanken wiederherzustellen.

#### <a name="remarks"></a>Bemerkungen

Der Wiederherstellungsprozess rekonstruiert die Datenbanken, die während der Sicherung an die Instanz angefügt sind, und speichern die Änderungen in den Datenbankdateien. Das Ergebnis sind Datenbanken, die transaktions konsistent sind. Wenn möglich, werden auch die Seit der Sicherung vorgenommenen Änderungen in der Datenbank gespeichert, bis die letzte Änderung in den Transaktionsprotokollen gefunden wurde. Dies wäre möglich, wenn die seit der Sicherung generierten Transaktionsprotokolle weiterhin im Transaktionsprotokollverzeichnis vorhanden sind. Beachten Sie, dass die generierten Transaktionsprotokolle wiederverwendet werden, wenn die zirkuläre Protokollierung für die Instanz aktiviert wurde, damit die Wiederherstellung die Änderungen speichern kann, die bis zum Sicherungsmoment stattgefunden haben. In jedem Fall kann dieser Prozess einige Zeit dauern, wenn die Anzahl der Transaktionsprotokolldateien, die für die Datenbanken wiedergegeben werden, groß ist.

**JetRestoreInstance** muss für eine Instanz aufgerufen werden, die bereits mit [JetCreateInstance erstellt wurde.](./jetcreateinstance-function.md)

Da während der Wiederherstellung eine erhebliche Anzahl von Datenbankseiten und Transaktionsprotokollen verwendet wird, gibt es eine ganze Reihe von Fehlern, die von diesen Funktionen zurückgegeben werden können. Diese Fehler können von temporären Ressourcenzuordnungsfehlern wie Jet_errOutOfMemory bis zu Fehlern, die physische Beschädigungen wie JET_errReadVerifyFailure, JET_errLogFileCorrupt oder JET_errBadPageLink. Diese Fehler werden fast immer durch Hardwareprobleme verursacht und können daher nicht vermieden werden. Die Fehlverwaltung von Dateien wird sich am häufigsten als JET_errMissingLogFile oder JET_errAttachedDatabaseMismatch oder JET_errDatabaseSharingViolation oder JET_errInvalidLogSequence. Diese Fehler können von der Anwendung verhindert werden. Die Anwendung muss darauf achten, das Repository dieser Dateien vor manipulation durch externe Erzwingungen wie den Benutzer oder andere Anwendungen zu schützen. Wenn die Anwendung eine Instanz vollständig zerstören möchte, müssen alle der Instanz zugeordneten Dateien gelöscht werden. Dazu gehören die Prüfpunktdatei, die Transaktionsprotokolldateien und alle Datenbankdateien, die an die Instanz angefügt sind.

Für die verschiedenen Schritte der Wiederherstellung werden Ereignisprotokolleinträge generiert, einschließlich des Fortschritts der Transaktionsprotokollwiedergabe und des Endergebnis der Wiederherstellung.

#### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista oder Windows XP.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008 oder Windows Server 2003.</p> | 
| <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | 
| <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implementiert als <strong>JetRestoreInstanceW</strong> (Unicode) und <strong>JetRestoreInstanceA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetBackup](./jetbackup-function.md)  
[JetBackupInstance](./jetbackupinstance-function.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)
