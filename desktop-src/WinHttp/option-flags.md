---
Description: Die folgenden Optionsflags werden von WinHttpQueryOption und WinHttpSetOption unterstützt.
ms.assetid: 2d0441f4-ddba-4f2a-8861-8803cad6f1ac
title: Optionsflags (Winhttp.h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 02/25/2020
ms.openlocfilehash: ecc3d27bd8d168c276ccac2544dbc648fbdfee5732e87892624903285b3a2fcf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117744061"
---
# <a name="option-flags"></a>Optionsflags

Die folgenden Optionsflags werden von [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) und [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)unterstützt.

<dl> <dt>

<span id="WINHTTP_OPTION_ASSURED_NON_BLOCKING_CALLBACKS"></span><span id="winhttp_option_assured_non_blocking_callbacks"></span>**\_WINHTTP-OPTION \_ GARANTIERT NICHT \_ \_ BLOCKIERENDE \_ RÜCKRUFE**
</dt> <dd> <dl> <dt>



Der Standardwert lautet FALSE. Wenn diese Einstellung auf TRUE festgelegt ist, garantiert WinHTTP nicht den Fortschritt, wenn Statusrückrufe von der Clientanwendung blockiert werden.

Die Clientanwendung muss besonders darauf achten, minimale Vorgänge innerhalb des Rückrufs ohne Blockierung auszuführen, so schnell wie möglich zurückzugeben und insbesondere nicht auf nachfolgende WinHTTP-Aufrufe zu warten. Wenn diese Richtlinien nicht befolgt werden, kann dies negative Auswirkungen auf die Leistung haben oder eine anwendung hängen bleiben. Wenn diese Option auf vorgeschriebene Weise verwendet wird, kann die Leistung verbessert werden.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_AUTOLOGON_POLICY"></span><span id="winhttp_option_autologon_policy"></span>**WINHTTP \_ OPTION \_ AUTOLOGON \_ POLICY**
</dt> <dd> <dl> <dt>



Legt einen ganzzahligen Wert ohne Vorzeichen fest, der die Richtlinie für automatische [Anmeldung](authentication-in-winhttp.md) mit einem der folgenden Werte angibt.

| Begriff | BESCHREIBUNG |
|-|-|
| <span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_HIGH"></span><span id="winhttp_autologon_security_level_high"></span>WINHTTP \_ AUTOLOGON \_ SECURITY \_ LEVEL \_ HIGH | Standardanmeldeinformationen werden nicht verwendet. Beachten Sie, dass dieses Flag nur wirksam wird, wenn Sie den Server anhand des tatsächlichen Computernamens angeben. Sie wird nicht wirksam, wenn Sie den Server nach "localhost" oder IP-Adresse angeben. |
| <span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_LOW"></span><span id="winhttp_autologon_security_level_low"></span>WINHTTP \_ AUTOLOGON \_ SECURITY \_ LEVEL \_ LOW | Eine authentifizierte Anmeldung mit den Standardanmeldeinformationen wird für alle Anforderungen ausgeführt. |
| <span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_MEDIUM"></span><span id="winhttp_autologon_security_level_medium"></span>WINHTTP \_ AUTOLOGON \_ SECURITY \_ LEVEL \_ MEDIUM | Eine authentifizierte Anmeldung mit den Standardanmeldeinformationen wird nur für Anforderungen im lokalen Intranet ausgeführt. |


</dl> </dd> <dt>

<span id="WINHTTP_OPTION_BACKGROUND_CONNECTIONS"></span><span id="winhttp_option_background_connections"></span>**HINTERGRUNDVERBINDUNGEN DER \_ WINHTTP-OPTION \_ \_**
</dt> <dd> <dl> <dt>

Wenn Sie diese Option für ein Sitzungshandle festlegen, müssen Sie die Anzahl der Verbindungen übergeben, die Sie öffnen möchten. Anschließend öffnet WinHttp beim ersten Senden einer Anforderung eine Reihe von Verbindungen parallel, anstatt nur eine einzelne Verbindung zu öffnen. Dies kann die Leistung nachfolgender Anforderungen an dasselbe Ziel verbessern, was nicht den Mehraufwand für die Verbindungseinrichtung mit sich bringen würde.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CALLBACK"></span><span id="winhttp_option_callback"></span>**\_ \_ WINHTTP-OPTIONSRÜCKRUF**
</dt> <dd> <dl> <dt>



Ruft den Zeiger auf die Rückruffunktion ab, die mit [**WinHttpSetStatusCallback**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback)festgelegt wurde.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CLIENT_CERT_CONTEXT"></span><span id="winhttp_option_client_cert_context"></span>**WINHTTP \_ OPTION \_ CLIENT \_ CERT \_ CONTEXT**
</dt> <dd> <dl> <dt>



Legt den Clientzertifikatkontext fest. Wenn eine Anwendung [**ERROR \_ WINHTTP CLIENT \_ \_ AUTH \_ CERT \_ NEEDED**](error-messages.md)empfängt, muss sie [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) aufrufen, um ein Zertifikat anzugeben, bevor die Anforderung erneut versucht wird. Im Rahmen der Verarbeitung dieser Option ruft WinHttp [**CertDuplicateCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecertificatecontext) für den vom Aufrufer bereitgestellten Zertifikatkontext auf, sodass der Zertifikatkontext unabhängig vom Aufrufer freigegeben werden kann.

> [!Note]
> Die Anwendung sollte nicht versuchen, den Zertifikatspeicher mit dem Flag CERT \_ CLOSE STORE FORCE FLAG im Aufruf von \_ \_ \_ [**CertCloseStore**](/windows/desktop/api/wincrypt/nf-wincrypt-certclosestore) für den Zertifikatspeicher zu schließen, aus dem der Zertifikatkontext abgerufen wurde. Es kann zu einer Zugriffsverletzung kommen.

Wenn der Server ein Clientzertifikat anfordert, gibt [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)oder [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) einen [**ERROR \_ WINHTTP \_ CLIENT \_ \_ AUTH CERT \_ NEEDED-Fehler**](error-messages.md) zurück. Wenn der Server das Zertifikat anfordert, es jedoch nicht benötigt, kann die Anwendung diese Option angeben, um anzugeben, dass es kein Zertifikat besitzt. Der Server kann ein anderes Authentifizierungsschema auswählen oder anonymen Zugriff auf den Server zulassen. Die Anwendung stellt das **WINHTTP \_ NO CLIENT \_ \_ CERT \_ CONTEXT-Makro** im *lpBuffer-Parameter* von [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) bereit, wie im folgenden Codebeispiel gezeigt.

``` syntax
BOOL fRet = WinHttpSetOption(hRequest,
                             WINHTTP_OPTION_CLIENT_CERT_CONTEXT,
                             WINHTTP_NO_CLIENT_CERT_CONTEXT,
                             0);
```

Wenn der Server ein Clientzertifikat erfordert, sendet er möglicherweise als Antwort den HTTP-Statuscode 403. Weitere Informationen finden Sie unter der OPTION **WINHTTP \_ OPTION CLIENT \_ \_ CERT ISSUER \_ \_ LIST.**


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CLIENT_CERT_ISSUER_LIST"></span><span id="winhttp_option_client_cert_issuer_list"></span>**WINHTTP \_ OPTION \_ CLIENT \_ CERT \_ ISSUER \_ LIST**
</dt> <dd> <dl> <dt>



Ruft eine [**SecPkgContext \_ IssuerListInfoEx-Struktur**](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) ab, wenn der Fehler von [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) oder [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) **ERROR \_ WINHTTP CLIENT \_ \_ \_ AUTH CERT \_ NEEDED** lautet. Die Ausstellerliste in der -Struktur enthält eine Liste zulässiger Zertifizierungsstellen vom Server. Die Clientanwendung kann die Liste der Zertifizierungsstellen filtern, um das Clientzertifikat für die SSL-Authentifizierung abzurufen.

Wenn der Server das Clientzertifikat anfordert, es jedoch nicht benötigt, kann die Anwendung [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) mit der OPTION **WINHTTP \_ OPTION CLIENT \_ \_ CERT \_ CONTEXT** aufrufen. Weitere Informationen finden Sie unter der OPTION **WINHTTP \_ OPTION CLIENT \_ \_ CERT \_ CONTEXT.**


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CODEPAGE"></span><span id="winhttp_option_codepage"></span>**WINHTTP \_ OPTION \_ CODEPAGE**
</dt> <dd> <dl> <dt>



Legt die [*Codepage*](glossary.md) fest, die zum Verarbeiten der URL verwendet wird (d. b. abfragezeichenfolge). Der Standardwert ist UTF8.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CONFIGURE_PASSPORT_AUTH"></span><span id="winhttp_option_configure_passport_auth"></span>**\_WINHTTP-OPTION \_ : KONFIGURIEREN DER \_ \_ PASSPORT-AUTHENTIFIZIERUNG**
</dt> <dd> <dl> <dt>



Legt einen ganzzahligen Wert ohne Vorzeichen fest, der angibt, ob die [Passport-Authentifizierung in der WinHTTP-Authentifizierung](passport-authentication-in-winhttp.md) aktiviert ist. Der Wert kann in folgenden Formen vorliegen:

| Begriff | BESCHREIBUNG |
|-|-|
| <span id="WINHTTP_DISABLE_PASSPORT_AUTH"></span><span id="winhttp_disable_passport_auth"></span>\_WINHTTP: DEAKTIVIEREN DER \_ \_ PASSPORT-AUTHENTIFIZIERUNG | Microsoft Passport Authentifizierung ist deaktiviert. Dies ist die Standardoption. |
| <span id="WINHTTP_DISABLE_PASSPORT_KEYRING"></span><span id="winhttp_disable_passport_keyring"></span>\_WINHTTP: DEAKTIVIEREN DES \_ \_ PASSPORT-SCHLÜSSELBUNDS | Der Passport-Schlüsselbund ist deaktiviert. Dies ist die Standardoption. |
| <span id="WINHTTP_ENABLE_PASSPORT_AUTH"></span><span id="winhttp_enable_passport_auth"></span>WINHTTP \_ ENABLE \_ PASSPORT \_ AUTH | Die Passport-Authentifizierung ist aktiviert. |
| <span id="WINHTTP_ENABLE_PASSPORT_KEYRING"></span><span id="winhttp_enable_passport_keyring"></span>WINHTTP \_ ENABLE \_ PASSPORT \_ KEYRING | Der Passport-Schlüsselbund ist aktiviert. |

</dl> </dd> <dt>

<span id="WINHTTP_OPTION_CONNECT_RETRIES"></span><span id="winhttp_option_connect_retries"></span>**WINHTTP \_ OPTION \_ \_ CONNECT-WIEDERHOLUNGEN**
</dt> <dd> <dl> <dt>



Legt einen ganzzahligen Wert ohne Vorzeichen fest oder ruft diesen ab, der die Anzahl der Versuche vonWinHTTP enthält, eine Verbindung mit einem Host herzustellen. Microsoft Windows HTTP Services (WinHTTP) versucht nur einmal pro IP-Adresse (Internet protocol). Wenn Sie beispielsweise versuchen, eine Verbindung mit einem mehrfach vernetzten Host herzustellen, der über 10 IP-Adressen verfügt, und **WINHTTP \_ OPTION CONNECT \_ \_ RETRIES** auf 7 festgelegt ist, versucht WinHTTP nur, eine Verbindung mit den ersten sieben IP-Adressen herzustellen. Wenn **winHTTP \_ OPTION CONNECT \_ \_ RETRIES** auf 20 festgelegt ist, versucht WinHTTP bei gleichem Satz von 10 IP-Adressen jede der 10 nur einmal. Wenn ein Verbindungsversuch nach der angegebenen Anzahl von Versuchen weiterhin fehlschlägt oder das Verbindungstimeout vor diesem Zeitpunkt abgelaufen ist, wird die Anforderung abgebrochen. Der Standardwert für **WINHTTP \_ OPTION CONNECT \_ \_ RETRIES** beträgt fünf Versuche.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CONNECT_TIMEOUT"></span><span id="winhttp_option_connect_timeout"></span>**WINHTTP \_ OPTION \_ CONNECT \_ TIMEOUT**
</dt> <dd> <dl> <dt>



Legt einen ganzzahligen Wert ohne Vorzeichen fest, der den Time out-Wert in Millisekunden enthält, oder ruft diesen ab. Wenn Sie diese Option auf infinite (0xFFFFFFFF) festlegen, wird dieser Timer deaktiviert.

Wenn eine TCP-Verbindungsanforderung länger als dieser Time out-Wert dauert, wird die Anforderung abgebrochen. Das Standardtimeout beträgt 60 Sekunden. Wenn Sie versuchen, eine Verbindung mit mehreren IP-Adressen für einen einzelnen Host (einen mehrfach vernetzten Host) herzustellen, gilt das Timeoutlimit für jede einzelne Verbindung.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CONNECTION_INFO"></span><span id="winhttp_option_connection_info"></span>**VERBINDUNGSINFORMATIONEN ZUR \_ WINHTTP-OPTION \_ \_**
</dt> <dd> <dl> <dt>



Ruft die Quell- und Ziel-IP-Adresse sowie den Port der Anforderung ab, die die Antwort generiert hat, wenn [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) zurückgegeben wird. Die Anwendung ruft [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) mit der OPTION **WINHTTP \_ OPTION CONNECTION \_ \_ INFO** auf und stellt die [**WINHTTP CONNECTION \_ \_ INFO-Struktur**](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info) im *lpBuffer-Parameter* bereit. Weitere Informationen finden Sie unter **WINHTTP \_ CONNECTION \_ INFO**.

**Windows Server 2003 mit SP1 und Windows XP mit SP2:** Dieses Flag ist veraltet.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CONNECTION_STATS_V0"></span><span id="winhttp_option_connection_stats_v0"></span>**WINHTTP \_ OPTION \_ CONNECTION \_ STATS \_ V0**
</dt> <dd> <dl> <dt>



Leitet die [**TCP \_ INFO \_ v0-Struktur**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0) für die zugrunde liegende Verbindung ab, die von der Anforderung verwendet wird. Die zurückgegebene Struktur kann Statistiken aus früheren Anforderungen enthalten, die über dieselbe Verbindung gesendet wurden.

> [!Note]
> Diese Option wurde durch **WINHTTP \_ OPTION \_ CONNECTION \_ STATS \_ V1** ersetzt.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CONNECTION_STATS_V1"></span><span id="winhttp_option_connection_stats_v1"></span>**WINHTTP \_ OPTION \_ CONNECTION \_ STATS \_ V1**
</dt> <dd> <dl> <dt>



Leitet die [**TCP \_ INFO \_ v1-Struktur**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1) für die zugrunde liegende Verbindung ab, die von der Anforderung verwendet wird. Die zurückgegebene Struktur kann Statistiken aus früheren Anforderungen enthalten, die über dieselbe Verbindung gesendet wurden.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CONTEXT_VALUE"></span><span id="winhttp_option_context_value"></span>**\_ \_ WINHTTP-OPTIONSKONTEXTWERT \_**
</dt> <dd> <dl> <dt>



Legt einen **\_ DWORD-PTR** fest oder ruft diesen ab, der einen Zeiger auf den Kontextwert enthält, der diesem [HINTERNET-Handle](hinternet-handles-in-winhttp.md) zugeordnet ist. Der im Puffer gespeicherte Wert wird verwendet, und dem **Optionsflag WINHTTP \_ OPTION CONTEXT \_ \_ VALUE** wird ein neuer Wert zugewiesen.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_DECOMPRESSION"></span><span id="winhttp_option_decompression"></span>**WINHTTP \_ OPTION \_ DEKOMPRIMIERUNG**
</dt> <dd> <dl> <dt>



Legt ein DWORD mit Flags fest, die bestimmen, ob WinHTTP Antwortkörper mit komprimierten Content-Encodings automatisch dekomprimiert. WinHTTP legt auch einen geeigneten Accept-Encoding Header fest, der alle vom Aufrufer bereitgestellten überschreibt. Diese Werte werden unterstützt:

| Begriff | BESCHREIBUNG |
|-|-|
| <span id="WINHTTP_DECOMPRESSION_FLAG_GZIP"></span><span id="winhttp_decompression_flag_gzip"></span>WINHTTP \_ DECOMPRESSION \_ FLAG \_ GZIP | Dekomprimieren von Content-Encoding: gzip-Antworten. |
| <span id="WINHTTP_DECOMPRESSION_FLAG_DEFLATE"></span><span id="winhttp_decompression_flag_deflate"></span>WINHTTP \_ DECOMPRESSION \_ FLAG \_ DEFLATE | Dekomprimieren der Inhaltscodierung: Deflate-Antworten. |
| <span id="WINHTTP_DECOMPRESSION_FLAG_ALL"></span><span id="winhttp_decompression_flag_all"></span>WINHTTP \_ DECOMPRESSION \_ FLAG \_ ALL | Dekomprimieren Sie Antworten mit jeder unterstützten Inhaltscodierung. |

Standardmäßig übermittelt WinHTTP komprimierte Antworten unverändert an den Aufrufer.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_DISABLE_CERT_CHAIN_BUILDING"></span><span id="winhttp_option_disable_cert_chain_building"></span>**WINHTTP \_ OPTION \_ DISABLE \_ CERT \_ CHAIN \_ BUILDING**
</dt> <dd> <dl> <dt>


Wenn Sie diese Option auf einem WinHttp-Sitzungshandle festlegen, können Sie aktivieren/deaktivieren, ob die Serverzertifikatkette erstellt wurde.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_DISABLE_FEATURE"></span><span id="winhttp_option_disable_feature"></span>**WINHTTP \_ OPTION \_ DISABLE \_ FEATURE**
</dt> <dd> <dl> <dt>



Legt einen ganzzahligen Wert ohne Vorzeichen fest, der angibt, welche Features mit einem oder mehreren der folgenden Flags deaktiviert werden. Beachten Sie, dass dieses Feature nur bei Anforderungshandles an [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) übergeben werden sollte, nachdem das Anforderungshandle mit [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)erstellt wurde und bevor die Anforderung mit [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)gesendet wird.

| Begriff | BESCHREIBUNG |
|-|-|
| <span id="WINHTTP_DISABLE_AUTHENTICATION"></span><span id="winhttp_disable_authentication"></span>WINHTTP \_ DISABLE \_ AUTHENTICATION | Die automatische Authentifizierung ist deaktiviert. |
| <span id="WINHTTP_DISABLE_COOKIES"></span><span id="winhttp_disable_cookies"></span>WINHTTP \_ DISABLE \_ COOKIES | Das automatische Hinzufügen von Cookieheadern zu Anforderungen ist deaktiviert. Außerdem werden zurückgegebene Cookies nicht automatisch zur Cookiedatenbank hinzugefügt. Das Deaktivieren von Cookies kann zu einer schlechten Leistung bei der Passport-Authentifizierung führen. |
| <span id="WINHTTP_DISABLE_KEEP_ALIVE"></span><span id="winhttp_disable_keep_alive"></span>WINHTTP \_ DISABLE \_ KEEP \_ ALIVE | Deaktiviert die Keep-Alive-Semantik für die Verbindung. Keep-Alive-Semantik ist für MSN, NTLM und andere Authentifizierungstypen erforderlich. |
| <span id="WINHTTP_DISABLE_REDIRECTS"></span><span id="winhttp_disable_redirects"></span>WINHTTP \_ DISABLE \_ REDIRECTS | Die automatische Umleitung ist deaktiviert, wenn Anforderungen mit [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)gesendet werden. Wenn die automatische Umleitung deaktiviert ist, muss eine Anwendung eine Rückruffunktion registrieren, damit die Passport-Authentifizierung erfolgreich ist. |


</dl> </dd> <dt>

<span id="WINHTTP_OPTION_DISABLE_SECURE_PROTOCOL_FALLBACK"></span><span id="winhttp_option_disable_secure_protocol_fallback"></span>**\_WINHTTP-OPTION \_ DISABLE SECURE \_ PROTOCOL \_ \_ FALLBACK**
</dt> <dd> <dl> <dt>



Verhindert, dass WinHTTP eine Verbindung mit einer niedrigeren Version des Sicherheitsprotokolls erneut versucht, wenn die anfängliche Protokollaushandlung fehlschlägt.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_DISABLE_STREAM_QUEUE"></span><span id="winhttp_option_disable_stream_queue"></span>**\_WINHTTP-OPTION \_ : DEAKTIVIEREN DER \_ \_ STREAMWARTESCHLANGE**
</dt> <dd> <dl> <dt>



Ermöglicht es neuen Anforderungen, eine zusätzliche HTTP/2-Verbindung zu öffnen, wenn der maximale Grenzwert für gleichzeitige Datenströme erreicht ist, anstatt auf den nächsten verfügbaren Stream auf einer vorhandenen Verbindung zu warten.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_ENABLE_FEATURE"></span><span id="winhttp_option_enable_feature"></span>**WINHTTP \_ OPTION \_ ENABLE \_ FEATURE**
</dt> <dd> <dl> <dt>



Legt einen ganzzahligen Wert ohne Vorzeichen fest, der die derzeit aktivierten Features angibt. Kann einer der folgenden Werte sein.

| Begriff | BESCHREIBUNG |
|-|-|
| <span id="WINHTTP_ENABLE_SSL_REVERT_IMPERSONATION"></span><span id="winhttp_enable_ssl_revert_impersonation"></span>WINHTTP \_ ENABLE \_ SSL \_ REVERT \_ IMPERSONATION | Wenn diese Option aktiviert ist, stellt WinHTTP den Clientidentitätswechsel für die Dauer der Authentifizierungsvorgänge für SSL-Zertifikate vorübergehend wieder her. Dieser Wert kann nur für das Sitzungshandle festgelegt werden. |
| <span id="WINHTTP_ENABLE_SSL_REVOCATION"></span><span id="winhttp_enable_ssl_revocation"></span>WINHTTP \_ ENABLE \_ SSL \_ REVOCATION | Wenn diese Option aktiviert ist, lässt WinHTTP SSL-Sperrung zu. Dieser Wert kann nur für das Anforderungshandle festgelegt werden. |


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_ENABLE_HTTP_PROTOCOL"></span><span id="winhttp_option_enable_http_protocol"></span>**\_WINHTTP-OPTION: \_ AKTIVIEREN DES \_ \_ HTTP-PROTOKOLLS**
</dt> <dd> <dl> <dt>



Legt eine DWORD-Bitmaske mit akzeptablen erweiterten HTTP-Versionen fest. Mögliche Werte:

| Begriff | BESCHREIBUNG |
|-|-|
| <span id="WINHTTP_PROTOCOL_FLAG_HTTP2"></span><span id="winhttp_protocol_flag_http2"></span>\_WINHTTP-PROTOKOLLFLAG \_ \_ HTTP2 (0x1) | Aktiviert HTTP/2 für die Anforderung. |
| None (0x0) | Schränkt die Anforderung auf HTTP/1.1 und früher ein. |

Legacyversionen von HTTP (1.1 und früher) können mit dieser Option nicht deaktiviert werden. Der Standardwert ist 0x0.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_ENABLE_HTTP2_PLUS_CLIENT_CERT"></span><span id="winhttp_option_enable_http2_plus_client_cert"></span>**WINHTTP \_ OPTION \_ ENABLE \_ HTTP2 \_ PLUS \_ CLIENT \_ CERT**
</dt> <dd> <dl> <dt>


Diese Option kann für ein WinHttp-Sitzungshandle festgelegt werden, damit WinHttp den vom Aufrufer bereitgestellten Clientzertifikatkontext verwenden kann, wenn HTTP/2 verwendet wird.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_ENABLETRACING"></span><span id="winhttp_option_enabletracing"></span>**\_WINHTTP-OPTION \_ ENABLETRACING**
</dt> <dd> <dl> <dt>



Legt einen **BOOL-Wert** fest, der angibt, ob die Ablaufverfolgung derzeit aktiviert ist. Weitere Informationen zur Ablaufverfolgungsfunktion in WinHTTP finden Sie unter [WinHTTP Trace Facility](winhttptracecfg-exe--a-trace-configuration-tool.md). Diese Option kann nur für ein **NULL** **HINTERNET-Handle** festgelegt werden.


</dt> </dl> </dd>

<dt>

<span id="WINHTTP_OPTION_ENCODE_EXTRA"></span><span id="winhttp_option_encode_extra"></span>**WINHTTP \_ OPTION \_ ENCODE \_ EXTRA**
</dt> <dd> <dl> <dt>



Aktiviert die URL-Prozentcodierung für Pfad und Abfragezeichenfolge.

Alternativ können Sie vor dem Aufruf von WinHttp prozentweise codieren.

</dt> </dl> </dd>

<dt>

<span id="WINHTTP_OPTION_EXPIRE_CONNECTION"></span><span id="winhttp_option_expire_connection"></span>**\_WINHTTP-OPTION \_ LÄUFT VERBINDUNG AB \_**
</dt> <dd> <dl> <dt>



Diese Option kann nur für ein Anforderungshandle festgelegt werden, das noch aktiv ist (Senden oder Empfangen). Wenn Sie diese Option festlegen, weist WinHttp an, die Verarbeitung von Anforderungen für die Verbindung zu beenden, die dem übergebenen Anforderungshandle zugeordnet ist. Die Verbindung wird geschlossen, nachdem das Anforderungshandle, mit dem diese Option aufgerufen wird, abgeschlossen wurde. Diese Option verwendet keine Parameter.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_EXTENDED_ERROR"></span><span id="winhttp_option_extended_error"></span>**\_ \_ ERWEITERTER \_ WINHTTP-OPTION-FEHLER**
</dt> <dd> <dl> <dt>



Ruft einen ganzzahligen Wert ohne Vorzeichen ab, der einen Microsoft Windows Sockets-Fehlercode enthält, der den ERROR WINHTTP-Fehlermeldungen zugeordnet wurde, die \_ \_ \* zuletzt in diesem Threadkontext zurückgegeben wurden. Sie können **NULL** als Handlewert übergeben.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_FIRST_AVAILABLE_CONNECTION"></span><span id="winhttp_option_first_available_connection"></span>**WINHTTP \_ OPTION \_ FIRST \_ AVAILABLE \_ CONNECTION**
</dt> <dd> <dl> <dt>


Wenn WinHttp eine Anforderung sendet und keine Verbindungen für die Anforderung verfügbar sind, versucht WinHttp standardmäßig, eine neue Verbindung herzustellen, und die Anforderung wird an diese neue Verbindung gebunden. Wenn Sie diese Option festlegen, wird eine solche Anforderung stattdessen für die erste verfügbare Verbindung und nicht unbedingt für die hergestellte Verbindung bereitgestellt.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_GLOBAL_PROXY_CREDS"></span><span id="winhttp_option_global_proxy_creds"></span>**WINHTTP \_ OPTION \_ GLOBAL \_ PROXY \_ CREDS**
</dt> <dd> <dl> <dt>



Verwendet einen Zeiger auf eine [**WINHTTP \_ CREDS \_ EX-Struktur,**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) wobei der *hInternet-Funktionsparameter* auf **NULL** festgelegt ist. Diese Option erfordert den Registrierungsschlüssel **HKLM \\ Software Microsoft \\ Windows \\ \\ CurrentVersion Internet \\ Einstellungen! ShareCredsWithWinHttp**. Wenn dieser Registrierungsschlüssel nicht festgelegt ist, gibt WinHTTP den Fehler **ERROR \_ WINHTTP \_ INVALID \_ OPTION** zurück. Dieser Registrierungsschlüssel ist standardmäßig nicht vorhanden. Wenn sie festgelegt ist, sendet WinINet Anmeldeinformationen an WinHTTP. Wenn WinHttp eine Authentifizierungsaufforderung erhält und keine Anmeldeinformationen für das aktuelle Handle festgelegt sind, werden die von WinINet bereitgestellten Anmeldeinformationen verwendet. Um Serveranmeldeinformationen zusätzlich zu Proxyanmeldeinformationen freizugeben, müssen Benutzer **WINHTTP \_ OPTION USE GLOBAL SERVER \_ \_ \_ \_ CREDENTIALS** festlegen.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_GLOBAL_SERVER_CREDS"></span><span id="winhttp_option_global_server_creds"></span>**WINHTTP \_ OPTION \_ GLOBAL \_ SERVER \_ CREDS**
</dt> <dd> <dl> <dt>



Verwendet einen Zeiger auf eine [**WINHTTP \_ CREDS \_ EX-Struktur,**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) wobei der *hInternet-Funktionsparameter* auf **NULL** festgelegt ist. Diese Option erfordert den Registrierungsschlüssel **HKLM \\ Software Microsoft \\ Windows \\ \\ CurrentVersion Internet \\ Einstellungen! ShareCredsWithWinHttp**. Wenn dieser Registrierungsschlüssel nicht festgelegt ist, gibt WinHTTP den Fehler **ERROR \_ WINHTTP \_ INVALID \_ OPTION** zurück. Dieser Registrierungsschlüssel ist standardmäßig nicht vorhanden. Wenn sie festgelegt ist, sendet WinINet Anmeldeinformationen an WinHTTP. Wenn WinHttp eine Authentifizierungsaufforderung erhält und keine Anmeldeinformationen für das aktuelle Handle festgelegt sind, werden die von WinINet bereitgestellten Anmeldeinformationen verwendet. Um Serveranmeldeinformationen zusätzlich zu Proxyanmeldeinformationen freizugeben, müssen Benutzer **WINHTTP \_ OPTION USE GLOBAL SERVER \_ \_ \_ \_ CREDENTIALS** festlegen.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_HANDLE_TYPE"></span><span id="winhttp_option_handle_type"></span>**TYP DES \_ WINHTTP-OPTIONSHANDLE \_ \_**
</dt> <dd> <dl> <dt>



Ruft einen ganzzahligen Wert ohne Vorzeichen ab, der den Typ des übergebenen [HINTERNET-Handles](hinternet-handles-in-winhttp.md) enthält. Einer der folgenden Werte kann zurückgegeben werden:

| Begriff | BESCHREIBUNG |
|-|-|
| <span id="WINHTTP_HANDLE_TYPE_CONNECT"></span><span id="winhttp_handle_type_connect"></span>\_WINHTTP-HANDLETYP \_ \_ CONNECT | Das Handle ist ein Verbindungshandle. |
| <span id="WINHTTP_HANDLE_TYPE_REQUEST"></span><span id="winhttp_handle_type_request"></span>\_ \_ WINHTTP-HANDLETYPANFORDERUNG \_ | Das Handle ist ein Anforderungshandle. |
| <span id="WINHTTP_HANDLE_TYPE_SESSION"></span><span id="winhttp_handle_type_session"></span>\_ \_ WINHTTP-HANDLETYPSITZUNG \_ | Das Handle ist ein Sitzungshandle. |


</dl> </dd> <dt>

<span id="WINHTTP_OPTION_HTTP_PROTOCOL_REQUIRED"></span><span id="winhttp_option_http_protocol_required"></span>**WINHTTP \_ OPTION HTTP PROTOCOL \_ \_ \_ ERFORDERLICH**
</dt> <dd> <dl> <dt>



Verhindert, dass andere Protokollversionen als die von **WINHTTP \_ OPTION ENABLE HTTP \_ \_ \_ PROTOCOL** aktivierten Protokollversionen für die Anforderung verwendet werden.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_HTTP_PROTOCOL_USED"></span><span id="winhttp_option_http_protocol_used"></span>**VERWENDETES \_ \_ WINHTTP-OPTION-HTTP-PROTOKOLL \_ \_**
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

<span id="WINHTTP_OPTION_IPV6_FAST_FALLBACK"></span><span id="winhttp_option_ipv6_fast_fallback"></span>**\_WINHTTP-OPTION \_ IPV6 \_ FAST \_ FALLBACK**
</dt> <dd> <dl> <dt>



Aktiviert schnelles IPv6-Fallback (Brillenbrillen) für die Verbindung. Dieses Verhalten ähnelt dem In RFC [6555](https://tools.ietf.org/html/rfc6555) beschriebenen Verhalten von Happy Eyeballs zur Verbesserung der Verbindungszeiten in Netzwerken, in denen IPv6 unzuverlässig ist.
- Wenn sowohl IPv6- als auch IPv4-Adressen für einen bestimmten Host aufgelöst werden, beginnt WinHttp mit dem Herstellen einer Verbindung mit der ersten aufgelösten IPv6-Adresse mit einem kurzen Timeout (300 ms).
- Sollte diese Verbindung fehlschlagen, versucht WinHttp, eine Verbindung mit der ersten aufgelösten IPv4-Adresse mit dem Standard-Timeout herzustellen.
- Sollte bei der zweiten Verbindung ein Fehler auftäussen, wird von WinHttp die erste aufgelöste IPv6-Adresse mit dem Standard-Timeout erneut verwendet.
- Sollte bei der dritten Verbindung ein Fehler auftäussen, wird winHttp auf das Standardverhalten für alle verbleibenden Adressen zurückverwendet und versucht, eine Verbindung mit jeder Adresse mit dem Standard-Timeout herzustellen, bis eine Verbindung hergestellt wird oder keine Adressen mehr bestehen.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_IS_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_is_proxy_connect_response"></span>**\_WINHTTP-OPTION \_ IST PROXY \_ \_ \_ CONNECT-ANTWORT**
</dt> <dd> <dl> <dt>



Ruft ab, ob ein Proxy return Verbinden Response abgerufen werden kann.


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

<span id="WINHTTP_OPTION_MAX_HTTP_STATUS_CONTINUE"></span><span id="winhttp_option_max_http_status_continue"></span>**WINHTTP-OPTION \_ \_ \_ MAX. \_ HTTP-STATUS \_ CONTINUE**
</dt> <dd> <dl> <dt>



Die maximale Anzahl von 100-199 Statuscodeantworten, die ignoriert wurden, bevor der endgültige Statuscode an den WinHTTP-Client zurücksendet. Informationsstatuscodes 100-199 können vom Server vor dem endgültigen Statuscode gesendet werden und werden in der Spezifikation für HTTP/1.1 beschrieben (weitere Informationen finden Sie unter [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt)). Der Standardwert ist 10.

**Windows XP mit SP1 und Windows 2000 mit SP3:** Dieses Flag ist veraltet.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_MAX_RESPONSE_DRAIN_SIZE"></span><span id="winhttp_option_max_response_drain_size"></span>**WINHTTP \_ OPTION \_ MAX \_ RESPONSE \_ DRAIN \_ SIZE**
</dt> <dd> <dl> <dt>



Eine Grenze für die Menge der Daten, die aus Antworten entleert werden, um eine Verbindung wiederzuverwenden, die in Bytes angegeben ist. Der Standardwert ist 1 MB.

**Windows XP mit SP1 und Windows 2000 mit SP3:** Dieses Flag ist veraltet.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_MAX_RESPONSE_HEADER_SIZE"></span><span id="winhttp_option_max_response_header_size"></span>**WINHTTP-OPTION \_ \_ \_ MAX. GRÖßE DES \_ \_ ANTWORTHEADERS**
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

<span id="WINHTTP_OPTION_PASSPORT_SIGN_OUT"></span><span id="winhttp_option_passport_sign_out"></span>**\_WINHTTP-OPTION \_ \_ \_ PASSPORT-ABMELDEN**
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

<span id="WINHTTP_OPTION_PROXY_USERNAME"></span><span id="winhttp_option_proxy_username"></span>**\_ \_ WINHTTP-OPTIONSPROXYBENUTZERNAME \_**
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

<span id="WINHTTP_OPTION_RECEIVE_RESPONSE_TIMEOUT"></span><span id="winhttp_option_receive_response_timeout"></span>**WINHTTP-OPTION \_ \_ \_ \_ EMPFANGSANTWORTZEITÜBERSCHREITUNG**
</dt> <dd> <dl> <dt>



Legt einen ganzzahligen Wert ohne Vorzeichen fest, der den Timeoutwert in Millisekunden enthält, um auf den Empfang aller Antwortheader für eine Anforderung zu warten, oder ruft diesen wert ab. Wenn WinHTTP nicht alle Header innerhalb dieses Timeoutzeitraums empfangen kann, wird die Anforderung abgebrochen. Der Standardwert für das Timeout beträgt 90 Sekunden.

Dieses Timeout wird nur überprüft, wenn Daten vom Socket empfangen werden. Wenn das Timeout abläuft, wird die Clientanwendung daher erst benachrichtigt, wenn weitere Daten vom Server eintreffen. Wenn keine Daten vom Server eintreffen, kann die Verzögerung zwischen dem Ablauf des Timeouts und der Benachrichtigung der Clientanwendung so groß sein wie der Timeoutwert, der mithilfe des *dwReceiveTimeout-Parameters* der [**WinHttpSetTimeouts-Funktion**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts) festgelegt wurde.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_RECEIVE_TIMEOUT"></span><span id="winhttp_option_receive_timeout"></span>**\_EMPFANGSZEITÜBERSCHREITUNG DER WINHTTP-OPTION \_ \_**
</dt> <dd> <dl> <dt>



Legt einen ganzzahligen Wert ohne Vorzeichen fest, der den Time out-Wert in Millisekunden enthält, um eine Teilantwort auf eine Anforderung zu empfangen oder einige Daten zu lesen, oder ruft diesen wert ab. Wenn die Antwort länger als dieser Time out-Wert dauert, wird die Anforderung abgebrochen. Der Standard-Timeoutwert beträgt 30 Sekunden.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_REDIRECT_POLICY"></span><span id="winhttp_option_redirect_policy"></span>**UMLEITUNGSRICHTLINIE \_ FÜR WINHTTP-OPTION \_ \_**
</dt> <dd> <dl> <dt>



Legt das Verhalten von WinHTTP in Bezug auf die Behandlung eines 30-fachen HTTP-Umleitungsstatuscodes fest. Diese Option kann für ein Sitzungs- oder Anforderungshand handle auf einen der folgenden Werte festgelegt werden:

| Begriff | BESCHREIBUNG |
|-|-|
| <span id="WINHTTP_OPTION_REDIRECT_POLICY_ALWAYS"></span><span id="winhttp_option_redirect_policy_always"></span>RICHTLINIE FÜR DIE UMLEITUNG \_ DER WINHTTP-OPTION \_ \_ \_ IMMER | Alle Umleitungen werden automatisch befolgt. |
| <span id="WINHTTP_OPTION_REDIRECT_POLICY_DISALLOW_HTTPS_TO_HTTP"></span><span id="winhttp_option_redirect_policy_disallow_https_to_http"></span>UMLEITUNGSRICHTLINIE \_ FÜR \_ WINHTTP-OPTION: \_ HTTPS ZU HTTP NICHT \_ \_ \_ \_ ZU | Alle Umleitungen werden befolgt, mit Ausnahme der Umleitungen, die von einer sicheren URL (https) zu einer unsicheren URL (HTTP) stammen. Dies ist die Standardeinstellung. |
| <span id="WINHTTP_OPTION_REDIRECT_POLICY_NEVER"></span><span id="winhttp_option_redirect_policy_never"></span>UMLEITUNGSRICHTLINIE \_ FÜR WINHTTP-OPTION \_ \_ \_ NIE | Umleitungen werden nie befolgt. Der 30-fache Status wird an die Anwendung zurückgegeben. |


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_REJECT_USERPWD_IN_URL"></span><span id="winhttp_option_reject_userpwd_in_url"></span>**\_WINHTTP-OPTION \_ BENUTZER IN URL \_ \_ \_ ABLEHNENPWD**
</dt> <dd> <dl> <dt>



Lehnt URLs ab, die einen Benutzernamen und ein Kennwort enthalten. Diese Option lehnt auch URLs ab, die *die Semantik username:password* enthalten, auch wenn kein Benutzername oder Kein Kennwort angegeben ist. Beispielsweise würde " u:p@hostname ", " :@hostname ", " u:@hostname ", " " und " :p@hostname " alle als ungültig gekennzeichnet werden. Wenn eine ungültige URL an die Funktion übergeben wird, wird [ERROR \_ WINHTTP \_ INVALID URL \_ zurückgegeben.](error-messages.md) Standardmäßig ist diese Option deaktiviert.


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


Diese Option kann für ein WinHttp-Anforderungshand handle festgelegt werden, bevor sie gesendet wurde. Wenn festgelegt, verwendet WinHttp die vom Aufrufer bereitgestellte Zeichenfolge als Hostnamen für die DNS-Auflösung.



</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_RESOLVE_TIMEOUT"></span><span id="winhttp_option_resolve_timeout"></span>**WINHTTP-OPTION \_ \_ \_ TIMEOUT AUFLÖSEN**
</dt> <dd> <dl> <dt>



Legt einen ganzzahligen Wert ohne Vorzeichen fest, der den Time out-Wert in Millisekunden enthält, um einen Hostnamen aufzulösen, oder ruft diesen wert ab. Der Standardwert für das Timeout ist **INFINITE.** Wenn ein nicht standardmäßiger Wert angegeben wird, verursacht dies einen Mehraufwand von einer Threaderstellung pro Namensauflösung.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SECURE_PROTOCOLS"></span><span id="winhttp_option_secure_protocols"></span>**SICHERE PROTOKOLLE \_ DER WINHTTP-OPTION \_ \_**
</dt> <dd> <dl> <dt>



Legt einen ganzzahligen Wert ohne Vorzeichen fest, der angibt, welche sicheren Protokolle zulässig sind. Standardmäßig sind nur SSL3 und TLS1 in Windows 7 und Windows 8. Standardmäßig sind nur SSL3, TLS1.0, TLS1.1 und TLS1.2 in Windows 8.1 und Windows 10. Der Wert kann eine Kombination aus mindestens einem der folgenden Werte sein.

| Begriff | BESCHREIBUNG |
|-|-|
| <span id="WINHTTP_FLAG_SECURE_PROTOCOL_ALL"></span><span id="winhttp_flag_secure_protocol_all"></span>WINHTTP \_ FLAG \_ SECURE \_ PROTOCOL \_ ALL | Die protokolle Secure Sockets Layer (SSL) 2.0, SSL 3.0 und Transport Layer Security (TLS) 1.0 können verwendet werden. |
| <span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL2"></span><span id="winhttp_flag_secure_protocol_ssl2"></span>WINHTTP-FLAG \_ \_ SECURE PROTOCOL \_ \_ SSL2 | Das SSL 2.0-Protokoll kann verwendet werden. |
| <span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL3"></span><span id="winhttp_flag_secure_protocol_ssl3"></span>WINHTTP-FLAG \_ \_ SECURE PROTOCOL \_ \_ SSL3 | Das SSL 3.0-Protokoll kann verwendet werden. |
| <span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1"></span><span id="winhttp_flag_secure_protocol_tls1"></span>WINHTTP-FLAG \_ \_ SECURE PROTOCOL \_ \_ TLS1 | Das TLS 1.0-Protokoll kann verwendet werden. |
| <span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_1"></span><span id="winhttp_flag_secure_protocol_tls1_1"></span>WINHTTP FLAG \_ \_ SECURE PROTOCOL \_ \_ TLS1 \_ 1 | Das TLS 1.1-Protokoll kann verwendet werden. |
| <span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_2"></span><span id="winhttp_flag_secure_protocol_tls1_2"></span>WINHTTP FLAG \_ \_ SECURE PROTOCOL \_ \_ TLS1 \_ 2 | Das TLS 1.2-Protokoll kann verwendet werden. |


</dl> </dd> <dt>

<span id="WINHTTP_OPTION_SECURITY_CERTIFICATE_STRUCT"></span><span id="winhttp_option_security_certificate_struct"></span>**\_SICHERHEITSZERTIFIKATSTRUKTUR DER \_ \_ \_ WINHTTP-OPTION**
</dt> <dd> <dl> <dt>



Ruft das Zertifikat für einen SSL/TLS-Server in der [**WINHTTP \_ CERTIFICATE \_ INFO-Struktur**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) ab. Die Anwendung muss die **Member lpszSubjectInfo** und **lpszIssuerInfo mit** [**LocalFree frei geben.**](/windows/desktop/api/winbase/nf-winbase-localfree)


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SECURITY_FLAGS"></span><span id="winhttp_option_security_flags"></span>**\_SICHERHEITSFLAGS FÜR DIE WINHTTP-OPTION \_ \_**
</dt> <dd> <dl> <dt>



Legt einen ganzzahligen Wert ohne Vorzeichen fest, der die Sicherheitsflags für ein Handle enthält, oder ruft diesen wert ab. Dabei kann es sich um eine Kombination dieser Werte handelt:

| Begriff | BESCHREIBUNG |
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



Ruft einen ganzzahligen Wert ohne Vorzeichen ab, der die Verschlüsselungsstärke des Verschlüsselungsschlüssels enthält. Eine größere Zahl weist auf eine stärkere Verschlüsselung der Verschlüsselung mit Verschlüsselungsstärke hin.


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
> Die Übergabe dieser  Option und eines NULL-Werts für *lpBuffer* an [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) gibt ERROR INSUFFICIENT BUFFER und die erforderliche Bytegröße für den Puffer im \_ \_ *lpdwBufferLength-Parameter* zurück. Dieser zurückgegebene Puffergrößenwert kann in einem nachfolgenden Aufruf zur Abfrage des Kanalbindungstokens übergeben werden. Diese Schritte sind erforderlich, wenn Sie WINHTTP CALLBACK STATUS REQUEST behandeln, wenn Sie Anforderungsheader basierend auf dem \_ \_ \_ Kanalbindungstoken ändern möchten. Beachten Sie, Windows XP und Vista das Ändern von Anforderungsheadern während dieses Rückrufs nicht unterstützen.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SERVER_CERT_CHAIN_CONTEXT"></span><span id="winhttp_option_server_cert_chain_context"></span>**WINHTTP \_ OPTION \_ SERVER \_ CERT \_ CHAIN \_ CONTEXT**
</dt> <dd> <dl> <dt>



Ruft den Kontext der Serverzertifizierungskette ab. **WINHTTP \_ OPTION \_ SERVER \_ CERT CHAIN \_ \_ CONTEXT** kann übergeben werden, um einen duplizierten Zeiger auf den **CERT CHAIN \_ \_ CONTEXT** für eine Serverzertifikatkette zu erhalten, die während einer ausgehandelten SSL-Verbindung empfangen wurde. Der Client muss [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) für den zurückgegebenen PCCERT \_ CONTEXT-Zeiger aufrufen, der in den Puffer gefüllt wird.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SERVER_CERT_CONTEXT"></span><span id="winhttp_option_server_cert_context"></span>**WINHTTP \_ OPTION \_ SERVER \_ CERT \_ CONTEXT**
</dt> <dd> <dl> <dt>



Ruft den Serverzertifizierungskontext ab. **WINHTTP \_ OPTION \_ SERVER \_ CERT \_ CONTEXT** kann übergeben werden, um einen duplizierten Zeiger auf den [**CERT CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) für ein Serverzertifikat abzurufen, das während einer ausgehandelten SSL-Verbindung empfangen wurde. Der Client muss [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) für den zurückgegebenen PCCERT \_ CONTEXT-Zeiger aufrufen, der in den Puffer gefüllt wird.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SERVER_SPN_USED"></span><span id="winhttp_option_server_spn_used"></span>**VERWENDETER \_ \_ WINHTTP-OPTIONSERVER-SPN \_ \_**
</dt> <dd> <dl> <dt>



Ruft den Serverprinzipalnamen ab, den WinHTTP während der Authentifizierung für SSPI bereitgestellt hat. Dieser Zeichenfolgenwert kann nach einem Authentifizierungsfehler an [**SspiPromptForCredentials**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) übergeben werden.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SPN"></span><span id="winhttp_option_spn"></span>**WINHTTP \_ OPTION \_ SPN**
</dt> <dd> <dl> <dt>



Schließt die Serverportnummer ein oder entfernt sie, wenn der SPN (Dienstprinzipalname) für die Kerberos- oder Negotiate Kerberos-Authentifizierung erstellt wird. Dieses Flag ist einer der folgenden Werte:

| Begriff | BESCHREIBUNG |
|-|-|
| <span id="WINHTTP_DISABLE_SPN_SERVER_PORT"></span><span id="winhttp_disable_spn_server_port"></span>WINHTTP \_ \_ \_ SPN-SERVERPORT DEAKTIVIEREN \_ | Entfernt die Serverportnummer. |
| <span id="WINHTTP_ENABLE_SPN_SERVER_PORT"></span><span id="winhttp_enable_spn_server_port"></span>WINHTTP \_ \_ \_ SPN-SERVERPORT AKTIVIEREN \_ | Enthält die Serverportnummer. |


</dl> </dd> <dt>

<span id="WINHTTP_OPTION_STREAM_ERROR_CODE"></span><span id="winhttp_option_stream_error_code"></span>**WINHTTP \_ OPTION \_ STREAM \_ ERROR \_ CODE**
</dt> <dd> <dl> <dt>


Diese Option kann für ein WinHttp-Anforderungshandle abgefragt werden und gibt den Fehlercode zurück, der durch einen RST_STREAM Frame angegeben wird, der in einem HTTP-Stream empfangen wurde.



</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_TCP_FAST_OPEN"></span><span id="winhttp_option_tcp_fast_open"></span>**WINHTTP \_ OPTION TCP FAST \_ \_ \_ OPEN**
</dt> <dd> <dl> <dt>



Aktiviert TCP Fast Open für die Verbindung.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_TCP_KEEPALIVE"></span><span id="winhttp_option_tcp_keepalive"></span>**\_WINHTTP-OPTION \_ TCP \_ KEEPALIVE**
</dt> <dd> <dl> <dt>



Diese Option kann für ein WinHttp-Sitzungshandle festgelegt werden, um das TCP-Keep-Alive-Verhalten für den zugrunde liegenden Socket zu aktivieren. Übernimmt eine [**\_ tcp-Keepalive-Struktur.**](/windows/win32/winsock/sio-keepalive-vals)


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_TLS_FALSE_START"></span><span id="winhttp_option_tls_false_start"></span>**WINHTTP \_ OPTION \_ TLS \_ FALSE \_ START**
</dt> <dd> <dl> <dt>



Aktiviert TLS False Start für die Verbindung.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_TLS_PROTOCOL_INSECURE_FALLBACK"></span><span id="winhttp_option_tls_protocol_insecure_fallback"></span>**WINHTTP \_ OPTION \_ TLS \_ PROTOCOL \_ INSECURE \_ FALLBACK**
</dt> <dd> <dl> <dt>



Diese Option kann für ein WinHttp-Sitzungshandle festgelegt werden, um zu steuern, ob ein Fallback auf TLS 1.0 zulässig ist, wenn ein TLS-Handshakefehler mit einer neueren Protokollversion vorliegt.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_UNLOAD_NOTIFY_EVENT"></span><span id="winhttp_option_unload_notify_event"></span>**WINHTTP \_ OPTION \_ UNLOAD \_ NOTIFY \_ EVENT**
</dt> <dd> <dl> <dt>



Nimmt ein Ereignis an, das festgelegt wird, wenn der letzte Rückruf für eine bestimmte Sitzung abgeschlossen wurde. Dieses Flag muss für ein Sitzungshandle verwendet werden. Das Ereignis kann erst geschlossen werden, nachdem es von WinHTTP festgelegt wurde.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_UNSAFE_HEADER_PARSING"></span><span id="winhttp_option_unsafe_header_parsing"></span>**WINHTTP \_ OPTION \_ UNSAFE \_ HEADER \_ PARSING**
</dt> <dd> <dl> <dt>



Diese Option ist für die interne Verwendung reserviert und sollte nicht aufgerufen werden.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_UPGRADE_TO_WEB_SOCKET"></span><span id="winhttp_option_upgrade_to_web_socket"></span>**UPGRADE DER \_ WINHTTP-OPTION \_ AUF \_ \_ \_ WEBSOCKET**
</dt> <dd> <dl> <dt>



Weist den Stapel an, einen WebSocket-Handshakeprozess mit [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)zu starten. Diese Option nimmt keine Parameter an.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_URL"></span><span id="winhttp_option_url"></span>**\_ \_ WINHTTP-OPTIONS-URL**
</dt> <dd> <dl> <dt>



Ruft einen Zeichenfolgenwert ab, der die vollständige URL einer heruntergeladenen Ressource enthält. Wenn die ursprüngliche URL zusätzliche Daten enthielt, z. B. Suchzeichenfolgen oder Anker, oder wenn der Aufruf umgeleitet wurde, unterscheidet sich die zurückgegebene URL von der ursprünglichen URL. Die Anwendung sollte einen Puffer in Bytes übergeben, der groß genug ist, um die zurückgegebene URL in wide char zu speichern.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_USE_GLOBAL_SERVER_CREDENTIALS"></span><span id="winhttp_option_use_global_server_credentials"></span>**\_WINHTTP-OPTION \_ VERWENDEN VON \_ \_ ANMELDEINFORMATIONEN FÜR GLOBALEN SERVER \_**
</dt> <dd> <dl> <dt>



Übernimmt eine **BOOL** und kann nur ein Sitzungshandle festlegen. Er wird nur an Handles weiter gegeben, die aus dem Sitzungshandle erstellt wurden, nachdem die Option festgelegt wurde. True gibt an, dass diese Option als letzte Möglichkeit die Verwendung globaler Serveranmeldeinformationen bewirkt, die von WinInet gepusht wurden. Der Standardwert für diese Option ist **FALSE.** Diese Option erfordert den Registrierungsschlüssel **HKLM \\ Software Microsoft \\ Windows \\ \\ CurrentVersion Internet \\ Einstellungen! ShareCredsWithWinHttp**. Dieser Registrierungsschlüssel ist standardmäßig nicht vorhanden. Wenn sie festgelegt ist, sendet WinINet Anmeldeinformationen an WinHTTP. Wenn WinHttp eine Authentifizierungsaufforderung erhält und keine Anmeldeinformationen für das aktuelle Handle festgelegt sind, werden die von WinINet bereitgestellten Anmeldeinformationen verwendet.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_USER_AGENT"></span><span id="winhttp_option_user_agent"></span>**WINHTTP \_ OPTION \_ USER \_ AGENT**
</dt> <dd> <dl> <dt>



Legt die Zeichenfolge des [*Benutzer-Agents*](glossary.md) auf Handles fest, die von [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) bereitgestellt und in nachfolgenden [**WinHttpSendRequest-Funktionen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) verwendet werden, oder ruft sie ab, solange sie nicht durch einen Header überschrieben wird, der von [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) oder **WinHttpSendRequest** hinzugefügt wurde. Beim Abrufen eines Benutzer-Agents sollte die Anwendung einen Puffer in Bytes übergeben, der groß genug ist, um die zurückgegebene URL in wide char zu speichern. Beim Festlegen des Benutzer-Agents entspricht die Puffergröße der Länge der Zeichenfolge in Zeichen sowie dem **NULL-Abschlusszeichen.**


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_USERNAME"></span><span id="winhttp_option_username"></span>**WINHTTP \_ OPTION \_ USERNAME**
</dt> <dd> <dl> <dt>



Legt eine Zeichenfolge fest, die den Benutzernamen enthält, oder ruft sie ab.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_WEB_SOCKET_CLOSE_TIMEOUT"></span><span id="winhttp_option_web_socket_close_timeout"></span>**WINHTTP \_ OPTION \_ WEB \_ SOCKET \_ CLOSE \_ TIMEOUT**
</dt> <dd> <dl> <dt>



Legt die Zeit in Millisekunden fest, die [**WinHttpWebSocketClose**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketclose) auf den Abschluss des schließenden Handshakes warten soll. Die Standardeinstellung beträgt 10 Sekunden.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_WEB_SOCKET_KEEPALIVE_INTERVAL"></span><span id="winhttp_option_web_socket_keepalive_interval"></span>**WINHTTP \_ OPTION \_ WEB \_ SOCKET \_ KEEPALIVE \_ INTERVAL**
</dt> <dd> <dl> <dt>



Legt das Intervall in Millisekunden fest, um ein Keep-Alive-Paket über die Verbindung zu senden. Das Standardintervall ist 30000 (30 Sekunden). Das Mindestintervall beträgt 15.000 (15 Sekunden). Wenn [**Sie WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) verwenden, um einen Wert unter 15000 festzulegen, wird mit **ERROR INVALID \_ \_ PARAMETER** zurückgegeben.

> [!Note]
> Der Standardwert für **WINHTTP \_ OPTION WEB SOCKET \_ \_ \_ KEEPALIVE \_ INTERVAL** wird aus **HKLM: \\ SOFTWARE Microsoft \\ \\ WebSocket \\ KeepaliveInterval** gelesen. Wenn kein Wert festgelegt ist, wird der Standardwert 30000 verwendet. Es ist nicht möglich, ein niedrigeres Keepalive-Intervall als 15.000 Millisekunden zu haben.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_WEB_SOCKET_RECEIVE_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_receive_buffer_size"></span>**WINHTTP \_ OPTION \_ WEB \_ SOCKET \_ RECEIVE \_ BUFFER \_ SIZE**
</dt> <dd> <dl> <dt>



Legt ein DWORD fest oder ruft es ab, das die Empfangspuffergröße angibt, die für WebSocket-Verbindungen verwendet werden soll.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_WEB_SOCKET_SEND_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_send_buffer_size"></span>**WINHTTP \_ OPTION \_ WEB \_ SOCKET \_ SEND \_ BUFFER \_ SIZE**
</dt> <dd> <dl> <dt>



Legt ein DWORD fest oder ruft es ab, das die Sendepuffergröße angibt, die für WebSocket-Verbindungen verwendet werden soll.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_WORKER_THREAD_COUNT"></span><span id="winhttp_option_worker_thread_count"></span>**ANZAHL VON \_ \_ WINHTTP-OPTION-WORKERTHREADS \_ \_**
</dt> <dd> <dl> <dt>



Legt einen ganzzahligen Wert ohne Vorzeichen fest, der die Anzahl der Arbeitsthreads angibt, die der Threadpool für asynchrone Vervollständigungen verwenden soll. Der Standardwert dieser Option ist 0 (null), was angibt, dass die Anzahl der Arbeitsthreads der Anzahl der CPUs im System entspricht. Diese Option kann nur für ein **NULL**  [HINTERNET-Handle](hinternet-handles-in-winhttp.md) festgelegt werden, bevor ein asynchroner Vorgang aufgetreten ist. Diese Option kann nur einmal festgelegt werden.

**Windows Server 2008 R2 und Windows 7:** Dieses Flag ist veraltet.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_WRITE_BUFFER_SIZE"></span><span id="winhttp_option_write_buffer_size"></span>**WINHTTP \_ OPTION \_ WRITE \_ BUFFER \_ SIZE**
</dt> <dd> <dl> <dt>



Diese Option ist veraltet. sie hat keine Auswirkungen.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Hinweise

In der folgenden Tabelle werden die Optionsflags aufgelistet, indem angegeben wird, auf welche Handles sie reagieren können, ob sie abgefragt und festgelegt werden können und welcher Datentyp verwendet wird. Ein "X" gibt an, dass das Optionsflag für die Verwendung mit der Funktion oder dem Handle gültig ist, während ein "-" angibt, dass das Optionsflag ungültig ist.

Der Versuch, ein Optionsflag für eine Windows Version festzulegen oder abzufragen, in der es nicht unterstützt wird, führt zu **ERROR \_ WINHTTP \_ INVALID \_ OPTION**.

| Optionsflag und Datentyp | Sitzungshandle | Anforderungshandle | Abfrageoption | SET-Option | Mindestversion Windows |
|-|-|-|-|-|-|
| \_WINHTTP-OPTION \_ GARANTIERT NICHT \_ \_ BLOCKIERENDE \_ RÜCKRUFE<br/>**Bool** | X | \- | \- | X | \- |
| WINHTTP \_ OPTION \_ AUTOLOGON \_ POLICY<br/>**DWORD** | \- | X | \- | X | \- |
| \_WINHTTP-OPTION \_ : \_ HINTERGRUNDVERBINDUNGEN<br/>**DWORD** | X | \- | \- | X | Windows 10 Version 21H1 |
| \_ \_ WINHTTP-OPTIONSRÜCKRUF<br/>**LPVOID** | X | X | X | X | \- |
| WINHTTP \_ OPTION \_ CLIENT \_ CERT \_ CONTEXT<br/>[**\_CERT-KONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) | \- | X | \- | X | Windows Vista |
| \_WINHTTP-OPTION \_ \_ CLIENTZERTIFIKATAUSSTELLERLISTE \_ \_<br/>[**SecPkgContext \_ IssuerListInfoEx**](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) | \- | X | X | \- | Windows Vista |
| \_ \_ WINHTTP-OPTIONSCODEPAGE<br/>**DWORD** | X | \- | \- | X | \- |
| \_WINHTTP-OPTION: \_ KONFIGURIEREN DER \_ \_ PASSPORT-AUTHENTIFIZIERUNG<br/>**DWORD** | X | \- | \- | X | \- |
| \_WINHTTP-OPTION \_ – \_ VERBINDUNGS-RETRIES<br/>**DWORD** | X | X | X | X | \- |
| WINHTTP \_ OPTION \_ CONNECT \_ TIMEOUT<br/>**DWORD** | X | X | X | X | \- |
| VERBINDUNGSINFORMATIONEN \_ ZUR WINHTTP-OPTION \_ \_<br/>[**\_WINHTTP-VERBINDUNGSINFORMATIONEN \_**](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info) | \- | X | X | \- | \- |
| WINHTTP \_ OPTION \_ CONNECTION \_ STATS \_ V0<br/>[**TCP \_ INFO \_ v0**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0) | \- | X | X | \- | Windows 10 Version 1903 |
| WINHTTP \_ OPTION \_ CONNECTION \_ STATS \_ V1<br/>[**TCP \_ INFO \_ v1**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1) | \- | X | X | \- | Windows 10 Version 2004 |
| KONTEXTWERT \_ DER WINHTTP-OPTION \_ \_<br/>**DWORD \_ PTR** | X | X | X | X | \- |
| DEKOMPRIMIERUNG \_ DER WINHTTP-OPTION \_<br/>**DWORD** | X | X | \- | X | Windows 8.1 |
| WINHTTP-OPTION \_ \_ \_ CERT CHAIN \_ BUILDING \_ DEAKTIVIEREN<br/>**Bool** | X | \- | \- | X | Windows 10 Version 21H1 |
| FUNKTION \_ "WINHTTP-OPTION \_ \_ DEAKTIVIEREN"<br/>**DWORD** | \- | X | \- | X | \- |
| \_WINHTTP-OPTION: \_ DEAKTIVIEREN DES \_ \_ \_ FALLBACKS DES SICHEREN PROTOKOLLS<br/>**Bool** | X | \- | \- | X | Windows 10 Version 1903 |
| WINHTTP-OPTION \_ \_ \_ STREAMWARTESCHLANGE \_ DEAKTIVIEREN<br/>**Bool** | X | X | \- | X | Windows 10 Version 1809 |
| FEATURE \_ "WINHTTP-OPTION \_ \_ AKTIVIEREN"<br/>**DWORD** | \* | \* | \- | X | \- |
| WINHTTP-OPTION \_ \_ \_ HTTP-PROTOKOLL \_ AKTIVIEREN<br/>**DWORD** | X | X | \- | X | Windows 10, Version 1607 |
| \_WINHTTP-OPTION: \_ \_ AKTIVIEREN DES HTTP2 \_ \_ PLUS-CLIENTZERTIFIKATKONTEXTS \_ \_<br/>**Bool** | X | \- | \- | X | Windows 10 Version 21H1 |
| \_WINHTTP-OPTION \_ ENABLETRACING<br/>**DWORD** | \- | \- | X | X | \- |
| WINHTTP \_ OPTION \_ ENCODE \_ EXTRA<br/>**Bool** | X | X | \- | X | Windows 10 Version 1803 |
| \_WINHTTP-OPTION \_ LÄUFT VERBINDUNG AB \_<br/>Nicht zutreffend | \- | X | \- | X | Windows 10 Version 1903 |
| \_ \_ ERWEITERTER \_ WINHTTP-OPTION-FEHLER<br/>**DWORD** | X | X | X | \- | \- |
| WINHTTP \_ OPTION \_ FIRST \_ AVAILABLE \_ CONNECTION<br/>**Bool** | X | \- | \- | X | Windows 10 Version 21H1 |
| WINHTTP \_ OPTION \_ GLOBAL \_ PROXY \_ CREDS<br/>[**WINHTTP \_ CREDS**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds) | X | X | \- | X | \- |
| WINHTTP \_ OPTION \_ GLOBAL \_ SERVER \_ CREDS<br/>[**WINHTTP \_ CREDS \_ EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) | X | X | \- | X | \- |
| TYP DES \_ WINHTTP-OPTIONSHANDLE \_ \_<br/>**DWORD** | X | X | X | \- | \- |
| WINHTTP \_ OPTION HTTP PROTOCOL \_ \_ \_ ERFORDERLICH<br/>**Bool** | X | X | \- | X | Windows 10 Version 1903 |
| VERWENDETES \_ \_ WINHTTP-OPTION-HTTP-PROTOKOLL \_ \_<br/>**DWORD** | \- | X | X | \- | Windows 10, Version 1607 |
| WINHTTP \_ OPTION \_ \_ HTTP-VERSION<br/>[**\_ \_ HTTP-VERSIONSINFORMATIONEN**](/windows/win32/api/winhttp/ns-winhttp-http_version_info) | X | X | X | X | \- |
| \_WINHTTP-OPTION \_ HTTP2 \_ KEEPALIVE<br/>**DWORD** | X | \- | \- | X | Windows 10 Version 21H1 |
| \_WINHTTP-OPTION \_ HTTP2 \_ PLUS \_ \_ ÜBERTRAGUNGSCODIERUNG<br/>**Bool** | X | X | \- | X | Windows 10 Version 21H1 |
| WINHTTP \_ OPTION \_ IGNORE \_ CERT \_ REVOCATION \_ OFFLINE<br/>**Bool** | \- | X | \- | X | Windows 10 Version 2004 |
| WINHTTP \_ \_ OPTION IPV6 \_ FAST \_ FALLBACK<br/>**Bool** | X | \- | \- | X | Windows 10 Version 1903 |
| \_WINHTTP-OPTION: \_ \_ PROXY \_ \_ CONNECT-ANTWORT<br/>**Bool** | X | X | X | \- | \- |
| WINHTTP \_ OPTION \_ \_ MAX. CONNS \_ PRO \_ 1 \_ 0 \_ SERVER<br/>**DWORD** | X | \- | X | X | \- |
| WINHTTP \_ OPTION \_ \_ MAX. ANZAHL VON CONNS \_ PRO \_ SERVER<br/>**DWORD** | X | \- | X | X | \- |
| WINHTTP \_ OPTION \_ \_ MAX. AUTOMATISCHE \_ \_ HTTP-UMLEITUNGEN<br/>**DWORD** | X | X | X | X | \- |
| WINHTTP-OPTION \_ \_ \_ MAX. \_ HTTP-STATUS \_ CONTINUE<br/>**DWORD** | X | X | X | X | \- |
| WINHTTP \_ OPTION \_ MAX \_ RESPONSE \_ DRAIN \_ SIZE<br/>**DWORD** | X | X | X | X | \- |
| WINHTTP-OPTION \_ \_ \_ MAX. GRÖßE DES \_ \_ ANTWORTHEADERS<br/>**DWORD** | X | X | X | X | \- |
| ÜBERGEORDNETES \_ HANDLE DER WINHTTP-OPTION \_ \_<br/>[HINTERNET](hinternet-handles-in-winhttp.md) | X | X | X | \- | \- |
| \_WINHTTP-OPTION \_ \_ PASSPORT-COBRANDINGTEXT \_<br/>**Lpwstr** | \- | X | X | \- | \- |
| \_WINHTTP-OPTION \_ \_ PASSPORT-COBRANDING-URL \_<br/>**Lpwstr** | \- | X | X | \- | \- |
| \_WINHTTP-OPTION \_ \_ \_ PASSPORT-RÜCKGABE-URL<br/>**LPVOID** | \- | X | X | \- | \- |
| \_WINHTTP-OPTION \_ \_ \_ PASSPORT-ABMELDE<br/>**LPVOID** | X | \- | \- | X | \- |
| \_ \_ WINHTTP-OPTIONSKENNWORT<br/>**Lpwstr** | \- | X | X | X | \- |
| \_WINHTTP-OPTIONSPROXY \_<br/>[**\_WINHTTP-PROXYINFORMATIONEN \_**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) | X | X | X | X | \- |
| \_PROXYKENNWORT \_ FÜR WINHTTP-OPTION \_<br/>**Lpwstr** | \- | X | X | X | \- |
| VERWENDETER \_ \_ WINHTTP-OPTIONSPROXY-SPN \_ \_<br/>**Lpwstr** | \- | X | X | \- | \- |
| \_PROXYBENUTZERNAME DER WINHTTP-OPTION \_ \_<br/>**Lpwstr** | \- | X | X | X | \- |
| WINHTTP-OPTION \_ \_ READ BUFFER \_ \_ SIZE<br/>**DWORD** | \- | X | X | X | \- |
| WINHTTP-OPTION \_ \_ "PROXY \_ \_ CONNECT-ANTWORT \_ EMPFANGEN"<br/>**Bool** | X | X | \- | X | \- |
| WINHTTP-OPTION \_ \_ \_ \_ EMPFANGSANTWORTZEITÜBERSCHREITUNG<br/>**DWORD** | X | X | X | X | \- |
| \_EMPFANGSZEITÜBERSCHREITUNG DER WINHTTP-OPTION \_ \_<br/>**DWORD** | X | X | X | X | \- |
| UMLEITUNGSRICHTLINIE \_ FÜR WINHTTP-OPTION \_ \_<br/>**DWORD** | X | X | X | X | \- |
| WINHTTP-OPTION BENUTZER IN URL \_ \_ \_ \_ \_ ABLEHNENPWD<br/>**Bool** | \- | X | \- | X | \- |
| \_ \_ ANFORDERUNGSPRIORITÄT DER WINHTTP-OPTION \_<br/>**DWORD** | \- | X | X | X | \- |
| WINHTTP \_ OPTION \_ REQUEST \_ STATS<br/>[**\_ \_ WINHTTP-ANFORDERUNGSSTATISTIKEN**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats) | \- | X | X | \- | Windows 10 Version 1903 |
| ANFORDERUNGSZEITEN DER \_ WINHTTP-OPTION \_ \_<br/>[**\_WINHTTP-ANFORDERUNGSZEITEN \_**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times) | \- | X | X | \- | Windows 10 Version 1903 |
| WINHTTP \_ OPTION \_ REQUIRE \_ STREAM \_ END<br/>**Bool** | X | X | \- | X | Windows 10 Version 21H1 |
| WINHTTP \_ OPTION \_ RESOLUTION \_ HOSTNAME<br/>**Lpwstr** | \- | X | \- | X | Windows 10 Version 21H1 |
| TIMEOUT FÜR AUFLÖSUNG DER \_ WINHTTP-OPTION \_ \_<br/>**DWORD** | X | X | X | X | \- |
| SICHERE \_ WINHTTP-OPTION \_ \_ – PROTOKOLLE<br/>**DWORD** | X | \- | \- | X | \- |
| WINHTTP \_ OPTION \_ SECURITY \_ CERTIFICATE \_ STRUCT<br/>[**WINHTTP \_ CERTIFICATE INFO (WINHTTP-ZERTIFIKATINFORMATIONEN) \_**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) | \- | X | X | \- | \- |
| SICHERHEITSFLAGS DER WINHTTP-OPTION \_ \_ \_<br/>**DWORD** | \- | X | X | X | \- |
| SICHERHEITSINFORMATIONEN ZUR WINHTTP-OPTION \_ \_ \_<br/>[**WINHTTP_SECURITY_INFO**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_security_info) | \- | X | X | \- | Windows 10 Version 2004 |
| WINHTTP \_ OPTION \_ SECURITY \_ KEY \_ BITNESS<br/>**DWORD** | \- | X | X | \- | \- |
| WINHTTP \_ OPTION \_ SEND \_ TIMEOUT<br/>**DWORD** | X | X | X | X | \- |
| WINHTTP \_ OPTION \_ SERVER \_ CBT<br/>[**\_SecPkgContext-Bindungen**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings)\* | \- | X | X | \- | \- |
| WINHTTP \_ OPTION \_ SERVER \_ CERT \_ CHAIN \_ CONTEXT<br/>[**CERT_CHAIN_CONTEXT**](/windows/win32/api/wincrypt/ns-wincrypt-cert_chain_context) | \- | X | X | \- | Windows 10 Version 2004 |
| WINHTTP \_ OPTION \_ SERVER \_ CERT \_ CONTEXT<br/>[**CERT-KONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) | \- | X | X | \- | \- |
| VERWENDETER \_ \_ WINHTTP-OPTIONSERVER-SPN \_ \_<br/>**Lpwstr** | \- | X | X | \- | \- |
| WINHTTP \_ OPTION \_ SPN<br/>**DWORD** | \- | X | \- | X | \- |
| WINHTTP \_ OPTION \_ STREAM \_ ERROR \_ CODE<br/>**DWORD** | \- | X | X | \- | Windows 10 Version 21H1 |
| WINHTTP \_ OPTION TCP FAST \_ \_ \_ OPEN<br/>**Bool** | X | \- | \- | X | Windows 10 Version 2004 |
| \_WINHTTP-OPTION \_ TCP \_ KEEPALIVE<br/>[**tcp \_ keepalive**](/windows/win32/winsock/sio-keepalive-vals) | X | \- | \- | X | Windows 10 Version 2004 |
| WINHTTP \_ OPTION \_ TLS \_ FALSE \_ START<br/>**Bool** | X | \- | \- | X | Windows 10 Version 2004 |
| WINHTTP \_ OPTION \_ TLS \_ PROTOCOL \_ INSECURE \_ FALLBACK<br/>**Bool** | X | \- | \- | X | Windows 10 Version 21H1 |
| WINHTTP-OPTION \_ \_ \_ ENTLADEBENACHRICHTIGUNGSEREIGNIS \_<br/>[HINTERNET](hinternet-handles-in-winhttp.md) | X | \- | \- | X | \- |
| \_WINHTTP-OPTION \_ UNSAFE \_ HEADER \_ PARSING<br/>**DWORD** | \- | X | \- | X | \- |
| UPGRADE DER \_ \_ WINHTTP-OPTION \_ AUF \_ \_ WEBSOCKET<br/>Nicht zutreffend | \- | X | \- | X | \- |
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
> Informationen Windows XP und Windows 2000 finden Sie unter [Laufzeitanforderungen.](winhttp-start-page.md)

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|--------------------------|---------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client) | Windows XP, Windows 2000 Professional nur mit \[ SP3-Desktop-Apps\]            |
| Unterstützte Mindestversion (Server) | Windows Server 2003, Windows 2000 Server nur mit \[ SP3-Desktop-Apps\]         |
| Verteilbare Komponente          | WinHTTP 5.0 und Internet Explorer 5.01 oder höher unter Windows XP und Windows 2000. |
| Header                   | Winhttp.h                                                                       |

## <a name="see-also"></a>Weitere Informationen

[WinHTTP-Versionen](winhttp-versions.md)
