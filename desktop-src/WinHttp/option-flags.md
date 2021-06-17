---
Description: Die folgenden Optionsflags werden von WinHttpQueryOption und WinHttpSetOption unterstützt.
ms.assetid: 2d0441f4-ddba-4f2a-8861-8803cad6f1ac
title: Optionsflags (Winhttp.h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 02/25/2020
ms.openlocfilehash: 91a9506225c53893990d4dcdc534293daa6c8e00
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262062"
---
# <a name="option-flags"></a>Optionsflags

Die folgenden Optionsflags werden von [**WinHttpQueryOption und**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) [**WinHttpSetOption unterstützt.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)

<dl> <dt>

<span id="WINHTTP_OPTION_ASSURED_NON_BLOCKING_CALLBACKS"></span><span id="winhttp_option_assured_non_blocking_callbacks"></span>**\_WINHTTP-OPTION \_ \_ GARANTIERTE NICHT \_ \_ BLOCKIERENDE RÜCKRUFE**
</dt> <dd> <dl> <dt>



Der Standardwert lautet FALSE. Wenn der Status auf TRUE festgelegt ist, garantiert WinHTTP den Fortschritt nicht, wenn Statusrückrufe von der Clientanwendung blockiert werden.

Die Clientanwendung muss besonders darauf achten, minimale Vorgänge innerhalb des Rückrufs ohne Blockierung durchzuführen, so schnell wie möglich zurückzukehren und insbesondere nicht auf nachfolgende WinHTTP-Aufrufe zu warten. Wenn sie diese Richtlinien nicht einfängt, ist es wahrscheinlich, dass es negative Auswirkungen auf die Leistung oder eine potenzielle Anwendung gibt, die nicht mehr funktioniert. Wenn diese Option auf die vorgeschriebene Weise verwendet wird, kann sie die Leistung verbessern.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_AUTOLOGON_POLICY"></span><span id="winhttp_option_autologon_policy"></span>**RICHTLINIE FÜR \_ DIE AUTOMATISCHE ANMELDUNG DER WINHTTP-OPTION \_ \_**
</dt> <dd> <dl> <dt>



Legt einen ganzzahligen Wert ohne Vorzeichen fest, der die Richtlinie für automatische [Anmeldung](authentication-in-winhttp.md) mit einem der folgenden Werte angibt.

| Begriff | Beschreibung |
|-|-|
| <span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_HIGH"></span><span id="winhttp_autologon_security_level_high"></span>WINHTTP \_ AUTOLOGON \_ SECURITY \_ LEVEL \_ HIGH | Standardanmeldeinformationen werden nicht verwendet. Beachten Sie, dass dieses Flag nur wirksam wird, wenn Sie den Server mit dem tatsächlichen Computernamen angeben. Sie wird nicht wirksam, wenn Sie den Server mit "localhost" oder IP-Adresse angeben. |
| <span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_LOW"></span><span id="winhttp_autologon_security_level_low"></span>WINHTTP \_ AUTOLOGON \_ SECURITY \_ LEVEL \_ LOW | Für alle Anforderungen wird eine authentifizierte Anmeldung mit den Standardanmeldeinformationen durchgeführt. |
| <span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_MEDIUM"></span><span id="winhttp_autologon_security_level_medium"></span>WINHTTP \_ AUTOLOGON \_ SECURITY \_ LEVEL \_ MEDIUM | Eine authentifizierte Anmeldung mit den Standardanmeldeinformationen wird nur für Anforderungen im lokalen Intranet ausgeführt. |


</dl> </dd> <dt>

<span id="WINHTTP_OPTION_CALLBACK"></span><span id="winhttp_option_callback"></span>**\_ \_ WINHTTP-OPTIONSRÜCKRUF**
</dt> <dd> <dl> <dt>



Ruft den Zeiger auf den Rückruffunktionssatz mit [**WinHttpSetStatusCallback ab.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback)


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CLIENT_CERT_CONTEXT"></span><span id="winhttp_option_client_cert_context"></span>**WINHTTP \_ OPTION \_ CLIENT \_ CERT \_ CONTEXT**
</dt> <dd> <dl> <dt>



Legt den Clientzertifikatkontext fest. Wenn eine Anwendung [**DEN FEHLER \_ WINHTTP CLIENT \_ \_ AUTH \_ CERT \_ NEEDED**](error-messages.md)empfängt, muss sie [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) aufrufen, um ein Zertifikat zur Verfügung zu stellen, bevor die Anforderung erneut ausgeführt wird. Im Rahmen der Verarbeitung dieser Option ruft WinHttp [**CertDuplicateCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecertificatecontext) im vom Aufrufer bereitgestellten Zertifikatkontext auf, damit der Zertifikatkontext unabhängig vom Aufrufer freigegeben werden kann.

> [!Note]
> Die Anwendung sollte nicht versuchen, den Zertifikatspeicher mit dem Flag CERT CLOSE STORE FORCE FLAG im Aufruf von \_ \_ \_ \_ [**CertCloseStore**](/windows/desktop/api/wincrypt/nf-wincrypt-certclosestore) in dem Zertifikatspeicher zu schließen, aus dem der Zertifikatkontext abgerufen wurde. Es kann zu einer Zugriffsverletzung kommen.

Wenn der Server ein Clientzertifikat anfordert, [**gibt WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)oder [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) einen [**ERROR \_ WINHTTP CLIENT \_ \_ AUTH \_ CERT \_ NEEDED-Fehler**](error-messages.md) zurück. Wenn der Server das Zertifikat an fordert, es aber nicht erfordert, kann die Anwendung diese Option angeben, um anzugeben, dass er kein Zertifikat hat. Der Server kann ein anderes Authentifizierungsschema auswählen oder anonymen Zugriff auf den Server zulassen. Die Anwendung stellt das **WINHTTP \_ NO CLIENT \_ \_ CERT \_ CONTEXT-Makro** im *lpBuffer-Parameter* von [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) wie im folgenden Codebeispiel gezeigt zur Anwendung.

``` syntax
BOOL fRet = WinHttpSetOption(hRequest,
                             WINHTTP_OPTION_CLIENT_CERT_CONTEXT,
                             WINHTTP_NO_CLIENT_CERT_CONTEXT,
                             0);
```

Wenn der Server ein Clientzertifikat erfordert, kann er als Antwort den HTTP-Statuscode 403 senden. Weitere Informationen finden Sie unter DER **OPTION WINHTTP \_ OPTION CLIENT \_ \_ CERT ISSUER \_ \_ LIST.**


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CLIENT_CERT_ISSUER_LIST"></span><span id="winhttp_option_client_cert_issuer_list"></span>**\_WINHTTP-OPTION \_ \_ CLIENTZERTIFIKATAUSSTELLERLISTE \_ \_**
</dt> <dd> <dl> <dt>



Ruft eine [**SecPkgContext \_ IssuerListInfoEx-Struktur**](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) ab, wenn der Fehler aus [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) oder [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) **ERROR \_ WINHTTP CLIENT \_ \_ AUTH \_ CERT NEEDED \_ lautet.** Die Ausstellerliste in der Struktur enthält eine Liste der zulässigen Zertifizierungsstellen (Certificate Authorities, CA) vom Server. Die Clientanwendung kann die Zertifizierungsstellenliste filtern, um das Clientzertifikat für die SSL-Authentifizierung abzurufen.

Alternativ kann die Anwendung [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) mit der OPTION **WINHTTP \_ OPTION CLIENT \_ \_ CERT \_ CONTEXT** aufrufen, wenn der Server das Clientzertifikat an fordert, es aber nicht erfordert. Weitere Informationen finden Sie unter DER **OPTION WINHTTP \_ OPTION CLIENT \_ \_ CERT \_ CONTEXT.**


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CODEPAGE"></span><span id="winhttp_option_codepage"></span>**\_ \_ WINHTTP-OPTIONSCODEPAGE**
</dt> <dd> <dl> <dt>



Legt die [*Codepage fest,*](glossary.md) die zum Verarbeiten der URL verwendet wird (d. h. Abfragezeichenfolge). Der Standardwert ist UTF8.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CONFIGURE_PASSPORT_AUTH"></span><span id="winhttp_option_configure_passport_auth"></span>**\_WINHTTP-OPTION: \_ \_ KONFIGURIEREN DER \_ PASSPORT-AUTHENTIFIZIERUNG**
</dt> <dd> <dl> <dt>



Legt einen ganzzahligen Wert ohne Vorzeichen fest, der angibt, ob [die Passport-Authentifizierung in der WinHTTP-Authentifizierung](passport-authentication-in-winhttp.md) aktiviert ist. Der Wert kann in folgenden Formen vorliegen:

| Begriff | Beschreibung |
|-|-|
| <span id="WINHTTP_DISABLE_PASSPORT_AUTH"></span><span id="winhttp_disable_passport_auth"></span>WINHTTP \_ DEAKTIVIEREN \_ DER \_ PASSPORT-AUTHENTIFIZIERUNG | Microsoft Passport Authentifizierung ist deaktiviert. Dies ist die Standardoption. |
| <span id="WINHTTP_DISABLE_PASSPORT_KEYRING"></span><span id="winhttp_disable_passport_keyring"></span>WINHTTP \_ DEAKTIVIEREN VON PASSPORT \_ \_ KEYRING | Der Passport-Schlüsselring ist deaktiviert. Dies ist die Standardoption. |
| <span id="WINHTTP_ENABLE_PASSPORT_AUTH"></span><span id="winhttp_enable_passport_auth"></span>WINHTTP \_ ENABLE \_ PASSPORT \_ AUTH | Die Passport-Authentifizierung ist aktiviert. |
| <span id="WINHTTP_ENABLE_PASSPORT_KEYRING"></span><span id="winhttp_enable_passport_keyring"></span>WINHTTP \_ ENABLE \_ PASSPORT \_ KEYRING | Der Passport-Schlüsselring ist aktiviert. |

</dl> </dd> <dt>

<span id="WINHTTP_OPTION_CONNECT_RETRIES"></span><span id="winhttp_option_connect_retries"></span>**\_WINHTTP-OPTION \_ – \_ VERBINDUNGS-RETRIES**
</dt> <dd> <dl> <dt>



Legt einen ganzzahligen Wert ohne Vorzeichen fest, der die Anzahl der Versuche vonWinHTTP enthält, eine Verbindung mit einem Host herzustellen, oder ruft diesen wert ab. Microsoft Windows HTTP Services (WinHTTP) versucht nur einmal pro IP-Adresse (InternetProtokoll). Wenn Sie beispielsweise versuchen, eine Verbindung mit einem mehrfach vernetzten Host herzustellen, der über 10 IP-Adressen verfügt und **WINHTTP \_ OPTION CONNECT \_ \_ RETRIES** auf 7 festgelegt ist, versucht WinHTTP nur, eine Verbindung mit den ersten sieben IP-Adressen herzustellen. Wenn **WINHTTP \_ OPTION CONNECT \_ \_ RETRIES** auf 20 festgelegt ist, versucht WinHTTP bei 10 IP-Adressen nur einmal, jede der zehn IP-Adressen zu verwenden. Wenn ein Verbindungsversuch nach der angegebenen Anzahl von Versuchen weiterhin fehlschlägt oder das Verbindungszeitout vor diesem Zeitpunkt abgelaufen ist, wird die Anforderung abgebrochen. Der Standardwert für **WINHTTP \_ OPTION CONNECT \_ \_ RETRIES** ist fünf Versuche.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CONNECT_TIMEOUT"></span><span id="winhttp_option_connect_timeout"></span>**WINHTTP \_ OPTION \_ CONNECT \_ TIMEOUT**
</dt> <dd> <dl> <dt>



Legt einen ganzzahligen Wert ohne Vorzeichen, der den Time out-Wert enthält, in Millisekunden fest oder ruft diesen ab. Wenn Sie diese Option auf unendlich (0xFFFFFFFF) festlegen, wird dieser Timer deaktiviert.

Wenn eine TCP-Verbindungsanforderung länger als dieser Time out-Wert dauert, wird die Anforderung abgebrochen. Das Standard-Timeout beträgt 60 Sekunden. Wenn Sie versuchen, eine Verbindung mit mehreren IP-Adressen für einen einzelnen Host (einen mehrfach vernetzten Host) herzustellen, gilt das Timeoutlimit für jede einzelne Verbindung.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CONNECTION_INFO"></span><span id="winhttp_option_connection_info"></span>**VERBINDUNGSINFORMATIONEN \_ ZUR WINHTTP-OPTION \_ \_**
</dt> <dd> <dl> <dt>



Ruft die Quell- und Ziel-IP-Adresse und den Port der Anforderung ab, die die Antwort generiert hat, wenn [**WinHttpReceiveResponse zurückgegeben**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) wird. Die Anwendung ruft [**WinHttpQueryOption mit**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) der **OPTION WINHTTP OPTION CONNECTION \_ \_ \_ INFO** auf und stellt die [**WINHTTP CONNECTION \_ \_ INFO-Struktur**](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info) im *lpBuffer-Parameter* zur Auswahl. Weitere Informationen finden Sie unter **WINHTTP \_ CONNECTION \_ INFO**.

**Windows Server 2003 mit SP1 und Windows XP mit SP2:** Dieses Flag ist veraltet.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CONNECTION_STATS_V0"></span><span id="winhttp_option_connection_stats_v0"></span>**WINHTTP \_ OPTION \_ CONNECTION \_ STATS \_ V0**
</dt> <dd> <dl> <dt>



Retreives die [**TCP \_ INFO \_ v0-Struktur**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0) für die zugrunde liegende Verbindung, die von der Anforderung verwendet wird. Die zurückgegebene Struktur kann Statistiken aus vorherigen Anforderungen enthalten, die über dieselbe Verbindung gesendet wurden.

> [!Note]
> Diese Option wurde durch **WINHTTP \_ OPTION \_ CONNECTION \_ STATS \_ V1 ersetzt.**


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CONNECTION_STATS_V1"></span><span id="winhttp_option_connection_stats_v1"></span>**WINHTTP \_ OPTION \_ CONNECTION \_ STATS \_ V1**
</dt> <dd> <dl> <dt>



Retreives die [**TCP \_ INFO \_ v1-Struktur**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1) für die zugrunde liegende Verbindung, die von der Anforderung verwendet wird. Die zurückgegebene Struktur kann Statistiken aus vorherigen Anforderungen enthalten, die über dieselbe Verbindung gesendet wurden.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CONTEXT_VALUE"></span><span id="winhttp_option_context_value"></span>**KONTEXTWERT \_ DER WINHTTP-OPTION \_ \_**
</dt> <dd> <dl> <dt>



Legt eine **\_ DWORD-PTR fest** oder ruft sie ab, die einen Zeiger auf den Kontextwert enthält, der diesem [HINTERNET-Handle zugeordnet](hinternet-handles-in-winhttp.md) ist. Der im Puffer gespeicherte Wert wird verwendet, und dem **Optionsflag WINHTTP \_ OPTION CONTEXT \_ \_ VALUE** wird ein neuer Wert zugewiesen.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_DECOMPRESSION"></span><span id="winhttp_option_decompression"></span>**DEKOMPRIMIERUNG \_ DER WINHTTP-OPTION \_**
</dt> <dd> <dl> <dt>



Legt ein DWORD von Flags fest, die bestimmen, ob WinHTTP Antwortkörper automatisch mit komprimierten Inhaltscodierungen dekomprimiert. WinHTTP wird auch einen geeigneten Accept-Encoding festlegen und alle vom Aufrufer bereitgestellten überschreiben. Diese Werte werden unterstützt:

| Begriff | Beschreibung |
|-|-|
| <span id="WINHTTP_DECOMPRESSION_FLAG_GZIP"></span><span id="winhttp_decompression_flag_gzip"></span>\_WINHTTP-DEKOMPRIMIERUNGSFLAG \_ \_ GZIP | Dekomprimieren der Inhaltscodierung: gzip-Antworten. |
| <span id="WINHTTP_DECOMPRESSION_FLAG_DEFLATE"></span><span id="winhttp_decompression_flag_deflate"></span>DEFLATE DES \_ WINHTTP-DEKOMPRIMIERUNGSFLAGS \_ \_ | Dekomprimieren der Inhaltscodierung: Verfeinern von Antworten. |
| <span id="WINHTTP_DECOMPRESSION_FLAG_ALL"></span><span id="winhttp_decompression_flag_all"></span>\_WINHTTP-DEKOMPRIMIERUNGSFLAG \_ \_ ALL | Dekomprimieren Sie Antworten mit allen unterstützten Inhaltscodierungen. |

Standardmäßig liefert WinHTTP komprimierte Antworten unverändert an den Aufrufer.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_DISABLE_FEATURE"></span><span id="winhttp_option_disable_feature"></span>**FUNKTION \_ "WINHTTP-OPTION \_ \_ DEAKTIVIEREN"**
</dt> <dd> <dl> <dt>



Legt einen ganzzahligen Wert ohne Vorzeichen fest, der angibt, welche Features mit mindestens einem der folgenden Flags deaktiviert werden. Beachten Sie, dass dieses Feature nur bei Anforderungshandles an [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) übergeben werden sollte, nachdem das Anforderungshandles mit [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)erstellt wurde und bevor die Anforderung mit [**WinHttpSendRequest gesendet wird.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)

| Begriff | Beschreibung |
|-|-|
| <span id="WINHTTP_DISABLE_AUTHENTICATION"></span><span id="winhttp_disable_authentication"></span>WINHTTP \_ DISABLE \_ AUTHENTICATION | Die automatische Authentifizierung ist deaktiviert. |
| <span id="WINHTTP_DISABLE_COOKIES"></span><span id="winhttp_disable_cookies"></span>WINHTTP \_ DEAKTIVIEREN VON \_ COOKIES | Das automatische Hinzufügen von Cookieheadern zu Anforderungen ist deaktiviert. Außerdem werden zurückgegebene Cookies nicht automatisch zur Cookiedatenbank hinzugefügt. Das Deaktivieren von Cookies kann zu einer schlechten Leistung bei der Passport-Authentifizierung führen. |
| <span id="WINHTTP_DISABLE_KEEP_ALIVE"></span><span id="winhttp_disable_keep_alive"></span>WINHTTP \_ DISABLE \_ KEEP \_ ALIVE | Deaktiviert die Keep-Alive-Semantik für die Verbindung. Keep-Alive-Semantik ist für MSN, NTLM und andere Authentifizierungstypen erforderlich. |
| <span id="WINHTTP_DISABLE_REDIRECTS"></span><span id="winhttp_disable_redirects"></span>\_WINHTTP: DEAKTIVIEREN \_ VON UMLEITUNGEN | Die automatische Umleitung ist deaktiviert, wenn Anforderungen mit [**WinHttpSendRequest gesendet werden.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) Wenn die automatische Umleitung deaktiviert ist, muss eine Anwendung eine Rückruffunktion registrieren, damit die Passport-Authentifizierung erfolgreich ist. |


</dl> </dd> <dt>

<span id="WINHTTP_OPTION_DISABLE_SECURE_PROTOCOL_FALLBACK"></span><span id="winhttp_option_disable_secure_protocol_fallback"></span>**\_WINHTTP-OPTION: \_ DEAKTIVIEREN DES \_ \_ \_ FALLBACKS DES SICHEREN PROTOKOLLS**
</dt> <dd> <dl> <dt>



Verhindert, dass WinHTTP eine Verbindung mit einer niedrigeren Version des Sicherheitsprotokolls erneut versucht, wenn die erste Protokollaushandlung fehlschlägt.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_DISABLE_STREAM_QUEUE"></span><span id="winhttp_option_disable_stream_queue"></span>**WINHTTP-OPTION \_ \_ \_ STREAMWARTESCHLANGE \_ DEAKTIVIEREN**
</dt> <dd> <dl> <dt>



Ermöglicht es neuen Anforderungen, eine zusätzliche HTTP/2-Verbindung zu öffnen, wenn die maximale Anzahl gleichzeitiger Streams erreicht ist, anstatt auf den nächsten verfügbaren Stream für eine vorhandene Verbindung zu warten.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_ENABLE_FEATURE"></span><span id="winhttp_option_enable_feature"></span>**FEATURE \_ "WINHTTP-OPTION \_ \_ AKTIVIEREN"**
</dt> <dd> <dl> <dt>



Legt einen ganzzahligen Wert ohne Vorzeichen fest, der die derzeit aktivierten Funktionen angibt. Kann einer der folgenden Werte sein.

| Begriff | Beschreibung |
|-|-|
| <span id="WINHTTP_ENABLE_SSL_REVERT_IMPERSONATION"></span><span id="winhttp_enable_ssl_revert_impersonation"></span>WINHTTP \_ ENABLE \_ SSL \_ REVERT \_ IMPERSONATION | Wenn diese Option aktiviert ist, wird der Clientwechsel für die Dauer von SSL-Zertifikatauthentifizierungsvorgängen vorübergehend von WinHTTP rückgängig machen. Dieser Wert kann nur für das Sitzungshand handle festgelegt werden. |
| <span id="WINHTTP_ENABLE_SSL_REVOCATION"></span><span id="winhttp_enable_ssl_revocation"></span>WINHTTP \_ AKTIVIEREN DER \_ \_ SSL-SPERRUNG | Wenn diese Option aktiviert ist, lässt WinHTTP die SSL-Sperrung zu. Dieser Wert kann nur für das Anforderungshand handle festgelegt werden. |


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_ENABLE_HTTP_PROTOCOL"></span><span id="winhttp_option_enable_http_protocol"></span>**WINHTTP-OPTION \_ \_ \_ HTTP-PROTOKOLL \_ AKTIVIEREN**
</dt> <dd> <dl> <dt>



Legt eine DWORD-Bitmaske zulässiger erweiterter HTTP-Versionen fest. Mögliche Werte:

| Begriff | Beschreibung |
|-|-|
| <span id="WINHTTP_PROTOCOL_FLAG_HTTP2"></span><span id="winhttp_protocol_flag_http2"></span>\_ \_ WINHTTP-PROTOKOLLFLAG \_ HTTP2 (0x1) | Aktiviert HTTP/2 für die Anforderung. |
| Keine (0x0) | Schränkt die Anforderung auf HTTP/1.1 und früher ein. |

Ältere Versionen von HTTP (1.1 und früher) können mit dieser Option nicht deaktiviert werden. Der Standardwert ist 0x0.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_ENABLE_HTTP2_PLUS_CLIENT_CERT"></span><span id="winhttp_option_enable_http2_plus_client_cert"></span>**\_WINHTTP-OPTION \_ \_ HTTP2 \_ PLUS CLIENT \_ \_ CERT AKTIVIEREN**
</dt> <dd> <dl> <dt>


Diese Option kann für ein WinHttp-Sitzungshand handle festgelegt werden, damit WinHttp den vom Aufrufer bereitgestellten Clientzertifikatkontext verwenden kann, wenn HTTP/2 verwendet wird.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_ENABLETRACING"></span><span id="winhttp_option_enabletracing"></span>**\_WINHTTP-OPTION \_ ENABLETRACING**
</dt> <dd> <dl> <dt>



Legt einen **BOOL-Wert** fest, der angibt, ob die Ablaufverfolgung derzeit aktiviert ist. Weitere Informationen zur Ablaufverfolgungseinrichtung in WinHTTP finden Sie unter [WinHTTP Trace Facility](winhttptracecfg-exe--a-trace-configuration-tool.md). Diese Option kann nur für ein **NULL** **HINTERNET-Handle festgelegt** werden.


</dt> </dl> </dd>

<dt>

<span id="WINHTTP_OPTION_ENCODE_EXTRA"></span><span id="winhttp_option_encode_extra"></span>**WINHTTP \_ OPTION \_ ENCODE \_ EXTRA**
</dt> <dd> <dl> <dt>



Aktiviert die URL-Prozentcodierung für Pfad und Abfragezeichenfolge.

Alternativ können Sie vor dem Aufrufen von WinHttp prozentweise codieren.

</dt> </dl> </dd>

<dt>

<span id="WINHTTP_OPTION_EXPIRE_CONNECTION"></span><span id="winhttp_option_expire_connection"></span>**WINHTTP-OPTION \_ \_ VERBINDUNG \_ ABLAUFEN**
</dt> <dd> <dl> <dt>



Diese Option kann nur für ein Anforderungshand handle festgelegt werden, das noch aktiv ist (senden oder empfangen). Wenn Sie diese Option festlegen, wird WinHttp dazu veranschlagen, die Verarbeiten von Anforderungen für die Verbindung zu beenden, die dem übergebenen Anforderungshand handle zugeordnet ist. Die Verbindung wird geschlossen, nachdem das Anforderungshand handle, mit dem diese Option aufgerufen wird, abgeschlossen ist. Bei dieser Option werden keine Parameter verwendet.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_EXTENDED_ERROR"></span><span id="winhttp_option_extended_error"></span>**ERWEITERTER \_ FEHLER DER WINHTTP-OPTION \_ \_**
</dt> <dd> <dl> <dt>



Ruft einen ganzzahligen Wert ohne Vorzeichen ab, der einen Microsoft Windows Sockets-Fehlercode enthält, der den ZULETZT in diesem Threadkontext zurückgegebenen \_ ERROR WINHTTP-Fehlermeldungen \_ \* zugeordnet wurde. Sie können **NULL als** Handlewert übergeben.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_GLOBAL_PROXY_CREDS"></span><span id="winhttp_option_global_proxy_creds"></span>**GLOBALE \_ PROXY-ANMELDEINFORMATIONEN FÜR DIE \_ \_ \_ WINHTTP-OPTION**
</dt> <dd> <dl> <dt>



Verwendet einen Zeiger auf eine [**WINHTTP \_ CREDS \_ EX-Struktur,**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) bei der der *hInternet-Funktionsparameter* auf **NULL festgelegt ist.** Diese Option erfordert den Registrierungsschlüssel **HKLM \\ Software Microsoft \\ Windows \\ \\ CurrentVersion Internet \\ Settings! ShareCredsWithWinHttp**. Wenn dieser Registrierungsschlüssel nicht festgelegt ist, gibt WinHTTP den Fehler **\_ ERROR WINHTTP INVALID OPTION \_ \_ zurück.** Dieser Registrierungsschlüssel ist standardmäßig nicht vorhanden. Wenn sie festgelegt ist, sendet WinINet Anmeldeinformationen an WinHTTP. Wenn WinHttp eine Authentifizierungsforderung erhält und keine Anmeldeinformationen für das aktuelle Handle festgelegt sind, werden die von WinINet bereitgestellten Anmeldeinformationen verwendet. Um Serveranmeldeinformationen zusätzlich zu Proxyanmeldeinformationen gemeinsam zu verwenden, müssen Benutzer **WINHTTP \_ OPTION USE GLOBAL SERVER CREDENTIALS \_ \_ \_ (GLOBALE SERVERANMELDEINFORMATIONEN \_ VERWENDEN) festlegen.**


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_GLOBAL_SERVER_CREDS"></span><span id="winhttp_option_global_server_creds"></span>**\_WINHTTP-OPTION \_ : GLOBALE \_ \_ SERVER-ANMELDEINFORMATIONEN**
</dt> <dd> <dl> <dt>



Verwendet einen Zeiger auf eine [**WINHTTP \_ CREDS \_ EX-Struktur,**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) bei der der *hInternet-Funktionsparameter* auf **NULL festgelegt ist.** Diese Option erfordert den Registrierungsschlüssel **HKLM \\ Software Microsoft \\ Windows \\ \\ CurrentVersion Internet \\ Settings! ShareCredsWithWinHttp**. Wenn dieser Registrierungsschlüssel nicht festgelegt ist, gibt WinHTTP den Fehler **\_ ERROR WINHTTP INVALID OPTION \_ \_ zurück.** Dieser Registrierungsschlüssel ist standardmäßig nicht vorhanden. Wenn sie festgelegt ist, sendet WinINet Anmeldeinformationen an WinHTTP. Wenn WinHttp eine Authentifizierungsforderung erhält und keine Anmeldeinformationen für das aktuelle Handle festgelegt sind, werden die von WinINet bereitgestellten Anmeldeinformationen verwendet. Um Serveranmeldeinformationen zusätzlich zu Proxyanmeldeinformationen gemeinsam zu verwenden, müssen Benutzer **WINHTTP \_ OPTION USE GLOBAL SERVER CREDENTIALS \_ \_ \_ (GLOBALE SERVERANMELDEINFORMATIONEN \_ VERWENDEN) festlegen.**


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_HANDLE_TYPE"></span><span id="winhttp_option_handle_type"></span>**HANDLETYP \_ DER WINHTTP-OPTION \_ \_**
</dt> <dd> <dl> <dt>



Ruft einen ganzzahligen Wert ohne Vorzeichen ab, der den Typ des übergebenen [HINTERNET-Handles](hinternet-handles-in-winhttp.md) enthält. Einer der folgenden Werte kann zurückgegeben werden:

| Begriff | Beschreibung |
|-|-|
| <span id="WINHTTP_HANDLE_TYPE_CONNECT"></span><span id="winhttp_handle_type_connect"></span>WINHTTP \_ HANDLE \_ TYPE \_ CONNECT | Das Handle ist ein Verbindungshand handle. |
| <span id="WINHTTP_HANDLE_TYPE_REQUEST"></span><span id="winhttp_handle_type_request"></span>\_ \_ WINHTTP-HANDLETYPANFORDERUNG \_ | Das Handle ist ein Anforderungshand handle. |
| <span id="WINHTTP_HANDLE_TYPE_SESSION"></span><span id="winhttp_handle_type_session"></span>SITZUNG MIT \_ \_ WINHTTP-HANDLETYP \_ | Das Handle ist ein Sitzungshand handle. |


</dl> </dd> <dt>

<span id="WINHTTP_OPTION_HTTP_PROTOCOL_REQUIRED"></span><span id="winhttp_option_http_protocol_required"></span>**\_WINHTTP-OPTION \_ \_ HTTP-PROTOKOLL \_ ERFORDERLICH**
</dt> <dd> <dl> <dt>



Verhindert, dass andere Protokollversionen als die von **WINHTTP \_ OPTION ENABLE HTTP \_ \_ \_ PROTOCOL** aktivierten für die Anforderung verwendet werden.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_HTTP_PROTOCOL_USED"></span><span id="winhttp_option_http_protocol_used"></span>**VERWENDETES \_ \_ HTTP-PROTOKOLL DER \_ WINHTTP-OPTION \_**
</dt> <dd> <dl> <dt>



Ruft ein DWORD ab, das angibt, welche erweiterte HTTP-Version für eine bestimmte Anforderung verwendet wurde. Eine Liste der möglichen Werte finden Sie unter **WINHTTP \_ OPTION ENABLE HTTP \_ \_ \_ PROTOCOL**.



</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_HTTP_VERSION"></span><span id="winhttp_option_http_version"></span>**\_HTTP-VERSION DER WINHTTP-OPTION \_ \_**
</dt> <dd> <dl> <dt>



Legt eine HTTP-VERSIONSinformationsstruktur fest, die die unterstützte HTTP-Version enthält, oder ruft sie ab. [**\_ \_**](/windows/win32/api/winhttp/ns-winhttp-http_version_info) Dies ist eine prozessweite Option. Verwenden **Sie NULL** für das Handle.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_HTTP2_KEEPALIVE"></span><span id="winhttp_option_http2_keepalive"></span>**\_WINHTTP-OPTION \_ HTTP2 \_ KEEPALIVE**
</dt> <dd> <dl> <dt>


Diese Option kann für ein Sitzungshand handle so festgelegt werden, dass WinHttp HTTP/2-PING-Frames als Keepalive-Mechanismus verwendet. Aufrufer geben ein Timeout in Millisekunden an, und wenn für diesen Timeoutzeitraum keine Aktivität für eine Verbindung besteht, beginnt WinHttp mit dem Senden von HTTP/2-PING-Frames. Aufrufer können keinen Timeoutwert von weniger als 5.000 Millisekunden festlegen.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_HTTP2_PLUS_TRANSFER_ENCODING"></span><span id="winhttp_option_http2_plus_transfer_encoding"></span>**WINHTTP-OPTION \_ \_ HTTP2 \_ PLUS \_ \_ ÜBERTRAGUNGSCODIERUNG**
</dt> <dd> <dl> <dt>


Diese Option kann für ein WinHttp-Anforderungshand handle festgelegt werden, um das Verhalten von WinHttp zu steuern, wenn eine HTTP/2-Antwort einen "Transfer-Encoding"-Header enthält. In diesem Fall gibt WinHttp einen Fehler zurück, wenn diese Option auf **FALSE festgelegt ist.**


</dt> </dl> </dd> <dt>


<span id="WINHTTP_OPTION_IGNORE_CERT_REVOCATION_OFFLINE"></span><span id="winhttp_option_ignore_cert_revocation_offline"></span>**WINHTTP-OPTION \_ \_ \_ ZERTIFIKATSPERRUNG \_ \_ OFFLINE IGNORIEREN**
</dt> <dd> <dl> <dt>



Ermöglicht sicheren Verbindungen die Verwendung von Sicherheitszertifikaten, für die die Zertifikatsperrliste nicht heruntergeladen werden konnte.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_IPV6_FAST_FALLBACK"></span><span id="winhttp_option_ipv6_fast_fallback"></span>**WINHTTP-OPTION \_ \_ IPV6 \_ – SCHNELLER \_ FALLBACK**
</dt> <dd> <dl> <dt>



Aktiviert schnelles IPv6-Fallback (Brillenbrillen) für die Verbindung. Dieses Verhalten ähnelt dem In RFC [6555](https://tools.ietf.org/html/rfc6555) beschriebenen Verhalten von Happy Eyeballs zur Verbesserung der Verbindungszeiten in Netzwerken, in denen IPv6 unzuverlässig ist.
- Wenn sowohl IPv6- als auch IPv4-Adressen für einen bestimmten Host aufgelöst werden, beginnt WinHttp mit dem Herstellen einer Verbindung mit der ersten aufgelösten IPv6-Adresse mit einem kurzen Timeout (300 ms).
- Sollte diese Verbindung fehlschlagen, versucht WinHttp, eine Verbindung mit der ersten aufgelösten IPv4-Adresse mit dem Standard-Timeout herzustellen.
- Sollte bei der zweiten Verbindung ein Fehler auftäussen, wird von WinHttp die erste aufgelöste IPv6-Adresse mit dem Standard-Timeout erneut verwendet.
- Sollte die dritte Verbindung fehlschlagen, wird WinHttp auf das Standardverhalten für alle verbleibenden Adressen zurückverwendet und versucht, eine Verbindung mit jeder Adresse mit dem Standard-Timeout herzustellen, bis eine Verbindung hergestellt wird oder keine Adressen mehr bestehen.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_IS_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_is_proxy_connect_response"></span>**\_WINHTTP-OPTION \_ IST PROXY \_ \_ \_ CONNECT-ANTWORT**
</dt> <dd> <dl> <dt>



Ruft ab, ob eine Proxy Return Connect-Antwort abgerufen werden kann.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_MAX_CONNS_PER_1_0_SERVER"></span><span id="winhttp_option_max_conns_per_1_0_server"></span>**\_WINHTTP-OPTION \_ \_ MAX. CONNS \_ PRO \_ 1 \_ 0 \_ SERVER**
</dt> <dd> <dl> <dt>



Legt einen ganzzahligen Wert ohne Vorzeichen fest, der die maximale Anzahl von Verbindungen enthält, die pro HTTP/1.0-Server zulässig sind, oder ruft diesen wert ab. Der Standardwert ist **INFINITE.**

**Windows Vista mit SP1 und Windows Server 2008:** Dieses Flag ist veraltet.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_MAX_CONNS_PER_SERVER"></span><span id="winhttp_option_max_conns_per_server"></span>**\_WINHTTP-OPTION \_ \_ MAX. CONNS \_ PRO \_ SERVER**
</dt> <dd> <dl> <dt>



Legt einen ganzzahligen Wert ohne Vorzeichen fest, der die maximal zulässige Anzahl von Verbindungen pro Server enthält, oder ruft diesen wert ab. Der Standardwert ist **INFINITE.**

Wenn diese Option auf 0 (null) festgelegt ist, legt WinHTTP den Grenzwert für die Anzahl von Verbindungen auf 2 fest.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_MAX_HTTP_AUTOMATIC_REDIRECTS"></span><span id="winhttp_option_max_http_automatic_redirects"></span>**WINHTTP-OPTION \_ \_ \_ MAX. AUTOMATISCHE \_ \_ HTTP-UMLEITUNGEN**
</dt> <dd> <dl> <dt>



Legt die maximale Anzahl von Umleitungen fest, auf die WinHTTP folgt. Der Standardwert ist 10. Dieser Grenzwert verhindert, dass nicht autorisierte Websites den WinHTTP-Client nach einer großen Anzahl von Umleitungen anhalten.

**Windows XP mit SP1 und Windows 2000 mit SP3:** Dieses Flag ist veraltet.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_MAX_HTTP_STATUS_CONTINUE"></span><span id="winhttp_option_max_http_status_continue"></span>**\_WINHTTP-OPTION \_ \_ MAX. \_ HTTP-STATUS \_ CONTINUE**
</dt> <dd> <dl> <dt>



Die maximale Anzahl von 100-199 Statuscodeantworten, die ignoriert wurden, bevor der endgültige Statuscode an den WinHTTP-Client zurücksendet. Informationsstatuscodes vom Status 100-199 können vom Server vor dem endgültigen Statuscode gesendet werden und werden in der Spezifikation für HTTP/1.1 beschrieben (weitere Informationen finden Sie unter [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt)). Der Standardwert ist 10.

**Windows XP mit SP1 und Windows 2000 mit SP3:** Dieses Flag ist veraltet.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_MAX_RESPONSE_DRAIN_SIZE"></span><span id="winhttp_option_max_response_drain_size"></span>**WINHTTP \_ OPTION \_ MAX \_ RESPONSE \_ DRAIN \_ SIZE**
</dt> <dd> <dl> <dt>



Eine Grenze für die Menge der Daten, die aus Antworten entleert werden, um eine Verbindung wiederzuverwenden, die in Bytes angegeben ist. Der Standardwert ist 1 MB.

**Windows XP mit SP1 und Windows 2000 mit SP3:** Dieses Flag ist veraltet.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_MAX_RESPONSE_HEADER_SIZE"></span><span id="winhttp_option_max_response_header_size"></span>**MAXIMALE GRÖßE DES \_ \_ \_ \_ ANTWORTHEADERS DER \_ WINHTTP-OPTION**
</dt> <dd> <dl> <dt>



Ein gebundener Satz für die maximale Größe des Headerbereichs der Serverantwort, angegeben in Bytes. Diese Gebundene schützt den Client vor einem nicht autorisierten Server, der versucht, den Client zu verhindern, indem eine Antwort mit einer unendlichen Menge von Headerdaten gesendet wird. Der Standardwert ist 64 KB.

**Windows XP mit SP1 und Windows 2000 mit SP3:** Dieses Flag ist veraltet.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PARENT_HANDLE"></span><span id="winhttp_option_parent_handle"></span>**ÜBERGEORDNETES \_ HANDLE DER WINHTTP-OPTION \_ \_**
</dt> <dd> <dl> <dt>



Ruft das übergeordnete Handle für dieses Handle ab.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PASSPORT_COBRANDING_TEXT"></span><span id="winhttp_option_passport_cobranding_text"></span>**\_WINHTTP-OPTION \_ \_ PASSPORT-COBRANDINGTEXT \_**
</dt> <dd> <dl> <dt>



Ruft eine Zeichenfolge ab, die den [*cobranding-Text*](glossary.md) enthält, der vom Passport-Anmeldeserver bereitgestellt wird. Diese Option sollte sofort abgerufen werden, nachdem der Anmeldeserver mit dem Statuscode 401 reagiert hat. Eine Anwendung sollte eine Puffergröße in Bytes übergeben, die groß genug ist, um die zurückgegebene Zeichenfolge zu enthalten.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PASSPORT_COBRANDING_URL"></span><span id="winhttp_option_passport_cobranding_url"></span>**\_WINHTTP-OPTION \_ \_ PASSPORT-COBRANDING-URL \_**
</dt> <dd> <dl> <dt>



Ruft eine Zeichenfolge ab, die eine URL für eine [*Cobrandinggrafik*](glossary.md) enthält, die vom Passport-Anmeldeserver bereitgestellt wird. Diese Option sollte sofort abgerufen werden, nachdem der Anmeldeserver mit dem Statuscode 401 reagiert hat. Eine Anwendung sollte eine Puffergröße in Bytes übergeben, die groß genug ist, um die zurückgegebene Zeichenfolge zu enthalten.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PASSPORT_RETURN_URL"></span><span id="winhttp_option_passport_return_url"></span>**\_WINHTTP-OPTION \_ \_ \_ PASSPORT-RÜCKGABE-URL**
</dt> <dd> <dl> <dt>



Legt eine schreibgeschützte Option für ein Anforderungshandles fest, das die Passport-Rückgabe-URL abruft.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PASSPORT_SIGN_OUT"></span><span id="winhttp_option_passport_sign_out"></span>**\_WINHTTP-OPTION \_ \_ \_ PASSPORT-ABMELDE**
</dt> <dd> <dl> <dt>



Legt die Option für ein Sitzungshand handle zum Abmelden von Passport-Anmeldungen fest. Eine Anwendung sollte die Passport-Rückgabe-URL übergeben, die mit **WINHTTP \_ OPTION PASSPORT RETURN URL abgerufen \_ \_ \_ wurde.** Alle Cookies im Zusammenhang mit der Rückgabe-URL werden wieder löschen.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PASSWORD"></span><span id="winhttp_option_password"></span>**\_ \_ WINHTTP-OPTIONSKENNWORT**
</dt> <dd> <dl> <dt>



Legt einen Zeichenfolgenwert fest, der das einem Anforderungshand handle zugeordnete Kennwort enthält, oder ruft diesen ab.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PROXY"></span><span id="winhttp_option_proxy"></span>**\_WINHTTP-OPTIONSPROXY \_**
</dt> <dd> <dl> <dt>



Legt eine [**WINHTTP PROXY \_ \_ INFO-Struktur**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) fest, die die Proxydaten auf einem vorhandenen Sitzungshand handle oder Anforderungshand handle enthält, oder ruft sie ab. Beim Abrufen von Proxydaten muss eine Anwendung die in dieser Struktur enthaltenen **lpszProxy-** und **lpszProxyBypass-Zeichenfolgen** (wenn sie nicht NULL **sind)** mithilfe der [**GlobalFree-Funktion**](/windows/desktop/api/winbase/nf-winbase-globalfree) frei geben. Eine Anwendung kann die globalen Proxydaten (den Standardproxy) abfragen, indem sie ein **NULL-Handle** übergibt.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PROXY_PASSWORD"></span><span id="winhttp_option_proxy_password"></span>**\_PROXYKENNWORT \_ FÜR WINHTTP-OPTION \_**
</dt> <dd> <dl> <dt>



Legt einen Zeichenfolgenwert fest, der das Kennwort für den Zugriff auf den Proxy enthält, oder ruft diesen ab.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PROXY_SPN_USED"></span><span id="winhttp_option_proxy_spn_used"></span>**VERWENDETER \_ \_ WINHTTP-OPTIONSPROXY-SPN \_ \_**
</dt> <dd> <dl> <dt>



Ruft den Proxyserverprinzipalnamen ab, den WinHTTP während der Authentifizierung an SSPI übermittelt hat. Dieser Zeichenfolgenwert wird verwendet, um nach einem [**Authentifizierungsfehler an SspiPromptForCredentials**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) zu übergeben.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PROXY_USERNAME"></span><span id="winhttp_option_proxy_username"></span>**\_PROXYBENUTZERNAME DER WINHTTP-OPTION \_ \_**
</dt> <dd> <dl> <dt>



Legt einen Zeichenfolgenwert fest, der den Benutzernamen enthält, der für den Zugriff auf den Proxy verwendet wird, oder ruft diesen ab.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_READ_BUFFER_SIZE"></span><span id="winhttp_option_read_buffer_size"></span>**\_WINHTTP-OPTION \_ READ BUFFER \_ \_ SIZE**
</dt> <dd> <dl> <dt>



Diese Option ist veraltet. es hat keine Auswirkungen.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_RECEIVE_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_receive_proxy_connect_response"></span>**WINHTTP-OPTION \_ \_ "PROXY \_ \_ CONNECT-ANTWORT \_ EMPFANGEN"**
</dt> <dd> <dl> <dt>



Legt fest, ob die Proxyantwortentität abgerufen werden kann. Diese Option ist standardmäßig deaktiviert.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_RECEIVE_RESPONSE_TIMEOUT"></span><span id="winhttp_option_receive_response_timeout"></span>**WINHTTP-OPTION \_ \_ \_ \_ EMPFANGSANTWORT-TIMEOUT**
</dt> <dd> <dl> <dt>



Legt einen ganzzahligen Wert ohne Vorzeichen fest, der den Timeoutwert in Millisekunden enthält, um auf den Empfang aller Antwortheader für eine Anforderung zu warten, oder ruft diesen wert ab. Wenn WinHTTP nicht alle Header innerhalb dieses Timeoutzeitraums empfangen kann, wird die Anforderung abgebrochen. Der Standardwert für das Timeout beträgt 90 Sekunden.

Dieses Timeout wird nur überprüft, wenn Daten vom Socket empfangen werden. Wenn das Timeout abläuft, wird die Clientanwendung daher erst benachrichtigt, wenn weitere Daten vom Server eintreffen. Wenn keine Daten vom Server eintreffen, kann die Verzögerung zwischen dem Ablauf des Timeouts und der Benachrichtigung der Clientanwendung so groß sein wie der Timeoutwert, der mit dem *dwReceiveTimeout-Parameter* der [**WinHttpSetTimeouts-Funktion**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts) festgelegt wurde.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_RECEIVE_TIMEOUT"></span><span id="winhttp_option_receive_timeout"></span>**\_EMPFANGSZEITÜBERSCHREITUNG DER WINHTTP-OPTION \_ \_**
</dt> <dd> <dl> <dt>



Legt einen ganzzahligen Wert ohne Vorzeichen fest, der den Time out-Wert in Millisekunden enthält, um eine Teilantwort auf eine Anforderung zu empfangen oder einige Daten zu lesen, oder ruft diesen wert ab. Wenn die Antwort länger als dieser Time out-Wert dauert, wird die Anforderung abgebrochen. Der Standard-Timeoutwert beträgt 30 Sekunden.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_REDIRECT_POLICY"></span><span id="winhttp_option_redirect_policy"></span>**UMLEITUNGSRICHTLINIE \_ FÜR WINHTTP-OPTION \_ \_**
</dt> <dd> <dl> <dt>



Legt das Verhalten von WinHTTP in Bezug auf die Behandlung eines 30-fachen HTTP-Umleitungsstatuscodes fest. Diese Option kann für ein Sitzungs- oder Anforderungshand handle auf einen der folgenden Werte festgelegt werden:

| Begriff | Beschreibung |
|-|-|
| <span id="WINHTTP_OPTION_REDIRECT_POLICY_ALWAYS"></span><span id="winhttp_option_redirect_policy_always"></span>RICHTLINIE FÜR DIE UMLEITUNG \_ DER WINHTTP-OPTION \_ \_ \_ IMMER | Alle Umleitungen werden automatisch befolgt. |
| <span id="WINHTTP_OPTION_REDIRECT_POLICY_DISALLOW_HTTPS_TO_HTTP"></span><span id="winhttp_option_redirect_policy_disallow_https_to_http"></span>UMLEITUNGSRICHTLINIE \_ FÜR \_ WINHTTP-OPTION: \_ HTTPS ZU HTTP NICHT \_ \_ \_ \_ ZU | Alle Umleitungen werden befolgt, mit Ausnahme der Umleitungen, die von einer sicheren URL (https) zu einer unsicheren URL (HTTP) stammen. Dies ist die Standardeinstellung. |
| <span id="WINHTTP_OPTION_REDIRECT_POLICY_NEVER"></span><span id="winhttp_option_redirect_policy_never"></span>UMLEITUNGSRICHTLINIE \_ FÜR WINHTTP-OPTION \_ \_ \_ NIE | Umleitungen werden nie befolgt. Der 30-fache Status wird an die Anwendung zurückgegeben. |


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_REJECT_USERPWD_IN_URL"></span><span id="winhttp_option_reject_userpwd_in_url"></span>**\_WINHTTP-OPTION \_ BENUTZER IN URL \_ \_ \_ ABLEHNENPWD**
</dt> <dd> <dl> <dt>



Lehnt URLs ab, die einen Benutzernamen und ein Kennwort enthalten. Diese Option lehnt auch URLs ab, die *die Semantik username:password* enthalten, auch wenn kein Benutzername oder Kennwort angegeben ist. Beispielsweise würde " u:p@hostname ", " :@hostname ", " u:@hostname ", " " und " :p@hostname " alle als ungültig gekennzeichnet werden. Wenn eine ungültige URL an die Funktion übergeben wird, wird [ERROR \_ WINHTTP \_ INVALID URL \_ zurückgegeben.](error-messages.md) Standardmäßig ist diese Option deaktiviert.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_REQUEST_PRIORITY"></span><span id="winhttp_option_request_priority"></span>**\_WINHTTP-OPTION \_ – \_ ANFORDERUNGSPRIORITÄT**
</dt> <dd> <dl> <dt>



Diese Option ist veraltet. es hat keine Auswirkungen.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_REQUEST_STATS"></span><span id="winhttp_option_request_stats"></span>**\_ \_ WINHTTP-OPTIONSANFORDERUNGSSTATISTIKEN \_**
</dt> <dd> <dl> <dt>



Retreives-Statistiken für die Anforderung.  Eine Liste der verfügbaren Statistiken finden Sie unter [**WINHTTP \_ REQUEST \_ STATS**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats).


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_REQUEST_TIMES"></span><span id="winhttp_option_request_times"></span>**ANFORDERUNGSZEITEN \_ DER WINHTTP-OPTION \_ \_**
</dt> <dd> <dl> <dt>



Sucht nach Zeitsteuerungsinformationen für die Anforderung. Eine Liste der verfügbaren Zeitsteuerungen finden Sie unter [**WINHTTP \_ REQUEST \_ TIMES**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times).


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_REQUIRE_STREAM_END"></span><span id="winhttp_option_require_stream_end"></span>**\_WINHTTP-OPTION \_ " \_ STREAMENDE \_ ERFORDERLICH"**
</dt> <dd> <dl> <dt>


Diese Option weist WinHttp an, "Content-Length"-Antwortheader zu ignorieren und weiterhin in einem Stream zu empfangen, bis das END_STREAM empfangen wird.



</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_RESOLUTION_HOSTNAME"></span><span id="winhttp_option_resolution_hostname"></span>**HOSTNAME \_ DER WINHTTP-OPTIONSAUFLÖSUNG \_ \_**
</dt> <dd> <dl> <dt>


Diese Option kann für ein WinHttp-Anforderungshand handle festgelegt werden, bevor es gesendet wurde. Wenn festgelegt, verwendet WinHttp die vom Aufrufer bereitgestellte Zeichenfolge als Hostnamen für die DNS-Auflösung.



</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_RESOLVE_TIMEOUT"></span><span id="winhttp_option_resolve_timeout"></span>**WINHTTP-OPTION \_ \_ \_ TIMEOUT AUFLÖSEN**
</dt> <dd> <dl> <dt>



Legt einen ganzzahligen Wert ohne Vorzeichen fest, der den Time out-Wert in Millisekunden enthält, um einen Hostnamen aufzulösen, oder ruft diesen wert ab. Der Standardwert für das Timeout ist **INFINITE.** Wenn ein nicht standardmäßiger Wert angegeben wird, verursacht dies einen Mehraufwand von einer Threaderstellung pro Namensauflösung.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SECURE_PROTOCOLS"></span><span id="winhttp_option_secure_protocols"></span>**SICHERE PROTOKOLLE \_ DER WINHTTP-OPTION \_ \_**
</dt> <dd> <dl> <dt>



Legt einen ganzzahligen Wert ohne Vorzeichen fest, der angibt, welche sicheren Protokolle zulässig sind. Standardmäßig sind nur SSL3 und TLS1 in Windows 7 und Windows 8. Standardmäßig sind nur SSL3, TLS1.0, TLS1.1 und TLS1.2 in Windows 8.1 und Windows 10. Der Wert kann eine Kombination aus mindestens einem der folgenden Werte sein.

| Begriff | Beschreibung |
|-|-|
| <span id="WINHTTP_FLAG_SECURE_PROTOCOL_ALL"></span><span id="winhttp_flag_secure_protocol_all"></span>WINHTTP \_ FLAG \_ SECURE \_ PROTOCOL \_ ALL | Die protokolle Secure Sockets Layer (SSL) 2.0, SSL 3.0 und Transport Layer Security (TLS) 1.0 können verwendet werden. |
| <span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL2"></span><span id="winhttp_flag_secure_protocol_ssl2"></span>WINHTTP-FLAG \_ \_ SECURE PROTOCOL \_ \_ SSL2 | Das SSL 2.0-Protokoll kann verwendet werden. |
| <span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL3"></span><span id="winhttp_flag_secure_protocol_ssl3"></span>WINHTTP-FLAG \_ \_ SECURE PROTOCOL \_ \_ SSL3 | Das SSL 3.0-Protokoll kann verwendet werden. |
| <span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1"></span><span id="winhttp_flag_secure_protocol_tls1"></span>WINHTTP-FLAG \_ \_ SECURE PROTOCOL \_ \_ TLS1 | Das TLS 1.0-Protokoll kann verwendet werden. |
| <span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_1"></span><span id="winhttp_flag_secure_protocol_tls1_1"></span>WINHTTP-FLAG \_ \_ SECURE PROTOCOL \_ \_ TLS1 \_ 1 | Das TLS 1.1-Protokoll kann verwendet werden. |
| <span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_2"></span><span id="winhttp_flag_secure_protocol_tls1_2"></span>WINHTTP-FLAG \_ \_ SECURE PROTOCOL \_ \_ TLS1 \_ 2 | Das TLS 1.2-Protokoll kann verwendet werden. |


</dl> </dd> <dt>

<span id="WINHTTP_OPTION_SECURITY_CERTIFICATE_STRUCT"></span><span id="winhttp_option_security_certificate_struct"></span>**\_SICHERHEITSZERTIFIKATSTRUKTUR DER WINHTTP-OPTION \_ \_ \_**
</dt> <dd> <dl> <dt>



Ruft das Zertifikat für einen SSL/TLS-Server in der [**WINHTTP \_ CERTIFICATE \_ INFO-Struktur**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) ab. Die Anwendung muss die **Member lpszSubjectInfo** und **lpszIssuerInfo mit** [**LocalFree frei geben.**](/windows/desktop/api/winbase/nf-winbase-localfree)


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SECURITY_FLAGS"></span><span id="winhttp_option_security_flags"></span>**\_SICHERHEITSFLAGS FÜR DIE WINHTTP-OPTION \_ \_**
</dt> <dd> <dl> <dt>



Legt einen ganzzahligen Wert ohne Vorzeichen fest, der die Sicherheitsflags für ein Handle enthält, oder ruft diesen wert ab. Dabei kann es sich um eine Kombination dieser Werte handelt:

| Begriff | Beschreibung |
|-|-|
| <span id="SECURITY_FLAG_IGNORE_CERT_CN_INVALID"></span><span id="security_flag_ignore_cert_cn_invalid"></span>\_ \_ SICHERHEITSFLAG \_ \_ ZERTIFIKAT-CN IGNORIEREN \_ UNGÜLTIG |Lässt einen ungültigen allgemeinen Namen in einem Zertifikat zu. Das heißt, der von der Anwendung angegebene Servername ist nicht mit dem allgemeinen Namen im Zertifikat übereinstimmen. Wenn dieses Flag festgelegt ist, erhält die Anwendung keinen **WINHTTP \_ CALLBACK \_ STATUS FLAG \_ \_ CERT \_ CN \_ INVALID-Rückruf.** |
| <span id="SECURITY_FLAG_IGNORE_CERT_DATE_INVALID"></span><span id="security_flag_ignore_cert_date_invalid"></span>SECURITY \_ FLAG \_ IGNORE \_ CERT \_ DATE \_ INVALID |Lässt ein ungültiges Zertifikatdatum zu, d. b. ein abgelaufenes oder noch nicht effektives Zertifikat. Wenn dieses Flag festgelegt ist, erhält die Anwendung keinen **WINHTTP \_ CALLBACK \_ STATUS FLAG \_ \_ CERT DATE \_ \_ INVALID-Rückruf.** |
| <span id="SECURITY_FLAG_IGNORE_UNKNOWN_CA"></span><span id="security_flag_ignore_unknown_ca"></span>\_ \_ SICHERHEITSFLAG UNBEKANNTE \_ ZERTIFIZIERUNGSSTELLE \_ IGNORIEREN | Lässt eine ungültige Zertifizierungsstelle zu. Wenn dieses Flag festgelegt ist, erhält die Anwendung keinen **WINHTTP \_ CALLBACK \_ STATUS FLAG INVALID \_ \_ \_ CA-Rückruf.** |
| <span id="SECURITY_FLAG_IGNORE_CERT_WRONG_USAGE"></span><span id="security_flag_ignore_cert_wrong_usage"></span>\_SICHERHEITSFLAG : FALSCHE VERWENDUNG DES \_ \_ \_ ZERTIFIKATS \_ IGNORIEREN | Ermöglicht das Herstellen der Identität eines Servers mit einem Nicht-Serverzertifikat (z. B. einem Clientzertifikat). |
| <span id="SECURITY_FLAG_IGNORE_WEAK_SIGNATURE"></span><span id="security_flag_ignore_weak_signature"></span>\_ \_ SICHERHEITSFLAG SCHWACHE SIGNATUR \_ \_ IGNORIEREN | Ermöglicht das Ignorieren einer schwachen Signatur.<br/>Dieses Flag ist im Rollupupdate für jedes Betriebssystem ab Windows 7 und Windows Server 2008 R2 verfügbar. |
| <span id="SECURITY_FLAG_SECURE"></span><span id="security_flag_secure"></span>\_SICHERHEITSFLAG \_ SICHER | Verwendet sichere Übertragungen. Dies wird nur in einem Aufruf von [**WinHttpQueryOption zurückgegeben.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) |
| <span id="SECURITY_FLAG_STRENGTH_MEDIUM"></span><span id="security_flag_strength_medium"></span>\_ \_ SICHERHEITSFLAGSTÄRKE \_ MITTEL | Verwendet eine mittlere (56-Bit)-Verschlüsselung. Dies wird nur in einem Aufruf von [**WinHttpQueryOption zurückgegeben.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) |
| <span id="SECURITY_FLAG_STRENGTH_STRONG"></span><span id="security_flag_strength_strong"></span>\_ \_ SICHERHEITSFLAGSTÄRKE \_ STARK | Verwendet eine starke Verschlüsselung (128 Bit). Dies wird nur in einem Aufruf von [**WinHttpQueryOption zurückgegeben.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) |
| <span id="SECURITY_FLAG_STRENGTH_WEAK"></span><span id="security_flag_strength_weak"></span>\_ \_ SICHERHEITSFLAGSTÄRKE \_ SCHWACH | Verwendet eine schwache (40-Bit)-Verschlüsselung. Dies wird nur in einem Aufruf von [**WinHttpQueryOption zurückgegeben.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) |


</dl> </dd> <dt>

<span id="WINHTTP_OPTION_SECURITY_INFO"></span><span id="winhttp_option_security_info"></span>**SICHERHEITSINFORMATIONEN \_ ZUR WINHTTP-OPTION \_ \_**
</dt> <dd> <dl> <dt>



Sucht die SChannel-Verbindung und Verschlüsselungsinformationen für eine Anforderung.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SECURITY_KEY_BITNESS"></span><span id="winhttp_option_security_key_bitness"></span>**\_WINHTTP-OPTION \_ \_ \_ SICHERHEITSSCHLÜSSELBITNESS**
</dt> <dd> <dl> <dt>



Ruft einen ganzzahligen Wert ohne Vorzeichen ab, der die Verschlüsselungsstärke des Verschlüsselungsschlüssels enthält. Eine größere Zahl gibt eine stärkere Verschlüsselung mit Verschlüsselungsstärke an.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SEND_TIMEOUT"></span><span id="winhttp_option_send_timeout"></span>**TIMEOUT \_ BEIM SENDEN DER \_ \_ WINHTTP-OPTION**
</dt> <dd> <dl> <dt>



Legt einen ganzzahligen Wert ohne Vorzeichen fest, der den Time out-Wert in Millisekunden enthält, um eine Anforderung zu senden oder Daten zu schreiben, oder ruft ihn ab. Wenn das Senden der Anforderung länger als das Timeout dauert, wird der Sendevorgang abgebrochen. Der Standardzeitraum bis zum Timeout beträgt 30 Sekunden.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SERVER_CBT"></span><span id="winhttp_option_server_cbt"></span>**WINHTTP \_ OPTION \_ SERVER \_ CBT**
</dt> <dd> <dl> <dt>



Ruft einen Zeiger auf die [**SecPkgContext-Bindungsstruktur \_**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings) ab, die ein Kanalbindungstoken (Channel Binding Token, CBT) angibt.

Ein Kanalbindungstoken ist eine Eigenschaft eines sicheren Transportkanals und wird verwendet, um einen Authentifizierungskanal an den sicheren Transportkanal zu binden. Dieses Token kann von dieser Option nur nach dem Herstellen einer SSL-Verbindung erhalten werden.

> [!Note]
> Die Übergabe dieser  Option und eines NULL-Werts für *lpBuffer* an [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) gibt ERROR INSUFFICIENT BUFFER und die erforderliche Bytegröße für den Puffer im \_ \_ *lpdwBufferLength-Parameter* zurück. Dieser zurückgegebene Puffergrößenwert kann in einem nachfolgenden Aufruf zur Abfrage des Kanalbindungstokens übergeben werden. Diese Schritte sind erforderlich, wenn Sie WINHTTP CALLBACK STATUS REQUEST behandeln, wenn Sie Anforderungsheader basierend auf dem \_ \_ \_ Kanalbindungstoken ändern möchten. Beachten Sie, dass Windows XP und Vista das Ändern von Anforderungsheadern während dieses Rückrufs nicht unterstützen.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SERVER_CERT_CHAIN_CONTEXT"></span><span id="winhttp_option_server_cert_chain_context"></span>**WINHTTP \_ OPTION \_ SERVER \_ CERT \_ CHAIN \_ CONTEXT**
</dt> <dd> <dl> <dt>



Ruft den Kontext der Serverzertifizierungskette ab. **WINHTTP \_ OPTION \_ SERVER \_ CERT CHAIN \_ \_ CONTEXT** kann übergeben werden, um einen duplizierten Zeiger auf **den CERT CHAIN \_ \_ CONTEXT** für eine Serverzertifikatkette zu erhalten, die während einer ausgehandelten SSL-Verbindung empfangen wird. Der Client muss [**CertFreeCertificateContext für**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) den zurückgegebenen PCCERT CONTEXT-Zeiger aufrufen, \_ der in den Puffer gefüllt wird.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SERVER_CERT_CONTEXT"></span><span id="winhttp_option_server_cert_context"></span>**WINHTTP \_ OPTION \_ SERVER \_ CERT \_ CONTEXT**
</dt> <dd> <dl> <dt>



Ruft den Serverzertifizierungskontext ab. **WINHTTP \_ OPTION \_ SERVER \_ CERT \_ CONTEXT** kann übergeben werden, um einen duplizierten Zeiger auf [**den CERT CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) für ein Serverzertifikat zu erhalten, das während einer ausgehandelten SSL-Verbindung empfangen wurde. Der Client muss [**CertFreeCertificateContext für**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) den zurückgegebenen PCCERT CONTEXT-Zeiger aufrufen, \_ der in den Puffer gefüllt wird.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SERVER_SPN_USED"></span><span id="winhttp_option_server_spn_used"></span>**VERWENDETER \_ \_ WINHTTP-OPTIONSSERVER-SPN \_ \_**
</dt> <dd> <dl> <dt>



Ruft den Serverprinzipalnamen ab, den WinHTTP während der Authentifizierung für SSPI bereitgestellt hat. Dieser Zeichenfolgenwert kann nach einem Authentifizierungsfehler [**an SspiPromptForCredentials**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) übergeben werden.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SPN"></span><span id="winhttp_option_spn"></span>**\_ \_ WINHTTP-OPTIONS-SPN**
</dt> <dd> <dl> <dt>



Schließt die Serverportnummer ein oder entfernt sie, wenn der SPN (Dienstprinzipalname) für die Kerberos- oder Negotiate Kerberos-Authentifizierung erstellt wurde. Dieses Flag ist einer der folgenden Werte:

| Begriff | Beschreibung |
|-|-|
| <span id="WINHTTP_DISABLE_SPN_SERVER_PORT"></span><span id="winhttp_disable_spn_server_port"></span>\_WINHTTP: \_ DEAKTIVIEREN DES SPN-SERVERPORTS \_ \_ | Entfernt die Serverportnummer. |
| <span id="WINHTTP_ENABLE_SPN_SERVER_PORT"></span><span id="winhttp_enable_spn_server_port"></span>WINHTTP \_ ENABLE \_ SPN \_ SERVER \_ PORT | Schließt die Serverportnummer ein. |


</dl> </dd> <dt>

<span id="WINHTTP_OPTION_STREAM_ERROR_CODE"></span><span id="winhttp_option_stream_error_code"></span>**\_ \_ WINHTTP-OPTIONSSTREAMFEHLERCODE \_ \_**
</dt> <dd> <dl> <dt>


Diese Option kann für ein WinHttp-Anforderungshand handle abgefragt werden und gibt den Fehlercode zurück, der durch einen RST_STREAM für einen HTTP-Stream empfangen wird.



</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_TCP_FAST_OPEN"></span><span id="winhttp_option_tcp_fast_open"></span>**WINHTTP-OPTION \_ \_ TCP FAST \_ \_ OPEN**
</dt> <dd> <dl> <dt>



Aktiviert TCP Fast Open für die Verbindung.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_TCP_KEEPALIVE"></span><span id="winhttp_option_tcp_keepalive"></span>**\_WINHTTP-OPTION \_ TCP \_ KEEPALIVE**
</dt> <dd> <dl> <dt>



Diese Option kann für ein WinHttp-Sitzungshand handle festgelegt werden, um das TCP-Keep-Alive-Verhalten für den zugrunde liegenden Socket zu aktivieren. Übernimmt eine [**\_ tcp-Keepalive-Struktur.**](/windows/win32/winsock/sio-keepalive-vals)


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_TLS_FALSE_START"></span><span id="winhttp_option_tls_false_start"></span>**WINHTTP-OPTION \_ \_ TLS FALSE \_ \_ START**
</dt> <dd> <dl> <dt>



Aktiviert TLS False Start für die Verbindung.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_TLS_PROTOCOL_INSECURE_FALLBACK"></span><span id="winhttp_option_tls_protocol_insecure_fallback"></span>**UNSICHERER \_ \_ \_ FALLBACK DES TLS-PROTOKOLLS DER \_ WINHTTP-OPTION \_**
</dt> <dd> <dl> <dt>



Diese Option kann für ein WinHttp-Sitzungshand handle festgelegt werden, um zu steuern, ob ein Fallback auf TLS 1.0 zulässig ist, wenn ein TLS-Handshakefehler mit einer neueren Protokollversion vorgibt.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_UNLOAD_NOTIFY_EVENT"></span><span id="winhttp_option_unload_notify_event"></span>**WINHTTP-OPTION \_ \_ \_ ENTLADEBENACHRICHTIGUNGSEREIGNIS \_**
</dt> <dd> <dl> <dt>



Nimmt ein Ereignis an, das festgelegt wird, wenn der letzte Rückruf für eine bestimmte Sitzung abgeschlossen wurde. Dieses Flag muss für ein Sitzungshand handle verwendet werden. Das Ereignis kann erst geschlossen werden, nachdem es von WinHTTP festgelegt wurde.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_UNSAFE_HEADER_PARSING"></span><span id="winhttp_option_unsafe_header_parsing"></span>**WINHTTP \_ OPTION \_ UNSAFE \_ HEADER \_ PARSING**
</dt> <dd> <dl> <dt>



Diese Option ist für die interne Verwendung reserviert und sollte nicht aufgerufen werden.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_UPGRADE_TO_WEB_SOCKET"></span><span id="winhttp_option_upgrade_to_web_socket"></span>**UPGRADE DER \_ \_ WINHTTP-OPTION \_ AUF \_ \_ WEBSOCKET**
</dt> <dd> <dl> <dt>



Weist den Stapel an, einen WebSocket-Handshakeprozess mit [**WinHttpSendRequest zu starten.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) Für diese Option werden keine Parameter verwendet.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_URL"></span><span id="winhttp_option_url"></span>**URL DER \_ \_ WINHTTP-OPTION**
</dt> <dd> <dl> <dt>



Ruft einen Zeichenfolgenwert ab, der die vollständige URL einer heruntergeladenen Ressource enthält. Wenn die ursprüngliche URL zusätzliche Daten enthält, z. B. Suchzeichenfolgen oder Anker, oder wenn der Aufruf umgeleitet wurde, unterscheidet sich die zurückgegebene URL von der ursprünglichen URL. Die Anwendung sollte einen Puffer in Bytegröße übergeben, der groß genug ist, um die zurückgegebene URL in wide char zu enthalten.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_USE_GLOBAL_SERVER_CREDENTIALS"></span><span id="winhttp_option_use_global_server_credentials"></span>**\_WINHTTP-OPTION \_ GLOBALE \_ SERVERANMELDEINFORMATIONEN \_ \_ VERWENDEN**
</dt> <dd> <dl> <dt>



Verwendet eine **BOOL** und kann nur für ein Sitzungshandl festgelegt werden. Sie wird nur an Handles, die aus dem Sitzungshandles erstellt wurden, nach dem Festlegen der Option weiter. True **gibt an,** dass diese Option als letztes Mittel die Verwendung globaler Serveranmeldeinformationen verursacht, die von WinInet übertragen wurden. Der Standardwert für diese Option ist **FALSE.** Diese Option erfordert den Registrierungsschlüssel **HKLM \\ Software Microsoft \\ Windows \\ \\ CurrentVersion Internet \\ Settings! ShareCredsWithWinHttp**. Dieser Registrierungsschlüssel ist standardmäßig nicht vorhanden. Wenn sie festgelegt ist, sendet WinINet Anmeldeinformationen an WinHTTP. Wenn WinHttp eine Authentifizierungsforderung erhält und keine Anmeldeinformationen für das aktuelle Handle festgelegt sind, werden die von WinINet bereitgestellten Anmeldeinformationen verwendet.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_USER_AGENT"></span><span id="winhttp_option_user_agent"></span>**\_BENUTZER-AGENT DER WINHTTP-OPTION \_ \_**
</dt> <dd> <dl> <dt>



Legt die Benutzer-Agent-Zeichenfolge für handles fest, die von [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) bereitgestellt und in [**nachfolgenden WinHttpSendRequest-Funktionen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) verwendet wird, oder ruft sie ab, solange sie nicht durch einen Header überschrieben wird, der von [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) oder **WinHttpSendRequest hinzugefügt** wurde. [](glossary.md) Beim Abrufen eines Benutzer-Agents sollte die Anwendung einen Puffer in Bytegröße übergeben, der groß genug ist, um die zurückgegebene URL in wide char zu speichern. Beim Festlegen des Benutzer-Agents ist die Puffergröße die Länge der Zeichenfolge in Zeichen plus **das NULL-Abschlusszeichen.**


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_USERNAME"></span><span id="winhttp_option_username"></span>**\_ \_ WINHTTP-OPTIONSBENUTZERNAME**
</dt> <dd> <dl> <dt>



Legt eine Zeichenfolge fest, die den Benutzernamen enthält, oder ruft sie ab.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_WEB_SOCKET_CLOSE_TIMEOUT"></span><span id="winhttp_option_web_socket_close_timeout"></span>**\_WINHTTP-OPTION: \_ \_ TIMEOUT BEIM \_ SCHLIEßEN DES WEBSOCKET \_**
</dt> <dd> <dl> <dt>



Legt die Zeit in Millisekunden fest, die [**WinHttpWebSocketClose**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketclose) warten soll, bis der schließende Handshake abgeschlossen ist. Die Standardeinstellung beträgt 10 Sekunden.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_WEB_SOCKET_KEEPALIVE_INTERVAL"></span><span id="winhttp_option_web_socket_keepalive_interval"></span>**WINHTTP-OPTION \_ \_ WEB SOCKET \_ \_ KEEPALIVE \_ INTERVAL**
</dt> <dd> <dl> <dt>



Legt das Intervall in Millisekunden fest, um ein Keep-Alive-Paket über die Verbindung zu senden. Das Standardintervall ist 30.000 (30 Sekunden). Das Mindestintervall beträgt 15.000 (15 Sekunden). Die [**Verwendung von WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) zum Festlegen eines Werts unter 15000 gibt mit **ERROR INVALID PARAMETER \_ \_ zurück.**

> [!Note]
> Der Standardwert für **WINHTTP \_ OPTION WEB SOCKET \_ \_ \_ KEEPALIVE \_ INTERVAL** wird aus **HKLM: \\ SOFTWARE Microsoft \\ \\ WebSocket \\ KeepaliveInterval gelesen.** Wenn kein Wert festgelegt ist, wird der Standardwert 30000 verwendet. Es ist nicht möglich, ein niedrigeres Keepalive-Intervall als 15.000 Millisekunden zu haben.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_WEB_SOCKET_RECEIVE_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_receive_buffer_size"></span>**WINHTTP-OPTION \_ \_ \_ WEBSOCKET \_ \_ \_ EMPFANGSPUFFERGRÖßE**
</dt> <dd> <dl> <dt>



Legt ein DWORD fest oder ruft es ab, das die Empfangspuffergröße angibt, die für WebSocket-Verbindungen verwendet werden soll.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_WEB_SOCKET_SEND_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_send_buffer_size"></span>**WINHTTP-OPTION \_ \_ \_ WEBSOCKET- \_ \_ \_ SENDEPUFFERGRÖßE**
</dt> <dd> <dl> <dt>



Legt ein DWORD fest oder ruft es ab, das die Sendepuffergröße angibt, die für WebSocket-Verbindungen verwendet werden soll.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_WORKER_THREAD_COUNT"></span><span id="winhttp_option_worker_thread_count"></span>**ANZAHL DER \_ \_ ARBEITSTHREADS \_ DER WINHTTP-OPTION \_**
</dt> <dd> <dl> <dt>



Legt einen ganzzahligen Wert ohne Vorzeichen fest, der die Anzahl der Arbeitsthreads angibt, die der Threadpool für asynchrone Vervollständigungen verwenden soll. Der Standardwert dieser Option ist 0 (null), was angibt, dass die Anzahl der Arbeitsthreads der Anzahl von CPUs im System entspricht. Diese Option kann nur für ein **NULL**  [HINTERNET-Handle festgelegt](hinternet-handles-in-winhttp.md) werden, bevor ein asynchroner Vorgang ausgeführt wurde. Diese Option kann nur einmal festgelegt werden.

**Windows Server 2008 R2 und Windows 7:** Dieses Flag ist veraltet.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_WRITE_BUFFER_SIZE"></span><span id="winhttp_option_write_buffer_size"></span>**\_WINHTTP-OPTION: \_ \_ \_ SCHREIBPUFFERGRÖßE**
</dt> <dd> <dl> <dt>



Diese Option ist veraltet. es hat keine Auswirkungen.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

In der folgenden Tabelle werden die Optionsflags aufgeführt, indem angegeben wird, auf welche Handles sie angewendet werden können, ob sie abgefragt und festgelegt werden können und welcher Datentyp verwendet werden kann. Ein "X" gibt an, dass das Optionsflag für die Verwendung mit der Funktion oder dem Handle gültig ist, während ein "-" angibt, dass das Optionsflag ungültig ist.

Der Versuch, ein Optionsflag für eine Windows-Version, in der es nicht unterstützt wird, zu festlegen oder abfragt, führt zu **ERROR \_ WINHTTP \_ INVALID \_ OPTION**.

| Optionsflag und Datentyp | Sitzungshand handle | Anforderungshand handle | Abfrageoption | SET-Option | Mindestversion von Windows |
|-|-|-|-|-|-|
| \_WINHTTP-OPTION \_ \_ GARANTIERTE NICHT \_ \_ BLOCKIERENDE RÜCKRUFE<br/>**Bool** | X | \- | \- | X | \- |
| RICHTLINIE FÜR \_ DIE AUTOMATISCHE ANMELDUNG DER WINHTTP-OPTION \_ \_<br/>**DWORD** | \- | X | \- | X | \- |
| \_ \_ WINHTTP-OPTIONSRÜCKRUF<br/>**LPVOID** | X | X | X | X | \- |
| WINHTTP \_ OPTION \_ CLIENT \_ CERT \_ CONTEXT<br/>[**\_CERT-KONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) | \- | X | \- | X | Windows Vista |
| WINHTTP \_ OPTION \_ CLIENT \_ CERT \_ ISSUER \_ LIST<br/>[**SecPkgContext \_ IssuerListInfoEx**](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) | \- | X | X | \- | Windows Vista |
| WINHTTP \_ OPTION \_ CODEPAGE<br/>**DWORD** | X | \- | \- | X | \- |
| \_WINHTTP-OPTION \_ : KONFIGURIEREN DER \_ \_ PASSPORT-AUTHENTIFIZIERUNG<br/>**DWORD** | X | \- | \- | X | \- |
| WINHTTP \_ OPTION \_ \_ CONNECT-WIEDERHOLUNGEN<br/>**DWORD** | X | X | X | X | \- |
| WINHTTP \_ OPTION \_ CONNECT \_ TIMEOUT<br/>**DWORD** | X | X | X | X | \- |
| VERBINDUNGSINFORMATIONEN ZUR \_ WINHTTP-OPTION \_ \_<br/>[**\_WINHTTP-VERBINDUNGSINFORMATIONEN \_**](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info) | \- | X | X | \- | \- |
| WINHTTP \_ OPTION \_ CONNECTION \_ STATS \_ V0<br/>[**TCP \_ INFO \_ v0**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0) | \- | X | X | \- | Windows 10 Version 1903 |
| WINHTTP \_ OPTION \_ CONNECTION \_ STATS \_ V1<br/>[**TCP \_ INFO \_ v1**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1) | \- | X | X | \- | Windows 10 Version 2004 |
| \_ \_ WINHTTP-OPTIONSKONTEXTWERT \_<br/>**DWORD \_ PTR** | X | X | X | X | \- |
| WINHTTP \_ OPTION \_ DEKOMPRIMIERUNG<br/>**DWORD** | X | X | \- | X | Windows 8.1 |
| WINHTTP \_ OPTION \_ DISABLE \_ FEATURE<br/>**DWORD** | \- | X | \- | X | \- |
| WINHTTP \_ OPTION \_ DISABLE \_ SECURE \_ PROTOCOL \_ FALLBACK<br/>**Bool** | X | \- | \- | X | Windows 10 Version 1903 |
| \_WINHTTP-OPTION \_ : DEAKTIVIEREN DER \_ \_ STREAMWARTESCHLANGE<br/>**Bool** | X | X | \- | X | Windows 10 Version 1809 |
| FEATURE \_ "WINHTTP-OPTION \_ \_ AKTIVIEREN"<br/>**DWORD** | \* | \* | \- | X | \- |
| WINHTTP \_ OPTION \_ ENABLE \_ HTTP \_ PROTOCOL<br/>**DWORD** | X | X | \- | X | Windows 10, Version 1607 |
| \_WINHTTP-OPTION \_ AKTIVIEREN DES \_ HTTP2 \_ \_ PLUS-CLIENTZERTIFIKATKONTEXTS \_ \_<br/>**Bool** | X | \- | \- | X | Windows 10 Version 21H1 |
| \_WINHTTP-OPTION \_ ENABLETRACING<br/>**DWORD** | \- | \- | X | X | \- |
| WINHTTP \_ OPTION \_ ENCODE \_ EXTRA<br/>**Bool** | X | X | \- | X | Windows 10 Version 1803 |
| \_WINHTTP-OPTION \_ LÄUFT VERBINDUNG AB \_<br/>– | \- | X | \- | X | Windows 10 Version 1903 |
| \_ \_ ERWEITERTER \_ WINHTTP-OPTION-FEHLER<br/>**DWORD** | X | X | X | \- | \- |
| WINHTTP \_ OPTION \_ GLOBAL \_ PROXY \_ CREDS<br/>[**WINHTTP \_ CREDS**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds) | X | X | \- | X | \- |
| WINHTTP \_ OPTION \_ GLOBAL \_ SERVER \_ CREDS<br/>[**WINHTTP \_ CREDS \_ EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) | X | X | \- | X | \- |
| TYP DES \_ WINHTTP-OPTIONSHANDLE \_ \_<br/>**DWORD** | X | X | X | \- | \- |
| WINHTTP \_ OPTION HTTP PROTOCOL \_ \_ \_ ERFORDERLICH<br/>**Bool** | X | X | \- | X | Windows 10 Version 1903 |
| VERWENDETES \_ \_ \_ HTTP-PROTOKOLL DER WINHTTP-OPTION \_<br/>**DWORD** | \- | X | X | \- | Windows 10, Version 1607 |
| WINHTTP \_ OPTION \_ \_ HTTP-VERSION<br/>[**\_ \_ HTTP-VERSIONSINFORMATIONEN**](/windows/win32/api/winhttp/ns-winhttp-http_version_info) | X | X | X | X | \- |
| \_WINHTTP-OPTION \_ HTTP2 \_ KEEPALIVE<br/>**DWORD** | X | \- | \- | X | Windows 10 Version 21H1 |
| \_WINHTTP-OPTION \_ HTTP2 \_ PLUS \_ \_ ÜBERTRAGUNGSCODIERUNG<br/>**Bool** | X | X | \- | X | Windows 10 Version 21H1 |
| WINHTTP \_ OPTION \_ IGNORE \_ CERT \_ REVOCATION \_ OFFLINE<br/>**Bool** | \- | X | \- | X | Windows 10 Version 2004 |
| WINHTTP \_ OPTION \_ IPV6 \_ FAST \_ FALLBACK<br/>**Bool** | X | \- | \- | X | Windows 10 Version 1903 |
| \_WINHTTP-OPTION: \_ \_ PROXY \_ \_ CONNECT-ANTWORT<br/>**Bool** | X | X | X | \- | \- |
| WINHTTP \_ OPTION \_ \_ MAX. CONNS \_ PRO \_ 1 \_ 0 \_ SERVER<br/>**DWORD** | X | \- | X | X | \- |
| WINHTTP \_ OPTION \_ \_ MAX. ANZAHL VON CONNS \_ PRO \_ SERVER<br/>**DWORD** | X | \- | X | X | \- |
| WINHTTP \_ OPTION \_ \_ MAX. AUTOMATISCHE \_ \_ HTTP-UMLEITUNGEN<br/>**DWORD** | X | X | X | X | \- |
| WINHTTP \_ OPTION \_ MAX \_ HTTP \_ STATUS \_ CONTINUE<br/>**DWORD** | X | X | X | X | \- |
| WINHTTP \_ OPTION \_ MAX \_ RESPONSE \_ DRAIN \_ SIZE<br/>**DWORD** | X | X | X | X | \- |
| MAXIMALE \_ \_ \_ \_ ANTWORTHEADERGRÖßE \_ DER WINHTTP-OPTION<br/>**DWORD** | X | X | X | X | \- |
| \_ \_ ÜBERGEORDNETES WINHTTP-OPTIONSHANDLE \_<br/>[HINTERNET](hinternet-handles-in-winhttp.md) | X | X | X | \- | \- |
| WINHTTP \_ OPTION \_ PASSPORT \_ COBRANDING \_ TEXT<br/>**Lpwstr** | \- | X | X | \- | \- |
| WINHTTP \_ OPTION \_ PASSPORT \_ COBRANDING \_ URL<br/>**Lpwstr** | \- | X | X | \- | \- |
| WINHTTP \_ OPTION \_ PASSPORT \_ RETURN \_ URL<br/>**LPVOID** | \- | X | X | \- | \- |
| WINHTTP \_ OPTION \_ PASSPORT \_ SIGN \_ OUT<br/>**LPVOID** | X | \- | \- | X | \- |
| \_ \_ WINHTTP-OPTIONSKENNWORT<br/>**Lpwstr** | \- | X | X | X | \- |
| \_WINHTTP-OPTIONSPROXY \_<br/>[**\_WINHTTP-PROXYINFORMATIONEN \_**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) | X | X | X | X | \- |
| WINHTTP \_ OPTION \_ PROXY \_ PASSWORD<br/>**Lpwstr** | \- | X | X | X | \- |
| VERWENDETER \_ \_ WINHTTP-OPTIONSPROXY-SPN \_ \_<br/>**Lpwstr** | \- | X | X | \- | \- |
| \_WINHTTP-OPTION \_ \_ PROXYBENUTZERNAME<br/>**Lpwstr** | \- | X | X | X | \- |
| WINHTTP \_ OPTION \_ READ \_ BUFFER \_ SIZE<br/>**DWORD** | \- | X | X | X | \- |
| \_WINHTTP-OPTION \_ " PROXY \_ \_ \_ CONNECT-ANTWORT EMPFANGEN"<br/>**Bool** | X | X | \- | X | \- |
| WINHTTP \_ OPTION \_ RECEIVE \_ RESPONSE \_ TIMEOUT<br/>**DWORD** | X | X | X | X | \- |
| WINHTTP \_ OPTION \_ RECEIVE \_ TIMEOUT<br/>**DWORD** | X | X | X | X | \- |
| UMLEITUNGSRICHTLINIE FÜR \_ WINHTTP-OPTION \_ \_<br/>**DWORD** | X | X | X | X | \- |
| \_WINHTTP-OPTION \_ \_ : USERPWD \_ IN \_ URL ABLEHNEN<br/>**Bool** | \- | X | \- | X | \- |
| \_ANFORDERUNGSPRIORITÄT DER WINHTTP-OPTION \_ \_<br/>**DWORD** | \- | X | X | X | \- |
| WINHTTP \_ OPTION \_ REQUEST \_ STATS<br/>[**WINHTTP \_ REQUEST \_ STATS**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats) | \- | X | X | \- | Windows 10 Version 1903 |
| ANFORDERUNGSZEITEN DER \_ WINHTTP-OPTION \_ \_<br/>[**\_WINHTTP-ANFORDERUNGSZEITEN \_**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times) | \- | X | X | \- | Windows 10 Version 1903 |
| WINHTTP \_ OPTION \_ REQUIRE \_ STREAM \_ END<br/>**Bool** | X | X | \- | X | Windows 10 Version 21H1 |
| WINHTTP \_ OPTION \_ RESOLUTION \_ HOSTNAME<br/>**Lpwstr** | \- | X | \- | X | Windows 10 Version 21H1 |
| TIMEOUT FÜR AUFLÖSUNG DER \_ WINHTTP-OPTION \_ \_<br/>**DWORD** | X | X | X | X | \- |
| SICHERE PROTOKOLLE \_ DER WINHTTP-OPTION \_ \_<br/>**DWORD** | X | \- | \- | X | \- |
| \_SICHERHEITSZERTIFIKATSTRUKTUR DER WINHTTP-OPTION \_ \_ \_<br/>[**\_WINHTTP-ZERTIFIKATINFORMATIONEN \_**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) | \- | X | X | \- | \- |
| \_SICHERHEITSFLAGS FÜR DIE WINHTTP-OPTION \_ \_<br/>**DWORD** | \- | X | X | X | \- |
| SICHERHEITSINFORMATIONEN \_ ZUR WINHTTP-OPTION \_ \_<br/>[**WINHTTP_SECURITY_INFO**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_security_info) | \- | X | X | \- | Windows 10 Version 2004 |
| \_WINHTTP-OPTION \_ \_ \_ SICHERHEITSSCHLÜSSELBITNESS<br/>**DWORD** | \- | X | X | \- | \- |
| TIMEOUT \_ BEIM SENDEN DER \_ \_ WINHTTP-OPTION<br/>**DWORD** | X | X | X | X | \- |
| WINHTTP \_ OPTION \_ SERVER \_ CBT<br/>[**\_SecPkgContext-Bindungen**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings)\* | \- | X | X | \- | \- |
| WINHTTP \_ OPTION \_ SERVER \_ CERT \_ CHAIN \_ CONTEXT<br/>[**CERT_CHAIN_CONTEXT**](/windows/win32/api/wincrypt/ns-wincrypt-cert_chain_context) | \- | X | X | \- | Windows 10 Version 2004 |
| WINHTTP \_ OPTION \_ SERVER \_ CERT \_ CONTEXT<br/>[**CERT-KONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) | \- | X | X | \- | \- |
| VERWENDETER \_ \_ WINHTTP-OPTIONSSERVER-SPN \_ \_<br/>**Lpwstr** | \- | X | X | \- | \- |
| \_ \_ WINHTTP-OPTIONS-SPN<br/>**DWORD** | \- | X | \- | X | \- |
| \_ \_ WINHTTP-OPTIONSSTREAMFEHLERCODE \_ \_<br/>**DWORD** | \- | X | X | \- | Windows 10 Version 21H1 |
| WINHTTP-OPTION \_ \_ TCP FAST \_ \_ OPEN<br/>**Bool** | X | \- | \- | X | Windows 10 Version 2004 |
| \_WINHTTP-OPTION \_ TCP \_ KEEPALIVE<br/>[**tcp \_ keepalive**](/windows/win32/winsock/sio-keepalive-vals) | X | \- | \- | X | Windows 10 Version 2004 |
| WINHTTP-OPTION \_ \_ TLS FALSE \_ \_ START<br/>**Bool** | X | \- | \- | X | Windows 10 Version 2004 |
| UNSICHERER \_ \_ \_ FALLBACK DES TLS-PROTOKOLLS DER \_ WINHTTP-OPTION \_<br/>**Bool** | X | \- | \- | X | Windows 10 Version 21H1 |
| WINHTTP-OPTION \_ \_ \_ ENTLADEBENACHRICHTIGUNGSEREIGNIS \_<br/>[HINTERNET](hinternet-handles-in-winhttp.md) | X | \- | \- | X | \- |
| WINHTTP \_ OPTION \_ UNSAFE \_ HEADER \_ PARSING<br/>**DWORD** | \- | X | \- | X | \- |
| UPGRADE DER \_ \_ WINHTTP-OPTION \_ AUF \_ \_ WEBSOCKET<br/>– | \- | X | \- | X | \- |
| URL DER \_ \_ WINHTTP-OPTION<br/>**Lpwstr** | \- | X | X | \- | \- |
| \_WINHTTP-OPTION \_ GLOBALE \_ SERVERANMELDEINFORMATIONEN \_ \_ VERWENDEN<br/>**Bool** | X | X | \- | X | \- |
| \_BENUTZER-AGENT DER WINHTTP-OPTION \_ \_<br/>**Lpwstr** | X | \- | X | X | \- |
| \_ \_ WINHTTP-OPTIONSBENUTZERNAME<br/>**Lpwstr** | \- | X | X | X | \- |
| \_WINHTTP-OPTION: \_ \_ TIMEOUT BEIM \_ SCHLIEßEN DES WEBSOCKET \_<br/>**DWORD** | \- | \- | X | X | \- |
| WINHTTP-OPTION \_ \_ WEB SOCKET \_ \_ KEEPALIVE \_ INTERVAL<br/>**DWORD** | \- | \- | X | X | \- |
| WINHTTP-OPTION \_ \_ \_ WEBSOCKET \_ \_ \_ EMPFANGSPUFFERGRÖßE<br/>**DWORD** | X | X | X | X | Windows 8.1 |
| WINHTTP-OPTION \_ \_ \_ WEBSOCKET- \_ \_ \_ SENDEPUFFERGRÖßE<br/>**DWORD** | X | X | X | X | Windows 8.1 |
| ANZAHL DER \_ \_ ARBEITSTHREADS \_ DER WINHTTP-OPTION \_<br/>**DWORD** | \- | \- | \- | X | \- |
| \_WINHTTP-OPTION: \_ \_ \_ SCHREIBPUFFERGRÖßE<br/>**DWORD** | \- | X | X | X | \- |

> [!Note]
> Informationen zu Windows XP und Windows 2000 finden Sie unter [Laufzeitanforderungen.](winhttp-start-page.md)

## <a name="requirements"></a>Requirements (Anforderungen)

| Anforderung | Wert |
|--------------------------|---------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client) | Nur Windows XP, Windows 2000 Professional mit \[ SP3-Desktop-Apps\]            |
| Unterstützte Mindestversion (Server) | Nur Windows Server 2003, Windows 2000 Server mit \[ SP3-Desktop-Apps\]         |
| Verteilbare Komponente          | WinHTTP 5.0 und Internet Explorer 5.01 oder höher unter Windows XP und Windows 2000. |
| Header                   | Winhttp.h                                                                       |

## <a name="see-also"></a>Siehe auch

[WinHTTP-Versionen](winhttp-versions.md)
