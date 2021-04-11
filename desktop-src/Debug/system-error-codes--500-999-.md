---
description: Beschreibt die in der Header Datei "Winerror. h" definierten Fehlercodes 500-999 und ist für Entwickler bestimmt.
ms.assetid: 8d8b427b-b761-4023-a834-a6eff96d6ba1
title: System Fehler Codes (500-999) (Winerror. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 02b35374fcb68f9b416948d5e39b2182f573b60f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214225"
---
# <a name="system-error-codes-500-999"></a>System Fehler Codes (500-999)

> [!NOTE]
> Diese Informationen sind für Entwickler gedacht, die Systemfehler Debuggen. Bei anderen Fehlern, wie z. b. Problemen mit Windows Update, finden Sie eine Liste der Ressourcen auf der Seite [Fehlercodes](system-error-codes.md) .

In der folgenden Liste werden die [Systemfehler Codes](system-error-codes.md) (Fehler 500 bis 999) beschrieben. Sie werden von der [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) -Funktion zurückgegeben, wenn viele Funktionen fehlschlagen. Um den Beschreibungstext für den Fehler in Ihrer Anwendung abzurufen, verwenden Sie die [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) -Funktion mit dem Flag " **Format \_ Message \_ from \_ System** ".

<dl> <dt>

<span id="ERROR_USER_PROFILE_LOAD"></span><span id="error_user_profile_load"></span>**Fehler beim \_ Laden des Benutzer \_ Profils. \_**
</dt> <dd> <dl> <dt>

500 (0x1F)
</dt> <dt>



Das Benutzerprofil kann nicht geladen werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_ARITHMETIC_OVERFLOW"></span><span id="error_arithmetic_overflow"></span>**Fehler \_ arithmetischer \_ Überlauf**
</dt> <dd> <dl> <dt>

534 (0x216)
</dt> <dt>



Arithmetisches Ergebnis hat 32 Bits überschritten.


</dt> </dl> </dd> <dt>

<span id="ERROR_PIPE_CONNECTED"></span><span id="error_pipe_connected"></span>**Fehler \_ Pipeline \_ verbunden**
</dt> <dd> <dl> <dt>

535 (0x217)
</dt> <dt>



Es gibt einen Prozess an einem anderen Ende der Pipe.


</dt> </dl> </dd> <dt>

<span id="ERROR_PIPE_LISTENING"></span><span id="error_pipe_listening"></span>**fehlerpipe-Überwachung \_ \_**
</dt> <dd> <dl> <dt>

536 (0x218)
</dt> <dt>



Warten, bis ein Prozess das andere Ende der Pipe öffnet.


</dt> </dl> </dd> <dt>

<span id="ERROR_VERIFIER_STOP"></span><span id="error_verifier_stop"></span>**Fehler \_ Überprüfung \_**
</dt> <dd> <dl> <dt>

537 (0x219)
</dt> <dt>



Der Anwendungs Verifier hat einen Fehler im aktuellen Prozess festgestellt.


</dt> </dl> </dd> <dt>

<span id="ERROR_ABIOS_ERROR"></span><span id="error_abios_error"></span>**Fehler \_ bei der Fehlermeldung. \_**
</dt> <dd> <dl> <dt>

538 (0x21a)
</dt> <dt>



Im ABIOS-Subsystem ist ein Fehler aufgetreten.


</dt> </dl> </dd> <dt>

<span id="ERROR_WX86_WARNING"></span><span id="error_wx86_warning"></span>**Fehler \_ WX86 \_ Warnung**
</dt> <dd> <dl> <dt>

539 (0x21b)
</dt> <dt>



Im WX86-Subsystem ist eine Warnung aufgetreten.


</dt> </dl> </dd> <dt>

<span id="ERROR_WX86_ERROR"></span><span id="error_wx86_error"></span>**Fehler \_ WX86 \_ Fehler**
</dt> <dd> <dl> <dt>

540 (0x21c)
</dt> <dt>



Fehler im WX86-Subsystem.


</dt> </dl> </dd> <dt>

<span id="ERROR_TIMER_NOT_CANCELED"></span><span id="error_timer_not_canceled"></span>**Fehler Zeit Geber \_ \_ nicht \_ abgebrochen**
</dt> <dd> <dl> <dt>

541 (0x21d)
</dt> <dt>



Es wurde versucht, einen Timer abzubrechen oder festzulegen, dem ein APC zugeordnet ist, und der Subjekt Thread ist nicht der Thread, der den Timer ursprünglich mit einer zugeordneten APC-Routine festgelegt hat.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNWIND"></span><span id="error_unwind"></span>**Fehler \_ beim Entladen**
</dt> <dd> <dl> <dt>

542 (0x21e)
</dt> <dt>



Entladen Sie den Ausnahme Code.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_STACK"></span><span id="error_bad_stack"></span>**fehlerhafter \_ \_ Stapelfehler**
</dt> <dd> <dl> <dt>

543 (0x21f)
</dt> <dt>



Während eines Entladevorgangs wurde ein ungültiger oder nicht ausgerichteter Stapel gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_UNWIND_TARGET"></span><span id="error_invalid_unwind_target"></span>**Fehler beim Entladen des \_ \_ \_ Ziels.**
</dt> <dd> <dl> <dt>

544 (0x220)
</dt> <dt>



Während eines Entladevorgangs wurde ein ungültiges Entlade Ziel gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PORT_ATTRIBUTES"></span><span id="error_invalid_port_attributes"></span>**\_ungültige \_ Port \_ Attribute.**
</dt> <dd> <dl> <dt>

545 (0x221)
</dt> <dt>



Ungültige Objekt Attribute für ntkreateport angegeben, oder für NtConnectPort wurden ungültige Port Attribute angegeben.


</dt> </dl> </dd> <dt>

<span id="ERROR_PORT_MESSAGE_TOO_LONG"></span><span id="error_port_message_too_long"></span>**\_fehlerport \_ Meldung \_ zu \_ lang**
</dt> <dd> <dl> <dt>

546 (0x222)
</dt> <dt>



Die Länge der an ntrequestport oder ntrequestwaitreplyport übergebenen Nachricht ist länger als die vom Port zulässige maximale Nachricht.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_QUOTA_LOWER"></span><span id="error_invalid_quota_lower"></span>**Fehler \_ ungültiges \_ Kontingent \_ niedriger.**
</dt> <dd> <dl> <dt>

547 (0x223)
</dt> <dt>



Es wurde versucht, eine Kontingent Grenze unterhalb der aktuellen Nutzung zu verringern.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_ALREADY_ATTACHED"></span><span id="error_device_already_attached"></span>**Fehler \_ Gerät \_ bereits \_ angefügt**
</dt> <dd> <dl> <dt>

548 (0x224)
</dt> <dt>



Es wurde versucht, eine Verbindung mit einem Gerät anzufügen, das bereits an ein anderes Gerät angefügt wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTRUCTION_MISALIGNMENT"></span><span id="error_instruction_misalignment"></span>**\_ \_ Fehlausrichtung der Fehler Anweisung**
</dt> <dd> <dl> <dt>

549 (0x225)
</dt> <dt>



Es wurde versucht, eine Anweisung an einer nicht ausgerichteten Adresse auszuführen, und das Host System unterstützt keine nicht ausgerichteten Anweisungs Verweise.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROFILING_NOT_STARTED"></span><span id="error_profiling_not_started"></span>**Fehler \_ Profilerstellung \_ nicht \_ gestartet**
</dt> <dd> <dl> <dt>

550 (0x226)
</dt> <dt>



Die Profilerstellung wurde nicht gestartet.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROFILING_NOT_STOPPED"></span><span id="error_profiling_not_stopped"></span>**Fehler \_ Profilerstellung \_ nicht \_ beendet**
</dt> <dd> <dl> <dt>

551 (0x227)
</dt> <dt>



Die Profilerstellung wurde nicht beendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_COULD_NOT_INTERPRET"></span><span id="error_could_not_interpret"></span>**Fehler \_ beim \_ \_ interpretieren**
</dt> <dd> <dl> <dt>

552 (0x228)
</dt> <dt>



Die bestandene ACL enthielt nicht die erforderlichen Mindestinformationen.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROFILING_AT_LIMIT"></span><span id="error_profiling_at_limit"></span>**Fehler \_ Profilerstellung \_ bei \_ Limit**
</dt> <dd> <dl> <dt>

553 (0x229)
</dt> <dt>



Die Anzahl aktiver Profil Erstellungs Objekte hat den Höchstwert, und es können keine weiteren Objekte gestartet werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_WAIT"></span><span id="error_cant_wait"></span>**Fehler \_ beim \_ warten.**
</dt> <dd> <dl> <dt>

554 (0x22a)
</dt> <dt>



Wird verwendet, um anzugeben, dass ein Vorgang ohne Blockierung für e/a nicht fortgesetzt werden kann.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_TERMINATE_SELF"></span><span id="error_cant_terminate_self"></span>**Fehler \_ beim \_ Beenden von \_ Self.**
</dt> <dd> <dl> <dt>

555 (0x22b)
</dt> <dt>



Gibt an, dass ein Thread standardmäßig versucht hat, sich selbst zu beenden (mit dem Namen NtTerminateThread mit **null**) und dem letzten Thread im aktuellen Prozess.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNEXPECTED_MM_CREATE_ERR"></span><span id="error_unexpected_mm_create_err"></span>**Fehler \_ unerwartetes mm-Fehler beim \_ \_ Erstellen \_**
</dt> <dd> <dl> <dt>

556 (0x22c)
</dt> <dt>



Wenn ein mm-Fehler zurückgegeben wird, der nicht im standardmäßigen FsRtl-Filter definiert ist, wird er in einen der folgenden Fehler konvertiert, der im Filter garantiert ist. In diesem Fall gehen die Informationen verloren, der Filter behandelt die Ausnahme jedoch ordnungsgemäß.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNEXPECTED_MM_MAP_ERROR"></span><span id="error_unexpected_mm_map_error"></span>**\_unerwarteter Fehler bei \_ mm- \_ Zuordnung. \_**
</dt> <dd> <dl> <dt>

557 (0x22d)
</dt> <dt>



Wenn ein mm-Fehler zurückgegeben wird, der nicht im standardmäßigen FsRtl-Filter definiert ist, wird er in einen der folgenden Fehler konvertiert, der im Filter garantiert ist. In diesem Fall gehen die Informationen verloren, der Filter behandelt die Ausnahme jedoch ordnungsgemäß.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNEXPECTED_MM_EXTEND_ERR"></span><span id="error_unexpected_mm_extend_err"></span>**Fehler \_ unerwartetes \_ mm- \_ Erweitern von \_ Err**
</dt> <dd> <dl> <dt>

558 (0x22e)
</dt> <dt>



Wenn ein mm-Fehler zurückgegeben wird, der nicht im standardmäßigen FsRtl-Filter definiert ist, wird er in einen der folgenden Fehler konvertiert, der im Filter garantiert ist. In diesem Fall gehen die Informationen verloren, der Filter behandelt die Ausnahme jedoch ordnungsgemäß.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_FUNCTION_TABLE"></span><span id="error_bad_function_table"></span>**Fehler \_ hafte \_ Funktions \_ Tabelle**
</dt> <dd> <dl> <dt>

559 (0x22f)
</dt> <dt>



Bei einem Entladevorgang wurde eine falsch formatierte Funktions Tabelle gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_GUID_TRANSLATION"></span><span id="error_no_guid_translation"></span>**Fehler \_ keine \_ GUID- \_ Übersetzung**
</dt> <dd> <dl> <dt>

560 (0x230)
</dt> <dt>



Gibt an, dass versucht wurde, eine Datei oder ein Verzeichnis des Dateisystems zu schützen. eine der SIDs in der Sicherheits Beschreibung konnte nicht in eine GUID übersetzt werden, die vom Dateisystem gespeichert werden konnte. Dies bewirkt, dass der Schutz Versuch fehlschlägt, was dazu führen kann, dass bei der Dateierstellung ein Fehler auftritt.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LDT_SIZE"></span><span id="error_invalid_ldt_size"></span>**Fehler \_ ungültige \_ LDT- \_ Größe**
</dt> <dd> <dl> <dt>

561 (0x231)
</dt> <dt>



Gibt an, dass versucht wurde, einen LDT zu vergrößern, indem er seine Größe festgelegt hat, oder dass die Größe keine gerade Anzahl von Selektoren war.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LDT_OFFSET"></span><span id="error_invalid_ldt_offset"></span>**Fehler \_ beim \_ LDT- \_ Offset.**
</dt> <dd> <dl> <dt>

563 (0x233)
</dt> <dt>



Gibt an, dass der Startwert für die LDT-Informationen kein ganzzahliges Vielfaches der Auswahl Größe war.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LDT_DESCRIPTOR"></span><span id="error_invalid_ldt_descriptor"></span>**Fehler \_ ungültiger \_ LDT- \_ Deskriptor.**
</dt> <dd> <dl> <dt>

564 (0x234)
</dt> <dt>



Gibt an, dass der Benutzer beim Einrichten von LDT-Deskriptoren einen ungültigen Deskriptor bereitgestellt hat.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_THREADS"></span><span id="error_too_many_threads"></span>**Fehler \_ zu \_ viele \_ Threads.**
</dt> <dd> <dl> <dt>

565 (0x235)
</dt> <dt>



Gibt an, dass ein Prozess zu viele Threads enthält, um die angeforderte Aktion auszuführen. Beispielsweise kann die Zuweisung eines primären Tokens nur ausgeführt werden, wenn ein Prozess über keinen oder einen Thread verfügt.


</dt> </dl> </dd> <dt>

<span id="ERROR_THREAD_NOT_IN_PROCESS"></span><span id="error_thread_not_in_process"></span>**Fehler \_ Thread \_ nicht \_ in \_ Verarbeitung**
</dt> <dd> <dl> <dt>

566 (0x236)
</dt> <dt>



Es wurde versucht, einen Thread in einem bestimmten Prozess auszuführen, aber der angegebene Thread befindet sich nicht im angegebenen Prozess.


</dt> </dl> </dd> <dt>

<span id="ERROR_PAGEFILE_QUOTA_EXCEEDED"></span><span id="error_pagefile_quota_exceeded"></span>**Fehler beim Seiten \_ Datei \_ Kontingent \_ überschritten.**
</dt> <dd> <dl> <dt>

567 (0x237)
</dt> <dt>



Das Seiten Datei Kontingent wurde überschritten.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOGON_SERVER_CONFLICT"></span><span id="error_logon_server_conflict"></span>**Fehler beim \_ Anmelden des \_ Servers. \_**
</dt> <dd> <dl> <dt>

568 (0x238)
</dt> <dt>



Der Netlogon-Dienst kann nicht gestartet werden, da ein anderer in der Domäne laufender Anmeldedienst mit der angegebenen Rolle in Konflikt steht.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYNCHRONIZATION_REQUIRED"></span><span id="error_synchronization_required"></span>**Fehler \_ Synchronisierung \_ erforderlich**
</dt> <dd> <dl> <dt>

569 (0x239)
</dt> <dt>



Die SAM-Datenbank auf einem Windows-Server ist deutlich nicht mit der Kopie auf dem Domänen Controller synchronisiert. Eine komplette Synchronisierung ist erforderlich.


</dt> </dl> </dd> <dt>

<span id="ERROR_NET_OPEN_FAILED"></span><span id="error_net_open_failed"></span>**Fehler \_ beim \_ Öffnen von NET Open \_**
</dt> <dd> <dl> <dt>

570 (0x23a)
</dt> <dt>



Fehler bei der ntkreatefile-API. Dieser Fehler sollte niemals an eine Anwendung zurückgegeben werden. er ist ein Platzhalter, den der Windows-LAN-Manager-Redirector in seinen internen Fehler zuordnungsroutinen verwenden kann.


</dt> </dl> </dd> <dt>

<span id="ERROR_IO_PRIVILEGE_FAILED"></span><span id="error_io_privilege_failed"></span>**Fehler bei \_ IO- \_ Berechtigung \_**
</dt> <dd> <dl> <dt>

571 (0x23b)
</dt> <dt>



{Berechtigungs Fehler} Die e/a-Berechtigungen für den Prozess konnten nicht geändert werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONTROL_C_EXIT"></span><span id="error_control_c_exit"></span>**Fehler \_ Steuerung \_ C \_ Beenden**
</dt> <dd> <dl> <dt>

572 (0x23c)
</dt> <dt>



{Beenden der Anwendung durch STRG + C} Die Anwendung wurde als Ergebnis von STRG + C beendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_MISSING_SYSTEMFILE"></span><span id="error_missing_systemfile"></span>**Fehler \_ bei \_ Systemdatei.**
</dt> <dd> <dl> <dt>

573 (0x23d)
</dt> <dt>



{System Datei fehlt} Die erforderliche Systemdatei "% hs" ist nicht vorhanden oder fehlt.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNHANDLED_EXCEPTION"></span><span id="error_unhandled_exception"></span>**\_nicht behandelte \_ Ausnahme Fehler.**
</dt> <dd> <dl> <dt>

574 (0x23e)
</dt> <dt>



{Anwendungsfehler} Die Ausnahme '% s ' (0x% 08lx) ist in der Anwendung an Speicherort 0x% 08lX aufgetreten.


</dt> </dl> </dd> <dt>

<span id="ERROR_APP_INIT_FAILURE"></span><span id="error_app_init_failure"></span>**Fehler- \_ App- \_ Init \_ -Fehler**
</dt> <dd> <dl> <dt>

575 (0x23f)
</dt> <dt>



{Anwendungsfehler} Die Anwendung konnte nicht ordnungsgemäß gestartet werden (0x% LX). Klicken Sie auf OK, um die Anwendung zu schließen.


</dt> </dl> </dd> <dt>

<span id="ERROR_PAGEFILE_CREATE_FAILED"></span><span id="error_pagefile_create_failed"></span>**Fehler beim Erstellen der Fehler \_ Datei. \_ \_**
</dt> <dd> <dl> <dt>

576 (0x240)
</dt> <dt>



{Paging-Datei konnte nicht erstellt werden.} Fehler beim Erstellen der Auslagerungs Datei "% hs" (% LX). Die angeforderte Größe war% LD.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_IMAGE_HASH"></span><span id="error_invalid_image_hash"></span>**\_ungültiger \_ \_ bildhash.**
</dt> <dd> <dl> <dt>

577 (0x241)
</dt> <dt>



Die digitale Signatur für diese Datei kann nicht überprüft werden. Bei einer aktuellen Hardware-oder Software Änderung wurde möglicherweise eine beschädigte oder beschädigte Datei oder Schadsoftware aus einer unbekannten Quelle installiert.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_PAGEFILE"></span><span id="error_no_pagefile"></span>**Fehler " \_ keine \_ Pagefile"**
</dt> <dd> <dl> <dt>

578 (0x242)
</dt> <dt>



{Keine Auslagerungs Datei angegeben} In der Systemkonfiguration wurde keine Auslagerungs Datei angegeben.


</dt> </dl> </dd> <dt>

<span id="ERROR_ILLEGAL_FLOAT_CONTEXT"></span><span id="error_illegal_float_context"></span>**Ungültiger \_ \_ float- \_ Kontext.**
</dt> <dd> <dl> <dt>

579 (0x243)
</dt> <dt>



Distanzieren Eine Anwendung im realen Modus hat eine Gleit Komma Anweisung ausgegeben, und es ist keine Gleit Komma Hardware vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_EVENT_PAIR"></span><span id="error_no_event_pair"></span>**Fehler " \_ kein \_ Ereignis \_ Paar"**
</dt> <dd> <dl> <dt>

580 (0x244)
</dt> <dt>



Ein Ereignispaar-Synchronisierungs Vorgang wurde mithilfe des Thread spezifischen Client/Server-Ereignispaar Objekts durchgeführt, aber es wurde kein Ereignispaar Objekt mit dem Thread verknüpft.


</dt> </dl> </dd> <dt>

<span id="ERROR_DOMAIN_CTRLR_CONFIG_ERROR"></span><span id="error_domain_ctrlr_config_error"></span>**Fehler \_ Domäne \_ ctrlr- \_ Konfigurations \_ Fehler**
</dt> <dd> <dl> <dt>

581 (0x245)
</dt> <dt>



Ein Windows-Server weist eine falsche Konfiguration auf.


</dt> </dl> </dd> <dt>

<span id="ERROR_ILLEGAL_CHARACTER"></span><span id="error_illegal_character"></span>**Ungültiges \_ \_ Zeichen.**
</dt> <dd> <dl> <dt>

582 (0x246)
</dt> <dt>



Ein ungültiges Zeichen wurde gefunden. Bei einem Multibyte-Zeichensatz enthält dies ein führendes Byte ohne nachfolgende nachfolgende Byte. Für den Unicode-Zeichensatz enthält dies die Zeichen 0xFFFF und 0xFFFE.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNDEFINED_CHARACTER"></span><span id="error_undefined_character"></span>**Fehler nicht \_ definiertes \_ Zeichen**
</dt> <dd> <dl> <dt>

583 (0x247)
</dt> <dt>



Das Unicode-Zeichen ist nicht im Unicode-Zeichensatz definiert, der auf dem System installiert ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_FLOPPY_VOLUME"></span><span id="error_floppy_volume"></span>**Fehler \_ Disketten \_ Volume**
</dt> <dd> <dl> <dt>

584 (0x248)
</dt> <dt>



Die Auslagerungs Datei kann nicht auf einer Disketten Diskette erstellt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_BIOS_FAILED_TO_CONNECT_INTERRUPT"></span><span id="error_bios_failed_to_connect_interrupt"></span>**Fehler-BIOS-Fehler beim \_ \_ \_ \_ Verbinden von \_ Interrupt**
</dt> <dd> <dl> <dt>

585 (0x249)
</dt> <dt>



Das System-BIOS konnte einen System Interrupt nicht mit dem Gerät oder dem Bus verbinden, für das das Gerät angeschlossen ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_BACKUP_CONTROLLER"></span><span id="error_backup_controller"></span>**Fehler \_ Sicherungs \_ Controller**
</dt> <dd> <dl> <dt>

586 (0x24a)
</dt> <dt>



Dieser Vorgang ist nur für den primären Domänen Controller der Domäne zulässig.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUTANT_LIMIT_EXCEEDED"></span><span id="error_mutant_limit_exceeded"></span>**Fehler \_ Mutant \_ Limit \_ überschritten**
</dt> <dd> <dl> <dt>

587 (0x24b)
</dt> <dt>



Es wurde versucht, eine muant so zu erhalten, dass die maximale Anzahl überschritten wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_FS_DRIVER_REQUIRED"></span><span id="error_fs_driver_required"></span>**Fehler- \_ FS- \_ Treiber \_ erforderlich**
</dt> <dd> <dl> <dt>

588 (0x24c)
</dt> <dt>



Es wurde auf ein Volume zugegriffen, für das ein Dateisystem Treiber erforderlich ist, der noch nicht geladen wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_LOAD_REGISTRY_FILE"></span><span id="error_cannot_load_registry_file"></span>**Fehler \_ beim \_ Laden der \_ Registrierungs \_ Datei.**
</dt> <dd> <dl> <dt>

589 (0x24d)
</dt> <dt>



{Fehler bei der Registrierungsdatei} Die Registrierung kann die Hive (Datei) nicht laden:% HS oder Ihr Protokoll oder eine Alternative. Er ist beschädigt, fehlt oder ist nicht beschreibbar.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEBUG_ATTACH_FAILED"></span><span id="error_debug_attach_failed"></span>**Fehler beim \_ Debuggen des Fehlers \_ \_**
</dt> <dd> <dl> <dt>

590 (0x24e)
</dt> <dt>



{Unerwarteter Fehler in [**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess)} Unerwarteter Fehler beim Verarbeiten einer **DebugActiveProcess** -API-Anforderung. Sie können OK auswählen, um den Prozess zu beenden, oder Abbrechen, um den Fehler zu ignorieren.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYSTEM_PROCESS_TERMINATED"></span><span id="error_system_process_terminated"></span>**Fehler \_ System \_ Prozess wurde \_ beendet.**
</dt> <dd> <dl> <dt>

591 (0x24f)
</dt> <dt>



{Schwerwiegender System Fehler} Der% HS-System Prozess wurde unerwartet mit dem Status 0x% 08x (0x% 08x 0x% 08x) beendet. Das System wurde heruntergefahren.


</dt> </dl> </dd> <dt>

<span id="ERROR_DATA_NOT_ACCEPTED"></span><span id="error_data_not_accepted"></span>**Fehler \_ Daten wurden \_ nicht \_ akzeptiert.**
</dt> <dd> <dl> <dt>

592 (0x250)
</dt> <dt>



{Daten nicht akzeptiert} Der TDI-Client konnte die während einer Angabe empfangenen Daten nicht verarbeiten.


</dt> </dl> </dd> <dt>

<span id="ERROR_VDM_HARD_ERROR"></span><span id="error_vdm_hard_error"></span>**VDM-Fehler mit \_ \_ hartem \_ Fehler**
</dt> <dd> <dl> <dt>

593 (0x251)
</dt> <dt>



Fehler bei ntvdm.


</dt> </dl> </dd> <dt>

<span id="ERROR_DRIVER_CANCEL_TIMEOUT"></span><span id="error_driver_cancel_timeout"></span>**Timeout beim Abbrechen des Fehler \_ Treibers \_ \_**
</dt> <dd> <dl> <dt>

594 (0x252)
</dt> <dt>



{Abbruch Timeout} Der Treiber% HS konnte eine abgebrochene e/a-Anforderung in der vorgesehenen Zeit nicht beenden.


</dt> </dl> </dd> <dt>

<span id="ERROR_REPLY_MESSAGE_MISMATCH"></span><span id="error_reply_message_mismatch"></span>**Fehler beim Antworten auf die Fehler \_ \_ Meldung. \_**
</dt> <dd> <dl> <dt>

595 (0x253)
</dt> <dt>



{Antwort Nachrichten stimmen nicht überein. Es wurde versucht, auf eine LPC-Nachricht zu antworten, aber der Thread, der von der Client-ID in der Nachricht angegeben wurde, hat nicht auf diese Nachricht gewartet.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOST_WRITEBEHIND_DATA"></span><span id="error_lost_writebehind_data"></span>**Fehler \_ beim \_ Zurückschreiben von \_ Daten.**
</dt> <dd> <dl> <dt>

596 (0x254)
</dt> <dt>



{Verzögertes Schreiben fehlgeschlagen} Es konnten nicht alle Daten für die Datei "% hs" gespeichert werden. Die Daten sind verloren gegangen. Dieser Fehler kann durch einen Ausfall der Computer Hardware oder Netzwerkverbindung verursacht werden. Versuchen Sie, diese Datei an anderer Stelle zu speichern.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLIENT_SERVER_PARAMETERS_INVALID"></span><span id="error_client_server_parameters_invalid"></span>**Fehler bei \_ Client \_ Server \_ Parametern \_ ungültig**
</dt> <dd> <dl> <dt>

597 (0x255)
</dt> <dt>



Die Parameter, die im Fenster "Shared Memory" für Client/Server an den Server übergeben wurden, waren ungültig. Möglicherweise wurden zu viele Daten im freigegebenen Speicherfenster abgelegt.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_TINY_STREAM"></span><span id="error_not_tiny_stream"></span>**Fehler ist \_ kein \_ kleiner Daten \_ Strom.**
</dt> <dd> <dl> <dt>

598 (0x256)
</dt> <dt>



Der Stream ist kein kleiner Datenstrom.


</dt> </dl> </dd> <dt>

<span id="ERROR_STACK_OVERFLOW_READ"></span><span id="error_stack_overflow_read"></span>**Fehler \_ Stapel \_ Überlauf \_ Lesevorgang**
</dt> <dd> <dl> <dt>

599 (0x257)
</dt> <dt>



Die Anforderung muss vom Stapelüberlauf Code verarbeitet werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONVERT_TO_LARGE"></span><span id="error_convert_to_large"></span>**Fehler \_ \_ in " \_ groß" konvertieren**
</dt> <dd> <dl> <dt>

600 (0x258)
</dt> <dt>



Interne OFS-Statuscodes, die angeben, wie eine Zuordnungs Operation verarbeitet wird. Der Vorgang wird wiederholt, nachdem der enthaltende onode verschoben oder der Blockdaten Strom in einen großen Stream konvertiert wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_FOUND_OUT_OF_SCOPE"></span><span id="error_found_out_of_scope"></span>**Fehler \_ im Gültigkeits \_ \_ \_ Bereich gefunden**
</dt> <dd> <dl> <dt>

601 (0x259)
</dt> <dt>



Beim Versuch, das Objekt zu finden, wurde ein Objekt gefunden, das anhand der ID auf dem Volume übereinstimmt, aber es liegt außerhalb des Gültigkeits Bereichs des für den Vorgang verwendeten Handles.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALLOCATE_BUCKET"></span><span id="error_allocate_bucket"></span>**Fehler beim \_ Zuordnen von \_ Bucket**
</dt> <dd> <dl> <dt>

602 (0x25a)
</dt> <dt>



Das Bucket-Array muss vergrößert werden. Wiederholen Sie die Transaktion.


</dt> </dl> </dd> <dt>

<span id="ERROR_MARSHALL_OVERFLOW"></span><span id="error_marshall_overflow"></span>**Fehler \_ Mars Hall \_ Überlauf**
</dt> <dd> <dl> <dt>

603 (0x25b)
</dt> <dt>



Überlauf des Benutzer-/kernelmarshalling-Puffers.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_VARIANT"></span><span id="error_invalid_variant"></span>**Fehler \_ ungültige \_ Variante**
</dt> <dd> <dl> <dt>

604 (0x25c)
</dt> <dt>



Die bereitgestellte VARIANT-Struktur enthält ungültige Daten.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_COMPRESSION_BUFFER"></span><span id="error_bad_compression_buffer"></span>**Fehler \_ beim \_ Komprimierungs \_ Puffer.**
</dt> <dd> <dl> <dt>

605 (0x25d)
</dt> <dt>



Der angegebene Puffer enthält falsch formatierte Daten.


</dt> </dl> </dd> <dt>

<span id="ERROR_AUDIT_FAILED"></span><span id="error_audit_failed"></span>**Fehler bei der Überwachung. \_ \_**
</dt> <dd> <dl> <dt>

606 (0x25e)
</dt> <dt>



{Audit failed} Fehler beim Versuch, eine Sicherheitsüberwachung zu generieren.


</dt> </dl> </dd> <dt>

<span id="ERROR_TIMER_RESOLUTION_NOT_SET"></span><span id="error_timer_resolution_not_set"></span>**Fehler- \_ Timer- \_ Auflösung \_ nicht \_ festgelegt**
</dt> <dd> <dl> <dt>

607 (0x25f)
</dt> <dt>



Die Zeit Geber Auflösung wurde zuvor nicht durch den aktuellen Prozess festgelegt.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSUFFICIENT_LOGON_INFO"></span><span id="error_insufficient_logon_info"></span>**Fehler aufgrund \_ unzureichender \_ Anmelde \_ Informationen**
</dt> <dd> <dl> <dt>

608 (0x260)
</dt> <dt>



Es sind nicht genügend Kontoinformationen zum Anmelden vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_DLL_ENTRYPOINT"></span><span id="error_bad_dll_entrypoint"></span>**Fehler \_ beim \_ dll- \_ Einstiegspunkt.**
</dt> <dd> <dl> <dt>

609 (0x261)
</dt> <dt>



{Ungültige DLL-Einstiegspunkt} Die Dynamic Link Library% HS wurde nicht ordnungsgemäß geschrieben. Der Stapelzeiger wurde in einem inkonsistenten Zustand belassen. Der EntryPoint sollte als WINAPI oder stdcalldeklariert werden. Wählen Sie ja aus, um die dll-Auslastung zu deaktivieren Wählen Sie Nein, um die Ausführung fortzusetzen. Wenn Sie Nein auswählen, funktioniert die Anwendung möglicherweise nicht ordnungsgemäß.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_SERVICE_ENTRYPOINT"></span><span id="error_bad_service_entrypoint"></span>**fehlerhafter \_ \_ Dienst \_ Einstiegspunkt**
</dt> <dd> <dl> <dt>

610 (0x262)
</dt> <dt>



{Ungültiger Dienst Rückruf Einstiegspunkt} Der Dienst "% hs" wurde nicht ordnungsgemäß geschrieben. Der Stapelzeiger wurde in einem inkonsistenten Zustand belassen. Der Callback-EntryPoint sollte als WINAPI oder stdcalldeklariert werden. Wenn Sie OK auswählen, wird der Dienst fortgesetzt. Der Dienst Prozess funktioniert jedoch möglicherweise nicht ordnungsgemäß.


</dt> </dl> </dd> <dt>

<span id="ERROR_IP_ADDRESS_CONFLICT1"></span><span id="error_ip_address_conflict1"></span>**Fehler \_ -IP- \_ Adresse \_ CONFLICT1**
</dt> <dd> <dl> <dt>

611 (0x263)
</dt> <dt>



Es gibt einen IP-Adress Konflikt mit einem anderen System im Netzwerk.


</dt> </dl> </dd> <dt>

<span id="ERROR_IP_ADDRESS_CONFLICT2"></span><span id="error_ip_address_conflict2"></span>**Fehler \_ -IP- \_ Adresse \_ CONFLICT2**
</dt> <dd> <dl> <dt>

612 (0x264)
</dt> <dt>



Es gibt einen IP-Adress Konflikt mit einem anderen System im Netzwerk.


</dt> </dl> </dd> <dt>

<span id="ERROR_REGISTRY_QUOTA_LIMIT"></span><span id="error_registry_quota_limit"></span>**\_ \_ Kontingent \_ Limit für Fehler Registrierung**
</dt> <dd> <dl> <dt>

613 (0x265)
</dt> <dt>



{Wenig Registrierungsbereich} Das System hat die maximal zulässige Größe für den System Teil der Registrierung erreicht. Zusätzliche Speicheranforderungen werden ignoriert.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_CALLBACK_ACTIVE"></span><span id="error_no_callback_active"></span>**Fehler " \_ kein \_ Rückruf \_ aktiv"**
</dt> <dd> <dl> <dt>

614 (0x266)
</dt> <dt>



Ein Rückruf Rückgabesystem Dienst kann nicht ausgeführt werden, wenn kein Rückruf aktiv ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_PWD_TOO_SHORT"></span><span id="error_pwd_too_short"></span>**Fehler \_ pwd \_ zu \_ kurz**
</dt> <dd> <dl> <dt>

615 (0x267)
</dt> <dt>



Das angegebene Kennwort ist zu kurz, um die Richtlinie Ihres Benutzerkontos zu erfüllen. Wählen Sie ein längeres Kennwort aus.


</dt> </dl> </dd> <dt>

<span id="ERROR_PWD_TOO_RECENT"></span><span id="error_pwd_too_recent"></span>**Fehler \_ pwd \_ zu \_ aktuell**
</dt> <dd> <dl> <dt>

616 (0x268)
</dt> <dt>



Die Richtlinie Ihres Benutzerkontos ermöglicht nicht das Ändern von Kenn Wörtern zu häufig. Dies geschieht, um zu verhindern, dass Benutzer zu einem vertrauten, aber potenziell ermittelten Kennwort zurück wechseln. Wenn Ihr Kennwort kompromittiert wurde, wenden Sie sich umgehend an Ihren Administrator, um ein neues Kennwort zuzuweisen.


</dt> </dl> </dd> <dt>

<span id="ERROR_PWD_HISTORY_CONFLICT"></span><span id="error_pwd_history_conflict"></span>**Fehler \_ pwd-Verlaufs \_ \_ Konflikt**
</dt> <dd> <dl> <dt>

617 (0x269)
</dt> <dt>



Sie haben versucht, Ihr Kennwort in ein solches Kennwort zu ändern, das Sie in der Vergangenheit verwendet haben. Die Richtlinie Ihres Benutzerkontos lässt dies nicht zu. Wählen Sie ein Kennwort aus, das Sie zuvor nicht verwendet haben.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNSUPPORTED_COMPRESSION"></span><span id="error_unsupported_compression"></span>**\_nicht unterstützte \_ Komprimierung.**
</dt> <dd> <dl> <dt>

618 (0x26a)
</dt> <dt>



Das angegebene Komprimierungs Format wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_HW_PROFILE"></span><span id="error_invalid_hw_profile"></span>**Fehler \_ ungültiges \_ HW- \_ Profil**
</dt> <dd> <dl> <dt>

619 (0x26b)
</dt> <dt>



Die angegebene Hardwareprofil Konfiguration ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PLUGPLAY_DEVICE_PATH"></span><span id="error_invalid_plugplay_device_path"></span>**Fehler \_ ungültiger \_ plugplay- \_ Geräte \_ Pfad**
</dt> <dd> <dl> <dt>

620 (0x26c)
</dt> <dt>



Der angegebene Plug & Play Registrierungs Gerätepfad ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_QUOTA_LIST_INCONSISTENT"></span><span id="error_quota_list_inconsistent"></span>**Fehler \_ Kontingent \_ Liste \_ inkonsistent**
</dt> <dd> <dl> <dt>

621 (0x26d)
</dt> <dt>



Die angegebene Kontingent Liste ist intern inkonsistent mit dem Deskriptor.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVALUATION_EXPIRATION"></span><span id="error_evaluation_expiration"></span>**Ablauf der Fehler \_ Auswertung \_**
</dt> <dd> <dl> <dt>

622 (0x26e)
</dt> <dt>



{Windows-Evaluierungs Benachrichtigung} Der Evaluierungszeitraum für diese Installation von Windows ist abgelaufen. Dieses System wird innerhalb einer Stunde heruntergefahren. Um den Zugriff auf diese Installation von Windows wiederherzustellen, aktualisieren Sie diese Installation mithilfe einer lizenzierten Distribution dieses Produkts.


</dt> </dl> </dd> <dt>

<span id="ERROR_ILLEGAL_DLL_RELOCATION"></span><span id="error_illegal_dll_relocation"></span>**Fehler bei ungültiger \_ \_ dll- \_ Verlagerung**
</dt> <dd> <dl> <dt>

623 (0x26f)
</dt> <dt>



{Illegale System-DLL-Verschiebung} Die System-dll "% hs" wurde im Arbeitsspeicher verschoben. Die Anwendung wird nicht ordnungsgemäß ausgeführt. Die Verschiebung ist aufgetreten, da die dll "% hs" einen für Windows-System-DLLs reservierten Adressbereich belegt hat. Der Hersteller, der die dll bereitstellt, sollte für eine neue dll kontaktiert werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DLL_INIT_FAILED_LOGOFF"></span><span id="error_dll_init_failed_logoff"></span>**Fehler-dll-Fehler beim Abmelden \_ \_ \_ \_**
</dt> <dd> <dl> <dt>

624 (0x270)
</dt> <dt>



{DLL-Initialisierung ist fehlgeschlagen. Die Anwendung konnte nicht initialisiert werden, da die Fenster Station heruntergefahren wird.


</dt> </dl> </dd> <dt>

<span id="ERROR_VALIDATE_CONTINUE"></span><span id="error_validate_continue"></span>**Fehler \_ beim \_ fortfahren**
</dt> <dd> <dl> <dt>

625 (0x271)
</dt> <dt>



Der Überprüfungs Vorgang muss mit dem nächsten Schritt fortgesetzt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MORE_MATCHES"></span><span id="error_no_more_matches"></span>**Fehler \_ keine \_ weiteren \_ Übereinstimmungen**
</dt> <dd> <dl> <dt>

626 (0x272)
</dt> <dt>



Es sind keine weiteren Übereinstimmungen für die aktuelle indexenumeration vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_RANGE_LIST_CONFLICT"></span><span id="error_range_list_conflict"></span>**Fehler \_ Bereich- \_ Listen \_ Konflikt**
</dt> <dd> <dl> <dt>

627 (0x273)
</dt> <dt>



Der Bereich konnte aufgrund eines Konflikts nicht zur Bereichs Liste hinzugefügt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVER_SID_MISMATCH"></span><span id="error_server_sid_mismatch"></span>**Fehler \_ Server- \_ sid \_ stimmt nicht überein.**
</dt> <dd> <dl> <dt>

628 (0x274)
</dt> <dt>



Der Server Prozess wird unter einer anderen sid ausgeführt als die für den Client erforderliche sid.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_ENABLE_DENY_ONLY"></span><span id="error_cant_enable_deny_only"></span>**Fehler \_ " \_ \_ nur verweigern" aktivieren \_**
</dt> <dd> <dl> <dt>

629 (0x275)
</dt> <dt>



Eine Gruppe, die nur für Deny gekennzeichnet ist, kann nicht aktiviert werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_FLOAT_MULTIPLE_FAULTS"></span><span id="error_float_multiple_faults"></span>**Fehler beim \_ float von \_ mehreren \_ Fehlern**
</dt> <dd> <dl> <dt>

630 (0x276)
</dt> <dt>



Distanzieren Mehrere Gleit Komma Fehler.


</dt> </dl> </dd> <dt>

<span id="ERROR_FLOAT_MULTIPLE_TRAPS"></span><span id="error_float_multiple_traps"></span>**Fehler beim \_ float \_ mehrerer \_ Traps**
</dt> <dd> <dl> <dt>

631 (0x277)
</dt> <dt>



Distanzieren Mehrere Gleit Komma Traps.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOINTERFACE"></span><span id="error_nointerface"></span>**Fehler- \_ nointerface**
</dt> <dd> <dl> <dt>

632 (0x278)
</dt> <dt>



Die angeforderte Schnittstelle wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_DRIVER_FAILED_SLEEP"></span><span id="error_driver_failed_sleep"></span>**Fehler Treiber Fehler beim Standbymodus \_ \_ \_**
</dt> <dd> <dl> <dt>

633 (0x279)
</dt> <dt>



{System Standby-Fehler Der% HS-Treiber unterstützt den Standbymodus nicht. Durch Aktualisieren dieses Treibers kann das System in den Standbymodus wechseln.


</dt> </dl> </dd> <dt>

<span id="ERROR_CORRUPT_SYSTEM_FILE"></span><span id="error_corrupt_system_file"></span>**Fehler beim \_ beschädigen der \_ System \_ Datei.**
</dt> <dd> <dl> <dt>

634 (0x27a)
</dt> <dt>



Die Systemdatei "%1" ist beschädigt und wurde ersetzt.


</dt> </dl> </dd> <dt>

<span id="ERROR_COMMITMENT_MINIMUM"></span><span id="error_commitment_minimum"></span>**\_mindestens fehlerverpflichtung \_**
</dt> <dd> <dl> <dt>

635 (0x27b)
</dt> <dt>



{Minimaler virtueller Arbeitsspeicher zu niedrig} Das System verfügt über wenig virtuellen Arbeitsspeicher. Die Größe der Auslagerungs Datei des virtuellen Speichers wird von Windows vergrößert. Während dieses Vorgangs werden Arbeitsspeicher Anforderungen für einige Anwendungen möglicherweise verweigert. Weitere Informationen finden Sie in der Hilfe.


</dt> </dl> </dd> <dt>

<span id="ERROR_PNP_RESTART_ENUMERATION"></span><span id="error_pnp_restart_enumeration"></span>**Fehler \_ pnp- \_ Neustart- \_ Enumeration**
</dt> <dd> <dl> <dt>

636 (0x27c)
</dt> <dt>



Ein Gerät wurde entfernt, sodass die Enumeration neu gestartet werden muss.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYSTEM_IMAGE_BAD_SIGNATURE"></span><span id="error_system_image_bad_signature"></span>**Fehler bei der Signatur des \_ System \_ Images. \_ \_**
</dt> <dd> <dl> <dt>

637 (0x27d)
</dt> <dt>



{Schwerwiegender System Fehler} Das System Image "% s" ist nicht ordnungsgemäß signiert. Die Datei wurde durch die signierte Datei ersetzt. Das System wurde heruntergefahren.


</dt> </dl> </dd> <dt>

<span id="ERROR_PNP_REBOOT_REQUIRED"></span><span id="error_pnp_reboot_required"></span>**Fehler \_ pnp- \_ Neustart \_ erforderlich**
</dt> <dd> <dl> <dt>

638 (0x27e)
</dt> <dt>



Das Gerät wird ohne Neustart nicht gestartet.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSUFFICIENT_POWER"></span><span id="error_insufficient_power"></span>**Fehler bei \_ unzureichender \_ Stromversorgung**
</dt> <dd> <dl> <dt>

639 (0x27f)
</dt> <dt>



Es ist nicht genügend Strom vorhanden, um den angeforderten Vorgang abzuschließen.


</dt> </dl> </dd> <dt>

<span id="ERROR_MULTIPLE_FAULT_VIOLATION"></span><span id="error_multiple_fault_violation"></span>**Fehler bei \_ mehrerer Fehler \_ \_ Verletzung**
</dt> <dd> <dl> <dt>

640 (0x280)
</dt> <dt>



Fehler bei \_ mehrerer Fehler \_ \_ Verletzung


</dt> </dl> </dd> <dt>

<span id="ERROR_SYSTEM_SHUTDOWN"></span><span id="error_system_shutdown"></span>**Fehler \_ System \_ Herunterfahren**
</dt> <dd> <dl> <dt>

641 (0x281)
</dt> <dt>



Das System wird gerade heruntergefahren.


</dt> </dl> </dd> <dt>

<span id="ERROR_PORT_NOT_SET"></span><span id="error_port_not_set"></span>**\_fehlerport \_ nicht \_ festgelegt**
</dt> <dd> <dl> <dt>

642 (0x282)
</dt> <dt>



Es wurde versucht, einen Debugport für Prozesse zu entfernen, aber es wurde noch kein Port mit dem Prozess verknüpft.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_VERSION_CHECK_FAILURE"></span><span id="error_ds_version_check_failure"></span>**Fehler bei der \_ \_ Versions \_ Überprüfung \_ des Fehlers.**
</dt> <dd> <dl> <dt>

643 (0x283)
</dt> <dt>



Diese Windows-Version ist nicht kompatibel mit der Verhaltens Version der Verzeichnis Gesamtstruktur, der Domäne oder des Domänen Controllers.


</dt> </dl> </dd> <dt>

<span id="ERROR_RANGE_NOT_FOUND"></span><span id="error_range_not_found"></span>**der Fehler \_ Bereich wurde \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

644 (0x284)
</dt> <dt>



Der angegebene Bereich wurde nicht in der Bereichs Liste gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SAFE_MODE_DRIVER"></span><span id="error_not_safe_mode_driver"></span>**Fehler \_ " \_ Treiber nicht sicher \_ Modus \_ "**
</dt> <dd> <dl> <dt>

646 (0x286)
</dt> <dt>



Der Treiber wurde nicht geladen, da das System im abgesicherten Modus gestartet wird.


</dt> </dl> </dd> <dt>

<span id="ERROR_FAILED_DRIVER_ENTRY"></span><span id="error_failed_driver_entry"></span>**Fehler \_ beim \_ Treiber \_ Eintrag.**
</dt> <dd> <dl> <dt>

647 (0x287)
</dt> <dt>



Der Treiber wurde nicht geladen, da der Initialisierungs Befehl nicht ausgeführt werden konnte.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_ENUMERATION_ERROR"></span><span id="error_device_enumeration_error"></span>**Fehler bei \_ Geräte \_ Enumeration. \_**
</dt> <dd> <dl> <dt>

648 (0x288)
</dt> <dt>



"% Hs" hat einen Fehler beim Anwenden von Energie oder Lesen der Gerätekonfiguration ermittelt. Dies kann durch einen Ausfall der Hardware oder durch eine schlechte Verbindung verursacht werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_MOUNT_POINT_NOT_RESOLVED"></span><span id="error_mount_point_not_resolved"></span>**Fehler \_ \_ Einfügepunkt \_ nicht \_ aufgelöst**
</dt> <dd> <dl> <dt>

649 (0x289)
</dt> <dt>



Fehler beim Erstellungs Vorgang, da der Name mindestens einen Einfügepunkt enthielt, der zu einem Volume aufgelöst wird, an das das angegebene Geräte Objekt nicht angefügt ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DEVICE_OBJECT_PARAMETER"></span><span id="error_invalid_device_object_parameter"></span>**Fehler bei \_ ungültigem \_ Geräte \_ Objekt \_ Parameter**
</dt> <dd> <dl> <dt>

650 (0x28a)
</dt> <dt>



Der Geräte Objekt Parameter ist entweder kein gültiges Geräte Objekt oder ist nicht an das durch den Dateinamen angegebene Volume angefügt.


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_OCCURED"></span><span id="error_mca_occured"></span>**Fehler- \_ MCA \_ aufgetreten**
</dt> <dd> <dl> <dt>

651 (0x28b)
</dt> <dt>



Fehler bei der Computer Überprüfung. Überprüfen Sie das System Ereignisprotokoll, um weitere Informationen zu erhalten.


</dt> </dl> </dd> <dt>

<span id="ERROR_DRIVER_DATABASE_ERROR"></span><span id="error_driver_database_error"></span>**Fehler \_ Treiber- \_ Daten Bank \_ Fehler**
</dt> <dd> <dl> <dt>

652 (0x28c)
</dt> <dt>



Fehler \[ %2 \] beim Verarbeiten der Treiberdatenbank.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYSTEM_HIVE_TOO_LARGE"></span><span id="error_system_hive_too_large"></span>**Fehler \_ System \_ Hive \_ zu \_ groß**
</dt> <dd> <dl> <dt>

653 (0x28d)
</dt> <dt>



Die Größe des System Hive hat das Limit überschritten.


</dt> </dl> </dd> <dt>

<span id="ERROR_DRIVER_FAILED_PRIOR_UNLOAD"></span><span id="error_driver_failed_prior_unload"></span>**Fehler \_ Treiber \_ Fehler \_ vor dem \_ entladen.**
</dt> <dd> <dl> <dt>

654 (0x28e)
</dt> <dt>



Der Treiber konnte nicht geladen werden, da sich eine frühere Version des Treibers noch im Speicher befindet.


</dt> </dl> </dd> <dt>

<span id="ERROR_VOLSNAP_PREPARE_HIBERNATE"></span><span id="error_volsnap_prepare_hibernate"></span>**Fehler beim Vorbereiten des Ruhe Zustands für " \_ Volsnap". \_ \_**
</dt> <dd> <dl> <dt>

655 (0x28f)
</dt> <dt>



{Volumeschattenkopie-Dienst} Warten Sie, während das Volumeschattenkopie-Dienst Volume% HS für den Ruhezustand vorbereitet.


</dt> </dl> </dd> <dt>

<span id="ERROR_HIBERNATION_FAILURE"></span><span id="error_hibernation_failure"></span>**Fehler im Ruhezustand \_ \_**
</dt> <dd> <dl> <dt>

656 (0x290)
</dt> <dt>



Das System konnte nicht in den Ruhezustand versetzt werden (der Fehlercode lautet% HS). Der Ruhezustand wird deaktiviert, bis das System neu gestartet wird.


</dt> </dl> </dd> <dt>

<span id="ERROR_PWD_TOO_LONG"></span><span id="error_pwd_too_long"></span>**Fehler \_ pwd \_ zu \_ lang**
</dt> <dd> <dl> <dt>

657 (0x291)
</dt> <dt>



Das angegebene Kennwort ist zu lang, um die Richtlinie Ihres Benutzerkontos zu erfüllen. Wählen Sie ein kürzeres Kennwort aus.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_SYSTEM_LIMITATION"></span><span id="error_file_system_limitation"></span>**\_ \_ System \_ Einschränkung für Fehler Datei**
</dt> <dd> <dl> <dt>

665 (0x299)
</dt> <dt>



Der angeforderte Vorgang konnte aufgrund einer Dateisystemeinschränkung nicht ausgeführt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_ASSERTION_FAILURE"></span><span id="error_assertion_failure"></span>**Fehler bei der Fehler \_ Behauptung \_**
</dt> <dd> <dl> <dt>

668 (0x29c)
</dt> <dt>



Ein Fehler bei der Übersetzung ist aufgetreten.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACPI_ERROR"></span><span id="error_acpi_error"></span>**Fehler- \_ ACPI- \_ Fehler**
</dt> <dd> <dl> <dt>

669 (0x29d)
</dt> <dt>



Im ACPI-Subsystem ist ein Fehler aufgetreten.


</dt> </dl> </dd> <dt>

<span id="ERROR_WOW_ASSERTION"></span><span id="error_wow_assertion"></span>**Fehler WOW-Assertion \_ \_**
</dt> <dd> <dl> <dt>

670 (0x29e)
</dt> <dt>



WOW-Assertionsfehler.


</dt> </dl> </dd> <dt>

<span id="ERROR_PNP_BAD_MPS_TABLE"></span><span id="error_pnp_bad_mps_table"></span>**Fehler PNP-Tabelle für ungültige \_ \_ \_ MPS \_**
</dt> <dd> <dl> <dt>

671 (0x29f)
</dt> <dt>



In der MPS-Tabelle des System-BIOS fehlt ein Gerät. Dieses Gerät wird nicht verwendet. Wenden Sie sich für das System-BIOS-Update an Ihren Systemanbieter.


</dt> </dl> </dd> <dt>

<span id="ERROR_PNP_TRANSLATION_FAILED"></span><span id="error_pnp_translation_failed"></span>**Fehler bei \_ pnp- \_ Übersetzung \_ .**
</dt> <dd> <dl> <dt>

672 (0x2a0)
</dt> <dt>



Ein Konvertierer konnte Ressourcen nicht übersetzen.


</dt> </dl> </dd> <dt>

<span id="ERROR_PNP_IRQ_TRANSLATION_FAILED"></span><span id="error_pnp_irq_translation_failed"></span>**Fehler bei PNP-Fehler bei der \_ \_ \_ Übersetzung. \_**
</dt> <dd> <dl> <dt>

673 (0x2a1)
</dt> <dt>



Ein iriq-Konvertierer konnte Ressourcen nicht übersetzen.


</dt> </dl> </dd> <dt>

<span id="ERROR_PNP_INVALID_ID"></span><span id="error_pnp_invalid_id"></span>**Fehler \_ pnp \_ - \_ ID ist ungültig.**
</dt> <dd> <dl> <dt>

674 (0x2a2)
</dt> <dt>



Treiber "%2" hat eine ungültige ID für ein untergeordnetes Gerät (%3) zurückgegeben.


</dt> </dl> </dd> <dt>

<span id="ERROR_WAKE_SYSTEM_DEBUGGER"></span><span id="error_wake_system_debugger"></span>**Fehler Reaktivierungs \_ \_ System \_ Debugger**
</dt> <dd> <dl> <dt>

675 (0x2a3)
</dt> <dt>



{Kernel Debugger erwacht}. der System Debugger wurde durch einen Interrupt aktiviert.


</dt> </dl> </dd> <dt>

<span id="ERROR_HANDLES_CLOSED"></span><span id="error_handles_closed"></span>**Fehler \_ Handles \_ geschlossen**
</dt> <dd> <dl> <dt>

676 (0x2a4)
</dt> <dt>



{Handles geschlossen} Handles zu Objekten wurden aufgrund des angeforderten Vorgangs automatisch geschlossen.


</dt> </dl> </dd> <dt>

<span id="ERROR_EXTRANEOUS_INFORMATION"></span><span id="error_extraneous_information"></span>**Fehler über \_ flüssige \_ Informationen**
</dt> <dd> <dl> <dt>

677 (0x2a5)
</dt> <dt>



{Zu viele Informationen} Die angegebene Zugriffs Steuerungs Liste (Access Control List, ACL) enthielt mehr Informationen als erwartet.


</dt> </dl> </dd> <dt>

<span id="ERROR_RXACT_COMMIT_NECESSARY"></span><span id="error_rxact_commit_necessary"></span>**Fehler- \_ rxact- \_ Commit \_ erforderlich**
</dt> <dd> <dl> <dt>

678 (0x2a6)
</dt> <dt>



Dieser warnebenenstatus gibt an, dass der Transaktionsstatus bereits für die Registrierungs Unterstruktur vorhanden ist, dass jedoch bereits ein Transaktionscommit abgebrochen wurde. Der Commit wurde nicht abgeschlossen, aber es wurde kein Rollback ausgeführt (es kann sein, dass ggf. ein Commit ausgeführt wird).


</dt> </dl> </dd> <dt>

<span id="ERROR_MEDIA_CHECK"></span><span id="error_media_check"></span>**Fehler \_ Medien \_ Überprüfung**
</dt> <dd> <dl> <dt>

679 (0x2a7)
</dt> <dt>



{Media Changed} Die Medien haben sich möglicherweise geändert.


</dt> </dl> </dd> <dt>

<span id="ERROR_GUID_SUBSTITUTION_MADE"></span><span id="error_guid_substitution_made"></span>**Fehler- \_ GUID- \_ Ersetzung \_**
</dt> <dd> <dl> <dt>

680 (0x2a8)
</dt> <dt>



{GUID-Ersetzung} Während der Übersetzung eines globalen Bezeichners (GUID) in eine Windows-Sicherheits-ID (SID) wurde kein administrativ definiertes GUID-Präfix gefunden. Ein Ersatz Präfix wurde verwendet, wodurch die Systemsicherheit nicht beeinträchtigt wird. Dies bietet jedoch möglicherweise einen restriktiveren Zugriff als beabsichtigt.


</dt> </dl> </dd> <dt>

<span id="ERROR_STOPPED_ON_SYMLINK"></span><span id="error_stopped_on_symlink"></span>**Fehler \_ \_ bei \_ symlink.**
</dt> <dd> <dl> <dt>

681 (0x2a9)
</dt> <dt>



Der Erstellungs Vorgang wurde beendet, nachdem eine symbolische Verknüpfung erreicht wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_LONGJUMP"></span><span id="error_longjump"></span>**Fehler beim \_ longjump**
</dt> <dd> <dl> <dt>

682 (0x2aa)
</dt> <dt>



Ein langer Sprung wurde ausgeführt.


</dt> </dl> </dd> <dt>

<span id="ERROR_PLUGPLAY_QUERY_VETOED"></span><span id="error_plugplay_query_vetoed"></span>**Fehler beim \_ plugplay der \_ Abfrage. \_**
</dt> <dd> <dl> <dt>

683 (0x2ab)
</dt> <dt>



Der Plug & Play Abfrage Vorgang war nicht erfolgreich.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNWIND_CONSOLIDATE"></span><span id="error_unwind_consolidate"></span>**Fehler \_ entladen \_ konsolidieren**
</dt> <dd> <dl> <dt>

684 (0x2ac)
</dt> <dt>



Eine Frame Konsolidierung wurde ausgeführt.


</dt> </dl> </dd> <dt>

<span id="ERROR_REGISTRY_HIVE_RECOVERED"></span><span id="error_registry_hive_recovered"></span>**Fehler \_ Registrierungs \_ Struktur \_ wieder hergestellt**
</dt> <dd> <dl> <dt>

685 (0x2ad)
</dt> <dt>



{Registrierungs Struktur wieder hergestellt} Registrierungs Struktur (Datei):% HS war beschädigt und wurde wieder hergestellt. Einige Daten sind möglicherweise verloren gegangen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DLL_MIGHT_BE_INSECURE"></span><span id="error_dll_might_be_insecure"></span>**Fehler- \_ dll ist \_ möglicherweise \_ \_ unsicher**
</dt> <dd> <dl> <dt>

686 (0x2ae)
</dt> <dt>



Die Anwendung versucht, ausführbaren Code aus dem Modul% HS auszuführen. Dies kann unsicher sein. Eine Alternative,% HS, ist verfügbar. Sollte die Anwendung das sichere Modul% HS verwenden?


</dt> </dl> </dd> <dt>

<span id="ERROR_DLL_MIGHT_BE_INCOMPATIBLE"></span><span id="error_dll_might_be_incompatible"></span>**Fehler- \_ dll ist \_ möglicherweise nicht \_ \_ kompatibel**
</dt> <dd> <dl> <dt>

687 (0x2af)
</dt> <dt>



Die Anwendung lädt ausführbaren Code aus dem Modul% HS. Dies ist sicher, kann jedoch mit früheren Versionen des Betriebssystems nicht kompatibel sein. Eine Alternative,% HS, ist verfügbar. Sollte die Anwendung das sichere Modul% HS verwenden?


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_EXCEPTION_NOT_HANDLED"></span><span id="error_dbg_exception_not_handled"></span>**Fehler bei \_ dbg- \_ Ausnahme \_ nicht \_ behandelt.**
</dt> <dd> <dl> <dt>

688 (0x2b0)
</dt> <dt>



Der Debugger hat die Ausnahme nicht behandelt.


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_REPLY_LATER"></span><span id="error_dbg_reply_later"></span>**Fehler \_ dbg- \_ Antwort \_ später**
</dt> <dd> <dl> <dt>

689 (0x2b1)
</dt> <dt>



Der Debugger antwortet später.


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_UNABLE_TO_PROVIDE_HANDLE"></span><span id="error_dbg_unable_to_provide_handle"></span>**Fehler \_ dbg \_ kann \_ \_ Handle nicht bereitstellen \_ .**
</dt> <dd> <dl> <dt>

690 (0x2b2)
</dt> <dt>



Der Debugger kann kein Handle bereitstellen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_TERMINATE_THREAD"></span><span id="error_dbg_terminate_thread"></span>**Fehler \_ dbg \_ - \_ Thread beenden**
</dt> <dd> <dl> <dt>

691 (0x2b3)
</dt> <dt>



Der Debugger hat den Thread beendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_TERMINATE_PROCESS"></span><span id="error_dbg_terminate_process"></span>**Fehler \_ dbg-Beendigungs \_ \_ Prozess**
</dt> <dd> <dl> <dt>

692 (0x2b4)
</dt> <dt>



Der Debugger hat den Prozess beendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_CONTROL_C"></span><span id="error_dbg_control_c"></span>**Fehler- \_ dbg- \_ Steuerelement \_ C**
</dt> <dd> <dl> <dt>

693 (0x2b5)
</dt> <dt>



Der Debugger hat die Steuerung C erhalten.


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_PRINTEXCEPTION_C"></span><span id="error_dbg_printexception_c"></span>**Fehler \_ dbg \_ PrintException \_ C**
</dt> <dd> <dl> <dt>

694 (0x2b6)
</dt> <dt>



Der Debugger hat eine Ausnahme für das Steuerelement C ausgegeben


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_RIPEXCEPTION"></span><span id="error_dbg_ripexception"></span>**Fehler \_ dbg- \_ ripexception**
</dt> <dd> <dl> <dt>

695 (0x2b7)
</dt> <dt>



Der Debugger hat eine RIP-Ausnahme empfangen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_CONTROL_BREAK"></span><span id="error_dbg_control_break"></span>**Fehler beim \_ dbg- \_ Steuerungs \_ Umbruch.**
</dt> <dd> <dl> <dt>

696 (0x2b8)
</dt> <dt>



Der Debugger hat die Steuerungs Pause empfangen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_COMMAND_EXCEPTION"></span><span id="error_dbg_command_exception"></span>**Fehler \_ dbg- \_ Befehls \_ Ausnahme**
</dt> <dd> <dl> <dt>

697 (0x2b9)
</dt> <dt>



Ausnahme bei der Kommunikation mit dem Debugger.


</dt> </dl> </dd> <dt>

<span id="ERROR_OBJECT_NAME_EXISTS"></span><span id="error_object_name_exists"></span>**der Fehler \_ Objekt \_ Name ist \_ vorhanden.**
</dt> <dd> <dl> <dt>

698 (0x2ba)
</dt> <dt>



{Object ist vorhanden} Es wurde versucht, ein Objekt zu erstellen, und der Objektname war bereits vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_THREAD_WAS_SUSPENDED"></span><span id="error_thread_was_suspended"></span>**der Fehler \_ Thread \_ wurde angeh \_ alten.**
</dt> <dd> <dl> <dt>

699 (0x2bb)
</dt> <dt>



{Thread angehalten} Eine Thread Beendigung ist aufgetreten, während der Thread angehalten wurde. Der Thread wurde fortgesetzt, und die Beendigung wurde fortgesetzt.


</dt> </dl> </dd> <dt>

<span id="ERROR_IMAGE_NOT_AT_BASE"></span><span id="error_image_not_at_base"></span>**Fehler \_ Bild \_ nicht \_ auf \_ Basis**
</dt> <dd> <dl> <dt>

700 (0x2bc)
</dt> <dt>



{Image verschoben} Eine Bilddatei konnte nicht an der in der Bilddatei angegebenen Adresse zugeordnet werden. Lokale Fixups müssen für dieses Image ausgeführt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_RXACT_STATE_CREATED"></span><span id="error_rxact_state_created"></span>**Fehler \_ rxact- \_ Status \_ erstellt**
</dt> <dd> <dl> <dt>

701 (0x2bd)
</dt> <dt>



Dieser Status der Informations Stufe gibt an, dass ein angegebener Transaktionsstatus der Registrierungs Teilstruktur noch nicht vorhanden war und erstellt werden musste.


</dt> </dl> </dd> <dt>

<span id="ERROR_SEGMENT_NOTIFICATION"></span><span id="error_segment_notification"></span>**Fehler \_ Segment \_ Benachrichtigung**
</dt> <dd> <dl> <dt>

702 (0x2be)
</dt> <dt>



{Segment laden} Ein VDM (Virtual DOS Machine) lädt, entladen oder verschiebt ein MS-DOS-oder Win16-Programm Segment Image. Eine Ausnahme wird ausgelöst, sodass ein Debugger Symbole und Breakpoints innerhalb dieser 16-Bit-Segmente laden, entladen oder nachverfolgen kann.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_CURRENT_DIRECTORY"></span><span id="error_bad_current_directory"></span>**Fehler \_ beim \_ aktuellen \_ Verzeichnis.**
</dt> <dd> <dl> <dt>

703 (0x2bf)
</dt> <dt>



{Ungültiges Aktuelles Verzeichnis} Der Prozess kann nicht zum aktuellen Start Verzeichnis% HS wechseln. Wählen Sie OK aus, um das aktuelle Verzeichnis auf% HS festzulegen, oder wählen Sie Abbrechen aus, um die


</dt> </dl> </dd> <dt>

<span id="ERROR_FT_READ_RECOVERY_FROM_BACKUP"></span><span id="error_ft_read_recovery_from_backup"></span>**Fehler \_ \_ beim Lesen \_ der Wiederherstellung \_ aus der \_ Sicherung**
</dt> <dd> <dl> <dt>

704 (0x2c0)
</dt> <dt>



{Redundant Read} Um eine Lese Anforderung zu erfüllen, liest das NT-fehlertolerante Dateisystem die angeforderten Daten erfolgreich aus einer redundanten Kopie. Der Grund hierfür ist, dass das Dateisystem auf einem Mitglied des fehlertoleranten Volumes fehlgeschlagen ist, den Fehlerbereich des Geräts jedoch nicht neu zuweisen konnte.


</dt> </dl> </dd> <dt>

<span id="ERROR_FT_WRITE_RECOVERY"></span><span id="error_ft_write_recovery"></span>**Fehler- \_ ft- \_ Schreib \_ Wiederherstellung**
</dt> <dd> <dl> <dt>

705 (0x2c1)
</dt> <dt>



{Redundanter Schreibvorgang} Zum erfüllen einer Schreib Anforderung hat das NT-fehlertolerante Dateisystem erfolgreich eine redundante Kopie der Informationen geschrieben. Dies wurde durchgeführt, weil das Dateisystem auf einem Mitglied des fehlertoleranten Volumes einen Fehler feststellt, den Fehlerbereich des Geräts jedoch nicht neu zuweisen konnte.


</dt> </dl> </dd> <dt>

<span id="ERROR_IMAGE_MACHINE_TYPE_MISMATCH"></span><span id="error_image_machine_type_mismatch"></span>**Fehler beim \_ Abbild des \_ Computer \_ Typs \_ .**
</dt> <dd> <dl> <dt>

706 (0x2c2)
</dt> <dt>



{Nicht übereinstimmende Computertypen} Die Abbild Datei "% hs" ist gültig, aber für einen anderen Computertyp als den aktuellen Computer. Wählen Sie OK aus, um den Vorgang fortzusetzen, oder Abbrechen, um die dll-Auslastung


</dt> </dl> </dd> <dt>

<span id="ERROR_RECEIVE_PARTIAL"></span><span id="error_receive_partial"></span>**Fehler beim \_ Empfang \_**
</dt> <dd> <dl> <dt>

707 (0x2c3)
</dt> <dt>



{Partielle Daten empfangen} Der Netzwerk Transport hat partielle Daten an den Client zurückgegeben. Die verbleibenden Daten werden später gesendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_RECEIVE_EXPEDITED"></span><span id="error_receive_expedited"></span>**Fehler beim \_ empfangen. \_**
</dt> <dd> <dl> <dt>

708 (0x2c4)
</dt> <dt>



{Beschleunigte empfangene Daten} Der Netzwerk Transport hat Daten an den Client zurückgegeben, der vom Remote System als beschleunigt gekennzeichnet wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_RECEIVE_PARTIAL_EXPEDITED"></span><span id="error_receive_partial_expedited"></span>**Fehler beim \_ Empfang \_ teilweise \_ beschleunigt**
</dt> <dd> <dl> <dt>

709 (0x2c5)
</dt> <dt>



{Teilweise beschleunigte Daten empfangen} Der Netzwerk Transport hat partielle Daten an den Client zurückgegeben, und diese Daten wurden vom Remote System als beschleunigt gekennzeichnet. Die verbleibenden Daten werden später gesendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVENT_DONE"></span><span id="error_event_done"></span>**Fehler \_ Ereignis \_ abgeschlossen**
</dt> <dd> <dl> <dt>

710 (0x2c6)
</dt> <dt>



{TDI-Ereignis abgeschlossen} Die TDI-Anzeige wurde erfolgreich abgeschlossen.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVENT_PENDING"></span><span id="error_event_pending"></span>**Fehler \_ Ereignis \_ Ausstehend**
</dt> <dd> <dl> <dt>

711 (0x2c7)
</dt> <dt>



{TDI-Ereignis steht aus. Der TDI-Hinweis wurde in den Status "Ausstehend" versetzt.


</dt> </dl> </dd> <dt>

<span id="ERROR_CHECKING_FILE_SYSTEM"></span><span id="error_checking_file_system"></span>**Fehler beim über \_ prüfen des \_ Datei \_ Systems**
</dt> <dd> <dl> <dt>

712 (0x2c8)
</dt> <dt>



Das Dateisystem auf% WZ wird überprüft.


</dt> </dl> </dd> <dt>

<span id="ERROR_FATAL_APP_EXIT"></span><span id="error_fatal_app_exit"></span>**Fehler \_ beim \_ Beenden der app. \_**
</dt> <dd> <dl> <dt>

713 (0x2c9)
</dt> <dt>



{Schwerwiegender Anwendungs Exit}% HS.


</dt> </dl> </dd> <dt>

<span id="ERROR_PREDEFINED_HANDLE"></span><span id="error_predefined_handle"></span>**Fehler \_ vordefiniertes \_ handle**
</dt> <dd> <dl> <dt>

714 (0x2ca)
</dt> <dt>



Auf den angegebenen Registrierungsschlüssel wird von einem vordefinierten Handle verwiesen.


</dt> </dl> </dd> <dt>

<span id="ERROR_WAS_UNLOCKED"></span><span id="error_was_unlocked"></span>**Fehler \_ wurde \_ entsperrt.**
</dt> <dd> <dl> <dt>

715 (0x2cb)
</dt> <dt>



{Seite entsperrt} Der Seitenschutz einer gesperrten Seite wurde in "kein Zugriff" geändert, und die Seite wurde aus dem Arbeitsspeicher und aus dem Prozess entsperrt.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_NOTIFICATION"></span><span id="error_service_notification"></span>**Fehler \_ Dienst \_ Benachrichtigung**
</dt> <dd> <dl> <dt>

716 (0x2cc)
</dt> <dt>



% HS


</dt> </dl> </dd> <dt>

<span id="ERROR_WAS_LOCKED"></span><span id="error_was_locked"></span>**der Fehler \_ wurde \_ gesperrt.**
</dt> <dd> <dl> <dt>

717 (0x2cd)
</dt> <dt>



{Seite gesperrt} Eine der zu Sperr enden Seiten war bereits gesperrt.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_HARD_ERROR"></span><span id="error_log_hard_error"></span>**\_ \_ schwer Fehlerprotokoll \_ Fehler**
</dt> <dd> <dl> <dt>

718 (0x2ce)
</dt> <dt>



Anwendungs Popup: %1: %2


</dt> </dl> </dd> <dt>

<span id="ERROR_ALREADY_WIN32"></span><span id="error_already_win32"></span>**Fehler \_ bereits \_ Win32**
</dt> <dd> <dl> <dt>

719 (0x2cf)
</dt> <dt>



Fehler \_ bereits \_ Win32


</dt> </dl> </dd> <dt>

<span id="ERROR_IMAGE_MACHINE_TYPE_MISMATCH_EXE"></span><span id="error_image_machine_type_mismatch_exe"></span>**Fehler \_ Bild des \_ Computer Typs nicht übereinstimmende \_ \_ \_ exe-Datei**
</dt> <dd> <dl> <dt>

720 (0x2d0)
</dt> <dt>



{Nicht übereinstimmende Computertypen} Die Abbild Datei "% hs" ist gültig, aber für einen anderen Computertyp als den aktuellen Computer.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_YIELD_PERFORMED"></span><span id="error_no_yield_performed"></span>**Fehler \_ keine \_ Yield- \_ Ausführung**
</dt> <dd> <dl> <dt>

721 (0x2d1)
</dt> <dt>



Eine Yield-Ausführung wurde ausgeführt, und es konnte kein Thread ausgeführt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_TIMER_RESUME_IGNORED"></span><span id="error_timer_resume_ignored"></span>**Fehler Zeit Geber-Fortsetzung \_ \_ \_ ignoriert**
</dt> <dd> <dl> <dt>

722 (0x2d2)
</dt> <dt>



Das Fort Setz Bare Flag für eine Timer-API wurde ignoriert.


</dt> </dl> </dd> <dt>

<span id="ERROR_ARBITRATION_UNHANDLED"></span><span id="error_arbitration_unhandled"></span>**Fehler bei der \_ Schiedsgerichtsbarkeit \_ nicht behandelt**
</dt> <dd> <dl> <dt>

723 (0x2d3)
</dt> <dt>



Der Arbiter hat die Vermittlung dieser Ressourcen für das übergeordnete Element verzögert.


</dt> </dl> </dd> <dt>

<span id="ERROR_CARDBUS_NOT_SUPPORTED"></span><span id="error_cardbus_not_supported"></span>**Fehler \_ CardBus \_ \_ wird nicht unterstützt.**
</dt> <dd> <dl> <dt>

724 (0x2d4)
</dt> <dt>



Das eingefügte CardBus-Gerät kann aufgrund eines Konfigurations Fehlers auf "% hs" nicht gestartet werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_MP_PROCESSOR_MISMATCH"></span><span id="error_mp_processor_mismatch"></span>**Fehler- \_ MP- \_ Prozessor Konflikt \_**
</dt> <dd> <dl> <dt>

725 (0x2d5)
</dt> <dt>



Die CPUs in diesem Multiprozessorsystem weisen nicht die gleiche Revisions Ebene auf. Um alle Prozessoren zu verwenden, schränkt das Betriebssystem die Funktionen des am wenigsten leistungsfähigen Prozessors im System ein. Sollten Probleme mit diesem System auftreten, wenden Sie sich an den CPU-Hersteller, um festzustellen, ob diese Kombination von Prozessoren unterstützt wird


</dt> </dl> </dd> <dt>

<span id="ERROR_HIBERNATED"></span><span id="error_hibernated"></span>**Fehler im Ruhezustand \_**
</dt> <dd> <dl> <dt>

726 (0x2d6)
</dt> <dt>



Das System wurde in den Ruhezustand versetzt.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESUME_HIBERNATION"></span><span id="error_resume_hibernation"></span>**Fehler beim Fortsetzen des Ruhe Zustands \_ \_**
</dt> <dd> <dl> <dt>

727 (0x2d7)
</dt> <dt>



Das System wurde aus dem Ruhezustand fortgesetzt.


</dt> </dl> </dd> <dt>

<span id="ERROR_FIRMWARE_UPDATED"></span><span id="error_firmware_updated"></span>**Fehler \_ Firmware \_ aktualisiert**
</dt> <dd> <dl> <dt>

728 (0x2d8)
</dt> <dt>



Es wurde festgestellt, dass das \[ vorherige Firmwareupdate = %2, Aktuelles Firmwareupdate %3, aktualisiert wurde \] .


</dt> </dl> </dd> <dt>

<span id="ERROR_DRIVERS_LEAKING_LOCKED_PAGES"></span><span id="error_drivers_leaking_locked_pages"></span>**Fehler Treiber, die auf \_ \_ \_ Gesperrte \_ Seiten weichen**
</dt> <dd> <dl> <dt>

729 (0x2d9)
</dt> <dt>



Ein Gerätetreiber entfernt gesperrte e/A-Seiten, die eine Beeinträchtigung des Systems verursachen. Das System hat den Verfolgungs Code automatisch aktiviert, um zu versuchen, den Übeltäter abzufangen.


</dt> </dl> </dd> <dt>

<span id="ERROR_WAKE_SYSTEM"></span><span id="error_wake_system"></span>**Fehler Reaktivierungs \_ \_ System**
</dt> <dd> <dl> <dt>

730 (0x2da)
</dt> <dt>



Das System wurde reaktiviert.


</dt> </dl> </dd> <dt>

<span id="ERROR_WAIT_1"></span><span id="error_wait_1"></span>**Fehler \_ Wartezeit \_ 1**
</dt> <dd> <dl> <dt>

731 (0x2db)
</dt> <dt>



Fehler \_ Wartezeit \_ 1


</dt> </dl> </dd> <dt>

<span id="ERROR_WAIT_2"></span><span id="error_wait_2"></span>**Fehler \_ Wartezeit \_ 2**
</dt> <dd> <dl> <dt>

732 (0x2dc)
</dt> <dt>



Fehler \_ Wartezeit \_ 2


</dt> </dl> </dd> <dt>

<span id="ERROR_WAIT_3"></span><span id="error_wait_3"></span>**Fehler \_ Wartezeit \_ 3**
</dt> <dd> <dl> <dt>

733 (0x2dd)
</dt> <dt>



Fehler \_ Wartezeit \_ 3


</dt> </dl> </dd> <dt>

<span id="ERROR_WAIT_63"></span><span id="error_wait_63"></span>**Fehler \_ Wartezeit \_ 63**
</dt> <dd> <dl> <dt>

734 (0x2de)
</dt> <dt>



Fehler \_ Wartezeit \_ 63


</dt> </dl> </dd> <dt>

<span id="ERROR_ABANDONED_WAIT_0"></span><span id="error_abandoned_wait_0"></span>**Fehler \_ abgebrochen, \_ Wartezeit \_ 0**
</dt> <dd> <dl> <dt>

735 (0x2df)
</dt> <dt>



Fehler \_ abgebrochen, \_ Wartezeit \_ 0


</dt> </dl> </dd> <dt>

<span id="ERROR_ABANDONED_WAIT_63"></span><span id="error_abandoned_wait_63"></span>**Fehler \_ abgebrochen, \_ Wartezeit \_ 63**
</dt> <dd> <dl> <dt>

736 (0x2e0)
</dt> <dt>



Fehler \_ abgebrochen, \_ Wartezeit \_ 63


</dt> </dl> </dd> <dt>

<span id="ERROR_USER_APC"></span><span id="error_user_apc"></span>**Fehler \_ Benutzer- \_ APC**
</dt> <dd> <dl> <dt>

737 (0x2e1)
</dt> <dt>



Fehler \_ Benutzer- \_ APC


</dt> </dl> </dd> <dt>

<span id="ERROR_KERNEL_APC"></span><span id="error_kernel_apc"></span>**Fehler \_ Kernel- \_ APC**
</dt> <dd> <dl> <dt>

738 (0x2e2)
</dt> <dt>



Fehler \_ Kernel- \_ APC


</dt> </dl> </dd> <dt>

<span id="ERROR_ALERTED"></span><span id="error_alerted"></span>**Fehler \_ gewarnt**
</dt> <dd> <dl> <dt>

739 (0x2e3)
</dt> <dt>



Fehler \_ gewarnt


</dt> </dl> </dd> <dt>

<span id="ERROR_ELEVATION_REQUIRED"></span><span id="error_elevation_required"></span>**Fehler \_ Erhöhung \_ erforderlich**
</dt> <dd> <dl> <dt>

740 (0x2e4)
</dt> <dt>



Der angeforderte Vorgang erfordert eine Erhöhung der Rechte.


</dt> </dl> </dd> <dt>

<span id="ERROR_REPARSE"></span><span id="error_reparse"></span>**Fehler \_ Analyse**
</dt> <dd> <dl> <dt>

741 (0x2e5)
</dt> <dt>



Vom Objekt-Manager sollte eine Analyse ausgeführt werden, da der Name der Datei zu einem symbolischen Link geführt hat.


</dt> </dl> </dd> <dt>

<span id="ERROR_OPLOCK_BREAK_IN_PROGRESS"></span><span id="error_oplock_break_in_progress"></span>**Fehler \_ beim Oplock-Vorgang \_ \_ in Bearbeitung. \_**
</dt> <dd> <dl> <dt>

742 (0x2e6)
</dt> <dt>



Ein Open/Create-Vorgang wurde abgeschlossen, während eine Unterbrechung der Sperre ausgeführt wird.


</dt> </dl> </dd> <dt>

<span id="ERROR_VOLUME_MOUNTED"></span><span id="error_volume_mounted"></span>**Fehler \_ Volume bereitgestellt \_**
</dt> <dd> <dl> <dt>

743 (0x2e7)
</dt> <dt>



Ein neues Volume wurde von einem Dateisystem bereitgestellt.


</dt> </dl> </dd> <dt>

<span id="ERROR_RXACT_COMMITTED"></span><span id="error_rxact_committed"></span>**Fehler beim Ausführen von \_ rxact. \_**
</dt> <dd> <dl> <dt>

744 (0x2E8)
</dt> <dt>



Dieser Status der Erfolgs Stufe gibt an, dass der Transaktionsstatus für die Registrierungs Unterstruktur bereits vorhanden ist, dass jedoch bereits ein Transaktionscommit abgebrochen wurde. Der Commit ist nun abgeschlossen.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOTIFY_CLEANUP"></span><span id="error_notify_cleanup"></span>**Fehler \_ beim \_ Cleanup der Fehler Benachrichtigung**
</dt> <dd> <dl> <dt>

745 (0x2e9)
</dt> <dt>



Dies weist darauf hin, dass ein Benachrichtigungs Change Request durch Schließen des Handles abgeschlossen wurde, das die Benachrichtigung Change Request.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRIMARY_TRANSPORT_CONNECT_FAILED"></span><span id="error_primary_transport_connect_failed"></span>**Fehler bei \_ primärer \_ Transport \_ Verbindung \_ .**
</dt> <dd> <dl> <dt>

746 (0x2ea)
</dt> <dt>



{Connect-Fehler beim primären Transport} Es wurde versucht, eine Verbindung mit dem Remote Server "% hs" auf dem primären Transport herzustellen, aber die Verbindung konnte nicht hergestellt werden. Der Computer konnte über einen sekundären Transport eine Verbindung herstellen.


</dt> </dl> </dd> <dt>

<span id="ERROR_PAGE_FAULT_TRANSITION"></span><span id="error_page_fault_transition"></span>**Fehler \_ Seiten-Fehler \_ \_ Übergang**
</dt> <dd> <dl> <dt>

747 (0x2eb)
</dt> <dt>



Der Seiten Fehler war ein Übergangs Fehler.


</dt> </dl> </dd> <dt>

<span id="ERROR_PAGE_FAULT_DEMAND_ZERO"></span><span id="error_page_fault_demand_zero"></span>**Fehler \_ Seiten-Fehler \_ \_ Anforderung \_ null**
</dt> <dd> <dl> <dt>

748 (0x2ec)
</dt> <dt>



Der Seiten Fehler war ein Fehler, der NULL ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_PAGE_FAULT_COPY_ON_WRITE"></span><span id="error_page_fault_copy_on_write"></span>**Fehler \_ Seiten-Fehler \_ \_ Kopie \_ beim \_ schreiben**
</dt> <dd> <dl> <dt>

749 (0x2ed)
</dt> <dt>



Der Seiten Fehler war ein Fehler, der NULL ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_PAGE_FAULT_GUARD_PAGE"></span><span id="error_page_fault_guard_page"></span>**Fehler \_ Seite \_ \_ Fehlerschutz ( \_ Seite)**
</dt> <dd> <dl> <dt>

750 (0x2ee)
</dt> <dt>



Der Seiten Fehler war ein Fehler, der NULL ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_PAGE_FAULT_PAGING_FILE"></span><span id="error_page_fault_paging_file"></span>**Fehler \_ Seiten \_ - \_ Paging- \_ Datei**
</dt> <dd> <dl> <dt>

751 (0x2ef)
</dt> <dt>



Der Seiten Fehler wurde durchlesen von einem sekundären Speichergerät erfüllt.


</dt> </dl> </dd> <dt>

<span id="ERROR_CACHE_PAGE_LOCKED"></span><span id="error_cache_page_locked"></span>**Fehler \_ Cache \_ Seite \_ gesperrt**
</dt> <dd> <dl> <dt>

752 (0x2F 0)
</dt> <dt>



Die zwischengespeicherte Seite wurde während des Vorgangs gesperrt.


</dt> </dl> </dd> <dt>

<span id="ERROR_CRASH_DUMP"></span><span id="error_crash_dump"></span>**Fehler \_ Absturz Abbild \_**
</dt> <dd> <dl> <dt>

753 (0x2F)
</dt> <dt>



Absturz Abbild ist in Auslagerungs Datei vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_BUFFER_ALL_ZEROS"></span><span id="error_buffer_all_zeros"></span>**Fehler \_ Puffer \_ alle \_ Nullen**
</dt> <dd> <dl> <dt>

754 (0x2F 2)
</dt> <dt>



Der angegebene Puffer enthält alle Nullen.


</dt> </dl> </dd> <dt>

<span id="ERROR_REPARSE_OBJECT"></span><span id="error_reparse_object"></span>**Fehleranalyse \_ \_ Objekt**
</dt> <dd> <dl> <dt>

755 (0x2F)
</dt> <dt>



Vom Objekt-Manager sollte eine Analyse ausgeführt werden, da der Name der Datei zu einem symbolischen Link geführt hat.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_REQUIREMENTS_CHANGED"></span><span id="error_resource_requirements_changed"></span>**Fehler beim \_ Ändern der Ressourcen \_ Anforderungen. \_**
</dt> <dd> <dl> <dt>

756 (0x2F)
</dt> <dt>



Das Gerät hat eine Abfrage beendet, und die zugehörigen Ressourcenanforderungen wurden geändert.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSLATION_COMPLETE"></span><span id="error_translation_complete"></span>**Fehler \_ Übersetzung ist \_ beendet**
</dt> <dd> <dl> <dt>

757 (0x2F)
</dt> <dt>



Der Konvertierer hat diese Ressourcen in den globalen Bereich übersetzt, und es sollten keine weiteren Übersetzungen durchgeführt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOTHING_TO_TERMINATE"></span><span id="error_nothing_to_terminate"></span>**Fehler \_ beim \_ \_ beenden.**
</dt> <dd> <dl> <dt>

758 (0x2F)
</dt> <dt>



Ein Prozess, der beendet wird, verfügt über keine zu beendenden Threads.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROCESS_NOT_IN_JOB"></span><span id="error_process_not_in_job"></span>**Fehler \_ Prozess \_ nicht \_ in \_ Auftrag**
</dt> <dd> <dl> <dt>

759 (0x2F)
</dt> <dt>



Der angegebene Prozess ist nicht Teil eines Auftrags.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROCESS_IN_JOB"></span><span id="error_process_in_job"></span>**Fehler \_ Prozess \_ in \_ Auftrag**
</dt> <dd> <dl> <dt>

760 (0x2F 8)
</dt> <dt>



Der angegebene Prozess ist Teil eines Auftrags.


</dt> </dl> </dd> <dt>

<span id="ERROR_VOLSNAP_HIBERNATE_READY"></span><span id="error_volsnap_hibernate_ready"></span>**Fehler beim Volsnap-in- \_ \_ \_ Ready-Zustand.**
</dt> <dd> <dl> <dt>

761 (0x2F)
</dt> <dt>



{Volumeschattenkopie-Dienst} Das System ist nun bereit für den Ruhezustand.


</dt> </dl> </dd> <dt>

<span id="ERROR_FSFILTER_OP_COMPLETED_SUCCESSFULLY"></span><span id="error_fsfilter_op_completed_successfully"></span>**Fehler " \_ fsfilter op" wurde \_ \_ \_ erfolgreich abgeschlossen.**
</dt> <dd> <dl> <dt>

762 (0x2fa)
</dt> <dt>



Ein Dateisystem-oder Dateisystem Filter-Treiber hat einen fsfilter-Vorgang erfolgreich abgeschlossen.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERRUPT_VECTOR_ALREADY_CONNECTED"></span><span id="error_interrupt_vector_already_connected"></span>**Fehler \_ Interrupt- \_ Vektor \_ bereits \_ verbunden**
</dt> <dd> <dl> <dt>

763 (0x2fb)
</dt> <dt>



Der angegebene Interrupt-Vektor war bereits verbunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERRUPT_STILL_CONNECTED"></span><span id="error_interrupt_still_connected"></span>**Fehler \_ Interrupt ist \_ weiterhin \_ verbunden.**
</dt> <dd> <dl> <dt>

764 (0x2fc)
</dt> <dt>



Der angegebene Interrupt-Vektor ist weiterhin verbunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_WAIT_FOR_OPLOCK"></span><span id="error_wait_for_oplock"></span>**Fehler beim \_ warten \_ auf \_ Oplock.**
</dt> <dd> <dl> <dt>

765 (0x2fd)
</dt> <dt>



Ein Vorgang wird blockiert, wenn auf eine Oplock-Sperre gewartet wird.


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_EXCEPTION_HANDLED"></span><span id="error_dbg_exception_handled"></span>**Fehler bei \_ dbg- \_ Ausnahme. \_**
</dt> <dd> <dl> <dt>

766 (0x2fe)
</dt> <dt>



Vom Debugger behandelte Ausnahme.


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_CONTINUE"></span><span id="error_dbg_continue"></span>**Fehler \_ dbg \_ fortsetzen**
</dt> <dd> <dl> <dt>

767 (0x2ff)
</dt> <dt>



Der Debugger wurde fortgesetzt.


</dt> </dl> </dd> <dt>

<span id="ERROR_CALLBACK_POP_STACK"></span><span id="error_callback_pop_stack"></span>**Fehler \_ Rückruf- \_ Pop- \_ Stapel**
</dt> <dd> <dl> <dt>

768 (0x300)
</dt> <dt>



Eine Ausnahme ist in einem Benutzermodus-Rückruf aufgetreten, und der Kernel Rückruf Frame sollte entfernt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_COMPRESSION_DISABLED"></span><span id="error_compression_disabled"></span>**Fehler \_ Komprimierung \_ deaktiviert**
</dt> <dd> <dl> <dt>

769 (0x301)
</dt> <dt>



Die Komprimierung ist für dieses Volume deaktiviert.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANTFETCHBACKWARDS"></span><span id="error_cantfetchbackwards"></span>**Fehler beim \_ kanfetchrückwärts**
</dt> <dd> <dl> <dt>

770 (0x302)
</dt> <dt>



Der Datenanbieter kann ein Resultset nicht rückwärts abrufen.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANTSCROLLBACKWARDS"></span><span id="error_cantscrollbackwards"></span>**Fehler beim \_ kanscrollrückwärts**
</dt> <dd> <dl> <dt>

771 (0x303)
</dt> <dt>



Der Datenanbieter kann nicht rückwärts durch ein Resultset scrollen.


</dt> </dl> </dd> <dt>

<span id="ERROR_ROWSNOTRELEASED"></span><span id="error_rowsnotreleased"></span>**Fehler \_ rowsnotregeleast**
</dt> <dd> <dl> <dt>

772 (0x304)
</dt> <dt>



Der Datenanbieter erfordert, dass zuvor abgerufene Daten freigegeben werden, bevor Sie weitere Daten anfordern.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_ACCESSOR_FLAGS"></span><span id="error_bad_accessor_flags"></span>**Fehler \_ hafte \_ Accessor- \_ Flags**
</dt> <dd> <dl> <dt>

773 (0x305)
</dt> <dt>



Der Datenanbieter konnte die Flags, die für eine Spalten Bindung in einem Accessor festgelegt wurden, nicht interpretieren.


</dt> </dl> </dd> <dt>

<span id="ERROR_ERRORS_ENCOUNTERED"></span><span id="error_errors_encountered"></span>**Fehler \_ Fehler \_**
</dt> <dd> <dl> <dt>

774 (0x306)
</dt> <dt>



Beim Verarbeiten der Anforderung ist mindestens ein Fehler aufgetreten.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_CAPABLE"></span><span id="error_not_capable"></span>**Fehler \_ nicht \_ möglich**
</dt> <dd> <dl> <dt>

775 (0x307)
</dt> <dt>



Die-Implementierung ist nicht in der Lage, die Anforderung auszuführen.


</dt> </dl> </dd> <dt>

<span id="ERROR_REQUEST_OUT_OF_SEQUENCE"></span><span id="error_request_out_of_sequence"></span>**Fehler \_ Anforderung \_ außerhalb \_ der \_ Reihenfolge**
</dt> <dd> <dl> <dt>

776 (0x308)
</dt> <dt>



Der Client einer Komponente hat einen Vorgang angefordert, der aufgrund des Status der Komponenteninstanz nicht gültig ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_VERSION_PARSE_ERROR"></span><span id="error_version_parse_error"></span>**Fehler beim Analysieren der Fehler \_ Version. \_ \_**
</dt> <dd> <dl> <dt>

777 (0x309)
</dt> <dt>



Eine Versionsnummer konnte nicht analysiert werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_BADSTARTPOSITION"></span><span id="error_badstartposition"></span>**Fehler \_ badstartposition**
</dt> <dd> <dl> <dt>

778 (0x30a)
</dt> <dt>



Die Startposition des Iterators ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEMORY_HARDWARE"></span><span id="error_memory_hardware"></span>**Hardware des Fehler \_ Speichers \_**
</dt> <dd> <dl> <dt>

779 (0x30b)
</dt> <dt>



Die Hardware hat einen nicht korrigierbaren Speicherfehler gemeldet.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_REPAIR_DISABLED"></span><span id="error_disk_repair_disabled"></span>**Fehler Datenträger \_ \_ Reparatur \_ deaktiviert**
</dt> <dd> <dl> <dt>

780 (0x30c)
</dt> <dt>



Für den versuchten Vorgang musste die Selbstreparatur aktiviert werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSUFFICIENT_RESOURCE_FOR_SPECIFIED_SHARED_SECTION_SIZE"></span><span id="error_insufficient_resource_for_specified_shared_section_size"></span>**Fehler \_ \_ bei unzureichender Ressource \_ für \_ angegebene Größe des frei \_ gegebenen \_ Abschnitts \_ .**
</dt> <dd> <dl> <dt>

781 (0x30d)
</dt> <dt>



Der Desktop Heap hat beim Zuordnen des Sitzungs Speichers einen Fehler gefunden. Weitere Informationen finden Sie im System Ereignisprotokoll.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYSTEM_POWERSTATE_TRANSITION"></span><span id="error_system_powerstate_transition"></span>**Fehler \_ System- \_ PowerState- \_ Übergang**
</dt> <dd> <dl> <dt>

782 (0x30e)
</dt> <dt>



Der System Energiezustand wechselt von "%2" in "%3".


</dt> </dl> </dd> <dt>

<span id="ERROR_SYSTEM_POWERSTATE_COMPLEX_TRANSITION"></span><span id="error_system_powerstate_complex_transition"></span>**Fehler \_ System- \_ PowerState- \_ komplexer \_ Übergang**
</dt> <dd> <dl> <dt>

783 (0x30f)
</dt> <dt>



Der System Energiezustand wechselt von "%2" in "%3", kann jedoch "%4" eingeben.


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_EXCEPTION"></span><span id="error_mca_exception"></span>**Fehler bei \_ MCA- \_ Ausnahme.**
</dt> <dd> <dl> <dt>

784 (0x310)
</dt> <dt>



Ein Thread wird aufgrund von MCA mit der MCA-Ausnahme versendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCESS_AUDIT_BY_POLICY"></span><span id="error_access_audit_by_policy"></span>**Fehler \_ Zugriffs \_ Überwachung \_ nach \_ Richtlinie**
</dt> <dd> <dl> <dt>

785 (0x311)
</dt> <dt>



Der Zugriff auf "%1" wird von der Richtlinien Regel "%2" überwacht.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCESS_DISABLED_NO_SAFER_UI_BY_POLICY"></span><span id="error_access_disabled_no_safer_ui_by_policy"></span>**Fehler \_ Zugriff \_ \_ ohne \_ sicherere \_ Benutzeroberfläche \_ nach \_ Richtlinie deaktiviert**
</dt> <dd> <dl> <dt>

786 (0x312)
</dt> <dt>



Der Zugriff auf "%1" wurde durch den Administrator durch die Richtlinien Regel "%2" eingeschränkt.


</dt> </dl> </dd> <dt>

<span id="ERROR_ABANDON_HIBERFILE"></span><span id="error_abandon_hiberfile"></span>**Fehler beim Abbrechen der Ruhe Zustands \_ \_ Datei**
</dt> <dd> <dl> <dt>

787 (0x313)
</dt> <dt>



Eine gültige Ruhe Zustands Datei wurde für ungültig erklärt und sollte abgebrochen werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOST_WRITEBEHIND_DATA_NETWORK_DISCONNECTED"></span><span id="error_lost_writebehind_data_network_disconnected"></span>**Fehler beim Rück Schreiben von \_ \_ Daten im \_ \_ Netzwerk \_ .**
</dt> <dd> <dl> <dt>

788 (0x314)
</dt> <dt>



{Verzögertes Schreiben fehlgeschlagen} In Windows konnten nicht alle Daten für die Datei "% hs;" gespeichert werden. die Daten sind verloren gegangen. Dieser Fehler kann durch Probleme mit der Netzwerk Konnektivität verursacht werden. Versuchen Sie, diese Datei an anderer Stelle zu speichern.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOST_WRITEBEHIND_DATA_NETWORK_SERVER_ERROR"></span><span id="error_lost_writebehind_data_network_server_error"></span>**Fehler \_ beim \_ \_ Daten \_ Netzwerk \_ Server- \_ Fehler beim Rück Schreiben von Daten.**
</dt> <dd> <dl> <dt>

789 (0x315)
</dt> <dt>



{Verzögertes Schreiben fehlgeschlagen} In Windows konnten nicht alle Daten für die Datei "% hs;" gespeichert werden. die Daten sind verloren gegangen. Dieser Fehler wurde vom Server zurückgegeben, auf dem die Datei vorhanden ist. Versuchen Sie, diese Datei an anderer Stelle zu speichern.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOST_WRITEBEHIND_DATA_LOCAL_DISK_ERROR"></span><span id="error_lost_writebehind_data_local_disk_error"></span>**Fehler beim Zugriff auf \_ \_ \_ \_ den lokalen Daten \_ Träger des Schreibvorgangs \_ .**
</dt> <dd> <dl> <dt>

790 (0x316)
</dt> <dt>



{Verzögertes Schreiben fehlgeschlagen} In Windows konnten nicht alle Daten für die Datei "% hs;" gespeichert werden. die Daten sind verloren gegangen. Dieser Fehler kann darauf zurückzuführen sein, dass das Gerät entfernt wurde oder das Medium schreibgeschützt ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_MCFG_TABLE"></span><span id="error_bad_mcfg_table"></span>**Fehler \_ hafte \_ MCFG- \_ Tabelle**
</dt> <dd> <dl> <dt>

791 (0x317)
</dt> <dt>



Die für dieses Gerät erforderlichen Ressourcen stehen in Konflikt mit der MCFG-Tabelle.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_REPAIR_REDIRECTED"></span><span id="error_disk_repair_redirected"></span>**Fehler Datenträger \_ \_ Reparatur \_ umgeleitet**
</dt> <dd> <dl> <dt>

792 (0x318)
</dt> <dt>



Die volumereparatur konnte nicht durchgeführt werden, während Sie online ist. Bitte planen Sie, das Volume offline zu schalten, damit es repariert werden kann.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_REPAIR_UNSUCCESSFUL"></span><span id="error_disk_repair_unsuccessful"></span>**Fehler beim Reparieren des Datenträgers. \_ \_ \_**
</dt> <dd> <dl> <dt>

793 (0x319)
</dt> <dt>



Die volumereparatur war nicht erfolgreich.


</dt> </dl> </dd> <dt>

<span id="ERROR_CORRUPT_LOG_OVERFULL"></span><span id="error_corrupt_log_overfull"></span>**Fehler \_ beschädigte \_ Protokoll \_ Überschreitung**
</dt> <dd> <dl> <dt>

794 (0x31a)
</dt> <dt>



Eines der volumebeschädigungsprotokolle ist voll. Weitere beschädigte Beschädigungen werden nicht protokolliert.


</dt> </dl> </dd> <dt>

<span id="ERROR_CORRUPT_LOG_CORRUPTED"></span><span id="error_corrupt_log_corrupted"></span>**Fehler \_ \_ beschädigte Protokoll \_ beschädigt.**
</dt> <dd> <dl> <dt>

795 (0x31b)
</dt> <dt>



Eines der Protokolle der Volumebeschädigung ist intern beschädigt und muss neu erstellt werden. Das Volume kann nicht erkannte Beschädigungen enthalten und muss gescannt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CORRUPT_LOG_UNAVAILABLE"></span><span id="error_corrupt_log_unavailable"></span>**Fehler \_ beschädigte \_ Protokoll nicht \_ verfügbar.**
</dt> <dd> <dl> <dt>

796 (0x31c)
</dt> <dt>



Eines der Protokolle der Volumebeschädigung ist nicht für die Verwendung verfügbar.


</dt> </dl> </dd> <dt>

<span id="ERROR_CORRUPT_LOG_DELETED_FULL"></span><span id="error_corrupt_log_deleted_full"></span>**Fehler \_ beim \_ Löschen des Protokolls \_ \_ vollständig.**
</dt> <dd> <dl> <dt>

797 (0x31d)
</dt> <dt>



Eines der volumebeschädigungsprotokolle wurde gelöscht, und es wurden weiterhin beschädigte Datensätze angezeigt. Das Volume enthält erkannte Beschädigungen und muss gescannt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CORRUPT_LOG_CLEARED"></span><span id="error_corrupt_log_cleared"></span>**Fehler \_ beim \_ Löschen des Protokolls. \_**
</dt> <dd> <dl> <dt>

798 (0x31e)
</dt> <dt>



Eines der Protokolle der Volumebeschädigung wurde von CHKDSK gelöscht und enthält keine echten Beschädigungen mehr.


</dt> </dl> </dd> <dt>

<span id="ERROR_ORPHAN_NAME_EXHAUSTED"></span><span id="error_orphan_name_exhausted"></span>**Fehler \_ verwaister \_ Name \_ aufgebraucht**
</dt> <dd> <dl> <dt>

799 (0x31f)
</dt> <dt>



Auf dem Volume sind verwaiste Dateien vorhanden, Sie konnten jedoch nicht wieder hergestellt werden, da im Wiederherstellungs Verzeichnis keine weiteren neuen Namen erstellt werden konnten. Dateien müssen aus dem Wiederherstellungs Verzeichnis verschoben werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_OPLOCK_SWITCHED_TO_NEW_HANDLE"></span><span id="error_oplock_switched_to_new_handle"></span>**Fehler- \_ Oplock \_ \_ zum \_ neuen \_ handle gewechselt**
</dt> <dd> <dl> <dt>

800 (0x320)
</dt> <dt>



Die Oplock, die diesem Handle zugeordnet war, ist jetzt einem anderen Handle zugeordnet.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_GRANT_REQUESTED_OPLOCK"></span><span id="error_cannot_grant_requested_oplock"></span>**Fehler \_ beim \_ erteilen der \_ angeforderten \_ Oplock.**
</dt> <dd> <dl> <dt>

801 (0x321)
</dt> <dt>



Eine Oplock der angeforderten Ebene kann nicht erteilt werden. Möglicherweise ist eine Oplock einer niedrigeren Ebene verfügbar.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_BREAK_OPLOCK"></span><span id="error_cannot_break_oplock"></span>**Fehler \_ beim \_ Abbrechen der \_ Oplock-Taste**
</dt> <dd> <dl> <dt>

802 (0x322)
</dt> <dt>



Der Vorgang wurde nicht erfolgreich abgeschlossen, da er dazu führen würde, dass ein Oplock-Vorgang abgebrochen wird. Der Aufrufer hat angefordert, dass vorhandene oplocks nicht beschädigt sind.


</dt> </dl> </dd> <dt>

<span id="ERROR_OPLOCK_HANDLE_CLOSED"></span><span id="error_oplock_handle_closed"></span>**Fehler " \_ Oplock \_ handle" \_ geschlossen**
</dt> <dd> <dl> <dt>

803 (0x323)
</dt> <dt>



Das Handle, dem diese Oplock zugeordnet war, wurde geschlossen. Die Oplock ist nun beschädigt.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_ACE_CONDITION"></span><span id="error_no_ace_condition"></span>**Error \_ No \_ ACE- \_ Bedingung**
</dt> <dd> <dl> <dt>

804 (0x324)
</dt> <dt>



Der angegebene ACE (Access Control Entry, Zugriffs Steuerungs Eintrag) enthält keine Bedingung.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ACE_CONDITION"></span><span id="error_invalid_ace_condition"></span>**\_ungültige \_ ACE- \_ Bedingung.**
</dt> <dd> <dl> <dt>

805 (0x325)
</dt> <dt>



Der angegebene ACE (Access Control Entry, Zugriffs Steuerungs Eintrag) enthält eine ungültige Bedingung.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_HANDLE_REVOKED"></span><span id="error_file_handle_revoked"></span>**Fehler \_ Datei \_ handle \_ gesperrt**
</dt> <dd> <dl> <dt>

806 (0x326)
</dt> <dt>



Der Zugriff auf das angegebene Datei Handle wurde widerrufen.


</dt> </dl> </dd> <dt>

<span id="ERROR_IMAGE_AT_DIFFERENT_BASE"></span><span id="error_image_at_different_base"></span>**Fehler \_ Bild \_ an \_ unterschiedlicher \_ Basis**
</dt> <dd> <dl> <dt>

807 (0x327)
</dt> <dt>



Eine Bilddatei wurde an einer anderen Adresse als der in der Bilddatei angegebenen Adresse zugeordnet, aber Fixups werden weiterhin automatisch für das Image ausgeführt.


</dt> </dl> </dd> <dt>

<span id="ERROR_EA_ACCESS_DENIED"></span><span id="error_ea_access_denied"></span>**Fehler- \_ EA- \_ Zugriff \_ verweigert**
</dt> <dd> <dl> <dt>

994 (0x3e2)
</dt> <dt>



Der Zugriff auf das erweiterte Attribut wurde verweigert.


</dt> </dl> </dd> <dt>

<span id="ERROR_OPERATION_ABORTED"></span><span id="error_operation_aborted"></span>**Fehler \_ Vorgang \_ abgebrochen**
</dt> <dd> <dl> <dt>

995 (0x3e3)
</dt> <dt>



Der e/a-Vorgang wurde aufgrund eines Thread Beendigungs-oder einer Anwendungsanforderung abgebrochen.


</dt> </dl> </dd> <dt>

<span id="ERROR_IO_INCOMPLETE"></span><span id="error_io_incomplete"></span>**Fehler- \_ IO \_ unvollständig**
</dt> <dd> <dl> <dt>

996 (0x3e4)
</dt> <dt>



Das überlappende e/a-Ereignis ist nicht in einem signalisierten Zustand.


</dt> </dl> </dd> <dt>

<span id="ERROR_IO_PENDING"></span><span id="error_io_pending"></span>**Fehler- \_ IO steht \_ aus**
</dt> <dd> <dl> <dt>

997 (0x3e5)
</dt> <dt>



Überlappende e/a-Vorgänge werden ausgeführt.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOACCESS"></span><span id="error_noaccess"></span>**Fehler \_ NoAccess**
</dt> <dd> <dl> <dt>

998 (0x3e6)
</dt> <dt>



Ungültiger Zugriff auf den Speicherort des Speichers.


</dt> </dl> </dd> <dt>

<span id="ERROR_SWAPERROR"></span><span id="error_swaperror"></span>**Fehler " \_ swaperror"**
</dt> <dd> <dl> <dt>

999 (0x3e7)
</dt> <dt>



Fehler beim Ausführen des InPage-Vorgangs.


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

 

 
