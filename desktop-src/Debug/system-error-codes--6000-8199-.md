---
description: Beschreibt die Fehlercodes 6000-8199, die in der WinError.h-Headerdatei definiert sind und für Entwickler bestimmt sind.
ms.assetid: eaaf9f65-e8ff-4e54-90a9-04252cdd773a
title: Systemfehlercodes (6000-8199) (WinError.h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: d24a165798f0d4bf8a3ed534880cd3f9ad1f2b8b85d072e8a4d7aae8e6345508
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120131660"
---
# <a name="system-error-codes-6000-8199"></a>Systemfehlercodes (6000-8199)

> [!NOTE]
> Diese Informationen sind für Entwickler gedacht, die Systemfehler debuggen. Für andere Fehler, z. B. Probleme mit Windows Update, finden Sie eine Liste der Ressourcen auf der [Seite Fehlercodes.](system-error-codes.md)

In der folgenden Liste werden [die Systemfehlercodes](system-error-codes.md) (Fehler 6000 bis 8199) beschrieben. Sie werden von der [**GetLastError-Funktion**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) zurückgegeben, wenn viele Funktionen fehlschlagen. Verwenden Sie zum Abrufen des Beschreibungstexts für den Fehler in Ihrer Anwendung die [**Funktion FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) mit dem **Flag FORMAT MESSAGE FROM \_ \_ \_ SYSTEM.**

<dl> <dt>

<span id="ERROR_ENCRYPTION_FAILED"></span><span id="error_encryption_failed"></span>**FEHLER BEI \_ \_ VERSCHLÜSSELUNGSFEHLER**
</dt> <dd> <dl> <dt>

6000 (0x1770)
</dt> <dt>



Die angegebene Datei konnte nicht verschlüsselt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DECRYPTION_FAILED"></span><span id="error_decryption_failed"></span>**FEHLER \_ BEI DER ENTSCHLÜSSELUNG \_**
</dt> <dd> <dl> <dt>

6001 (0x1771)
</dt> <dt>



Die angegebene Datei konnte nicht entschlüsselt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_ENCRYPTED"></span><span id="error_file_encrypted"></span>**FEHLERDATEI \_ \_ VERSCHLÜSSELT**
</dt> <dd> <dl> <dt>

6002 (0x1772)
</dt> <dt>



Die angegebene Datei wird verschlüsselt, und der Benutzer kann sie nicht entschlüsseln.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_RECOVERY_POLICY"></span><span id="error_no_recovery_policy"></span>**FEHLER: \_ KEINE \_ \_ WIEDERHERSTELLUNGSRICHTLINIE**
</dt> <dd> <dl> <dt>

6003 (0x1773)
</dt> <dt>



Für dieses System ist keine gültige Verschlüsselungswiederherstellungsrichtlinie konfiguriert.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_EFS"></span><span id="error_no_efs"></span>**FEHLER: \_ \_ KEINE EFS**
</dt> <dd> <dl> <dt>

6004 (0x1774)
</dt> <dt>



Der erforderliche Verschlüsselungstreiber wird für dieses System nicht geladen.


</dt> </dl> </dd> <dt>

<span id="ERROR_WRONG_EFS"></span><span id="error_wrong_efs"></span>**FEHLER: \_ \_ FEHLER BEI EFS**
</dt> <dd> <dl> <dt>

6005 (0x1775)
</dt> <dt>



Die Datei wurde mit einem anderen Verschlüsselungstreiber als derzeit geladen verschlüsselt.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_USER_KEYS"></span><span id="error_no_user_keys"></span>**FEHLER: \_ \_ KEINE \_ BENUTZERSCHLÜSSEL**
</dt> <dd> <dl> <dt>

6006 (0x1776)
</dt> <dt>



Für den Benutzer sind keine EFS-Schlüssel definiert.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_NOT_ENCRYPTED"></span><span id="error_file_not_encrypted"></span>**FEHLERDATEI \_ \_ NICHT \_ VERSCHLÜSSELT**
</dt> <dd> <dl> <dt>

6007 (0x1777)
</dt> <dt>



Die angegebene Datei ist nicht verschlüsselt.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_EXPORT_FORMAT"></span><span id="error_not_export_format"></span>**FEHLER: \_ FORMAT \_ "NICHT \_ EXPORTIEREN"**
</dt> <dd> <dl> <dt>

6008 (0x1778)
</dt> <dt>



Die angegebene Datei hat nicht das definierte EFS-Exportformat.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_READ_ONLY"></span><span id="error_file_read_only"></span>**\_FEHLERDATEI \_ \_ SCHREIBGESCHÜTZT**
</dt> <dd> <dl> <dt>

6009 (0x1779)
</dt> <dt>



Die angegebene Datei ist schreibgeschützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_DIR_EFS_DISALLOWED"></span><span id="error_dir_efs_disallowed"></span>**FEHLER \_ DIR \_ EFS \_ DISALLOWED**
</dt> <dd> <dl> <dt>

6010 (0x177A)
</dt> <dt>



Das Verzeichnis wurde für die Verschlüsselung deaktiviert.


</dt> </dl> </dd> <dt>

<span id="ERROR_EFS_SERVER_NOT_TRUSTED"></span><span id="error_efs_server_not_trusted"></span>**\_FEHLER: \_ EFS-SERVER \_ NICHT \_ VERTRAUENSWÜRDIG**
</dt> <dd> <dl> <dt>

6011 (0x177B)
</dt> <dt>



Der Server ist für den Remoteverschlüsselungsvorgang nicht vertrauenswürdig.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_RECOVERY_POLICY"></span><span id="error_bad_recovery_policy"></span>**FEHLER: \_ FEHLERHAFTE \_ \_ WIEDERHERSTELLUNGSRICHTLINIE**
</dt> <dd> <dl> <dt>

6012 (0x177C)
</dt> <dt>



Die für dieses System konfigurierte Wiederherstellungsrichtlinie enthält ein ungültiges Wiederherstellungszertifikat.


</dt> </dl> </dd> <dt>

<span id="ERROR_EFS_ALG_BLOB_TOO_BIG"></span><span id="error_efs_alg_blob_too_big"></span>**FEHLER: \_ EFS \_ \_ ALG-BLOB \_ ZU \_ GROß**
</dt> <dd> <dl> <dt>

6013 (0x177D)
</dt> <dt>



Der für die Quelldatei verwendete Verschlüsselungsalgorithmus benötigt einen größeren Schlüsselpuffer als der in der Zieldatei.


</dt> </dl> </dd> <dt>

<span id="ERROR_VOLUME_NOT_SUPPORT_EFS"></span><span id="error_volume_not_support_efs"></span>**FEHLERVOLUMEN \_ \_ UNTERSTÜTZT \_ \_ EFS NICHT**
</dt> <dd> <dl> <dt>

6014 (0x177E)
</dt> <dt>



Die Datenträgerpartition unterstützt keine Dateiverschlüsselung.


</dt> </dl> </dd> <dt>

<span id="ERROR_EFS_DISABLED"></span><span id="error_efs_disabled"></span>**FEHLER: \_ EFS \_ DEAKTIVIERT**
</dt> <dd> <dl> <dt>

6015 (0x177F)
</dt> <dt>



Dieser Computer ist für die Dateiverschlüsselung deaktiviert.


</dt> </dl> </dd> <dt>

<span id="ERROR_EFS_VERSION_NOT_SUPPORT"></span><span id="error_efs_version_not_support"></span>**\_FEHLER: \_ EFS-VERSION \_ WIRD NICHT \_ UNTERSTÜTZT**
</dt> <dd> <dl> <dt>

6016 (0x1780)
</dt> <dt>



Zum Entschlüsseln dieser verschlüsselten Datei ist ein neueres System erforderlich.


</dt> </dl> </dd> <dt>

<span id="ERROR_CS_ENCRYPTION_INVALID_SERVER_RESPONSE"></span><span id="error_cs_encryption_invalid_server_response"></span>**FEHLER CS \_ \_ ENCRYPTION INVALID SERVER \_ \_ \_ RESPONSE**
</dt> <dd> <dl> <dt>

6017 (0x1781)
</dt> <dt>



Der Remoteserver hat eine ungültige Antwort für eine Datei gesendet, die mit clientseitiger Verschlüsselung geöffnet wird.


</dt> </dl> </dd> <dt>

<span id="ERROR_CS_ENCRYPTION_UNSUPPORTED_SERVER"></span><span id="error_cs_encryption_unsupported_server"></span>**FEHLER \_ CS \_ ENCRYPTION \_ UNSUPPORTED \_ SERVER**
</dt> <dd> <dl> <dt>

6018 (0x1782)
</dt> <dt>



Die clientseitige Verschlüsselung wird vom Remoteserver nicht unterstützt, obwohl er diese unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_CS_ENCRYPTION_EXISTING_ENCRYPTED_FILE"></span><span id="error_cs_encryption_existing_encrypted_file"></span>**FEHLER: \_ CS ENCRYPTION EXISTING ENCRYPTED \_ \_ \_ \_ FILE**
</dt> <dd> <dl> <dt>

6019 (0x1783)
</dt> <dt>



Die Datei ist verschlüsselt und sollte im Clientseitigen Verschlüsselungsmodus geöffnet werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CS_ENCRYPTION_NEW_ENCRYPTED_FILE"></span><span id="error_cs_encryption_new_encrypted_file"></span>**FEHLER: \_ CS ENCRYPTION NEW ENCRYPTED \_ \_ \_ \_ FILE**
</dt> <dd> <dl> <dt>

6020 (0x1784)
</dt> <dt>



Es wird eine neue verschlüsselte Datei erstellt, und $EFS muss bereitgestellt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CS_ENCRYPTION_FILE_NOT_CSE"></span><span id="error_cs_encryption_file_not_cse"></span>**FEHLER: \_ \_ CS-VERSCHLÜSSELUNGSDATEI \_ \_ NICHT \_ CSE**
</dt> <dd> <dl> <dt>

6021 (0x1785)
</dt> <dt>



Der SMB-Client hat eine CSE FSCTL für eine Nicht-CSE-Datei angefordert.


</dt> </dl> </dd> <dt>

<span id="ERROR_ENCRYPTION_POLICY_DENIES_OPERATION"></span><span id="error_encryption_policy_denies_operation"></span>**\_ \_ FEHLERVERSCHLÜSSELUNGSRICHTLINIE VERWEIGERT \_ \_ VORGANG**
</dt> <dd> <dl> <dt>

6022 (0x1786)
</dt> <dt>



Der angeforderte Vorgang wurde durch die Richtlinie blockiert. Weitere Informationen erhalten Sie von Ihrem Systemadministrator.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_BROWSER_SERVERS_FOUND"></span><span id="error_no_browser_servers_found"></span>**FEHLER \_ KEINE \_ \_ BROWSERSERVER \_ GEFUNDEN**
</dt> <dd> <dl> <dt>

6118 (0x17E6)
</dt> <dt>



Die Liste der Server für diese Arbeitsgruppe ist derzeit nicht verfügbar.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_SERVICE_NOT_LOCALSYSTEM"></span><span id="sched_e_service_not_localsystem"></span>**SCHED \_ E \_ SERVICE \_ NOT \_ LOCALSYSTEM**
</dt> <dd> <dl> <dt>

6200 (0x1838)
</dt> <dt>



Der Taskplaner muss so konfiguriert sein, dass er im Systemkonto ausgeführt wird, damit er ordnungsgemäß funktioniert. Einzelne Aufgaben können für die Ausführung in anderen Konten konfiguriert werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_SECTOR_INVALID"></span><span id="error_log_sector_invalid"></span>**\_ \_ FEHLERPROTOKOLLBEREICH \_ UNGÜLTIG**
</dt> <dd> <dl> <dt>

6600 (0x19C8)
</dt> <dt>



Beim Protokolldienst ist ein ungültiger Protokollsektor aufgetreten.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_SECTOR_PARITY_INVALID"></span><span id="error_log_sector_parity_invalid"></span>**\_ \_ FEHLERPROTOKOLL: \_ SEKTORPARITÄT \_ UNGÜLTIG**
</dt> <dd> <dl> <dt>

6601 (0x19C9)
</dt> <dt>



Der Protokolldienst hat einen Protokollsektor mit ungültiger Blockparität festgestellt.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_SECTOR_REMAPPED"></span><span id="error_log_sector_remapped"></span>**NEU \_ \_ ZUGEORDNETER \_ FEHLERPROTOKOLLBEREICH**
</dt> <dd> <dl> <dt>

6602 (0x19CA)
</dt> <dt>



Der Protokolldienst hat einen neu zugeordneten Protokollsektor gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_BLOCK_INCOMPLETE"></span><span id="error_log_block_incomplete"></span>**\_ \_ FEHLERPROTOKOLLBLOCK \_ UNVOLLSTÄNDIG**
</dt> <dd> <dl> <dt>

6603 (0x19CB)
</dt> <dt>



Der Protokolldienst hat einen partiellen oder unvollständigen Protokollblock gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_INVALID_RANGE"></span><span id="error_log_invalid_range"></span>**FEHLERPROTOKOLL \_ \_ UNGÜLTIGER \_ BEREICH**
</dt> <dd> <dl> <dt>

6604 (0x19CC)
</dt> <dt>



Der Protokolldienst hat versucht, außerhalb des aktiven Protokollbereichs auf Daten zu zugreifen.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_BLOCKS_EXHAUSTED"></span><span id="error_log_blocks_exhausted"></span>**\_ \_ FEHLERPROTOKOLLBLÖCKE \_ ERSCHÖPFT**
</dt> <dd> <dl> <dt>

6605 (0x19CD)
</dt> <dt>



Die Marshallingpuffer des Protokolldienstbenutzers sind erschöpft.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_READ_CONTEXT_INVALID"></span><span id="error_log_read_context_invalid"></span>**\_ \_ FEHLERPROTOKOLLLESEKONTEXT \_ \_ UNGÜLTIG**
</dt> <dd> <dl> <dt>

6606 (0x19CE)
</dt> <dt>



Der Protokolldienst hat versucht, aus einem Marshallingbereich mit einem ungültigen Lesekontext zu lesen.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_RESTART_INVALID"></span><span id="error_log_restart_invalid"></span>**\_ \_ FEHLERPROTOKOLLNEUSTART \_ UNGÜLTIG**
</dt> <dd> <dl> <dt>

6607 (0x19CF)
</dt> <dt>



Der Protokolldienst hat einen ungültigen Protokollneustartbereich gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_BLOCK_VERSION"></span><span id="error_log_block_version"></span>**\_ \_ \_ FEHLERPROTOKOLLBLOCKVERSION**
</dt> <dd> <dl> <dt>

6608 (0x19D0)
</dt> <dt>



Der Protokolldienst hat eine ungültige Protokollblockversion gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_BLOCK_INVALID"></span><span id="error_log_block_invalid"></span>**\_ \_ FEHLERPROTOKOLLBLOCK \_ UNGÜLTIG**
</dt> <dd> <dl> <dt>

6609 (0x19D1)
</dt> <dt>



Der Protokolldienst hat einen ungültigen Protokollblock gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_READ_MODE_INVALID"></span><span id="error_log_read_mode_invalid"></span>**\_ \_ FEHLERPROTOKOLLLESEMODUS \_ \_ UNGÜLTIG**
</dt> <dd> <dl> <dt>

6610 (0x19D2)
</dt> <dt>



Der Protokolldienst hat versucht, das Protokoll mit einem ungültigen Lesemodus zu lesen.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_NO_RESTART"></span><span id="error_log_no_restart"></span>**FEHLERPROTOKOLL \_ \_ KEIN \_ NEUSTART**
</dt> <dd> <dl> <dt>

6611 (0x19D3)
</dt> <dt>



Der Protokolldienst hat einen Protokolldatenstrom ohne Neustartbereich gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_METADATA_CORRUPT"></span><span id="error_log_metadata_corrupt"></span>**\_ \_ FEHLERPROTOKOLLMETADATEN \_ BESCHÄDIGT**
</dt> <dd> <dl> <dt>

6612 (0x19D4)
</dt> <dt>



Der Protokolldienst hat eine beschädigte Metadatendatei gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_METADATA_INVALID"></span><span id="error_log_metadata_invalid"></span>**\_ \_ FEHLERPROTOKOLLMETADATEN \_ UNGÜLTIG**
</dt> <dd> <dl> <dt>

6613 (0x19D5)
</dt> <dt>



Der Protokolldienst hat eine Metadatendatei gefunden, die vom Protokolldateisystem nicht erstellt werden konnte.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_METADATA_INCONSISTENT"></span><span id="error_log_metadata_inconsistent"></span>**\_ \_ FEHLERPROTOKOLLMETADATEN \_ INKONSISTENT**
</dt> <dd> <dl> <dt>

6614 (0x19D6)
</dt> <dt>



Der Protokolldienst hat eine Metadatendatei mit inkonsistenten Daten gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_RESERVATION_INVALID"></span><span id="error_log_reservation_invalid"></span>**\_ \_ FEHLERPROTOKOLLRESERVIERUNG \_ UNGÜLTIG**
</dt> <dd> <dl> <dt>

6615 (0x19D7)
</dt> <dt>



Der Protokolldienst hat versucht, fälschlicherweise Reservierungsspeicherplatz zu reservieren oder zu veräußern.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CANT_DELETE"></span><span id="error_log_cant_delete"></span>**FEHLERPROTOKOLL \_ \_ KANN NICHT GELÖSCHT \_ WERDEN**
</dt> <dd> <dl> <dt>

6616 (0x19D8)
</dt> <dt>



Der Protokolldienst kann keine Protokolldatei oder keinen Dateisystemcontainer löschen.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CONTAINER_LIMIT_EXCEEDED"></span><span id="error_log_container_limit_exceeded"></span>**\_ \_ FEHLERPROTOKOLLCONTAINERLIMIT \_ \_ ÜBERSCHRITTEN**
</dt> <dd> <dl> <dt>

6617 (0x19D9)
</dt> <dt>



Der Protokolldienst hat die maximal zulässige Anzahl von Containern erreicht, die einer Protokolldatei zugeordnet sind.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_START_OF_LOG"></span><span id="error_log_start_of_log"></span>**\_ \_ FEHLERPROTOKOLL: \_ \_ PROTOKOLLSTART**
</dt> <dd> <dl> <dt>

6618 (0x19DA)
</dt> <dt>



Der Protokolldienst hat versucht, nach dem Beginn des Protokolls rückwärts zu lesen oder zu schreiben.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_POLICY_ALREADY_INSTALLED"></span><span id="error_log_policy_already_installed"></span>**\_ \_ FEHLERPROTOKOLLRICHTLINIE BEREITS \_ \_ INSTALLIERT**
</dt> <dd> <dl> <dt>

6619 (0x19DB)
</dt> <dt>



Die Protokollrichtlinie konnte nicht installiert werden, da bereits eine Richtlinie desselben Typs vorhanden ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_POLICY_NOT_INSTALLED"></span><span id="error_log_policy_not_installed"></span>**\_ \_ FEHLERPROTOKOLLRICHTLINIE NICHT \_ \_ INSTALLIERT**
</dt> <dd> <dl> <dt>

6620 (0x19DC)
</dt> <dt>



Die protokollierte Richtlinie wurde zum Zeitpunkt der Anforderung nicht installiert.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_POLICY_INVALID"></span><span id="error_log_policy_invalid"></span>**\_ \_ FEHLERPROTOKOLLRICHTLINIE \_ UNGÜLTIG**
</dt> <dd> <dl> <dt>

6621 (0x19DD)
</dt> <dt>



Der im Protokoll installierte Satz von Richtlinien ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_POLICY_CONFLICT"></span><span id="error_log_policy_conflict"></span>**\_ \_ \_ FEHLERPROTOKOLLRICHTLINIENKONFLIKT**
</dt> <dd> <dl> <dt>

6622 (0x19DE)
</dt> <dt>



Eine Richtlinie für das protokoll in Frage hat verhindert, dass der Vorgang abgeschlossen wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_PINNED_ARCHIVE_TAIL"></span><span id="error_log_pinned_archive_tail"></span>**\_ \_ FEHLERPROTOKOLL- ANGEHEFTETER \_ \_ ARCHIV-TAIL**
</dt> <dd> <dl> <dt>

6623 (0x19DF)
</dt> <dt>



Protokollspeicherplatz kann nicht wiedergefordert werden, da das Protokoll vom Archiv-Ende angeheftet wird.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_RECORD_NONEXISTENT"></span><span id="error_log_record_nonexistent"></span>**\_ \_ FEHLERPROTOKOLLDATENSATZ \_ NICHT VORHANDEN**
</dt> <dd> <dl> <dt>

6624 (0x19E0)
</dt> <dt>



Der Protokolldatensatz ist kein Datensatz in der Protokolldatei.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_RECORDS_RESERVED_INVALID"></span><span id="error_log_records_reserved_invalid"></span>**RESERVIERTE \_ \_ FEHLERPROTOKOLLDATENSÄTZE \_ \_ UNGÜLTIG**
</dt> <dd> <dl> <dt>

6625 (0x19E1)
</dt> <dt>



Die Anzahl reservierter Protokolldatensätze oder die Anpassung der Anzahl reservierter Protokolldatensätze ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_SPACE_RESERVED_INVALID"></span><span id="error_log_space_reserved_invalid"></span>**\_RESERVIERTER \_ \_ FEHLERPROTOKOLLSPEICHERPLATZ \_ UNGÜLTIG**
</dt> <dd> <dl> <dt>

6626 (0x19E2)
</dt> <dt>



Reservierter Protokollspeicherplatz oder die Anpassung des Protokollspeicherplatzes ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_TAIL_INVALID"></span><span id="error_log_tail_invalid"></span>**FEHLERPROTOKOLL \_ \_ TAIL \_ INVALID**
</dt> <dd> <dl> <dt>

6627 (0x19E3)
</dt> <dt>



Ein neues oder vorhandenes Archivdetail oder eine basis des aktiven Protokolls ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_FULL"></span><span id="error_log_full"></span>**FEHLERPROTOKOLL \_ \_ VOLLSTÄNDIG**
</dt> <dd> <dl> <dt>

6628 (0x19E4)
</dt> <dt>



Der Protokollspeicherplatz ist erschöpft.


</dt> </dl> </dd> <dt>

<span id="ERROR_COULD_NOT_RESIZE_LOG"></span><span id="error_could_not_resize_log"></span>**FEHLER: \_ DIE GRÖßE DES PROTOKOLLS KONNTE NICHT GEÄNDERT \_ \_ \_ WERDEN.**
</dt> <dd> <dl> <dt>

6629 (0x19E5)
</dt> <dt>



Das Protokoll konnte nicht auf die angeforderte Größe festgelegt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_MULTIPLEXED"></span><span id="error_log_multiplexed"></span>**FEHLERPROTOKOLL \_ \_ MULTIPLEXED**
</dt> <dd> <dl> <dt>

6630 (0x19E6)
</dt> <dt>



Das Protokoll ist multiplexiert, es sind keine direkten Schreibvorgänge in das physische Protokoll zulässig.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_DEDICATED"></span><span id="error_log_dedicated"></span>**FEHLERPROTOKOLL \_ \_ DE DEDICATED**
</dt> <dd> <dl> <dt>

6631 (0x19E7)
</dt> <dt>



Fehler beim Vorgang, da es sich bei dem Protokoll um ein dediziertes Protokoll handelt.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_ARCHIVE_NOT_IN_PROGRESS"></span><span id="error_log_archive_not_in_progress"></span>**\_FEHLERPROTOKOLLARCHIV WIRD NICHT IN \_ \_ \_ \_ BEARBEITUNG**
</dt> <dd> <dl> <dt>

6632 (0x19E8)
</dt> <dt>



Der Vorgang erfordert einen Archivkontext.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_ARCHIVE_IN_PROGRESS"></span><span id="error_log_archive_in_progress"></span>**\_ \_ FEHLERPROTOKOLLARCHIV WIRD IN \_ \_ BEARBEITUNG**
</dt> <dd> <dl> <dt>

6633 (0x19E9)
</dt> <dt>



Die Protokollarchivierung wird in Bearbeitung.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_EPHEMERAL"></span><span id="error_log_ephemeral"></span>**FEHLERPROTOKOLL \_ \_ KURZLEBIG**
</dt> <dd> <dl> <dt>

6634 (0x19EA)
</dt> <dt>



Der Vorgang erfordert ein nicht kurzlebiger Protokoll, aber das Protokoll ist kurzlebig.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_NOT_ENOUGH_CONTAINERS"></span><span id="error_log_not_enough_containers"></span>**FEHLERPROTOKOLL \_ \_ NICHT GENÜGEND \_ \_ CONTAINER**
</dt> <dd> <dl> <dt>

6635 (0x19EB)
</dt> <dt>



Das Protokoll muss über mindestens zwei Container verfügen, bevor es gelesen oder geschrieben werden kann.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CLIENT_ALREADY_REGISTERED"></span><span id="error_log_client_already_registered"></span>**\_ \_ FEHLERPROTOKOLLCLIENT BEREITS \_ \_ REGISTRIERT**
</dt> <dd> <dl> <dt>

6636 (0x19EC)
</dt> <dt>



Ein Protokollclient wurde bereits für den Stream registriert.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CLIENT_NOT_REGISTERED"></span><span id="error_log_client_not_registered"></span>**\_ \_ FEHLERPROTOKOLLCLIENT NICHT \_ \_ REGISTRIERT**
</dt> <dd> <dl> <dt>

6637 (0x19ED)
</dt> <dt>



Ein Protokollclient wurde nicht für den Stream registriert.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_FULL_HANDLER_IN_PROGRESS"></span><span id="error_log_full_handler_in_progress"></span>**ERROR \_ LOG \_ FULL \_ HANDLER \_ IN \_ PROGRESS**
</dt> <dd> <dl> <dt>

6638 (0x19EE)
</dt> <dt>



Es wurde bereits eine Anforderung zum Verarbeiten der vollständigen Protokollbedingung gestellt.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CONTAINER_READ_FAILED"></span><span id="error_log_container_read_failed"></span>**\_ \_ FEHLERPROTOKOLL: FEHLER BEIM LESEN DES CONTAINERS \_ \_**
</dt> <dd> <dl> <dt>

6639 (0x19EF)
</dt> <dt>



Der Protokolldienst hat beim Versuch, aus einem Protokollcontainer zu lesen, einen Fehler festgestellt.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CONTAINER_WRITE_FAILED"></span><span id="error_log_container_write_failed"></span>**\_ \_ FEHLERPROTOKOLL: FEHLER BEIM SCHREIBEN DES CONTAINERS \_ \_**
</dt> <dd> <dl> <dt>

6640 (0x19F0)
</dt> <dt>



Beim Versuch, in einen Protokollcontainer zu schreiben, ist beim Protokolldienst ein Fehler aufgetreten.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CONTAINER_OPEN_FAILED"></span><span id="error_log_container_open_failed"></span>**\_FEHLERPROTOKOLL: FEHLER BEIM \_ ÖFFNEN DES CONTAINERS \_ \_**
</dt> <dd> <dl> <dt>

6641 (0x19F1)
</dt> <dt>



Der Protokolldienst hat beim Öffnen eines Protokollcontainers einen Fehler festgestellt.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CONTAINER_STATE_INVALID"></span><span id="error_log_container_state_invalid"></span>**\_ \_ FEHLERPROTOKOLLCONTAINERSTATUS \_ \_ UNGÜLTIG**
</dt> <dd> <dl> <dt>

6642 (0x19F2)
</dt> <dt>



Der Protokolldienst hat beim Versuch, eine angeforderte Aktion zu versuchen, einen ungültigen Containerstatus festgestellt.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_STATE_INVALID"></span><span id="error_log_state_invalid"></span>**\_ \_ FEHLERPROTOKOLLZUSTAND \_ UNGÜLTIG**
</dt> <dd> <dl> <dt>

6643 (0x19F3)
</dt> <dt>



Der Protokolldienst befindet sich nicht im richtigen Zustand, um eine angeforderte Aktion auszuführen.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_PINNED"></span><span id="error_log_pinned"></span>**FEHLERPROTOKOLL \_ \_ ANGEHEFTET**
</dt> <dd> <dl> <dt>

6644 (0x19F4)
</dt> <dt>



Der Protokollspeicherplatz kann nicht freigefordert werden, da das Protokoll angeheftet ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_METADATA_FLUSH_FAILED"></span><span id="error_log_metadata_flush_failed"></span>**\_FEHLER \_ BEIM LEEREN VON \_ PROTOKOLLMETADATEN \_**
</dt> <dd> <dl> <dt>

6645 (0x19F5)
</dt> <dt>



Fehler beim Leeren von Protokollmetadaten.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_INCONSISTENT_SECURITY"></span><span id="error_log_inconsistent_security"></span>**\_ \_ INKONSISTENTE SICHERHEIT DES \_ FEHLERPROTOKOLLS**
</dt> <dd> <dl> <dt>

6646 (0x19F6)
</dt> <dt>



Die Sicherheit im Protokoll und seinen Containern ist inkonsistent.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_APPENDED_FLUSH_FAILED"></span><span id="error_log_appended_flush_failed"></span>**FEHLER BEIM LEEREN DES \_ ANGEFÜGTEN FEHLERPROTOKOLLS \_ \_ \_**
</dt> <dd> <dl> <dt>

6647 (0x19F7)
</dt> <dt>



Datensätze wurden an das Protokoll angefügt, oder Es wurden Reservierungsänderungen vorgenommen, aber das Protokoll konnte nicht geleert werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_PINNED_RESERVATION"></span><span id="error_log_pinned_reservation"></span>**FEHLERPROTOKOLL \_ \_ : ANGEHEFTETE \_ RESERVIERUNG**
</dt> <dd> <dl> <dt>

6648 (0x19F8)
</dt> <dt>



Das Protokoll wird angeheftet, weil die Reservierung den größten Teil des Protokollspeicherplatzes verbraucht. Freigeben einiger reservierter Datensätze, um Speicherplatz verfügbar zu machen.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_TRANSACTION"></span><span id="error_invalid_transaction"></span>**FEHLER: \_ UNGÜLTIGE \_ TRANSAKTION**
</dt> <dd> <dl> <dt>

6700 (0x1A2C)
</dt> <dt>



Das diesem Vorgang zugeordnete Transaktionshandle ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_NOT_ACTIVE"></span><span id="error_transaction_not_active"></span>**FEHLERTRANSAKTION \_ \_ NICHT \_ AKTIV**
</dt> <dd> <dl> <dt>

6701 (0x1A2D)
</dt> <dt>



Der angeforderte Vorgang wurde im Kontext einer Transaktion ausgeführt, die nicht mehr aktiv ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_REQUEST_NOT_VALID"></span><span id="error_transaction_request_not_valid"></span>**FEHLER: \_ \_ TRANSAKTIONSANFORDERUNG \_ \_ UNGÜLTIG**
</dt> <dd> <dl> <dt>

6702 (0x1A2E)
</dt> <dt>



Der angeforderte Vorgang ist für das Transaction-Objekt im aktuellen Zustand ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_NOT_REQUESTED"></span><span id="error_transaction_not_requested"></span>**FEHLERTRANSAKTION \_ \_ NICHT \_ ANGEFORDERT**
</dt> <dd> <dl> <dt>

6703 (0x1A2F)
</dt> <dt>



Der Aufrufer hat eine Antwort-API aufgerufen, aber die Antwort wird nicht erwartet, da der TM die entsprechende Anforderung nicht an den Aufrufer ausgegeben hat.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_ALREADY_ABORTED"></span><span id="error_transaction_already_aborted"></span>**FEHLERTRANSAKTION \_ \_ WURDE BEREITS \_ ABGEBROCHEN**
</dt> <dd> <dl> <dt>

6704 (0x1A30)
</dt> <dt>



Es ist zu spät, den angeforderten Vorgang auszuführen, da die Transaktion bereits abgebrochen wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_ALREADY_COMMITTED"></span><span id="error_transaction_already_committed"></span>**FEHLERTRANSAKTION \_ \_ WURDE BEREITS \_ AUSGEFÜHRT**
</dt> <dd> <dl> <dt>

6705 (0x1A31)
</dt> <dt>



Es ist zu spät, den angeforderten Vorgang auszuführen, da für die Transaktion bereits ein Commit ausgeführt wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_TM_INITIALIZATION_FAILED"></span><span id="error_tm_initialization_failed"></span>**FEHLER BEI \_ \_ TM-INITIALISIERUNGSFEHLER \_**
</dt> <dd> <dl> <dt>

6706 (0x1A32)
</dt> <dt>



Der Transaktions-Manager konnte nicht erfolgreich initialisiert werden. Transaktive Vorgänge werden nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCEMANAGER_READ_ONLY"></span><span id="error_resourcemanager_read_only"></span>**FEHLER \_ RESOURCEMANAGER \_ READ \_ ONLY**
</dt> <dd> <dl> <dt>

6707 (0x1A33)
</dt> <dt>



Der angegebene ResourceManager hat keine Änderungen oder Aktualisierungen an der Ressource unter dieser Transaktion vorgenommen.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_NOT_JOINED"></span><span id="error_transaction_not_joined"></span>**FEHLERTRANSAKTION \_ \_ NICHT \_ VERKNÜPFT**
</dt> <dd> <dl> <dt>

6708 (0x1A34)
</dt> <dt>



Der Ressourcen-Manager hat versucht, eine Transaktion vorzubereiten, der er nicht erfolgreich beigetreten ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_SUPERIOR_EXISTS"></span><span id="error_transaction_superior_exists"></span>**FEHLER \_ TRANSACTION \_ SUPERIOR \_ EXISTS**
</dt> <dd> <dl> <dt>

6709 (0x1A35)
</dt> <dt>



Das Transaction-Objekt verfügt bereits über eine übergeordnete Eintragung, und der Aufrufer hat versucht, einen Vorgang durchzuführen, der einen neuen übergeordneten Erstellt hätte. Nur eine einzelne übergeordnete Eintragung ist zulässig.


</dt> </dl> </dd> <dt>

<span id="ERROR_CRM_PROTOCOL_ALREADY_EXISTS"></span><span id="error_crm_protocol_already_exists"></span>**ERROR \_ CRM \_ PROTOCOL \_ ALREADY \_ EXISTS**
</dt> <dd> <dl> <dt>

6710 (0x1A36)
</dt> <dt>



Der RM hat versucht, ein protokoll zu registrieren, das bereits vorhanden ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_PROPAGATION_FAILED"></span><span id="error_transaction_propagation_failed"></span>**\_FEHLER \_ BEI TRANSAKTIONSWEITERGABEFEHLER \_**
</dt> <dd> <dl> <dt>

6711 (0x1A37)
</dt> <dt>



Fehler beim Versuch, die Transaktion zu propagieren.


</dt> </dl> </dd> <dt>

<span id="ERROR_CRM_PROTOCOL_NOT_FOUND"></span><span id="error_crm_protocol_not_found"></span>**FEHLER: \_ \_ CRM-PROTOKOLL \_ NICHT \_ GEFUNDEN**
</dt> <dd> <dl> <dt>

6712 (0x1A38)
</dt> <dt>



Das angeforderte Weitergabeprotokoll wurde nicht als CRM registriert.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_INVALID_MARSHALL_BUFFER"></span><span id="error_transaction_invalid_marshall_buffer"></span>**FEHLERTRANSAKTION \_ \_ UNGÜLTIGER \_ \_ MARSHALLPUFFER**
</dt> <dd> <dl> <dt>

6713 (0x1A39)
</dt> <dt>



Der an PushTransaction oder PullTransaction übergebene Puffer hat kein gültiges Format.


</dt> </dl> </dd> <dt>

<span id="ERROR_CURRENT_TRANSACTION_NOT_VALID"></span><span id="error_current_transaction_not_valid"></span>**FEHLER \_ BEI DER AKTUELLEN TRANSAKTION \_ \_ \_ UNGÜLTIG**
</dt> <dd> <dl> <dt>

6714 (0x1A3A)
</dt> <dt>



Der dem Thread zugeordnete aktuelle Transaktionskontext ist kein gültiges Handle für ein Transaktionsobjekt.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_NOT_FOUND"></span><span id="error_transaction_not_found"></span>**FEHLERTRANSAKTION \_ \_ NICHT \_ GEFUNDEN**
</dt> <dd> <dl> <dt>

6715 (0x1A3B)
</dt> <dt>



Das angegebene Transaktionsobjekt konnte nicht geöffnet werden, da es nicht gefunden wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCEMANAGER_NOT_FOUND"></span><span id="error_resourcemanager_not_found"></span>**FEHLER \_ RESOURCEMANAGER \_ NICHT \_ GEFUNDEN**
</dt> <dd> <dl> <dt>

6716 (0x1A3C)
</dt> <dt>



Das angegebene ResourceManager-Objekt konnte nicht geöffnet werden, da es nicht gefunden wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_ENLISTMENT_NOT_FOUND"></span><span id="error_enlistment_not_found"></span>**FEHLER \_ BEIM EINTRAG NICHT \_ \_ GEFUNDEN**
</dt> <dd> <dl> <dt>

6717 (0x1A3D)
</dt> <dt>



Das angegebene Eintragungsobjekt konnte nicht geöffnet werden, da es nicht gefunden wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTIONMANAGER_NOT_FOUND"></span><span id="error_transactionmanager_not_found"></span>**FEHLER \_ TRANSACTIONMANAGER \_ NICHT \_ GEFUNDEN**
</dt> <dd> <dl> <dt>

6718 (0x1A3E)
</dt> <dt>



Das angegebene TransactionManager-Objekt konnte nicht geöffnet werden, da es nicht gefunden wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTIONMANAGER_NOT_ONLINE"></span><span id="error_transactionmanager_not_online"></span>**FEHLER \_ TRANSACTIONMANAGER \_ NICHT \_ ONLINE**
</dt> <dd> <dl> <dt>

6719 (0x1A3F)
</dt> <dt>



Das angegebene Objekt konnte nicht erstellt oder geöffnet werden, da sein zugeordneter TransactionManager nicht online ist. TransactionManager muss vollständig online geschaltet werden, indem RecoverTransactionManager aufgerufen wird, um die Wiederherstellung bis zum Ende der LogFile-Datei durchzuführen, bevor Objekte in seinen Transaction- oder ResourceManager-Namespaces geöffnet werden können. Darüber hinaus können Fehler beim Schreiben von Datensätzen in logFile dazu führen, dass ein TransactionManager offline geschaltet wird.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTIONMANAGER_RECOVERY_NAME_COLLISION"></span><span id="error_transactionmanager_recovery_name_collision"></span>**ERROR \_ TRANSACTIONMANAGER \_ RECOVERY \_ NAME \_ COLLISION**
</dt> <dd> <dl> <dt>

6720 (0x1A40)
</dt> <dt>



Der angegebene TransactionManager konnte die in seiner Protokolldatei enthaltenen Objekte im Ob-Namespace nicht erstellen. Daher konnte der TransactionManager nicht wiederhergestellt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_NOT_ROOT"></span><span id="error_transaction_not_root"></span>**FEHLERTRANSAKTION \_ \_ NICHT \_ ROOT**
</dt> <dd> <dl> <dt>

6721 (0x1A41)
</dt> <dt>



Der Aufruf zum Erstellen einer übergeordneten Eintragung für dieses Transaktionsobjekt konnte nicht abgeschlossen werden, da das für die Eintragung angegebene Transaktionsobjekt ein untergeordneter Branch der Transaktion ist. Nur der Stamm der Transaktion kann als übergeordnetes Mitglied eingetragen werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_OBJECT_EXPIRED"></span><span id="error_transaction_object_expired"></span>**FEHLER \_ \_ TRANSAKTIONSOBJEKT \_ ABGELAUFEN**
</dt> <dd> <dl> <dt>

6722 (0x1A42)
</dt> <dt>



Da der zugeordnete Transaktions-Manager oder Ressourcen-Manager geschlossen wurde, ist das Handle nicht mehr gültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_RESPONSE_NOT_ENLISTED"></span><span id="error_transaction_response_not_enlisted"></span>**\_ \_ FEHLERTRANSAKTIONSANTWORT \_ NICHT \_ EINGETRAGEN**
</dt> <dd> <dl> <dt>

6723 (0x1A43)
</dt> <dt>



Der angegebene Vorgang konnte für diese übergeordnete Eintragung nicht ausgeführt werden, da die Eintragung nicht mit der entsprechenden Abschlussantwort in der NotificationMask erstellt wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_RECORD_TOO_LONG"></span><span id="error_transaction_record_too_long"></span>**\_ \_ FEHLERTRANSAKTIONSDATENSATZ \_ ZU \_ LANG**
</dt> <dd> <dl> <dt>

6724 (0x1A44)
</dt> <dt>



Der angegebene Vorgang konnte nicht ausgeführt werden, da der protokollierte Datensatz zu lang war. Dies kann aufgrund von zwei Bedingungen auftreten: Entweder sind zu viele Eintragungen für diese Transaktion vorhanden, oder die kombinierte RecoveryInformation, die im Namen dieser Eintragungen protokolliert wird, ist zu lang.


</dt> </dl> </dd> <dt>

<span id="ERROR_IMPLICIT_TRANSACTION_NOT_SUPPORTED"></span><span id="error_implicit_transaction_not_supported"></span>**FEHLER \_ IMPLIZITE \_ TRANSAKTION WIRD NICHT \_ \_ UNTERSTÜTZT**
</dt> <dd> <dl> <dt>

6725 (0x1A45)
</dt> <dt>



Implizite Transaktionen werden nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_INTEGRITY_VIOLATED"></span><span id="error_transaction_integrity_violated"></span>**FEHLER \_ DER \_ TRANSAKTIONSINTEGRITÄT \_ VERLETZT**
</dt> <dd> <dl> <dt>

6726 (0x1A46)
</dt> <dt>



Der Kerneltransaktions-Manager musste die Transaktion abbrechen oder vergessen, da der Fortschritt blockiert wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTIONMANAGER_IDENTITY_MISMATCH"></span><span id="error_transactionmanager_identity_mismatch"></span>**ERROR \_ TRANSACTIONMANAGER \_ IDENTITY \_ MISMATCH**
</dt> <dd> <dl> <dt>

6727 (0x1A47)
</dt> <dt>



Die angegebene TransactionManager-Identität stimmte nicht mit der identität überein, die in der Protokolldatei von TransactionManager aufgezeichnet wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_RM_CANNOT_BE_FROZEN_FOR_SNAPSHOT"></span><span id="error_rm_cannot_be_frozen_for_snapshot"></span>**FEHLER \_ RM KANN FÜR \_ \_ \_ \_ \_ MOMENTAUFNAHME NICHT FIXIERT WERDEN**
</dt> <dd> <dl> <dt>

6728 (0x1A48)
</dt> <dt>



Dieser Momentaufnahmevorgang kann nicht fortgesetzt werden, da ein Transaktionsressourcen-Manager im aktuellen Zustand nicht fixiert werden kann. Versuchen Sie es erneut.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_MUST_WRITETHROUGH"></span><span id="error_transaction_must_writethrough"></span>**FEHLERTRANSAKTION \_ \_ MUSS \_ DURCHGESCHRIEBEN WERDEN**
</dt> <dd> <dl> <dt>

6729 (0x1A49)
</dt> <dt>



Die Transaktion kann nicht mit der angegebenen EnlistmentMask eingetragen werden, da die PrePrepare-Phase der Transaktion bereits abgeschlossen wurde. Um die Richtigkeit sicherzustellen, muss resourceManager in einen Schreibmodus wechseln und das Zwischenspeichern von Daten innerhalb dieser Transaktion beenden. Die Eintragung nur für nachfolgende Transaktionsphasen ist möglicherweise noch erfolgreich.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_NO_SUPERIOR"></span><span id="error_transaction_no_superior"></span>**FEHLERTRANSAKTION \_ \_ KEINE \_ ÜBERLEGENE**
</dt> <dd> <dl> <dt>

6730 (0x1A4A)
</dt> <dt>



Die Transaktion verfügt nicht über eine übergeordnete Eintragung.


</dt> </dl> </dd> <dt>

<span id="ERROR_HEURISTIC_DAMAGE_POSSIBLE"></span><span id="error_heuristic_damage_possible"></span>**FEHLER \_ HEURISTISCHE \_ \_ BESCHÄDIGUNG MÖGLICH**
</dt> <dd> <dl> <dt>

6731 (0x1A4B)
</dt> <dt>



Der Versuch, die Transaktion zu committen, wurde abgeschlossen, aber es ist möglich, dass ein Teil der Transaktionsstruktur aufgrund von Heuristiken keinen erfolgreichen Commit ausgeführt hat. Daher ist es möglich, dass für einige in der Transaktion geänderte Daten möglicherweise kein Commit ausgeführt wurde, was zu Transaktionsinkonsistenzen führt. Überprüfen Sie nach Möglichkeit die Konsistenz der zugeordneten Daten.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTIONAL_CONFLICT"></span><span id="error_transactional_conflict"></span>**ERROR \_ TRANSACTIONAL \_ CONFLICT**
</dt> <dd> <dl> <dt>

6800 (0x1A90)
</dt> <dt>



Die Funktion hat versucht, einen Namen zu verwenden, der für die Verwendung durch eine andere Transaktion reserviert ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_RM_NOT_ACTIVE"></span><span id="error_rm_not_active"></span>**FEHLER \_ RM \_ NICHT \_ AKTIV**
</dt> <dd> <dl> <dt>

6801 (0x1A91)
</dt> <dt>



Die Transaktionsunterstützung innerhalb des angegebenen Ressourcen-Managers wird nicht gestartet oder wurde aufgrund eines Fehlers beendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_RM_METADATA_CORRUPT"></span><span id="error_rm_metadata_corrupt"></span>**FEHLER \_ RM \_ METADATA \_ CORRUPT**
</dt> <dd> <dl> <dt>

6802 (0x1A92)
</dt> <dt>



Die Metadaten des RM wurden beschädigt. Der RM funktioniert nicht.


</dt> </dl> </dd> <dt>

<span id="ERROR_DIRECTORY_NOT_RM"></span><span id="error_directory_not_rm"></span>**ERROR \_ DIRECTORY \_ NOT \_ RM**
</dt> <dd> <dl> <dt>

6803 (0x1A93)
</dt> <dt>



Das angegebene Verzeichnis enthält keinen Ressourcen-Manager.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTIONS_UNSUPPORTED_REMOTE"></span><span id="error_transactions_unsupported_remote"></span>**\_FEHLERTRANSAKTIONEN \_ NICHT UNTERSTÜTZT REMOTE \_**
</dt> <dd> <dl> <dt>

6805 (0x1A95)
</dt> <dt>



Der Remoteserver oder die Remotefreigabe unterstützt keine transaktionsgesteuerten Dateivorgänge.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_RESIZE_INVALID_SIZE"></span><span id="error_log_resize_invalid_size"></span>**ÄNDERN DER GRÖßE \_ DES \_ FEHLERPROTOKOLLS \_ UNGÜLTIGE \_ GRÖßE**
</dt> <dd> <dl> <dt>

6806 (0x1A96)
</dt> <dt>



Die angeforderte Protokollgröße ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_OBJECT_NO_LONGER_EXISTS"></span><span id="error_object_no_longer_exists"></span>**FEHLEROBJEKT \_ \_ NICHT MEHR \_ \_ VORHANDEN**
</dt> <dd> <dl> <dt>

6807 (0x1A97)
</dt> <dt>



Das Objekt (Datei, Stream, Link), das dem Handle entspricht, wurde von einem Transaktionsschonpunktrollback gelöscht.


</dt> </dl> </dd> <dt>

<span id="ERROR_STREAM_MINIVERSION_NOT_FOUND"></span><span id="error_stream_miniversion_not_found"></span>**ERROR \_ STREAM \_ MINIVERSION \_ NOT \_ FOUND**
</dt> <dd> <dl> <dt>

6808 (0x1A98)
</dt> <dt>



Die angegebene Miniversion der Datei wurde für diese geöffnete transaktionierte Datei nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_STREAM_MINIVERSION_NOT_VALID"></span><span id="error_stream_miniversion_not_valid"></span>**ERROR \_ STREAM \_ MINIVERSION \_ NOT \_ VALID**
</dt> <dd> <dl> <dt>

6809 (0x1A99)
</dt> <dt>



Die angegebene Dateiminiversion wurde gefunden, aber für ungültig erklärt. Die wahrscheinlichste Ursache ist ein Transaktionsschonpunktrollback.


</dt> </dl> </dd> <dt>

<span id="ERROR_MINIVERSION_INACCESSIBLE_FROM_SPECIFIED_TRANSACTION"></span><span id="error_miniversion_inaccessible_from_specified_transaction"></span>**FEHLER: \_ MINIVERSION \_ KANN VON \_ DER \_ ANGEGEBENEN TRANSAKTION NICHT ZUGEGRIFFEN WERDEN \_**
</dt> <dd> <dl> <dt>

6810 (0x1A9A)
</dt> <dt>



Eine Miniversion kann nur im Kontext der Transaktion geöffnet werden, die sie erstellt hat.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_OPEN_MINIVERSION_WITH_MODIFY_INTENT"></span><span id="error_cant_open_miniversion_with_modify_intent"></span>**ERROR \_ CANT \_ OPEN \_ MINIVERSION \_ WITH \_ MODIFY \_ INTENT**
</dt> <dd> <dl> <dt>

6811 (0x1A9B)
</dt> <dt>



Es ist nicht möglich, eine Miniversion mit Änderungszugriff zu öffnen.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_CREATE_MORE_STREAM_MINIVERSIONS"></span><span id="error_cant_create_more_stream_miniversions"></span>**FEHLER \_ CANT \_ CREATE MORE \_ STREAM \_ \_ MINIVERSIONS**
</dt> <dd> <dl> <dt>

6812 (0x1A9C)
</dt> <dt>



Es ist nicht möglich, weitere Miniversionen für diesen Stream zu erstellen.


</dt> </dl> </dd> <dt>

<span id="ERROR_REMOTE_FILE_VERSION_MISMATCH"></span><span id="error_remote_file_version_mismatch"></span>**FEHLER: \_ \_ NICHT \_ ÜBEREINSTIMMENDE REMOTEDATEIVERSION \_**
</dt> <dd> <dl> <dt>

6814 (0x1A9E)
</dt> <dt>



Der Remoteserver hat eine nicht übereinstimmende Versionsnummer oder Fid für eine Datei gesendet, die mit Transaktionen geöffnet wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_HANDLE_NO_LONGER_VALID"></span><span id="error_handle_no_longer_valid"></span>**\_FEHLERHANDLE \_ NICHT MEHR \_ \_ GÜLTIG**
</dt> <dd> <dl> <dt>

6815 (0x1A9F)
</dt> <dt>



Das Handle wurde von einer Transaktion ungültig gemacht. Die wahrscheinlichste Ursache ist das Vorhandensein einer Speicherzuordnung für eine Datei oder ein geöffnetes Handle, wenn die Transaktion beendet wurde oder ein Rollback zum Sicherungspunkt ausgeführt wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_TXF_METADATA"></span><span id="error_no_txf_metadata"></span>**FEHLER \_ KEINE \_ TXF-METADATEN \_**
</dt> <dd> <dl> <dt>

6816 (0x1AA0)
</dt> <dt>



Die Datei enthält keine Transaktionsmetadaten.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CORRUPTION_DETECTED"></span><span id="error_log_corruption_detected"></span>**\_ \_ FEHLERPROTOKOLLBESCHÄDIGUNG \_ ERKANNT**
</dt> <dd> <dl> <dt>

6817 (0x1AA1)
</dt> <dt>



Die Protokolldaten sind beschädigt.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_RECOVER_WITH_HANDLE_OPEN"></span><span id="error_cant_recover_with_handle_open"></span>**FEHLER \_ CANT \_ RECOVER WITH HANDLE \_ \_ \_ OPEN**
</dt> <dd> <dl> <dt>

6818 (0x1AA2)
</dt> <dt>



Die Datei kann nicht wiederhergestellt werden, da noch ein Handle geöffnet ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_RM_DISCONNECTED"></span><span id="error_rm_disconnected"></span>**FEHLER \_ RM \_ GETRENNT**
</dt> <dd> <dl> <dt>

6819 (0x1AA3)
</dt> <dt>



Das Transaktionsergebnis ist nicht verfügbar, da der dafür zuständige Ressourcen-Manager die Verbindung getrennt hat.


</dt> </dl> </dd> <dt>

<span id="ERROR_ENLISTMENT_NOT_SUPERIOR"></span><span id="error_enlistment_not_superior"></span>**\_FEHLEREINLISTUNG \_ NICHT \_ ÜBERLEGEN**
</dt> <dd> <dl> <dt>

6820 (0x1AA4)
</dt> <dt>



Die Anforderung wurde abgelehnt, da es sich bei der in Frage gestellten Eintragung nicht um eine übergeordnete Eintragung handelt.


</dt> </dl> </dd> <dt>

<span id="ERROR_RECOVERY_NOT_NEEDED"></span><span id="error_recovery_not_needed"></span>**\_ \_ FEHLERWIEDERHERSTELLUNG NICHT \_ ERFORDERLICH**
</dt> <dd> <dl> <dt>

6821 (0x1AA5)
</dt> <dt>



Der Transaktionsressourcen-Manager ist bereits konsistent. Die Wiederherstellung ist nicht erforderlich.


</dt> </dl> </dd> <dt>

<span id="ERROR_RM_ALREADY_STARTED"></span><span id="error_rm_already_started"></span>**FEHLER \_ RM WURDE BEREITS \_ \_ GESTARTET**
</dt> <dd> <dl> <dt>

6822 (0x1AA6)
</dt> <dt>



Der Transaktionsressourcen-Manager wurde bereits gestartet.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_IDENTITY_NOT_PERSISTENT"></span><span id="error_file_identity_not_persistent"></span>**\_ \_ FEHLERDATEIIDENTITÄT NICHT \_ \_ PERSISTENT**
</dt> <dd> <dl> <dt>

6823 (0x1AA7)
</dt> <dt>



Die Datei kann nicht transaktional geöffnet werden, da ihre Identität vom Ergebnis einer nicht aufgelösten Transaktion abhängt.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_BREAK_TRANSACTIONAL_DEPENDENCY"></span><span id="error_cant_break_transactional_dependency"></span>**\_FEHLER: \_ TRANSAKTIONALE ABHÄNGIGKEIT \_ KANN NICHT UNTERBRICHT \_ WERDEN**
</dt> <dd> <dl> <dt>

6824 (0x1AA8)
</dt> <dt>



Der Vorgang kann nicht ausgeführt werden, da eine andere Transaktion davon abhängig ist, dass sich diese Eigenschaft nicht ändert.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_CROSS_RM_BOUNDARY"></span><span id="error_cant_cross_rm_boundary"></span>**FEHLER \_ KANN NICHT \_ \_ RM-ÜBERGREIFEND \_ SEIN**
</dt> <dd> <dl> <dt>

6825 (0x1AA9)
</dt> <dt>



Der Vorgang würde eine einzelne Datei mit zwei Transaktionsressourcen-Managern umfassen und ist daher nicht zulässig.


</dt> </dl> </dd> <dt>

<span id="ERROR_TXF_DIR_NOT_EMPTY"></span><span id="error_txf_dir_not_empty"></span>**FEHLER \_ TXF \_ DIR NICHT \_ \_ LEER**
</dt> <dd> <dl> <dt>

6826 (0x1AAA)
</dt> <dt>



Das $Txf muss leer sein, damit dieser Vorgang erfolgreich ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_INDOUBT_TRANSACTIONS_EXIST"></span><span id="error_indoubt_transactions_exist"></span>**FEHLER \_ \_ INDOUBT-TRANSAKTIONEN \_ VORHANDEN**
</dt> <dd> <dl> <dt>

6827 (0x1AAB)
</dt> <dt>



Der Vorgang würde einen Transaktionsressourcen-Manager in einem inkonsistenten Zustand beenden und ist daher nicht zulässig.


</dt> </dl> </dd> <dt>

<span id="ERROR_TM_VOLATILE"></span><span id="error_tm_volatile"></span>**FEHLER \_ TM \_ VOLATILE**
</dt> <dd> <dl> <dt>

6828 (0x1AAC)
</dt> <dt>



Der Vorgang konnte nicht abgeschlossen werden, da der Transaktions-Manager über kein Protokoll verfügt.


</dt> </dl> </dd> <dt>

<span id="ERROR_ROLLBACK_TIMER_EXPIRED"></span><span id="error_rollback_timer_expired"></span>**FEHLER \_ \_ ROLLBACKZEITR \_ ABGELAUFEN**
</dt> <dd> <dl> <dt>

6829 (0x1AAD)
</dt> <dt>



Ein Rollback konnte nicht geplant werden, da ein zuvor geplanter Rollback bereits ausgeführt wurde oder für die Ausführung in die Warteschlange eingereiht wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_TXF_ATTRIBUTE_CORRUPT"></span><span id="error_txf_attribute_corrupt"></span>**FEHLER: \_ \_ TXF-ATTRIBUT \_ BESCHÄDIGT**
</dt> <dd> <dl> <dt>

6830 (0x1AAE)
</dt> <dt>



Das Transaktionsmetadatenattribut für die Datei oder das Verzeichnis ist beschädigt und nicht lesbar.


</dt> </dl> </dd> <dt>

<span id="ERROR_EFS_NOT_ALLOWED_IN_TRANSACTION"></span><span id="error_efs_not_allowed_in_transaction"></span>**FEHLER: \_ EFS \_ IN TRANSAKTION NICHT \_ \_ \_ ZULÄSSIG**
</dt> <dd> <dl> <dt>

6831 (0x1AAF)
</dt> <dt>



Der Verschlüsselungsvorgang konnte nicht abgeschlossen werden, da eine Transaktion aktiv ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTIONAL_OPEN_NOT_ALLOWED"></span><span id="error_transactional_open_not_allowed"></span>**ERROR \_ TRANSACTIONAL OPEN NOT ALLOWED (FEHLER: \_ \_ TRANSAKTIONSÖFFNEN \_ NICHT ZULÄSSIG)**
</dt> <dd> <dl> <dt>

6832 (0x1AB0)
</dt> <dt>



Dieses Objekt darf in einer Transaktion nicht geöffnet werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_GROWTH_FAILED"></span><span id="error_log_growth_failed"></span>**FEHLER \_ BEIM WACHSTUM DES \_ \_ FEHLERPROTOKOLLS**
</dt> <dd> <dl> <dt>

6833 (0x1AB1)
</dt> <dt>



Fehler beim Erstellen von Speicherplatz im Protokoll des Transaktionsressourcen-Managers. Der Fehlerstatus wurde im Ereignisprotokoll aufgezeichnet.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTED_MAPPING_UNSUPPORTED_REMOTE"></span><span id="error_transacted_mapping_unsupported_remote"></span>**FEHLER \_ BEI DER \_ TRANSAKTIVEN ZUORDNUNG \_ NICHT UNTERSTÜTZTER \_ REMOTECOMPUTER**
</dt> <dd> <dl> <dt>

6834 (0x1AB2)
</dt> <dt>



Die Speicherzuordnung (Erstellen eines zugeordneten Abschnitts) einer Remotedatei unter einer Transaktion wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_TXF_METADATA_ALREADY_PRESENT"></span><span id="error_txf_metadata_already_present"></span>**FEHLER \_ TXF METADATA ALREADY PRESENT (TXF-METADATEN \_ SIND BEREITS \_ \_ VORHANDEN)**
</dt> <dd> <dl> <dt>

6835 (0x1AB3)
</dt> <dt>



Transaktionsmetadaten sind bereits in dieser Datei vorhanden und können nicht ersetzt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_SCOPE_CALLBACKS_NOT_SET"></span><span id="error_transaction_scope_callbacks_not_set"></span>**\_FEHLER: \_ \_ TRANSAKTIONSBEREICHSRÜCKRUFE \_ NICHT \_ FESTGELEGT**
</dt> <dd> <dl> <dt>

6836 (0x1AB4)
</dt> <dt>



Ein Transaktionsbereich konnte nicht eingegeben werden, da der Bereichshandler nicht initialisiert wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_REQUIRED_PROMOTION"></span><span id="error_transaction_required_promotion"></span>**ERROR \_ TRANSACTION \_ REQUIRED \_ PROMOTION**
</dt> <dd> <dl> <dt>

6837 (0x1AB5)
</dt> <dt>



Die Aufstufung war erforderlich, damit sich der Ressourcen-Manager in die Liste einträgt, aber die Transaktion wurde so festgelegt, dass sie nicht zulässig ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_EXECUTE_FILE_IN_TRANSACTION"></span><span id="error_cannot_execute_file_in_transaction"></span>**FEHLER: \_ DATEI IN TRANSAKTION KANN NICHT AUSGEFÜHRT \_ \_ \_ \_ WERDEN**
</dt> <dd> <dl> <dt>

6838 (0x1AB6)
</dt> <dt>



Diese Datei ist für Änderungen in einer nicht aufgelösten Transaktion geöffnet und kann nur von einem transaktiven Reader für die Ausführung geöffnet werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTIONS_NOT_FROZEN"></span><span id="error_transactions_not_frozen"></span>**FEHLERTRANSAKTIONEN \_ \_ NICHT \_ FIXIERT**
</dt> <dd> <dl> <dt>

6839 (0x1AB7)
</dt> <dt>



Die Anforderung, fixierte Transaktionen zu tauen, wurde ignoriert, da Transaktionen zuvor nicht fixiert waren.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_FREEZE_IN_PROGRESS"></span><span id="error_transaction_freeze_in_progress"></span>**FEHLER \_ BEIM EINFRIEREN DER TRANSAKTION IN \_ \_ \_ BEARBEITUNG**
</dt> <dd> <dl> <dt>

6840 (0x1AB8)
</dt> <dt>



Transaktionen können nicht eingefroren werden, da bereits ein Einfrieren vor sich geht.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SNAPSHOT_VOLUME"></span><span id="error_not_snapshot_volume"></span>**FEHLER \_ NICHT \_ \_ MOMENTAUFNAHMEVOLUMEN**
</dt> <dd> <dl> <dt>

6841 (0x1AB9)
</dt> <dt>



Das Zielvolumen ist kein Momentaufnahmevolumen. Dieser Vorgang ist nur auf einem Volume gültig, das als Momentaufnahme bereitgestellt wird.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SAVEPOINT_WITH_OPEN_FILES"></span><span id="error_no_savepoint_with_open_files"></span>**FEHLER: \_ \_ KEIN SAVEPOINT MIT \_ \_ GEÖFFNETEN \_ DATEIEN**
</dt> <dd> <dl> <dt>

6842 (0x1ABA)
</dt> <dt>



Fehler beim Savepoint-Vorgang, da Dateien für die Transaktion geöffnet sind. Dies ist nicht zulässig.


</dt> </dl> </dd> <dt>

<span id="ERROR_DATA_LOST_REPAIR"></span><span id="error_data_lost_repair"></span>**FEHLERDATEN \_ \_ VERLORENE \_ REPARATUR**
</dt> <dd> <dl> <dt>

6843 (0x1ABB)
</dt> <dt>



Windows wurde eine Beschädigung in einer Datei festgestellt, und diese Datei wurde seitdem repariert. Möglicherweise ist ein Datenverlust aufgetreten.


</dt> </dl> </dd> <dt>

<span id="ERROR_SPARSE_NOT_ALLOWED_IN_TRANSACTION"></span><span id="error_sparse_not_allowed_in_transaction"></span>**FEHLER \_ BEI SPARSE \_ IN TRANSAKTION NICHT \_ \_ \_ ZULÄSSIG**
</dt> <dd> <dl> <dt>

6844 (0x1ABC)
</dt> <dt>



Der Sparsevorgang konnte nicht abgeschlossen werden, da eine Transaktion für die Datei aktiv ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_TM_IDENTITY_MISMATCH"></span><span id="error_tm_identity_mismatch"></span>**FEHLER: \_ TM \_ IDENTITY \_ MISMATCH**
</dt> <dd> <dl> <dt>

6845 (0x1ABD)
</dt> <dt>



Fehler beim Aufruf zum Erstellen eines TransactionManager-Objekts, da die in der Protokolldatei gespeicherte Tm Identity nicht mit der tm-Identität übereinstimmen, die als Argument übergeben wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_FLOATED_SECTION"></span><span id="error_floated_section"></span>**ERROR \_ FLOATED \_ SECTION**
</dt> <dd> <dl> <dt>

6846 (0x1ABE)
</dt> <dt>



Es wurde versucht, eine E/A für ein Abschnittsobjekt zu erstellen, das als Ergebnis eines Transaktionsendes gleitet. Es gibt keine gültigen Daten.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_ACCEPT_TRANSACTED_WORK"></span><span id="error_cannot_accept_transacted_work"></span>**ERROR \_ CANNOT ACCEPT TRANSACTED WORK (FEHLER: \_ \_ TRANSAKTIONSTRANSAKTIVE ARBEIT KANN NICHT AKZEPTIERT \_ WERDEN)**
</dt> <dd> <dl> <dt>

6847 (0x1ABF)
</dt> <dt>



Der Transaktionsressourcen-Manager kann derzeit aufgrund eines vorübergehenden Zustands, z. B. einer geringen Ressourcenauslastung, keine transaktionale Arbeit akzeptieren.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_ABORT_TRANSACTIONS"></span><span id="error_cannot_abort_transactions"></span>**FEHLER: \_ TRANSAKTIONEN KÖNNEN NICHT ABGEBROCHEN \_ \_ WERDEN**
</dt> <dd> <dl> <dt>

6848 (0x1AC0)
</dt> <dt>



Der Transaktionsressourcen-Manager hatte zu viele ausstehende Tranactions, die nicht abgebrochen werden konnten. Der Transaktionsressourcen-Manager wurde heruntergefahren.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_CLUSTERS"></span><span id="error_bad_clusters"></span>**FEHLER: \_ FEHLERHAFTE \_ CLUSTER**
</dt> <dd> <dl> <dt>

6849 (0x1AC1)
</dt> <dt>



Der Vorgang konnte aufgrund fehlerhafter Cluster auf dem Datenträger nicht abgeschlossen werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_COMPRESSION_NOT_ALLOWED_IN_TRANSACTION"></span><span id="error_compression_not_allowed_in_transaction"></span>**FEHLERKOMPRIMIERUNG \_ \_ IN TRANSAKTION NICHT \_ \_ \_ ZULÄSSIG**
</dt> <dd> <dl> <dt>

6850 (0x1AC2)
</dt> <dt>



Der Komprimierungsvorgang konnte nicht abgeschlossen werden, da eine Transaktion für die Datei aktiv ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_VOLUME_DIRTY"></span><span id="error_volume_dirty"></span>**FEHLER \_ VOLUME \_ DIRTY**
</dt> <dd> <dl> <dt>

6851 (0x1AC3)
</dt> <dt>



Der Vorgang konnte nicht abgeschlossen werden, da das Volume "dirty" ist. Führen Sie chkdsk aus, und versuchen Sie es erneut.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_LINK_TRACKING_IN_TRANSACTION"></span><span id="error_no_link_tracking_in_transaction"></span>**FEHLER: \_ KEINE \_ \_ LINKNACHVERFOLGUNG \_ IN \_ TRANSAKTION**
</dt> <dd> <dl> <dt>

6852 (0x1AC4)
</dt> <dt>



Der Linknachverfolgungsvorgang konnte nicht abgeschlossen werden, da eine Transaktion aktiv ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_OPERATION_NOT_SUPPORTED_IN_TRANSACTION"></span><span id="error_operation_not_supported_in_transaction"></span>**FEHLERVORGANG \_ WIRD IN TRANSAKTION NICHT \_ \_ \_ \_ UNTERSTÜTZT**
</dt> <dd> <dl> <dt>

6853 (0x1AC5)
</dt> <dt>



Dieser Vorgang kann in einer Transaktion nicht ausgeführt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_EXPIRED_HANDLE"></span><span id="error_expired_handle"></span>**ERROR EXPIRED HANDLE (HANDLE \_ FÜR \_ FEHLER ABGELAUFEN)**
</dt> <dd> <dl> <dt>

6854 (0x1AC6)
</dt> <dt>



Das Handle ist seiner Transaktion nicht mehr ordnungsgemäß zugeordnet. Es wurde möglicherweise in einem Transaktionsressourcen-Manager geöffnet, der anschließend zum Neustart gezwungen wurde. Schließen Sie das Handle, und öffnen Sie ein neues.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_NOT_ENLISTED"></span><span id="error_transaction_not_enlisted"></span>**\_ \_ FEHLERTRANSAKTION NICHT \_ EINGETRAGEN**
</dt> <dd> <dl> <dt>

6855 (0x1AC7)
</dt> <dt>



Der angegebene Vorgang konnte nicht ausgeführt werden, da der Ressourcen-Manager nicht in der Transaktion eingetragen ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_WINSTATION_NAME_INVALID"></span><span id="error_ctx_winstation_name_invalid"></span>**FEHLER: \_ CTX \_ WINSTATION \_ NAME \_ INVALID**
</dt> <dd> <dl> <dt>

7001 (0x1B59)
</dt> <dt>



Der angegebene Sitzungsname ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_INVALID_PD"></span><span id="error_ctx_invalid_pd"></span>**FEHLER \_ CTX \_ INVALID \_ PD**
</dt> <dd> <dl> <dt>

7002 (0x1B5A)
</dt> <dt>



Der angegebene Protokolltreiber ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_PD_NOT_FOUND"></span><span id="error_ctx_pd_not_found"></span>**FEHLER \_ CTX \_ PD NICHT \_ \_ GEFUNDEN**
</dt> <dd> <dl> <dt>

7003 (0x1B5B)
</dt> <dt>



Der angegebene Protokolltreiber wurde im Systempfad nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_WD_NOT_FOUND"></span><span id="error_ctx_wd_not_found"></span>**FEHLER \_ CTX \_ WD \_ NICHT \_ GEFUNDEN**
</dt> <dd> <dl> <dt>

7004 (0x1B5C)
</dt> <dt>



Der angegebene Terminalverbindungstreiber wurde im Systempfad nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CANNOT_MAKE_EVENTLOG_ENTRY"></span><span id="error_ctx_cannot_make_eventlog_entry"></span>**FEHLER: \_ CTX \_ KANN \_ \_ EVENTLOG-EINTRAG NICHT \_ MACHEN**
</dt> <dd> <dl> <dt>

7005 (0x1B5D)
</dt> <dt>



Für diese Sitzung konnte kein Registrierungsschlüssel für die Ereignisprotokollierung erstellt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_SERVICE_NAME_COLLISION"></span><span id="error_ctx_service_name_collision"></span>**\_FEHLER: \_ CTX-DIENSTNAMENSKOLLISION \_ \_**
</dt> <dd> <dl> <dt>

7006 (0x1B5E)
</dt> <dt>



Ein Dienst mit dem gleichen Namen ist bereits auf dem System vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CLOSE_PENDING"></span><span id="error_ctx_close_pending"></span>**FEHLER \_ CTX \_ CLOSE \_ PENDING**
</dt> <dd> <dl> <dt>

7007 (0x1B5F)
</dt> <dt>



Für die Sitzung steht ein Schlussvorgang aus.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_NO_OUTBUF"></span><span id="error_ctx_no_outbuf"></span>**FEHLER \_ CTX \_ NO \_ OUTBUF**
</dt> <dd> <dl> <dt>

7008 (0x1B60)
</dt> <dt>



Es sind keine freien Ausgabepuffer verfügbar.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_MODEM_INF_NOT_FOUND"></span><span id="error_ctx_modem_inf_not_found"></span>**FEHLER \_ CTX \_ MODEM \_ INF NICHT \_ \_ GEFUNDEN**
</dt> <dd> <dl> <dt>

7009 (0x1B61)
</dt> <dt>



Das MODEM. Die INF-Datei wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_INVALID_MODEMNAME"></span><span id="error_ctx_invalid_modemname"></span>**FEHLER \_ CTX \_ INVALID \_ MODEMNAME**
</dt> <dd> <dl> <dt>

7010 (0x1B62)
</dt> <dt>



Der Modemname wurde in MODEM.INF nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_MODEM_RESPONSE_ERROR"></span><span id="error_ctx_modem_response_error"></span>**FEHLER \_ BEI CTX \_ \_ MODEM-ANTWORTFEHLER \_**
</dt> <dd> <dl> <dt>

7011 (0x1B63)
</dt> <dt>



Das Modem hat den an das Modem gesendeten Befehl nicht akzeptiert. Stellen Sie sicher, dass der konfigurierte Modemname dem angeschlossenen Modem entspricht.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_MODEM_RESPONSE_TIMEOUT"></span><span id="error_ctx_modem_response_timeout"></span>**FEHLER: \_ CTX \_ MODEM RESPONSE \_ \_ TIMEOUT**
</dt> <dd> <dl> <dt>

7012 (0x1B64)
</dt> <dt>



Das Modem hat nicht auf den an ihn gesendeten Befehl geantwortet. Stellen Sie sicher, dass das Modem ordnungsgemäß verkabelt und eingeschaltet ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_MODEM_RESPONSE_NO_CARRIER"></span><span id="error_ctx_modem_response_no_carrier"></span>**FEHLER \_ CTX \_ MODEM RESPONSE NO \_ \_ \_ CARRIER**
</dt> <dd> <dl> <dt>

7013 (0x1B65)
</dt> <dt>



Die Erkennung durch den Netzbetreiber ist fehlgeschlagen, oder der Netzbetreiber wurde aufgrund einer Trennung der Verbindung verworfen.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_MODEM_RESPONSE_NO_DIALTONE"></span><span id="error_ctx_modem_response_no_dialtone"></span>**FEHLER \_ CTX \_ MODEM RESPONSE \_ NO \_ \_ DIALTONE**
</dt> <dd> <dl> <dt>

7014 (0x1B66)
</dt> <dt>



Der Farbton wird nicht innerhalb der erforderlichen Zeit erkannt. Stellen Sie sicher, dass das Telefonkabel ordnungsgemäß angeschlossen und funktionsfähig ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_MODEM_RESPONSE_BUSY"></span><span id="error_ctx_modem_response_busy"></span>**\_FEHLER: \_ CTX-MODEMANTWORT \_ \_ AUSGELASTET**
</dt> <dd> <dl> <dt>

7015 (0x1B67)
</dt> <dt>



Ausgelasteter Signal beim Rückruf am Remotestandort erkannt.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_MODEM_RESPONSE_VOICE"></span><span id="error_ctx_modem_response_voice"></span>**FEHLER \_ CTX \_ MODEM RESPONSE \_ \_ VOICE**
</dt> <dd> <dl> <dt>

7016 (0x1B68)
</dt> <dt>



Spracherkennung am Remotestandort beim Rückruf.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_TD_ERROR"></span><span id="error_ctx_td_error"></span>**FEHLER: \_ CTX \_ \_ TD-FEHLER**
</dt> <dd> <dl> <dt>

7017 (0x1B69)
</dt> <dt>



Transporttreiberfehler.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_WINSTATION_NOT_FOUND"></span><span id="error_ctx_winstation_not_found"></span>**FEHLER \_ CTX \_ WINSTATION \_ NICHT \_ GEFUNDEN**
</dt> <dd> <dl> <dt>

7022 (0x1B6E)
</dt> <dt>



Die angegebene Sitzung wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_WINSTATION_ALREADY_EXISTS"></span><span id="error_ctx_winstation_already_exists"></span>**FEHLER: \_ CTX \_ WINSTATION \_ IST BEREITS \_ VORHANDEN**
</dt> <dd> <dl> <dt>

7023 (0x1B6F)
</dt> <dt>



Der angegebene Sitzungsname wird bereits verwendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_WINSTATION_BUSY"></span><span id="error_ctx_winstation_busy"></span>**FEHLER \_ CTX \_ WINSTATION \_ AUSGELASTET**
</dt> <dd> <dl> <dt>

7024 (0x1B70)
</dt> <dt>



Die Aufgabe, die Sie auszuführen versuchen, kann nicht abgeschlossen werden, da Remotedesktopdienste derzeit ausgelastet ist. Wiederholen Sie den Vorgang in einigen Minuten. Andere Benutzer sollten sich weiterhin anmelden können.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_BAD_VIDEO_MODE"></span><span id="error_ctx_bad_video_mode"></span>**\_FEHLER: \_ CTX– MODUS \_ "FEHLERHAFTES \_ VIDEO"**
</dt> <dd> <dl> <dt>

7025 (0x1B71)
</dt> <dt>



Es wurde versucht, eine Verbindung mit einer Sitzung herzustellen, deren Videomodus vom aktuellen Client nicht unterstützt wird.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_GRAPHICS_INVALID"></span><span id="error_ctx_graphics_invalid"></span>**FEHLER: \_ \_ CTX-GRAFIK \_ UNGÜLTIG**
</dt> <dd> <dl> <dt>

7035 (0x1B7B)
</dt> <dt>



Die Anwendung hat versucht, den DOS-Grafikmodus zu aktivieren. Der DOS-Grafikmodus wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_LOGON_DISABLED"></span><span id="error_ctx_logon_disabled"></span>**\_FEHLER: \_ STRGX-ANMELDUNG \_ DEAKTIVIERT**
</dt> <dd> <dl> <dt>

7037 (0x1B7D)
</dt> <dt>



Ihre berechtigung für die interaktive Anmeldung wurde deaktiviert. Wenden Sie sich an den Administrator.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_NOT_CONSOLE"></span><span id="error_ctx_not_console"></span>**FEHLER \_ CTX \_ NOT \_ CONSOLE**
</dt> <dd> <dl> <dt>

7038 (0x1B7E)
</dt> <dt>



Der angeforderte Vorgang kann nur in der Systemkonsole ausgeführt werden. Dies ist meistens das Ergebnis einer Treiber- oder System-DLL, die direkten Konsolenzugriff erfordert.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CLIENT_QUERY_TIMEOUT"></span><span id="error_ctx_client_query_timeout"></span>**\_FEHLER: \_ TIMEOUT BEI CTX-CLIENTABFRAGE \_ \_**
</dt> <dd> <dl> <dt>

7040 (0x1B80)
</dt> <dt>



Der Client konnte nicht auf die Server-Verbindungsnachricht antworten.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CONSOLE_DISCONNECT"></span><span id="error_ctx_console_disconnect"></span>**FEHLER: \_ CTX \_ CONSOLE \_ DISCONNECT**
</dt> <dd> <dl> <dt>

7041 (0x1B81)
</dt> <dt>



Das Trennen der Konsolensitzung wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CONSOLE_CONNECT"></span><span id="error_ctx_console_connect"></span>**FEHLER \_ CTX \_ CONSOLE \_ CONNECT**
</dt> <dd> <dl> <dt>

7042 (0x1B82)
</dt> <dt>



Das erneute Verbinden einer getrennten Sitzung mit der Konsole wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_SHADOW_DENIED"></span><span id="error_ctx_shadow_denied"></span>**FEHLER \_ CTX \_ SHADOW \_ DENIED**
</dt> <dd> <dl> <dt>

7044 (0x1B84)
</dt> <dt>



Die Anforderung, eine andere Sitzung remote zu steuern, wurde abgelehnt.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_WINSTATION_ACCESS_DENIED"></span><span id="error_ctx_winstation_access_denied"></span>**FEHLER \_ CTX \_ WINSTATION \_ ACCESS \_ DENIED**
</dt> <dd> <dl> <dt>

7045 (0x1B85)
</dt> <dt>



Der angeforderte Sitzungszugriff wird verweigert.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_INVALID_WD"></span><span id="error_ctx_invalid_wd"></span>**FEHLER \_ CTX \_ INVALID \_ WD**
</dt> <dd> <dl> <dt>

7049 (0x1B89)
</dt> <dt>



Der angegebene Terminalverbindungstreiber ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_SHADOW_INVALID"></span><span id="error_ctx_shadow_invalid"></span>**FEHLER \_ CTX \_ SHADOW \_ INVALID**
</dt> <dd> <dl> <dt>

7050 (0x1B8A)
</dt> <dt>



Die angeforderte Sitzung kann nicht remote gesteuert werden. Dies kann daran liegt, dass die Sitzung getrennt ist oder derzeit kein Benutzer angemeldet ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_SHADOW_DISABLED"></span><span id="error_ctx_shadow_disabled"></span>**FEHLER \_ CTX \_ SHADOW \_ DISABLED**
</dt> <dd> <dl> <dt>

7051 (0x1B8B)
</dt> <dt>



Die angeforderte Sitzung ist nicht für die Remotesteuerung konfiguriert.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CLIENT_LICENSE_IN_USE"></span><span id="error_ctx_client_license_in_use"></span>**FEHLER BEI VERWENDUNG DER \_ \_ CTX-CLIENTLIZENZ \_ \_ \_**
</dt> <dd> <dl> <dt>

7052 (0x1B8C)
</dt> <dt>



Ihre Anforderung, eine Verbindung mit diesem Terminalserver herzustellen, wurde abgelehnt. Ihre Terminalserver-Clientlizenznummer wird derzeit von einem anderen Benutzer verwendet. Rufen Sie Ihren Systemadministrator auf, um eine eindeutige Lizenznummer zu erhalten.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CLIENT_LICENSE_NOT_SET"></span><span id="error_ctx_client_license_not_set"></span>**\_FEHLER: \_ CTX-CLIENTLIZENZ \_ \_ NICHT \_ FESTGELEGT**
</dt> <dd> <dl> <dt>

7053 (0x1B8D)
</dt> <dt>



Ihre Anforderung, eine Verbindung mit diesem Terminalserver herzustellen, wurde abgelehnt. Ihre Terminalserver-Clientlizenznummer wurde für diese Kopie des Terminalserverclients nicht eingegeben. Wenden Sie sich an den Systemadministrator.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_LICENSE_NOT_AVAILABLE"></span><span id="error_ctx_license_not_available"></span>**FEHLER \_ \_ CTX-LIZENZ \_ NICHT \_ VERFÜGBAR**
</dt> <dd> <dl> <dt>

7054 (0x1B8E)
</dt> <dt>



Die Anzahl der Verbindungen mit diesem Computer ist begrenzt, und alle Verbindungen werden derzeit verwendet. Versuchen Sie später, eine Verbindung herzustellen, oder wenden Sie sich an Ihren Systemadministrator.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_LICENSE_CLIENT_INVALID"></span><span id="error_ctx_license_client_invalid"></span>**\_FEHLER: \_ CTX-LIZENZCLIENT \_ \_ UNGÜLTIG**
</dt> <dd> <dl> <dt>

7055 (0x1B8F)
</dt> <dt>



Der Client, den Sie verwenden, ist nicht für die Verwendung dieses Systems lizenziert. Ihre Anmeldeanforderung wird abgelehnt.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_LICENSE_EXPIRED"></span><span id="error_ctx_license_expired"></span>**\_FEHLER: \_ CTX-LIZENZ \_ ABGELAUFEN**
</dt> <dd> <dl> <dt>

7056 (0x1B90)
</dt> <dt>



Die Systemlizenz ist abgelaufen. Ihre Anmeldeanforderung wird abgelehnt.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_SHADOW_NOT_RUNNING"></span><span id="error_ctx_shadow_not_running"></span>**\_FEHLER: \_ CTX-SCHATTEN \_ WIRD NICHT \_ AUSGEFÜHRT**
</dt> <dd> <dl> <dt>

7057 (0x1B91)
</dt> <dt>



Die Remotesteuerung konnte nicht beendet werden, da die angegebene Sitzung derzeit nicht remote gesteuert wird.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_SHADOW_ENDED_BY_MODE_CHANGE"></span><span id="error_ctx_shadow_ended_by_mode_change"></span>**FEHLER \_ CTX \_ SHADOW ENDED BY MODE \_ \_ \_ \_ CHANGE**
</dt> <dd> <dl> <dt>

7058 (0x1B92)
</dt> <dt>



Die Remotesteuerung der Konsole wurde beendet, weil der Anzeigemodus geändert wurde. Das Ändern des Anzeigemodus in einer Remotesteuerungssitzung wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACTIVATION_COUNT_EXCEEDED"></span><span id="error_activation_count_exceeded"></span>**\_ \_ FEHLERAKTIVIERUNGSANZAHL \_ ÜBERSCHRITTEN**
</dt> <dd> <dl> <dt>

7059 (0x1B93)
</dt> <dt>



Die maximale Anzahl von Aktivierungen für diese Installation wurde bereits zurückgesetzt. Der Aktivierungszeitgeber wird nicht gelöscht.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_WINSTATIONS_DISABLED"></span><span id="error_ctx_winstations_disabled"></span>**FEHLER \_ CTX \_ WINSTATIONS \_ DEAKTIVIERT**
</dt> <dd> <dl> <dt>

7060 (0x1B94)
</dt> <dt>



Remoteanmeldungen sind derzeit deaktiviert.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_ENCRYPTION_LEVEL_REQUIRED"></span><span id="error_ctx_encryption_level_required"></span>**FEHLER \_ CTX \_ ENCRYPTION LEVEL \_ \_ REQUIRED**
</dt> <dd> <dl> <dt>

7061 (0x1B95)
</dt> <dt>



Sie verfügen nicht über die richtige Verschlüsselungsebene für den Zugriff auf diese Sitzung.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_SESSION_IN_USE"></span><span id="error_ctx_session_in_use"></span>**FEHLER \_ BEI VERWENDUNG DER CTX-SITZUNG \_ \_ \_**
</dt> <dd> <dl> <dt>

7062 (0x1B96)
</dt> <dt>



Der %s \\ \\ %s-Benutzer ist derzeit bei diesem Computer angemeldet. Nur der aktuelle Benutzer oder ein Administrator kann sich bei diesem Computer anmelden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_NO_FORCE_LOGOFF"></span><span id="error_ctx_no_force_logoff"></span>**FEHLER \_ CTX \_ NO FORCE \_ \_ LOGOFF**
</dt> <dd> <dl> <dt>

7063 (0x1B97)
</dt> <dt>



Der %s \\ \\ %s-Benutzer ist bereits bei der Konsole dieses Computers angemeldet. Sie verfügen derzeit nicht über die Berechtigung zum Anmelden. Wenden Sie sich an %s %s, und lassen Sie sie sich abmelden, um dieses Problem zu \\ \\ beheben.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_ACCOUNT_RESTRICTION"></span><span id="error_ctx_account_restriction"></span>**\_FEHLER: \_ CTX-KONTOEINSCHRÄNKUNG \_**
</dt> <dd> <dl> <dt>

7064 (0x1B98)
</dt> <dt>



Sie können sich aufgrund einer Kontoeinschränkung nicht anmelden.


</dt> </dl> </dd> <dt>

<span id="ERROR_RDP_PROTOCOL_ERROR"></span><span id="error_rdp_protocol_error"></span>**FEHLER \_ \_ RDP-PROTOKOLLFEHLER \_**
</dt> <dd> <dl> <dt>

7065 (0x1B99)
</dt> <dt>



Die RDP-Protokollkomponente %2 hat einen Fehler im Protokollstream erkannt und die Verbindung mit dem Client getrennt.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CDM_CONNECT"></span><span id="error_ctx_cdm_connect"></span>**FEHLER \_ CTX \_ CDM \_ CONNECT**
</dt> <dd> <dl> <dt>

7066 (0x1B9A)
</dt> <dt>



Der Clientlaufwerkzuordnungsdienst ist über eine Terminalverbindung verbunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CDM_DISCONNECT"></span><span id="error_ctx_cdm_disconnect"></span>**FEHLER: \_ CTX \_ CDM \_ DISCONNECT**
</dt> <dd> <dl> <dt>

7067 (0x1B9B)
</dt> <dt>



Der Clientlaufwerkzuordnungsdienst wurde bei der Terminalverbindung getrennt.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_SECURITY_LAYER_ERROR"></span><span id="error_ctx_security_layer_error"></span>**FEHLER \_ CTX \_ SECURITY LAYER \_ \_ ERROR**
</dt> <dd> <dl> <dt>

7068 (0x1B9C)
</dt> <dt>



Die Terminalserver-Sicherheitsschicht hat einen Fehler im Protokolldatenstrom erkannt und die Verbindung mit dem Client getrennt.


</dt> </dl> </dd> <dt>

<span id="ERROR_TS_INCOMPATIBLE_SESSIONS"></span><span id="error_ts_incompatible_sessions"></span>**\_ \_ INKOMPATIBLE \_ TS-SITZUNGEN MIT FEHLER**
</dt> <dd> <dl> <dt>

7069 (0x1B9D)
</dt> <dt>



Die Zielsitzung ist mit der aktuellen Sitzung nicht kompatibel.


</dt> </dl> </dd> <dt>

<span id="ERROR_TS_VIDEO_SUBSYSTEM_ERROR"></span><span id="error_ts_video_subsystem_error"></span>**ERROR \_ TS \_ VIDEO \_ SUBSYSTEM \_ ERROR**
</dt> <dd> <dl> <dt>

7070 (0x1B9E)
</dt> <dt>



Windows können keine Verbindung mit Ihrer Sitzung herstellen, da im Windows Videosubsystem ein Problem aufgetreten ist. Versuchen Sie später erneut, eine Verbindung herzustellen, oder wenden Sie sich an den Serveradministrator, um Unterstützung zu erhalten.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_INVALID_API_SEQUENCE"></span><span id="frs_err_invalid_api_sequence"></span>**\_ \_ UNGÜLTIGE \_ FRS \_ ERR-API-SEQUENZ**
</dt> <dd> <dl> <dt>

8001 (0x1F41)
</dt> <dt>



Die Dateireplikationsdienst-API wurde falsch aufgerufen.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_STARTING_SERVICE"></span><span id="frs_err_starting_service"></span>**FRS \_ ERR \_ STARTING \_ SERVICE**
</dt> <dd> <dl> <dt>

8002 (0x1F42)
</dt> <dt>



Der Dateireplikationsdienst kann nicht gestartet werden.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_STOPPING_SERVICE"></span><span id="frs_err_stopping_service"></span>**FRS \_ ERR \_ STOPPING \_ SERVICE**
</dt> <dd> <dl> <dt>

8003 (0x1F43)
</dt> <dt>



Der Dateireplikationsdienst kann nicht beendet werden.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_INTERNAL_API"></span><span id="frs_err_internal_api"></span>**INTERNE FRS \_ \_ \_ ERR-API**
</dt> <dd> <dl> <dt>

8004 (0x1F44)
</dt> <dt>



Die Dateireplikationsdienst-API hat die Anforderung beendet. Das Ereignisprotokoll enthält möglicherweise weitere Informationen.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_INTERNAL"></span><span id="frs_err_internal"></span>**FRS \_ ERR \_ INTERNAL**
</dt> <dd> <dl> <dt>

8005 (0x1F45)
</dt> <dt>



Der Dateireplikationsdienst hat die Anforderung beendet. Das Ereignisprotokoll enthält möglicherweise weitere Informationen.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_SERVICE_COMM"></span><span id="frs_err_service_comm"></span>**FRS \_ ERR \_ SERVICE \_ COMM**
</dt> <dd> <dl> <dt>

8006 (0x1F46)
</dt> <dt>



Der Dateireplikationsdienst kann nicht kontaktiert werden. Das Ereignisprotokoll enthält möglicherweise weitere Informationen.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_INSUFFICIENT_PRIV"></span><span id="frs_err_insufficient_priv"></span>**FRS \_ ERR \_ INSUFFICIENT \_ PRIV**
</dt> <dd> <dl> <dt>

8007 (0x1F47)
</dt> <dt>



Der Dateireplikationsdienst kann die Anforderung nicht erfüllen, da der Benutzer nicht über unzureichende Berechtigungen verfügt. Das Ereignisprotokoll enthält möglicherweise weitere Informationen.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_AUTHENTICATION"></span><span id="frs_err_authentication"></span>**FRS \_ ERR \_ AUTHENTICATION**
</dt> <dd> <dl> <dt>

8008 (0x1F48)
</dt> <dt>



Der Dateireplikationsdienst kann die Anforderung nicht erfüllen, da kein authentifizierter RPC verfügbar ist. Das Ereignisprotokoll enthält möglicherweise weitere Informationen.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_PARENT_INSUFFICIENT_PRIV"></span><span id="frs_err_parent_insufficient_priv"></span>**FRS \_ ERR \_ PARENT \_ INSUFFICIENT \_ PRIV**
</dt> <dd> <dl> <dt>

8009 (0x1F49)
</dt> <dt>



Der Dateireplikationsdienst kann die Anforderung nicht erfüllen, da der Benutzer nicht über ausreichende Berechtigungen auf dem Domänencontroller verfügt. Das Ereignisprotokoll enthält möglicherweise weitere Informationen.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_PARENT_AUTHENTICATION"></span><span id="frs_err_parent_authentication"></span>**ÜBERGEORDNETE \_ \_ FRS-ERR-AUTHENTIFIZIERUNG \_**
</dt> <dd> <dl> <dt>

8010 (0x1F4A)
</dt> <dt>



Der Dateireplikationsdienst kann die Anforderung nicht erfüllen, da der authentifizierte RPC auf dem Domänencontroller nicht verfügbar ist. Das Ereignisprotokoll enthält möglicherweise weitere Informationen.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_CHILD_TO_PARENT_COMM"></span><span id="frs_err_child_to_parent_comm"></span>**FRS \_ ERR \_ CHILD \_ TO \_ PARENT \_ COMM**
</dt> <dd> <dl> <dt>

8011 (0x1F4B)
</dt> <dt>



Der Dateireplikationsdienst kann nicht mit dem Dateireplikationsdienst auf dem Domänencontroller kommunizieren. Das Ereignisprotokoll enthält möglicherweise weitere Informationen.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_PARENT_TO_CHILD_COMM"></span><span id="frs_err_parent_to_child_comm"></span>**FRS \_ ERR \_ PARENT \_ TO \_ CHILD \_ COMM**
</dt> <dd> <dl> <dt>

8012 (0x1F4C)
</dt> <dt>



Der Dateireplikationsdienst auf dem Domänencontroller kann nicht mit dem Dateireplikationsdienst auf diesem Computer kommunizieren. Das Ereignisprotokoll enthält möglicherweise weitere Informationen.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_SYSVOL_POPULATE"></span><span id="frs_err_sysvol_populate"></span>**FRS \_ ERR \_ SYSVOL \_ POPULATE**
</dt> <dd> <dl> <dt>

8013 (0x1F4D)
</dt> <dt>



Der Dateireplikationsdienst kann das Systemvolume aufgrund eines internen Fehlers nicht auffüllen. Das Ereignisprotokoll enthält möglicherweise weitere Informationen.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_SYSVOL_POPULATE_TIMEOUT"></span><span id="frs_err_sysvol_populate_timeout"></span>**FRS \_ ERR \_ SYSVOL \_ POPULATE \_ TIMEOUT**
</dt> <dd> <dl> <dt>

8014 (0x1F4E)
</dt> <dt>



Der Dateireplikationsdienst kann das Systemvolume aufgrund eines internen Timeouts nicht auffüllen. Das Ereignisprotokoll enthält möglicherweise weitere Informationen.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_SYSVOL_IS_BUSY"></span><span id="frs_err_sysvol_is_busy"></span>**FRS \_ ERR \_ SYSVOL \_ IST \_ AUSGELASTET**
</dt> <dd> <dl> <dt>

8015 (0x1F4F)
</dt> <dt>



Der Dateireplikationsdienst kann die Anforderung nicht verarbeiten. Das Systemvolume ist mit einer vorherigen Anforderung ausgelastet.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_SYSVOL_DEMOTE"></span><span id="frs_err_sysvol_demote"></span>**FRS \_ ERR \_ SYSVOL \_ DEMOTE**
</dt> <dd> <dl> <dt>

8016 (0x1F50)
</dt> <dt>



Der Dateireplikationsdienst kann die Replikation des Systemvolumes aufgrund eines internen Fehlers nicht beenden. Das Ereignisprotokoll enthält möglicherweise weitere Informationen.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_INVALID_SERVICE_PARAMETER"></span><span id="frs_err_invalid_service_parameter"></span>**FRS \_ ERR \_ INVALID \_ SERVICE \_ PARAMETER**
</dt> <dd> <dl> <dt>

8017 (0x1F51)
</dt> <dt>



Der Dateireplikationsdienst hat einen ungültigen Parameter erkannt.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>WinError.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Systemfehlercodes](system-error-codes.md)
</dt> </dl>

 

 




