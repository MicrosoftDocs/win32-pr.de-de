---
description: Weitere Informationen finden Sie in der jetbackupinstance-Funktion.
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
ms.openlocfilehash: fab20676267333ae8f60e4fe4f07d98a8b45e88d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128176"
---
# <a name="jetbackupinstance-function"></a>JetBackupInstance-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetbackupinstance-function"></a>JetBackupInstance-Funktion

Die **jetbackupinstance** -Funktion führt eine Streamingsicherung einer Instanz, einschließlich aller angefügten Datenbanken, in ein Verzeichnis aus. Mit mehreren Sicherungsmethoden, die von der-Engine unterstützt werden, ist dies die einfachste und gekapselte Funktion.

**Windows XP: jetbackupinstance** wird in Windows XP eingeführt.

```cpp
    JET_ERR JET_API JetBackupInstance(
      __in          JET_INSTANCE instance,
      __in          JET_PCSTR szBackupPath,
      __in          JET_GRBIT grbit,
      __in          JET_PFNSTATUS pfnStatus
    );
```

### <a name="parameters"></a>Parameter

*lichen*

Die Instanz der Datenbank, die gesichert werden soll.

*szbackuppath*

Das Verzeichnis, in dem die Sicherung gespeichert ist. Wenn der Sicherungs Pfad für die Verwendung von NULL ist, schneidet die-Funktion die Protokolle ab, sofern dies möglich ist.

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
<td><p>Erstellt im Gegensatz zu einer vollständigen Sicherung eine inkrementelle Sicherung. Dies bedeutet, dass nur die Protokolldateien gesichert werden, die seit der letzten vollständigen oder inkrementellen Sicherung erstellt wurden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitBackupSnapshot</p></td>
<td><p>Für die zukünftige Verwendung reserviert.</p></td>
</tr>
</tbody>
</table>


*pfnstatus*

Ein Zeiger auf die [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) Callback-Funktion, die Benachrichtigungs Informationen zum Fortschritt des Sicherungs Vorgangs bereitstellt.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).

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
<td><p>Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg294108(v=exchg.10).md">jetstopserviceinstance</a>beendet wurden.</p></td>
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


Nachdem die Funktion erfolgreich zurückgegeben wurde, sind im Sicherungs Verzeichnis alle Dateien vorhanden, die für eine Wiederherstellung bis zum Zeitpunkt der Sicherung benötigt werden. Wenn es sich um eine vollständige Sicherung handelt, sind die Dateien die Datenbankdateien und die Protokolldateien, die erforderlich sind, um die Datenbank in einen konsistenten Zustand zu bringen. Wenn es sich um eine inkrementelle Sicherung handelt, werden den Verzeichnissen nur Protokolldateien hinzugefügt, aber die bereits vorhandenen Dateien (Datenbanken und Protokolldateien) zusammen mit den neuen Protokolldateien können wieder hergestellt werden, und die Datenbank wird zum Zeitpunkt der Sicherung wieder in den Zustand versetzt.

Als Nebeneffekt der Sicherung werden die Protokolldateien, die nicht mehr benötigt werden, abgeschnitten.

Gleichzeitig werden die Daten Bank Header mit den Informationen aktualisiert, wann die letzte Sicherung erfolgte.

Bei einem Fehler werden keine Dateien im Sicherungs Verzeichnis Ziel vorhanden sein, sodass keine Wiederherstellung möglich ist. Gleichzeitig werden die aktuellen Protokolldateien nicht abgeschnitten.

#### <a name="remarks"></a>Bemerkungen

In den verschiedenen Schritten der Sicherung werden Ereignisprotokoll Einträge generiert, einschließlich der Dateinamen, der Protokoll Verkürzung und des Endergebnisses der Sicherung.

Die inkrementelle Sicherung ist nur möglich, nachdem eine vollständige Sicherung erstellt wurde. Außerdem sind inkrementelle Sicherungen nur möglich, wenn die zirkuläre Protokollierung deaktiviert ist. Es wird empfohlen, dass das Sicherungs Verzeichnis keine anderen Dateien enthält, dann das, das in der Sicherung enthalten ist, oder das von einer vorherigen erfolgreichen Sicherung hinzugefügt wurde.

Das Sicherungs Verzeichnis sollte vorhanden sein, es sei denn, der Parameter *JET_paramCreatePathIfNotExist* für die Instanz festgelegt. Weitere Informationen finden Sie unter [System Parameter](./extensible-storage-engine-system-parameters.md).

Bei der Sicherung wird die Prüfsummen Überprüfung auf allen verwendeten Datenbankseiten und beginnend mit Windows Server 2003 in den Protokolldateien durchgeführt. Dadurch haben Sie die Möglichkeit, die Integrität der Datenbank zu schätzen, auch für Seiten, die während des normalen Betriebs nicht gelesen werden. Wenn eine solche Beschädigung auftritt, tritt bei der Sicherung ein Fehler auf.

Während der Sicherung wird die aktuelle Protokolldatei fertiggestellt, und es wird eine neue Protokoll Generierung gestartet. Dadurch wird das Kopieren der erforderlichen Protokolldateien ermöglicht, da das letzte benötigte Protokoll nicht mehr verwendet wird.

Es wird dringend empfohlen, die Sicherung nicht für andere Zwecke der Sicherung zu verwenden und auf der Engine-Ebene wiederherzustellen. Dadurch wird die Änderung von Fehlern bei Sicherungs-und Wiederherstellungs Vorgängen minimiert.

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
<td><p>Implementiert als <strong>jetbackupinstancew</strong> (Unicode) und <strong>jetbackupinstancea</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_PFNSTATUS](./jet-pfnstatus-callback-function.md)  
[Jetrestore](./jetrestore-function.md)  
[JetRestore2](./jetrestore2-function.md)  
[Jetrestoreingestance](./jetrestoreinstance-function.md)  
[Jetstopserviczustance](./jetstopserviceinstance-function.md)  
[System Parameter](./extensible-storage-engine-system-parameters.md)
