---
title: Sicherheitsübersicht
description: Das Sicherheitsframework in Windows Web Services API (WWSAPI) bietet Nachrichtenintegrität, Vertraulichkeit, Wiedergabeerkennung und Serverauthentifizierung mit Transportsicherheit.
ms.assetid: 2681bffc-ba07-4822-b265-2bf7f95297d4
keywords:
- Sicherheitsübersicht Webdienste für Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6928afd51ded7104e909994f8b625b931da6a157e859c890066c73074ae7d16
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089440"
---
# <a name="security-overview"></a>Sicherheitsübersicht

Das Sicherheitsframework in Windows Web Services API (WWSAPI) bietet:

-   Nachrichtenintegrität, Vertraulichkeit, Wiedergabeerkennung und Serverauthentifizierung mit Transportsicherheit.
-   Clientauthentifizierung, z. B. Sicherheitstokenüberprüfung, Zertifikatvertrauens- und Sperrüberprüfungen usw. mit SOAP-Nachrichtensicherheit oder Transportsicherheit.

## <a name="the-security-programming-model"></a>Das Sicherheitsprogrammiermodell

Sicherheit ist [Kommunikationskanälen zugeordnet.](channel-layer-overview.md) Das Sichern eines Kanals umfasst die folgenden Schritte.

-   Erstellen und initialisieren Sie eine oder mehrere [**Sicherheitsbindungen,**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding) die für die Sicherheitsanforderungen der Anwendung geeignet sind.
-   Erstellen Sie [**eine Sicherheitsbeschreibung,**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) die diese Sicherheitsbindungen enthält.
-   Erstellen Sie einen [**Kanal**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannel) [**oder Dienstproxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) (auf [](/windows/desktop/api/WebServices/nf-webservices-wscreatelistener) clientseitiger Seite), oder erstellen Sie einen Listener oder [**Diensthost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) (auf Serverseite), der diese Sicherheitsbeschreibung über gibt.
-   Führen Sie die normalen Schritte für die Kanalprogrammierung unter Öffnen, Akzeptieren, Senden, Empfangen, Schließen usw. aus.

Nachrichten, die über den Kanal gesendet und empfangen werden, werden automatisch von der Laufzeit gemäß der angegebenen Sicherheitsbeschreibung gesichert. Optional können diese Schritte optimiert werden, indem eine oder mehrere kanalweite Sicherheitseinstellungen [in](security-channel-settings.md) der Sicherheitsbeschreibung oder bindungsweite Sicherheitseinstellungen [in](security-binding-settings.md) einer Sicherheitsbindung angegeben werden.

Jede erforderliche Autorisierung von Absenderidentitäten muss von der Anwendung mithilfe der Sicherheitsverarbeitungsergebnisse durchgeführt werden, [die](security-processing-results.md) an jede empfangene Nachricht angefügt sind. Autorisierungsschritte werden nicht in der Sicherheitsbeschreibung angegeben und auch nicht automatisch von der Laufzeit ausgeführt.

Fehler in der Sicherheitsbeschreibung, z. B. nicht unterstützte Bindungen, nicht anwendungsfähige Eigenschaften/Felder, fehlende erforderliche Eigenschaften/Felder oder ungültige Eigenschafts-/Feldwerte, führen dazu, dass die Kanal- oder Listenererstellung fehlschlägt.

## <a name="selecting-security-bindings"></a>Auswählen von Sicherheitsbindungen

Beim Entwerfen der Sicherheit für eine Anwendung ist die wichtigste Entscheidung die Auswahl der Sicherheitsbindungen, die in die Sicherheitsbeschreibung aufgenommen werden sollen. Im Folgenden finden Sie einige Richtlinien für die Auswahl von Sicherheitsbindungen, die für das Sicherheitsszenario einer Anwendung geeignet sind. Eine nützliche Heuristik ist es, zunächst zu verstehen, welche Sicherheits-Anmeldeinformationstypen (z. B. [**X.509-Zertifikate,**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_credential) [**Windows Domänenbenutzername/-kennwörter,**](/windows/desktop/api/WebServices/ns-webservices-ws_windows_integrated_auth_credential)anwendungsdefinierte [**Benutzernamen/Kennwörter)**](/windows/desktop/api/WebServices/ns-webservices-ws_username_credential)für die Anwendung verfügbar sein werden, und dann eine Sicherheitsbindung zu wählen, die diesen Anmeldeinformationstyp verwenden kann.

-   Transportsicherheit, bei der die Sicherheit auf der Ebene des Transport bytestreams (unterhalb der SOAP-Nachrichtengrenzen) angewendet wird, ist die erste zu berücksichtigende Option.
    -   Für Internetszenarien und für Intranetszenarien, in denen ein X.509-Zertifikat auf dem Server bereitgestellt werden kann, kann die Anwendung [**WS \_ SSL TRANSPORT SECURITY BINDING \_ \_ \_ verwenden.**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) Im folgenden Beispiel wird diese Option veranschaulicht. Client: [HttpClientWithSslExample](httpclientwithsslexample.md) Server: [HttpServerWithSslExample](httpserverwithsslexample.md).

        Wenn die Clientauthentifizierung über die HTTP-Headerauthentifizierung gewünscht ist, kann eine [**WS \_ HTTP HEADER \_ \_ AUTH SECURITY \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding) hinzugefügt werden, um diese Funktionalität zu bieten.

    -   Für Intranetszenarien, Windows integrierte Authentifizierungsprotokolle wie Kerberos, NTLM und SPNEGO geeignet sind, kann die Anwendung [**WS \_ TCP \_ SSPI \_ TRANSPORT SECURITY BINDING \_ \_ verwenden.**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding) Das folgende Beispiel veranschaulicht diese Option: Client: [RequestReplyTcpClientWithWindowsTransportSecurityExample](requestreplytcpclientwithwindowstransportsecurityexample.md) Server: [RequestReplyTcpServerWithWindowsTransportSecurityExample](requestreplytcpserverwithwindowstransportsecurityexample.md).

        Client über Named Pipes: [RequestReplyNamedPipesClientWithWindowsTransportSecurityExample](requestreplynamedpipesclientwithwindowstransportsecurityexample.md)

        Server über Named Pipes: [RequestReplyNamedPipesServerWithWindowsTransportSecurityExample](requestreplynamedpipesserverwithwindowstransportsecurityexample.md)

    -   Für Lokale Computer, in denen Windows integrierte Authentifizierungsprotokolle wie Kerberos, NTLM und SPNEGO geeignet sind, kann die Anwendung [**WS \_ TCP \_ SSPI \_ TRANSPORT SECURITY \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding) oder [**WS \_ NAMEDPIPE \_ SSPI \_ TRANSPORT SECURITY BINDING \_ \_ verwenden.**](/windows/desktop/api/WebServices/ns-webservices-ws_namedpipe_sspi_transport_security_binding) Die [**WS \_ \_ NAMEDPIPE-KANALBINDUNG \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) wird in solchen Szenarien bevorzugt, da sie garantiert, dass der Datenverkehr den Computer nicht verlässt (dies ist die Eigenschaft von **WS \_ NAMEDPIPE \_ CHANNEL \_ BINDING**).

-   Sicherheit im gemischten Modus, bei der die Transportsicherheit die Verbindung schützt und ein WS-Security-Header in der SOAP-Nachricht clientauthentifizierung bietet, ist die nächste Zu berücksichtigende Option. Die folgenden Bindungen werden in Verbindung mit einer der im vorherigen Abschnitt beschriebenen Transportsicherheitsbindungen verwendet.
    -   Wenn der Client durch ein Benutzername-Kennwort-Paar auf Anwendungsebene authentifiziert wird, kann die Anwendung eine [**WS \_ USERNAME MESSAGE SECURITY \_ \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding) verwenden, um die Authentifizierungsdaten zur Verfügung zu stellen. Die folgenden Beispiele veranschaulichen die Verwendung dieser Bindung in Verbindung mit einer [**WS \_ SSL TRANSPORT \_ SECURITY \_ \_ BINDING:**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding)
        -   Client: [HttpClientWithUsernameOverSslExample](httpclientwithusernameoversslexample.md)
        -   Server: [HttpServerWithUsernameOverSslExample](httpserverwithusernameoversslexample.md)
    -   Wenn der Client durch ein Kerberos-Ticket authentifiziert wird, kann die Anwendung eine [**WS \_ KERBEROS \_ APREQ \_ MESSAGE SECURITY \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) verwenden, um die Authentifizierungsdaten bereitzustellen.
    -   Bei Verwendung eines [Sicherheitskontexts](security-context.md)richtet der Client zunächst einen Sicherheitskontext mit dem Server ein und verwendet diesen Kontext dann zum Authentifizieren von Nachrichten. Um diese Funktionalität zu aktivieren, muss die Sicherheitsbeschreibung eine [**WS \_ SECURITY CONTEXT MESSAGE SECURITY BINDING \_ \_ \_ \_ enthalten.**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) Nach dem Erstellen können Sicherheitskontexte mit einfachen Token übertragen werden, wodurch vermieden wird, dass die potenziell großen und rechenintensiven Clientanmeldeinformationen mit jeder Nachricht gesendet werden müssen.
    -   In [](federation.md) einem Verbundsicherheitsszenario erhält der Client zunächst ein Sicherheitstoken, das von einem Sicherheitstokendienst (STS) ausgestellt wurde, und präsentiert das ausgestellte Token dann einem Dienst. Clientseitig: Zum Abrufen des Sicherheitstokens vom STS kann die Anwendung [**WsRequestSecurityToken verwenden.**](/windows/desktop/api/WebServices/nf-webservices-wsrequestsecuritytoken) Alternativ kann die Anwendung eine clientseitige Sicherheitstokenanbieterbibliothek wie CardSpace oder LiveID verwenden und dann ihre Ausgabe verwenden, um mithilfe von [**WsCreateXmlSecurityToken**](/windows/desktop/api/WebServices/nf-webservices-wscreatexmlsecuritytoken)lokal ein Sicherheitstoken zu erstellen. Sobald das Sicherheitstoken für den Client verfügbar ist, kann es dem Dienst mithilfe einer Sicherheitsbeschreibung angezeigt werden, die eine [**WS \_ XML TOKEN MESSAGE SECURITY BINDING \_ \_ \_ \_ enthält.**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_token_message_security_binding) Serverseitig: Wenn das vom STS ausgestellte Sicherheitstoken ein SAML-Token ist, kann der Server eine Sicherheitsbeschreibung mit einer [**WS \_ SAML \_ MESSAGE SECURITY \_ BINDING \_ verwenden.**](/windows/desktop/api/WebServices/ns-webservices-ws_saml_message_security_binding)
        > [!Note]  
        > Windows 7 und Windows Server 2008 R2: WWSAPI unterstützt nur [Ws-Trust](http://specs.xmlsoap.org/ws/2005/02/trust/WS-Trust.pdf) und [Ws-SecureConversation,](http://specs.xmlsoap.org/ws/2005/02/sc/WS-SecureConversation.pdf) wie von [Lightweight Webdienstesicherheit Profile (LWSSP) definiert.](/openspecs/windows_protocols/ms-lwssp/376af2f8-f4fe-4577-bfd5-370ac12cac2e) Weitere Informationen zur Implementierung von Microsoft finden Sie im Abschnitt [MESSAGE Syntax (NACHRICHTENsyntax)](/openspecs/windows_protocols/ms-lwssp/d4f0f509-e14a-47b5-81e8-ade06a51d1ed) von LWSSP.

         
-   Die letzte zu berücksichtigende Option ist die Verwendung von Authentifizierungsbindungen ohne Verwendung einer Schutzbindung wie [**WS \_ SSL TRANSPORT \_ SECURITY \_ \_ BINDING.**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) Dies führt dazu, dass die Anmeldeinformationen in Klartext übertragen werden, was sich auf die Sicherheit auswirken kann. Die Verwendung dieser Option sollte sorgfältig ausgewertet werden, um sicherzustellen, dass keine Sicherheitsrisiken entstehen. Ein Beispiel für eine mögliche Verwendung ist der Austausch von Nachrichten zwischen Back-End-Servern über ein sicheres privates Netzwerk. Diese Option wird von den folgenden Konfigurationen unterstützt.

    -   [**WS \_ HTTP \_ HEADER \_ AUTH SECURITY \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding) unterstützt diese Option in allen Konfigurationen.
    -   [**WS \_ USERNAME \_ MESSAGE \_ SECURITY \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding) unterstützt diese Option auf dem Server, wenn HTTP als Transport verwendet wird.
    -   [**WS \_ KERBEROS \_ APREQ \_ MESSAGE SECURITY \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) unterstützt diese Option auf dem Server, wenn HTTP als Transport verwendet wird.
    -   [**WS \_ SECURITY \_ CONTEXT MESSAGE SECURITY \_ \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) unterstützt diese Option auf dem Server, wenn HTTP als Transport verwendet wird.
    -   [**WS \_ SAML \_ MESSAGE \_ SECURITY \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_saml_message_security_binding) unterstützt diese Option auf dem Server, wenn HTTP als Transport verwendet wird.

    Zum Aktivieren dieser Option müssen Sie [**die WS \_ PROTECTION \_ LEVEL**](/windows/desktop/api/WebServices/ne-webservices-ws_protection_level) explizit auf einen anderen Wert als **WS PROTECTION LEVEL SIGN \_ AND ENCRYPT \_ \_ \_ \_ festlegen.**

## <a name="channels-and-security"></a>Kanäle und Sicherheit

Wie bereits erwähnt, ist die Sicherheit auf Kanäle zu sehen. Darüber hinaus werden Kanalvorgänge den Sicherheitsschritten konsistent über alle Sicherheitsbindungen hinweg zuordnen.

-   Kanalerstelle: Der Satz von Sicherheitsbindungen, die in der Sicherheitsbeschreibung angegeben sind, wird überprüft und bleibt danach für den Kanal korrigiert. Außerdem wird die Form des Kanalstapels bestimmt, einschließlich aller Seitenkanäle, die für WS-Trust auf Der Basis von Effekten verwendet werden sollen.
-   Kanal geöffnet: Alle Anmeldeinformationen, die als Teil von Sicherheitsbindungen bereitgestellt werden, werden geladen, und Sicherheitssitzungen werden eingerichtet. Im Allgemeinen enthält ein offener Kanal den Sicherheitsstatus "Live". Beim Öffnen eines Clientkanals wird auch die Endpunktadresse des Servers angegeben, für die die Serverauthentifizierung von der Laufzeit durchgeführt wird.
-   Zwischen geöffneten und schließenden Kanälen: Während dieser Phase können Nachrichten sicher gesendet und empfangen werden.
-   Nachrichtensendung: Sicherheitskontexttoken werden bei Bedarf erhalten oder erneuert, und die Sicherheit wird gemäß der Sicherheitsbeschreibung auf jede übertragene Nachricht angewendet. Fehler, die beim Anwenden der Sicherheit auftreten, werden als Sendefehler an die Anwendung zurückgegeben.
-   Nachrichten empfangen: Die Sicherheit wird für jede empfangene Nachricht gemäß der Sicherheitsbeschreibung überprüft. Alle Fehler bei der Nachrichtensicherheitsüberprüfung werden als Empfangsfehler an die Anwendung zurückgegeben. Diese Pro-Nachricht-Fehler wirken sich nicht auf den Kanalzustand oder nachfolgende Empfangene aus. Die Anwendung kann einen fehlgeschlagenen Empfang verwerfen und einen Empfang für eine andere Nachricht neu starten.
-   Kanalabbruch: Der Kanal kann jederzeit abgebrochen werden, um alle E/A-Nachrichten im Kanal anzuhalten. Bei einem Abbruch geht der Kanal in einen fehlerhaften Zustand über und lässt keine weitere Sende- oder Sende- oder Sende empfangene Daten zu. Der Kanal behält jedoch möglicherweise weiterhin einen "live"-Sicherheitsstatus bei, sodass ein nachfolgender Kanalschluss erforderlich ist, um den zustandsbereinigungsbereinigten Zustand zu veräussern.
-   Kanal schließen: Der beim Öffnen erstellte Sicherheitsstatus wird verworfen, und Sitzungen werden heruntergefahren. Sicherheitskontexttoken werden abgebrochen. Der Kanalstapel bleibt erhalten, enthält aber keinen "Live"-Sicherheitsstatus oder geladene Anmeldeinformationen.
-   Kanalfrei: Der bei der Erstellung erstellte Kanalstapel wird zusammen mit allen Sicherheitsressourcen frei.

## <a name="security-apis"></a>Sicherheits-APIs

Die API-Dokumentation für die Sicherheit ist in die folgenden Themen eingekreist.

-   [Sicherheitsbeschreibung](security-description.md)
    -   [Sicherheitskanal-Einstellungen](security-channel-settings.md)
    -   [Sicherheitsbindungen](security-bindings.md)
        -   [Sicherheitsanmeldeinformationen](security-credentials.md)
        -   [Sicherheitsbindungseinstellungen](security-binding-settings.md)
-   [Verbund](federation.md)
-   [Sicherheitskontext](security-context.md)
-   [Endpunktidentität](endpoint-identity.md)
-   [Ergebnisse der Sicherheitsverarbeitung](security-processing-results.md)

## <a name="security"></a>Sicherheit

Bei Verwendung der WWSAPI-Sicherheits-API sind Anwendungen mehreren Sicherheitsrisiken ausgesetzt:

<dl> <dt>

<span id="Accidental_misconfiguration"></span><span id="accidental_misconfiguration"></span><span id="ACCIDENTAL_MISCONFIGURATION"></span>Versehentliche Fehlkonfiguration
</dt> <dd>

WWSAPI unterstützt eine Reihe von sicherheitsbezogenen Konfigurationsoptionen. Siehe z.B. [**WS \_ SECURITY BINDING PROPERTY \_ \_ \_ ID**](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_property_id). Einige dieser Optionen, z. **B. WS \_ SECURITY BINDING PROPERTY ALLOW ANONYMOUS \_ \_ \_ \_ \_ CLIENTS,** ermöglichen es der Anwendung, die Standardsicherheitsstufe zu verringern, die von den verschiedenen Sicherheitsbindungen bereitgestellt wird. Die Verwendung solcher Optionen sollte sorgfältig ausgewertet werden, um sicherzustellen, dass keine resultierenden Angriffsvektoren vorhanden sind.

Darüber hinaus ermöglicht WWSAPI einer Anwendung, wie oben beschrieben, bestimmte Schritte absichtlich zu deaktivieren, die zum vollständigen Schützen eines Nachrichtenaustauschs erforderlich sind, z. B. das Deaktivieren der Verschlüsselung, obwohl Sicherheitsanmeldeinformationen übertragen werden. Dies ist zulässig, um bestimmte Szenarien zu ermöglichen und sollte nicht für die allgemeine Kommunikation verwendet werden. Die [**\_ WS-SCHUTZEBENE \_**](/windows/desktop/api/WebServices/ne-webservices-ws_protection_level) muss speziell herabgesetzt werden, um diese Szenarien zu ermöglichen, und Anwendungen sollten diesen Wert nur ändern, wenn dies unbedingt erforderlich ist, da dadurch viele Überprüfungen deaktiviert werden, die eine sichere Konfiguration gewährleisten.

</dd> <dt>

<span id="Storing_confidential_information_in_memory"></span><span id="storing_confidential_information_in_memory"></span><span id="STORING_CONFIDENTIAL_INFORMATION_IN_MEMORY"></span>Speichern vertraulicher Informationen im Arbeitsspeicher
</dt> <dd>

Vertrauliche Informationen, z. B. Kennwörter, die im Arbeitsspeicher gespeichert sind, sind anfällig für die Extraktion durch einen privilegierten Angreifer, z. B. die Auslagerungsdatei. WWSAPI erstellt eine Kopie der angegebenen Anmeldeinformationen und verschlüsselt diese Kopie, sodass die ursprünglichen Daten nicht geschützt sind. Es liegt in der Verantwortung der Anwendung, die ursprüngliche Instanz zu schützen. Darüber hinaus wird die verschlüsselte Kopie kurz entschlüsselt, während sie verwendet wird, und öffnet ein Fenster, um sie zu extrahieren.

</dd> <dt>

<span id="Denial_of_service"></span><span id="denial_of_service"></span><span id="DENIAL_OF_SERVICE"></span>Denial-of-Service-Angriffe
</dt> <dd>

Die Sicherheitsverarbeitung kann erhebliche Ressourcen verbrauchen. Jede zusätzliche Sicherheitsbindung erhöht diese Kosten. WWSAPI bricht die Sicherheitsverarbeitung ab, sobald ein Fehler bei der Sicherheitsüberprüfung auftritt. Bestimmte Überprüfungen wie Autorisierungsentscheidungen werden jedoch erst durchgeführt, nachdem umfangreiche Arbeit ausgeführt wurde.

Während eine Nachricht auf dem Server verarbeitet wird, wird der Sicherheitsstatus auf dem Nachrichtenheap gespeichert. Die Anwendung kann den Arbeitsspeicherverbrauch während der Sicherheitsverarbeitung einschränken, indem sie die Größe dieses Heaps über WS \_ MESSAGE PROPERTY HEAP PROPERTIES \_ \_ \_ reduziert. Darüber hinaus können bestimmte Sicherheitsbindungen, z. B. die WS \_ SECURITY CONTEXT MESSAGE SECURITY \_ \_ \_ \_ BINDING, dazu führen, dass der Server Ressourcen im Auftrag des Clients zuweist. Die Grenzwerte für diese Ressourcen können mithilfe der folgenden [**WS \_ SECURITY BINDING \_ PROPERTY \_ \_ ID-Werte**](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_property_id) konfiguriert werden:

-   \_ \_ WS-SICHERHEITSBINDUNGSEIGENSCHAFT \_ \_ \_ SICHERHEITSKONTEXT \_ \_ MAX. AUSSTEHENDE \_ KONTEXTE
-   \_ \_ WS-SICHERHEITSBINDUNGSEIGENSCHAFT \_ \_ \_ SICHERHEITSKONTEXT \_ \_ MAX. AKTIVE \_ KONTEXTE
-   ERNEUERUNGSINTERVALL FÜR SICHERHEITSKONTEXT DER WS-SICHERHEITSBINDUNGSEIGENSCHAFT \_ \_ \_ \_ \_ \_ \_
-   \_ \_ \_ \_ WS-SICHERHEITSBINDUNGSEIGENSCHAFTENSICHERHEITSKONTEXTROLLOVERINTERVALL \_ \_ \_

Wenn Sie diese Grenzwerte auf niedrige Werte festlegen, wird der maximale Arbeitsspeicherverbrauch verringert, aber es kann dazu führen, dass legitime Clients abgelehnt werden, wenn das Kontingent erreicht wird.

</dd> </dl>

 

 