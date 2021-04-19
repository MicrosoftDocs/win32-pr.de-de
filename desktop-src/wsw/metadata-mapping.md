---
title: Metadatenzuordnung
description: Der Inhalt eines Metadatendokuments wird der Metadaten-API auf die in den folgenden Abschnitten erläuterten Methoden zugeordnet.
ms.assetid: 266f8319-b7ac-497f-8eb7-8e2c7bcede33
keywords:
- Webdienste für die metadatenzuordnung für Windows
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb9da067768569e78ba6bb98ee219e11917d3201
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "106341756"
---
# <a name="metadata-mapping"></a><span data-ttu-id="3a53e-106">Metadatenzuordnung</span><span class="sxs-lookup"><span data-stu-id="3a53e-106">Metadata Mapping</span></span>

<span data-ttu-id="3a53e-107">Der Inhalt eines Metadatendokuments wird der Metadaten-API auf die in den folgenden Abschnitten erläuterten Methoden zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="3a53e-107">The contents of a metadata document map to the metadata API in the ways explained in the following sections.</span></span>


<span data-ttu-id="3a53e-108">Die folgenden Namespace Präfixe werden in dieser Dokumentation verwendet:</span><span class="sxs-lookup"><span data-stu-id="3a53e-108">The following namespace prefixes are used throughout this documentation:</span></span>

``` syntax
wsdl   => http://schemas.xmlsoap.org/wsdl/
soap11 => http://schemas.xmlsoap.org/wsdl/soap/
soap12 => http://schemas.xmlsoap.org/wsdl/soap12/
wsa09  => http://schemas.xmlsoap.org/ws/2004/08/addressing
wsa10  => http://www.w3.org/2005/08/addressing
wsa09p => http://schemas.xmlsoap.org/ws/2004/08/addressing/policy
wsa10p => http://www.w3.org/2006/05/addressing/wsdl
binp   => http://schemas.microsoft.com/ws/06/2004/mspolicy/netbinary1
mtomp  => http://schemas.xmlsoap.org/ws/2004/09/policy/optimizedmimeserialization
sp     => http://schemas.xmlsoap.org/ws/2005/07/securitypolicy
wsp    => http://schemas.xmlsoap.org/ws/2004/09/policy
netf   => http://schemas.microsoft.com/ws/2006/05/framing/policy
httpp  => http://schemas.microsoft.com/ws/06/2004/policy/http
wst10  => http://schemas.xmlsoap.org/ws/2005/02/trust
wsi    => http://schemas.xmlsoap.org/ws/2005/05/identity
```

<span data-ttu-id="3a53e-109">In den nachfolgenden Abschnitten werden API-Konstrukte sowie die entsprechenden Metadatenkonstrukte (WSDL oder Richtlinie) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="3a53e-109">The subsequent sections describe API constructs along with what metadata constructs (WSDL or Policy) they correspond to.</span></span>

<span data-ttu-id="3a53e-110">Kenntnisse in Bezug auf Metadatenspezifikationen wie WSDL und die Richtlinie erleichtern das Verständnis dieses Abschnitts.</span><span class="sxs-lookup"><span data-stu-id="3a53e-110">Familiarity with metadata specifications such as WSDL and Policy will aid in understanding this section.</span></span>

## <a name="endpoint-address"></a><span data-ttu-id="3a53e-111">Endpunkt Adresse</span><span class="sxs-lookup"><span data-stu-id="3a53e-111">Endpoint address</span></span>

<span data-ttu-id="3a53e-112">Die Adresse eines Endpunkts (siehe [**WS- \_ Endpunkt \_ Adresse**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address)) wird von einem Erweiterbarkeits Element im WSDL: Port-Element des WSDL-Dokuments abgerufen.</span><span class="sxs-lookup"><span data-stu-id="3a53e-112">The address of an endpoint (see [**WS\_ENDPOINT\_ADDRESS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address)) is obtained from an extensibility element within the wsdl:port element of the WSDL document.</span></span> <span data-ttu-id="3a53e-113">Die folgenden Erweiterbarkeits Elemente werden zum Angeben der Adresse unterstützt:</span><span class="sxs-lookup"><span data-stu-id="3a53e-113">The following extensibility elements are supported for specifying the address:</span></span>

``` syntax
<wsdl:port...>
    <soap11:address.../>
</wsdl:port>
```

``` syntax
<wsdl:port...>
    <soap12:address.../>
</wsdl:port>
```

``` syntax
<wsdl:port...>
    <wsa09:EndpointReference.../>
</wsdl:port>
```

``` syntax
<wsdl:port...>
    <wsa10:EndpointReference.../>
</wsdl:port>
```

## <a name="ws_channel_binding"></a><span data-ttu-id="3a53e-114">WS- \_ Kanal \_ Bindung</span><span class="sxs-lookup"><span data-stu-id="3a53e-114">WS\_CHANNEL\_BINDING</span></span>

<span data-ttu-id="3a53e-115">Die kanalbindung (siehe [**WS \_ - \_ channelbindung**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)) wird wie folgt durch den Transport der verwendeten SOAP-Bindung bestimmt:</span><span class="sxs-lookup"><span data-stu-id="3a53e-115">The channel binding (see [**WS\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)) is determined by the transport the soap binding used, as follows:</span></span>

``` syntax
<soap:binding transport=&quot;http://schemas.microsoft.com/soap/tcp&quot;/> => WS_TCP_CHANNEL_BINDING
```

``` syntax
<soap:binding transport=&quot;http://schemas.xmlsoap.org/soap/http&quot;/> => WS_HTTP_CHANNEL_BINDING
```

## <a name="ws_channel_property_envelope_version"></a><span data-ttu-id="3a53e-116">Umschlag Version der WS- \_ Kanal \_ Eigenschaft \_ \_</span><span class="sxs-lookup"><span data-stu-id="3a53e-116">WS\_CHANNEL\_PROPERTY\_ENVELOPE\_VERSION</span></span>

<span data-ttu-id="3a53e-117">Die Umschlag Version (siehe [**WS \_ - \_ Channeleigenschaft \_ Umschlag \_ Version**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)) wird wie folgt bestimmt, wie die SOAP-Bindung verwendet wird:</span><span class="sxs-lookup"><span data-stu-id="3a53e-117">The envelope version (see [**WS\_CHANNEL\_PROPERTY\_ENVELOPE\_VERSION**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)) is determined by which soap binding is used, as follows:</span></span>

``` syntax
<wsdl:binding...>
    <soap11:binding.../> => WS_ENVELOPE_VERSION_SOAP_1_1
</wsdl:binding>
```

``` syntax
<wsdl:binding...>
    <soap12:binding.../> => WS_ENVELOPE_VERSION_SOAP_1_2
</wsdl:binding>
```

## <a name="addressing-version"></a><span data-ttu-id="3a53e-118">Adressierungs Version</span><span class="sxs-lookup"><span data-stu-id="3a53e-118">Addressing Version</span></span>

<span data-ttu-id="3a53e-119">Die Adressierungs Version (siehe die [**\_ \_ \_ Adressierungs \_ Version der WS-Kanal Eigenschaft**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)) wird durch die folgenden Assertionen in der Endpunkt Richtlinie bestimmt:</span><span class="sxs-lookup"><span data-stu-id="3a53e-119">The addressing version (see [**WS\_CHANNEL\_PROPERTY\_ADDRESSING\_VERSION**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)) is determined by the following assertions in the endpoint policy:</span></span>

``` syntax
<wsp:Policy...>
    <wsa09p:UsingAddressing.../> => WS_ADDRESSING_VERSION_0_9
</wsp:Policy>
```

``` syntax
<wsp:Policy...>
    <wsa10p:UsingAddressing.../> => WS_ADDRESSING_VERSION_1_0
</wsp:Policy>
```

<span data-ttu-id="3a53e-120">Wenn keine Adressierungs Erklärung vorhanden ist, wird von der [**WS- \_ Adressierungs \_ Versions \_ Transport**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) ausgegangen.</span><span class="sxs-lookup"><span data-stu-id="3a53e-120">If an addressing assertion is not present, then [**WS\_ADDRESSING\_VERSION\_TRANSPORT**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) is assumed.</span></span>

## <a name="message-encoding"></a><span data-ttu-id="3a53e-121">Nachrichtenverschlüsselung</span><span class="sxs-lookup"><span data-stu-id="3a53e-121">Message Encoding</span></span>

<span data-ttu-id="3a53e-122">Die Codierung der Nachricht (siehe [**WS- \_ \_ channeleigenschaftencodierung \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)) wird durch die folgenden Assertionen in der Endpunkt Richtlinie bestimmt:</span><span class="sxs-lookup"><span data-stu-id="3a53e-122">The encoding of the message (see [**WS\_CHANNEL\_PROPERTY\_ENCODING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)) is determined by the following assertions in the endpoint policy:</span></span>

``` syntax
<wsp:Policy...>
    <binp:BinaryEncoding.../> => WS_ENCODING_XML_BINARY_SESSION_1, WS_ENCODING_XML_BINARY_1
</wsp:Policy>
```

<span data-ttu-id="3a53e-123">Beachten Sie, dass die Richtlinien Assertionen für binäre Codierungen keine Informationen darüber enthalten, ob die binäre Codierung Sitzungs basiert oder Sitzungs unabhängig ist.</span><span class="sxs-lookup"><span data-stu-id="3a53e-123">Note that the binary encoding policy assertion does not include information about whether the binary encoding is sessionful or sessionless.</span></span> <span data-ttu-id="3a53e-124">Dies wird durch die Codierungs Eigenschafts Einschränkung bestimmt (die entsprechend der Verwendung des verwendeten WS- [**\_ \_ Kanaltyps**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) angemessen ist oder nicht).</span><span class="sxs-lookup"><span data-stu-id="3a53e-124">This is determined by the encoding property constraint (which should be appropriate according to whether or not the [**WS\_CHANNEL\_TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) being used is sessionful or not).</span></span>

``` syntax
<wsp:Policy...>
    <mtomp:OptimizedMimeSerialization.../> => WS_ENCODING_XML_MTOM_UTF8, WS_ENCODING_XML_MTOM_UTF16LE, WS_ENCODING_XML_MTOM_UTF16BE
</wsp:Policy>
```

<span data-ttu-id="3a53e-125">Wenn keine der obigen Assertionen vorhanden ist, wird eine Text Codierung verwendet: [**WS \_ Encoding \_ XML \_ UTF8**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding), **WS \_ Encoding \_ XML \_ UTF16LE**, **WS \_ Encoding \_ XML \_ UTF16BE**.</span><span class="sxs-lookup"><span data-stu-id="3a53e-125">If neither of the above assertions are present, then a text encoding is used: [**WS\_ENCODING\_XML\_UTF8**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding), **WS\_ENCODING\_XML\_UTF16LE**, **WS\_ENCODING\_XML\_UTF16BE**.</span></span>

<span data-ttu-id="3a53e-126">Beachten Sie, dass die Richtlinie keine Informationen über den Zeichensatz für MTOM oder Text Codierungen enthält (d. h. UTF8, UTF16LE oder UTF16BE).</span><span class="sxs-lookup"><span data-stu-id="3a53e-126">Note that policy does not include information about the character set for MTOM or text encodings (whether it is UTF8, UTF16LE or UTF16BE).</span></span> <span data-ttu-id="3a53e-127">Der tatsächlich verwendete Zeichensatz Wert wird durch die Codierungs Eigenschafts Einschränkung bestimmt.</span><span class="sxs-lookup"><span data-stu-id="3a53e-127">The actual character set value used is determined by the encoding property constraint.</span></span>

## <a name="constraints-with-http-header-authentication"></a><span data-ttu-id="3a53e-128">Einschränkungen bei der HTTP-Header Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="3a53e-128">Constraints with HTTP Header Authentication</span></span>

<span data-ttu-id="3a53e-129">Dieser Abschnitt gilt für den Fall, dass die Einschränkung der sicherheitsbindungs Einschränkung der [**WS \_ http-Header Authentifizierungs \_ \_ \_ \_ \_ Einschränkung**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding_constraint) angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="3a53e-129">This section applies when the [**WS\_HTTP\_HEADER\_AUTH\_SECURITY\_BINDING\_CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding_constraint) security binding constraint is specified.</span></span>

<span data-ttu-id="3a53e-130">Diese Sicherheitsbindung wird in der Richtlinie durch unterschiedliche Assertionen angegeben, die angeben, dass die HTTP-Header Authentifizierung verwendet werden soll, und dass ein bestimmtes Authentifizierungsschema verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3a53e-130">This security binding is indicated in the policy by different assertions that states both that HTTP header authentication should be used, and that a particular authentication scheme should be used.</span></span> <span data-ttu-id="3a53e-131">Die Richtlinien Assertionen entsprechen den Werten der [**WS- \_ Sicherheits \_ Bindungs \_ Eigenschaft \_ http- \_ Header \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_property_id) -Authentifizierungsschema wie folgt:</span><span class="sxs-lookup"><span data-stu-id="3a53e-131">The policy assertions correspond to the values of the [**WS\_SECURITY\_BINDING\_PROPERTY\_HTTP\_HEADER\_AUTH\_SCHEME**](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_property_id) as follows:</span></span>

``` syntax
<wsp:Policy...>
    <httpp:BasicAuthentication.../> => WS_HTTP_HEADER_AUTH_SCHEME_BASIC
</wsp:Policy>
```

``` syntax
<wsp:Policy...>
    <httpp:NegotiateAuthentication.../> => WS_HTTP_HEADER_AUTH_SCHEME_NEGOTIATE
</wsp:Policy>
```

``` syntax
<wsp:Policy...>
    <httpp:NtlmAuthentication.../> => WS_HTTP_HEADER_AUTH_SCHEME_NTLM
</wsp:Policy>
```

``` syntax
<wsp:Policy...>
    <httpp:DigestAuthentication.../> => WS_HTTP_HEADER_AUTH_SCHEME_DIGEST
</wsp:Policy>
```

## <a name="constraints-with-sll-transport-security"></a><span data-ttu-id="3a53e-132">Einschränkungen bei der SLL-Transport Sicherheit</span><span class="sxs-lookup"><span data-stu-id="3a53e-132">Constraints with SLL Transport Security</span></span>

<span data-ttu-id="3a53e-133">Dieser Abschnitt gilt, wenn die Sicherheits Bindungs Einschränkung der [**WS \_ SSL- \_ Transport \_ Sicherheits \_ Bindung \_**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_constraint) angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="3a53e-133">This section applies when the [**WS\_SSL\_TRANSPORT\_SECURITY\_BINDING\_CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_constraint) security binding constraint is specified.</span></span> <span data-ttu-id="3a53e-134">In diesem Fall werden die folgenden Richtlinien Assertionen verwendet:</span><span class="sxs-lookup"><span data-stu-id="3a53e-134">The following policy assertions are used in this case:</span></span>

``` syntax
<wsp:Policy...>
    <sp:TransportBinding...>
        <wsp:Policy...>
            <sp:TransportToken...>
                <wsp:Policy...>
                    <sp:HttpsToken.../>
            </wsp:Policy...>
        </wsp:Policy>
    </sp:TransportBinding...>
</wsp:Policy>
```

## <a name="constraints-with-sspi-transport-security"></a><span data-ttu-id="3a53e-135">Einschränkungen bei der SSPI-Transport Sicherheit</span><span class="sxs-lookup"><span data-stu-id="3a53e-135">Constraints with SSPI Transport Security</span></span>

<span data-ttu-id="3a53e-136">Dieser Abschnitt gilt, wenn die Sicherheits Bindungs Einschränkung der [**WS \_ TCP \_ SSPI- \_ Transport \_ Sicherheits \_ Bindung \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding_constraint) angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="3a53e-136">This section applies when the [**WS\_TCP\_SSPI\_TRANSPORT\_SECURITY\_BINDING\_CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding_constraint) security binding constraint is specified.</span></span> <span data-ttu-id="3a53e-137">In diesem Fall werden die folgenden Richtlinien Assertionen verwendet:</span><span class="sxs-lookup"><span data-stu-id="3a53e-137">The following policy assertions are used in this case:</span></span>

``` syntax
<wsp:Policy...>
    <sp:TransportBinding...>
        <wsp:Policy...>
            <sp:TransportToken...>
                <wsp:Policy...>
                    <netf:WindowsTransportSecurity.../>
            </wsp:Policy...>
        </wsp:Policy>
    </sp:TransportBinding...>
</wsp:Policy>
```

## <a name="constrains-with-transport-security"></a><span data-ttu-id="3a53e-138">Einschränken der Transport Sicherheit</span><span class="sxs-lookup"><span data-stu-id="3a53e-138">Constrains with Transport Security</span></span>

<span data-ttu-id="3a53e-139">Die Eigenschaften Einschränkung der [**\_ \_ \_ Transport \_ Schutz \_ Ebene der WS-Sicherheits Eigenschaft**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id) kann angegeben werden, wenn eine der sicherheitsbindungs Einschränkungen angegeben ist:</span><span class="sxs-lookup"><span data-stu-id="3a53e-139">The [**WS\_SECURITY\_PROPERTY\_TRANSPORT\_PROTECTION\_LEVEL**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id) property constraint can be specified if any of the security binding constraints are specified:</span></span>

-   [<span data-ttu-id="3a53e-140">**WS \_ SSL \_ - \_ Transport \_ sicherheitsbindungs \_ Einschränkung**</span><span class="sxs-lookup"><span data-stu-id="3a53e-140">**WS\_SSL\_TRANSPORT\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_constraint)

    <span data-ttu-id="3a53e-141">Der Wert aus der Richtlinie lautet immer [**WS \_ \_ -Schutzgrad \_ Signieren \_ und \_ verschlüsseln**](/windows/desktop/api/WebServices/ne-webservices-ws_protection_level).</span><span class="sxs-lookup"><span data-stu-id="3a53e-141">The value from policy is always [**WS\_PROTECTION\_LEVEL\_SIGN\_AND\_ENCRYPT**](/windows/desktop/api/WebServices/ne-webservices-ws_protection_level).</span></span>

-   [<span data-ttu-id="3a53e-142">**WS \_ TCP \_ SSPI \_ - \_ Transport \_ sicherheitsbindungs \_ Einschränkung**</span><span class="sxs-lookup"><span data-stu-id="3a53e-142">**WS\_TCP\_SSPI\_TRANSPORT\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding_constraint)

    <span data-ttu-id="3a53e-143">Der Wert aus der Richtlinie wird als Teil der windowstransportsecurity-Assertion wie folgt angegeben:</span><span class="sxs-lookup"><span data-stu-id="3a53e-143">The value from policy is specified as part of the WindowsTransportSecurity assertion, as follows:</span></span>

    ``` syntax
    <netf:WindowsTransportSecurity...>None</netf:WindowsTransportSecurity> => WS_PROTECTION_LEVEL_NONE
    ```

    ``` syntax
    <netf:WindowsTransportSecurity...>Sign</netf:WindowsTransportSecurity> => WS_PROTECTION_LEVEL_SIGN
    ```

    ``` syntax
    <netf:WindowsTransportSecurity...>EncryptAndSign</netf:WindowsTransportSecurity> => WS_PROTECTION_LEVEL_SIGN_AND_ENCRYPT
    ```

-   [<span data-ttu-id="3a53e-144">**WS-HTTP-Header Authentifizierung- \_ \_ \_ \_ Sicherheits \_ Bindungs \_ Einschränkung**</span><span class="sxs-lookup"><span data-stu-id="3a53e-144">**WS\_HTTP\_HEADER\_AUTH\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding_constraint)

    <span data-ttu-id="3a53e-145">Der Wert aus der Richtlinie lautet immer [**WS- \_ Schutz \_ Ebene \_ None**](/windows/desktop/api/WebServices/ne-webservices-ws_protection_level).</span><span class="sxs-lookup"><span data-stu-id="3a53e-145">The value from policy is always [**WS\_PROTECTION\_LEVEL\_NONE**](/windows/desktop/api/WebServices/ne-webservices-ws_protection_level).</span></span>

## <a name="constraints-with-kerberos-apreq-security-binding"></a><span data-ttu-id="3a53e-146">Einschränkungen bei der Kerberos-apreq-Sicherheitsbindung</span><span class="sxs-lookup"><span data-stu-id="3a53e-146">Constraints with Kerberos APREQ Security Binding</span></span>

<span data-ttu-id="3a53e-147">Dieser Abschnitt gilt für den Fall, dass die Sicherheits Bindungs Einschränkung der [**WS \_ Kerberos- \_ apreq- \_ Nachrichten \_ Sicherheits \_ Bindung \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint) angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="3a53e-147">This section applies when the [**WS\_KERBEROS\_APREQ\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint) security binding constraint is specified.</span></span> <span data-ttu-id="3a53e-148">In diesem Fall werden die folgenden Richtlinien Assertionen verwendet:</span><span class="sxs-lookup"><span data-stu-id="3a53e-148">The following policy assertions are used in this case:</span></span>

``` syntax
<sp:EndorsingSupportingTokens...>
    <wsp:Policy>
        <sp:KerberosToken>
            <WssGssKerberosV5ApReqToken11.../>
        </sp:KerberosToken>
    </wsp:Policy>
</sp:EndorsingSupportingTokens>
```

## <a name="constraints-with-message-security-binding"></a><span data-ttu-id="3a53e-149">Einschränkungen mit Nachrichten Sicherheitsbindung</span><span class="sxs-lookup"><span data-stu-id="3a53e-149">Constraints with Message Security Binding</span></span>

<span data-ttu-id="3a53e-150">Dieser Abschnitt gilt, wenn die Sicherheits Bindungs Einschränkung der [**WS \_ username \_ Message \_ Security \_ Binding- \_ Einschränkung**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint) angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="3a53e-150">This section applies when the [**WS\_USERNAME\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint) security binding constraint is specified.</span></span> <span data-ttu-id="3a53e-151">In diesem Fall werden die folgenden Richtlinien Assertionen verwendet:</span><span class="sxs-lookup"><span data-stu-id="3a53e-151">The following policy assertions are used in this case:</span></span>

``` syntax
<sp:SignedSupportingTokens>
    <wsp:Policy>
        <sp:UsernameToken.../>
    </wsp:Policy>
</sp:SignedSupportingTokens>
```

## <a name="ws_cert_message_security_binding_constraint"></a><span data-ttu-id="3a53e-152">WS \_ CERT \_ Message \_ - \_ sicherheitsbindungs \_ Einschränkung</span><span class="sxs-lookup"><span data-stu-id="3a53e-152">WS\_CERT\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT</span></span>

<span data-ttu-id="3a53e-153">Dieser Abschnitt gilt, wenn die Sicherheits Bindungs Einschränkung der [**WS \_ CERT \_ Message \_ Security \_ Binding- \_ Einschränkung**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint) angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="3a53e-153">This section applies when the [**WS\_CERT\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint) security binding constraint is specified.</span></span> <span data-ttu-id="3a53e-154">In diesem Fall werden die folgenden Richtlinien Assertionen verwendet:</span><span class="sxs-lookup"><span data-stu-id="3a53e-154">The following policy assertions are used in this case:</span></span>

``` syntax
<sp:EndorsingSupportingTokens>
    <wsp:Policy>
        <sp:X509Token.../>
   </wsp:Policy>
</sp:EndorsingSupportingTokens>
```

## <a name="ws_issued_token_message_security_binding_constraint"></a><span data-ttu-id="3a53e-155">WS \_ - \_ Token- \_ Nachrichten \_ Sicherheits \_ Bindungs \_ Einschränkung</span><span class="sxs-lookup"><span data-stu-id="3a53e-155">WS\_ISSUED\_TOKEN\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT</span></span>

<span data-ttu-id="3a53e-156">Dieser Abschnitt gilt, wenn die Sicherheits Bindungs Einschränkung der [**WS- \_ Token- \_ \_ Nachrichten \_ Sicherheits \_ Bindung \_**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint) angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="3a53e-156">This section applies when the [**WS\_ISSUED\_TOKEN\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint) security binding constraint is specified.</span></span> <span data-ttu-id="3a53e-157">In diesem Fall werden die folgenden Richtlinien Assertionen verwendet:</span><span class="sxs-lookup"><span data-stu-id="3a53e-157">The following policy assertions are used in this case:</span></span>

``` syntax
<sp:EndorsingSupportingTokens...>
    <wsp:Policy>
        <sp:IssuedToken sp:IncludeToken=&quot;xs:anyURI&quot;? ...=&quot;&quot; >
            <wsp:Issuer>...</wsp:Issuer>?
            <wsp:RequestSecurityTokenTemplate TrustVersion='xs:anyURI&quot;?>
                ...
                <wst10:Claims>
                    <wsi:ClaimType Optional='xs:boolean'?>xs:anyURI<wt:ClaimType>*
                </wst10:Claims>
                ...
            </wsp:RequestSecurityTokenTemplate>
            <wsp:Policy>
                <sp:RequireDerivedKeys/> ?
                <sp:RequireExternalReference/> ?
                <sp:RequireInternalReference/> ?
            </wsp:Policy> ?
        </sp:IssuedToken>
    </wsp:Policy>
</sp:EndorsingSupportingTokens>
```

<span data-ttu-id="3a53e-158">Im folgenden wird die Zuordnung von Feldern der WS-Richtlinie für das Token für die [**\_ \_ \_ Nachrichten \_ Sicherheits \_ Bindung \_**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint) zur obigen Richtlinie beschrieben:</span><span class="sxs-lookup"><span data-stu-id="3a53e-158">The following describes the mapping of fields of the [**WS\_ISSUED\_TOKEN\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint) to the above policy:</span></span>

-   <span data-ttu-id="3a53e-159">Das Feld "claimeinschränkungs" wird verwendet, um den Satz von Anspruchstyp-URIs zu überprüfen, die im obigen WSI: ClaimType-Element angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="3a53e-159">The claimConstraints field is used to verify the set of claim type URIs that appear within the wsi:ClaimType element above.</span></span>

-   <span data-ttu-id="3a53e-160">Das issuerAddress-Feld entspricht dem obigen wsp: Aussteller-Element, das die [**WS- \_ Endpunkt \_ Adresse**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) des Diensts ist, der das Token ausgeben kann.</span><span class="sxs-lookup"><span data-stu-id="3a53e-160">The issuerAddress field corresponds to the wsp:Issuer element above, which is the [**WS\_ENDPOINT\_ADDRESS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) of the service that can issue the token.</span></span>

-   <span data-ttu-id="3a53e-161">Das Feld RequestSecurityTokenTemplate entspricht den untergeordneten Elementen des Elements wsp: RequestSecurityTokenTemplate.</span><span class="sxs-lookup"><span data-stu-id="3a53e-161">The requestSecurityTokenTemplate field corresponds to the child elements of the wsp:RequestSecurityTokenTemplate element.</span></span>

## <a name="ws_security_context_message_security_binding_constraint"></a><span data-ttu-id="3a53e-162">WS- \_ Sicherheits \_ Kontext- \_ Nachrichten \_ Sicherheits \_ Bindungs \_ Einschränkung</span><span class="sxs-lookup"><span data-stu-id="3a53e-162">WS\_SECURITY\_CONTEXT\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT</span></span>

<span data-ttu-id="3a53e-163">Dieser Abschnitt gilt, wenn die Sicherheits Bindungs Einschränkung der [**WS- \_ Sicherheits \_ Kontext- \_ Nachrichten \_ Sicherheits \_ Bindung \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding_constraint) angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="3a53e-163">This section applies when the [**WS\_SECURITY\_CONTEXT\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding_constraint) security binding constraint is specified.</span></span> <span data-ttu-id="3a53e-164">In diesem Fall werden die folgenden Richtlinien Assertionen verwendet:</span><span class="sxs-lookup"><span data-stu-id="3a53e-164">The following policy assertions are used in this case:</span></span>

``` syntax
<sp:EndorsingSupportingTokens...>
    <wsp:Policy>
        <sp:SecureConversationToken sp:IncludeToken=&quot;xs:anyURI&quot;? ...=&quot;&quot; >
            <wsp:Issuer>...</wsp:Issuer>?
            <wsp:Policy>
                <sp:RequireDerivedKeys.../>?
                <sp:RequireExternalUriReference.../>?
                <sp:SC10SecurityContextToken.../>? => WS_SECURE_CONVERSATION_VERSION_FEBRUARY_2005
                <sp:BootstrapPolicy... >?
                   <wsp:Policy> ...  </wsp:Policy> => WS_SECURITY_CONSTRAINTS
                </sp:BootstrapPolicy>
            </wsp:Policy>
        </wsp:SecureConversationToken>
    </wsp:Policy>
</sp:EndorsingSupportingTokens>
```

<span data-ttu-id="3a53e-165">Der Entropie Modus wird durch die <SP: Trust10>-Assertionen bestimmt.</span><span class="sxs-lookup"><span data-stu-id="3a53e-165">The entropy mode is determined by the <sp:Trust10> assertion.</span></span> <span data-ttu-id="3a53e-166"><SP: requirecliententropy/> und <SP: Requirements ServerEntropy/> => [**WS \_ Security \_ Key \_ Entropy \_ Mode \_ kombinierte**](/windows/desktop/api/WebServices/ne-webservices-ws_security_key_entropy_mode) <SP: requirecliententropy/> => **WS \_ Security \_ Key \_ Entropy \_ Mode \_ Client \_ only** <SP: Requirements ServerEntropy/> => **WS \_ Security \_ Key \_ Entropy \_ Mode \_ Server \_ only**</span><span class="sxs-lookup"><span data-stu-id="3a53e-166"><sp:RequireClientEntropy/> and <sp:RequireServerEntropy/> => [**WS\_SECURITY\_KEY\_ENTROPY\_MODE\_COMBINED**](/windows/desktop/api/WebServices/ne-webservices-ws_security_key_entropy_mode) <sp:RequireClientEntropy/> => **WS\_SECURITY\_KEY\_ENTROPY\_MODE\_CLIENT\_ONLY** <sp:RequireServerEntropy/> => **WS\_SECURITY\_KEY\_ENTROPY\_MODE\_SERVER\_ONLY**</span></span>

## <a name="ws_request_security_token_property_trust_version"></a><span data-ttu-id="3a53e-167">Vertrauens Version der WS- \_ Anforderungs \_ Sicherheits \_ Token- \_ Eigenschaft \_ \_</span><span class="sxs-lookup"><span data-stu-id="3a53e-167">WS\_REQUEST\_SECURITY\_TOKEN\_PROPERTY\_TRUST\_VERSION</span></span>

<span data-ttu-id="3a53e-168">Dieser Abschnitt gilt, wenn die Sicherheits Bindungs Einschränkung der [**WS- \_ Token- \_ \_ Nachrichten \_ Sicherheits \_ Bindung \_**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint) angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="3a53e-168">This section applies when the [**WS\_ISSUED\_TOKEN\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint) security binding constraint is specified.</span></span> <span data-ttu-id="3a53e-169">Die folgenden Richtlinien Assertionen werden verwendet, um die [**WS- \_ Trust- \_ Version**](/windows/desktop/api/WebServices/ne-webservices-ws_trust_version) und zugehörige Optionen zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="3a53e-169">The following policy assertions are used to identify the [**WS\_TRUST\_VERSION**](/windows/desktop/api/WebServices/ne-webservices-ws_trust_version) and associated options.</span></span>

``` syntax
<sp:Trust10> => WS_TRUST_VERSION_FEBRUARY_2005
    <sp:Policy>
        <sp:MustSupportClientChallenge/> ?
        <sp:MustSupportServerChallenge/> ?
        <sp:RequireClientEntropy/> ?
        <sp:RequireServerEntropy/> ?
        <sp:MustSupportIssuedTokens/> ?
    </sp:Policy>
</sp:Trust10>
```

<span data-ttu-id="3a53e-170">Die Trust-Version kann mithilfe der [**WS- \_ Anforderungs \_ Sicherheits \_ Token- \_ Eigenschafts \_ Einschränkung**](/windows/desktop/api/WebServices/ns-webservices-ws_request_security_token_property_constraint) mit der Eigenschaften-ID [**WS \_ Request \_ Security \_ Token \_ \_ Trust \_ Version**](/windows/desktop/api/WebServices/ne-webservices-ws_request_security_token_property_id)angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="3a53e-170">The trust version can be specified using the [**WS\_REQUEST\_SECURITY\_TOKEN\_PROPERTY\_CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_request_security_token_property_constraint) with a property id of [**WS\_REQUEST\_SECURITY\_TOKEN\_PROPERTY\_TRUST\_VERSION**](/windows/desktop/api/WebServices/ne-webservices-ws_request_security_token_property_id).</span></span>

## <a name="ws_security_property_security_header_version"></a><span data-ttu-id="3a53e-171">\_ \_ \_ Sicherheits \_ Header \_ Version der WS-Sicherheits Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3a53e-171">WS\_SECURITY\_PROPERTY\_SECURITY\_HEADER\_VERSION</span></span>

<span data-ttu-id="3a53e-172">Dieser Abschnitt gilt, wenn eine der folgenden Bindungs Einschränkungen verwendet wird:</span><span class="sxs-lookup"><span data-stu-id="3a53e-172">This section applies when any of the following binding constraints are used:</span></span>

-   [<span data-ttu-id="3a53e-173">**WS- \_ Kerberos- \_ apreq- \_ Nachrichten \_ Sicherheits \_ Bindungs \_ Einschränkung**</span><span class="sxs-lookup"><span data-stu-id="3a53e-173">**WS\_KERBEROS\_APREQ\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint)
-   [<span data-ttu-id="3a53e-174">**WS \_ username \_ Message \_ Security \_ Binding- \_ Einschränkung**</span><span class="sxs-lookup"><span data-stu-id="3a53e-174">**WS\_USERNAME\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint)
-   [<span data-ttu-id="3a53e-175">**WS \_ CERT \_ Message \_ - \_ sicherheitsbindungs \_ Einschränkung**</span><span class="sxs-lookup"><span data-stu-id="3a53e-175">**WS\_CERT\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint)
-   [<span data-ttu-id="3a53e-176">**WS \_ - \_ Token- \_ Nachrichten \_ Sicherheits \_ Bindungs \_ Einschränkung**</span><span class="sxs-lookup"><span data-stu-id="3a53e-176">**WS\_ISSUED\_TOKEN\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint)

<span data-ttu-id="3a53e-177">Die Header Sicherheitsversion (wie in der [**Sicherheits \_ \_ \_ \_ Header \_ Version der WS-Sicherheits Eigenschaft**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)angegeben) wird durch eine der folgenden Richtlinien Assertionen bestimmt:</span><span class="sxs-lookup"><span data-stu-id="3a53e-177">The header security version (as specified by [**WS\_SECURITY\_PROPERTY\_SECURITY\_HEADER\_VERSION**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)) is determined by one of the following policy assertions:</span></span>

``` syntax
<wsp:Wss10> ... </wsp:Wss10> => WS_SECURITY_HEADER_VERSION_1_0
```

``` syntax
<wsp:Wss11> ... </wsp:Wss11> => WS_SECURITY_HEADER_VERSION_1_1
```

## <a name="constraints-with-header-security-layout"></a><span data-ttu-id="3a53e-178">Einschränkungen mit Header-Sicherheits Layout</span><span class="sxs-lookup"><span data-stu-id="3a53e-178">Constraints with Header Security Layout</span></span>

<span data-ttu-id="3a53e-179">Dieser Abschnitt gilt, wenn eine der folgenden Bindungs Einschränkungen verwendet wird:</span><span class="sxs-lookup"><span data-stu-id="3a53e-179">This section applies when any of the following binding constraints are used:</span></span>

-   [<span data-ttu-id="3a53e-180">**WS- \_ Kerberos- \_ apreq- \_ Nachrichten \_ Sicherheits \_ Bindungs \_ Einschränkung**</span><span class="sxs-lookup"><span data-stu-id="3a53e-180">**WS\_KERBEROS\_APREQ\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint)
-   [<span data-ttu-id="3a53e-181">**WS \_ username \_ Message \_ Security \_ Binding- \_ Einschränkung**</span><span class="sxs-lookup"><span data-stu-id="3a53e-181">**WS\_USERNAME\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint)
-   [<span data-ttu-id="3a53e-182">**WS \_ CERT \_ Message \_ - \_ sicherheitsbindungs \_ Einschränkung**</span><span class="sxs-lookup"><span data-stu-id="3a53e-182">**WS\_CERT\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint)
-   [<span data-ttu-id="3a53e-183">**WS \_ - \_ Token- \_ Nachrichten \_ Sicherheits \_ Bindungs \_ Einschränkung**</span><span class="sxs-lookup"><span data-stu-id="3a53e-183">**WS\_ISSUED\_TOKEN\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint)

<span data-ttu-id="3a53e-184">Das Layout des Sicherheits Headers (wie durch das Sicherheits [**\_ \_ \_ \_ Header \_ Layout der WS-Sicherheits Eigenschaft**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)angegeben) wird durch eine der folgenden Richtlinien Assertionen bestimmt:</span><span class="sxs-lookup"><span data-stu-id="3a53e-184">The security header layout (as specified by [**WS\_SECURITY\_PROPERTY\_SECURITY\_HEADER\_LAYOUT**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)) is determined by one of the following policy assertions:</span></span>

``` syntax
<sp:TransportBinding>
    <wsp:Policy>
        <sp:Layout>
            <sp:Lax.../> => WS_SECURITY_HEADER_LAYOUT_LAX
        </sp:Layout>
    </wsp:Policy>
</sp:TransportBinding>
```

``` syntax
<sp:TransportBinding>
    <wsp:Policy>
        <sp:Layout>
            <sp:Strict.../> => WS_SECURITY_HEADER_LAYOUT_STRICT
        </sp:Layout>
    </wsp:Policy>
</sp:TransportBinding>
```

``` syntax
<sp:TransportBinding>
    <wsp:Policy>
        <sp:Layout>
            <sp:LaxTsFirst.../> => WS_SECURITY_HEADER_LAYOUT_LAX_WITH_TIMESTAMP_FIRST
        </sp:Layout>
    </wsp:Policy>
</sp:TransportBinding>
```

``` syntax
<sp:TransportBinding>
    <wsp:Policy>
        <sp:Layout>
            <sp:LaxTsLast.../> => WS_SECURITY_HEADER_LAYOUT_LAX_WITH_TIMESTAMP_LAST
        </sp:Layout>
    </wsp:Policy>
</sp:TransportBinding>
```

## <a name="constraints-with-timestamp-security"></a><span data-ttu-id="3a53e-185">Einschränkungen mit Zeitstempel Sicherheit</span><span class="sxs-lookup"><span data-stu-id="3a53e-185">Constraints with Timestamp Security</span></span>

<span data-ttu-id="3a53e-186">Dieser Abschnitt gilt, wenn eine der folgenden Bindungs Einschränkungen verwendet wird:</span><span class="sxs-lookup"><span data-stu-id="3a53e-186">This section applies when any of the following binding constraints are used:</span></span>

-   [<span data-ttu-id="3a53e-187">**WS- \_ Kerberos- \_ apreq- \_ Nachrichten \_ Sicherheits \_ Bindungs \_ Einschränkung**</span><span class="sxs-lookup"><span data-stu-id="3a53e-187">**WS\_KERBEROS\_APREQ\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint)
-   [<span data-ttu-id="3a53e-188">**WS \_ username \_ Message \_ Security \_ Binding- \_ Einschränkung**</span><span class="sxs-lookup"><span data-stu-id="3a53e-188">**WS\_USERNAME\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint)
-   [<span data-ttu-id="3a53e-189">**WS \_ CERT \_ Message \_ - \_ sicherheitsbindungs \_ Einschränkung**</span><span class="sxs-lookup"><span data-stu-id="3a53e-189">**WS\_CERT\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint)
-   [<span data-ttu-id="3a53e-190">**WS \_ - \_ Token- \_ Nachrichten \_ Sicherheits \_ Bindungs \_ Einschränkung**</span><span class="sxs-lookup"><span data-stu-id="3a53e-190">**WS\_ISSUED\_TOKEN\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint)

<span data-ttu-id="3a53e-191">Ob ein Zeitstempel im Sicherheits Header enthalten ist (wie durch die [**WS- \_ Sicherheitseigenschaften- \_ \_ Zeitstempel \_ Verwendung**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)angegeben), wird durch das vorhanden sein von SP: IncludeTimestamp an folgendem Speicherort bestimmt:</span><span class="sxs-lookup"><span data-stu-id="3a53e-191">Whether or not a timestamp is included in the security header (as specified by [**WS\_SECURITY\_PROPERTY\_TIMESTAMP\_USAGE**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)) is determined by the presence of the sp:IncludeTimestamp in the following location:</span></span>

``` syntax
<sp:TransportBinding>
    <wsp:Policy>
        <sp:IncludeTimestamp.../>
    </wsp:Policy>
</sp:TransportBinding>
```

<span data-ttu-id="3a53e-192">Wenn die SP: incluabtimestamp-Übersetzung vorhanden ist, lautet der Wert aus der Richtlinie [**immer WS- \_ Sicherheits \_ Zeitstempel- \_ Verwendung \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_timestamp_usage).</span><span class="sxs-lookup"><span data-stu-id="3a53e-192">If the sp:IncludeTimestamp assertion is present, the value from policy is [**WS\_SECURITY\_TIMESTAMP\_USAGE\_ALWAYS**](/windows/desktop/api/WebServices/ne-webservices-ws_security_timestamp_usage).</span></span>

<span data-ttu-id="3a53e-193">Wenn die SP: incluuntimestamp-Assertionen nicht vorhanden sind, lautet der Wert aus der Richtlinie [**nie WS- \_ Sicherheits \_ Zeitstempel- \_ Verwendung \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_timestamp_usage).</span><span class="sxs-lookup"><span data-stu-id="3a53e-193">If the sp:IncludeTimestamp assertion is not present, the value from policy is [**WS\_SECURITY\_TIMESTAMP\_USAGE\_NEVER**](/windows/desktop/api/WebServices/ne-webservices-ws_security_timestamp_usage).</span></span>

 

 




