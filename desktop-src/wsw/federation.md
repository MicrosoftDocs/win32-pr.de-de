---
title: Verbund
description: Der Verbund ermöglicht die Delegierung der Autorisierungs Autorität an andere Member einer Interprise.
ms.assetid: 574496df-95dc-45f7-8c42-e646aec12e69
keywords:
- Verbund-Webdienste für Windows
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45a02744c9c0a5358da35f4c31c20633c420fee9
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/12/2021
ms.locfileid: "104559948"
---
# <a name="federation"></a>Verbund

Der Verbund ermöglicht die Delegierung der Autorisierungs Autorität an andere Member einer Interprise. Stellen Sie sich z. b. das folgende Geschäftsproblem vor: das automatische Teilehersteller Konto von "Fabrikam Inc" möchte den autorisierten Mitarbeitern des Kunden Fabrikam Inc den sicheren Zugriff auf den Webdienst von "Webdienst für die Teile Bestellung" von Configuration Manager gewähren. Eine Sicherheitslösung für dieses Szenario besteht darin, dass von Configuration Manager ein Vertrauens Mechanismus mit Fabrikam eingerichtet wird, um die Zugriffs Autorisierungs Entscheidung an fabrikam zu delegieren. Dieser Prozess kann folgendermaßen funktionieren:

-   Fabrikam, wenn es ein Partner von "Configuration Manager" wird, richtet eine Vertrauens Vereinbarung mit "Configuration Manager" ein. Das Ziel dieses Schritts besteht darin, den Sicherheitstokentyp und den Inhalt zu akzeptieren, der die Autorisierung von Fabrikam repräsentiert und für "antoso" akzeptabel ist. Es kann z. b. beschlossen werden, dass ein vertrauenswürdiges X. 509-Zertifikat mit dem Antragsteller Namen "CN = Fabrikam Inc Supplier STS" ein SAML-Token signieren muss, damit diese SAML vom Webdienst von "Webdienst" akzeptiert wird. Außerdem wird möglicherweise entschieden, dass der Sicherheitsanspruch im ausgestellten SAML-Token entweder ' https://schemas.contoso.com/claims/lookup ' (für die Teil Such Autorisierung) oder ' https://schemas.contoso.com/claims/order ' (für die Autorisierung der Teilbestellung) lauten soll.
-   Wenn ein Fabrikam-Mitarbeiter die Anwendung für die interne Teile Bestellung verwendet, kontaktiert er zunächst einen Sicherheitstokendienst (Security Token Service, STS) in fabrikam. Dieser Mitarbeiter wird mithilfe des internen Fabrikam-Sicherheitsmechanismus (z. b. Windows-Domäne Benutzername/Kennwort) authentifiziert, seine Autorisierung für Bestell Teile wird überprüft, und er gibt ein kurzlebiges SAML-Token aus, das die entsprechenden Ansprüche enthält und durch das oben beschriebene X. 509-Zertifikat signiert wurde. Die Anwendung für die Teile Bestellung kontaktiert dann den Dienst "Configuration Manager", der das ausgestellte SAML-Token zum Authentifizieren und Ausführen der Bestell Aufgabe darstellt.

Hier fungiert der Fabrikam-STS als "ausstellende Partei", und der "Configuration Manager"-Parts-Dienst fungiert als "vertrauende Seite". ![Das Diagramm zeigt eine ausstellende Partei und eine vertrauende Seite in einem Verbund.](images/stsmodel.png)

## <a name="federation-features"></a>Verbund Funktionen

Im folgenden finden Sie die unterstützten Sicherheitsfeatures für die Parteien oder Rollen, die an einem Verbund Szenario beteiligt sind:

-   Client seitig: zum Abrufen des Sicherheits Tokens vom STS kann eine [**wsrequestsecuritytoken**](/windows/desktop/api/WebServices/nf-webservices-wsrequestsecuritytoken) -Funktion verwendet werden. Alternativ dazu kann eine Client seitige sicherheitstokenanbieterbibliothek wie z. b. CardSpace oder LiveID verwendet werden. Anschließend wird Ihre Ausgabe verwendet, um mithilfe von [**wscreatexmlsecuritytoken**](/windows/desktop/api/WebServices/nf-webservices-wscreatexmlsecuritytoken)lokal ein Sicherheits Token zu erstellen. Wenn der Client über das Sicherheits Token verfügt, kann er dann einen Kanal zu dem Dienst erstellen, der die [**WS \_ XML \_ - \_ tokennachrichtensicherheitsbindung \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_token_message_security_binding) angibt, um das Token zu präsentieren, sowie eine Transport Sicherheitsbindung, wie z. b. [**WS \_ SSL- \_ Transport \_ Sicherheits \_ Bindung**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) zum Schutz des Kanals.
-   Serverseitig: bei einem Verbund Szenario mit einem Sicherheitstokendienst, der SAML-Token ausgibt, kann der Server die [**WS \_ SAML- \_ Nachrichten \_ Sicherheits \_ Bindung**](/windows/desktop/api/WebServices/ns-webservices-ws_saml_message_security_binding)zusammen mit einer Transport Sicherheitsbindung wie der [**WS \_ SSL- \_ Transport \_ Sicherheits \_**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) Bindung zum Schutz des Kanals verwenden.
-   STS-Side: Beachten Sie, dass STS eine Webdienst Anwendung ist und die Sicherheitsanforderungen für diejenigen, die ein Sicherheits Token anfordern, mithilfe einer [**Sicherheits Beschreibungs**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) Struktur zum Erstellungs Zeitpunkt des listenerstellers, wie jeder andere sichere Webdienst, angeben kann. Anschließend können eingehende Anforderungs Nachrichten-Nutzlasten analysiert werden, um die Tokenanforderungen zu überprüfen und ausgestellte Token als Nutzlasten für die Antwortnachricht zurücksenden. Zurzeit werden keine Funktionen bereitgestellt, um diese auszuführenden und auszuführenden Schritte zu unterstützen.

Beachten Sie, dass die Clientseite das ausgegebene Sicherheits Token generisch als XML-Sicherheits Token verarbeiten kann, ohne den Tokentyp zu kennen oder eine tokentypspezifische Verarbeitung durchzuführen. Der Server muss jedoch den spezifischen Sicherheitstokentyp verstehen, um ihn zu verstehen und zu verarbeiten. In den Schritten für Sicherheitstokenanforderungen und-Antworten werden die in der WS-Trust Spezifikation definierten Konstrukte verwendet.

## <a name="more-complex-federation-scenarios"></a>Komplexere Verbund Szenarien

Ein Verbund Szenario kann mehrere Sicherheitstokendienste umfassen, die eine Verbund Kette bilden. Betrachten Sie das folgenden Beispiel:

-   Der Client authentifiziert sich beim LiveID-STS mit einem LiveID-Benutzernamen/-Kennwort und erhält ein Sicherheits Token T1.
-   Der Client authentifiziert sich mit T1 bei sts1 und erhält ein Sicherheits Token T2.
-   Client authentifiziert sich mit T2 bei STS2 und erhält ein Sicherheits Token T3.
-   Der Client wird mithilfe von T3 bei den Ziel Diensten authentifiziert.

Hier bilden die LiveID STS, sts1, STS2 und S die Verbund Kette. Die Sicherheitstokendienste in einer Verbund Kette können verschiedene Rollen für das gesamte Anwendungsszenario durchführen. Beispiele für funktionstüchtige STS-Rollen sind Identitäts Anbieter, Autorisierungs Entscheidungsträger, anonymizer und Ressourcen-Manager.

## <a name="sts-request-parameters-and-metadata-exchange"></a>STS-Anforderungs Parameter und Metadatenaustausch

Damit der Client einen erfolgreichen [**wsrequestsecuritytoken**](/windows/desktop/api/WebServices/nf-webservices-wsrequestsecuritytoken) -Aufrufvorgang ausführen kann, muss er die Parameter dieses Aufrufes (z. b. den erforderlichen Tokentyp und die Anspruchs Typen), die [**Sicherheits Beschreibungs**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) Anforderungen des Anforderungs Kanals an den STS und die [Endpunkt Adresse](endpoint-address.md) des STS kennen. Die Client Anwendung kann die folgenden Techniken zum Ermitteln dieser Informationen verwenden:

-   Die Informationen in der Anwendung werden im Rahmen der Entwurfszeit Entscheidungen hart codiert.
-   Lesen Sie diese Informationen aus einer Konfigurationsdatei auf Anwendungsebene, die vom lokalen Anwendungs Bereitsteller eingerichtet wurde.
-   Diese Informationen zur Laufzeit dynamisch ermitteln, indem Sie die Funktion zum [Importieren von Metadaten](metadata-import.md) mit der [**\_ \_ \_ \_ Sicherheits \_ Bindungs \_**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint) Einschränkungs Struktur der WS-Token-Nachricht verwenden.

Um die Verwendung von Dynamic MEX mit Verbund zu veranschaulichen, sehen Sie sich das obige 3 STS-Beispiel an. Der Client führt zunächst einen dynamischen MEX mit S aus, um Informationen zu T3 (d. h. zur Frage, was von STS2 angefordert werden soll) sowie zur STS2 Dynamic MEX-Adresse (d.h. zum Suchen von STS2) zu erhalten. Diese Informationen werden dann für einen dynamischen MEX mit STS2 verwendet, um Informationen zu T2 und sts1 zu ermitteln usw.

Folglich werden die dynamischen MEX-Schritte in der Reihenfolge 4, 3, 2, 1 durchgeführt, um die Verbund Kette zu erstellen, und die tokenanforderungs-und Präsentations Schritte werden in der Reihenfolge 1, 2, 3, 4 ausgeführt, um die Verbund Kette zu entladen.

> [!Note]  
> Windows 7 und Windows Server 2008 R2: wwsapi unterstützt nur [WS-Trust](https://specs.xmlsoap.org/ws/2005/02/trust/WS-Trust.pdf) und [WS-SecureConversation](https://specs.xmlsoap.org/ws/2005/02/sc/WS-SecureConversation.pdf) gemäß der Definition durch [Lightweight Webdienstesicherheit profile (lwssp)](/openspecs/windows_protocols/ms-lwssp/376af2f8-f4fe-4577-bfd5-370ac12cac2e). Ausführliche Informationen zur Implementierung von Microsoft finden Sie im Abschnitt zur [Nachrichten Syntax](/openspecs/windows_protocols/ms-lwssp/d4f0f509-e14a-47b5-81e8-ade06a51d1ed) von lwssp.

 

 

 