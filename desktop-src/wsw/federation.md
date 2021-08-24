---
title: Verbund
description: Der Verbund ermöglicht die Delegierung der Autorisierungsstelle an andere Mitglieder einer Interprise.
ms.assetid: 574496df-95dc-45f7-8c42-e646aec12e69
keywords:
- Verbundwebdienste für Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9a902eb9469ad75e8c3c5a283284a009af11bb59b42470c91c39b1f16f83c61
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119703655"
---
# <a name="federation"></a>Verbund

Der Verbund ermöglicht die Delegierung der Autorisierungsstelle an andere Mitglieder einer Interprise. Betrachten Sie beispielsweise das folgende Geschäftsproblem: Das Autoparts-Fertigungsunternehmen Contoso Ltd möchte autorisierten Mitarbeitern des Kunden Fabrikam Inc den sicheren Zugriff auf den Webdienst des Contoso-Teileauftrags ermöglichen. Eine Sicherheitslösung für dieses Szenario besteht in der Einrichtung eines Vertrauensmechanismus mit Fabrikam, um die Zugriffsautorisierungsentscheidung an Fabrikam zu delegieren. Dieser Prozess kann wie folgt funktionieren:

-   Wenn Fabrikam Partner von Contoso wird, richtet er eine Vertrauensstellung mit Contoso ein. Das Ziel dieses Schritts besteht darin, sich auf den Sicherheitstokentyp und den Inhalt zu einigen, die die Fabrikam-Autorisierung darstellen und für Contoso akzeptabel sind. Beispielsweise kann entschieden werden, dass ein vertrauenswürdiges X.509-Zertifikat mit dem Betreffnamen "CN=Fabrikam Inc Supplier STS" ein SAML-Token für diese SAML signiert, damit es vom Contoso-Webdienst akzeptiert wird. Darüber hinaus kann entschieden werden, dass der Sicherheitsanspruch im ausgestellten SAML-Token entweder ' ' (für die Autorisierung der Teilsuche) oder ' ' ' (für die Autorisierung der https://schemas.contoso.com/claims/lookup Teilebestellung) https://schemas.contoso.com/claims/order sein sollte.
-   Wenn ein Fabrikam-Mitarbeiter die Anwendung für die interne Teilebestellung verwendet, kontaktiert er zunächst einen Sicherheitstokendienst (STS) in Fabrikam. Dieser Mitarbeiter wird mit dem internen Fabrikam-Sicherheitsmechanismus authentifiziert (z. B. Windows Domänenbenutzername/-kennwort), seine Autorisierung zum Bestellen von Teilen wird überprüft, und er wird ein kurzlebiges SAML-Token mit den entsprechenden Ansprüchen ausgestellt und durch das oben entschiedene X.509-Zertifikat signiert. Die Anwendung für die Teilebestellung kontaktiert dann den Contoso-Dienst, der das ausgestellte SAML-Token zur Authentifizierung und Durchführung der Bestellaufgabe präsentiert.

Hier fungiert der Fabrikam STS als "ausstellende Partei", und der Contoso-Teiledienst fungiert als "vertrauende Partei". ![Diagramm, das eine ausstellende Partei und eine vertrauende Partei in einem Verbund zeigt.](images/stsmodel.png)

## <a name="federation-features"></a>Verbundfeatures

Im Folgenden finden Sie die unterstützten Sicherheitsfeatures für die Parteien oder Rollen, die an einem Verbundszenario beteiligt sind:

-   Clientseitig: Zum Abrufen des Sicherheitstokens vom STS kann die [**WsRequestSecurityToken-Funktion verwendet**](/windows/desktop/api/WebServices/nf-webservices-wsrequestsecuritytoken) werden. Alternativ können Sie eine clientseitige Bibliothek für Sicherheitstokenanbieter wie CardSpace oder LiveID verwenden und dann ihre Ausgabe verwenden, um mithilfe von [**WsCreateXmlSecurityToken**](/windows/desktop/api/WebServices/nf-webservices-wscreatexmlsecuritytoken)lokal ein Sicherheitstoken zu erstellen. In beiden Fällen kann der Client, sobald er über das Sicherheitstoken verfügt, einen Kanal zum Dienst erstellen, der [**WS \_ XML TOKEN MESSAGE SECURITY \_ \_ \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_token_message_security_binding) zum Präsentieren des Tokens zusammen mit einer Transportsicherheitsbindung wie [**WS SSL TRANSPORT SECURITY \_ \_ \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) zum Schutz des Kanals anknöpf.
-   Serverseitig: In einem Verbundszenario mit einem Sicherheitstokendienst, der SAML-Token aus gibt, kann der Server die [**WS \_ SAML \_ MESSAGE SECURITY \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_saml_message_security_binding)zusammen mit einer Transportsicherheitsbindung wie [**WS SSL TRANSPORT SECURITY \_ \_ \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) verwenden, um den Kanal zu schützen.
-   STS-seite: Beachten Sie, dass der STS eine Webdienstanwendung ist und die Sicherheitsanforderungen für [](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) diejenigen angeben kann, die ein Sicherheitstoken von ihm anfordern. Dabei wird zum Zeitpunkt der Listenererstellung eine Sicherheitsbeschreibungsstruktur verwendet, wie dies bei jedem anderen sicheren Webdienst der Fall wäre. Anschließend kann er eingehende Anforderungsnachrichtennutzlasten analysieren, um die Tokenanforderungen zu überprüfen und ausgestellte Token als Antwortnachrichtennutzlasten zurücksingen. Derzeit werden keine Features bereitgestellt, um diese Analyse- und Ausgabeschritte zu unterstützen.

Beachten Sie, dass die Clientseite das ausgestellte Sicherheitstoken generisch als XML-Sicherheitstoken behandeln kann, ohne den Tokentyp zu kennen oder eine spezifische Verarbeitung des Tokentyps zu tun. Der Server muss jedoch den spezifischen Sicherheitstokentyp verstehen, um ihn zu verstehen und zu verarbeiten. In den Schritten zur Sicherheitstokenanforderung und -antwort werden die in der WS-Trust definierten Konstrukte verwendet.

## <a name="more-complex-federation-scenarios"></a>Komplexere Verbundszenarien

Ein Verbundszenario kann mehrere STS umfassen, die eine Verbundkette bilden. Betrachten Sie das folgenden Beispiel:

-   Der Client authentifiziert sich beim LiveID STS mithilfe eines LiveID-Benutzernamens/-Kennworts und erhält ein Sicherheitstoken T1.
-   Der Client authentifiziert sich bei STS1 mithilfe von T1 und erhält ein Sicherheitstoken T2.
-   Der Client authentifiziert sich bei STS2 mithilfe von T2 und erhält ein Sicherheitstoken T3.
-   Der Client authentifiziert sich mit T3 beim Zieldienst S.

Hier bilden LiveID STS, STS1, STS2 und S die Verbundkette. Die STS in einer Verbundkette können verschiedene Rollen für das gesamte Anwendungsszenario ausführen. Beispiele für solche funktionalen STS-Rollen sind Identitätsanbieter, Autorisierungsentscheidungsträger, Anonymisierer und Ressourcen-Manager.

## <a name="sts-request-parameters-and-metadata-exchange"></a>STS-Anforderungsparameter und Exchange

Damit der Client einen erfolgreichen [**WsRequestSecurityToken-Aufruf**](/windows/desktop/api/WebServices/nf-webservices-wsrequestsecuritytoken) ausführen kann, muss er die Parameter dieses Aufrufs (z. B. den erforderlichen Tokentyp und Anspruchstypen), die Sicherheitsbeschreibungsanforderungen des Anforderungskanals an den STS und die Endpunktadresse des STS kennen. [](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) [](endpoint-address.md) Die Clientanwendung kann eine der folgenden Verfahren verwenden, um diese Informationen zu bestimmen:

-   Schreiben Sie die Informationen in der Anwendung im Rahmen der Entwurfszeitentscheidungen hart.
-   Lesen Sie diese Informationen aus einer Konfigurationsdatei auf Anwendungsebene, die vom lokalen Anwendungs deployer eingerichtet wurde.
-   Diese Informationen werden zur Laufzeit [](metadata-import.md) dynamisch mithilfe des Metadatenimportfeatures mit der [**WS \_ ISSUED TOKEN MESSAGE SECURITY BINDING \_ \_ \_ \_ \_ CONSTRAINT-Struktur**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint) gefunden.

Um die Verwendung von dynamischem MEX mit Verbund zu veranschaulichen, sehen Sie sich das obige Beispiel 3 STS an. Der Client verwendet zunächst ein dynamisches MEX mit S, um Informationen zu T3 (d. h. was von STS2 zu fragen ist) sowie die dynamische MEX-Adresse STS2 (d. h. wo STS2 zu finden ist) zu erhalten. Diese Informationen werden dann verwendet, um eine dynamische MEX mit STS2 zu verwenden, um Informationen zu T2 und STS1 zu finden, und so weiter.

Daher werden die dynamischen MEX-Schritte in der Reihenfolge 4, 3, 2, 1 zum Erstellen der Verbundkette und die Tokenanforderungs- und Präsentationsschritte in der Reihenfolge 1, 2, 3, 4 zum Entladung der Verbundkette stattfinden.

> [!Note]  
> Windows 7 und Windows Server 2008 R2: WWSAPI unterstützt nur [Ws-Trust](https://specs.xmlsoap.org/ws/2005/02/trust/WS-Trust.pdf) und [Ws-SecureConversation,](https://specs.xmlsoap.org/ws/2005/02/sc/WS-SecureConversation.pdf) wie von [Lightweight Webdienstesicherheit Profile (LWSSP) definiert.](/openspecs/windows_protocols/ms-lwssp/376af2f8-f4fe-4577-bfd5-370ac12cac2e) Weitere Informationen zur Implementierung von Microsoft finden Sie im Abschnitt [MESSAGE Syntax (NACHRICHTENsyntax)](/openspecs/windows_protocols/ms-lwssp/d4f0f509-e14a-47b5-81e8-ade06a51d1ed) von LWSSP.

 

 

 