---
Description: Die folgenden Optionsflags werden von WinHttpQueryOption und WinHttpSetOption unterstützt.
ms.assetid: 2d0441f4-ddba-4f2a-8861-8803cad6f1ac
title: Optionsflags (WinHTTP. h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 02/25/2020
ms.openlocfilehash: 56eea8e528c445c5ce6f852ff8841073dd74d6a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358770"
---
# <a name="option-flags"></a>Optionsflags

Die folgenden Optionsflags werden von [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) und [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)unterstützt.

<dl> <dt>

<span id="WINHTTP_OPTION_ASSURED_NON_BLOCKING_CALLBACKS"></span><span id="winhttp_option_assured_non_blocking_callbacks"></span>**WinHTTP- \_ Option \_ garantierte \_ nicht \_ blockierende \_ Rückrufe**
</dt> <dd> <dl> <dt>



Der Standardwert lautet FALSE. Wenn der Wert auf true festgelegt ist, garantiert WinHTTP nicht den Fortschritt, wenn Status Rückrufe durch die Client Anwendung blockiert werden.

Die Client Anwendung muss besondere Vorsicht walten lassen, um minimale Vorgänge innerhalb des Rückrufs auszuführen, ohne zu blockieren, so schnell wie möglich zurückzukehren, und insbesondere nicht auf nachfolgende WinHTTP-Aufrufe warten dürfen. Wenn diese Richtlinien nicht eingehalten werden, liegt wahrscheinlich eine negative Auswirkung auf die Leistung vor, oder es ist ein potenzieller Anwendungs Absturz vorhanden. Diese Option kann die Leistung verbessern, wenn Sie in der vorgeschriebenen Weise verwendet wird.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_AUTOLOGON_POLICY"></span><span id="winhttp_option_autologon_policy"></span>**\_ \_ \_ Richtlinie für die automatische WinHTTP-Option**
</dt> <dd> <dl> <dt>



Legt einen langen ganzzahligen Wert ohne Vorzeichen fest, der die [Richtlinie für die automatische Anmeldung](authentication-in-winhttp.md) mit einem der folgenden Werte angibt.

| Begriff | BESCHREIBUNG |
|-|-|
| <span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_HIGH"></span><span id="winhttp_autologon_security_level_high"></span>WinHTTP \_ Autologon- \_ Sicherheits \_ Stufe \_ hoch | Standard Anmelde Informationen werden nicht verwendet. Beachten Sie, dass dieses Flag nur wirksam wird, wenn Sie den Server mit dem tatsächlichen Computernamen angeben. Dies wird nicht wirksam, wenn Sie den Server durch "localhost" oder die IP-Adresse angeben. |
| <span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_LOW"></span><span id="winhttp_autologon_security_level_low"></span>WinHTTP \_ Autologon- \_ Sicherheits \_ Stufe \_ niedrig | Für alle Anforderungen wird eine authentifizierte Anmeldung mit den Standard Anmelde Informationen ausgeführt. |
| <span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_MEDIUM"></span><span id="winhttp_autologon_security_level_medium"></span>WinHTTP \_ Autologon- \_ Sicherheits \_ Stufe \_ Mittel | Eine authentifizierte Anmeldung mit den Standard Anmelde Informationen wird nur für Anforderungen im lokalen Intranet ausgeführt. |


</dl> </dd> <dt>

<span id="WINHTTP_OPTION_CALLBACK"></span><span id="winhttp_option_callback"></span>**WinHTTP- \_ options \_ Rückruf**
</dt> <dd> <dl> <dt>



Ruft den Zeiger auf die Rückruffunktion ab, die mit [**winhttpsetstatus Callback**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback)festgelegt wurde.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CLIENT_CERT_CONTEXT"></span><span id="winhttp_option_client_cert_context"></span>**WinHTTP- \_ Option \_ Client \_ Zertifikat \_ Kontext**
</dt> <dd> <dl> <dt>



Legt den Client Zertifikat Kontext fest. Wenn eine Anwendung den [**Fehler für das \_ WinHTTP- \_ Client \_ \_ \_**](error-messages.md)Authentifizierungszertifikat erhält, muss Sie " [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) " anrufen, um ein Zertifikat bereitzustellen, bevor Sie die Anforderung wiederholen. Im Rahmen der Verarbeitung dieser Option ruft WinHTTP [**certduplikatecertifitorecontext**](/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecertificatecontext) im vom Aufrufer bereitgestellten Zertifikat Kontext auf, damit der Zertifikat Kontext unabhängig vom Aufrufer freigegeben werden kann.

> [!Note]
> Die Anwendung sollte nicht versuchen, den Zertifikat Speicher im Zertifikat Speicher, \_ in dem der \_ \_ \_ Zertifikat Kontext abgerufen wurde [](/windows/desktop/api/wincrypt/nf-wincrypt-certclosestore) , mit dem Flag zum Erzwingen des Zertifikats der Zertifikat Schließung zu schließen. Es kann eine Zugriffsverletzung auftreten.

Wenn der Server ein Client Zertifikat anfordert, gibt [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)oder [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) einen Fehler an, dass ein Fehler für das [**\_ WinHTTP- \_ Client Authentifizierungs \_ \_ Zertifikat \_ erforderlich**](error-messages.md) ist. Wenn der Server das Zertifikat anfordert, es aber nicht benötigt, kann die Anwendung diese Option angeben, um anzugeben, dass Sie über kein Zertifikat verfügt. Der Server kann ein anderes Authentifizierungsschema auswählen oder den anonymen Zugriff auf den Server zulassen. Die Anwendung stellt das **WinHTTP \_ No \_ Client \_ CERT- \_ Kontext** Makro im *lpBuffer* -Parameter von [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) bereit, wie im folgenden Codebeispiel gezeigt.

``` syntax
BOOL fRet = WinHttpSetOption(hRequest,
                             WINHTTP_OPTION_CLIENT_CERT_CONTEXT,
                             WINHTTP_NO_CLIENT_CERT_CONTEXT,
                             0);
```

Wenn der Server ein Client Zertifikat erfordert, wird möglicherweise ein 403-HTTP-Statuscode als Antwort gesendet. Weitere Informationen finden Sie in der Option **WinHTTP- \_ Option \_ Client \_ Zertifikat \_ Aussteller \_ Liste** .


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CLIENT_CERT_ISSUER_LIST"></span><span id="winhttp_option_client_cert_issuer_list"></span>**WinHTTP- \_ Option \_ Client Zertifikat- \_ \_ Aussteller \_ Liste**
</dt> <dd> <dl> <dt>



Ruft eine [**secpkgcontext \_ issuverstinfoex**](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) -Struktur ab, wenn der Fehler von " [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) " oder " [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) " lautet, dass das **\_ WinHTTP- \_ Client Authentifizierungs \_ \_ Zertifikat \_ erforderlich** ist. Die Liste der Aussteller in der Struktur enthält eine Liste zulässiger Zertifizierungsstellen (ca) vom Server. Die Client Anwendung kann die Zertifizierungsstellen Liste filtern, um das Client Zertifikat für die SSL-Authentifizierung abzurufen.

Wenn der Server das Client Zertifikat anfordert, dies jedoch nicht erfordert, kann die Anwendung [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) mit der **\_ Option \_ Client \_ CERT- \_ Kontext Option WinHTTP-Option** abrufen. Weitere Informationen finden Sie unter der **WinHTTP- \_ Option \_ Client CERT- \_ \_ Kontext** Option.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CODEPAGE"></span><span id="winhttp_option_codepage"></span>**WinHTTP- \_ options \_ Codepage**
</dt> <dd> <dl> <dt>



Legt die [*Codepage*](glossary.md) fest, die verwendet wird, um die URL zu verarbeiten (d. h. Abfrage Zeichenfolge). Der Standardwert ist UTF8.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CONFIGURE_PASSPORT_AUTH"></span><span id="winhttp_option_configure_passport_auth"></span>**WinHTTP- \_ Option \_ Konfigurieren der \_ Passport \_ -Authentifizierung**
</dt> <dd> <dl> <dt>



Legt einen ganzzahligen Wert ohne Vorzeichen fest, der angibt, ob die [Passport-Authentifizierung bei der WinHTTP](passport-authentication-in-winhttp.md) -Authentifizierung aktiviert ist. Der Wert kann in folgenden Formen vorliegen:

| Begriff | BESCHREIBUNG |
|-|-|
| <span id="WINHTTP_DISABLE_PASSPORT_AUTH"></span><span id="winhttp_disable_passport_auth"></span>WinHTTP-Passport-Authentifizierung \_ Deaktivieren \_ \_ | Microsoft Passport Authentifizierung ist deaktiviert. Dies ist die Standardoption. |
| <span id="WINHTTP_DISABLE_PASSPORT_KEYRING"></span><span id="winhttp_disable_passport_keyring"></span>WinHTTP \_ - \_ Passport- \_ Schlüsselbund deaktivieren | Der Passport-Schlüsselbund ist deaktiviert. Dies ist die Standardoption. |
| <span id="WINHTTP_ENABLE_PASSPORT_AUTH"></span><span id="winhttp_enable_passport_auth"></span>WinHTTP \_ enable \_ Passport \_ auth | Die Passport-Authentifizierung ist aktiviert. |
| <span id="WINHTTP_ENABLE_PASSPORT_KEYRING"></span><span id="winhttp_enable_passport_keyring"></span>WinHTTP \_ - \_ Passport- \_ Schlüsselbund aktivieren | Der Passport-Schlüsselbund ist aktiviert. |

</dl> </dd> <dt>

<span id="WINHTTP_OPTION_CONNECT_RETRIES"></span><span id="winhttp_option_connect_retries"></span>**WinHTTP- \_ Option \_ Connect- \_ Wiederholungs Versuche**
</dt> <dd> <dl> <dt>



Legt einen ganzzahligen Wert ohne Vorzeichen fest oder ruft ihn ab, der die Anzahl der timeswinhttp-Versuche zum Herstellen einer Verbindung mit einem Host enthält. Die Microsoft Windows HTTP-Dienste (WinHTTP) versuchen nur einmal pro IP-Adresse (Internet Protocol). Wenn Sie z. b. versuchen, eine Verbindung mit einem mehrfach vernetzten Host mit 10 IP-Adressen herzustellen, und **WinHTTP- \_ Option \_ Connect \_ Retry** auf 7 festgelegt ist, versucht WinHTTP nur, eine Verbindung mit der ersten sieben IP-Adresse herzustellen. Wenn bei der gleichen Gruppe von 10 IP-Adressen die **WinHTTP- \_ Option \_ Connect \_ Retry** auf 20 festgelegt ist, versucht WinHTTP jede der 10 nur einmal. Wenn nach der angegebenen Anzahl von versuchen weiterhin ein Verbindungsversuch fehlschlägt oder das Verbindungs Timeout vorher abgelaufen ist, wird die Anforderung abgebrochen. Der Standardwert für die **WinHTTP- \_ Option \_ Connect- \_ Wiederholungen** sind fünf Versuche.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CONNECT_TIMEOUT"></span><span id="winhttp_option_connect_timeout"></span>**WinHTTP- \_ Option \_ Connect- \_ Timeout**
</dt> <dd> <dl> <dt>



Legt einen ganz Zahl Wert ohne Vorzeichen, der den Timeout Wert enthält, in Millisekunden fest oder ruft ihn ab. Wenn Sie diese Option auf unendlich (0xFFFFFFFF) festlegen, wird dieser Timer deaktiviert.

Wenn eine TCP-Verbindungsanforderung länger dauert als dieser Timeout Wert, wird die Anforderung abgebrochen. Der Standardwert für das Timeout beträgt 60 Sekunden. Wenn Sie versuchen, eine Verbindung mit mehreren IP-Adressen für einen einzelnen Host (einen mehrfach vernetzten Host) herzustellen, ist das Timeout Limit für jede einzelne Verbindung festgelegt.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CONNECTION_INFO"></span><span id="winhttp_option_connection_info"></span>**\_ \_ Verbindungs \_ Informationen zur WinHTTP-Option**
</dt> <dd> <dl> <dt>



Ruft die Quell-und Ziel-IP-Adresse und den Port der Anforderung ab, die die Antwort generiert hat, wenn " [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) " zurückgegeben wird. Die Anwendung ruft [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) mit der Option **\_ \_ Connection \_ Info der WinHTTP-Option** auf und stellt die [**WinHTTP- \_ Verbindungs \_ Informations**](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info) Struktur im *lpBuffer* -Parameter bereit. Weitere Informationen finden Sie unter **WinHTTP- \_ Verbindungs \_ Informationen**.

**Windows Server 2003 mit SP1 und Windows XP mit SP2:** Dieses Flag ist veraltet.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CONNECTION_STATS_V0"></span><span id="winhttp_option_connection_stats_v0"></span>**WinHTTP- \_ options \_ Verbindungs \_ Statistik \_ v0**
</dt> <dd> <dl> <dt>



Dient zum Abrufen der [**TCP- \_ Info \_ v0**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0) -Struktur für die zugrunde liegende Verbindung, die von der Anforderung verwendet wird. Die zurückgegebene Struktur kann Statistiken aus früheren Anforderungen enthalten, die über dieselbe Verbindung gesendet wurden.

> [!Note]
> Diese Option wurde durch die **WinHTTP- \_ options \_ Verbindungs \_ Statistik \_ v1** abgelöst.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CONNECTION_STATS_V1"></span><span id="winhttp_option_connection_stats_v1"></span>**WinHTTP- \_ options \_ Verbindungs \_ Statistik \_ v1**
</dt> <dd> <dl> <dt>



Dient zum Abrufen der [**TCP- \_ Info \_ v1**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1) -Struktur für die zugrunde liegende Verbindung, die von der Anforderung verwendet wird. Die zurückgegebene Struktur kann Statistiken aus früheren Anforderungen enthalten, die über dieselbe Verbindung gesendet wurden.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CONTEXT_VALUE"></span><span id="winhttp_option_context_value"></span>**WinHTTP- \_ options \_ Kontext \_ Wert**
</dt> <dd> <dl> <dt>



Legt ein **DWORD- \_ ptr** fest, das einen Zeiger auf den Kontextwert enthält, der diesem [HINTERNET](hinternet-handles-in-winhttp.md) -Handle zugeordnet ist, oder ruft diesen ab. Der im Puffer gespeicherte Wert wird verwendet, und dem Options Flag für die **WinHTTP- \_ Option- \_ Kontext \_ Wert** wird ein neuer Wert zugewiesen.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_DECOMPRESSION"></span><span id="winhttp_option_decompression"></span>**WinHTTP- \_ options \_ Dekomprimierung**
</dt> <dd> <dl> <dt>



Legt ein DWORD von Flags fest, die bestimmen, ob WinHTTP Antwort Texte mit komprimierten Inhalts Codierungen automatisch dekomprimieren soll. WinHTTP legt außerdem einen entsprechenden Accept-Encoding-Header fest, wobei alle vom Aufrufer bereitgestellten überschrieben werden. Diese Werte werden unterstützt:

| Begriff | BESCHREIBUNG |
|-|-|
| <span id="WINHTTP_DECOMPRESSION_FLAG_GZIP"></span><span id="winhttp_decompression_flag_gzip"></span>WinHTTP- \_ \_ decoderungsflag \_ gzip | Inhalts Codierung decodieren: gzip-Antworten. |
| <span id="WINHTTP_DECOMPRESSION_FLAG_DEFLATE"></span><span id="winhttp_decompression_flag_deflate"></span>WinHTTP-Debug- \_ \_ Flag \_ deflate | Inhalts Codierung decodieren: deflate von Antworten. |
| <span id="WINHTTP_DECOMPRESSION_FLAG_ALL"></span><span id="winhttp_decompression_flag_all"></span>WinHTTP- \_ \_ komprimierungsflag \_ alle | Decodieren Sie Antworten mit allen unterstützten Inhalts Codierungen. |

Standardmäßig werden von WinHTTP komprimierte Antworten an den Aufrufer unverändert bereitstellt.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_DISABLE_FEATURE"></span><span id="winhttp_option_disable_feature"></span>**Funktion zum Deaktivieren der WinHTTP- \_ Option \_ \_**
</dt> <dd> <dl> <dt>



Legt einen langen ganzzahligen Wert ohne Vorzeichen fest, der angibt, welche Funktionen mit einem oder mehreren der folgenden Flags deaktiviert werden. Beachten Sie, dass diese Funktion nur in Anforderungs Handles an [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) übergeben werden sollte, nachdem das Anforderungs Handle mit [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)erstellt und die Anforderung mit [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)gesendet wurde.

| Begriff | BESCHREIBUNG |
|-|-|
| <span id="WINHTTP_DISABLE_AUTHENTICATION"></span><span id="winhttp_disable_authentication"></span>WinHTTP \_ - \_ Authentifizierung deaktivieren | Die automatische Authentifizierung ist deaktiviert. |
| <span id="WINHTTP_DISABLE_COOKIES"></span><span id="winhttp_disable_cookies"></span>WinHTTP \_ - \_ Cookies deaktivieren | Das automatische Hinzufügen von Cookie-Headern zu Anforderungen ist deaktiviert. Außerdem werden zurückgegebene Cookies der cookiedatenbank nicht automatisch hinzugefügt. Das Deaktivieren von Cookies kann zu einer schlechten Leistung bei der Passport-Authentifizierung führen. |
| <span id="WINHTTP_DISABLE_KEEP_ALIVE"></span><span id="winhttp_disable_keep_alive"></span>WinHTTP \_ - \_ Keep-Alive-Aktivierung \_ | Deaktiviert die Keep-Alive-Semantik für die Verbindung. Die Keep-Alive-Semantik ist für MSN, NTLM und andere Arten der Authentifizierung erforderlich. |
| <span id="WINHTTP_DISABLE_REDIRECTS"></span><span id="winhttp_disable_redirects"></span>WinHTTP-Umleitungen \_ Deaktivieren \_ | Beim Senden von Anforderungen mit [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)ist die automatische Umleitung deaktiviert. Wenn die automatische Umleitung deaktiviert ist, muss eine Anwendung eine Rückruffunktion registrieren, damit die Passport-Authentifizierung erfolgreich ausgeführt werden kann. |


</dl> </dd> <dt>

<span id="WINHTTP_OPTION_DISABLE_SECURE_PROTOCOL_FALLBACK"></span><span id="winhttp_option_disable_secure_protocol_fallback"></span>**WinHTTP- \_ Option " \_ \_ Secure \_ Protocol \_ Fallback deaktivieren"**
</dt> <dd> <dl> <dt>



Verhindert, dass WinHTTP eine Verbindung mit einer niedrigeren Version des Sicherheitsprotokolls wiederholt, wenn die anfängliche Protokoll Aushandlung fehlschlägt.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_DISABLE_STREAM_QUEUE"></span><span id="winhttp_option_disable_stream_queue"></span>**WinHTTP- \_ Option ' \_ Stream- \_ \_ Warteschlange deaktivieren**
</dt> <dd> <dl> <dt>



Ermöglicht neuen Anforderungen das Öffnen einer zusätzlichen http/2-Verbindung, wenn die maximale Anzahl von gleichzeitigen Datenströmen erreicht wird, anstatt auf den nächsten verfügbaren Stream für eine vorhandene Verbindung zu warten.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_ENABLE_FEATURE"></span><span id="winhttp_option_enable_feature"></span>**Feature "WinHTTP- \_ Option \_ aktivieren" \_**
</dt> <dd> <dl> <dt>



Legt einen langen ganzzahligen Wert ohne Vorzeichen fest, der die derzeit aktivierten Funktionen angibt. Kann einen der folgenden Werte aufweisen.

| Begriff | BESCHREIBUNG |
|-|-|
| <span id="WINHTTP_ENABLE_SSL_REVERT_IMPERSONATION"></span><span id="winhttp_enable_ssl_revert_impersonation"></span>WinHTTP \_ enable \_ SSL \_ Revert \_ -Identitätswechsel | Wenn diese Option aktiviert ist, wird der Client Identitätswechsel von WinHTTP für die Dauer der SSL-Zertifikat Authentifizierungs Vorgänge vorübergehend wieder hergestellt. Dieser Wert kann nur für das Sitzungs handle festgelegt werden. |
| <span id="WINHTTP_ENABLE_SSL_REVOCATION"></span><span id="winhttp_enable_ssl_revocation"></span>WinHTTP-SSL-Sperrung \_ aktivieren \_ \_ | Wenn diese Option aktiviert ist, ermöglicht WinHTTP die SSL-Sperrung. Dieser Wert kann nur für das Anforderungs handle festgelegt werden. |


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_ENABLE_HTTP_PROTOCOL"></span><span id="winhttp_option_enable_http_protocol"></span>**WinHTTP- \_ Option \_ http- \_ \_ Protokoll aktivieren**
</dt> <dd> <dl> <dt>



Legt eine DWORD-Bitmaske von zulässigen erweiterten HTTP-Versionen fest. Dabei sind folgende Werte möglich:

| Begriff | BESCHREIBUNG |
|-|-|
| <span id="WINHTTP_PROTOCOL_FLAG_HTTP2"></span><span id="winhttp_protocol_flag_http2"></span>WinHTTP \_ - \_ protokollflag \_ HTTP2 (0x1) | Aktiviert http/2 für die Anforderung. |
| None (0x0) | Schränkt die Anforderung auf HTTP/1.1 und vor. |

Ältere Versionen von http (1,1 und früher) können mit dieser Option nicht deaktiviert werden. Der Standardwert ist 0x0.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_ENABLETRACING"></span><span id="winhttp_option_enabletracing"></span>**WinHTTP- \_ Option \_ EnableTracing**
</dt> <dd> <dl> <dt>



Legt einen **booleschen** Wert fest, der angibt, ob die Ablauf Verfolgung derzeit aktiviert ist. Weitere Informationen zur Ablauf Verfolgungs Funktion in WinHTTP finden Sie unter [WinHTTP-Ablauf Verfolgungs Funktion](winhttptracecfg-exe--a-trace-configuration-tool.md). Diese Option kann nur für ein NULL-  **HINTERNET** -handle festgelegt werden.


</dt> </dl> </dd>

<dt>

<span id="WINHTTP_OPTION_ENCODE_EXTRA"></span><span id="winhttp_option_encode_extra"></span>**WinHTTP- \_ Option " \_ \_ zusätzliche Codierung"**
</dt> <dd> <dl> <dt>



Aktiviert die URL-Codierung für den Pfad und die Abfrage Zeichenfolge.

Alternativ können Sie die Codierung auch vor dem Aufrufen von WinHTTP codieren.

</dt> </dl> </dd>

<dt>

<span id="WINHTTP_OPTION_EXTENDED_ERROR"></span><span id="winhttp_option_extended_error"></span>**Erweiterte WinHTTP- \_ Option- \_ \_ Fehler**
</dt> <dd> <dl> <dt>



Ruft den Wert einer langen ganzen Zahl ohne Vorzeichen ab, der einen Microsoft Windows Sockets-Fehlercode enthält, der den Fehlermeldungen angezeigt wurde, die \_ \_ \* zuletzt in diesem Thread Kontext zurückgegeben wurden. Sie können **null** als handle-Wert übergeben.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_GLOBAL_PROXY_CREDS"></span><span id="winhttp_option_global_proxy_creds"></span>**WinHTTP- \_ Option \_ globale Proxy-Anmelde- \_ \_ Befehle**
</dt> <dd> <dl> <dt>



Nimmt einen Zeiger auf eine WinHTTP-Struktur von " [**\_ \_ ExDS Ex**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) ", wobei der *HINTERNET* -Funktionsparameter auf **null** festgelegt ist. Für diese Option ist der Registrierungsschlüssel " **HKLM \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Internet Settings" erforderlich. Sharecredswithwinhttp**. Wenn dieser Registrierungsschlüssel nicht festgelegt ist, wird von WinHTTP die Fehler **Meldung " \_ WinHTTP \_ invalid \_**" zurückgegeben. Dieser Registrierungsschlüssel ist standardmäßig nicht vorhanden. Wenn er festgelegt ist, sendet WinInet Anmelde Informationen an WinHTTP. Wenn WinHTTP eine Authentifizierungs Aufforderung erhält und keine Anmelde Informationen für das aktuelle handle festgelegt sind, werden die von WinInet bereitgestellten Anmelde Informationen verwendet. Um Server Anmelde Informationen zusätzlich zu den Proxy Anmelde Informationen freizugeben, müssen Benutzer die **WinHTTP- \_ Option " \_ \_ globale \_ Server \_ Anmelde Informationen verwenden** " festlegen.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_GLOBAL_SERVER_CREDS"></span><span id="winhttp_option_global_server_creds"></span>**WinHTTP- \_ Option " \_ globale \_ Server \_ -Erstellungs Dienste"**
</dt> <dd> <dl> <dt>



Nimmt einen Zeiger auf eine WinHTTP-Struktur von " [**\_ \_ ExDS Ex**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) ", wobei der *HINTERNET* -Funktionsparameter auf **null** festgelegt ist. Für diese Option ist der Registrierungsschlüssel " **HKLM \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Internet Settings" erforderlich. Sharecredswithwinhttp**. Wenn dieser Registrierungsschlüssel nicht festgelegt ist, wird von WinHTTP die Fehler **Meldung " \_ WinHTTP \_ invalid \_**" zurückgegeben. Dieser Registrierungsschlüssel ist standardmäßig nicht vorhanden. Wenn er festgelegt ist, sendet WinInet Anmelde Informationen an WinHTTP. Wenn WinHTTP eine Authentifizierungs Aufforderung erhält und keine Anmelde Informationen für das aktuelle handle festgelegt sind, werden die von WinInet bereitgestellten Anmelde Informationen verwendet. Um Server Anmelde Informationen zusätzlich zu den Proxy Anmelde Informationen freizugeben, müssen Benutzer die **WinHTTP- \_ Option " \_ \_ globale \_ Server \_ Anmelde Informationen verwenden** " festlegen.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_HANDLE_TYPE"></span><span id="winhttp_option_handle_type"></span>**WinHTTP- \_ Option \_ handle- \_ Typ**
</dt> <dd> <dl> <dt>



Ruft den Wert einer langen ganzen Zahl ohne Vorzeichen ab, der den Typ des weiter gegebenen [hinternethandles](hinternet-handles-in-winhttp.md) enthält. Einer der folgenden Werte kann zurückgegeben werden:

| Begriff | BESCHREIBUNG |
|-|-|
| <span id="WINHTTP_HANDLE_TYPE_CONNECT"></span><span id="winhttp_handle_type_connect"></span>WinHTTP \_ - \_ Handlertyp \_ Verbindung | Das Handle ist ein Verbindungs Handle. |
| <span id="WINHTTP_HANDLE_TYPE_REQUEST"></span><span id="winhttp_handle_type_request"></span>WinHTTP \_ - \_ Handlertyp \_ Anforderung | Das Handle ist ein Anforderungs handle. |
| <span id="WINHTTP_HANDLE_TYPE_SESSION"></span><span id="winhttp_handle_type_session"></span>WinHTTP \_ - \_ Handlertyp \_ Sitzung | Das Handle ist ein Sitzungs handle. |


</dl> </dd> <dt>

<span id="WINHTTP_OPTION_HTTP_PROTOCOL_REQUIRED"></span><span id="winhttp_option_http_protocol_required"></span>**WinHTTP- \_ Option \_ http- \_ Protokoll \_ erforderlich**
</dt> <dd> <dl> <dt>



Verhindert, dass andere Protokoll Versionen als die von der **WinHTTP- \_ Option \_ http- \_ \_ Protokoll aktivieren** für die Anforderung aktiviert werden.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_HTTP_PROTOCOL_USED"></span><span id="winhttp_option_http_protocol_used"></span>**WinHTTP- \_ Option \_ http- \_ Protokoll \_ verwendet**
</dt> <dd> <dl> <dt>



Ruft ein DWORD ab, das angibt, welche erweiterte http-Version für eine bestimmte Anforderung verwendet wurde. Eine Liste möglicher Werte finden Sie unter **WinHTTP- \_ Option \_ \_ http- \_ Protokoll aktivieren**.



</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_HTTP_VERSION"></span><span id="winhttp_option_http_version"></span>**WinHTTP- \_ Option \_ http- \_ Version**
</dt> <dd> <dl> <dt>



Legt eine [**http- \_ Versions \_ Informations**](/windows/win32/api/winhttp/ns-winhttp-http_version_info) Struktur fest, die die unterstützte HTTP-Version enthält, oder ruft Sie ab. Dies ist eine Prozess weite Option. Verwenden Sie für das Handle **null** .


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_IGNORE_CERT_REVOCATION_OFFLINE"></span><span id="winhttp_option_ignore_cert_revocation_offline"></span>**WinHTTP- \_ Option \_ Zertifikat Sperrung \_ \_ \_ Offline ignorieren**
</dt> <dd> <dl> <dt>



Ermöglicht sicheren Verbindungen die Verwendung von Sicherheitszertifikaten, für die die Zertifikats Sperr Liste nicht heruntergeladen werden konnte.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_IPV6_FAST_FALLBACK"></span><span id="winhttp_option_ipv6_fast_fallback"></span>**WinHTTP- \_ Option \_ IPv6- \_ schnelles \_ Fallback**
</dt> <dd> <dl> <dt>



Aktiviert den schnellen IPv6-Fall Back (glücklichere pipebälle) für die Verbindung. Dieses Verhalten ähnelt dem in [RFC 6555](https://tools.ietf.org/html/rfc6555) beschriebenen glücklichen Verhalten, das zum Verbessern der Verbindungszeiten in Netzwerken, in denen IPv6 unzuverlässig ist, beschrieben wird.
- Wenn sowohl IPv6-als auch IPv4-Adressen für einen bestimmten Host aufgelöst werden, beginnt WinHTTP mit dem Herstellen einer Verbindung mit der ersten aufgelösten IPv6-Adresse mit einem kurzen Timeout (300 ms).
- Wenn diese Verbindung nicht hergestellt werden kann, versucht WinHTTP, eine Verbindung mit der ersten aufgelösten IPv4-Adresse mit dem Standard Timeout herzustellen.
- Wenn die zweite Verbindung nicht hergestellt werden kann, versucht WinHTTP die erste aufgelöste IPv6-Adresse mit dem Standard Timeout.
- Wenn die dritte Verbindung fehlschlägt, wird das Standardverhalten für alle verbleibenden Adressen von WinHTTP wieder hergestellt, und es wird versucht, eine Verbindung mit jedem Standard Timeout herzustellen, bis eine Verbindung hergestellt oder keine Adressen mehr vorhanden sind.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_IS_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_is_proxy_connect_response"></span>**die WinHTTP- \_ Option \_ ist eine \_ Proxy \_ Verbindungs \_ Antwort.**
</dt> <dd> <dl> <dt>



Ruft ab, ob eine Proxy Return Connect-Antwort abgerufen werden kann.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_MAX_CONNS_PER_1_0_SERVER"></span><span id="winhttp_option_max_conns_per_1_0_server"></span>**WinHTTP-Option max. Anzahl von Verbindungs- \_ \_ \_ \_ und \_ 1 \_ 0- \_ Servern**
</dt> <dd> <dl> <dt>



Legt einen langen ganzzahligen Wert ohne Vorzeichen fest oder ruft ihn ab, der die maximale Anzahl von Verbindungen pro HTTP/1.0-Server enthält. Der Standardwert ist **unendlich**.

**Windows Vista mit SP1 und Windows Server 2008:** Dieses Flag ist veraltet.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_MAX_CONNS_PER_SERVER"></span><span id="winhttp_option_max_conns_per_server"></span>**WinHTTP-Option max. Anzahl von Verbindungs \_ \_ \_ \_ \_ Servern pro Server**
</dt> <dd> <dl> <dt>



Legt einen langen ganzzahligen Wert ohne Vorzeichen fest oder ruft ihn ab, der die maximale Anzahl der pro Server zulässigen Verbindungen enthält. Der Standardwert ist **unendlich**.

Wenn diese Option auf NULL festgelegt ist, legt WinHTTP das Limit für die Anzahl der Verbindungen auf 2 fest.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_MAX_HTTP_AUTOMATIC_REDIRECTS"></span><span id="winhttp_option_max_http_automatic_redirects"></span>**WinHTTP- \_ Option \_ Max. \_ \_ Automatische HTTP \_ -Umleitungen**
</dt> <dd> <dl> <dt>



Legt die maximale Anzahl von Umleitungen fest, die WinHTTP befolgt. der Standardwert ist 10. Diese Beschränkung verhindert, dass nicht autorisierte Standorte den WinHTTP-Client nach einer großen Anzahl von Umleitungen anhalten.

**Windows XP mit SP1 und Windows 2000 mit SP3:** Dieses Flag ist veraltet.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_MAX_HTTP_STATUS_CONTINUE"></span><span id="winhttp_option_max_http_status_continue"></span>**WinHTTP- \_ Option \_ Max HTTP-Status wird \_ \_ \_ fortgesetzt**
</dt> <dd> <dl> <dt>



Die maximale Anzahl von Informationen, die von 100-199-Statuscodes ignoriert werden, bevor der endgültige Statuscode an den WinHTTP-Client zurückgegeben wird. Die Statuscodes "Information 100-199" können vom Server vor dem endgültigen Statuscode gesendet werden und werden in der Spezifikation für HTTP/1.1 beschrieben (Weitere Informationen finden Sie unter [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt)). Der Standardwert ist 10.

**Windows XP mit SP1 und Windows 2000 mit SP3:** Dieses Flag ist veraltet.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_MAX_RESPONSE_DRAIN_SIZE"></span><span id="winhttp_option_max_response_drain_size"></span>**WinHTTP- \_ Option \_ Max. Antwort Ausgleichs \_ \_ \_ Größe**
</dt> <dd> <dl> <dt>



Eine gebundene Datenmenge, die aus Antworten entfernt wurde, um eine in Bytes angegebene Verbindung wiederzuverwenden. Der Standardwert ist 1 MB.

**Windows XP mit SP1 und Windows 2000 mit SP3:** Dieses Flag ist veraltet.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_MAX_RESPONSE_HEADER_SIZE"></span><span id="winhttp_option_max_response_header_size"></span>**WinHTTP- \_ Option \_ Max- \_ Antwort \_ Header \_ Größe**
</dt> <dd> <dl> <dt>



Eine gebundene Menge an der maximalen Größe des Header Teils der Serverantwort, angegeben in Bytes. Diese Bindung schützt den Client vor einem nicht autorisierten Server, der versucht, den Client zu stoppen, indem er eine Antwort mit einer unendlichen Menge von Header Daten sendet. Der Standardwert ist 64 KB.

**Windows XP mit SP1 und Windows 2000 mit SP3:** Dieses Flag ist veraltet.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PARENT_HANDLE"></span><span id="winhttp_option_parent_handle"></span>**über \_ \_ geordnetes \_ Handle der WinHTTP-Option**
</dt> <dd> <dl> <dt>



Ruft das übergeordnete Handle für dieses Handle ab.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PASSPORT_COBRANDING_TEXT"></span><span id="winhttp_option_passport_cobranding_text"></span>**WinHTTP- \_ Option \_ Passport- \_ cobrandingtext \_**
</dt> <dd> <dl> <dt>



Ruft eine Zeichenfolge ab, die den [*cobrandingtext*](glossary.md) enthält, der vom Passport-Anmelde Server bereitgestellt wird. Diese Option sollte sofort abgerufen werden, wenn der Anmelde Server mit dem Statuscode 401 antwortet. Eine Anwendung sollte eine Puffergröße (in Bytes) übergeben, die groß genug ist, um die zurückgegebene Zeichenfolge zu speichern.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PASSPORT_COBRANDING_URL"></span><span id="winhttp_option_passport_cobranding_url"></span>**WinHTTP- \_ Option \_ Passport- \_ cobrandingurl \_**
</dt> <dd> <dl> <dt>



Ruft eine Zeichenfolge ab, die eine URL für eine [*cobrandgrafiegrafik*](glossary.md) enthält, die vom Passport-Anmelde Server bereitgestellt wird. Diese Option sollte sofort abgerufen werden, wenn der Anmelde Server mit dem Statuscode 401 antwortet. Eine Anwendung sollte eine Puffergröße (in Bytes) übergeben, die groß genug ist, um die zurückgegebene Zeichenfolge zu speichern.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PASSPORT_RETURN_URL"></span><span id="winhttp_option_passport_return_url"></span>**Rückgabe-URL der WinHTTP- \_ Option \_ Passport \_ \_**
</dt> <dd> <dl> <dt>



Legt eine schreibgeschützte Option für ein Anforderungs Handle fest, das die Passport-Rückgabe-URL abruft.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PASSPORT_SIGN_OUT"></span><span id="winhttp_option_passport_sign_out"></span>**WinHTTP- \_ Option \_ Passport- \_ \_ Abmeldung**
</dt> <dd> <dl> <dt>



Legt die-Option für ein Sitzungs Handle fest, um sich von allen Passport-Anmeldungen abzumelden. Eine Anwendung sollte die Passport-Rückgabe-URL übergeben, die mit der **Rückgabe-URL der WinHTTP- \_ Option \_ Passport \_ \_** abgerufen wurde. Alle Cookies, die sich auf die Rückgabe-URL beziehen, werden gelöscht.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PASSWORD"></span><span id="winhttp_option_password"></span>**WinHTTP- \_ options \_ Kennwort**
</dt> <dd> <dl> <dt>



Legt einen Zeichen folgen Wert fest, der das einem Anforderungs Handle zugeordnete Kennwort enthält, oder ruft ihn ab.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PROXY"></span><span id="winhttp_option_proxy"></span>**WinHTTP- \_ options \_ Proxy**
</dt> <dd> <dl> <dt>



Legt eine [**WinHTTP- \_ Proxy \_ Informations**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) Struktur fest, die die Proxy Daten für ein vorhandenes Sitzungs handle oder Anforderungs Handle enthält, oder ruft Sie ab. Beim Abrufen von Proxy Daten muss eine Anwendung die in dieser Struktur enthaltenen **lpszProxy** -und **lpszProxyBypass** -Zeichen folgen (wenn Sie nicht **null** sind) mithilfe der [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) -Funktion freigeben. Eine Anwendung kann die globalen Proxy Daten (den Standard Proxy) Abfragen, indem Sie ein **null** -handle übergibt.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PROXY_PASSWORD"></span><span id="winhttp_option_proxy_password"></span>**WinHTTP- \_ Option \_ Proxy \_ Kennwort**
</dt> <dd> <dl> <dt>



Legt einen Zeichen folgen Wert fest, der das Kennwort für den Zugriff auf den Proxy enthält, oder ruft diesen ab.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PROXY_SPN_USED"></span><span id="winhttp_option_proxy_spn_used"></span>**WinHTTP- \_ options \_ Proxy- \_ SPN \_ verwendet**
</dt> <dd> <dl> <dt>



Ruft den Proxy Server Prinzipal Namen ab, den WinHTTP während der Authentifizierung für SSPI bereitgestellt hat. Dieser Zeichen folgen Wert ist für die Übergabe an [**sspipromptforcredencredene**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) nach einem Authentifizierungsfehler verwendbar.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PROXY_USERNAME"></span><span id="winhttp_option_proxy_username"></span>**WinHTTP- \_ Option \_ Proxy \_ Benutzername**
</dt> <dd> <dl> <dt>



Legt einen Zeichen folgen Wert fest, der den für den Zugriff auf den Proxy verwendeten Benutzernamen enthält, oder ruft ihn ab.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_READ_BUFFER_SIZE"></span><span id="winhttp_option_read_buffer_size"></span>**WinHTTP- \_ Option, \_ Lese \_ Puffer \_ Größe**
</dt> <dd> <dl> <dt>



Diese Option ist veraltet. Dies hat keine Auswirkungen.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_RECEIVE_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_receive_proxy_connect_response"></span>**WinHTTP- \_ Option \_ empfangen von \_ Proxy \_ Verbindungs \_ Antworten**
</dt> <dd> <dl> <dt>



Legt fest, ob die Proxy Antwort Entität abgerufen werden kann. Diese Option ist standardmäßig deaktiviert.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_RECEIVE_RESPONSE_TIMEOUT"></span><span id="winhttp_option_receive_response_timeout"></span>**WinHTTP- \_ Option- \_ Empfangs \_ Antwort \_ Timeout**
</dt> <dd> <dl> <dt>



Legt einen langen ganzzahligen Wert ohne Vorzeichen fest oder ruft ihn ab, der den Timeout Wert in Millisekunden enthält, der auf den Empfang aller Antwortheader für eine Anforderung gewartet werden soll. Wenn WinHTTP nicht alle Header innerhalb dieses Timeout Zeitraums empfängt, wird die Anforderung abgebrochen. Der Standardwert für das Timeout beträgt 90 Sekunden.

Dieses Timeout wird nur geprüft, wenn Daten vom Socket empfangen werden. Wenn das Timeout abläuft, wird die Client Anwendung daher erst benachrichtigt, wenn vom Server mehr Daten empfangen werden. Wenn keine Daten vom Server empfangen werden, kann die Verzögerung zwischen dem Timeout Ablauf und der Benachrichtigung über die Client Anwendung so groß sein wie der Timeout Wert, der mit dem Parameter *dwreceivetimeout* der [**winhttpsettimeouts**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts) -Funktion festgelegt wird.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_RECEIVE_TIMEOUT"></span><span id="winhttp_option_receive_timeout"></span>**\_ \_ Empfangs \_ Timeout für WinHTTP-Option**
</dt> <dd> <dl> <dt>



Legt einen ganz Zahl Wert ohne Vorzeichen fest oder ruft ihn ab, der den Timeout Wert (in Millisekunden) enthält, um eine partielle Antwort auf eine Anforderung zu empfangen oder einige Daten zu lesen. Wenn die Antwort länger dauert als dieser Timeout Wert, wird die Anforderung abgebrochen. Der Standard-Timeoutwert beträgt 30 Sekunden.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_REDIRECT_POLICY"></span><span id="winhttp_option_redirect_policy"></span>**WinHTTP- \_ Option \_ Umleitungs \_ Richtlinie**
</dt> <dd> <dl> <dt>



Legt das Verhalten von WinHTTP in Bezug auf die Behandlung eines 30X-http-Umleitungs Statuscodes fest. Diese Option kann für eine Sitzung oder ein Anforderungs Handle auf einen der folgenden Werte festgelegt werden:

| Begriff | BESCHREIBUNG |
|-|-|
| <span id="WINHTTP_OPTION_REDIRECT_POLICY_ALWAYS"></span><span id="winhttp_option_redirect_policy_always"></span>WinHTTP- \_ Option " \_ Umleitungs \_ Richtlinie" \_ immer | Alle Umleitungen werden automatisch befolgt. |
| <span id="WINHTTP_OPTION_REDIRECT_POLICY_DISALLOW_HTTPS_TO_HTTP"></span><span id="winhttp_option_redirect_policy_disallow_https_to_http"></span>WinHTTP- \_ Option \_ Umleitungs \_ Richtlinie \_ lässt HTTPS nicht \_ \_ zu \_ http zu | Alle Umleitungen werden befolgt, mit Ausnahme derjenigen, die von einer sicheren URL (HTTPS) zu einer unsicheren URL (http) stammen. Dies ist die Standardeinstellung. |
| <span id="WINHTTP_OPTION_REDIRECT_POLICY_NEVER"></span><span id="winhttp_option_redirect_policy_never"></span>WinHTTP- \_ Option \_ Umleitungs \_ Richtlinie \_ nie | Umleitungen werden nie befolgt. Der Status "30X" wird an die Anwendung zurückgegeben. |


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_REJECT_USERPWD_IN_URL"></span><span id="winhttp_option_reject_userpwd_in_url"></span>**WinHTTP \_ - \_ Option \_ userpwd \_ in \_ URL ablehnen**
</dt> <dd> <dl> <dt>



Lehnt URLs ab, die einen Benutzernamen und ein Kennwort enthalten. Diese Option lehnt auch URLs ab, die *username: Password* -Semantik enthalten, auch wenn kein Benutzername oder Kennwort angegeben ist. Beispielsweise werden " u:p@hostname ", " :@hostname ", " u:@hostname " und " :p@hostname " als ungültig gekennzeichnet. Wenn eine ungültige URL an die Funktion übermittelt wird, wird die [ \_ \_ ungültige \_ WinHTTP-URL](error-messages.md)zurückgegeben. Standardmäßig ist diese Option deaktiviert.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_REQUEST_PRIORITY"></span><span id="winhttp_option_request_priority"></span>**WinHTTP- \_ Option- \_ Anforderungs \_ Priorität**
</dt> <dd> <dl> <dt>



Diese Option ist veraltet. Dies hat keine Auswirkungen.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_REQUEST_STATS"></span><span id="winhttp_option_request_stats"></span>**\_ \_ Anforderungs \_ Statistik für WinHTTP-Optionen**
</dt> <dd> <dl> <dt>



Gibt Statistiken für die Anforderung zurück.  Eine Liste der verfügbaren Statistiken finden Sie unter [**WinHTTP- \_ Anforderungs \_ Statistiken**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats).


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_REQUEST_TIMES"></span><span id="winhttp_option_request_times"></span>**\_ \_ Anforderungs \_ Zeiten für WinHTTP-Optionen**
</dt> <dd> <dl> <dt>



Gibt Informationen zur zeitlichen Steuerung für die Anforderung zurück. Eine Liste der verfügbaren Zeitangaben finden Sie unter [**WinHTTP- \_ Anforderungs \_ Zeiten**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times).


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_RESOLVE_TIMEOUT"></span><span id="winhttp_option_resolve_timeout"></span>**WinHTTP- \_ Option ' \_ \_ Timeout auflösen '**
</dt> <dd> <dl> <dt>



Legt einen langen ganzzahligen Wert ohne Vorzeichen fest oder ruft ihn ab, der den Timeout Wert in Millisekunden zum Auflösen eines Host Namens enthält. Der Standardwert für das Timeout ist **unendlich**. Wenn ein nicht standardmäßiger Wert angegeben wird, gibt es einen mehr Aufwand für eine Thread Erstellung pro Namensauflösung.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SECURE_PROTOCOLS"></span><span id="winhttp_option_secure_protocols"></span>**\_ \_ sichere \_ Protokolle der WinHTTP-Option**
</dt> <dd> <dl> <dt>



Legt einen langen ganzzahligen Wert ohne Vorzeichen fest, der angibt, welche sicheren Protokolle zulässig sind. Standardmäßig sind nur SSL3 und das TLS1 verwendet in Windows 7 und Windows 8 aktiviert. Standardmäßig sind nur SSL3, TLS 1.0, TLS 1.1 und TLS 1.2 in Windows 8.1 und Windows 10 aktiviert. Der Wert kann eine Kombination aus einem oder mehreren der folgenden Werte sein.

| Begriff | BESCHREIBUNG |
|-|-|
| <span id="WINHTTP_FLAG_SECURE_PROTOCOL_ALL"></span><span id="winhttp_flag_secure_protocol_all"></span>sicheres WinHTTP- \_ Flag zum \_ sicheren \_ Protokoll \_ | Die Protokolle Secure Sockets Layer (SSL) 2,0, SSL 3,0 und Transport Layer Security (TLS) 1,0 können verwendet werden. |
| <span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL2"></span><span id="winhttp_flag_secure_protocol_ssl2"></span>Sicheres WinHTTP- \_ Flag \_ \_ \_ SSL2 verwendet | Das SSL 2,0-Protokoll kann verwendet werden. |
| <span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL3"></span><span id="winhttp_flag_secure_protocol_ssl3"></span>Sicheres WinHTTP- \_ Flag \_ \_ \_ SSL3 | Das SSL 3,0-Protokoll kann verwendet werden. |
| <span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1"></span><span id="winhttp_flag_secure_protocol_tls1"></span>Sicheres WinHTTP- \_ Flag \_ \_ \_ das TLS1 verwendet | Das TLS 1,0-Protokoll kann verwendet werden. |
| <span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_1"></span><span id="winhttp_flag_secure_protocol_tls1_1"></span>Sicheres WinHTTP- \_ Flag \_ \_ \_ das TLS1 verwendet \_ 1 | Das TLS 1,1-Protokoll kann verwendet werden. |
| <span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_2"></span><span id="winhttp_flag_secure_protocol_tls1_2"></span>Sicheres WinHTTP- \_ Flag \_ \_ \_ das TLS1 verwendet \_ 2 | Das TLS 1,2-Protokoll kann verwendet werden. |


</dl> </dd> <dt>

<span id="WINHTTP_OPTION_SECURITY_CERTIFICATE_STRUCT"></span><span id="winhttp_option_security_certificate_struct"></span>**Struktur der WinHTTP- \_ Option- \_ Sicherheits \_ Zertifikat \_**
</dt> <dd> <dl> <dt>



Ruft das Zertifikat für einen SSL/TLS-Server in die [**WinHTTP- \_ Zertifikat \_ Informations**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) Struktur ab. Die Anwendung muss die **lpszsubjetinfo** -und **lpszissuerinfo** -Member mit [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree)freigeben.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SECURITY_FLAGS"></span><span id="winhttp_option_security_flags"></span>**WinHTTP- \_ Option ( \_ \_ sicherheitsflags)**
</dt> <dd> <dl> <dt>



Legt einen langen ganzzahligen Wert ohne Vorzeichen fest oder ruft ihn ab, der die sicherheitsflags für ein Handle enthält. Dies kann eine Kombination folgender Werte sein:

| Begriff | BESCHREIBUNG |
|-|-|
| <span id="SECURITY_FLAG_IGNORE_CERT_CN_INVALID"></span><span id="security_flag_ignore_cert_cn_invalid"></span>sicherheitsflag zum \_ \_ Ignorieren von \_ Zertifikat \_ CN \_ ungültig |Ermöglicht einen ungültigen allgemeinen Namen in einem Zertifikat. Dies bedeutet, dass der von der Anwendung angegebene Servername nicht mit dem allgemeinen Namen im Zertifikat identisch ist. Wenn dieses Flag festgelegt ist, empfängt die Anwendung kein **WinHTTP- \_ Rückruf \_ - \_ Statusflag \_ CERT \_ CN \_ Ungültiger** Rückruf. |
| <span id="SECURITY_FLAG_IGNORE_CERT_DATE_INVALID"></span><span id="security_flag_ignore_cert_date_invalid"></span>sicherheitsflag " \_ \_ Zertifikat mit \_ \_ \_ ungültigem Zertifikat ignorieren" |Ermöglicht ein ungültiges Zertifikat Datum, d. h. ein abgelaufenes oder noch nicht effektives Zertifikat. Wenn dieses Flag festgelegt ist, empfängt die Anwendung keinen **\_ \_ \_ \_ \_ \_ ungültigen Rückruf für ein WinHTTP-Rückruf Status** Kennzeichen. |
| <span id="SECURITY_FLAG_IGNORE_UNKNOWN_CA"></span><span id="security_flag_ignore_unknown_ca"></span>\_sicherheitsflag \_ ignoriert \_ unbekannte \_ Zertifizierungsstelle | Lässt eine ungültige Zertifizierungsstelle zu. Wenn dieses Flag festgelegt ist, empfängt die Anwendung keinen **\_ \_ \_ \_ ungültigen \_** ZS-Rückruf des WinHTTP-Rückruf Status. |
| <span id="SECURITY_FLAG_IGNORE_CERT_WRONG_USAGE"></span><span id="security_flag_ignore_cert_wrong_usage"></span>\_sicherheitsflag \_ " \_ \_ falsche Zertifikat \_ Verwendung ignorieren" | Ermöglicht die Einrichtung der Identität eines Servers mit einem nicht-Serverzertifikat (z. b. einem Client Zertifikat). |
| <span id="SECURITY_FLAG_IGNORE_WEAK_SIGNATURE"></span><span id="security_flag_ignore_weak_signature"></span>\_sicherheitsflag \_ ignoriert \_ schwache \_ Signatur | Ermöglicht, dass eine schwache Signatur ignoriert wird.<br/>Dieses Flag ist im Rollup-Update für jedes Betriebssystem ab Windows 7 und Windows Server 2008 R2 verfügbar. |
| <span id="SECURITY_FLAG_SECURE"></span><span id="security_flag_secure"></span>\_sicherheitsflag \_ sicher | Verwendet sichere Übertragungen. Dies wird nur in einem [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)-aufrufswert zurückgegeben. |
| <span id="SECURITY_FLAG_STRENGTH_MEDIUM"></span><span id="security_flag_strength_medium"></span>sicherheitsflag- \_ \_ Stärke \_ Mittel | Verwendet die mittlere Verschlüsselung (56-Bit). Dies wird nur in einem [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)-aufrufswert zurückgegeben. |
| <span id="SECURITY_FLAG_STRENGTH_STRONG"></span><span id="security_flag_strength_strong"></span>sicherheitsflag- \_ \_ Stärke \_ stark | Verwendet die starke Verschlüsselung (128-Bit). Dies wird nur in einem [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)-aufrufswert zurückgegeben. |
| <span id="SECURITY_FLAG_STRENGTH_WEAK"></span><span id="security_flag_strength_weak"></span>sicherheitsflag- \_ \_ Stärke \_ schwach | Verwendet die schwache Verschlüsselung (40-Bit). Dies wird nur in einem [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)-aufrufswert zurückgegeben. |


</dl> </dd> <dt>

<span id="WINHTTP_OPTION_SECURITY_INFO"></span><span id="winhttp_option_security_info"></span>**\_ \_ Sicherheits \_ Informationen für die WinHTTP-Option**
</dt> <dd> <dl> <dt>



Gibt die SChannel-Verbindung und Chiffre Informationen für eine Anforderung zurück.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SECURITY_KEY_BITNESS"></span><span id="winhttp_option_security_key_bitness"></span>**WinHTTP- \_ Option- \_ Sicherheits \_ Schlüssel \_ Bitness**
</dt> <dd> <dl> <dt>



Ruft den Wert einer langen ganzen Zahl ohne Vorzeichen ab, der die Verschlüsselungsstärke des Verschlüsselungsschlüssels enthält. Eine höhere Zahl deutet auf eine strengere Verschlüsselung der Verschlüsselungsstärke hin.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SEND_TIMEOUT"></span><span id="winhttp_option_send_timeout"></span>**WinHTTP- \_ Option \_ Send \_ Timeout**
</dt> <dd> <dl> <dt>



Legt einen ganz Zahl Wert ohne Vorzeichen fest, der den Timeout Wert (in Millisekunden) enthält, um eine Anforderung zu senden oder Daten zu schreiben, oder ruft ihn ab. Wenn das Senden der Anforderung länger dauert als das Timeout, wird der Sendevorgang abgebrochen. Der Standardzeitraum bis zum Timeout beträgt 30 Sekunden.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SERVER_CBT"></span><span id="winhttp_option_server_cbt"></span>**WinHTTP- \_ options \_ Server \_ CBT**
</dt> <dd> <dl> <dt>



Ruft einen Zeiger auf eine [**secpkgcontext- \_ Bindungs**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings) Struktur ab, die ein channelbindungs Token (Channel Binding Token, CBT) angibt.

Ein Kanal Bindungs Token ist eine Eigenschaft eines sicheren Transport Kanals und wird verwendet, um einen Authentifizierungs Kanal an den sicheren Transport Kanal zu binden. Dieses Token kann nur von dieser Option abgerufen werden, nachdem eine SSL-Verbindung hergestellt wurde.

> [!Note]
> Wenn Sie diese Option und einen **null** -Wert für *lpBuffer* an [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) übergeben, wird \_ der Fehler nicht genügend \_ Puffer und die erforderliche Bytegröße für den Puffer im *lpdwbufferlength* -Parameter zurückgegeben. Dieser zurückgegebene Puffergrößen Wert kann in einem nachfolgenden Abfrage Abfrage für das channelbindungstoken übergebenen werden. Diese Schritte sind erforderlich, wenn Sie die WinHTTP- \_ Rückruf \_ Status \_ Anforderung verarbeiten möchten, wenn Sie Anforderungs Header basierend auf dem Kanal Bindungs Token ändern möchten. Beachten Sie, dass Windows XP und Vista das Ändern von Anforderungs Headern während dieses Rückrufs nicht unterstützen.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SERVER_CERT_CHAIN_CONTEXT"></span><span id="winhttp_option_server_cert_chain_context"></span>**WinHTTP- \_ Option \_ Server Zertifikat- \_ \_ Ketten \_ Kontext**
</dt> <dd> <dl> <dt>



Ruft den Server Zertifizierungs Ketten Kontext ab. **WinHTTP \_ Die \_ Option \_ \_ \_** zum Abrufen eines doppelten Zeigers auf den Zertifikat **\_ Ketten \_ Kontext** für eine Serverzertifikat Kette, die während einer ausgehandelten SSL-Verbindung empfangen wurde, kann erfolgreich verwendet werden. Der Client muss [**certfreecertifitorecontext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) für den zurückgegebenen pccert- \_ Kontext Zeiger abrufen, der in den Puffer gefüllt wird.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SERVER_CERT_CONTEXT"></span><span id="winhttp_option_server_cert_context"></span>**WinHTTP- \_ Option \_ Server CERT- \_ \_ Kontext**
</dt> <dd> <dl> <dt>



Ruft den Server Zertifizierungs Kontext ab. **WinHTTP \_ Die Option \_ Server \_ CERT- \_ Kontext** kann zum Abrufen eines doppelten Zeigers auf den Zertifikat [**Kontext**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) eines Server Zertifikats, das während einer ausgehandelten SSL-Verbindung empfangen wurde, verwendet werden. Der Client muss [**certfreecertifitorecontext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) für den zurückgegebenen pccert- \_ Kontext Zeiger abrufen, der in den Puffer gefüllt wird.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SERVER_SPN_USED"></span><span id="winhttp_option_server_spn_used"></span>**WinHTTP- \_ options \_ Server- \_ SPN \_ verwendet**
</dt> <dd> <dl> <dt>



Ruft den Server Server Prinzipal Namen ab, den WinHTTP während der Authentifizierung an SSPI bereitgestellt hat. Dieser Zeichen folgen Wert kann nach einem Authentifizierungsfehler an [**sspipromptforanmelde**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) Informationen übermittelt werden.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SPN"></span><span id="winhttp_option_spn"></span>**WinHTTP- \_ options- \_ SPN**
</dt> <dd> <dl> <dt>



Schließt die Server Portnummer ein oder entfernt Sie, wenn der SPN (Dienst Prinzipal Name) für Kerberos erstellt wird oder die Kerberos-Authentifizierung aushandelt. Dieses Flag ist einer der folgenden Werte:

| Begriff | BESCHREIBUNG |
|-|-|
| <span id="WINHTTP_DISABLE_SPN_SERVER_PORT"></span><span id="winhttp_disable_spn_server_port"></span>WinHTTP-Port für den \_ \_ SPN- \_ Server deaktivieren \_ | Entfernt die Server Portnummer. |
| <span id="WINHTTP_ENABLE_SPN_SERVER_PORT"></span><span id="winhttp_enable_spn_server_port"></span>WinHTTP- \_ Port zum Aktivieren des \_ SPN- \_ Servers \_ | Schließt die Server Portnummer ein. |


</dl> </dd> <dt>

<span id="WINHTTP_OPTION_TCP_FAST_OPEN"></span><span id="winhttp_option_tcp_fast_open"></span>**WinHTTP- \_ Option \_ TCP \_ fast \_ Open**
</dt> <dd> <dl> <dt>



Aktiviert TCP fast Open für die Verbindung.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_TLS_FALSE_START"></span><span id="winhttp_option_tls_false_start"></span>**WinHTTP- \_ Option \_ TLS \_ false \_ Start**
</dt> <dd> <dl> <dt>



Aktiviert TLS false Start für die Verbindung.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_UNLOAD_NOTIFY_EVENT"></span><span id="winhttp_option_unload_notify_event"></span>**WinHTTP- \_ Option zum \_ Entladen von \_ Benachrichtigungs \_ Ereignissen**
</dt> <dd> <dl> <dt>



Nimmt ein Ereignis an, das festgelegt wird, wenn der letzte Rückruf für eine bestimmte Sitzung abgeschlossen wurde. Dieses Flag muss für ein Sitzungs Handle verwendet werden. Das Ereignis kann erst geschlossen werden, nachdem es von WinHTTP festgelegt wurde.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_UNSAFE_HEADER_PARSING"></span><span id="winhttp_option_unsafe_header_parsing"></span>**nicht unsichere WinHTTP- \_ Option- \_ \_ Header \_ -Verarbeitung**
</dt> <dd> <dl> <dt>



Diese Option ist für die interne Verwendung reserviert und sollte nicht aufgerufen werden.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_UPGRADE_TO_WEB_SOCKET"></span><span id="winhttp_option_upgrade_to_web_socket"></span>**WinHTTP- \_ Option \_ Upgrade \_ auf \_ Web \_ Socket**
</dt> <dd> <dl> <dt>



Weist den Stapel an, einen WebSocket-Handshake-Prozess mit [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)zu starten. Diese Option nimmt keine Parameter an.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_URL"></span><span id="winhttp_option_url"></span>**WinHTTP- \_ options- \_ URL**
</dt> <dd> <dl> <dt>



Ruft einen Zeichen folgen Wert ab, der die vollständige URL einer heruntergeladenen Ressource enthält. Wenn die ursprüngliche URL zusätzliche Daten enthielt, z. b. Such Zeichenfolgen oder Anker, oder wenn der-Rückruf umgeleitet wurde, unterscheidet sich die zurückgegebene URL vom ursprünglichen. Die Anwendung sollte einen Puffer mit einer Größe in Byte übergeben, der groß genug ist, um die zurückgegebene URL in wide char zu speichern.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_USE_GLOBAL_SERVER_CREDENTIALS"></span><span id="winhttp_option_use_global_server_credentials"></span>**WinHTTP- \_ Option \_ use \_ Global Server- \_ \_ Anmelde Informationen**
</dt> <dd> <dl> <dt>



Nimmt einen **booleschen** Wert auf und kann nur ein Sitzungs handle festgelegt werden. Sie wird nur nach dem Festlegen der-Option an Handles weitergegeben, die aus dem Sitzungs Handle erstellt wurden. Wenn **true**, bewirkt diese Option als letztes Mittel die Verwendung von Anmelde Informationen für den globalen Server, die von WinInet übermittelt wurden. Der Standardwert für diese Option ist **false**. Für diese Option ist der Registrierungsschlüssel " **HKLM \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Internet Settings" erforderlich. Sharecredswithwinhttp**. Dieser Registrierungsschlüssel ist standardmäßig nicht vorhanden. Wenn er festgelegt ist, sendet WinInet Anmelde Informationen an WinHTTP. Wenn WinHTTP eine Authentifizierungs Aufforderung erhält und keine Anmelde Informationen für das aktuelle handle festgelegt sind, werden die von WinInet bereitgestellten Anmelde Informationen verwendet.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_USER_AGENT"></span><span id="winhttp_option_user_agent"></span>**WinHTTP- \_ Option- \_ Benutzer- \_ Agent**
</dt> <dd> <dl> <dt>



Legt die [*Benutzer-Agent*](glossary.md) -Zeichenfolge für Handles fest, die von [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) bereitgestellt werden, und wird in nachfolgenden [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) -Funktionen verwendet, sofern Sie nicht durch einen von [**winhttpadrequestheaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) oder **WinHttpSendRequest** hinzugefügten Header überschrieben wird. Beim Abrufen eines Benutzer-Agents sollte die Anwendung einen Puffer mit einer Größe in Byte übergeben, der groß genug ist, um die zurückgegebene URL in wide char aufzunehmen. Beim Festlegen des Benutzer-Agents entspricht die Puffergröße der Länge der Zeichenfolge in Zeichen und dem **null** -Terminator.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_USERNAME"></span><span id="winhttp_option_username"></span>**WinHTTP- \_ Option \_ username**
</dt> <dd> <dl> <dt>



Legt eine Zeichenfolge fest, die den Benutzernamen enthält, oder ruft diese ab.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_WEB_SOCKET_CLOSE_TIMEOUT"></span><span id="winhttp_option_web_socket_close_timeout"></span>**WinHTTP- \_ Option " \_ Web \_ Socket \_ Close \_ Timeout"**
</dt> <dd> <dl> <dt>



Legt die Zeit (in Millisekunden) fest, die [**winhttpwebsocketclose**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketclose) warten soll, bis der schließen-Handshake abgeschlossen ist. Der Standardwert ist 10 Sekunden.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_WEB_SOCKET_KEEPALIVE_INTERVAL"></span><span id="winhttp_option_web_socket_keepalive_interval"></span>**WinHTTP \_ - \_ Option \_ WebSocket \_ KeepAlive- \_ Intervall**
</dt> <dd> <dl> <dt>



Legt das Intervall (in Millisekunden) fest, mit dem ein Keep-Alive-Paket über die Verbindung gesendet wird. Das Standardintervall beträgt 30000 (30 Sekunden). Das Mindestintervall beträgt 15000 (15 Sekunden). Wenn Sie " [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) " verwenden, um einen niedrigeren Wert als 15000 festzulegen, wird ein **\_ ungültiger \_ Parameter** zurückgegeben.

> [!Note]
> Der Standardwert für die **WinHTTP- \_ Option \_ Web \_ Socket \_ KeepAlive \_ Interval** wird von **HKLM: \\ Software \\ Microsoft \\ WebSocket \\ keepAliveInterval** gelesen. Wenn kein Wert festgelegt ist, wird der Standardwert 30000 verwendet. Es ist nicht möglich, ein niedrigeres KeepAlive-Intervall als 15000 Millisekunden zu haben.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_WEB_SOCKET_RECEIVE_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_receive_buffer_size"></span>**WinHTTP- \_ Option- \_ \_ WebSocket- \_ Empfangs \_ Puffer \_ Größe**
</dt> <dd> <dl> <dt>



Legt ein DWORD fest oder ruft es ab, das die Größe des Empfangspuffers angibt, die für WebSocket-Verbindungen verwendet werden soll.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_WEB_SOCKET_SEND_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_send_buffer_size"></span>**WinHTTP \_ - \_ Option \_ WebSocket- \_ Sende \_ Puffer \_ Größe**
</dt> <dd> <dl> <dt>



Legt ein DWORD fest oder ruft es ab, das die Größe des Sendepuffers angibt, die für WebSocket-Verbindungen verwendet werden soll.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_WORKER_THREAD_COUNT"></span><span id="winhttp_option_worker_thread_count"></span>**WinHTTP- \_ Option Arbeits \_ \_ Thread \_ Anzahl**
</dt> <dd> <dl> <dt>



Legt einen langen ganzzahligen Wert ohne Vorzeichen fest, der die Anzahl der Arbeitsthreads angibt, die der Thread Pool für asynchrone Vervollständigungen verwenden soll. Der Standardwert dieser Option ist 0 (null), wodurch angegeben wird, dass die Anzahl der Arbeitsthreads gleich der Anzahl der CPUs im System ist. Diese Option kann nur für ein NULL- [hinternethandle](hinternet-handles-in-winhttp.md) festgelegt werden, bevor ein asynchroner Vorgang aufgetreten ist.   Diese Option kann nur einmal festgelegt werden.

**Windows Server 2008 R2 und Windows 7:** Dieses Flag ist veraltet.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_WRITE_BUFFER_SIZE"></span><span id="winhttp_option_write_buffer_size"></span>**Größe des \_ \_ Schreib \_ Puffers der WinHTTP-Option \_**
</dt> <dd> <dl> <dt>



Diese Option ist veraltet. Dies hat keine Auswirkungen.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

In der folgenden Tabelle werden die Optionsflags aufgelistet, indem angegeben wird, auf welche Handles Sie reagieren können, ob Sie abgefragt und festgelegt werden können und welcher Datentyp verwendet werden kann. Ein "X" gibt an, dass das Optionsflag für die Verwendung mit der Funktion oder dem Handle gültig ist, während ein "-" angibt, dass das Optionsflag ungültig ist.

Der Versuch, ein Optionsflag in einer Windows-Version festzulegen oder abzufragen, wo es nicht unterstützt wird, führt zu einer **\_ ungültigen WinHTTP- \_ \_ Option**.

| Optionsflag und Datentyp | Sitzungs handle | Anforderungs handle | Abfrageoption | SET-Option | Windows-Mindestversion |
|-|-|-|-|-|-|
| WinHTTP- \_ Option \_ garantierte \_ nicht \_ blockierende \_ Rückrufe<br/>**BOOL** | X | \- | \- | X | \- |
| \_ \_ \_ Richtlinie für die automatische WinHTTP-Option<br/>**DWORD** | \- | X | \- | X | \- |
| WinHTTP- \_ options \_ Rückruf<br/>**LPVOID** | X | X | X | X | \- |
| WinHTTP- \_ Option \_ Client \_ Zertifikat \_ Kontext<br/>[**CERT- \_ Kontext**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) | \- | X | \- | X | Windows Vista |
| WinHTTP- \_ Option \_ Client Zertifikat- \_ \_ Aussteller \_ Liste<br/>[**Secpkgcontext \_ issuerlistinfoex**](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) | \- | X | X | \- | Windows Vista |
| WinHTTP- \_ options \_ Codepage<br/>**DWORD** | X | \- | \- | X | \- |
| WinHTTP- \_ Option \_ Konfigurieren der \_ Passport \_ -Authentifizierung<br/>**DWORD** | X | \- | \- | X | \- |
| WinHTTP- \_ Option \_ Connect- \_ Wiederholungs Versuche<br/>**DWORD** | X | X | X | X | \- |
| WinHTTP- \_ Option \_ Connect- \_ Timeout<br/>**DWORD** | X | X | X | X | \- |
| \_ \_ Verbindungs \_ Informationen zur WinHTTP-Option<br/>[**WinHTTP- \_ Verbindungs \_ Informationen**](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info) | \- | X | X | \- | \- |
| WinHTTP- \_ options \_ Verbindungs \_ Statistik \_ v0<br/>[**TCP- \_ Informationen \_ v0**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0) | \- | X | X | \- | Windows 10, Version 1903 |
| WinHTTP- \_ options \_ Verbindungs \_ Statistik \_ v1<br/>[**TCP- \_ Informationen \_ v1**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1) | \- | X | X | \- | Windows 10, Version 2004 |
| WinHTTP- \_ options \_ Kontext \_ Wert<br/>**DWORD \_ ptr** | X | X | X | X | \- |
| WinHTTP- \_ options \_ Dekomprimierung<br/>**DWORD** | X | X | \- | X | Windows 8.1 |
| Funktion zum Deaktivieren der WinHTTP- \_ Option \_ \_<br/>**DWORD** | \- | X | \- | X | \- |
| WinHTTP- \_ Option " \_ \_ Secure \_ Protocol \_ Fallback deaktivieren"<br/>**BOOL** | X | \- | \- | X | Windows 10, Version 1903 |
| WinHTTP- \_ Option ' \_ Stream- \_ \_ Warteschlange deaktivieren<br/>**BOOL** | X | X | \- | X | Windows 10, Version 1809 |
| Feature "WinHTTP- \_ Option \_ aktivieren" \_<br/>**DWORD** | \* | \* | \- | X | \- |
| WinHTTP- \_ Option \_ http- \_ \_ Protokoll aktivieren<br/>**DWORD** | X | X | \- | X | Windows 10, Version 1607 |
| WinHTTP- \_ Option \_ EnableTracing<br/>**DWORD** | \- | \- | X | X | \- |
| WinHTTP- \_ Option " \_ \_ zusätzliche Codierung"<br/>**BOOL** | X | X | \- | X | Windows 10, Version 1803 |
| Erweiterte WinHTTP- \_ Option- \_ \_ Fehler<br/>**DWORD** | X | X | X | \- | \- |
| WinHTTP- \_ Option \_ globale Proxy-Anmelde- \_ \_ Befehle<br/>[**WinHTTP- \_ Befehle**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds) | X | X | \- | X | \- |
| WinHTTP- \_ Option " \_ globale \_ Server \_ -Erstellungs Dienste"<br/>[**WinHTTP-Anmelde-" \_ \_ Ex"**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) | X | X | \- | X | \- |
| WinHTTP- \_ Option \_ handle- \_ Typ<br/>**DWORD** | X | X | X | \- | \- |
| WinHTTP- \_ Option \_ http- \_ Protokoll \_ erforderlich<br/>**BOOL** | X | X | \- | X | Windows 10, Version 1903 |
| WinHTTP- \_ Option \_ http- \_ Protokoll \_ verwendet<br/>**DWORD** | \- | X | X | \- | Windows 10, Version 1607 |
| WinHTTP- \_ Option \_ http- \_ Version<br/>[**HTTP- \_ Versions \_ Informationen**](/windows/win32/api/winhttp/ns-winhttp-http_version_info) | X | X | X | X | \- |
| WinHTTP- \_ Option \_ Zertifikat Sperrung \_ \_ \_ Offline ignorieren<br/>**BOOL** | \- | X | \- | X | Windows 10, Version 2004 |
| WinHTTP- \_ Option \_ IPv6- \_ schnelles \_ Fallback<br/>**BOOL** | X | \- | \- | X | Windows 10, Version 1903 |
| die WinHTTP- \_ Option \_ ist eine \_ Proxy \_ Verbindungs \_ Antwort.<br/>**BOOL** | X | X | X | \- | \- |
| WinHTTP-Option max. Anzahl von Verbindungs- \_ \_ \_ \_ und \_ 1 \_ 0- \_ Servern<br/>**DWORD** | X | \- | X | X | \- |
| WinHTTP-Option max. Anzahl von Verbindungs \_ \_ \_ \_ \_ Servern pro Server<br/>**DWORD** | X | \- | X | X | \- |
| WinHTTP- \_ Option \_ Max. \_ \_ Automatische HTTP \_ -Umleitungen<br/>**DWORD** | X | X | X | X | \- |
| WinHTTP- \_ Option \_ Max HTTP-Status wird \_ \_ \_ fortgesetzt<br/>**DWORD** | X | X | X | X | \- |
| WinHTTP- \_ Option \_ Max. Antwort Ausgleichs \_ \_ \_ Größe<br/>**DWORD** | X | X | X | X | \- |
| WinHTTP- \_ Option \_ Max- \_ Antwort \_ Header \_ Größe<br/>**DWORD** | X | X | X | X | \- |
| über \_ \_ geordnetes \_ Handle der WinHTTP-Option<br/>[HINTERNET](hinternet-handles-in-winhttp.md) | X | X | X | \- | \- |
| WinHTTP- \_ Option \_ Passport- \_ cobrandingtext \_<br/>**LPWSTR** | \- | X | X | \- | \- |
| WinHTTP- \_ Option \_ Passport- \_ cobrandingurl \_<br/>**LPWSTR** | \- | X | X | \- | \- |
| Rückgabe-URL der WinHTTP- \_ Option \_ Passport \_ \_<br/>**LPVOID** | \- | X | X | \- | \- |
| WinHTTP- \_ Option \_ Passport- \_ \_ Abmeldung<br/>**LPVOID** | X | \- | \- | X | \- |
| WinHTTP- \_ options \_ Kennwort<br/>**LPWSTR** | \- | X | X | X | \- |
| WinHTTP- \_ options \_ Proxy<br/>[**WinHTTP- \_ Proxy \_ Informationen**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) | X | X | X | X | \- |
| WinHTTP- \_ Option \_ Proxy \_ Kennwort<br/>**LPWSTR** | \- | X | X | X | \- |
| WinHTTP- \_ options \_ Proxy- \_ SPN \_ verwendet<br/>**LPWSTR** | \- | X | X | \- | \- |
| WinHTTP- \_ Option \_ Proxy \_ Benutzername<br/>**LPWSTR** | \- | X | X | X | \- |
| WinHTTP- \_ Option, \_ Lese \_ Puffer \_ Größe<br/>**DWORD** | \- | X | X | X | \- |
| WinHTTP- \_ Option \_ empfangen von \_ Proxy \_ Verbindungs \_ Antworten<br/>**BOOL** | X | X | \- | X | \- |
| WinHTTP- \_ Option- \_ Empfangs \_ Antwort \_ Timeout<br/>**DWORD** | X | X | X | X | \- |
| \_ \_ Empfangs \_ Timeout für WinHTTP-Option<br/>**DWORD** | X | X | X | X | \- |
| WinHTTP- \_ Option \_ Umleitungs \_ Richtlinie<br/>**DWORD** | X | X | X | X | \- |
| WinHTTP \_ - \_ Option \_ userpwd \_ in \_ URL ablehnen<br/>**BOOL** | \- | X | \- | X | \- |
| WinHTTP- \_ Option- \_ Anforderungs \_ Priorität<br/>**DWORD** | \- | X | X | X | \- |
| \_ \_ Anforderungs \_ Statistik für WinHTTP-Optionen<br/>[**WinHTTP- \_ Anforderungs \_ Statistik**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats) | \- | X | X | \- | Windows 10, Version 1903 |
| \_ \_ Anforderungs \_ Zeiten für WinHTTP-Optionen<br/>[**WinHTTP- \_ Anforderungs \_ Zeiten**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times) | \- | X | X | \- | Windows 10, Version 1903 |
| WinHTTP- \_ Option ' \_ \_ Timeout auflösen '<br/>**DWORD** | X | X | X | X | \- |
| \_ \_ sichere \_ Protokolle der WinHTTP-Option<br/>**DWORD** | X | \- | \- | X | \- |
| Struktur der WinHTTP- \_ Option- \_ Sicherheits \_ Zertifikat \_<br/>[**Informationen zum WinHTTP- \_ Zertifikat \_**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) | \- | X | X | \- | \- |
| WinHTTP- \_ Option ( \_ \_ sicherheitsflags)<br/>**DWORD** | \- | X | X | X | \- |
| \_ \_ Sicherheits \_ Informationen für die WinHTTP-Option<br/>[**WINHTTP_SECURITY_INFO**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_security_info) | \- | X | X | \- | Windows 10, Version 2004 |
| WinHTTP- \_ Option- \_ Sicherheits \_ Schlüssel \_ Bitness<br/>**DWORD** | \- | X | X | \- | \- |
| WinHTTP- \_ Option \_ Send \_ Timeout<br/>**DWORD** | X | X | X | X | \- |
| WinHTTP- \_ options \_ Server \_ CBT<br/>[**Secpkgcontext- \_ Bindungen**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings)\* | \- | X | X | \- | \- |
| WinHTTP- \_ Option \_ Server Zertifikat- \_ \_ Ketten \_ Kontext<br/>[**CERT_CHAIN_CONTEXT**](/windows/win32/api/wincrypt/ns-wincrypt-cert_chain_context) | \- | X | X | \- | Windows 10, Version 2004 |
| WinHTTP- \_ Option \_ Server CERT- \_ \_ Kontext<br/>[**CERT-Kontext**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) | \- | X | X | \- | \- |
| WinHTTP- \_ options \_ Server- \_ SPN \_ verwendet<br/>**LPWSTR** | \- | X | X | \- | \- |
| WinHTTP- \_ options- \_ SPN<br/>**DWORD** | \- | X | \- | X | \- |
| WinHTTP- \_ Option \_ TCP \_ fast \_ Open<br/>**BOOL** | X | \- | \- | X | Windows 10, Version 2004 |
| WinHTTP- \_ Option \_ TLS \_ false \_ Start<br/>**BOOL** | X | \- | \- | X | Windows 10, Version 2004 |
| WinHTTP- \_ Option zum \_ Entladen von \_ Benachrichtigungs \_ Ereignissen<br/>[HINTERNET](hinternet-handles-in-winhttp.md) | X | \- | \- | X | \- |
| nicht unsichere WinHTTP- \_ Option- \_ \_ Header \_ -Verarbeitung<br/>**DWORD** | \- | X | \- | X | \- |
| WinHTTP- \_ Option \_ Upgrade \_ auf \_ Web \_ Socket<br/>– | \- | X | \- | X | \- |
| WinHTTP- \_ options- \_ URL<br/>**LPWSTR** | \- | X | X | \- | \- |
| WinHTTP- \_ Option \_ use \_ Global Server- \_ \_ Anmelde Informationen<br/>**BOOL** | X | X | \- | X | \- |
| WinHTTP- \_ Option- \_ Benutzer- \_ Agent<br/>**LPWSTR** | X | \- | X | X | \- |
| WinHTTP- \_ Option \_ username<br/>**LPWSTR** | \- | X | X | X | \- |
| WinHTTP- \_ Option " \_ Web \_ Socket \_ Close \_ Timeout"<br/>**DWORD** | \- | \- | X | X | \- |
| WinHTTP \_ - \_ Option \_ WebSocket \_ KeepAlive- \_ Intervall<br/>**DWORD** | \- | \- | X | X | \- |
| WinHTTP- \_ Option- \_ \_ WebSocket- \_ Empfangs \_ Puffer \_ Größe<br/>**DWORD** | X | X | X | X | Windows 8.1 |
| WinHTTP \_ - \_ Option \_ WebSocket- \_ Sende \_ Puffer \_ Größe<br/>**DWORD** | X | X | X | X | Windows 8.1 |
| WinHTTP- \_ Option Arbeits \_ \_ Thread \_ Anzahl<br/>**DWORD** | \- | \- | \- | X | \- |
| Größe des \_ \_ Schreib \_ Puffers der WinHTTP-Option \_<br/>**DWORD** | \- | X | X | X | \- |

> [!Note]
> Informationen zu Windows XP und Windows 2000 finden Sie unter [Lauf Zeitanforderungen](winhttp-start-page.md).

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|--------------------------|---------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client) | Windows XP, Windows 2000 Professional mit SP3 \[ Desktop-Apps\]            |
| Unterstützte Mindestversion (Server) | Windows Server 2003, Windows 2000-Server mit \[ nur SP3-Desktop-Apps\]         |
| Verteilbare Komponente          | WinHTTP 5,0 und Internet Explorer 5,01 oder höher unter Windows XP und Windows 2000. |
| Header                   | WinHTTP. h                                                                       |

## <a name="see-also"></a>Siehe auch

[WinHTTP-Versionen](winhttp-versions.md)
