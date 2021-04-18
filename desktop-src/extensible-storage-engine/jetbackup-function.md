---
description: 'Weitere Informationen zu: JetBackup-Funktion'
title: JetBackup-Funktion
TOCTitle: JetBackup Function
ms:assetid: afff995f-378a-4e67-b522-d5eafcbad57e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294058(v=EXCHG.10)
ms:contentKeyID: 32765673
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBackupA
- JetBackup
- JetBackupW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f225053df36ebe98bc890a8e036d84ee31b6b154
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351134"
---
# <a name="jetbackup-function"></a>JetBackup-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetbackup-function"></a>JetBackup-Funktion

Die **JetBackup** -Funktion erstellt eine Sicherung der Datenbank, während die Datenbank online ist. Bei dieser Funktion handelt es sich hauptsächlich um Abwärtskompatibilität mit Windows 2000 und früheren Datenbank-Engines, bei denen nur eine Instanz einer Datenbank zulässig ist. In diesem Fall ist die aktive Instanz die Instanz, die gesichert wird.

```cpp
    JET_ERR JET_API JetBackup(
      __in          JET_PCSTR szBackupPath,
      __in          JET_GRBIT grbit,
      __in          JET_PFNSTATUS pfnStatus
    );
```

### <a name="parameters"></a>Parameter

*szbackuppath*

Das Verzeichnis, in dem die Sicherung gespeichert ist. Wenn der Sicherungs Pfad NULL ist, schneidet die Funktion die Protokolle nach Möglichkeit ab.

*grbit*

Eine Gruppe von Bits, die NULL oder mehr der folgenden Optionen angibt.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Wert</p></th>
<th><p>Bedeutung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitBackupAtomic</p></td>
<td><p>Erstellt eine vollständige Sicherung der Datenbank. Dies ermöglicht die Beibehaltung einer vorhandenen Sicherung im gleichen Verzeichnis, wenn die neue Sicherung nicht ausgeführt werden kann.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitBackupIncremental</p></td>
<td><p>Erstellt im Gegensatz zu einer vollständigen Sicherung eine inkrementelle Sicherung. Dies bedeutet, dass nur die Protokolldateien seit der letzten vollständigen oder inkrementellen Sicherung gesichert werden.</p></td>
</tr>
</tbody>
</table>


*pfnstatus*

Ein Zeiger auf die [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) Callback-Funktion, die Benachrichtigungs Informationen zum Fortschritt des Sicherungs Vorgangs bereitstellt.

### <a name="return-value"></a>Rückgabewert

Die-Funktion gibt einen der [JET_ERR](./jet-err.md) Fehlercodes zurück. Im folgenden finden Sie die am häufigsten zurückgegebenen. (Eine komplette Liste der Fehler für diese API finden Sie unter [Extensible Storage Engine Error Codes](./extensible-storage-engine-error-codes.md).)

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
<td><p>JET_errBackupInProgress</p></td>
<td><p>Für dieselbe Instanz wird bereits eine Sicherung ausgeführt. Mehrere Sicherungen sind gleichzeitig nicht zulässig.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBackupNotAllowedYet</p></td>
<td><p>Die Instanz ist noch nicht für die Sicherung bereit, während Sie initialisiert wird.</p></td>
</tr>
<tr class="even">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da der der Sitzung zugeordnete-Instanz einen schwerwiegenden Fehler festgestellt hat, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</p>
<p><strong>Windows XP:  </strong> Dieser Rückgabewert wird in Windows XP eingeführt.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidBackup</p></td>
<td><p>Eine inkrementelle Sicherung ist nicht zulässig, wenn die zirkuläre Protokollierung on</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidGrbit</p></td>
<td><p>Die angegebenen Optionen sind ungültig.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Ein ungültiger Parameter wurde an die API übergeben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidPath</p></td>
<td><p>Der Zielpfad ist nicht vorhanden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLoggingDisabled</p></td>
<td><p>Die Instanz wird ohne Protokollierung ausgeführt. Es ist keine Sicherung zulässig.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLogReadVerifyFailure</p></td>
<td><p>Bei einer Protokolldatei ist ein Prüfsummen Überprüfungs Fehler aufgetreten.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogWriteFail</p></td>
<td><p>Die Protokollierung für die Instanz ist aufgrund eines unerwarteten Fehlers temporär oder dauerhaft deaktiviert.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</p></td>
</tr>
<tr class="even">
<td><p>JET_errReadVerifyFailure</p></td>
<td><p>Auf einer Datenbankseite ist ein Prüfsummen Überprüfungs Fehler aufgetreten.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Dieselbe Sitzung kann nicht für mehr als einen Thread gleichzeitig verwendet werden.</p>
<p><strong>Windows XP:  </strong> Dieser Rückgabewert wird in Windows XP eingeführt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</p></td>
</tr>
</tbody>
</table>


Wenn die Funktion erfolgreich ausgeführt wird, sind alle Dateien, die für eine Wiederherstellung bis zum Zeitpunkt der Sicherung benötigt werden, im Sicherungs Verzeichnis enthalten. Wenn es sich um eine vollständige Sicherung handelt, sind die Dateien die Datenbankdateien und die Protokolldateien, die erforderlich sind, um die Datenbank in einen konsistenten Zustand zu bringen. Wenn es sich um eine inkrementelle Sicherung handelt, werden den Verzeichnissen nur Protokolldateien hinzugefügt, aber die bereits vorhandenen Dateien (Datenbanken und Protokolldateien) können zusammen mit den neuen Protokolldateien wieder hergestellt werden, um die Datenbank wieder in den Zustand zu bringen, in dem Sie sich zum Zeitpunkt der Sicherung befand.

Als Nebeneffekt der Sicherung werden die Protokolldateien, die nicht mehr benötigt werden, abgeschnitten.

Gleichzeitig werden die Daten Bank Header mit den Informationen aktualisiert, wann die letzte Sicherung erfolgte.

Wenn die Funktion fehlschlägt, sind keine Dateien im Sicherungs Verzeichnis vorhanden, sodass keine Wiederherstellung möglich ist. Gleichzeitig werden die aktuellen Protokolldateien nicht abgeschnitten.

#### <a name="remarks"></a>Bemerkungen

In den verschiedenen Schritten der Sicherung werden Ereignisprotokoll Einträge generiert, einschließlich der Dateinamen, der Protokoll Verkürzung und des Endergebnisses der Sicherung.

Inkrementelle Sicherungen können erst nach dem Erstellen einer vollständigen Sicherung durchgeführt werden. Außerdem sind inkrementelle Sicherungen nur möglich, wenn die zirkuläre Protokollierung deaktiviert ist. Es wird empfohlen, dass das Sicherungs Verzeichnis keine Dateien enthält, die nicht in der Sicherung verwendet wurden oder von einer vorherigen erfolgreichen Sicherung hinzugefügt wurden.

Das Sicherungs Verzeichnis sollte vorhanden sein, es sei denn, der Parameter *JET_paramCreatePathIfNotExist* für die Instanz festgelegt. Weitere Informationen finden Sie unter [System Parameter](./extensible-storage-engine-system-parameters.md).

Die Sicherung führt eine Prüfsummen Überprüfung auf allen verwendeten Datenbankseiten und ab Windows Server 2003 in den Protokolldateien aus. Dadurch haben Sie die Möglichkeit, die Integrität der Datenbank zu schätzen, auch für Seiten, die während des normalen Betriebs nicht gelesen werden. Wenn eine solche Beschädigung aufgetreten ist, tritt bei der Sicherung ein Fehler auf.

Während der Sicherung wird die aktuelle Protokolldatei fertiggestellt, und es wird ein neues Protokoll generiert. Auf diese Weise können alle erforderlichen Protokolldateien kopiert werden, da das aktuelle Protokoll nicht mehr verwendet wird.

Es wird dringend empfohlen, die Sicherung nicht für andere Zwecke als die Sicherung und Wiederherstellung auf Engine-Ebene zu verwenden. Dadurch wird die Wahrscheinlichkeit minimiert, dass während der Sicherungs-und Wiederherstellungs Vorgänge Fehler auftreten.

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
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implementiert als <strong>jetbackupw</strong> (Unicode) und <strong>jetbackupa</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Weitere Informationen

[Extensible Storage Engine-Dateien](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_PFNSTATUS](./jet-pfnstatus-callback-function.md)  
[Jetrestore](./jetrestore-function.md)  
[JetRestore2](./jetrestore2-function.md)  
[Jetrestoreingestance](./jetrestoreinstance-function.md)  
[Jetstopservice](./jetstopservice-function.md)  
[System Parameter](./extensible-storage-engine-system-parameters.md)
