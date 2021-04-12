---
description: Enthält Optionen, die für die aktuelle Microsoft Windows HTTP-Dienste (WinHTTP)-Sitzung festgelegt oder abgerufen werden können.
ms.assetid: 8464d794-b4a8-4c83-9e26-69257000102a
title: Winhttprequestoption-Enumeration
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
ms.openlocfilehash: 32ae65f43cd04027027e43d29c49ed0f68f29c9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526237"
---
# <a name="winhttprequestoption-enumeration"></a>Winhttprequestoption-Enumeration

Die **winhttprequestoption** -Enumeration enthält Optionen, die für die aktuelle Microsoft Windows HTTP-Dienste (WinHTTP)-Sitzung festgelegt oder abgerufen werden können.

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

<span id="WinHttpRequestOption_UserAgentString"></span><span id="winhttprequestoption_useragentstring"></span><span id="WINHTTPREQUESTOPTION_USERAGENTSTRING"></span>**Winhttprequestoption \_ useragentstring**
</dt> <dd>

Legt eine **Variante** fest oder ruft Sie ab, die die Zeichenfolge des [*Benutzer-Agents*](glossary.md) enthält.

</dd> <dt>

<span id="WinHttpRequestOption_URL"></span><span id="winhttprequestoption_url"></span><span id="WINHTTPREQUESTOPTION_URL"></span>**Winhttprequestoption- \_ URL**
</dt> <dd>

Ruft eine **Variante** ab, die die URL der Ressource enthält. Dieser Wert ist schreibgeschützt. die URL kann nicht mit dieser Eigenschaft festgelegt werden. Die URL kann erst gelesen werden, wenn die [**Open**](iwinhttprequest-open.md) -Methode aufgerufen wird. Diese Option ist nützlich, wenn die URL nach Abschluss der [**Sende**](iwinhttprequest-send.md) Methode überprüft werden soll, um zu überprüfen, ob eine Umleitung erfolgt ist.

</dd> <dt>

<span id="WinHttpRequestOption_URLCodePage"></span><span id="winhttprequestoption_urlcodepage"></span><span id="WINHTTPREQUESTOPTION_URLCODEPAGE"></span>**Winhttprequestoption \_ urlcodepage**
</dt> <dd>

Legt einen **Variant** fest, der die [*Codepage*](glossary.md) für die URL-Zeichenfolge angibt, oder ruft ihn ab. Der Standardwert ist die UTF-8-Codepage. Die Codepage wird verwendet, um die Unicode-URL-Zeichenfolge, die in der [**Open**](iwinhttprequest-open.md) -Methode verwendet wird, in eine Einzel Byte-Zeichen folgen Darstellung zu konvertieren.

</dd> <dt>

<span id="WinHttpRequestOption_EscapePercentInURL"></span><span id="winhttprequestoption_escapepercentinurl"></span><span id="WINHTTPREQUESTOPTION_ESCAPEPERCENTINURL"></span>**Winhttprequestoption \_ escapeprozentualurl**
</dt> <dd>

Legt einen **Variant** -Wert fest, der angibt, ob Prozentzeichen in der URL-Zeichenfolge in eine Escapesequenz konvertiert werden. Der Standardwert dieser Option ist **Variant \_ true** , der alle unsicheren American National Standards Institute (ANSI)-Zeichen angibt, außer das Prozentzeichen wird in eine Escapesequenz konvertiert.

</dd> <dt>

<span id="WinHttpRequestOption_SslErrorIgnoreFlags"></span><span id="winhttprequestoption_sslerrorignoreflags"></span><span id="WINHTTPREQUESTOPTION_SSLERRORIGNOREFLAGS"></span>**Winhttprequestoption \_ sslerrorignoreflags**
</dt> <dd>

Legt einen **Variant** -Wert fest, der angibt, welche Serverzertifikat Fehler ignoriert werden sollen, oder ruft ihn ab. Dabei kann es sich um eine Kombination aus einem oder mehreren der folgenden Flags handeln.



| Fehler                                                  | Wert  |
|--------------------------------------------------------|--------|
| Unbekannte Zertifizierungsstelle (Certification Authority, ca) oder nicht vertrauenswürdiger Stamm | 0x0100 |
| Falsche Verwendung                                            | 0x0200 |
| Ungültiger allgemeiner Name (Common Name, CN)                               | 0x1000 |
| Ungültiges Datum oder Zertifikat abgelaufen.                    | 0x2000 |



 

Der Standardwert dieser Option in Version 5,1 von WinHTTP ist 0 (null), was dazu führt, dass keine Fehler ignoriert werden. In früheren Versionen von WinHTTP war die Standardeinstellung 0x3300, was dazu geführt hat, dass alle Serverzertifikat Fehler standardmäßig ignoriert wurden.

</dd> <dt>

<span id="WinHttpRequestOption_SelectCertificate"></span><span id="winhttprequestoption_selectcertificate"></span><span id="WINHTTPREQUESTOPTION_SELECTCERTIFICATE"></span>**Winhttprequestoption \_ selectcertificate**
</dt> <dd>

Legt einen **Variant** -Wert fest, der das Client Zertifikat angibt, das zur Authentifizierung an einen Server gesendet wird. Diese Option gibt den Speicherort, den [*Zertifikat Speicher*](glossary.md)und den Betreff eines Client Zertifikats an, das mit umgekehrten Schrägstrichen getrennt ist. Weitere Informationen zum Auswählen eines Client Zertifikats finden Sie unter [SSL in WinHTTP](ssl-in-winhttp.md).

</dd> <dt>

<span id="WinHttpRequestOption_EnableRedirects"></span><span id="winhttprequestoption_enableredirects"></span><span id="WINHTTPREQUESTOPTION_ENABLEREDIRECTS"></span>**Winhttprequestoption \_ enablereumleitungen**
</dt> <dd>

Legt einen **Variant** -Wert fest, der angibt, ob Anforderungen automatisch umgeleitet werden, wenn der Server einen neuen Speicherort für die Ressource angibt, oder ruft ihn ab. Der Standardwert dieser Option ist **Variant \_ true** , um anzugeben, dass Anforderungen automatisch umgeleitet werden.

</dd> <dt>

<span id="WinHttpRequestOption_UrlEscapeDisable"></span><span id="winhttprequestoption_urlescapedisable"></span><span id="WINHTTPREQUESTOPTION_URLESCAPEDISABLE"></span>**Winhttprequestoption \_ urlescapedeaktiviert**
</dt> <dd>

Legt einen **Variant** -Wert fest, der angibt, ob unsichere Zeichen in den Pfad-und Abfrage Komponenten einer URL in Escapesequenzen konvertiert werden, oder ruft ihn ab. Der Standardwert dieser Option ist **Variant \_ true**, das angibt, dass die Zeichen im Pfad und in der Abfrage konvertiert werden.

</dd> <dt>

<span id="WinHttpRequestOption_UrlEscapeDisableQuery"></span><span id="winhttprequestoption_urlescapedisablequery"></span><span id="WINHTTPREQUESTOPTION_URLESCAPEDISABLEQUERY"></span>**Winhttprequestoption \_ urlescapedisablequery**
</dt> <dd>

Legt einen **Variant** -Wert fest, der angibt, ob unsichere Zeichen in der Abfrage Komponente der URL in Escapesequenzen konvertiert werden, oder ruft ihn ab. Der Standardwert dieser Option ist **Variant \_ true**, das angibt, dass Zeichen in der Abfrage konvertiert werden.

</dd> <dt>

<span id="WinHttpRequestOption_SecureProtocols"></span><span id="winhttprequestoption_secureprotocols"></span><span id="WINHTTPREQUESTOPTION_SECUREPROTOCOLS"></span>**Winhttprequestoption \_ secureprotokolls**
</dt> <dd>

Legt einen **Variant** -Wert fest, der angibt, welche sicheren Protokolle verwendet werden können, oder ruft ihn ab. Mit dieser Option werden die für den Client zulässigen Protokolle ausgewählt. Das Protokoll wird während des Secure Sockets Layer (SSL)-Handshake ausgehandelt. Dabei kann es sich um eine Kombination aus einem oder mehreren der folgenden Flags handeln.



| Protokoll                           | Wert  |
|------------------------------------|--------|
| SSL 2.0                            | 0x0008 |
| SSL 3.0                            | 0x0020 |
| Transport Layer Security (TLS) 1,0 | 0x0080 |



 

Der Standardwert dieser Option ist 0x0028 und gibt an, dass SSL 2,0 oder SSL 3,0 verwendet werden kann. Wenn diese Option auf NULL festgelegt ist, können der Client und der Server kein akzeptables Sicherheitsprotokoll ermitteln, und der nächste [**Sende**](iwinhttprequest-send.md) Vorgang führt zu einem Fehler.

</dd> <dt>

<span id="WinHttpRequestOption_EnableTracing"></span><span id="winhttprequestoption_enabletracing"></span><span id="WINHTTPREQUESTOPTION_ENABLETRACING"></span>**Winhttprequestoption \_ EnableTracing**
</dt> <dd>

Legt einen **Variant** fest oder ruft ihn ab, der angibt, ob die Ablauf Verfolgung derzeit aktiviert ist. Weitere Informationen zur Ablauf Verfolgungs Funktion in den Microsoft Windows HTTP-Diensten (WinHTTP) finden Sie unter [WinHTTP-Ablauf Verfolgungs Funktion](winhttptracecfg-exe--a-trace-configuration-tool.md).

</dd> <dt>

<span id="WinHttpRequestOption_RevertImpersonationOverSsl"></span><span id="winhttprequestoption_revertimpersonationoverssl"></span><span id="WINHTTPREQUESTOPTION_REVERTIMPERSONATIONOVERSSL"></span>**Winhttprequestoption \_ revertimpersonationoverssl**
</dt> <dd>

Steuert, ob das [**WinHttpRequest**](winhttprequest.md) -Objekt den Client Identitätswechsel vorübergehend für die Dauer der SSL-Zertifikat Authentifizierungs Vorgänge zurücksetzt. Die Standardeinstellung für das **WinHttpRequest** -Objekt ist " **true**". Legen Sie diese Option auf **false** fest, um den Identitätswechsel beim Ausführen von Zertifikat Authentifizierungs Vorgängen beizubehalten.

</dd> <dt>

<span id="WinHttpRequestOption_EnableHttpsToHttpRedirects"></span><span id="winhttprequestoption_enablehttpstohttpredirects"></span><span id="WINHTTPREQUESTOPTION_ENABLEHTTPSTOHTTPREDIRECTS"></span>**Winhttprequestoption \_ enablehttpstohttpredirektionen**
</dt> <dd>

Steuert, ob WinHTTP Umleitungen zulässt. Standardmäßig werden alle Umleitungen automatisch befolgt, mit Ausnahme derjenigen, die von einer sicheren URL (HTTPS) an eine nicht sichere URL (http) übertragen werden. Legen Sie diese Option auf " **true** " fest, um HTTPS-HTTP-Umleitungen zu aktivieren.

</dd> <dt>

<span id="WinHttpRequestOption_EnablePassportAuthentication"></span><span id="winhttprequestoption_enablepassportauthentication"></span><span id="WINHTTPREQUESTOPTION_ENABLEPASSPORTAUTHENTICATION"></span>**Winhttprequestoption \_ enablepassportauthentication**
</dt> <dd>

Aktiviert oder deaktiviert die Unterstützung für die Passport-Authentifizierung. Standardmäßig ist die automatische Unterstützung für die Passport-Authentifizierung deaktiviert. Legen Sie diese Option auf **true** fest, um die Unterstützung der Passport-Authentifizierung

</dd> <dt>

<span id="WinHttpRequestOption_MaxAutomaticRedirects"></span><span id="winhttprequestoption_maxautomaticredirects"></span><span id="WINHTTPREQUESTOPTION_MAXAUTOMATICREDIRECTS"></span>**Winhttprequestoption \_ maxautomatikreumleitungen**
</dt> <dd>

Legt die maximale Anzahl von Umleitungen fest, die WinHTTP befolgt, oder ruft Sie ab. der Standardwert ist 10. Diese Beschränkung verhindert, dass nicht autorisierte Standorte den WinHTTP-Client Stall nach einer großen Anzahl von Umleitungen durchführen.

**Windows XP mit SP1 und Windows 2000 mit SP3:** Dieser Enumerationswert wird nicht unterstützt.

</dd> <dt>

<span id="WinHttpRequestOption_MaxResponseHeaderSize"></span><span id="winhttprequestoption_maxresponseheadersize"></span><span id="WINHTTPREQUESTOPTION_MAXRESPONSEHEADERSIZE"></span>**Winhttprequestoption \_ maxresponsheadersize**
</dt> <dd>

Legt eine gebundene Menge für die maximale Größe des Header Teils der Serverantwort fest oder ruft diese ab. Diese Bindung schützt den Client vor einem böswilligen Server, der versucht, den Client zu stoppen, indem er eine Antwort mit einer unendlichen Menge von Header Daten sendet. Der Standardwert ist 64 KB.

**Windows XP mit SP1 und Windows 2000 mit SP3:** Dieser Enumerationswert wird nicht unterstützt.

</dd> <dt>

<span id="WinHttpRequestOption_MaxResponseDrainSize"></span><span id="winhttprequestoption_maxresponsedrainsize"></span><span id="WINHTTPREQUESTOPTION_MAXRESPONSEDRAINSIZE"></span>**Winhttprequestoption \_ maxresponsdrainsize**
</dt> <dd>

Legt eine gebundene Datenmenge fest oder ruft Sie ab, um eine Verbindung wiederzuverwenden. Die Standardeinstellung ist 1 MB.

**Windows XP mit SP1 und Windows 2000 mit SP3:** Dieser Enumerationswert wird nicht unterstützt.

</dd> <dt>

<span id="WinHttpRequestOption_EnableHttp1_1"></span><span id="winhttprequestoption_enablehttp1_1"></span><span id="WINHTTPREQUESTOPTION_ENABLEHTTP1_1"></span>**Winhttprequestoption \_ EnableHttp1 \_ 1**
</dt> <dd>

Legt einen booleschen Wert fest, der angibt, ob HTTP/1.1 oder http/1.0 verwendet werden soll, oder ruft ihn ab. Der Standardwert ist " **true**", sodass "http/1.1" standardmäßig verwendet wird.

**Windows XP mit SP1 und Windows 2000 mit SP3:** Dieser Enumerationswert wird nicht unterstützt.

</dd> <dt>

<span id="WinHttpRequestOption_EnableCertificateRevocationCheck"></span><span id="winhttprequestoption_enablecertificaterevocationcheck"></span><span id="WINHTTPREQUESTOPTION_ENABLECERTIFICATEREVOCATIONCHECK"></span>**Winhttprequestoption \_ enablecertificaterevocationcheck**
</dt> <dd>

Aktiviert die Serverzertifikat Sperr Überprüfung während der SSL-Aushandlung. Wenn der Server ein Zertifikat anzeigt, wird eine Überprüfung durchgeführt, um zu bestimmen, ob das Zertifikat vom Aussteller widerrufen wurde. Wenn das Zertifikat tatsächlich widerrufen wird oder die Sperr Überprüfung fehlschlägt, weil die Zertifikat Sperr Liste nicht heruntergeladen werden kann, schlägt die Anforderung fehl. solche Sperr Fehler können nicht unterdrückt werden.

**Windows XP mit SP1 und Windows 2000 mit SP3:** Dieser Enumerationswert wird nicht unterstützt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Legen Sie eine Option fest, indem Sie eine der vorangehenden Konstanten als Parameter der [**Option**](iwinhttprequest-option.md) -Eigenschaft angeben.

> [!Note]  
> Informationen zu Windows XP und Windows 2000 finden Sie im Abschnitt [Lauf Zeitanforderungen](winhttp-start-page.md) auf der WinHTTP-Startseite.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP, Windows 2000 Professional mit SP3 \[ Desktop-Apps\]<br/>            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003, Windows 2000-Server mit \[ nur SP3-Desktop-Apps\]<br/>         |
| Verteilbare Komponente<br/>          | WinHTTP 5,0 und Internet Explorer 5,01 oder höher unter Windows XP und Windows 2000.<br/> |
| IDL<br/>                      | <dl> <dt>HttpRequest. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[WinHTTP-Versionen](winhttp-versions.md)
</dt> </dl>

 

 




