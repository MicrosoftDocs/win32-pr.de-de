---
title: RADIUS-Authentifizierung, -Autorisierung und -Buchhaltung
description: NPS unterstützt das RADIUS-Protokoll (Remote Authentication Dial-In User Service) vollständig. Das RADIUS-Protokoll ist der De-facto-Standard für die Remotebenutzerauthentifizierung und ist in RFC 2865 und RFC 2866 dokumentiert.
ms.assetid: 3e00d555-355c-4a4c-a389-ab44e9ed9ca9
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3b0395b6bc147da4f78bb718cda714014b9b665f5a26a8d20fa29402ee8dec1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119063493"
---
# <a name="radius-authentication-authorization-and-accounting"></a>RADIUS-Authentifizierung, -Autorisierung und -Buchhaltung

> [!Note]  
> Der Internetauthentifizierungsdienst (INTERNET Authentication Service, IAS) wurde ab Windows Server 2008 in Netzwerkrichtlinienserver (Network Policy Server, NPS) umbenannt. Der Inhalt dieses Themas gilt sowohl für IAS als auch für NPS. Im gesamten Text wird NPS verwendet, um auf alle Versionen des Diensts zu verweisen, einschließlich der Versionen, die ursprünglich als IAS bezeichnet wurden.

 

NPS unterstützt das RADIUS-Protokoll (Remote Authentication Dial-In User Service) vollständig. Das RADIUS-Protokoll ist der De-facto-Standard für die Remotebenutzerauthentifizierung und ist in [RFC 2865](https://www.ietf.org/rfc/rfc2865.txt) und [RFC 2866](https://www.ietf.org/rfc/rfc2866.txt)dokumentiert.

## <a name="radius-authentication-and-authorization"></a>RADIUS-Authentifizierung und -Autorisierung

Das folgende Diagramm zeigt einen authentifizierenden Client ("Benutzer"), der über eine DFÜ-Verbindung eine Verbindung mit einem Netzwerkzugriffsserver (NAS) über die Point-to-Point-Protokoll herstellt. Um den Benutzer zu authentifizieren, kontaktiert das NAS einen Remoteserver, auf dem NPS ausgeführt wird. Nas und NPS-Server kommunizieren über das RADIUS-Protokoll.

![Remotebenutzerauthentifizierung](images/ias01.png)

Ein NAS fungiert als Client eines Servers oder eines Servers, der das RADIUS-Protokoll unterstützt. Server, die das RADIUS-Protokoll unterstützen, werden im Allgemeinen als RADIUS-Server bezeichnet. Der RADIUS-Client, d. h. der NAS, übergibt Informationen über den Benutzer an die angegebenen RADIUS-Server und reagiert dann auf die Antwort, die die Server zurückgeben. Die Anforderung, die vom NAS an den RADIUS-Server gesendet wird, um den Benutzer zu authentifizieren, wird im Allgemeinen als "Authentifizierungsanforderung" bezeichnet.

Wenn ein RADIUS-Server den Benutzer erfolgreich authentifiziert, gibt der RADIUS-Server Konfigurationsinformationen an das NAS zurück, damit er dem Benutzer Einen Netzwerkdienst bereitstellen kann. Diese Konfigurationsinformationen bestehen aus "Autorisierungen" und enthalten unter anderem den Typ des Diensts NAS, der dem Benutzer zur Verfügung steht (z. B. PPUs oder Telnet).

Während der RADIUS-Server die Authentifizierungsanforderung verarbeitet, kann er Autorisierungsfunktionen wie das Überprüfen der Telefonnummer des Benutzers und das Überprüfen, ob der Benutzer bereits über eine Sitzung verfügt, ausführen. Der RADIUS-Server kann ermitteln, ob der Benutzer bereits eine Sitzung ausgeführt hat, indem er sich an einen Zustandsserver wendet.

Weitere Informationen zur RADIUS-Authentifizierung und -Autorisierung finden Sie unter [RFC 2865](https://www.ietf.org/rfc/rfc2865.txt).

## <a name="radius-accounting"></a>RADIUS-Kontoführung

Der RADIUS-Server sammelt auch eine Vielzahl von Informationen, die vom NAS gesendet werden und für die Kontoführung und Berichterstellung zur Netzwerkaktivität verwendet werden können. Der RADIUS-Client sendet Informationen an festgelegte RADIUS-Server, wenn sich der Benutzer anmeldet und sich abmeldet. Der RADIUS-Client sendet möglicherweise regelmäßig zusätzliche Nutzungsinformationen, während die Sitzung ausgeführt wird. Die Anforderungen, die vom Client an den Server gesendet werden, um Anmeldung/Abmeldung und Nutzungsinformationen aufzuzeichnen, werden im Allgemeinen als "Buchhaltungsanforderungen" bezeichnet.

Weitere Informationen zur RADIUS-Kontoführung finden Sie unter [RFC 2866](https://www.ietf.org/rfc/rfc2866.txt).

## <a name="radius-proxy"></a>RADIUS-Proxy

Ein RADIUS-Server kann als Proxyclient für andere RADIUS-Server fungieren. In diesen Fällen übergibt der VOM NAS kontaktierte RADIUS-Server die Authentifizierungs- oder Buchhaltungsanforderung an einen anderen RADIUS-Server, der die Authentifizierung oder die Buchhaltungsaufgabe tatsächlich ausführt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Internetauthentifizierungsdienst und Netzwerkrichtlinienserver](internet-authentication-service-vs-network-policy-server.md)
</dt> <dt>

[RADIUS-Buchhaltungspakete](/windows/desktop/Nps/ias-radius-accounting-packets)
</dt> <dt>

[Arbeiten mit einem Zustandsserver](/windows/desktop/Nps/ias-working-with-a-state-server)
</dt> </dl>

 

 