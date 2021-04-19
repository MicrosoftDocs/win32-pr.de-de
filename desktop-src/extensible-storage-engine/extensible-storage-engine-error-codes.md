---
description: Weitere Informationen finden Sie in den Fehler Codes der Extensible Storage Engine.
title: Fehler Codes für erweiterbare Speicher-Engine
TOCTitle: Extensible Storage Engine Error Codes
ms:assetid: 7534370d-aed6-4980-b1ca-c3d063507e31
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269297(v=EXCHG.10)
ms:contentKeyID: 32765589
ms.date: 09/22/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9de4bd8157e0b7210315352ba0760293a892f087
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360796"
---
# <a name="extensible-storage-engine-error-codes"></a>Fehler Codes für erweiterbare Speicher-Engine


_**Gilt für:** Windows | Windows Server_

## <a name="extensible-storage-engine-error-codes"></a>Fehler Codes für erweiterbare Speicher-Engine

Die folgenden Fehlercodes (Flags) werden von Funktionen in der Extensible Storage Engine-API verwendet.

Ein [JET_ERR](./jet-err.md) Wert von 0 (null) sollte als Erfolg interpretiert werden.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Erfolg</p></th>
<th><p>BESCHREIBUNG</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess 0</p></td>
<td><p>Die Funktion wurde erfolgreich ausgeführt.</p></td>
</tr>
</tbody>
</table>


Ein [JET_ERR](./jet-err.md) Wert, der größer als 0 (null) ist, sollte als Warnung interpretiert werden.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Warnungen</p></th>
<th><p>BESCHREIBUNG</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_wrnRemainingVersions<br />
321</p></td>
<td><p>Der Versionsspeicher ist noch aktiv. Dieser Fehler wird vom Verzeichnis-Manager zurückgegeben.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnUniqueKey<br />
345</p></td>
<td><p>Eine Suche nach einem nicht eindeutigen Index ergab einen eindeutigen Schlüssel. Dieser Fehler wird vom Verzeichnis-Manager zurückgegeben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnSeparateLongValue<br />
406</p></td>
<td><p>Eine Daten Bank Spalte ist ein getrennter Long-Wert. Dieser Fehler wird vom Daten Satz-Manager zurückgegeben.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnExistingLogFileHasBadSignature<br />
558</p></td>
<td><p>Die vorhandene Protokolldatei hat eine ungültige Signatur.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnExistingLogFileIsNotContiguous<br />
559</p></td>
<td><p>Die vorhandene Protokolldatei ist nicht zusammenhängend.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnSkipThisRecord<br />
564</p></td>
<td><p>Dieser Fehler ist nur für die interne Verwendung vorgesehen.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnTargetInstanceRunning<br />
578</p></td>
<td><p>Die für die Wiederherstellung angegebene TargetInstance wird ausgeführt.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnDatabaseRepaired<br />
595</p></td>
<td><p>Die Daten Bank Beschädigung wurde repariert.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnNull<br />
1004</p></td>
<td><p>Die Spalte weist einen <strong>null</strong> -Wert auf.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnBufferTruncated<br />
1006</p></td>
<td><p>Der Puffer ist zu klein für die Daten.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnDatabaseAttached<br />
1007</p></td>
<td><p>Die Datenbank ist bereits angefügt.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnSortOverflow<br />
1009</p></td>
<td><p>Die Sortierung, die versucht wird, verfügt nicht über genügend Arbeitsspeicher, um den Vorgang abzuschließen.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnSeekNotEqual<br />
1039</p></td>
<td><p>Bei einer Suche wurde eine genaue Entsprechung nicht gefunden.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnRecordFoundGreater<br />
JET_wrnSeekNotEqual</p></td>
<td><p>Bei einer Suche wurde eine genaue Entsprechung nicht gefunden. Dieser Fehler wird vom Daten Satz-Manager zurückgegeben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnRecordFoundLess<br />
JET_wrnSeekNotEqual</p></td>
<td><p>Bei einer Suche wurde eine genaue Entsprechung nicht gefunden. Dieser Fehler wird vom Daten Satz-Manager zurückgegeben.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnNoErrorInfo<br />
1.055</p></td>
<td><p>Es sind keine erweiterten Fehlerinformationen vorhanden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnNoIdleActivity<br />
1058</p></td>
<td><p>Es ist keine Aktivität im Leerlauf aufgetreten.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnNoWriteLock<br />
1067</p></td>
<td><p>Es ist keine Schreibsperre auf Transaktionsebene 0 vorhanden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnSetNull<br />
1068</p></td>
<td><p>Die Spalte wird auf einen <strong>null</strong> -Wert festgelegt.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnTableEmpty<br />
1301</p></td>
<td><p>Eine leere Tabelle wurde geöffnet.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnTableInUseBySystem<br />
1327</p></td>
<td><p>Für die System Bereinigung ist ein Cursor in der Tabelle geöffnet.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnCorruptIndexDeleted<br />
1415</p></td>
<td><p>Der veraltete Index muss entfernt werden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnMaxTruncated<br />
1512</p></td>
<td><p>Die maximale Länge ist zu groß und wurde abgeschnitten.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnCopyLongValue<br />
1520</p></td>
<td><p>Ein BLOB-Wert wurde aus dem Datensatz in einen separaten Speicher großer BLOBs verschoben.</p>
<p><strong>Hinweis</strong> Dieser Fehler ist nur für die interne Verwendung vorgesehen.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnSkipped<br />
1531</p></td>
<td><p>Die Spaltenwerte wurden nicht zurückgegeben, weil die entsprechende Spalten-ID oder das <em>itagsequence</em> -Element aus der <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a> Struktur, die für die Enumeration angefordert wurde, NULL war.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnColumnNotLocal<br />
1532</p></td>
<td><p>Die Spaltenwerte wurden nicht zurückgegeben, da Sie nicht aus den vorhandenen Daten rekonstruiert werden konnten.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnMoreTags<br />
1533</p></td>
<td><p>Die vorhandenen Spaltenwerte wurden nicht für die Enumeration angefordert.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnColumnTruncated<br />
1534</p></td>
<td><p>Der Spaltenwert wurde bei der Enumeration an der angeforderten Größenbeschränkung abgeschnitten.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnPresent<br />
1535</p></td>
<td><p>Die Spaltenwerte sind vorhanden, wurden jedoch nicht von der Anforderung zurückgegeben.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnColumnSingleValue<br />
1536</p></td>
<td><p>Der Spaltenwert wurde in JET_COLUMNENUM zurückgegeben, weil der JET_bitEnumerateCompressOutput festgelegt wurde.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnDefault<br />
1537</p></td>
<td><p>Der Spaltenwert wird auf den Standardwert der Spalte festgelegt.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnDataHasChanged<br />
1610</p></td>
<td><p>Die Daten wurden geändert.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnKeyChanged<br />
1618</p></td>
<td><p>Es wird ein neuer Schlüssel verwendet.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnFileOpenReadOnly<br />
1813</p></td>
<td><p>Die Datenbankdatei ist schreibgeschützt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnIdleFull<br />
1908</p></td>
<td><p>Die Registrierung im Leerlauf ist voll.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnDefragAlreadyRunning<br />
2000</p></td>
<td><p>Es wurde bereits eine Online Defragmentierung für die angegebene Datenbank ausgeführt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnDefragNotRunning<br />
2001</p></td>
<td><p>Eine Online Defragmentierung wird nicht für die angegebene Datenbank ausgeführt.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnCallbackNotRegistered<br />
2100</p></td>
<td><p>Die Registrierung einer nicht vorhandenen Rückruffunktion wurde aufgehoben.</p></td>
</tr>
</tbody>
</table>


Ein [JET_ERR](./jet-err.md) Wert, der kleiner als 0 (null) ist, sollte als Fehler interpretiert werden.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Errors</p></th>
<th><p>BESCHREIBUNG</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_wrnNyi<br />
-1</p></td>
<td><p>Die Funktion ist noch nicht implementiert.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRfsFailure<br />
-100</p></td>
<td><p>Der Ressourcen Fehler Simulator ist fehlgeschlagen.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRfsNotArmed<br />
-101</p></td>
<td><p>Der Ressourcen Fehler Simulator wurde nicht initialisiert.</p></td>
</tr>
<tr class="even">
<td><p>JET_errFileClose<br />
-102</p></td>
<td><p>Die Datei konnte nicht geschlossen werden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfThreads<br />
-103</p></td>
<td><p>Der Thread konnte nicht gestartet werden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyIO<br />
-105</p></td>
<td><p>Das System ist aufgrund zu vieler IOS ausgelastet.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTaskDropped<br />
-106</p></td>
<td><p>Die angeforderte asynchrone Aufgabe konnte nicht ausgeführt werden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInternalError<br />
-107</p></td>
<td><p>Es ist ein schwerwiegender interner Fehler aufgetreten.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseBufferDependenciesCorrupted<br />
-255</p></td>
<td><p>Die Puffer Abhängigkeiten wurden nicht ordnungsgemäß festgelegt, und es ist ein Wiederherstellungs Fehler aufgetreten.</p></td>
</tr>
<tr class="even">
<td><p>JET_errPreviousVersion<br />
-322</p></td>
<td><p>Die Version war bereits vorhanden, und es ist ein Wiederherstellungs Fehler aufgetreten. Dieser Fehler wird vom Verzeichnis-Manager zurückgegeben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errPageBoundary<br />
-323</p></td>
<td><p>Die Seiten Grenze wurde erreicht. Dieser Fehler wird vom Verzeichnis-Manager zurückgegeben.</p></td>
</tr>
<tr class="even">
<td><p>JET_errKeyBoundary<br />
-324</p></td>
<td><p>Die Schlüssel Grenze wurde erreicht. Dieser Fehler wird vom Verzeichnis-Manager zurückgegeben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBadPageLink<br />
-327</p></td>
<td><p>Die Datenbank ist beschädigt. Dieser Fehler wird vom Verzeichnis-Manager zurückgegeben.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBadBookmark<br />
-328</p></td>
<td><p>Das Lesezeichen hat keine entsprechende Adresse in der Datenbank. Dieser Fehler wird vom Verzeichnis-Manager zurückgegeben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNTSystemCallFailed<br />
-334</p></td>
<td><p>Fehler beim Abrufen des Betriebssystems. Dieser Fehler wird vom Verzeichnis-Manager zurückgegeben.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBadParentPageLink<br />
-338</p></td>
<td><p>Eine übergeordnete Datenbank ist beschädigt. Dieser Fehler wird vom Verzeichnis-Manager zurückgegeben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSPAvailExtCacheOutOfSync<br />
-340</p></td>
<td><p>Der availext-Cache entspricht nicht der B +-Struktur. Dieser Fehler wird vom Verzeichnis-Manager zurückgegeben.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSPAvailExtCorrupted<br />
-341</p></td>
<td><p>Die Struktur des allavailext-Raums ist beschädigt. Dieser Fehler wird vom Verzeichnis-Manager zurückgegeben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSPAvailExtCacheOutOfMemory<br />
-342</p></td>
<td><p>Fehler aufgrund von nicht genügend Arbeitsspeicher beim Zuordnen eines availext-Cache Knotens. Dieser Fehler wird vom Verzeichnis-Manager zurückgegeben.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSPOwnExtCorrupted<br />
-343</p></td>
<td><p>Der OwnExt-Raum Baum ist beschädigt. Dieser Fehler wird vom Verzeichnis-Manager zurückgegeben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDbTimeCorrupted<br />
-344</p></td>
<td><p>Der dbtime-Wert auf der aktuellen Seite ist größer als die globale dbtime-Datenbank. Dieser Fehler wird vom Verzeichnis-Manager zurückgegeben.</p></td>
</tr>
<tr class="even">
<td><p>JET_errKeyTruncated<br />
-346</p></td>
<td><p>Der Versuch, einen Schlüssel für einen Index Eintrag zu erstellen, ist fehlgeschlagen, da der Schlüssel abgeschnitten wurde und die Index Definition die Schlüssel abgeschnittene nicht zulässt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errKeyTooBig<br />
-408</p></td>
<td><p>Der Schlüssel ist zu groß. Dieser Fehler wird vom Daten Satz-Manager zurückgegeben.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidLoggedOperation<br />
-500</p></td>
<td><p>Der protokollierte Vorgang kann nicht wiederholt werden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLogFileCorrupt<br />
-501</p></td>
<td><p>Die Protokolldatei ist beschädigt.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNoBackupDirectory<br />
-503</p></td>
<td><p>Es wurde kein Sicherungs Verzeichnis angegeben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBackupDirectoryNotEmpty<br />
-504</p></td>
<td><p>Das Sicherungs Verzeichnis ist nicht leer.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBackupInProgress<br />
-505</p></td>
<td><p>Die Sicherung ist bereits aktiv.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress<br />
-506</p></td>
<td><p>Eine Wiederherstellung wird ausgeführt.</p></td>
</tr>
<tr class="even">
<td><p>JET_errMissingPreviousLogFile<br />
-509</p></td>
<td><p>Die Protokolldatei fehlt für den Prüf Punkt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLogWriteFail<br />
-510</p></td>
<td><p>Fehler beim Schreiben in die Protokolldatei.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogDisabledDueToRecoveryFailure<br />
-511</p></td>
<td><p>Der Versuch, nach der Wiederherstellung in das Protokoll zu schreiben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errCannotLogDuringRecoveryRedo<br />
-512</p></td>
<td><p>Fehler beim Schreiben in das Protokoll während der Wiederherstellungs Wiederholung.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogGenerationMismatch<br />
-513</p></td>
<td><p>Der Name der Protokolldatei entspricht nicht der internen Generierungs Nummer.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBadLogVersion<br />
-514</p></td>
<td><p>Die Version der Protokolldatei ist nicht mit der ESE-Version kompatibel.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidLogSequence<br />
-515</p></td>
<td><p>Der Zeitstempel im nächsten Protokoll stimmt nicht mit dem erwarteten Zeitstempel.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLoggingDisabled<br />
-516</p></td>
<td><p>Das Protokoll ist nicht aktiv.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogBufferTooSmall<br />
-517</p></td>
<td><p>Der Protokollpuffer ist zu klein für die Wiederherstellung.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLogSequenceEnd<br />
-519</p></td>
<td><p>Die maximale Protokolldatei Nummer wurde überschritten.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNoBackup<br />
-520</p></td>
<td><p>Es wird keine Sicherung durchgeführt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidBackupSequence<br />
-521</p></td>
<td><p>Der Sicherungs Aufrufwert ist nicht in der Reihenfolge.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBackupNotAllowedYet<br />
-523</p></td>
<td><p>Zurzeit kann keine Sicherung durchgeführt werden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDeleteBackupFileFail<br />
-524</p></td>
<td><p>Eine Sicherungsdatei konnte nicht gelöscht werden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errMakeBackupDirectoryFail<br />
-525</p></td>
<td><p>Das temporäre Sicherungs Verzeichnis konnte nicht erstellt werden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidBackup<br />
-526</p></td>
<td><p>Zirkuläre Protokollierung ist aktiviert. eine inkrementelle Sicherung kann nicht ausgeführt werden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRecoveredWithErrors<br />
-527</p></td>
<td><p>Die Daten wurden mit Fehlern wieder hergestellt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errMissingLogFile<br />
-528</p></td>
<td><p>Die aktuelle Protokolldatei fehlt.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogDiskFull<br />
-529</p></td>
<td><p>Der Protokolldatenträger ist voll.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBadLogSignature<br />
-530</p></td>
<td><p>Für eine Protokolldatei ist eine ungültige Signatur vorhanden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBadDbSignature<br />
-531</p></td>
<td><p>Für eine Datenbankdatei ist eine ungültige Signatur vorhanden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBadCheckpointSignature<br />
-532</p></td>
<td><p>Es ist eine ungültige Signatur für eine Prüf Punkt Datei vorhanden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errCheckpointCorrupt<br />
-533</p></td>
<td><p>Die Prüf Punkt Datei wurde nicht gefunden oder ist beschädigt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errMissingPatchPage<br />
-534</p></td>
<td><p>Die Seite "Datenbank-Patchdatei" wurde während der Wiederherstellung nicht gefunden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBadPatchPage<br />
-535</p></td>
<td><p>Die Seite "Datenbank-Patchdatei" ist ungültig.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRedoAbruptEnded<br />
-536</p></td>
<td><p>Die Wiederholung wurde aufgrund eines plötzlichen Fehlers beim Lesen der Protokolle aus der Protokolldatei plötzlich beendet.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBadSLVSignature<br />
-537</p></td>
<td><p>Dieses Flag ist reserviert.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errPatchFileMissing<br />
-538</p></td>
<td><p>Die feste Wiederherstellung hat erkannt, dass eine datenbankpatchdatei im Sicherungs Satz fehlt.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseLogSetMismatch<br />
-539</p></td>
<td><p>Die Datenbank gehört nicht zum aktuellen Satz von Protokolldateien.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseStreamingFileMismatch<br />
-540</p></td>
<td><p>Dieses Flag ist reserviert.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogFileSizeMismatch<br />
-541</p></td>
<td><p>Die tatsächliche Protokolldatei Größe entspricht nicht <a href="gg269235(v=exchg.10).md">JET_paramLogFileSize</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errCheckpointFileNotFound<br />
-542</p></td>
<td><p>Die Prüf Punkt Datei konnte nicht gefunden werden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRequiredLogFilesMissing<br />
-543</p></td>
<td><p>Die für die Wiederherstellung erforderlichen Protokolldateien fehlen.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSoftRecoveryOnBackupDatabase<br />
-544</p></td>
<td><p>Eine weiche Wiederherstellung wird in der Regel für eine Sicherungs Datenbank verwendet, wenn stattdessen eine Wiederherstellung verwendet werden soll.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogFileSizeMismatchDatabasesConsistent<br />
-545</p></td>
<td><p>Die Datenbanken wurden wieder hergestellt, die Protokolldatei Größe, die während der Wiederherstellung verwendet wird, stimmt jedoch nicht mit <a href="gg269235(v=exchg.10).md">JET_paramLogFileSize</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLogSectorSizeMismatch<br />
-546</p></td>
<td><p>Die Sektorgröße der Protokolldatei stimmt nicht mit der Sektorgröße des aktuellen Volumes identisch.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogSectorSizeMismatchDatabasesConsistent<br />
-547</p></td>
<td><p>Die Datenbanken wurden wieder hergestellt, aber die Sektorgröße der Protokolldatei (die während der Wiederherstellung verwendet wird) entspricht nicht der Sektorgröße des aktuellen Volumes.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLogSequenceEndDatabasesConsistent<br />
-548</p></td>
<td><p>Die Datenbanken wurden wieder hergestellt, aber alle möglichen Protokoll Generierungen in der aktuellen Sequenz wurden verwendet. Alle Protokolldateien und die Prüf Punkt Datei müssen gelöscht werden, und die Datenbanken müssen gesichert werden, bevor Sie fortfahren können.</p></td>
</tr>
<tr class="even">
<td><p>JET_errStreamingDataNotLogged<br />
-549</p></td>
<td><p>Es wurde ein unzulässiger Versuch unternommen, einen Vorgang zum Streamen von Dateien wiederzugeben, bei dem die Daten nicht protokolliert wurden Dies wird wahrscheinlich durch einen Roll Forward-Versuch verursacht, bei dem die zirkuläre Protokollierung aktiviert ist.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseDirtyShutdown<br />
-550</p></td>
<td><p>Die Datenbank wurde nicht ordnungsgemäß heruntergefahren. Eine Wiederherstellung muss zuerst ausgeführt werden, um Daten Bank Vorgänge für das vorherige Herunterfahren ordnungsgemäß abzuschließen.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseInconsistent<br />
JET_errDatabaseDirtyShutdown</p></td>
<td><p>Dieser Fehler ist veraltet und wurde durch JET_errDatabaseDirtyShutdown ersetzt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errConsistentTimeMismatch<br />
-551</p></td>
<td><p>Der letzte konsistente Zeitpunkt für die Datenbank wurde nicht abgeglichen.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabasePatchFileMismatch<br />
-552</p></td>
<td><p>Die Datenbank-Patchdatei wird nicht aus dieser Sicherung generiert.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errEndingRestoreLogTooLow<br />
-553</p></td>
<td><p>Die Start Protokollnummer ist zu niedrig für die Wiederherstellung.</p></td>
</tr>
<tr class="even">
<td><p>JET_errStartingRestoreLogTooHigh<br />
-554</p></td>
<td><p>Die Start Protokollnummer ist zu hoch für die Wiederherstellung.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errGivenLogFileHasBadSignature<br />
-555</p></td>
<td><p>Die Wiederherstellungs Protokolldatei hat eine ungültige Signatur.</p></td>
</tr>
<tr class="even">
<td><p>JET_errGivenLogFileIsNotContiguous<br />
-556</p></td>
<td><p>Die Wiederherstellungs Protokolldatei ist nicht zusammenhängend.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errMissingRestoreLogFiles<br />
-557</p></td>
<td><p>Einige Wiederherstellungs Protokolldateien fehlen.</p></td>
</tr>
<tr class="even">
<td><p>JET_errMissingFullBackup<br />
-560</p></td>
<td><p>Die Datenbank hat vor dem Versuch, eine inkrementelle Sicherung auszuführen, eine vorherige vollständige Sicherung verpasst.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBadBackupDatabaseSize<br />
-561</p></td>
<td><p>Die Größe der Sicherungs Datenbank ist kein Vielfaches der Seitengröße der Datenbank.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseAlreadyUpgraded<br />
-562</p></td>
<td><p>Der aktuelle Versuch, eine Datenbank zu aktualisieren, wurde angehalten, da die Datenbank bereits aktuell ist.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseIncompleteUpgrade<br />
-563</p></td>
<td><p>Die Datenbank wurde nur teilweise in das aktuelle Format konvertiert. Die Datenbank muss von der Sicherung wieder hergestellt werden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errMissingCurrentLogFiles<br />
-565</p></td>
<td><p>Einige aktuelle Protokolldateien fehlen für die fortlaufende Wiederherstellung.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDbTimeTooOld<br />
-566</p></td>
<td><p>Der dbtime fest-Wert auf einer Seite ist kleiner als der dbtimebefore-Wert, der im Datensatz liegt.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDbTimeTooNew<br />
-567</p></td>
<td><p>Der dbtime fest-Wert auf einer Seite liegt vor dem dbtimebefore-Wert, der im Datensatz liegt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errMissingFileToBackup<br />
-569</p></td>
<td><p>Einige Protokolldateien oder Datenbank-Patchdateien fehlten während der Sicherung.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogTornWriteDuringHardRestore<br />
-570</p></td>
<td><p>Ein zerrissener Schreibvorgang wurde in einer Sicherung erkannt, die während einer fest Wiederherstellung festgelegt wurde.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLogTornWriteDuringHardRecovery<br />
-571</p></td>
<td><p>Während einer fest Wiederherstellung wurde ein zerrissener Schreibvorgang erkannt (das Protokoll war nicht Teil eines Sicherungs Satzes).</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogCorruptDuringHardRestore<br />
-573</p></td>
<td><p>Während einer fest Wiederherstellung wurde in einem Sicherungs Satz eine Beschädigung festgestellt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLogCorruptDuringHardRecovery<br />
-574</p></td>
<td><p>Während der fest Wiederherstellung wurde eine Beschädigung festgestellt (das Protokoll war nicht Teil eines Sicherungs Satzes).</p></td>
</tr>
<tr class="even">
<td><p>JET_errMustDisableLoggingForDbUpgrade<br />
-575</p></td>
<td><p>Beim Upgraden einer Datenbank kann die Protokollierung nicht aktiviert werden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBadRestoreTargetInstance<br />
-577</p></td>
<td><p>Entweder wurde die für die Wiederherstellung angegebene TargetInstance nicht gefunden, oder die Protokolldateien stimmen nicht ab.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRecoveredWithoutUndo<br />
-579</p></td>
<td><p>Die Datenbank-Engine hat alle Vorgänge im Transaktionsprotokoll wiedergegeben, um eine Wiederherstellung durchzuführen, aber der Aufrufer hat die Wiederherstellung beendet, ohne dass ein Rollback für nicht ausgeführten Updates</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabasesNotFromSameSnapshot<br />
-580</p></td>
<td><p>Die wiederherzustellenden Datenbanken stammen nicht aus derselben Schattenkopiesicherung.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSoftRecoveryOnSnapshot<br />
-581</p></td>
<td><p>Es gibt eine weiche Wiederherstellung einer Datenbank aus einem schattenkopiesicherungssatz.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errUnicodeTranslationBufferTooSmall<br />
-601</p></td>
<td><p>Der Unicode-Übersetzungs Puffer ist zu klein.</p></td>
</tr>
<tr class="even">
<td><p>JET_errUnicodeTranslationFail<br />
-602</p></td>
<td><p>Die Unicode-Normalisierung ist fehlgeschlagen.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errUnicodeNormalizationNotSupported<br />
-603</p></td>
<td><p>Das Betriebssystem bietet keine Unterstützung für die Unicode-Normalisierung, und es wurde kein normalisierungs Rückruf angegeben.</p></td>
</tr>
<tr class="even">
<td><p>JET_errExistingLogFileHasBadSignature<br />
-610</p></td>
<td><p>Die vorhandene Protokolldatei hat eine ungültige Signatur.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errExistingLogFileIsNotContiguous<br />
-611</p></td>
<td><p>Eine vorhandene Protokolldatei ist nicht zusammenhängend.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogReadVerifyFailure<br />
-612</p></td>
<td><p>In der Protokolldatei wurde während der Sicherung ein Prüfsummen Fehler gefunden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSLVReadVerifyFailure<br />
-613</p></td>
<td><p>Dieses Flag ist reserviert.</p></td>
</tr>
<tr class="even">
<td><p>JET_errCheckpointDepthTooDeep<br />
-614</p></td>
<td><p>Zwischen dem Prüfpunkt und der aktuellen Generierung sind zu viele ausstehende Generationen vorhanden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreOfNonBackupDatabase<br />
-615</p></td>
<td><p>Für eine Datenbank, die keine Sicherungs Datenbank war, wurde eine harte Wiederherstellung versucht.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidGrbit<br />
-900</p></td>
<td><p>Es ist ein ungültiger grbit-Parameter vorhanden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress<br />
-1000</p></td>
<td><p>Die Beendigung wird ausgeführt.</p></td>
</tr>
<tr class="even">
<td><p>JET_errFeatureNotAvailable<br />
-1001</p></td>
<td><p>Dieses API-Element wird nicht unterstützt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidName<br />
-1002</p></td>
<td><p>Ein ungültiger Name wird verwendet.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter<br />
-1003</p></td>
<td><p>Ein ungültiger API-Parameter wird verwendet.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseFileReadOnly<br />
-1008</p></td>
<td><p>Es wurde versucht, eine schreibgeschützte Datenbankdatei für Lese-/Schreibvorgänge anzufügen.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidDatabaseId<br />
-1010</p></td>
<td><p>Es ist eine ungültige Datenbank-ID vorhanden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfMemory<br />
-1011</p></td>
<td><p>Das System verfügt nicht über genügend Arbeitsspeicher.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfDatabaseSpace<br />
-1012</p></td>
<td><p>Die maximale Datenbankgröße wurde erreicht.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfCursors<br />
-1013</p></td>
<td><p>Die Tabelle ist nicht von den Cursorn.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfBuffers<br />
-1014</p></td>
<td><p>Die Datenbank befindet sich nicht im Seiten Puffer.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyIndexes<br />
-1015</p></td>
<td><p>Es sind zu viele Indizes vorhanden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyKeys<br />
-1016</p></td>
<td><p>Es gibt zu viele Spalten in einem Index.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRecordDeleted<br />
-1017</p></td>
<td><p>Der Datensatz wurde gelöscht.</p></td>
</tr>
<tr class="even">
<td><p>JET_errReadVerifyFailure<br />
-1018</p></td>
<td><p>Prüfsummen Fehler auf einer Datenbankseite.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errPageNotInitialized<br />
-1019</p></td>
<td><p>Es gibt eine leere Datenbankseite.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfFileHandles<br />
-1020</p></td>
<td><p>Es sind keine Datei Handles vorhanden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDiskIO<br />
-1022</p></td>
<td><p>Ein Datenträger-e/a-Fehler ist aufgetreten.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidPath<br />
-1023</p></td>
<td><p>Ungültiger Dateipfad.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidSystemPath<br />
-1024</p></td>
<td><p>Es ist ein ungültiger Systempfad vorhanden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidLogDirectory<br />
-1025</p></td>
<td><p>Es ist ein ungültiges Protokoll Verzeichnis vorhanden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRecordTooBig<br />
-1026</p></td>
<td><p>Der Datensatz ist größer als die maximale Größe.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyOpenDatabases<br />
-1027</p></td>
<td><p>Es sind zu viele geöffnete Datenbanken vorhanden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidDatabase<br />
-1028</p></td>
<td><p>Dabei handelt es sich nicht um eine Datenbankdatei.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized<br />
-1029</p></td>
<td><p>Die Datenbank-Engine wurde nicht initialisiert.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errAlreadyInitialized<br />
-1030</p></td>
<td><p>Die Datenbank-Engine ist bereits initialisiert.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInitInProgress<br />
-1031</p></td>
<td><p>Die Datenbank-Engine wird initialisiert.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFileAccessDenied<br />
-1032</p></td>
<td><p>Auf die Datei kann nicht zugegriffen werden, da die Datei gesperrt ist oder verwendet wird.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBufferTooSmall<br />
-1038</p></td>
<td><p>Der Puffer ist zu klein.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyColumns<br />
-1040</p></td>
<td><p>Es sind zu viele Spalten definiert.</p></td>
</tr>
<tr class="even">
<td><p>JET_errContainerNotEmpty<br />
-1043</p></td>
<td><p>Der Container ist nicht leer.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidFilename<br />
-1044</p></td>
<td><p>Der Dateiname ist ungültig.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidBookmark<br />
-1045</p></td>
<td><p>Es ist ein ungültiges Lesezeichen vorhanden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnInUse<br />
-1046</p></td>
<td><p>Die verwendete Spalte befindet sich in einem Index.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidBufferSize<br />
-1047</p></td>
<td><p>Der Datenpuffer stimmt nicht mit der Spaltengröße identisch.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnNotUpdatable<br />
-1048</p></td>
<td><p>Der Spaltenwert kann nicht festgelegt werden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexInUse<br />
-1051</p></td>
<td><p>Der Index wird verwendet.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLinkNotSupported<br />
-1052</p></td>
<td><p>Die Link Unterstützung ist nicht verfügbar.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNullKeyDisallowed<br />
-1053</p></td>
<td><p>NULL-Schlüssel sind für einen Index nicht zulässig.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInTransaction<br />
-1054</p></td>
<td><p>Der Vorgang muss innerhalb einer Transaktion erfolgen.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyActiveUsers<br />
-1059</p></td>
<td><p>Es sind zu viele aktive Datenbankbenutzer vorhanden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidCountry<br />
-1061</p></td>
<td><p>Es ist ein ungültiger oder unbekannter Ländercode vorhanden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidLanguageId<br />
-1062</p></td>
<td><p>Es ist eine ungültige oder unbekannte Sprach-ID vorhanden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidCodePage<br />
-1063</p></td>
<td><p>Es ist eine ungültige oder unbekannte Codepage vorhanden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidLCMapStringFlags<br />
-1064</p></td>
<td><p>Es werden ungültige Flags für " <a href="/windows/win32/api/winnls/nf-winnls-lcmapstringa">LCMapString</a>" verwendet.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errVersionStoreEntryTooBig<br />
-1065</p></td>
<td><p>Es wurde versucht, einen Versionsspeicher Eintrag (RCE) zu erstellen, der größer als ein versionsbucket war.</p></td>
</tr>
<tr class="even">
<td><p>JET_errVersionStoreOutOfMemoryAndCleanupTimedOut<br />
-1066</p></td>
<td><p>Der Versionsspeicher weist nicht genügend Arbeitsspeicher auf, und der Bereinigungs Versuch konnte nicht durchgeführt werden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errVersionStoreOutOfMemory<br />
-1069</p></td>
<td><p>Der Versionsspeicher weist nicht genügend Arbeitsspeicher auf, und es wurde bereits versucht, eine Bereinigung auszuführen.)</p></td>
</tr>
<tr class="even">
<td><p>JET_errCannotIndex<br />
-1071</p></td>
<td><p>Die Spalten "hinterlegter" und "SLV" können nicht indiziert werden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRecordNotDeleted<br />
-1072</p></td>
<td><p>Der Datensatz wurde nicht gelöscht.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyMempoolEntries<br />
-1073</p></td>
<td><p>Es wurden zu viele mempool-Einträge angefordert.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfObjectIDs<br />
-1074</p></td>
<td><p>Die Datenbank befindet sich außerhalb der B +-Struktur-ObjectIDs, sodass eine Offline Defragmentierung ausgeführt werden muss, um freigegebene oder nicht verwendete ObjectIDs freizugeben.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfLongValueIDs<br />
-1075</p></td>
<td><p>Der lange Wert-ID-Leistungs Bewert hat den maximalen Wert erreicht. Eine Offline Defragmentierung muss ausgeführt werden, um freie oder nicht verwendete longvalueids freizugeben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfAutoincrementValues<br />
-1076</p></td>
<td><p>Der Wert für automatische Inkrement hat den maximalen Wert erreicht. Eine Offline Defragmentierung kann keine freien oder nicht genutzten automatischen Inkrement-Werte freigeben.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfDbtimeValues<br />
-1077</p></td>
<td><p>Der dbtime-Leistungswert hat den maximalen Wert erreicht. Eine Offline Defragmentierung muss ausgeführt werden, um freie oder nicht verwendete dbtime-Werte freizugeben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfSequentialIndexValues<br />
-1078</p></td>
<td><p>Ein sequenzieller Index Indikator hat den maximalen Wert erreicht. Eine Offline Defragmentierung muss ausgeführt werden, um freie oder nicht verwendete sequentialindex-Werte freizugeben.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRunningInOneInstanceMode<br />
-1080</p></td>
<td><p>Bei diesem multiinstanzaufruter ist der einzelinstanzmodus aktiviert.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRunningInMultiInstanceMode<br />
-1081</p></td>
<td><p>Bei diesem einzelinstanzrückruf ist der Modus für mehrere Instanzen aktiviert.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSystemParamsAlreadySet<br />
-1082</p></td>
<td><p>Die globalen Systemparameter wurden bereits festgelegt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSystemPathInUse<br />
-1083</p></td>
<td><p>Der Systempfad wird bereits von einer anderen Daten Bank Instanz verwendet.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogFilePathInUse<br />
-1084</p></td>
<td><p>Der Protokolldatei Pfad wird bereits von einer anderen Daten Bank Instanz verwendet.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTempPathInUse<br />
-1085</p></td>
<td><p>Der Pfad zur temporären Datenbank wird bereits von einer anderen Daten Bank Instanz verwendet.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceNameInUse<br />
-1086</p></td>
<td><p>Der Instanzname wird bereits verwendet.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable<br />
-1090</p></td>
<td><p>Diese Instanz kann nicht verwendet werden, da ein schwerwiegender Fehler aufgetreten ist.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseUnavailable<br />
-1091</p></td>
<td><p>Diese Datenbank kann nicht verwendet werden, weil ein schwerwiegender Fehler aufgetreten ist.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailableDueToFatalLogDiskFull<br />
-1092</p></td>
<td><p>Diese Instanz kann nicht verwendet werden, da beim Ausführen eines Vorgangs (z. b. einem Transaktionsrollback) ein Fehler aufgrund eines Protokoll Datenträgers aufgetreten ist, der einen Fehler nicht tolerieren konnte.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfSessions<br />
-1101</p></td>
<td><p>Die Datenbank ist nicht in der Sitzung.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errWriteConflict<br />
-1102</p></td>
<td><p>Fehler bei der Schreibsperre, weil eine ausstehende Schreibsperre vorhanden ist.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTransTooDeep<br />
-1103</p></td>
<td><p>Die Transaktionen sind zu tief geschachtelt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidSesid<br />
-1104</p></td>
<td><p>Es ist ein ungültiges Sitzungs handle vorhanden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errWriteConflictPrimaryIndex<br />
-1105</p></td>
<td><p>Es wurde versucht, einen nicht ausgeführtem primären Index zu aktualisieren.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInTransaction<br />
-1108</p></td>
<td><p>Der Vorgang ist innerhalb einer Transaktion nicht zulässig.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRollbackRequired<br />
-1109</p></td>
<td><p>Für die aktuelle Transaktion muss ein Rollback ausgeführt werden. Ein Commit kann nicht ausgeführt werden, und ein neuer kann nicht gestartet werden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTransReadOnly<br />
-1110</p></td>
<td><p>Eine schreibgeschützte Transaktion hat versucht, die Datenbank zu ändern.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionWriteConflict<br />
-1111</p></td>
<td><p>Es wurde versucht, denselben Datensatz durch zwei verschiedene Cursor in derselben Sitzung zu ersetzen.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRecordTooBigForBackwardCompatibility<br />
-1112</p></td>
<td><p>Der Datensatz wäre zu groß, wenn er in einem Datenbankformat aus einer früheren Version von Jet dargestellt wird.</p></td>
</tr>
<tr class="even">
<td><p>JET_errCannotMaterializeForwardOnlySort<br />
-1113</p></td>
<td><p>Die temporäre Tabelle konnte aufgrund von Parametern, die mit JET_bitTTForwardOnly in Konflikt stehen, nicht erstellt werden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSesidTableIdMismatch<br />
-1114</p></td>
<td><p>Das Sitzungs Handle kann nicht mit der Tabellen-ID verwendet werden, da es nicht zum Erstellen verwendet wurde.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidInstance<br />
-1115</p></td>
<td><p>Der Instanzhandle ist ungültig oder verweist auf eine Instanz, die heruntergefahren wurde.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errReadLostFlushVerifyFailure<br />
-1119</p></td>
<td><p>Auf der vom Datenträger gelesenen Datenbankseite wurde ein vorheriger Schreibvorgang auf der Seite nicht dargestellt. Verfügbar unter Windows 8 und höher für den-Client und Windows Server 2012 und höher für den-Server.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseDuplicate<br />
-1201</p></td>
<td><p>Die Datenbank ist bereits vorhanden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseInUse<br />
-1202</p></td>
<td><p>Die verwendete Datenbank.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseNotFound<br />
-1203</p></td>
<td><p>Diese Datenbank ist nicht vorhanden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseInvalidName<br />
-1204</p></td>
<td><p>Der Datenbankname ist ungültig.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseInvalidPages<br />
-1205</p></td>
<td><p>Es ist eine ungültige Anzahl von Seiten vorhanden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseCorrupted<br />
-1206</p></td>
<td><p>Es ist eine nicht-Datenbankdatei oder eine beschädigte Datenbank vorhanden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseLocked<br />
-1207</p></td>
<td><p>Die Datenbank ist exklusiv gesperrt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errCannotDisableVersioning<br />
-1208</p></td>
<td><p>Die Versionsverwaltung für diese Datenbank kann nicht deaktiviert werden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidDatabaseVersion<br />
-1209</p></td>
<td><p>Die Datenbank-Engine ist nicht mit der Datenbank kompatibel.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabase200Format<br />
-1210</p></td>
<td><p>Die Datenbank weist ein älteres Format (200) auf. Dieser Fehler wird von <a href="gg294068(v=exchg.10).md">jetinit</a> zurückgegeben, wenn <a href="gg269337(v=exchg.10).md">JET_paramCheckFormatWhenOpenFail</a> festgelegt ist. Nur Windows NT-Client.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabase400Format<br />
-1211</p></td>
<td><p>Die Datenbank weist ein älteres Format (400) auf. Dieser Fehler wird von <a href="gg294068(v=exchg.10).md">jetinit</a> zurückgegeben, wenn <a href="gg269337(v=exchg.10).md">JET_paramCheckFormatWhenOpenFail</a> festgelegt ist. Nur Windows NT-Client.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabase500Format<br />
-1212</p></td>
<td><p>Die Datenbank weist ein älteres Format (500) auf. Dieser Fehler wird von <a href="gg294068(v=exchg.10).md">jetinit</a> zurückgegeben, wenn <a href="gg269337(v=exchg.10).md">JET_paramCheckFormatWhenOpenFail</a> festgelegt ist. Nur Windows NT-Client.</p></td>
</tr>
<tr class="even">
<td><p>JET_errPageSizeMismatch<br />
-1213</p></td>
<td><p>Die Seitengröße der Datenbank stimmt nicht mit der Engine identisch.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyInstances<br />
-1214</p></td>
<td><p>Es können keine weiteren Datenbankinstanzen gestartet werden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseSharingViolation<br />
-1215</p></td>
<td><p>Diese Datenbank wird von einer anderen Daten Bank Instanz verwendet.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errAttachedDatabaseMismatch<br />
-1216</p></td>
<td><p>Am Anfang oder Ende der Wiederherstellung wurde eine ausstehende Daten Bank Anlage erkannt, die Datenbank ist jedoch nicht vorhanden oder entspricht nicht den Informationen zur Anlage.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseInvalidPath<br />
-1217</p></td>
<td><p>Der angegebene Pfad zur Datenbankdatei ist unzulässig.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseIdInUse<br />
-1218</p></td>
<td><p>Einer Datenbank wird eine ID zugewiesen, die bereits verwendet wird.</p></td>
</tr>
<tr class="even">
<td><p>JET_errForceDetachNotAllowed<br />
-1219</p></td>
<td><p>Das Erzwingen von Trenn Einheiten ist nur zulässig, nachdem der normale Trennvorgang aufgrund eines Fehlers beendet wurde.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errCatalogCorrupted<br />
-1220</p></td>
<td><p>Im Katalog wurde eine Beschädigung festgestellt.</p></td>
</tr>
<tr class="even">
<td><p>JET_errPartiallyAttachedDB<br />
-1221</p></td>
<td><p>Die Datenbank ist nur teilweise angefügt, und der Anfüge Vorgang kann nicht abgeschlossen werden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseSignInUse<br />
-1222</p></td>
<td><p>Die Datenbank mit der gleichen Signatur wird bereits verwendet.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseCorruptedNoRepair<br />
-1224</p></td>
<td><p>Die Datenbank ist beschädigt, aber eine Reparatur ist nicht zulässig.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidCreateDbVersion<br />
-1225</p></td>
<td><p>Die Datenbank-Engine hat versucht, einen CREATE DATABASE-Vorgang aus dem Transaktionsprotokoll wiederzugeben, konnte jedoch aufgrund einer inkompatiblen Version dieses Vorgangs nicht ausgeführt werden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTableLocked<br />
-1302</p></td>
<td><p>Die Tabelle ist exklusiv gesperrt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTableDuplicate<br />
-1303</p></td>
<td><p>Die Tabelle ist bereits vorhanden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTableInUse<br />
-1304</p></td>
<td><p>Die Tabelle wird verwendet und kann nicht gesperrt werden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errObjectNotFound<br />
-1305</p></td>
<td><p>Eine solche Tabelle oder ein solches Objekt ist nicht vorhanden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDensityInvalid<br />
-1307</p></td>
<td><p>Es ist eine ungültige Datei-oder Index Dichte vorhanden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTableNotEmpty<br />
-1308</p></td>
<td><p>Die Tabelle ist nicht leer.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidTableId<br />
-1310</p></td>
<td><p>Die Tabellen-ID ist ungültig.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyOpenTables<br />
-1311</p></td>
<td><p>Es können keine weiteren Tabellen geöffnet werden, auch nachdem die interne Bereinigungs Aufgabe ausgeführt wurde.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIllegalOperation<br />
-1312</p></td>
<td><p>Der Vorgang wird für die Tabelle nicht unterstützt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyOpenTablesAndCleanupTimedOut<br />
-1313</p></td>
<td><p>Es können keine weiteren Tabellen geöffnet werden, da der Cleanupversuch nicht durchgeführt werden konnte.</p></td>
</tr>
<tr class="even">
<td><p>JET_errObjectDuplicate<br />
-1314</p></td>
<td><p>Der Tabellen-oder Objektname wird verwendet.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidObject<br />
-1316</p></td>
<td><p>Das Objekt ist für den Vorgang ungültig.</p></td>
</tr>
<tr class="even">
<td><p>JET_errCannotDeleteTempTable<br />
-1317</p></td>
<td><p><a href="gg294087(v=exchg.10).md">Jetclosetable</a> muss anstelle von <a href="gg294128(v=exchg.10).md">jetdeletetable</a> verwendet werden, um eine temporäre Tabelle zu löschen.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errCannotDeleteSystemTable<br />
-1318</p></td>
<td><p>Es wurde ein unzulässiger Versuch unternommen, eine Systemtabelle zu löschen.</p></td>
</tr>
<tr class="even">
<td><p>JET_errCannotDeleteTemplateTable<br />
-1319</p></td>
<td><p>Es wurde ein unzulässiger Versuch unternommen, eine Vorlagen Tabelle zu löschen.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errExclusiveTableLockRequired<br />
-1322</p></td>
<td><p>Es muss eine exklusive Sperre für die Tabelle vorhanden sein.</p></td>
</tr>
<tr class="even">
<td><p>JET_errFixedDDL<br />
-1323</p></td>
<td><p>DDL-Vorgänge sind in dieser Tabelle nicht zulässig.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFixedInheritedDDL<br />
-1324</p></td>
<td><p>Für eine abgeleitete Tabelle sind DDL-Vorgänge für den geerbten Teil der DDL unzulässig.</p></td>
</tr>
<tr class="even">
<td><p>JET_errCannotNestDDL<br />
-1325</p></td>
<td><p>Das Schachteln der hierarchischen DDL wird derzeit nicht unterstützt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDDLNotInheritable<br />
-1326</p></td>
<td><p>Es wurde versucht, eine DDL von einer Tabelle zu erben, die nicht als Vorlagen Tabelle gekennzeichnet ist.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidSettings<br />
-1328</p></td>
<td><p>Die Systemparameter wurden nicht ordnungsgemäß festgelegt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService<br />
-1329</p></td>
<td><p>Der Client hat angefordert, dass der Dienst beendet wird.</p></td>
</tr>
<tr class="even">
<td><p>JET_errCannotAddFixedVarColumnToDerivedTable<br />
-1330</p></td>
<td><p>Die Vorlagen Tabelle wurde erstellt, wobei das nofixedvarcolumnsinderivedtables-Flag festgelegt wurde.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexCantBuild<br />
-1401</p></td>
<td><p>Der indexbuild ist fehlgeschlagen.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexHasPrimary<br />
-1402</p></td>
<td><p>Der primäre Index ist bereits definiert.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexDuplicate<br />
-1403</p></td>
<td><p>Der Index ist bereits definiert.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexNotFound<br />
-1404</p></td>
<td><p>Es ist kein solcher Index vorhanden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexMustStay<br />
-1405</p></td>
<td><p>Der gruppierte Index kann nicht gelöscht werden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexInvalidDef<br />
-1406</p></td>
<td><p>Die Index Definition ist ungültig.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidCreateIndex<br />
-1409</p></td>
<td><p>Die Index Beschreibung ist ungültig.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyOpenIndexes<br />
-1410</p></td>
<td><p>Die Datenbank weist keine Index Beschreibungs Blöcke auf.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errMultiValuedIndexViolation<br />
-1411</p></td>
<td><p>Für einen mehrwertigen Index wurden nicht eindeutige Index Schlüssel für den zwischen Daten Satz generiert.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexBuildCorrupted<br />
-1412</p></td>
<td><p>Ein sekundärer Index, der den primären Index korrekt widerspiegelt, konnte nicht erstellt werden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errPrimaryIndexCorrupted<br />
-1413</p></td>
<td><p>Der primäre Index ist beschädigt, und die Datenbank muss zerlegt werden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSecondaryIndexCorrupted<br />
-1414</p></td>
<td><p>Der sekundäre Index ist beschädigt, und die Datenbank muss zerlegt werden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidIndexId<br />
-1416</p></td>
<td><p>Die Index-ID ist ungültig.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesSecondaryIndexOnly<br />
-1430</p></td>
<td><p>Der Tupelindex kann nur für einen sekundären Index festgelegt werden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesTooManyColumns<br />
-1431</p></td>
<td><p>Die Index Definition für den Tupelindex enthält mehr Schlüssel Spalten, die von der Datenbank-Engine unterstützt werden können.</p>
<p><strong>Hinweis  </strong> Der JET_errIndexTuplesOneColumnOnly Fehler ist veraltet und wurde durch JET_errIndexTuplesTooManyColumns ersetzt.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesNonUniqueOnly<br />
-1432</p></td>
<td><p>Der Tupelindex muss ein nicht eindeutiger Index sein.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesTextBinaryColumnsOnly<br />
-1433</p></td>
<td><p>Eine tupelindexdefinition kann nur Schlüssel Spalten mit Text-oder Binär Spaltentypen enthalten.</p>
<p><strong>Hinweis  </strong> Der JET_errIndexTuplesTextColumnsOnly Fehler ist veraltet und wurde durch JET_errIndexTuplesTextBinaryColumnsOnly ersetzt.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesVarSegMacNotAllowed<br />
-1434</p></td>
<td><p>Der Tupelindex lässt das Festlegen von cbvarsegmac nicht zu.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesInvalidLimits<br />
-1435</p></td>
<td><p>Die minimale/maximale tupellänge oder die maximale Anzahl von Zeichen, die für einen Index angegeben sind, sind ungültig.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesCannotRetrieveFromIndex<br />
-1436</p></td>
<td><p><a href="gg269198(v=exchg.10).md">Jetretrievecolenn</a> kann nicht mit dem JET_bitRetrieveFromIndex Flag aufgerufen werden, wenn eine Spalte für einen Tupelindex abgerufen wird.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesKeyTooSmall<br />
-1437</p></td>
<td><p>Der angegebene Schlüssel entspricht nicht der minimalen tupellänge.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnLong<br />
-1501</p></td>
<td><p>Der Spaltenwert ist Long.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnNoChunk<br />
-1502</p></td>
<td><p>Es gibt keinen solchen Block in einem Long-Wert.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnDoesNotFit<br />
-1503</p></td>
<td><p>Das Feld passt nicht in den Datensatz.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNullInvalid<br />
-1504</p></td>
<td><p>NULL ist ungültig.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnIllegalNull<br />
JET_errNullInvalid</p></td>
<td><p>NULL ist ungültig. Dieser Fehler wird vom Daten Satz-Manager zurückgegeben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnIndexed-1505</p></td>
<td><p>Die Spalte ist indiziert und kann nicht gelöscht werden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnTooBig-1506</p></td>
<td><p>Die Feldlänge ist größer als die maximal zulässige Länge.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnNotFound-1507</p></td>
<td><p>Diese Spalte ist nicht vorhanden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnDuplicate-1508</p></td>
<td><p>Dieses Feld ist bereits definiert.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errMultiValuedColumnMustBeTagged-1509</p></td>
<td><p>Es wurde versucht, eine mehrwertige Spalte zu erstellen, aber die Spalte wurde nicht markiert.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnRedundant-1510</p></td>
<td><p>Es gab eine zweite Spalte mit automatischer Inkrement oder Version.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidColumnType-1511</p></td>
<td><p>Der Spaltendatentyp ist ungültig.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTaggedNotNULL-1514</p></td>
<td><p>Es sind keine markierten Spalten ungleich NULL vorhanden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoCurrentIndex-1515</p></td>
<td><p>Die Datenbank ist ungültig, da Sie keinen aktuellen Index enthält.</p></td>
</tr>
<tr class="even">
<td><p>JET_errKeyIsMade-1516</p></td>
<td><p>Der Schlüssel wird vollständig erstellt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBadColumnId-1517</p></td>
<td><p>Die Spalten-ID ist falsch.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBadItagSequence-1518</p></td>
<td><p>Für die markierte Spalte ist eine ungültige itagsequence vorhanden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnInRelationship-1519</p></td>
<td><p>Eine Spalte kann nicht gelöscht werden, da Sie Teil einer Beziehung ist.</p></td>
</tr>
<tr class="even">
<td><p>JET_errCannotBeTagged-1521</p></td>
<td><p>Das automatische Inkrement und die Version können nicht markiert werden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDefaultValueTooBig-1524</p></td>
<td><p>Der Standardwert überschreitet die maximale Größe.</p></td>
</tr>
<tr class="even">
<td><p>JET_errMultiValuedDuplicate-1525</p></td>
<td><p>Ein doppelter Wert wurde für eine eindeutige mehrwertige Spalte erkannt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLVCorrupted-1526</p></td>
<td><p>In einer lange Wert Struktur ist eine Beschädigung aufgetreten.</p></td>
</tr>
<tr class="even">
<td><p>JET_errMultiValuedDuplicateAfterTruncation-1528</p></td>
<td><p>Ein doppelter Wert wurde für eine eindeutige mehrwertige Spalte erkannt, nachdem die Daten normalisiert wurden, und Sie normalisiert die Daten vor dem Vergleich.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDerivedColumnCorruption-1529</p></td>
<td><p>In der abgeleiteten Tabelle ist eine ungültige Spalte vorhanden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidPlaceholderColumn-1530</p></td>
<td><p>Es wurde versucht, eine Spalte in einen primären Index Platzhalter zu konvertieren, aber die Spalte erfüllt nicht die erforderlichen Kriterien.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRecordNotFound-1601</p></td>
<td><p>Der Schlüssel wurde nicht gefunden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRecordNoCopy-1602</p></td>
<td><p>Es ist kein Arbeits Puffer vorhanden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoCurrentRecord-1603</p></td>
<td><p>Es ist kein aktueller Datensatz vorhanden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRecordPrimaryChanged-1604</p></td>
<td><p>Der Primärschlüssel kann nicht geändert werden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errKeyDuplicate-1605</p></td>
<td><p>Es ist ein ungültiger doppelter Schlüssel vorhanden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errAlreadyPrepared-1607</p></td>
<td><p>Es wurde versucht, einen Datensatz zu aktualisieren, während bereits eine Daten Satz Aktualisierung durchgeführt wurde.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errKeyNotMade-1608</p></td>
<td><p>Es wurde kein " <a href="gg269329(v=exchg.10).md">jetmakekey</a>" aufgerufen.</p></td>
</tr>
<tr class="even">
<td><p>JET_errUpdateNotPrepared-1609</p></td>
<td><p>Es wurde kein " <a href="gg269339(v=exchg.10).md">jetprepareupdate</a>" aufgerufen.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDataHasChanged-1611</p></td>
<td><p>Die Daten wurden geändert, und der Vorgang wurde abgebrochen.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLanguageNotSupported-1619</p></td>
<td><p>Die ausgewählte Sprache wird von dieser Windows-Installation nicht unterstützt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManySorts-1701</p></td>
<td><p>Es sind zu viele Sortier Prozesse vorhanden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidOnSort-1702</p></td>
<td><p>Beim Sortieren ist ein ungültiger Vorgang aufgetreten.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTempFileOpenError-1803</p></td>
<td><p>Die temporäre Datei konnte nicht geöffnet werden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyAttachedDatabases-1805</p></td>
<td><p>Zu viele Datenbanken sind geöffnet.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDiskFull-1808</p></td>
<td><p>Auf dem Datenträger ist kein Speicherplatz mehr vorhanden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errPermissionDenied-1809</p></td>
<td><p>Die Berechtigung wurde verweigert.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFileNotFound-1811</p></td>
<td><p>Die Datei wurde nicht gefunden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errFileInvalidType-1812</p></td>
<td><p>Der Dateityp ist ungültig.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errAfterInitialization-1850</p></td>
<td><p>Eine Wiederherstellung kann nach der Initialisierung nicht gestartet werden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogCorrupted-1852</p></td>
<td><p>Die Protokolle konnten nicht interpretiert werden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidOperation-1906</p></td>
<td><p>Der Vorgang ist ungültig.</p></td>
</tr>
<tr class="even">
<td><p>JET_errAccessDenied-1907</p></td>
<td><p>Zugriff verweigert.“</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManySplits-1909</p></td>
<td><p>Eine unendliche Teilung.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation-1910</p></td>
<td><p>Mehrere Threads verwenden dieselbe Sitzung.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errEntryPointNotFound-1911</p></td>
<td><p>Ein Einstiegspunkt in einer erforderlichen dll konnte nicht gefunden werden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionContextAlreadySet-1912</p></td>
<td><p>Für die angegebene Sitzung ist bereits ein Sitzungs Kontext festgelegt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionContextNotSetByThisThread-1913</p></td>
<td><p>Es wurde versucht, den Sitzungs Kontext zurückzusetzen, aber der aktuelle Thread war nicht der ursprüngliche Thread, der den Sitzungs Kontext festgelegt hat.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionInUse-1914</p></td>
<td><p>Es wurde versucht, die derzeit verwendete Sitzung zu beenden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRecordFormatConversionFailed-1915</p></td>
<td><p>Interner Fehler bei der Konvertierung von dynamischen Daten Satz Formaten.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOneDatabasePerSession-1916</p></td>
<td><p>Pro Sitzung ist nur eine geöffnete Benutzerdatenbank zulässig (wie durch Festlegen des <a href="gg269337(v=exchg.10).md">JET_paramOneDatabasePerSession</a> Flags während der Erstellung der Datenbank angegeben).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRollbackError-1917</p></td>
<td><p>Fehler beim Rollback.</p></td>
</tr>
<tr class="even">
<td><p>JET_errCallbackFailed-2101</p></td>
<td><p>Fehler beim Rückruf Funktionsaufrufs.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errCallbackNotResolved-2102</p></td>
<td><p>Eine Rückruffunktion wurde nicht gefunden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOSSnapshotInvalidSequence-2401</p></td>
<td><p>Die schattenkopieapi des Betriebssystems wurde in einer ungültigen Sequenz verwendet.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOSSnapshotTimeOut-2402</p></td>
<td><p>Die Schatten Kopie des Betriebssystems wurde mit einem Timeout beendet.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOSSnapshotNotAllowed-2403</p></td>
<td><p>Die Schatten Kopie des Betriebssystems ist nicht zulässig, da eine Sicherung oder Wiederherstellung in ausgeführt wird.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOSSnapshotInvalidSnapId-2404</p></td>
<td><p>Der Vorgang ist fehlgeschlagen, weil das angegebene Schatten Kopie-Handle des Betriebssystems ungültig war.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLSCallbackNotSpecified-3000</p></td>
<td><p>Es wurde versucht, den lokalen Speicher zu verwenden, ohne dass eine Rückruffunktion angegeben wurde.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLSAlreadySet-3001</p></td>
<td><p>Es wurde versucht, den lokalen Speicher für ein Objekt festzulegen, das bereits festgelegt wurde.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLSNotSet-3002</p></td>
<td><p>Es wurde versucht, den lokalen Speicher von einem Objekt abzurufen, für das es nicht festgelegt wurde.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFileIOSparse-4000</p></td>
<td><p>Bei einem e/a-Vorgang ist ein Fehler aufgetreten, da versucht wurde, einen nicht zugeordneten Bereich einer Datei zu haben.</p></td>
</tr>
<tr class="even">
<td><p>JET_errFileIOBeyondEOF-4001</p></td>
<td><p>Ein Lesevorgang wurde für einen Speicherort außerhalb der EOF-Anweisung ausgegeben (die Datei wird von den Schreibvorgängen erweitert).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFileIOAbort-4002</p></td>
<td><p>Dieses Flag weist den JET_ABORTRETRYFAILCALLBACK Aufrufer an, den angegebenen e/a-Vorgang abzubrechen.</p></td>
</tr>
<tr class="even">
<td><p>JET_errFileIORetry-4003</p></td>
<td><p>Dieses Flag weist den JET_ABORTRETRYFAILCALLBACK Aufrufer an, den angegebenen e/a-Vorgang zu wiederholen.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFileIOFail-4004</p></td>
<td><p>Dieses Flag weist den JET_ABORTRETRYFAILCALLBACK Aufrufer an, den angegebenen e/a-Fehler zu verursachen.</p></td>
</tr>
<tr class="even">
<td><p>JET_errFileCompressed-4005</p></td>
<td><p>Der Lese-/Schreibzugriff wird für komprimierte Dateien nicht unterstützt.</p></td>
</tr>
</tbody>
</table>


### <a name="remarks"></a>Bemerkungen

Im Allgemeinen sollte ein Wert, der größer als 0 (null) ist, als Warnung interpretiert werden. der Wert 0 (null) sollte als Success interpretiert werden, und ein Wert, der kleiner als 0 (null) ist, sollte als Fehler interpretiert werden. Keine anderen Muster in diesen Werten, z. b. Wertebereiche, sollten von einer Anwendung abhängig sein.

### <a name="requirements"></a>Anforderungen

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
</tbody>
</table>


### <a name="see-also"></a>Weitere Informationen

[Fehler Behandlungsparameter](./error-handling-parameters.md)  
[Erweiterbare Speicher-Engine-Fehler](./extensible-storage-engine-errors.md)  
[Extensible Storage Engine-Dateien](./extensible-storage-engine-files.md)
