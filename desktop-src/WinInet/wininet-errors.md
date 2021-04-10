---
title: Fehlermeldungen (WinInet. h)
description: In den WinInet-Funktionen werden ggf. Fehlercodes zurückgegeben. Die folgenden Fehler sind spezifisch für die WinInet-Funktionen.
ms.assetid: 338bf65f-ebe5-4434-8407-9ab2a4c8d381
topic_type:
- apiref
api_name:
- ERROR_FTP_DROPPED
- ERROR_FTP_NO_PASSIVE_MODE
- ERROR_FTP_TRANSFER_IN_PROGRESS
- ERROR_GOPHER_ATTRIBUTE_NOT_FOUND
- ERROR_GOPHER_DATA_ERROR
- ERROR_GOPHER_END_OF_DATA
- ERROR_GOPHER_INCORRECT_LOCATOR_TYPE
- ERROR_GOPHER_INVALID_LOCATOR
- ERROR_GOPHER_NOT_FILE
- ERROR_GOPHER_NOT_GOPHER_PLUS
- ERROR_GOPHER_PROTOCOL_ERROR
- ERROR_GOPHER_UNKNOWN_LOCATOR
- ERROR_HTTP_COOKIE_DECLINED
- ERROR_HTTP_COOKIE_NEEDS_CONFIRMATION
- ERROR_HTTP_DOWNLEVEL_SERVER
- ERROR_HTTP_HEADER_ALREADY_EXISTS
- ERROR_HTTP_HEADER_NOT_FOUND
- ERROR_HTTP_INVALID_HEADER
- ERROR_HTTP_INVALID_QUERY_REQUEST
- ERROR_HTTP_INVALID_SERVER_RESPONSE
- ERROR_HTTP_NOT_REDIRECTED
- ERROR_HTTP_REDIRECT_FAILED
- ERROR_HTTP_REDIRECT_NEEDS_CONFIRMATION
- ERROR_INTERNET_ASYNC_THREAD_FAILED
- ERROR_INTERNET_BAD_AUTO_PROXY_SCRIPT
- ERROR_INTERNET_BAD_OPTION_LENGTH
- ERROR_INTERNET_BAD_REGISTRY_PARAMETER
- ERROR_INTERNET_CANNOT_CONNECT
- ERROR_INTERNET_CHG_POST_IS_NON_SECURE
- ERROR_INTERNET_CLIENT_AUTH_CERT_NEEDED
- ERROR_INTERNET_CLIENT_AUTH_NOT_SETUP
- ERROR_INTERNET_CONNECTION_ABORTED
- ERROR_INTERNET_CONNECTION_RESET
- ERROR_INTERNET_DECODING_FAILED
- ERROR_INTERNET_DIALOG_PENDING
- ERROR_INTERNET_DISCONNECTED
- ERROR_INTERNET_EXTENDED_ERROR
- ERROR_INTERNET_FAILED_DUETOSECURITYCHECK
- ERROR_INTERNET_FORCE_RETRY
- ERROR_INTERNET_FORTEZZA_LOGIN_NEEDED
- ERROR_INTERNET_HANDLE_EXISTS
- ERROR_INTERNET_HTTP_TO_HTTPS_ON_REDIR
- ERROR_INTERNET_HTTPS_HTTP_SUBMIT_REDIR
- ERROR_INTERNET_HTTPS_TO_HTTP_ON_REDIR
- ERROR_INTERNET_INCORRECT_FORMAT
- ERROR_INTERNET_INCORRECT_HANDLE_STATE
- ERROR_INTERNET_INCORRECT_HANDLE_TYPE
- ERROR_INTERNET_INCORRECT_PASSWORD
- ERROR_INTERNET_INCORRECT_USER_NAME
- ERROR_INTERNET_INSERT_CDROM
- ERROR_INTERNET_INTERNAL_ERROR
- ERROR_INTERNET_INVALID_CA
- ERROR_INTERNET_INVALID_OPERATION
- ERROR_INTERNET_INVALID_OPTION
- ERROR_INTERNET_INVALID_PROXY_REQUEST
- ERROR_INTERNET_INVALID_URL
- ERROR_INTERNET_ITEM_NOT_FOUND
- ERROR_INTERNET_LOGIN_FAILURE
- ERROR_INTERNET_LOGIN_FAILURE_DISPLAY_ENTITY_BODY
- ERROR_INTERNET_MIXED_SECURITY
- ERROR_INTERNET_NAME_NOT_RESOLVED
- ERROR_INTERNET_NEED_MSN_SSPI_PKG
- ERROR_INTERNET_NEED_UI
- ERROR_INTERNET_NO_CALLBACK
- ERROR_INTERNET_NO_CONTEXT
- ERROR_INTERNET_NO_DIRECT_ACCESS
- ERROR_INTERNET_NOT_INITIALIZED
- ERROR_INTERNET_NOT_PROXY_REQUEST
- ERROR_INTERNET_OPERATION_CANCELLED
- ERROR_INTERNET_OPTION_NOT_SETTABLE
- ERROR_INTERNET_OUT_OF_HANDLES
- ERROR_INTERNET_POST_IS_NON_SECURE
- ERROR_INTERNET_PROTOCOL_NOT_FOUND
- ERROR_INTERNET_PROXY_SERVER_UNREACHABLE
- ERROR_INTERNET_REDIRECT_SCHEME_CHANGE
- ERROR_INTERNET_REGISTRY_VALUE_NOT_FOUND
- ERROR_INTERNET_REQUEST_PENDING
- ERROR_INTERNET_RETRY_DIALOG
- ERROR_INTERNET_SEC_CERT_CN_INVALID
- ERROR_INTERNET_SEC_CERT_DATE_INVALID
- ERROR_INTERNET_SEC_CERT_ERRORS
- ERROR_INTERNET_SEC_CERT_NO_REV
- ERROR_INTERNET_SEC_CERT_REV_FAILED
- ERROR_INTERNET_SEC_CERT_REVOKED
- ERROR_INTERNET_SEC_INVALID_CERT
- ERROR_INTERNET_SECURITY_CHANNEL_ERROR
- ERROR_INTERNET_SERVER_UNREACHABLE
- ERROR_INTERNET_SHUTDOWN
- ERROR_INTERNET_TCPIP_NOT_INSTALLED
- ERROR_INTERNET_TIMEOUT
- ERROR_INTERNET_UNABLE_TO_CACHE_FILE
- ERROR_INTERNET_UNABLE_TO_DOWNLOAD_SCRIPT
- ERROR_INTERNET_UNRECOGNIZED_SCHEME
- ERROR_INVALID_HANDLE
- ERROR_MORE_DATA
- ERROR_NO_MORE_FILES
- ERROR_NO_MORE_ITEMS
api_location:
- Wininet.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d43fcaba7f0404ad002d2a94ac8291c95b0f7440
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106460"
---
# <a name="error-messages-winineth"></a>Fehlermeldungen (WinInet. h)

In den WinInet-Funktionen werden ggf. Fehlercodes zurückgegeben. Die folgenden Fehler sind spezifisch für die WinInet-Funktionen.

<dl> <dt>

<span id="ERROR_FTP_DROPPED"></span><span id="error_ftp_dropped"></span>**Fehler beim Löschen von \_ FTP \_**
</dt> <dd> <dl> <dt>

12111
</dt> <dt>



Der FTP-Vorgang wurde nicht abgeschlossen, da die Sitzung abgebrochen wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_FTP_NO_PASSIVE_MODE"></span><span id="error_ftp_no_passive_mode"></span>**Fehler " \_ FTP \_ nicht \_ passiv \_ "**
</dt> <dd> <dl> <dt>

12112
</dt> <dt>



Der passive Modus ist auf dem Server nicht verfügbar.


</dt> </dl> </dd> <dt>

<span id="ERROR_FTP_TRANSFER_IN_PROGRESS"></span><span id="error_ftp_transfer_in_progress"></span>**Fehler \_ bei FTP- \_ Übertragung wird \_ ausgeführt \_**
</dt> <dd> <dl> <dt>

12110
</dt> <dt>



Der angeforderte Vorgang kann nicht für das FTP-Sitzungs handle ausgeführt werden, da bereits ein Vorgang ausgeführt wird.


</dt> </dl> </dd> <dt>

<span id="ERROR_GOPHER_ATTRIBUTE_NOT_FOUND"></span><span id="error_gopher_attribute_not_found"></span>**Fehler \_ Gopher- \_ Attribut wurde \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

12137
</dt> <dt>



Das angeforderte Attribut konnte nicht gefunden werden.

> [!Note]  
> Nur Windows XP und Windows Server 2003 R2 und früher.

 


</dt> </dl> </dd> <dt>

<span id="ERROR_GOPHER_DATA_ERROR"></span><span id="error_gopher_data_error"></span>**Fehler beim \_ Gopher- \_ Daten \_ Fehler.**
</dt> <dd> <dl> <dt>

12132
</dt> <dt>



Beim Empfangen von Daten vom Gopher-Server wurde ein Fehler festgestellt.

> [!Note]  
> Nur Windows XP und Windows Server 2003 R2 und früher.

 


</dt> </dl> </dd> <dt>

<span id="ERROR_GOPHER_END_OF_DATA"></span><span id="error_gopher_end_of_data"></span>**Fehler beim \_ Gopher- \_ Ende \_ der \_ Daten.**
</dt> <dd> <dl> <dt>

12133
</dt> <dt>



Das Ende der Daten wurde erreicht.

> [!Note]  
> Nur Windows XP und Windows Server 2003 R2 und früher.

 


</dt> </dl> </dd> <dt>

<span id="ERROR_GOPHER_INCORRECT_LOCATOR_TYPE"></span><span id="error_gopher_incorrect_locator_type"></span>**Fehler bei \_ \_ fehlerhafter \_ Art von Locator \_ .**
</dt> <dd> <dl> <dt>

12135
</dt> <dt>



Der Serverlocatorpunkt-Typ ist für diesen Vorgang nicht richtig.

> [!Note]  
> Nur Windows XP und Windows Server 2003 R2 und früher.

 


</dt> </dl> </dd> <dt>

<span id="ERROR_GOPHER_INVALID_LOCATOR"></span><span id="error_gopher_invalid_locator"></span>**Fehler " \_ gopher" \_ ungültiger \_ Locator.**
</dt> <dd> <dl> <dt>

12134
</dt> <dt>



Der angegebene Serverlocatorpunkt ist ungültig.

> [!Note]  
> Nur Windows XP und Windows Server 2003 R2 und früher.

 


</dt> </dl> </dd> <dt>

<span id="ERROR_GOPHER_NOT_FILE"></span><span id="error_gopher_not_file"></span>**Fehler- \_ Gopher \_ nicht \_ Datei**
</dt> <dd> <dl> <dt>

12131
</dt> <dt>



Die Anforderung muss für einen Dateilocator erfolgen.

> [!Note]  
> Nur Windows XP und Windows Server 2003 R2 und früher.

 


</dt> </dl> </dd> <dt>

<span id="ERROR_GOPHER_NOT_GOPHER_PLUS"></span><span id="error_gopher_not_gopher_plus"></span>**Fehler \_ Gopher \_ nicht \_ Gopher \_ Plus**
</dt> <dd> <dl> <dt>

12136
</dt> <dt>



Der angeforderte Vorgang kann nur für einen Gopher +-Server oder mit einem Serverlocatorpunkt erfolgen, der einen Gopher +-Vorgang angibt.

> [!Note]  
> Nur Windows XP und Windows Server 2003 R2 und früher.

 


</dt> </dl> </dd> <dt>

<span id="ERROR_GOPHER_PROTOCOL_ERROR"></span><span id="error_gopher_protocol_error"></span>**Fehler beim \_ Gopher- \_ Protokoll. \_**
</dt> <dd> <dl> <dt>

12130
</dt> <dt>



Fehler beim Übernehmen der vom Gopher-Server zurückgegebenen Daten.

> [!Note]  
> Nur Windows XP und Windows Server 2003 R2 und früher.

 


</dt> </dl> </dd> <dt>

<span id="ERROR_GOPHER_UNKNOWN_LOCATOR"></span><span id="error_gopher_unknown_locator"></span>**Fehler \_ Gopher \_ unbekannter \_ Locator.**
</dt> <dd> <dl> <dt>

12138
</dt> <dt>



Der Locatortyp ist unbekannt.

> [!Note]  
> Nur Windows XP und Windows Server 2003 R2 und früher.

 


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_COOKIE_DECLINED"></span><span id="error_http_cookie_declined"></span>**Fehler \_ http- \_ Cookie \_ abgelehnt**
</dt> <dd> <dl> <dt>

12162
</dt> <dt>



Das HTTP-Cookie wurde vom Server abgelehnt.


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_COOKIE_NEEDS_CONFIRMATION"></span><span id="error_http_cookie_needs_confirmation"></span>**Fehler \_ http- \_ Cookie \_ muss \_ bestätigt werden**
</dt> <dd> <dl> <dt>

12161
</dt> <dt>



Das HTTP-Cookie erfordert eine Bestätigung.

> [!Note]  
> Nur Windows Vista und Windows Server 2008 und früher.

 


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_DOWNLEVEL_SERVER"></span><span id="error_http_downlevel_server"></span>**Fehler \_ http- \_ \_ Downlevelserver**
</dt> <dd> <dl> <dt>

12151
</dt> <dt>



Der Server hat keine Header zurückgegeben.


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_HEADER_ALREADY_EXISTS"></span><span id="error_http_header_already_exists"></span>**HTTP-Fehler \_ \_ Header ist \_ bereits \_ vorhanden.**
</dt> <dd> <dl> <dt>

12155
</dt> <dt>



Der Header konnte nicht hinzugefügt werden, da er bereits vorhanden ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_HEADER_NOT_FOUND"></span><span id="error_http_header_not_found"></span>**HTTP-Fehler \_ \_ Header wurde \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

12150
</dt> <dt>



Der angeforderte Header konnte nicht gefunden werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_INVALID_HEADER"></span><span id="error_http_invalid_header"></span>**HTTP-Fehler bei \_ \_ ungültigem \_ Header**
</dt> <dd> <dl> <dt>

12153
</dt> <dt>



Der angegebene Header ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_INVALID_QUERY_REQUEST"></span><span id="error_http_invalid_query_request"></span>**HTTP-Fehler bei \_ \_ ungültiger \_ Abfrage \_ Anforderung**
</dt> <dd> <dl> <dt>

12154
</dt> <dt>



Die an [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) gestellte Anforderung ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_INVALID_SERVER_RESPONSE"></span><span id="error_http_invalid_server_response"></span>**Fehler \_ http \_ - \_ Antwort auf ungültige Server \_**
</dt> <dd> <dl> <dt>

12152
</dt> <dt>



Die Serverantwort konnte nicht analysiert werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_NOT_REDIRECTED"></span><span id="error_http_not_redirected"></span>**Fehler \_ http \_ nicht \_ umgeleitet**
</dt> <dd> <dl> <dt>

12160
</dt> <dt>



Die HTTP-Anforderung wurde nicht umgeleitet.


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_REDIRECT_FAILED"></span><span id="error_http_redirect_failed"></span>**Fehler bei \_ http- \_ Umleitung. \_**
</dt> <dd> <dl> <dt>

12156
</dt> <dt>



Die Umleitung ist fehlgeschlagen, da entweder das Schema geändert wurde (z. b. http zu FTP) oder alle Versuche zum Umleiten fehlgeschlagen sind (der Standardwert ist fünf Versuche).


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_REDIRECT_NEEDS_CONFIRMATION"></span><span id="error_http_redirect_needs_confirmation"></span>**Fehler \_ http- \_ Umleitung \_ muss \_ bestätigt werden**
</dt> <dd> <dl> <dt>

12168
</dt> <dt>



Die Umleitung erfordert eine Bestätigung des Benutzers.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_ASYNC_THREAD_FAILED"></span><span id="error_internet_async_thread_failed"></span>**Fehler beim asynchronen Thread für das \_ Internet. \_ \_ \_**
</dt> <dd> <dl> <dt>

12047
</dt> <dt>



Die Anwendung konnte keinen asynchronen Thread starten.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_BAD_AUTO_PROXY_SCRIPT"></span><span id="error_internet_bad_auto_proxy_script"></span>**Fehler "Internet fehlerhaftes \_ \_ Auto- \_ \_ Proxy \_ Skript"**
</dt> <dd> <dl> <dt>

12166
</dt> <dt>



Fehler beim automatischen Proxy Konfigurationsskript.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_BAD_OPTION_LENGTH"></span><span id="error_internet_bad_option_length"></span>**Fehler beim Internet mit fehlerhafter \_ \_ \_ options \_ Länge**
</dt> <dd> <dl> <dt>

12010
</dt> <dt>



Die Länge einer für [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) oder [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) angegebenen Option ist für den angegebenen Typ der Option falsch.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_BAD_REGISTRY_PARAMETER"></span><span id="error_internet_bad_registry_parameter"></span>**Fehler "Internet fehlerhafter \_ \_ \_ Registrierungs \_ Parameter"**
</dt> <dd> <dl> <dt>

12022
</dt> <dt>



Ein erforderlicher Registrierungs Wert wurde gefunden, weist aber einen falschen Typ auf oder weist einen ungültigen Wert auf.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_CANNOT_CONNECT"></span><span id="error_internet_cannot_connect"></span>**Fehler \_ Internet \_ Verbindung kann nicht hergestellt werden \_**
</dt> <dd> <dl> <dt>

12029
</dt> <dt>



Fehler beim Versuch, eine Verbindung mit dem Server herzustellen.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_CHG_POST_IS_NON_SECURE"></span><span id="error_internet_chg_post_is_non_secure"></span>**Fehler \_ Internet- \_ CHG- \_ Post \_ ist \_ nicht \_ sicher**
</dt> <dd> <dl> <dt>

12042
</dt> <dt>



Die Anwendung stellt eine Bereitstellung durch und versucht, mehrere Textzeilen auf einem Server zu ändern, der nicht sicher ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_CLIENT_AUTH_CERT_NEEDED"></span><span id="error_internet_client_auth_cert_needed"></span>**Fehler " \_ Internet \_ Client Authentifizierungs \_ \_ Zertifikat \_ erforderlich"**
</dt> <dd> <dl> <dt>

12044
</dt> <dt>



Der Server fordert die Client Authentifizierung an.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_CLIENT_AUTH_NOT_SETUP"></span><span id="error_internet_client_auth_not_setup"></span>**Fehler \_ beim \_ Einrichten der Internet Client Authentifizierung \_ . \_ \_**
</dt> <dd> <dl> <dt>

12046
</dt> <dt>



Auf diesem Computer ist keine Client Autorisierung eingerichtet.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_CONNECTION_ABORTED"></span><span id="error_internet_connection_aborted"></span>**Fehler beim Abbrechen der \_ Internet \_ Verbindung. \_**
</dt> <dd> <dl> <dt>

12030
</dt> <dt>



Die Verbindung mit dem Server wurde beendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_CONNECTION_RESET"></span><span id="error_internet_connection_reset"></span>**Fehler \_ beim \_ Zurücksetzen der Internet Verbindung \_**
</dt> <dd> <dl> <dt>

12031
</dt> <dt>



Die Verbindung mit dem Server wurde zurückgesetzt.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_DECODING_FAILED"></span><span id="error_internet_decoding_failed"></span>**Fehler \_ beim \_ Decodieren des Internets. \_**
</dt> <dd> <dl> <dt>

12175
</dt> <dt>



WinInet konnte die Decodierung von Inhalten für die Antwort nicht durchführen. Weitere Informationen finden Sie im Thema [**Inhalts Codierung**](content-encoding.md) .


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_DIALOG_PENDING"></span><span id="error_internet_dialog_pending"></span>**Fehler beim \_ Internet \_ Dialogfeld \_**
</dt> <dd> <dl> <dt>

12049
</dt> <dt>



Ein anderer Thread enthält ein Kennwort-Dialogfeld.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_DISCONNECTED"></span><span id="error_internet_disconnected"></span>**Fehler beim Internet Verbindung. \_ \_**
</dt> <dd> <dl> <dt>

12163
</dt> <dt>



Die Internet Verbindung ist verloren gegangen.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_EXTENDED_ERROR"></span><span id="error_internet_extended_error"></span>**Fehler \_ beim \_ erweiterten \_ Internet Fehler**
</dt> <dd> <dl> <dt>

12003
</dt> <dt>



Vom Server wurde ein erweiterter Fehler zurückgegeben. Dies ist in der Regel eine Zeichenfolge oder ein Puffer, der eine ausführliche Fehlermeldung enthält. Rufen Sie [**InternetGetLastResponseInfo**](/windows/desktop/api/Wininet/nf-wininet-internetgetlastresponseinfoa) auf, um den Fehlertext abzurufen.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_FAILED_DUETOSECURITYCHECK"></span><span id="error_internet_failed_duetosecuritycheck"></span>**Fehler beim \_ Internet mit \_ \_ duetosecuritycheck.**
</dt> <dd> <dl> <dt>

12171
</dt> <dt>



Die Funktion konnte aufgrund einer Sicherheitsüberprüfung nicht ausgeführt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_FORCE_RETRY"></span><span id="error_internet_force_retry"></span>**Fehler \_ beim \_ erneuten Versuch von Internet Force \_**
</dt> <dd> <dl> <dt>

12032
</dt> <dt>



Die Funktion muss die Anforderung wiederholen.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_FORTEZZA_LOGIN_NEEDED"></span><span id="error_internet_fortezza_login_needed"></span>**Fehler \_ Internet- \_ Fortezza- \_ Anmeldung \_ erforderlich**
</dt> <dd> <dl> <dt>

12054
</dt> <dt>



Die angeforderte Ressource erfordert die Fortezza-Authentifizierung.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_HANDLE_EXISTS"></span><span id="error_internet_handle_exists"></span>**Fehler \_ Internet \_ handle \_ vorhanden**
</dt> <dd> <dl> <dt>

12036
</dt> <dt>



Die Anforderung ist fehlgeschlagen, da das Handle bereits vorhanden ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_HTTP_TO_HTTPS_ON_REDIR"></span><span id="error_internet_http_to_https_on_redir"></span>**Fehler " \_ Internet \_ http \_ zu https" \_ \_ beim \_ redir**
</dt> <dd> <dl> <dt>

12039
</dt> <dt>



Die Anwendung wechselt aufgrund einer Umleitung von einer nicht-SSL-zu einer SSL-Verbindung.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_HTTPS_HTTP_SUBMIT_REDIR"></span><span id="error_internet_https_http_submit_redir"></span>**Fehler " \_ Internet \_ https \_ http \_ Submit \_ redir"**
</dt> <dd> <dl> <dt>

12052
</dt> <dt>



Die Daten, die an eine SSL-Verbindung übermittelt werden, werden an eine nicht-SSL-Verbindung umgeleitet.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_HTTPS_TO_HTTP_ON_REDIR"></span><span id="error_internet_https_to_http_on_redir"></span>**Fehler \_ \_ beim Internet HTTPS \_ zu \_ http \_ bei \_ redir.**
</dt> <dd> <dl> <dt>

12040
</dt> <dt>



Die Anwendung wechselt aufgrund einer Umleitung von einer SSL-zu einer nicht-SSL-Verbindung.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INCORRECT_FORMAT"></span><span id="error_internet_incorrect_format"></span>**Fehler \_ im Internet des \_ falschen \_ Formats**
</dt> <dd> <dl> <dt>

12027
</dt> <dt>



Das Format der Anforderung ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INCORRECT_HANDLE_STATE"></span><span id="error_internet_incorrect_handle_state"></span>**Fehler beim \_ Internet \_ fehlerhafter \_ handle- \_ Status**
</dt> <dd> <dl> <dt>

12019
</dt> <dt>



Der angeforderte Vorgang kann nicht ausgeführt werden, da das angegebene Handle nicht den richtigen Status aufweist.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INCORRECT_HANDLE_TYPE"></span><span id="error_internet_incorrect_handle_type"></span>**Fehler \_ im Internet \_ fehlerhafter \_ handle- \_ Typ**
</dt> <dd> <dl> <dt>

12018
</dt> <dt>



Der angegebene Handlertyp ist für diesen Vorgang falsch.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INCORRECT_PASSWORD"></span><span id="error_internet_incorrect_password"></span>**\_ \_ Fehlerhaftes Internet \_ Kennwort**
</dt> <dd> <dl> <dt>

12014
</dt> <dt>



Die Anforderung zum Verbinden und Anmelden bei einem FTP-Server konnte nicht abgeschlossen werden, da das angegebene Kennwort falsch ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INCORRECT_USER_NAME"></span><span id="error_internet_incorrect_user_name"></span>**\_fehlerhafter \_ Internet \_ Benutzer \_ Name**
</dt> <dd> <dl> <dt>

12013
</dt> <dt>



Die Anforderung zum Verbinden und Anmelden bei einem FTP-Server konnte nicht abgeschlossen werden, da der angegebene Benutzername falsch ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INSERT_CDROM"></span><span id="error_internet_insert_cdrom"></span>**Fehler \_ beim \_ Einfügen der \_ Crom-Datei**
</dt> <dd> <dl> <dt>

12053
</dt> <dt>



Die Anforderung erfordert, dass eine CD-ROM in das CD-ROM-Laufwerk eingefügt wird, um die angeforderte Ressource zu suchen.

> [!Note]  
> Nur Windows Vista und Windows Server 2008 und früher.

 


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INTERNAL_ERROR"></span><span id="error_internet_internal_error"></span>**\_Interner Fehler im Internet. \_ \_**
</dt> <dd> <dl> <dt>

12004
</dt> <dt>



Ein interner Fehler ist aufgetreten.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INVALID_CA"></span><span id="error_internet_invalid_ca"></span>**Fehler beim \_ Internet \_ ungültige Zertifizierungsstelle \_**
</dt> <dd> <dl> <dt>

12045
</dt> <dt>



Die Funktion ist mit der Zertifizierungsstelle, die das Zertifikat des Servers generiert hat, nicht vertraut.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INVALID_OPERATION"></span><span id="error_internet_invalid_operation"></span>**Fehler beim \_ Internet \_ ungültiger \_ Vorgang.**
</dt> <dd> <dl> <dt>

12016
</dt> <dt>



Der angeforderte Vorgang ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INVALID_OPTION"></span><span id="error_internet_invalid_option"></span>**Fehler beim \_ Internet \_ ungültige \_ Option**
</dt> <dd> <dl> <dt>

12009
</dt> <dt>



Eine Anforderung an [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) oder [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) hat einen ungültigen Optionswert angegeben.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INVALID_PROXY_REQUEST"></span><span id="error_internet_invalid_proxy_request"></span>**Fehler beim \_ Internet \_ ungültige \_ Proxy \_ Anforderung.**
</dt> <dd> <dl> <dt>

12033
</dt> <dt>



Die Anforderung an den Proxy war ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INVALID_URL"></span><span id="error_internet_invalid_url"></span>**Fehler beim \_ Internet \_ ungültige \_ URL.**
</dt> <dd> <dl> <dt>

12005
</dt> <dt>



Die URL ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_ITEM_NOT_FOUND"></span><span id="error_internet_item_not_found"></span>**Fehler beim \_ Internet \_ Element \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

12028
</dt> <dt>



Das angeforderte Element konnte nicht gefunden werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_LOGIN_FAILURE"></span><span id="error_internet_login_failure"></span>**Fehler beim \_ Internet \_ Anmelde \_ Fehler.**
</dt> <dd> <dl> <dt>

12015
</dt> <dt>



Fehler bei der Anforderung zum Verbinden und Anmelden bei einem FTP-Server.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_LOGIN_FAILURE_DISPLAY_ENTITY_BODY"></span><span id="error_internet_login_failure_display_entity_body"></span>**Fehler beim \_ Internet Anmeldefehler beim \_ Anzeigen des \_ \_ \_ Entitäts \_ Texts.**
</dt> <dd> <dl> <dt>

12174
</dt> <dt>



Der MS-Logoff Digest-Header wurde von der Website zurückgegeben. Dieser Header weist das Digest-Paket ausdrücklich an, Anmelde Informationen für den zugeordneten Bereich zu löschen. Dieser Fehler wird nur zurückgegeben, wenn die Option zum [ \_ Anzeigen von \_ \_ \_ \_ \_ Entitäts \_ Text der Internet Fehler Maske angezeigt](option-flags.md) wird; andernfalls wird der **Fehler " \_ Internet \_ Login \_ Failure** " zurückgegeben.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_MIXED_SECURITY"></span><span id="error_internet_mixed_security"></span>**Fehler \_ im Internet mit \_ gemischter \_ Sicherheit**
</dt> <dd> <dl> <dt>

12041
</dt> <dt>



Der Inhalt ist nicht vollständig sicher. Einige der Inhalte, die angezeigt werden, stammen möglicherweise von nicht geschützten Servern.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_NAME_NOT_RESOLVED"></span><span id="error_internet_name_not_resolved"></span>**Fehler beim Auflösen des \_ Internet \_ namens. \_ \_**
</dt> <dd> <dl> <dt>

12007
</dt> <dt>



Der Servername konnte nicht aufgelöst werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_NEED_MSN_SSPI_PKG"></span><span id="error_internet_need_msn_sspi_pkg"></span>**Fehler \_ Internet \_ benötigt \_ MSN \_ SSPI \_ pkg**
</dt> <dd> <dl> <dt>

12173
</dt> <dt>



Derzeit nicht implementiert.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_NEED_UI"></span><span id="error_internet_need_ui"></span>**Fehler \_ Internet \_ \_ Benutzeroberfläche erforderlich**
</dt> <dd> <dl> <dt>

12034
</dt> <dt>



Eine Benutzeroberfläche oder ein anderer Blockierungs Vorgang wurde angefordert.

> [!Note]  
> Nur Windows Vista und Windows Server 2008 und früher.

 


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_NO_CALLBACK"></span><span id="error_internet_no_callback"></span>**Fehler \_ Internet \_ kein \_ Rückruf**
</dt> <dd> <dl> <dt>

12025
</dt> <dt>



Eine asynchrone Anforderung konnte nicht durchgeführt werden, da keine Rückruffunktion festgelegt wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_NO_CONTEXT"></span><span id="error_internet_no_context"></span>**Fehler \_ Internet \_ ohne \_ Kontext**
</dt> <dd> <dl> <dt>

12024
</dt> <dt>



Eine asynchrone Anforderung konnte nicht durchgeführt werden, da ein NULL-Kontextwert angegeben wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_NO_DIRECT_ACCESS"></span><span id="error_internet_no_direct_access"></span>**Fehler \_ Internet \_ kein \_ direkter \_ Zugriff**
</dt> <dd> <dl> <dt>

12023
</dt> <dt>



Zurzeit kann kein direkter Netzwerk Zugriff erfolgen.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_NOT_INITIALIZED"></span><span id="error_internet_not_initialized"></span>**Fehler " \_ Internet" \_ nicht \_ Initialisiert**
</dt> <dd> <dl> <dt>

12172
</dt> <dt>



Die Initialisierung der WinInet-API ist nicht erfolgt. Gibt an, dass eine Funktion auf höherer Ebene, z. b. [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena), noch nicht aufgerufen wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_NOT_PROXY_REQUEST"></span><span id="error_internet_not_proxy_request"></span>**Fehler " \_ Internet \_ nicht \_ Proxy \_ Anforderung"**
</dt> <dd> <dl> <dt>

12020
</dt> <dt>



Die Anforderung kann nicht über einen Proxy durchgeführt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_OPERATION_CANCELLED"></span><span id="error_internet_operation_cancelled"></span>**Fehler beim \_ Internet \_ Vorgang. \_**
</dt> <dd> <dl> <dt>

12017
</dt> <dt>



Der Vorgang wurde abgebrochen, in der Regel, weil das Handle, für das die Anforderung ausgeführt wurde, vor dem Abschluss des Vorgangs geschlossen wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_OPTION_NOT_SETTABLE"></span><span id="error_internet_option_not_settable"></span>**Fehler " \_ Internet \_ Option \_ nicht \_ feststellbar"**
</dt> <dd> <dl> <dt>

12011
</dt> <dt>



Die angeforderte Option kann nicht festgelegt werden, sondern nur abgefragt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_OUT_OF_HANDLES"></span><span id="error_internet_out_of_handles"></span>**Fehler beim \_ Internet \_ außerhalb \_ der \_ Handles**
</dt> <dd> <dl> <dt>

12001
</dt> <dt>



Zu diesem Zeitpunkt können keine weiteren Handles generiert werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_POST_IS_NON_SECURE"></span><span id="error_internet_post_is_non_secure"></span>**Fehler " \_ Internet \_ Post" \_ ist \_ nicht \_ sicher.**
</dt> <dd> <dl> <dt>

12043
</dt> <dt>



Die Anwendung veröffentlicht Daten auf einem Server, der nicht sicher ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_PROTOCOL_NOT_FOUND"></span><span id="error_internet_protocol_not_found"></span>**Fehler " \_ Internet \_ Protokoll \_ nicht \_ gefunden"**
</dt> <dd> <dl> <dt>

12008
</dt> <dt>



Das angeforderte Protokoll konnte nicht gefunden werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_PROXY_SERVER_UNREACHABLE"></span><span id="error_internet_proxy_server_unreachable"></span>**Fehler \_ beim \_ Internet \_ Proxyserver \_ nicht erreichbar.**
</dt> <dd> <dl> <dt>

12165
</dt> <dt>



Der angegebene Proxy Server kann nicht erreicht werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_REDIRECT_SCHEME_CHANGE"></span><span id="error_internet_redirect_scheme_change"></span>**Fehler beim \_ Ändern der Internet \_ Umleitungs \_ Schema \_**
</dt> <dd> <dl> <dt>

12048
</dt> <dt>



Die Funktion konnte die Umleitung nicht verarbeiten, da das Schema geändert wurde (z. b. http zu FTP).


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_REGISTRY_VALUE_NOT_FOUND"></span><span id="error_internet_registry_value_not_found"></span>**Fehler beim \_ Internet \_ Registrierungs \_ Wert \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

12021
</dt> <dt>



Ein erforderlicher Registrierungs Wert wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_REQUEST_PENDING"></span><span id="error_internet_request_pending"></span>**Fehler \_ Internet \_ Anforderung steht \_ aus.**
</dt> <dd> <dl> <dt>

12026
</dt> <dt>



Der erforderliche Vorgang konnte nicht abgeschlossen werden, da eine oder mehrere Anforderungen ausstehen.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_RETRY_DIALOG"></span><span id="error_internet_retry_dialog"></span>**Fehler beim \_ Internet- \_ Wiederholungs \_ Dialogfeld**
</dt> <dd> <dl> <dt>

12050
</dt> <dt>



Das Dialogfeld sollte erneut versucht werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_SEC_CERT_CN_INVALID"></span><span id="error_internet_sec_cert_cn_invalid"></span>**Fehler \_ Internet \_ sec \_ CERT \_ CN ist \_ ungültig.**
</dt> <dd> <dl> <dt>

12038
</dt> <dt>



Der allgemeine Name des SSL-Zertifikats (Hostname) ist falsch, wenn Sie z. b. www.Server.com eingegeben haben und der allgemeine Name des Zertifikats www.different.com lautet.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_SEC_CERT_DATE_INVALID"></span><span id="error_internet_sec_cert_date_invalid"></span>**Fehler \_ Internet \_ Sek. \_ CERT- \_ Datum \_ ungültig**
</dt> <dd> <dl> <dt>

12037
</dt> <dt>



Das vom Server empfangene SSL-Zertifikat ist ungültig. Das Zertifikat ist abgelaufen.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_SEC_CERT_ERRORS"></span><span id="error_internet_sec_cert_errors"></span>**Fehler \_ Internet \_ Sek. \_ CERT- \_ Fehler**
</dt> <dd> <dl> <dt>

12055
</dt> <dt>



Das SSL-Zertifikat enthält Fehler.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_SEC_CERT_NO_REV"></span><span id="error_internet_sec_cert_no_rev"></span>**Fehler \_ Internet \_ sec \_ CERT \_ No \_ Rev**
</dt> <dd> <dl> <dt>

12056
</dt> <dt>



Das SSL-Zertifikat wurde nicht widerrufen.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_SEC_CERT_REV_FAILED"></span><span id="error_internet_sec_cert_rev_failed"></span>**Fehler beim \_ Internet \_ sec- \_ CERT \_ Rev \_ .**
</dt> <dd> <dl> <dt>

12057
</dt> <dt>



Die Sperrung des SSL-Zertifikats ist fehlgeschlagen.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_SEC_CERT_REVOKED"></span><span id="error_internet_sec_cert_revoked"></span>**Fehler \_ Internet \_ Sek. \_ Zertifikat \_ gesperrt**
</dt> <dd> <dl> <dt>

12170
</dt> <dt>



Das SSL-Zertifikat wurde widerrufen.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_SEC_INVALID_CERT"></span><span id="error_internet_sec_invalid_cert"></span>**Fehler \_ Internet \_ Sek. \_ ungültiges \_ Zertifikat**
</dt> <dd> <dl> <dt>

12169
</dt> <dt>



Das SSL-Zertifikat ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_SECURITY_CHANNEL_ERROR"></span><span id="error_internet_security_channel_error"></span>**Fehler beim \_ Internet \_ Sicherheits \_ Kanal \_ .**
</dt> <dd> <dl> <dt>

12157
</dt> <dt>



Bei der Anwendung ist ein interner Fehler beim Laden der SSL-Bibliotheken aufgetreten.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_SERVER_UNREACHABLE"></span><span id="error_internet_server_unreachable"></span>**Fehler " \_ Internet \_ Server \_ nicht erreichbar"**
</dt> <dd> <dl> <dt>

12164
</dt> <dt>



Die angegebener Website oder der Server ist nicht erreichbar.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_SHUTDOWN"></span><span id="error_internet_shutdown"></span>**Fehler beim \_ Internet \_ Herunterfahren**
</dt> <dd> <dl> <dt>

12012
</dt> <dt>



Die WinInet-Unterstützung wird heruntergefahren oder entladen.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_TCPIP_NOT_INSTALLED"></span><span id="error_internet_tcpip_not_installed"></span>**Fehler \_ Internet \_ tcpip \_ nicht \_ installiert**
</dt> <dd> <dl> <dt>

12159
</dt> <dt>



Der erforderliche Protokollstapel ist nicht geladen, und die Anwendung kann Winsock nicht starten.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_TIMEOUT"></span><span id="error_internet_timeout"></span>**Fehler beim \_ Internet \_ Timeout.**
</dt> <dd> <dl> <dt>

12002
</dt> <dt>



Timeout für die Anforderung.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_UNABLE_TO_CACHE_FILE"></span><span id="error_internet_unable_to_cache_file"></span>**Fehler beim zwischen \_ \_ Speichern der \_ \_ \_ Datei durch das Internet.**
</dt> <dd> <dl> <dt>

12158
</dt> <dt>



Die Funktion konnte die Datei nicht zwischenspeichern.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_UNABLE_TO_DOWNLOAD_SCRIPT"></span><span id="error_internet_unable_to_download_script"></span>**Fehler \_ beim \_ \_ \_ herunterladen des \_ Skripts durch das Internet**
</dt> <dd> <dl> <dt>

12167
</dt> <dt>



Das Skript für die automatische Proxykonfiguration konnte nicht heruntergeladen werden. Das kennflag für das Internet Kennzeichen \_ \_ muss zwischengespeichert werden \_ \_ .


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_UNRECOGNIZED_SCHEME"></span><span id="error_internet_unrecognized_scheme"></span>**Fehler \_ im Internet \_ unbekannter \_ Schema**
</dt> <dd> <dl> <dt>

12006
</dt> <dt>



Das URL-Schema konnte nicht erkannt werden, oder es wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_HANDLE"></span><span id="error_invalid_handle"></span>**Fehler bei \_ ungültigem \_ handle**
</dt> <dd> <dl> <dt>



Das Handle, das an die API übermittelt wurde, wurde entweder ungültig oder wurde geschlossen.

**Header:** In "Winerror. h" deklariert


</dt> </dl> </dd> <dt>

<span id="ERROR_MORE_DATA"></span><span id="error_more_data"></span>**Fehler \_ Weitere \_ Daten**
</dt> <dd> <dl> <dt>



Weitere Daten sind verfügbar.

**Header:** In "Winerror. h" deklariert


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MORE_FILES"></span><span id="error_no_more_files"></span>**Fehler \_ keine \_ weiteren \_ Dateien**
</dt> <dd> <dl> <dt>



Es wurden keine weiteren Dateien gefunden.

**Header:** In "Winerror. h" deklariert


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MORE_ITEMS"></span><span id="error_no_more_items"></span>**Fehler \_ keine \_ weiteren \_ Elemente**
</dt> <dd> <dl> <dt>



Es wurden keine weiteren Elemente gefunden.

**Header:** In "Winerror. h" deklariert


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> WinInet unterstützt keine Server Implementierungen. Außerdem sollte Sie nicht von einem Dienst verwendet werden. Verwenden Sie für Server Implementierungen oder-Dienste [Microsoft Windows HTTP-Dienste (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Wininet. h</dt> </dl> |



 

