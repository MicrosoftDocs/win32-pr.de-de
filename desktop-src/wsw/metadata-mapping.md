---
title: Metadatenzuordnung
description: Der Inhalt eines Metadatendokuments wird der Metadaten-API wie in den folgenden Abschnitten erläutert zugeordnet.
ms.assetid: 266f8319-b7ac-497f-8eb7-8e2c7bcede33
keywords:
- Metadatenzuordnungswebdienste für Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57e6577e05f1d51ec13cc917465c306b94c403827149b086f252a38964997ab6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117841490"
---
# <a name="metadata-mapping"></a>Metadatenzuordnung

Der Inhalt eines Metadatendokuments wird der Metadaten-API wie in den folgenden Abschnitten erläutert zugeordnet.


Die folgenden Namespacepräfixe werden in dieser Dokumentation verwendet:

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

In den nachfolgenden Abschnitten werden API-Konstrukte sowie die Metadatenkonstrukte (WSDL oder Policy) beschrieben, denen sie entsprechen.

Kenntnisse in Bezug auf Metadatenspezifikationen wie WSDL und Policy helfen ihnen, diesen Abschnitt zu verstehen.

## <a name="endpoint-address"></a>Endpunktadresse

Die Adresse eines Endpunkts (siehe [**WS \_ ENDPOINT \_ ADDRESS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address)) wird von einem Erweiterbarkeitselement innerhalb des wsdl:port-Elements des WSDL-Dokuments abgerufen. Die folgenden Erweiterbarkeitselemente werden zum Angeben der Adresse unterstützt:

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

## <a name="ws_channel_binding"></a>\_WS-KANALBINDUNG \_

Die Kanalbindung (siehe [**\_ WS-KANALBINDUNG) \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)wird wie folgt durch den Transport bestimmt, den die soap-Bindung verwendet:

``` syntax
<soap:binding transport=&quot;http://schemas.microsoft.com/soap/tcp&quot;/> => WS_TCP_CHANNEL_BINDING
```

``` syntax
<soap:binding transport=&quot;http://schemas.xmlsoap.org/soap/http&quot;/> => WS_HTTP_CHANNEL_BINDING
```

## <a name="ws_channel_property_envelope_version"></a>VERSION DES \_ WS-KANALEIGENSCHAFTENUMSCHLAGS \_ \_ \_

Die Umschlagversion (siehe [**WS \_ CHANNEL PROPERTY \_ ENVELOPE \_ \_ VERSION)**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)wird wie folgt von der verwendeten Soap-Bindung bestimmt:

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

## <a name="addressing-version"></a>Adressierungsversion

Die Adressierungsversion (siehe [**WS \_ CHANNEL PROPERTY ADDRESSING \_ \_ \_ VERSION**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)) wird durch die folgenden Assertionen in der Endpunktrichtlinie bestimmt:

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

Wenn keine Adressierungsassertion vorhanden ist, wird [**WS \_ ADDRESSING VERSION \_ \_ TRANSPORT**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) angenommen.

## <a name="message-encoding"></a>Nachrichtenverschlüsselung

Die Codierung der Nachricht (siehe [**WS \_ CHANNEL PROPERTY \_ \_ ENCODING)**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)wird durch die folgenden Assertionen in der Endpunktrichtlinie bestimmt:

``` syntax
<wsp:Policy...>
    <binp:BinaryEncoding.../> => WS_ENCODING_XML_BINARY_SESSION_1, WS_ENCODING_XML_BINARY_1
</wsp:Policy>
```

Beachten Sie, dass die Richtlinienassertion für die binäre Codierung keine Informationen darüber enthält, ob die binäre Codierung sitzungs- oder sitzungslos ist. Dies wird durch die Einschränkung der Codierungseigenschaft bestimmt (die geeignet sein sollte, je nachdem, ob der verwendete [**\_ WS-KANALTYP \_ sitzungsbehaftet**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) ist oder nicht).

``` syntax
<wsp:Policy...>
    <mtomp:OptimizedMimeSerialization.../> => WS_ENCODING_XML_MTOM_UTF8, WS_ENCODING_XML_MTOM_UTF16LE, WS_ENCODING_XML_MTOM_UTF16BE
</wsp:Policy>
```

Wenn keine der oben genannten Assertionen vorhanden ist, wird eine Textcodierung verwendet: [**WS \_ ENCODING XML \_ \_ UTF8**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding), **WS ENCODING XML \_ \_ \_ UTF16LE**, **WS ENCODING XML \_ \_ \_ UTF16BE**.

Beachten Sie, dass die Richtlinie keine Informationen zum Zeichensatz für MTOM oder Textcodierungen enthält (unabhängig davon, ob es sich um UTF8, UTF16LE oder UTF16BE handelt). Der tatsächlich verwendete Zeichensatzwert wird durch die Einschränkung der Codierungseigenschaft bestimmt.

## <a name="constraints-with-http-header-authentication"></a>Einschränkungen bei der HTTP-Headerauthentifizierung

Dieser Abschnitt gilt, wenn die [**Sicherheitsbindungseinschränkung WS \_ HTTP \_ HEADER \_ AUTH SECURITY BINDING \_ \_ \_ CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding_constraint) angegeben wird.

Diese Sicherheitsbindung wird in der Richtlinie durch verschiedene Assertionen angegeben, die angeben, dass sowohl die HTTP-Headerauthentifizierung als auch ein bestimmtes Authentifizierungsschema verwendet werden soll. Die Richtlinienassertionen entsprechen den Werten des [**\_ WS SECURITY \_ BINDING PROPERTY HTTP HEADER \_ \_ \_ \_ AUTH \_ SCHEME**](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_property_id) wie folgt:

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

## <a name="constraints-with-sll-transport-security"></a>Einschränkungen mit SLL-Transportsicherheit

Dieser Abschnitt gilt, wenn die [**Sicherheitsbindungseinschränkung WS \_ SSL TRANSPORT SECURITY BINDING \_ \_ \_ \_ CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_constraint) angegeben wird. In diesem Fall werden die folgenden Richtlinienassertionen verwendet:

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

## <a name="constraints-with-sspi-transport-security"></a>Einschränkungen mit SSPI-Transportsicherheit

Dieser Abschnitt gilt, wenn die [**Sicherheitsbindungseinschränkung WS \_ TCP \_ SSPI \_ TRANSPORT SECURITY BINDING \_ \_ \_ CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding_constraint) angegeben wird. In diesem Fall werden die folgenden Richtlinienassertionen verwendet:

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

## <a name="constrains-with-transport-security"></a>Einschränkungen mit Transportsicherheit

Die [**WS \_ SECURITY PROPERTY TRANSPORT PROTECTION \_ \_ \_ \_ LEVEL-Eigenschafteneinschränkung**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id) kann angegeben werden, wenn eine der Sicherheitsbindungseinschränkungen angegeben ist:

-   [**\_ \_ \_ WS-SSL-TRANSPORTSICHERHEITSBINDUNGSEINSCHRÄNKUNG \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_constraint)

    Der Wert aus der Richtlinie ist immer [**WS \_ PROTECTION LEVEL SIGN AND \_ \_ \_ \_ ENCRYPT**](/windows/desktop/api/WebServices/ne-webservices-ws_protection_level).

-   [**\_ \_ \_ WS-TCP-SSPI-TRANSPORTSICHERHEITSBINDUNGSEINSCHRÄNKUNG \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding_constraint)

    Der Wert aus der Richtlinie wird wie folgt als Teil der WindowsTransportSecurity-Assertion angegeben:

    ``` syntax
    <netf:WindowsTransportSecurity...>None</netf:WindowsTransportSecurity> => WS_PROTECTION_LEVEL_NONE
    ```

    ``` syntax
    <netf:WindowsTransportSecurity...>Sign</netf:WindowsTransportSecurity> => WS_PROTECTION_LEVEL_SIGN
    ```

    ``` syntax
    <netf:WindowsTransportSecurity...>EncryptAndSign</netf:WindowsTransportSecurity> => WS_PROTECTION_LEVEL_SIGN_AND_ENCRYPT
    ```

-   [**SICHERHEITSBINDUNGSEINSCHRÄNKUNG FÜR \_ WS-HTTP-HEADERAUTHENTIFIZIERUNG \_ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding_constraint)

    Der Wert aus der Richtlinie ist immer [**WS \_ PROTECTION LEVEL \_ \_ NONE**](/windows/desktop/api/WebServices/ne-webservices-ws_protection_level).

## <a name="constraints-with-kerberos-apreq-security-binding"></a>Einschränkungen bei der Kerberos-APREQ-Sicherheitsbindung

Dieser Abschnitt gilt, wenn die [**Sicherheitsbindungseinschränkung WS \_ KERBEROS \_ APREQ \_ MESSAGE SECURITY BINDING \_ \_ \_ CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint) angegeben wird. In diesem Fall werden die folgenden Richtlinienassertionen verwendet:

``` syntax
<sp:EndorsingSupportingTokens...>
    <wsp:Policy>
        <sp:KerberosToken>
            <WssGssKerberosV5ApReqToken11.../>
        </sp:KerberosToken>
    </wsp:Policy>
</sp:EndorsingSupportingTokens>
```

## <a name="constraints-with-message-security-binding"></a>Einschränkungen bei der Nachrichtensicherheitsbindung

Dieser Abschnitt gilt, wenn die [**Sicherheitsbindungseinschränkung WS \_ USERNAME MESSAGE SECURITY BINDING \_ \_ \_ \_ CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint) angegeben wird. In diesem Fall werden die folgenden Richtlinienassertionen verwendet:

``` syntax
<sp:SignedSupportingTokens>
    <wsp:Policy>
        <sp:UsernameToken.../>
    </wsp:Policy>
</sp:SignedSupportingTokens>
```

## <a name="ws_cert_message_security_binding_constraint"></a>\_ \_ \_ \_ SICHERHEITSBINDUNGSEINSCHRÄNKUNG FÜR WS-ZERTIFIKATNACHRICHTEN \_

Dieser Abschnitt gilt, wenn die [**Sicherheitsbindungseinschränkung WS \_ CERT \_ MESSAGE SECURITY \_ BINDING \_ \_ CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint) angegeben wird. In diesem Fall werden die folgenden Richtlinienassertionen verwendet:

``` syntax
<sp:EndorsingSupportingTokens>
    <wsp:Policy>
        <sp:X509Token.../>
   </wsp:Policy>
</sp:EndorsingSupportingTokens>
```

## <a name="ws_issued_token_message_security_binding_constraint"></a>WS \_ ISSUED \_ TOKEN MESSAGE SECURITY BINDING CONSTRAINT \_ \_ \_ \_ (SICHERHEITSBINDUNGSEINSCHRÄNKUNG FÜR WS-AUSGESTELLTE TOKENNACHRICHTEN)

Dieser Abschnitt gilt, wenn die [**Sicherheitsbindungseinschränkung WS \_ ISSUED \_ TOKEN MESSAGE SECURITY BINDING \_ \_ \_ \_ CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint) angegeben wird. In diesem Fall werden die folgenden Richtlinienassertionen verwendet:

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

Im Folgenden wird die Zuordnung der Felder der [**WS \_ ISSUED \_ TOKEN MESSAGE SECURITY BINDING \_ \_ \_ \_ CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint) zur obigen Richtlinie beschrieben:

-   Das Feld claimConstraints wird verwendet, um den Satz von Anspruchstyp-URIs zu überprüfen, die im obigen wsi:ClaimType-Element angezeigt werden.

-   Das Feld issuerAddress entspricht dem obigen wsp:Issuer-Element, bei dem es sich um die [**\_ WS-ENDPUNKTADRESSE \_**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) des Diensts handelt, der das Token ausstellen kann.

-   Das Feld requestSecurityTokenTemplate entspricht den untergeordneten Elementen des wsp:RequestSecurityTokenTemplate-Elements.

## <a name="ws_security_context_message_security_binding_constraint"></a>SICHERHEITSBINDUNGSEINSCHRÄNKUNG FÜR \_ WS-SICHERHEITSKONTEXTNACHRICHTEN \_ \_ \_ \_ \_

Dieser Abschnitt gilt, wenn die [**Sicherheitsbindungseinschränkung WS \_ SECURITY CONTEXT MESSAGE SECURITY BINDING \_ \_ \_ \_ \_ CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding_constraint) angegeben wird. In diesem Fall werden die folgenden Richtlinienassertionen verwendet:

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

Der Entropiemodus wird durch die <sp:Trust10> Assertion bestimmt. <sp:RequireClientEntropy/> und <sp:RequireServerEntropy/> => [**WS \_ SECURITY KEY \_ \_ ENTROPY \_ MODE \_ COMBINED**](/windows/desktop/api/WebServices/ne-webservices-ws_security_key_entropy_mode) <sp:RequireClientEntropy/> => **WS SECURITY KEY \_ \_ \_ ENTROPY \_ MODE CLIENT \_ \_ ONLY** <sp:RequireServerEntropy/> => **WS SECURITY KEY \_ \_ \_ ENTROPY \_ MODE \_ SERVER \_ ONLY**

## <a name="ws_request_security_token_property_trust_version"></a>WS \_ REQUEST \_ SECURITY \_ TOKEN \_ PROPERTY \_ TRUST \_ VERSION

Dieser Abschnitt gilt, wenn die [**Sicherheitsbindungseinschränkung WS \_ ISSUED \_ TOKEN MESSAGE SECURITY BINDING \_ \_ \_ \_ CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint) angegeben wird. Die folgenden Richtlinienassertionen werden verwendet, um die [**WS \_ TRUST \_ VERSION**](/windows/desktop/api/WebServices/ne-webservices-ws_trust_version) und die zugehörigen Optionen zu identifizieren.

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

Die Vertrauensstellungsversion kann mithilfe der [**WS \_ REQUEST SECURITY TOKEN PROPERTY \_ \_ \_ \_ CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_request_security_token_property_constraint) mit der Eigenschaften-ID [**WS REQUEST SECURITY TOKEN \_ PROPERTY TRUST \_ \_ \_ \_ \_ VERSION**](/windows/desktop/api/WebServices/ne-webservices-ws_request_security_token_property_id)angegeben werden.

## <a name="ws_security_property_security_header_version"></a>SICHERHEITSHEADERVERSION DER WS-SICHERHEITSEIGENSCHAFT \_ \_ \_ \_ \_

Dieser Abschnitt gilt, wenn eine der folgenden Bindungseinschränkungen verwendet wird:

-   [**WS \_ KERBEROS \_ APREQ \_ MESSAGE \_ SECURITY \_ BINDING \_ CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint)
-   [**\_ \_ \_ \_ SICHERHEITSBINDUNGSEINSCHRÄNKUNG FÜR \_ WS-BENUTZERNAMENNACHRICHTEN**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint)
-   [**\_ \_ \_ \_ SICHERHEITSBINDUNGSEINSCHRÄNKUNG FÜR WS-ZERTIFIKATNACHRICHTEN \_**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint)
-   [**WS \_ ISSUED \_ TOKEN MESSAGE SECURITY BINDING CONSTRAINT \_ \_ \_ \_ (SICHERHEITSBINDUNGSEINSCHRÄNKUNG FÜR WS-AUSGESTELLTE TOKENNACHRICHTEN)**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint)

Die Headersicherheitsversion (wie von [**WS \_ SECURITY PROPERTY SECURITY HEADER \_ \_ \_ \_ VERSION**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)angegeben) wird durch eine der folgenden Richtlinienassertionen bestimmt:

``` syntax
<wsp:Wss10> ... </wsp:Wss10> => WS_SECURITY_HEADER_VERSION_1_0
```

``` syntax
<wsp:Wss11> ... </wsp:Wss11> => WS_SECURITY_HEADER_VERSION_1_1
```

## <a name="constraints-with-header-security-layout"></a>Einschränkungen beim Headersicherheitslayout

Dieser Abschnitt gilt, wenn eine der folgenden Bindungseinschränkungen verwendet wird:

-   [**WS \_ KERBEROS \_ APREQ \_ MESSAGE \_ SECURITY \_ BINDING \_ CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint)
-   [**\_ \_ \_ \_ SICHERHEITSBINDUNGSEINSCHRÄNKUNG FÜR \_ WS-BENUTZERNAMENNACHRICHTEN**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint)
-   [**\_ \_ \_ \_ SICHERHEITSBINDUNGSEINSCHRÄNKUNG FÜR WS-ZERTIFIKATNACHRICHTEN \_**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint)
-   [**WS \_ ISSUED \_ TOKEN MESSAGE SECURITY BINDING CONSTRAINT \_ \_ \_ \_ (SICHERHEITSBINDUNGSEINSCHRÄNKUNG FÜR WS-AUSGESTELLTE TOKENNACHRICHTEN)**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint)

Das Sicherheitsheaderlayout (wie von [**WS \_ SECURITY PROPERTY SECURITY HEADER \_ \_ \_ \_ LAYOUT**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)angegeben) wird durch eine der folgenden Richtlinienassertionen bestimmt:

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

## <a name="constraints-with-timestamp-security"></a>Einschränkungen mit Zeitstempelsicherheit

Dieser Abschnitt gilt, wenn eine der folgenden Bindungseinschränkungen verwendet wird:

-   [**WS \_ KERBEROS \_ APREQ \_ MESSAGE \_ SECURITY \_ BINDING \_ CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint)
-   [**\_ \_ \_ \_ SICHERHEITSBINDUNGSEINSCHRÄNKUNG FÜR \_ WS-BENUTZERNAMENNACHRICHTEN**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint)
-   [**\_ \_ \_ \_ SICHERHEITSBINDUNGSEINSCHRÄNKUNG FÜR WS-ZERTIFIKATNACHRICHTEN \_**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint)
-   [**WS \_ ISSUED \_ TOKEN MESSAGE SECURITY BINDING CONSTRAINT \_ \_ \_ \_ (SICHERHEITSBINDUNGSEINSCHRÄNKUNG FÜR WS-AUSGESTELLTE TOKENNACHRICHTEN)**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint)

Ob ein Zeitstempel im Sicherheitsheader enthalten ist (wie von [**WS \_ SECURITY PROPERTY \_ \_ TIMESTAMP \_ USAGE**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)angegeben), wird durch das Vorhandensein von sp:IncludeTimestamp an folgendem Speicherort bestimmt:

``` syntax
<sp:TransportBinding>
    <wsp:Policy>
        <sp:IncludeTimestamp.../>
    </wsp:Policy>
</sp:TransportBinding>
```

Wenn die assertion sp:IncludeTimestamp vorhanden ist, lautet der Wert aus der Richtlinie [**WS \_ SECURITY \_ TIMESTAMP \_ USAGE \_ ALWAYS**](/windows/desktop/api/WebServices/ne-webservices-ws_security_timestamp_usage).

Wenn die assertion sp:IncludeTimestamp nicht vorhanden ist, lautet der Wert aus der Richtlinie [**WS \_ SECURITY \_ TIMESTAMP \_ USAGE \_ NEVER**](/windows/desktop/api/WebServices/ne-webservices-ws_security_timestamp_usage).

 

 




