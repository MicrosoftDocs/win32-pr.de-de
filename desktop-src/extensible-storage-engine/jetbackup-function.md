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
ms.openlocfilehash: e17ee5029da8ac71b5421e44a3647494e676ba71
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122982993"
---
# <a name="jetbackup-function"></a>JetBackup-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetbackup-function"></a>JetBackup-Funktion

Die **JetBackup-Funktion** erstellt eine Sicherung der Datenbank, während die Datenbank online ist. Diese Funktion dient in erster Linie der Abwärtskompatibilität mit Windows 2000 und früheren Datenbank-Engines, bei denen nur eine Instanz einer Datenbank zulässig ist. In diesem Fall ist die aktive Instanz die Instanz, die gesichert wird.

```cpp
    JET_ERR JET_API JetBackup(
      __in          JET_PCSTR szBackupPath,
      __in          JET_GRBIT grbit,
      __in          JET_PFNSTATUS pfnStatus
    );
```

### <a name="parameters"></a>Parameter

*szBackupPath*

Das Verzeichnis, in dem die Sicherung gespeichert wird. Wenn der Sicherungspfad NULL ist, werden die Protokolle nach Möglichkeit von der Funktion abgeschnitten.

*grbit*

Eine Gruppe von Bits, die null oder mehr der folgenden Optionen angibt.


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>JET_bitBackupAtomic</p> | <p>Erstellt eine vollständige Sicherung der Datenbank. Dies ermöglicht die Beibehaltung einer vorhandenen Sicherung im gleichen Verzeichnis, wenn bei der neuen Sicherung ein Fehler auftritt.</p> | 
| <p>JET_bitBackupIncremental</p> | <p>Erstellt eine inkrementelle Sicherung im Gegensatz zu einer vollständigen Sicherung. Dies bedeutet, dass nur die Protokolldateien seit der letzten vollständigen oder inkrementellen Sicherung gesichert werden.</p> | 



*pfnStatus*

Zeiger auf die [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) Rückruffunktion, die Benachrichtigungsinformationen zum Fortschritt des Sicherungsvorgangs bereitstellt.

### <a name="return-value"></a>Rückgabewert

Die Funktion gibt einen der [JET_ERR](./jet-err.md) Fehlercodes zurück. Die folgenden werden am häufigsten zurückgegeben. (Eine vollständige Liste der Fehler für diese API finden Sie unter [Extensible Storage Engine Error Codes](./extensible-storage-engine-error-codes.md).)


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errBackupInProgress</p> | <p>Für dieselbe Instanz wird bereits eine Sicherung ausgeführt. Mehrere Sicherungen sind nicht gleichzeitig zulässig.</p> | 
| <p>JET_errBackupNotAllowedYet</p> | <p>Die Instanz ist noch nicht für die Sicherung bereit, da sie initialisiert wird.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da alle Aktivitäten in der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufs von <a href="gg269240(v=exchg.10).md">JetStopService</a>beendet wurden.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da für die der Sitzung zugeordnete Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen.</p><p><strong>Windows XP:</strong> Dieser Rückgabewert wird in Windows XP eingeführt.</p> | 
| <p>JET_errInvalidBackup</p> | <p>Eine inkrementelle Sicherung ist nicht zulässig, wenn die zirkuläre Protokollierung eingeschaltet ist.</p> | 
| <p>JET_errInvalidGrbit</p> | <p>Die angegebenen Optionen sind ungültig.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Ein ungültiger Parameter wurde an die API übergeben.</p> | 
| <p>JET_errInvalidPath</p> | <p>Der Zielpfad ist nicht vorhanden.</p> | 
| <p>JET_errLoggingDisabled</p> | <p>Die Instanz wird ohne Protokollierung ausgeführt. Es ist keine Sicherung zulässig.</p> | 
| <p>JET_errLogReadVerifyFailure</p> | <p>In einer Protokolldatei ist ein Prüfsummenüberprüfungsfehler aufgetreten.</p> | 
| <p>JET_errLogWriteFail</p> | <p>Die Protokollierung für die Instanz ist aufgrund eines unerwarteten Fehlers temporär oder dauerhaft deaktiviert.</p> | 
| <p>JET_errNotInitialized</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz noch nicht initialisiert wurde.</p> | 
| <p>JET_errReadVerifyFailure</p> | <p>Auf einer Datenbankseite ist ein Prüfsummenüberprüfungsfehler aufgetreten.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da ein Wiederherstellungsvorgang für die Instanz ausgeführt wird, die der Sitzung zugeordnet ist.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>Dieselbe Sitzung kann nicht für mehrere Threads gleichzeitig verwendet werden.</p><p><strong>Windows XP:</strong> Dieser Rückgabewert wird in Windows XP eingeführt.</p> | 
| <p>JET_errTermInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz heruntergefahren wird.</p> | 



Wenn die Funktion erfolgreich ausgeführt wird, sind alle Dateien, die für eine Wiederherstellung bis zum Zeitpunkt der Sicherung erforderlich sind, im Sicherungsverzeichnis enthalten. Wenn es sich um eine vollständige Sicherung handelt, handelt es sich bei den Dateien um die Datenbankdateien und die Protokolldateien, die benötigt werden, um die Datenbank in einen konsistenten Zustand zu bringen. Wenn es sich um eine inkrementelle Sicherung handelt, werden den Verzeichnissen nur Protokolldateien hinzugefügt, aber die bereits vorhandenen Dateien (Datenbanken und Protokolldateien) können zusammen mit den neuen Protokolldateien wiederhergestellt werden, um die Datenbank wieder in den Zustand zu bringen, in dem sie sich zu dem Zeitpunkt befand, zu dem die Sicherung begonnen hat.

Als Nebeneffekt der Sicherung werden die Protokolldateien abgeschnitten, die nicht mehr benötigt werden.

Gleichzeitig werden die Datenbankheader mit den Informationen aktualisiert, als die letzte Sicherung durchgeführt wurde.

Wenn die Funktion fehlschlägt, sind keine Dateien im Sicherungsverzeichnisziel vorhanden, sodass keine Wiederherstellung möglich ist. Gleichzeitig werden die aktuellen Protokolldateien nicht abgeschnitten.

#### <a name="remarks"></a>Bemerkungen

Für die verschiedenen Schritte der Sicherung werden Ereignisprotokolleinträge generiert, einschließlich der Dateinamen, der Protokollkürzung und des Endergebnisses der Sicherung.

Inkrementelle Sicherungen sind erst möglich, nachdem eine vollständige Sicherung erstellt wurde. Inkrementelle Sicherungen sind auch nur möglich, wenn die zirkuläre Protokollierung deaktiviert ist. Es wird empfohlen, dass das Sicherungsverzeichnis keine anderen Dateien als die datei enthält, die in der Sicherung verwendet oder von einer vorherigen erfolgreichen Sicherung hinzugefügt wurde.

Das Sicherungsverzeichnis sollte vorhanden sein, es sei denn, der Parameter *JET_paramCreatePathIfNotExist* ist für die Instanz festgelegt. Weitere Informationen finden Sie unter [Systemparameter.](./extensible-storage-engine-system-parameters.md)

Die Sicherung führt eine Prüfsummenüberprüfung auf allen verwendeten Datenbankseiten und ab Windows Server 2003 auch in den Protokolldateien durch. Dies bietet die Möglichkeit, die Integrität der Datenbank zu schätzen, auch für Seiten, die während des normalen Betriebs nicht gelesen werden. Wenn eine solche Beschädigung auftritt, schlägt die Sicherung fehl.

Während der Sicherung wird die aktuelle Protokolldatei abgeschlossen, und es wird ein neues Protokoll generiert. Auf diese Weise können alle erforderlichen Protokolldateien Kopien sein, da das aktuelle Protokoll nicht mehr verwendet wird.

Es wird dringend empfohlen, die Sicherung nicht für andere Zwecke als die Sicherung und Wiederherstellung auf Engine-Ebene zu verwenden. Dadurch wird die Wahrscheinlichkeit minimiert, dass während der Sicherungs- und Wiederherstellungsvorgänge Fehler auftreten.

#### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | 
| <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implementiert als <strong>JetBackupW</strong> (Unicode) und <strong>JetBackupA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Weitere Informationen

[Erweiterbare Storage-Engine-Dateien](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_PFNSTATUS](./jet-pfnstatus-callback-function.md)  
[JetRestore](./jetrestore-function.md)  
[JetRestore2](./jetrestore2-function.md)  
[JetRestoreInstance](./jetrestoreinstance-function.md)  
[JetStopService](./jetstopservice-function.md)  
[Systemparameter](./extensible-storage-engine-system-parameters.md)
