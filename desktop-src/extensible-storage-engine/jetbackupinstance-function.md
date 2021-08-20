---
description: 'Weitere Informationen zu: JetBackupInstance-Funktion'
title: JetBackupInstance-Funktion
TOCTitle: JetBackupInstance Function
ms:assetid: 82486441-5037-440b-8632-038e953ad870
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269318(v=EXCHG.10)
ms:contentKeyID: 32765608
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBackupInstanceW
- JetBackupInstanceA
- JetBackupInstance
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5cf601593d970f56be80b75ef5744295e7b4cf0941a6c401d8bae78c15542f21
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119889720"
---
# <a name="jetbackupinstance-function"></a>JetBackupInstance-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetbackupinstance-function"></a>JetBackupInstance-Funktion

Die **JetBackupInstance-Funktion** führt eine Streamingsicherung einer Instanz einschließlich aller angefügten Datenbanken in einem Verzeichnis aus. Da die Engine mehrere Sicherungsmethoden unterstützt, ist dies die einfachste und am häufigsten gekapselte Funktion.

**Windows XP: JetBackupInstance** wird in Windows XP eingeführt.

```cpp
    JET_ERR JET_API JetBackupInstance(
      __in          JET_INSTANCE instance,
      __in          JET_PCSTR szBackupPath,
      __in          JET_GRBIT grbit,
      __in          JET_PFNSTATUS pfnStatus
    );
```

### <a name="parameters"></a>Parameter

*Instanz*

Die Instanz der zu sichernde Datenbank.

*szBackupPath*

Das Verzeichnis, in dem die Sicherung gespeichert wird. Wenn der Sicherungspfad NULL ist, um die Funktion zu verwenden, werden die Protokolle nach Möglichkeit abgeschnitten.

*grbit*

Eine Gruppe von Bits, die null oder mehr der folgenden Optionen angibt.

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
<td><p>Erstellt eine vollständige Sicherung der Datenbank. Dies ermöglicht die Beibehaltung einer vorhandenen Sicherung im gleichen Verzeichnis, wenn bei der neuen Sicherung ein Fehler auftritt.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitBackupIncremental</p></td>
<td><p>Erstellt eine inkrementelle Sicherung im Gegensatz zu einer vollständigen Sicherung. Dies bedeutet, dass nur die Protokolldateien gesichert werden, die seit der letzten vollständigen oder inkrementellen Sicherung erstellt wurden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitBackupSnapshot</p></td>
<td><p>Für die zukünftige Verwendung reserviert.</p></td>
</tr>
</tbody>
</table>


*pfnStatus*

Zeiger auf die [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) Rückruffunktion, die Benachrichtigungsinformationen zum Fortschritt des Sicherungsvorgangs bereitstellt.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).

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
<td><p>Für dieselbe Instanz wird bereits eine Sicherung ausgeführt. Mehrere Sicherungen sind nicht gleichzeitig zulässig.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBackupNotAllowedYet</p></td>
<td><p>Die Instanz ist noch nicht für die Sicherung bereit, da sie initialisiert wird.</p></td>
</tr>
<tr class="even">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da alle Aktivitäten in der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufs von <a href="gg294108(v=exchg.10).md">JetStopServiceInstance</a>beendet wurden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da für die der Sitzung zugeordnete Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen.</p>
<p><strong>Windows XP:</strong> Dieser Rückgabewert wird in Windows XP eingeführt.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidBackup</p></td>
<td><p>Eine inkrementelle Sicherung ist nicht zulässig, wenn die zirkuläre Protokollierung eingeschaltet ist.</p></td>
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
<td><p>In einer Protokolldatei ist ein Prüfsummenüberprüfungsfehler aufgetreten.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogWriteFail</p></td>
<td><p>Die Protokollierung für die Instanz ist aufgrund eines unerwarteten Fehlers temporär oder dauerhaft deaktiviert.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz noch nicht initialisiert wurde.</p></td>
</tr>
<tr class="even">
<td><p>JET_errReadVerifyFailure</p></td>
<td><p>Auf einer Datenbankseite ist ein Prüfsummenüberprüfungsfehler aufgetreten.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da ein Wiederherstellungsvorgang für die Instanz ausgeführt wird, die der Sitzung zugeordnet ist.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Dieselbe Sitzung kann nicht für mehrere Threads gleichzeitig verwendet werden.</p>
<p><strong>Windows XP:</strong> Dieser Rückgabewert wird in Windows XP eingeführt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz heruntergefahren wird.</p></td>
</tr>
</tbody>
</table>


Nachdem die Funktion erfolgreich zurückgegeben wurde, sind im Sicherungsverzeichnis alle Dateien vorhanden, die für eine Wiederherstellung bis zum Zeitpunkt der Sicherung erforderlich sind. Wenn es sich um eine vollständige Sicherung handelt, handelt es sich bei den Dateien um die Datenbankdateien und die Protokolldateien, die benötigt werden, um die Datenbank in einen konsistenten Zustand zu bringen. Wenn es sich um eine inkrementelle Sicherung handelt, werden den Verzeichnissen nur Protokolldateien hinzugefügt, aber die bereits vorhandenen Dateien (Datenbanken und Protokolldateien) zusammen mit den neuen Protokolldateien können wiederhergestellt werden und die Datenbank zum Zeitpunkt der Sicherung wieder in den Zustand versetzt werden.

Als Nebeneffekt der Sicherung werden die Protokolldateien abgeschnitten, die nicht mehr benötigt werden.

Gleichzeitig werden die Datenbankheader mit den Informationen aktualisiert, als die letzte Sicherung durchgeführt wurde.

Bei einem Fehler sind keine Dateien im Sicherungsverzeichnisziel vorhanden, sodass keine Wiederherstellung möglich ist. Gleichzeitig werden die aktuellen Protokolldateien nicht abgeschnitten.

#### <a name="remarks"></a>Hinweise

Für die verschiedenen Schritte der Sicherung werden Ereignisprotokolleinträge generiert, einschließlich der Dateinamen, der Protokollkürzung und des Endergebnisses der Sicherung.

Inkrementelle Sicherungen sind erst möglich, nachdem eine vollständige Sicherung erstellt wurde. Inkrementelle Sicherungen sind auch nur möglich, wenn die zirkuläre Protokollierung deaktiviert ist. Es wird empfohlen, dass das Sicherungsverzeichnis keine anderen Dateien als die dateien enthält, die an der Sicherung beteiligt sind oder von einer vorherigen erfolgreichen Sicherung hinzugefügt wurden.

Das Sicherungsverzeichnis sollte vorhanden sein, es sei denn, der Parameter *JET_paramCreatePathIfNotExist* ist für die Instanz festgelegt. Weitere Informationen finden Sie unter [Systemparameter.](./extensible-storage-engine-system-parameters.md)

Die Sicherung führt die Prüfsummenüberprüfung auf allen verwendeten Datenbankseiten und ab Windows Server 2003 auch in den Protokolldateien durch. Dies bietet die Möglichkeit, die Integrität der Datenbank auch für Seiten zu schätzen, die während des normalen Betriebs nicht gelesen werden. Wenn eine solche Beschädigung auftritt, schlägt die Sicherung fehl.

Während der Sicherung wird die aktuelle Protokolldatei abgeschlossen, und wir starten eine neue Protokollgenerierung. Dies ermöglicht das Kopieren der erforderlichen Protokolldateien, da die letzte benötigte Protokolldatei nicht mehr verwendet wird.

Es wird dringend empfohlen, die Sicherung nicht für andere Zwecke als die Sicherung zu verwenden und auf Engine-Ebene wiederherzustellen. Dadurch wird die Änderung beim Abrufen von Fehlern während der Sicherungs- und Wiederherstellungsvorgänge minimiert.

#### <a name="requirements"></a>Anforderungen

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Erfordert Windows Vista oder Windows XP.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Erfordert Windows Server 2008 oder Windows Server 2003.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Deklariert in Esent.h.</p></td>
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
<td><p>Implementiert als <strong>JetBackupInstanceW</strong> (Unicode) und <strong>JetBackupInstanceA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_PFNSTATUS](./jet-pfnstatus-callback-function.md)  
[JetRestore](./jetrestore-function.md)  
[JetRestore2](./jetrestore2-function.md)  
[JetRestoreInstance](./jetrestoreinstance-function.md)  
[JetStopServiceInstance](./jetstopserviceinstance-function.md)  
[Systemparameter](./extensible-storage-engine-system-parameters.md)
