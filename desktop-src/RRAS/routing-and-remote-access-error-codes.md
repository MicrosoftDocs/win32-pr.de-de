---
title: Fehler Codes für Routing und Remote Zugriff
description: Die folgenden Fehlercodes für die Routing-und RAS-API (RRAS) werden in "raserror. h" definiert.
ms.assetid: 1fa41438-7c93-4e9c-851c-652fba23da4f
topic_type:
- apiref
api_name:
- Routing and Remote Access Error Codes
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 15966d009f0690a1db24c21460da5b9e08a38347
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040289"
---
# <a name="routing-and-remote-access-error-codes"></a>Fehler Codes für Routing und Remote Zugriff

Die folgenden Fehlercodes für die Routing-und RAS-API (RRAS) werden in "raserror. h" definiert. Alle Fehlercodes werden in Windows 2000 oder höheren Versionen von Windows unterstützt, sofern nicht anders angegeben.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Rückgabecode/-wert</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="PENDING"></span><span id="pending"></span><dl> <dt><strong>Ausstehende</strong></dt> <dt>600</dt> </dl></td>
<td>Ein Vorgang steht aus.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_PORT_HANDLE"></span><span id="error_invalid_port_handle"></span><dl> <dt><strong>ERROR_INVALID_PORT_HANDLE</strong></dt> <dt>601</dt> </dl></td>
<td>Das angegebene Port Handle ist ungültig.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PORT_ALREADY_OPEN"></span><span id="error_port_already_open"></span><dl> <dt><strong>ERROR_PORT_ALREADY_OPEN</strong></dt> <dt>602</dt> </dl></td>
<td>Der angegebene Port ist bereits geöffnet.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_BUFFER_TOO_SMALL"></span><span id="error_buffer_too_small"></span><dl> <dt><strong>ERROR_BUFFER_TOO_SMALL</strong></dt> <dt>603</dt> </dl></td>
<td>Der angegebene Puffer ist zu klein.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_WRONG_INFO_SPECIFIED"></span><span id="error_wrong_info_specified"></span><dl> <dt><strong>ERROR_WRONG_INFO_SPECIFIED</strong></dt> <dt>604</dt> </dl></td>
<td>Die angegebenen Port Informationen sind falsch.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CANNOT_SET_PORT_INFO"></span><span id="error_cannot_set_port_info"></span><dl> <dt><strong>ERROR_CANNOT_SET_PORT_INFO</strong></dt> <dt>605</dt> </dl></td>
<td>Die angegebenen Port Informationen können nicht festgelegt werden.<br/>
<blockquote>
[!Note]<br />
Veraltet in Windows Vista und höheren Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PORT_NOT_CONNECTED"></span><span id="error_port_not_connected"></span><dl> <dt><strong>ERROR_PORT_NOT_CONNECTED</strong></dt> <dt>606</dt> </dl></td>
<td>Der angegebene Port ist nicht verbunden.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EVENT_INVALID"></span><span id="error_event_invalid"></span><dl> <dt><strong>ERROR_EVENT_INVALID</strong></dt> <dt>607</dt> </dl></td>
<td>Es wurde ein ungültiges Ereignis erkannt.<br/>
<blockquote>
[!Note]<br />
Veraltet in Windows Vista und höheren Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DEVICE_DOES_NOT_EXIST"></span><span id="error_device_does_not_exist"></span><dl> <dt><strong>ERROR_DEVICE_DOES_NOT_EXIST</strong></dt> <dt>608</dt> </dl></td>
<td>Das angegebene Gerät ist nicht vorhanden.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_DEVICETYPE_DOES_NOT_EXIST"></span><span id="error_devicetype_does_not_exist"></span><dl> <dt><strong>ERROR_DEVICETYPE_DOES_NOT_EXIST</strong></dt> <dt>609</dt> </dl></td>
<td>Der angegebene Gerätetyp ist nicht vorhanden.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_BUFFER_INVALID"></span><span id="error_buffer_invalid"></span><dl> <dt><strong>ERROR_BUFFER_INVALID</strong></dt> <dt>610</dt> </dl></td>
<td>Der angegebene Puffer ist ungültig.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_ROUTE_NOT_AVAILABLE"></span><span id="error_route_not_available"></span><dl> <dt><strong>ERROR_ROUTE_NOT_AVAILABLE</strong></dt> <dt>611</dt> </dl></td>
<td>Es wurde eine Route angegeben, die nicht verfügbar ist.<br/>
<blockquote>
[!Note]<br />
Veraltet in Windows Vista und höheren Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_ROUTE_NOT_ALLOCATED"></span><span id="error_route_not_allocated"></span><dl> <dt><strong>ERROR_ROUTE_NOT_ALLOCATED</strong></dt> <dt>612</dt> </dl></td>
<td>Die angegebene Route ist nicht zugeordnet.<br/></td>
</tr>
<tr class="even">
<td><span id="ERRERROR_INVALID_COMPRESSION_SPECIFIED"></span><span id="errerror_invalid_compression_specified"></span><dl> <dt><strong>ERRERROR_INVALID_COMPRESSION_SPECIFIED</strong></dt> <dt>613</dt> </dl></td>
<td>Die angegebene Komprimierung ist ungültig.<br/>
<blockquote>
[!Note]<br />
Veraltet in Windows Vista und höheren Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_OUT_OF_BUFFERS"></span><span id="error_out_of_buffers"></span><dl> <dt><strong>ERROR_OUT_OF_BUFFERS</strong></dt> <dt>614</dt> </dl></td>
<td>Es waren nicht genügend Puffer verfügbar.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PORT_NOT_FOUND_"></span><span id="error_port_not_found_"></span><dl> <dt> <strong>ERROR_PORT_NOT_FOUND</strong> </dt> <dt>615</dt> </dl></td>
<td>Der angegebene Port wurde nicht gefunden.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_ASYNC_REQUEST_PENDING"></span><span id="error_async_request_pending"></span><dl> <dt><strong>ERROR_ASYNC_REQUEST_PENDING</strong></dt> <dt>616</dt> </dl></td>
<td>Eine asynchrone Anforderung steht aus.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_ALREADY_DISCONNECTING"></span><span id="error_already_disconnecting"></span><dl> <dt><strong>ERROR_ALREADY_DISCONNECTING</strong></dt> <dt>617</dt> </dl></td>
<td>Der angegebene Port bzw. das angegebene Gerät trennt bereits die Verbindung.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PORT_NOT_OPEN"></span><span id="error_port_not_open"></span><dl> <dt><strong>ERROR_PORT_NOT_OPEN</strong></dt> <dt>618</dt> </dl></td>
<td>Der angegebene Anschluss ist nicht offen.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PORT_DISCONNECTED"></span><span id="error_port_disconnected"></span><dl> <dt><strong>ERROR_PORT_DISCONNECTED</strong></dt> <dt>619</dt> </dl></td>
<td>Der angegebene Port wird getrennt.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_ENDPOINTS"></span><span id="error_no_endpoints"></span><dl> <dt><strong>ERROR_NO_ENDPOINTS</strong></dt> <dt>620</dt> </dl></td>
<td>Es konnten keine Endpunkte bestimmt werden.<br/>
<blockquote>
[!Note]<br />
Veraltet in Windows Vista und höheren Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CANNOT_OPEN_PHONEBOOK"></span><span id="error_cannot_open_phonebook"></span><dl> <dt><strong>ERROR_CANNOT_OPEN_PHONEBOOK</strong></dt> <dt>621</dt> </dl></td>
<td>Die angegebene Telefonbuchdatei kann nicht geöffnet werden.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_CANNOT_LOAD_PHONEBOOK"></span><span id="error_cannot_load_phonebook"></span><dl> <dt><strong>ERROR_CANNOT_LOAD_PHONEBOOK</strong></dt> <dt>622</dt> </dl></td>
<td>Die angegebene Telefonbuchdatei kann nicht geladen werden.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CANNOT_FIND_PHONEBOOK_ENTRY"></span><span id="error_cannot_find_phonebook_entry"></span><dl> <dt><strong>ERROR_CANNOT_FIND_PHONEBOOK_ENTRY</strong></dt> <dt>623</dt> </dl></td>
<td>Der angegebene Telefonbucheintrag wurde nicht gefunden.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_CANNOT_WRITE_PHONEBOOK"></span><span id="error_cannot_write_phonebook"></span><dl> <dt><strong>ERROR_CANNOT_WRITE_PHONEBOOK</strong></dt> <dt>624</dt> </dl></td>
<td>In die angegebene Telefonbuchdatei kann nicht geschrieben werden.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CORRUPT_PHONEBOOK"></span><span id="error_corrupt_phonebook"></span><dl> <dt><strong>ERROR_CORRUPT_PHONEBOOK</strong></dt> <dt>625</dt> </dl></td>
<td>Die im angegebenen Telefonbuch gefundenen Informationen sind ungültig.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_CANNOT_LOAD_STRING"></span><span id="error_cannot_load_string"></span><dl> <dt><strong>ERROR_CANNOT_LOAD_STRING</strong></dt> <dt>626</dt> </dl></td>
<td>Eine Zeichenfolge konnte nicht geladen werden.<br/>
<blockquote>
[!Note]<br />
Veraltet in Windows Vista und höheren Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_KEY_NOT_FOUND"></span><span id="error_key_not_found"></span><dl> <dt><strong>ERROR_KEY_NOT_FOUND</strong></dt> <dt>627</dt> </dl></td>
<td>Der angegebene Schlüssel wurde nicht gefunden.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DISCONNECTION"></span><span id="error_disconnection"></span><dl> <dt><strong>ERROR_DISCONNECTION</strong></dt> <dt>628</dt> </dl></td>
<td>Der angegebene Port wurde getrennt.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_REMOTE_DISCONNECTION"></span><span id="error_remote_disconnection"></span><dl> <dt><strong>ERROR_REMOTE_DISCONNECTION</strong></dt> <dt>629</dt> </dl></td>
<td>Der angegebene Port wurde vom Remote Computer getrennt.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_HARDWARE_FAILURE"></span><span id="error_hardware_failure"></span><dl> <dt><strong>ERROR_HARDWARE_FAILURE</strong></dt> <dt>630</dt> </dl></td>
<td>Der angegebene Port wurde aufgrund eines Hardwarefehlers getrennt.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_USER_DISCONNECTION"></span><span id="error_user_disconnection"></span><dl> <dt><strong>ERROR_USER_DISCONNECTION</strong></dt> <dt>631</dt> </dl></td>
<td>Der angegebene Port wurde vom Benutzer getrennt.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INVALID_SIZE"></span><span id="error_invalid_size"></span><dl> <dt><strong>ERROR_INVALID_SIZE</strong></dt> <dt>632</dt> </dl></td>
<td>Falsche Struktur Größe.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PORT_NOT_AVAILABLE"></span><span id="error_port_not_available"></span><dl> <dt><strong>ERROR_PORT_NOT_AVAILABLE</strong></dt> <dt>633</dt> </dl></td>
<td>Der angegebene Port wird bereits verwendet oder ist nicht für Remote Zugriff-DFÜ konfiguriert.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_CANNOT_PROJECT_CLIENT"></span><span id="error_cannot_project_client"></span><dl> <dt><strong>ERROR_CANNOT_PROJECT_CLIENT</strong></dt> <dt>634</dt> </dl></td>
<td>Der Computer konnte nicht im Remote Netzwerk registriert werden.<br/>
<blockquote>
[!Note]<br />
Veraltet in Windows Vista und höheren Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_UNKNOWN"></span><span id="error_unknown"></span><dl> <dt><strong>ERROR_UNKNOWN</strong></dt> <dt>635</dt> </dl></td>
<td>Ein unbekannter Fehler ist aufgetreten.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_WRONG_DEVICE_ATTACHED"></span><span id="error_wrong_device_attached"></span><dl> <dt><strong>ERROR_WRONG_DEVICE_ATTACHED</strong></dt> <dt>636</dt> </dl></td>
<td>Das falsche Gerät ist an den angegebenen Port angefügt.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_BAD_STRING"></span><span id="error_bad_string"></span><dl> <dt><strong>ERROR_BAD_STRING</strong></dt> <dt>637</dt> </dl></td>
<td>Es wurde eine Zeichenfolge erkannt, die nicht konvertiert werden konnte.<br/>
<blockquote>
[!Note]<br />
Veraltet in Windows Vista und höheren Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_REQUEST_TIMEOUT"></span><span id="error_request_timeout"></span><dl> <dt><strong>ERROR_REQUEST_TIMEOUT</strong></dt> <dt>638</dt> </dl></td>
<td>Timeout für die Anforderung.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CANNOT_GET_LANA"></span><span id="error_cannot_get_lana"></span><dl> <dt><strong>ERROR_CANNOT_GET_LANA</strong></dt> <dt>639</dt> </dl></td>
<td>Es ist kein asynchrones Netzwerk verfügbar.<br/>
<blockquote>
[!Note]<br />
Veraltet in Windows Vista und höheren Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NETBIOS_ERROR"></span><span id="error_netbios_error"></span><dl> <dt><strong>ERROR_NETBIOS_ERROR</strong></dt> <dt>640</dt> </dl></td>
<td>Es ist ein Fehler im Zusammenhang mit NetBIOS aufgetreten.<br/>
<blockquote>
[!Note]<br />
Veraltet in Windows Vista und höheren Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SERVER_OUT_OF_RESOURCES"></span><span id="error_server_out_of_resources"></span><dl> <dt><strong>ERROR_SERVER_OUT_OF_RESOURCES</strong></dt> <dt>641</dt> </dl></td>
<td>der Server kann keine NetBIOS-Ressourcen zuordnen, die zur Unterstützung des Clients benötigt werden.<br/>
<blockquote>
[!Note]<br />
Veraltet in Windows Vista und höheren Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NAME_EXISTS_ON_NET"></span><span id="error_name_exists_on_net"></span><dl> <dt><strong>ERROR_NAME_EXISTS_ON_NET</strong></dt> <dt>642</dt> </dl></td>
<td>Einer der NetBIOS-Namen Ihres Computers ist bereits im Remote Netzwerk registriert.<br/>
<blockquote>
[!Note]<br />
Veraltet in Windows Vista und höheren Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SERVER_GENERAL_NET_FAILURE"></span><span id="error_server_general_net_failure"></span><dl> <dt><strong>ERROR_SERVER_GENERAL_NET_FAILURE</strong></dt> <dt>643</dt> </dl></td>
<td>Ein Netzwerkadapter auf dem Server ist fehlgeschlagen.<br/>
<blockquote>
[!Note]<br />
Veraltet in Windows Vista und höheren Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="WARNING_MSG_ALIAS_NOT_ADDED"></span><span id="warning_msg_alias_not_added"></span><dl> <dt><strong>WARNING_MSG_ALIAS_NOT_ADDED</strong></dt> <dt>644</dt> </dl></td>
<td>Sie erhalten keine netzwerknachrichtenpopups.<br/>
<blockquote>
[!Note]<br />
Veraltet in Windows Vista und höheren Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_AUTH_INTERNAL"></span><span id="error_auth_internal"></span><dl> <dt><strong>ERROR_AUTH_INTERNAL</strong></dt> <dt>645</dt> </dl></td>
<td>Ein interner Authentifizierungsfehler ist aufgetreten.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_RESTRICTED_LOGON_HOURS"></span><span id="error_restricted_logon_hours"></span><dl> <dt><strong>ERROR_RESTRICTED_LOGON_HOURS</strong></dt> <dt>646</dt> </dl></td>
<td>Das angegebene Konto darf sich zu diesem Zeitpunkt nicht anmelden.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_ACCT_DISABLED"></span><span id="error_acct_disabled"></span><dl> <dt><strong>ERROR_ACCT_DISABLED</strong></dt> <dt>647</dt> </dl></td>
<td>Das angegebene Konto ist deaktiviert.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PASSWD_EXPIRED"></span><span id="error_passwd_expired"></span><dl> <dt><strong>ERROR_PASSWD_EXPIRED</strong></dt> <dt>648</dt> </dl></td>
<td>Das angegebene Kennwort ist abgelaufen.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_DIALIN_PERMISSION"></span><span id="error_no_dialin_permission"></span><dl> <dt><strong>ERROR_NO_DIALIN_PERMISSION</strong></dt> <dt>649</dt> </dl></td>
<td>Das angegebene Konto verfügt nicht über Remote Zugriffsberechtigungen.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_SERVER_NOT_RESPONDING"></span><span id="error_server_not_responding"></span><dl> <dt><strong>ERROR_SERVER_NOT_RESPONDING</strong></dt> <dt>650</dt> </dl></td>
<td>Der Remote Zugriffs Server antwortet nicht.<br/>
<blockquote>
[!Note]<br />
Veraltet in Windows Vista und höheren Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_FROM_DEVICE"></span><span id="error_from_device"></span><dl> <dt><strong>ERROR_FROM_DEVICE</strong></dt> <dt>651</dt> </dl></td>
<td>Ihr Modem oder ein anderes Verbindungsgerät hat einen Fehler gemeldet.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_UNRECOGNIZED_RESPONSE"></span><span id="error_unrecognized_response"></span><dl> <dt><strong>ERROR_UNRECOGNIZED_RESPONSE</strong></dt> <dt>652</dt> </dl></td>
<td>Vom Gerät wurde eine nicht erkannte Antwort zurückgegeben.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_MACRO_NOT_FOUND"></span><span id="error_macro_not_found"></span><dl> <dt><strong>ERROR_MACRO_NOT_FOUND</strong></dt> <dt>653</dt> </dl></td>
<td>Ein für das Gerät erforderliches Makro wurde nicht auf dem Gerät gefunden. Abschnitt "INF-Datei".<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_MACRO_NOT_DEFINED"></span><span id="error_macro_not_defined"></span><dl> <dt><strong>ERROR_MACRO_NOT_DEFINED</strong></dt> <dt>654</dt> </dl></td>
<td>Ein Befehl oder eine Antwort im Gerät. Der Abschnitt der INF-Datei verweist auf ein nicht definiertes Makro.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_MESSAGE_MACRO_NOT_FOUND"></span><span id="error_message_macro_not_found"></span><dl> <dt><strong>ERROR_MESSAGE_MACRO_NOT_FOUND</strong></dt> <dt>655</dt> </dl></td>
<td>Das <message> Makro wurde nicht auf dem Gerät gefunden. Abschnitt "INF-Datei".<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DEFAULTOFF_MACRO_NOT_FOUND"></span><span id="error_defaultoff_macro_not_found"></span><dl> <dt><strong>ERROR_DEFAULTOFF_MACRO_NOT_FOUND</strong></dt> <dt>656</dt> </dl></td>
<td>Das <defaultoff> Makro im Gerät. Der Abschnitt der INF-Datei enthält ein nicht definiertes Makro.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_FILE_COULD_NOT_BE_OPENED"></span><span id="error_file_could_not_be_opened"></span><dl> <dt><strong>ERROR_FILE_COULD_NOT_BE_OPENED</strong></dt> <dt>657</dt> </dl></td>
<td>Das Gerät. Die INF-Datei konnte nicht geöffnet werden.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DEVICENAME_TOO_LONG"></span><span id="error_devicename_too_long"></span><dl> <dt><strong>ERROR_DEVICENAME_TOO_LONG</strong></dt> <dt>658</dt> </dl></td>
<td>Der Gerätename im Gerät. INF oder Medien. Die INI-Datei ist zu lang. <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_DEVICENAME_NOT_FOUND"></span><span id="error_devicename_not_found"></span><dl> <dt><strong>ERROR_DEVICENAME_NOT_FOUND</strong></dt> <dt>659</dt> </dl></td>
<td>Das Medium. Die INI-Datei verweist auf einen unbekannten Gerätenamen.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_RESPONSES"></span><span id="error_no_responses"></span><dl> <dt><strong>ERROR_NO_RESPONSES</strong></dt> <dt>660</dt> </dl></td>
<td>Das Gerät. Die INF-Datei enthält keine Antworten für den Befehl.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_COMMAND_FOUND"></span><span id="error_no_command_found"></span><dl> <dt><strong>ERROR_NO_COMMAND_FOUND</strong></dt> <dt>661</dt> </dl></td>
<td>Das Gerät. In der INF-Datei fehlt ein Befehl.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_WRONG_KEY_SPECIFIED"></span><span id="error_wrong_key_specified"></span><dl> <dt><strong>ERROR_WRONG_KEY_SPECIFIED</strong></dt> <dt>662</dt> </dl></td>
<td>Es wurde versucht, ein Makro festzulegen, das nicht im Gerät aufgeführt ist Abschnitt "INF-Datei".<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_UNKNOWN_DEVICE_TYPE"></span><span id="error_unknown_device_type"></span><dl> <dt><strong>ERROR_UNKNOWN_DEVICE_TYPE</strong></dt> <dt>663</dt> </dl></td>
<td>Das Medium. Die INI-Datei verweist auf einen unbekannten Gerätetyp.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_ALLOCATING_MEMORY"></span><span id="error_allocating_memory"></span><dl> <dt><strong>ERROR_ALLOCATING_MEMORY</strong></dt> <dt>664</dt> </dl></td>
<td>Arbeitsspeicher kann nicht belegt werden.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PORT_NOT_CONFIGURED"></span><span id="error_port_not_configured"></span><dl> <dt><strong>ERROR_PORT_NOT_CONFIGURED</strong></dt> <dt>665</dt> </dl></td>
<td>Der Port ist nicht für den Remote Zugriff konfiguriert.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DEVICE_NOT_READY"></span><span id="error_device_not_ready"></span><dl> <dt><strong>ERROR_DEVICE_NOT_READY</strong></dt> <dt>666</dt> </dl></td>
<td>Ihr Modem oder ein anderes Verbindungsgerät funktioniert nicht.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_READING_INI_FILE"></span><span id="error_reading_ini_file"></span><dl> <dt><strong>ERROR_READING_INI_FILE</strong></dt> <dt>667</dt> </dl></td>
<td>Das Medium kann nicht gelesen werden. INI-Datei.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_CONNECTION"></span><span id="error_no_connection"></span><dl> <dt><strong>ERROR_NO_CONNECTION</strong></dt> <dt>668</dt> </dl></td>
<td>Die Verbindung wurde getrennt.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_BAD_USAGE_IN_INI_FILE"></span><span id="error_bad_usage_in_ini_file"></span><dl> <dt><strong>ERROR_BAD_USAGE_IN_INI_FILE</strong></dt> <dt>669</dt> </dl></td>
<td>Der use-Parameter in der Datei "Media. ini" ist ungültig.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_READING_SECTIONNAME"></span><span id="error_reading_sectionname"></span><dl> <dt><strong>ERROR_READING_SECTIONNAME</strong></dt> <dt>670</dt> </dl></td>
<td>Der Abschnitts Name kann nicht vom Medium gelesen werden. INI-Datei.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_READING_DEVICETYPE"></span><span id="error_reading_devicetype"></span><dl> <dt><strong>ERROR_READING_DEVICETYPE</strong></dt> <dt>671</dt> </dl></td>
<td>Der Gerätetyp kann nicht vom Medium gelesen werden. INI-Datei.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_READING_DEVICENAME"></span><span id="error_reading_devicename"></span><dl> <dt><strong>ERROR_READING_DEVICENAME</strong></dt> <dt>672</dt> </dl></td>
<td>Der Gerätename kann nicht vom Medium gelesen werden. INI-Datei.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_READING_USAGE"></span><span id="error_reading_usage"></span><dl> <dt><strong>ERROR_READING_USAGE</strong></dt> <dt>673</dt> </dl></td>
<td>Die Verwendung des Mediums kann nicht gelesen werden. INI-Datei.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_READING_MAXCONNECTBPS"></span><span id="error_reading_maxconnectbps"></span><dl> <dt><strong>ERROR_READING_MAXCONNECTBPS</strong></dt> <dt>674</dt> </dl></td>
<td>Das System konnte die maximale trägerverbindungsgeschwindigkeit des Mediums nicht lesen. INI-Datei.<br/>
<blockquote>
[!Note]<br />
Veraltet in Windows Vista und höheren Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_READING_MAXCARRIERBPS"></span><span id="error_reading_maxcarrierbps"></span><dl> <dt><strong>ERROR_READING_MAXCARRIERBPS</strong></dt> <dt>675</dt> </dl></td>
<td>Die Verwendung des Mediums kann nicht gelesen werden. INI-Datei.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_LINE_BUSY"></span><span id="error_line_busy"></span><dl> <dt><strong>ERROR_LINE_BUSY</strong></dt> <dt>676</dt> </dl></td>
<td>Die Zeile ist ausgelastet.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_VOICE_ANSWER"></span><span id="error_voice_answer"></span><dl> <dt><strong>ERROR_VOICE_ANSWER</strong></dt> <dt>677</dt> </dl></td>
<td>Eine Person, die statt eines Modem geantwortet hat.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_ANSWER"></span><span id="error_no_answer"></span><dl> <dt><strong>ERROR_NO_ANSWER</strong></dt> <dt>678</dt> </dl></td>
<td>Es gibt keine Antwort.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_CARRIER"></span><span id="error_no_carrier"></span><dl> <dt><strong>ERROR_NO_CARRIER</strong></dt> <dt>679</dt> </dl></td>
<td>Ein Netzbetreiber Signal kann nicht erkannt werden.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_DIALTONE"></span><span id="error_no_dialtone"></span><dl> <dt><strong>ERROR_NO_DIALTONE</strong></dt> <dt>680</dt> </dl></td>
<td>Es ist kein Wählton vorhanden.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_IN_COMMAND"></span><span id="error_in_command"></span><dl> <dt><strong>ERROR_IN_COMMAND</strong></dt> <dt>681</dt> </dl></td>
<td>Das Modem (oder ein anderes Verbindungsgerät) hat einen allgemeinen Fehler gemeldet.<br/>
<blockquote>
[!Note]<br />
Veraltet in Windows Vista und höheren Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_WRITING_SECTIONNAME"></span><span id="error_writing_sectionname"></span><dl> <dt><strong>ERROR_WRITING_SECTIONNAME</strong></dt> <dt>682</dt> </dl></td>
<td>Beim Schreiben des Abschnitts namens ist ein Fehler aufgetreten.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_WRITING_DEVICETYPE"></span><span id="error_writing_devicetype"></span><dl> <dt><strong>ERROR_WRITING_DEVICETYPE</strong></dt> <dt>683</dt> </dl></td>
<td>Beim Schreiben des Gerätetyps ist ein Fehler aufgetreten.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_WRITING_DEVICENAME"></span><span id="error_writing_devicename"></span><dl> <dt><strong>ERROR_WRITING_DEVICENAME</strong></dt> <dt>684</dt> </dl></td>
<td>Beim Schreiben des Geräte namens ist ein Fehler aufgetreten.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_WRITING_MAXCONNECTBPS"></span><span id="error_writing_maxconnectbps"></span><dl> <dt><strong>ERROR_WRITING_MAXCONNECTBPS</strong></dt> <dt>685</dt> </dl></td>
<td>Fehler beim Schreiben der maximalen Verbindungsgeschwindigkeit.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_WRITING_MAXCARRIERBPS"></span><span id="error_writing_maxcarrierbps"></span><dl> <dt><strong>ERROR_WRITING_MAXCARRIERBPS</strong></dt> <dt>686</dt> </dl></td>
<td>Beim Schreiben der maximalen Transportgeschwindigkeit ist ein Fehler aufgetreten.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_WRITING_USAGE"></span><span id="error_writing_usage"></span><dl> <dt><strong>ERROR_WRITING_USAGE</strong></dt> <dt>687</dt> </dl></td>
<td>Fehler beim Schreiben der Verwendung.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_WRITING_DEFAULTOFF"></span><span id="error_writing_defaultoff"></span><dl> <dt><strong>ERROR_WRITING_DEFAULTOFF</strong></dt> <dt>688</dt> </dl></td>
<td>Beim Schreiben der Standardeinstellung ist ein Fehler aufgetreten.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_READING_DEFAULTOFF"></span><span id="error_reading_defaultoff"></span><dl> <dt><strong>ERROR_READING_DEFAULTOFF</strong></dt> <dt>689</dt> </dl></td>

</tr>
<tr class="odd">
<td><span id="ERROR_EMPTY_INI_FILE"></span><span id="error_empty_ini_file"></span><dl> <dt><strong>ERROR_EMPTY_INI_FILE</strong></dt> <dt>690</dt> </dl></td>
<td>Das Medium. Die INI-Datei ist leer.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_AUTHENTICATION_FAILURE"></span><span id="error_authentication_failure"></span><dl> <dt><strong>ERROR_AUTHENTICATION_FAILURE</strong></dt> <dt>691</dt> </dl></td>
<td>Der Zugriff wurde verweigert, da der Benutzername, das Kennwort oder beides in der Domäne nicht gültig ist.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PORT_OR_DEVICE"></span><span id="error_port_or_device"></span><dl> <dt><strong>ERROR_PORT_OR_DEVICE</strong></dt> <dt>692</dt> </dl></td>
<td>Ein Hardwarefehler ist am Port oder angehängtem Gerät aufgetreten.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NOT_BINARY_MACRO"></span><span id="error_not_binary_macro"></span><dl> <dt><strong>ERROR_NOT_BINARY_MACRO</strong></dt> <dt>693</dt> </dl></td>
<td>Das-Makro ist kein binäres Makro.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DCB_NOT_FOUND"></span><span id="error_dcb_not_found"></span><dl> <dt><strong>ERROR_DCB_NOT_FOUND</strong></dt> <dt>694</dt> </dl></td>
<td>DCB nicht gefunden.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_STATE_MACHINES_NOT_STARTED"></span><span id="error_state_machines_not_started"></span><dl> <dt><strong>ERROR_STATE_MACHINES_NOT_STARTED</strong></dt> <dt>695</dt> </dl></td>
<td>Zustands Automaten werden nicht gestartet.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_STATE_MACHINES_ALREADY_STARTED"></span><span id="error_state_machines_already_started"></span><dl> <dt><strong>ERROR_STATE_MACHINES_ALREADY_STARTED</strong></dt> <dt>696</dt> </dl></td>
<td>Zustands Automaten wurden bereits gestartet.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PARTIAL_RESPONSE_LOOPING"></span><span id="error_partial_response_looping"></span><dl> <dt><strong>ERROR_PARTIAL_RESPONSE_LOOPING</strong></dt> <dt>697</dt> </dl></td>
<td>Teilweise Antwort Schleife.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_UNKNOWN_RESPONSE_KEY"></span><span id="error_unknown_response_key"></span><dl> <dt><strong>ERROR_UNKNOWN_RESPONSE_KEY</strong></dt> <dt>698</dt> </dl></td>
<td>Ein Antwortschlüssel Name im Gerät. Die INF-Datei weist nicht das erwartete Format auf.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_RECV_BUF_FULL"></span><span id="error_recv_buf_full"></span><dl> <dt><strong>ERROR_RECV_BUF_FULL</strong></dt> <dt>699</dt> </dl></td>
<td>Die Geräte Antwort hat einen Pufferüberlauf verursacht.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_CMD_TOO_LONG"></span><span id="error_cmd_too_long"></span><dl> <dt><strong>ERROR_CMD_TOO_LONG</strong></dt> <dt>700</dt> </dl></td>
<td>Der erweiterte Befehl im Gerät. Die INF-Datei ist zu lang.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_UNSUPPORTED_BPS"></span><span id="error_unsupported_bps"></span><dl> <dt><strong>ERROR_UNSUPPORTED_BPS</strong></dt> <dt>701</dt> </dl></td>
<td>Das Gerät wurde in eine Verbindungsgeschwindigkeit verschoben, die vom com-Treiber nicht unterstützt wird.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_UNEXPECTED_RESPONSE"></span><span id="error_unexpected_response"></span><dl> <dt><strong>ERROR_UNEXPECTED_RESPONSE</strong></dt> <dt>702</dt> </dl></td>
<td>Geräte Antwort empfangen, wenn keine erwartet wurde.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INTERACTIVE_MODE"></span><span id="error_interactive_mode"></span><dl> <dt><strong>ERROR_INTERACTIVE_MODE</strong></dt> <dt>703</dt> </dl></td>
<td>Ein Fehler ist aufgetreten, weil der interaktive Modus aktiviert ist.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_BAD_CALLBACK_NUMBER"></span><span id="error_bad_callback_number"></span><dl> <dt><strong>ERROR_BAD_CALLBACK_NUMBER</strong></dt> <dt>704</dt> </dl></td>
<td>Es wurde eine ungültige Rückrufnummer angegeben.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_AUTH_STATE"></span><span id="error_invalid_auth_state"></span><dl> <dt><strong>ERROR_INVALID_AUTH_STATE</strong></dt> <dt>705</dt> </dl></td>
<td>Der angegebene Authentifizierungs Status ist ungültig.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_WRITING_INITBPS"></span><span id="error_writing_initbps"></span><dl> <dt><strong>ERROR_WRITING_INITBPS</strong></dt> <dt>706</dt> </dl></td>
<td>Fehler beim Schreiben der anfänglichen Verbindungsgeschwindigkeit.<br/>
<blockquote>
[!Note]<br />
Veraltet in Windows Vista und höheren Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_X25_DIAGNOSTIC"></span><span id="error_x25_diagnostic"></span><dl> <dt><strong>ERROR_X25_DIAGNOSTIC</strong></dt> <dt>707</dt> </dl></td>
<td>Ein X. 25-Diagnose Hinweis wurde empfangen.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_ACCT_EXPIRED"></span><span id="error_acct_expired"></span><dl> <dt><strong>ERROR_ACCT_EXPIRED</strong></dt> <dt>708</dt> </dl></td>
<td>Das angegebene Konto ist abgelaufen.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CHANGING_PASSWORD"></span><span id="error_changing_password"></span><dl> <dt><strong>ERROR_CHANGING_PASSWORD</strong></dt> <dt>709</dt> </dl></td>
<td>Fehler beim Versuch, das Kennwort für die Domäne zu ändern.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_OVERRUN"></span><span id="error_overrun"></span><dl> <dt><strong>ERROR_OVERRUN</strong></dt> <dt>710</dt> </dl></td>
<td>Bei der Kommunikation mit dem Modem wurden serielle Überlauf Fehler festgestellt.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_RASMAN_CANNOT_INITIALIZE"></span><span id="error_rasman_cannot_initialize"></span><dl> <dt><strong>ERROR_RASMAN_CANNOT_INITIALIZE</strong></dt> <dt>711</dt> </dl></td>
<td>Fehler bei der RASMAN-Initialisierung. Überprüfen Sie das Ereignisprotokoll.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_BIPLEX_PORT_NOT_AVAILABLE"></span><span id="error_biplex_port_not_available"></span><dl> <dt><strong>ERROR_BIPLEX_PORT_NOT_AVAILABLE</strong></dt> <dt>712</dt> </dl></td>
<td>Der bidirektionale Port wird initialisiert. Warten Sie einige Sekunden, und wählen Sie dann erneut aus.<br/>
<blockquote>
[!Note]<br />
Veraltet in Windows Vista und höheren Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_ACTIVE_ISDN_LINES"></span><span id="error_no_active_isdn_lines"></span><dl> <dt><strong>ERROR_NO_ACTIVE_ISDN_LINES</strong></dt> <dt>713</dt> </dl></td>
<td>Es sind keine aktiven ISDN-Zeilen verfügbar.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_ISDN_CHANNELS_AVAILABLE"></span><span id="error_no_isdn_channels_available"></span><dl> <dt><strong>ERROR_NO_ISDN_CHANNELS_AVAILABLE</strong></dt> <dt>714</dt> </dl></td>
<td>Es sind keine ISDN-Kanäle zum Ausführen des Aufrufes verfügbar.<br/>
<blockquote>
[!Note]<br />
Veraltet in Windows Vista und höheren Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_TOO_MANY_LINE_ERRORS"></span><span id="error_too_many_line_errors"></span><dl> <dt><strong>ERROR_TOO_MANY_LINE_ERRORS</strong></dt> <dt>715</dt> </dl></td>
<td>Aufgrund der schlechten Qualität der Telefonleitung sind zu viele Fehler aufgetreten.<br/>
<blockquote>
[!Note]<br />
Veraltet in Windows Vista und höheren Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_IP_CONFIGURATION"></span><span id="error_ip_configuration"></span><dl> <dt><strong>ERROR_IP_CONFIGURATION</strong></dt> <dt>716</dt> </dl></td>
<td>Die IP-Konfiguration für den Remote Zugriff ist unbrauchbar.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_IP_ADDRESSES"></span><span id="error_no_ip_addresses"></span><dl> <dt><strong>ERROR_NO_IP_ADDRESSES</strong></dt> <dt>717</dt> </dl></td>
<td>Im statischen Pool der Remote Zugriffs-IP-Adressen sind keine IP-Adressen verfügbar.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PPP_TIMEOUT"></span><span id="error_ppp_timeout"></span><dl> <dt><strong>ERROR_PPP_TIMEOUT</strong></dt> <dt>718</dt> </dl></td>
<td>Ein PPP-Timeout ist aufgetreten.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PPP_REMOTE_TERMINATED"></span><span id="error_ppp_remote_terminated"></span><dl> <dt><strong>ERROR_PPP_REMOTE_TERMINATED</strong></dt> <dt>719</dt> </dl></td>
<td>Die Verbindung wurde vom Remote Computer beendet.<br/>
<blockquote>
[!Note]<br />
Veraltet in Windows Vista und höheren Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PPP_NO_PROTOCOLS_CONFIGURED"></span><span id="error_ppp_no_protocols_configured"></span><dl> <dt><strong>ERROR_PPP_NO_PROTOCOLS_CONFIGURED</strong></dt> <dt>720</dt> </dl></td>
<td>Es sind keine PPP-Steuerungsprotokolle konfiguriert.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PPP_NO_RESPONSE"></span><span id="error_ppp_no_response"></span><dl> <dt><strong>ERROR_PPP_NO_RESPONSE</strong></dt> <dt>721</dt> </dl></td>
<td>Der PPP-Remote Peer antwortet nicht.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PPP_INVALID_PACKET"></span><span id="error_ppp_invalid_packet"></span><dl> <dt><strong>ERROR_PPP_INVALID_PACKET</strong></dt> <dt>722</dt> </dl></td>
<td>Das PPP-Paket ist ungültig.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PHONE_NUMBER_TOO_LONG"></span><span id="error_phone_number_too_long"></span><dl> <dt><strong>ERROR_PHONE_NUMBER_TOO_LONG</strong></dt> <dt>723</dt> </dl></td>
<td>Die Telefonnummer (einschließlich Präfix und Suffix) ist zu lang.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_IPXCP_NO_DIALOUT_CONFIGURED"></span><span id="error_ipxcp_no_dialout_configured"></span><dl> <dt><strong>ERROR_IPXCP_NO_DIALOUT_CONFIGURED</strong></dt> <dt>724</dt> </dl></td>
<td>Das IPX-Protokoll kann nicht auf dem Modem (oder einem anderen Verbindungsgerät) eingeblendet werden, da dieser Computer nicht für die Abwahl konfiguriert ist (es handelt sich um einen IPX-Router).<br/>
<blockquote>
[!Note]<br />
Veraltet in Windows Vista und höheren Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_IPXCP_NO_DIALIN_CONFIGURED"></span><span id="error_ipxcp_no_dialin_configured"></span><dl> <dt><strong>ERROR_IPXCP_NO_DIALIN_CONFIGURED</strong></dt> <dt>725</dt> </dl></td>
<td>Das IPX-Protokoll kann nicht auf dem Modem (oder einem anderen Verbindungsgerät) wählen, da dieser Computer nicht für die Wahl von (der IPX-Router ist nicht installiert) konfiguriert ist.<br/>
<blockquote>
[!Note]<br />
Veraltet in Windows Vista und höheren Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_IPXCP_DIALOUT_ALREADY_ACTIVE"></span><span id="error_ipxcp_dialout_already_active"></span><dl> <dt><strong>ERROR_IPXCP_DIALOUT_ALREADY_ACTIVE</strong></dt> <dt>726</dt> </dl></td>
<td>Das IPX-Protokoll kann nicht für mehr als einen Port gleichzeitig verwendet werden.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_ACCESSING_TCPCFGDLL"></span><span id="error_accessing_tcpcfgdll"></span><dl> <dt><strong>ERROR_ACCESSING_TCPCFGDLL</strong></dt> <dt>727</dt> </dl></td>
<td>Auf TCPCFG.DLL kann nicht zugegriffen werden.<br/>
<blockquote>
[!Note]<br />
Veraltet in Windows Vista und höheren Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_IP_RAS_ADAPTER"></span><span id="error_no_ip_ras_adapter"></span><dl> <dt><strong>ERROR_NO_IP_RAS_ADAPTER</strong></dt> <dt>728</dt> </dl></td>
<td>Es wurde kein an den Remote Zugriff gebundener IP-Adapter gefunden.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SLIP_REQUIRES_IP"></span><span id="error_slip_requires_ip"></span><dl> <dt><strong>ERROR_SLIP_REQUIRES_IP</strong></dt> <dt>729</dt> </dl></td>
<td>Der Slip kann nur verwendet werden, wenn das IP-Protokoll installiert ist.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PROJECTION_NOT_COMPLETE"></span><span id="error_projection_not_complete"></span><dl> <dt><strong>ERROR_PROJECTION_NOT_COMPLETE</strong></dt> <dt>730</dt> </dl></td>
<td>Die Computer Registrierung ist nicht fertiggestellt.<br/>
<blockquote>
[!Note]<br />
Veraltet in Windows Vista und höheren Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PROTOCOL_NOT_CONFIGURED"></span><span id="error_protocol_not_configured"></span><dl> <dt><strong>ERROR_PROTOCOL_NOT_CONFIGURED</strong></dt> <dt>731</dt> </dl></td>
<td>Das angegebene Protokoll ist nicht konfiguriert.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PPP_NOT_CONVERGING"></span><span id="error_ppp_not_converging"></span><dl> <dt><strong>ERROR_PPP_NOT_CONVERGING</strong></dt> <dt>732</dt> </dl></td>
<td>Die PPP-Aushandlung wird nicht konvergieren.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PPP_CP_REJECTED"></span><span id="error_ppp_cp_rejected"></span><dl> <dt><strong>ERROR_PPP_CP_REJECTED</strong></dt> <dt>733</dt> </dl></td>
<td>Das PPP-Steuerungs Protokoll für das angegebene Netzwerkprotokoll ist auf dem Server nicht verfügbar.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PPP_LCP_TERMINATED"></span><span id="error_ppp_lcp_terminated"></span><dl> <dt><strong>ERROR_PPP_LCP_TERMINATED</strong></dt> <dt>734</dt> </dl></td>
<td>Das PPP-Link Steuerungs Protokoll wurde beendet.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PPP_REQUIRED_ADDRESS_REJECTED"></span><span id="error_ppp_required_address_rejected"></span><dl> <dt><strong>ERROR_PPP_REQUIRED_ADDRESS_REJECTED</strong></dt> <dt>735</dt> </dl></td>
<td>Die angeforderte Adresse wurde vom Server abgelehnt.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PPP_NCP_TERMINATED"></span><span id="error_ppp_ncp_terminated"></span><dl> <dt><strong>ERROR_PPP_NCP_TERMINATED</strong></dt> <dt>736</dt> </dl></td>
<td>Der Remote Computer hat das Steuerungs Protokoll beendet.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PPP_LOOPBACK_DETECTED"></span><span id="error_ppp_loopback_detected"></span><dl> <dt><strong>ERROR_PPP_LOOPBACK_DETECTED</strong></dt> <dt>737</dt> </dl></td>
<td>Loopback erkannt.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PPP_NO_ADDRESS_ASSIGNED"></span><span id="error_ppp_no_address_assigned"></span><dl> <dt><strong>ERROR_PPP_NO_ADDRESS_ASSIGNED</strong></dt> <dt>738</dt> </dl></td>
<td>Der Server hat keine Adresse zugewiesen.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CANNOT_USE_LOGON_CREDENTIALS"></span><span id="error_cannot_use_logon_credentials"></span><dl> <dt><strong>ERROR_CANNOT_USE_LOGON_CREDENTIALS</strong></dt> <dt>739</dt> </dl></td>
<td>Der Remote Server kann das verschlüsselte Windows NT-Kennwort nicht verwenden.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_TAPI_CONFIGURATION"></span><span id="error_tapi_configuration"></span><dl> <dt><strong>ERROR_TAPI_CONFIGURATION</strong></dt> <dt>740</dt> </dl></td>
<td>Die für den Remote Zugriff konfigurierten TAPI-Geräte konnten nicht initialisiert werden oder wurden nicht ordnungsgemäß installiert.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_LOCAL_ENCRYPTION"></span><span id="error_no_local_encryption"></span><dl> <dt><strong>ERROR_NO_LOCAL_ENCRYPTION</strong></dt> <dt>741</dt> </dl></td>
<td>Der lokale Computer unterstützt keine Verschlüsselung.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_REMOTE_ENCRYPTION"></span><span id="error_no_remote_encryption"></span><dl> <dt><strong>ERROR_NO_REMOTE_ENCRYPTION</strong></dt> <dt>742</dt> </dl></td>
<td>Der Remote Server unterstützt keine Verschlüsselung.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_REMOTE_REQUIRES_ENCRYPTION"></span><span id="error_remote_requires_encryption"></span><dl> <dt><strong>ERROR_REMOTE_REQUIRES_ENCRYPTION</strong></dt> <dt>743</dt> </dl></td>
<td>Für den Remote Computer ist eine Datenverschlüsselung erforderlich.<br/>
<blockquote>
[!Note]<br />
Veraltet in Windows Vista und höheren Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_IPXCP_NET_NUMBER_CONFLICT"></span><span id="error_ipxcp_net_number_conflict"></span><dl> <dt><strong>ERROR_IPXCP_NET_NUMBER_CONFLICT</strong></dt> <dt>744</dt> </dl></td>
<td>Die vom Remote Computer zugewiesene IPX-Netzwerk Nummer kann vom System nicht verwendet werden. Im Ereignisprotokoll werden zusätzliche Informationen bereitgestellt.<br/>
<blockquote>
[!Note]<br />
Veraltet in Windows Vista und höheren Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_SMM"></span><span id="error_invalid_smm"></span><dl> <dt><strong>ERROR_INVALID_SMM</strong></dt> <dt>745</dt> </dl></td>
<td>Das Sitzungs Verwaltungsmodul (SMM) ist ungültig.<br/>
<blockquote>
[!Note]<br />
Veraltet in Windows Vista und höheren Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_SMM_UNINITIALIZED"></span><span id="error_smm_uninitialized"></span><dl> <dt><strong>ERROR_SMM_UNINITIALIZED</strong></dt> <dt>746</dt> </dl></td>
<td>Die SMM ist nicht initialisiert.<br/>
<blockquote>
[!Note]<br />
Veraltet in Windows Vista und höheren Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_MAC_FOR_PORT"></span><span id="error_no_mac_for_port"></span><dl> <dt><strong>ERROR_NO_MAC_FOR_PORT</strong></dt> <dt>747</dt> </dl></td>
<td>Kein Mac für Port.<br/>
<blockquote>
[!Note]<br />
Veraltet in Windows Vista und höheren Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_SMM_TIMEOUT"></span><span id="error_smm_timeout"></span><dl> <dt><strong>ERROR_SMM_TIMEOUT</strong></dt> <dt>748</dt> </dl></td>
<td>Timeout bei der SMM.<br/>
<blockquote>
[!Note]<br />
Veraltet in Windows Vista und höheren Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_BAD_PHONE_NUMBER"></span><span id="error_bad_phone_number"></span><dl> <dt><strong>ERROR_BAD_PHONE_NUMBER</strong></dt> <dt>749</dt> </dl></td>
<td>Es wurde eine ungültige Telefonnummer angegeben.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_WRONG_MODULE"></span><span id="error_wrong_module"></span><dl> <dt><strong>ERROR_WRONG_MODULE</strong></dt> <dt>750</dt> </dl></td>
<td>Die falsche SMM wurde angegeben.<br/>
<blockquote>
[!Note]<br />
Veraltet in Windows Vista und höheren Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_CALLBACK_NUMBER"></span><span id="error_invalid_callback_number"></span><dl> <dt><strong>ERROR_INVALID_CALLBACK_NUMBER</strong></dt> <dt>751</dt> </dl></td>
<td>Die Rückrufnummer enthält ein ungültiges Zeichen. Nur die folgenden 18 Zeichen sind zulässig: 0 bis 9, T, P, W, (,),-, @ und Leerzeichen.<br/>
<blockquote>
[!Note]<br />
Veraltet in Windows Vista und höheren Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_SCRIPT_SYNTAX"></span><span id="error_script_syntax"></span><dl> <dt><strong>ERROR_SCRIPT_SYNTAX</strong></dt> <dt>752</dt> </dl></td>
<td>Beim Verarbeiten eines Skripts ist ein Syntax Fehler aufgetreten.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_HANGUP_FAILED"></span><span id="error_hangup_failed"></span><dl> <dt><strong>ERROR_HANGUP_FAILED</strong></dt> <dt>753</dt> </dl></td>
<td>Die Verbindung konnte nicht getrennt werden, da Sie vom Multiprotokollrouter erstellt wurde.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_BUNDLE_NOT_FOUND"></span><span id="error_bundle_not_found"></span><dl> <dt><strong>ERROR_BUNDLE_NOT_FOUND</strong></dt> <dt>754</dt> </dl></td>
<td>Das multilinkbündel konnte vom System nicht gefunden werden.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CANNOT_DO_CUSTOMDIAL"></span><span id="error_cannot_do_customdial"></span><dl> <dt><strong>ERROR_CANNOT_DO_CUSTOMDIAL</strong></dt> <dt>755</dt> </dl></td>
<td>Das System kann die automatisierte Wahl nicht durchführen, da für diese Verbindung eine benutzerdefinierte Einwählprogramm festgelegt ist.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DIAL_ALREADY_IN_PROGRESS"></span><span id="error_dial_already_in_progress"></span><dl> <dt><strong>ERROR_DIAL_ALREADY_IN_PROGRESS</strong></dt> <dt>756</dt> </dl></td>
<td>Diese Verbindung wird bereits gewählt.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_RASAUTO_CANNOT_INITIALIZE"></span><span id="error_rasauto_cannot_initialize"></span><dl> <dt><strong>ERROR_RASAUTO_CANNOT_INITIALIZE</strong></dt> <dt>757</dt> </dl></td>
<td>RAS konnte nicht automatisch gestartet werden. Im Ereignisprotokoll werden zusätzliche Informationen bereitgestellt.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_CONNECTION_ALREADY_SHARED"></span><span id="error_connection_already_shared"></span><dl> <dt><strong>ERROR_CONNECTION_ALREADY_SHARED</strong></dt> <dt>758</dt> </dl></td>
<td>Internet Connection Sharing (ICS) ist bereits für die Verbindung aktiviert.<br/>
<blockquote>
[!Note]<br />
Veraltet in Windows Vista und höheren Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SHARING_CHANGE_FAILED"></span><span id="error_sharing_change_failed"></span><dl> <dt><strong>ERROR_SHARING_CHANGE_FAILED</strong></dt> <dt>759</dt> </dl></td>
<td>Fehler beim Ändern der vorhandenen Einstellungen für die gemeinsame Nutzung der Internet Verbindung.<br/>
<blockquote>
[!Note]<br />
Veraltet in Windows Vista und höheren Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_SHARING_ROUTER_INSTALL"></span><span id="error_sharing_router_install"></span><dl> <dt><strong>ERROR_SHARING_ROUTER_INSTALL</strong></dt> <dt>760</dt> </dl></td>
<td>Fehler beim Aktivieren der Routing Funktionen.<br/>
<blockquote>
[!Note]<br />
Veraltet in Windows Vista und höheren Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SHARE_CONNECTION_FAILED"></span><span id="error_share_connection_failed"></span><dl> <dt><strong>ERROR_SHARE_CONNECTION_FAILED</strong></dt> <dt>761</dt> </dl></td>
<td>Fehler beim Aktivieren der gemeinsamen Nutzung der Internet Verbindung für die Verbindung.<br/>
<blockquote>
[!Note]<br />
Veraltet in Windows Vista und höheren Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="7ERROR_SHARING_PRIVATE_INSTALL64"></span><span id="7error_sharing_private_install64"></span><dl> <dt><strong>7ERROR_SHARING_PRIVATE_INSTALL64</strong></dt> <dt>762</dt> </dl></td>
<td>Fehler beim Konfigurieren des lokalen Netzwerks für die Freigabe.<br/>
<blockquote>
[!Note]<br />
Veraltet in Windows Vista und höheren Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CANNOT_SHARE_CONNECTION"></span><span id="error_cannot_share_connection"></span><dl> <dt><strong>ERROR_CANNOT_SHARE_CONNECTION</strong></dt> <dt>763</dt> </dl></td>
<td>Die Freigabe der Internet Verbindung kann nicht aktiviert werden. Es sind mehr als eine LAN-Verbindung außer der Verbindung vorhanden, die freigegeben werden soll.<br/>
<blockquote>
[!Note]<br />
Veraltet in Windows Vista und höheren Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_SMART_CARD_READER"></span><span id="error_no_smart_card_reader"></span><dl> <dt><strong>ERROR_NO_SMART_CARD_READER</strong></dt> <dt>764</dt> </dl></td>
<td>Es ist kein Smartcardleser installiert.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SHARING_ADDRESS_EXISTS"></span><span id="error_sharing_address_exists"></span><dl> <dt><strong>ERROR_SHARING_ADDRESS_EXISTS</strong></dt> <dt>765</dt> </dl></td>
<td>Die Freigabe der Internet Verbindung kann nicht aktiviert werden. Eine LAN-Verbindung ist bereits mit der IP-Adresse konfiguriert, die für die automatische IP-Adressierung erforderlich ist. <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_CERTIFICATE"></span><span id="error_no_certificate"></span><dl> <dt><strong>ERROR_NO_CERTIFICATE</strong></dt> <dt>766</dt> </dl></td>
<td>Ein Zertifikat konnte nicht gefunden werden. Für Verbindungen, die das L2TP-Protokoll über IPSec verwenden, muss ein Computer Zertifikat installiert werden, das auch als Computer Zertifikat bezeichnet wird. <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SHARING_MULTIPLE_ADDRESSES"></span><span id="error_sharing_multiple_addresses"></span><dl> <dt><strong>ERROR_SHARING_MULTIPLE_ADDRESSES</strong></dt> <dt>767</dt> </dl></td>
<td>Die Freigabe der Internet Verbindung kann nicht aktiviert werden. Die LAN-Verbindung, die als privates Netzwerk ausgewählt ist, verfügt über mehr als eine IP-Adresse. Konfigurieren Sie die LAN-Verbindung mit einer einzelnen IP-Adresse neu, bevor Sie die Freigabe der Internet Verbindung aktivieren. <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_FAILED_TO_ENCRYPT"></span><span id="error_failed_to_encrypt"></span><dl> <dt><strong>ERROR_FAILED_TO_ENCRYPT</strong></dt> <dt>768</dt> </dl></td>
<td>Der Verbindungsversuch ist fehlgeschlagen, weil die Daten nicht verschlüsselt wurden. <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_BAD_ADDRESS_SPECIFIED"></span><span id="error_bad_address_specified"></span><dl> <dt><strong>ERROR_BAD_ADDRESS_SPECIFIED</strong></dt> <dt>769</dt> </dl></td>
<td>Das angegebene Ziel ist nicht erreichbar. <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_CONNECTION_REJECT"></span><span id="error_connection_reject"></span><dl> <dt><strong>ERROR_CONNECTION_REJECT</strong></dt> <dt>770</dt> </dl></td>
<td>Der Remote Computer hat den Verbindungsversuch zurückgewiesen. <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CONGESTION"></span><span id="error_congestion"></span><dl> <dt><strong>ERROR_CONGESTION</strong></dt> <dt>771</dt> </dl></td>
<td>Der Verbindungsversuch ist fehlgeschlagen, da das Netzwerk ausgelastet ist. <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INCOMPATIBLE"></span><span id="error_incompatible"></span><dl> <dt><strong>ERROR_INCOMPATIBLE</strong></dt> <dt>772</dt> </dl></td>
<td>Die Netzwerkhardware des Remote Computers ist nicht mit dem angeforderten Anforderungstyp kompatibel. <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NUMBERCHANGED"></span><span id="error_numberchanged"></span><dl> <dt><strong>ERROR_NUMBERCHANGED</strong></dt> <dt>773</dt> </dl></td>
<td>Der Verbindungsversuch ist fehlgeschlagen, da sich die Ziel Nummer geändert hat. <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_TEMPFAILURE"></span><span id="error_tempfailure"></span><dl> <dt><strong>ERROR_TEMPFAILURE</strong></dt> <dt>774</dt> </dl></td>
<td>Der Verbindungsversuch ist aufgrund eines vorübergehenden Fehlers fehlgeschlagen. Try connecting again.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_BLOCKED"></span><span id="error_blocked"></span><dl> <dt><strong>ERROR_BLOCKED</strong></dt> <dt>775</dt> </dl></td>
<td>Der-Befehl wurde vom Remote Computer blockiert. <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DONOTDISTURB"></span><span id="error_donotdisturb"></span><dl> <dt><strong>ERROR_DONOTDISTURB</strong></dt> <dt>776</dt> </dl></td>
<td>Der Aufruf konnte nicht verbunden werden, da der Remote Computer die Funktion "nicht stören" aufgerufen hat. <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_OUTOFORDER"></span><span id="error_outoforder"></span><dl> <dt><strong>ERROR_OUTOFORDER</strong></dt> <dt>777</dt> </dl></td>
<td>Der Verbindungsversuch ist fehlgeschlagen, weil das Modem oder ein anderes Verbindungsgerät auf dem Remote Computer nicht in der richtigen Reihenfolge ist. <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_UNABLE_TO_AUTHENTICATE_SERVER"></span><span id="error_unable_to_authenticate_server"></span><dl> <dt><strong>ERROR_UNABLE_TO_AUTHENTICATE_SERVER</strong></dt> <dt>778</dt> </dl></td>
<td>Es war nicht möglich, die Identität des Servers zu überprüfen. <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SMART_CARD_REQUIRED"></span><span id="error_smart_card_required"></span><dl> <dt><strong>ERROR_SMART_CARD_REQUIRED</strong></dt> <dt>779</dt> </dl></td>
<td>Wenn Sie diese Verbindung verwenden möchten, müssen Sie eine Smartcard verwenden.<br/>
<blockquote>
[!Note]<br />
Veraltet in Windows Vista und höheren Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INVALID_FUNCTION_FOR_ENTRY"></span><span id="error_invalid_function_for_entry"></span><dl> <dt><strong>ERROR_INVALID_FUNCTION_FOR_ENTRY</strong></dt> <dt>780</dt> </dl></td>
<td>Eine versuchte Funktion ist für diese Verbindung ungültig. <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CERT_FOR_ENCRYPTION_NOT_FOUND"></span><span id="error_cert_for_encryption_not_found"></span><dl> <dt><strong>ERROR_CERT_FOR_ENCRYPTION_NOT_FOUND</strong></dt> <dt>781</dt> </dl></td>
<td>Der Verschlüsselungs Versuch ist fehlgeschlagen, da kein gültiges Zertifikat gefunden wurde.<br/>
<blockquote>
[!Note]<br />
Veraltet in Windows Vista und höheren Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_SHARING_RRAS_CONFLICT"></span><span id="error_sharing_rras_conflict"></span><dl> <dt><strong>ERROR_SHARING_RRAS_CONFLICT</strong></dt> <dt>782</dt> </dl></td>
<td>Die Verbindungs Freigabe (NAT) ist zurzeit als Routing Protokoll installiert und muss entfernt werden, bevor die gemeinsame Nutzung der Internet Verbindung aktiviert wird.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SHARING_NO_PRIVATE_LAN"></span><span id="error_sharing_no_private_lan"></span><dl> <dt><strong>ERROR_SHARING_NO_PRIVATE_LAN</strong></dt> <dt>783</dt> </dl></td>
<td>Die Freigabe der Internet Verbindung kann nicht aktiviert werden. Die als privates Netzwerk ausgewählte LAN-Verbindung ist entweder nicht vorhanden oder wird vom Netzwerk getrennt. Stellen Sie sicher, dass der LAN-Adapter verbunden ist, bevor Sie die Freigabe von Internet Verbindungen aktivieren <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_DIFF_USER_AT_LOGON"></span><span id="error_no_diff_user_at_logon"></span><dl> <dt><strong>ERROR_NO_DIFF_USER_AT_LOGON</strong></dt> <dt>784</dt> </dl></td>
<td>Sie können diese Verbindung zum Anmeldezeitpunkt nicht verwenden, da Sie so konfiguriert ist, dass Sie einen anderen Benutzernamen als den auf der Smartcard verwendet. Wenn Sie diese Verbindung zum Anmeldezeitpunkt verwenden möchten, müssen Sie Sie so konfigurieren, dass Sie den Benutzernamen auf der Smartcard verwendet. <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_REG_CERT_AT_LOGON"></span><span id="error_no_reg_cert_at_logon"></span><dl> <dt><strong>ERROR_NO_REG_CERT_AT_LOGON</strong></dt> <dt>785</dt> </dl></td>
<td>Sie können diese Verbindung nicht zum Anmeldezeitpunkt verwenden, da Sie nicht für die Verwendung einer Smartcard konfiguriert ist. Wenn Sie diese zum Anmeldezeitpunkt verwenden möchten, müssen Sie die Eigenschaften dieser Verbindung bearbeiten, damit Sie eine Smartcard verwendet. <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_OAKLEY_NO_CERT"></span><span id="error_oakley_no_cert"></span><dl> <dt><strong>ERROR_OAKLEY_NO_CERT</strong></dt> <dt>786</dt> </dl></td>
<td>Der L2TP-Verbindungsversuch ist fehlgeschlagen, weil auf dem Computer kein gültiges Computer Zertifikat für die Sicherheits Authentifizierung vorhanden ist. <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_OAKLEY_AUTH_FAIL"></span><span id="error_oakley_auth_fail"></span><dl> <dt><strong>ERROR_OAKLEY_AUTH_FAIL</strong></dt> <dt>787</dt> </dl></td>
<td>Der L2TP-Verbindungsversuch ist fehlgeschlagen, da die Sicherheitsebene den Remote Computer nicht authentifizieren konnte. <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_OAKLEY_ATTRIB_FAIL"></span><span id="error_oakley_attrib_fail"></span><dl> <dt><strong>ERROR_OAKLEY_ATTRIB_FAIL</strong></dt> <dt>788</dt> </dl></td>
<td>Der L2TP-Verbindungsversuch ist fehlgeschlagen, da die Sicherheitsebene keine kompatiblen Parameter mit dem Remote Computer aushandeln konnte. <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_OAKLEY_GENERAL_PROCESSING"></span><span id="error_oakley_general_processing"></span><dl> <dt><strong>ERROR_OAKLEY_GENERAL_PROCESSING</strong></dt> <dt>789</dt> </dl></td>
<td>Fehler beim Verbindungsversuch L2TP, weil auf der Sicherheitsebene während der ersten Verhandlung mit dem Remote Computer ein Verarbeitungsfehler aufgetreten ist. <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_OAKLEY_NO_PEER_CERT"></span><span id="error_oakley_no_peer_cert"></span><dl> <dt><strong>ERROR_OAKLEY_NO_PEER_CERT</strong></dt> <dt>790</dt> </dl></td>
<td>Fehler beim L2TP-Verbindungsversuch, weil die Zertifikat Überprüfung auf dem Remote Computer fehlgeschlagen ist. <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_OAKLEY_NO_POLICY"></span><span id="error_oakley_no_policy"></span><dl> <dt><strong>ERROR_OAKLEY_NO_POLICY</strong></dt> <dt>791</dt> </dl></td>
<td>Der L2TP-Verbindungsversuch ist fehlgeschlagen, da die Sicherheitsrichtlinie für die Verbindung nicht gefunden wurde. <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_OAKLEY_TIMED_OUT"></span><span id="error_oakley_timed_out"></span><dl> <dt><strong>ERROR_OAKLEY_TIMED_OUT</strong></dt> <dt>792</dt> </dl></td>
<td>Fehler beim L2TP-Verbindungsversuch aufgrund einer Zeitüberschreitung bei der Sicherheitsaus Handlung. <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_OAKLEY_ERROR"></span><span id="error_oakley_error"></span><dl> <dt><strong>ERROR_OAKLEY_ERROR</strong></dt> <dt>793</dt> </dl></td>
<td>Der L2TP-Verbindungsversuch ist fehlgeschlagen, weil beim Aushandeln der Sicherheit ein Fehler aufgetreten ist. <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_UNKNOWN_FRAMED_PROTOCOL"></span><span id="error_unknown_framed_protocol"></span><dl> <dt><strong>ERROR_UNKNOWN_FRAMED_PROTOCOL</strong></dt> <dt>794</dt> </dl></td>
<td>Das RADIUS-Attribut des Attributs für diesen Benutzer ist nicht PPP. <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_WRONG_TUNNEL_TYPE"></span><span id="error_wrong_tunnel_type"></span><dl> <dt><strong>ERROR_WRONG_TUNNEL_TYPE</strong></dt> <dt>795</dt> </dl></td>
<td>Das Tunnel-typradius-Attribut für diesen Benutzer ist nicht korrekt. <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_UNKNOWN_SERVICE_TYPE"></span><span id="error_unknown_service_type"></span><dl> <dt><strong>ERROR_UNKNOWN_SERVICE_TYPE</strong></dt> <dt>796</dt> </dl></td>
<td>Das RADIUS-Attribut des Dienst Typs für diesen Benutzer ist weder "gerahmt" noch "Callback" eingeschlossen. <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CONNECTING_DEVICE_NOT_FOUND"></span><span id="error_connecting_device_not_found"></span><dl> <dt><strong>ERROR_CONNECTING_DEVICE_NOT_FOUND</strong></dt> <dt>797</dt> </dl></td>
<td>Es konnte keine Verbindung mit dem Remote Computer hergestellt werden, da das Modem nicht gefunden wurde oder ausgelastet war. <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_EAPTLS_CERTIFICATE"></span><span id="error_no_eaptls_certificate"></span><dl> <dt><strong>ERROR_NO_EAPTLS_CERTIFICATE</strong></dt> <dt>798</dt> </dl></td>
<td>Es konnte kein Zertifikat gefunden werden, das mit dem Extensible Authentication Protocol (EAP) verwendet werden kann. <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SHARING_HOST_ADDRESS_CONFLICT"></span><span id="error_sharing_host_address_conflict"></span><dl> <dt><strong>ERROR_SHARING_HOST_ADDRESS_CONFLICT</strong></dt> <dt>799</dt> </dl></td>
<td>Die gemeinsame Nutzung der Internet Verbindung (ICS) kann aufgrund eines IP-Adress Konflikts im Netzwerk nicht aktiviert werden. ICS erfordert, dass der Host für die Verwendung von <strong>192.168.0.1</strong>konfiguriert ist. Stellen Sie sicher, dass kein anderer Client im Netzwerk für die Verwendung von <strong>192.168.0.1</strong>konfiguriert ist.<br/>
<blockquote>
[!Note]<br />
Unterstützt in Windows XP und höheren Versionen von Windows.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
Windows 7 und höher: der Host muss für die Verwendung von <strong>192.168.137.1</strong> konfiguriert werden.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_AUTOMATIC_VPN_FAILED"></span><span id="error_automatic_vpn_failed"></span><dl> <dt><strong>ERROR_AUTOMATIC_VPN_FAILED</strong></dt> <dt>800</dt> </dl></td>
<td>Die VPN-Verbindung konnte nicht hergestellt werden. Möglicherweise ist der VPN-Server nicht erreichbar, oder die Sicherheitsparameter sind für diese Verbindung nicht ordnungsgemäß konfiguriert. <br/>
<blockquote>
[!Note]<br />
Unterstützt in Windows XP und höheren Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_VALIDATING_SERVER_CERT"></span><span id="error_validating_server_cert"></span><dl> <dt><strong>ERROR_VALIDATING_SERVER_CERT</strong></dt> <dt>801</dt> </dl></td>
<td>Diese Verbindung ist so konfiguriert, dass die Identität des Zugriffs Servers überprüft wird, Windows kann jedoch das vom Server gesendete digitale Zertifikat nicht überprüfen.<br/>
<blockquote>
[!Note]<br />
Unterstützt in Windows XP und höheren Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_READING_SCARD"></span><span id="error_reading_scard"></span><dl> <dt><strong>ERROR_READING_SCARD</strong></dt> <dt>802</dt> </dl></td>
<td>Die angegebene Karte wurde nicht erkannt. Überprüfen Sie, ob die Karte ordnungsgemäß eingefügt wurde und sicher ist.<br/>
<blockquote>
[!Note]<br />
Wird in Windows XP mit SP1 und höheren Versionen von Windows unterstützt.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_PEAP_COOKIE_CONFIG"></span><span id="error_invalid_peap_cookie_config"></span><dl> <dt><strong>ERROR_INVALID_PEAP_COOKIE_CONFIG</strong></dt> <dt>803</dt> </dl></td>
<td>Die im Sitzungs Cookie gespeicherte Peer-Konfiguration stimmt nicht mit der aktuellen Sitzungs Konfiguration identisch.<br/>
<blockquote>
[!Note]<br />
Wird in Windows XP mit SP1 und höheren Versionen von Windows unterstützt.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INVALID_PEAP_COOKIE_USER"></span><span id="error_invalid_peap_cookie_user"></span><dl> <dt><strong>ERROR_INVALID_PEAP_COOKIE_USER</strong></dt> <dt>804</dt> </dl></td>
<td>Die im Sitzungs Cookie gespeicherte Peer-ID stimmt nicht mit der aktuellen Identität identisch.<br/>
<blockquote>
[!Note]<br />
Wird in Windows XP mit SP1 und höheren Versionen von Windows unterstützt.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_MSCHAPV2_CONFIG"></span><span id="error_invalid_mschapv2_config"></span><dl> <dt><strong>ERROR_INVALID_MSCHAPV2_CONFIG</strong></dt> <dt>805</dt> </dl></td>
<td>Sie können diese Verbindung zum Anmeldezeitpunkt nicht verwenden, da Sie so konfiguriert ist, dass Sie die Anmelde Informationen des aktuell angemeldeten Benutzers verwendet.<br/>
<blockquote>
[!Note]<br />
Wird in Windows XP mit SP1 und höheren Versionen von Windows unterstützt.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_VPN_GRE_BLOCKED"></span><span id="error_vpn_gre_blocked"></span><dl> <dt><strong>ERROR_VPN_GRE_BLOCKED</strong></dt> <dt>806</dt> </dl></td>
<td>Es wurde eine Verbindung zwischen Ihrem Computer und dem VPN-Server gestartet, aber die VPN-Verbindung kann nicht hergestellt werden. Die häufigste Ursache hierfür ist, dass mindestens ein Internet Gerät (z. b. eine Firewall oder ein Router) zwischen Ihrem Computer und dem VPN-Server nicht so konfiguriert ist, dass GRE-Protokoll Pakete (Generic Routing Kapseln) zugelassen werden.<br/>
<blockquote>
[!Note]<br />
Unterstützt in Windows Vista und höheren Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_VPN_DISCONNECT"></span><span id="error_vpn_disconnect"></span><dl> <dt><strong>ERROR_VPN_DISCONNECT</strong></dt> <dt>807</dt> </dl></td>
<td>Die Netzwerkverbindung zwischen Ihrem Computer und dem VPN-Server wurde unterbrochen. Dies kann durch ein Problem bei der VPN-Übertragung verursacht werden und ist in der Regel das Ergebnis der Internet Latenz oder einfach, dass Ihr VPN-Server die Kapazität erreicht hat. Versuchen Sie, erneut eine Verbindung mit dem VPN-Server herzustellen.<br/>
<blockquote>
[!Note]<br />
Unterstützt in Windows Vista und höheren Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_VPN_REFUSED"></span><span id="error_vpn_refused"></span><dl> <dt><strong>ERROR_VPN_REFUSED</strong></dt> <dt>808</dt> </dl></td>
<td>Die Netzwerkverbindung zwischen Ihrem Computer und dem VPN-Server konnte nicht hergestellt werden, da der Remote Server die Verbindung verweigert hat. Dies wird in der Regel durch einen Konflikt zwischen der Serverkonfiguration und den Verbindungseinstellungen verursacht.<br/>
<blockquote>
[!Note]<br />
Unterstützt in Windows Vista und höheren Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_VPN_TIMEOUT"></span><span id="error_vpn_timeout"></span><dl> <dt><strong>ERROR_VPN_TIMEOUT</strong></dt> <dt>809</dt> </dl></td>
<td>Die Netzwerkverbindung zwischen Ihrem Computer und dem VPN-Server konnte nicht hergestellt werden, da der Remote Server nicht antwortet. Dies liegt möglicherweise daran, dass eines der Netzwerkgeräte (z. b. Firewalls, NAT, Router) zwischen Ihrem Computer und dem Remote Server nicht für das Zulassen von VPN-Verbindungen konfiguriert ist.<br/>
<blockquote>
[!Note]<br />
Unterstützt in Windows Vista und höheren Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_VPN_BAD_CERT"></span><span id="error_vpn_bad_cert"></span><dl> <dt><strong>ERROR_VPN_BAD_CERT</strong></dt> <dt>810</dt> </dl></td>
<td>Eine Netzwerkverbindung zwischen Ihrem Computer und dem VPN-Server wurde gestartet, aber die VPN-Verbindung wurde nicht abgeschlossen. Dies wird in der Regel durch die Verwendung eines falschen oder abgelaufenen Zertifikats für die Authentifizierung zwischen dem Client und dem Server verursacht.<br/>
<blockquote>
[!Note]<br />
Unterstützt in Windows Vista und höheren Versionen von Windows
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_VPN_BAD_PSK"></span><span id="error_vpn_bad_psk"></span><dl> <dt><strong>ERROR_VPN_BAD_PSK</strong></dt> <dt>811</dt> </dl></td>
<td>Die Netzwerkverbindung zwischen Ihrem Computer und dem VPN-Server konnte nicht hergestellt werden, da der Remote Server nicht antwortet. Dies wird in der Regel durch ein Problem vor dem gemeinsamen Schlüssel zwischen Client und Server verursacht. Ein vorinstaltzter Schlüssel wird verwendet, um sicherzustellen, dass Sie sich in einem Kommunikations Zeitraum von IP-Sicherheit (IPSec) befinden.<br/>
<blockquote>
[!Note]<br />
Unterstützt in Windows Vista und höheren Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_SERVER_POLICY"></span><span id="error_server_policy"></span><dl> <dt><strong>ERROR_SERVER_POLICY</strong></dt> <dt>812</dt> </dl></td>
<td>Die Verbindung wurde aufgrund einer auf dem RAS-/VPN-Server konfigurierten Richtlinie verhindert. Insbesondere die Authentifizierungsmethode, die vom Server zum Überprüfen Ihres Benutzernamens und Kennworts verwendet wird, stimmt möglicherweise nicht mit der Authentifizierungsmethode, die in Ihrem Verbindungsprofil konfiguriert ist<br/>
<blockquote>
[!Note]<br />
Unterstützt in Windows Vista und höheren Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_BROADBAND_ACTIVE"></span><span id="error_broadband_active"></span><dl> <dt><strong>ERROR_BROADBAND_ACTIVE</strong></dt> <dt>813</dt> </dl></td>
<td>Sie haben versucht, eine zweite Breitbandverbindung herzustellen, während eine vorherige Breitbandverbindung bereits über das gleiche Gerät oder den gleichen Port hergestellt wurde.<br/>
<blockquote>
[!Note]<br />
Unterstützt in Windows Vista und höheren Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_BROADBAND_NO_NIC"></span><span id="error_broadband_no_nic"></span><dl> <dt><strong>ERROR_BROADBAND_NO_NIC</strong></dt> <dt>814</dt> </dl></td>
<td>Die zugrunde liegende Ethernet-Konnektivität, die für die Breitbandverbindung erforderlich ist, wurde nicht gefunden.<br/>
<blockquote>
[!Note]<br />
Unterstützt in Windows Vista und höheren Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_BROADBAND_TIMEOUT"></span><span id="error_broadband_timeout"></span><dl> <dt><strong>ERROR_BROADBAND_TIMEOUT</strong></dt> <dt>815</dt> </dl></td>
<td>Die Breitband Netzwerkverbindung konnte nicht auf dem Computer hergestellt werden, da der Remote Server nicht antwortet. Dies kann auf einen Wert zurückzuführen sein, der für das Feld ' Dienst Name ' für diese Verbindung nicht gültig ist.<br/>
<blockquote>
[!Note]<br />
Unterstützt in Windows Vista und höheren Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_FEATURE_DEPRECATED"></span><span id="error_feature_deprecated"></span><dl> <dt><strong>ERROR_FEATURE_DEPRECATED</strong></dt> <dt>816</dt> </dl></td>
<td>Ein Feature oder eine Einstellung, die Sie aktivieren möchten, wird vom Remote Zugriffs Dienst nicht mehr unterstützt.<br/>
<blockquote>
[!Note]<br />
Unterstützt in Windows Vista und höheren Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CANNOT_DELETE"></span><span id="error_cannot_delete"></span><dl> <dt><strong>ERROR_CANNOT_DELETE</strong></dt> <dt>817</dt> </dl></td>
<td>Eine Verbindung kann nicht gelöscht werden, wenn Sie verbunden ist.<br/>
<blockquote>
[!Note]<br />
Unterstützt in Windows Vista und höheren Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_RASQEC_RESOURCE_CREATION_FAILED"></span><span id="error_rasqec_resource_creation_failed"></span><dl> <dt><strong>ERROR_RASQEC_RESOURCE_CREATION_FAILED</strong></dt> <dt>818</dt> </dl></td>
<td>Der NAP-Erzwingungs Client konnte keine Systemressourcen für RAS-Verbindungen erstellen. Einige Netzwerkdienste oder Ressourcen sind möglicherweise nicht verfügbar.<br/>
<blockquote>
[!Note]<br />
Unterstützt in Windows Vista und höheren Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_RASQEC_NAPAGENT_NOT_ENABLED"></span><span id="error_rasqec_napagent_not_enabled"></span><dl> <dt><strong>ERROR_RASQEC_NAPAGENT_NOT_ENABLED</strong></dt> <dt>819</dt> </dl></td>
<td>Der Dienst für den Netzwerk Zugriffsschutz-Agent (NAP-Agent) wurde deaktiviert oder ist nicht auf diesem Computer installiert. Einige Netzwerkdienste oder Ressourcen sind möglicherweise nicht verfügbar.<br/>
<blockquote>
[!Note]<br />
Unterstützt in Windows Vista und höheren Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_RASQEC_NAPAGENT_NOT_CONNECTED"></span><span id="error_rasqec_napagent_not_connected"></span><dl> <dt><strong>ERROR_RASQEC_NAPAGENT_NOT_CONNECTED</strong></dt> <dt>820</dt> </dl></td>
<td>Der NAP-Erzwingungs Client konnte beim Netzwerk Zugriffsschutz-Agent-Dienst (NAP-Agent) nicht registriert werden. Einige Netzwerkdienste oder Ressourcen sind möglicherweise nicht verfügbar.<br/>
<blockquote>
[!Note]<br />
Unterstützt in Windows Vista und höheren Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_RASQEC_CONN_DOESNOTEXIST"></span><span id="error_rasqec_conn_doesnotexist"></span><dl> <dt><strong>ERROR_RASQEC_CONN_DOESNOTEXIST</strong></dt> <dt>821</dt> </dl></td>
<td>Der NAP-Erzwingungs Client konnte die Anforderung nicht verarbeiten, da die Remote Zugriffs Verbindung nicht vorhanden ist.<br/>
<blockquote>
[!Note]<br />
Unterstützt in Windows Vista und höheren Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_RASQEC_TIMEOUT"></span><span id="error_rasqec_timeout"></span><dl> <dt><strong>ERROR_RASQEC_TIMEOUT</strong></dt> <dt>822</dt> </dl></td>
<td>Der NAP-Erzwingungs Client hat nicht geantwortet. Einige Netzwerkdienste oder Ressourcen sind möglicherweise nicht verfügbar.<br/>
<blockquote>
[!Note]<br />
Unterstützt in Windows Vista und höheren Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PEAP_CRYPTOBINDING_INVALID"></span><span id="error_peap_cryptobinding_invalid"></span><dl> <dt><strong>ERROR_PEAP_CRYPTOBINDING_INVALID</strong></dt> <dt>823</dt> </dl></td>
<td>Der empfangene Crypto-Binding Type-Length-Value (TLV) ist ungültig.<br/>
<blockquote>
[!Note]<br />
Unterstützt in Windows Vista und höheren Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PEAP_CRYPTOBINDING_NOTRECEIVED"></span><span id="error_peap_cryptobinding_notreceived"></span><dl> <dt><strong>ERROR_PEAP_CRYPTOBINDING_NOTRECEIVED</strong></dt> <dt>824</dt> </dl></td>
<td>Crypto-Binding TLV wurde nicht empfangen.<br/>
<blockquote>
[!Note]<br />
Unterstützt in Windows Vista und höheren Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_VPNSTRATEGY"></span><span id="error_invalid_vpnstrategy"></span><dl> <dt><strong>ERROR_INVALID_VPNSTRATEGY</strong></dt> <dt>825</dt> </dl></td>
<td>Das Point-to-Point-Tunnelingprotokoll (PPTP) ist mit IPv6 nicht kompatibel. Ändern Sie den Typ des virtuellen privaten Netzwerks in das Layer-Two-Tunnelingprotokoll (L2TP).<br/>
<blockquote>
[!Note]<br />
Unterstützt in Windows Vista und höheren Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAPTLS_CACHE_CREDENTIALS_INVALID"></span><span id="error_eaptls_cache_credentials_invalid"></span><dl> <dt><strong>ERROR_EAPTLS_CACHE_CREDENTIALS_INVALID</strong></dt> <dt>826</dt> </dl></td>
<td>Fehler bei der eaptls-Überprüfung der zwischengespeicherten Anmelde Informationen. Verwerfen von zwischengespeicherten Anmelde Informationen.<br/>
<blockquote>
[!Note]<br />
Unterstützt in Windows Vista und höheren Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_IPSEC_SERVICE_STOPPED"></span><span id="error_ipsec_service_stopped"></span><dl> <dt><strong>ERROR_IPSEC_SERVICE_STOPPED</strong></dt> <dt>827</dt> </dl></td>
<td>Die L2TP/IPSec-Verbindung kann nicht hergestellt werden, weil der IKE-und AuthIP IPsec-Schlüssel für die IPSec-Schlüssel Erstellung und/oder der basisfilterungsmoduldienst nicht ausgeführt wird Diese Dienste sind erforderlich, um eine L2TP/IPSec-Verbindung herzustellen.<br/>
<blockquote>
[!Note]<br />
Unterstützt in Windows Vista und höheren Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_IDLE_TIMEOUT"></span><span id="error_idle_timeout"></span><dl> <dt><strong>ERROR_IDLE_TIMEOUT</strong></dt> <dt>828</dt> </dl></td>
<td>Die Verbindung wurde aufgrund eines Leerlauf Timeouts beendet.<br/>
<blockquote>
[!Note]<br />
Unterstützt in Windows Vista und höheren Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_LINK_FAILURE"></span><span id="error_link_failure"></span><dl> <dt><strong>ERROR_LINK_FAILURE</strong></dt> <dt>829</dt> </dl></td>
<td>Das Modem (oder ein anderes Verbindungsgerät) wurde aufgrund eines Verbindungsfehlers getrennt.<br/>
<blockquote>
[!Note]<br />
Unterstützt in Windows Vista und höheren Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_USER_LOGOFF"></span><span id="error_user_logoff"></span><dl> <dt><strong>ERROR_USER_LOGOFF</strong></dt> <dt>830</dt> </dl></td>
<td>Die Verbindung wurde beendet, weil der Benutzer abgemeldet hat.<br/>
<blockquote>
[!Note]<br />
Unterstützt in Windows Vista und höheren Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_FAST_USER_SWITCH"></span><span id="error_fast_user_switch"></span><dl> <dt><strong>ERROR_FAST_USER_SWITCH</strong></dt> <dt>831</dt> </dl></td>
<td>Die Verbindung wurde beendet, weil der Benutzer Switch aufgetreten ist.<br/>
<blockquote>
[!Note]<br />
Unterstützt in Windows Vista und höheren Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_HIBERNATION"></span><span id="error_hibernation"></span><dl> <dt><strong>ERROR_HIBERNATION</strong></dt> <dt>832</dt> </dl></td>
<td>Die Verbindung wurde aufgrund des Ruhe Zustands beendet.<br/>
<blockquote>
[!Note]<br />
Unterstützt in Windows Vista und höheren Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SYSTEM_SUSPENDED"></span><span id="error_system_suspended"></span><dl> <dt><strong>ERROR_SYSTEM_SUSPENDED</strong></dt> <dt>833</dt> </dl></td>
<td>Die Verbindung wurde beendet, weil das System angehalten wurde.<br/>
<blockquote>
[!Note]<br />
Unterstützt in Windows Vista und höheren Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_RASMAN_SERVICE_STOPPED"></span><span id="error_rasman_service_stopped"></span><dl> <dt><strong>ERROR_RASMAN_SERVICE_STOPPED</strong></dt> <dt>834</dt> </dl></td>
<td>Die Verbindung wurde beendet, weil der RAS-Verbindungs-Manager angehalten wurde.<br/>
<blockquote>
[!Note]<br />
Unterstützt in Windows Vista und höheren Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_SERVER_CERT"></span><span id="error_invalid_server_cert"></span><dl> <dt><strong>ERROR_INVALID_SERVER_CERT</strong></dt> <dt>835</dt> </dl></td>
<td>Der L2TP-Verbindungsversuch ist fehlgeschlagen, da die Sicherheitsebene den Remote Computer nicht authentifizieren konnte. Dies kann daran liegen, dass mindestens ein Feld des Zertifikats, das vom Remote Server vorgelegt wurde, nicht als Teil des Ziel Ziels überprüft werden konnte.<br/>
<blockquote>
[!Note]<br />
Unterstützt in Windows Vista und höheren Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NOT_NAP_CAPABLE"></span><span id="error_not_nap_capable"></span><dl> <dt><strong>ERROR_NOT_NAP_CAPABLE</strong></dt> <dt>836</dt> </dl></td>
<td>Der Computer ist nicht NAP-fähig.<br/>
<blockquote>
[!Note]<br />
Unterstützt in Windows Vista und höheren Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_TUNNELID"></span><span id="error_invalid_tunnelid"></span><dl> <dt><strong>ERROR_INVALID_TUNNELID</strong></dt> <dt>837</dt> </dl></td>
<td>Ungültige Tunnel-ID.<br/>
<blockquote>
[!Note]<br />
Wird in Windows 7 und höheren Versionen von Windows unterstützt.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_UPDATECONNECTION_REQUEST_IN_PROCESS"></span><span id="error_updateconnection_request_in_process"></span><dl> <dt><strong>ERROR_UPDATECONNECTION_REQUEST_IN_PROCESS</strong></dt> <dt>838</dt> </dl></td>
<td>Eine weitere Aktualisierungs Verbindungsanforderung wird ausgeführt. RAS ermöglicht jeweils nur eine Anforderung zum Aktualisieren der Verbindung.<br/>
<blockquote>
[!Note]<br />
Wird in Windows 7 und höheren Versionen von Windows unterstützt.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PROTOCOL_ENGINE_DISABLED"></span><span id="error_protocol_engine_disabled"></span><dl> <dt><strong>ERROR_PROTOCOL_ENGINE_DISABLED</strong></dt> <dt>839</dt> </dl></td>
<td>Das Aushandeln mithilfe des konfigurierten Protokolls ist deaktiviert. Bearbeiten Sie Verbindungs Eigenschaften, wählen Sie ein anderes Protokoll für die Aushandlung aus, und versuchen Sie es<br/>
<blockquote>
[!Note]<br />
Wird in Windows 7 und höheren Versionen von Windows unterstützt.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INTERNAL_ADDRESS_FAILURE"></span><span id="error_internal_address_failure"></span><dl> <dt><strong>ERROR_INTERNAL_ADDRESS_FAILURE</strong></dt> <dt>840</dt> </dl></td>
<td>Fehler bei der internen Adress Aushandlung.<br/>
<blockquote>
[!Note]<br />
Wird in Windows 7 und höheren Versionen von Windows unterstützt.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_FAILED_CP_REQUIRED"></span><span id="error_failed_cp_required"></span><dl> <dt><strong>ERROR_FAILED_CP_REQUIRED</strong></dt> <dt>841</dt> </dl></td>
<td>Der Client muss eine interne IPv4-oder IPv6-Adresse anfordern.<br/>
<blockquote>
[!Note]<br />
Wird in Windows 7 und höheren Versionen von Windows unterstützt.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_TS_UNACCEPTABLE"></span><span id="error_ts_unacceptable"></span><dl> <dt><strong>ERROR_TS_UNACCEPTABLE</strong></dt> <dt>842</dt> </dl></td>
<td>Fehler bei der Aushandlung von datenverkehrselektoren.<br/>
<blockquote>
[!Note]<br />
Wird in Windows 7 und höheren Versionen von Windows unterstützt.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_MOBIKE_DISABLED"></span><span id="error_mobike_disabled"></span><dl> <dt><strong>ERROR_MOBIKE_DISABLED</strong></dt> <dt>843</dt> </dl></td>
<td>Mobilität ist für diese Verbindung deaktiviert.<br/>
<blockquote>
[!Note]<br />
Wird in Windows 7 und höheren Versionen von Windows unterstützt.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_CANNOT_INITIATE_MOBIKE_UPDATE"></span><span id="error_cannot_initiate_mobike_update"></span><dl> <dt><strong>ERROR_CANNOT_INITIATE_MOBIKE_UPDATE</strong></dt> <dt>844</dt> </dl></td>
<td>Die VPN-Verbindung wird aufgrund einer Änderung des Quarantäne Zustands weiterhin hergestellt oder erneut authentifiziert. Initiieren Sie das Mobile Update nur, wenn der Verbindungsstatus "verbunden" lautet.<br/>
<blockquote>
[!Note]<br />
Wird in Windows 7 und höheren Versionen von Windows unterstützt.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PEAP_SERVER_REJECTED_CLIENT_TLV"></span><span id="error_peap_server_rejected_client_tlv"></span><dl> <dt><strong>ERROR_PEAP_SERVER_REJECTED_CLIENT_TLV</strong></dt> <dt>845</dt> </dl></td>
<td>Der Server hat die Client Authentifizierung aufgrund eines unerwarteten TLV-Fehlers oder eines nicht übereinstimmenden Werts für ein TLV abgelehnt.<br/>
<blockquote>
[!Note]<br />
Wird in Windows 7 und höheren Versionen von Windows unterstützt.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INVALID_PREFERENCES"></span><span id="error_invalid_preferences"></span><dl> <dt><strong>ERROR_INVALID_PREFERENCES</strong></dt> <dt>846</dt> </dl></td>
<td>Entweder wird die VPN-Zieleinstellung nicht vom Benutzer ausgewählt, oder Sie ist nicht mehr gültig.<br/>
<blockquote>
[!Note]<br />
Wird in Windows 7 und höheren Versionen von Windows unterstützt.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAPTLS_SCARD_CACHE_CREDENTIALS_INVALID"></span><span id="error_eaptls_scard_cache_credentials_invalid"></span><dl> <dt><strong>ERROR_EAPTLS_SCARD_CACHE_CREDENTIALS_INVALID</strong></dt> <dt>847</dt> </dl></td>
<td>Die zwischengespeicherten Smartcard-Anmelde Informationen sind ungültig.<br/>
<blockquote>
[!Note]<br />
Wird in Windows 7 und höheren Versionen von Windows unterstützt.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_SSTP_COOKIE_SET_FAILURE"></span><span id="error_sstp_cookie_set_failure"></span><dl> <dt><strong>ERROR_SSTP_COOKIE_SET_FAILURE</strong></dt> <dt>848</dt> </dl></td>
<td>Fehler beim VPN-Verbindungsversuch aufgrund eines internen Fehlers beim Hinzufügen von Cookies zum Secure Socket Tunnelung-Protokoll (SSTP). Ausführliche Informationen finden Sie im System Ereignisprotokoll.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_PEAP_COOKIE_ATTRIBUTES"></span><span id="error_invalid_peap_cookie_attributes"></span><dl> <dt><strong>ERROR_INVALID_PEAP_COOKIE_ATTRIBUTES</strong></dt> <dt>849</dt> </dl></td>
<td>Die im Cookie gespeicherten Methoden der inneren (n) Peer-Methode sind/sind ungültig.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAP_METHOD_NOT_INSTALLED"></span><span id="error_eap_method_not_installed"></span><dl> <dt><strong>ERROR_EAP_METHOD_NOT_INSTALLED</strong></dt> <dt>850</dt> </dl></td>
<td>Der für die Authentifizierung der Remote Zugriffs Verbindung erforderliche erweiterbare Authentifizierungs Protokolltyp ist nicht auf dem Computer installiert.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAP_METHOD_DOES_NOT_SUPPORT_SSO"></span><span id="error_eap_method_does_not_support_sso"></span><dl> <dt><strong>ERROR_EAP_METHOD_DOES_NOT_SUPPORT_SSO</strong></dt> <dt>851</dt> </dl></td>
<td>Der für die Remote Zugriffs Verbindung konfigurierte erweiterbare Authentifizierungs Protokolltyp unterstützt Single Sign-on nicht.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAP_METHOD_OPERATION_NOT_SUPPORTED"></span><span id="error_eap_method_operation_not_supported"></span><dl> <dt><strong>ERROR_EAP_METHOD_OPERATION_NOT_SUPPORTED</strong></dt> <dt>852</dt> </dl></td>
<td>Der angeforderte Vorgang wird vom Extensible Authentication-Protokolltyp, der für die Remote Zugriffs Verbindung konfiguriert ist, nicht unterstützt.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAP_USER_CERT_INVALID"></span><span id="error_eap_user_cert_invalid"></span><dl> <dt><strong>ERROR_EAP_USER_CERT_INVALID</strong></dt> <dt>853</dt> </dl></td>
<td>Die Remote Zugriffs Verbindung wurde abgeschlossen, aber die Authentifizierung ist fehlgeschlagen, da das Zertifikat, mit dem der Client beim Server authentifiziert wird, ungültig ist. Stellen Sie sicher, dass das für die Authentifizierung verwendete Zertifikat gültig ist.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAP_USER_CERT_EXPIRED"></span><span id="error_eap_user_cert_expired"></span><dl> <dt><strong>ERROR_EAP_USER_CERT_EXPIRED</strong></dt> <dt>854</dt> </dl></td>
<td>Die Remote Zugriffs Verbindung wurde abgeschlossen, aber die Authentifizierung ist fehlgeschlagen, da das Zertifikat, mit dem der Client beim Server authentifiziert wird, abgelaufen ist. Erneuern Sie das Zertifikat.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAP_USER_CERT_REVOKED"></span><span id="error_eap_user_cert_revoked"></span><dl> <dt><strong>ERROR_EAP_USER_CERT_REVOKED</strong></dt> <dt>855</dt> </dl></td>
<td>Die Remote Zugriffs Verbindung wurde abgeschlossen, aber die Authentifizierung ist fehlgeschlagen, da das Zertifikat, mit dem der Client beim Server authentifiziert wird, gesperrt ist. Verwenden Sie ein Zertifikat, das nicht widerrufen wurde.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAP_USER_CERT_OTHER_ERROR"></span><span id="error_eap_user_cert_other_error"></span><dl> <dt><strong>ERROR_EAP_USER_CERT_OTHER_ERROR</strong></dt> <dt>856</dt> </dl></td>
<td>Die Remote Zugriffs Verbindung wurde abgeschlossen, aber die Authentifizierung ist aufgrund eines Fehlers im Zertifikat, mit dem der Client beim Server authentifiziert wird, fehlgeschlagen.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAP_SERVER_CERT_INVALID"></span><span id="error_eap_server_cert_invalid"></span><dl> <dt><strong>ERROR_EAP_SERVER_CERT_INVALID</strong></dt> <dt>857</dt> </dl></td>
<td>Die Remote Zugriffs Verbindung wurde abgeschlossen, aber die Authentifizierung ist fehlgeschlagen, da das Zertifikat, das der Client zum Authentifizieren des Servers verwendet, ungültig ist.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAP_SERVER_CERT_EXPIRED"></span><span id="error_eap_server_cert_expired"></span><dl> <dt><strong>ERROR_EAP_SERVER_CERT_EXPIRED</strong></dt> <dt>858</dt> </dl></td>
<td>Die Remote Zugriffs Verbindung wurde abgeschlossen, aber die Authentifizierung ist fehlgeschlagen, da das Zertifikat, das der Client zum Authentifizieren des Servers verwendet, abgelaufen ist.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAP_SERVER_CERT_REVOKED"></span><span id="error_eap_server_cert_revoked"></span><dl> <dt><strong>ERROR_EAP_SERVER_CERT_REVOKED</strong></dt> <dt>859</dt> </dl></td>
<td>Die Remote Zugriffs Verbindung wurde abgeschlossen, aber die Authentifizierung ist fehlgeschlagen, da das Zertifikat, das der Client zum Authentifizieren des Servers verwendet, gesperrt wird.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAP_SERVER_CERT_OTHER_ERROR"></span><span id="error_eap_server_cert_other_error"></span><dl> <dt><strong>ERROR_EAP_SERVER_CERT_OTHER_ERROR</strong></dt> <dt>860</dt> </dl></td>
<td>Die Remote Zugriffs Verbindung wurde abgeschlossen, aber die Authentifizierung ist aufgrund eines Fehlers im Zertifikat, das der Client zum Authentifizieren des Servers verwendet, fehlgeschlagen.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAP_USER_ROOT_CERT_NOT_FOUND"></span><span id="error_eap_user_root_cert_not_found"></span><dl> <dt><strong>ERROR_EAP_USER_ROOT_CERT_NOT_FOUND</strong></dt> <dt>861</dt> </dl></td>
<td>Die Remote Zugriffs Verbindung wurde abgeschlossen, aber die Authentifizierung ist fehlgeschlagen, da ein vertrauenswürdiges Stamm Zertifikat, das das Benutzerzertifikat überprüft, nicht im Zertifikat Speicher der vertrauenswürdigen Stamm Zertifizierungsstellen gefunden wurde.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAP_USER_ROOT_CERT_INVALID"></span><span id="error_eap_user_root_cert_invalid"></span><dl> <dt><strong>ERROR_EAP_USER_ROOT_CERT_INVALID</strong></dt> <dt>862</dt> </dl></td>
<td>Die Remote Zugriffs Verbindung wurde abgeschlossen, aber die Authentifizierung ist fehlgeschlagen, weil das vertrauenswürdige Stamm Zertifikat, das zum Überprüfen des Benutzer Zertifikats verwendet wird, ungültig ist.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAP_USER_ROOT_CERT_EXPIRED"></span><span id="error_eap_user_root_cert_expired"></span><dl> <dt><strong>ERROR_EAP_USER_ROOT_CERT_EXPIRED</strong></dt> <dt>863</dt> </dl></td>
<td>Die Remote Zugriffs Verbindung wurde abgeschlossen, aber die Authentifizierung ist fehlgeschlagen, da das Zertifikat im Zertifikat Speicher für vertrauenswürdige Stamm Zertifizierungsstellen, von dem das Benutzerzertifikat authentifiziert wird, abgelaufen ist. Erneuern Sie das Zertifikat.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAP_SERVER_ROOT_CERT_NOT_FOUND"></span><span id="error_eap_server_root_cert_not_found"></span><dl> <dt><strong>ERROR_EAP_SERVER_ROOT_CERT_NOT_FOUND</strong></dt> <dt>864</dt> </dl></td>
<td>Die Remote Zugriffs Verbindung wurde abgeschlossen, aber die Authentifizierung ist fehlgeschlagen, da ein Zertifikat, das das Serverzertifikat überprüft, im Zertifikat Speicher der vertrauenswürdigen Stamm Zertifizierungsstellen nicht gefunden wurde.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAP_SERVER_ROOT_CERT_INVALID"></span><span id="error_eap_server_root_cert_invalid"></span><dl> <dt><strong>ERROR_EAP_SERVER_ROOT_CERT_INVALID</strong></dt> <dt>865</dt> </dl></td>
<td>Die Remote Zugriffs Verbindung wurde abgeschlossen, aber die Authentifizierung ist fehlgeschlagen, da das Zertifikat im Zertifikat Speicher der vertrauenswürdigen Stamm Zertifizierungsstellen, der das Serverzertifikat überprüft, ungültig ist.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAP_SERVER_ROOT_CERT_NAME_REQUIRED"></span><span id="error_eap_server_root_cert_name_required"></span><dl> <dt><strong>ERROR_EAP_SERVER_ROOT_CERT_NAME_REQUIRED</strong></dt> <dt>866</dt> </dl></td>
<td>Die Remote Zugriffs Verbindung wurde abgeschlossen, aber die Authentifizierung ist fehlgeschlagen, da für das Zertifikat auf dem Server Computer kein Servername angegeben wurde.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PEAP_IDENTITY_MISMATCH"></span><span id="error_peap_identity_mismatch"></span><dl> <dt><strong>ERROR_PEAP_IDENTITY_MISMATCH</strong></dt> <dt>867</dt> </dl></td>
<td>Die äußere Identität von Peer ist nicht mit der inneren Identität identisch, wenn der Identitätsschutz deaktiviert ist.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DNSNAME_NOT_RESOLVABLE"></span><span id="error_dnsname_not_resolvable"></span><dl> <dt><strong>ERROR_DNSNAME_NOT_RESOLVABLE</strong></dt> <dt>868</dt> </dl></td>
<td>Die Remote Verbindung wurde nicht hergestellt, weil der Name des Remote Zugriffs Servers nicht aufgelöst wurde.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAPTLS_PASSWD_INVALID"></span><span id="error_eaptls_passwd_invalid"></span><dl> <dt><strong>ERROR_EAPTLS_PASSWD_INVALID</strong></dt> <dt>869</dt> </dl></td>
<td>Das für das Zertifikat angegebene Kennwort ist ungültig.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_IKEV2_PSK_INTERFACE_ALREADY_EXISTS"></span><span id="error_ikev2_psk_interface_already_exists"></span><dl> <dt><strong>ERROR_IKEV2_PSK_INTERFACE_ALREADY_EXISTS</strong></dt> <dt>870</dt> </dl></td>
<td>Die Schnittstelle konnte nicht aktiviert werden, da mehr als eine Schnittstelle mit dem gleichen Ziel mit der Authentifizierungsmethode vor dem gemeinsamen Schlüssel erstellt wurde. Ändern Sie die Ziel-/auth-Methode, und aktivieren Sie die Schnittstelle.<br/></td>
</tr>
</tbody>
</table>



 

Die folgenden Fehlercodes für die Routing-und RAS-API (RRAS) werden in "mprerror. h" definiert. Alle Fehlercodes werden in Windows 2000 oder höheren Versionen von Windows unterstützt, sofern nicht anders angegeben.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Rückgabecode/-wert</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="ERROR_ROUTER_STOPPED"></span><span id="error_router_stopped"></span><dl> <dt><strong>ERROR_ROUTER_STOPPED</strong></dt> <dt>900</dt> </dl></td>
<td>Der Router wird nicht ausgeführt.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_ALREADY_CONNECTED"></span><span id="error_already_connected"></span><dl> <dt><strong>ERROR_ALREADY_CONNECTED</strong></dt> <dt>901</dt> </dl></td>
<td>Die Schnittstelle ist bereits verbunden.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_UNKNOWN_PROTOCOL_ID"></span><span id="error_unknown_protocol_id"></span><dl> <dt><strong>ERROR_UNKNOWN_PROTOCOL_ID</strong></dt> <dt>902</dt> </dl></td>
<td>Der angegebene Protokoll Bezeichner ist dem Router nicht bekannt.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_DDM_NOT_RUNNING"></span><span id="error_ddm_not_running"></span><dl> <dt><strong>ERROR_DDM_NOT_RUNNING</strong></dt> <dt>903</dt> </dl></td>
<td>Der DDM (Demand-Dial Interface Manager) wird nicht ausgeführt.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INTERFACE_ALREADY_EXISTS"></span><span id="error_interface_already_exists"></span><dl> <dt><strong>ERROR_INTERFACE_ALREADY_EXISTS</strong></dt> <dt>904</dt> </dl></td>
<td>Eine Schnittstelle mit diesem Namen ist bereits beim Router registriert.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_SUCH_INTERFACE"></span><span id="error_no_such_interface"></span><dl> <dt><strong>ERROR_NO_SUCH_INTERFACE</strong></dt> <dt>905</dt> </dl></td>
<td>Eine Schnittstelle mit diesem Namen ist nicht beim Router registriert.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INTERFACE_NOT_CONNECTED"></span><span id="error_interface_not_connected"></span><dl> <dt><strong>ERROR_INTERFACE_NOT_CONNECTED</strong></dt> <dt>906</dt> </dl></td>
<td>Die Schnittstelle ist nicht verbunden.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PROTOCOL_STOP_PENDING"></span><span id="error_protocol_stop_pending"></span><dl> <dt><strong>ERROR_PROTOCOL_STOP_PENDING</strong></dt> <dt>907</dt> </dl></td>
<td>Das angegebene Protokoll wird angehalten.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INTERFACE_CONNECTED"></span><span id="error_interface_connected"></span><dl> <dt><strong>ERROR_INTERFACE_CONNECTED</strong></dt> <dt>908</dt> </dl></td>
<td>Die Schnittstelle ist verbunden und kann daher nicht gelöscht werden.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_INTERFACE_CREDENTIALS_SET"></span><span id="error_no_interface_credentials_set"></span><dl> <dt><strong>ERROR_NO_INTERFACE_CREDENTIALS_SET</strong></dt> <dt>909</dt> </dl></td>
<td>Die Anmelde Informationen für die Benutzeroberfläche wurden nicht festgelegt.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_ALREADY_CONNECTING"></span><span id="error_already_connecting"></span><dl> <dt><strong>ERROR_ALREADY_CONNECTING</strong></dt> <dt>910</dt> </dl></td>
<td>Diese Schnittstelle befindet sich bereits im Prozess der Verbindungs Herstellung.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_UPDATE_IN_PROGRESS"></span><span id="error_update_in_progress"></span><dl> <dt><strong>ERROR_UPDATE_IN_PROGRESS</strong></dt> <dt>911</dt> </dl></td>
<td>Ein Update der Routing Informationen für diese Schnittstelle wird bereits durchgeführt.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INTERFACE_CONFIGURATION"></span><span id="error_interface_configuration"></span><dl> <dt><strong>ERROR_INTERFACE_CONFIGURATION</strong></dt> <dt>912</dt> </dl></td>
<td>Die Schnittstellen Konfiguration ist ungültig. Es ist bereits eine andere Schnittstelle vorhanden, die mit derselben Schnittstelle auf dem Remote Router verbunden ist.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NOT_CLIENT_PORT"></span><span id="error_not_client_port"></span><dl> <dt><strong>ERROR_NOT_CLIENT_PORT</strong></dt> <dt>913</dt> </dl></td>
<td>Ein RAS-Client hat versucht, eine Verbindung über einen Port herzustellen, der nur für Router reserviert war.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NOT_ROUTER_PORT"></span><span id="error_not_router_port"></span><dl> <dt><strong>ERROR_NOT_ROUTER_PORT</strong></dt> <dt>914</dt> </dl></td>
<td>Ein Bedarfs gesteuerter wählrouter hat versucht, eine Verbindung über einen Port herzustellen, der nur für RAS-Clients reserviert war.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CLIENT_INTERFACE_ALREADY_EXISTS"></span><span id="error_client_interface_already_exists"></span><dl> <dt><strong>ERROR_CLIENT_INTERFACE_ALREADY_EXISTS</strong></dt> <dt>915</dt> </dl></td>
<td>Die Client Schnittstelle mit diesem Namen ist bereits vorhanden und zurzeit verbunden.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INTERFACE_DISABLED"></span><span id="error_interface_disabled"></span><dl> <dt><strong>ERROR_INTERFACE_DISABLED</strong></dt> <dt>916</dt> </dl></td>
<td>Die Schnittstelle befindet sich in einem deaktivierten Zustand.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_AUTH_PROTOCOL_REJECTED"></span><span id="error_auth_protocol_rejected"></span><dl> <dt><strong>ERROR_AUTH_PROTOCOL_REJECTED</strong></dt> <dt>917</dt> </dl></td>
<td>Das Authentifizierungsprotokoll wurde vom Remotepeer abgelehnt.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_AUTH_PROTOCOL_AVAILABLE"></span><span id="error_no_auth_protocol_available"></span><dl> <dt><strong>ERROR_NO_AUTH_PROTOCOL_AVAILABLE</strong></dt> <dt>918</dt> </dl></td>
<td>Es sind keine Authentifizierungsprotokolle zur Verwendung verfügbar.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PEER_REFUSED_AUTH"></span><span id="error_peer_refused_auth"></span><dl> <dt><strong>ERROR_PEER_REFUSED_AUTH</strong></dt> <dt>919</dt> </dl></td>
<td>Die Verbindung konnte nicht hergestellt werden, da das vom RAS/VPN-Server verwendete Authentifizierungsprotokoll zum Überprüfen des Benutzernamens und Kennworts nicht mit den Einstellungen in Ihrem Verbindungsprofil abgeglichen werden konnte.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_REMOTE_NO_DIALIN_PERMISSION"></span><span id="error_remote_no_dialin_permission"></span><dl> <dt><strong>ERROR_REMOTE_NO_DIALIN_PERMISSION</strong></dt> <dt>920</dt> </dl></td>
<td>Das Remote Konto verfügt nicht über die Remote Zugriffsberechtigung.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_REMOTE_PASSWD_EXPIRED"></span><span id="error_remote_passwd_expired"></span><dl> <dt><strong>ERROR_REMOTE_PASSWD_EXPIRED</strong></dt> <dt>921</dt> </dl></td>
<td>Das Remote Konto ist abgelaufen.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_REMOTE_ACCT_DISABLED"></span><span id="error_remote_acct_disabled"></span><dl> <dt><strong>ERROR_REMOTE_ACCT_DISABLED</strong></dt> <dt>922</dt> </dl></td>
<td>Das Remote Konto ist deaktiviert.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_REMOTE_RESTRICTED_LOGON_HOURS"></span><span id="error_remote_restricted_logon_hours"></span><dl> <dt><strong>ERROR_REMOTE_RESTRICTED_LOGON_HOURS</strong></dt> <dt>923</dt> </dl></td>
<td>Das Remote Konto darf sich zu diesem Zeitpunkt nicht anmelden.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_REMOTE_AUTHENTICATION_FAILURE"></span><span id="error_remote_authentication_failure"></span><dl> <dt><strong>ERROR_REMOTE_AUTHENTICATION_FAILURE</strong></dt> <dt>924</dt> </dl></td>
<td>Der Zugriff auf den Remotepeer wurde verweigert, da der Benutzername, das Kennwort oder beides in der Domäne nicht gültig ist.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INTERFACE_HAS_NO_DEVICES"></span><span id="error_interface_has_no_devices"></span><dl> <dt><strong>ERROR_INTERFACE_HAS_NO_DEVICES</strong></dt> <dt>925</dt> </dl></td>
<td>Es sind keine Ports für das Routing aktiviert, die von dieser Schnittstelle für die Bedarfs gesteuerte Verwendung verwendet werden können<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_IDLE_DISCONNECTED"></span><span id="error_idle_disconnected"></span><dl> <dt><strong>ERROR_IDLE_DISCONNECTED</strong></dt> <dt>926</dt> </dl></td>
<td>Der Port wurde aufgrund von Inaktivität getrennt.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INTERFACE_UNREACHABLE"></span><span id="error_interface_unreachable"></span><dl> <dt><strong>ERROR_INTERFACE_UNREACHABLE</strong></dt> <dt>927</dt> </dl></td>
<td>Die Schnittstelle ist zu diesem Zeitpunkt nicht erreichbar.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_SERVICE_IS_PAUSED"></span><span id="error_service_is_paused"></span><dl> <dt><strong>ERROR_SERVICE_IS_PAUSED</strong></dt> <dt>928</dt> </dl></td>
<td>Der Anforderungs wähldienst befindet sich im angehaltenen Zustand.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INTERFACE_DISCONNECTED"></span><span id="error_interface_disconnected"></span><dl> <dt><strong>ERROR_INTERFACE_DISCONNECTED</strong></dt> <dt>929</dt> </dl></td>
<td>Die Schnittstelle wurde vom Administrator getrennt.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_AUTH_SERVER_TIMEOUT"></span><span id="error_auth_server_timeout"></span><dl> <dt><strong>ERROR_AUTH_SERVER_TIMEOUT</strong></dt> <dt>930</dt> </dl></td>
<td>Der Authentifizierungsserver hat nicht rechtzeitig auf Authentifizierungsanforderungen reagiert.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PORT_LIMIT_REACHED"></span><span id="error_port_limit_reached"></span><dl> <dt><strong>ERROR_PORT_LIMIT_REACHED</strong></dt> <dt>931</dt> </dl></td>
<td>Die maximale Anzahl von Ports, die für die Verbindung mit mehreren verknüpften Verbindungen zulässig sind, wurde erreicht.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PPP_SESSION_TIMEOUT"></span><span id="error_ppp_session_timeout"></span><dl> <dt><strong>ERROR_PPP_SESSION_TIMEOUT</strong></dt> <dt>932</dt> </dl></td>
<td>Das Verbindungszeit Limit für den Benutzer wurde erreicht.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_MAX_LAN_INTERFACE_LIMIT"></span><span id="error_max_lan_interface_limit"></span><dl> <dt><strong>ERROR_MAX_LAN_INTERFACE_LIMIT</strong></dt> <dt>933</dt> </dl></td>
<td>Der maximale Grenzwert für die Anzahl der unterstützten LAN-Schnittstellen wurde erreicht.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_MAX_WAN_INTERFACE_LIMIT"></span><span id="error_max_wan_interface_limit"></span><dl> <dt><strong>ERROR_MAX_WAN_INTERFACE_LIMIT</strong></dt> <dt>934</dt> </dl></td>
<td>Der maximale Grenzwert für die Anzahl unterstützter Bedarfs gesteuerter Wähl Schnittstellen ist erreicht.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_MAX_CLIENT_INTERFACE_LIMIT"></span><span id="error_max_client_interface_limit"></span><dl> <dt><strong>ERROR_MAX_CLIENT_INTERFACE_LIMIT</strong></dt> <dt>935</dt> </dl></td>
<td>Der maximale Grenzwert für die Anzahl der unterstützten RAS-Clients wurde erreicht.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_BAP_DISCONNECTED"></span><span id="error_bap_disconnected"></span><dl> <dt><strong>ERROR_BAP_DISCONNECTED</strong></dt> <dt>936</dt> </dl></td>
<td>Der Port wurde aufgrund der Richtlinie für das Bandbreiten Zuweisungs Protokoll (BAP) getrennt.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_USER_LIMIT"></span><span id="error_user_limit"></span><dl> <dt><strong>ERROR_USER_LIMIT</strong></dt> <dt>937</dt> </dl></td>
<td>Da eine andere Verbindung Ihres Typs verwendet wird, kann die eingehende Verbindung die Verbindungsanforderung nicht akzeptieren.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_RADIUS_SERVERS"></span><span id="error_no_radius_servers"></span><dl> <dt><strong>ERROR_NO_RADIUS_SERVERS</strong></dt> <dt>938</dt> </dl></td>
<td>Im Netzwerk wurden keine RADIUS-Server gefunden.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_RADIUS_RESPONSE"></span><span id="error_invalid_radius_response"></span><dl> <dt><strong>ERROR_INVALID_RADIUS_RESPONSE</strong></dt> <dt>939</dt> </dl></td>
<td>Die vom RADIUS-Authentifizierungsserver empfangene Antwort war ungültig. Stellen Sie sicher, dass die Groß-/Kleinschreibung beachtet das Kennwort für den RADIUS-Server richtig festgelegt<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DIALIN_HOURS_RESTRICTION"></span><span id="error_dialin_hours_restriction"></span><dl> <dt><strong>ERROR_DIALIN_HOURS_RESTRICTION</strong></dt> <dt>940</dt> </dl></td>
<td>Sie verfügen zu diesem Zeitpunkt nicht über die Berechtigung zum Herstellen einer Verbindung.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_ALLOWED_PORT_TYPE_RESTRICTION"></span><span id="error_allowed_port_type_restriction"></span><dl> <dt><strong>ERROR_ALLOWED_PORT_TYPE_RESTRICTION</strong></dt> <dt>941</dt> </dl></td>
<td>Sie verfügen nicht über die Berechtigung zum Herstellen einer Verbindung mithilfe des aktuellen Gerätetyps.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_AUTH_PROTOCOL_RESTRICTION"></span><span id="error_auth_protocol_restriction"></span><dl> <dt><strong>ERROR_AUTH_PROTOCOL_RESTRICTION</strong></dt> <dt>942</dt> </dl></td>
<td>Die Verbindung konnte nicht hergestellt werden, da die Authentifizierungsmethode, die von Ihrem Verbindungsprofil verwendet wird, nicht für die Verwendung durch eine auf dem RAS/VPN-Server konfigurierte Zugriffs Richtlinie zulässig ist. Dies kann insbesondere auf Konfigurations Unterschiede zwischen der auf dem RAS/VPN-Server ausgewählten Authentifizierungsmethode und der Zugriffs Richtlinie zurückzuführen sein, die für den RAS-Server konfiguriert wurde.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_BAP_REQUIRED"></span><span id="error_bap_required"></span><dl> <dt><strong>ERROR_BAP_REQUIRED</strong></dt> <dt>943</dt> </dl></td>
<td>Für diesen Benutzer ist BAP erforderlich.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DIALOUT_HOURS_RESTRICTION"></span><span id="error_dialout_hours_restriction"></span><dl> <dt><strong>ERROR_DIALOUT_HOURS_RESTRICTION</strong></dt> <dt>944</dt> </dl></td>
<td>Es ist nicht zulässig, die Schnittstelle zu diesem Zeitpunkt zu verbinden.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_ROUTER_CONFIG_INCOMPATIBLE"></span><span id="error_router_config_incompatible"></span><dl> <dt><strong>ERROR_ROUTER_CONFIG_INCOMPATIBLE</strong></dt> <dt>945</dt> </dl></td>
<td>Die gespeicherte Routerkonfiguration ist mit dem aktuellen Router nicht kompatibel.<br/></td>
</tr>
<tr class="odd">
<td><span id="WARNING_NO_MD5_MIGRATION"></span><span id="warning_no_md5_migration"></span><dl> <dt><strong>WARNING_NO_MD5_MIGRATION</strong></dt> <dt>946</dt> </dl></td>
<td>Der Remote Zugriff hat Benutzerkonten älterer Formate erkannt, die nicht automatisch migriert werden.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PROTOCOL_ALREADY_INSTALLED"></span><span id="error_protocol_already_installed"></span><dl> <dt><strong>ERROR_PROTOCOL_ALREADY_INSTALLED</strong></dt> <dt>948</dt> </dl></td>
<td>Der Transport ist bereits mit dem Router installiert.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INVALID_SIGNATURE_LENGTH"></span><span id="error_invalid_signature_length"></span><dl> <dt><strong>ERROR_INVALID_SIGNATURE_LENGTH</strong></dt> <dt>949</dt> </dl></td>
<td>Die in einem Paket vom RADIUS-Server empfangene Signatur Länge ist ungültig.<br/>
<blockquote>
[!Note]<br />
Unterstützt in Windows XP und höheren Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_SIGNATURE"></span><span id="error_invalid_signature"></span><dl> <dt><strong>ERROR_INVALID_SIGNATURE</strong></dt> <dt>950</dt> </dl></td>
<td>Die in einem Paket vom RADIUS-Server empfangene Signatur ist ungültig.<br/>
<blockquote>
[!Note]<br />
Unterstützt in Windows XP und höheren Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_SIGNATURE"></span><span id="error_no_signature"></span><dl> <dt><strong>ERROR_NO_SIGNATURE</strong></dt> <dt>951</dt> </dl></td>
<td>Die Signatur wurde nicht zusammen mit eapmessage vom RADIUS-Server empfangen.<br/>
<blockquote>
[!Note]<br />
Unterstützt in Windows XP und höheren Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_PACKET_LENGTH_OR_ID"></span><span id="error_invalid_packet_length_or_id"></span><dl> <dt><strong>ERROR_INVALID_PACKET_LENGTH_OR_ID</strong></dt> <dt>952</dt> </dl></td>
<td>Die in einem Paket vom RADIUS-Server empfangene Länge oder ID ist ungültig.<br/>
<blockquote>
[!Note]<br />
Unterstützt in Windows XP und höheren Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INVALID_ATTRIBUTE_LENGTH"></span><span id="error_invalid_attribute_length"></span><dl> <dt><strong>ERROR_INVALID_ATTRIBUTE_LENGTH</strong></dt> <dt>953</dt> </dl></td>
<td>Die in einem Paket mit dem Attribut vom RADIUS-Server empfangene Länge ist ungültig.<br/>
<blockquote>
[!Note]<br />
Unterstützt in Windows XP und höheren Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_PACKET"></span><span id="error_invalid_packet"></span><dl> <dt><strong>ERROR_INVALID_PACKET</strong></dt> <dt>954</dt> </dl></td>
<td>Das vom RADIUS-Server empfangene Paket ist ungültig.<br/>
<blockquote>
[!Note]<br />
Unterstützt in Windows XP und höheren Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_AUTHENTICATOR_MISMATCH"></span><span id="error_authenticator_mismatch"></span><dl> <dt><strong>ERROR_AUTHENTICATOR_MISMATCH</strong></dt> <dt>955</dt> </dl></td>
<td>Der Authentifikator stimmt nicht mit dem Paket vom RADIUS-Server.<br/>
<blockquote>
[!Note]<br />
Unterstützt in Windows XP und höheren Versionen von Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_REMOTEACCESS_NOT_CONFIGURED"></span><span id="error_remoteaccess_not_configured"></span><dl> <dt><strong>ERROR_REMOTEACCESS_NOT_CONFIGURED</strong></dt> <dt>956</dt> </dl></td>
<td>Der Routing-und RAS-Server ist entweder nicht konfiguriert oder wird nicht ausgeführt.<br/>
<blockquote>
[!Note]<br />
Wird in Windows 7 und höheren Versionen von Windows unterstützt.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>       |



 

 





