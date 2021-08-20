---
description: Beschreibt die Fehlercodes 1000-1299, die in der WinError.h-Headerdatei definiert sind und für Entwickler bestimmt sind.
ms.assetid: 0061feb6-e1a0-4fcd-8f80-954087c799d7
title: Systemfehlercodes (1000-1299) (WinError.h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: dfda2e29a6b75acd683842509229f3bc52d7e8d3599855b01d8376f5a7daf2ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076334"
---
# <a name="system-error-codes-1000-1299"></a>Systemfehlercodes (1000-1299)

> [!NOTE]
> Diese Informationen sind für Entwickler gedacht, die Systemfehler debuggen. Für andere Fehler, z. B. Probleme mit Windows Update, finden Sie eine Liste der Ressourcen auf der [Seite Fehlercodes.](system-error-codes.md)

In der folgenden Liste werden [die Systemfehlercodes für](system-error-codes.md) die Fehler 1000 bis 1299 beschrieben. Sie werden von der [**GetLastError-Funktion**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) zurückgegeben, wenn viele Funktionen fehlschlagen. Verwenden Sie zum Abrufen des Beschreibungstexts für den Fehler in Ihrer Anwendung die [**Funktion FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) mit dem **Flag FORMAT MESSAGE FROM \_ \_ \_ SYSTEM.**

<dl> <dt>

<span id="ERROR_STACK_OVERFLOW"></span><span id="error_stack_overflow"></span>**\_ \_ FEHLERSTAPELÜBERLAUF**
</dt> <dd> <dl> <dt>

1001 (0x3E9)
</dt> <dt>



Rekursion zu tief; Der Stapel ist überlaufen.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MESSAGE"></span><span id="error_invalid_message"></span>**FEHLER: \_ \_ UNGÜLTIGE MELDUNG**
</dt> <dd> <dl> <dt>

1002 (0x3EA)
</dt> <dt>



Das Fenster kann nicht auf die gesendete Nachricht wirken.


</dt> </dl> </dd> <dt>

<span id="ERROR_CAN_NOT_COMPLETE"></span><span id="error_can_not_complete"></span>**FEHLER \_ KANN NICHT ABGESCHLOSSEN \_ \_ WERDEN**
</dt> <dd> <dl> <dt>

1003 (0x3EB)
</dt> <dt>



Diese Funktion kann nicht abgeschlossen werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_FLAGS"></span><span id="error_invalid_flags"></span>**FEHLER \_ \_ UNGÜLTIGE FLAGS**
</dt> <dd> <dl> <dt>

1004 (0x3EC)
</dt> <dt>



Ungültige Flags.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNRECOGNIZED_VOLUME"></span><span id="error_unrecognized_volume"></span>**FEHLER: \_ NICHT UNBEKANNTES \_ VOLUME**
</dt> <dd> <dl> <dt>

1005 (0x3ED)
</dt> <dt>



Das Volume enthält kein erkanntes Dateisystem. Stellen Sie sicher, dass alle erforderlichen Dateisystemtreiber geladen sind und dass das Volume nicht beschädigt ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_INVALID"></span><span id="error_file_invalid"></span>**FEHLERDATEI \_ \_ UNGÜLTIG**
</dt> <dd> <dl> <dt>

1006 (0x3EE)
</dt> <dt>



Das Volume für eine Datei wurde extern geändert, sodass die geöffnete Datei nicht mehr gültig ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_FULLSCREEN_MODE"></span><span id="error_fullscreen_mode"></span>**FEHLER \_ IM \_ VOLLBILDMODUS**
</dt> <dd> <dl> <dt>

1007 (0x3EF)
</dt> <dt>



Der angeforderte Vorgang kann nicht im Vollbildmodus ausgeführt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_TOKEN"></span><span id="error_no_token"></span>**FEHLER \_ KEIN \_ TOKEN**
</dt> <dd> <dl> <dt>

1008 (0x3F0)
</dt> <dt>



Es wurde versucht, auf ein Token zu verweisen, das nicht vorhanden ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_BADDB"></span><span id="error_baddb"></span>**FEHLER \_ BADDB**
</dt> <dd> <dl> <dt>

1009 (0x3F1)
</dt> <dt>



Die Konfigurationsregistrierungsdatenbank ist beschädigt.


</dt> </dl> </dd> <dt>

<span id="ERROR_BADKEY"></span><span id="error_badkey"></span>**FEHLER \_ BADKEY**
</dt> <dd> <dl> <dt>

1010 (0x3F2)
</dt> <dt>



Der Registrierungsschlüssel für die Konfiguration ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANTOPEN"></span><span id="error_cantopen"></span>**FEHLER \_ CANTOPEN**
</dt> <dd> <dl> <dt>

1011 (0x3F3)
</dt> <dt>



Der Konfigurationsregistrierungsschlüssel konnte nicht geöffnet werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANTREAD"></span><span id="error_cantread"></span>**FEHLER: \_ CANTREAD**
</dt> <dd> <dl> <dt>

1012 (0x3F4)
</dt> <dt>



Der Konfigurationsregistrierungsschlüssel konnte nicht gelesen werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANTWRITE"></span><span id="error_cantwrite"></span>**FEHLER \_ CANTWRITE**
</dt> <dd> <dl> <dt>

1013 (0x3F5)
</dt> <dt>



Der Konfigurationsregistrierungsschlüssel konnte nicht geschrieben werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_REGISTRY_RECOVERED"></span><span id="error_registry_recovered"></span>**FEHLERREGISTRIERUNG \_ \_ WIEDERHERGESTELLT**
</dt> <dd> <dl> <dt>

1014 (0x3F6)
</dt> <dt>



Eine der Dateien in der Registrierungsdatenbank musste mithilfe eines Protokolls oder einer alternativen Kopie wiederhergestellt werden. Die Wiederherstellung war erfolgreich.


</dt> </dl> </dd> <dt>

<span id="ERROR_REGISTRY_CORRUPT"></span><span id="error_registry_corrupt"></span>**FEHLER \_ BEI REGISTRIERUNG \_ BESCHÄDIGT**
</dt> <dd> <dl> <dt>

1015 (0x3F7)
</dt> <dt>



Die Registrierung ist beschädigt. Die Struktur einer der Dateien, die Registrierungsdaten enthalten, ist beschädigt, oder das Speicherimage des Systems der Datei ist beschädigt, oder die Datei konnte nicht wiederhergestellt werden, weil die alternative Kopie oder das alternative Protokoll nicht vorhanden oder beschädigt war.


</dt> </dl> </dd> <dt>

<span id="ERROR_REGISTRY_IO_FAILED"></span><span id="error_registry_io_failed"></span>**FEHLER BEIM \_ \_ E/A-FEHLER BEI \_ DER REGISTRIERUNG**
</dt> <dd> <dl> <dt>

1016 (0x3F8)
</dt> <dt>



Ein von der Registrierung initiierter E/A-Vorgang ist nicht wiederhergestellt worden. Die Registrierung konnte eine der Dateien, die das Systemimage der Registrierung enthalten, weder einlesen noch ausschreiben oder leeren.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_REGISTRY_FILE"></span><span id="error_not_registry_file"></span>**FEHLER \_ NICHT \_ \_ REGISTRIERUNGSDATEI**
</dt> <dd> <dl> <dt>

1017 (0x3F9)
</dt> <dt>



Das System hat versucht, eine Datei in die Registrierung zu laden oder wiederherzustellen, aber die angegebene Datei hat kein Registrierungsdateiformat.


</dt> </dl> </dd> <dt>

<span id="ERROR_KEY_DELETED"></span><span id="error_key_deleted"></span>**FEHLERSCHLÜSSEL \_ \_ GELÖSCHT**
</dt> <dd> <dl> <dt>

1018 (0x3FA)
</dt> <dt>



Ungültiger Vorgang für einen Registrierungsschlüssel, der zum Löschen markiert wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_LOG_SPACE"></span><span id="error_no_log_space"></span>**FEHLER \_ KEIN \_ \_ PROTOKOLLSPEICHERPLATZ**
</dt> <dd> <dl> <dt>

1019 (0x3FB)
</dt> <dt>



Das System konnte den erforderlichen Speicherplatz in einem Registrierungsprotokoll nicht zuordnen.


</dt> </dl> </dd> <dt>

<span id="ERROR_KEY_HAS_CHILDREN"></span><span id="error_key_has_children"></span>**FEHLERSCHLÜSSEL \_ \_ HAT \_ CHILDREN**
</dt> <dd> <dl> <dt>

1020 (0x3FC)
</dt> <dt>



In einem Registrierungsschlüssel, der bereits über Unterschlüssel oder Werte verfügt, kann keine symbolische Verknüpfung erstellt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CHILD_MUST_BE_VOLATILE"></span><span id="error_child_must_be_volatile"></span>**ERROR \_ CHILD MUST BE VOLATILE (UNTERGEORDNETER FEHLER MUSS \_ \_ \_ FLÜCHTIG SEIN)**
</dt> <dd> <dl> <dt>

1021 (0x3FD)
</dt> <dt>



Unter einem flüchtigen übergeordneten Schlüssel kann kein stabiler Unterschlüssel erstellt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOTIFY_ENUM_DIR"></span><span id="error_notify_enum_dir"></span>**FEHLERBENACHRICHTIGUNG \_ \_ ENUM \_ DIR**
</dt> <dd> <dl> <dt>

1022 (0x3FE)
</dt> <dt>



Eine Benachrichtigungsänderungsanforderung wird abgeschlossen, und die Informationen werden nicht im Puffer des Aufrufers zurückgegeben. Der Aufrufer muss nun die Dateien aufzählen, um die Änderungen zu finden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEPENDENT_SERVICES_RUNNING"></span><span id="error_dependent_services_running"></span>**FEHLERABHÄNGIGE \_ \_ DIENSTE, DIE \_ AUSGEFÜHRT WERDEN**
</dt> <dd> <dl> <dt>

1051 (0x41B)
</dt> <dt>



Ein Stop-Steuerelement wurde an einen Dienst gesendet, von dem andere ausgeführte Dienste abhängig sind.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SERVICE_CONTROL"></span><span id="error_invalid_service_control"></span>**FEHLER: \_ \_ UNGÜLTIGE \_ DIENSTSTEUERUNG**
</dt> <dd> <dl> <dt>

1052 (0x41C)
</dt> <dt>



Das angeforderte Steuerelement ist für diesen Dienst ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_REQUEST_TIMEOUT"></span><span id="error_service_request_timeout"></span>**TIMEOUT \_ FÜR \_ \_ FEHLERDIENSTANFORDERUNG**
</dt> <dd> <dl> <dt>

1053 (0x41D)
</dt> <dt>



Der Dienst antwortete nicht rechtzeitig auf die Start- oder Steuerungsanforderung.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_NO_THREAD"></span><span id="error_service_no_thread"></span>**FEHLERDIENST \_ \_ KEIN \_ THREAD**
</dt> <dd> <dl> <dt>

1054 (0x41E)
</dt> <dt>



Für den Dienst konnte kein Thread erstellt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_DATABASE_LOCKED"></span><span id="error_service_database_locked"></span>**\_ \_ FEHLERDIENSTDATENBANK \_ GESPERRT**
</dt> <dd> <dl> <dt>

1055 (0x41F)
</dt> <dt>



Die Dienstdatenbank ist gesperrt.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_ALREADY_RUNNING"></span><span id="error_service_already_running"></span>**FEHLERDIENST \_ \_ WIRD BEREITS \_ AUSGEFÜHRT**
</dt> <dd> <dl> <dt>

1056 (0x420)
</dt> <dt>



Eine Instanz des Diensts wird bereits ausgeführt.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SERVICE_ACCOUNT"></span><span id="error_invalid_service_account"></span>**FEHLER: \_ \_ UNGÜLTIGES \_ DIENSTKONTO**
</dt> <dd> <dl> <dt>

1057 (0x421)
</dt> <dt>



Der Kontoname ist ungültig oder nicht vorhanden, oder das Kennwort ist für den angegebenen Kontonamen ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_DISABLED"></span><span id="error_service_disabled"></span>**FEHLERDIENST \_ \_ DEAKTIVIERT**
</dt> <dd> <dl> <dt>

1058 (0x422)
</dt> <dt>



Der Dienst kann nicht gestartet werden, weil er deaktiviert wurde oder weil ihm keine aktivierten Geräte zugeordnet sind.


</dt> </dl> </dd> <dt>

<span id="ERROR_CIRCULAR_DEPENDENCY"></span><span id="error_circular_dependency"></span>**\_FEHLERKREISFÖRMIGE \_ ABHÄNGIGKEIT**
</dt> <dd> <dl> <dt>

1059 (0x423)
</dt> <dt>



Die Zirkeldienstabhängigkeit wurde angegeben.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_DOES_NOT_EXIST"></span><span id="error_service_does_not_exist"></span>**FEHLERDIENST \_ \_ IST NICHT \_ \_ VORHANDEN**
</dt> <dd> <dl> <dt>

1060 (0x424)
</dt> <dt>



Der angegebene Dienst ist nicht als installierter Dienst vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_CANNOT_ACCEPT_CTRL"></span><span id="error_service_cannot_accept_ctrl"></span>**FEHLERDIENST \_ \_ KANN \_ STRG NICHT \_ AKZEPTIEREN**
</dt> <dd> <dl> <dt>

1061 (0x425)
</dt> <dt>



Der Dienst kann derzeit keine Steuerungsmeldungen akzeptieren.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_NOT_ACTIVE"></span><span id="error_service_not_active"></span>**FEHLERDIENST \_ \_ NICHT \_ AKTIV**
</dt> <dd> <dl> <dt>

1062 (0x426)
</dt> <dt>



Der Dienst wurde nicht gestartet.


</dt> </dl> </dd> <dt>

<span id="ERROR_FAILED_SERVICE_CONTROLLER_CONNECT"></span><span id="error_failed_service_controller_connect"></span>**FEHLER BEIM \_ HERSTELLEN EINER VERBINDUNG MIT DEM \_ \_ \_ DIENSTCONTROLLER**
</dt> <dd> <dl> <dt>

1063 (0x427)
</dt> <dt>



Der Dienstprozess konnte keine Verbindung mit dem Dienstcontroller herstellen.


</dt> </dl> </dd> <dt>

<span id="ERROR_EXCEPTION_IN_SERVICE"></span><span id="error_exception_in_service"></span>**\_ \_ FEHLERAUSNAHME IM \_ DIENST**
</dt> <dd> <dl> <dt>

1064 (0x428)
</dt> <dt>



Beim Behandeln der Steuerungsanforderung ist im Dienst eine Ausnahme aufgetreten.


</dt> </dl> </dd> <dt>

<span id="ERROR_DATABASE_DOES_NOT_EXIST"></span><span id="error_database_does_not_exist"></span>**FEHLERDATENBANK \_ \_ NICHT \_ \_ VORHANDEN**
</dt> <dd> <dl> <dt>

1065 (0x429)
</dt> <dt>



Die angegebene Datenbank ist nicht vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_SPECIFIC_ERROR"></span><span id="error_service_specific_error"></span>**DIENSTSPEZIFISCHER \_ \_ FEHLER \_**
</dt> <dd> <dl> <dt>

1066 (0x42A)
</dt> <dt>



Der Dienst hat einen dienstspezifischen Fehlercode zurückgegeben.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROCESS_ABORTED"></span><span id="error_process_aborted"></span>**FEHLERPROZESS \_ \_ ABGEBROCHEN**
</dt> <dd> <dl> <dt>

1067 (0x42B)
</dt> <dt>



Der Prozess wurde unerwartet beendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_DEPENDENCY_FAIL"></span><span id="error_service_dependency_fail"></span>**FEHLER BEI \_ \_ \_ DIENSTABHÄNGIGKEITSFEHLER**
</dt> <dd> <dl> <dt>

1068 (0x42C)
</dt> <dt>



Fehler beim Starten des Abhängigkeitsdiensts oder der Abhängigkeitsgruppe.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_LOGON_FAILED"></span><span id="error_service_logon_failed"></span>**FEHLER \_ BEI \_ DER \_ DIENSTANMELDUNG**
</dt> <dd> <dl> <dt>

1069 (0x42D)
</dt> <dt>



Der Dienst konnte wegen einer fehlerhaften Anmeldung nicht gestartet werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_START_HANG"></span><span id="error_service_start_hang"></span>**FEHLER \_ BEIM STARTEN DES \_ \_ DIENSTS HÄNGT**
</dt> <dd> <dl> <dt>

1070 (0x42E)
</dt> <dt>



Nach dem Starten hängte der Dienst in einem start ausstehenden Zustand.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SERVICE_LOCK"></span><span id="error_invalid_service_lock"></span>**FEHLER: \_ \_ UNGÜLTIGE \_ DIENSTSPERRE**
</dt> <dd> <dl> <dt>

1071 (0x42F)
</dt> <dt>



Die angegebene Dienstdatenbanksperre ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_MARKED_FOR_DELETE"></span><span id="error_service_marked_for_delete"></span>**\_FEHLERDIENST, DER ZUM LÖSCHEN MARKIERT \_ \_ \_ IST**
</dt> <dd> <dl> <dt>

1072 (0x430)
</dt> <dt>



Der angegebene Dienst wurde zum Löschen markiert.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_EXISTS"></span><span id="error_service_exists"></span>**FEHLERDIENST \_ \_ VORHANDEN**
</dt> <dd> <dl> <dt>

1073 (0x431)
</dt> <dt>



Der angegebene Dienst ist bereits vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALREADY_RUNNING_LKG"></span><span id="error_already_running_lkg"></span>**FEHLER, \_ DER \_ \_ LKG BEREITS AUSGEFÜHRT HAT**
</dt> <dd> <dl> <dt>

1074 (0x432)
</dt> <dt>



Das System wird derzeit mit der letzten als gut bekannten Konfiguration ausgeführt.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_DEPENDENCY_DELETED"></span><span id="error_service_dependency_deleted"></span>**FEHLER: \_ \_ DIENSTABHÄNGIGKEIT \_ GELÖSCHT**
</dt> <dd> <dl> <dt>

1075 (0x433)
</dt> <dt>



Der Abhängigkeitsdienst ist nicht vorhanden oder wurde zum Löschen markiert.


</dt> </dl> </dd> <dt>

<span id="ERROR_BOOT_ALREADY_ACCEPTED"></span><span id="error_boot_already_accepted"></span>**FEHLER \_ BEIM START WURDE BEREITS \_ \_ AKZEPTIERT**
</dt> <dd> <dl> <dt>

1076 (0x434)
</dt> <dt>



Der aktuelle Start wurde bereits für die Verwendung als letzter bekannter guter Steuerelementsatz akzeptiert.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_NEVER_STARTED"></span><span id="error_service_never_started"></span>**FEHLERDIENST \_ \_ WURDE NIE \_ GESTARTET**
</dt> <dd> <dl> <dt>

1077 (0x435)
</dt> <dt>



Seit dem letzten Start wurden keine Versuche unternommen, den Dienst zu starten.


</dt> </dl> </dd> <dt>

<span id="ERROR_DUPLICATE_SERVICE_NAME"></span><span id="error_duplicate_service_name"></span>**FEHLER: \_ \_ DOPPELTER \_ DIENSTNAME**
</dt> <dd> <dl> <dt>

1078 (0x436)
</dt> <dt>



Der Name wird bereits als Dienstname oder Dienstanzeigename verwendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_DIFFERENT_SERVICE_ACCOUNT"></span><span id="error_different_service_account"></span>**FEHLER: \_ ANDERES \_ \_ DIENSTKONTO**
</dt> <dd> <dl> <dt>

1079 (0x437)
</dt> <dt>



Das für diesen Dienst angegebene Konto ist nicht mit dem Konto identisch, das für andere Dienste angegeben ist, die im selben Prozess ausgeführt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_DETECT_DRIVER_FAILURE"></span><span id="error_cannot_detect_driver_failure"></span>**FEHLER: \_ \_ TREIBERFEHLER \_ KANN NICHT ERKANNT \_ WERDEN**
</dt> <dd> <dl> <dt>

1080 (0x438)
</dt> <dt>



Fehleraktionen können nur für Win32-Dienste und nicht für Treiber festgelegt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_DETECT_PROCESS_ABORT"></span><span id="error_cannot_detect_process_abort"></span>**\_FEHLER: \_ \_ \_ PROZESSABBRUCH KANN NICHT ERKANNT WERDEN**
</dt> <dd> <dl> <dt>

1081 (0x439)
</dt> <dt>



Dieser Dienst wird im gleichen Prozess wie der Dienststeuerungs-Manager ausgeführt. Daher kann der Dienststeuerungs-Manager keine Maßnahmen ergreifen, wenn der Prozess dieses Diensts unerwartet beendet wird.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_RECOVERY_PROGRAM"></span><span id="error_no_recovery_program"></span>**FEHLER \_ KEIN \_ \_ WIEDERHERSTELLUNGSPROGRAMM**
</dt> <dd> <dl> <dt>

1082 (0x43A)
</dt> <dt>



Für diesen Dienst wurde kein Wiederherstellungsprogramm konfiguriert.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_NOT_IN_EXE"></span><span id="error_service_not_in_exe"></span>**FEHLERDIENST \_ \_ NICHT IN \_ \_ EXE**
</dt> <dd> <dl> <dt>

1083 (0x43B)
</dt> <dt>



Das ausführbare Programm, für das dieser Dienst für die Ausführung konfiguriert ist, implementiert den Dienst nicht.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SAFEBOOT_SERVICE"></span><span id="error_not_safeboot_service"></span>**FEHLER \_ NICHT \_ SAFEBOOT \_ SERVICE**
</dt> <dd> <dl> <dt>

1084 (0x43C)
</dt> <dt>



Dieser Dienst kann nicht im Tresor gestartet werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_END_OF_MEDIA"></span><span id="error_end_of_media"></span>**FEHLER \_ ENDE \_ DES \_ MEDIUMS**
</dt> <dd> <dl> <dt>

1100 (0x44C)
</dt> <dt>



Das physische Ende des Bandes wurde erreicht.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILEMARK_DETECTED"></span><span id="error_filemark_detected"></span>**\_FEHLERDATEIMARK \_ ERKANNT**
</dt> <dd> <dl> <dt>

1101 (0x44D)
</dt> <dt>



Ein Bandzugriff hat ein Dateizeichen erreicht.


</dt> </dl> </dd> <dt>

<span id="ERROR_BEGINNING_OF_MEDIA"></span><span id="error_beginning_of_media"></span>**FEHLER \_ BEIM ANFANG DES \_ \_ MEDIUMS**
</dt> <dd> <dl> <dt>

1102 (0x44E)
</dt> <dt>



Der Anfang des Bandes oder einer Partition wurde gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_SETMARK_DETECTED"></span><span id="error_setmark_detected"></span>**FEHLER \_ SETMARK \_ ERKANNT**
</dt> <dd> <dl> <dt>

1103 (0x44F)
</dt> <dt>



Ein Bandzugriff hat das Ende einer Gruppe von Dateien erreicht.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_DATA_DETECTED"></span><span id="error_no_data_detected"></span>**FEHLER \_ KEINE \_ DATEN \_ ERKANNT**
</dt> <dd> <dl> <dt>

1104 (0x450)
</dt> <dt>



Auf dem Band sind keine Daten mehr zu finden.


</dt> </dl> </dd> <dt>

<span id="ERROR_PARTITION_FAILURE"></span><span id="error_partition_failure"></span>**FEHLER \_ BEIM \_ PARTITIONSFEHLER**
</dt> <dd> <dl> <dt>

1105 (0x451)
</dt> <dt>



Das Band konnte nicht partitioniert werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_BLOCK_LENGTH"></span><span id="error_invalid_block_length"></span>**FEHLER: \_ UNGÜLTIGE \_ \_ BLOCKLÄNGE**
</dt> <dd> <dl> <dt>

1106 (0x452)
</dt> <dt>



Beim Zugriff auf ein neues Band einer Mehrvolumepartition ist die aktuelle Blockgröße falsch.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_NOT_PARTITIONED"></span><span id="error_device_not_partitioned"></span>**FEHLER \_ GERÄT \_ NICHT \_ PARTITIONIERT**
</dt> <dd> <dl> <dt>

1107 (0x453)
</dt> <dt>



Informationen zur Bandpartition konnten beim Laden eines Bands nicht gefunden werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_LOCK_MEDIA"></span><span id="error_unable_to_lock_media"></span>**FEHLER: \_ MEDIEN KÖNNEN NICHT \_ GESPERRT WERDEN \_ \_**
</dt> <dd> <dl> <dt>

1108 (0x454)
</dt> <dt>



Der Mechanismus zum Auswerfen von Medien kann nicht gesperrt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_UNLOAD_MEDIA"></span><span id="error_unable_to_unload_media"></span>**FEHLER \_ BEIM ENTLADEN VON \_ \_ \_ MEDIEN NICHT MÖGLICH**
</dt> <dd> <dl> <dt>

1109 (0x455)
</dt> <dt>



Das Medium kann nicht entladen werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEDIA_CHANGED"></span><span id="error_media_changed"></span>**FEHLERMEDIEN \_ \_ GEÄNDERT**
</dt> <dd> <dl> <dt>

1110 (0x456)
</dt> <dt>



Die Medien auf dem Laufwerk haben sich möglicherweise geändert.


</dt> </dl> </dd> <dt>

<span id="ERROR_BUS_RESET"></span><span id="error_bus_reset"></span>**FEHLER \_ BEI DER \_ BUSRÜCKSETZUNG**
</dt> <dd> <dl> <dt>

1111 (0x457)
</dt> <dt>



Der E/A-Bus wurde zurückgesetzt.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MEDIA_IN_DRIVE"></span><span id="error_no_media_in_drive"></span>**FEHLER: \_ KEIN MEDIUM \_ AUF \_ \_ LAUFWERK**
</dt> <dd> <dl> <dt>

1112 (0x458)
</dt> <dt>



Kein Medium im Laufwerk.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_UNICODE_TRANSLATION"></span><span id="error_no_unicode_translation"></span>**FEHLER \_ KEINE \_ \_ UNICODE-ÜBERSETZUNG**
</dt> <dd> <dl> <dt>

1113 (0x459)
</dt> <dt>



Auf der Zielcodepage mit mehreren Byte ist keine Zuordnung für das Unicode-Zeichen vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DLL_INIT_FAILED"></span><span id="error_dll_init_failed"></span>**FEHLER BEIM \_ \_ DLL-INIT-FEHLER \_**
</dt> <dd> <dl> <dt>

1114 (0x45A)
</dt> <dt>



Fehler bei einer DLL-Initialisierungsroutine (Dynamic Link Library).


</dt> </dl> </dd> <dt>

<span id="ERROR_SHUTDOWN_IN_PROGRESS"></span><span id="error_shutdown_in_progress"></span>**FEHLER \_ BEIM HERUNTERFAHREN \_ IN \_ BEARBEITUNG**
</dt> <dd> <dl> <dt>

1115 (0x45B)
</dt> <dt>



Das Herunterfahren des Systems wird ausgeführt.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SHUTDOWN_IN_PROGRESS"></span><span id="error_no_shutdown_in_progress"></span>**FEHLER: \_ \_ KEIN HERUNTERFAHREN WIRD \_ \_ AUSGEFÜHRT**
</dt> <dd> <dl> <dt>

1116 (0x45C)
</dt> <dt>



Das Herunterfahren des Systems kann nicht abgebrochen werden, da kein Herunterfahren ausgeführt wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_IO_DEVICE"></span><span id="error_io_device"></span>**FEHLER BEIM \_ \_ E/A-GERÄT**
</dt> <dd> <dl> <dt>

1117 (0x45D)
</dt> <dt>



Die Anforderung konnte aufgrund eines E/A-Gerätefehlers nicht ausgeführt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERIAL_NO_DEVICE"></span><span id="error_serial_no_device"></span>**FEHLER \_ \_ SERIELL KEIN \_ GERÄT**
</dt> <dd> <dl> <dt>

1118 (0x45E)
</dt> <dt>



Es wurde kein serielles Gerät erfolgreich initialisiert. Der serielle Treiber wird entladen.


</dt> </dl> </dd> <dt>

<span id="ERROR_IRQ_BUSY"></span><span id="error_irq_busy"></span>**FEHLER \_ IRQ \_ AUSGELASTET**
</dt> <dd> <dl> <dt>

1119 (0x45F)
</dt> <dt>



Ein Gerät, das eine Interruptanforderung (IRQ) gemeinsam mit anderen Geräten freigegeben hat, kann nicht geöffnet werden. Mindestens ein anderes Gerät, das diese IRQ verwendet, wurde bereits geöffnet.


</dt> </dl> </dd> <dt>

<span id="ERROR_MORE_WRITES"></span><span id="error_more_writes"></span>**FEHLER \_ BEI MEHR \_ SCHREIBVORGÄNGEN**
</dt> <dd> <dl> <dt>

1120 (0x460)
</dt> <dt>



Ein serieller E/A-Vorgang wurde durch einen anderen Schreibvorgang an den seriellen Anschluss abgeschlossen. Der IOCTL \_ SERIAL \_ XOFF \_ COUNTER hat 0 (null) erreicht.)


</dt> </dl> </dd> <dt>

<span id="ERROR_COUNTER_TIMEOUT"></span><span id="error_counter_timeout"></span>**\_TIMEOUT DES \_ FEHLERZÄHLERS**
</dt> <dd> <dl> <dt>

1121 (0x461)
</dt> <dt>



Ein serieller E/A-Vorgang wurde abgeschlossen, weil der Timeoutzeitraum abgelaufen ist. Der IOCTL \_ SERIAL \_ XOFF \_ COUNTER hat 0 (null) nicht erreicht.)


</dt> </dl> </dd> <dt>

<span id="ERROR_FLOPPY_ID_MARK_NOT_FOUND"></span><span id="error_floppy_id_mark_not_found"></span>**FEHLER: \_ \_ FLOPPY-ID-MARKIERUNG \_ \_ NICHT \_ GEFUNDEN**
</dt> <dd> <dl> <dt>

1122 (0x462)
</dt> <dt>



Auf der Diskette wurde keine ID-Adressmarkierung gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_FLOPPY_WRONG_CYLINDER"></span><span id="error_floppy_wrong_cylinder"></span>**FEHLER: \_ FLOPPY \_ WRONG \_ CYLINDER**
</dt> <dd> <dl> <dt>

1123 (0x463)
</dt> <dt>



Konflikt zwischen dem Feld für die Sektor-ID des Diskettendatenträgers und der Nachverfolgungsadresse des Diskettendatenträgercontrollers.


</dt> </dl> </dd> <dt>

<span id="ERROR_FLOPPY_UNKNOWN_ERROR"></span><span id="error_floppy_unknown_error"></span>**FEHLER: \_ \_ UNBEKANNTER \_ FEHLER BEI DER DISKETTE**
</dt> <dd> <dl> <dt>

1124 (0x464)
</dt> <dt>



Der Diskettencontroller hat einen Fehler gemeldet, der vom Diskettentreiber nicht erkannt wird.


</dt> </dl> </dd> <dt>

<span id="ERROR_FLOPPY_BAD_REGISTERS"></span><span id="error_floppy_bad_registers"></span>**FEHLER: \_ \_ FEHLERHAFTE \_ FEHLERREGISTER**
</dt> <dd> <dl> <dt>

1125 (0x465)
</dt> <dt>



Der Diskettencontroller hat in seinen Registern inkonsistente Ergebnisse zurückgegeben.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_RECALIBRATE_FAILED"></span><span id="error_disk_recalibrate_failed"></span>**FEHLER: \_ \_ FEHLER BEI DATENTRÄGERRECALIBRATE \_**
</dt> <dd> <dl> <dt>

1126 (0x466)
</dt> <dt>



Beim Zugriff auf die Festplatte ist auch nach wiederholungsversuche ein Neucalibrierungsvorgang fehlgeschlagen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_OPERATION_FAILED"></span><span id="error_disk_operation_failed"></span>**FEHLER \_ \_ BEIM DATENTRÄGERVORGANG \_**
</dt> <dd> <dl> <dt>

1127 (0x467)
</dt> <dt>



Beim Zugriff auf die Festplatte ist ein Datenträgervorgang auch nach wiederholungsversuche fehlgeschlagen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_RESET_FAILED"></span><span id="error_disk_reset_failed"></span>**FEHLER \_ BEIM ZURÜCKSETZEN DES \_ \_ DATENTRÄGERS**
</dt> <dd> <dl> <dt>

1128 (0x468)
</dt> <dt>



Beim Zugriff auf die Festplatte war eine Zurücksetzung des Datenträgercontrollers erforderlich, aber auch dies ist fehlgeschlagen.


</dt> </dl> </dd> <dt>

<span id="ERROR_EOM_OVERFLOW"></span><span id="error_eom_overflow"></span>**\_FEHLER: \_ EOM-ÜBERLAUF**
</dt> <dd> <dl> <dt>

1129 (0x469)
</dt> <dt>



Physisches Bandende gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_ENOUGH_SERVER_MEMORY"></span><span id="error_not_enough_server_memory"></span>**FEHLER \_ NICHT \_ GENÜGEND \_ \_ SERVERSPEICHER**
</dt> <dd> <dl> <dt>

1130 (0x46A)
</dt> <dt>



Für diesen Befehl ist nicht genügend Serverspeicher verfügbar.


</dt> </dl> </dd> <dt>

<span id="ERROR_POSSIBLE_DEADLOCK"></span><span id="error_possible_deadlock"></span>**FEHLER: \_ MÖGLICHER \_ DEADLOCK**
</dt> <dd> <dl> <dt>

1131 (0x46B)
</dt> <dt>



Eine potenzielle Deadlockbedingung wurde erkannt.


</dt> </dl> </dd> <dt>

<span id="ERROR_MAPPED_ALIGNMENT"></span><span id="error_mapped_alignment"></span>**\_FEHLERZUORDNUNG \_ DER AUSRICHTUNG**
</dt> <dd> <dl> <dt>

1132 (0x46C)
</dt> <dt>



Die angegebene Basisadresse oder der angegebene Dateioffset verfügt nicht über die richtige Ausrichtung.


</dt> </dl> </dd> <dt>

<span id="ERROR_SET_POWER_STATE_VETOED"></span><span id="error_set_power_state_vetoed"></span>**FEHLER \_ BEIM FESTLEGEN DES \_ \_ \_ ENERGIEZUSTANDS BEHOBEN**
</dt> <dd> <dl> <dt>

1140 (0x474)
</dt> <dt>



Ein Versuch, den Energiezustand des Systems zu ändern, wurde von einer anderen Anwendung oder einem anderen Treiber verhindert.


</dt> </dl> </dd> <dt>

<span id="ERROR_SET_POWER_STATE_FAILED"></span><span id="error_set_power_state_failed"></span>**FEHLER \_ BEIM FESTLEGEN DES \_ \_ ENERGIEZUSTANDSFEHLERS \_**
</dt> <dd> <dl> <dt>

1141 (0x475)
</dt> <dt>



Das System-BIOS konnte den Energiezustand des Systems nicht ändern.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_LINKS"></span><span id="error_too_many_links"></span>**FEHLER \_ ZU \_ VIELE \_ LINKS**
</dt> <dd> <dl> <dt>

1142 (0x476)
</dt> <dt>



Es wurde versucht, mehr Links für eine Datei zu erstellen, als das Dateisystem unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_OLD_WIN_VERSION"></span><span id="error_old_win_version"></span>**FEHLER \_ BEI ALTER \_ \_ WIN-VERSION**
</dt> <dd> <dl> <dt>

1150 (0x47E)
</dt> <dt>



Das angegebene Programm erfordert eine neuere Version von Windows.


</dt> </dl> </dd> <dt>

<span id="ERROR_APP_WRONG_OS"></span><span id="error_app_wrong_os"></span>**FEHLER \_ BEIM \_ FALSCHEN \_ BETRIEBSSYSTEM DER APP**
</dt> <dd> <dl> <dt>

1151 (0x47F)
</dt> <dt>



Das angegebene Programm ist keine MS-DOS- oder Windows-Anwendung.


</dt> </dl> </dd> <dt>

<span id="ERROR_SINGLE_INSTANCE_APP"></span><span id="error_single_instance_app"></span>**FEHLER: \_ \_ EINZELINSTANZ-APP \_**
</dt> <dd> <dl> <dt>

1152 (0x480)
</dt> <dt>



Es können nicht mehrere Instanzen des angegebenen Programms gestartet werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_RMODE_APP"></span><span id="error_rmode_app"></span>**FEHLER \_ BEI RMODE-APP \_**
</dt> <dd> <dl> <dt>

1153 (0x481)
</dt> <dt>



Das angegebene Programm wurde für eine frühere Version von Windows.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DLL"></span><span id="error_invalid_dll"></span>**FEHLER: \_ UNGÜLTIGE \_ DLL**
</dt> <dd> <dl> <dt>

1154 (0x482)
</dt> <dt>



Eine der Bibliotheksdateien, die zum Ausführen dieser Anwendung erforderlich ist, ist beschädigt.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_ASSOCIATION"></span><span id="error_no_association"></span>**FEHLER \_ KEINE \_ ZUORDNUNG**
</dt> <dd> <dl> <dt>

1155 (0x483)
</dt> <dt>



Der angegebenen Datei für diesen Vorgang ist keine Anwendung zugeordnet.


</dt> </dl> </dd> <dt>

<span id="ERROR_DDE_FAIL"></span><span id="error_dde_fail"></span>**FEHLER \_ \_ DDE-FEHLER**
</dt> <dd> <dl> <dt>

1156 (0x484)
</dt> <dt>



Fehler beim Senden des Befehls an die Anwendung.


</dt> </dl> </dd> <dt>

<span id="ERROR_DLL_NOT_FOUND"></span><span id="error_dll_not_found"></span>**\_FEHLER-DLL \_ NICHT \_ GEFUNDEN**
</dt> <dd> <dl> <dt>

1157 (0x485)
</dt> <dt>



Eine der Bibliotheksdateien, die zum Ausführen dieser Anwendung erforderlich sind, wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MORE_USER_HANDLES"></span><span id="error_no_more_user_handles"></span>**FEHLER \_ KEINE \_ \_ BENUTZERHANDLES \_ MEHR**
</dt> <dd> <dl> <dt>

1158 (0x486)
</dt> <dt>



Der aktuelle Prozess hat das System für Handles für Window Manager-Objekte verwendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_MESSAGE_SYNC_ONLY"></span><span id="error_message_sync_only"></span>**NUR \_ \_ \_ FEHLERMELDUNGSSYNCHRONISIERUNG**
</dt> <dd> <dl> <dt>

1159 (0x487)
</dt> <dt>



Die Meldung kann nur mit synchronen Vorgängen verwendet werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_SOURCE_ELEMENT_EMPTY"></span><span id="error_source_element_empty"></span>**\_ \_ FEHLERQUELLENELEMENT \_ LEER**
</dt> <dd> <dl> <dt>

1160 (0x488)
</dt> <dt>



Das angegebene Quellelement verfügt über keine Medien.


</dt> </dl> </dd> <dt>

<span id="ERROR_DESTINATION_ELEMENT_FULL"></span><span id="error_destination_element_full"></span>**ERROR \_ DESTINATION \_ ELEMENT \_ FULL**
</dt> <dd> <dl> <dt>

1161 (0x489)
</dt> <dt>



Das angegebene Zielelement enthält bereits Medien.


</dt> </dl> </dd> <dt>

<span id="ERROR_ILLEGAL_ELEMENT_ADDRESS"></span><span id="error_illegal_element_address"></span>**FEHLER: \_ \_ UNGÜLTIGE \_ ELEMENTADRESSE**
</dt> <dd> <dl> <dt>

1162 (0x48A)
</dt> <dt>



Das angegebene Element ist nicht vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_MAGAZINE_NOT_PRESENT"></span><span id="error_magazine_not_present"></span>**ERROR \_ MAGAZINE \_ NICHT \_ VORHANDEN**
</dt> <dd> <dl> <dt>

1163 (0x48B)
</dt> <dt>



Das angegebene Element ist Teil eines nicht vorhandenen Magazines.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_REINITIALIZATION_NEEDED"></span><span id="error_device_reinitialization_needed"></span>**FEHLER: \_ \_ GERÄTE-NEUINIALISIERUNG \_ ERFORDERLICH**
</dt> <dd> <dl> <dt>

1164 (0x48C)
</dt> <dt>



Das angegebene Gerät muss aufgrund von Hardwarefehlern erneut initialisiert werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_REQUIRES_CLEANING"></span><span id="error_device_requires_cleaning"></span>**FEHLER \_ GERÄT \_ ERFORDERT \_ BEREINIGUNG**
</dt> <dd> <dl> <dt>

1165 (0x48D)
</dt> <dt>



Das Gerät hat angegeben, dass eine Bereinigung erforderlich ist, bevor weitere Vorgänge versucht werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_DOOR_OPEN"></span><span id="error_device_door_open"></span>**FEHLER: \_ \_ GERÄTETÜR \_ GEÖFFNET**
</dt> <dd> <dl> <dt>

1166 (0x48E)
</dt> <dt>



Das Gerät hat angezeigt, dass seine Tür geöffnet ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_NOT_CONNECTED"></span><span id="error_device_not_connected"></span>**FEHLER \_ GERÄT \_ NICHT \_ VERBUNDEN**
</dt> <dd> <dl> <dt>

1167 (0x48F)
</dt> <dt>



Das Gerät ist nicht verbunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_FOUND"></span><span id="error_not_found"></span>**FEHLER \_ NICHT \_ GEFUNDEN**
</dt> <dd> <dl> <dt>

1168 (0x490)
</dt> <dt>



Element wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MATCH"></span><span id="error_no_match"></span>**FEHLER \_ KEINE \_ ÜBEREINSTIMMUNG**
</dt> <dd> <dl> <dt>

1169 (0x491)
</dt> <dt>



Es gab keine Übereinstimmung für den angegebenen Schlüssel im Index.


</dt> </dl> </dd> <dt>

<span id="ERROR_SET_NOT_FOUND"></span><span id="error_set_not_found"></span>**FEHLERSATZ \_ \_ NICHT \_ GEFUNDEN**
</dt> <dd> <dl> <dt>

1170 (0x492)
</dt> <dt>



Der angegebene Eigenschaftensatz ist für das -Objekt nicht vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_POINT_NOT_FOUND"></span><span id="error_point_not_found"></span>**FEHLERPUNKT \_ \_ NICHT \_ GEFUNDEN**
</dt> <dd> <dl> <dt>

1171 (0x493)
</dt> <dt>



Der an GetMouseMovePoints übergebene Punkt befindet sich nicht im Puffer.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_TRACKING_SERVICE"></span><span id="error_no_tracking_service"></span>**FEHLER: \_ KEIN \_ \_ NACHVERFOLGUNGSDIENST**
</dt> <dd> <dl> <dt>

1172 (0x494)
</dt> <dt>



Der Nachverfolgungsdienst (Arbeitsstation) wird nicht ausgeführt.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_VOLUME_ID"></span><span id="error_no_volume_id"></span>**FEHLER: \_ \_ KEINE \_ VOLUME-ID**
</dt> <dd> <dl> <dt>

1173 (0x495)
</dt> <dt>



Die Volume-ID wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_REMOVE_REPLACED"></span><span id="error_unable_to_remove_replaced"></span>**\_FEHLER: \_ \_ \_ "REPLACED" KANN NICHT ENTFERNT WERDEN**
</dt> <dd> <dl> <dt>

1175 (0x497)
</dt> <dt>



Die zu ersetzende Datei kann nicht entfernt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_MOVE_REPLACEMENT"></span><span id="error_unable_to_move_replacement"></span>**FEHLER: \_ \_ ERSETZUNG \_ KANN NICHT BEWEGT \_ WERDEN**
</dt> <dd> <dl> <dt>

1176 (0x498)
</dt> <dt>



Die Ersetzungsdatei kann nicht in die zu ersetzende Datei verschieben. Die zu ersetzende Datei hat ihren ursprünglichen Namen beibehalten.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_MOVE_REPLACEMENT_2"></span><span id="error_unable_to_move_replacement_2"></span>**FEHLER: \_ \_ ERSETZUNG \_ \_ 2 KONNTE NICHT \_ BEWEGT WERDEN**
</dt> <dd> <dl> <dt>

1177 (0x499)
</dt> <dt>



Die Ersetzungsdatei kann nicht in die zu ersetzende Datei verschieben. Die zu ersetzende Datei wurde mithilfe des Sicherungsnamens umbenannt.


</dt> </dl> </dd> <dt>

<span id="ERROR_JOURNAL_DELETE_IN_PROGRESS"></span><span id="error_journal_delete_in_progress"></span>**ERROR \_ JOURNAL \_ DELETE \_ IN \_ PROGRESS**
</dt> <dd> <dl> <dt>

1178 (0x49A)
</dt> <dt>



Das Volumeänderungsjournal wird gelöscht.


</dt> </dl> </dd> <dt>

<span id="ERROR_JOURNAL_NOT_ACTIVE"></span><span id="error_journal_not_active"></span>**FEHLERJOURNAL \_ \_ NICHT \_ AKTIV**
</dt> <dd> <dl> <dt>

1179 (0x49B)
</dt> <dt>



Das Volumeänderungsjournal ist nicht aktiv.


</dt> </dl> </dd> <dt>

<span id="ERROR_POTENTIAL_FILE_FOUND"></span><span id="error_potential_file_found"></span>**MÖGLICHE \_ \_ FEHLERDATEI \_ GEFUNDEN**
</dt> <dd> <dl> <dt>

1180 (0x49C)
</dt> <dt>



Eine Datei wurde gefunden, ist aber möglicherweise nicht die richtige Datei.


</dt> </dl> </dd> <dt>

<span id="ERROR_JOURNAL_ENTRY_DELETED"></span><span id="error_journal_entry_deleted"></span>**\_ \_ FEHLERJOURNALEINTRAG \_ GELÖSCHT**
</dt> <dd> <dl> <dt>

1181 (0x49D)
</dt> <dt>



Der Journaleintrag wurde aus dem Journal gelöscht.


</dt> </dl> </dd> <dt>

<span id="ERROR_SHUTDOWN_IS_SCHEDULED"></span><span id="error_shutdown_is_scheduled"></span>**FEHLER \_ BEIM \_ HERUNTERFAHREN IST \_ GEPLANT**
</dt> <dd> <dl> <dt>

1190 (0x4A6)
</dt> <dt>



Das Herunterfahren des Systems wurde bereits geplant.


</dt> </dl> </dd> <dt>

<span id="ERROR_SHUTDOWN_USERS_LOGGED_ON"></span><span id="error_shutdown_users_logged_on"></span>**FEHLER \_ BEIM \_ HERUNTERFAHREN \_ ANGEMELDETER \_ BENUTZER**
</dt> <dd> <dl> <dt>

1191 (0x4A7)
</dt> <dt>



Das Herunterfahren des Systems kann nicht initiiert werden, da andere Benutzer am Computer angemeldet sind.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_DEVICE"></span><span id="error_bad_device"></span>**FEHLER: \_ \_ FEHLERHAFTES GERÄT**
</dt> <dd> <dl> <dt>

1200 (0x4B0)
</dt> <dt>



Der angegebene Gerätename ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONNECTION_UNAVAIL"></span><span id="error_connection_unavail"></span>**FEHLERVERBINDUNG \_ \_ NICHT VERFÜGBAR**
</dt> <dd> <dl> <dt>

1201 (0x4B1)
</dt> <dt>



Das Gerät ist derzeit nicht verbunden, aber es handelt sich um eine gespeicherte Verbindung.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_ALREADY_REMEMBERED"></span><span id="error_device_already_remembered"></span>**FEHLERGERÄT \_ \_ WURDE BEREITS \_ GESPEICHERT**
</dt> <dd> <dl> <dt>

1202 (0x4B2)
</dt> <dt>



Der Name des lokalen Geräts verfügt über eine gespeicherte Verbindung mit einer anderen Netzwerkressource.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_NET_OR_BAD_PATH"></span><span id="error_no_net_or_bad_path"></span>**FEHLER: \_ KEIN \_ \_ NET- ODER \_ UNGÜLTIGER \_ PFAD**
</dt> <dd> <dl> <dt>

1203 (0x4B3)
</dt> <dt>



Der Netzwerkpfad wurde entweder falsch eingegeben, ist nicht vorhanden, oder der Netzwerkanbieter ist derzeit nicht verfügbar. Geben Sie den Pfad erneut ein, oder wenden Sie sich an Ihren Netzwerkadministrator.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_PROVIDER"></span><span id="error_bad_provider"></span>**FEHLER: \_ \_ FEHLERHAFTER ANBIETER**
</dt> <dd> <dl> <dt>

1204 (0x4B4)
</dt> <dt>



Der angegebene Netzwerkanbietername ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_OPEN_PROFILE"></span><span id="error_cannot_open_profile"></span>**FEHLER \_ KANN PROFIL NICHT \_ ÖFFNEN \_**
</dt> <dd> <dl> <dt>

1205 (0x4B5)
</dt> <dt>



Das Netzwerkverbindungsprofil kann nicht geöffnet werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_PROFILE"></span><span id="error_bad_profile"></span>**FEHLER: \_ \_ FEHLERHAFTES PROFIL**
</dt> <dd> <dl> <dt>

1206 (0x4B6)
</dt> <dt>



Das Netzwerkverbindungsprofil ist beschädigt.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_CONTAINER"></span><span id="error_not_container"></span>**FEHLER \_ NICHT \_ CONTAINER**
</dt> <dd> <dl> <dt>

1207 (0x4B7)
</dt> <dt>



Ein Nichtcontainer kann nicht aufzählen.


</dt> </dl> </dd> <dt>

<span id="ERROR_EXTENDED_ERROR"></span><span id="error_extended_error"></span>**FEHLER \_ \_ ERWEITERTER FEHLER**
</dt> <dd> <dl> <dt>

1208 (0x4B8)
</dt> <dt>



Es ist ein erweiterter Fehler aufgetreten.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_GROUPNAME"></span><span id="error_invalid_groupname"></span>**FEHLER: \_ UNGÜLTIGER \_ GROUPNAME**
</dt> <dd> <dl> <dt>

1209 (0x4B9)
</dt> <dt>



Das Format des angegebenen Gruppennamens ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_COMPUTERNAME"></span><span id="error_invalid_computername"></span>**FEHLER: \_ UNGÜLTIGER \_ COMPUTERNAME**
</dt> <dd> <dl> <dt>

1210 (0x4BA)
</dt> <dt>



Das Format des angegebenen Computernamens ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_EVENTNAME"></span><span id="error_invalid_eventname"></span>**ERROR \_ INVALID \_ EVENTNAME**
</dt> <dd> <dl> <dt>

1211 (0x4BB)
</dt> <dt>



Das Format des angegebenen Ereignisnamens ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DOMAINNAME"></span><span id="error_invalid_domainname"></span>**FEHLER: \_ UNGÜLTIGER \_ DOMÄNENNAME**
</dt> <dd> <dl> <dt>

1212 (0x4BC)
</dt> <dt>



Das Format des angegebenen Domänennamens ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SERVICENAME"></span><span id="error_invalid_servicename"></span>**FEHLER: \_ UNGÜLTIGER \_ DIENSTNAME**
</dt> <dd> <dl> <dt>

1213 (0x4BD)
</dt> <dt>



Das Format des angegebenen Dienstnamens ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_NETNAME"></span><span id="error_invalid_netname"></span>**FEHLER: \_ UNGÜLTIGER \_ NETNAME**
</dt> <dd> <dl> <dt>

1214 (0x4BE)
</dt> <dt>



Das Format des angegebenen Netzwerknamens ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SHARENAME"></span><span id="error_invalid_sharename"></span>**FEHLER: \_ UNGÜLTIGER \_ SHARENAME**
</dt> <dd> <dl> <dt>

1215 (0x4BF)
</dt> <dt>



Das Format des angegebenen Freigabenamens ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PASSWORDNAME"></span><span id="error_invalid_passwordname"></span>**FEHLER: \_ \_ UNGÜLTIGER KENNWORTNAME**
</dt> <dd> <dl> <dt>

1216 (0x4C0)
</dt> <dt>



Das Format des angegebenen Kennworts ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MESSAGENAME"></span><span id="error_invalid_messagename"></span>**FEHLER: \_ UNGÜLTIGER \_ MESSAGENAME**
</dt> <dd> <dl> <dt>

1217 (0x4C1)
</dt> <dt>



Das Format des angegebenen Nachrichtennamens ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MESSAGEDEST"></span><span id="error_invalid_messagedest"></span>**FEHLER: \_ \_ UNGÜLTIGE MELDUNGDEST**
</dt> <dd> <dl> <dt>

1218 (0x4C2)
</dt> <dt>



Das Format des angegebenen Nachrichtenziels ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_SESSION_CREDENTIAL_CONFLICT"></span><span id="error_session_credential_conflict"></span>**FEHLER: \_ \_ \_ SITZUNGSANMELDEINFORMATIONSKONFLIKT**
</dt> <dd> <dl> <dt>

1219 (0x4C3)
</dt> <dt>



Mehrere Verbindungen mit einem Server oder einer freigegebenen Ressource durch denselben Benutzer mit mehreren Benutzernamen sind nicht zulässig. Trennen Sie alle vorherigen Verbindungen mit dem Server oder der freigegebenen Ressource, und versuchen Sie es erneut.


</dt> </dl> </dd> <dt>

<span id="ERROR_REMOTE_SESSION_LIMIT_EXCEEDED"></span><span id="error_remote_session_limit_exceeded"></span>**\_FEHLER: \_ \_ REMOTESITZUNGSLIMIT \_ ÜBERSCHRITTEN**
</dt> <dd> <dl> <dt>

1220 (0x4C4)
</dt> <dt>



Es wurde versucht, eine Sitzung mit einem Netzwerkserver einzurichten, aber es wurden bereits zu viele Sitzungen für diesen Server eingerichtet.


</dt> </dl> </dd> <dt>

<span id="ERROR_DUP_DOMAINNAME"></span><span id="error_dup_domainname"></span>**FEHLER \_ DUP \_ DOMAINNAME**
</dt> <dd> <dl> <dt>

1221 (0x4C5)
</dt> <dt>



Die Arbeitsgruppe oder der Domänenname wird bereits von einem anderen Computer im Netzwerk verwendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_NETWORK"></span><span id="error_no_network"></span>**FEHLER \_ KEIN \_ NETZWERK**
</dt> <dd> <dl> <dt>

1222 (0x4C6)
</dt> <dt>



Das Netzwerk ist nicht vorhanden oder wurde nicht gestartet.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANCELLED"></span><span id="error_cancelled"></span>**FEHLER \_ ABGEBROCHEN**
</dt> <dd> <dl> <dt>

1223 (0x4C7)
</dt> <dt>



Der Vorgang wurde vom Benutzer abgebrochen.


</dt> </dl> </dd> <dt>

<span id="ERROR_USER_MAPPED_FILE"></span><span id="error_user_mapped_file"></span>**FEHLER: \_ VOM BENUTZER \_ ZUGEORDNETE \_ DATEI**
</dt> <dd> <dl> <dt>

1224 (0x4C8)
</dt> <dt>



Der angeforderte Vorgang kann nicht für eine Datei ausgeführt werden, in der ein vom Benutzer zugeordneter Abschnitt geöffnet ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONNECTION_REFUSED"></span><span id="error_connection_refused"></span>**FEHLERVERBINDUNG \_ \_ VERWEIGERT**
</dt> <dd> <dl> <dt>

1225 (0x4C9)
</dt> <dt>



Der Remotecomputer hat die Netzwerkverbindung abgelehnt.


</dt> </dl> </dd> <dt>

<span id="ERROR_GRACEFUL_DISCONNECT"></span><span id="error_graceful_disconnect"></span>**FEHLER: \_ ORDNUNGSGEMÄß \_ TRENNEN**
</dt> <dd> <dl> <dt>

1226 (0x4CA)
</dt> <dt>



Die Netzwerkverbindung wurde ordnungsgemäß geschlossen.


</dt> </dl> </dd> <dt>

<span id="ERROR_ADDRESS_ALREADY_ASSOCIATED"></span><span id="error_address_already_associated"></span>**FEHLERADRESSE \_ \_ BEREITS \_ ZUGEORDNET**
</dt> <dd> <dl> <dt>

1227 (0x4CB)
</dt> <dt>



Dem Netzwerktransportendpunkt ist bereits eine Adresse zugeordnet.


</dt> </dl> </dd> <dt>

<span id="ERROR_ADDRESS_NOT_ASSOCIATED"></span><span id="error_address_not_associated"></span>**FEHLERADRESSE \_ \_ NICHT \_ ZUGEORDNET**
</dt> <dd> <dl> <dt>

1228 (0x4CC)
</dt> <dt>



Dem Netzwerkendpunkt wurde noch keine Adresse zugeordnet.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONNECTION_INVALID"></span><span id="error_connection_invalid"></span>**FEHLER \_ VERBINDUNG \_ UNGÜLTIG**
</dt> <dd> <dl> <dt>

1229 (0x4CD)
</dt> <dt>



Es wurde versucht, einen Vorgang für eine nicht vorhandene Netzwerkverbindung herzustellen.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONNECTION_ACTIVE"></span><span id="error_connection_active"></span>**FEHLERVERBINDUNG \_ \_ AKTIV**
</dt> <dd> <dl> <dt>

1230 (0x4CE)
</dt> <dt>



Für eine aktive Netzwerkverbindung wurde ein ungültiger Vorgang versucht.


</dt> </dl> </dd> <dt>

<span id="ERROR_NETWORK_UNREACHABLE"></span><span id="error_network_unreachable"></span>**FEHLER \_ NETZWERK \_ NICHT ERREICHBAR**
</dt> <dd> <dl> <dt>

1231 (0x4CF)
</dt> <dt>



Der Netzwerkstandort kann nicht erreicht werden. Informationen zur Netzwerkproblembehandlung finden Sie unter Windows Hilfe.


</dt> </dl> </dd> <dt>

<span id="ERROR_HOST_UNREACHABLE"></span><span id="error_host_unreachable"></span>**FEHLERHOST \_ \_ NICHT ERREICHBAR**
</dt> <dd> <dl> <dt>

1232 (0x4D0)
</dt> <dt>



Der Netzwerkstandort kann nicht erreicht werden. Informationen zur Netzwerkproblembehandlung finden Sie unter Windows Hilfe.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROTOCOL_UNREACHABLE"></span><span id="error_protocol_unreachable"></span>**FEHLERPROTOKOLL \_ \_ NICHT ERREICHBAR**
</dt> <dd> <dl> <dt>

1233 (0x4D1)
</dt> <dt>



Der Netzwerkstandort kann nicht erreicht werden. Informationen zur Netzwerkproblembehandlung finden Sie unter Windows Hilfe.


</dt> </dl> </dd> <dt>

<span id="ERROR_PORT_UNREACHABLE"></span><span id="error_port_unreachable"></span>**FEHLER \_ PORT \_ NICHT ERREICHBAR**
</dt> <dd> <dl> <dt>

1234 (0x4D2)
</dt> <dt>



Am Zielnetzwerkendpunkt auf dem Remotesystem wird kein Dienst betrieben.


</dt> </dl> </dd> <dt>

<span id="ERROR_REQUEST_ABORTED"></span><span id="error_request_aborted"></span>**FEHLERANFORDERUNG \_ \_ ABGEBROCHEN**
</dt> <dd> <dl> <dt>

1235 (0x4D3)
</dt> <dt>



Die Anforderung wurde abgebrochen.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONNECTION_ABORTED"></span><span id="error_connection_aborted"></span>**FEHLER BEIM ABBRECHEN DER \_ VERBINDUNG \_**
</dt> <dd> <dl> <dt>

1236 (0x4D4)
</dt> <dt>



Die Netzwerkverbindung wurde vom lokalen System abgebrochen.


</dt> </dl> </dd> <dt>

<span id="ERROR_RETRY"></span><span id="error_retry"></span>**\_FEHLERWIEDERHOLUNG**
</dt> <dd> <dl> <dt>

1237 (0x4D5)
</dt> <dt>



Der Vorgang konnte nicht abgeschlossen werden. Es sollte ein Wiederholungsversuch ausgeführt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONNECTION_COUNT_LIMIT"></span><span id="error_connection_count_limit"></span>**\_LIMIT FÜR \_ FEHLERVERBINDUNGSANZAHL \_**
</dt> <dd> <dl> <dt>

1238 (0x4D6)
</dt> <dt>



Eine Verbindung mit dem Server konnte nicht hergestellt werden, da der Grenzwert für die Anzahl gleichzeitiger Verbindungen für dieses Konto erreicht wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOGIN_TIME_RESTRICTION"></span><span id="error_login_time_restriction"></span>**EINSCHRÄNKUNG \_ \_ DER ANMELDEZEIT \_ FÜR FEHLER**
</dt> <dd> <dl> <dt>

1239 (0x4D7)
</dt> <dt>



Es wurde versucht, sich während einer nicht autorisierten Tageszeit für dieses Konto anzumelden.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOGIN_WKSTA_RESTRICTION"></span><span id="error_login_wksta_restriction"></span>**FEHLER: \_ \_ WKSTA-EINSCHRÄNKUNG FÜR DIE ANMELDUNG \_**
</dt> <dd> <dl> <dt>

1240 (0x4D8)
</dt> <dt>



Das Konto ist nicht berechtigt, sich von dieser Station aus anzumelden.


</dt> </dl> </dd> <dt>

<span id="ERROR_INCORRECT_ADDRESS"></span><span id="error_incorrect_address"></span>**FEHLER: \_ FALSCHE \_ ADRESSE**
</dt> <dd> <dl> <dt>

1241 (0x4D9)
</dt> <dt>



Die Netzwerkadresse konnte nicht für den angeforderten Vorgang verwendet werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALREADY_REGISTERED"></span><span id="error_already_registered"></span>**FEHLER \_ BEREITS \_ REGISTRIERT**
</dt> <dd> <dl> <dt>

1242 (0x4DA)
</dt> <dt>



Der Dienst ist bereits registriert.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_NOT_FOUND"></span><span id="error_service_not_found"></span>**FEHLERDIENST \_ \_ NICHT \_ GEFUNDEN**
</dt> <dd> <dl> <dt>

1243 (0x4DB)
</dt> <dt>



Der angegebene Dienst ist nicht vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_AUTHENTICATED"></span><span id="error_not_authenticated"></span>**FEHLER \_ NICHT \_ AUTHENTIFIZIERT**
</dt> <dd> <dl> <dt>

1244 (0x4DC)
</dt> <dt>



Der angeforderte Vorgang wurde nicht ausgeführt, da der Benutzer nicht authentifiziert wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_LOGGED_ON"></span><span id="error_not_logged_on"></span>**FEHLER \_ NICHT \_ ANGEMELDET \_**
</dt> <dd> <dl> <dt>

1245 (0x4DD)
</dt> <dt>



Der angeforderte Vorgang wurde nicht ausgeführt, da sich der Benutzer nicht beim Netzwerk angemeldet hat. Der angegebene Dienst ist nicht vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONTINUE"></span><span id="error_continue"></span>**FEHLER \_ FORTSETZEN**
</dt> <dd> <dl> <dt>

1246 (0x4DE)
</dt> <dt>



Fahren Sie mit der Arbeit fort.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALREADY_INITIALIZED"></span><span id="error_already_initialized"></span>**FEHLER \_ WURDE BEREITS \_ INITIALISIERT**
</dt> <dd> <dl> <dt>

1247 (0x4DF)
</dt> <dt>



Es wurde versucht, einen Initialisierungsvorgang auszuführen, wenn die Initialisierung bereits abgeschlossen wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MORE_DEVICES"></span><span id="error_no_more_devices"></span>**FEHLER \_ KEINE \_ WEITEREN \_ GERÄTE**
</dt> <dd> <dl> <dt>

1248 (0x4E0)
</dt> <dt>



Keine lokalen Geräte mehr.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUCH_SITE"></span><span id="error_no_such_site"></span>**FEHLER: \_ KEINE \_ SOLCHE \_ WEBSITE**
</dt> <dd> <dl> <dt>

1249 (0x4E1)
</dt> <dt>



Der angegebene Standort ist nicht vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DOMAIN_CONTROLLER_EXISTS"></span><span id="error_domain_controller_exists"></span>**FEHLER \_ \_ DOMÄNENCONTROLLER \_ VORHANDEN**
</dt> <dd> <dl> <dt>

1250 (0x4E2)
</dt> <dt>



Ein Domänencontroller mit dem angegebenen Namen ist bereits vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_ONLY_IF_CONNECTED"></span><span id="error_only_if_connected"></span>**FEHLER \_ NUR \_ BEI \_ VERBUNDENER VERBINDUNG**
</dt> <dd> <dl> <dt>

1251 (0x4E3)
</dt> <dt>



Dieser Vorgang wird nur unterstützt, wenn Sie mit dem Server verbunden sind.


</dt> </dl> </dd> <dt>

<span id="ERROR_OVERRIDE_NOCHANGES"></span><span id="error_override_nochanges"></span>**\_FEHLERÜBERSCHREIBUNG \_ NOCHANGES**
</dt> <dd> <dl> <dt>

1252 (0x4E4)
</dt> <dt>



Das Gruppenrichtlinienframework sollte die Erweiterung auch dann aufrufen, wenn keine Änderungen vorgenommen werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_USER_PROFILE"></span><span id="error_bad_user_profile"></span>**FEHLER: \_ \_ FEHLERHAFTES \_ BENUTZERPROFIL**
</dt> <dd> <dl> <dt>

1253 (0x4E5)
</dt> <dt>



Der angegebene Benutzer verfügt nicht über ein gültiges Profil.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SUPPORTED_ON_SBS"></span><span id="error_not_supported_on_sbs"></span>**FEHLER \_ WIRD IN \_ \_ \_ SBS NICHT UNTERSTÜTZT**
</dt> <dd> <dl> <dt>

1254 (0x4E6)
</dt> <dt>



Dieser Vorgang wird auf einem Computer, auf dem Windows Server 2003 für Small Business Server ausgeführt wird, nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVER_SHUTDOWN_IN_PROGRESS"></span><span id="error_server_shutdown_in_progress"></span>**FEHLER \_ BEIM HERUNTERFAHREN DES SERVERS \_ IN \_ \_ BEARBEITUNG**
</dt> <dd> <dl> <dt>

1255 (0x4E7)
</dt> <dt>



Der Servercomputer wird heruntergefahren.


</dt> </dl> </dd> <dt>

<span id="ERROR_HOST_DOWN"></span><span id="error_host_down"></span>**FEHLER \_ BEIM \_ HOSTEN**
</dt> <dd> <dl> <dt>

1256 (0x4E8)
</dt> <dt>



Das Remotesystem ist nicht verfügbar. Informationen zur Netzwerkproblembehandlung finden Sie unter Windows Hilfe.


</dt> </dl> </dd> <dt>

<span id="ERROR_NON_ACCOUNT_SID"></span><span id="error_non_account_sid"></span>**FEHLER: \_ NICHT \_ \_ KONTO-SID**
</dt> <dd> <dl> <dt>

1257 (0x4E9)
</dt> <dt>



Die bereitgestellte Sicherheits-ID stammt nicht aus einer Kontodomäne.


</dt> </dl> </dd> <dt>

<span id="ERROR_NON_DOMAIN_SID"></span><span id="error_non_domain_sid"></span>**FEHLER: \_ NICHT \_ \_ DOMÄNEN-SID**
</dt> <dd> <dl> <dt>

1258 (0x4EA)
</dt> <dt>



Der bereitgestellte Sicherheitsbezeichner verfügt nicht über eine Domänenkomponente.


</dt> </dl> </dd> <dt>

<span id="ERROR_APPHELP_BLOCK"></span><span id="error_apphelp_block"></span>**\_FEHLER: \_ APPHELP-BLOCK**
</dt> <dd> <dl> <dt>

1259 (0x4EB)
</dt> <dt>



Das Dialogfeld AppHelp wurde abgebrochen, sodass das Starten der Anwendung verhindert wird.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCESS_DISABLED_BY_POLICY"></span><span id="error_access_disabled_by_policy"></span>**FEHLERZUGRIFF \_ \_ DURCH \_ RICHTLINIE DEAKTIVIERT \_**
</dt> <dd> <dl> <dt>

1260 (0x4EC)
</dt> <dt>



Dieses Programm wird durch eine Gruppenrichtlinie blockiert. Wenden Sie sich an Ihren Systemadministrator, um weitere Informationen zu erfahren.


</dt> </dl> </dd> <dt>

<span id="ERROR_REG_NAT_CONSUMPTION"></span><span id="error_reg_nat_consumption"></span>**FEHLER: \_ REG \_ \_ NAT-VERBRAUCH**
</dt> <dd> <dl> <dt>

1261 (0x4ED)
</dt> <dt>



Ein Programm versucht, einen ungültigen Registerwert zu verwenden. Normalerweise durch ein nicht initialisiertes Register verursacht. Dieser Fehler ist Itanium-spezifisch.


</dt> </dl> </dd> <dt>

<span id="ERROR_CSCSHARE_OFFLINE"></span><span id="error_cscshare_offline"></span>**FEHLER \_ CSCSHARE \_ OFFLINE**
</dt> <dd> <dl> <dt>

1262 (0x4EE)
</dt> <dt>



Die Freigabe ist derzeit offline oder nicht vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_PKINIT_FAILURE"></span><span id="error_pkinit_failure"></span>**FEHLER \_ \_ PKINIT-FEHLER**
</dt> <dd> <dl> <dt>

1263 (0x4EF)
</dt> <dt>



Beim Kerberos-Protokoll ist beim Überprüfen des KDC-Zertifikats während der Smartcard-Anmeldung ein Fehler aufgetreten. Im Systemereignisprotokoll sind weitere Informationen enthalten.


</dt> </dl> </dd> <dt>

<span id="ERROR_SMARTCARD_SUBSYSTEM_FAILURE"></span><span id="error_smartcard_subsystem_failure"></span>**FEHLER: \_ \_ \_ SMARTCARD-SUBSYSTEMFEHLER**
</dt> <dd> <dl> <dt>

1264 (0x4F0)
</dt> <dt>



Das Kerberos-Protokoll hat beim Versuch, das Smartcard-Subsystem zu verwenden, einen Fehler festgestellt.


</dt> </dl> </dd> <dt>

<span id="ERROR_DOWNGRADE_DETECTED"></span><span id="error_downgrade_detected"></span>**FEHLER \_ DOWNGRADE \_ ERKANNT**
</dt> <dd> <dl> <dt>

1265 (0x4F1)
</dt> <dt>



Das System kann keinen Domänencontroller kontaktieren, um die Authentifizierungsanforderung zu bedienen. Versuchen Sie es später noch mal.


</dt> </dl> </dd> <dt>

<span id="ERROR_MACHINE_LOCKED"></span><span id="error_machine_locked"></span>**FEHLERCOMPUTER \_ \_ GESPERRT**
</dt> <dd> <dl> <dt>

1271 (0x4F7)
</dt> <dt>



Der Computer ist gesperrt und kann nicht ohne die Option Force heruntergefahren werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CALLBACK_SUPPLIED_INVALID_DATA"></span><span id="error_callback_supplied_invalid_data"></span>**\_FEHLERRÜCKRUF \_ HAT \_ UNGÜLTIGE DATEN BEREITGESTELLT \_**
</dt> <dd> <dl> <dt>

1273 (0x4F9)
</dt> <dt>



Ein anwendungsdefiniertes Rückruf hat beim Aufruf ungültige Daten gegeben.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYNC_FOREGROUND_REFRESH_REQUIRED"></span><span id="error_sync_foreground_refresh_required"></span>**ERROR \_ SYNC \_ FOREGROUND \_ REFRESH \_ REQUIRED**
</dt> <dd> <dl> <dt>

1274 (0x4FA)
</dt> <dt>



Das Gruppenrichtlinienframework sollte die Erweiterung in der synchronen Aktualisierung der Vordergrundrichtlinie aufrufen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DRIVER_BLOCKED"></span><span id="error_driver_blocked"></span>**FEHLERTREIBER \_ \_ BLOCKIERT**
</dt> <dd> <dl> <dt>

1275 (0x4FB)
</dt> <dt>



Das Laden dieses Treibers wurde blockiert.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_IMPORT_OF_NON_DLL"></span><span id="error_invalid_import_of_non_dll"></span>**FEHLER: \_ \_ UNGÜLTIGER IMPORT \_ EINER \_ \_ NICHT-DLL**
</dt> <dd> <dl> <dt>

1276 (0x4FC)
</dt> <dt>



Eine Dynamic Link Library (DLL) hat auf ein Modul verwiesen, das weder eine DLL noch das ausführbare Image des Prozesses war.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCESS_DISABLED_WEBBLADE"></span><span id="error_access_disabled_webblade"></span>**ERROR \_ ACCESS \_ DISABLED \_ WEBBLADE**
</dt> <dd> <dl> <dt>

1277 (0x4FD)
</dt> <dt>



Windows können dieses Programm nicht öffnen, da es deaktiviert wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCESS_DISABLED_WEBBLADE_TAMPER"></span><span id="error_access_disabled_webblade_tamper"></span>**\_FEHLERZUGRIFF \_ \_ DEAKTIVIERTE \_ WEBBLADE-MANIPULATION**
</dt> <dd> <dl> <dt>

1278 (0x4FE)
</dt> <dt>



Windows können dieses Programm nicht öffnen, da das Lizenzerzwingungssystem manipuliert oder beschädigt wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_RECOVERY_FAILURE"></span><span id="error_recovery_failure"></span>**\_FEHLERWIEDERHERSTELLUNGSFEHLER \_**
</dt> <dd> <dl> <dt>

1279 (0x4FF)
</dt> <dt>



Fehler bei der Wiederherstellung einer Transaktion.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALREADY_FIBER"></span><span id="error_already_fiber"></span>**FEHLER \_ BEREITS \_ FIBER**
</dt> <dd> <dl> <dt>

1280 (0x500)
</dt> <dt>



Der aktuelle Thread wurde bereits in eine Fiber konvertiert.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALREADY_THREAD"></span><span id="error_already_thread"></span>**FEHLER \_ BEREITS \_ THREAD**
</dt> <dd> <dl> <dt>

1281 (0x501)
</dt> <dt>



Der aktuelle Thread wurde bereits aus einer Fiber konvertiert.


</dt> </dl> </dd> <dt>

<span id="ERROR_STACK_BUFFER_OVERRUN"></span><span id="error_stack_buffer_overrun"></span>**FEHLER \_ BEIM \_ \_ STAPELPUFFERÜBERLAUF**
</dt> <dd> <dl> <dt>

1282 (0x502)
</dt> <dt>



Das System hat einen Überlauf eines stapelbasierten Puffers in dieser Anwendung erkannt. Dieser Überlauf könnte es einem böswilligen Benutzer möglicherweise ermöglichen, die Kontrolle über diese Anwendung zu erlangen.


</dt> </dl> </dd> <dt>

<span id="ERROR_PARAMETER_QUOTA_EXCEEDED"></span><span id="error_parameter_quota_exceeded"></span>**\_ \_ FEHLERPARAMETERKONTINGENT \_ ÜBERSCHRITTEN**
</dt> <dd> <dl> <dt>

1283 (0x503)
</dt> <dt>



Daten, die in einem der Parameter vorhanden sind, sind mehr, als die Funktion verarbeiten kann.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEBUGGER_INACTIVE"></span><span id="error_debugger_inactive"></span>**\_FEHLERDEBUGGER \_ INAKTIV**
</dt> <dd> <dl> <dt>

1284 (0x504)
</dt> <dt>



Fehler beim Versuch, einen Vorgang für ein Debugobjekt zu erstellen, weil das Objekt gerade gelöscht wird.


</dt> </dl> </dd> <dt>

<span id="ERROR_DELAY_LOAD_FAILED"></span><span id="error_delay_load_failed"></span>**\_ \_ FEHLER: FEHLER BEIM LADEN DER VERZÖGERUNG \_**
</dt> <dd> <dl> <dt>

1285 (0x505)
</dt> <dt>



Fehler beim Verzögertladen eines .dll oder abrufen einer Funktionsadresse in einem verzögert geladenen .dll.


</dt> </dl> </dd> <dt>

<span id="ERROR_VDM_DISALLOWED"></span><span id="error_vdm_disallowed"></span>**FEHLER \_ VDM \_ NICHT ZULÄSSIG**
</dt> <dd> <dl> <dt>

1286 (0x506)
</dt> <dt>



%1 ist eine 16-Bit-Anwendung. Sie haben keine Berechtigungen zum Ausführen von 16-Bit-Anwendungen. Überprüfen Sie Ihre Berechtigungen mit Ihrem Systemadministrator.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNIDENTIFIED_ERROR"></span><span id="error_unidentified_error"></span>**FEHLER: \_ NICHT \_ IDENTIFIZIERTER FEHLER**
</dt> <dd> <dl> <dt>

1287 (0x507)
</dt> <dt>



Es sind nicht genügend Informationen vorhanden, um die Fehlerursache zu identifizieren.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_CRUNTIME_PARAMETER"></span><span id="error_invalid_cruntime_parameter"></span>**FEHLER: \_ UNGÜLTIGER \_ CRUNTIME-PARAMETER \_**
</dt> <dd> <dl> <dt>

1288 (0x508)
</dt> <dt>



Der an eine C-Laufzeitfunktion übergebene Parameter ist falsch.


</dt> </dl> </dd> <dt>

<span id="ERROR_BEYOND_VDL"></span><span id="error_beyond_vdl"></span>**FEHLER \_ ÜBER \_ VDL HINAUS**
</dt> <dd> <dl> <dt>

1289 (0x509)
</dt> <dt>



Der Vorgang ist über die gültige Datenlänge der Datei hinaus aufgetreten.


</dt> </dl> </dd> <dt>

<span id="ERROR_INCOMPATIBLE_SERVICE_SID_TYPE"></span><span id="error_incompatible_service_sid_type"></span>**FEHLER: \_ INKOMPATIBLER \_ \_ DIENST-SID-TYP \_**
</dt> <dd> <dl> <dt>

1290 (0x50A)
</dt> <dt>



Fehler beim Starten des Diensts, da mindestens ein Dienst im gleichen Prozess über eine inkompatible Dienst-SID-Typeinstellung verfügt. Ein Dienst mit eingeschränktem Dienst-SID-Typ kann nur im selben Prozess mit anderen Diensten mit einem eingeschränkten SID-Typ vorhanden sein. Wenn der Dienst-SID-Typ für diesen Dienst gerade konfiguriert wurde, muss der Hostingprozess neu gestartet werden, um diesen Dienst zu starten.

Auf Windows Server 2003 und Windows XP kann ein uneingeschränkter Dienst nicht gleichzeitig mit anderen Diensten im selben Prozess vorhanden sein. Der Dienst mit dem uneingeschränkten Dienst-SID-Typ muss in einen eigenen Prozess verschoben werden, um diesen Dienst zu starten.


</dt> </dl> </dd> <dt>

<span id="ERROR_DRIVER_PROCESS_TERMINATED"></span><span id="error_driver_process_terminated"></span>**FEHLER: \_ \_ TREIBERPROZESS \_ BEENDET**
</dt> <dd> <dl> <dt>

1291 (0x50B)
</dt> <dt>



Der Prozess, der den Treiber für dieses Gerät hostet, wurde beendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_IMPLEMENTATION_LIMIT"></span><span id="error_implementation_limit"></span>**\_GRENZWERT FÜR FEHLERIMPLEMENTIERUNGEN \_**
</dt> <dd> <dl> <dt>

1292 (0x50C)
</dt> <dt>



Ein Vorgang hat versucht, einen von der Implementierung definierten Grenzwert zu überschreiten.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROCESS_IS_PROTECTED"></span><span id="error_process_is_protected"></span>**FEHLERPROZESS \_ \_ IST \_ GESCHÜTZT**
</dt> <dd> <dl> <dt>

1293 (0x50D)
</dt> <dt>



Entweder der Zielprozess oder der enthaltende Prozess des Zielthreads ist ein geschützter Prozess.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_NOTIFY_CLIENT_LAGGING"></span><span id="error_service_notify_client_lagging"></span>**\_ \_ FEHLERDIENST: \_ \_ CLIENTVERZÖGERUNG BENACHRICHTIGEN**
</dt> <dd> <dl> <dt>

1294 (0x50E)
</dt> <dt>



Der Dienstbenachrichtigungsclient liegt zu weit hinter dem aktuellen Status der Dienste auf dem Computer.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_QUOTA_EXCEEDED"></span><span id="error_disk_quota_exceeded"></span>**FEHLER: \_ \_ DATENTRÄGERKONTINGENT \_ ÜBERSCHRITTEN**
</dt> <dd> <dl> <dt>

1295 (0x50F)
</dt> <dt>



Fehler beim angeforderten Dateivorgang, weil das Speicherkontingent überschritten wurde. Um Speicherplatz frei zu machen, verschieben Sie Dateien an einen anderen Speicherort, oder löschen Sie unnötige Dateien. Wenden Sie sich an Ihren Systemadministrator, um weitere Informationen zu erfahren.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONTENT_BLOCKED"></span><span id="error_content_blocked"></span>**FEHLERINHALT \_ \_ BLOCKIERT**
</dt> <dd> <dl> <dt>

1296 (0x510)
</dt> <dt>



Fehler beim angeforderten Dateivorgang, weil die Speicherrichtlinie diesen Dateityp blockiert. Wenden Sie sich an Ihren Systemadministrator, um weitere Informationen zu erfahren.


</dt> </dl> </dd> <dt>

<span id="ERROR_INCOMPATIBLE_SERVICE_PRIVILEGE"></span><span id="error_incompatible_service_privilege"></span>**FEHLER: \_ INKOMPATIBLE \_ \_ DIENSTBERECHTIGUNG**
</dt> <dd> <dl> <dt>

1297 (0x511)
</dt> <dt>



Eine Berechtigung, die der Dienst benötigt, um ordnungsgemäß zu funktionieren, ist in der Dienstkontokonfiguration nicht vorhanden. Sie können das MMC-Snap-In (Services Microsoft Management Console) (services.msc) und das MMC-Snap-In lokale Sicherheit Einstellungen (secpol.msc) verwenden, um die Dienstkonfiguration und die Kontokonfiguration anzuzeigen.


</dt> </dl> </dd> <dt>

<span id="ERROR_APP_HANG"></span><span id="error_app_hang"></span>**FEHLER: \_ \_ APP HÄNGT**
</dt> <dd> <dl> <dt>

1298 (0x512)
</dt> <dt>



Ein an diesem Vorgang beteiligter Thread reagiert anscheinend nicht.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LABEL"></span><span id="error_invalid_label"></span>**FEHLER: \_ UNGÜLTIGE \_ BEZEICHNUNG**
</dt> <dd> <dl> <dt>

1299 (0x513)
</dt> <dt>



Gibt an, dass eine bestimmte Sicherheits-ID möglicherweise nicht als Bezeichnung eines Objekts zugewiesen wird.


</dt> </dl> </dd> </dl>


## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>WinError.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Systemfehlercodes](system-error-codes.md)
</dt> </dl>

 

 




