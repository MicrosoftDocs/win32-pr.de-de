---
description: Enthält Optionen, die für die aktuelle WinHTTP-Sitzung (Microsoft Windows HTTP Services) festgelegt oder abgerufen werden können.
ms.assetid: 8464d794-b4a8-4c83-9e26-69257000102a
title: WinHttpRequestOption-Enumeration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WinHttpRequestOption
api_type:
- IDLDef
api_location:
- HttpRequest.idl
ms.openlocfilehash: ff4112538aff4c76c02e251f45e9dc78e6778633de6a5d93f6892dd87ff70c43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051878"
---
# <a name="winhttprequestoption-enumeration"></a>WinHttpRequestOption-Enumeration

Die **WinHttpRequestOption-Enumeration** enthält Optionen, die für die aktuelle WinHTTP-Sitzung (Microsoft Windows HTTP Services) festgelegt oder abgerufen werden können.

## <a name="syntax"></a>Syntax


```C++
typedef enum WinHttpRequestOption { 
  WinHttpRequestOption_UserAgentString,
  WinHttpRequestOption_URL,
  WinHttpRequestOption_URLCodePage,
  WinHttpRequestOption_EscapePercentInURL,
  WinHttpRequestOption_SslErrorIgnoreFlags,
  WinHttpRequestOption_SelectCertificate,
  WinHttpRequestOption_EnableRedirects,
  WinHttpRequestOption_UrlEscapeDisable,
  WinHttpRequestOption_UrlEscapeDisableQuery,
  WinHttpRequestOption_SecureProtocols,
  WinHttpRequestOption_EnableTracing,
  WinHttpRequestOption_RevertImpersonationOverSsl,
  WinHttpRequestOption_EnableHttpsToHttpRedirects,
  WinHttpRequestOption_EnablePassportAuthentication,
  WinHttpRequestOption_MaxAutomaticRedirects,
  WinHttpRequestOption_MaxResponseHeaderSize,
  WinHttpRequestOption_MaxResponseDrainSize,
  WinHttpRequestOption_EnableHttp1_1,
  WinHttpRequestOption_EnableCertificateRevocationCheck
} WinHttpRequestOption;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="WinHttpRequestOption_UserAgentString"></span><span id="winhttprequestoption_useragentstring"></span><span id="WINHTTPREQUESTOPTION_USERAGENTSTRING"></span>**WinHttpRequestOption \_ UserAgentString**
</dt> <dd>

Legt einen **VARIANT-Wert** fest, der die Zeichenfolge des [*Benutzer-Agents*](glossary.md) enthält, oder ruft diese ab.

</dd> <dt>

<span id="WinHttpRequestOption_URL"></span><span id="winhttprequestoption_url"></span><span id="WINHTTPREQUESTOPTION_URL"></span>**\_WinHttpRequestOption-URL**
</dt> <dd>

Ruft einen **VARIANT-Wert** ab, der die URL der Ressource enthält. Dieser Wert ist schreibgeschützt. Sie können die URL nicht mit dieser Eigenschaft festlegen. Die URL kann erst gelesen werden, wenn die [**Open-Methode**](iwinhttprequest-open.md) aufgerufen wird. Diese Option ist nützlich, um die URL nach Abschluss der [**Send-Methode**](iwinhttprequest-send.md) zu überprüfen, um zu überprüfen, ob eine Umleitung aufgetreten ist.

</dd> <dt>

<span id="WinHttpRequestOption_URLCodePage"></span><span id="winhttprequestoption_urlcodepage"></span><span id="WINHTTPREQUESTOPTION_URLCODEPAGE"></span>**WinHttpRequestOption \_ URLCodePage**
</dt> <dd>

Legt einen VARIANT fest oder ruft einen **VARIANT** ab, der die [*Codepage*](glossary.md) für die URL-Zeichenfolge identifiziert. Der Standardwert ist die UTF-8-Codepage. Die Codepage wird verwendet, um die In der [**Open-Methode**](iwinhttprequest-open.md) übergebene Unicode-URL-Zeichenfolge in eine Einzel-Byte-Zeichenfolgendarstellung zu konvertieren.

</dd> <dt>

<span id="WinHttpRequestOption_EscapePercentInURL"></span><span id="winhttprequestoption_escapepercentinurl"></span><span id="WINHTTPREQUESTOPTION_ESCAPEPERCENTINURL"></span>**WinHttpRequestOption \_ EscapePercentInURL**
</dt> <dd>

Legt einen VARIANT fest oder ruft einen **VARIANT** ab, der angibt, ob Prozentzeichen in der URL-Zeichenfolge in eine Escapesequenz konvertiert werden. Der Standardwert dieser Option ist **VARIANT \_ TRUE,** der alle ANSI-Zeichen (Unsafe American National Standards Institute) mit Ausnahme des Prozentzeichens angibt, die in eine Escapesequenz konvertiert werden.

</dd> <dt>

<span id="WinHttpRequestOption_SslErrorIgnoreFlags"></span><span id="winhttprequestoption_sslerrorignoreflags"></span><span id="WINHTTPREQUESTOPTION_SSLERRORIGNOREFLAGS"></span>**WinHttpRequestOption \_ SslErrorIgnoreFlags**
</dt> <dd>

Legt einen VARIANT fest oder ruft einen **VARIANT** ab, der angibt, welche Serverzertifikatfehler ignoriert werden sollen. Dies kann eine Kombination aus einem oder mehreren der folgenden Flags sein.



| Fehler                                                  | Wert  |
|--------------------------------------------------------|--------|
| Unbekannte Zertifizierungsstelle oder nicht vertrauenswürdiger Stamm | 0x0100 |
| Falsche Verwendung                                            | 0x0200 |
| Ungültiger allgemeiner Name (Common Name, CN)                               | 0x1000 |
| Ungültiges Datum oder abgelaufenes Zertifikat                    | 0x2000 |



 

Der Standardwert dieser Option in Version 5.1 von WinHTTP ist 0 (null), was dazu führt, dass keine Fehler ignoriert werden. In früheren Versionen von WinHTTP war die Standardeinstellung 0x3300, was dazu führte, dass alle Serverzertifikatfehler standardmäßig ignoriert wurden.

</dd> <dt>

<span id="WinHttpRequestOption_SelectCertificate"></span><span id="winhttprequestoption_selectcertificate"></span><span id="WINHTTPREQUESTOPTION_SELECTCERTIFICATE"></span>**WinHttpRequestOption \_ SelectCertificate**
</dt> <dd>

Legt einen **VARIANT-Wert** fest, der das Clientzertifikat angibt, das zur Authentifizierung an einen Server gesendet wird. Diese Option gibt den Speicherort, [*den Zertifikatspeicher*](glossary.md)und den Antragsteller eines Clientzertifikats an, die mit umgekehrten Schrägstrichen getrennt sind. Weitere Informationen zum Auswählen eines Clientzertifikats finden Sie unter [SSL in WinHTTP.](ssl-in-winhttp.md)

</dd> <dt>

<span id="WinHttpRequestOption_EnableRedirects"></span><span id="winhttprequestoption_enableredirects"></span><span id="WINHTTPREQUESTOPTION_ENABLEREDIRECTS"></span>**WinHttpRequestOption \_ EnableRedirects**
</dt> <dd>

Legt einen VARIANT fest oder ruft einen **VARIANT** ab, der angibt, ob Anforderungen automatisch umgeleitet werden, wenn der Server einen neuen Speicherort für die Ressource angibt. Der Standardwert dieser Option ist **VARIANT \_ TRUE,** um anzugeben, dass Anforderungen automatisch umgeleitet werden.

</dd> <dt>

<span id="WinHttpRequestOption_UrlEscapeDisable"></span><span id="winhttprequestoption_urlescapedisable"></span><span id="WINHTTPREQUESTOPTION_URLESCAPEDISABLE"></span>**WinHttpRequestOption \_ UrlEscapeDisable**
</dt> <dd>

Legt einen VARIANT fest oder ruft einen **VARIANT** ab, der angibt, ob unsichere Zeichen in den Pfad- und Abfragekomponenten einer URL in Escapesequenzen konvertiert werden. Der Standardwert dieser Option ist **VARIANT \_ TRUE,** der angibt, dass Zeichen im Pfad und in der Abfrage konvertiert werden.

</dd> <dt>

<span id="WinHttpRequestOption_UrlEscapeDisableQuery"></span><span id="winhttprequestoption_urlescapedisablequery"></span><span id="WINHTTPREQUESTOPTION_URLESCAPEDISABLEQUERY"></span>**WinHttpRequestOption \_ UrlEscapeDisableQuery**
</dt> <dd>

Legt einen VARIANT fest oder ruft einen **VARIANT** ab, der angibt, ob unsichere Zeichen in der Abfragekomponente der URL in Escapesequenzen konvertiert werden. Der Standardwert dieser Option ist **VARIANT \_ TRUE,** der angibt, dass Zeichen in der Abfrage konvertiert werden.

</dd> <dt>

<span id="WinHttpRequestOption_SecureProtocols"></span><span id="winhttprequestoption_secureprotocols"></span><span id="WINHTTPREQUESTOPTION_SECUREPROTOCOLS"></span>**WinHttpRequestOption \_ SecureProtocols**
</dt> <dd>

Legt einen VARIANT fest oder ruft einen **VARIANT** ab, der angibt, welche sicheren Protokolle verwendet werden können. Mit dieser Option werden die protokolle ausgewählt, die für den Client zulässig sind. Das Protokoll wird während des SSL-Handshakes (Secure Sockets Layer) ausgehandelt. Dies kann eine Kombination aus einem oder mehreren der folgenden Flags sein.



| Protokoll                           | Wert  |
|------------------------------------|--------|
| SSL 2.0                            | 0x0008 |
| SSL 3.0                            | 0x0020 |
| Transport Layer Security (TLS) 1.0 | 0x0080 |



 

Der Standardwert dieser Option ist 0x0028, der angibt, dass SSL 2.0 oder SSL 3.0 verwendet werden kann. Wenn diese Option auf 0 (null) festgelegt ist, können Client und Server kein akzeptables Sicherheitsprotokoll ermitteln, und das nächste [**Senden**](iwinhttprequest-send.md) führt zu einem Fehler.

</dd> <dt>

<span id="WinHttpRequestOption_EnableTracing"></span><span id="winhttprequestoption_enabletracing"></span><span id="WINHTTPREQUESTOPTION_ENABLETRACING"></span>**WinHttpRequestOption \_ EnableTracing**
</dt> <dd>

Legt einen VARIANT fest oder ruft einen **VARIANT** ab, der angibt, ob die Ablaufverfolgung derzeit aktiviert ist. Weitere Informationen zur Ablaufverfolgungsfunktion in Microsoft Windows HTTP Services (WinHTTP) finden Sie unter [WinHTTP Trace Facility](winhttptracecfg-exe--a-trace-configuration-tool.md).

</dd> <dt>

<span id="WinHttpRequestOption_RevertImpersonationOverSsl"></span><span id="winhttprequestoption_revertimpersonationoverssl"></span><span id="WINHTTPREQUESTOPTION_REVERTIMPERSONATIONOVERSSL"></span>**WinHttpRequestOption \_ RevertImpersonationOverSsl**
</dt> <dd>

Steuert, ob das [**WinHttpRequest-Objekt**](winhttprequest.md) den Clientidentitätswechsel für die Dauer der SSL-Zertifikatauthentifizierungsvorgänge vorübergehend zurückgesetzt. Die Standardeinstellung für das **WinHttpRequest-Objekt** ist **TRUE.** Legen Sie diese Option auf **FALSE** fest, um beim Ausführen von Zertifikatauthentifizierungsvorgängen den Identitätswechsel beizubehalten.

</dd> <dt>

<span id="WinHttpRequestOption_EnableHttpsToHttpRedirects"></span><span id="winhttprequestoption_enablehttpstohttpredirects"></span><span id="WINHTTPREQUESTOPTION_ENABLEHTTPSTOHTTPREDIRECTS"></span>**WinHttpRequestOption \_ EnableHttpsToHttpRedirects**
</dt> <dd>

Steuert, ob WinHTTP Umleitungen zulässt. Standardmäßig werden alle Umleitungen automatisch befolgt, mit Ausnahme derjenigen, die von einer sicheren (HTTPS)-URL an eine nicht sichere (HTTP)-URL übertragen werden. Legen Sie diese Option auf **TRUE** fest, um HTTPS-zu-HTTP-Umleitungen zu aktivieren.

</dd> <dt>

<span id="WinHttpRequestOption_EnablePassportAuthentication"></span><span id="winhttprequestoption_enablepassportauthentication"></span><span id="WINHTTPREQUESTOPTION_ENABLEPASSPORTAUTHENTICATION"></span>**WinHttpRequestOption \_ EnablePassportAuthentication**
</dt> <dd>

Aktiviert oder deaktiviert die Unterstützung für die Passport-Authentifizierung. Standardmäßig ist die automatische Unterstützung für die Passport-Authentifizierung deaktiviert. Legen Sie diese Option auf **TRUE** fest, um die Passport-Authentifizierungsunterstützung zu aktivieren.

</dd> <dt>

<span id="WinHttpRequestOption_MaxAutomaticRedirects"></span><span id="winhttprequestoption_maxautomaticredirects"></span><span id="WINHTTPREQUESTOPTION_MAXAUTOMATICREDIRECTS"></span>**WinHttpRequestOption \_ MaxAutomaticRedirects**
</dt> <dd>

Legt die maximale Anzahl von Umleitungen fest, denen WinHTTP folgt, oder ruft sie ab. der Standardwert ist 10. Dieser Grenzwert verhindert, dass nicht autorisierte Websites den WinHTTP-Client nach einer großen Anzahl von Umleitungen angehalten haben.

**Windows XP mit SP1 und Windows 2000 mit SP3:** Dieser Enumerationswert wird nicht unterstützt.

</dd> <dt>

<span id="WinHttpRequestOption_MaxResponseHeaderSize"></span><span id="winhttprequestoption_maxresponseheadersize"></span><span id="WINHTTPREQUESTOPTION_MAXRESPONSEHEADERSIZE"></span>**WinHttpRequestOption \_ MaxResponseHeaderSize**
</dt> <dd>

Legt einen gebundenen Satz für die maximale Größe des Headerteils der Serverantwort fest oder ruft diese ab. Diese Grenze schützt den Client vor einem böswilligen Server, der versucht, den Client zu lahmen, indem eine Antwort mit einer unendlichen Menge von Headerdaten gesendet wird. Der Standardwert ist 64 KB.

**Windows XP mit SP1 und Windows 2000 mit SP3:** Dieser Enumerationswert wird nicht unterstützt.

</dd> <dt>

<span id="WinHttpRequestOption_MaxResponseDrainSize"></span><span id="winhttprequestoption_maxresponsedrainsize"></span><span id="WINHTTPREQUESTOPTION_MAXRESPONSEDRAINSIZE"></span>**WinHttpRequestOption \_ MaxResponseDrainSize**
</dt> <dd>

Legt eine Grenze für die Datenmenge fest, die aus Antworten entladen wird, um eine Verbindung wiederzuverwenden, oder ruft sie ab. Die Standardeinstellung ist 1 MB.

**Windows XP mit SP1 und Windows 2000 mit SP3:** Dieser Enumerationswert wird nicht unterstützt.

</dd> <dt>

<span id="WinHttpRequestOption_EnableHttp1_1"></span><span id="winhttprequestoption_enablehttp1_1"></span><span id="WINHTTPREQUESTOPTION_ENABLEHTTP1_1"></span>**WinHttpRequestOption \_ EnableHttp1 \_ 1**
</dt> <dd>

Legt einen booleschen Wert fest, der angibt, ob HTTP/1.1 oder HTTP/1.0 verwendet werden soll, oder ruft diesen ab. Der Standardwert ist **TRUE,** sodass HTTP/1.1 standardmäßig verwendet wird.

**Windows XP mit SP1 und Windows 2000 mit SP3:** Dieser Enumerationswert wird nicht unterstützt.

</dd> <dt>

<span id="WinHttpRequestOption_EnableCertificateRevocationCheck"></span><span id="winhttprequestoption_enablecertificaterevocationcheck"></span><span id="WINHTTPREQUESTOPTION_ENABLECERTIFICATEREVOCATIONCHECK"></span>**WinHttpRequestOption \_ EnableCertificateRevocationCheck**
</dt> <dd>

Aktiviert die Überprüfung der Serverzertifikatsperrung während der SSL-Aushandlung. Wenn der Server ein Zertifikat vorlegt, wird eine Überprüfung durchgeführt, um festzustellen, ob das Zertifikat vom Aussteller widerrufen wurde. Wenn das Zertifikat tatsächlich widerrufen wird oder die Sperrprüfung fehlschlägt, weil die Zertifikatsperrliste (Certificate Revocation List, CRL) nicht heruntergeladen werden kann, schlägt die Anforderung fehl. solche Sperrfehler können nicht unterdrückt werden.

**Windows XP mit SP1 und Windows 2000 mit SP3:** Dieser Enumerationswert wird nicht unterstützt.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Legen Sie eine Option fest, indem Sie eine der vorangehenden Konstanten als Parameter der [**Option-Eigenschaft**](iwinhttprequest-option.md) angeben.

> [!Note]  
> Informationen Windows XP und Windows 2000 finden Sie im Abschnitt Laufzeitanforderungen der [WinHttp-Startseite.](winhttp-start-page.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP, Windows 2000 Professional nur mit \[ SP3-Desktop-Apps\]<br/>            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003, Windows 2000 Server nur mit \[ SP3-Desktop-Apps\]<br/>         |
| Verteilbare Komponente<br/>          | WinHTTP 5.0 und Internet Explorer 5.01 oder höher unter Windows XP und Windows 2000.<br/> |
| Idl<br/>                      | <dl> <dt>HttpRequest.idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[WinHTTP-Versionen](winhttp-versions.md)
</dt> </dl>

 

 




