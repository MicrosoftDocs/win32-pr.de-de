---
description: Beschreibt die in der Header Datei "Winerror. h" definierten Fehlercodes 6000-8199 und ist für Entwickler bestimmt.
ms.assetid: eaaf9f65-e8ff-4e54-90a9-04252cdd773a
title: System Fehler Codes (6000-8199) (Winerror. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 0660009411224673481e9b65bcb62d7b194ab71f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861376"
---
# <a name="system-error-codes-6000-8199"></a>System Fehler Codes (6000-8199)

> [!NOTE]
> Diese Informationen sind für Entwickler gedacht, die Systemfehler Debuggen. Bei anderen Fehlern, wie z. b. Problemen mit Windows Update, finden Sie eine Liste der Ressourcen auf der Seite [Fehlercodes](system-error-codes.md) .

In der folgenden Liste werden die [Systemfehler Codes](system-error-codes.md) (Fehler 6000 bis 8199) beschrieben. Sie werden von der [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) -Funktion zurückgegeben, wenn viele Funktionen fehlschlagen. Um den Beschreibungstext für den Fehler in Ihrer Anwendung abzurufen, verwenden Sie die [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) -Funktion mit dem Flag " **Format \_ Message \_ from \_ System** ".

<dl> <dt>

<span id="ERROR_ENCRYPTION_FAILED"></span><span id="error_encryption_failed"></span>**Fehler beim \_ verschlüsseln. \_**
</dt> <dd> <dl> <dt>

6000 (0x1770)
</dt> <dt>



Die angegebene Datei konnte nicht verschlüsselt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DECRYPTION_FAILED"></span><span id="error_decryption_failed"></span>**Fehler beim \_ entschlüsseln \_ .**
</dt> <dd> <dl> <dt>

6001 (0x1771)
</dt> <dt>



Die angegebene Datei konnte nicht entschlüsselt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_ENCRYPTED"></span><span id="error_file_encrypted"></span>**Fehler \_ Datei \_ verschlüsselt**
</dt> <dd> <dl> <dt>

6002 (0x1772)
</dt> <dt>



Die angegebene Datei ist verschlüsselt, und der Benutzer ist nicht in der Lage, Sie zu entschlüsseln.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_RECOVERY_POLICY"></span><span id="error_no_recovery_policy"></span>**Fehler \_ keine \_ Wiederherstellungs \_ Richtlinie**
</dt> <dd> <dl> <dt>

6003 (0x1773)
</dt> <dt>



Für dieses System ist keine gültige Verschlüsselungs Wiederherstellungs Richtlinie konfiguriert.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_EFS"></span><span id="error_no_efs"></span>**Fehler " \_ keine \_ EFS"**
</dt> <dd> <dl> <dt>

6004 (0x1774)
</dt> <dt>



Der erforderliche Verschlüsselungs Treiber ist für dieses System nicht geladen.


</dt> </dl> </dd> <dt>

<span id="ERROR_WRONG_EFS"></span><span id="error_wrong_efs"></span>**\_falscher Fehler \_ EFS**
</dt> <dd> <dl> <dt>

6005 (0x1775)
</dt> <dt>



Die Datei wurde mit einem anderen Verschlüsselungs Treiber verschlüsselt, als gerade geladen wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_USER_KEYS"></span><span id="error_no_user_keys"></span>**Fehler \_ keine \_ Benutzer \_ Schlüssel**
</dt> <dd> <dl> <dt>

6006 (0x1776)
</dt> <dt>



Für den Benutzer sind keine EFS-Schlüssel definiert.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_NOT_ENCRYPTED"></span><span id="error_file_not_encrypted"></span>**Fehler \_ Datei \_ nicht \_ verschlüsselt**
</dt> <dd> <dl> <dt>

6007 (0x1777)
</dt> <dt>



Die angegebene Datei ist nicht verschlüsselt.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_EXPORT_FORMAT"></span><span id="error_not_export_format"></span>**Fehler \_ beim \_ Exportieren des \_ Formats.**
</dt> <dd> <dl> <dt>

6008 (0x1778)
</dt> <dt>



Die angegebene Datei weist nicht das definierte EFS-Exportformat auf.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_READ_ONLY"></span><span id="error_file_read_only"></span>**Fehler \_ Datei schreibgeschützt \_ \_**
</dt> <dd> <dl> <dt>

6009 (0x1779)
</dt> <dt>



Die angegebene Datei ist schreibgeschützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_DIR_EFS_DISALLOWED"></span><span id="error_dir_efs_disallowed"></span>**Fehler Verzeichnis- \_ \_ EFS nicht \_ zulässig**
</dt> <dd> <dl> <dt>

6010 (0x177a)
</dt> <dt>



Das Verzeichnis wurde für die Verschlüsselung deaktiviert.


</dt> </dl> </dd> <dt>

<span id="ERROR_EFS_SERVER_NOT_TRUSTED"></span><span id="error_efs_server_not_trusted"></span>**Fehler \_ EFS- \_ Server \_ nicht \_ vertrauenswürdig**
</dt> <dd> <dl> <dt>

6011 (0x177b)
</dt> <dt>



Der Server ist für den Remote Verschlüsselungs Vorgang nicht vertrauenswürdig.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_RECOVERY_POLICY"></span><span id="error_bad_recovery_policy"></span>**fehlerhafter \_ \_ Wiederherstellungs \_ Richtlinie**
</dt> <dd> <dl> <dt>

6012 (0x177c)
</dt> <dt>



Für dieses System konfigurierte Wiederherstellungs Richtlinie enthält ein ungültiges Wiederherstellungs Zertifikat.


</dt> </dl> </dd> <dt>

<span id="ERROR_EFS_ALG_BLOB_TOO_BIG"></span><span id="error_efs_alg_blob_too_big"></span>**Fehler \_ EFS \_ ALG \_ BLOB \_ zu \_ groß**
</dt> <dd> <dl> <dt>

6013 (0x177d)
</dt> <dt>



Der Verschlüsselungsalgorithmus, der in der Quelldatei verwendet wird, benötigt einen größeren Schlüsselpuffer als der in der Zieldatei.


</dt> </dl> </dd> <dt>

<span id="ERROR_VOLUME_NOT_SUPPORT_EFS"></span><span id="error_volume_not_support_efs"></span>**Fehler \_ Volume \_ \_ unterstützt \_ EFS nicht**
</dt> <dd> <dl> <dt>

6014 (0x177e)
</dt> <dt>



Die Datenträger Partition unterstützt keine Dateiverschlüsselung.


</dt> </dl> </dd> <dt>

<span id="ERROR_EFS_DISABLED"></span><span id="error_efs_disabled"></span>**Fehler \_ EFS \_ deaktiviert**
</dt> <dd> <dl> <dt>

6015 (0x177f)
</dt> <dt>



Dieser Computer ist für die Dateiverschlüsselung deaktiviert.


</dt> </dl> </dd> <dt>

<span id="ERROR_EFS_VERSION_NOT_SUPPORT"></span><span id="error_efs_version_not_support"></span>**Fehler \_ EFS- \_ Version wird \_ nicht \_ unterstützt**
</dt> <dd> <dl> <dt>

6016 (0x1780)
</dt> <dt>



Ein neueres System ist erforderlich, um diese verschlüsselte Datei zu entschlüsseln.


</dt> </dl> </dd> <dt>

<span id="ERROR_CS_ENCRYPTION_INVALID_SERVER_RESPONSE"></span><span id="error_cs_encryption_invalid_server_response"></span>**Fehler bei \_ CS- \_ Verschlüsselung \_ ungültige \_ Server \_ Antwort.**
</dt> <dd> <dl> <dt>

6017 (0x1781)
</dt> <dt>



Der Remote Server hat eine ungültige Antwort für eine Datei gesendet, die mit der Client seitigen Verschlüsselung geöffnet wird.


</dt> </dl> </dd> <dt>

<span id="ERROR_CS_ENCRYPTION_UNSUPPORTED_SERVER"></span><span id="error_cs_encryption_unsupported_server"></span>**Fehler bei \_ CS- \_ Verschlüsselung \_ nicht unterstützter \_ Server**
</dt> <dd> <dl> <dt>

6018 (0x1782)
</dt> <dt>



Die Client seitige Verschlüsselung wird vom Remote Server nicht unterstützt, obwohl Sie von der Anwendung unterstützt wird.


</dt> </dl> </dd> <dt>

<span id="ERROR_CS_ENCRYPTION_EXISTING_ENCRYPTED_FILE"></span><span id="error_cs_encryption_existing_encrypted_file"></span>**Fehler- \_ CS- \_ Verschlüsselung \_ vorhanden \_ verschlüsselte \_ Datei**
</dt> <dd> <dl> <dt>

6019 (0x1783)
</dt> <dt>



Die Datei ist verschlüsselt und sollte im Client seitigen Verschlüsselungs Modus geöffnet werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CS_ENCRYPTION_NEW_ENCRYPTED_FILE"></span><span id="error_cs_encryption_new_encrypted_file"></span>**Fehler bei \_ CS- \_ Verschlüsselung \_ neue \_ verschlüsselte \_ Datei**
</dt> <dd> <dl> <dt>

6020 (0x1784)
</dt> <dt>



Eine neue verschlüsselte Datei wird erstellt, und ein $EFS muss angegeben werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CS_ENCRYPTION_FILE_NOT_CSE"></span><span id="error_cs_encryption_file_not_cse"></span>**Fehler- \_ CS- \_ Verschlüsselungs \_ Datei \_ nicht \_ CSE**
</dt> <dd> <dl> <dt>

6021 (0x1785)
</dt> <dt>



Der SMB-Client hat eine Client seitige Erweiterung für eine nicht-CSE-Datei angefordert.


</dt> </dl> </dd> <dt>

<span id="ERROR_ENCRYPTION_POLICY_DENIES_OPERATION"></span><span id="error_encryption_policy_denies_operation"></span>**Fehler \_ Verschlüsselungs \_ Richtlinie \_ verweigert \_ Vorgang**
</dt> <dd> <dl> <dt>

6022 (0x1786)
</dt> <dt>



Der angeforderte Vorgang wurde durch die Richtlinie blockiert. Wenden Sie sich an Ihren Systemadministrator, um weitere Informationen zu erhalten.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_BROWSER_SERVERS_FOUND"></span><span id="error_no_browser_servers_found"></span>**Fehler \_ keine \_ Browser \_ Server \_ gefunden.**
</dt> <dd> <dl> <dt>

6118 (0x17e6)
</dt> <dt>



Die Liste der Server für diese Arbeitsgruppe ist zurzeit nicht verfügbar.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_SERVICE_NOT_LOCALSYSTEM"></span><span id="sched_e_service_not_localsystem"></span>**sched \_ E \_ Dienst \_ nicht \_ LocalSystem**
</dt> <dd> <dl> <dt>

6200 (0x1838)
</dt> <dt>



Der Taskplaner-Dienst muss so konfiguriert werden, dass er im System Konto ausgeführt wird, damit er ordnungsgemäß funktioniert. Einzelne Tasks können so konfiguriert werden, dass Sie in anderen Konten ausgeführt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_SECTOR_INVALID"></span><span id="error_log_sector_invalid"></span>**Fehler \_ Protokoll \_ Sektor \_ ungültig**
</dt> <dd> <dl> <dt>

6600 (0x19c8)
</dt> <dt>



Der Protokolldienst hat einen ungültigen Protokoll Sektor gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_SECTOR_PARITY_INVALID"></span><span id="error_log_sector_parity_invalid"></span>**\_sektorparität des Fehler Protokolls \_ \_ \_ ungültig**
</dt> <dd> <dl> <dt>

6601 (0x19c9)
</dt> <dt>



Protokolldienst hat einen Protokoll Sektor mit ungültiger Block Parität gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_SECTOR_REMAPPED"></span><span id="error_log_sector_remapped"></span>**Fehler \_ Protokoll \_ Sektor neu zugeordnet \_**
</dt> <dd> <dl> <dt>

6602 (0x19ca)
</dt> <dt>



Der Protokolldienst hat einen neu zugeordnete Protokoll Sektor gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_BLOCK_INCOMPLETE"></span><span id="error_log_block_incomplete"></span>**Fehler \_ Protokoll \_ Block \_ unvollständig**
</dt> <dd> <dl> <dt>

6603 (0x19cb)
</dt> <dt>



Der Protokolldienst hat einen partiellen oder unvollständigen Protokoll Block gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_INVALID_RANGE"></span><span id="error_log_invalid_range"></span>**\_ \_ Ungültiger Bereich im Fehlerprotokoll. \_**
</dt> <dd> <dl> <dt>

6604 (0x19cc)
</dt> <dt>



Der Protokolldienst hat versucht, auf Daten außerhalb des aktiven Protokoll Bereichs zuzugreifen.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_BLOCKS_EXHAUSTED"></span><span id="error_log_blocks_exhausted"></span>**Fehler \_ Protokoll \_ Blöcke \_ aufgebraucht**
</dt> <dd> <dl> <dt>

6605 (0x19cd)
</dt> <dt>



Protokolldienst-Benutzer Marshalling Puffer sind erschöpft.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_READ_CONTEXT_INVALID"></span><span id="error_log_read_context_invalid"></span>**Fehler \_ Protokoll- \_ Lese \_ Kontext \_ ungültig**
</dt> <dd> <dl> <dt>

6606 (0x19ce)
</dt> <dt>



Der Protokolldienst hat versucht, einen Lesevorgang aus einem Marshalling Bereich mit einem ungültigen Lese Kontext durchführen.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_RESTART_INVALID"></span><span id="error_log_restart_invalid"></span>**Fehler \_ Protokoll- \_ Neustart \_ ungültig**
</dt> <dd> <dl> <dt>

6607 (0x19cf)
</dt> <dt>



Der Protokolldienst hat einen ungültigen Protokoll Neustart Bereich gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_BLOCK_VERSION"></span><span id="error_log_block_version"></span>**Version des Fehler \_ Protokoll \_ Blocks \_**
</dt> <dd> <dl> <dt>

6608 (0x19d0)
</dt> <dt>



Der Protokolldienst hat eine ungültige Protokoll Block Version gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_BLOCK_INVALID"></span><span id="error_log_block_invalid"></span>**der Fehler \_ Protokoll \_ Block ist \_ ungültig.**
</dt> <dd> <dl> <dt>

6609 (0x19d1)
</dt> <dt>



Der Protokolldienst hat einen ungültigen Protokoll Block gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_READ_MODE_INVALID"></span><span id="error_log_read_mode_invalid"></span>**Fehler \_ Protokoll \_ - \_ Lesemodus \_ ungültig**
</dt> <dd> <dl> <dt>

6610 (0x19d2)
</dt> <dt>



Der Protokolldienst hat versucht, das Protokoll mit einem ungültigen Lesemodus zu lesen.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_NO_RESTART"></span><span id="error_log_no_restart"></span>**Fehler \_ Protokoll \_ kein \_ Neustart**
</dt> <dd> <dl> <dt>

6611 (0x19d3)
</dt> <dt>



Protokolldienst hat einen Protokolldaten Strom ohne Neustart Bereich gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_METADATA_CORRUPT"></span><span id="error_log_metadata_corrupt"></span>**Fehler \_ Protokoll \_ Metadaten sind \_ beschädigt.**
</dt> <dd> <dl> <dt>

6612 (0x19d4)
</dt> <dt>



Protokolldienst hat eine beschädigte Metadatendatei gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_METADATA_INVALID"></span><span id="error_log_metadata_invalid"></span>**Fehler \_ Protokoll \_ Metadaten sind \_ ungültig.**
</dt> <dd> <dl> <dt>

6613 (0x19d5)
</dt> <dt>



Der Protokolldienst hat eine Metadatendatei gefunden, die nicht vom Protokolldatei System erstellt werden konnte.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_METADATA_INCONSISTENT"></span><span id="error_log_metadata_inconsistent"></span>**Fehler \_ Protokoll \_ Metadaten \_ inkonsistent**
</dt> <dd> <dl> <dt>

6614 (0x19d6)
</dt> <dt>



Der Protokolldienst hat eine Metadatendatei mit inkonsistenten Daten gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_RESERVATION_INVALID"></span><span id="error_log_reservation_invalid"></span>**Fehler \_ Protokoll \_ Reservierung \_ ungültig**
</dt> <dd> <dl> <dt>

6615 (0x19d7)
</dt> <dt>



Der Protokolldienst hat versucht, den Reservierungsbereich zu löschen oder zu verwerfen.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CANT_DELETE"></span><span id="error_log_cant_delete"></span>**Fehler \_ Protokoll \_ nicht \_ Löschen**
</dt> <dd> <dl> <dt>

6616 (0x19d8)
</dt> <dt>



Der Protokolldienst kann die Protokolldatei oder den Dateisystem Container nicht löschen.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CONTAINER_LIMIT_EXCEEDED"></span><span id="error_log_container_limit_exceeded"></span>**Fehler \_ Protokoll- \_ Container \_ Limit \_ überschritten**
</dt> <dd> <dl> <dt>

6617 (0x19d9)
</dt> <dt>



Der Protokolldienst hat die maximal zulässige Anzahl von Containern erreicht, die einer Protokolldatei zugeordnet sind.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_START_OF_LOG"></span><span id="error_log_start_of_log"></span>**\_ \_ \_ Protokoll Anfang des \_ Fehler Protokolls**
</dt> <dd> <dl> <dt>

6618 (0x19da)
</dt> <dt>



Der Protokolldienst hat versucht, einen Rückstand nach dem Beginn des Protokolls zu lesen oder zu schreiben.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_POLICY_ALREADY_INSTALLED"></span><span id="error_log_policy_already_installed"></span>**die Fehler \_ Protokoll \_ Richtlinie ist \_ bereits \_ installiert.**
</dt> <dd> <dl> <dt>

6619 (0x19db)
</dt> <dt>



Die Protokoll Richtlinie konnte nicht installiert werden, da bereits eine Richtlinie desselben Typs vorhanden ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_POLICY_NOT_INSTALLED"></span><span id="error_log_policy_not_installed"></span>**die Fehler \_ Protokoll \_ Richtlinie ist \_ nicht \_ installiert.**
</dt> <dd> <dl> <dt>

6620 (0x19dc)
</dt> <dt>



Die betreffende Protokoll Richtlinie wurde zum Zeitpunkt der Anforderung nicht installiert.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_POLICY_INVALID"></span><span id="error_log_policy_invalid"></span>**die Fehler \_ Protokoll \_ Richtlinie ist \_ ungültig.**
</dt> <dd> <dl> <dt>

6621 (0x19dd)
</dt> <dt>



Der installierte Satz von Richtlinien für das Protokoll ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_POLICY_CONFLICT"></span><span id="error_log_policy_conflict"></span>**Fehler \_ Protokoll- \_ Richtlinien \_ Konflikt**
</dt> <dd> <dl> <dt>

6622 (0x19de)
</dt> <dt>



Eine Richtlinie für das betreffende Protokoll hat verhindert, dass der Vorgang abgeschlossen wird.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_PINNED_ARCHIVE_TAIL"></span><span id="error_log_pinned_archive_tail"></span>**Fehler \_ Protokoll- \_ fixierte \_ Archiv \_ Ende**
</dt> <dd> <dl> <dt>

6623 (0x19df)
</dt> <dt>



Der Protokoll Speicher kann nicht freigegeben werden, da das Protokoll durch das Archiv Ende fixiert wird.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_RECORD_NONEXISTENT"></span><span id="error_log_record_nonexistent"></span>**Fehler \_ Protokoll \_ Daten Satz \_ nicht vorhanden**
</dt> <dd> <dl> <dt>

6624 (0x19e0)
</dt> <dt>



Der Protokolldaten Satz ist kein Datensatz in der Protokolldatei.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_RECORDS_RESERVED_INVALID"></span><span id="error_log_records_reserved_invalid"></span>**\_ \_ ungültige Fehlerprotokoll Datensätze \_ \_**
</dt> <dd> <dl> <dt>

6625 (0x19e1)
</dt> <dt>



Die Anzahl der reservierten Protokolldaten Sätze oder die Anpassung der Anzahl der reservierten Protokolldaten Sätze ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_SPACE_RESERVED_INVALID"></span><span id="error_log_space_reserved_invalid"></span>**\_ \_ Ungültiger Fehlerprotokoll Speicher. \_ \_**
</dt> <dd> <dl> <dt>

6626 (0x19e2)
</dt> <dt>



Der reservierte Protokoll Speicher oder die Anpassung des Protokoll Speicherplatzes ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_TAIL_INVALID"></span><span id="error_log_tail_invalid"></span>**Fehler \_ Protokoll \_ Ende \_ ungültig**
</dt> <dd> <dl> <dt>

6627 (0x19e3)
</dt> <dt>



Ein neues oder vorhandenes Archiv Ende oder eine Basis des aktiven Protokolls ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_FULL"></span><span id="error_log_full"></span>**Fehler \_ Protokoll \_ voll**
</dt> <dd> <dl> <dt>

6628 (0x19e4)
</dt> <dt>



Der Protokoll Speicher ist erschöpft.


</dt> </dl> </dd> <dt>

<span id="ERROR_COULD_NOT_RESIZE_LOG"></span><span id="error_could_not_resize_log"></span>**Fehler \_ beim \_ Ändern der Größe des \_ \_ Protokolls.**
</dt> <dd> <dl> <dt>

6629 (0x19e5)
</dt> <dt>



Das Protokoll konnte nicht auf die angeforderte Größe festgelegt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_MULTIPLEXED"></span><span id="error_log_multiplexed"></span>**Fehler \_ Protokoll \_ multiplexed**
</dt> <dd> <dl> <dt>

6630 (0x19e6)
</dt> <dt>



Das Protokoll ist multiplext, es sind keine direkten Schreibvorgänge in das physische Protokoll zulässig.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_DEDICATED"></span><span id="error_log_dedicated"></span>**Fehler \_ Protokoll \_ dediziert**
</dt> <dd> <dl> <dt>

6631 (0x19e7)
</dt> <dt>



Der Vorgang ist fehlgeschlagen, da es sich um ein dediziertes Protokoll handelt.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_ARCHIVE_NOT_IN_PROGRESS"></span><span id="error_log_archive_not_in_progress"></span>**Fehler \_ Protokoll \_ Archiv \_ wird \_ nicht \_ ausgeführt**
</dt> <dd> <dl> <dt>

6632 (0x19e8)
</dt> <dt>



Für den Vorgang ist ein Archiv Kontext erforderlich.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_ARCHIVE_IN_PROGRESS"></span><span id="error_log_archive_in_progress"></span>**Fehler \_ Protokoll \_ Archiv \_ wird \_ ausgeführt**
</dt> <dd> <dl> <dt>

6633 (0x19e9)
</dt> <dt>



Die Protokoll Archivierung wird ausgeführt.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_EPHEMERAL"></span><span id="error_log_ephemeral"></span>**\_ \_ kurzlebige Fehlerprotokoll**
</dt> <dd> <dl> <dt>

6634 (0x19ea)
</dt> <dt>



Der Vorgang erfordert ein nicht kurzlebiges Protokoll, aber das Protokoll ist kurzlebig.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_NOT_ENOUGH_CONTAINERS"></span><span id="error_log_not_enough_containers"></span>**Fehler \_ Protokoll \_ nicht \_ genügend \_ Container**
</dt> <dd> <dl> <dt>

6635 (0x19eb)
</dt> <dt>



Das Protokoll muss mindestens zwei Container aufweisen, bevor es gelesen oder in das Protokoll geschrieben werden kann.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CLIENT_ALREADY_REGISTERED"></span><span id="error_log_client_already_registered"></span>**der Fehler \_ Protokoll \_ Client wurde \_ bereits \_ registriert.**
</dt> <dd> <dl> <dt>

6636 (0x19ec)
</dt> <dt>



Ein Protokoll Client wurde bereits im Stream registriert.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CLIENT_NOT_REGISTERED"></span><span id="error_log_client_not_registered"></span>**Fehler \_ Protokoll \_ Client \_ nicht \_ registriert**
</dt> <dd> <dl> <dt>

6637 (0x19ed)
</dt> <dt>



Ein Protokoll Client wurde nicht im Stream registriert.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_FULL_HANDLER_IN_PROGRESS"></span><span id="error_log_full_handler_in_progress"></span>**Fehler \_ Protokoll \_ Vollständiger \_ Handler \_ in \_ Bearbeitung**
</dt> <dd> <dl> <dt>

6638 (0x19ee)
</dt> <dt>



Es wurde bereits eine Anforderung zum Verarbeiten der vollständigen Protokolldatei vorgenommen.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CONTAINER_READ_FAILED"></span><span id="error_log_container_read_failed"></span>**Fehler \_ Protokoll- \_ Container \_ Lese \_ Vorgang**
</dt> <dd> <dl> <dt>

6639 (0x19ef)
</dt> <dt>



Fehler beim Protokolldienst beim Lesen aus einem Protokoll Container.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CONTAINER_WRITE_FAILED"></span><span id="error_log_container_write_failed"></span>**Fehler beim Schreiben des Fehler \_ Protokoll \_ Containers. \_ \_**
</dt> <dd> <dl> <dt>

6640 (0x19f 0)
</dt> <dt>



Der Protokolldienst hat beim Schreiben in einen Protokoll Container einen Fehler gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CONTAINER_OPEN_FAILED"></span><span id="error_log_container_open_failed"></span>**Fehler \_ Protokoll \_ Container \_ geöffnet \_**
</dt> <dd> <dl> <dt>

6641 (0x19f 1)
</dt> <dt>



Protokolldienst hat beim Versuch, einen Protokoll Container zu öffnen, einen Fehler ermittelt.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CONTAINER_STATE_INVALID"></span><span id="error_log_container_state_invalid"></span>**Fehler \_ Protokoll- \_ Container \_ Status \_ ungültig**
</dt> <dd> <dl> <dt>

6642 (0x19f 2)
</dt> <dt>



Der Protokolldienst hat beim Versuch einer angeforderten Aktion einen ungültigen Container Zustand fest.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_STATE_INVALID"></span><span id="error_log_state_invalid"></span>**Fehler \_ Protokoll \_ Status \_ ungültig**
</dt> <dd> <dl> <dt>

6643 (0x19f 3)
</dt> <dt>



Der Protokolldienst weist nicht den richtigen Status auf, um eine angeforderte Aktion auszuführen.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_PINNED"></span><span id="error_log_pinned"></span>**Fehler \_ Protokoll \_ fixiert**
</dt> <dd> <dl> <dt>

6644 (0x19f 4)
</dt> <dt>



Der Protokoll Speicher kann nicht freigegeben werden, da das Protokoll fixiert ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_METADATA_FLUSH_FAILED"></span><span id="error_log_metadata_flush_failed"></span>**Fehler beim Leeren der Fehler \_ Protokoll \_ Metadaten. \_ \_**
</dt> <dd> <dl> <dt>

6645 (0x19f 5)
</dt> <dt>



Fehler beim Leeren der Protokoll Metadaten.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_INCONSISTENT_SECURITY"></span><span id="error_log_inconsistent_security"></span>**Fehler \_ Protokoll \_ inkonsistente \_ Sicherheit**
</dt> <dd> <dl> <dt>

6646 (0x19f 6)
</dt> <dt>



Die Sicherheitseinstellungen für das Protokoll und seine Container sind inkonsistent.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_APPENDED_FLUSH_FAILED"></span><span id="error_log_appended_flush_failed"></span>**Fehler beim Anhängen des Fehler \_ Protokolls \_ \_ \_**
</dt> <dd> <dl> <dt>

6647 (0x19f)
</dt> <dt>



Es wurden Datensätze an das Protokoll angehängt, oder es wurden Reservierungs Änderungen vorgenommen, aber das Protokoll konnte nicht geleert werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_PINNED_RESERVATION"></span><span id="error_log_pinned_reservation"></span>**Fehler \_ Protokoll-feste \_ \_ Reservierung**
</dt> <dd> <dl> <dt>

6648 (0x19f 8)
</dt> <dt>



Das Protokoll wird aufgrund einer Reservierung fixiert, die den größten Teil des Protokoll Speicherplatzes beansprucht. Freigeben von reservierten Datensätzen, um Speicherplatz verfügbar zu machen.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_TRANSACTION"></span><span id="error_invalid_transaction"></span>**\_ungültige \_ Transaktion.**
</dt> <dd> <dl> <dt>

6700 (0x1a2c)
</dt> <dt>



Das diesem Vorgang zugeordnete Transaktions Handle ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_NOT_ACTIVE"></span><span id="error_transaction_not_active"></span>**Fehler \_ Transaktion \_ nicht \_ aktiv**
</dt> <dd> <dl> <dt>

6701 (0x1a2d)
</dt> <dt>



Der angeforderte Vorgang wurde im Kontext einer Transaktion durchgeführt, die nicht mehr aktiv ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_REQUEST_NOT_VALID"></span><span id="error_transaction_request_not_valid"></span>**Fehler \_ Transaktions \_ Anforderung \_ ist \_ ungültig.**
</dt> <dd> <dl> <dt>

6702 (0x1a2e)
</dt> <dt>



Der angeforderte Vorgang ist für das Transaktions Objekt im aktuellen Zustand ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_NOT_REQUESTED"></span><span id="error_transaction_not_requested"></span>**Fehler \_ Transaktion \_ nicht \_ angefordert**
</dt> <dd> <dl> <dt>

6703 (0x1a2f)
</dt> <dt>



Der Aufrufer hat eine Antwort-API aufgerufen, aber die Antwort wird nicht erwartet, da der TM die entsprechende Anforderung an den Aufrufer nicht ausgegeben hat.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_ALREADY_ABORTED"></span><span id="error_transaction_already_aborted"></span>**Fehler \_ Transaktion wurde \_ bereits \_ abgebrochen.**
</dt> <dd> <dl> <dt>

6704 (0x1A30)
</dt> <dt>



Es ist zu spät, den angeforderten Vorgang auszuführen, da die Transaktion bereits abgebrochen wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_ALREADY_COMMITTED"></span><span id="error_transaction_already_committed"></span>**Fehler \_ Transaktion \_ bereits committet \_**
</dt> <dd> <dl> <dt>

6705 (0x1a31)
</dt> <dt>



Es ist zu spät, den angeforderten Vorgang auszuführen, da für die Transaktion bereits ein Commit ausgeführt wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_TM_INITIALIZATION_FAILED"></span><span id="error_tm_initialization_failed"></span>**Fehler bei der \_ \_ Initialisierung des Fehlers TM \_**
</dt> <dd> <dl> <dt>

6706 (0x1a32)
</dt> <dt>



Der Transaktions-Manager konnte nicht erfolgreich initialisiert werden. Transaktive Vorgänge werden nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCEMANAGER_READ_ONLY"></span><span id="error_resourcemanager_read_only"></span>**Fehler \_ ResourceManager schreibgeschützt \_ \_**
</dt> <dd> <dl> <dt>

6707 (0x1a33)
</dt> <dt>



Der angegebene ResourceManager hat keine Änderungen oder Aktualisierungen an der Ressource in dieser Transaktion vorgenommen.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_NOT_JOINED"></span><span id="error_transaction_not_joined"></span>**Fehler \_ Transaktion \_ nicht \_ verknüpft**
</dt> <dd> <dl> <dt>

6708 (0x1a34)
</dt> <dt>



Der Ressourcen-Manager hat versucht, eine Transaktion vorzubereiten, der er nicht erfolgreich hinzugefügt wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_SUPERIOR_EXISTS"></span><span id="error_transaction_superior_exists"></span>**Fehler bei der über \_ \_ geordneten Transaktion \_ vorhanden**
</dt> <dd> <dl> <dt>

6709 (0x1a35)
</dt> <dt>



Das Transaktions Objekt weist bereits eine übergeordnete Eintragung auf, und der Aufrufer hat versucht, einen Vorgang auszuführen, der einen neuen übergeordneten erstellt hätte. Nur eine einzige übergeordnete Eintragung ist zulässig.


</dt> </dl> </dd> <dt>

<span id="ERROR_CRM_PROTOCOL_ALREADY_EXISTS"></span><span id="error_crm_protocol_already_exists"></span>**Error \_ CRM- \_ Protokoll ist \_ bereits \_ vorhanden.**
</dt> <dd> <dl> <dt>

6710 (0x1a36)
</dt> <dt>



Der RM hat versucht, ein bereits vorhandener Protokoll zu registrieren.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_PROPAGATION_FAILED"></span><span id="error_transaction_propagation_failed"></span>**Fehler bei Transaktions Weitergabe \_ \_ \_**
</dt> <dd> <dl> <dt>

6711 (0x1a37)
</dt> <dt>



Fehler beim Übertragen der Transaktion.


</dt> </dl> </dd> <dt>

<span id="ERROR_CRM_PROTOCOL_NOT_FOUND"></span><span id="error_crm_protocol_not_found"></span>**Fehler- \_ CRM- \_ Protokoll \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

6712 (0x1a38)
</dt> <dt>



Das angeforderte propagierungs Protokoll wurde nicht als CRM registriert.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_INVALID_MARSHALL_BUFFER"></span><span id="error_transaction_invalid_marshall_buffer"></span>**Fehler \_ Transaktion \_ ungültiger \_ Mars Hall \_ Puffer.**
</dt> <dd> <dl> <dt>

6713 (0x1a39)
</dt> <dt>



Der an PushTransaction oder PullTransaction weiter gegebene Puffer weist kein gültiges Format auf.


</dt> </dl> </dd> <dt>

<span id="ERROR_CURRENT_TRANSACTION_NOT_VALID"></span><span id="error_current_transaction_not_valid"></span>**Fehler der \_ aktuellen \_ Transaktion ist \_ \_ ungültig.**
</dt> <dd> <dl> <dt>

6714 (0x1a3a)
</dt> <dt>



Der dem Thread zugeordnete aktuelle Transaktionskontext ist kein gültiges Handle für ein Transaktions Objekt.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_NOT_FOUND"></span><span id="error_transaction_not_found"></span>**Fehler \_ Transaktion \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

6715 (0x1a3b)
</dt> <dt>



Das angegebene Transaktions Objekt konnte nicht geöffnet werden, da es nicht gefunden wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCEMANAGER_NOT_FOUND"></span><span id="error_resourcemanager_not_found"></span>**Fehler \_ ResourceManager \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

6716 (0x1a3c)
</dt> <dt>



Das angegebene ResourceManager-Objekt konnte nicht geöffnet werden, da es nicht gefunden wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_ENLISTMENT_NOT_FOUND"></span><span id="error_enlistment_not_found"></span>**Fehler \_ Eintragung \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

6717 (0x1a3d)
</dt> <dt>



Das angegebene Enlistment-Objekt konnte nicht geöffnet werden, da es nicht gefunden wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTIONMANAGER_NOT_FOUND"></span><span id="error_transactionmanager_not_found"></span>**Fehler " \_ transaktionmanager" \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

6718 (0x1a3e)
</dt> <dt>



Das angegebene transaktionmanager-Objekt konnte nicht geöffnet werden, da es nicht gefunden wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTIONMANAGER_NOT_ONLINE"></span><span id="error_transactionmanager_not_online"></span>**Fehler " \_ transaktionmanager" ist \_ nicht \_ Online.**
</dt> <dd> <dl> <dt>

6719 (0x1a3f)
</dt> <dt>



Das angegebene Objekt konnte nicht erstellt oder geöffnet werden, da der zugehörige transaktionmanager nicht online ist. Der Transaktionsmanager muss vollständig online geschaltet werden, indem wieder herstelltransaktionsmanager aufgerufen wird, um das Ende der Protokolldatei wiederherzustellen, bevor Objekte in den zugehörigen Transaktions-oder ResourceManager-Namespaces geöffnet werden können. Außerdem können Fehler beim Schreiben von Datensätzen in die Protokolldatei bewirken, dass ein transaktionmanager offline geschaltet wird.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTIONMANAGER_RECOVERY_NAME_COLLISION"></span><span id="error_transactionmanager_recovery_name_collision"></span>**Fehler beim \_ Transaktions-Manager- \_ Wiederherstellungs \_ namens \_ Konflikt.**
</dt> <dd> <dl> <dt>

6720 (0x1a40)
</dt> <dt>



Der angegebene transaktionmanager konnte die Objekte, die in der Protokolldatei enthalten sind, nicht im ob-Namespace erstellen. Daher konnte transaktionmanager nicht wieder hergestellt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_NOT_ROOT"></span><span id="error_transaction_not_root"></span>**Fehler \_ Transaktion \_ nicht \_ root**
</dt> <dd> <dl> <dt>

6721 (0x1a41)
</dt> <dt>



Der-Befehl zum Erstellen einer übergeordneten Eintragung für dieses Transaktions Objekt konnte nicht abgeschlossen werden, da das für die Eintragung angegebene Transaktions Objekt eine untergeordnete Verzweigung der Transaktion ist. Nur der Stamm der Transaktion kann als übergeordnetes Element eingetragen werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_OBJECT_EXPIRED"></span><span id="error_transaction_object_expired"></span>**Fehler \_ Transaktions \_ Objekt ist \_ abgelaufen.**
</dt> <dd> <dl> <dt>

6722 (0x1a42)
</dt> <dt>



Da der zugeordnete Transaktions-Manager oder der zugehörige Ressourcen-Manager geschlossen wurde, ist das Handle nicht mehr gültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_RESPONSE_NOT_ENLISTED"></span><span id="error_transaction_response_not_enlisted"></span>**Fehler \_ Transaktions \_ Antwort \_ nicht \_ eingetragen**
</dt> <dd> <dl> <dt>

6723 (0x1a43)
</dt> <dt>



Der angegebene Vorgang konnte für diese übergeordnete Eintragung nicht ausgeführt werden, da die Eintragung nicht mit der entsprechenden Vervollständigungs Antwort in notificationmask erstellt wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_RECORD_TOO_LONG"></span><span id="error_transaction_record_too_long"></span>**Fehler \_ Transaktions \_ Daten Satz \_ zu \_ lang**
</dt> <dd> <dl> <dt>

6724 (0x1a44)
</dt> <dt>



Der angegebene Vorgang konnte nicht ausgeführt werden, da der zu protokollierende Datensatz zu lang war. Dies kann auf zwei Bedingungen auftreten: entweder gibt es zu viele Einfügungen für diese Transaktion, oder die kombinierten Wiederherstellungsinformationen, die im Auftrag dieser Eintragung protokolliert werden, sind zu lang.


</dt> </dl> </dd> <dt>

<span id="ERROR_IMPLICIT_TRANSACTION_NOT_SUPPORTED"></span><span id="error_implicit_transaction_not_supported"></span>**die \_ implizite \_ Transaktion \_ \_ wird nicht unterstützt.**
</dt> <dd> <dl> <dt>

6725 (0x1a45)
</dt> <dt>



Implizite Transaktionen werden nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_INTEGRITY_VIOLATED"></span><span id="error_transaction_integrity_violated"></span>**Fehler \_ Transaktions \_ Integrität \_ verletzt**
</dt> <dd> <dl> <dt>

6726 (0x1a46)
</dt> <dt>



Der Kerneltransaktions-Manager musste die Transaktion abbrechen oder vergessen, da der Fortschritt des Vorgangs blockiert ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTIONMANAGER_IDENTITY_MISMATCH"></span><span id="error_transactionmanager_identity_mismatch"></span>**Fehler bei der \_ transaktionmanager- \_ Identitäts \_ Übereinstimmung.**
</dt> <dd> <dl> <dt>

6727 (0x1a47)
</dt> <dt>



Die bereitgestellte transaktionmanager-Identität entsprach nicht der in der Protokolldatei des Transaktions-Managers aufgezeichneten.


</dt> </dl> </dd> <dt>

<span id="ERROR_RM_CANNOT_BE_FROZEN_FOR_SNAPSHOT"></span><span id="error_rm_cannot_be_frozen_for_snapshot"></span>**Fehler \_ RM \_ kann \_ \_ für die \_ \_ Momentaufnahme nicht eingefroren werden.**
</dt> <dd> <dl> <dt>

6728 (0x1a48)
</dt> <dt>



Dieser Momentaufnahme Vorgang kann nicht fortgesetzt werden, da ein transaktionaler Ressourcen-Manager im aktuellen Zustand nicht fixiert werden kann. Versuchen Sie es erneut.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_MUST_WRITETHROUGH"></span><span id="error_transaction_must_writethrough"></span>**Fehler beim Überschreiben der \_ Transaktion \_ \_**
</dt> <dd> <dl> <dt>

6729 (0x1a49)
</dt> <dt>



Die Transaktion kann nicht mit der angegebenen enlistmentmask eingetragen werden, weil die Transaktion die vorvorbereitungs Phase bereits abgeschlossen hat. Um die Richtigkeit sicherzustellen, muss der ResourceManager zu einem Lese-/Schreibmodus wechseln und das Zwischenspeichern von Daten innerhalb dieser Transaktion beenden. Die Eintragung nur für nachfolgende Transaktions Phasen ist möglicherweise dennoch erfolgreich.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_NO_SUPERIOR"></span><span id="error_transaction_no_superior"></span>**Fehler \_ Transaktion \_ keine über \_ geordnete Transaktion**
</dt> <dd> <dl> <dt>

6730 (0x1a4a)
</dt> <dt>



Die Transaktion weist keine übergeordnete Eintragung auf.


</dt> </dl> </dd> <dt>

<span id="ERROR_HEURISTIC_DAMAGE_POSSIBLE"></span><span id="error_heuristic_damage_possible"></span>**Fehler \_ heuristischer \_ Schaden \_**
</dt> <dd> <dl> <dt>

6731 (0x1a4b)
</dt> <dt>



Der Versuch, einen Commit für die Transaktion durchzuführen, wurde abgeschlossen, es ist jedoch möglich, dass ein Teil der Transaktionsstruktur aufgrund der Heuristik nicht erfolgreich ausgeführt wurde. Daher ist es möglich, dass für einige Daten, die in der Transaktion geändert wurden, möglicherweise kein Commit ausgeführt wurde, was zu Transaktions Inkonsistenz führt. Überprüfen Sie nach Möglichkeit die Konsistenz der zugehörigen Daten.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTIONAL_CONFLICT"></span><span id="error_transactional_conflict"></span>**Fehler \_ Transaktions \_ Konflikt**
</dt> <dd> <dl> <dt>

6800 (0x1a90)
</dt> <dt>



Die Funktion hat versucht, einen Namen zu verwenden, der für die Verwendung durch eine andere Transaktion reserviert ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_RM_NOT_ACTIVE"></span><span id="error_rm_not_active"></span>**Fehler \_ RM \_ nicht \_ aktiv**
</dt> <dd> <dl> <dt>

6801 (0x1a91)
</dt> <dt>



Die Transaktionsunterstützung innerhalb des angegebenen Ressourcen-Managers wurde nicht gestartet oder wurde aufgrund eines Fehlers heruntergefahren.


</dt> </dl> </dd> <dt>

<span id="ERROR_RM_METADATA_CORRUPT"></span><span id="error_rm_metadata_corrupt"></span>**Fehler \_ RM- \_ Metadaten \_ beschädigt**
</dt> <dd> <dl> <dt>

6802 (0x1a92)
</dt> <dt>



Die Metadaten des RM sind beschädigt. Der RM funktioniert nicht.


</dt> </dl> </dd> <dt>

<span id="ERROR_DIRECTORY_NOT_RM"></span><span id="error_directory_not_rm"></span>**Fehler \_ Verzeichnis \_ nicht \_ RM**
</dt> <dd> <dl> <dt>

6803 (0x1a93)
</dt> <dt>



Das angegebene Verzeichnis enthält keinen Ressourcen-Manager.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTIONS_UNSUPPORTED_REMOTE"></span><span id="error_transactions_unsupported_remote"></span>**\_ \_ nicht unterstützte Remote Fehler Transaktionen \_**
</dt> <dd> <dl> <dt>

6805 (0x1a95)
</dt> <dt>



Der Remote Server oder die Freigabe unterstützt keine transaktiven Datei Vorgänge.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_RESIZE_INVALID_SIZE"></span><span id="error_log_resize_invalid_size"></span>**Größe des Fehler \_ Protokoll- \_ Größenänderung ist \_ ungültig \_ .**
</dt> <dd> <dl> <dt>

6806 (0x1a96)
</dt> <dt>



Die angeforderte Protokoll Größe ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_OBJECT_NO_LONGER_EXISTS"></span><span id="error_object_no_longer_exists"></span>**das Fehler \_ Objekt ist \_ nicht \_ mehr \_ vorhanden.**
</dt> <dd> <dl> <dt>

6807 (0x1a97)
</dt> <dt>



Das Objekt (Datei, Stream, Link), das dem Handle entspricht, wurde durch ein Sicherungspunkt-Rollback für die Transaktion gelöscht.


</dt> </dl> </dd> <dt>

<span id="ERROR_STREAM_MINIVERSION_NOT_FOUND"></span><span id="error_stream_miniversion_not_found"></span>**Fehler Daten \_ Strom- \_ Miniversion wurde \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

6808 (0x1a98)
</dt> <dt>



Die angegebene Triggerszenarios der Datei wurde für die geöffnete Transaktions Datei nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_STREAM_MINIVERSION_NOT_VALID"></span><span id="error_stream_miniversion_not_valid"></span>**Fehler Daten \_ Strom- \_ Miniversion ist \_ \_ ungültig.**
</dt> <dd> <dl> <dt>

6809 (0x1a99)
</dt> <dt>



Die angegebene Triggerszenarios der Datei wurde gefunden, Sie wurde jedoch für ungültig erklärt. Die wahrscheinlichste Ursache ist ein Sicherungspunkt-Rollback für die Transaktion.


</dt> </dl> </dd> <dt>

<span id="ERROR_MINIVERSION_INACCESSIBLE_FROM_SPECIFIED_TRANSACTION"></span><span id="error_miniversion_inaccessible_from_specified_transaction"></span>**Fehler \_ Miniversion \_ \_ von der \_ angegebenen Transaktion aus nicht zugänglich \_**
</dt> <dd> <dl> <dt>

6810 (0x1a9a)
</dt> <dt>



Eine Triggerszenarios kann nur im Kontext der Transaktion geöffnet werden, von der Sie erstellt wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_OPEN_MINIVERSION_WITH_MODIFY_INTENT"></span><span id="error_cant_open_miniversion_with_modify_intent"></span>**Fehler \_ \_ beim Öffnen \_ von Miniversion \_ mit Änderungs \_ \_ Absicht.**
</dt> <dd> <dl> <dt>

6811 (0x1a9b)
</dt> <dt>



Es ist nicht möglich, eine Triggerszenarios mit Änderungs Zugriff zu öffnen.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_CREATE_MORE_STREAM_MINIVERSIONS"></span><span id="error_cant_create_more_stream_miniversions"></span>**Fehler \_ beim \_ Erstellen von \_ weiteren \_ Stream- \_ Miniversionen.**
</dt> <dd> <dl> <dt>

6812 (0x1a9c)
</dt> <dt>



Es ist nicht möglich, weitere miniversions für diesen Stream zu erstellen.


</dt> </dl> </dd> <dt>

<span id="ERROR_REMOTE_FILE_VERSION_MISMATCH"></span><span id="error_remote_file_version_mismatch"></span>**Fehler bei \_ Remote \_ Datei \_ Version \_ .**
</dt> <dd> <dl> <dt>

6814 (0x1a9e)
</dt> <dt>



Der Remote Server hat eine nicht übereinstimmende Versionsnummer oder FID für eine Datei gesendet, die mit Transaktionen geöffnet wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_HANDLE_NO_LONGER_VALID"></span><span id="error_handle_no_longer_valid"></span>**Fehler \_ handle ist \_ nicht \_ mehr \_ gültig.**
</dt> <dd> <dl> <dt>

6815 (0x1a9f)
</dt> <dt>



Das Handle wurde durch eine Transaktion für ungültig erklärt. Die wahrscheinlichste Ursache ist das vorhanden sein einer Speicher Zuordnung für eine Datei oder ein geöffnetes Handle, wenn die Transaktion beendet oder auf Sicherungspunkt zurückgesetzt wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_TXF_METADATA"></span><span id="error_no_txf_metadata"></span>**Fehler \_ keine \_ TxF- \_ Metadaten.**
</dt> <dd> <dl> <dt>

6816 (0x1aa0)
</dt> <dt>



Es sind keine Transaktions Metadaten für die Datei vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CORRUPTION_DETECTED"></span><span id="error_log_corruption_detected"></span>**Fehler \_ Protokoll \_ Beschädigung \_ erkannt**
</dt> <dd> <dl> <dt>

6817 (0x1aa1)
</dt> <dt>



Die Protokolldaten sind beschädigt.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_RECOVER_WITH_HANDLE_OPEN"></span><span id="error_cant_recover_with_handle_open"></span>**Fehler \_ \_ bei der Wiederherstellung \_ mit dem \_ \_ geöffneten handle.**
</dt> <dd> <dl> <dt>

6818 (0x1aa2)
</dt> <dt>



Die Datei kann nicht wieder hergestellt werden, da noch ein Handle geöffnet ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_RM_DISCONNECTED"></span><span id="error_rm_disconnected"></span>**Fehler \_ RM \_ getrennt**
</dt> <dd> <dl> <dt>

6819 (0x1aa3)
</dt> <dt>



Das Transaktions Ergebnis ist nicht verfügbar, da der für die IT Verantwortliche Ressourcen-Manager getrennt ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_ENLISTMENT_NOT_SUPERIOR"></span><span id="error_enlistment_not_superior"></span>**Fehler \_ Eintragung ist \_ nicht über \_ geordneter Name**
</dt> <dd> <dl> <dt>

6820 (0x1aa4)
</dt> <dt>



Die Anforderung wurde zurückgewiesen, weil es sich bei der fraglichen Eintragung nicht um eine überragende Eintragung handelt.


</dt> </dl> </dd> <dt>

<span id="ERROR_RECOVERY_NOT_NEEDED"></span><span id="error_recovery_not_needed"></span>**Fehler \_ Wiederherstellung \_ nicht \_ erforderlich**
</dt> <dd> <dl> <dt>

6821 (0x1aa5)
</dt> <dt>



Der transaktionale Ressourcen-Manager ist bereits konsistent. Die Wiederherstellung ist nicht erforderlich.


</dt> </dl> </dd> <dt>

<span id="ERROR_RM_ALREADY_STARTED"></span><span id="error_rm_already_started"></span>**Fehler \_ RM \_ bereits \_ gestartet**
</dt> <dd> <dl> <dt>

6822 (0x1aa6)
</dt> <dt>



Der transaktionale Ressourcen-Manager wurde bereits gestartet.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_IDENTITY_NOT_PERSISTENT"></span><span id="error_file_identity_not_persistent"></span>**Fehler \_ Datei \_ Identität \_ nicht \_ persistent**
</dt> <dd> <dl> <dt>

6823 (0x1aa7)
</dt> <dt>



Die Datei kann nicht transaktional geöffnet werden, da ihre Identität vom Ergebnis einer nicht aufgelösten Transaktion abhängt.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_BREAK_TRANSACTIONAL_DEPENDENCY"></span><span id="error_cant_break_transactional_dependency"></span>**Fehler \_ beim \_ Abbrechen der \_ Transaktions \_ Abhängigkeit.**
</dt> <dd> <dl> <dt>

6824 (0x1aa8)
</dt> <dt>



Der Vorgang kann nicht ausgeführt werden, da eine andere Transaktion von der Tatsache abhängig ist, dass diese Eigenschaft nicht geändert wird.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_CROSS_RM_BOUNDARY"></span><span id="error_cant_cross_rm_boundary"></span>**Fehler \_ beim \_ überschreiten der \_ \_ Grenze.**
</dt> <dd> <dl> <dt>

6825 (0x1aa9)
</dt> <dt>



Der Vorgang würde eine einzelne Datei mit zwei transaktionalen Ressourcen-Managern einschließen und ist daher nicht zulässig.


</dt> </dl> </dd> <dt>

<span id="ERROR_TXF_DIR_NOT_EMPTY"></span><span id="error_txf_dir_not_empty"></span>**Fehler \_ TxF-Verzeichnis \_ \_ nicht \_ leer**
</dt> <dd> <dl> <dt>

6826 (0x1aaa)
</dt> <dt>



Das $TxF Verzeichnis muss leer sein, damit dieser Vorgang erfolgreich ausgeführt werden konnte.


</dt> </dl> </dd> <dt>

<span id="ERROR_INDOUBT_TRANSACTIONS_EXIST"></span><span id="error_indoubt_transactions_exist"></span>**fehlerhafte \_ \_ Transaktionen sind \_ vorhanden.**
</dt> <dd> <dl> <dt>

6827 (0x1aab)
</dt> <dt>



Der Vorgang würde einen transaktionalen Ressourcen-Manager in einem inkonsistenten Zustand belassen und ist daher nicht zulässig.


</dt> </dl> </dd> <dt>

<span id="ERROR_TM_VOLATILE"></span><span id="error_tm_volatile"></span>**Fehler \_ TM \_ flüchtig**
</dt> <dd> <dl> <dt>

6828 (0x1aac)
</dt> <dt>



Der Vorgang konnte nicht abgeschlossen werden, da der Transaktions-Manager kein Protokoll hat.


</dt> </dl> </dd> <dt>

<span id="ERROR_ROLLBACK_TIMER_EXPIRED"></span><span id="error_rollback_timer_expired"></span>**Fehler beim \_ Rollback- \_ Zeitgeber. \_**
</dt> <dd> <dl> <dt>

6829 (0x1aad)
</dt> <dt>



Ein Rollback konnte nicht geplant werden, da ein zuvor geplanter Rollback bereits ausgeführt wurde oder für die Ausführung in die Warteschlange eingereiht wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_TXF_ATTRIBUTE_CORRUPT"></span><span id="error_txf_attribute_corrupt"></span>**Fehler \_ TxF- \_ Attribut ist \_ beschädigt.**
</dt> <dd> <dl> <dt>

6830 (0x1aae)
</dt> <dt>



Das transaktionale Metadatenattribut für die Datei oder das Verzeichnis ist beschädigt und kann nicht gelesen werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_EFS_NOT_ALLOWED_IN_TRANSACTION"></span><span id="error_efs_not_allowed_in_transaction"></span>**Fehler \_ EFS \_ \_ \_ in Transaktion nicht \_ zulässig**
</dt> <dd> <dl> <dt>

6831 (0x1aaf)
</dt> <dt>



Der Verschlüsselungs Vorgang konnte nicht abgeschlossen werden, da eine Transaktion aktiv ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTIONAL_OPEN_NOT_ALLOWED"></span><span id="error_transactional_open_not_allowed"></span>**Fehler beim \_ Öffnen der Transaktion ist \_ \_ nicht \_ zulässig.**
</dt> <dd> <dl> <dt>

6832 (0x1ab0)
</dt> <dt>



Dieses Objekt darf nicht in einer Transaktion geöffnet werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_GROWTH_FAILED"></span><span id="error_log_growth_failed"></span>**Fehler beim Vergrößern des Fehler \_ Protokolls \_ \_**
</dt> <dd> <dl> <dt>

6833 (0x1ab1)
</dt> <dt>



Fehler beim Erstellen von Speicherplatz im Protokoll des Transaktions Ressourcen-Managers. Der Fehlerstatus wurde im Ereignisprotokoll aufgezeichnet.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTED_MAPPING_UNSUPPORTED_REMOTE"></span><span id="error_transacted_mapping_unsupported_remote"></span>**Fehler bei der \_ Transaktions Zuordnung, die \_ \_ nicht unterstützt wird \_ .**
</dt> <dd> <dl> <dt>

6834 (0x1ab2)
</dt> <dt>



Speicher Zuordnung (Erstellen eines zugeordneten Abschnitts) eine Remote Datei unter einer Transaktion wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_TXF_METADATA_ALREADY_PRESENT"></span><span id="error_txf_metadata_already_present"></span>**Fehler \_ TxF- \_ Metadaten sind \_ bereits \_ vorhanden.**
</dt> <dd> <dl> <dt>

6835 (0x1ab3)
</dt> <dt>



Transaktions Metadaten sind bereits in dieser Datei vorhanden und können nicht abgelöst werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_SCOPE_CALLBACKS_NOT_SET"></span><span id="error_transaction_scope_callbacks_not_set"></span>**Fehler \_ Transaktions \_ Bereichs- \_ Rückrufe \_ nicht \_ festgelegt**
</dt> <dd> <dl> <dt>

6836 (0x1ab4)
</dt> <dt>



Ein Transaktions Bereich konnte nicht eingegeben werden, da der Bereichs Handler nicht initialisiert wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_REQUIRED_PROMOTION"></span><span id="error_transaction_required_promotion"></span>**herauf Stufung der Fehler \_ Transaktion \_ erforderlich \_**
</dt> <dd> <dl> <dt>

6837 (0x1ab5)
</dt> <dt>



Die herauf Stufung war erforderlich, damit sich der Ressourcen-Manager eintragen kann, aber die Transaktion wurde so festgelegt, dass Sie nicht zulässig ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_EXECUTE_FILE_IN_TRANSACTION"></span><span id="error_cannot_execute_file_in_transaction"></span>**Fehler \_ \_ beim Ausführen \_ \_ der Datei in der \_ Transaktion.**
</dt> <dd> <dl> <dt>

6838 (0x1ab6)
</dt> <dt>



Diese Datei ist für Änderungen in einer nicht aufgelösten Transaktion geöffnet und kann nur für die Ausführung durch einen transaktiven Reader geöffnet werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTIONS_NOT_FROZEN"></span><span id="error_transactions_not_frozen"></span>**Fehler \_ Transaktionen \_ nicht \_ eingefroren**
</dt> <dd> <dl> <dt>

6839 (0x1ab7)
</dt> <dt>



Die Anforderung zum Aktivieren von fixierten Transaktionen wurde ignoriert, da Transaktionen zuvor nicht eingefroren wurden.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_FREEZE_IN_PROGRESS"></span><span id="error_transaction_freeze_in_progress"></span>**Fehler \_ \_ beim Einfrieren \_ der Transaktion. \_**
</dt> <dd> <dl> <dt>

6840 (0x1ab8)
</dt> <dt>



Transaktionen können nicht eingefroren werden, weil bereits eine Sperre ausgeführt wird.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SNAPSHOT_VOLUME"></span><span id="error_not_snapshot_volume"></span>**Fehler beim Erstellen eines \_ \_ Momentaufnahme \_ Volumens**
</dt> <dd> <dl> <dt>

6841 (0x1ab9)
</dt> <dt>



Das Ziel Volume ist kein momentaufnahmenvolume. Dieser Vorgang gilt nur für ein Volume, das als Momentaufnahme bereitgestellt wird.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SAVEPOINT_WITH_OPEN_FILES"></span><span id="error_no_savepoint_with_open_files"></span>**Fehler " \_ kein Sicherungs \_ Punkt" \_ mit \_ geöffneten \_ Dateien**
</dt> <dd> <dl> <dt>

6842 (0x1aba)
</dt> <dt>



Fehler beim Sicherungspunkt-Vorgang, da Dateien für die Transaktion geöffnet sind. Dies ist nicht zulässig.


</dt> </dl> </dd> <dt>

<span id="ERROR_DATA_LOST_REPAIR"></span><span id="error_data_lost_repair"></span>**Fehler beim Reparieren von Fehler \_ Daten. \_ \_**
</dt> <dd> <dl> <dt>

6843 (0x1abb)
</dt> <dt>



Windows hat Beschädigungen in einer Datei erkannt, und diese Datei wurde seit der Reparatur repariert. Möglicherweise ist ein Datenverlust aufgetreten.


</dt> </dl> </dd> <dt>

<span id="ERROR_SPARSE_NOT_ALLOWED_IN_TRANSACTION"></span><span id="error_sparse_not_allowed_in_transaction"></span>**Fehler \_ Sparse \_ ist \_ \_ in der \_ Transaktion nicht zulässig.**
</dt> <dd> <dl> <dt>

6844 (0x1abc)
</dt> <dt>



Der sparsesvorgang konnte nicht abgeschlossen werden, da eine Transaktion in der Datei aktiv ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_TM_IDENTITY_MISMATCH"></span><span id="error_tm_identity_mismatch"></span>**Fehler- \_ TM- \_ Identitätskonflikt \_**
</dt> <dd> <dl> <dt>

6845 (0x1abd)
</dt> <dt>



Fehler beim Erstellen eines transaktionmanager-Objekts, weil die in der Protokolldatei gespeicherte TM-Identität nicht mit der als Argument übergebenen TM-Identität identisch ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_FLOATED_SECTION"></span><span id="error_floated_section"></span>**Fehler \_ im \_ Abschnitt**
</dt> <dd> <dl> <dt>

6846 (0x1abe)
</dt> <dt>



Es wurde versucht, auf einem Abschnitts Objekt einen e/a-Vorgang auszuführen, der als Ergebnis einer Transaktions Ende aufgetreten ist. Es sind keine gültigen Daten vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_ACCEPT_TRANSACTED_WORK"></span><span id="error_cannot_accept_transacted_work"></span>**Fehler \_ kann \_ keine \_ transaktive \_ Arbeit annehmen.**
</dt> <dd> <dl> <dt>

6847 (0x1abf)
</dt> <dt>



Der Transaktions Ressourcen-Manager kann derzeit keine transaktiven Arbeiten aufgrund eines vorübergehenden Zustands, wie z. b. geringer Ressourcen, akzeptieren.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_ABORT_TRANSACTIONS"></span><span id="error_cannot_abort_transactions"></span>**Fehler \_ beim \_ Abbrechen der \_ Transaktionen.**
</dt> <dd> <dl> <dt>

6848 (0x1ac0)
</dt> <dt>



Für den transaktionalen Ressourcen-Manager waren zu viele ausstehende Zuweisungs Vorgänge möglich, die nicht abgebrochen werden konnten. Der transaktionale Ressourcen-Manager wurde heruntergefahren.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_CLUSTERS"></span><span id="error_bad_clusters"></span>**Fehler \_ hafte \_ Cluster**
</dt> <dd> <dl> <dt>

6849 (0x1ac1)
</dt> <dt>



Der Vorgang konnte aufgrund von fehlerhaften Clustern auf dem Datenträger nicht abgeschlossen werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_COMPRESSION_NOT_ALLOWED_IN_TRANSACTION"></span><span id="error_compression_not_allowed_in_transaction"></span>**Fehler \_ Komprimierung \_ \_ \_ in \_ Transaktion nicht zulässig.**
</dt> <dd> <dl> <dt>

6850 (0x1ac2)
</dt> <dt>



Der Komprimierungs Vorgang konnte nicht abgeschlossen werden, da für die Datei eine Transaktion aktiv ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_VOLUME_DIRTY"></span><span id="error_volume_dirty"></span>**Fehler \_ Volume \_ geändert**
</dt> <dd> <dl> <dt>

6851 (0x1ac3)
</dt> <dt>



Der Vorgang konnte nicht abgeschlossen werden, da das Volume geändert wurde. Führen Sie Chkdsk aus, und versuchen Sie es noch mal.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_LINK_TRACKING_IN_TRANSACTION"></span><span id="error_no_link_tracking_in_transaction"></span>**Fehler \_ \_ beim Nachverfolgen von Verbindungen \_ \_ in der \_ Transaktion.**
</dt> <dd> <dl> <dt>

6852 (0x1ac4)
</dt> <dt>



Der Link nach Verfolgungs Vorgang konnte nicht abgeschlossen werden, da eine Transaktion aktiv ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_OPERATION_NOT_SUPPORTED_IN_TRANSACTION"></span><span id="error_operation_not_supported_in_transaction"></span>**Fehler \_ Vorgang \_ \_ wird \_ in der \_ Transaktion nicht unterstützt.**
</dt> <dd> <dl> <dt>

6853 (0x1ac5)
</dt> <dt>



Dieser Vorgang kann nicht in einer Transaktion ausgeführt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_EXPIRED_HANDLE"></span><span id="error_expired_handle"></span>**Fehler \_ abgelaufenes \_ handle**
</dt> <dd> <dl> <dt>

6854 (0x1ac6)
</dt> <dt>



Das Handle ist nicht mehr ordnungsgemäß mit der zugehörigen Transaktion verknüpft. Möglicherweise wurde Sie in einem transaktionalen Ressourcen-Manager geöffnet, der später neu gestartet werden musste. Schließen Sie das Handle, und öffnen Sie ein neues.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_NOT_ENLISTED"></span><span id="error_transaction_not_enlisted"></span>**Fehler \_ Transaktion \_ nicht \_ eingetragen.**
</dt> <dd> <dl> <dt>

6855 (0x1ac7)
</dt> <dt>



Der angegebene Vorgang konnte nicht ausgeführt werden, da der Ressourcen-Manager nicht in der Transaktion eingetragen ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_WINSTATION_NAME_INVALID"></span><span id="error_ctx_winstation_name_invalid"></span>**Fehler \_ ctx- \_ Winstations \_ Name \_ ungültig**
</dt> <dd> <dl> <dt>

7001 (0x1b59)
</dt> <dt>



Der angegebene Sitzungsname ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_INVALID_PD"></span><span id="error_ctx_invalid_pd"></span>**Fehler \_ ctx \_ ungültige \_ PD.**
</dt> <dd> <dl> <dt>

7002 (0x1b5a)
</dt> <dt>



Der angegebene Protokoll Treiber ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_PD_NOT_FOUND"></span><span id="error_ctx_pd_not_found"></span>**Fehler \_ ctx- \_ PD \_ nicht \_ gefunden**
</dt> <dd> <dl> <dt>

7003 (0x1b5b)
</dt> <dt>



Der angegebene Protokoll Treiber wurde nicht im Systempfad gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_WD_NOT_FOUND"></span><span id="error_ctx_wd_not_found"></span>**Fehler \_ ctx \_ WD \_ nicht \_ gefunden**
</dt> <dd> <dl> <dt>

7004 (0x1b5c)
</dt> <dt>



Der angegebene terminalverbindungs-Treiber wurde nicht im Systempfad gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CANNOT_MAKE_EVENTLOG_ENTRY"></span><span id="error_ctx_cannot_make_eventlog_entry"></span>**Fehler \_ ctx \_ kann \_ \_ EventLog- \_ Eintrag nicht erstellen**
</dt> <dd> <dl> <dt>

7005 (0x1b5d)
</dt> <dt>



Für diese Sitzung konnte kein Registrierungsschlüssel für die Ereignisprotokollierung erstellt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_SERVICE_NAME_COLLISION"></span><span id="error_ctx_service_name_collision"></span>**Fehler \_ ctx- \_ Dienst \_ namens \_ Kollision**
</dt> <dd> <dl> <dt>

7006 (0x1b5e)
</dt> <dt>



Ein Dienst mit diesem Namen ist bereits im System vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CLOSE_PENDING"></span><span id="error_ctx_close_pending"></span>**Fehler beim \_ Schließen der ctx-Datei \_ \_**
</dt> <dd> <dl> <dt>

7007 (0x1b5f)
</dt> <dt>



Ein Schließvorgang steht in der Sitzung aus.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_NO_OUTBUF"></span><span id="error_ctx_no_outbuf"></span>**Fehler \_ ctx \_ No \_ outbuf**
</dt> <dd> <dl> <dt>

7008 (0x1b60)
</dt> <dt>



Es sind keine freien Ausgabepuffer verfügbar.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_MODEM_INF_NOT_FOUND"></span><span id="error_ctx_modem_inf_not_found"></span>**Fehler " \_ ctx \_ Modem \_ INF" \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

7009 (0x1b61)
</dt> <dt>



Das Modem. Die INF-Datei wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_INVALID_MODEMNAME"></span><span id="error_ctx_invalid_modemname"></span>**Fehler \_ ctx \_ ungültige " \_ mudemname".**
</dt> <dd> <dl> <dt>

7010 (0x1b62)
</dt> <dt>



Der Modem Name wurde in "Modem. inf" nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_MODEM_RESPONSE_ERROR"></span><span id="error_ctx_modem_response_error"></span>**Fehler \_ ctx- \_ Modem \_ Antwort \_ Fehler**
</dt> <dd> <dl> <dt>

7011 (0x1b63)
</dt> <dt>



Das Modem hat den an ihn gesendeten Befehl nicht akzeptiert. Überprüfen Sie, ob der konfigurierte Modem Name mit dem angeschlossenen Modem übereinstimmt


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_MODEM_RESPONSE_TIMEOUT"></span><span id="error_ctx_modem_response_timeout"></span>**Fehler \_ ctx- \_ Modem \_ Antwort \_ Timeout**
</dt> <dd> <dl> <dt>

7012 (0x1b64)
</dt> <dt>



Das Modem hat nicht auf den an ihn gesendeten Befehl geantwortet. Vergewissern Sie sich, dass das Modem ordnungsgemäß verkabelt und eingeschaltet ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_MODEM_RESPONSE_NO_CARRIER"></span><span id="error_ctx_modem_response_no_carrier"></span>**Fehler \_ ctx- \_ Modem \_ Antwort kein Netz \_ \_ Betreiber**
</dt> <dd> <dl> <dt>

7013 (0x1b65)
</dt> <dt>



Fehler bei der Träger Erkennung, oder der Netzbetreiber wurde aufgrund einer Trennung gelöscht.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_MODEM_RESPONSE_NO_DIALTONE"></span><span id="error_ctx_modem_response_no_dialtone"></span>**Fehler " \_ ctx \_ Modem \_ Response \_ No \_ Dialtone"**
</dt> <dd> <dl> <dt>

7014 (0x1b66)
</dt> <dt>



Der Wählton wurde innerhalb der erforderlichen Zeit nicht erkannt. Stellen Sie sicher, dass das Telefonkabel ordnungsgemäß angeschlossen und funktionsfähig ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_MODEM_RESPONSE_BUSY"></span><span id="error_ctx_modem_response_busy"></span>**Fehler \_ ctx- \_ Modem \_ Antwort \_ ausgelastet**
</dt> <dd> <dl> <dt>

7015 (0x1b67)
</dt> <dt>



Das ausgelastete Signal wurde an der Remote Site beim Rückruf erkannt.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_MODEM_RESPONSE_VOICE"></span><span id="error_ctx_modem_response_voice"></span>**Fehler \_ ctx- \_ Modem \_ Antwort \_ Sprache**
</dt> <dd> <dl> <dt>

7016 (0x1b68)
</dt> <dt>



Die Stimme wurde bei einem Rückruf an der Remote Site erkannt.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_TD_ERROR"></span><span id="error_ctx_td_error"></span>**Fehler \_ ctx- \_ TD- \_ Fehler**
</dt> <dd> <dl> <dt>

7017 (0x1b69)
</dt> <dt>



Transport Treiber Fehler.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_WINSTATION_NOT_FOUND"></span><span id="error_ctx_winstation_not_found"></span>**Fehler \_ ctx- \_ WinStation \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

7022 (0x1b6e)
</dt> <dt>



Die angegebene Sitzung wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_WINSTATION_ALREADY_EXISTS"></span><span id="error_ctx_winstation_already_exists"></span>**Fehler \_ ctx- \_ WinStation ist \_ bereits \_ vorhanden.**
</dt> <dd> <dl> <dt>

7023 (0x1b6f)
</dt> <dt>



Der angegebene Sitzungsname wird bereits verwendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_WINSTATION_BUSY"></span><span id="error_ctx_winstation_busy"></span>**Fehler \_ ctx- \_ WinStation \_ ausgelastet**
</dt> <dd> <dl> <dt>

7024 (0x1b70)
</dt> <dt>



Der Task, den Sie ausführen möchten, kann nicht abgeschlossen werden, da Remotedesktopdienste aktuell ausgelastet ist. Wiederholen Sie den Vorgang in einigen Minuten. Andere Benutzer sollten sich weiterhin anmelden können.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_BAD_VIDEO_MODE"></span><span id="error_ctx_bad_video_mode"></span>**fehlerhafter \_ ctx- \_ \_ Video \_ Modus (falsch)**
</dt> <dd> <dl> <dt>

7025 (0x1b71)
</dt> <dt>



Es wurde versucht, eine Verbindung mit einer Sitzung herzustellen, deren Videomodus vom aktuellen Client nicht unterstützt wird.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_GRAPHICS_INVALID"></span><span id="error_ctx_graphics_invalid"></span>**Fehler \_ ctx- \_ Grafik \_ ungültig**
</dt> <dd> <dl> <dt>

7035 (0x1b7b)
</dt> <dt>



Die Anwendung hat versucht, den DOS-Grafikmodus zu aktivieren. Der DOS-Grafikmodus wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_LOGON_DISABLED"></span><span id="error_ctx_logon_disabled"></span>**Fehler bei \_ ctx- \_ Anmeldung \_ deaktiviert**
</dt> <dd> <dl> <dt>

7037 (0x1b7d)
</dt> <dt>



Ihre interaktive Anmelde Berechtigung wurde deaktiviert. Wenden Sie sich an den Administrator.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_NOT_CONSOLE"></span><span id="error_ctx_not_console"></span>**Fehler \_ ctx \_ nicht \_ Konsole**
</dt> <dd> <dl> <dt>

7038 (0x1b7e)
</dt> <dt>



Der angeforderte Vorgang kann nur in der Systemkonsole ausgeführt werden. Dies ist meistens das Ergebnis eines Treibers oder einer System-DLL, die direkten Zugriff auf die Konsole benötigt.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CLIENT_QUERY_TIMEOUT"></span><span id="error_ctx_client_query_timeout"></span>**Fehler \_ ctx- \_ Client \_ Abfrage \_ Timeout**
</dt> <dd> <dl> <dt>

7040 (0x1b80)
</dt> <dt>



Der Client konnte nicht auf die Verbindungs Nachricht des Servers Antworten.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CONSOLE_DISCONNECT"></span><span id="error_ctx_console_disconnect"></span>**Fehler beim \_ Trennen der ctx- \_ Konsole \_**
</dt> <dd> <dl> <dt>

7041 (0x1b81)
</dt> <dt>



Das Trennen der Konsolen Sitzung wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CONSOLE_CONNECT"></span><span id="error_ctx_console_connect"></span>**Fehler \_ ctx- \_ Konsolen \_ Verbindung**
</dt> <dd> <dl> <dt>

7042 (0x1b82)
</dt> <dt>



Die erneute Verbindung einer getrennten Sitzung mit der Konsole wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_SHADOW_DENIED"></span><span id="error_ctx_shadow_denied"></span>**Fehler \_ ctx, \_ Schatten \_ verweigert**
</dt> <dd> <dl> <dt>

7044 (0x1b84)
</dt> <dt>



Die Anforderung, eine andere Sitzung Remote zu steuern, wurde verweigert.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_WINSTATION_ACCESS_DENIED"></span><span id="error_ctx_winstation_access_denied"></span>**Fehler \_ ctx- \_ WinStation- \_ Zugriff \_ verweigert**
</dt> <dd> <dl> <dt>

7045 (0x1b85)
</dt> <dt>



Der angeforderte Sitzungs Zugriff wurde verweigert.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_INVALID_WD"></span><span id="error_ctx_invalid_wd"></span>**Fehler " \_ ctx" ist \_ ungültig. \_**
</dt> <dd> <dl> <dt>

7049 (0x1b89)
</dt> <dt>



Der angegebene terminalverbindungs-Treiber ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_SHADOW_INVALID"></span><span id="error_ctx_shadow_invalid"></span>**Fehler \_ ctx, \_ Schatten ist \_ ungültig.**
</dt> <dd> <dl> <dt>

7050 (0x1b8a)
</dt> <dt>



Die angeforderte Sitzung kann nicht remote gesteuert werden. Dies kann daran liegen, dass die Sitzung getrennt ist oder zurzeit kein Benutzer angemeldet ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_SHADOW_DISABLED"></span><span id="error_ctx_shadow_disabled"></span>**Fehler \_ ctx- \_ Schatten \_ deaktiviert**
</dt> <dd> <dl> <dt>

7051 (0x1b8b)
</dt> <dt>



Die angeforderte Sitzung ist nicht für die Remote Steuerung konfiguriert.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CLIENT_LICENSE_IN_USE"></span><span id="error_ctx_client_license_in_use"></span>**Fehler \_ ctx- \_ Client \_ Lizenz wird \_ \_ verwendet**
</dt> <dd> <dl> <dt>

7052 (0x1b8c)
</dt> <dt>



Ihre Anforderung zum Herstellen einer Verbindung mit diesem Terminal Server wurde abgelehnt. Ihre Terminal Server-Client Lizenznummer wird derzeit von einem anderen Benutzer verwendet. Wenden Sie sich an Ihren Systemadministrator, um eine eindeutige Lizenznummer zu erhalten.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CLIENT_LICENSE_NOT_SET"></span><span id="error_ctx_client_license_not_set"></span>**Fehler \_ ctx- \_ Client \_ Lizenz \_ nicht \_ festgelegt**
</dt> <dd> <dl> <dt>

7053 (0x1b8d)
</dt> <dt>



Ihre Anforderung zum Herstellen einer Verbindung mit diesem Terminal Server wurde abgelehnt. Die Lizenznummer des Terminal Server-Clients wurde für diese Kopie des Terminal Server Clients nicht eingegeben. Wenden Sie sich an Ihren Systemadministrator.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_LICENSE_NOT_AVAILABLE"></span><span id="error_ctx_license_not_available"></span>**Fehler- \_ ctx- \_ Lizenz \_ nicht \_ verfügbar.**
</dt> <dd> <dl> <dt>

7054 (0x1b8e)
</dt> <dt>



Die Anzahl der Verbindungen mit diesem Computer ist begrenzt, und alle Verbindungen werden momentan verwendet. Versuchen Sie, später eine Verbindung herzustellen, oder wenden Sie sich an den


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_LICENSE_CLIENT_INVALID"></span><span id="error_ctx_license_client_invalid"></span>**Fehler \_ ctx- \_ Lizenz \_ Client \_ ungültig**
</dt> <dd> <dl> <dt>

7055 (0x1b8f)
</dt> <dt>



Der von Ihnen verwendete Client ist nicht für die Verwendung dieses Systems lizenziert. Ihre Anmelde Anforderung wurde verweigert.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_LICENSE_EXPIRED"></span><span id="error_ctx_license_expired"></span>**Fehler- \_ ctx- \_ Lizenz \_ abgelaufen**
</dt> <dd> <dl> <dt>

7056 (0x1b90)
</dt> <dt>



Die System Lizenz ist abgelaufen. Ihre Anmelde Anforderung wurde verweigert.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_SHADOW_NOT_RUNNING"></span><span id="error_ctx_shadow_not_running"></span>**Fehler \_ ctx- \_ Schatten wird \_ nicht \_ ausgeführt**
</dt> <dd> <dl> <dt>

7057 (0x1b91)
</dt> <dt>



Die Remote Steuerung konnte nicht beendet werden, da die angegebene Sitzung zurzeit nicht remote gesteuert wird.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_SHADOW_ENDED_BY_MODE_CHANGE"></span><span id="error_ctx_shadow_ended_by_mode_change"></span>**Fehler \_ ctx \_ - \_ Schatten \_ wurde durch \_ Modusänderung beendet \_**
</dt> <dd> <dl> <dt>

7058 (0x1b92)
</dt> <dt>



Die Remote Steuerung der Konsole wurde beendet, weil der Anzeigemodus geändert wurde. Das Ändern des Anzeigemodus in einer Remote Steuerungs Sitzung wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACTIVATION_COUNT_EXCEEDED"></span><span id="error_activation_count_exceeded"></span>**Fehler \_ Aktivierungs \_ Anzahl \_ überschritten**
</dt> <dd> <dl> <dt>

7059 (0x1b93)
</dt> <dt>



Die Aktivierung der maximalen Anzahl von Wiederholungen für diese Installation wurde bereits zurückgesetzt. Der Aktivierungszeit Geber wird nicht gelöscht.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_WINSTATIONS_DISABLED"></span><span id="error_ctx_winstations_disabled"></span>**Fehler \_ ctx- \_ Winstations \_ deaktiviert**
</dt> <dd> <dl> <dt>

7060 (0x1b94)
</dt> <dt>



Remote Anmeldungen sind zurzeit deaktiviert.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_ENCRYPTION_LEVEL_REQUIRED"></span><span id="error_ctx_encryption_level_required"></span>**Fehler \_ ctx- \_ Verschlüsselungs \_ Stufe \_ erforderlich**
</dt> <dd> <dl> <dt>

7061 (0x1b95)
</dt> <dt>



Sie verfügen nicht über die richtige Verschlüsselungs Stufe für den Zugriff auf diese Sitzung.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_SESSION_IN_USE"></span><span id="error_ctx_session_in_use"></span>**Fehler- \_ ctx- \_ Sitzung wird \_ \_ verwendet**
</dt> <dd> <dl> <dt>

7062 (0x1b96)
</dt> <dt>



Der Benutzer "% s \\ \\ % s" ist zurzeit an diesem Computer angemeldet. Nur der aktuelle Benutzer oder ein Administrator kann sich an diesem Computer anmelden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_NO_FORCE_LOGOFF"></span><span id="error_ctx_no_force_logoff"></span>**Fehler \_ ctx \_ keine Abmeldung \_ erzwingen \_**
</dt> <dd> <dl> <dt>

7063 (0x1b97)
</dt> <dt>



Der Benutzer "% s \\ \\ % s" ist bereits in der Konsole dieses Computers angemeldet. Sie verfügen zurzeit nicht über die Berechtigung, sich anzumelden. Um dieses Problem zu beheben, wenden Sie sich an% s \\ \\ % s, und melden Sie sich ab.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_ACCOUNT_RESTRICTION"></span><span id="error_ctx_account_restriction"></span>**Fehler- \_ ctx- \_ Konto \_ Einschränkung**
</dt> <dd> <dl> <dt>

7064 (0x1b98)
</dt> <dt>



Sie können sich aufgrund einer Konto Einschränkung nicht anmelden.


</dt> </dl> </dd> <dt>

<span id="ERROR_RDP_PROTOCOL_ERROR"></span><span id="error_rdp_protocol_error"></span>**Fehler beim \_ RDP- \_ Protokoll. \_**
</dt> <dd> <dl> <dt>

7065 (0x1b99)
</dt> <dt>



Die RDP-Protokoll Komponente "%2" hat einen Fehler im Protokolldaten Strom erkannt und hat den Client getrennt.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CDM_CONNECT"></span><span id="error_ctx_cdm_connect"></span>**Fehler \_ ctx \_ CDM \_ Connect**
</dt> <dd> <dl> <dt>

7066 (0x1b9a)
</dt> <dt>



Der Client Laufwerk Zuordnungsdienst hat eine Verbindung mit der Terminal Verbindung hergestellt.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CDM_DISCONNECT"></span><span id="error_ctx_cdm_disconnect"></span>**Fehler \_ ctx- \_ CDM- \_ Trennung**
</dt> <dd> <dl> <dt>

7067 (0x1b9b)
</dt> <dt>



Der Client Laufwerk Zuordnungsdienst hat die Verbindung mit der Terminal Verbindung getrennt.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_SECURITY_LAYER_ERROR"></span><span id="error_ctx_security_layer_error"></span>**Fehler \_ ctx- \_ Sicherheits \_ Schicht \_ Fehler**
</dt> <dd> <dl> <dt>

7068 (0x1b9c)
</dt> <dt>



Die Sicherheitsschicht des Terminal Servers hat einen Fehler im Protokolldaten Strom festgestellt und den Client getrennt.


</dt> </dl> </dd> <dt>

<span id="ERROR_TS_INCOMPATIBLE_SESSIONS"></span><span id="error_ts_incompatible_sessions"></span>**Fehler \_ TS \_ inkompatible \_ Sitzungen**
</dt> <dd> <dl> <dt>

7069 (0x1b9d)
</dt> <dt>



Die Ziel Sitzung ist mit der aktuellen Sitzung nicht kompatibel.


</dt> </dl> </dd> <dt>

<span id="ERROR_TS_VIDEO_SUBSYSTEM_ERROR"></span><span id="error_ts_video_subsystem_error"></span>**Fehler \_ TS- \_ Video \_ Subsystem \_ Fehler**
</dt> <dd> <dl> <dt>

7070 (0x1b9e)
</dt> <dt>



Windows kann keine Verbindung mit ihrer Sitzung herstellen, da im Windows-Video Subsystem ein Problem aufgetreten ist. Versuchen Sie später erneut, eine Verbindung herzustellen, oder wenden Sie sich an den Server Administrator.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_INVALID_API_SEQUENCE"></span><span id="frs_err_invalid_api_sequence"></span>**FRS \_ Err \_ ungültige \_ API- \_ Sequenz**
</dt> <dd> <dl> <dt>

8001 (0x1F)
</dt> <dt>



Die Datei Replikations Dienst-API wurde falsch aufgerufen.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_STARTING_SERVICE"></span><span id="frs_err_starting_service"></span>**FRS \_ Err- \_ Start \_ Dienst**
</dt> <dd> <dl> <dt>

8002 (0x1F 42)
</dt> <dt>



Der Datei Replikations Dienst kann nicht gestartet werden.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_STOPPING_SERVICE"></span><span id="frs_err_stopping_service"></span>**FRS \_ Err \_ Dienst wird angehalten \_**
</dt> <dd> <dl> <dt>

8003 (0x1F 43)
</dt> <dt>



Der Datei Replikations Dienst kann nicht beendet werden.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_INTERNAL_API"></span><span id="frs_err_internal_api"></span>**\_interne FRS \_ - \_ API**
</dt> <dd> <dl> <dt>

8004 (0x1F 44)
</dt> <dt>



Die Datei Replikations Dienst-API hat die Anforderung beendet. Das Ereignisprotokoll kann weitere Informationen enthalten.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_INTERNAL"></span><span id="frs_err_internal"></span>**FRS \_ , \_ intern**
</dt> <dd> <dl> <dt>

8005 (0x1F)
</dt> <dt>



Der Datei Replikations Dienst hat die Anforderung beendet. Das Ereignisprotokoll kann weitere Informationen enthalten.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_SERVICE_COMM"></span><span id="frs_err_service_comm"></span>**FRS \_ Err- \_ Dienst- \_ comm**
</dt> <dd> <dl> <dt>

8006 (0x1F 46)
</dt> <dt>



Der Datei Replikations Dienst kann nicht kontaktiert werden. Das Ereignisprotokoll kann weitere Informationen enthalten.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_INSUFFICIENT_PRIV"></span><span id="frs_err_insufficient_priv"></span>**FRS \_ Err \_ nicht ausreichend \_ PRIV**
</dt> <dd> <dl> <dt>

8007 (0x1F 47)
</dt> <dt>



Der Datei Replikations Dienst kann die Anforderung nicht erfüllen, da der Benutzer nicht über ausreichende Berechtigungen verfügt. Das Ereignisprotokoll kann weitere Informationen enthalten.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_AUTHENTICATION"></span><span id="frs_err_authentication"></span>**FRS \_ Err- \_ Authentifizierung**
</dt> <dd> <dl> <dt>

8008 (0x1F 48)
</dt> <dt>



Der Datei Replikations Dienst kann die Anforderung nicht erfüllen, da der authentifizierte RPC nicht verfügbar ist. Das Ereignisprotokoll kann weitere Informationen enthalten.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_PARENT_INSUFFICIENT_PRIV"></span><span id="frs_err_parent_insufficient_priv"></span>**FRS \_ Err \_ Parent \_ nicht ausreichend \_ PRIV**
</dt> <dd> <dl> <dt>

8009 (0x1F 49)
</dt> <dt>



Der Datei Replikations Dienst kann die Anforderung nicht erfüllen, da der Benutzer nicht über ausreichende Berechtigungen auf dem Domänen Controller verfügt. Das Ereignisprotokoll kann weitere Informationen enthalten.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_PARENT_AUTHENTICATION"></span><span id="frs_err_parent_authentication"></span>**FRS \_ Err \_ Parent- \_ Authentifizierung**
</dt> <dd> <dl> <dt>

8010 (0x1F 4a)
</dt> <dt>



Der Datei Replikations Dienst kann die Anforderung nicht erfüllen, da das authentifizierte RPC auf dem Domänen Controller nicht verfügbar ist. Das Ereignisprotokoll kann weitere Informationen enthalten.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_CHILD_TO_PARENT_COMM"></span><span id="frs_err_child_to_parent_comm"></span>**FRS \_ Err \_ - \_ untergeordnetes Element zum über \_ geordneten \_ Element**
</dt> <dd> <dl> <dt>

8011 (0x1F 4B)
</dt> <dt>



Der Datei Replikations Dienst kann nicht mit dem Datei Replikations Dienst auf dem Domänen Controller kommunizieren. Das Ereignisprotokoll kann weitere Informationen enthalten.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_PARENT_TO_CHILD_COMM"></span><span id="frs_err_parent_to_child_comm"></span>**FRS \_ Err \_ übergeordnetes Element \_ zu untergeordnetem \_ \_ comm**
</dt> <dd> <dl> <dt>

8012 (0x1F 4C)
</dt> <dt>



Der Datei Replikations Dienst auf dem Domänen Controller kann nicht mit dem Datei Replikations Dienst auf diesem Computer kommunizieren. Das Ereignisprotokoll kann weitere Informationen enthalten.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_SYSVOL_POPULATE"></span><span id="frs_err_sysvol_populate"></span>**FRS \_ Err \_ Sysvol \_ Auffüllen**
</dt> <dd> <dl> <dt>

8013 (0x1F 4D)
</dt> <dt>



Der Datei Replikations Dienst kann das System Volume aufgrund eines internen Fehlers nicht auffüllen. Das Ereignisprotokoll kann weitere Informationen enthalten.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_SYSVOL_POPULATE_TIMEOUT"></span><span id="frs_err_sysvol_populate_timeout"></span>**FRS \_ - \_ Timeout für SYSVOL- \_ Auffüllen \_**
</dt> <dd> <dl> <dt>

8014 (0x1F 4E)
</dt> <dt>



Der Datei Replikations Dienst kann das System Volume aufgrund eines internen Timeouts nicht auffüllen. Das Ereignisprotokoll kann weitere Informationen enthalten.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_SYSVOL_IS_BUSY"></span><span id="frs_err_sysvol_is_busy"></span>**FRS \_ Err \_ Sysvol \_ ist \_ ausgelastet.**
</dt> <dd> <dl> <dt>

8015 (0x1F 4)
</dt> <dt>



Der Datei Replikations Dienst kann die Anforderung nicht verarbeiten. Das System Volume ist mit einer vorherigen Anforderung ausgelastet.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_SYSVOL_DEMOTE"></span><span id="frs_err_sysvol_demote"></span>**FRS \_ Err \_ Sysvol \_ Demote**
</dt> <dd> <dl> <dt>

8016 (0x1F 50)
</dt> <dt>



Der Datei Replikations Dienst kann die Replikation des Systemvolumes aufgrund eines internen Fehlers nicht beenden. Das Ereignisprotokoll kann weitere Informationen enthalten.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_INVALID_SERVICE_PARAMETER"></span><span id="frs_err_invalid_service_parameter"></span>**FRS \_ Err ( \_ ungültiger \_ Dienst \_ Parameter)**
</dt> <dd> <dl> <dt>

8017 (0x1F 51)
</dt> <dt>



Der Datei Replikations Dienst hat einen ungültigen Parameter erkannt.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Winerror. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[System Fehler Codes](system-error-codes.md)
</dt> </dl>

 

 




