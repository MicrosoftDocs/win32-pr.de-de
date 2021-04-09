---
description: Die in diesem Thema identifizierten Fehler Werte werden von GetLastError zurückgegeben, wenn eine der Microsoft Windows HTTP-Dienste (WinHTTP) fehlschlägt.
ms.assetid: c8a863cd-d36c-4ec8-ac49-0b714a5e4cc2
title: Fehlermeldungen (WinHTTP. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eccdc8be4b1e7c3cc7f9a03403c2f8778ddd19b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866232"
---
# <a name="error-messages-winhttph"></a>Fehlermeldungen (WinHTTP. h)

Die unten aufgeführten Fehler Werte werden von [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) zurückgegeben, wenn eine der Microsoft Windows HTTP-Dienste (WinHTTP) fehlschlägt und auch in den unteren 16 Bits der [**HRESULT**](../com/structure-of-com-error-codes.md) -Fehler zurückgegeben wird, die vom [**WinHttpRequest**](winhttprequest.md) -Objekt zurückgegeben werden.

Fehler Werte, deren Namen mit "Fehler- \_ WinHTTP \_ " beginnen, sind spezifisch für die WinHTTP-Funktionen. Die WinHTTP-Funktionen geben ggf. auch Windows-Fehlermeldungen zurück.

<dl> <dt>

<span id="ERROR_WINHTTP_AUTO_PROXY_SERVICE_ERROR"></span><span id="error_winhttp_auto_proxy_service_error"></span>**Fehler beim \_ WinHTTP- \_ automatischen \_ Proxy \_ Dienst \_ .**
</dt> <dd> <dl> <dt>

12178
</dt> <dt>



Wird von [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) zurückgegeben, wenn ein Proxy für die angegebene URL nicht gefunden werden kann.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_AUTODETECTION_FAILED"></span><span id="error_winhttp_autodetection_failed"></span>**Fehler beim \_ WinHTTP- \_ Autoerkennungs-Fehler. \_**
</dt> <dd> <dl> <dt>

12180
</dt> <dt>



Wird von [**winhttpdetectautoproxyconfigurl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl) zurückgegeben, wenn WinHTTP die URL der PAC-Datei (Proxy Auto-Configuration) nicht ermitteln konnte.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_BAD_AUTO_PROXY_SCRIPT"></span><span id="error_winhttp_bad_auto_proxy_script"></span>**Fehler \_ WinHTTP-fehlerhaftes \_ \_ \_ autoproxyskript \_**
</dt> <dd> <dl> <dt>

12166
</dt> <dt>



Fehler beim Ausführen des Skriptcodes in der PAC-Datei (Proxy Auto-Configuration).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CANNOT_CALL_AFTER_OPEN"></span><span id="error_winhttp_cannot_call_after_open"></span>**Fehler \_ WinHTTP \_ kann \_ \_ nach dem \_ Öffnen nicht aufgerufen werden.**
</dt> <dd> <dl> <dt>

12103
</dt> <dt>



Wird vom [**HttpRequest**](winhttprequest.md) -Objekt zurückgegeben, wenn eine angegebene Option nicht angefordert werden kann, nachdem die [**Open**](iwinhttprequest-open.md) -Methode aufgerufen wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CANNOT_CALL_AFTER_SEND"></span><span id="error_winhttp_cannot_call_after_send"></span>**Fehler \_ WinHTTP \_ kann \_ \_ nach dem \_ Senden nicht aufgerufen werden.**
</dt> <dd> <dl> <dt>

12102
</dt> <dt>



Wird vom [**HttpRequest**](winhttprequest.md) -Objekt zurückgegeben, wenn ein angeforderter Vorgang nach dem Aufrufen der [**Send**](iwinhttprequest-send.md) -Methode nicht ausgeführt werden kann.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CANNOT_CALL_BEFORE_OPEN"></span><span id="error_winhttp_cannot_call_before_open"></span>**Fehler \_ WinHTTP \_ kann \_ nicht \_ vor dem \_ Öffnen aufgerufen werden**
</dt> <dd> <dl> <dt>

12100
</dt> <dt>



Wird vom [**HttpRequest**](winhttprequest.md) -Objekt zurückgegeben, wenn ein angeforderter Vorgang vor dem Aufrufen der [**Open**](iwinhttprequest-open.md) -Methode nicht ausgeführt werden kann.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CANNOT_CALL_BEFORE_SEND"></span><span id="error_winhttp_cannot_call_before_send"></span>**Fehler \_ WinHTTP \_ kann \_ nicht \_ vor dem \_ senden aufgerufen werden**
</dt> <dd> <dl> <dt>

12101
</dt> <dt>



Wird vom [**HttpRequest**](winhttprequest.md) -Objekt zurückgegeben, wenn ein angeforderter Vorgang vor dem Aufrufen der [**Send**](iwinhttprequest-send.md) -Methode nicht ausgeführt werden kann.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CANNOT_CONNECT"></span><span id="error_winhttp_cannot_connect"></span>**Fehler beim \_ \_ Herstellen einer Verbindung mit WinHTTP \_**
</dt> <dd> <dl> <dt>

12029
</dt> <dt>



Wird zurückgegeben, wenn die Verbindung zum Server fehlgeschlagen ist


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CLIENT_AUTH_CERT_NEEDED"></span><span id="error_winhttp_client_auth_cert_needed"></span>**Fehler beim \_ WinHTTP- \_ Client Authentifizierungs \_ \_ Zertifikat. \_**
</dt> <dd> <dl> <dt>



Der Server erfordert eine SSL-Client Authentifizierung. Die Anwendung ruft die Liste der Zertifikat Aussteller durch Aufrufen von [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) mit der Option **WinHTTP- \_ Option \_ Client \_ Zertifikat \_ Aussteller \_ Liste** ab. Weitere Informationen finden Sie in der Option **WinHTTP- \_ Option \_ Client \_ Zertifikat \_ Aussteller \_ Liste** .

Wenn der Server das Client Zertifikat anfordert, jedoch nicht erforderlich ist, kann die Anwendung [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) alternativ mit der **\_ Option \_ Client \_ CERT- \_ Kontext Option WinHTTP-Option** aufruft. In diesem Fall gibt die Anwendung das WinHTTP- \_ \_ Kontext Makro "No Client \_ CERT" \_ im *lpBuffer* -Parameter von " **WinHttpSetOption**" an. Weitere Informationen finden Sie unter der **WinHTTP- \_ Option \_ Client CERT- \_ \_ Kontext** Option.

**Windows Server 2003 mit SP1 und Windows XP mit SP2:** Dieser Fehler wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CLIENT_CERT_NO_ACCESS_PRIVATE_KEY"></span><span id="error_winhttp_client_cert_no_access_private_key"></span>**Fehler \_ WinHTTP \_ Client \_ CERT \_ No \_ Access \_ private \_ Key**
</dt> <dd> <dl> <dt>



Die Anwendung verfügt nicht über die erforderlichen Berechtigungen für den Zugriff auf den privaten Schlüssel, der dem Client Zertifikat zugeordnet ist.

**Windows Server 2003 mit SP1 und Windows XP mit SP2:** Dieser Fehler wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CLIENT_CERT_NO_PRIVATE_KEY"></span><span id="error_winhttp_client_cert_no_private_key"></span>**Fehler \_ WinHTTP \_ Client \_ CERT \_ kein \_ privater \_ Schlüssel**
</dt> <dd> <dl> <dt>



Dem Kontext für das SSL-Client Zertifikat ist kein privater Schlüssel zugeordnet. Das Client Zertifikat wurde möglicherweise ohne den privaten Schlüssel auf den Computer importiert.

**Windows Server 2003 mit SP1 und Windows XP mit SP2:** Dieser Fehler wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CHUNKED_ENCODING_HEADER_SIZE_OVERFLOW"></span><span id="error_winhttp_chunked_encoding_header_size_overflow"></span>**Fehler bei WinHTTP-segmentierter \_ \_ \_ Codierungs \_ Header \_ Größe. \_ Überlauf**
</dt> <dd> <dl> <dt>

12183
</dt> <dt>



Wird von [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) zurückgegeben, wenn beim Analysieren der segmentierten Codierung eine Überlauf Bedingung auftritt.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CLIENT_AUTH_CERT_NEEDED"></span><span id="error_winhttp_client_auth_cert_needed"></span>**Fehler beim \_ WinHTTP- \_ Client Authentifizierungs \_ \_ Zertifikat. \_**
</dt> <dd> <dl> <dt>

12044
</dt> <dt>



Wird von [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) zurückgegeben, wenn der Server die Client Authentifizierung anfordert.

**Windows Server 2003 mit SP1 und Windows XP mit SP2:** Dieser Fehler wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CONNECTION_ERROR"></span><span id="error_winhttp_connection_error"></span>**Fehler beim \_ WinHTTP- \_ Verbindungs \_ Fehler.**
</dt> <dd> <dl> <dt>

12030
</dt> <dt>



Die Verbindung mit dem Server wurde zurückgesetzt oder beendet, oder es wurde ein nicht kompatibles SSL-Protokoll gefunden. Beispielsweise unterstützt die WinHTTP-Version 5,1 nicht SSL2 verwendet, es sei denn, der Client aktiviert Sie ausdrücklich.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_HEADER_ALREADY_EXISTS"></span><span id="error_winhttp_header_already_exists"></span>**\_WinHTTP-Fehler \_ Header ist \_ bereits \_ vorhanden.**
</dt> <dd> <dl> <dt>

12155
</dt> <dt>



Veralteten nicht mehr verwendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_HEADER_COUNT_EXCEEDED"></span><span id="error_winhttp_header_count_exceeded"></span>**Fehler bei \_ WinHTTP- \_ Header \_ Anzahl \_ überschritten.**
</dt> <dd> <dl> <dt>

12181
</dt> <dt>



Wird von [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) zurückgegeben, wenn eine größere Anzahl von Headern in einer Antwort vorhanden war, als WinHTTP empfangen konnte.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_HEADER_NOT_FOUND"></span><span id="error_winhttp_header_not_found"></span>**Fehler beim \_ WinHTTP- \_ Header \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

12150
</dt> <dt>



Der angeforderte Header wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_HEADER_SIZE_OVERFLOW"></span><span id="error_winhttp_header_size_overflow"></span>**Fehler bei \_ WinHTTP- \_ Header \_ Größen \_ Überlauf.**
</dt> <dd> <dl> <dt>

12182
</dt> <dt>



Wird von [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) zurückgegeben, wenn die empfangene Header Größe den Grenzwert für das Anforderungs handle überschreitet.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_INCORRECT_HANDLE_STATE"></span><span id="error_winhttp_incorrect_handle_state"></span>**Fehler \_ WinHTTP- \_ fehlerhafter \_ handle- \_ Zustand**
</dt> <dd> <dl> <dt>

12019
</dt> <dt>



Der angeforderte Vorgang kann nicht ausgeführt werden, da das angegebene Handle nicht den richtigen Status aufweist.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_INCORRECT_HANDLE_TYPE"></span><span id="error_winhttp_incorrect_handle_type"></span>**\_fehlerhafter WinHTTP- \_ \_ handle- \_ Typ**
</dt> <dd> <dl> <dt>

12018
</dt> <dt>



Der angegebene Handlertyp ist für diesen Vorgang falsch.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_INTERNAL_ERROR"></span><span id="error_winhttp_internal_error"></span>**Fehler bei \_ WinHTTP- \_ interner \_ Fehler.**
</dt> <dd> <dl> <dt>

12004
</dt> <dt>



Ein interner Fehler ist aufgetreten.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_INVALID_OPTION"></span><span id="error_winhttp_invalid_option"></span>**Fehler bei \_ WinHTTP- \_ \_ Option ungültig**
</dt> <dd> <dl> <dt>

12009
</dt> <dt>



Eine Anforderung an " [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) " oder " [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) " hat einen ungültigen Optionswert angegeben.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_INVALID_QUERY_REQUEST"></span><span id="error_winhttp_invalid_query_request"></span>**Fehler bei \_ WinHTTP- \_ \_ Abfrage \_ Anforderung**
</dt> <dd> <dl> <dt>

12154
</dt> <dt>



Veralteten nicht mehr verwendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_INVALID_SERVER_RESPONSE"></span><span id="error_winhttp_invalid_server_response"></span>**Fehler \_ WinHTTP \_ - \_ Antwort auf ungültige Server \_**
</dt> <dd> <dl> <dt>

12152
</dt> <dt>



Die Serverantwort kann nicht analysiert werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_INVALID_URL"></span><span id="error_winhttp_invalid_url"></span>**Fehler \_ WinHTTP- \_ ungültige \_ URL**
</dt> <dd> <dl> <dt>

12005
</dt> <dt>



Die URL ist nicht gültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_LOGIN_FAILURE"></span><span id="error_winhttp_login_failure"></span>**Fehler beim \_ WinHTTP- \_ Anmelde \_ Fehler.**
</dt> <dd> <dl> <dt>

12015
</dt> <dt>



Der Anmeldeversuch ist fehlgeschlagen. Wenn dieser Fehler auftritt, sollte das Anforderungs Handle mit [**WinHttpCloseHandle**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpclosehandle)geschlossen werden. Ein neues Anforderungs Handle muss erstellt werden, bevor die Funktion erneut versucht wird, die den Fehler ursprünglich erzeugt hat.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_NAME_NOT_RESOLVED"></span><span id="error_winhttp_name_not_resolved"></span>**\_WinHTTP-Fehler \_ Name wurde \_ nicht \_ aufgelöst.**
</dt> <dd> <dl> <dt>

12007
</dt> <dt>



Der Servername kann nicht aufgelöst werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_NOT_INITIALIZED"></span><span id="error_winhttp_not_initialized"></span>**Fehler \_ WinHTTP wurde \_ nicht \_ initialisiert.**
</dt> <dd> <dl> <dt>

12172
</dt> <dt>



Veralteten nicht mehr verwendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_OPERATION_CANCELLED"></span><span id="error_winhttp_operation_cancelled"></span>**Fehler beim \_ WinHTTP- \_ Vorgang. \_**
</dt> <dd> <dl> <dt>

12017
</dt> <dt>



Der Vorgang wurde abgebrochen, in der Regel, weil das Handle, für das die Anforderung ausgeführt wurde, vor dem Abschluss des Vorgangs geschlossen wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_OPTION_NOT_SETTABLE"></span><span id="error_winhttp_option_not_settable"></span>**Fehler bei \_ WinHTTP- \_ Option \_ nicht \_ feststellbar.**
</dt> <dd> <dl> <dt>

12011
</dt> <dt>



Die angeforderte Option kann nicht festgelegt werden, sondern nur abgefragt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_OUT_OF_HANDLES"></span><span id="error_winhttp_out_of_handles"></span>**Fehler bei \_ WinHTTP- \_ \_ über \_ griffen**
</dt> <dd> <dl> <dt>

12001
</dt> <dt>



Veralteten nicht mehr verwendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_REDIRECT_FAILED"></span><span id="error_winhttp_redirect_failed"></span>**Fehler bei \_ WinHTTP- \_ Umleitung. \_**
</dt> <dd> <dl> <dt>

12156
</dt> <dt>



Die Umleitung ist fehlgeschlagen, da entweder das Schema geändert wurde oder alle Versuche zum Umleiten fehlgeschlagen sind (standardmäßig fünf Versuche).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_RESEND_REQUEST"></span><span id="error_winhttp_resend_request"></span>**Fehler bei \_ WinHTTP- \_ Anforderung zum erneuten senden. \_**
</dt> <dd> <dl> <dt>

12032
</dt> <dt>



Die WinHTTP-Funktion konnte nicht ausgeführt werden. Die gewünschte Funktion kann auf demselben Anforderungs handle wiederholt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_RESPONSE_DRAIN_OVERFLOW"></span><span id="error_winhttp_response_drain_overflow"></span>**Fehler beim \_ WinHTTP- \_ Antwort- \_ \_ Überlauf Überlauf.**
</dt> <dd> <dl> <dt>

12184
</dt> <dt>



Wird zurückgegeben, wenn eine eingehende Antwort eine interne WinHTTP-Größenbeschränkung überschreitet.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SCRIPT_EXECUTION_ERROR"></span><span id="error_winhttp_script_execution_error"></span>**Fehler beim \_ Ausführen des WinHTTP- \_ Skripts. \_ \_**
</dt> <dd> <dl> <dt>

12177
</dt> <dt>



Beim Ausführen eines Skripts ist ein Fehler aufgetreten.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_CERT_CN_INVALID"></span><span id="error_winhttp_secure_cert_cn_invalid"></span>**Fehler " \_ WinHTTP \_ Secure \_ CERT CN" ist \_ \_ ungültig.**
</dt> <dd> <dl> <dt>

12038
</dt> <dt>



Wird zurückgegeben, wenn der CN-Name des Zertifikats nicht mit dem übergebenen Wert übereinstimmt (entspricht dem Fehler " **CERT \_ E \_ CN \_ No \_ Match** ").


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_CERT_DATE_INVALID"></span><span id="error_winhttp_secure_cert_date_invalid"></span>**Fehler " \_ WinHTTP \_ Secure \_ CERT Date" ist \_ \_ ungültig.**
</dt> <dd> <dl> <dt>

12037
</dt> <dt>



Gibt an, dass ein erforderliches Zertifikat nicht innerhalb seines Gültigkeits Zeitraums liegt, wenn die aktuelle Systemuhr oder der Zeitstempel in der signierten Datei überprüft wird, oder dass die Gültigkeits Zeiträume der Zertifizierungs Kette nicht ordnungsgemäß geschachtelt werden (äquivalent zu einem **Zertifikat \_ e \_** oder einem **CERT \_ e \_ validityperiodnist** -Fehler).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_CERT_REV_FAILED"></span><span id="error_winhttp_secure_cert_rev_failed"></span>**Fehler bei \_ WinHTTP \_ Secure \_ CERT \_ Rev \_ .**
</dt> <dd> <dl> <dt>

12057
</dt> <dt>



Gibt an, dass die Sperrung nicht geprüft werden kann, weil der Sperr Server offline war (äquivalent zur Sperre von **crypt \_ E, \_ \_ Offline**).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_CERT_REVOKED"></span><span id="error_winhttp_secure_cert_revoked"></span>**Fehler " \_ WinHTTP \_ Secure \_ CERT \_ " wurde gesperrt.**
</dt> <dd> <dl> <dt>

12170
</dt> <dt>



Gibt an, dass ein Zertifikat widerrufen wurde (äquivalent zu **crypt \_ E \_ widerrufen**).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_CERT_WRONG_USAGE"></span><span id="error_winhttp_secure_cert_wrong_usage"></span>**Fehler bei \_ WinHTTP \_ Secure \_ CERT \_ falsche \_ Verwendung**
</dt> <dd> <dl> <dt>

12179
</dt> <dt>



Gibt an, dass ein Zertifikat für die angeforderte Verwendung ungültig ist (äquivalent zur **\_ \_ falschen \_ Verwendung von CERT E**).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_CHANNEL_ERROR"></span><span id="error_winhttp_secure_channel_error"></span>**Fehler bei WinHTTP-Fehler des \_ \_ sicheren \_ Kanals \_**
</dt> <dd> <dl> <dt>

12157
</dt> <dt>



Gibt an, dass ein Fehler mit einem sicheren Kanal aufgetreten ist (äquivalent zu Fehlercodes, die mit "sec \_ E \_ " beginnen, und "s \_ I \_ ", die in der Header Datei "Winerror. h" aufgeführt sind).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_FAILURE"></span><span id="error_winhttp_secure_failure"></span>**Fehler beim \_ WinHTTP- \_ sicheren \_ Fehler.**
</dt> <dd> <dl> <dt>

12175
</dt> <dt>



Es wurde mindestens ein Fehler im vom Server gesendeten Secure Sockets Layer (SSL)-Zertifikat gefunden. Um zu ermitteln, welche Art von Fehler aufgetreten ist, überprüfen Sie, ob in einer Status Rückruffunktion eine Benachrichtigung über den [**WinHTTP- \_ Rückruf \_ Status \_ sicherer \_ Fehler**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) vorliegt. Weitere Informationen finden Sie unter [**WinHTTP- \_ Status \_ Rückruf**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_INVALID_CA"></span><span id="error_winhttp_secure_invalid_ca"></span>**Fehler \_ WinHTTP- \_ sichere \_ ungültige \_ Zertifizierungsstelle**
</dt> <dd> <dl> <dt>

12045
</dt> <dt>



Gibt an, dass eine Zertifikat Kette verarbeitet, aber in einem Stamm Zertifikat beendet wurde, das vom Vertrauens Anbieter nicht als vertrauenswürdig eingestuft wird (äquivalent zu **CERT \_ E \_ untrustdroot**).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_INVALID_CERT"></span><span id="error_winhttp_secure_invalid_cert"></span>**Fehler \_ WinHTTP \_ Secure \_ ungültiges \_ Zertifikat**
</dt> <dd> <dl> <dt>

12169
</dt> <dt>



Gibt an, dass ein Zertifikat ungültig ist (äquivalent zu Fehlern wie " **CERT \_ e \_ Role**", " **CERT e \_ \_ pathlenconst**", " **CERT \_ e \_ Critical**", " **CERT \_ e \_ Purpose**", " **CERT \_ e \_ issuerchaining**", " **CERT \_ e \_ falsch** formatiert" und " **CERT \_ e \_ Chaining**


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SHUTDOWN"></span><span id="error_winhttp_shutdown"></span>**Fehler beim Herunterfahren von \_ WinHTTP \_**
</dt> <dd> <dl> <dt>

12012
</dt> <dt>



Die Unterstützung der WinHTTP-Funktion wird heruntergefahren oder entladen.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_TIMEOUT"></span><span id="error_winhttp_timeout"></span>**Fehler beim \_ WinHTTP- \_ Timeout.**
</dt> <dd> <dl> <dt>

12002
</dt> <dt>



Timeout für die Anforderung.

Dieser Fehler kann aufgrund eines TCP/IP-Timeout Verhaltens zurückgegeben werden, unabhängig davon, welche Timeout Werte in Windows HTTP-Diensten festgelegt sind.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_UNABLE_TO_DOWNLOAD_SCRIPT"></span><span id="error_winhttp_unable_to_download_script"></span>**Fehler \_ WinHTTP \_ kann \_ \_ Skript nicht herunterladen \_**
</dt> <dd> <dl> <dt>

12167
</dt> <dt>



Die PAC-Datei kann nicht heruntergeladen werden. Beispielsweise ist der Server, auf den die PAC-URL verweist, möglicherweise nicht erreichbar, oder der Server hat die Antwort "404 nicht gefunden" zurückgegeben.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_UNHANDLED_SCRIPT_TYPE"></span><span id="error_winhttp_unhandled_script_type"></span>**Fehler bei \_ WinHTTP- \_ unbehandeltem \_ \_ Skripttyp**
</dt> <dd> <dl> <dt>

12176
</dt> <dt>



Der Skripttyp wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_UNRECOGNIZED_SCHEME"></span><span id="error_winhttp_unrecognized_scheme"></span>**Fehler beim nicht \_ erkannten WinHTTP- \_ \_ Schema**
</dt> <dd> <dl> <dt>

12006
</dt> <dt>



Die URL hat ein anderes Schema als "http:" oder "https:" angegeben.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_ENOUGH_MEMORY"></span><span id="error_not_enough_memory"></span>**Fehler \_ nicht \_ genügend Arbeits \_ Speicher**
</dt> <dd> <dl> <dt>



Es war nicht genügend Arbeitsspeicher verfügbar, um den angeforderten Vorgang abzuschließen.

**Header:** In "Winerror. h" deklariert


</dt> </dl> </dd> <dt>

<span id="ERROR_INSUFFICIENT_BUFFER"></span><span id="error_insufficient_buffer"></span>**Fehler \_ beim \_ Puffer.**
</dt> <dd> <dl> <dt>



Die Größe (in Bytes) des Puffers, der für eine Funktion angegeben wurde, war nicht ausreichend, um die zurückgegebenen Daten zu enthalten. Weitere Informationen finden Sie in der jeweiligen Funktion.

**Header:** In "Winerror. h" deklariert


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_HANDLE"></span><span id="error_invalid_handle"></span>**Fehler bei \_ ungültigem \_ handle**
</dt> <dd> <dl> <dt>



Das an die API (Application Programming Interface) über gegebene Handle wurde entweder ungültig oder wurde geschlossen.

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


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SUPPORTED"></span><span id="error_not_supported"></span>**Fehler \_ nicht \_ unterstützt**
</dt> <dd> <dl> <dt>



Der erforderliche Protokollstapel ist nicht geladen, und die Anwendung kann Winsock nicht starten.

**Header:** In "Winerror. h" deklariert


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

Informationen zu Windows XP und Windows 2000 finden Sie im Abschnitt [Lauf Zeitanforderungen](winhttp-start-page.md) auf der WinHTTP-Startseite.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP, Windows 2000 Professional mit SP3 \[ Desktop-Apps\]<br/>            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003, Windows 2000-Server mit \[ nur SP3-Desktop-Apps\]<br/>         |
| Verteilbare Komponente<br/>          | WinHTTP 5,0 und Internet Explorer 5,01 oder höher unter Windows XP und Windows 2000.<br/> |
| Header<br/>                   | <dl> <dt>WinHTTP. h</dt> </dl>       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[WinHTTP-Versionen](winhttp-versions.md)
</dt> </dl>

 

