---
title: Sicherheits Bindungen
description: Eine Sicherheitsbindung ist die Spezifikation eines Sicherheits Tokens und teilt der Laufzeit mit, wie Sie ein Sicherheits Token für die Kanal Sicherheit abrufen und verwenden können.
ms.assetid: 3e50e0fb-a7ca-4615-ac4c-5d93988e6460
keywords:
- Sicherheitsbindungs-Webdienste für Windows
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8a263c1a79212f3438e77c3dca519f6493cf40e
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104102562"
---
# <a name="security-bindings"></a>Sicherheits Bindungen

Eine Sicherheitsbindung ist die Spezifikation eines Sicherheits Tokens und teilt der Laufzeit mit, wie Sie ein Sicherheits Token für die Kanal Sicherheit abrufen und verwenden können. Das-Sicherheits Token enthält Informationen, die für den Zugriff auf Ressourcen bürgt. Es kann auch ein zugeordneter kryptografischer Schlüssel zum Durchführen von Signaturen und Verschlüsselung vorhanden sein.


Jede Sicherheitsbindung enthält eine eigene Auflistung Optionaler [sicherheitsbindungs Einstellungen](security-binding-settings.md) , die auf das Sicherheits Token beschränkt sind, das Sie definiert. Sie enthält auch [Sicherheits Anmelde](security-credentials.md)Informationen, die die Sicherheits Beweise darstellen (z. b. Benutzername und Kennwort oder Zertifikate), die zum Erstellen von Sicherheits Token benötigt werden.

Die folgenden Rückrufe sind Teil der Sicherheitsbindung:

-   [**WS-Überprüfungs- \_ \_ SAML- \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_validate_saml_callback)

Die folgenden Enumerationen sind Teil der Sicherheitsbindung:

-   [**WS- \_ Nachrichten \_ Sicherheits \_ Verwendung**](/windows/desktop/api/WebServices/ne-webservices-ws_message_security_usage)
-   [**WS \_ SAML \_ Authenticator- \_ Typ**](/windows/desktop/api/WebServices/ne-webservices-ws_saml_authenticator_type)
-   [**WS \_ - \_ Sicherheits \_ Bindungstyp**](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_type)
-   [**Typ des WS- \_ Sicherheits \_ Schlüssel \_ Handles \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_key_handle_type)

Die folgenden Funktionen sind Teil der Sicherheitsbindung:

-   [**Wscreatexmlsecuritytoken**](/windows/desktop/api/WebServices/nf-webservices-wscreatexmlsecuritytoken)
-   [**Wsfreesecuritytoken**](/windows/desktop/api/WebServices/nf-webservices-wsfreesecuritytoken)
-   

Die folgenden Strukturen sind Teil der Sicherheitsbindung:

-   [**WS \_ CAPI \_ asymmetrisches \_ Sicherheits \_ Schlüssel \_ handle**](/windows/desktop/api/WebServices/ns-webservices-ws_capi_asymmetric_security_key_handle)
-   [**WS- \_ CERT- \_ \_ SAML- \_ Authentifikator mit Vorzeichen**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_signed_saml_authenticator)
-   [**WS-HTTP-Header Authentifizierung- \_ \_ \_ \_ Sicherheits \_ Bindung**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding)
-   [**WS- \_ Kerberos- \_ apreq- \_ Nachrichten \_ \_ Sicherheitsbindung**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding)
-   [**WS \_ NamedPipe \_ SSPI- \_ Transport \_ Sicherheits \_ Bindung**](/windows/desktop/api/WebServices/ns-webservices-ws_namedpipe_sspi_transport_security_binding)
-   [**\_asymmetrischer WS NCrypt- \_ \_ Sicherheits \_ Schlüssel \_ handle**](/windows/desktop/api/WebServices/ns-webservices-ws_ncrypt_asymmetric_security_key_handle)
-   [**WS \_ - \_ \_ \_ rohschlüssel Handle für symmetrischen Sicherheitsschlüssel \_**](/windows/desktop/api/WebServices/ns-webservices-ws_raw_symmetric_security_key_handle)
-   [**WS- \_ SAML- \_ Authentifikator**](/windows/desktop/api/WebServices/ns-webservices-ws_saml_authenticator)
-   [**WS \_ SAML \_ Message- \_ Sicherheits \_ Bindung**](/windows/desktop/api/WebServices/ns-webservices-ws_saml_message_security_binding)
-   [**WS- \_ Sicherheits \_ Bindung**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding)
-   [**WS- \_ Sicherheits \_ Kontext Nachrichten- \_ \_ Sicherheits \_ Bindung**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding)
-   [**WS- \_ Sicherheits \_ Schlüssel \_ handle**](/windows/desktop/api/WebServices/ns-webservices-ws_security_key_handle)
-   [**WS \_ SSL- \_ Transport \_ Sicherheits \_ Bindung**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding)
-   [**WS \_ TCP- \_ SSPI- \_ Transport \_ Sicherheits \_ Bindung**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding)
-   [**WS \_ username \_ Message- \_ Sicherheits \_ Bindung**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding)
-   [**WS- \_ XML- \_ \_ tokennachrichtensicherheitsbindung \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_token_message_security_binding)

 

 




