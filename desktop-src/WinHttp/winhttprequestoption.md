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
# <a name="winhttprequestoption-enumeration"></a><span data-ttu-id="c41c0-103">Winhttprequestoption-Enumeration</span><span class="sxs-lookup"><span data-stu-id="c41c0-103">WinHttpRequestOption enumeration</span></span>

<span data-ttu-id="c41c0-104">Die **winhttprequestoption** -Enumeration enthält Optionen, die für die aktuelle Microsoft Windows HTTP-Dienste (WinHTTP)-Sitzung festgelegt oder abgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="c41c0-104">The **WinHttpRequestOption** enumeration includes options that can be set or retrieved for the current Microsoft Windows HTTP Services (WinHTTP) session.</span></span>

## <a name="syntax"></a><span data-ttu-id="c41c0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c41c0-105">Syntax</span></span>


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



## <a name="constants"></a><span data-ttu-id="c41c0-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="c41c0-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="c41c0-107"><span id="WinHttpRequestOption_UserAgentString"></span><span id="winhttprequestoption_useragentstring"></span><span id="WINHTTPREQUESTOPTION_USERAGENTSTRING"></span>**Winhttprequestoption \_ useragentstring**</span><span class="sxs-lookup"><span data-stu-id="c41c0-107"><span id="WinHttpRequestOption_UserAgentString"></span><span id="winhttprequestoption_useragentstring"></span><span id="WINHTTPREQUESTOPTION_USERAGENTSTRING"></span>**WinHttpRequestOption\_UserAgentString**</span></span>
</dt> <dd>

<span data-ttu-id="c41c0-108">Legt eine **Variante** fest oder ruft Sie ab, die die Zeichenfolge des [*Benutzer-Agents*](glossary.md) enthält.</span><span class="sxs-lookup"><span data-stu-id="c41c0-108">Sets or retrieves a **VARIANT** that contains the [*user agent*](glossary.md) string.</span></span>

</dd> <dt>

<span data-ttu-id="c41c0-109"><span id="WinHttpRequestOption_URL"></span><span id="winhttprequestoption_url"></span><span id="WINHTTPREQUESTOPTION_URL"></span>**Winhttprequestoption- \_ URL**</span><span class="sxs-lookup"><span data-stu-id="c41c0-109"><span id="WinHttpRequestOption_URL"></span><span id="winhttprequestoption_url"></span><span id="WINHTTPREQUESTOPTION_URL"></span>**WinHttpRequestOption\_URL**</span></span>
</dt> <dd>

<span data-ttu-id="c41c0-110">Ruft eine **Variante** ab, die die URL der Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="c41c0-110">Retrieves a **VARIANT** that contains the URL of the resource.</span></span> <span data-ttu-id="c41c0-111">Dieser Wert ist schreibgeschützt. die URL kann nicht mit dieser Eigenschaft festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="c41c0-111">This value is read-only; you cannot set the URL using this property.</span></span> <span data-ttu-id="c41c0-112">Die URL kann erst gelesen werden, wenn die [**Open**](iwinhttprequest-open.md) -Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="c41c0-112">The URL cannot be read until the [**Open**](iwinhttprequest-open.md) method is called.</span></span> <span data-ttu-id="c41c0-113">Diese Option ist nützlich, wenn die URL nach Abschluss der [**Sende**](iwinhttprequest-send.md) Methode überprüft werden soll, um zu überprüfen, ob eine Umleitung erfolgt ist.</span><span class="sxs-lookup"><span data-stu-id="c41c0-113">This option is useful for checking the URL after the [**Send**](iwinhttprequest-send.md) method is finished to verify that any redirection occurred.</span></span>

</dd> <dt>

<span data-ttu-id="c41c0-114"><span id="WinHttpRequestOption_URLCodePage"></span><span id="winhttprequestoption_urlcodepage"></span><span id="WINHTTPREQUESTOPTION_URLCODEPAGE"></span>**Winhttprequestoption \_ urlcodepage**</span><span class="sxs-lookup"><span data-stu-id="c41c0-114"><span id="WinHttpRequestOption_URLCodePage"></span><span id="winhttprequestoption_urlcodepage"></span><span id="WINHTTPREQUESTOPTION_URLCODEPAGE"></span>**WinHttpRequestOption\_URLCodePage**</span></span>
</dt> <dd>

<span data-ttu-id="c41c0-115">Legt einen **Variant** fest, der die [*Codepage*](glossary.md) für die URL-Zeichenfolge angibt, oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="c41c0-115">Sets or retrieves a **VARIANT** that identifies the [*code page*](glossary.md) for the URL string.</span></span> <span data-ttu-id="c41c0-116">Der Standardwert ist die UTF-8-Codepage.</span><span class="sxs-lookup"><span data-stu-id="c41c0-116">The default value is the UTF-8 code page.</span></span> <span data-ttu-id="c41c0-117">Die Codepage wird verwendet, um die Unicode-URL-Zeichenfolge, die in der [**Open**](iwinhttprequest-open.md) -Methode verwendet wird, in eine Einzel Byte-Zeichen folgen Darstellung zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="c41c0-117">The code page is used to convert the Unicode URL string, passed in the [**Open**](iwinhttprequest-open.md) method, to a single-byte string representation.</span></span>

</dd> <dt>

<span data-ttu-id="c41c0-118"><span id="WinHttpRequestOption_EscapePercentInURL"></span><span id="winhttprequestoption_escapepercentinurl"></span><span id="WINHTTPREQUESTOPTION_ESCAPEPERCENTINURL"></span>**Winhttprequestoption \_ escapeprozentualurl**</span><span class="sxs-lookup"><span data-stu-id="c41c0-118"><span id="WinHttpRequestOption_EscapePercentInURL"></span><span id="winhttprequestoption_escapepercentinurl"></span><span id="WINHTTPREQUESTOPTION_ESCAPEPERCENTINURL"></span>**WinHttpRequestOption\_EscapePercentInURL**</span></span>
</dt> <dd>

<span data-ttu-id="c41c0-119">Legt einen **Variant** -Wert fest, der angibt, ob Prozentzeichen in der URL-Zeichenfolge in eine Escapesequenz konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="c41c0-119">Sets or retrieves a **VARIANT** that indicates whether percent characters in the URL string are converted to an escape sequence.</span></span> <span data-ttu-id="c41c0-120">Der Standardwert dieser Option ist **Variant \_ true** , der alle unsicheren American National Standards Institute (ANSI)-Zeichen angibt, außer das Prozentzeichen wird in eine Escapesequenz konvertiert.</span><span class="sxs-lookup"><span data-stu-id="c41c0-120">The default value of this option is **VARIANT\_TRUE** which specifies all unsafe American National Standards Institute (ANSI) characters except the percent symbol are converted to an escape sequence.</span></span>

</dd> <dt>

<span data-ttu-id="c41c0-121"><span id="WinHttpRequestOption_SslErrorIgnoreFlags"></span><span id="winhttprequestoption_sslerrorignoreflags"></span><span id="WINHTTPREQUESTOPTION_SSLERRORIGNOREFLAGS"></span>**Winhttprequestoption \_ sslerrorignoreflags**</span><span class="sxs-lookup"><span data-stu-id="c41c0-121"><span id="WinHttpRequestOption_SslErrorIgnoreFlags"></span><span id="winhttprequestoption_sslerrorignoreflags"></span><span id="WINHTTPREQUESTOPTION_SSLERRORIGNOREFLAGS"></span>**WinHttpRequestOption\_SslErrorIgnoreFlags**</span></span>
</dt> <dd>

<span data-ttu-id="c41c0-122">Legt einen **Variant** -Wert fest, der angibt, welche Serverzertifikat Fehler ignoriert werden sollen, oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="c41c0-122">Sets or retrieves a **VARIANT** that indicates which server certificate errors should be ignored.</span></span> <span data-ttu-id="c41c0-123">Dabei kann es sich um eine Kombination aus einem oder mehreren der folgenden Flags handeln.</span><span class="sxs-lookup"><span data-stu-id="c41c0-123">This can be a combination of one or more of the following flags.</span></span>



| <span data-ttu-id="c41c0-124">Fehler</span><span class="sxs-lookup"><span data-stu-id="c41c0-124">Error</span></span>                                                  | <span data-ttu-id="c41c0-125">Wert</span><span class="sxs-lookup"><span data-stu-id="c41c0-125">Value</span></span>  |
|--------------------------------------------------------|--------|
| <span data-ttu-id="c41c0-126">Unbekannte Zertifizierungsstelle (Certification Authority, ca) oder nicht vertrauenswürdiger Stamm</span><span class="sxs-lookup"><span data-stu-id="c41c0-126">Unknown certification authority (CA) or untrusted root</span></span> | <span data-ttu-id="c41c0-127">0x0100</span><span class="sxs-lookup"><span data-stu-id="c41c0-127">0x0100</span></span> |
| <span data-ttu-id="c41c0-128">Falsche Verwendung</span><span class="sxs-lookup"><span data-stu-id="c41c0-128">Wrong usage</span></span>                                            | <span data-ttu-id="c41c0-129">0x0200</span><span class="sxs-lookup"><span data-stu-id="c41c0-129">0x0200</span></span> |
| <span data-ttu-id="c41c0-130">Ungültiger allgemeiner Name (Common Name, CN)</span><span class="sxs-lookup"><span data-stu-id="c41c0-130">Invalid common name (CN)</span></span>                               | <span data-ttu-id="c41c0-131">0x1000</span><span class="sxs-lookup"><span data-stu-id="c41c0-131">0x1000</span></span> |
| <span data-ttu-id="c41c0-132">Ungültiges Datum oder Zertifikat abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="c41c0-132">Invalid date or certificate expired</span></span>                    | <span data-ttu-id="c41c0-133">0x2000</span><span class="sxs-lookup"><span data-stu-id="c41c0-133">0x2000</span></span> |



 

<span data-ttu-id="c41c0-134">Der Standardwert dieser Option in Version 5,1 von WinHTTP ist 0 (null), was dazu führt, dass keine Fehler ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="c41c0-134">The default value of this option in Version 5.1 of WinHTTP is zero, which results in no errors being ignored.</span></span> <span data-ttu-id="c41c0-135">In früheren Versionen von WinHTTP war die Standardeinstellung 0x3300, was dazu geführt hat, dass alle Serverzertifikat Fehler standardmäßig ignoriert wurden.</span><span class="sxs-lookup"><span data-stu-id="c41c0-135">In earlier versions of WinHTTP, the default setting was 0x3300, which resulted in all server certificate errors being ignored by default.</span></span>

</dd> <dt>

<span data-ttu-id="c41c0-136"><span id="WinHttpRequestOption_SelectCertificate"></span><span id="winhttprequestoption_selectcertificate"></span><span id="WINHTTPREQUESTOPTION_SELECTCERTIFICATE"></span>**Winhttprequestoption \_ selectcertificate**</span><span class="sxs-lookup"><span data-stu-id="c41c0-136"><span id="WinHttpRequestOption_SelectCertificate"></span><span id="winhttprequestoption_selectcertificate"></span><span id="WINHTTPREQUESTOPTION_SELECTCERTIFICATE"></span>**WinHttpRequestOption\_SelectCertificate**</span></span>
</dt> <dd>

<span data-ttu-id="c41c0-137">Legt einen **Variant** -Wert fest, der das Client Zertifikat angibt, das zur Authentifizierung an einen Server gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="c41c0-137">Sets a **VARIANT** that specifies the client certificate that is sent to a server for authentication.</span></span> <span data-ttu-id="c41c0-138">Diese Option gibt den Speicherort, den [*Zertifikat Speicher*](glossary.md)und den Betreff eines Client Zertifikats an, das mit umgekehrten Schrägstrichen getrennt ist.</span><span class="sxs-lookup"><span data-stu-id="c41c0-138">This option indicates the location, [*certificate store*](glossary.md), and subject of a client certificate delimited with backslashes.</span></span> <span data-ttu-id="c41c0-139">Weitere Informationen zum Auswählen eines Client Zertifikats finden Sie unter [SSL in WinHTTP](ssl-in-winhttp.md).</span><span class="sxs-lookup"><span data-stu-id="c41c0-139">For more information about selecting a client certificate, see [SSL in WinHTTP](ssl-in-winhttp.md).</span></span>

</dd> <dt>

<span data-ttu-id="c41c0-140"><span id="WinHttpRequestOption_EnableRedirects"></span><span id="winhttprequestoption_enableredirects"></span><span id="WINHTTPREQUESTOPTION_ENABLEREDIRECTS"></span>**Winhttprequestoption \_ enablereumleitungen**</span><span class="sxs-lookup"><span data-stu-id="c41c0-140"><span id="WinHttpRequestOption_EnableRedirects"></span><span id="winhttprequestoption_enableredirects"></span><span id="WINHTTPREQUESTOPTION_ENABLEREDIRECTS"></span>**WinHttpRequestOption\_EnableRedirects**</span></span>
</dt> <dd>

<span data-ttu-id="c41c0-141">Legt einen **Variant** -Wert fest, der angibt, ob Anforderungen automatisch umgeleitet werden, wenn der Server einen neuen Speicherort für die Ressource angibt, oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="c41c0-141">Sets or retrieves a **VARIANT** that indicates whether requests are automatically redirected when the server specifies a new location for the resource.</span></span> <span data-ttu-id="c41c0-142">Der Standardwert dieser Option ist **Variant \_ true** , um anzugeben, dass Anforderungen automatisch umgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="c41c0-142">The default value of this option is **VARIANT\_TRUE** to indicate that requests are automatically redirected.</span></span>

</dd> <dt>

<span data-ttu-id="c41c0-143"><span id="WinHttpRequestOption_UrlEscapeDisable"></span><span id="winhttprequestoption_urlescapedisable"></span><span id="WINHTTPREQUESTOPTION_URLESCAPEDISABLE"></span>**Winhttprequestoption \_ urlescapedeaktiviert**</span><span class="sxs-lookup"><span data-stu-id="c41c0-143"><span id="WinHttpRequestOption_UrlEscapeDisable"></span><span id="winhttprequestoption_urlescapedisable"></span><span id="WINHTTPREQUESTOPTION_URLESCAPEDISABLE"></span>**WinHttpRequestOption\_UrlEscapeDisable**</span></span>
</dt> <dd>

<span data-ttu-id="c41c0-144">Legt einen **Variant** -Wert fest, der angibt, ob unsichere Zeichen in den Pfad-und Abfrage Komponenten einer URL in Escapesequenzen konvertiert werden, oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="c41c0-144">Sets or retrieves a **VARIANT** that indicates whether unsafe characters in the path and query components of a URL are converted to escape sequences.</span></span> <span data-ttu-id="c41c0-145">Der Standardwert dieser Option ist **Variant \_ true**, das angibt, dass die Zeichen im Pfad und in der Abfrage konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="c41c0-145">The default value of this option is **VARIANT\_TRUE**, which specifies that characters in the path and query are converted.</span></span>

</dd> <dt>

<span data-ttu-id="c41c0-146"><span id="WinHttpRequestOption_UrlEscapeDisableQuery"></span><span id="winhttprequestoption_urlescapedisablequery"></span><span id="WINHTTPREQUESTOPTION_URLESCAPEDISABLEQUERY"></span>**Winhttprequestoption \_ urlescapedisablequery**</span><span class="sxs-lookup"><span data-stu-id="c41c0-146"><span id="WinHttpRequestOption_UrlEscapeDisableQuery"></span><span id="winhttprequestoption_urlescapedisablequery"></span><span id="WINHTTPREQUESTOPTION_URLESCAPEDISABLEQUERY"></span>**WinHttpRequestOption\_UrlEscapeDisableQuery**</span></span>
</dt> <dd>

<span data-ttu-id="c41c0-147">Legt einen **Variant** -Wert fest, der angibt, ob unsichere Zeichen in der Abfrage Komponente der URL in Escapesequenzen konvertiert werden, oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="c41c0-147">Sets or retrieves a **VARIANT** that indicates whether unsafe characters in the query component of the URL are converted to escape sequences.</span></span> <span data-ttu-id="c41c0-148">Der Standardwert dieser Option ist **Variant \_ true**, das angibt, dass Zeichen in der Abfrage konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="c41c0-148">The default value of this option is **VARIANT\_TRUE**, which specifies that characters in the query are converted.</span></span>

</dd> <dt>

<span data-ttu-id="c41c0-149"><span id="WinHttpRequestOption_SecureProtocols"></span><span id="winhttprequestoption_secureprotocols"></span><span id="WINHTTPREQUESTOPTION_SECUREPROTOCOLS"></span>**Winhttprequestoption \_ secureprotokolls**</span><span class="sxs-lookup"><span data-stu-id="c41c0-149"><span id="WinHttpRequestOption_SecureProtocols"></span><span id="winhttprequestoption_secureprotocols"></span><span id="WINHTTPREQUESTOPTION_SECUREPROTOCOLS"></span>**WinHttpRequestOption\_SecureProtocols**</span></span>
</dt> <dd>

<span data-ttu-id="c41c0-150">Legt einen **Variant** -Wert fest, der angibt, welche sicheren Protokolle verwendet werden können, oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="c41c0-150">Sets or retrieves a **VARIANT** that indicates which secure protocols can be used.</span></span> <span data-ttu-id="c41c0-151">Mit dieser Option werden die für den Client zulässigen Protokolle ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="c41c0-151">This option selects the protocols acceptable to the client.</span></span> <span data-ttu-id="c41c0-152">Das Protokoll wird während des Secure Sockets Layer (SSL)-Handshake ausgehandelt.</span><span class="sxs-lookup"><span data-stu-id="c41c0-152">The protocol is negotiated during the Secure Sockets Layer (SSL) handshake.</span></span> <span data-ttu-id="c41c0-153">Dabei kann es sich um eine Kombination aus einem oder mehreren der folgenden Flags handeln.</span><span class="sxs-lookup"><span data-stu-id="c41c0-153">This can be a combination of one or more of the following flags.</span></span>



| <span data-ttu-id="c41c0-154">Protokoll</span><span class="sxs-lookup"><span data-stu-id="c41c0-154">Protocol</span></span>                           | <span data-ttu-id="c41c0-155">Wert</span><span class="sxs-lookup"><span data-stu-id="c41c0-155">Value</span></span>  |
|------------------------------------|--------|
| <span data-ttu-id="c41c0-156">SSL 2.0</span><span class="sxs-lookup"><span data-stu-id="c41c0-156">SSL 2.0</span></span>                            | <span data-ttu-id="c41c0-157">0x0008</span><span class="sxs-lookup"><span data-stu-id="c41c0-157">0x0008</span></span> |
| <span data-ttu-id="c41c0-158">SSL 3.0</span><span class="sxs-lookup"><span data-stu-id="c41c0-158">SSL 3.0</span></span>                            | <span data-ttu-id="c41c0-159">0x0020</span><span class="sxs-lookup"><span data-stu-id="c41c0-159">0x0020</span></span> |
| <span data-ttu-id="c41c0-160">Transport Layer Security (TLS) 1,0</span><span class="sxs-lookup"><span data-stu-id="c41c0-160">Transport Layer Security (TLS) 1.0</span></span> | <span data-ttu-id="c41c0-161">0x0080</span><span class="sxs-lookup"><span data-stu-id="c41c0-161">0x0080</span></span> |



 

<span data-ttu-id="c41c0-162">Der Standardwert dieser Option ist 0x0028 und gibt an, dass SSL 2,0 oder SSL 3,0 verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="c41c0-162">The default value of this option is 0x0028, which indicates that SSL 2.0 or SSL 3.0 can be used.</span></span> <span data-ttu-id="c41c0-163">Wenn diese Option auf NULL festgelegt ist, können der Client und der Server kein akzeptables Sicherheitsprotokoll ermitteln, und der nächste [**Sende**](iwinhttprequest-send.md) Vorgang führt zu einem Fehler.</span><span class="sxs-lookup"><span data-stu-id="c41c0-163">If this option is set to zero, the client and server are not able to determine an acceptable security protocol and the next [**Send**](iwinhttprequest-send.md) results in an error.</span></span>

</dd> <dt>

<span data-ttu-id="c41c0-164"><span id="WinHttpRequestOption_EnableTracing"></span><span id="winhttprequestoption_enabletracing"></span><span id="WINHTTPREQUESTOPTION_ENABLETRACING"></span>**Winhttprequestoption \_ EnableTracing**</span><span class="sxs-lookup"><span data-stu-id="c41c0-164"><span id="WinHttpRequestOption_EnableTracing"></span><span id="winhttprequestoption_enabletracing"></span><span id="WINHTTPREQUESTOPTION_ENABLETRACING"></span>**WinHttpRequestOption\_EnableTracing**</span></span>
</dt> <dd>

<span data-ttu-id="c41c0-165">Legt einen **Variant** fest oder ruft ihn ab, der angibt, ob die Ablauf Verfolgung derzeit aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="c41c0-165">Sets or retrieves a **VARIANT** that indicates whether tracing is currently enabled.</span></span> <span data-ttu-id="c41c0-166">Weitere Informationen zur Ablauf Verfolgungs Funktion in den Microsoft Windows HTTP-Diensten (WinHTTP) finden Sie unter [WinHTTP-Ablauf Verfolgungs Funktion](winhttptracecfg-exe--a-trace-configuration-tool.md).</span><span class="sxs-lookup"><span data-stu-id="c41c0-166">For more information about the trace facility in Microsoft Windows HTTP Services (WinHTTP), see [WinHTTP Trace Facility](winhttptracecfg-exe--a-trace-configuration-tool.md).</span></span>

</dd> <dt>

<span data-ttu-id="c41c0-167"><span id="WinHttpRequestOption_RevertImpersonationOverSsl"></span><span id="winhttprequestoption_revertimpersonationoverssl"></span><span id="WINHTTPREQUESTOPTION_REVERTIMPERSONATIONOVERSSL"></span>**Winhttprequestoption \_ revertimpersonationoverssl**</span><span class="sxs-lookup"><span data-stu-id="c41c0-167"><span id="WinHttpRequestOption_RevertImpersonationOverSsl"></span><span id="winhttprequestoption_revertimpersonationoverssl"></span><span id="WINHTTPREQUESTOPTION_REVERTIMPERSONATIONOVERSSL"></span>**WinHttpRequestOption\_RevertImpersonationOverSsl**</span></span>
</dt> <dd>

<span data-ttu-id="c41c0-168">Steuert, ob das [**WinHttpRequest**](winhttprequest.md) -Objekt den Client Identitätswechsel vorübergehend für die Dauer der SSL-Zertifikat Authentifizierungs Vorgänge zurücksetzt.</span><span class="sxs-lookup"><span data-stu-id="c41c0-168">Controls whether the [**WinHttpRequest**](winhttprequest.md) object temporarily reverts client impersonation for the duration of the SSL certificate authentication operations.</span></span> <span data-ttu-id="c41c0-169">Die Standardeinstellung für das **WinHttpRequest** -Objekt ist " **true**".</span><span class="sxs-lookup"><span data-stu-id="c41c0-169">The default setting for the **WinHttpRequest** object is **TRUE**.</span></span> <span data-ttu-id="c41c0-170">Legen Sie diese Option auf **false** fest, um den Identitätswechsel beim Ausführen von Zertifikat Authentifizierungs Vorgängen beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="c41c0-170">Set this option to **FALSE** to keep impersonation while performing certificate authentication operations.</span></span>

</dd> <dt>

<span data-ttu-id="c41c0-171"><span id="WinHttpRequestOption_EnableHttpsToHttpRedirects"></span><span id="winhttprequestoption_enablehttpstohttpredirects"></span><span id="WINHTTPREQUESTOPTION_ENABLEHTTPSTOHTTPREDIRECTS"></span>**Winhttprequestoption \_ enablehttpstohttpredirektionen**</span><span class="sxs-lookup"><span data-stu-id="c41c0-171"><span id="WinHttpRequestOption_EnableHttpsToHttpRedirects"></span><span id="winhttprequestoption_enablehttpstohttpredirects"></span><span id="WINHTTPREQUESTOPTION_ENABLEHTTPSTOHTTPREDIRECTS"></span>**WinHttpRequestOption\_EnableHttpsToHttpRedirects**</span></span>
</dt> <dd>

<span data-ttu-id="c41c0-172">Steuert, ob WinHTTP Umleitungen zulässt.</span><span class="sxs-lookup"><span data-stu-id="c41c0-172">Controls whether or not WinHTTP allows redirects.</span></span> <span data-ttu-id="c41c0-173">Standardmäßig werden alle Umleitungen automatisch befolgt, mit Ausnahme derjenigen, die von einer sicheren URL (HTTPS) an eine nicht sichere URL (http) übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="c41c0-173">By default, all redirects are automatically followed, except those that transfer from a secure (https) URL to an non-secure (http) URL.</span></span> <span data-ttu-id="c41c0-174">Legen Sie diese Option auf " **true** " fest, um HTTPS-HTTP-Umleitungen zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="c41c0-174">Set this option to **TRUE** to enable HTTPS to HTTP redirects.</span></span>

</dd> <dt>

<span data-ttu-id="c41c0-175"><span id="WinHttpRequestOption_EnablePassportAuthentication"></span><span id="winhttprequestoption_enablepassportauthentication"></span><span id="WINHTTPREQUESTOPTION_ENABLEPASSPORTAUTHENTICATION"></span>**Winhttprequestoption \_ enablepassportauthentication**</span><span class="sxs-lookup"><span data-stu-id="c41c0-175"><span id="WinHttpRequestOption_EnablePassportAuthentication"></span><span id="winhttprequestoption_enablepassportauthentication"></span><span id="WINHTTPREQUESTOPTION_ENABLEPASSPORTAUTHENTICATION"></span>**WinHttpRequestOption\_EnablePassportAuthentication**</span></span>
</dt> <dd>

<span data-ttu-id="c41c0-176">Aktiviert oder deaktiviert die Unterstützung für die Passport-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="c41c0-176">Enables or disables support for Passport authentication.</span></span> <span data-ttu-id="c41c0-177">Standardmäßig ist die automatische Unterstützung für die Passport-Authentifizierung deaktiviert. Legen Sie diese Option auf **true** fest, um die Unterstützung der Passport-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="c41c0-177">By default, automatic support for Passport authentication is disabled; set this option to **TRUE** to enable Passport authentication support.</span></span>

</dd> <dt>

<span data-ttu-id="c41c0-178"><span id="WinHttpRequestOption_MaxAutomaticRedirects"></span><span id="winhttprequestoption_maxautomaticredirects"></span><span id="WINHTTPREQUESTOPTION_MAXAUTOMATICREDIRECTS"></span>**Winhttprequestoption \_ maxautomatikreumleitungen**</span><span class="sxs-lookup"><span data-stu-id="c41c0-178"><span id="WinHttpRequestOption_MaxAutomaticRedirects"></span><span id="winhttprequestoption_maxautomaticredirects"></span><span id="WINHTTPREQUESTOPTION_MAXAUTOMATICREDIRECTS"></span>**WinHttpRequestOption\_MaxAutomaticRedirects**</span></span>
</dt> <dd>

<span data-ttu-id="c41c0-179">Legt die maximale Anzahl von Umleitungen fest, die WinHTTP befolgt, oder ruft Sie ab. der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="c41c0-179">Sets or retrieves the maximum number of redirects that WinHTTP follows; the default is 10.</span></span> <span data-ttu-id="c41c0-180">Diese Beschränkung verhindert, dass nicht autorisierte Standorte den WinHTTP-Client Stall nach einer großen Anzahl von Umleitungen durchführen.</span><span class="sxs-lookup"><span data-stu-id="c41c0-180">This limit prevents unauthorized sites from making the WinHTTP client stall following a large number of redirects.</span></span>

<span data-ttu-id="c41c0-181">**Windows XP mit SP1 und Windows 2000 mit SP3:** Dieser Enumerationswert wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c41c0-181">**Windows XP with SP1 and Windows 2000 with SP3:** This enumeration value is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="c41c0-182"><span id="WinHttpRequestOption_MaxResponseHeaderSize"></span><span id="winhttprequestoption_maxresponseheadersize"></span><span id="WINHTTPREQUESTOPTION_MAXRESPONSEHEADERSIZE"></span>**Winhttprequestoption \_ maxresponsheadersize**</span><span class="sxs-lookup"><span data-stu-id="c41c0-182"><span id="WinHttpRequestOption_MaxResponseHeaderSize"></span><span id="winhttprequestoption_maxresponseheadersize"></span><span id="WINHTTPREQUESTOPTION_MAXRESPONSEHEADERSIZE"></span>**WinHttpRequestOption\_MaxResponseHeaderSize**</span></span>
</dt> <dd>

<span data-ttu-id="c41c0-183">Legt eine gebundene Menge für die maximale Größe des Header Teils der Serverantwort fest oder ruft diese ab.</span><span class="sxs-lookup"><span data-stu-id="c41c0-183">Sets or retrieves a bound set on the maximum size of the header portion of the server's response.</span></span> <span data-ttu-id="c41c0-184">Diese Bindung schützt den Client vor einem böswilligen Server, der versucht, den Client zu stoppen, indem er eine Antwort mit einer unendlichen Menge von Header Daten sendet.</span><span class="sxs-lookup"><span data-stu-id="c41c0-184">This bound protects the client from a malicious server attempting to stall the client by sending a response with an infinite amount of header data.</span></span> <span data-ttu-id="c41c0-185">Der Standardwert ist 64 KB.</span><span class="sxs-lookup"><span data-stu-id="c41c0-185">The default value is 64 KB.</span></span>

<span data-ttu-id="c41c0-186">**Windows XP mit SP1 und Windows 2000 mit SP3:** Dieser Enumerationswert wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c41c0-186">**Windows XP with SP1 and Windows 2000 with SP3:** This enumeration value is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="c41c0-187"><span id="WinHttpRequestOption_MaxResponseDrainSize"></span><span id="winhttprequestoption_maxresponsedrainsize"></span><span id="WINHTTPREQUESTOPTION_MAXRESPONSEDRAINSIZE"></span>**Winhttprequestoption \_ maxresponsdrainsize**</span><span class="sxs-lookup"><span data-stu-id="c41c0-187"><span id="WinHttpRequestOption_MaxResponseDrainSize"></span><span id="winhttprequestoption_maxresponsedrainsize"></span><span id="WINHTTPREQUESTOPTION_MAXRESPONSEDRAINSIZE"></span>**WinHttpRequestOption\_MaxResponseDrainSize**</span></span>
</dt> <dd>

<span data-ttu-id="c41c0-188">Legt eine gebundene Datenmenge fest oder ruft Sie ab, um eine Verbindung wiederzuverwenden.</span><span class="sxs-lookup"><span data-stu-id="c41c0-188">Sets or retrieves a bound on the amount of data that will be drained from responses in order to reuse a connection.</span></span> <span data-ttu-id="c41c0-189">Die Standardeinstellung ist 1 MB.</span><span class="sxs-lookup"><span data-stu-id="c41c0-189">The default is 1 MB.</span></span>

<span data-ttu-id="c41c0-190">**Windows XP mit SP1 und Windows 2000 mit SP3:** Dieser Enumerationswert wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c41c0-190">**Windows XP with SP1 and Windows 2000 with SP3:** This enumeration value is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="c41c0-191"><span id="WinHttpRequestOption_EnableHttp1_1"></span><span id="winhttprequestoption_enablehttp1_1"></span><span id="WINHTTPREQUESTOPTION_ENABLEHTTP1_1"></span>**Winhttprequestoption \_ EnableHttp1 \_ 1**</span><span class="sxs-lookup"><span data-stu-id="c41c0-191"><span id="WinHttpRequestOption_EnableHttp1_1"></span><span id="winhttprequestoption_enablehttp1_1"></span><span id="WINHTTPREQUESTOPTION_ENABLEHTTP1_1"></span>**WinHttpRequestOption\_EnableHttp1\_1**</span></span>
</dt> <dd>

<span data-ttu-id="c41c0-192">Legt einen booleschen Wert fest, der angibt, ob HTTP/1.1 oder http/1.0 verwendet werden soll, oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="c41c0-192">Sets or retrieves a boolean value that indicates whether HTTP/1.1 or HTTP/1.0 should be used.</span></span> <span data-ttu-id="c41c0-193">Der Standardwert ist " **true**", sodass "http/1.1" standardmäßig verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c41c0-193">The default is **TRUE**, so that HTTP/1.1 is used by default.</span></span>

<span data-ttu-id="c41c0-194">**Windows XP mit SP1 und Windows 2000 mit SP3:** Dieser Enumerationswert wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c41c0-194">**Windows XP with SP1 and Windows 2000 with SP3:** This enumeration value is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="c41c0-195"><span id="WinHttpRequestOption_EnableCertificateRevocationCheck"></span><span id="winhttprequestoption_enablecertificaterevocationcheck"></span><span id="WINHTTPREQUESTOPTION_ENABLECERTIFICATEREVOCATIONCHECK"></span>**Winhttprequestoption \_ enablecertificaterevocationcheck**</span><span class="sxs-lookup"><span data-stu-id="c41c0-195"><span id="WinHttpRequestOption_EnableCertificateRevocationCheck"></span><span id="winhttprequestoption_enablecertificaterevocationcheck"></span><span id="WINHTTPREQUESTOPTION_ENABLECERTIFICATEREVOCATIONCHECK"></span>**WinHttpRequestOption\_EnableCertificateRevocationCheck**</span></span>
</dt> <dd>

<span data-ttu-id="c41c0-196">Aktiviert die Serverzertifikat Sperr Überprüfung während der SSL-Aushandlung.</span><span class="sxs-lookup"><span data-stu-id="c41c0-196">Enables server certificate revocation checking during SSL negotiation.</span></span> <span data-ttu-id="c41c0-197">Wenn der Server ein Zertifikat anzeigt, wird eine Überprüfung durchgeführt, um zu bestimmen, ob das Zertifikat vom Aussteller widerrufen wurde.</span><span class="sxs-lookup"><span data-stu-id="c41c0-197">When the server presents a certificate, a check is performed to determine whether the certificate has been revoked by its issuer.</span></span> <span data-ttu-id="c41c0-198">Wenn das Zertifikat tatsächlich widerrufen wird oder die Sperr Überprüfung fehlschlägt, weil die Zertifikat Sperr Liste nicht heruntergeladen werden kann, schlägt die Anforderung fehl. solche Sperr Fehler können nicht unterdrückt werden.</span><span class="sxs-lookup"><span data-stu-id="c41c0-198">If the certificate is indeed revoked, or the revocation check fails because the Certificate Revocation List (CRL) cannot be downloaded, the request fails; such revocation errors cannot be suppressed.</span></span>

<span data-ttu-id="c41c0-199">**Windows XP mit SP1 und Windows 2000 mit SP3:** Dieser Enumerationswert wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c41c0-199">**Windows XP with SP1 and Windows 2000 with SP3:** This enumeration value is not supported.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c41c0-200">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c41c0-200">Remarks</span></span>

<span data-ttu-id="c41c0-201">Legen Sie eine Option fest, indem Sie eine der vorangehenden Konstanten als Parameter der [**Option**](iwinhttprequest-option.md) -Eigenschaft angeben.</span><span class="sxs-lookup"><span data-stu-id="c41c0-201">Set an option by specifying one of the preceding constants as the parameter of the [**Option**](iwinhttprequest-option.md) property.</span></span>

> [!Note]  
> <span data-ttu-id="c41c0-202">Informationen zu Windows XP und Windows 2000 finden Sie im Abschnitt [Lauf Zeitanforderungen](winhttp-start-page.md) auf der WinHTTP-Startseite.</span><span class="sxs-lookup"><span data-stu-id="c41c0-202">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHttp start page.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c41c0-203">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c41c0-203">Requirements</span></span>



| <span data-ttu-id="c41c0-204">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c41c0-204">Requirement</span></span> | <span data-ttu-id="c41c0-205">Wert</span><span class="sxs-lookup"><span data-stu-id="c41c0-205">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="c41c0-206">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c41c0-206">Minimum supported client</span></span><br/> | <span data-ttu-id="c41c0-207">Windows XP, Windows 2000 Professional mit SP3 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c41c0-207">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="c41c0-208">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c41c0-208">Minimum supported server</span></span><br/> | <span data-ttu-id="c41c0-209">Windows Server 2003, Windows 2000-Server mit \[ nur SP3-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c41c0-209">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="c41c0-210">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="c41c0-210">Redistributable</span></span><br/>          | <span data-ttu-id="c41c0-211">WinHTTP 5,0 und Internet Explorer 5,01 oder höher unter Windows XP und Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="c41c0-211">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="c41c0-212">IDL</span><span class="sxs-lookup"><span data-stu-id="c41c0-212">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c41c0-213"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c41c0-213"><dt>HttpRequest.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c41c0-214">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c41c0-214">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c41c0-215">WinHTTP-Versionen</span><span class="sxs-lookup"><span data-stu-id="c41c0-215">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




