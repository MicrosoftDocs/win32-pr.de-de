---
description: Weitere Informationen finden Sie unter JetRestore2-Funktion.
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
ms.openlocfilehash: 38b669fdf38d6dcaffe5d8a0ac77c8ac362142faca2df03fb23eb45d869ed0ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117704044"
---
# <a name="jetrestore2-function"></a>JetRestore2-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetrestore2-function"></a>JetRestore2-Funktion

**JetRestore2 stellt** eine Streamingsicherung einer Instanz wieder her, einschließlich aller angefügten Datenbanken. Diese Funktion dient in erster Linie der Abwärtskompatibilität mit Windows 2000 und früheren Datenbank-Engines, bei denen nur eine Instanz einer Datenbank zulässig ist. In diesem Fall ist die aktive Instanz die Instanz, die wiederhergestellt wird.

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

Name des Ordners, in den die Datenbankdateien aus dem Sicherungssatz kopiert und wiederhergestellt werden. Wenn dies auf NULL festgelegt ist (was für den legacy [JetRestore](./jetrestore-function.md)der Fall ist), werden die Datenbankdateien kopiert und am ursprünglichen Speicherort wiederhergestellt.

*pfn*

Der optionale Zeiger auf die Funktion, die als Benachrichtigungsinformationen zum Fortschritt des Wiederherstellungsvorgang aufgerufen wird.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR-Datentyp](./jet-err.md) mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Rückgabecode</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>Der Vorgang wurde erfolgreich abgeschlossen.</p></td>
</tr>
<tr class="even">
<td><p>JET_errAlreadyInitialized</p></td>
<td><p>Fehler beim Vorgang, da die Engine bereits für diese Instanz initialisiert wurde.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidLogSequence</p></td>
<td><p>Der Satz von Protokolldateien aus dem Sicherungssatz und aus dem aktuellen Protokollpfad ist nicht übereinstimmend.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Einer der bereitgestellten Parameter enthielt einen unerwarteten Wert oder einen Wert, der in Kombination mit dem Wert eines anderen Parameters nicht sinnvoll war. Dieser Fehler wird von <a href="gg269306(v=exchg.10).md">JetRestoreInstance</a> zurückgegeben, wenn sich die Engine im Modus mit mehreren Instanzen befindet und Pinstance auf eine ungültige Instanz Windows XP und späteren Releases verweist.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidPath</p></td>
<td><p>Fehler beim Vorgang, weil einige der bereitgestellten Pfade ungültig sind (Sicherungspfad, Zielpfad, Protokoll- oder Systempfad für die Instanz).</p></td>
</tr>
<tr class="even">
<td><p>JET_errPageSizeMismatch</p></td>
<td><p>Fehler beim Vorgang, da die Engine so konfiguriert ist, dass eine Datenbankseitengröße (mit <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> für <a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>) verwendet wird, die nicht der Datenbankseitengröße entspricht, die zum Erstellen der Transaktionsprotokolldateien oder der den Transaktionsprotokolldateien zugeordneten Datenbanken verwendet wird.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRunningInMultiInstanceMode</p></td>
<td><p>Fehler beim Vorgang, da die Parameter den Einzelinstanzmodus implizierten (Windows 2000-Kompatibilitätsmodus), und die Engine sich bereits im Modus mit mehreren Instanzen befindet.</p></td>
</tr>
</tbody>
</table>


Bei Erfolg werden Datenbankdateien aus dem Sicherungssatz an ihrem Speicherort wiederhergestellt, und die Wiederherstellung wird so ausgeführt, dass sich die Datenbanken in einem sauberen Transaktionskonsistenzzustand befinden. Bei der Wiederherstellung werden die Protokolldateien aus dem Sicherungssatz und die Protokolldateien aus dem Protokollpfad wiedergegeben, sofern solche Dateien vorhanden sind. Diese Wiederherstellung führt zu Änderungen an der Prüfpunktdatei, den Transaktionsprotokolldateien und allen Datenbanken, auf die von diesen Transaktionsprotokolldateien verwiesen wird.

Bei einem Fehler verbleibt die Instanz in einem nicht initialisierten Zustand. Der Status der Transaktionsprotokolldateien und aller Datenbanken, auf die von diesen Transaktionsprotokolldateien verwiesen wird, wurde wahrscheinlich beim Versuch geändert, die Wiederherstellung zu initialisieren und die Datenbanken wiederherzustellen.

#### <a name="remarks"></a>Hinweise

Der Wiederherstellungsprozess rekonstruiert die Datenbanken, die während der Sicherung an die Instanz angefügt sind, und speichern die Änderungen in den Datenbankdateien. Das Ergebnis sind Datenbanken, die transaktions konsistent sind. Wenn möglich, werden auch die Seit der Sicherung vorgenommenen Änderungen in der Datenbank gespeichert, bis die letzte Änderung in den Transaktionsprotokollen gefunden wurde. Dies wäre möglich, wenn die seit der Sicherung generierten Transaktionsprotokolle weiterhin im Transaktionsprotokollverzeichnis vorhanden sind. Beachten Sie, dass die generierten Transaktionsprotokolle wiederverwendet werden, wenn die zirkuläre Protokollierung für die Instanz aktiviert wurde, damit die Wiederherstellung die Änderungen speichern kann, die bis zum Sicherungsmoment stattgefunden haben. In jedem Fall kann dieser Prozess einige Zeit dauern, wenn die Anzahl der Transaktionsprotokolldateien, die für die Datenbanken wiedergegeben werden, groß ist.

[JetRestore-Funktionen](./jetrestore-function.md) müssen für eine Instanz aufgerufen werden, bevor [JetInit](./jetinit-function.md) für diese Instanz aufgerufen wird.

Da während der Wiederherstellung eine erhebliche Anzahl von Datenbankseiten und Transaktionsprotokollen verwendet wird, gibt es eine ganze Reihe von Fehlern, die von diesen Funktionen zurückgegeben werden können. Diese Fehler können von temporären Ressourcenzuordnungsfehlern wie Jet_errOutOfMemory bis zu Fehlern bei physischen Beschädigungen wie JET_errReadVerifyFailure, JET_errLogFileCorrupt oder JET_errBadPageLink. Diese Fehler werden fast immer durch Hardwareprobleme verursacht und können daher nicht vermieden werden. Die Fehlverwaltung von Dateien wird sich am häufigsten als JET_errMissingLogFile oder JET_errAttachedDatabaseMismatch oder JET_errDatabaseSharingViolation oder JET_errInvalidLogSequence. Diese Fehler können von der Anwendung verhindert werden. Die Anwendung muss darauf achten, das Repository dieser Dateien vor manipulation durch externe Erzwingungen wie den Benutzer oder andere Anwendungen zu schützen. Wenn die Anwendung eine Instanz vollständig zerstören möchte, müssen alle der Instanz zugeordneten Dateien gelöscht werden. Dazu gehören die Prüfpunktdatei, die Transaktionsprotokolldateien und alle Datenbankdateien, die an die Instanz angefügt sind.

Für die verschiedenen Schritte der Wiederherstellung werden Ereignisprotokolleinträge generiert, einschließlich des Fortschritts der Transaktionsprotokollwiedergabe und des Endergebnis der Wiederherstellung.

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
<td><p>Wird in Esent.h deklariert.</p></td>
</tr>
<tr class="even">
<td><p><strong>Bibliothek</strong></p></td>
<td><p>Verwenden Sie ESENT.lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Dll</strong></p></td>
<td><p>Erfordert ESENT.dll.</p></td>
</tr>
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implementiert als <strong>JetRestore2W</strong> (Unicode) und <strong>JetRestore2A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


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
