---
title: Protokollierungs- und Wiederherstellungsfehler in Functions in Active Directory Domain Services
description: In diesem Thema werden die Rückgabewerte für Protokollierungs- und Wiederherstellungsfehler für Funktionen in Active Directory Domain Services aufgelistet.
ms.assetid: b927073a-8bbc-45d4-b9d3-25f3aa6c6f53
ms.tgt_platform: multiple
keywords:
- Active Directory-Protokollierung und -Wiederherstellungsfehler AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b267b359b5244fddc0e8a9b2ddfbfb5d6e5f9ab0a7e647683d44759f8a7261b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118186591"
---
# <a name="logging-and-recovery-errors-in-functions-in-active-directory-domain-services"></a>Protokollierungs- und Wiederherstellungsfehler in Functions in Active Directory Domain Services

In diesem Thema werden die Rückgabewerte für Protokollierungs- und Wiederherstellungsfehler für Funktionen in Active Directory Domain Services aufgelistet.



| Wert                                | BESCHREIBUNG                                                                                                                      |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| **hrLogFileCorrupt**                 | Die Protokolldatei ist beschädigt.                                                                                                         |
| **hrNoBackupDirectory**              | Es wurde kein Sicherungsverzeichnis angegeben.                                                                                                   |
| **hrBackupDirectoryNotEmpty**        | Das Sicherungsverzeichnis ist nicht leer.                                                                                               |
| **hrBackupInProgress**               | Die Sicherung ist aktiv.                                                                                                                |
| **hrMissingPreviousLogFile**         | Eine Protokolldatei für den Prüfpunkt fehlt.                                                                                        |
| **hrLogWriteFail**                   | In die Protokolldatei kann nicht geschrieben werden.                                                                                                 |
| **hrBadLogVersion**                  | Die Version der Protokolldatei ist nicht mit der Version des Windows NT/Windows 2000 Directory Service Database (NTDS) kompatibel. |
| **hrInvalidLogSequence**             | Der Zeitstempel im nächsten Protokoll stimmt nicht mit dem erwarteten Wert überein.                                                                 |
| **hrLoggingDisabled**                | Das Protokoll ist nicht aktiv.                                                                                                           |
| **hrLogBufferTooSmall**              | Der Protokollpuffer ist zu klein, um wiederhergestellt zu werden.                                                                                     |
| **hrLogSequenceEnd**                 | Die maximale Anzahl von Protokolldateien wurde überschritten.                                                                               |
| **hrNoBackup**                       | Es wird keine Sicherung ausgeführt.                                                                                                  |
| **hrInvalidBackupSequence**          | Der Sicherungsaufruf ist nicht mehr sequenzierend.                                                                                              |
| **hrBackupNotAllowedYet**            | Eine Sicherung kann jetzt nicht ausgeführt werden.                                                                                                  |
| **hrDeleteBackupFileFail**           | Die Sicherungsdatei kann nicht gelöscht werden.                                                                                                |
| **hrMakeBackupDirectoryFail**        | Ein temporäres Sicherungsverzeichnis kann nicht erstellt werden.                                                                                     |
| **hrInvalidBackup**                  | Eine inkrementelle Sicherung kann nicht ausgeführt werden, wenn die zirkuläre Protokollierung aktiviert ist.                                                      |
| **hrRecoveredWithErrors**            | Während des Reparaturvorgangs sind Fehler aufgetreten.                                                                               |
| **hrMissingLogFile**                 | Die aktuelle Protokolldatei fehlt.                                                                                                 |
| **hrLogDiskFull**                    | Der Protokolldatenträger ist voll.                                                                                                            |
| **hrBadLogSignature**                | Eine Protokolldatei ist beschädigt.                                                                                                           |
| **hrBadDbSignature**                 | Eine Datenbankdatei ist beschädigt.                                                                                                      |
| **hrBadCheckpointSignature**         | Eine Prüfpunktdatei ist beschädigt.                                                                                                    |
| **hrCheckpointCorrupt**              | Eine Prüfpunktdatei wurde nicht gefunden oder ist beschädigt.                                                                       |
| **hrDatabaseInconsistent**           | Die Datenbank ist beschädigt.                                                                                                         |
| **hrConsistentTimeMismatch**         | Die letzte konsistente Uhrzeit der Datenbank stimmt nicht überein.                                                                      |
| **hrPatchFileMismatch**              | Die Patchdatei wird nicht aus dieser Sicherung generiert.                                                                                |
| **hrRestoreLogTooLow**               | Die Startprotokollnummer ist für die Wiederherstellung zu niedrig.                                                                              |
| **hrRestoreLogTooHigh**              | Die Startprotokollnummer ist für die Wiederherstellung zu hoch.                                                                             |
| **hrGivenLogFileHasBadSignature**    | Die vom Band heruntergeladene Protokolldatei ist beschädigt.                                                                                |
| **hrGivenLogFileIsNotContiguous**    | Nach dem Herunterladen des Bands konnte keine erforderliche Protokolldatei gefunden werden.                                                               |
| **hrMissingRestoreLogFiles**         | Die Daten werden nicht vollständig wiederhergestellt, da einige Protokolldateien fehlen.                                                               |
| **hrExistingLogFileHasBadSignature** | Die Protokolldatei im Protokolldateipfad ist beschädigt.                                                                                    |
| **hrExistingLogFileIsNotContiguous** | Eine erforderliche Protokolldatei im Protokolldateipfad wurde nicht gefunden.                                                                        |
| **hrMissingFullBackup**              | Die Datenbank hat vor der inkrementellen Sicherung eine vorherige vollständige Sicherung verpasst.                                                        |
| **hrBadBackupDatabaseSize**          | Die Größe der Sicherungsdatenbank muss ein Vielfaches von 4000 (4096 Bytes) sein.                                                                |
| **hrTermInProgress**                 | Die Datenbank wird heruntergefahren.                                                                                                 |
| **hrFeatureNotAvailable**            | Das Feature ist nicht verfügbar.                                                                                                    |
| **hrInvalidName**                    | Der Name ist ungültig.                                                                                                             |
| **hrInvalidParameter**               | Der Parameter ist ungültig.                                                                                                        |
| **hrColumnNull**                     | Der Wert der Spalte ist NULL.                                                                                                 |
| **hrBufferTruncated**                | Der Puffer ist zu klein für Daten.                                                                                                |
| **hrDatabaseAttached**               | Die Datenbank ist bereits angefügt.                                                                                                |
| **hrInvalidDatabaseId**              | Die Datenbank-ID ist ungültig.                                                                                                      |
| **hrOutOfMemory**                    | Der Computer verfügt nicht über genügend Arbeitsspeicher.                                                                                                   |
| **hrOutOfDatabaseSpace**             | Die Datenbank hat die maximale Größe von 16 GB erreicht.                                                                              |
| **hrOutOfCursors**                   | Out-of-Table-Cursor.                                                                                                            |
| **hrOutOfBuffers**                   | Aus datenbankseitigen Puffern.                                                                                                    |
| **hrTooManyIndexes**                 | Es gibt zu viele Indizes.                                                                                                      |
| **hrTooManyKeys**                    | Ein Index enthält zu viele Spalten.                                                                                          |
| **hrRecordDeleted**                  | Der Datensatz wurde gelöscht.                                                                                                     |
| **hrReadVerifyFailure**              | Fehler bei der Leseüberprüfung.                                                                                              |
| **hrOutOfFileHandles**               | Keine weiteren Dateihandles vorhanden.                                                                                                             |
| **hrDiskIO**                         | Ein Datenträger-E/A-Fehler ist aufgetreten.                                                                                                       |
| **hrInvalidPath**                    | Der Pfad zur Datei ist ungültig.                                                                                                 |
| **hrRecordTooBig**                   | Der Datensatz hat die maximale Größe überschritten.                                                                                        |
| **hrTooManyOpenDatabases**           | Es gibt zu viele geöffnete Datenbanken.                                                                                               |
| **hrInvalidDatabase**                | Die Datei ist keine Datenbankdatei.                                                                                                 |
| **hrNotInitialized**                 | Die Datenbank wurde noch nicht aufgerufen.                                                                                                 |
| **hrAlreadyInitialized**             | Die Datenbank wurde bereits aufgerufen.                                                                                                 |
| **hrFileAccessDenied**               | Auf die Datei kann nicht zugegriffen werden.                                                                                                       |
| **hrBufferTooSmall**                 | Der Puffer ist zu klein.                                                                                                         |
| **hrSeekNotEqual**                   | Entweder SeekLE oder SeekGE kann keine genaue Übereinstimmung finden.                                                                              |
| **hrTooManyColumns**                 | Es sind zu viele Spalten definiert.                                                                                              |
| **hrContainerNotEmpty**              | Der Container ist nicht leer.                                                                                                      |
| **hrInvalidFilename**                | Der Dateiname ist ungültig.                                                                                                         |
| **hrInvalidBookmark**                | Das Lesezeichen ist ungültig.                                                                                                         |
| **hrColumnInUse**                    | Die Spalte wird in einem Index verwendet.                                                                                                  |
| **hrInvalidBufferSize**              | Der Datenpuffer stimmt nicht mit der Spaltengröße überein.                                                                                  |
| **hrColumnNotUpdatable**             | Der Spaltenwert kann nicht festgelegt werden.                                                                                                  |
| **hrIndexInUse**                     | Der Index wird verwendet.                                                                                                             |
| **hrNullKeyDisallowed**              | NULL-Schlüssel sind für einen Index nicht zulässig.                                                                                           |
| **hrNotInTransaction**               | Die Operation muss Teil einer Transaktion sein.                                                                                      |
| **hrNoIdleActivity**                 | Es ist keine Aktivität im Leerlauf aufgetreten.                                                                                                       |
| **hrTooManyActiveUsers**             | Es gibt zu viele aktive Datenbankbenutzer.                                                                                        |
| **hrInvalidCountry**                 | Der Länder- oder Regionscode ist entweder nicht bekannt oder ungültig.                                                                    |
| **hrInvalidLanguageId**              | Die Sprach-ID ist entweder nicht bekannt oder ungültig.                                                                               |
| **hrInvalidCodePage**                | Die Codepage ist entweder nicht bekannt oder ungültig.                                                                                 |
| **hrNoWriteLock**                    | Es gibt keine Schreibsperre auf Transaktionsebene 0.                                                                                   |
| **hrColumnSetNull**                  | Der Spaltenwert ist auf NULL festgelegt.                                                                                                 |
| **hrVersionStoreOutOfMemory**        | Die lMaxVerPages-Werte wurden überschritten (nur XJET).                                                                                           |
| **hrCurrencyStackOutOfMemory**       | Out-of-Cursor.                                                                                                                  |
| **hrOutOfSessions**                  | Außerhalb der Sitzungen.                                                                                                                 |
| **hrWriteConflict**                  | Fehler bei der Schreibsperre aufgrund einer ausstehenden Schreibsperre.                                                                          |
| **hrTransTooDeep**                   | Die Transaktionen sind zu tief geschachtelt.                                                                                          |
| **hrInvalidSesid**                   | Das Sitzungshandle ist ungültig.                                                                                                   |
| **hrSessionWriteConflict**           | Eine andere Sitzung verfügt über eine private Version der Seite.                                                                               |
| **hrInTransaction**                  | Der Vorgang ist innerhalb einer Transaktion nicht zulässig.                                                                               |
| **hrDatabaseDuplicate**              | Die Datenbank ist bereits vorhanden.                                                                                                     |
| **hrDatabaseInUse**                  | Die Datenbank wird verwendet.                                                                                                          |
| **hrDatabaseNotFound**               | Die Datenbank ist nicht vorhanden.                                                                                                     |
| **hrDatabaseInvalidName**            | Der Datenbankname ist ungültig.                                                                                                    |
| **hrDatabaseInvalidPages**           | Die Anzahl der Seiten ist ungültig.                                                                                                  |
| **hrDatabaseCorrupted**              | Die Datenbankdatei ist entweder beschädigt oder wurde nicht gefunden.                                                                          |
| **hrDatabaseLocked**                 | Die Datenbank ist gesperrt.                                                                                                          |
| **hrTableEmpty**                     | Eine leere Tabelle wurde geöffnet.                                                                                                       |
| **hrTableLocked**                    | Die Tabelle ist gesperrt.                                                                                                             |
| **hrTableDuplicate**                 | Die Tabelle ist bereits vorhanden.                                                                                                        |
| **hrTableInUse**                     | Die Tabelle kann nicht gesperrt werden, da sie bereits verwendet wird.                                                                           |
| **hrObjectNotFound**                 | Die Tabelle oder das Objekt ist nicht vorhanden.                                                                                              |
| **hrCannotRename**                   | Die temporäre Datei kann nicht umbenannt werden.                                                                                             |
| **hrDensityInvalid**                 | Die Datei-/Indexdichte ist ungültig.                                                                                               |
| **hrTableNotEmpty**                  | Der gruppierte Index kann nicht definiert werden.                                                                                            |
| **hrInvalidTableId**                 | Die Tabellen-ID ist ungültig.                                                                                                         |
| **hrTooManyOpenTables**              | Weitere Tabellen können nicht geöffnet werden.                                                                                                  |
| **hrHypergalOperation**               | Der Vorgang wird für Tabellen nicht unterstützt.                                                                                        |
| **hrObjectDuplicate**                | Der Tabellen- oder Objektname wird bereits verwendet.                                                                                  |
| **hrInvalidObject**                  | Das -Objekt ist für den -Vorgang ungültig.                                                                                             |
| **hrIndexBuild**                 | Ein gruppierter Index kann nicht erstellt werden.                                                                                               |
| **hrIndexHasPrimary**                | Der primäre Index ist bereits definiert.                                                                                            |
| **hrIndexDuplicate**                 | Der Index ist bereits definiert.                                                                                                    |
| **hrIndexNotFound**                  | Der Index ist nicht vorhanden.                                                                                                        |
| **hrIndexMustStay**                  | Ein gruppierter Index kann nicht gelöscht werden.                                                                                              |
| **hrIndexInvalidDef**                | Die Indexdefinition ist ungültig.                                                                                                 |
| **hrIndexHasClustered**              | Der gruppierte Index ist bereits definiert.                                                                                          |
| **hrCreateIndexFailed**              | Der Index kann nicht erstellt werden, weil beim Erstellen einer Tabelle ein Fehler aufgetreten ist.                                                     |
| **hrTooManyOpenIndexes**             | Außerhalb der Indexbeschreibungsblöcke.                                                                                                 |
| **hrColumnLong**                     | Der Spaltenwert ist zu lang.                                                                                                    |
| **hrColumnDoesNotFit**               | Das Feld passt nicht in den Datensatz.                                                                                            |
| **hrNullInvalid**                    | Der Wert darf nicht null sein.                                                                                                        |
| **hrColumnIndexed**                  | Die Spalte kann nicht gelöscht werden, da sie indiziert ist.                                                                                  |
| **hrColumnTooBig**                   | Die Länge des Felds überschreitet die maximale Länge von 255 Byte.                                                                 |
| **hrColumnNotFound**                 | Die Spalte kann nicht gefunden werden.                                                                                                       |
| **hrColumnDuplicate**                | Das Feld ist bereits definiert.                                                                                                    |
| **hrColumn2ndSysMaint**              | Pro Tabelle ist nur eine Spalte mit automatischer Inkrement- oder Versionsinkrementausführung zulässig.                                                                  |
| **hrInvalidColumnType**              | Der Spaltendatentyp ist ungültig.                                                                                                 |
| **hrColumnMaxTruncated**             | Die Spalte wurde abgeschnitten, da sie die maximale Länge von 255 Bytes überschritten hat.                                                    |
| **hrColumnCannotIndex**              | Eine Long Value-Spalte kann nicht indiziert werden.                                                                                             |
| **hrTaggedNotNULL**                  | Markierte Spalten dürfen nicht NULL sein.                                                                                                   |
| **hrNoCurrentIndex**                 | Der Eintrag ist ohne aktuellen Index ungültig.                                                                                    |
| **hrKeyIs Auswendung**                      | Der Schlüssel ist vollständig.                                                                                                             |
| **hrBadColumnId**                    | Die Spalten-ID ist falsch.                                                                                                      |
| **hrBadItagSequence**                | Es gibt einen ungültigen Instanzbezeichner für eine mehrwertige Spalte.                                                                     |
| **hrCannotBeTagged**                 | AutoIncrement und Version können nicht mehrwertige Werte enthalten.                                                                                 |
| **hrRecordNotFound**                 | Der Schlüssel konnte nicht gefunden werden.                                                                                                          |
| **hrNoCurrentRecord**                | Die Währung befindet sich nicht in einem Datensatz.                                                                                                 |
| **hrRecordClusteredChanged**         | Ein gruppierter Schlüssel kann nicht geändert werden.                                                                                               |
| **hrKeyDuplicate**                   | Der Schlüssel ist bereits vorhanden.                                                                                                          |
| **hrAlreadyPrepared**                | Der aktuelle Eintrag wurde bereits kopiert oder gelöscht.                                                                            |
| **hrKeyNot Auswendung**                     | Es wurde kein Schlüssel erstellt.                                                                                                                 |
| **hrUpdateNotPrepared**              | Das Update wurde nicht vorbereitet.                                                                                                         |
| **hrwrnDataHasChanged**              | Die Daten wurden geändert.                                                                                                                |
| **hrerrDataHasChanged**              | Der Vorgang wurde abgebrochen, weil sich die Daten geändert haben.                                                                            |
| **hrKeyChanged**                     | In einen neuen Schlüssel verschoben.                                                                                                              |
| **hrTooManySorts**                   | Es gibt zu viele Sortierprozesse.                                                                                               |
| **hrInvalidOnSort**                  | Ein ungültiger Vorgang ist in der Sortierung aufgetreten.                                                                               |
| **hrTempFileOpenError**              | Die temporäre Datei kann nicht geöffnet werden.                                                                                               |
| **hrTooManyAttachedDatabases**       | Es sind zu viele Datenbanken geöffnet.                                                                                               |
| **hrDiskFull**                       | Der Datenträger ist voll.                                                                                                                |
| **hrPermissionDenied**               | Die Berechtigung wird verweigert.                                                                                                            |
| **hrFileNotFound**                   | Die Datei wurde nicht finden.                                                                                                         |
| **hrFileOpenReadOnly**               | Die Datenbankdatei ist schreibgeschützt.                                                                                                  |
| **hrAfterInitialization**            | Die Wiederherstellung nach der Initialisierung ist nicht möglich.                                                                                          |
| **hrLogCorrupted**                   | Die Datenbankprotokolldateien sind beschädigt.                                                                                              |
| **hrInvalidOperation**               | Der Vorgang ist ungültig.                                                                                                        |
| **hrAccessDenied**                   | Zugriff verweigert.“                                                                                                                |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erfolgreich](success.md)
</dt> <dt>

[Sicherungsfehler in Active Directory Domain Services](backup-errors-in-active-directory-domain-services.md)
</dt> <dt>

[Systemfehler in Active Directory Domain Services](system-errors-in-active-directory-domain-services.md)
</dt> <dt>

[Verzeichnis-Manager-Fehler](directory-manager-errors.md)
</dt> <dt>

[Rückgabewerte für Funktionen in Active Directory Domain Services](return-values-for-functions-in-active-directory-domain-services.md)
</dt> </dl>

 

 




