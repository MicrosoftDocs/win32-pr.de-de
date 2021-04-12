---
description: Beschreibt die in der Header Datei "Winerror. h" definierten Fehlercodes 1000-1299 und ist für Entwickler bestimmt.
ms.assetid: 0061feb6-e1a0-4fcd-8f80-954087c799d7
title: System Fehler Codes (1000-1299) (Winerror. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 592bd5c6653526d87fed05d6ec76f739355ae359
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523715"
---
# <a name="system-error-codes-1000-1299"></a>System Fehler Codes (1000-1299)

> [!NOTE]
> Diese Informationen sind für Entwickler gedacht, die Systemfehler Debuggen. Bei anderen Fehlern, wie z. b. Problemen mit Windows Update, finden Sie eine Liste der Ressourcen auf der Seite [Fehlercodes](system-error-codes.md) .

In der folgenden Liste werden die [Systemfehler Codes](system-error-codes.md) für die Fehler 1000 bis 1299 beschrieben. Sie werden von der [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) -Funktion zurückgegeben, wenn viele Funktionen fehlschlagen. Um den Beschreibungstext für den Fehler in Ihrer Anwendung abzurufen, verwenden Sie die [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) -Funktion mit dem Flag " **Format \_ Message \_ from \_ System** ".

<dl> <dt>

<span id="ERROR_STACK_OVERFLOW"></span><span id="error_stack_overflow"></span>**Fehler \_ Stapel \_ Überlauf**
</dt> <dd> <dl> <dt>

1001 (0x3e9)
</dt> <dt>



Rekursion zu tief Überlauf des Stapels.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MESSAGE"></span><span id="error_invalid_message"></span>**\_ungültige \_ Meldung für Fehler**
</dt> <dd> <dl> <dt>

1002 (0x3ea)
</dt> <dt>



Das Fenster kann nicht für die gesendete Nachricht fungieren.


</dt> </dl> </dd> <dt>

<span id="ERROR_CAN_NOT_COMPLETE"></span><span id="error_can_not_complete"></span>**der Fehler \_ kann \_ nicht \_ vervollständigt werden.**
</dt> <dd> <dl> <dt>

1003 (0x3eb)
</dt> <dt>



Diese Funktion kann nicht ausgeführt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_FLAGS"></span><span id="error_invalid_flags"></span>**\_ungültige \_ Flags.**
</dt> <dd> <dl> <dt>

1004 (0x3ec)
</dt> <dt>



Ungültige Flags.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNRECOGNIZED_VOLUME"></span><span id="error_unrecognized_volume"></span>**Fehler \_ unbekanntes \_ Volume**
</dt> <dd> <dl> <dt>

1005 (0x3ed)
</dt> <dt>



Das Volume enthält kein bekanntes Dateisystem. Stellen Sie sicher, dass alle erforderlichen Dateisystem Treiber geladen sind und das Volume nicht beschädigt ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_INVALID"></span><span id="error_file_invalid"></span>**Fehler \_ Datei \_ ungültig**
</dt> <dd> <dl> <dt>

1006 (0x3EE)
</dt> <dt>



Das Volume für eine Datei wurde extern geändert, sodass die geöffnete Datei nicht mehr gültig ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_FULLSCREEN_MODE"></span><span id="error_fullscreen_mode"></span>**Fehler im \_ voll Bild \_ Modus**
</dt> <dd> <dl> <dt>

1007 (0x3ef)
</dt> <dt>



Der angeforderte Vorgang kann nicht im Vollbildmodus ausgeführt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_TOKEN"></span><span id="error_no_token"></span>**Fehler \_ ohne \_ Token**
</dt> <dd> <dl> <dt>

1008 (0x3f 0)
</dt> <dt>



Es wurde versucht, auf ein nicht vorhandenes Token zu verweisen.


</dt> </dl> </dd> <dt>

<span id="ERROR_BADDB"></span><span id="error_baddb"></span>**Fehler \_ baddb**
</dt> <dd> <dl> <dt>

1009 (0x3f 1)
</dt> <dt>



Die Konfigurations Registrierungsdatenbank ist beschädigt.


</dt> </dl> </dd> <dt>

<span id="ERROR_BADKEY"></span><span id="error_badkey"></span>**Fehler \_ badkey**
</dt> <dd> <dl> <dt>

1010 (0x3f 2)
</dt> <dt>



Der Konfigurations Registrierungsschlüssel ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANTOPEN"></span><span id="error_cantopen"></span>**Fehler- \_ cantopen**
</dt> <dd> <dl> <dt>

1011 (0x3f)
</dt> <dt>



Der Konfigurations Registrierungsschlüssel konnte nicht geöffnet werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANTREAD"></span><span id="error_cantread"></span>**Fehler- \_ cantread**
</dt> <dd> <dl> <dt>

1012 (0x3f 4)
</dt> <dt>



Der Konfigurations Registrierungsschlüssel konnte nicht gelesen werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANTWRITE"></span><span id="error_cantwrite"></span>**Fehler beim \_ kanschreiben**
</dt> <dd> <dl> <dt>

1013 (0x3f)
</dt> <dt>



Der Konfigurations Registrierungsschlüssel konnte nicht geschrieben werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_REGISTRY_RECOVERED"></span><span id="error_registry_recovered"></span>**Fehler \_ Registrierung \_ wieder hergestellt**
</dt> <dd> <dl> <dt>

1014 (0x3f)
</dt> <dt>



Eine der Dateien in der Registrierungsdatenbank musste mithilfe eines Protokolls oder einer alternativen Kopie wieder hergestellt werden. Die Wiederherstellung war erfolgreich.


</dt> </dl> </dd> <dt>

<span id="ERROR_REGISTRY_CORRUPT"></span><span id="error_registry_corrupt"></span>**Fehler \_ Registrierung \_ beschädigt**
</dt> <dd> <dl> <dt>

1015 (0x3f)
</dt> <dt>



Die Registrierung ist beschädigt. Die Struktur einer der Dateien, die Registrierungsdaten enthalten, ist beschädigt, oder das Speicher Abbild des Systems der Datei ist beschädigt, oder die Datei konnte nicht wieder hergestellt werden, da die Alternative Kopie oder das alternative Protokoll nicht vorhanden oder beschädigt war.


</dt> </dl> </dd> <dt>

<span id="ERROR_REGISTRY_IO_FAILED"></span><span id="error_registry_io_failed"></span>**Fehler Registrierungs-e/a Fehler \_ \_ \_**
</dt> <dd> <dl> <dt>

1016 (0x3f 8)
</dt> <dt>



Ein e/a-Vorgang, der von der Registrierung initiiert wurde, ist nicht wiederherstellbar. Eine der Dateien, die das System Abbild der Registrierung enthalten, konnte von der Registrierung nicht gelesen, geschrieben oder geleert werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_REGISTRY_FILE"></span><span id="error_not_registry_file"></span>**Fehler bei der \_ \_ Registrierungs \_ Datei.**
</dt> <dd> <dl> <dt>

1017 (0x3f 9)
</dt> <dt>



Das System hat versucht, eine Datei in die Registrierung zu laden oder wiederherzustellen, aber die angegebene Datei weist nicht das Registrierungsdatei Format auf.


</dt> </dl> </dd> <dt>

<span id="ERROR_KEY_DELETED"></span><span id="error_key_deleted"></span>**Fehler \_ Schlüssel \_ gelöscht**
</dt> <dd> <dl> <dt>

1018 (0x3fa)
</dt> <dt>



Ungültiger Vorgang für einen Registrierungsschlüssel, der zum Löschen markiert wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_LOG_SPACE"></span><span id="error_no_log_space"></span>**Fehler \_ ohne \_ Protokoll \_ Speicher**
</dt> <dd> <dl> <dt>

1019 (0x3fb)
</dt> <dt>



Das System konnte den erforderlichen Speicherplatz nicht in einem Registrierungs Protokoll zuordnen.


</dt> </dl> </dd> <dt>

<span id="ERROR_KEY_HAS_CHILDREN"></span><span id="error_key_has_children"></span>**Fehler \_ Schlüssel \_ hat untergeordnete Elemente \_**
</dt> <dd> <dl> <dt>

1020 (0x3fc)
</dt> <dt>



In einem Registrierungsschlüssel, der bereits über Unterschlüssel oder Werte verfügt, kann keine symbolische Verknüpfung erstellt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CHILD_MUST_BE_VOLATILE"></span><span id="error_child_must_be_volatile"></span>**Fehler untergeordnetes Element \_ \_ muss \_ \_ flüchtig sein**
</dt> <dd> <dl> <dt>

1021 (0x3fd)
</dt> <dt>



Unter einem flüchtigen übergeordneten Schlüssel kann kein stabiler Unterschlüssel erstellt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOTIFY_ENUM_DIR"></span><span id="error_notify_enum_dir"></span>**Fehler beim einschließen der Aufzählung. \_ \_ \_**
</dt> <dd> <dl> <dt>

1022 (0x3fe)
</dt> <dt>



Ein Benachrichtigungs Change Request wird abgeschlossen, und die Informationen werden nicht im Puffer des Aufrufers zurückgegeben. Der Aufrufer muss nun die Dateien aufzählen, um die Änderungen zu finden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEPENDENT_SERVICES_RUNNING"></span><span id="error_dependent_services_running"></span>**Fehler \_ abhängige \_ Dienste werden \_ ausgeführt.**
</dt> <dd> <dl> <dt>

1051 (0x41b)
</dt> <dt>



Ein Steuerelement für die Beendigung wurde an einen Dienst gesendet, von dem andere ausgelaufende Dienste abhängig sind.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SERVICE_CONTROL"></span><span id="error_invalid_service_control"></span>**\_ungültige \_ Dienst \_ Kontrolle.**
</dt> <dd> <dl> <dt>

1052 (0x41c)
</dt> <dt>



Das angeforderte Steuerelement ist für diesen Dienst ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_REQUEST_TIMEOUT"></span><span id="error_service_request_timeout"></span>**Timeout für Fehler \_ Dienst \_ Anforderung \_**
</dt> <dd> <dl> <dt>

1053 (0x41d)
</dt> <dt>



Der Dienst antwortete nicht rechtzeitig auf die Start- oder Steuerungsanforderung.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_NO_THREAD"></span><span id="error_service_no_thread"></span>**Fehler \_ Dienst \_ ohne \_ Thread**
</dt> <dd> <dl> <dt>

1054 (0x41e)
</dt> <dt>



Für den Dienst konnte kein Thread erstellt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_DATABASE_LOCKED"></span><span id="error_service_database_locked"></span>**Fehler \_ Dienst \_ Datenbank \_ gesperrt**
</dt> <dd> <dl> <dt>

1055 (0x41f)
</dt> <dt>



Die Dienst Datenbank ist gesperrt.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_ALREADY_RUNNING"></span><span id="error_service_already_running"></span>**der Fehler \_ Dienst wird \_ bereits \_ ausgeführt.**
</dt> <dd> <dl> <dt>

1056 (0x420)
</dt> <dt>



Eine Instanz des Dienstanbieter wird bereits ausgeführt.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SERVICE_ACCOUNT"></span><span id="error_invalid_service_account"></span>**\_ungültiges \_ Dienst \_ Konto.**
</dt> <dd> <dl> <dt>

1057 (0x421)
</dt> <dt>



Der Kontoname ist ungültig oder nicht vorhanden, oder das Kennwort für den angegebenen Kontonamen ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_DISABLED"></span><span id="error_service_disabled"></span>**Fehler \_ Dienst \_ deaktiviert**
</dt> <dd> <dl> <dt>

1058 (0x422)
</dt> <dt>



Der Dienst kann nicht gestartet werden, weil er deaktiviert wurde oder weil ihm keine aktivierten Geräte zugeordnet sind.


</dt> </dl> </dd> <dt>

<span id="ERROR_CIRCULAR_DEPENDENCY"></span><span id="error_circular_dependency"></span>**Fehler \_ zirkuläre \_ Abhängigkeit**
</dt> <dd> <dl> <dt>

1059 (0x423)
</dt> <dt>



Es wurde eine zirkuläre Dienst Abhängigkeit angegeben.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_DOES_NOT_EXIST"></span><span id="error_service_does_not_exist"></span>**der Fehler \_ Dienst \_ ist \_ nicht \_ vorhanden.**
</dt> <dd> <dl> <dt>

1060 (0x424)
</dt> <dt>



Der angegebene Dienst ist nicht als installierter Dienst vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_CANNOT_ACCEPT_CTRL"></span><span id="error_service_cannot_accept_ctrl"></span>**Fehler \_ Dienst \_ kann \_ STRG nicht akzeptieren \_ .**
</dt> <dd> <dl> <dt>

1061 (0x425)
</dt> <dt>



Der Dienst kann zurzeit keine Steuerungs Meldungen akzeptieren.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_NOT_ACTIVE"></span><span id="error_service_not_active"></span>**Fehler \_ Dienst \_ nicht \_ aktiv**
</dt> <dd> <dl> <dt>

1062 (0x426)
</dt> <dt>



Der Dienst wurde nicht gestartet.


</dt> </dl> </dd> <dt>

<span id="ERROR_FAILED_SERVICE_CONTROLLER_CONNECT"></span><span id="error_failed_service_controller_connect"></span>**Fehler \_ bei \_ Dienst \_ Controller \_ Verbindung.**
</dt> <dd> <dl> <dt>

1063 (0x427)
</dt> <dt>



Vom Dienst Prozess konnte keine Verbindung mit dem Dienst Controller hergestellt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_EXCEPTION_IN_SERVICE"></span><span id="error_exception_in_service"></span>**Fehler \_ Ausnahme \_ im \_ Dienst.**
</dt> <dd> <dl> <dt>

1064 (0x428)
</dt> <dt>



Beim Verarbeiten der Steuerungs Anforderung ist eine Ausnahme im Dienst aufgetreten.


</dt> </dl> </dd> <dt>

<span id="ERROR_DATABASE_DOES_NOT_EXIST"></span><span id="error_database_does_not_exist"></span>**Fehler \_ Datenbank \_ ist \_ nicht \_ vorhanden.**
</dt> <dd> <dl> <dt>

1065 (0x429)
</dt> <dt>



Die angegebene Datenbank ist nicht vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_SPECIFIC_ERROR"></span><span id="error_service_specific_error"></span>**Fehler \_ Dienst \_ spezifischer \_ Fehler**
</dt> <dd> <dl> <dt>

1066 (0x42a)
</dt> <dt>



Der Dienst hat einen Dienst spezifischen Fehlercode zurückgegeben.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROCESS_ABORTED"></span><span id="error_process_aborted"></span>**Fehler \_ Prozess \_ abgebrochen**
</dt> <dd> <dl> <dt>

1067 (0x42b)
</dt> <dt>



Der Prozess wurde unerwartet beendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_DEPENDENCY_FAIL"></span><span id="error_service_dependency_fail"></span>**Fehler \_ Dienst- \_ Abhängigkeitsfehler \_**
</dt> <dd> <dl> <dt>

1068 (0x42c)
</dt> <dt>



Der Abhängigkeits Dienst oder die Abhängigkeits Gruppe konnte nicht gestartet werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_LOGON_FAILED"></span><span id="error_service_logon_failed"></span>**Fehler beim Anmelden des Fehler \_ Diensts \_ \_**
</dt> <dd> <dl> <dt>

1069 (0x42d)
</dt> <dt>



Der Dienst konnte wegen einer fehlerhaften Anmeldung nicht gestartet werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_START_HANG"></span><span id="error_service_start_hang"></span>**Fehler \_ beim \_ Starten des dienstanhangs \_**
</dt> <dd> <dl> <dt>

1070 (0x42e)
</dt> <dt>



Nachdem der Dienst gestartet wurde, hat der Dienst nicht mehr reagiert.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SERVICE_LOCK"></span><span id="error_invalid_service_lock"></span>**\_ungültige \_ Dienst \_ Sperre.**
</dt> <dd> <dl> <dt>

1071 (0x42f)
</dt> <dt>



Die angegebene Dienst Datenbanksperre ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_MARKED_FOR_DELETE"></span><span id="error_service_marked_for_delete"></span>**der Fehler \_ Dienst wurde \_ \_ zum \_ Löschen markiert.**
</dt> <dd> <dl> <dt>

1072 (0x430)
</dt> <dt>



Der angegebene Dienst wurde zum Löschen markiert.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_EXISTS"></span><span id="error_service_exists"></span>**Fehler \_ Dienst \_ vorhanden**
</dt> <dd> <dl> <dt>

1073 (0x431)
</dt> <dt>



Der angegebene Dienst ist bereits vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALREADY_RUNNING_LKG"></span><span id="error_already_running_lkg"></span>**Fehler \_ beim \_ Ausführen von \_ LKG.**
</dt> <dd> <dl> <dt>

1074 (0x432)
</dt> <dt>



Das System wird zurzeit mit der zuletzt bekannten, ordnungsgemäßen Konfiguration ausgeführt.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_DEPENDENCY_DELETED"></span><span id="error_service_dependency_deleted"></span>**Fehler \_ Dienst \_ Abhängigkeit \_ gelöscht**
</dt> <dd> <dl> <dt>

1075 (0x433)
</dt> <dt>



Der Abhängigkeits Dienst ist nicht vorhanden oder wurde zum Löschen markiert.


</dt> </dl> </dd> <dt>

<span id="ERROR_BOOT_ALREADY_ACCEPTED"></span><span id="error_boot_already_accepted"></span>**Fehler beim \_ Start \_ bereits \_ akzeptiert.**
</dt> <dd> <dl> <dt>

1076 (0x434)
</dt> <dt>



Der aktuelle Start wurde bereits für die Verwendung als zuletzt bekannter, funktionierendes Steuerelement akzeptiert.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_NEVER_STARTED"></span><span id="error_service_never_started"></span>**Fehler \_ Dienst wurde \_ nie \_ gestartet.**
</dt> <dd> <dl> <dt>

1077 (0x435)
</dt> <dt>



Seit dem letzten Start wurden keine Versuche unternommen, den Dienst zu starten.


</dt> </dl> </dd> <dt>

<span id="ERROR_DUPLICATE_SERVICE_NAME"></span><span id="error_duplicate_service_name"></span>**Fehler beim \_ doppelten \_ Dienst \_ Namen.**
</dt> <dd> <dl> <dt>

1078 (0x436)
</dt> <dt>



Der Name wird bereits als Dienst Name oder Dienst Anzeige Name verwendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_DIFFERENT_SERVICE_ACCOUNT"></span><span id="error_different_service_account"></span>**Fehler \_ anderes \_ Dienst \_ Konto**
</dt> <dd> <dl> <dt>

1079 (0x437)
</dt> <dt>



Das für diesen Dienst angegebene Konto unterscheidet sich von dem Konto, das für andere Dienste angegeben wurde, die im selben Prozess ausgeführt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_DETECT_DRIVER_FAILURE"></span><span id="error_cannot_detect_driver_failure"></span>**Fehler \_ beim \_ Erkennen des \_ Treiber \_ Fehlers.**
</dt> <dd> <dl> <dt>

1080 (0x438)
</dt> <dt>



Fehler Aktionen können nur für Win32-Dienste, nicht für Treiber, festgelegt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_DETECT_PROCESS_ABORT"></span><span id="error_cannot_detect_process_abort"></span>**Fehler \_ beim \_ Erkennen des \_ Prozess \_ Abbruchs.**
</dt> <dd> <dl> <dt>

1081 (0x439)
</dt> <dt>



Dieser Dienst wird in demselben Prozess wie der Dienststeuerungs-Manager ausgeführt. Daher kann der Dienststeuerungs-Manager keine Maßnahmen ergreifen, wenn dieser Dienst Prozess unerwartet beendet wird.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_RECOVERY_PROGRAM"></span><span id="error_no_recovery_program"></span>**Fehler " \_ kein \_ Wiederherstellungs \_ Programm"**
</dt> <dd> <dl> <dt>

1082 (0x43a)
</dt> <dt>



Es wurde kein Wiederherstellungsprogramm für diesen Dienst konfiguriert.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_NOT_IN_EXE"></span><span id="error_service_not_in_exe"></span>**Fehler \_ Dienst \_ nicht \_ in \_ exe**
</dt> <dd> <dl> <dt>

1083 (0x43b)
</dt> <dt>



Das ausführbare Programm, mit dem dieser Dienst für die Durchführung konfiguriert ist, implementiert den Dienst nicht.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SAFEBOOT_SERVICE"></span><span id="error_not_safeboot_service"></span>**Fehler \_ beim \_ SafeBoot- \_ Dienst.**
</dt> <dd> <dl> <dt>

1084 (0x43c)
</dt> <dt>



Dieser Dienst kann nicht im abgesicherten Modus gestartet werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_END_OF_MEDIA"></span><span id="error_end_of_media"></span>**Fehler \_ Ende \_ des \_ Mediums**
</dt> <dd> <dl> <dt>

1100 (0x44c)
</dt> <dt>



Das physische Ende des Bands wurde erreicht.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILEMARK_DETECTED"></span><span id="error_filemark_detected"></span>**Fehler \_ Datei Markierung \_ erkannt**
</dt> <dd> <dl> <dt>

1101 (0x44d)
</dt> <dt>



Ein Band Zugriff hat ein Datei Zeichen erreicht.


</dt> </dl> </dd> <dt>

<span id="ERROR_BEGINNING_OF_MEDIA"></span><span id="error_beginning_of_media"></span>**Fehler beim \_ Start \_ des \_ Mediums.**
</dt> <dd> <dl> <dt>

1102 (0x44e)
</dt> <dt>



Der Anfang des Bands oder eine Partition wurde gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_SETMARK_DETECTED"></span><span id="error_setmark_detected"></span>**Fehler- \_ setmark \_ erkannt**
</dt> <dd> <dl> <dt>

1103 (0x44f)
</dt> <dt>



Ein Band Zugriff hat das Ende eines Satzes von Dateien erreicht.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_DATA_DETECTED"></span><span id="error_no_data_detected"></span>**Fehler \_ beim \_ Erkennen von Daten. \_**
</dt> <dd> <dl> <dt>

1104 (0x450)
</dt> <dt>



Es befinden sich keine weiteren Daten auf dem Band.


</dt> </dl> </dd> <dt>

<span id="ERROR_PARTITION_FAILURE"></span><span id="error_partition_failure"></span>**Fehler \_ Partitions \_ Fehler**
</dt> <dd> <dl> <dt>

1105 (0x451)
</dt> <dt>



Das Band konnte nicht partitioniert werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_BLOCK_LENGTH"></span><span id="error_invalid_block_length"></span>**Fehler \_ ungültige \_ Block \_ Länge.**
</dt> <dd> <dl> <dt>

1106 (0x452)
</dt> <dt>



Beim Zugriff auf ein neues Band einer Partition mit mehreren Volumes ist die aktuelle Blockgröße falsch.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_NOT_PARTITIONED"></span><span id="error_device_not_partitioned"></span>**Fehler \_ Gerät \_ nicht \_ partitioniert**
</dt> <dd> <dl> <dt>

1107 (0x453)
</dt> <dt>



Beim Laden eines Bands konnten keine Band Partitionsinformationen gefunden werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_LOCK_MEDIA"></span><span id="error_unable_to_lock_media"></span>**Fehler \_ beim \_ \_ Sperren des \_ Mediums.**
</dt> <dd> <dl> <dt>

1108 (0x454)
</dt> <dt>



Der Auswerfen-Mechanismus für Medien kann nicht gesperrt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_UNLOAD_MEDIA"></span><span id="error_unable_to_unload_media"></span>**Fehler \_ beim \_ \_ Entladen des \_ Mediums.**
</dt> <dd> <dl> <dt>

1109 (0x455)
</dt> <dt>



Das Medium kann nicht entladen werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEDIA_CHANGED"></span><span id="error_media_changed"></span>**Fehler \_ Medien \_ geändert**
</dt> <dd> <dl> <dt>

1110 (0x456)
</dt> <dt>



Möglicherweise hat sich das Medium auf dem Laufwerk geändert.


</dt> </dl> </dd> <dt>

<span id="ERROR_BUS_RESET"></span><span id="error_bus_reset"></span>**\_ \_ Zurücksetzen des Fehler Busses**
</dt> <dd> <dl> <dt>

1111 (0x457)
</dt> <dt>



Der e/a-Bus wurde zurückgesetzt.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MEDIA_IN_DRIVE"></span><span id="error_no_media_in_drive"></span>**Fehler " \_ kein \_ Medium \_ in \_ Laufwerk"**
</dt> <dd> <dl> <dt>

1112 (0x458)
</dt> <dt>



Kein Medium in Laufwerk.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_UNICODE_TRANSLATION"></span><span id="error_no_unicode_translation"></span>**Fehler \_ keine \_ Unicode- \_ Übersetzung**
</dt> <dd> <dl> <dt>

1113 (0x459)
</dt> <dt>



Auf der Multi-Byte-Ziel Codepage ist keine Zuordnung für das Unicode-Zeichen vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DLL_INIT_FAILED"></span><span id="error_dll_init_failed"></span>**Fehler bei DLL-Initialisierung. \_ \_ \_**
</dt> <dd> <dl> <dt>

1114 (0x45a)
</dt> <dt>



Fehler bei einer Initialisierungs Routine für eine Dynamic Link Library (dll).


</dt> </dl> </dd> <dt>

<span id="ERROR_SHUTDOWN_IN_PROGRESS"></span><span id="error_shutdown_in_progress"></span>**Fehler \_ beim Herunterfahren. \_ \_**
</dt> <dd> <dl> <dt>

1115 (0x45b)
</dt> <dt>



Ein System wird heruntergefahren.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SHUTDOWN_IN_PROGRESS"></span><span id="error_no_shutdown_in_progress"></span>**Fehler \_ \_ beim herunter \_ fahren \_ .**
</dt> <dd> <dl> <dt>

1116 (0x45c)
</dt> <dt>



Das Herunterfahren des Systems kann nicht abgebrochen werden, weil das Herunterfahren nicht durchgeführt wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_IO_DEVICE"></span><span id="error_io_device"></span>**Fehler- \_ IO- \_ Gerät**
</dt> <dd> <dl> <dt>

1117 (0x45d)
</dt> <dt>



Die Anforderung konnte aufgrund eines E/A-Gerätefehlers nicht ausgeführt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERIAL_NO_DEVICE"></span><span id="error_serial_no_device"></span>**Fehler " \_ seriell \_ kein \_ Gerät"**
</dt> <dd> <dl> <dt>

1118 (0x45e)
</dt> <dt>



Es wurde kein serielles Gerät erfolgreich initialisiert. Der serielle Treiber wird entladen.


</dt> </dl> </dd> <dt>

<span id="ERROR_IRQ_BUSY"></span><span id="error_irq_busy"></span>**Fehler \_ : UNQ \_ ausgelastet**
</dt> <dd> <dl> <dt>

1119 (0x45f)
</dt> <dt>



Ein Gerät, das eine Interrupt-Anforderung (UNQ) mit anderen Geräten gemeinsam genutzt hat, kann nicht geöffnet werden. Mindestens ein anderes Gerät, das diesen UNQ verwendet, wurde bereits geöffnet.


</dt> </dl> </dd> <dt>

<span id="ERROR_MORE_WRITES"></span><span id="error_more_writes"></span>**Fehler \_ Weitere \_ Schreibvorgänge**
</dt> <dd> <dl> <dt>

1120 (0x460)
</dt> <dt>



Ein serieller e/A-Vorgang wurde durch einen anderen Schreibvorgang an den seriellen Anschluss abgeschlossen. Der serielle XOFF-Wert von IOCTL hat \_ \_ \_ Null erreicht.)


</dt> </dl> </dd> <dt>

<span id="ERROR_COUNTER_TIMEOUT"></span><span id="error_counter_timeout"></span>**Fehler \_ Zählers- \_ Timeout**
</dt> <dd> <dl> <dt>

1121 (0x461)
</dt> <dt>



Ein serieller e/A-Vorgang wurde abgeschlossen, da der Timeout Zeitraum abgelaufen ist. Der serielle XOFF-Wert von IOCTL \_ \_ \_ hat keine Null erreicht.)


</dt> </dl> </dd> <dt>

<span id="ERROR_FLOPPY_ID_MARK_NOT_FOUND"></span><span id="error_floppy_id_mark_not_found"></span>**Fehler \_ Disketten \_ Kennung \_ \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

1122 (0x462)
</dt> <dt>



Auf der Diskette wurde keine ID-Adress Markierung gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_FLOPPY_WRONG_CYLINDER"></span><span id="error_floppy_wrong_cylinder"></span>**Fehler \_ Disketten \_ \_ Zylinder**
</dt> <dd> <dl> <dt>

1123 (0x463)
</dt> <dt>



Konflikt zwischen dem Feld für die ID des Disketten Datenträgers und der Nachverfolgung der Disketten Adresse des Disketten Controllers.


</dt> </dl> </dd> <dt>

<span id="ERROR_FLOPPY_UNKNOWN_ERROR"></span><span id="error_floppy_unknown_error"></span>**Fehler \_ Disketten \_ unbekannter \_ Fehler.**
</dt> <dd> <dl> <dt>

1124 (0x464)
</dt> <dt>



Der Disketten Controller hat einen Fehler gemeldet, der vom Disketten Treiber nicht erkannt wird.


</dt> </dl> </dd> <dt>

<span id="ERROR_FLOPPY_BAD_REGISTERS"></span><span id="error_floppy_bad_registers"></span>**Fehler \_ Disketten \_ \_ Register**
</dt> <dd> <dl> <dt>

1125 (0x465)
</dt> <dt>



Der Disketten Controller hat inkonsistente Ergebnisse in seinen Registern zurückgegeben.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_RECALIBRATE_FAILED"></span><span id="error_disk_recalibrate_failed"></span>**Fehler \_ beim \_ Neuinitialisieren des Fehlers. \_**
</dt> <dd> <dl> <dt>

1126 (0x466)
</dt> <dt>



Beim Zugriff auf die Festplatte ist ein Wiederholungs Vorgang auch nach Wiederholungs versuchen fehlgeschlagen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_OPERATION_FAILED"></span><span id="error_disk_operation_failed"></span>**Fehler beim \_ Festplatten \_ Vorgang. \_**
</dt> <dd> <dl> <dt>

1127 (0x467)
</dt> <dt>



Beim Zugriff auf die Festplatte ist ein Datenträger Vorgang auch nach Wiederholungs versuchen fehlgeschlagen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_RESET_FAILED"></span><span id="error_disk_reset_failed"></span>**Fehler \_ beim \_ Zurücksetzen des Datenträgers \_**
</dt> <dd> <dl> <dt>

1128 (0x468)
</dt> <dt>



Beim Zugriff auf die Festplatte war eine Datenträger Controller-zurück Setzung erforderlich, aber auch dies ist nicht erfolgreich.


</dt> </dl> </dd> <dt>

<span id="ERROR_EOM_OVERFLOW"></span><span id="error_eom_overflow"></span>**Fehler bei \_ EOM- \_ Überlauf**
</dt> <dd> <dl> <dt>

1129 (0x469)
</dt> <dt>



Das physische Ende des Bands ist aufgetreten.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_ENOUGH_SERVER_MEMORY"></span><span id="error_not_enough_server_memory"></span>**Fehler \_ nicht \_ genug \_ Server \_ Arbeitsspeicher**
</dt> <dd> <dl> <dt>

1130 (0x46a)
</dt> <dt>



Für diesen Befehl ist nicht genügend Serverspeicher verfügbar.


</dt> </dl> </dd> <dt>

<span id="ERROR_POSSIBLE_DEADLOCK"></span><span id="error_possible_deadlock"></span>**Fehler \_ möglicher \_ Deadlock**
</dt> <dd> <dl> <dt>

1131 (0x46b)
</dt> <dt>



Es wurde eine potenzielle Deadlockbedingung erkannt.


</dt> </dl> </dd> <dt>

<span id="ERROR_MAPPED_ALIGNMENT"></span><span id="error_mapped_alignment"></span>**Fehler beim Zuordnen der \_ \_ Ausrichtung**
</dt> <dd> <dl> <dt>

1132 (0x46c)
</dt> <dt>



Die angegebene Basisadresse oder der angegebene Dateioffset weist nicht die richtige Ausrichtung auf.


</dt> </dl> </dd> <dt>

<span id="ERROR_SET_POWER_STATE_VETOED"></span><span id="error_set_power_state_vetoed"></span>**Fehler beim \_ Festlegen des \_ Energie \_ Zustands \_ .**
</dt> <dd> <dl> <dt>

1140 (0x474)
</dt> <dt>



Der Versuch, den System Energiezustand zu ändern, wurde von einer anderen Anwendung oder einem anderen Treiber geprüft.


</dt> </dl> </dd> <dt>

<span id="ERROR_SET_POWER_STATE_FAILED"></span><span id="error_set_power_state_failed"></span>**Fehler beim \_ Festlegen des \_ Energie \_ Zustands \_ .**
</dt> <dd> <dl> <dt>

1141 (0x475)
</dt> <dt>



Vom System-BIOS konnte der System Energiezustand nicht geändert werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_LINKS"></span><span id="error_too_many_links"></span>**Fehler \_ zu \_ viele \_ Verknüpfungen**
</dt> <dd> <dl> <dt>

1142 (0x476)
</dt> <dt>



Es wurde versucht, mehr Verknüpfungen für eine Datei zu erstellen, als das Dateisystem unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_OLD_WIN_VERSION"></span><span id="error_old_win_version"></span>**Fehler \_ alte \_ Win- \_ Version**
</dt> <dd> <dl> <dt>

1150 (0x47e)
</dt> <dt>



Das angegebene Programm erfordert eine neuere Version von Windows.


</dt> </dl> </dd> <dt>

<span id="ERROR_APP_WRONG_OS"></span><span id="error_app_wrong_os"></span>**Fehler- \_ App- \_ falsches \_ Betriebssystem**
</dt> <dd> <dl> <dt>

1151 (0x47f)
</dt> <dt>



Das angegebene Programm ist keine MS-DOS- oder Windows-Anwendung.


</dt> </dl> </dd> <dt>

<span id="ERROR_SINGLE_INSTANCE_APP"></span><span id="error_single_instance_app"></span>**Fehler bei \_ Einzel \_ Instanz- \_ App**
</dt> <dd> <dl> <dt>

1152 (0x480)
</dt> <dt>



Es kann nicht mehr als eine Instanz des angegebenen Programms gestartet werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_RMODE_APP"></span><span id="error_rmode_app"></span>**Fehler- \_ rmode- \_ App**
</dt> <dd> <dl> <dt>

1153 (0x481)
</dt> <dt>



Das angegebene Programm wurde für eine frühere Version von Windows geschrieben.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DLL"></span><span id="error_invalid_dll"></span>**Fehler \_ ungültige \_ dll.**
</dt> <dd> <dl> <dt>

1154 (0x482)
</dt> <dt>



Eine der Bibliotheksdateien, die zum Ausführen dieser Anwendung benötigt werden, ist beschädigt.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_ASSOCIATION"></span><span id="error_no_association"></span>**Fehler \_ ohne \_ Zuordnung**
</dt> <dd> <dl> <dt>

1155 (0x483)
</dt> <dt>



Der angegebenen Datei ist keine Anwendung für diesen Vorgang zugeordnet.


</dt> </dl> </dd> <dt>

<span id="ERROR_DDE_FAIL"></span><span id="error_dde_fail"></span>**Fehler \_ DDE \_ schlägt fehl**
</dt> <dd> <dl> <dt>

1156 (0x484)
</dt> <dt>



Fehler beim Senden des Befehls an die Anwendung.


</dt> </dl> </dd> <dt>

<span id="ERROR_DLL_NOT_FOUND"></span><span id="error_dll_not_found"></span>**Fehler- \_ dll wurde \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

1157 (0x485)
</dt> <dt>



Eine der Bibliotheksdateien, die zum Ausführen dieser Anwendung benötigt werden, wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MORE_USER_HANDLES"></span><span id="error_no_more_user_handles"></span>**Fehler \_ keine \_ weiteren \_ Benutzer \_ Handles**
</dt> <dd> <dl> <dt>

1158 (0x486)
</dt> <dt>



Der aktuelle Prozess hat das gesamte System Kontingent von Handles für Fenster-Manager-Objekte verwendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_MESSAGE_SYNC_ONLY"></span><span id="error_message_sync_only"></span>**\_nur Fehlermeldung \_ Synchronisieren \_**
</dt> <dd> <dl> <dt>

1159 (0x487)
</dt> <dt>



Die Nachricht kann nur mit synchronen Vorgängen verwendet werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_SOURCE_ELEMENT_EMPTY"></span><span id="error_source_element_empty"></span>**Fehler \_ Quell \_ Element \_ leer**
</dt> <dd> <dl> <dt>

1160 (0x488)
</dt> <dt>



Das festgestellte Quell Element weist kein Medium auf.


</dt> </dl> </dd> <dt>

<span id="ERROR_DESTINATION_ELEMENT_FULL"></span><span id="error_destination_element_full"></span>**Fehler \_ Ziel \_ Element \_ voll**
</dt> <dd> <dl> <dt>

1161 (0x489)
</dt> <dt>



Das angegeben Ziel Element enthält bereits Medien.


</dt> </dl> </dd> <dt>

<span id="ERROR_ILLEGAL_ELEMENT_ADDRESS"></span><span id="error_illegal_element_address"></span>**Fehler ungültige \_ \_ Element \_ Adresse**
</dt> <dd> <dl> <dt>

1162 (0x48a)
</dt> <dt>



Das angegeben Element ist nicht vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_MAGAZINE_NOT_PRESENT"></span><span id="error_magazine_not_present"></span>**das Fehler \_ Magazin ist \_ nicht \_ vorhanden.**
</dt> <dd> <dl> <dt>

1163 (0x48b)
</dt> <dt>



Das festgestellte Element ist Teil eines Magazins, das nicht vorhanden ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_REINITIALIZATION_NEEDED"></span><span id="error_device_reinitialization_needed"></span>**Fehler bei der \_ \_ erneuten Initialisierung des Geräts. \_**
</dt> <dd> <dl> <dt>

1164 (0x48c)
</dt> <dt>



Das für das Gerät erforderliche Gerät muss aufgrund von Hardwarefehlern erneut initialisiert werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_REQUIRES_CLEANING"></span><span id="error_device_requires_cleaning"></span>**Fehler \_ Gerät \_ erfordert \_ Bereinigen**
</dt> <dd> <dl> <dt>

1165 (0x48d)
</dt> <dt>



Das Gerät hat angegeben, dass eine Bereinigung erforderlich ist, bevor weitere Vorgänge versucht werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_DOOR_OPEN"></span><span id="error_device_door_open"></span>**Fehler \_ beim \_ Öffnen des Geräts. \_**
</dt> <dd> <dl> <dt>

1166 (0x48e)
</dt> <dt>



Das Gerät hat angegeben, dass seine Tür geöffnet ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_NOT_CONNECTED"></span><span id="error_device_not_connected"></span>**Fehler \_ Gerät \_ nicht \_ verbunden**
</dt> <dd> <dl> <dt>

1167 (0x48f)
</dt> <dt>



Das Gerät ist nicht verbunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_FOUND"></span><span id="error_not_found"></span>**Fehler \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

1168 (0x490)
</dt> <dt>



Element wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MATCH"></span><span id="error_no_match"></span>**Fehler \_ keine Entsprechung \_**
</dt> <dd> <dl> <dt>

1169 (0x491)
</dt> <dt>



Es gab keine Entsprechung für den angegebenen Schlüssel im Index.


</dt> </dl> </dd> <dt>

<span id="ERROR_SET_NOT_FOUND"></span><span id="error_set_not_found"></span>**Fehler \_ Satz \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

1170 (0x492)
</dt> <dt>



Der angegebene Eigenschaften Satz ist im Objekt nicht vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_POINT_NOT_FOUND"></span><span id="error_point_not_found"></span>**der Fehler \_ Punkt wurde \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

1171 (0x493)
</dt> <dt>



Der an getmoucmuvepoints über gegebene Punkt befindet sich nicht im Puffer.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_TRACKING_SERVICE"></span><span id="error_no_tracking_service"></span>**Fehler " \_ kein \_ Überwachungs \_ Dienst"**
</dt> <dd> <dl> <dt>

1172 (0x494)
</dt> <dt>



Der Überwachungsdienst (Arbeitsstations Dienst) wird nicht ausgeführt.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_VOLUME_ID"></span><span id="error_no_volume_id"></span>**Fehler " \_ keine \_ Volume- \_ ID"**
</dt> <dd> <dl> <dt>

1173 (0x495)
</dt> <dt>



Die Volume-ID wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_REMOVE_REPLACED"></span><span id="error_unable_to_remove_replaced"></span>**Fehler \_ beim \_ \_ Entfernen des \_ ersetzenden**
</dt> <dd> <dl> <dt>

1175 (0x497)
</dt> <dt>



Die zu ersetzende Datei kann nicht entfernt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_MOVE_REPLACEMENT"></span><span id="error_unable_to_move_replacement"></span>**Fehler \_ beim \_ \_ Verschieben der \_ Ersetzung.**
</dt> <dd> <dl> <dt>

1176 (0x498)
</dt> <dt>



Die Ersetzungs Datei kann nicht in die zu ersetzende Datei verschoben werden. Die zu ersetzende Datei hat den ursprünglichen Namen beibehalten.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_MOVE_REPLACEMENT_2"></span><span id="error_unable_to_move_replacement_2"></span>**Fehler \_ beim \_ \_ Verschieben von \_ Ersetzung \_ 2.**
</dt> <dd> <dl> <dt>

1177 (0x499)
</dt> <dt>



Die Ersetzungs Datei kann nicht in die zu ersetzende Datei verschoben werden. Die zu ersetzende Datei wurde mit dem Sicherungs Namen umbenannt.


</dt> </dl> </dd> <dt>

<span id="ERROR_JOURNAL_DELETE_IN_PROGRESS"></span><span id="error_journal_delete_in_progress"></span>**Fehler \_ Journal \_ wird \_ gelöscht \_**
</dt> <dd> <dl> <dt>

1178 (0x49a)
</dt> <dt>



Das Volume-Änderungs Journal wird gelöscht.


</dt> </dl> </dd> <dt>

<span id="ERROR_JOURNAL_NOT_ACTIVE"></span><span id="error_journal_not_active"></span>**das Fehler \_ Journal ist \_ nicht \_ aktiv.**
</dt> <dd> <dl> <dt>

1179 (0x49b)
</dt> <dt>



Das Volume-Änderungs Journal ist nicht aktiv.


</dt> </dl> </dd> <dt>

<span id="ERROR_POTENTIAL_FILE_FOUND"></span><span id="error_potential_file_found"></span>**Fehler \_ mögliche \_ Datei \_ gefunden.**
</dt> <dd> <dl> <dt>

1180 (0x49c)
</dt> <dt>



Eine Datei wurde gefunden, Sie ist jedoch möglicherweise nicht die richtige Datei.


</dt> </dl> </dd> <dt>

<span id="ERROR_JOURNAL_ENTRY_DELETED"></span><span id="error_journal_entry_deleted"></span>**Fehler \_ Journal \_ Eintrag \_ gelöscht**
</dt> <dd> <dl> <dt>

1181 (0x49d)
</dt> <dt>



Der Journal Eintrag wurde aus dem Journal gelöscht.


</dt> </dl> </dd> <dt>

<span id="ERROR_SHUTDOWN_IS_SCHEDULED"></span><span id="error_shutdown_is_scheduled"></span>**Fehler beim Herunterfahren des Fehlers. \_ \_ \_**
</dt> <dd> <dl> <dt>

1190 (0x4a6)
</dt> <dt>



Das Herunterfahren des Systems wurde bereits geplant.


</dt> </dl> </dd> <dt>

<span id="ERROR_SHUTDOWN_USERS_LOGGED_ON"></span><span id="error_shutdown_users_logged_on"></span>**Fehler \_ beim Herunterfahren \_ \_ der angemeldeten Benutzer \_ .**
</dt> <dd> <dl> <dt>

1191 (0x4a7)
</dt> <dt>



Das Herunterfahren des Systems kann nicht initiiert werden, da andere Benutzer auf dem Computer angemeldet sind.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_DEVICE"></span><span id="error_bad_device"></span>**fehlerhaftes \_ \_ Gerät**
</dt> <dd> <dl> <dt>

1200 (0x4b0)
</dt> <dt>



Der angegebene Gerätename ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONNECTION_UNAVAIL"></span><span id="error_connection_unavail"></span>**Fehler beim wieder \_ herstellen der Verbindung. \_**
</dt> <dd> <dl> <dt>

1201 (0x4b1)
</dt> <dt>



Das Gerät ist zurzeit nicht verbunden, aber es handelt sich um eine gespeicherte Verbindung.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_ALREADY_REMEMBERED"></span><span id="error_device_already_remembered"></span>**das Fehler \_ Gerät wurde \_ bereits \_ gespeichert.**
</dt> <dd> <dl> <dt>

1202 (0x4b2)
</dt> <dt>



Der Name des lokalen Geräts hat eine Verbindung mit einer anderen Netzwerkressource.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_NET_OR_BAD_PATH"></span><span id="error_no_net_or_bad_path"></span>**Fehler \_ beim \_ Netzwerk \_ oder ungültigen \_ \_ Pfad.**
</dt> <dd> <dl> <dt>

1203 (0x4b3)
</dt> <dt>



Der Netzwerkpfad wurde entweder falsch eingegeben, ist nicht vorhanden, oder der Netzwerkanbieter ist zurzeit nicht verfügbar. Versuchen Sie, den Pfad erneut einzugeben, oder wenden Sie sich an Ihren Netzwerkadministrator.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_PROVIDER"></span><span id="error_bad_provider"></span>**fehlerhafter \_ \_ Anbieter**
</dt> <dd> <dl> <dt>

1204 (0x4b4)
</dt> <dt>



Der angegebene Netzwerkanbieter Name ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_OPEN_PROFILE"></span><span id="error_cannot_open_profile"></span>**Fehler \_ beim \_ Öffnen des \_ Profils.**
</dt> <dd> <dl> <dt>

1205 (0x4b5)
</dt> <dt>



Das Netzwerk Verbindungsprofil kann nicht geöffnet werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_PROFILE"></span><span id="error_bad_profile"></span>**fehlerhaftes \_ \_ Profil**
</dt> <dd> <dl> <dt>

1206 (0x4b6)
</dt> <dt>



Das Netzwerk Verbindungsprofil ist beschädigt.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_CONTAINER"></span><span id="error_not_container"></span>**Fehler \_ nicht \_ Container**
</dt> <dd> <dl> <dt>

1207 (0x4b7)
</dt> <dt>



Ein nicht Container kann nicht aufgelistet werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_EXTENDED_ERROR"></span><span id="error_extended_error"></span>**Fehler beim \_ erweiterten \_ Fehler.**
</dt> <dd> <dl> <dt>

1208 (0x4b8)
</dt> <dt>



Ein erweiterter Fehler ist aufgetreten.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_GROUPNAME"></span><span id="error_invalid_groupname"></span>**Fehler \_ ungültiger \_ Gruppenname.**
</dt> <dd> <dl> <dt>

1209 (0x4b9)
</dt> <dt>



Das Format des angegebenen Gruppennamens ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_COMPUTERNAME"></span><span id="error_invalid_computername"></span>**Fehler \_ ungültiger \_ Computername.**
</dt> <dd> <dl> <dt>

1210 (0x4ba)
</dt> <dt>



Das Format des angegebenen Computer namens ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_EVENTNAME"></span><span id="error_invalid_eventname"></span>**Fehler bei \_ ungültigem \_ Ereignis Name.**
</dt> <dd> <dl> <dt>

1211 (0x4bb)
</dt> <dt>



Das Format des angegebenen Ereignis namens ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DOMAINNAME"></span><span id="error_invalid_domainname"></span>**\_ungültiger \_ Domänen Name.**
</dt> <dd> <dl> <dt>

1212 (0x4bc)
</dt> <dt>



Das Format des angegebenen Domänen Namens ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SERVICENAME"></span><span id="error_invalid_servicename"></span>**Fehler \_ ungültiger \_ Dienst Name.**
</dt> <dd> <dl> <dt>

1213 (0x4bd)
</dt> <dt>



Das Format des angegebenen Dienst namens ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_NETNAME"></span><span id="error_invalid_netname"></span>**Fehler \_ beim \_ NetName.**
</dt> <dd> <dl> <dt>

1214 (0x4be)
</dt> <dt>



Das Format des angegebenen Netzwerk namens ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SHARENAME"></span><span id="error_invalid_sharename"></span>**\_ungültiger \_ ShareName.**
</dt> <dd> <dl> <dt>

1215 (0x4bf)
</dt> <dt>



Das Format des angegebenen Freigabe namens ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PASSWORDNAME"></span><span id="error_invalid_passwordname"></span>**\_ungültiger \_ passwordname.**
</dt> <dd> <dl> <dt>

1216 (0x4c0)
</dt> <dt>



Das Format des angegebenen Kennworts ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MESSAGENAME"></span><span id="error_invalid_messagename"></span>**Fehler \_ ungültiger \_ MessageName.**
</dt> <dd> <dl> <dt>

1217 (0x4c1)
</dt> <dt>



Das Format des angegebenen Nachrichten namens ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MESSAGEDEST"></span><span id="error_invalid_messagedest"></span>**Fehler \_ ungültige \_ messagedest.**
</dt> <dd> <dl> <dt>

1218 (0x4c2)
</dt> <dt>



Das Format des angegebenen Nachrichten Ziels ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_SESSION_CREDENTIAL_CONFLICT"></span><span id="error_session_credential_conflict"></span>**Konflikt mit Anmelde Informationen für die Fehler \_ Sitzung \_ \_**
</dt> <dd> <dl> <dt>

1219 (0x4c3)
</dt> <dt>



Mehrere Verbindungen mit einem Server oder einer gemeinsam genutzten Ressource durch denselben Benutzer mit mehr als einem Benutzernamen sind nicht zulässig. Trennen Sie alle vorherigen Verbindungen mit dem Server oder der freigegebenen Ressource, und versuchen Sie es erneut.


</dt> </dl> </dd> <dt>

<span id="ERROR_REMOTE_SESSION_LIMIT_EXCEEDED"></span><span id="error_remote_session_limit_exceeded"></span>**Fehler bei \_ Remote \_ Sitzungs \_ Limit \_ überschritten.**
</dt> <dd> <dl> <dt>

1220 (0x4c4)
</dt> <dt>



Es wurde versucht, eine Sitzung mit einem Netzwerkserver einzurichten, aber es wurden bereits zu viele Sitzungen auf diesem Server eingerichtet.


</dt> </dl> </dd> <dt>

<span id="ERROR_DUP_DOMAINNAME"></span><span id="error_dup_domainname"></span>**Fehler \_ DUP \_ Domain Name**
</dt> <dd> <dl> <dt>

1221 (0x4c5)
</dt> <dt>



Der Arbeitsgruppen-oder Domänen Name wird bereits von einem anderen Computer im Netzwerk verwendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_NETWORK"></span><span id="error_no_network"></span>**Fehler " \_ kein \_ Netzwerk"**
</dt> <dd> <dl> <dt>

1222 (0x4c6)
</dt> <dt>



Das Netzwerk ist nicht vorhanden oder wurde nicht gestartet.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANCELLED"></span><span id="error_cancelled"></span>**Fehler \_ abgebrochen**
</dt> <dd> <dl> <dt>

1223 (0x4c7)
</dt> <dt>



Der Vorgang wurde vom Benutzer abgebrochen.


</dt> </dl> </dd> <dt>

<span id="ERROR_USER_MAPPED_FILE"></span><span id="error_user_mapped_file"></span>**Benutzer zugeordnete Datei mit Fehler \_ \_ \_**
</dt> <dd> <dl> <dt>

1224 (0x4c8)
</dt> <dt>



Der angeforderte Vorgang kann nicht für eine Datei ausgeführt werden, in der ein vom Benutzer zugeordneter Abschnitt geöffnet ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONNECTION_REFUSED"></span><span id="error_connection_refused"></span>**Fehler \_ Verbindung \_ verweigert**
</dt> <dd> <dl> <dt>

1225 (0x4c9)
</dt> <dt>



Der Remote Computer hat die Netzwerkverbindung verweigert.


</dt> </dl> </dd> <dt>

<span id="ERROR_GRACEFUL_DISCONNECT"></span><span id="error_graceful_disconnect"></span>**Fehler beim Trennen der Verbindung \_ \_**
</dt> <dd> <dl> <dt>

1226 (0x4ca)
</dt> <dt>



Die Netzwerkverbindung wurde ordnungsgemäß geschlossen.


</dt> </dl> </dd> <dt>

<span id="ERROR_ADDRESS_ALREADY_ASSOCIATED"></span><span id="error_address_already_associated"></span>**die Fehler \_ Adresse ist \_ bereits \_ zugeordnet.**
</dt> <dd> <dl> <dt>

1227 (0x4cb)
</dt> <dt>



Dem Netzwerk Transport Endpunkt ist bereits eine Adresse zugeordnet.


</dt> </dl> </dd> <dt>

<span id="ERROR_ADDRESS_NOT_ASSOCIATED"></span><span id="error_address_not_associated"></span>**Fehler \_ Adresse \_ nicht \_ zugeordnet**
</dt> <dd> <dl> <dt>

1228 (0x4cc)
</dt> <dt>



Dem Netzwerk Endpunkt wurde noch keine Adresse zugeordnet.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONNECTION_INVALID"></span><span id="error_connection_invalid"></span>**Fehler \_ Verbindung \_ ungültig**
</dt> <dd> <dl> <dt>

1229 (0x4cd)
</dt> <dt>



Es wurde versucht, einen Vorgang für eine nicht vorhandene Netzwerkverbindung auszuführen.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONNECTION_ACTIVE"></span><span id="error_connection_active"></span>**Fehler \_ Verbindung \_ aktiv**
</dt> <dd> <dl> <dt>

1230 (0x4ce)
</dt> <dt>



Es wurde versucht, einen ungültigen Vorgang für eine aktive Netzwerkverbindung auszuführen.


</dt> </dl> </dd> <dt>

<span id="ERROR_NETWORK_UNREACHABLE"></span><span id="error_network_unreachable"></span>**Fehler \_ Netzwerk \_ nicht erreichbar**
</dt> <dd> <dl> <dt>

1231 (0x4cf)
</dt> <dt>



Der Netzwerk Speicherort ist nicht erreichbar. Informationen zur Netzwerkproblem Behandlung finden Sie in der Windows-Hilfe.


</dt> </dl> </dd> <dt>

<span id="ERROR_HOST_UNREACHABLE"></span><span id="error_host_unreachable"></span>**Fehler \_ Host ist \_ nicht erreichbar.**
</dt> <dd> <dl> <dt>

1232 (0x4d0)
</dt> <dt>



Der Netzwerk Speicherort ist nicht erreichbar. Informationen zur Netzwerkproblem Behandlung finden Sie in der Windows-Hilfe.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROTOCOL_UNREACHABLE"></span><span id="error_protocol_unreachable"></span>**das Fehler \_ Protokoll ist \_ nicht erreichbar.**
</dt> <dd> <dl> <dt>

1233 (0x4d1)
</dt> <dt>



Der Netzwerk Speicherort ist nicht erreichbar. Informationen zur Netzwerkproblem Behandlung finden Sie in der Windows-Hilfe.


</dt> </dl> </dd> <dt>

<span id="ERROR_PORT_UNREACHABLE"></span><span id="error_port_unreachable"></span>**der \_ fehlerport ist \_ nicht erreichbar.**
</dt> <dd> <dl> <dt>

1234 (0x4d2)
</dt> <dt>



Am Zielnetzwerk Endpunkt auf dem Remote System ist kein Dienst Betriebssystem.


</dt> </dl> </dd> <dt>

<span id="ERROR_REQUEST_ABORTED"></span><span id="error_request_aborted"></span>**Fehler \_ Anforderung \_ abgebrochen**
</dt> <dd> <dl> <dt>

1235 (0x4d3)
</dt> <dt>



Die Anforderung wurde abgebrochen.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONNECTION_ABORTED"></span><span id="error_connection_aborted"></span>**Fehler \_ Verbindung \_ abgebrochen**
</dt> <dd> <dl> <dt>

1236 (0x4d4)
</dt> <dt>



Die Netzwerkverbindung wurde vom lokalen System abgebrochen.


</dt> </dl> </dd> <dt>

<span id="ERROR_RETRY"></span><span id="error_retry"></span>**Fehler beim \_ Wiederholungsversuch.**
</dt> <dd> <dl> <dt>

1237 (0x4d5)
</dt> <dt>



Der Vorgang konnte nicht abgeschlossen werden. Es sollte eine Wiederholung ausgeführt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONNECTION_COUNT_LIMIT"></span><span id="error_connection_count_limit"></span>**Limit für die \_ Anzahl von Verbindungsfehlern \_ \_**
</dt> <dd> <dl> <dt>

1238 (0x4d6)
</dt> <dt>



Es konnte keine Verbindung mit dem Server hergestellt werden, da der Grenzwert für die Anzahl der gleichzeitigen Verbindungen für dieses Konto erreicht wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOGIN_TIME_RESTRICTION"></span><span id="error_login_time_restriction"></span>**Einschränkung der Fehler \_ Anmelde \_ Zeit \_**
</dt> <dd> <dl> <dt>

1239 (0x4d7)
</dt> <dt>



Es wird versucht, sich während einer nicht autorisierten Tageszeit für dieses Konto anzumelden.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOGIN_WKSTA_RESTRICTION"></span><span id="error_login_wksta_restriction"></span>**Fehler beim \_ Anmelden mit \_ wksta- \_ Einschränkung**
</dt> <dd> <dl> <dt>

1240 (0x4d8)
</dt> <dt>



Das Konto ist nicht autorisiert, sich von dieser Station aus anzumelden.


</dt> </dl> </dd> <dt>

<span id="ERROR_INCORRECT_ADDRESS"></span><span id="error_incorrect_address"></span>**Fehler \_ hafte \_ Adresse**
</dt> <dd> <dl> <dt>

1241 (0x4d9)
</dt> <dt>



Die Netzwerkadresse konnte nicht für den angeforderten Vorgang verwendet werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALREADY_REGISTERED"></span><span id="error_already_registered"></span>**Fehler \_ bereits \_ registriert**
</dt> <dd> <dl> <dt>

1242 (0x4da)
</dt> <dt>



Der Dienst ist bereits registriert.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_NOT_FOUND"></span><span id="error_service_not_found"></span>**Fehler \_ Dienst \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

1243 (0x4db)
</dt> <dt>



Der angegebene Dienst ist nicht vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_AUTHENTICATED"></span><span id="error_not_authenticated"></span>**Fehler \_ nicht \_ authentifiziert**
</dt> <dd> <dl> <dt>

1244 (0x4dc)
</dt> <dt>



Der angeforderte Vorgang wurde nicht ausgeführt, da der Benutzer nicht authentifiziert wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_LOGGED_ON"></span><span id="error_not_logged_on"></span>**Fehler \_ nicht \_ angemeldet \_ .**
</dt> <dd> <dl> <dt>

1245 (0x4dd)
</dt> <dt>



Der angeforderte Vorgang wurde nicht ausgeführt, da sich der Benutzer nicht am Netzwerk angemeldet hat. Der angegebene Dienst ist nicht vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONTINUE"></span><span id="error_continue"></span>**Fehler beim \_ fortsetzen**
</dt> <dd> <dl> <dt>

1246 (0x4de)
</dt> <dt>



Fahren Sie mit der aktuell ausgeführten Arbeit fort.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALREADY_INITIALIZED"></span><span id="error_already_initialized"></span>**Fehler \_ bereits \_ Initialisiert**
</dt> <dd> <dl> <dt>

1247 (0x4df)
</dt> <dt>



Es wurde versucht, eine Initialisierungs Operation auszuführen, wenn die Initialisierung bereits abgeschlossen wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MORE_DEVICES"></span><span id="error_no_more_devices"></span>**Fehler \_ keine \_ weiteren \_ Geräte**
</dt> <dd> <dl> <dt>

1248 (0x4e0)
</dt> <dt>



Keine weiteren lokalen Geräte.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUCH_SITE"></span><span id="error_no_such_site"></span>**Fehler " \_ kein \_ solcher \_ Standort"**
</dt> <dd> <dl> <dt>

1249 (0x4e1)
</dt> <dt>



Die angegebene Site ist nicht vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DOMAIN_CONTROLLER_EXISTS"></span><span id="error_domain_controller_exists"></span>**Fehler \_ Domänen \_ Controller \_ vorhanden**
</dt> <dd> <dl> <dt>

1250 (0x4e2)
</dt> <dt>



Ein Domänen Controller mit dem angegebenen Namen ist bereits vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_ONLY_IF_CONNECTED"></span><span id="error_only_if_connected"></span>**nur Fehler, \_ \_ Wenn eine \_ Verbindung besteht**
</dt> <dd> <dl> <dt>

1251 (0x4e3)
</dt> <dt>



Dieser Vorgang wird nur unterstützt, wenn Sie mit dem Server verbunden sind.


</dt> </dl> </dd> <dt>

<span id="ERROR_OVERRIDE_NOCHANGES"></span><span id="error_override_nochanges"></span>**Fehler beim über \_ Schreiben von \_ noChanges**
</dt> <dd> <dl> <dt>

1252 (0x4e4)
</dt> <dt>



Das Gruppenrichtlinien Framework sollte die Erweiterung auch dann anrufen, wenn keine Änderungen vorhanden sind.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_USER_PROFILE"></span><span id="error_bad_user_profile"></span>**Fehler \_ beim \_ Benutzer \_ Profil.**
</dt> <dd> <dl> <dt>

1253 (0x4e5)
</dt> <dt>



Der angegebene Benutzer verfügt über kein gültiges Profil.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SUPPORTED_ON_SBS"></span><span id="error_not_supported_on_sbs"></span>**\_der Fehler \_ wird \_ für \_ SSB nicht unterstützt.**
</dt> <dd> <dl> <dt>

1254 (0x4e6)
</dt> <dt>



Dieser Vorgang wird auf Computern, auf denen Windows Server 2003 für Small Business Server ausgeführt wird, nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVER_SHUTDOWN_IN_PROGRESS"></span><span id="error_server_shutdown_in_progress"></span>**Fehler \_ Server wird \_ heruntergefahren \_ . \_**
</dt> <dd> <dl> <dt>

1255 (0x4e7)
</dt> <dt>



Der Server Computer wird heruntergefahren.


</dt> </dl> </dd> <dt>

<span id="ERROR_HOST_DOWN"></span><span id="error_host_down"></span>**Fehler \_ Host \_**
</dt> <dd> <dl> <dt>

1256 (0x4e8)
</dt> <dt>



Das Remote System ist nicht verfügbar. Informationen zur Netzwerkproblem Behandlung finden Sie in der Windows-Hilfe.


</dt> </dl> </dd> <dt>

<span id="ERROR_NON_ACCOUNT_SID"></span><span id="error_non_account_sid"></span>**\_nicht- \_ Konto- \_ SID des Fehlers**
</dt> <dd> <dl> <dt>

1257 (0x4e9)
</dt> <dt>



Die angegebene Sicherheits-ID wird nicht von einer Konto Domäne abgeleitet.


</dt> </dl> </dd> <dt>

<span id="ERROR_NON_DOMAIN_SID"></span><span id="error_non_domain_sid"></span>**Fehler \_ nicht- \_ Domänen- \_ sid**
</dt> <dd> <dl> <dt>

1258 (0x4ea)
</dt> <dt>



Die angegebene Sicherheits-ID verfügt über keine Domänen Komponente.


</dt> </dl> </dd> <dt>

<span id="ERROR_APPHELP_BLOCK"></span><span id="error_apphelp_block"></span>**Fehler " \_ AppHelp"- \_ Block**
</dt> <dd> <dl> <dt>

1259 (0x4eb)
</dt> <dt>



Das AppHelp-Dialogfeld wurde abgebrochen und verhindert somit das Starten der Anwendung.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCESS_DISABLED_BY_POLICY"></span><span id="error_access_disabled_by_policy"></span>**Fehler \_ Zugriff \_ \_ durch \_ Richtlinie deaktiviert**
</dt> <dd> <dl> <dt>

1260 (0x4ec)
</dt> <dt>



Dieses Programm wird durch die Gruppenrichtlinie blockiert. Wenden Sie sich an Ihren Systemadministrator, um weitere Informationen zu erhalten.


</dt> </dl> </dd> <dt>

<span id="ERROR_REG_NAT_CONSUMPTION"></span><span id="error_reg_nat_consumption"></span>**Fehler \_ beim \_ NAT- \_ Verbrauch.**
</dt> <dd> <dl> <dt>

1261 (0x4ed)
</dt> <dt>



Ein Programm hat versucht, einen ungültigen Registerwert zu verwenden. Wird normalerweise durch ein nicht initialisiertes Register verursacht. Dieser Fehler ist Itanium-spezifisch.


</dt> </dl> </dd> <dt>

<span id="ERROR_CSCSHARE_OFFLINE"></span><span id="error_cscshare_offline"></span>**Fehler " \_ cscshare" \_ Offline**
</dt> <dd> <dl> <dt>

1262 (0x4ee)
</dt> <dt>



Die Freigabe ist zurzeit offline oder nicht vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_PKINIT_FAILURE"></span><span id="error_pkinit_failure"></span>**\_PKINIT- \_ Fehler**
</dt> <dd> <dl> <dt>

1263 (0x4ef)
</dt> <dt>



Im Kerberos-Protokoll ist ein Fehler aufgetreten, während das KDC-Zertifikat bei der Smartcard-Anmeldung überprüft wird. Weitere Informationen finden Sie im System Ereignisprotokoll.


</dt> </dl> </dd> <dt>

<span id="ERROR_SMARTCARD_SUBSYSTEM_FAILURE"></span><span id="error_smartcard_subsystem_failure"></span>**Fehler beim \_ Smartcard- \_ Subsystem. \_**
</dt> <dd> <dl> <dt>

1264 (0x4F 0)
</dt> <dt>



Im Kerberos-Protokoll ist ein Fehler beim Versuch aufgetreten, das Smartcard-Subsystem zu verwenden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DOWNGRADE_DETECTED"></span><span id="error_downgrade_detected"></span>**\_fehlerdowngrade \_ erkannt**
</dt> <dd> <dl> <dt>

1265 (0x4F 1)
</dt> <dt>



Das System kann keine Verbindung mit einem Domänen Controller aufnehmen, um die Authentifizierungsanforderung zu bedienen. Versuchen Sie es später noch mal.


</dt> </dl> </dd> <dt>

<span id="ERROR_MACHINE_LOCKED"></span><span id="error_machine_locked"></span>**Fehler \_ Computer \_ gesperrt**
</dt> <dd> <dl> <dt>

1271 (0x4F)
</dt> <dt>



Der Computer ist gesperrt und kann nicht ohne die Option "Force" heruntergefahren werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CALLBACK_SUPPLIED_INVALID_DATA"></span><span id="error_callback_supplied_invalid_data"></span>**Fehler \_ Rückruf \_ hat \_ ungültige \_ Daten angegeben.**
</dt> <dd> <dl> <dt>

1273 (0x4F 9)
</dt> <dt>



Ein von der Anwendung definierter Rückruf hat beim Aufruf ungültige Daten angegeben.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYNC_FOREGROUND_REFRESH_REQUIRED"></span><span id="error_sync_foreground_refresh_required"></span>**Fehler \_ Synchronisierungs- \_ Vordergrund \_ Aktualisierung \_ erforderlich**
</dt> <dd> <dl> <dt>

1274 (0x4fa)
</dt> <dt>



Das Gruppenrichtlinien Framework sollte die Erweiterung bei der synchronen Aktualisierung der Vordergrund Richtlinie aufruft.


</dt> </dl> </dd> <dt>

<span id="ERROR_DRIVER_BLOCKED"></span><span id="error_driver_blocked"></span>**Fehler \_ Treiber \_ blockiert**
</dt> <dd> <dl> <dt>

1275 (0x4fb)
</dt> <dt>



Das Laden dieses Treibers wurde blockiert.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_IMPORT_OF_NON_DLL"></span><span id="error_invalid_import_of_non_dll"></span>**Fehler \_ beim \_ importieren \_ der \_ nicht- \_ dll.**
</dt> <dd> <dl> <dt>

1276 (0x4fc)
</dt> <dt>



In einer Dynamic Link Library (dll) wurde auf ein Modul verwiesen, das weder eine DLL noch das ausführbare Image des Prozesses war.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCESS_DISABLED_WEBBLADE"></span><span id="error_access_disabled_webblade"></span>**\_WebBlade für Fehler Zugriff \_ deaktiviert \_**
</dt> <dd> <dl> <dt>

1277 (0x4fd)
</dt> <dt>



Dieses Programm kann nicht geöffnet werden, da es deaktiviert wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCESS_DISABLED_WEBBLADE_TAMPER"></span><span id="error_access_disabled_webblade_tamper"></span>**Fehler \_ beim \_ Deaktivieren des \_ WebBlade- \_ Manipulations Diensts**
</dt> <dd> <dl> <dt>

1278 (0x4fe)
</dt> <dt>



Dieses Programm kann nicht geöffnet werden, da das Lizenz Erzwingungs System manipuliert oder beschädigt wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_RECOVERY_FAILURE"></span><span id="error_recovery_failure"></span>**Fehler beim Wiederherstellen. \_ \_**
</dt> <dd> <dl> <dt>

1279 (0x4ff)
</dt> <dt>



Fehler beim Wiederherstellen einer Transaktion.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALREADY_FIBER"></span><span id="error_already_fiber"></span>**Fehler \_ bereits \_ Fiber**
</dt> <dd> <dl> <dt>

1280 (0x500)
</dt> <dt>



Der aktuelle Thread wurde bereits in eine Fiber konvertiert.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALREADY_THREAD"></span><span id="error_already_thread"></span>**Fehler \_ bereits \_ Thread**
</dt> <dd> <dl> <dt>

1281 (0x501)
</dt> <dt>



Der aktuelle Thread wurde bereits aus einer Fiber konvertiert.


</dt> </dl> </dd> <dt>

<span id="ERROR_STACK_BUFFER_OVERRUN"></span><span id="error_stack_buffer_overrun"></span>**Fehler \_ Stapel- \_ Puffer \_ Überlauf**
</dt> <dd> <dl> <dt>

1282 (0x502)
</dt> <dt>



Das System hat einen Überlauf eines Stapel basierten Puffers in dieser Anwendung erkannt. Mit diesem Überlauf kann ein böswilliger Benutzer möglicherweise die Kontrolle über diese Anwendung erlangen.


</dt> </dl> </dd> <dt>

<span id="ERROR_PARAMETER_QUOTA_EXCEEDED"></span><span id="error_parameter_quota_exceeded"></span>**Fehler \_ Parameter \_ Kontingent \_ überschritten**
</dt> <dd> <dl> <dt>

1283 (0x503)
</dt> <dt>



Daten, die in einem der Parameter vorhanden sind, sind größer als die Funktion, die verwendet werden kann.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEBUGGER_INACTIVE"></span><span id="error_debugger_inactive"></span>**Fehler \_ Debugger \_ inaktiv**
</dt> <dd> <dl> <dt>

1284 (0x504)
</dt> <dt>



Der Versuch, einen Vorgang für ein Debug-Objekt durchzuführen, ist fehlgeschlagen, da das Objekt gerade gelöscht wird.


</dt> </dl> </dd> <dt>

<span id="ERROR_DELAY_LOAD_FAILED"></span><span id="error_delay_load_failed"></span>**Fehler beim Laden der Fehler \_ Verzögerung \_ \_**
</dt> <dd> <dl> <dt>

1285 (0x505)
</dt> <dt>



Fehler beim Versuch, eine DLL oder eine Funktions Adresse in einer verzögert geladenen DLL zu laden.


</dt> </dl> </dd> <dt>

<span id="ERROR_VDM_DISALLOWED"></span><span id="error_vdm_disallowed"></span>**VDM-Fehler ist unzulässig. \_ \_**
</dt> <dd> <dl> <dt>

1286 (0x506)
</dt> <dt>



%1 ist eine 16-Bit-Anwendung. Sie verfügen nicht über die Berechtigungen zum Ausführen von 16-Bit-Anwendungen. Überprüfen Sie Ihre Berechtigungen mit dem Systemadministrator.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNIDENTIFIED_ERROR"></span><span id="error_unidentified_error"></span>**\_unbekannter \_ Fehler.**
</dt> <dd> <dl> <dt>

1287 (0x507)
</dt> <dt>



Es sind nicht genügend Informationen vorhanden, um die Fehlerursache zu ermitteln.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_CRUNTIME_PARAMETER"></span><span id="error_invalid_cruntime_parameter"></span>**Fehler \_ ungültiger \_ cruntime- \_ Parameter**
</dt> <dd> <dl> <dt>

1288 (0x508)
</dt> <dt>



Der an eine C-Lauf Zeitfunktion übergebenen Parameter ist falsch.


</dt> </dl> </dd> <dt>

<span id="ERROR_BEYOND_VDL"></span><span id="error_beyond_vdl"></span>**Fehler \_ über \_ VDL hinaus**
</dt> <dd> <dl> <dt>

1289 (0x509)
</dt> <dt>



Der Vorgang ist über die gültige Daten Länge der Datei hinaus aufgetreten.


</dt> </dl> </dd> <dt>

<span id="ERROR_INCOMPATIBLE_SERVICE_SID_TYPE"></span><span id="error_incompatible_service_sid_type"></span>**nicht \_ kompatibler \_ Dienst- \_ sid- \_ Typ**
</dt> <dd> <dl> <dt>

1290 (0x50A)
</dt> <dt>



Fehler beim Starten des Diensts, da mindestens ein Dienst im selben Prozess über eine nicht kompatible Dienst-SID-Typ-Einstellung verfügt. Ein Dienst mit dem SID-Typ "eingeschränkter Dienst" kann nur im gleichen Prozess mit anderen Diensten mit eingeschränktem SID-Typ vorhanden sein. Wenn der Dienst-SID-Typ für diesen Dienst soeben konfiguriert wurde, muss der Hostingprozess neu gestartet werden, um diesen Dienst zu starten.

Unter Windows Server 2003 und Windows XP kann ein uneingeschränkter Dienst nicht in demselben Prozess wie andere Dienste nebeneinander vorhanden sein. Der Dienst mit dem SID-Typ "uneingeschränkter Dienst" muss in einen eigenen Prozess verschoben werden, um diesen Dienst zu starten.


</dt> </dl> </dd> <dt>

<span id="ERROR_DRIVER_PROCESS_TERMINATED"></span><span id="error_driver_process_terminated"></span>**Fehler \_ Treiber \_ Prozess \_ beendet**
</dt> <dd> <dl> <dt>

1291 (0x50B)
</dt> <dt>



Der Prozess, der den Treiber für dieses Gerät gehostet, wurde beendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_IMPLEMENTATION_LIMIT"></span><span id="error_implementation_limit"></span>**Fehler \_ Implementierungs \_ Limit**
</dt> <dd> <dl> <dt>

1292 (0x50C)
</dt> <dt>



Ein Vorgang hat versucht, einen von der Implementierung definierten Grenzwert zu überschreiten.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROCESS_IS_PROTECTED"></span><span id="error_process_is_protected"></span>**der Fehler \_ Prozess \_ ist \_ geschützt.**
</dt> <dd> <dl> <dt>

1293 (0x50D)
</dt> <dt>



Entweder der Ziel Prozess oder der enthaltende Prozess des Zielthreads ist ein geschützter Prozess.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_NOTIFY_CLIENT_LAGGING"></span><span id="error_service_notify_client_lagging"></span>**Fehler \_ Dienst hat den \_ \_ Client \_ Rückstand benachrichtigt**
</dt> <dd> <dl> <dt>

1294 (0x50E)
</dt> <dt>



Der Dienst Benachrichtigungs Client geht zu weit hinter dem aktuellen Status der Dienste auf dem Computer.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_QUOTA_EXCEEDED"></span><span id="error_disk_quota_exceeded"></span>**Fehler Datenträger \_ \_ Kontingent \_ überschritten**
</dt> <dd> <dl> <dt>

1295 (0x50F)
</dt> <dt>



Fehler beim angeforderten Datei Vorgang, weil das Speicher Kontingent überschritten wurde. Verschieben Sie Dateien an einen anderen Speicherort, oder löschen Sie unnötige Dateien, um Speicherplatz freizugeben. Wenden Sie sich an Ihren Systemadministrator, um weitere Informationen zu erhalten.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONTENT_BLOCKED"></span><span id="error_content_blocked"></span>**Fehler \_ Inhalt \_ blockiert**
</dt> <dd> <dl> <dt>

1296 (0x510)
</dt> <dt>



Der angeforderte Datei Vorgang ist fehlgeschlagen, da die Speicher Richtlinie diese Art von Datei blockiert. Wenden Sie sich an Ihren Systemadministrator, um weitere Informationen zu erhalten.


</dt> </dl> </dd> <dt>

<span id="ERROR_INCOMPATIBLE_SERVICE_PRIVILEGE"></span><span id="error_incompatible_service_privilege"></span>**Fehler bei \_ inkompatibler \_ Dienst \_ Berechtigung**
</dt> <dd> <dl> <dt>

1297 (0x511)
</dt> <dt>



Eine Berechtigung, die der Dienst benötigt, um ordnungsgemäß zu funktionieren, ist in der Dienst Konto Konfiguration nicht vorhanden. Sie können das Microsoft Management Console (MMC)-Snap-in (Services. msc) und das lokale Sicherheitseinstellungen MMC-Snap-in (secpol. msc) verwenden, um die Dienst Konfiguration und die Konto Konfiguration anzuzeigen.


</dt> </dl> </dd> <dt>

<span id="ERROR_APP_HANG"></span><span id="error_app_hang"></span>**Fehler-App-Absturz \_ \_**
</dt> <dd> <dl> <dt>

1298 (0x512)
</dt> <dt>



Ein Thread, der an diesem Vorgang beteiligt ist, reagiert anscheinend nicht.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LABEL"></span><span id="error_invalid_label"></span>**\_ungültige \_ Bezeichnung.**
</dt> <dd> <dl> <dt>

1299 (0x513)
</dt> <dt>



Gibt an, dass eine bestimmte Sicherheits-ID nicht als Bezeichnung eines Objekts zugewiesen werden kann.


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

 

 




