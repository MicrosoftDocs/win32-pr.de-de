---
description: 'Weitere Informationen zu: JetRestore2-Funktion'
title: JetRestore2-Funktion
TOCTitle: JetRestore2 Function
ms:assetid: 7f7fc2e3-727a-43e4-8497-64ff56d92b9f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269313(v=EXCHG.10)
ms:contentKeyID: 32765603
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRestore2
- JetRestore2A
- JetRestore2W
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 464fbc228acc1d73b50253b2312edd3889289e2d
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987253"
---
# <a name="jetrestore2-function"></a>JetRestore2-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetrestore2-function"></a>JetRestore2-Funktion

**JetRestore2** stellt eine Streamingsicherung einer Instanz einschließlich aller angefügten Datenbanken wieder her und stellt sie wieder her. Diese Funktion dient in erster Linie der Abwärtskompatibilität mit Windows 2000 und früheren Datenbank-Engines, bei denen nur eine Instanz einer Datenbank zulässig ist. In diesem Fall ist die aktive Instanz die Instanz, die wiederhergestellt wird.

```cpp
    JET_ERR JET_API JetRestore2(
      __in          JET_PCSTR sz,
      __in_opt      JET_PCSTR szDest,
      __in          JET_PFNSTATUS pfn
    );
```

### <a name="parameters"></a>Parameter

*Sz*

Der Ordner, in dem sich die Sicherung befindet. Die Sicherung sollte mithilfe der [JetBackup-APIs](./jetbackup-function.md) generiert worden sein.

*szDest*

Name des Ordners, in den die Datenbankdateien aus dem Sicherungssatz kopiert und wiederhergestellt werden. Wenn dieser Wert auf NULL festgelegt ist (was bei der älteren [JetRestore-Version](./jetrestore-function.md)der Fall ist), werden die Datenbankdateien kopiert und an ihrem ursprünglichen Speicherort wiederhergestellt.

*pfn*

Der optionale Zeiger auf die Funktion, die als Benachrichtigungsinformationen zum Fortschritt des Wiederherstellungsvorgangs aufgerufen wird.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errAlreadyInitialized</p> | <p>Fehler beim Vorgang, weil die Engine bereits für diese Instanz initialisiert wurde.</p> | 
| <p>JET_errInvalidLogSequence</p> | <p>Die Protokolldateien aus dem Sicherungssatz und dem aktuellen Protokollpfad stimmen nicht überein.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Einer der bereitgestellten Parameter enthielt einen unerwarteten Wert oder einen Wert, der in Kombination mit dem Wert eines anderen Parameters nicht sinnvoll war. Dieser Fehler wird von <a href="gg269306(v=exchg.10).md">JetRestoreInstance</a> zurückgegeben, wenn sich die Engine im Modus mit mehreren Instanzen befindet und pinstance auf eine ungültige Instanz Windows XP und höher verweist.</p> | 
| <p>JET_errInvalidPath</p> | <p>Der Vorgang ist fehlgeschlagen, weil einige der bereitgestellten Pfade ungültig sind (der Sicherungspfad, der Zielpfad, der Protokoll- oder Systempfad für die Instanz).</p> | 
| <p>JET_errPageSizeMismatch</p> | <p>Fehler beim Vorgang, weil die Engine für die Verwendung einer Datenbankseitengröße (mit <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> für <a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize)</a>konfiguriert ist, die nicht mit der Datenbankseitengröße übereinstimmt, die zum Erstellen der Transaktionsprotokolldateien oder der Datenbanken verwendet wird, die den Transaktionsprotokolldateien zugeordnet sind.</p> | 
| <p>JET_errRunningInMultiInstanceMode</p> | <p>Der Vorgang ist fehlgeschlagen, weil die Parameter den Einzelinstanzmodus (Windows 2000-Kompatibilitätsmodus) impliziert haben und sich die Engine bereits im Modus mit mehreren Instanzen befindet.</p> | 



Bei Erfolg werden Datenbankdateien aus dem Sicherungssatz an ihrem Speicherort wiederhergestellt, und die Wiederherstellung wird so ausgeführt, dass sich die Datenbanken in einem bereinigten Transaktionskonsistenzzustand befinden. Bei der Wiederherstellung werden die Protokolldateien aus dem Sicherungssatz und die Protokolldateien aus dem Protokollpfad wiedergegeben, sofern diese Dateien vorhanden sind. Diese Wiederherstellung führt zu Änderungen an der Prüfpunktdatei, den Transaktionsprotokolldateien und allen Datenbanken, auf die von diesen Transaktionsprotokolldateien verwiesen wird.

Bei einem Fehler verbleibt die Instanz in einem nicht initialisierten Zustand. Der Status der Transaktionsprotokolldateien und aller Datenbanken, auf die von diesen Transaktionsprotokolldateien verwiesen wird, wurde wahrscheinlich geändert, wenn versucht wird, die Wiederherstellung und Wiederherstellung der Datenbanken zu initialisieren.

#### <a name="remarks"></a>Bemerkungen

Der Wiederherstellungsprozess rekonstruiert die Datenbanken, die während der Sicherung an die Instanz angefügt wurden, und speichert die Änderungen wieder in den Datenbankdateien. Das Ergebnis sind Datenbanken, die transaktionskonsynt sind. Nach Möglichkeit werden auch die Änderungen, die seit der Sicherung vorgenommen wurden, bis zur letzten Änderung in den Transaktionsprotokollen in der Datenbank gespeichert. Dies wäre möglich, wenn die seit der Sicherung generierten Transaktionsprotokolle weiterhin im Transaktionsprotokollverzeichnis vorhanden sind. Beachten Sie, dass die generierten Transaktionsprotokolle wiederverwendet werden, wenn die zirkuläre Protokollierung für die Instanz aktiviert wurde, sodass die Wiederherstellung die Änderungen speichern kann, die bis zum Zeitpunkt der Sicherung vorgenommen wurden. In jedem Fall kann dieser Vorgang einige Zeit in Anspruch nehmen, wenn die Anzahl der Transaktionsprotokolldateien, die für die Datenbanken wiedergegeben werden sollen, groß ist.

[JetRestore-Funktionen](./jetrestore-function.md) müssen für eine Instanz aufgerufen werden, bevor [JetInit](./jetinit-function.md) für diese Instanz aufgerufen wird.

Da während der Wiederherstellung eine erhebliche Anzahl von Datenbankseiten und Transaktionsprotokollen verwendet wird, gibt es eine ganze Reihe von Fehlern, die von diesen Funktionen zurückgegeben werden können. Solche Fehler können von temporären Ressourcenzuordnungsfehlern wie Jet_errOutOfMemory zu Fehlern führen, die physische Beschädigungen wie JET_errReadVerifyFailure, JET_errLogFileCorrupt oder JET_errBadPageLink darstellen. Diese Fehler werden fast immer durch Hardwareprobleme verursacht und können daher nicht vermieden werden. Dateifehler treten am häufigsten als JET_errMissingLogFile oder JET_errAttachedDatabaseMismatch oder JET_errDatabaseSharingViolation oder JET_errInvalidLogSequence auf. Diese Fehler können von der Anwendung verhindert werden. Die Anwendung muss darauf achten, das Repository dieser Dateien vor manipulation durch externe Zwingen wie den Benutzer oder andere Anwendungen zu schützen. Wenn die Anwendung eine Instanz vollständig zerstören möchte, müssen alle der Instanz zugeordneten Dateien gelöscht werden. Dazu gehören die Prüfpunktdatei, die Transaktionsprotokolldateien und alle Datenbankdateien, die an die Instanz angefügt sind.

Für die verschiedenen Schritte der Wiederherstellung werden Ereignisprotokolleinträge generiert, einschließlich des Fortschritts der Transaktionsprotokollwiedergabe und des Endergebnisses der Wiederherstellung.

#### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | 
| <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implementiert als <strong>JetRestore2W</strong> (Unicode) und <strong>JetRestore2A</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetBackup](./jetbackup-function.md)  
[JetBackupInstance](./jetbackupinstance-function.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JetRestore](./jetrestore-function.md)  
[JetRestoreInstance](./jetrestoreinstance-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)
