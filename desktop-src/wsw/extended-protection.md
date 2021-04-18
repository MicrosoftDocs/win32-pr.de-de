---
title: wird von
description: Erweiterter Schutz ist ein Mechanismus zum Binden eines äußeren sicheren Kanals, wie z. b. SSL, an Authentifizierungsprotokolle für den inneren Kanal, z. b. Kerberos-apreq und HTTP-Header Authentifizierung
ms.assetid: 35e48846-05e5-4db9-a3b5-098b62815b66
keywords:
- Erweiterter Schutz für Native Webdienste
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 895bdfecf994f6673c2ed7e7367bc3a7b5bd70c9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338202"
---
# <a name="extended-protection"></a>wird von

Erweiterter Schutz ist ein Mechanismus zum Binden eines äußeren sicheren Kanals, wie z. b. SSL, an Authentifizierungsprotokolle für den inneren Kanal, z. b. Kerberos-apreq und HTTP-Header Authentifizierung

Das Konzept des erweiterten Schutzes wird in RFC2743 definiert.

Der erweiterte Schutz wird, falls verfügbar, automatisch auf dem Client konfiguriert, erfordert jedoch möglicherweise eine Konfiguration auf dem Server für nicht standardmäßige Szenarien.

## <a name="supported-configurations"></a>Unterstützte Konfigurationen

Erweiterter Schutz wird unterstützt, wenn die [**WS- \_ http- \_ Kanal \_ Bindung**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) mit Sicherheits Bindungen mithilfe von integrierten Windows-Authentifizierungs Protokollen verwendet wird, z. b. WS-HTTP-Header Authentifizierung- [**\_ \_ \_ \_ Sicherheits \_ Bindung**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding) und [**WS \_ Kerberos \_ apreq \_ Message \_ \_ Security**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) Sie wird über die folgenden [**Sicherheitseigenschaften**](/windows/desktop/api/WebServices/ns-webservices-ws_security_property)konfiguriert:

-   [**\_ \_ \_ Erweiterte \_ Schutz \_ Richtlinie für WS-Sicherheitseigenschaften**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)
-   [**\_Szenario mit \_ \_ erweitertem \_ Schutz \_ von WS-Sicherheitseigenschaften**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)
-   [**WS- \_ Sicherheits \_ Eigenschafts \_ Dienst \_ Identitäten**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)

Die folgenden Konfigurationen mit erweitertem Schutz sind möglich:

Client

-   [**WS \_ Die SSL- \_ Transport \_ Sicherheits \_ Bindung**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) wird mit der [**WS- \_ Kerberos- \_ apreq- \_ Nachrichten \_ Sicherheits \_ Bindung**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) oder der WS-HTTP-Header Authentifizierung-Sicherheits [**\_ \_ \_ \_ \_ Bindung**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding)verwendet. In dieser Konfiguration wird die Authentifizierungs Bindung über ein erweitertes Schutz Token, das automatisch aus der SSL-Verbindung extrahiert wird, an die SSL-Verbindung gebunden.
-   SSL wird nicht verwendet, und die [**\_ \_ \_ \_ Sicherheits \_ Bindung**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding) für die WS-HTTP-Header Authentifizierung wird festgelegt. Die Authentifizierungs Bindung wird über den Server Prinzipal Namen (Server Principal Name, SPN) gebunden, der automatisch von der [**WS- \_ Endpunkt \_ Adresse**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address)bestimmt wird.

Server

-   [**WS \_ Die SSL- \_ Transport \_ Sicherheits \_ Bindung**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) wird mit der [**WS- \_ Kerberos- \_ apreq- \_ Nachrichten \_ Sicherheits \_ Bindung**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) oder der WS-HTTP-Header Authentifizierung-Sicherheits [**\_ \_ \_ \_ \_ Bindung**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding)verwendet. In dieser Konfiguration wird die Authentifizierungs Bindung über ein erweitertes Schutz Token, das aus der SSL-Verbindung extrahiert und automatisch überprüft wird, an die SSL-Verbindung gebunden.
-   SSL wird nicht verwendet, und die [**\_ \_ \_ \_ Sicherheits \_ Bindung**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding) für die WS-HTTP-Header Authentifizierung wird festgelegt. Die Authentifizierungs Bindung wird über den Server Prinzipal Namen (Server Principal Name, SPN) gebunden, der über [**WS- \_ Sicherheits \_ Eigenschafts \_ Dienst \_ Identitäten**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)bereitgestellt werden muss. Wenn eine Nachricht empfangen wird, wird der SPN extrahiert und für eine genaue Entsprechung mit den bereitgestellten Dienstnamen überprüft. Das Bereitstellen von SPNs entspricht nicht der Einstellung der [**erweiterten WS- \_ \_ Schutz \_ Richtlinie \_**](/windows/desktop/api/WebServices/ne-webservices-ws_extended_protection_policy).
-   SSL wird nicht verwendet, es wird ein [**\_ Erweiterter Server mit WS- \_ Schutz \_ Szenario \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_extended_protection_scenario) angegeben, und es wird eine [**WS- \_ Kerberos- \_ apreq- \_ Nachrichten \_ Sicherheits \_ Bindung**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) verwendet In dieser Konfiguration dürfen [**WS- \_ Sicherheits \_ Eigenschafts \_ Dienst \_ Identitäten**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id) nicht festgelegt werden. Eine SPN-Prüfung wird nicht ausgeführt, was als Teil des Kerberos-Protokolls erfolgt.
-   [**WS \_ Das erweiterte \_ Schutz \_ Szenario wurde \_ beendet \_**](/windows/desktop/api/WebServices/ne-webservices-ws_extended_protection_scenario) , und es wird entweder die [**WS- \_ Kerberos- \_ apreq- \_ Nachrichten \_ Sicherheits \_ Bindung**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) oder die WS-HTTP-Header Authentifizierungs- [**\_ \_ \_ \_ Sicherheits \_ Bindung**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding) verwendet. [**WS \_ Sicherheits \_ Eigenschafts \_ Dienst \_ Identitäten**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id) müssen festgelegt werden.

## <a name="supported-platforms"></a>Unterstützte Plattformen

Erweiterter Schutz wird auf Plattformen unterstützt, deren Unterstützung im Betriebssystem unterstützt wird. Windows 7 und Windows Server 2008 R2 bieten integrierte Unterstützung. Für andere Plattformen ist möglicherweise ein Update erforderlich.

Wenn das Betriebssystem des Servers keine solche Unterstützung bietet, werden alle vom Client gesendeten erweiterten Schutz Informationen ignoriert. Daher können Clients mit erweitertem Schutz mit einem solchen Server kommunizieren, der Sicherheitsvorteil geht jedoch verloren. Auf dem Client unterstützt die [**WS- \_ Kerberos- \_ apreq- \_ Nachrichten \_ Sicherheits \_ Bindung**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) in Kombination mit der [**WS \_ SSL- \_ Transport \_ Sicherheits \_ Bindung**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) nur erweiterten Schutz für Vista und höher.

Hinweis: der erweiterte Schutz, der nicht verfügbar ist, verhindert nicht, dass eine bestimmte Konfiguration verwendet wird.

## <a name="interoperability"></a>Interoperabilität

Ein standardmäßig konfigurierter Server kann mit SOAP-Clients kommunizieren, unabhängig davon, ob er erweiterten Schutz verwendet oder nicht. Die einzige Ausnahme sind Windows XP-und Windows Server 2003-wwsapi-Clients, die aktualisiert wurden, um den erweiterten Schutz zu unterstützen und sowohl die [**WS- \_ Kerberos- \_ apreq- \_ Nachrichten \_ Sicherheits \_ Bindung**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) als auch die [**WS \_ SSL- \_ Transport \_ \_ Sicherheitsbindung**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) Zur Unterstützung solcher Clients muss die [**\_ Erweiterte \_ Schutz \_ Richtlinie \_ nie**](/windows/desktop/api/WebServices/ne-webservices-ws_extended_protection_policy) von dem Server angegeben werden. Bei Servern, die mit der **\_ erweiterten \_ Schutz \_ Richtlinie \_ von WS** konfiguriert wurden, wird die Kommunikation von Clients, die keinen erweiterten Schutz verwenden, abgelehnt. Auf dem Client führt die **WS- \_ Kerberos- \_ apreq- \_ Nachrichten \_ Sicherheits \_ Bindung** in Kombination mit der **WS SSL- \_ \_ Transport \_ Sicherheits \_ Bindung** dazu, dass die Nachricht mithilfe der in der http-Unterteilung verwendeten Übertragungs Codierung in Vista und höher gesendet wird. Dies verursacht möglicherweise Interop-Probleme bei Servern, die eine segmentierte Übertragung nicht unterstützen.

Die folgenden enumerationszeichen/Konstanten sind Teil des erweiterten Schutzes:

-   [**Erweiterte WS- \_ \_ Schutz \_ Richtlinie**](/windows/desktop/api/WebServices/ne-webservices-ws_extended_protection_policy)
-   [**WS- \_ Szenario mit erweitertem \_ Schutz \_**](/windows/desktop/api/WebServices/ne-webservices-ws_extended_protection_scenario)

Die folgenden stucturen sind Teil des erweiterten Schutzes:

-   [**WS- \_ Dienst- \_ Sicherheits \_ Identitäten**](/windows/desktop/api/WebServices/ns-webservices-ws_service_security_identities)

 

 




