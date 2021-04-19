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
# <a name="metadata-mapping"></a>Metadatenzuordnung

Der Inhalt eines Metadatendokuments wird der Metadaten-API auf die in den folgenden Abschnitten erläuterten Methoden zugeordnet.


Die folgenden Namespace Präfixe werden in dieser Dokumentation verwendet:

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

In den nachfolgenden Abschnitten werden API-Konstrukte sowie die entsprechenden Metadatenkonstrukte (WSDL oder Richtlinie) beschrieben.

Kenntnisse in Bezug auf Metadatenspezifikationen wie WSDL und die Richtlinie erleichtern das Verständnis dieses Abschnitts.

## <a name="endpoint-address"></a>Endpunkt Adresse

Die Adresse eines Endpunkts (siehe [**WS- \_ Endpunkt \_ Adresse**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address)) wird von einem Erweiterbarkeits Element im WSDL: Port-Element des WSDL-Dokuments abgerufen. Die folgenden Erweiterbarkeits Elemente werden zum Angeben der Adresse unterstützt:

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

## <a name="ws_channel_binding"></a>WS- \_ Kanal \_ Bindung

Die kanalbindung (siehe [**WS \_ - \_ channelbindung**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)) wird wie folgt durch den Transport der verwendeten SOAP-Bindung bestimmt:

``` syntax
<soap:binding transport=&quot;http://schemas.microsoft.com/soap/tcp&quot;/> => WS_TCP_CHANNEL_BINDING
```

``` syntax
<soap:binding transport=&quot;http://schemas.xmlsoap.org/soap/http&quot;/> => WS_HTTP_CHANNEL_BINDING
```

## <a name="ws_channel_property_envelope_version"></a>Umschlag Version der WS- \_ Kanal \_ Eigenschaft \_ \_

Die Umschlag Version (siehe [**WS \_ - \_ Channeleigenschaft \_ Umschlag \_ Version**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)) wird wie folgt bestimmt, wie die SOAP-Bindung verwendet wird:

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

## <a name="addressing-version"></a>Adressierungs Version

Die Adressierungs Version (siehe die [**\_ \_ \_ Adressierungs \_ Version der WS-Kanal Eigenschaft**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)) wird durch die folgenden Assertionen in der Endpunkt Richtlinie bestimmt:

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

Wenn keine Adressierungs Erklärung vorhanden ist, wird von der [**WS- \_ Adressierungs \_ Versions \_ Transport**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) ausgegangen.

## <a name="message-encoding"></a>Nachrichtenverschlüsselung

Die Codierung der Nachricht (siehe [**WS- \_ \_ channeleigenschaftencodierung \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)) wird durch die folgenden Assertionen in der Endpunkt Richtlinie bestimmt:

``` syntax
<wsp:Policy...>
    <binp:BinaryEncoding.../> => WS_ENCODING_XML_BINARY_SESSION_1, WS_ENCODING_XML_BINARY_1
</wsp:Policy>
```

Beachten Sie, dass die Richtlinien Assertionen für binäre Codierungen keine Informationen darüber enthalten, ob die binäre Codierung Sitzungs basiert oder Sitzungs unabhängig ist. Dies wird durch die Codierungs Eigenschafts Einschränkung bestimmt (die entsprechend der Verwendung des verwendeten WS- [**\_ \_ Kanaltyps**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) angemessen ist oder nicht).

``` syntax
<wsp:Policy...>
    <mtomp:OptimizedMimeSerialization.../> => WS_ENCODING_XML_MTOM_UTF8, WS_ENCODING_XML_MTOM_UTF16LE, WS_ENCODING_XML_MTOM_UTF16BE
</wsp:Policy>
```

Wenn keine der obigen Assertionen vorhanden ist, wird eine Text Codierung verwendet: [**WS \_ Encoding \_ XML \_ UTF8**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding), **WS \_ Encoding \_ XML \_ UTF16LE**, **WS \_ Encoding \_ XML \_ UTF16BE**.

Beachten Sie, dass die Richtlinie keine Informationen über den Zeichensatz für MTOM oder Text Codierungen enthält (d. h. UTF8, UTF16LE oder UTF16BE). Der tatsächlich verwendete Zeichensatz Wert wird durch die Codierungs Eigenschafts Einschränkung bestimmt.

## <a name="constraints-with-http-header-authentication"></a>Einschränkungen bei der HTTP-Header Authentifizierung

Dieser Abschnitt gilt für den Fall, dass die Einschränkung der sicherheitsbindungs Einschränkung der [**WS \_ http-Header Authentifizierungs \_ \_ \_ \_ \_ Einschränkung**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding_constraint) angegeben wird.

Diese Sicherheitsbindung wird in der Richtlinie durch unterschiedliche Assertionen angegeben, die angeben, dass die HTTP-Header Authentifizierung verwendet werden soll, und dass ein bestimmtes Authentifizierungsschema verwendet werden soll. Die Richtlinien Assertionen entsprechen den Werten der [**WS- \_ Sicherheits \_ Bindungs \_ Eigenschaft \_ http- \_ Header \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_property_id) -Authentifizierungsschema wie folgt:

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

## <a name="constraints-with-sll-transport-security"></a>Einschränkungen bei der SLL-Transport Sicherheit

Dieser Abschnitt gilt, wenn die Sicherheits Bindungs Einschränkung der [**WS \_ SSL- \_ Transport \_ Sicherheits \_ Bindung \_**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_constraint) angegeben wird. In diesem Fall werden die folgenden Richtlinien Assertionen verwendet:

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

## <a name="constraints-with-sspi-transport-security"></a>Einschränkungen bei der SSPI-Transport Sicherheit

Dieser Abschnitt gilt, wenn die Sicherheits Bindungs Einschränkung der [**WS \_ TCP \_ SSPI- \_ Transport \_ Sicherheits \_ Bindung \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding_constraint) angegeben wird. In diesem Fall werden die folgenden Richtlinien Assertionen verwendet:

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

## <a name="constrains-with-transport-security"></a>Einschränken der Transport Sicherheit

Die Eigenschaften Einschränkung der [**\_ \_ \_ Transport \_ Schutz \_ Ebene der WS-Sicherheits Eigenschaft**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id) kann angegeben werden, wenn eine der sicherheitsbindungs Einschränkungen angegeben ist:

-   [**WS \_ SSL \_ - \_ Transport \_ sicherheitsbindungs \_ Einschränkung**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_constraint)

    Der Wert aus der Richtlinie lautet immer [**WS \_ \_ -Schutzgrad \_ Signieren \_ und \_ verschlüsseln**](/windows/desktop/api/WebServices/ne-webservices-ws_protection_level).

-   [**WS \_ TCP \_ SSPI \_ - \_ Transport \_ sicherheitsbindungs \_ Einschränkung**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding_constraint)

    Der Wert aus der Richtlinie wird als Teil der windowstransportsecurity-Assertion wie folgt angegeben:

    ``` syntax
    <netf:WindowsTransportSecurity...>None</netf:WindowsTransportSecurity> => WS_PROTECTION_LEVEL_NONE
    ```

    ``` syntax
    <netf:WindowsTransportSecurity...>Sign</netf:WindowsTransportSecurity> => WS_PROTECTION_LEVEL_SIGN
    ```

    ``` syntax
    <netf:WindowsTransportSecurity...>EncryptAndSign</netf:WindowsTransportSecurity> => WS_PROTECTION_LEVEL_SIGN_AND_ENCRYPT
    ```

-   [**WS-HTTP-Header Authentifizierung- \_ \_ \_ \_ Sicherheits \_ Bindungs \_ Einschränkung**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding_constraint)

    Der Wert aus der Richtlinie lautet immer [**WS- \_ Schutz \_ Ebene \_ None**](/windows/desktop/api/WebServices/ne-webservices-ws_protection_level).

## <a name="constraints-with-kerberos-apreq-security-binding"></a>Einschränkungen bei der Kerberos-apreq-Sicherheitsbindung

Dieser Abschnitt gilt für den Fall, dass die Sicherheits Bindungs Einschränkung der [**WS \_ Kerberos- \_ apreq- \_ Nachrichten \_ Sicherheits \_ Bindung \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint) angegeben wird. In diesem Fall werden die folgenden Richtlinien Assertionen verwendet:

``` syntax
<sp:EndorsingSupportingTokens...>
    <wsp:Policy>
        <sp:KerberosToken>
            <WssGssKerberosV5ApReqToken11.../>
        </sp:KerberosToken>
    </wsp:Policy>
</sp:EndorsingSupportingTokens>
```

## <a name="constraints-with-message-security-binding"></a>Einschränkungen mit Nachrichten Sicherheitsbindung

Dieser Abschnitt gilt, wenn die Sicherheits Bindungs Einschränkung der [**WS \_ username \_ Message \_ Security \_ Binding- \_ Einschränkung**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint) angegeben wird. In diesem Fall werden die folgenden Richtlinien Assertionen verwendet:

``` syntax
<sp:SignedSupportingTokens>
    <wsp:Policy>
        <sp:UsernameToken.../>
    </wsp:Policy>
</sp:SignedSupportingTokens>
```

## <a name="ws_cert_message_security_binding_constraint"></a>WS \_ CERT \_ Message \_ - \_ sicherheitsbindungs \_ Einschränkung

Dieser Abschnitt gilt, wenn die Sicherheits Bindungs Einschränkung der [**WS \_ CERT \_ Message \_ Security \_ Binding- \_ Einschränkung**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint) angegeben wird. In diesem Fall werden die folgenden Richtlinien Assertionen verwendet:

``` syntax
<sp:EndorsingSupportingTokens>
    <wsp:Policy>
        <sp:X509Token.../>
   </wsp:Policy>
</sp:EndorsingSupportingTokens>
```

## <a name="ws_issued_token_message_security_binding_constraint"></a>WS \_ - \_ Token- \_ Nachrichten \_ Sicherheits \_ Bindungs \_ Einschränkung

Dieser Abschnitt gilt, wenn die Sicherheits Bindungs Einschränkung der [**WS- \_ Token- \_ \_ Nachrichten \_ Sicherheits \_ Bindung \_**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint) angegeben wird. In diesem Fall werden die folgenden Richtlinien Assertionen verwendet:

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

Im folgenden wird die Zuordnung von Feldern der WS-Richtlinie für das Token für die [**\_ \_ \_ Nachrichten \_ Sicherheits \_ Bindung \_**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint) zur obigen Richtlinie beschrieben:

-   Das Feld "claimeinschränkungs" wird verwendet, um den Satz von Anspruchstyp-URIs zu überprüfen, die im obigen WSI: ClaimType-Element angezeigt werden.

-   Das issuerAddress-Feld entspricht dem obigen wsp: Aussteller-Element, das die [**WS- \_ Endpunkt \_ Adresse**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) des Diensts ist, der das Token ausgeben kann.

-   Das Feld RequestSecurityTokenTemplate entspricht den untergeordneten Elementen des Elements wsp: RequestSecurityTokenTemplate.

## <a name="ws_security_context_message_security_binding_constraint"></a>WS- \_ Sicherheits \_ Kontext- \_ Nachrichten \_ Sicherheits \_ Bindungs \_ Einschränkung

Dieser Abschnitt gilt, wenn die Sicherheits Bindungs Einschränkung der [**WS- \_ Sicherheits \_ Kontext- \_ Nachrichten \_ Sicherheits \_ Bindung \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding_constraint) angegeben wird. In diesem Fall werden die folgenden Richtlinien Assertionen verwendet:

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

Der Entropie Modus wird durch die <SP: Trust10>-Assertionen bestimmt. <SP: requirecliententropy/> und <SP: Requirements ServerEntropy/> => [**WS \_ Security \_ Key \_ Entropy \_ Mode \_ kombinierte**](/windows/desktop/api/WebServices/ne-webservices-ws_security_key_entropy_mode) <SP: requirecliententropy/> => **WS \_ Security \_ Key \_ Entropy \_ Mode \_ Client \_ only** <SP: Requirements ServerEntropy/> => **WS \_ Security \_ Key \_ Entropy \_ Mode \_ Server \_ only**

## <a name="ws_request_security_token_property_trust_version"></a>Vertrauens Version der WS- \_ Anforderungs \_ Sicherheits \_ Token- \_ Eigenschaft \_ \_

Dieser Abschnitt gilt, wenn die Sicherheits Bindungs Einschränkung der [**WS- \_ Token- \_ \_ Nachrichten \_ Sicherheits \_ Bindung \_**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint) angegeben wird. Die folgenden Richtlinien Assertionen werden verwendet, um die [**WS- \_ Trust- \_ Version**](/windows/desktop/api/WebServices/ne-webservices-ws_trust_version) und zugehörige Optionen zu identifizieren.

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

Die Trust-Version kann mithilfe der [**WS- \_ Anforderungs \_ Sicherheits \_ Token- \_ Eigenschafts \_ Einschränkung**](/windows/desktop/api/WebServices/ns-webservices-ws_request_security_token_property_constraint) mit der Eigenschaften-ID [**WS \_ Request \_ Security \_ Token \_ \_ Trust \_ Version**](/windows/desktop/api/WebServices/ne-webservices-ws_request_security_token_property_id)angegeben werden.

## <a name="ws_security_property_security_header_version"></a>\_ \_ \_ Sicherheits \_ Header \_ Version der WS-Sicherheits Eigenschaft

Dieser Abschnitt gilt, wenn eine der folgenden Bindungs Einschränkungen verwendet wird:

-   [**WS- \_ Kerberos- \_ apreq- \_ Nachrichten \_ Sicherheits \_ Bindungs \_ Einschränkung**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint)
-   [**WS \_ username \_ Message \_ Security \_ Binding- \_ Einschränkung**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint)
-   [**WS \_ CERT \_ Message \_ - \_ sicherheitsbindungs \_ Einschränkung**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint)
-   [**WS \_ - \_ Token- \_ Nachrichten \_ Sicherheits \_ Bindungs \_ Einschränkung**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint)

Die Header Sicherheitsversion (wie in der [**Sicherheits \_ \_ \_ \_ Header \_ Version der WS-Sicherheits Eigenschaft**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)angegeben) wird durch eine der folgenden Richtlinien Assertionen bestimmt:

``` syntax
<wsp:Wss10> ... </wsp:Wss10> => WS_SECURITY_HEADER_VERSION_1_0
```

``` syntax
<wsp:Wss11> ... </wsp:Wss11> => WS_SECURITY_HEADER_VERSION_1_1
```

## <a name="constraints-with-header-security-layout"></a>Einschränkungen mit Header-Sicherheits Layout

Dieser Abschnitt gilt, wenn eine der folgenden Bindungs Einschränkungen verwendet wird:

-   [**WS- \_ Kerberos- \_ apreq- \_ Nachrichten \_ Sicherheits \_ Bindungs \_ Einschränkung**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint)
-   [**WS \_ username \_ Message \_ Security \_ Binding- \_ Einschränkung**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint)
-   [**WS \_ CERT \_ Message \_ - \_ sicherheitsbindungs \_ Einschränkung**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint)
-   [**WS \_ - \_ Token- \_ Nachrichten \_ Sicherheits \_ Bindungs \_ Einschränkung**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint)

Das Layout des Sicherheits Headers (wie durch das Sicherheits [**\_ \_ \_ \_ Header \_ Layout der WS-Sicherheits Eigenschaft**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)angegeben) wird durch eine der folgenden Richtlinien Assertionen bestimmt:

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

## <a name="constraints-with-timestamp-security"></a>Einschränkungen mit Zeitstempel Sicherheit

Dieser Abschnitt gilt, wenn eine der folgenden Bindungs Einschränkungen verwendet wird:

-   [**WS- \_ Kerberos- \_ apreq- \_ Nachrichten \_ Sicherheits \_ Bindungs \_ Einschränkung**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint)
-   [**WS \_ username \_ Message \_ Security \_ Binding- \_ Einschränkung**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint)
-   [**WS \_ CERT \_ Message \_ - \_ sicherheitsbindungs \_ Einschränkung**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint)
-   [**WS \_ - \_ Token- \_ Nachrichten \_ Sicherheits \_ Bindungs \_ Einschränkung**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint)

Ob ein Zeitstempel im Sicherheits Header enthalten ist (wie durch die [**WS- \_ Sicherheitseigenschaften- \_ \_ Zeitstempel \_ Verwendung**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)angegeben), wird durch das vorhanden sein von SP: IncludeTimestamp an folgendem Speicherort bestimmt:

``` syntax
<sp:TransportBinding>
    <wsp:Policy>
        <sp:IncludeTimestamp.../>
    </wsp:Policy>
</sp:TransportBinding>
```

Wenn die SP: incluabtimestamp-Übersetzung vorhanden ist, lautet der Wert aus der Richtlinie [**immer WS- \_ Sicherheits \_ Zeitstempel- \_ Verwendung \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_timestamp_usage).

Wenn die SP: incluuntimestamp-Assertionen nicht vorhanden sind, lautet der Wert aus der Richtlinie [**nie WS- \_ Sicherheits \_ Zeitstempel- \_ Verwendung \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_timestamp_usage).

 

 




