---
description: Die in diesem Thema identifizierten Fehlerwerte werden von GetLastError zurückgegeben, wenn eine der WinHTTP-Funktionen (Microsoft Windows HTTP Services) fehlschlägt.
ms.assetid: c8a863cd-d36c-4ec8-ac49-0b714a5e4cc2
title: Fehlermeldungen (Winhttp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d83fa1859f071b0fc0e651235deea51626f55b8a45cdb2a3ea8736a57317741
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117744716"
---
# <a name="error-messages-winhttph"></a>Fehlermeldungen (Winhttp.h)

Die unten aufgeführten Fehlerwerte werden von [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) zurückgegeben, wenn eine der WinHTTP-Funktionen (Microsoft Windows HTTP Services) fehlschlägt, und sie werden auch in den unteren 16 Bits des [**HRESULT-Fehlers**](../com/structure-of-com-error-codes.md) zurückgegeben, die vom [**WinHttpRequest-Objekt**](winhttprequest.md) zurückgegeben werden.

Fehlerwerte, deren Namen mit "ERROR \_ \_ WINHTTP" beginnen, sind spezifisch für die WinHTTP-Funktionen. Die WinHTTP-Funktionen geben auch Windows Fehlermeldungen zurück.

<dl> <dt>

<span id="ERROR_WINHTTP_AUTO_PROXY_SERVICE_ERROR"></span><span id="error_winhttp_auto_proxy_service_error"></span>**FEHLER: \_ WINHTTP \_ AUTO PROXY SERVICE \_ \_ \_ ERROR**
</dt> <dd> <dl> <dt>

12178
</dt> <dt>



Wird von [**WinHttpGetProxyForUrl zurückgegeben,**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) wenn kein Proxy für die angegebene URL gefunden werden kann.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_AUTODETECTION_FAILED"></span><span id="error_winhttp_autodetection_failed"></span>**FEHLER: \_ FEHLER BEI \_ WINHTTP AUTODETECTION \_**
</dt> <dd> <dl> <dt>

12180
</dt> <dt>



Wird von [**WinHttpDetectAutoProxyConfigUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl) zurückgegeben, wenn WinHTTP die URL der PAC-Datei (Proxy Auto-Configuration) nicht finden konnte.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_BAD_AUTO_PROXY_SCRIPT"></span><span id="error_winhttp_bad_auto_proxy_script"></span>**\_FEHLER: \_ WINHTTP– \_ FEHLERHAFTES \_ AUTOMATISCHES \_ PROXYSKRIPT**
</dt> <dd> <dl> <dt>

12166
</dt> <dt>



Fehler beim Ausführen des Skriptcodes in der PAC-Datei (Proxy Auto-Configuration).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CANNOT_CALL_AFTER_OPEN"></span><span id="error_winhttp_cannot_call_after_open"></span>**FEHLER: \_ WINHTTP \_ KANN NACH DEM ÖFFNEN NICHT MEHR \_ \_ \_ AUFRUFEN**
</dt> <dd> <dl> <dt>

12103
</dt> <dt>



Wird vom [**HttpRequest-Objekt**](winhttprequest.md) zurückgegeben, wenn eine angegebene Option nicht angefordert werden kann, nachdem die [**Open-Methode**](iwinhttprequest-open.md) aufgerufen wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CANNOT_CALL_AFTER_SEND"></span><span id="error_winhttp_cannot_call_after_send"></span>**FEHLER: \_ WINHTTP \_ KANN NACH DEM SENDEN NICHT \_ \_ AUFRUFEN \_**
</dt> <dd> <dl> <dt>

12102
</dt> <dt>



Wird vom [**HttpRequest-Objekt**](winhttprequest.md) zurückgegeben, wenn ein angeforderter Vorgang nach dem Aufruf der [**Send-Methode nicht ausgeführt werden**](iwinhttprequest-send.md) kann.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CANNOT_CALL_BEFORE_OPEN"></span><span id="error_winhttp_cannot_call_before_open"></span>**FEHLER: \_ WINHTTP \_ KANN VOR DEM ÖFFNEN NICHT \_ \_ AUFRUFEN \_**
</dt> <dd> <dl> <dt>

12100
</dt> <dt>



Wird vom [**HttpRequest-Objekt**](winhttprequest.md) zurückgegeben, wenn ein angeforderter Vorgang vor dem Aufruf der [**Open-Methode nicht ausgeführt werden**](iwinhttprequest-open.md) kann.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CANNOT_CALL_BEFORE_SEND"></span><span id="error_winhttp_cannot_call_before_send"></span>**FEHLER: \_ WINHTTP \_ KANN VOR DEM SENDEN NICHT \_ \_ \_ AUFRUFEN**
</dt> <dd> <dl> <dt>

12101
</dt> <dt>



Wird vom [**HttpRequest-Objekt**](winhttprequest.md) zurückgegeben, wenn ein angeforderter Vorgang vor dem Aufruf der [**Send-Methode nicht ausgeführt werden**](iwinhttprequest-send.md) kann.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CANNOT_CONNECT"></span><span id="error_winhttp_cannot_connect"></span>**FEHLER: \_ WINHTTP \_ KANN KEINE VERBINDUNG \_ HERSTELLEN**
</dt> <dd> <dl> <dt>

12029
</dt> <dt>



Wird zurückgegeben, wenn die Verbindung mit dem Server fehlgeschlagen ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CLIENT_AUTH_CERT_NEEDED"></span><span id="error_winhttp_client_auth_cert_needed"></span>**\_FEHLER: \_ WINHTTP-CLIENTAUTHENTIFIZIERUNGSZERTIFIKAT \_ \_ \_ ERFORDERLICH**
</dt> <dd> <dl> <dt>



Der Server erfordert die SSL-Clientauthentifizierung. Die Anwendung ruft die Liste der Zertifikataussteller ab, indem [**sie WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) mit der **OPTION WINHTTP OPTION CLIENT \_ \_ \_ CERT ISSUER LIST \_ \_ aufruft.** Weitere Informationen finden Sie unter DER **OPTION WINHTTP \_ OPTION CLIENT \_ \_ CERT ISSUER \_ \_ LIST.**

Wenn der Server das Clientzertifikat an fordert, es aber nicht erfordert, kann die Anwendung [**alternativ WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) mit der **OPTION WINHTTP OPTION CLIENT \_ \_ \_ CERT \_ CONTEXT** aufrufen. In diesem Fall gibt die Anwendung das WINHTTP \_ NO \_ CLIENT \_ CERT CONTEXT-Makro im \_ *lpBuffer-Parameter* von **WinHttpSetOption an.** Weitere Informationen finden Sie unter DER **OPTION WINHTTP \_ OPTION CLIENT \_ \_ CERT \_ CONTEXT.**

**Windows Server 2003 mit SP1 und Windows XP mit SP2:** Dieser Fehler wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CLIENT_CERT_NO_ACCESS_PRIVATE_KEY"></span><span id="error_winhttp_client_cert_no_access_private_key"></span>**\_FEHLER: \_ WINHTTP-CLIENTZERTIFIKAT \_ KEIN PRIVATER \_ \_ \_ \_ ZUGRIFFSSCHLÜSSEL**
</dt> <dd> <dl> <dt>



Die Anwendung verfügt nicht über die erforderlichen Berechtigungen für den Zugriff auf den privaten Schlüssel, der dem Clientzertifikat zugeordnet ist.

**Windows Server 2003 mit SP1 und Windows XP mit SP2:** Dieser Fehler wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CLIENT_CERT_NO_PRIVATE_KEY"></span><span id="error_winhttp_client_cert_no_private_key"></span>**\_FEHLER: \_ WINHTTP-CLIENTZERTIFIKAT \_ KEIN PRIVATER \_ \_ \_ SCHLÜSSEL**
</dt> <dd> <dl> <dt>



Dem Kontext für das SSL-Clientzertifikat ist kein privater Schlüssel zugeordnet. Das Clientzertifikat wurde möglicherweise ohne den privaten Schlüssel auf den Computer importiert.

**Windows Server 2003 mit SP1 und Windows XP mit SP2:** Dieser Fehler wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CHUNKED_ENCODING_HEADER_SIZE_OVERFLOW"></span><span id="error_winhttp_chunked_encoding_header_size_overflow"></span>**FEHLER: \_ WINHTTP \_ CHUNKED \_ ENCODING HEADER SIZE \_ \_ \_ OVERFLOW**
</dt> <dd> <dl> <dt>

12183
</dt> <dt>



Wird von [**WinHttpReceiveResponse zurückgegeben,**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) wenn bei der Analyse der blockierten Codierung eine Überlaufbedingung auftritt.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CLIENT_AUTH_CERT_NEEDED"></span><span id="error_winhttp_client_auth_cert_needed"></span>**\_FEHLER: \_ WINHTTP-CLIENTAUTHENTIFIZIERUNGSZERTIFIKAT \_ \_ \_ ERFORDERLICH**
</dt> <dd> <dl> <dt>

12044
</dt> <dt>



Wird von [**WinHttpReceiveResponse zurückgegeben,**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) wenn der Server die Clientauthentifizierung an fordert.

**Windows Server 2003 mit SP1 und Windows XP mit SP2:** Dieser Fehler wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CONNECTION_ERROR"></span><span id="error_winhttp_connection_error"></span>**FEHLER: \_ \_ WINHTTP-VERBINDUNGSFEHLER \_**
</dt> <dd> <dl> <dt>

12030
</dt> <dt>



Die Verbindung mit dem Server wurde zurückgesetzt oder beendet, oder es wurde ein inkompatibles SSL-Protokoll gefunden. Beispielsweise unterstützt WinHTTP Version 5.1 SSL2 nur, wenn der Client dies ausdrücklich aktiviert.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_HEADER_ALREADY_EXISTS"></span><span id="error_winhttp_header_already_exists"></span>**\_FEHLER: \_ WINHTTP-HEADER \_ IST BEREITS \_ VORHANDEN**
</dt> <dd> <dl> <dt>

12155
</dt> <dt>



Veraltet; wird nicht mehr verwendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_HEADER_COUNT_EXCEEDED"></span><span id="error_winhttp_header_count_exceeded"></span>**FEHLER: \_ \_ WINHTTP-HEADERANZAHL \_ \_ ÜBERSCHRITTEN**
</dt> <dd> <dl> <dt>

12181
</dt> <dt>



Wird von [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) zurückgegeben, wenn eine größere Anzahl von Headern in einer Antwort vorhanden war, als WinHTTP empfangen konnte.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_HEADER_NOT_FOUND"></span><span id="error_winhttp_header_not_found"></span>**\_FEHLER: \_ WINHTTP-HEADER \_ NICHT \_ GEFUNDEN**
</dt> <dd> <dl> <dt>

12150
</dt> <dt>



Der angeforderte Header kann nicht gefunden werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_HEADER_SIZE_OVERFLOW"></span><span id="error_winhttp_header_size_overflow"></span>**FEHLER: \_ ÜBERLAUF DER GRÖßE DES WINHTTP-HEADERS \_ \_ \_**
</dt> <dd> <dl> <dt>

12182
</dt> <dt>



Wird von [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) zurückgegeben, wenn die Größe der empfangenen Header den Grenzwert für das Anforderungshand handle überschreitet.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_INCORRECT_HANDLE_STATE"></span><span id="error_winhttp_incorrect_handle_state"></span>**\_FEHLER: \_ WINHTTP: \_ FALSCHER \_ HANDLEZUSTAND**
</dt> <dd> <dl> <dt>

12019
</dt> <dt>



Der angeforderte Vorgang kann nicht ausgeführt werden, da sich das angegebene Handle nicht im richtigen Zustand befindet.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_INCORRECT_HANDLE_TYPE"></span><span id="error_winhttp_incorrect_handle_type"></span>**\_FEHLER: \_ WINHTTP: \_ FALSCHER \_ HANDLETYP**
</dt> <dd> <dl> <dt>

12018
</dt> <dt>



Der angegebene Handletyp ist für diesen Vorgang falsch.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_INTERNAL_ERROR"></span><span id="error_winhttp_internal_error"></span>**FEHLER: \_ INTERNER \_ WINHTTP-FEHLER \_**
</dt> <dd> <dl> <dt>

12004
</dt> <dt>



Ein interner Fehler ist aufgetreten.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_INVALID_OPTION"></span><span id="error_winhttp_invalid_option"></span>**FEHLEROPTION \_ "WINHTTP \_ \_ UNGÜLTIG"**
</dt> <dd> <dl> <dt>

12009
</dt> <dt>



Eine Anforderung an [**WinHttpQueryOption oder**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) hat einen ungültigen Optionswert angegeben.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_INVALID_QUERY_REQUEST"></span><span id="error_winhttp_invalid_query_request"></span>**FEHLER: \_ WINHTTP \_ \_ UNGÜLTIGE \_ ABFRAGEANFORDERUNG**
</dt> <dd> <dl> <dt>

12154
</dt> <dt>



Veraltet; wird nicht mehr verwendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_INVALID_SERVER_RESPONSE"></span><span id="error_winhttp_invalid_server_response"></span>**FEHLER: \_ WINHTTP \_ \_ UNGÜLTIGE \_ SERVERANTWORT**
</dt> <dd> <dl> <dt>

12152
</dt> <dt>



Die Serverantwort kann nicht analysiert werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_INVALID_URL"></span><span id="error_winhttp_invalid_url"></span>**FEHLER: \_ WINHTTP \_ UNGÜLTIGE \_ URL**
</dt> <dd> <dl> <dt>

12005
</dt> <dt>



Die URL ist nicht gültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_LOGIN_FAILURE"></span><span id="error_winhttp_login_failure"></span>**\_FEHLER: \_ WINHTTP-ANMELDEFEHLER \_**
</dt> <dd> <dl> <dt>

12015
</dt> <dt>



Fehler beim Anmeldeversuch. Wenn dieser Fehler auftritt, sollte das Anforderungshandle mit [**WinHttpCloseHandle geschlossen werden.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpclosehandle) Ein neues Anforderungshandle muss erstellt werden, bevor Sie die Funktion wiederholen, die diesen Fehler ursprünglich verursacht hat.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_NAME_NOT_RESOLVED"></span><span id="error_winhttp_name_not_resolved"></span>**FEHLER \_ \_ WINHTTP-NAME \_ NICHT \_ AUFGELÖST**
</dt> <dd> <dl> <dt>

12007
</dt> <dt>



Der Servername kann nicht aufgelöst werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_NOT_INITIALIZED"></span><span id="error_winhttp_not_initialized"></span>**FEHLER: \_ WINHTTP \_ NICHT \_ INITIALISIERT**
</dt> <dd> <dl> <dt>

12172
</dt> <dt>



Veraltet; wird nicht mehr verwendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_OPERATION_CANCELLED"></span><span id="error_winhttp_operation_cancelled"></span>**FEHLER: \_ \_ WINHTTP-VORGANG \_ ABGEBROCHEN**
</dt> <dd> <dl> <dt>

12017
</dt> <dt>



Der Vorgang wurde abgebrochen, in der Regel, weil das Handle, auf dem die Anforderung ausgeführt wurde, geschlossen wurde, bevor der Vorgang abgeschlossen wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_OPTION_NOT_SETTABLE"></span><span id="error_winhttp_option_not_settable"></span>**FEHLER: \_ \_ WINHTTP-OPTION \_ NICHT \_ FESTLEGBAR**
</dt> <dd> <dl> <dt>

12011
</dt> <dt>



Die angeforderte Option kann nicht festgelegt werden, sondern nur abgefragt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_OUT_OF_HANDLES"></span><span id="error_winhttp_out_of_handles"></span>**FEHLER: \_ WINHTTP \_ OUT OF \_ \_ HANDLES**
</dt> <dd> <dl> <dt>

12001
</dt> <dt>



Veraltet; wird nicht mehr verwendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_REDIRECT_FAILED"></span><span id="error_winhttp_redirect_failed"></span>**FEHLER: \_ FEHLER BEI \_ WINHTTP-UMLEITUNG \_**
</dt> <dd> <dl> <dt>

12156
</dt> <dt>



Die Umleitung ist fehlgeschlagen, weil entweder das Schema geändert wurde oder alle Umleitungsversuche fehlgeschlagen sind (der Standardwert ist fünf Versuche).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_RESEND_REQUEST"></span><span id="error_winhttp_resend_request"></span>**\_FEHLER: \_ WINHTTP-ANFORDERUNG ERNEUT \_ SENDEN**
</dt> <dd> <dl> <dt>

12032
</dt> <dt>



Fehler bei der WinHTTP-Funktion. Die gewünschte Funktion kann für dasselbe Anforderungshand handle wiederholt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_RESPONSE_DRAIN_OVERFLOW"></span><span id="error_winhttp_response_drain_overflow"></span>**FEHLER: \_ WINHTTP \_ RESPONSE DRAIN \_ \_ OVERFLOW**
</dt> <dd> <dl> <dt>

12184
</dt> <dt>



Wird zurückgegeben, wenn eine eingehende Antwort eine interne WinHTTP-Größenbeschränkung überschreitet.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SCRIPT_EXECUTION_ERROR"></span><span id="error_winhttp_script_execution_error"></span>**FEHLER: \_ \_ WINHTTP-SKRIPTAUSFÜHRUNGSFEHLER \_ \_**
</dt> <dd> <dl> <dt>

12177
</dt> <dt>



Beim Ausführen eines Skripts ist ein Fehler aufgetreten.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_CERT_CN_INVALID"></span><span id="error_winhttp_secure_cert_cn_invalid"></span>**FEHLER: \_ WINHTTP \_ SECURE \_ CERT \_ CN \_ UNGÜLTIG**
</dt> <dd> <dl> <dt>

12038
</dt> <dt>



Wird zurückgegeben, wenn ein CN-Name des Zertifikats nicht mit dem übergebenen Wert (entspricht einem **CERT \_ E \_ CN \_ NO \_ MATCH-Fehler)** übereinstimmen.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_CERT_DATE_INVALID"></span><span id="error_winhttp_secure_cert_date_invalid"></span>**FEHLER: \_ WINHTTP \_ SECURE \_ CERT \_ DATE \_ UNGÜLTIG**
</dt> <dd> <dl> <dt>

12037
</dt> <dt>



Gibt an, dass ein erforderliches Zertifikat bei der Überprüfung mit der aktuellen Systemuhr oder dem Zeitstempel in der signierten Datei nicht innerhalb seiner Gültigkeitsdauer liegt oder dass die Gültigkeitsdauern der Zertifizierungskette nicht ordnungsgemäß geschachtelt sind (äquivalent zu **einem CERT \_ E \_ EXPIRED-** oder **\_ CERT E \_ VALIDITYPERIODNESTING-Fehler).**


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_CERT_REV_FAILED"></span><span id="error_winhttp_secure_cert_rev_failed"></span>**FEHLER: \_ FEHLER BEI WINHTTP \_ SECURE \_ CERT \_ REV \_**
</dt> <dd> <dl> <dt>

12057
</dt> <dt>



Gibt an, dass die Sperrung nicht überprüft werden kann, da der Sperrserver offline war (entspricht **CRYPT \_ E REVOCATION \_ \_ OFFLINE**).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_CERT_REVOKED"></span><span id="error_winhttp_secure_cert_revoked"></span>**FEHLER: \_ WINHTTP \_ SECURE \_ CERT \_ WIDERRUFEN**
</dt> <dd> <dl> <dt>

12170
</dt> <dt>



Gibt an, dass ein Zertifikat widerrufen wurde (entspricht **CRYPT \_ E \_ REVOKED**).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_CERT_WRONG_USAGE"></span><span id="error_winhttp_secure_cert_wrong_usage"></span>**FEHLER: \_ WINHTTP \_ SECURE \_ \_ CERT: FALSCHE \_ VERWENDUNG**
</dt> <dd> <dl> <dt>

12179
</dt> <dt>



Gibt an, dass ein Zertifikat für die angeforderte Verwendung nicht gültig ist (entspricht **CERT \_ E WRONG \_ \_ USAGE**).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_CHANNEL_ERROR"></span><span id="error_winhttp_secure_channel_error"></span>**FEHLER: \_ WINHTTP \_ SECURE CHANNEL \_ \_ ERROR**
</dt> <dd> <dl> <dt>

12157
</dt> <dt>



Gibt an, dass bei einem sicheren Kanal ein Fehler aufgetreten ist (äquivalent zu Fehlercodes, die mit "SEC E" und "SEC I" beginnen, die in der Headerdatei \_ \_ \_ \_ "winerror.h" aufgeführt sind).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_FAILURE"></span><span id="error_winhttp_secure_failure"></span>**FEHLER: \_ WINHTTP \_ \_ SECURE-FEHLER**
</dt> <dd> <dl> <dt>

12175
</dt> <dt>



Mindestens ein Fehler wurde im vom Server Secure Sockets Layer (SSL)-Zertifikat gefunden. Um zu ermitteln, welcher Fehlertyp aufgetreten ist, überprüfen Sie in einer Statusrückruffunktion nach einer [**WINHTTP \_ CALLBACK \_ STATUS SECURE \_ FAILURE-Benachrichtigung. \_**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) Weitere Informationen finden Sie unter [**WINHTTP \_ STATUS \_ CALLBACK**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_INVALID_CA"></span><span id="error_winhttp_secure_invalid_ca"></span>**FEHLER: \_ WINHTTP \_ SECURE \_ UNGÜLTIGE \_ ZERTIFIZIERUNGSSTELLE**
</dt> <dd> <dl> <dt>

12045
</dt> <dt>



Gibt an, dass eine Zertifikatkette verarbeitet, aber in einem Stammzertifikat beendet wurde, das vom Vertrauensanbieter nicht als vertrauenswürdig eingestuft wird (entspricht **CERT \_ E \_ UNTRUSTEDROOT**).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_INVALID_CERT"></span><span id="error_winhttp_secure_invalid_cert"></span>**FEHLER: \_ WINHTTP \_ SECURE \_ \_ UNGÜLTIGES ZERTIFIKAT**
</dt> <dd> <dl> <dt>

12169
</dt> <dt>



Gibt an, dass ein Zertifikat ungültig ist (äquivalent zu Fehlern wie **CERT \_ E \_ ROLE,** **CERT \_ E \_ PATHLENCONST,** **CERT E \_ \_ CRITICAL,** **CERT E \_ \_ PURPOSE,** **CERT E \_ \_ ISSUERCHAINING,** **CERT E \_ \_ MALFORMED** und **CERT E \_ \_ CHAINING).**


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SHUTDOWN"></span><span id="error_winhttp_shutdown"></span>**FEHLER: \_ WINHTTP \_ SHUTDOWN**
</dt> <dd> <dl> <dt>

12012
</dt> <dt>



Die WinHTTP-Funktionsunterstützung wird heruntergefahren oder entladen.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_TIMEOUT"></span><span id="error_winhttp_timeout"></span>**\_FEHLER: \_ WINHTTP-TIMEOUT**
</dt> <dd> <dl> <dt>

12002
</dt> <dt>



Timeout für die Anforderung.

Dieser Fehler kann als Ergebnis des TCP/IP-Time out-Verhaltens zurückgegeben werden, unabhängig von den in den HTTP-Diensten Windows Festgelegten Time out-Werten.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_UNABLE_TO_DOWNLOAD_SCRIPT"></span><span id="error_winhttp_unable_to_download_script"></span>**FEHLER: \_ WINHTTP \_ KONNTE SKRIPT NICHT \_ \_ \_ HERUNTERLADEN**
</dt> <dd> <dl> <dt>

12167
</dt> <dt>



Die PAC-Datei kann nicht heruntergeladen werden. Beispielsweise war der Server, auf den die PAC-URL verweist, möglicherweise nicht erreichbar, oder der Server hat die Antwort 404 NOT FOUND zurückgegeben.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_UNHANDLED_SCRIPT_TYPE"></span><span id="error_winhttp_unhandled_script_type"></span>**FEHLER: \_ WINHTTP \_ UNHANDLED \_ SCRIPT \_ TYPE**
</dt> <dd> <dl> <dt>

12176
</dt> <dt>



Der Skripttyp wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_UNRECOGNIZED_SCHEME"></span><span id="error_winhttp_unrecognized_scheme"></span>**FEHLER: \_ WINHTTP \_ UNRECOGNIZED \_ SCHEME**
</dt> <dd> <dl> <dt>

12006
</dt> <dt>



Die URL hat ein anderes Schema als "http:" oder "https:" angegeben.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_ENOUGH_MEMORY"></span><span id="error_not_enough_memory"></span>**FEHLER: \_ NICHT \_ GENÜGEND \_ ARBEITSSPEICHER**
</dt> <dd> <dl> <dt>



Es war nicht genügend Arbeitsspeicher verfügbar, um den angeforderten Vorgang abschließen zu können.

**Header:** Deklariert in "Winerror.h"


</dt> </dl> </dd> <dt>

<span id="ERROR_INSUFFICIENT_BUFFER"></span><span id="error_insufficient_buffer"></span>**FEHLER: \_ NICHT GENÜGEND \_ PUFFER**
</dt> <dd> <dl> <dt>



Die Größe des Puffers in Bytes, der für eine Funktion bereitgestellt wurde, reicht nicht aus, um die zurückgegebenen Daten zu enthalten. Weitere Informationen finden Sie unter der jeweiligen Funktion.

**Header:** Deklariert in "Winerror.h"


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_HANDLE"></span><span id="error_invalid_handle"></span>**FEHLER \_ UNGÜLTIGES \_ HANDLE**
</dt> <dd> <dl> <dt>



Das an die Anwendungsprogrammierschnittstelle (API) übergebene Handle wurde entweder ungültig gemacht oder geschlossen.

**Header:** Deklariert in "Winerror.h"


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MORE_FILES"></span><span id="error_no_more_files"></span>**FEHLER: \_ \_ KEINE DATEIEN \_ MEHR**
</dt> <dd> <dl> <dt>



Es wurden keine Dateien mehr gefunden.

**Header:** Deklariert in "Winerror.h"


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MORE_ITEMS"></span><span id="error_no_more_items"></span>**FEHLER: \_ \_ KEINE ELEMENTE \_ MEHR**
</dt> <dd> <dl> <dt>



Es wurden keine elemente mehr gefunden.

**Header:** Deklariert in "Winerror.h"


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SUPPORTED"></span><span id="error_not_supported"></span>**FEHLER \_ WIRD NICHT \_ UNTERSTÜTZT**
</dt> <dd> <dl> <dt>



Der erforderliche Protokollstapel wird nicht geladen, und die Anwendung kann WinSock nicht starten.

**Header:** Deklariert in "Winerror.h"


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Hinweise

Informationen Windows XP und Windows 2000 finden Sie im Abschnitt Laufzeitanforderungen der [WinHttp-Startseite.](winhttp-start-page.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP, Windows 2000 Professional nur mit \[ SP3-Desktop-Apps\]<br/>            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003, Windows 2000 Server nur mit \[ SP3-Desktop-Apps\]<br/>         |
| Verteilbare Komponente<br/>          | WinHTTP 5.0 und Internet Explorer 5.01 oder höher unter Windows XP und Windows 2000.<br/> |
| Header<br/>                   | <dl> <dt>Winhttp.h</dt> </dl>       |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[WinHTTP-Versionen](winhttp-versions.md)
</dt> </dl>

 

