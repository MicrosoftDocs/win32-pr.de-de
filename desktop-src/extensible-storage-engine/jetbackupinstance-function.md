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
ms.openlocfilehash: 138d95c80070d8e1b1d7c958534cd93965db47aa
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472666"
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


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>JET_bitBackupAtomic</p> | <p>Erstellt eine vollständige Sicherung der Datenbank. Dies ermöglicht die Beibehaltung einer vorhandenen Sicherung im gleichen Verzeichnis, wenn bei der neuen Sicherung ein Fehler auftritt.</p> | 
| <p>JET_bitBackupIncremental</p> | <p>Erstellt eine inkrementelle Sicherung im Gegensatz zu einer vollständigen Sicherung. Dies bedeutet, dass nur die Protokolldateien gesichert werden, die seit der letzten vollständigen oder inkrementellen Sicherung erstellt wurden.</p> | 
| <p>JET_bitBackupSnapshot</p> | <p>Für die zukünftige Verwendung reserviert.</p> | 



*pfnStatus*

Zeiger auf die [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) Rückruffunktion, die Benachrichtigungsinformationen zum Fortschritt des Sicherungsvorgangs bereitstellt.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errBackupInProgress</p> | <p>Für dieselbe Instanz wird bereits eine Sicherung ausgeführt. Mehrere Sicherungen sind nicht gleichzeitig zulässig.</p> | 
| <p>JET_errBackupNotAllowedYet</p> | <p>Die Instanz ist noch nicht für die Sicherung bereit, da sie initialisiert wird.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da alle Aktivitäten in der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufs von <a href="gg294108(v=exchg.10).md">JetStopServiceInstance</a>beendet wurden.</p> | 
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


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista oder Windows XP.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008 oder Windows Server 2003.</p> | | <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | | <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Wird als <strong>JetBackupInstanceW</strong> (Unicode) und <strong>JetBackupInstanceA</strong> (ANSI) implementiert.</p> | 



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
