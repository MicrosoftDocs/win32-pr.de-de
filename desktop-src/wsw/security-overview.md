---
title: Sicherheitsübersicht
description: Das Sicherheits Framework in der Windows-Webdienste-API (wwsapi) bietet Nachrichten Integrität, Vertraulichkeit, Wiedergabe Erkennung und Server Authentifizierung mithilfe der Transportsicherheit.
ms.assetid: 2681bffc-ba07-4822-b265-2bf7f95297d4
keywords:
- Sicherheitsübersicht Webdienste für Windows
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 741e98ef023c0bae146b5fde582484f2dd133df6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473772"
---
# <a name="security-overview"></a>Sicherheitsübersicht

Das Sicherheits Framework in der Windows-Webdienste-API (wwsapi) bietet Folgendes:

-   Nachrichten Integrität, Vertraulichkeit, Wiedergabe Erkennung und Server Authentifizierung mit Transportsicherheit.
-   Client Authentifizierung, z. b. Überprüfung des Sicherheits Tokens, Zertifikats Vertrauensstellung und Sperr Überprüfungen usw. mithilfe von SOAP-Nachrichten Sicherheit oder Transportsicherheit

## <a name="the-security-programming-model"></a>Das Sicherheits Programmiermodell

Die Sicherheit ist mit [Kommunikationskanälen](channel-layer-overview.md)verknüpft. Das Sichern eines Kanals besteht aus den folgenden Schritten.

-   Erstellen und initialisieren Sie eine oder mehrere [**Sicherheits Bindungen**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding) , die den Sicherheitsanforderungen der Anwendung entsprechen.
-   Erstellen Sie eine [**Sicherheits Beschreibung**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) , die diese Sicherheits Bindungen enthält.
-   Erstellen Sie einen [**Kanal**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannel) -oder [**Dienst Proxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) (auf der Clientseite), oder erstellen Sie einen [**Listener**](/windows/desktop/api/WebServices/nf-webservices-wscreatelistener) oder [**Dienst Host**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) (auf der Serverseite), und übergeben Sie die Sicherheits Beschreibung.
-   Führen Sie die üblichen Schritte zur Kanal Programmierung von öffnen, annehmen, senden, empfangen, schließen usw. aus.

Nachrichten, die auf dem Kanal gesendet und empfangen werden, werden von der Laufzeit automatisch entsprechend der angegebenen Sicherheits Beschreibung gesichert. Optional können diese Schritte optimiert werden, indem Sie eine oder mehrere [Kanal weite Sicherheitseinstellungen](security-channel-settings.md) in der Sicherheits Beschreibung oder die [Bindungs weiten Sicherheitseinstellungen](security-binding-settings.md) in einer Sicherheitsbindung angeben.

Jede erforderliche Autorisierung von Absender Identitäten muss von der Anwendung mithilfe der an jede empfangene Nachricht angefügten [sicherheitsverarbeitungs Ergebnisse](security-processing-results.md) durchgeführt werden. In der Sicherheits Beschreibung sind keine Autorisierungs Schritte angegeben, und Sie werden nicht automatisch von der Laufzeit ausgeführt.

Fehler in der Sicherheits Beschreibung, z. b. nicht unterstützte Bindungen, nicht anwendbare Eigenschaften/Felder, fehlende erforderliche Eigenschaften/Felder oder ungültige Eigenschafts-/Feldwerte, führen zu einem Fehler bei der Kanal-oder listenererstellung.

## <a name="selecting-security-bindings"></a>Auswählen von Sicherheits Bindungen

Beim Entwerfen der Sicherheit für eine Anwendung ist die wichtigste Entscheidung die Auswahl der Sicherheits Bindungen, die in die Sicherheits Beschreibung eingeschlossen werden sollen. Im folgenden finden Sie einige Richtlinien für die Auswahl von Sicherheits Bindungen, die für das Sicherheitsszenario einer Anwendung geeignet sind. Eine nützliche heuristische Aufgabe besteht darin, zuerst zu verstehen, welche Sicherheits Anmelde Informationstypen (z [**. b. X. 509-Zertifikate**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_credential), [**Windows-Domänen Benutzernamen/-Kenn Wörter**](/windows/desktop/api/WebServices/ns-webservices-ws_windows_integrated_auth_credential), [**Anwendungs definierter Benutzername/**](/windows/desktop/api/WebServices/ns-webservices-ws_username_credential)Kennwort) für die Anwendung verfügbar sind, und dann eine Sicherheitsbindung auszuwählen, die diesen Anmelde Informationstyp verwenden kann.

-   Die Transportsicherheit, bei der Sicherheit auf der Transport Byte Datenstrom-Ebene (unterhalb der SOAP-Nachrichten Grenzen) angewendet wird, ist die erste zu berücksichtigende Option.
    -   Für Internet Szenarios und für Intranetszenarien, in denen ein X. 509-Zertifikat auf dem Server bereitgestellt werden kann, verwendet die Anwendung möglicherweise die [**WS \_ SSL- \_ Transport \_ Sicherheits \_ Bindung**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding). Diese Option wird im folgenden Beispiel veranschaulicht. Client: [httpclientwithsslexample](httpclientwithsslexample.md) Server: [httpserverwithsslexample](httpserverwithsslexample.md).

        Wenn die Client Authentifizierung über die HTTP-Header Authentifizierung gewünscht ist, kann eine WS-HTTP-Header Authentifizierung- [**\_ \_ \_ \_ Sicherheits \_ Bindung**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding) hinzugefügt werden, um diese Funktionalität bereitzustellen.

    -   Bei Intranetszenarien, in denen integrierte Windows-Authentifizierungsprotokolle wie Kerberos, NTLM und SPNEGO geeignet sind, verwendet die Anwendung möglicherweise die [**WS \_ TCP- \_ SSPI- \_ Transport \_ Sicherheits \_ Bindung**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding). Das folgende Beispiel veranschaulicht diese Option: Client: [requestreplytcpclientwithwindowstransportsecurityexample](requestreplytcpclientwithwindowstransportsecurityexample.md) Server: [requestreplytcpserverwithwindowstransportsecurityexample](requestreplytcpserverwithwindowstransportsecurityexample.md).

        Client über Named Pipes: [requestreplynamedpipesclientwithwindowstransportsecurityexample](requestreplynamedpipesclientwithwindowstransportsecurityexample.md)

        Server over Named Pipes: [requestreplynamedpipesserverwithwindowstransportsecurityexample](requestreplynamedpipesserverwithwindowstransportsecurityexample.md)

    -   Für Szenarien mit lokalen Computern, in denen integrierte Windows-Authentifizierungsprotokolle wie Kerberos, NTLM und SPNEGO geeignet sind, verwendet die Anwendung möglicherweise die [**WS \_ TCP- \_ SSPI- \_ Transport \_ Sicherheits \_ Bindung**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding) oder die [**WS- \_ NamedPipe- \_ SSPI- \_ Transport \_ Sicherheits \_ Bindung**](/windows/desktop/api/WebServices/ns-webservices-ws_namedpipe_sspi_transport_security_binding). Die [**WS- \_ NamedPipe- \_ Kanal \_ Bindung**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) wird in solchen Szenarien bevorzugt, da sie sicherstellt, dass der Datenverkehr den Computer nicht verlässt (Dies ist die Eigenschaft der **WS- \_ NamedPipe- \_ \_ channelbindung**).

-   Die Sicherheit im gemischten Modus, bei der die-Transportsicherheit die Verbindung schützt und ein WS-Security-Header in der SOAP-Nachricht die Client Authentifizierung bereitstellt, ist die nächste zu berücksichtigende Option. Die folgenden Bindungen werden in Verbindung mit einer der Transport Sicherheits Bindungen verwendet, die im vorherigen Abschnitt beschrieben wurden.
    -   Wenn der Client durch ein Benutzername/Kennwort-Paar auf Anwendungsebene authentifiziert wird, kann die Anwendung eine [**WS \_ username \_ Message- \_ Sicherheits \_ Bindung**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding) verwenden, um die Authentifizierungsdaten bereitzustellen. In den folgenden Beispielen wird die Verwendung dieser Bindung in Verbindung mit einer [**WS \_ SSL- \_ Transport \_ Sicherheits \_ Bindung**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding)veranschaulicht:
        -   Client: [httpclientwithusernameoversslexample](httpclientwithusernameoversslexample.md)
        -   Server: [httpserverwithusernameoversslexample](httpserverwithusernameoversslexample.md)
    -   Wenn der Client durch ein Kerberos-Ticket authentifiziert wird, kann die Anwendung eine [**WS- \_ Kerberos- \_ apreq- \_ Nachrichten \_ Sicherheits \_ Bindung**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) verwenden, um die Authentifizierungsdaten bereitzustellen.
    -   Wenn ein [Sicherheitskontext](security-context.md)verwendet wird, erstellt der Client zunächst einen Sicherheitskontext mit dem Server und verwendet diesen Kontext zum Authentifizieren von Nachrichten. Um diese Funktionalität zu aktivieren, muss die Sicherheits Beschreibung eine [**WS- \_ Sicherheits \_ Kontext- \_ Nachrichten \_ Sicherheits \_ Bindung**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding)enthalten. Nach der Einrichtung können Sicherheits Kontexte mithilfe von Lightweight-Token übertragen werden, wodurch vermieden wird, dass die potenziell großen und rechenintensiven Client Anmelde Informationen mit jeder Nachricht gesendet werden müssen.
    -   Bei einem [Verbund Sicherheits](federation.md) Szenario ruft der Client zuerst ein Sicherheits Token ab, das von einem Sicherheitstokendienst (STS) ausgegeben wird, und zeigt dann das ausgestellte Token für einen Dienst an. Client seitig: um das Sicherheits Token vom STS abzurufen, verwendet die Anwendung möglicherweise [**wsrequestsecuritytoken**](/windows/desktop/api/WebServices/nf-webservices-wsrequestsecuritytoken). Alternativ kann die Anwendung eine Client seitige sicherheitstokenanbieterbibliothek, z. b. CardSpace oder LiveID, verwenden und dann Ihre Ausgabe verwenden, um mithilfe von [**wscreatexmlsecuritytoken**](/windows/desktop/api/WebServices/nf-webservices-wscreatexmlsecuritytoken)lokal ein Sicherheits Token zu erstellen. Wenn das Sicherheits Token für den Client verfügbar ist, kann es in beiden Fällen dem Dienst mithilfe einer Sicherheits Beschreibung angezeigt werden, die eine [**WS- \_ XML- \_ \_ tokennachrichtensicherheitsbindung \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_token_message_security_binding)enthält. Serverseitig: Wenn das vom STS ausgegebene Sicherheits Token ein SAML-Token ist, kann der Server eine Sicherheits Beschreibung mit einer [**WS \_ SAML Message- \_ \_ Sicherheits \_ Bindung**](/windows/desktop/api/WebServices/ns-webservices-ws_saml_message_security_binding)verwenden.
        > [!Note]  
        > Windows 7 und Windows Server 2008 R2: wwsapi unterstützt nur [WS-Trust](http://specs.xmlsoap.org/ws/2005/02/trust/WS-Trust.pdf) und [WS-SecureConversation](http://specs.xmlsoap.org/ws/2005/02/sc/WS-SecureConversation.pdf) gemäß der Definition durch [Lightweight Webdienstesicherheit profile (lwssp)](/openspecs/windows_protocols/ms-lwssp/376af2f8-f4fe-4577-bfd5-370ac12cac2e). Ausführliche Informationen zur Implementierung von Microsoft finden Sie im Abschnitt zur [Nachrichten Syntax](/openspecs/windows_protocols/ms-lwssp/d4f0f509-e14a-47b5-81e8-ade06a51d1ed) von lwssp.

         
-   Die letzte zu berücksichtigende Option ist die Verwendung von Authentifizierungs Bindungen ohne Verwendung einer Schutz Bindung, wie z. b. [**WS \_ SSL- \_ Transport \_ Sicherheits \_ Bindung**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) Dies führt dazu, dass die Anmelde Informationen in Klartext übertragen werden und die Auswirkungen auf die Sicherheit haben können. Die Verwendung dieser Option sollte sorgfältig ausgewertet werden, um sicherzustellen, dass keine Schwachstellen vorhanden sind. Ein Beispiel für eine mögliche Verwendung ist der Austausch von Nachrichten zwischen Back-End-Servern über ein sicheres privates Netzwerk. Diese Option wird von den folgenden Konfigurationen unterstützt.

    -   [**WS \_ Die \_ \_ \_ Sicherheits \_ Bindung der HTTP-Header**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding) Authentifizierung unterstützt diese Option in allen Konfigurationen.
    -   [**WS \_ Die Benutzernamen- \_ Nachrichten \_ Sicherheits \_ Bindung**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding) unterstützt diese Option auf dem Server bei Verwendung von http als Transport.
    -   [**WS \_ Die Kerberos- \_ apreq- \_ Nachrichten \_ Sicherheits \_ Bindung**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) unterstützt diese Option auf dem Server bei Verwendung von http als Transport.
    -   [**WS \_ Sicherheits \_ Kontext \_ Nachrichten- \_ Sicherheits \_ Bindung**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) unterstützt diese Option auf dem Server bei Verwendung von http als Transport.
    -   [**WS \_ Die SAML- \_ Nachrichten \_ Sicherheits \_ Bindung**](/windows/desktop/api/WebServices/ns-webservices-ws_saml_message_security_binding) unterstützt diese Option auf dem Server bei Verwendung von http als Transport.

    Wenn Sie diese Option aktivieren, ist es erforderlich, die [**WS- \_ Schutz \_ Ebene**](/windows/desktop/api/WebServices/ne-webservices-ws_protection_level) explizit auf einen anderen Wert als **WS \_ \_ -Schutzgrad \_ \_ und- \_ Verschlüsselung** festzulegen

## <a name="channels-and-security"></a>Kanäle und Sicherheit

Wie bereits erwähnt, ist die Sicherheit auf Kanäle beschränkt. Darüber hinaus werden Kanal Vorgänge Sicherheits Schritten konsistent über alle Sicherheits Bindungen zugeordnet.

-   Channel Create: der in der Sicherheits Beschreibung angegebene Satz von Sicherheits Bindungen wird überprüft und bleibt anschließend für den Kanal korrigiert. Die Form des Kanal Stapels, einschließlich der für WS-Trust basierten Verhandlungen zu verwendenden seitenkanäle, wird ebenfalls festgelegt.
-   Channel geöffnet: alle Anmelde Informationen, die als Teil der Sicherheits Bindungen bereitgestellt werden, werden geladen, und es werden Sicherheits Sitzungen eingerichtet. Im Allgemeinen enthält ein offener Kanal den Sicherheitsstatus "Live". Durch das Öffnen eines Client Kanals wird auch die Endpunkt Adresse des Servers angegeben, mit der die Server Authentifizierung durch die Laufzeit erfolgt.
-   Zwischen dem Öffnen und Schließen von Kanälen: Nachrichten können in dieser Phase sicher gesendet und empfangen werden.
-   Message Send: Sicherheitskontext Token werden bei Bedarf abgerufen oder erneuert, und die Sicherheit wird auf jede übertragene Nachricht entsprechend der Sicherheits Beschreibung angewendet. Fehler, die beim Anwenden der Sicherheit auftreten, werden als Sende Fehler an die Anwendung zurückgegeben.
-   Nachrichten Empfang: die Sicherheit wird für jede empfangene Nachricht entsprechend der Sicherheits Beschreibung überprüft. Alle Fehler bei der Überprüfung der Nachrichten Sicherheit werden als Empfangs Fehler an die Anwendung zurückgegeben. Diese Nachrichten Nachrichten Fehler wirken sich nicht auf den Kanalstatus oder nachfolgende Empfangs Vorgänge aus. Die Anwendung kann einen fehlgeschlagenen Empfang verwerfen und einen Empfangsvorgang für eine andere Nachricht neu starten.
-   Kanal Abbruch: der Kanal kann jederzeit abgebrochen werden, damit alle e/a-Vorgänge auf dem Kanal angehalten werden. Beim Abbrechen wechselt der Kanal in einen fehlerhaften Zustand und lässt keine weiteren Sende-oder Empfangs Vorgänge zu. Der Kanal behält jedoch möglicherweise weiterhin den Sicherheitsstatus "Live" bei, sodass eine nachfolgende Kanal Schließung notwendig ist, um den gesamten Zustand sauber zu löschen.
-   Channel Close: der bei Open erstellte Sicherheitszustand wird verworfen, und die Sitzungen werden abgebrochen. Sicherheitskontext Token werden abgebrochen. Der Kanal Stapel bleibt bestehen, enthält jedoch keinen "Live"-Sicherheitszustand oder geladene Anmelde Informationen.
-   Channel Free: der in erstellte Kanal Stapel und alle Sicherheitsressourcen werden freigegeben.

## <a name="security-apis"></a>Sicherheits-APIs

Die API-Dokumentation für die Sicherheit wird in die folgenden Themen eingeteilt.

-   [Sicherheits Beschreibung](security-description.md)
    -   [Sicherheits Kanaleinstellungen](security-channel-settings.md)
    -   [Sicherheits Bindungen](security-bindings.md)
        -   [Sicherheitsanmeldeinformationen](security-credentials.md)
        -   [Sicherheitsbindungseinstellungen](security-binding-settings.md)
-   [Verbund](federation.md)
-   [Sicherheitskontext](security-context.md)
-   [Endpunktidentität](endpoint-identity.md)
-   [Ergebnisse der Sicherheits Verarbeitung](security-processing-results.md)

## <a name="security"></a>Sicherheit

Bei der Verwendung der wwsapi-Sicherheits-API haben Anwendungen verschiedene Sicherheitsrisiken:

<dl> <dt>

<span id="Accidental_misconfiguration"></span><span id="accidental_misconfiguration"></span><span id="ACCIDENTAL_MISCONFIGURATION"></span>Versehentliche Fehlkonfiguration
</dt> <dd>

Wwsapi unterstützt eine Reihe von sicherheitsbezogenen Konfigurationsoptionen. Siehe beispielsweise [**die \_ Eigenschaften \_ - \_ \_ ID der WS-Sicherheitsbindung**](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_property_id). Durch einige dieser Optionen, wie z. b. die **WS- \_ \_ sicherheitsbindungs \_ Eigenschaft \_ zulassen \_ Anonymer \_ Clients** , kann die Anwendung die Standard Sicherheitsstufe verringern, die von den verschiedenen Sicherheits Bindungen bereitgestellt wird. Die Verwendung solcher Optionen sollte sorgfältig ausgewertet werden, um sicherzustellen, dass keine resultierenden Angriffsvektoren vorhanden sind.

Außerdem ermöglicht wwsapi, wie oben beschrieben, die absichtliche Deaktivierung bestimmter Schritte, die erforderlich sind, um einen Nachrichtenaustausch vollständig zu schützen, z. b. das Deaktivieren der Verschlüsselung, auch wenn Anmelde Informationen übertragen werden. Dies ermöglicht die Aktivierung bestimmter spezifischer Szenarien und sollte nicht für die allgemeine Kommunikation verwendet werden. Die [**WS- \_ Schutz \_ Ebene**](/windows/desktop/api/WebServices/ne-webservices-ws_protection_level) muss speziell gesenkt werden, um diese Szenarios zu ermöglichen, und Anwendungen sollten diesen Wert nur ändern, wenn dies unbedingt erforderlich ist. Dadurch werden viele Überprüfungen deaktiviert, die zur Sicherstellung einer sicheren Konfiguration entworfen wurden.

</dd> <dt>

<span id="Storing_confidential_information_in_memory"></span><span id="storing_confidential_information_in_memory"></span><span id="STORING_CONFIDENTIAL_INFORMATION_IN_MEMORY"></span>Speichern vertraulicher Informationen im Arbeitsspeicher
</dt> <dd>

Vertrauliche Informationen, wie z. b. Kenn Wörter, die im Arbeitsspeicher gespeichert sind, sind anfällig für das Extrahieren durch einen privilegierten Angreifer, z. b. die Auslagerungs Datei. Wwsapi erstellt eine Kopie der angegebenen Anmelde Informationen und verschlüsselt diese Kopie, sodass die ursprünglichen Daten nicht geschützt sind. Die Anwendung ist dafür verantwortlich, die ursprüngliche Instanz zu schützen. Außerdem wird die verschlüsselte Kopie bei der Verwendung kurz entschlüsselt und ein Fenster geöffnet, in dem Sie extrahiert werden kann.

</dd> <dt>

<span id="Denial_of_service"></span><span id="denial_of_service"></span><span id="DENIAL_OF_SERVICE"></span>Denial-of-Service
</dt> <dd>

Die Sicherheits Verarbeitung kann beträchtliche Ressourcen beanspruchen. Jede zusätzliche Sicherheitsbindung erhöht diese Kosten. Wwsapi bricht die Sicherheits Verarbeitung ab, sobald ein Fehler bei der Sicherheitsüberprüfung aufgetreten ist, aber bestimmte Überprüfungen, wie z. b. Autorisierungs Entscheidungen, werden möglicherweise erst nach dem Ausführen wichtiger Arbeiten durchgeführt.

Während eine Nachricht auf dem Server verarbeitet wird, wird der Sicherheitsstatus auf dem Nachrichten Heap gespeichert. Die Anwendung kann den Arbeitsspeicher Verbrauch während der Sicherheits Verarbeitung begrenzen, indem die Größe dieses Heaps über die \_ \_ \_ \_ Eigenschaften Heap Eigenschaften von WS-Nachrichten Eigenschaften reduziert wird. Darüber hinaus können bestimmte Sicherheits Bindungen, wie z. b. die WS- \_ Sicherheits \_ Kontext \_ Nachrichten-Sicherheitsbindung, bewirken, dass \_ \_ der Server im Auftrag des Clients Ressourcen zuweist. Die Grenzwerte für diese Ressourcen können mithilfe der folgenden [**WS- \_ \_ sicherheitsbindungs- \_ Eigenschafts- \_ ID**](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_property_id) -Werte konfiguriert werden:

-   Sicherheitskontext der WS- \_ Sicherheits \_ Bindung \_ Max. \_ \_ \_ \_ ausstehende \_ Kontexte
-   Sicherheitskontext der WS- \_ Sicherheits \_ Bindung \_ Max. \_ \_ \_ \_ aktive \_ Kontexte
-   \_ \_ \_ \_ Sicherheits \_ Kontext- \_ Erneuerungs \_ Intervall für WS-Sicherheitsbindung
-   \_ \_ \_ \_ Sicherheits \_ Kontext- \_ Rollover- \_ Intervall der WS-Sicherheitsbindung

Das Festlegen dieser Grenzwerte auf niedrige Werte reduziert den maximalen Arbeitsspeicher Verbrauch, kann jedoch dazu führen, dass legitime Clients zurückgewiesen werden, wenn das Kontingent erreicht wird.

</dd> </dl>

 

 