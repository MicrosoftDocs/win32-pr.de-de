---
description: 'Weitere Informationen zu: JetRestore-Funktion'
title: JetRestore-Funktion
TOCTitle: JetRestore Function
ms:assetid: cdfb8823-6260-46f2-adfc-77e2512a68fd
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294093(v=EXCHG.10)
ms:contentKeyID: 32765708
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRestore
- JetRestoreW
- JetRestoreA
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 22aef03477e0a489b27a544255f6583fbe2a60b9
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466235"
---
# <a name="jetrestore-function"></a>JetRestore-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetrestore-function"></a>JetRestore-Funktion

Die **JetRestore-Funktion** stellt eine Streamingsicherung einer Instanz einschließlich aller angefügten Datenbanken wieder her und stellt sie wieder her. Diese Funktion dient in erster Linie der Abwärtskompatibilität mit Windows 2000 und früheren Datenbank-Engines, bei denen nur eine Instanz einer Datenbank zulässig ist. In diesem Fall ist die aktive Instanz die Instanz, die wiederhergestellt wird. Mit **JetRestore** kann der Speicherort für die wiederhergestellten Datenbanken nicht angegeben werden.

```cpp
JET_ERR JET_API JetRestore(
  __in          JET_PCSTR sz,
  __in          JET_PFNSTATUS pfn
);
```

### <a name="parameters"></a>Parameter

*Sz*

Der Ordner, in dem sich die Sicherung befindet. Die Sicherung sollte mithilfe der [JetBackup-Funktion](./jetbackup-function.md) generiert worden sein.

*pfn*

Der optionale Zeiger auf die Funktion, die als Benachrichtigungsinformationen zum Fortschritt des Wiederherstellungsvorgangs aufgerufen wird.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errAlreadyInitialized</p> | <p>Fehler beim Vorgang, weil die Engine bereits für diese Instanz initialisiert wurde.</p> | 
| <p>JET_errInvalidLogSequence</p> | <p>Die Protokolldateien aus dem Sicherungssatz und dem aktuellen Protokollpfad stimmen nicht überein.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Einer der bereitgestellten Parameter enthielt einen unerwarteten Wert oder einen Wert, der in Kombination mit dem Wert eines anderen Parameters nicht sinnvoll war.</p> | 
| <p>JET_errInvalidPath</p> | <p>Der Vorgang ist fehlgeschlagen, weil einige der bereitgestellten Pfade ungültig sind (der Sicherungspfad, der Zielpfad, der Protokoll- oder Systempfad für die Instanz).</p> | 
| <p>JET_errPageSizeMismatch</p> | <p>Fehler beim Vorgang, weil die Engine für die Verwendung einer Datenbankseitengröße konfiguriert ist (mit <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> für <a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>), die nicht mit der Datenbankseitengröße übereinstimmt, die zum Erstellen der Transaktionsprotokolldateien oder der Datenbanken verwendet wird, die den Transaktionsprotokolldateien zugeordnet sind.</p> | 
| <p>JET_errRunningInMultiInstanceMode</p> | <p>Fehler beim Vorgang, weil die Parameter den Einzelinstanzmodus implizierten (Windows Kompatibilitätsmodus 2000), und die Engine sich bereits im Modus mit mehreren Instanzen befindet.</p> | 



Bei Erfolg werden Datenbankdateien aus dem Sicherungssatz an ihrem Speicherort wiederhergestellt, und die Wiederherstellung wird so ausgeführt, dass sich die Datenbanken in einem bereinigten Transaktionskonsistenzzustand befinden. Bei der Wiederherstellung werden die Protokolldateien aus dem Sicherungssatz und die Protokolldateien aus dem Protokollpfad wiedergegeben, sofern diese Dateien vorhanden sind. Diese Wiederherstellung führt zu Änderungen an der Prüfpunktdatei, den Transaktionsprotokolldateien und allen Datenbanken, auf die von diesen Transaktionsprotokolldateien verwiesen wird.

Bei einem Fehler verbleibt die Instanz in einem nicht initialisierten Zustand. Der Status der Transaktionsprotokolldateien und aller Datenbanken, auf die von diesen Transaktionsprotokolldateien verwiesen wird, wurde wahrscheinlich geändert, wenn versucht wird, die Wiederherstellung und Wiederherstellung der Datenbanken zu initialisieren.

#### <a name="remarks"></a>Hinweise

Der Wiederherstellungsprozess rekonstruiert die Datenbanken, die während der Sicherung an die Instanz angefügt wurden, und speichert die Änderungen wieder in den Datenbankdateien. Das Ergebnis sind Datenbanken, die transaktionskonsynt sind. Nach Möglichkeit werden auch die Änderungen, die seit der Sicherung vorgenommen wurden, bis zur letzten Änderung in den Transaktionsprotokollen in der Datenbank gespeichert. Dies ist möglich, wenn die seit der Sicherung generierten Transaktionsprotokolle weiterhin im Transaktionsprotokollverzeichnis vorhanden sind. Beachten Sie, dass die generierten Transaktionsprotokolle wiederverwendet werden, wenn die zirkuläre Protokollierung für die Instanz aktiviert wurde, sodass die Wiederherstellung die Änderungen speichern kann, die bis zum Zeitpunkt der Sicherung vorgenommen wurden. In jedem Fall kann dieser Vorgang einige Zeit in Anspruch nehmen, wenn die Anzahl der Transaktionsprotokolldateien, die für die Datenbanken wiedergegeben werden sollen, groß ist.

**JetRestore-Funktionen** müssen für eine Instanz aufgerufen werden, bevor [JetInit](./jetinit-function.md) für diese Instanz aufgerufen wird.

Da während der Wiederherstellung eine erhebliche Anzahl von Datenbankseiten und Transaktionsprotokollen verwendet wird, gibt es eine ganze Reihe von Fehlern, die von diesen Funktionen zurückgegeben werden können. Solche Fehler können von temporären Ressourcenzuordnungsfehlern wie Jet_errOutOfMemory zu Fehlern führen, die physische Beschädigungen wie JET_errReadVerifyFailure, JET_errLogFileCorrupt oder JET_errBadPageLink darstellen. Diese Fehler werden fast immer durch Hardwareprobleme verursacht und können daher nicht vermieden werden. Dateifehler treten am häufigsten als JET_errMissingLogFile, JET_errAttachedDatabaseMismatch oder JET_errDatabaseSharingViolation oder JET_errInvalidLogSequence auf. Diese Fehler können von der Anwendung verhindert werden. Die Anwendung muss darauf achten, das Repository dieser Dateien vor manipulation durch externe Zwingen wie den Benutzer oder andere Anwendungen zu schützen. Wenn die Anwendung eine Instanz vollständig zerstören möchte, müssen alle der Instanz zugeordneten Dateien gelöscht werden. Dazu gehören die Prüfpunktdatei, die Transaktionsprotokolldateien und alle Datenbankdateien, die an die Instanz angefügt sind.

Für die verschiedenen Schritte der Wiederherstellung werden Ereignisprotokolleinträge generiert, einschließlich des Fortschritts der Transaktionsprotokollwiedergabe und des Endergebnisses der Wiederherstellung.

#### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | | <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Implementiert als <strong>JetRestoreW</strong> (Unicode) und <strong>JetRestoreA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetBackup](./jetbackup-function.md)  
[JetBackupInstance](./jetbackupinstance-function.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)
