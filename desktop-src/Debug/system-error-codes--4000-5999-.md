---
description: Beschreibt die in der Header Datei "Winerror. h" definierten Fehlercodes 4000-5999 und ist für Entwickler bestimmt.
ms.assetid: 1d2f7160-6322-4c75-abbc-4a882bbdf7ce
title: System Fehler Codes (4000-5999) (Winerror. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: bfd39042489f2a92ff2eb13df92a22e392c5405e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126892"
---
# <a name="system-error-codes-4000-5999"></a>System Fehler Codes (4000-5999)

> [!NOTE]
> Diese Informationen sind für Entwickler gedacht, die Systemfehler Debuggen. Bei anderen Fehlern, wie z. b. Problemen mit Windows Update, finden Sie eine Liste der Ressourcen auf der Seite [Fehlercodes](system-error-codes.md) .

In der folgenden Liste werden die [Systemfehler Codes](system-error-codes.md) für die Fehler 4000 bis 5999 beschrieben. Sie werden von der [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) -Funktion zurückgegeben, wenn viele Funktionen fehlschlagen. Um den Beschreibungstext für den Fehler in Ihrer Anwendung abzurufen, verwenden Sie die [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) -Funktion mit dem Flag " **Format \_ Message \_ from \_ System** ".

<dl> <dt>

<span id="ERROR_WINS_INTERNAL"></span><span id="error_wins_internal"></span>**Fehler \_ gewinnt \_ intern**
</dt> <dd> <dl> <dt>

4000 (0xfa0)
</dt> <dt>



Fehler beim Verarbeiten des Befehls.


</dt> </dl> </dd> <dt>

<span id="ERROR_CAN_NOT_DEL_LOCAL_WINS"></span><span id="error_can_not_del_local_wins"></span>**Fehler \_ beim \_ \_ \_ lokalen \_ WINS-Fehler.**
</dt> <dd> <dl> <dt>

4001 (0xfa1)
</dt> <dt>



Der lokale WINS kann nicht gelöscht werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATIC_INIT"></span><span id="error_static_init"></span>**Fehler bei \_ statischer \_ Init**
</dt> <dd> <dl> <dt>

4002 (0xfa2)
</dt> <dt>



Fehler beim Importieren aus der Datei.


</dt> </dl> </dd> <dt>

<span id="ERROR_INC_BACKUP"></span><span id="error_inc_backup"></span>**Fehler \_ inkl. \_ Sicherung**
</dt> <dd> <dl> <dt>

4003 (0xfa3)
</dt> <dt>



Die Sicherung ist fehlgeschlagen. Wurde zuvor eine vollständige Sicherung durchgeführt?


</dt> </dl> </dd> <dt>

<span id="ERROR_FULL_BACKUP"></span><span id="error_full_backup"></span>**\_vollständige Fehler \_ Sicherung**
</dt> <dd> <dl> <dt>

4004 (0xfa4)
</dt> <dt>



Die Sicherung ist fehlgeschlagen. Überprüfen Sie das Verzeichnis, in dem Sie die Datenbank sichern.


</dt> </dl> </dd> <dt>

<span id="ERROR_REC_NON_EXISTENT"></span><span id="error_rec_non_existent"></span>**Fehler- \_ rec \_ nicht \_ vorhanden**
</dt> <dd> <dl> <dt>

4005 (0xfa5)
</dt> <dt>



Der Name ist in der WINS-Datenbank nicht vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_RPL_NOT_ALLOWED"></span><span id="error_rpl_not_allowed"></span>**Fehler- \_ RPL \_ nicht \_ zulässig**
</dt> <dd> <dl> <dt>

4006 (0xfa6)
</dt> <dt>



Die Replikation mit einem nicht konfigurierten Partner ist nicht zulässig.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_CONTENTINFO_VERSION_UNSUPPORTED"></span><span id="peerdist_error_contentinfo_version_unsupported"></span>**Die ContentInfo-Version von "Peer" ist \_ \_ \_ \_ nicht unterstützt.**
</dt> <dd> <dl> <dt>

4050 (0xF-2)
</dt> <dt>



Die Version der bereitgestellten Inhaltsinformationen wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_CANNOT_PARSE_CONTENTINFO"></span><span id="peerdist_error_cannot_parse_contentinfo"></span>**der Peer-Manager- \_ Fehler \_ kann \_ \_ ContentInfo nicht analysieren.**
</dt> <dd> <dl> <dt>

4051 (0xF-3)
</dt> <dt>



Die angegebenen Inhaltsinformationen sind falsch formatiert.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_MISSING_DATA"></span><span id="peerdist_error_missing_data"></span>**Fehler beim Peer von "Peer". \_ \_ \_**
</dt> <dd> <dl> <dt>

4052 (0xF)
</dt> <dt>



Die angeforderten Daten wurden in lokalen oder Peer Caches nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_NO_MORE"></span><span id="peerdist_error_no_more"></span>**Peer \_ Fehler \_ nicht \_ mehr**
</dt> <dd> <dl> <dt>

4053 (0xF D5)
</dt> <dt>



Es sind keine weiteren Daten verfügbar oder erforderlich.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_NOT_INITIALIZED"></span><span id="peerdist_error_not_initialized"></span>**der Peer-Manager- \_ Fehler wurde \_ nicht \_ initialisiert.**
</dt> <dd> <dl> <dt>

4054 (0xF, 6)
</dt> <dt>



Das angegebene Objekt wurde nicht initialisiert.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_ALREADY_INITIALIZED"></span><span id="peerdist_error_already_initialized"></span>**der Peer-dist- \_ Fehler wurde \_ bereits \_ initialisiert.**
</dt> <dd> <dl> <dt>

4055 (0xF)
</dt> <dt>



Das angegebene Objekt wurde bereits initialisiert.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_SHUTDOWN_IN_PROGRESS"></span><span id="peerdist_error_shutdown_in_progress"></span>**\_Fehler \_ beim Herunterfahren \_ des \_ Peer-dist-Vorgangs.**
</dt> <dd> <dl> <dt>

4056 (0xF D8)
</dt> <dt>



Ein Shutdown-Vorgang wird bereits ausgeführt.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_INVALIDATED"></span><span id="peerdist_error_invalidated"></span>**der Peer \_ Fehler ist \_ ungültig.**
</dt> <dd> <dl> <dt>

4057 (0xF)
</dt> <dt>



Das angegebene Objekt wurde bereits für ungültig erklärt.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_ALREADY_EXISTS"></span><span id="peerdist_error_already_exists"></span>**der Peer-Manager- \_ Fehler ist \_ bereits \_ vorhanden.**
</dt> <dd> <dl> <dt>

4058 (0xfda)
</dt> <dt>



Ein Element ist bereits vorhanden und wurde nicht ersetzt.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_OPERATION_NOTFOUND"></span><span id="peerdist_error_operation_notfound"></span>**Fehler beim Peer \_ - \_ /Fehlervorgang. \_**
</dt> <dd> <dl> <dt>

4059 (0xF)
</dt> <dt>



Der angeforderte Vorgang kann nicht abgebrochen werden, da er bereits abgeschlossen ist.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_ALREADY_COMPLETED"></span><span id="peerdist_error_already_completed"></span>**der Peer-Manager- \_ Fehler ist \_ bereits \_ abgeschlossen.**
</dt> <dd> <dl> <dt>

4060 (0xF)
</dt> <dt>



Der Vorgang kann nicht durchgeführt werden, da er bereits durchgeführt wurde.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_OUT_OF_BOUNDS"></span><span id="peerdist_error_out_of_bounds"></span>**Peer \_ Fehler \_ außerhalb \_ des \_ gültigen Bereichs**
</dt> <dd> <dl> <dt>

4061 (0xF)
</dt> <dt>



Ein Vorgang, auf den über die Grenzen gültiger Daten zugegriffen wird.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_VERSION_UNSUPPORTED"></span><span id="peerdist_error_version_unsupported"></span>**\_ \_ \_ nicht unterstützte Version von "Peer Manager"**
</dt> <dd> <dl> <dt>

4062 (0xF)
</dt> <dt>



Die angeforderte Version wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_INVALID_CONFIGURATION"></span><span id="peerdist_error_invalid_configuration"></span>**\_ \_ ungültige Konfiguration des Peer-dist-Fehlers \_**
</dt> <dd> <dl> <dt>

4063 (0xF)
</dt> <dt>



Ein Konfigurations Wert ist ungültig.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_NOT_LICENSED"></span><span id="peerdist_error_not_licensed"></span>**der Peer \_ Fehler ist \_ nicht \_ lizenziert.**
</dt> <dd> <dl> <dt>

4064 (0xfe0)
</dt> <dt>



Die SKU ist nicht lizenziert.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_SERVICE_UNAVAILABLE"></span><span id="peerdist_error_service_unavailable"></span>**Peer- \_ \_ /fehlerdienst nicht \_ verfügbar**
</dt> <dd> <dl> <dt>

4065 (0xfe1)
</dt> <dt>



Der Peer-Manager-Dienst wird noch initialisiert und ist in Kürze verfügbar.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_TRUST_FAILURE"></span><span id="peerdist_error_trust_failure"></span>**Fehler bei der Peer- \_ \_ Vertrauensstellung \_**
</dt> <dd> <dl> <dt>

4066 (0xfe2)
</dt> <dt>



Die Kommunikation mit einem oder mehreren Computern wird aufgrund aktueller Fehler vorübergehend blockiert.


</dt> </dl> </dd> <dt>

<span id="ERROR_DHCP_ADDRESS_CONFLICT"></span><span id="error_dhcp_address_conflict"></span>**Fehler \_ DHCP- \_ Adress \_ Konflikt**
</dt> <dd> <dl> <dt>

4100 (0x1004)
</dt> <dt>



Der DHCP-Client hat eine IP-Adresse abgerufen, die bereits im Netzwerk verwendet wird. Die lokale Schnittstelle wird deaktiviert, bis der DHCP-Client eine neue Adresse abrufen kann.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_GUID_NOT_FOUND"></span><span id="error_wmi_guid_not_found"></span>**Fehler beim \_ WMI- \_ GUID wurde \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

4200 (0x1068)
</dt> <dt>



Die Übergabe der GUID wurde von einem WMI-Datenanbieter nicht als gültig erkannt.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_INSTANCE_NOT_FOUND"></span><span id="error_wmi_instance_not_found"></span>**Fehler bei \_ WMI- \_ Instanz \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

4201 (0x1069)
</dt> <dt>



Der Übergabe des Instanznamens wurde von einem WMI-Datenanbieter nicht als gültig erkannt.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_ITEMID_NOT_FOUND"></span><span id="error_wmi_itemid_not_found"></span>**Fehler \_ WMI- \_ ItemID \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

4202 (0x106a)
</dt> <dt>



Die bestandene Datenelement-ID wurde von einem WMI-Datenanbieter nicht als gültig erkannt.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_TRY_AGAIN"></span><span id="error_wmi_try_again"></span>**Fehler \_ WMI \_ \_ erneut versuchen**
</dt> <dd> <dl> <dt>

4203 (0x106b)
</dt> <dt>



Die WMI-Anforderung konnte nicht abgeschlossen werden und sollte erneut versucht werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_DP_NOT_FOUND"></span><span id="error_wmi_dp_not_found"></span>**Fehler beim \_ WMI- \_ DP \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

4204 (0x106c)
</dt> <dt>



Der WMI-Datenanbieter wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_UNRESOLVED_INSTANCE_REF"></span><span id="error_wmi_unresolved_instance_ref"></span>**Fehler beim Verweis auf \_ WMI- \_ aufgelöste \_ Instanz \_**
</dt> <dd> <dl> <dt>

4205 (0x106d)
</dt> <dt>



Der WMI-Datenanbieter verweist auf einen Instanzsatz, der nicht registriert wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_ALREADY_ENABLED"></span><span id="error_wmi_already_enabled"></span>**\_WMI-Fehler \_ bereits \_ aktiviert**
</dt> <dd> <dl> <dt>

4206 (0x106 e)
</dt> <dt>



Der WMI-Datenblock oder die Ereignis Benachrichtigung wurde bereits aktiviert.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_GUID_DISCONNECTED"></span><span id="error_wmi_guid_disconnected"></span>**Fehler beim \_ WMI- \_ GUID. \_**
</dt> <dd> <dl> <dt>

4207 (0x106f)
</dt> <dt>



Der WMI-Datenblock ist nicht mehr verfügbar.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_SERVER_UNAVAILABLE"></span><span id="error_wmi_server_unavailable"></span>**Fehler \_ WMI- \_ Server nicht \_ verfügbar**
</dt> <dd> <dl> <dt>

4208 (0x1070)
</dt> <dt>



Der WMI-Datendienst ist nicht verfügbar.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_DP_FAILED"></span><span id="error_wmi_dp_failed"></span>**Fehler beim WMI-Fehler. \_ \_ \_**
</dt> <dd> <dl> <dt>

4209 (0x1071)
</dt> <dt>



Fehler beim Ausführen der Anforderung durch den WMI-Datenanbieter.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_INVALID_MOF"></span><span id="error_wmi_invalid_mof"></span>**Fehler \_ WMI \_ ungültige \_ MOF**
</dt> <dd> <dl> <dt>

4210 (0x1072)
</dt> <dt>



Die WMI-MOF-Informationen sind ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_INVALID_REGINFO"></span><span id="error_wmi_invalid_reginfo"></span>**Fehler \_ WMI \_ ungültige \_ reginfo**
</dt> <dd> <dl> <dt>

4211 (0x1073)
</dt> <dt>



Die WMI-Registrierungsinformationen sind ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_ALREADY_DISABLED"></span><span id="error_wmi_already_disabled"></span>**WMI-Fehler ist \_ \_ bereits \_ deaktiviert.**
</dt> <dd> <dl> <dt>

4212 (0x1074)
</dt> <dt>



Der WMI-Datenblock oder die Ereignis Benachrichtigung wurde bereits deaktiviert.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_READ_ONLY"></span><span id="error_wmi_read_only"></span>**WMI-Fehler schreibgeschützt \_ \_ \_**
</dt> <dd> <dl> <dt>

4213 (0x1075)
</dt> <dt>



Das WMI-Datenelement oder der Datenblock ist schreibgeschützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_SET_FAILURE"></span><span id="error_wmi_set_failure"></span>**Fehler beim \_ WMI-Fehler \_ Satz. \_**
</dt> <dd> <dl> <dt>

4214 (0x1076)
</dt> <dt>



Das WMI-Datenelement oder der Datenblock konnte nicht geändert werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_APPCONTAINER"></span><span id="error_not_appcontainer"></span>**Fehler \_ nicht \_ appcontainer**
</dt> <dd> <dl> <dt>

4250 (0x109a)
</dt> <dt>



Dieser Vorgang ist nur im Kontext eines App-Containers gültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_APPCONTAINER_REQUIRED"></span><span id="error_appcontainer_required"></span>**Fehler \_ appcontainer \_ erforderlich**
</dt> <dd> <dl> <dt>

4251 (0x109b)
</dt> <dt>



Diese Anwendung kann nur im Kontext eines App-Containers ausgeführt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SUPPORTED_IN_APPCONTAINER"></span><span id="error_not_supported_in_appcontainer"></span>**Fehler \_ \_ wird \_ in appcontainer nicht unterstützt \_ .**
</dt> <dd> <dl> <dt>

4252 (0x109c)
</dt> <dt>



Diese Funktion wird im Kontext eines App-Containers nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PACKAGE_SID_LENGTH"></span><span id="error_invalid_package_sid_length"></span>**Fehler \_ ungültige \_ Paket- \_ sid- \_ Länge**
</dt> <dd> <dl> <dt>

4253 (0x109d)
</dt> <dt>



Die Länge der angegebenen SID ist keine gültige Länge für App-Container-SIDs.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MEDIA"></span><span id="error_invalid_media"></span>**\_ungültiger \_ Medien Fehler**
</dt> <dd> <dl> <dt>

4300 (0x10cc)
</dt> <dt>



Der Medien Bezeichner stellt kein gültiges Medium dar.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LIBRARY"></span><span id="error_invalid_library"></span>**\_ungültige \_ Bibliothek.**
</dt> <dd> <dl> <dt>

4301 (0x10cd)
</dt> <dt>



Der Bibliotheks Bezeichner stellt keine gültige Bibliothek dar.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MEDIA_POOL"></span><span id="error_invalid_media_pool"></span>**\_ungültiger \_ Medien \_ Pool**
</dt> <dd> <dl> <dt>

4302 (0x10ce)
</dt> <dt>



Der Medienpool Bezeichner stellt keinen gültigen Medienpool dar.


</dt> </dl> </dd> <dt>

<span id="ERROR_DRIVE_MEDIA_MISMATCH"></span><span id="error_drive_media_mismatch"></span>**Fehler \_ Laufwerk \_ Medien \_ stimmen nicht überein.**
</dt> <dd> <dl> <dt>

4303 (0x10cf)
</dt> <dt>



Das Laufwerk und das Medium sind nicht kompatibel oder nicht in verschiedenen Bibliotheken vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEDIA_OFFLINE"></span><span id="error_media_offline"></span>**Fehler \_ Medien \_ Offline**
</dt> <dd> <dl> <dt>

4304 (0x10d0)
</dt> <dt>



Das Medium ist zurzeit in einer Offline Bibliothek vorhanden und muss online sein, um diesen Vorgang auszuführen.


</dt> </dl> </dd> <dt>

<span id="ERROR_LIBRARY_OFFLINE"></span><span id="error_library_offline"></span>**Fehler \_ Bibliothek \_ Offline**
</dt> <dd> <dl> <dt>

4305 (0x10d1)
</dt> <dt>



Der Vorgang kann nicht für eine Offline Bibliothek ausgeführt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_EMPTY"></span><span id="error_empty"></span>**Fehler \_ leer**
</dt> <dd> <dl> <dt>

4306 (0x10d2)
</dt> <dt>



Die Bibliothek, das Laufwerk oder der Medienpool ist leer.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_EMPTY"></span><span id="error_not_empty"></span>**Fehler ist \_ nicht \_ leer.**
</dt> <dd> <dl> <dt>

4307 (0x10d3)
</dt> <dt>



Die Bibliothek, das Laufwerk oder der Medienpool müssen leer sein, um diesen Vorgang auszuführen.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEDIA_UNAVAILABLE"></span><span id="error_media_unavailable"></span>**Fehler \_ Medien nicht \_ verfügbar**
</dt> <dd> <dl> <dt>

4308 (0x10d4)
</dt> <dt>



In diesem Medienpool oder in der Bibliothek sind zurzeit keine Medien verfügbar.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_DISABLED"></span><span id="error_resource_disabled"></span>**Fehler \_ Ressource \_ deaktiviert**
</dt> <dd> <dl> <dt>

4309 (0x10d5)
</dt> <dt>



Eine für diesen Vorgang erforderliche Ressource ist deaktiviert.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_CLEANER"></span><span id="error_invalid_cleaner"></span>**Fehler \_ ungültiger \_ Reinigungs Fehler**
</dt> <dd> <dl> <dt>

4310 (0x10d6)
</dt> <dt>



Der Medien Bezeichner stellt keinen gültigen Bereinigungs Wert dar.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_CLEAN"></span><span id="error_unable_to_clean"></span>**Fehler \_ beim \_ \_ bereinigen.**
</dt> <dd> <dl> <dt>

4311 (0x10d7)
</dt> <dt>



Das Laufwerk kann nicht bereinigt werden oder unterstützt keine Bereinigung.


</dt> </dl> </dd> <dt>

<span id="ERROR_OBJECT_NOT_FOUND"></span><span id="error_object_not_found"></span>**Fehler \_ Objekt wurde \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

4312 (0x10d8)
</dt> <dt>



Der Objekt Bezeichner stellt kein gültiges Objekt dar.


</dt> </dl> </dd> <dt>

<span id="ERROR_DATABASE_FAILURE"></span><span id="error_database_failure"></span>**Fehler \_ Daten Bank \_ Fehler**
</dt> <dd> <dl> <dt>

4313 (0x10d9)
</dt> <dt>



Aus der Datenbank kann nicht gelesen oder in diese geschrieben werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DATABASE_FULL"></span><span id="error_database_full"></span>**Fehler \_ Datenbank \_ voll**
</dt> <dd> <dl> <dt>

4314 (0x10da)
</dt> <dt>



Die Datenbank ist voll.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEDIA_INCOMPATIBLE"></span><span id="error_media_incompatible"></span>**Fehler \_ Medien nicht \_ kompatibel**
</dt> <dd> <dl> <dt>

4315 (0x10db)
</dt> <dt>



Das Medium ist mit dem Gerät oder dem Medienpool nicht kompatibel.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_NOT_PRESENT"></span><span id="error_resource_not_present"></span>**die Fehler \_ Ressource ist \_ nicht \_ vorhanden.**
</dt> <dd> <dl> <dt>

4316 (0x10dc)
</dt> <dt>



Die für diesen Vorgang erforderliche Ressource ist nicht vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_OPERATION"></span><span id="error_invalid_operation"></span>**\_ungültiger \_ Vorgang.**
</dt> <dd> <dl> <dt>

4317 (0x10dd)
</dt> <dt>



Der Vorgangs Bezeichner ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEDIA_NOT_AVAILABLE"></span><span id="error_media_not_available"></span>**Fehler \_ Medien \_ nicht \_ verfügbar**
</dt> <dd> <dl> <dt>

4318 (0x10de)
</dt> <dt>



Das Medium ist nicht bereitgestellt oder kann nicht verwendet werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_NOT_AVAILABLE"></span><span id="error_device_not_available"></span>**Fehler \_ Gerät \_ nicht \_ verfügbar**
</dt> <dd> <dl> <dt>

4319 (0x10df)
</dt> <dt>



Das Gerät ist nicht einsatzbereit.


</dt> </dl> </dd> <dt>

<span id="ERROR_REQUEST_REFUSED"></span><span id="error_request_refused"></span>**Fehler \_ Anforderung \_ abgelehnt**
</dt> <dd> <dl> <dt>

4320 (0x10e0)
</dt> <dt>



Der Operator oder Administrator hat die Anforderung abgelehnt.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DRIVE_OBJECT"></span><span id="error_invalid_drive_object"></span>**Fehler \_ ungültiges \_ Laufwerks \_ Objekt.**
</dt> <dd> <dl> <dt>

4321 (0x10e1)
</dt> <dt>



Der Laufwerks Bezeichner stellt kein gültiges Laufwerk dar.


</dt> </dl> </dd> <dt>

<span id="ERROR_LIBRARY_FULL"></span><span id="error_library_full"></span>**Fehler \_ Bibliothek \_ voll**
</dt> <dd> <dl> <dt>

4322 (0x10e2)
</dt> <dt>



Die Bibliothek ist voll. Es ist kein Slot zur Verwendung verfügbar.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEDIUM_NOT_ACCESSIBLE"></span><span id="error_medium_not_accessible"></span>**Fehler \_ Medium ist \_ nicht \_ verfügbar.**
</dt> <dd> <dl> <dt>

4323 (0x10e3)
</dt> <dt>



Der Transport kann nicht auf das Medium zugreifen.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_LOAD_MEDIUM"></span><span id="error_unable_to_load_medium"></span>**Fehler \_ beim \_ \_ Laden des \_ Mediums.**
</dt> <dd> <dl> <dt>

4324 (0x10e4)
</dt> <dt>



Das Medium kann nicht in das Laufwerk geladen werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_INVENTORY_DRIVE"></span><span id="error_unable_to_inventory_drive"></span>**Fehler \_ beim \_ \_ inventarisieren des \_ Laufwerks**
</dt> <dd> <dl> <dt>

4325 (0x10e5)
</dt> <dt>



Der Laufwerks Status kann nicht abgerufen werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_INVENTORY_SLOT"></span><span id="error_unable_to_inventory_slot"></span>**Fehler \_ beim \_ \_ inventarisieren des \_ Slots.**
</dt> <dd> <dl> <dt>

4326 (0x10e6)
</dt> <dt>



Der slotstatus kann nicht abgerufen werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_INVENTORY_TRANSPORT"></span><span id="error_unable_to_inventory_transport"></span>**Fehler \_ beim \_ \_ inventarisieren des \_ Transports.**
</dt> <dd> <dl> <dt>

4327 (0x10e7)
</dt> <dt>



Der Status des Transports kann nicht abgerufen werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSPORT_FULL"></span><span id="error_transport_full"></span>**Fehler \_ Transport \_ voll**
</dt> <dd> <dl> <dt>

4328 (0x10e8)
</dt> <dt>



Der Transport kann nicht verwendet werden, da er bereits verwendet wird.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONTROLLING_IEPORT"></span><span id="error_controlling_ieport"></span>**Fehler beim \_ Steuern von \_ ieport.**
</dt> <dd> <dl> <dt>

4329 (0x10e9)
</dt> <dt>



Der einschleusen-/Ausgabeport kann nicht geöffnet oder geschlossen werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_EJECT_MOUNTED_MEDIA"></span><span id="error_unable_to_eject_mounted_media"></span>**Fehler \_ beim \_ \_ \_ eingebundenen Medienobjekt \_ .**
</dt> <dd> <dl> <dt>

4330 (0x10ea)
</dt> <dt>



Das Medium kann nicht ausstoßen, weil es sich in einem Laufwerk befindet.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLEANER_SLOT_SET"></span><span id="error_cleaner_slot_set"></span>**\_fehlerreinigungs \_ - \_ slotset**
</dt> <dd> <dl> <dt>

4331 (0x10eb)
</dt> <dt>



Ein Reinigungs Slot ist bereits reserviert.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLEANER_SLOT_NOT_SET"></span><span id="error_cleaner_slot_not_set"></span>**Fehlerbereinigungs \_ \_ Slot \_ nicht \_ festgelegt**
</dt> <dd> <dl> <dt>

4332 (0x10ec)
</dt> <dt>



Ein Reinigungs Slot ist nicht reserviert.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLEANER_CARTRIDGE_SPENT"></span><span id="error_cleaner_cartridge_spent"></span>**Fehler \_ Reinigungs- \_ Cartridge \_ aufgewendet**
</dt> <dd> <dl> <dt>

4333 (0x10ed)
</dt> <dt>



Die Reinigungs Patrone hat die maximale Anzahl von Laufwerks Bereinigungs Vorlagen durchgeführt.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNEXPECTED_OMID"></span><span id="error_unexpected_omid"></span>**\_unerwarteter Fehler bei \_ Omid.**
</dt> <dd> <dl> <dt>

4334 (0x10ee)
</dt> <dt>



Unerwarteter auf-Medium-Bezeichner.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_DELETE_LAST_ITEM"></span><span id="error_cant_delete_last_item"></span>**Fehler \_ \_ beim Löschen des \_ letzten \_ Elements.**
</dt> <dd> <dl> <dt>

4335 (0x10ef)
</dt> <dt>



Das letzte verbleibende Element in dieser Gruppe oder Ressource kann nicht gelöscht werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_MESSAGE_EXCEEDS_MAX_SIZE"></span><span id="error_message_exceeds_max_size"></span>**die Fehler \_ Meldung über \_ schreitet die \_ Maximale \_ Größe**
</dt> <dd> <dl> <dt>

4336 (0x10f 0)
</dt> <dt>



Die angegebene Meldung überschreitet die maximal zulässige Größe für diesen Parameter.


</dt> </dl> </dd> <dt>

<span id="ERROR_VOLUME_CONTAINS_SYS_FILES"></span><span id="error_volume_contains_sys_files"></span>**Fehler \_ Volume \_ enthält \_ sys- \_ Dateien**
</dt> <dd> <dl> <dt>

4337 (0x10f)
</dt> <dt>



Das Volume enthält System-oder Auslagerungs Dateien.


</dt> </dl> </dd> <dt>

<span id="ERROR_INDIGENOUS_TYPE"></span><span id="error_indigenous_type"></span>**\_Typ des indigenen Fehlers \_**
</dt> <dd> <dl> <dt>

4338 (0x10f 2)
</dt> <dt>



Der Medientyp kann nicht aus dieser Bibliothek entfernt werden, da mindestens ein Laufwerk in der Bibliothek meldet, dass dieser Medientyp unterstützt werden kann.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUPPORTING_DRIVES"></span><span id="error_no_supporting_drives"></span>**Fehler \_ beim \_ unterstützen von \_ Laufwerken**
</dt> <dd> <dl> <dt>

4339 (0x10f)
</dt> <dt>



Diese Offline Medien können nicht auf diesem System bereitgestellt werden, da keine aktivierten Laufwerke vorhanden sind, die verwendet werden können.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLEANER_CARTRIDGE_INSTALLED"></span><span id="error_cleaner_cartridge_installed"></span>**Fehler \_ Reinigungs- \_ Cartridge \_ installiert**
</dt> <dd> <dl> <dt>

4340 (0x10f)
</dt> <dt>



In der Band Bibliothek ist eine Reinigungs Bare Cartridge vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_IEPORT_FULL"></span><span id="error_ieport_full"></span>**Fehler- \_ ieport \_ voll**
</dt> <dd> <dl> <dt>

4341 (0x10f)
</dt> <dt>



Der einschleusen-/Ausgabeport kann nicht verwendet werden, da er nicht leer ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_OFFLINE"></span><span id="error_file_offline"></span>**Fehler \_ Datei \_ Offline**
</dt> <dd> <dl> <dt>

4350 (0x10fe)
</dt> <dt>



Diese Datei ist zurzeit nicht für die Verwendung auf diesem Computer verfügbar.


</dt> </dl> </dd> <dt>

<span id="ERROR_REMOTE_STORAGE_NOT_ACTIVE"></span><span id="error_remote_storage_not_active"></span>**Fehler beim \_ Remote \_ Speicher ist \_ nicht \_ aktiv.**
</dt> <dd> <dl> <dt>

4351 (0x10ff)
</dt> <dt>



Der Remote Speicherdienst ist zurzeit nicht funktionsfähig.


</dt> </dl> </dd> <dt>

<span id="ERROR_REMOTE_STORAGE_MEDIA_ERROR"></span><span id="error_remote_storage_media_error"></span>**Fehler beim \_ Remote \_ Speicher \_ Medium \_ .**
</dt> <dd> <dl> <dt>

4352 (0x1100)
</dt> <dt>



Der Remote Speicherdienst hat einen Medien Fehler gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_A_REPARSE_POINT"></span><span id="error_not_a_reparse_point"></span>**Fehler, \_ kein Analyse \_ \_ \_ Punkt**
</dt> <dd> <dl> <dt>

4390 (0x1126)
</dt> <dt>



Die Datei oder das Verzeichnis ist kein Analyse Punkt.


</dt> </dl> </dd> <dt>

<span id="ERROR_REPARSE_ATTRIBUTE_CONFLICT"></span><span id="error_reparse_attribute_conflict"></span>**Fehleranalyse \_ \_ Attribut \_ Konflikt**
</dt> <dd> <dl> <dt>

4391 (0x1127)
</dt> <dt>



Das Attribut für den Analyse Punkt kann nicht festgelegt werden, da es mit einem vorhandenen Attribut in Konflikt steht.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_REPARSE_DATA"></span><span id="error_invalid_reparse_data"></span>**Fehler beim Analysieren von \_ \_ \_ Daten.**
</dt> <dd> <dl> <dt>

4392 (0x1128)
</dt> <dt>



Die im Analyse Punkt Puffer vorhandenen Daten sind ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_REPARSE_TAG_INVALID"></span><span id="error_reparse_tag_invalid"></span>**Fehleranalyse- \_ \_ Tag ist \_ ungültig.**
</dt> <dd> <dl> <dt>

4393 (0x1129)
</dt> <dt>



Das im Analyse Punkt Puffer vorhandene Tag ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_REPARSE_TAG_MISMATCH"></span><span id="error_reparse_tag_mismatch"></span>**Fehler beim Analysieren der \_ \_ tagnicht \_ Übereinstimmung.**
</dt> <dd> <dl> <dt>

4394 (0x112a)
</dt> <dt>



Es gibt einen Konflikt zwischen dem in der Anforderung angegebenen Tag und dem Tag, das im Analyse Punkt vorhanden ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_APP_DATA_NOT_FOUND"></span><span id="error_app_data_not_found"></span>**Fehler- \_ App- \_ Daten \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

4400 (0x1130)
</dt> <dt>



Es wurden keine schnellen Cache Daten gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_APP_DATA_EXPIRED"></span><span id="error_app_data_expired"></span>**Fehler- \_ App- \_ Daten \_ abgelaufen**
</dt> <dd> <dl> <dt>

4401 (0x1131)
</dt> <dt>



Schnelle Cache Daten sind abgelaufen.


</dt> </dl> </dd> <dt>

<span id="ERROR_APP_DATA_CORRUPT"></span><span id="error_app_data_corrupt"></span>**Fehler- \_ App- \_ Daten \_ beschädigt**
</dt> <dd> <dl> <dt>

4402 (0x1132)
</dt> <dt>



Schnelle Cache Daten sind beschädigt.


</dt> </dl> </dd> <dt>

<span id="ERROR_APP_DATA_LIMIT_EXCEEDED"></span><span id="error_app_data_limit_exceeded"></span>**Fehler bei \_ App- \_ Daten \_ Limit \_ überschritten**
</dt> <dd> <dl> <dt>

4403 (0x1133)
</dt> <dt>



Schnelle Cache Daten haben die maximale Größe überschritten und können nicht aktualisiert werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_APP_DATA_REBOOT_REQUIRED"></span><span id="error_app_data_reboot_required"></span>**Fehler bei \_ App- \_ Daten \_ Neustart \_ erforderlich**
</dt> <dd> <dl> <dt>

4404 (0x1134)
</dt> <dt>



Der schnelle Cache wurde zurückgesetzt und erfordert einen Neustart, bis er aktualisiert werden kann.


</dt> </dl> </dd> <dt>

<span id="ERROR_SECUREBOOT_ROLLBACK_DETECTED"></span><span id="error_secureboot_rollback_detected"></span>**Fehler \_ secureboot- \_ Rollback \_ erkannt**
</dt> <dd> <dl> <dt>

4420 (0x1144)
</dt> <dt>



Der sichere Start hat festgestellt, dass ein Rollback geschützter Daten versucht wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_SECUREBOOT_POLICY_VIOLATION"></span><span id="error_secureboot_policy_violation"></span>**Fehler beim \_ secureboot- \_ Richtlinien \_ Verstoß.**
</dt> <dd> <dl> <dt>

4421 (0x1145)
</dt> <dt>



Der Wert wird durch eine Richtlinie für den sicheren Start geschützt und kann nicht geändert oder gelöscht werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_SECUREBOOT_INVALID_POLICY"></span><span id="error_secureboot_invalid_policy"></span>**Fehlermeldung \_ secureboot \_ ungültige \_ Richtlinie**
</dt> <dd> <dl> <dt>

4422 (0x1146)
</dt> <dt>



Die Richtlinie für den sicheren Start ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_SECUREBOOT_POLICY_PUBLISHER_NOT_FOUND"></span><span id="error_secureboot_policy_publisher_not_found"></span>**Fehler \_ secureboot- \_ Richtlinien- \_ Verleger \_ nicht \_ gefunden**
</dt> <dd> <dl> <dt>

4423 (0x1147)
</dt> <dt>



Eine neue Richtlinie für den sicheren Start enthielt nicht den aktuellen Verleger in der Update Liste.


</dt> </dl> </dd> <dt>

<span id="ERROR_SECUREBOOT_POLICY_NOT_SIGNED"></span><span id="error_secureboot_policy_not_signed"></span>**Fehler \_ secureboot- \_ Richtlinie \_ nicht \_ signiert**
</dt> <dd> <dl> <dt>

4424 (0x1148)
</dt> <dt>



Die Richtlinie für den sicheren Start ist entweder nicht signiert oder wird von einem nicht vertrauenswürdigen Signatur Geber signiert.


</dt> </dl> </dd> <dt>

<span id="ERROR_SECUREBOOT_NOT_ENABLED"></span><span id="error_secureboot_not_enabled"></span>**Fehler \_ secureboot ist \_ nicht \_ aktiviert.**
</dt> <dd> <dl> <dt>

4425 (0x1149)
</dt> <dt>



Der sichere Start ist auf diesem Computer nicht aktiviert.


</dt> </dl> </dd> <dt>

<span id="ERROR_SECUREBOOT_FILE_REPLACED"></span><span id="error_secureboot_file_replaced"></span>**Fehler \_ secureboot- \_ Datei wurde \_ ersetzt**
</dt> <dd> <dl> <dt>

4426 (0x114 a)
</dt> <dt>



Der sichere Start erfordert, dass bestimmte Dateien und Treiber nicht durch andere Dateien oder Treiber ersetzt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_OFFLOAD_READ_FLT_NOT_SUPPORTED"></span><span id="error_offload_read_flt_not_supported"></span>**Fehler beim \_ \_ auslagern, lesen, \_ \_ nicht \_ unterstützt.**
</dt> <dd> <dl> <dt>

4440 (0x1158)
</dt> <dt>



Der Lesevorgang zum Kopieren auslagern wird von einem Filter nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_OFFLOAD_WRITE_FLT_NOT_SUPPORTED"></span><span id="error_offload_write_flt_not_supported"></span>**Fehler beim auslagern, \_ \_ \_ \_ nicht \_ unterstützt.**
</dt> <dd> <dl> <dt>

4441 (0x1159)
</dt> <dt>



Der Kopiervorgang zum Kopieren auslagern wird von einem Filter nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_OFFLOAD_READ_FILE_NOT_SUPPORTED"></span><span id="error_offload_read_file_not_supported"></span>**Fehler beim \_ \_ Auslagern der Lese \_ Datei \_ nicht \_ unterstützt.**
</dt> <dd> <dl> <dt>

4442 (0x115a)
</dt> <dt>



Der Lesevorgang zum Kopieren auslagern wird für die Datei nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_OFFLOAD_WRITE_FILE_NOT_SUPPORTED"></span><span id="error_offload_write_file_not_supported"></span>**Fehler beim auslagern der \_ \_ Schreib \_ Datei \_ \_ wird nicht unterstützt.**
</dt> <dd> <dl> <dt>

4443 (0x115b)
</dt> <dt>



Der Kopiervorgang zum Kopieren auslagern wird für die Datei nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_VOLUME_NOT_SIS_ENABLED"></span><span id="error_volume_not_sis_enabled"></span>**Fehler \_ Volume \_ nicht \_ SIS \_ aktiviert**
</dt> <dd> <dl> <dt>

4500 (0x1194)
</dt> <dt>



Der Einzelinstanzspeicher ist auf diesem Volume nicht verfügbar.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEPENDENT_RESOURCE_EXISTS"></span><span id="error_dependent_resource_exists"></span>**Fehler \_ abhängige \_ Ressource ist \_ vorhanden.**
</dt> <dd> <dl> <dt>

5001 (0x1389)
</dt> <dt>



Der Vorgang kann nicht abgeschlossen werden, da andere Ressourcen von dieser Ressource abhängig sind.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEPENDENCY_NOT_FOUND"></span><span id="error_dependency_not_found"></span>**Fehler \_ Abhängigkeit wurde \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

5002 (0x138a)
</dt> <dt>



Die Abhängigkeit der Cluster Ressource wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEPENDENCY_ALREADY_EXISTS"></span><span id="error_dependency_already_exists"></span>**die Fehler \_ Abhängigkeit ist \_ bereits \_ vorhanden.**
</dt> <dd> <dl> <dt>

5003 (0x138b)
</dt> <dt>



Die Cluster Ressource kann nicht von der angegebenen Ressource abhängig gemacht werden, da Sie bereits abhängig ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_NOT_ONLINE"></span><span id="error_resource_not_online"></span>**Fehler \_ Ressource \_ nicht \_ Online**
</dt> <dd> <dl> <dt>

5004 (0x138c)
</dt> <dt>



Die Cluster Ressource ist nicht online.


</dt> </dl> </dd> <dt>

<span id="ERROR_HOST_NODE_NOT_AVAILABLE"></span><span id="error_host_node_not_available"></span>**der Fehler \_ Host \_ Knoten ist \_ nicht \_ verfügbar.**
</dt> <dd> <dl> <dt>

5005 (0x138d)
</dt> <dt>



Für diesen Vorgang ist kein Cluster Knoten verfügbar.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_NOT_AVAILABLE"></span><span id="error_resource_not_available"></span>**Fehler \_ Ressource \_ nicht \_ verfügbar**
</dt> <dd> <dl> <dt>

5006 (0x138e)
</dt> <dt>



Die Cluster Ressource ist nicht verfügbar.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_NOT_FOUND"></span><span id="error_resource_not_found"></span>**Fehler \_ Ressource \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

5007 (0x138f)
</dt> <dt>



Die Cluster Ressource wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_SHUTDOWN_CLUSTER"></span><span id="error_shutdown_cluster"></span>**Fehler beim Beenden des \_ \_ Clusters**
</dt> <dd> <dl> <dt>

5008 (0x1390)
</dt> <dt>



Der Cluster wird heruntergefahren.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_EVICT_ACTIVE_NODE"></span><span id="error_cant_evict_active_node"></span>**Fehler beim Entfernen des \_ \_ \_ aktiven \_ Knotens.**
</dt> <dd> <dl> <dt>

5009 (0x1391)
</dt> <dt>



Ein Cluster Knoten kann nicht aus dem Cluster entfernt werden, es sei denn, der Knoten ist herunter oder der letzte Knoten.


</dt> </dl> </dd> <dt>

<span id="ERROR_OBJECT_ALREADY_EXISTS"></span><span id="error_object_already_exists"></span>**das Fehler \_ Objekt ist \_ bereits \_ vorhanden.**
</dt> <dd> <dl> <dt>

5010 (0x1392)
</dt> <dt>



Das Objekt ist bereits vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_OBJECT_IN_LIST"></span><span id="error_object_in_list"></span>**Fehler \_ Objekt \_ in \_ Liste**
</dt> <dd> <dl> <dt>

5011 (0x1393)
</dt> <dt>



Das Objekt ist bereits in der Liste enthalten.


</dt> </dl> </dd> <dt>

<span id="ERROR_GROUP_NOT_AVAILABLE"></span><span id="error_group_not_available"></span>**Fehler \_ Gruppe \_ nicht \_ verfügbar**
</dt> <dd> <dl> <dt>

5012 (0x1394)
</dt> <dt>



Die Clustergruppe ist für keine neuen Anforderungen verfügbar.


</dt> </dl> </dd> <dt>

<span id="ERROR_GROUP_NOT_FOUND"></span><span id="error_group_not_found"></span>**Fehler \_ Gruppe \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

5013 (0x1395)
</dt> <dt>



Die Clustergruppe konnte nicht gefunden werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_GROUP_NOT_ONLINE"></span><span id="error_group_not_online"></span>**die Fehler \_ Gruppe ist \_ nicht \_ Online.**
</dt> <dd> <dl> <dt>

5014 (0x1396)
</dt> <dt>



Der Vorgang konnte nicht abgeschlossen werden, da die Clustergruppe nicht online ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_HOST_NODE_NOT_RESOURCE_OWNER"></span><span id="error_host_node_not_resource_owner"></span>**Fehler \_ Host \_ Knoten \_ nicht \_ Ressourcen \_ Besitzer**
</dt> <dd> <dl> <dt>

5015 (0x1397)
</dt> <dt>



Der Vorgang ist fehlgeschlagen, da entweder der angegebene Cluster Knoten nicht der Besitzer der Ressource ist oder der Knoten kein möglicher Besitzer der Ressource ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_HOST_NODE_NOT_GROUP_OWNER"></span><span id="error_host_node_not_group_owner"></span>**Fehler \_ Host \_ Knoten, \_ nicht \_ Gruppen \_ Besitzer**
</dt> <dd> <dl> <dt>

5016 (0x1398)
</dt> <dt>



Der Vorgang ist fehlgeschlagen, da entweder der angegebene Clusterknoten nicht Besitzer der Gruppe ist, oder der Knoten kein möglicher Besitzer der Gruppe ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESMON_CREATE_FAILED"></span><span id="error_resmon_create_failed"></span>**Fehler \_ beim Erstellen des Fehlers. \_ \_**
</dt> <dd> <dl> <dt>

5017 (0x1399)
</dt> <dt>



Die Cluster Ressource konnte im angegebenen Ressourcen Monitor nicht erstellt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESMON_ONLINE_FAILED"></span><span id="error_resmon_online_failed"></span>**Fehler \_ bei der \_ Online Fehlermeldung. \_**
</dt> <dd> <dl> <dt>

5018 (0x139 a)
</dt> <dt>



Die Cluster Ressource konnte nicht vom Ressourcen Monitor online geschaltet werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_ONLINE"></span><span id="error_resource_online"></span>**Fehler \_ Ressource \_ Online**
</dt> <dd> <dl> <dt>

5019 (0x139 b)
</dt> <dt>



Der Vorgang konnte nicht abgeschlossen werden, da die Cluster Ressource online ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_QUORUM_RESOURCE"></span><span id="error_quorum_resource"></span>**Fehler \_ Quorum \_ Ressource**
</dt> <dd> <dl> <dt>

5020 (0x139 c)
</dt> <dt>



Die Cluster Ressource konnte nicht gelöscht oder offline geschaltet werden, da es sich um die Quorum Ressource handelt.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_QUORUM_CAPABLE"></span><span id="error_not_quorum_capable"></span>**Fehler \_ nicht \_ Quorum \_ fähig**
</dt> <dd> <dl> <dt>

5021 (0x139 d)
</dt> <dt>



Der Cluster konnte die angegebene Ressource nicht zu einer Quorum Ressource machen, da Sie keine Quorum Ressource sein kann.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_SHUTTING_DOWN"></span><span id="error_cluster_shutting_down"></span>**Fehler beim Herunterfahren des \_ Clusters \_ \_**
</dt> <dd> <dl> <dt>

5022 (0x139 e)
</dt> <dt>



Die Cluster Software wird heruntergefahren.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_STATE"></span><span id="error_invalid_state"></span>**Fehler bei \_ ungültigem \_ Status**
</dt> <dd> <dl> <dt>

5023 (0x139 f)
</dt> <dt>



Die Gruppe oder Ressource weist nicht den richtigen Status auf, um den angeforderten Vorgang auszuführen.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_PROPERTIES_STORED"></span><span id="error_resource_properties_stored"></span>**\_gespeicherte Fehler Ressourcen \_ Eigenschaften \_**
</dt> <dd> <dl> <dt>

5024 (0x13a0)
</dt> <dt>



Die Eigenschaften wurden gespeichert, aber nicht alle Änderungen werden wirksam, bis die Ressource das nächste Mal online geschaltet wird.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_QUORUM_CLASS"></span><span id="error_not_quorum_class"></span>**Fehler \_ nicht \_ Quorum \_ Klasse**
</dt> <dd> <dl> <dt>

5025 (0x13a1)
</dt> <dt>



Der Cluster konnte die angegebene Ressource nicht zu einer Quorum Ressource machen, da Sie nicht zu einer freigegebenen Speicher Klasse gehört.


</dt> </dl> </dd> <dt>

<span id="ERROR_CORE_RESOURCE"></span><span id="error_core_resource"></span>**Fehler \_ Kern \_ Ressource**
</dt> <dd> <dl> <dt>

5026 (0x13a2)
</dt> <dt>



Die Cluster Ressource konnte nicht gelöscht werden, da es sich um eine Kernressource handelt.


</dt> </dl> </dd> <dt>

<span id="ERROR_QUORUM_RESOURCE_ONLINE_FAILED"></span><span id="error_quorum_resource_online_failed"></span>**Fehler \_ Quorum \_ Ressource \_ Online \_**
</dt> <dd> <dl> <dt>

5027 (0x13a3)
</dt> <dt>



Die Quorum Ressource konnte nicht online geschaltet werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_QUORUMLOG_OPEN_FAILED"></span><span id="error_quorumlog_open_failed"></span>**Fehler beim \_ Öffnen von " \_ quortolog". \_**
</dt> <dd> <dl> <dt>

5028 (0x13a4)
</dt> <dt>



Das Quorum Protokoll konnte nicht erstellt oder bereitgestellt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTERLOG_CORRUPT"></span><span id="error_clusterlog_corrupt"></span>**Fehler \_ Cluster Protokoll \_ beschädigt**
</dt> <dd> <dl> <dt>

5029 (0x13a5)
</dt> <dt>



Das Cluster Protokoll ist beschädigt.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTERLOG_RECORD_EXCEEDS_MAXSIZE"></span><span id="error_clusterlog_record_exceeds_maxsize"></span>**Fehler \_ CLUSTERLOG- \_ Datensatz über \_ schreitet \_ MaxSize**
</dt> <dd> <dl> <dt>

5030 (0x13a6)
</dt> <dt>



Der Datensatz konnte nicht in das Cluster Protokoll geschrieben werden, da er die maximale Größe überschreitet.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTERLOG_EXCEEDS_MAXSIZE"></span><span id="error_clusterlog_exceeds_maxsize"></span>**Fehler \_ Cluster Protokoll über \_ schreitet \_ MaxSize**
</dt> <dd> <dl> <dt>

5031 (0x13a7)
</dt> <dt>



Das Cluster Protokoll überschreitet die maximale Größe.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTERLOG_CHKPOINT_NOT_FOUND"></span><span id="error_clusterlog_chkpoint_not_found"></span>**Fehler beim \_ CLUSTERLOG- \_ chkpoint \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

5032 (0x13a8)
</dt> <dt>



Es wurde kein Prüf Punktdaten Satz im Cluster Protokoll gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTERLOG_NOT_ENOUGH_SPACE"></span><span id="error_clusterlog_not_enough_space"></span>**Fehler beim \_ CLUSTERLOG \_ nicht \_ genügend \_ Speicherplatz.**
</dt> <dd> <dl> <dt>

5033 (0x13a9)
</dt> <dt>



Der mindestens erforderliche Speicherplatz für die Protokollierung ist nicht verfügbar.


</dt> </dl> </dd> <dt>

<span id="ERROR_QUORUM_OWNER_ALIVE"></span><span id="error_quorum_owner_alive"></span>**Fehler \_ Quorum \_ Besitzer \_ Alive**
</dt> <dd> <dl> <dt>

5034 (0x13aa)
</dt> <dt>



Der Cluster Knoten konnte die Quorum Ressource nicht steuern, da die Ressource im Besitz eines anderen aktiven Knotens ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_NETWORK_NOT_AVAILABLE"></span><span id="error_network_not_available"></span>**Fehler \_ Netzwerk \_ nicht \_ verfügbar**
</dt> <dd> <dl> <dt>

5035 (0x13ab)
</dt> <dt>



Ein Cluster Netzwerk ist für diesen Vorgang nicht verfügbar.


</dt> </dl> </dd> <dt>

<span id="ERROR_NODE_NOT_AVAILABLE"></span><span id="error_node_not_available"></span>**der Fehler \_ Knoten ist \_ nicht \_ verfügbar.**
</dt> <dd> <dl> <dt>

5036 (0x13ac)
</dt> <dt>



Für diesen Vorgang ist kein Cluster Knoten verfügbar.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALL_NODES_NOT_AVAILABLE"></span><span id="error_all_nodes_not_available"></span>**Fehler \_ alle \_ Knoten \_ nicht \_ verfügbar**
</dt> <dd> <dl> <dt>

5037 (0x13ad)
</dt> <dt>



Alle Cluster Knoten müssen ausgeführt werden, um diesen Vorgang auszuführen.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_FAILED"></span><span id="error_resource_failed"></span>**Fehler bei \_ Ressource. \_**
</dt> <dd> <dl> <dt>

5038 (0x13ae)
</dt> <dt>



Fehler in einer Clusterressource.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INVALID_NODE"></span><span id="error_cluster_invalid_node"></span>**\_ \_ Ungültiger Knoten beim Fehler Cluster. \_**
</dt> <dd> <dl> <dt>

5039 (0x13af)
</dt> <dt>



Der Cluster Knoten ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_EXISTS"></span><span id="error_cluster_node_exists"></span>**Fehler \_ Cluster \_ Knoten \_ vorhanden**
</dt> <dd> <dl> <dt>

5040 (0x13b0)
</dt> <dt>



Der Cluster Knoten ist bereits vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_JOIN_IN_PROGRESS"></span><span id="error_cluster_join_in_progress"></span>**Fehler \_ \_ beim Cluster \_ Beitritt \_ .**
</dt> <dd> <dl> <dt>

5041 (0x13b1)
</dt> <dt>



Ein Knoten wird gerade dem Cluster beitreten.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_NOT_FOUND"></span><span id="error_cluster_node_not_found"></span>**Fehler \_ Cluster \_ Knoten wurde \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

5042 (0x13b2)
</dt> <dt>



Der Cluster Knoten wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_LOCAL_NODE_NOT_FOUND"></span><span id="error_cluster_local_node_not_found"></span>**der \_ lokale Knoten des Fehler Clusters wurde \_ \_ \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

5043 (0x13b3)
</dt> <dt>



Die Informationen zum lokalen Cluster Knoten wurden nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NETWORK_EXISTS"></span><span id="error_cluster_network_exists"></span>**Fehler \_ Cluster \_ Netzwerk \_ vorhanden**
</dt> <dd> <dl> <dt>

5044 (0x13b4)
</dt> <dt>



Das Cluster Netzwerk ist bereits vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NETWORK_NOT_FOUND"></span><span id="error_cluster_network_not_found"></span>**Fehler \_ Cluster \_ Netzwerk \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

5045 (0x13b5)
</dt> <dt>



Das Cluster Netzwerk wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NETINTERFACE_EXISTS"></span><span id="error_cluster_netinterface_exists"></span>**Fehler \_ Cluster- \_ netinterface \_ vorhanden**
</dt> <dd> <dl> <dt>

5046 (0x13b6)
</dt> <dt>



Die Cluster Netzwerkschnittstelle ist bereits vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NETINTERFACE_NOT_FOUND"></span><span id="error_cluster_netinterface_not_found"></span>**Fehler \_ Cluster- \_ netinterface \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

5047 (0x13b7)
</dt> <dt>



Die Cluster Netzwerkschnittstelle wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INVALID_REQUEST"></span><span id="error_cluster_invalid_request"></span>**\_ \_ ungültige Anforderung für Fehler Cluster. \_**
</dt> <dd> <dl> <dt>

5048 (0x13b8)
</dt> <dt>



Die Cluster Anforderung ist für dieses Objekt ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INVALID_NETWORK_PROVIDER"></span><span id="error_cluster_invalid_network_provider"></span>**Fehler \_ Cluster bei \_ ungültigem \_ Netzwerk \_ Anbieter.**
</dt> <dd> <dl> <dt>

5049 (0x13b9)
</dt> <dt>



Der Cluster Netzwerkanbieter ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_DOWN"></span><span id="error_cluster_node_down"></span>**Fehler \_ Cluster \_ Knoten \_ nach unten**
</dt> <dd> <dl> <dt>

5050 (0x13ba)
</dt> <dt>



Der Cluster Knoten ist nicht mehr festgelegt.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_UNREACHABLE"></span><span id="error_cluster_node_unreachable"></span>**Fehler \_ Cluster \_ Knoten \_ nicht erreichbar**
</dt> <dd> <dl> <dt>

5051 (0x13bb)
</dt> <dt>



Der Cluster Knoten ist nicht erreichbar.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_NOT_MEMBER"></span><span id="error_cluster_node_not_member"></span>**Fehler \_ Cluster \_ Knoten ist \_ nicht \_ Mitglied**
</dt> <dd> <dl> <dt>

5052 (0x13bc)
</dt> <dt>



Der Cluster Knoten ist kein Mitglied des Clusters.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_JOIN_NOT_IN_PROGRESS"></span><span id="error_cluster_join_not_in_progress"></span>**Fehler \_ \_ beim Cluster \_ Beitritt \_ nicht \_ .**
</dt> <dd> <dl> <dt>

5053 (0x13bd)
</dt> <dt>



Ein clusterjoinvorgang wird nicht ausgeführt.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INVALID_NETWORK"></span><span id="error_cluster_invalid_network"></span>**\_ \_ Ungültiges Netzwerk für Fehler Cluster. \_**
</dt> <dd> <dl> <dt>

5054 (0x13be)
</dt> <dt>



Das Cluster Netzwerk ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_UP"></span><span id="error_cluster_node_up"></span>**Fehler \_ Cluster \_ Knoten \_ hoch**
</dt> <dd> <dl> <dt>

5056 (0x13c0)
</dt> <dt>



Der Cluster Knoten ist aktiv.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_IPADDR_IN_USE"></span><span id="error_cluster_ipaddr_in_use"></span>**Fehler \_ Cluster " \_ ipaddr" wird \_ \_ verwendet.**
</dt> <dd> <dl> <dt>

5057 (0x13c1)
</dt> <dt>



Die Cluster-IP-Adresse wird bereits verwendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_NOT_PAUSED"></span><span id="error_cluster_node_not_paused"></span>**Fehler \_ Cluster \_ Knoten wurde \_ nicht \_ angehalten.**
</dt> <dd> <dl> <dt>

5058 (0x13c2)
</dt> <dt>



Der Cluster Knoten wurde nicht angehalten.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NO_SECURITY_CONTEXT"></span><span id="error_cluster_no_security_context"></span>**Fehler \_ Cluster \_ ohne \_ Sicherheits \_ Kontext**
</dt> <dd> <dl> <dt>

5059 (0x13c3)
</dt> <dt>



Es ist kein Cluster Sicherheitskontext verfügbar.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NETWORK_NOT_INTERNAL"></span><span id="error_cluster_network_not_internal"></span>**Fehler \_ Cluster \_ Netzwerk \_ nicht \_ intern**
</dt> <dd> <dl> <dt>

5060 (0x13c4)
</dt> <dt>



Das Cluster Netzwerk ist nicht für die interne Cluster Kommunikation konfiguriert.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_ALREADY_UP"></span><span id="error_cluster_node_already_up"></span>**Fehler \_ Cluster \_ Knoten ist \_ bereits \_ vorhanden.**
</dt> <dd> <dl> <dt>

5061 (0x13c5)
</dt> <dt>



Der Cluster Knoten ist bereits aktiv.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_ALREADY_DOWN"></span><span id="error_cluster_node_already_down"></span>**Fehler \_ Cluster \_ Knoten ist \_ bereits \_ herunter**
</dt> <dd> <dl> <dt>

5062 (0x13c6)
</dt> <dt>



Der Cluster Knoten ist bereits herunter.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NETWORK_ALREADY_ONLINE"></span><span id="error_cluster_network_already_online"></span>**Fehler \_ Cluster \_ Netzwerk ist \_ bereits \_ Online.**
</dt> <dd> <dl> <dt>

5063 (0x13c7)
</dt> <dt>



Das Cluster Netzwerk ist bereits online.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NETWORK_ALREADY_OFFLINE"></span><span id="error_cluster_network_already_offline"></span>**Fehler \_ Cluster \_ Netzwerk ist \_ bereits \_ Offline.**
</dt> <dd> <dl> <dt>

5064 (0x13c8)
</dt> <dt>



Das Cluster Netzwerk ist bereits offline.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_ALREADY_MEMBER"></span><span id="error_cluster_node_already_member"></span>**Fehler \_ Cluster \_ Knoten ist \_ bereits \_ Mitglied**
</dt> <dd> <dl> <dt>

5065 (0x13c9)
</dt> <dt>



Der Cluster Knoten ist bereits Mitglied des Clusters.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_LAST_INTERNAL_NETWORK"></span><span id="error_cluster_last_internal_network"></span>**\_ \_ Letztes \_ internes \_ Netzwerk des Fehler Clusters**
</dt> <dd> <dl> <dt>

5066 (0x13ca)
</dt> <dt>



Das Cluster Netzwerk ist das einzige, das für die interne Cluster Kommunikation zwischen mindestens zwei aktiven Cluster Knoten konfiguriert ist. Die interne Kommunikationsfunktion kann nicht aus dem Netzwerk entfernt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NETWORK_HAS_DEPENDENTS"></span><span id="error_cluster_network_has_dependents"></span>**Fehler \_ Cluster \_ Netzwerk \_ hat \_ abhängige Elemente**
</dt> <dd> <dl> <dt>

5067 (0x13cb)
</dt> <dt>



Mindestens eine Cluster Ressource ist vom Netzwerk abhängig, um Dienste für Clients bereitzustellen. Die Client Zugriffs Funktion kann nicht aus dem Netzwerk entfernt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_OPERATION_ON_QUORUM"></span><span id="error_invalid_operation_on_quorum"></span>**Fehler \_ bei ungültigem \_ Vorgang \_ für \_ Quorum.**
</dt> <dd> <dl> <dt>

5068 (0x13cc)
</dt> <dt>



Dieser Vorgang kann für die Cluster Ressource nicht ausgeführt werden, da es sich um die Quorum Ressource handelt. Sie dürfen die Quorum Ressource nicht offline schalten oder die Liste möglicher Besitzer ändern.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEPENDENCY_NOT_ALLOWED"></span><span id="error_dependency_not_allowed"></span>**die Fehler \_ Abhängigkeit ist \_ nicht \_ zulässig.**
</dt> <dd> <dl> <dt>

5069 (0x13cd)
</dt> <dt>



Für die Cluster Quorum Ressource sind keine Abhängigkeiten zulässig.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_PAUSED"></span><span id="error_cluster_node_paused"></span>**Fehler \_ Cluster \_ Knoten \_ angehalten**
</dt> <dd> <dl> <dt>

5070 (0x13ce)
</dt> <dt>



Der Cluster Knoten wurde angehalten.


</dt> </dl> </dd> <dt>

<span id="ERROR_NODE_CANT_HOST_RESOURCE"></span><span id="error_node_cant_host_resource"></span>**Fehler \_ Knoten \_ , \_ Host \_ Ressource nicht**
</dt> <dd> <dl> <dt>

5071 (0x13cf)
</dt> <dt>



Die Cluster Ressource kann nicht online geschaltet werden. Der Besitzer Knoten kann diese Ressource nicht ausführen.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_NOT_READY"></span><span id="error_cluster_node_not_ready"></span>**Fehler \_ Cluster \_ Knoten ist \_ nicht \_ bereit**
</dt> <dd> <dl> <dt>

5072 (0x13d0)
</dt> <dt>



Der Cluster Knoten ist nicht bereit zum Ausführen des angeforderten Vorgangs.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_SHUTTING_DOWN"></span><span id="error_cluster_node_shutting_down"></span>**Fehler beim Herunterfahren des \_ Cluster \_ Knotens \_ \_**
</dt> <dd> <dl> <dt>

5073 (0x13d1)
</dt> <dt>



Der Cluster Knoten wird heruntergefahren.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_JOIN_ABORTED"></span><span id="error_cluster_join_aborted"></span>**Fehler beim Abbrechen des Cluster Joins. \_ \_ \_**
</dt> <dd> <dl> <dt>

5074 (0x13d2)
</dt> <dt>



Der clusterjoinvorgang wurde abgebrochen.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INCOMPATIBLE_VERSIONS"></span><span id="error_cluster_incompatible_versions"></span>**Fehler \_ Cluster- \_ inkompatible \_ Versionen**
</dt> <dd> <dl> <dt>

5075 (0x13d3)
</dt> <dt>



Fehler beim clusterjoinvorgang aufgrund nicht kompatibler Softwareversionen zwischen dem Verknüpfungs Knoten und seinem Sponsor.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_MAXNUM_OF_RESOURCES_EXCEEDED"></span><span id="error_cluster_maxnum_of_resources_exceeded"></span>**Fehler \_ Cluster- \_ maxnum \_ von \_ Ressourcen \_ überschritten**
</dt> <dd> <dl> <dt>

5076 (0x13d4)
</dt> <dt>



Diese Ressource kann nicht erstellt werden, da der Cluster das Limit für die Anzahl der zu überwachenden Ressourcen erreicht hat.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_SYSTEM_CONFIG_CHANGED"></span><span id="error_cluster_system_config_changed"></span>**Fehler beim \_ Ändern der Cluster \_ System \_ Konfiguration \_ .**
</dt> <dd> <dl> <dt>

5077 (0x13d5)
</dt> <dt>



Die Systemkonfiguration wurde während des clusterjoins oder-Formular Vorgangs geändert. Der Join-oder Form-Vorgang wurde abgebrochen.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCE_TYPE_NOT_FOUND"></span><span id="error_cluster_resource_type_not_found"></span>**Fehler \_ beim \_ Cluster \_ Ressourcentyp \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

5078 (0x13d6)
</dt> <dt>



Der angegebene Ressourcentyp wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESTYPE_NOT_SUPPORTED"></span><span id="error_cluster_restype_not_supported"></span>**Fehler \_ Cluster- \_ RESTYPE \_ \_ wird nicht unterstützt.**
</dt> <dd> <dl> <dt>

5079 (0x13d7)
</dt> <dt>



Der angegebene Knoten unterstützt keine Ressource dieses Typs. Dies kann auf Versions Inkonsistenzen oder darauf zurückzuführen sein, dass die Ressourcen-DLL auf diesem Knoten fehlt.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESNAME_NOT_FOUND"></span><span id="error_cluster_resname_not_found"></span>**Fehler \_ Cluster- \_ Resname wurde \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

5080 (0x13d8)
</dt> <dt>



Der angegebene Ressourcen Name wird von dieser Ressourcen-DLL nicht unterstützt. Dies kann auf einen ungültigen (oder geänderten) Namen zurückzuführen sein, der für die Ressourcen-DLL angegeben wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NO_RPC_PACKAGES_REGISTERED"></span><span id="error_cluster_no_rpc_packages_registered"></span>**Fehler \_ Cluster \_ keine \_ RPC- \_ Pakete \_ registriert**
</dt> <dd> <dl> <dt>

5081 (0x13d9)
</dt> <dt>



Es konnte kein Authentifizierungs Paket beim RPC-Server registriert werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_OWNER_NOT_IN_PREFLIST"></span><span id="error_cluster_owner_not_in_preflist"></span>**\_ \_ der Besitzer des Fehler Clusters ist \_ nicht \_ im \_ voraus.**
</dt> <dd> <dl> <dt>

5082 (0x13da)
</dt> <dt>



Die Gruppe kann nicht online geschaltet werden, da der Besitzer der Gruppe nicht in der bevorzugten Liste für die Gruppe enthalten ist. Um den Besitzer Knoten für die Gruppe zu ändern, verschieben Sie die Gruppe.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_DATABASE_SEQMISMATCH"></span><span id="error_cluster_database_seqmismatch"></span>**Fehler bei \_ Cluster Datenbank, nicht \_ \_ übereinstimmende**
</dt> <dd> <dl> <dt>

5083 (0x13db)
</dt> <dt>



Der Joinvorgang ist fehlgeschlagen, weil die Sequenznummer der Cluster Datenbank geändert wurde oder mit dem Knoten locker nicht kompatibel ist. Dies kann während eines Verknüpfungs Vorgangs vorkommen, wenn die Cluster Datenbank während des Joins geändert wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESMON_INVALID_STATE"></span><span id="error_resmon_invalid_state"></span>**Fehler \_ beim resmon ( \_ ungültiger \_ Zustand)**
</dt> <dd> <dl> <dt>

5084 (0x13dc)
</dt> <dt>



Der Ressourcen Monitor lässt nicht zu, dass der Fail-Vorgang ausgeführt wird, während sich die Ressource in Ihrem aktuellen Zustand befindet. Dies kann vorkommen, wenn sich die Ressource im Status "Ausstehend" befindet.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_GUM_NOT_LOCKER"></span><span id="error_cluster_gum_not_locker"></span>**Fehler \_ Cluster- \_ Kaugummi \_ nicht \_ locker**
</dt> <dd> <dl> <dt>

5085 (0x13dd)
</dt> <dt>



Ein nicht locker-Code hat eine Anforderung zum Reservieren der Sperre für globale Updates erhalten.


</dt> </dl> </dd> <dt>

<span id="ERROR_QUORUM_DISK_NOT_FOUND"></span><span id="error_quorum_disk_not_found"></span>**Fehler Quorum Datenträger \_ \_ \_ nicht \_ gefunden**
</dt> <dd> <dl> <dt>

5086 (0x13de)
</dt> <dt>



Der Quorum Datenträger konnte vom Cluster Dienst nicht gefunden werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DATABASE_BACKUP_CORRUPT"></span><span id="error_database_backup_corrupt"></span>**Fehler \_ Daten Bank \_ Sicherung \_ beschädigt**
</dt> <dd> <dl> <dt>

5087 (0x13df)
</dt> <dt>



Die gesicherte Cluster Datenbank ist möglicherweise beschädigt.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_ALREADY_HAS_DFS_ROOT"></span><span id="error_cluster_node_already_has_dfs_root"></span>**Fehler \_ Cluster \_ Knoten \_ \_ weist bereits \_ DFS \_ -Stamm auf.**
</dt> <dd> <dl> <dt>

5088 (0x13e0)
</dt> <dt>



Ein DFS-Stamm ist bereits in diesem Cluster Knoten vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_PROPERTY_UNCHANGEABLE"></span><span id="error_resource_property_unchangeable"></span>**fehlerhafte \_ Ressourcen \_ Eigenschaft \_ nicht änderbar**
</dt> <dd> <dl> <dt>

5089 (0x13e1)
</dt> <dt>



Der Versuch, eine Ressourcen Eigenschaft zu ändern, ist fehlgeschlagen, da Sie einen Konflikt mit einer anderen vorhandenen Eigenschaft verursacht


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_MEMBERSHIP_INVALID_STATE"></span><span id="error_cluster_membership_invalid_state"></span>**\_ \_ \_ Ungültiger Status der Fehler Cluster Mitgliedschaft. \_**
</dt> <dd> <dl> <dt>

5890 (0x1702)
</dt> <dt>



Es wurde versucht, einen Vorgang auszuführen, der nicht mit dem aktuellen Mitgliedschaftsstatus des Knotens kompatibel ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_QUORUMLOG_NOT_FOUND"></span><span id="error_cluster_quorumlog_not_found"></span>**Fehler \_ Cluster- \_ quorumschlag \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

5891 (0x1703)
</dt> <dt>



Die Quorum Ressource enthält nicht das Quorum Protokoll.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_MEMBERSHIP_HALT"></span><span id="error_cluster_membership_halt"></span>**Fehler beim \_ Anhalten der Cluster \_ Mitgliedschaft \_**
</dt> <dd> <dl> <dt>

5892 (0x1704)
</dt> <dt>



Das Mitgliedschafts Modul hat das Herunterfahren des Cluster Dienstanbieter auf diesem Knoten angefordert.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INSTANCE_ID_MISMATCH"></span><span id="error_cluster_instance_id_mismatch"></span>**Fehler bei \_ Cluster \_ Instanz- \_ ID stimmen nicht \_ überein.**
</dt> <dd> <dl> <dt>

5893 (0x1705)
</dt> <dt>



Der Joinvorgang ist fehlgeschlagen, da die Clusterinstanz-ID des verknüpften Knotens nicht mit der Cluster Instanz-ID des Sponsor-Knotens identisch ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NETWORK_NOT_FOUND_FOR_IP"></span><span id="error_cluster_network_not_found_for_ip"></span>**Fehler \_ Cluster \_ Netzwerk \_ \_ \_ für IP nicht \_ gefunden**
</dt> <dd> <dl> <dt>

5894 (0x1706)
</dt> <dt>



Ein entsprechendes Cluster Netzwerk für die angegebene IP-Adresse wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_PROPERTY_DATA_TYPE_MISMATCH"></span><span id="error_cluster_property_data_type_mismatch"></span>**Fehler \_ beim \_ \_ \_ Datentyp der Cluster Eigenschaft. \_**
</dt> <dd> <dl> <dt>

5895 (0x1707)
</dt> <dt>



Der tatsächliche Datentyp der Eigenschaft entsprach nicht dem erwarteten Datentyp der Eigenschaft.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_EVICT_WITHOUT_CLEANUP"></span><span id="error_cluster_evict_without_cleanup"></span>**Fehler \_ Cluster entfernen \_ \_ ohne \_ Cleanup**
</dt> <dd> <dl> <dt>

5896 (0x1708)
</dt> <dt>



Der Cluster Knoten wurde erfolgreich aus dem Cluster entfernt, aber der Knoten wurde nicht bereinigt. Informationen zu den fehlerhaften Bereinigungs Schritten und zur Wiederherstellung finden Sie im Ereignisprotokoll für die Failoverclustering-Anwendung mit Ereignisanzeige.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_PARAMETER_MISMATCH"></span><span id="error_cluster_parameter_mismatch"></span>**Fehler \_ Cluster \_ Parameter \_ stimmen nicht überein.**
</dt> <dd> <dl> <dt>

5897 (0x1709)
</dt> <dt>



Mindestens zwei Parameterwerte, die für die Eigenschaften einer Ressource angegeben sind, sind in Konflikt.


</dt> </dl> </dd> <dt>

<span id="ERROR_NODE_CANNOT_BE_CLUSTERED"></span><span id="error_node_cannot_be_clustered"></span>**Fehler \_ Knoten \_ kann \_ nicht \_ gruppiert werden.**
</dt> <dd> <dl> <dt>

5898 (0x170a)
</dt> <dt>



Dieser Computer kann nicht Mitglied eines Clusters werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_WRONG_OS_VERSION"></span><span id="error_cluster_wrong_os_version"></span>**\_ \_ falsche \_ Betriebssystem \_ Version des Fehler Clusters**
</dt> <dd> <dl> <dt>

5899 (0x170b)
</dt> <dt>



Dieser Computer kann nicht Mitglied eines Clusters werden, da er nicht die richtige Version von Windows installiert hat.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_CANT_CREATE_DUP_CLUSTER_NAME"></span><span id="error_cluster_cant_create_dup_cluster_name"></span>**Fehler \_ Cluster Fehler beim \_ Erstellen des DUP- \_ \_ \_ Cluster \_ namens**
</dt> <dd> <dl> <dt>

5900 (0x170c)
</dt> <dt>



Ein Cluster kann nicht mit dem angegebenen Cluster Namen erstellt werden, da dieser Cluster Name bereits verwendet wird. Geben Sie einen anderen Namen für den Cluster an.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSCFG_ALREADY_COMMITTED"></span><span id="error_cluscfg_already_committed"></span>**Fehler beim \_ Cluscfg-Commit. \_ \_**
</dt> <dd> <dl> <dt>

5901 (0x170d)
</dt> <dt>



Für die Cluster Konfigurations Aktion wurde bereits ein Commit ausgeführt.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSCFG_ROLLBACK_FAILED"></span><span id="error_cluscfg_rollback_failed"></span>**Fehler beim \_ Cluscfg- \_ Rollback. \_**
</dt> <dd> <dl> <dt>

5902 (0x170e)
</dt> <dt>



Für die Cluster Konfigurations Aktion konnte kein Rollback ausgeführt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSCFG_SYSTEM_DISK_DRIVE_LETTER_CONFLICT"></span><span id="error_cluscfg_system_disk_drive_letter_conflict"></span>**Fehler beim \_ Cluscfg-System Laufwerks \_ \_ \_ \_ Buchstaben \_ .**
</dt> <dd> <dl> <dt>

5903 (0x170f)
</dt> <dt>



Der einem System Datenträger auf einem Knoten zugewiesene Laufwerk Buchstabe steht in Konflikt mit dem Laufwerk Buchstaben, der einem Datenträger auf einem anderen Knoten zugewiesen ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_OLD_VERSION"></span><span id="error_cluster_old_version"></span>**Fehler beim \_ Gruppieren der \_ alten \_ Version.**
</dt> <dd> <dl> <dt>

5904 (0x1710)
</dt> <dt>



Mindestens ein Knoten im Cluster führt eine Version von Windows aus, die diesen Vorgang nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_MISMATCHED_COMPUTER_ACCT_NAME"></span><span id="error_cluster_mismatched_computer_acct_name"></span>**Fehler \_ Cluster nicht \_ übereinstimmender \_ Computer \_ Acct- \_ Name**
</dt> <dd> <dl> <dt>

5905 (0x1711)
</dt> <dt>



Der Name des entsprechenden Computer Kontos stimmt nicht mit dem Netzwerknamen für diese Ressource überein.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NO_NET_ADAPTERS"></span><span id="error_cluster_no_net_adapters"></span>**Fehler \_ Cluster \_ ohne \_ Netzwerk \_ Adapter**
</dt> <dd> <dl> <dt>

5906 (0x1712)
</dt> <dt>



Es sind keine Netzwerkadapter verfügbar.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_POISONED"></span><span id="error_cluster_poisoned"></span>**Fehler \_ Cluster \_ vergiftet**
</dt> <dd> <dl> <dt>

5907 (0x1713)
</dt> <dt>



Der Cluster Knoten wurde vergiftet.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_GROUP_MOVING"></span><span id="error_cluster_group_moving"></span>**Verschieben von Fehler \_ Cluster \_ Gruppen \_**
</dt> <dd> <dl> <dt>

5908 (0x1714)
</dt> <dt>



Die Gruppe kann die Anforderung nicht akzeptieren, da Sie auf einen anderen Knoten verschoben wird.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCE_TYPE_BUSY"></span><span id="error_cluster_resource_type_busy"></span>**Fehler \_ Cluster \_ - \_ Ressourcentyp \_ ausgelastet**
</dt> <dd> <dl> <dt>

5909 (0x1715)
</dt> <dt>



Der Ressourcentyp kann die Anforderung nicht akzeptieren, da zu stark ausgelastet ist und einen anderen Vorgang ausführt.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_CALL_TIMED_OUT"></span><span id="error_resource_call_timed_out"></span>**\_Timeout beim \_ Ressourcen \_ Rückruf \_ .**
</dt> <dd> <dl> <dt>

5910 (0x1716)
</dt> <dt>



Timeout beim Abrufen der Cluster Ressourcen-DLL.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_CLUSTER_IPV6_ADDRESS"></span><span id="error_invalid_cluster_ipv6_address"></span>**Fehler \_ ungültige \_ Cluster- \_ IPv6- \_ Adresse**
</dt> <dd> <dl> <dt>

5911 (0x1717)
</dt> <dt>



Die Adresse ist für eine IPv6-Adress Ressource ungültig. Eine globale IPv6-Adresse ist erforderlich, und Sie muss mit einem Cluster Netzwerk identisch sein. Kompatibilitäts Adressen sind nicht zulässig.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INTERNAL_INVALID_FUNCTION"></span><span id="error_cluster_internal_invalid_function"></span>**Fehler bei der \_ internen Fehler Cluster \_ \_ \_ Funktion.**
</dt> <dd> <dl> <dt>

5912 (0x1718)
</dt> <dt>



Ein interner Cluster Fehler ist aufgetreten. Es wurde versucht, eine ungültige Funktion aufzurufen.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_PARAMETER_OUT_OF_BOUNDS"></span><span id="error_cluster_parameter_out_of_bounds"></span>**Fehler \_ Cluster \_ Parameter \_ außerhalb \_ des \_ gültigen Bereichs**
</dt> <dd> <dl> <dt>

5913 (0x1719)
</dt> <dt>



Ein Parameterwert liegt außerhalb des zulässigen Bereichs.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_PARTIAL_SEND"></span><span id="error_cluster_partial_send"></span>**Fehler \_ beim \_ partiellen Senden des Fehlers \_**
</dt> <dd> <dl> <dt>

5914 (0x171a)
</dt> <dt>



Beim Senden von Daten an einen anderen Knoten im Cluster ist ein Netzwerkfehler aufgetreten. Die Anzahl der übertragenen Bytes war kleiner als erforderlich.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_REGISTRY_INVALID_FUNCTION"></span><span id="error_cluster_registry_invalid_function"></span>**\_ \_ \_ Ungültige Funktion der Fehler Cluster Registrierung \_**
</dt> <dd> <dl> <dt>

5915 (0x171b)
</dt> <dt>



Es wurde versucht, einen ungültigen Cluster Registrierungsvorgang auszuführen.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INVALID_STRING_TERMINATION"></span><span id="error_cluster_invalid_string_termination"></span>**Fehler beim Beenden des Fehler \_ Clusters \_ \_ \_**
</dt> <dd> <dl> <dt>

5916 (0x171c)
</dt> <dt>



Eine Eingabe Zeichenfolge von Zeichen wird nicht ordnungsgemäß beendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INVALID_STRING_FORMAT"></span><span id="error_cluster_invalid_string_format"></span>**\_ \_ ungültiges \_ Zeichen folgen \_ Format für Fehler Cluster**
</dt> <dd> <dl> <dt>

5917 (0x171d)
</dt> <dt>



Eine Eingabe Zeichenfolge von Zeichen weist kein gültiges Format für die Daten auf, die Sie darstellt.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_DATABASE_TRANSACTION_IN_PROGRESS"></span><span id="error_cluster_database_transaction_in_progress"></span>**Fehler \_ Cluster- \_ Daten Bank \_ Transaktion \_ \_ wird ausgeführt.**
</dt> <dd> <dl> <dt>

5918 (0x171e)
</dt> <dt>



Ein interner Cluster Fehler ist aufgetreten. Es wurde versucht, eine Cluster Datenbanktransaktion auszuführen, während bereits eine Transaktion ausgeführt wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_DATABASE_TRANSACTION_NOT_IN_PROGRESS"></span><span id="error_cluster_database_transaction_not_in_progress"></span>**Fehler \_ Cluster- \_ Daten Bank \_ Transaktion wird \_ nicht \_ \_ ausgeführt**
</dt> <dd> <dl> <dt>

5919 (0x171f)
</dt> <dt>



Ein interner Cluster Fehler ist aufgetreten. Es wurde versucht, einen Commit für eine Cluster Datenbanktransaktion durchgeführt, während keine Transaktion durchgeführt wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NULL_DATA"></span><span id="error_cluster_null_data"></span>**Fehler beim \_ Cluster \_ NULL- \_ Daten**
</dt> <dd> <dl> <dt>

5920 (0x1720)
</dt> <dt>



Ein interner Cluster Fehler ist aufgetreten. Die Daten wurden nicht ordnungsgemäß initialisiert.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_PARTIAL_READ"></span><span id="error_cluster_partial_read"></span>**\_ \_ teilweises \_ Lesen des Fehler Clusters**
</dt> <dd> <dl> <dt>

5921 (0x1721)
</dt> <dt>



Fehler beim Lesen aus einem Datenstrom. Es wurde eine unerwartete Anzahl von Bytes zurückgegeben.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_PARTIAL_WRITE"></span><span id="error_cluster_partial_write"></span>**Fehler \_ beim \_ partiellen Schreiben des Clusters \_**
</dt> <dd> <dl> <dt>

5922 (0x1722)
</dt> <dt>



Fehler beim Schreiben in einen Datenstrom. Die erforderliche Anzahl von Bytes konnte nicht geschrieben werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_CANT_DESERIALIZE_DATA"></span><span id="error_cluster_cant_deserialize_data"></span>**Fehler \_ Cluster Fehler beim \_ \_ Deserialisieren von \_ Daten**
</dt> <dd> <dl> <dt>

5923 (0x1723)
</dt> <dt>



Fehler beim Deserialisieren eines Streams von Cluster Daten.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEPENDENT_RESOURCE_PROPERTY_CONFLICT"></span><span id="error_dependent_resource_property_conflict"></span>**Fehler \_ abhängiger \_ Ressourcen \_ Eigenschafts \_ Konflikt**
</dt> <dd> <dl> <dt>

5924 (0x1724)
</dt> <dt>



Mindestens ein Eigenschafts Wert für diese Ressource steht in Konflikt mit einem oder mehreren Eigenschafts Werten, die den abhängigen Ressourcen zugeordnet sind.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NO_QUORUM"></span><span id="error_cluster_no_quorum"></span>**Fehler \_ Cluster \_ ohne \_ Quorum**
</dt> <dd> <dl> <dt>

5925 (0x1725)
</dt> <dt>



Es war kein Quorum von Cluster Knoten vorhanden, um einen Cluster zu bilden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INVALID_IPV6_NETWORK"></span><span id="error_cluster_invalid_ipv6_network"></span>**\_ \_ Ungültiges \_ IPv6- \_ Netzwerk für Fehler Cluster**
</dt> <dd> <dl> <dt>

5926 (0x1726)
</dt> <dt>



Das Cluster Netzwerk ist für eine IPv6-Adress Ressource ungültig oder entspricht nicht der konfigurierten Adresse.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INVALID_IPV6_TUNNEL_NETWORK"></span><span id="error_cluster_invalid_ipv6_tunnel_network"></span>**Fehler \_ Cluster \_ ungültiges \_ IPv6- \_ Tunnel \_ Netzwerk**
</dt> <dd> <dl> <dt>

5927 (0x1727)
</dt> <dt>



Das Cluster Netzwerk ist für eine IPv6-Tunnel Ressource ungültig. Überprüfen Sie die Konfiguration der IP-Adress Ressource, von der die IPv6-Tunnel Ressource abhängig ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_QUORUM_NOT_ALLOWED_IN_THIS_GROUP"></span><span id="error_quorum_not_allowed_in_this_group"></span>**\_das Fehler Quorum ist \_ \_ \_ in \_ dieser \_ Gruppe nicht zulässig.**
</dt> <dd> <dl> <dt>

5928 (0x1728)
</dt> <dt>



Die Quorum Ressource darf sich nicht in der verfügbaren Speicher Gruppe befinden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEPENDENCY_TREE_TOO_COMPLEX"></span><span id="error_dependency_tree_too_complex"></span>**Fehler \_ Abhängigkeitsstruktur \_ \_ zu \_ Komplex**
</dt> <dd> <dl> <dt>

5929 (0x1729)
</dt> <dt>



Die Abhängigkeiten für diese Ressource sind zu tief geschachtelt.


</dt> </dl> </dd> <dt>

<span id="ERROR_EXCEPTION_IN_RESOURCE_CALL"></span><span id="error_exception_in_resource_call"></span>**Fehler \_ Ausnahme \_ beim \_ Ressourcen \_ Rückruf.**
</dt> <dd> <dl> <dt>

5930 (0x172 a)
</dt> <dt>



Beim Abrufen der Ressourcen-DLL wurde eine nicht behandelte Ausnahme ausgelöst.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RHS_FAILED_INITIALIZATION"></span><span id="error_cluster_rhs_failed_initialization"></span>**Fehler \_ Cluster- \_ RHS \_ konnte nicht \_ initialisiert werden**
</dt> <dd> <dl> <dt>

5931 (0x172 b)
</dt> <dt>



Der RHS-Prozess konnte nicht initialisiert werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NOT_INSTALLED"></span><span id="error_cluster_not_installed"></span>**Fehler \_ Cluster \_ nicht \_ installiert**
</dt> <dd> <dl> <dt>

5932 (0x172 c)
</dt> <dt>



Das Failoverclustering-Feature ist auf diesem Knoten nicht installiert.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCES_MUST_BE_ONLINE_ON_THE_SAME_NODE"></span><span id="error_cluster_resources_must_be_online_on_the_same_node"></span>**Fehler \_ Cluster \_ Ressourcen \_ müssen \_ \_ \_ auf \_ \_ demselben \_ Knoten online sein**
</dt> <dd> <dl> <dt>

5933 (0x172 d)
</dt> <dt>



Die Ressourcen müssen für diesen Vorgang auf dem gleichen Knoten online sein.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_MAX_NODES_IN_CLUSTER"></span><span id="error_cluster_max_nodes_in_cluster"></span>**\_Knoten "Max. Cluster Knoten" \_ \_ \_ im \_ Cluster**
</dt> <dd> <dl> <dt>

5934 (0x172 e)
</dt> <dt>



Ein neuer Knoten kann nicht hinzugefügt werden, da dieser Cluster bereits über die maximale Anzahl von Knoten verfügt.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_TOO_MANY_NODES"></span><span id="error_cluster_too_many_nodes"></span>**Fehler \_ Cluster \_ zu \_ viele \_ Knoten**
</dt> <dd> <dl> <dt>

5935 (0x172 f)
</dt> <dt>



Dieser Cluster kann nicht erstellt werden, da die angegebene Anzahl von Knoten die maximal zulässige Grenze überschreitet.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_OBJECT_ALREADY_USED"></span><span id="error_cluster_object_already_used"></span>**Fehler \_ Cluster \_ Objekt \_ bereits \_ verwendet**
</dt> <dd> <dl> <dt>

5936 (0x1730)
</dt> <dt>



Der Versuch, den angegebenen Cluster Namen zu verwenden, ist fehlgeschlagen, da ein aktiviertes Computer Objekt mit dem angegebenen Namen bereits in der Domäne vorhanden ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_NONCORE_GROUPS_FOUND"></span><span id="error_noncore_groups_found"></span>**Fehler \_ nicht-Kern \_ Gruppen \_ gefunden.**
</dt> <dd> <dl> <dt>

5937 (0x1731)
</dt> <dt>



Dieser Cluster kann nicht zerstört werden. Sie verfügt über nicht-Kern Anwendungs Gruppen, die gelöscht werden müssen, bevor der Cluster zerstört werden kann.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_SHARE_RESOURCE_CONFLICT"></span><span id="error_file_share_resource_conflict"></span>**Fehler \_ Datei \_ Freigabe- \_ Ressourcen \_ Konflikt**
</dt> <dd> <dl> <dt>

5938 (0x1732)
</dt> <dt>



Die Dateifreigabe, die der Dateifreigabe Zeugen-Ressource zugeordnet ist, kann nicht von diesem Cluster oder einem ihrer Knoten gehostet werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_EVICT_INVALID_REQUEST"></span><span id="error_cluster_evict_invalid_request"></span>**Fehler beim Entfernen einer \_ \_ \_ ungültigen \_ Anforderung durch den Cluster**
</dt> <dd> <dl> <dt>

5939 (0x1733)
</dt> <dt>



Das Entfernen dieses Knotens ist zu diesem Zeitpunkt ungültig. Aufgrund der Quorum Anforderungen führt das Entfernen des Knotens zum Herunterfahren des Clusters. Wenn es sich um den letzten Knoten im Cluster handelt, sollte der Befehl zum Löschen des Clusters verwendet werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_SINGLETON_RESOURCE"></span><span id="error_cluster_singleton_resource"></span>**Fehler \_ Cluster- \_ Singleton- \_ Ressource**
</dt> <dd> <dl> <dt>

5940 (0x1734)
</dt> <dt>



Im Cluster ist nur eine Instanz dieses Ressourcentyps zulässig.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_GROUP_SINGLETON_RESOURCE"></span><span id="error_cluster_group_singleton_resource"></span>**\_ \_ \_ Singleton- \_ Ressource für Fehler Cluster Gruppe**
</dt> <dd> <dl> <dt>

5941 (0x1735)
</dt> <dt>



Pro Ressourcengruppe ist nur eine Instanz dieses Ressourcentyps zulässig.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCE_PROVIDER_FAILED"></span><span id="error_cluster_resource_provider_failed"></span>**Fehler beim \_ Cluster \_ Ressourcen \_ Anbieter \_ .**
</dt> <dd> <dl> <dt>

5942 (0x1736)
</dt> <dt>



Die Ressource konnte aufgrund eines Fehlers bei mindestens einer Anbieter Ressource nicht online geschaltet werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCE_CONFIGURATION_ERROR"></span><span id="error_cluster_resource_configuration_error"></span>**Fehler bei der \_ Konfiguration der Cluster \_ Ressource. \_ \_**
</dt> <dd> <dl> <dt>

5943 (0x1737)
</dt> <dt>



Die Ressource hat angegeben, dass Sie auf keinem Knoten online geschaltet werden kann.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_GROUP_BUSY"></span><span id="error_cluster_group_busy"></span>**Fehler \_ Cluster \_ Gruppe \_ ausgelastet**
</dt> <dd> <dl> <dt>

5944 (0x1738)
</dt> <dt>



Der aktuelle Vorgang kann für diese Gruppe zu diesem Zeitpunkt nicht ausgeführt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NOT_SHARED_VOLUME"></span><span id="error_cluster_not_shared_volume"></span>**Fehler \_ Cluster nicht frei gegebenes \_ \_ \_ Volume**
</dt> <dd> <dl> <dt>

5945 (0x1739)
</dt> <dt>



Das Verzeichnis oder die Datei befindet sich nicht auf einem freigegebenen Cluster Volume.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INVALID_SECURITY_DESCRIPTOR"></span><span id="error_cluster_invalid_security_descriptor"></span>**\_ \_ ungültiger \_ Sicherheits \_ Deskriptor für Fehler Cluster**
</dt> <dd> <dl> <dt>

5946 (0x173a)
</dt> <dt>



Die Sicherheits Beschreibung erfüllt die Anforderungen für einen Cluster nicht.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_SHARED_VOLUMES_IN_USE"></span><span id="error_cluster_shared_volumes_in_use"></span>**Fehler \_ frei \_ gegebene \_ Clustervolumes \_ in \_ Verwendung**
</dt> <dd> <dl> <dt>

5947 (0x173b)
</dt> <dt>



Im Cluster ist mindestens eine freigegebene Volumes-Ressource konfiguriert. Diese Ressourcen müssen in den verfügbaren Speicher verschoben werden, damit der Vorgang erfolgreich ausgeführt werden konnte.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_USE_SHARED_VOLUMES_API"></span><span id="error_cluster_use_shared_volumes_api"></span>**Fehler \_ Cluster \_ Verwenden der frei \_ gegebenen \_ Volumes- \_ API**
</dt> <dd> <dl> <dt>

5948 (0x173c)
</dt> <dt>



Diese Gruppe oder Ressource kann nicht direkt bearbeitet werden. Verwenden Sie APIs für freigegebene Volumes, um den gewünschten Vorgang auszuführen.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_BACKUP_IN_PROGRESS"></span><span id="error_cluster_backup_in_progress"></span>**Fehler \_ Cluster \_ Sicherung \_ wird \_ ausgeführt.**
</dt> <dd> <dl> <dt>

5949 (0x173d)
</dt> <dt>



Die Sicherungskopie wird gerade ausgeführt. Warten Sie auf den Abschluss der Sicherung, und wiederholen Sie dann den Vorgang.


</dt> </dl> </dd> <dt>

<span id="ERROR_NON_CSV_PATH"></span><span id="error_non_csv_path"></span>**Fehler bei \_ nicht- \_ CSV- \_ Pfad**
</dt> <dd> <dl> <dt>

5950 (0x173e)
</dt> <dt>



Der Pfad gehört nicht zu einem freigegebenen Cluster Volume.


</dt> </dl> </dd> <dt>

<span id="ERROR_CSV_VOLUME_NOT_LOCAL"></span><span id="error_csv_volume_not_local"></span>**Fehler beim \_ CSV- \_ Volume \_ nicht \_ lokal.**
</dt> <dd> <dl> <dt>

5951 (0x173f)
</dt> <dt>



Das freigegebene Cluster Volume ist nicht lokal auf diesem Knoten eingebunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_WATCHDOG_TERMINATING"></span><span id="error_cluster_watchdog_terminating"></span>**Fehler beim \_ Beenden des Cluster- \_ Watchdog \_**
</dt> <dd> <dl> <dt>

5952 (0x1740)
</dt> <dt>



Der Cluster Watchdog wird beendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCE_VETOED_MOVE_INCOMPATIBLE_NODES"></span><span id="error_cluster_resource_vetoed_move_incompatible_nodes"></span>**Fehler beim Verschieben von nicht \_ \_ \_ \_ \_ kompatiblen \_ Knoten durch Fehler Cluster Ressource**
</dt> <dd> <dl> <dt>

5953 (0x1741)
</dt> <dt>



Eine Ressource hat einen Wechsel zwischen zwei Knoten überprüft, da Sie nicht kompatibel sind.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INVALID_NODE_WEIGHT"></span><span id="error_cluster_invalid_node_weight"></span>**Fehler \_ Cluster mit \_ ungültiger \_ Knoten \_ Gewichtung**
</dt> <dd> <dl> <dt>

5954 (0x1742)
</dt> <dt>



Die Anforderung ist ungültig, weil die Knoten Gewichtung nicht geändert werden kann, während sich der Cluster im nur Datenträger-Quorum Modus befindet, oder weil das Ändern der Knoten Gewichtung gegen die Mindestanforderungen für das Cluster Quorum verstoßen würde.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCE_VETOED_CALL"></span><span id="error_cluster_resource_vetoed_call"></span>**Fehler bei der Überprüfung des Fehlers bei der \_ Cluster \_ Ressource. \_ \_**
</dt> <dd> <dl> <dt>

5955 (0x1743)
</dt> <dt>



Die Ressource hat den-Rückruf überprüft.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESMON_SYSTEM_RESOURCES_LACKING"></span><span id="error_resmon_system_resources_lacking"></span>**Fehler \_ beim resmon der \_ System \_ Ressourcen \_ .**
</dt> <dd> <dl> <dt>

5956 (0x1744)
</dt> <dt>



Die Ressource konnte nicht gestartet oder ausgeführt werden, da Sie nicht genügend Systemressourcen reservieren konnte.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCE_VETOED_MOVE_NOT_ENOUGH_RESOURCES_ON_DESTINATION"></span><span id="error_cluster_resource_vetoed_move_not_enough_resources_on_destination"></span>**Fehler \_ \_ \_ \_ \_ \_ \_ \_ bei der Überprüfung der Fehler Cluster Ressource auf dem \_ Ziel nicht genügend Ressourcen.**
</dt> <dd> <dl> <dt>

5957 (0x1745)
</dt> <dt>



Eine Ressource hat einen Wechsel zwischen zwei Knoten überprüft, weil das Ziel derzeit nicht über genügend Ressourcen verfügt, um den Vorgang abzuschließen.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCE_VETOED_MOVE_NOT_ENOUGH_RESOURCES_ON_SOURCE"></span><span id="error_cluster_resource_vetoed_move_not_enough_resources_on_source"></span>**Fehler \_ \_ \_ \_ \_ \_ \_ \_ bei der Überprüfung der Fehler Cluster Ressource für die \_ Quelle nicht genügend Ressourcen.**
</dt> <dd> <dl> <dt>

5958 (0x1746)
</dt> <dt>



Eine Ressource hat einen Wechsel zwischen zwei Knoten überprüft, da die Quelle derzeit nicht über genügend Ressourcen verfügt, um den Vorgang abzuschließen.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_GROUP_QUEUED"></span><span id="error_cluster_group_queued"></span>**Fehler \_ Cluster \_ Gruppe in \_ Warteschlange eingereiht**
</dt> <dd> <dl> <dt>

5959 (0x1747)
</dt> <dt>



Der angeforderte Vorgang kann nicht abgeschlossen werden, da die Gruppe für einen Vorgang in die Warteschlange eingereiht wird.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCE_LOCKED_STATUS"></span><span id="error_cluster_resource_locked_status"></span>**Fehler \_ beim \_ \_ gesperrten \_ Status der Cluster Ressource.**
</dt> <dd> <dl> <dt>

5960 (0x1748)
</dt> <dt>



Der angeforderte Vorgang kann nicht abgeschlossen werden, da eine Ressource den gesperrten Status aufweist.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_SHARED_VOLUME_FAILOVER_NOT_ALLOWED"></span><span id="error_cluster_shared_volume_failover_not_allowed"></span>**Failover für frei gegebenes \_ Cluster \_ \_ Volume \_ \_ nicht \_ zulässig**
</dt> <dd> <dl> <dt>

5961 (0x1749)
</dt> <dt>



Die Ressource kann nicht auf einen anderen Knoten verschoben werden, da ein frei gegebenes Cluster Volume den Vorgang überprüft hat.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_DRAIN_IN_PROGRESS"></span><span id="error_cluster_node_drain_in_progress"></span>**Fehler \_ \_ \_ \_ beim Entladen des Cluster Knotens. \_**
</dt> <dd> <dl> <dt>

5962 (0x174a)
</dt> <dt>



Ein Knoten Ausgleichs Vorgang wird bereits ausgeführt.

Dieser Wert wurde auch als **Fehler \_ Cluster \_ Knoten \_ - \_ Evakuierung \_ in** Bearbeitung bezeichnet.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_DISK_NOT_CONNECTED"></span><span id="error_cluster_disk_not_connected"></span>**Fehler Cluster Datenträger \_ \_ \_ nicht \_ verbunden**
</dt> <dd> <dl> <dt>

5963 (0x174b)
</dt> <dt>



Der Cluster Speicher ist nicht mit dem Knoten verbunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_NOT_CSV_CAPABLE"></span><span id="error_disk_not_csv_capable"></span>**Fehler Datenträger \_ \_ nicht \_ CSV- \_ fähig**
</dt> <dd> <dl> <dt>

5964 (0x174c)
</dt> <dt>



Der Datenträger ist nicht so konfiguriert, dass er mit CSV verwendet werden kann. CSV-Datenträger müssen über mindestens eine Partition verfügen, die mit NTFS formatiert ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_NOT_IN_AVAILABLE_STORAGE"></span><span id="error_resource_not_in_available_storage"></span>**Fehler \_ Ressource \_ nicht \_ im \_ verfügbaren \_ Speicher**
</dt> <dd> <dl> <dt>

5965 (0x174d)
</dt> <dt>



Die Ressource muss Teil der verfügbaren Speicher Gruppe sein, um diese Aktion abzuschließen.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_SHARED_VOLUME_REDIRECTED"></span><span id="error_cluster_shared_volume_redirected"></span>**fehlerfrei gegebenes \_ Cluster \_ \_ Volume \_ umgeleitet**
</dt> <dd> <dl> <dt>

5966 (0x174e)
</dt> <dt>



Fehler bei csvfs-Vorgang, weil sich das Volume im umgeleiteten Modus befindet.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_SHARED_VOLUME_NOT_REDIRECTED"></span><span id="error_cluster_shared_volume_not_redirected"></span>**fehlerfrei gegebenes \_ Cluster \_ \_ Volume \_ nicht \_ umgeleitet**
</dt> <dd> <dl> <dt>

5967 (0x174f)
</dt> <dt>



Fehler bei csvfs-Vorgang, weil sich das Volume nicht im umgeleiteten Modus befindet.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_CANNOT_RETURN_PROPERTIES"></span><span id="error_cluster_cannot_return_properties"></span>**Fehler \_ Cluster \_ kann \_ keine \_ Eigenschaften zurückgeben.**
</dt> <dd> <dl> <dt>

5968 (0x1750)
</dt> <dt>



Cluster Eigenschaften können zurzeit nicht zurückgegeben werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCE_CONTAINS_UNSUPPORTED_DIFF_AREA_FOR_SHARED_VOLUMES"></span><span id="error_cluster_resource_contains_unsupported_diff_area_for_shared_volumes"></span>**Fehler \_ Cluster \_ Ressource \_ enthält \_ nicht unterstützten Vergleichs \_ \_ Bereich \_ für frei \_ gegebene \_ Volumes**
</dt> <dd> <dl> <dt>

5969 (0x1751)
</dt> <dt>



Die geclusterte Datenträger Ressource enthält den Bereich für Software Momentaufnahme-Vergleiche, der für freigegebene Clustervolumes nicht unterstützt


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCE_IS_IN_MAINTENANCE_MODE"></span><span id="error_cluster_resource_is_in_maintenance_mode"></span>**Fehler \_ Cluster \_ Ressource \_ befindet sich \_ im \_ Wartungs \_ Modus**
</dt> <dd> <dl> <dt>

5970 (0x1752)
</dt> <dt>



Der Vorgang kann nicht abgeschlossen werden, da sich die Ressource im Wartungsmodus befindet.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_AFFINITY_CONFLICT"></span><span id="error_cluster_affinity_conflict"></span>**Fehler \_ Cluster- \_ Affinitäts \_ Konflikt**
</dt> <dd> <dl> <dt>

5971 (0x1753)
</dt> <dt>



Der Vorgang kann aufgrund von Cluster Affinitäts Konflikten nicht abgeschlossen werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCE_IS_REPLICA_VIRTUAL_MACHINE"></span><span id="error_cluster_resource_is_replica_virtual_machine"></span>**Fehler \_ Cluster \_ Ressource \_ ist \_ \_ virtuelle \_ Replikat Maschine**
</dt> <dd> <dl> <dt>

5972 (0x1754)
</dt> <dt>



Der Vorgang kann nicht abgeschlossen werden, da die Ressource ein virtueller Replikat Computer ist.


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

 

 




