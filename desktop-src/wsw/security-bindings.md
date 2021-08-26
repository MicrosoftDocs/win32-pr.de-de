---
title: Sicherheitsbindungen
description: Eine Sicherheitsbindung ist die Spezifikation eines Sicherheitstokens und teilt der Runtime mit, wie sie ein Sicherheitstoken für die Kanalsicherheit abrufen und verwenden kann.
ms.assetid: 3e50e0fb-a7ca-4615-ac4c-5d93988e6460
keywords:
- Security Bindings Web Services for Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4afc668e6dc6ab42e2d57066ecfb47ce337603bcadeccfb6b12a14a0e0550381
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120054540"
---
# <a name="security-bindings"></a>Sicherheitsbindungen

Eine Sicherheitsbindung ist die Spezifikation eines Sicherheitstokens und teilt der Runtime mit, wie sie ein Sicherheitstoken für die Kanalsicherheit abrufen und verwenden kann. Das Sicherheitstoken enthält Informationen, die für das Recht auf Zugriff auf Ressourcen verfügbar sind. Sie kann auch über einen zugeordneten kryptografischen Schlüssel zum Ausführen von Signaturen und Verschlüsselung verfügen.


Jede Sicherheitsbindung enthält eine eigene Sammlung optionaler [Sicherheitsbindungseinstellungen,](security-binding-settings.md) die auf das von ihr definierte Sicherheitstoken festgelegt sind. Es enthält auch [Sicherheitsanmeldeinformationen,](security-credentials.md)die den Sicherheitsbeweis (z. B. Benutzername und Kennwörter oder Zertifikate) darstellen, die zum Erstellen von Sicherheitstoken erforderlich sind.

Die folgenden Rückrufe sind Teil der Sicherheitsbindung:

-   [**WS \_ VALIDATE \_ SAML \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_validate_saml_callback)

Die folgenden Enumerationen sind Teil der Sicherheitsbindung:

-   [**VERWENDUNG DER \_ \_ WS-NACHRICHTENSICHERHEIT \_**](/windows/desktop/api/WebServices/ne-webservices-ws_message_security_usage)
-   [**WS \_ SAML \_ AUTHENTICATOR-TYP \_**](/windows/desktop/api/WebServices/ne-webservices-ws_saml_authenticator_type)
-   [**\_ \_ WS-SICHERHEITSBINDUNGSTYP \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_type)
-   [**HANDLETYP DES \_ \_ WS-SICHERHEITSSCHLÜSSELS \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_key_handle_type)

Die folgenden Funktionen sind Teil der Sicherheitsbindung:

-   [**WsCreateXmlSecurityToken**](/windows/desktop/api/WebServices/nf-webservices-wscreatexmlsecuritytoken)
-   [**WsFreeSecurityToken**](/windows/desktop/api/WebServices/nf-webservices-wsfreesecuritytoken)
-   

Die folgenden Strukturen sind Teil der Sicherheitsbindung:

-   [**ASYMMETRISCHES \_ \_ WS-CAPI-SICHERHEITSSCHLÜSSELHANDLI \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_capi_asymmetric_security_key_handle)
-   [**\_WS-ZERTIFIKATSIGNIERTE \_ \_ \_ SAML-AUTHENTIFIZIERER**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_signed_saml_authenticator)
-   [**\_ \_ \_ WS-HTTP-HEADERAUTHENTIFIZIERUNGS-SICHERHEITSBINDUNG \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding)
-   [**WS \_ \_ KERBEROS-APREQ-NACHRICHTENSICHERHEITSBINDUNG \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding)
-   [**WS \_ \_ NAMEDPIPE-SSPI-TRANSPORTSICHERHEITSBINDUNG \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_namedpipe_sspi_transport_security_binding)
-   [**WS \_ NCRYPT \_ ASYMMETRIC \_ SECURITY \_ KEY \_ HANDLE**](/windows/desktop/api/WebServices/ns-webservices-ws_ncrypt_asymmetric_security_key_handle)
-   [**WS \_ RAW \_ SYMMETRIC \_ SECURITY \_ KEY \_ HANDLE**](/windows/desktop/api/WebServices/ns-webservices-ws_raw_symmetric_security_key_handle)
-   [**WS \_ SAML \_ AUTHENTICATOR**](/windows/desktop/api/WebServices/ns-webservices-ws_saml_authenticator)
-   [**\_ \_ WS-SAML-NACHRICHTENSICHERHEITSBINDUNG \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_saml_message_security_binding)
-   [**\_WS-SICHERHEITSBINDUNG \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding)
-   [**SICHERHEITSBINDUNG FÜR \_ WS-SICHERHEITSKONTEXTNACHRICHTEN \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding)
-   [**\_WS-SICHERHEITSSCHLÜSSELHAND \_ \_ HANDLE**](/windows/desktop/api/WebServices/ns-webservices-ws_security_key_handle)
-   [**WS \_ \_ SSL-TRANSPORTSICHERHEITSBINDUNG \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding)
-   [**\_ \_ WS-TCP-SSPI-TRANSPORTSICHERHEITSBINDUNG \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding)
-   [**WS \_ USERNAME \_ MESSAGE \_ SECURITY \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding)
-   [**WS \_ XML \_ TOKEN \_ MESSAGE \_ SECURITY \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_token_message_security_binding)

 

 




