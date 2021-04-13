---
title: RADIUS-Authentifizierung,-Autorisierung und-Kontoführung
description: NPS unterstützt das RADIUS-Protokoll (Remote Authentication Dial-in User Service) vollständig. Das RADIUS-Protokoll ist der de-facto-Standard für die Remote Benutzerauthentifizierung und ist in RFC 2865 und RFC 2866 dokumentiert.
ms.assetid: 3e00d555-355c-4a4c-a389-ab44e9ed9ca9
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cce45bbc6e4802ed5137849a5b22520c8a4badbb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390693"
---
# <a name="radius-authentication-authorization-and-accounting"></a>RADIUS-Authentifizierung,-Autorisierung und-Kontoführung

> [!Note]  
> Der Internet Authentifizierungsdienst (IAS) wurde ab Windows Server 2008 in den Netzwerk Richtlinien Server (Network Policy Server, NPS) umbenannt. Der Inhalt dieses Themas gilt sowohl für IAS als auch für NPS. Im gesamten Text wird NPS verwendet, um auf alle Versionen des Dienstanbieter zu verweisen, einschließlich der Versionen, die ursprünglich als IAS bezeichnet wurden.

 

NPS unterstützt das RADIUS-Protokoll (Remote Authentication Dial-in User Service) vollständig. Das RADIUS-Protokoll ist der de-facto-Standard für die Remote Benutzerauthentifizierung und ist in [RFC 2865](https://www.ietf.org/rfc/rfc2865.txt) und [RFC 2866](https://www.ietf.org/rfc/rfc2866.txt)dokumentiert.

## <a name="radius-authentication-and-authorization"></a>RADIUS-Authentifizierung und-Autorisierung

Das folgende Diagramm zeigt einen authentifizier enden Client ("User"), der über eine DFÜ-Verbindung mithilfe des Point-to-Point-Protokoll (PPP) eine Verbindung mit einem Netzwerk Zugriffs Server (NAS) herstellt. Um den Benutzer zu authentifizieren, kontaktiert der NAS einen Remote Server, auf dem NPS ausgeführt wird. Der NAS-und der NPS-Server kommunizieren mit dem RADIUS-Protokoll.

![Remote Benutzerauthentifizierung](images/ias01.png)

Ein NAS fungiert als Client eines Servers oder von Servern, die das RADIUS-Protokoll unterstützen. Server, die das RADIUS-Protokoll unterstützen, werden im Allgemeinen als RADIUS-Server bezeichnet. Der RADIUS-Client, d. h. das NAS, übergibt Informationen über den Benutzer an bestimmte RADIUS-Server und verhält sich dann mit der Antwort, die die Server zurückgeben. Die Anforderung, die vom NAS an den RADIUS-Server gesendet wird, um den Benutzer zu authentifizieren, wird im Allgemeinen als "Authentifizierungsanforderung" bezeichnet.

Wenn der Benutzer von einem RADIUS-Server erfolgreich authentifiziert wird, gibt der RADIUS-Server Konfigurationsinformationen an den NAS zurück, damit er dem Benutzer Netzwerkdienst bereitstellen kann. Diese Konfigurationsinformationen bestehen aus "Autorisierungen" und enthalten unter anderem den Typ des dienstannas, den der Benutzer möglicherweise bereitstellt (z. b. PPP oder Telnet).

Während der RADIUS-Server die Authentifizierungsanforderung verarbeitet, kann er Autorisierungs Funktionen ausführen, wie z. b. das Überprüfen der Telefonnummer des Benutzers und das überprüfen, ob der Benutzer bereits über eine Sitzung verfügt. Der RADIUS-Server kann ermitteln, ob der Benutzer bereits über eine Sitzung verfügt, indem er eine Verbindung mit einem Zustands Server aufnimmt.

Weitere Informationen zur RADIUS-Authentifizierung und-Autorisierung finden Sie unter [RFC 2865](https://www.ietf.org/rfc/rfc2865.txt).

## <a name="radius-accounting"></a>RADIUS-Kontoführung

Der RADIUS-Server sammelt außerdem eine Vielzahl von Informationen, die vom NAS gesendet werden, die für die Buchhaltung und die Berichterstellung zur Netzwerkaktivität verwendet werden können. Der RADIUS-Client sendet Informationen an bestimmte RADIUS-Server, wenn sich der Benutzer anmeldet und abmeldet. Der RADIUS-Client sendet möglicherweise regelmäßig zusätzliche Verwendungs Informationen, während die Sitzung ausgeführt wird. Die Anforderungen, die vom Client an den Server gesendet werden, um Anmelde-/Abmelde-und Verwendungs Informationen aufzuzeichnen, werden im Allgemeinen als "Buchhaltungs Anforderungen" bezeichnet.

Weitere Informationen zur RADIUS-Buchhaltung finden Sie unter [RFC 2866](https://www.ietf.org/rfc/rfc2866.txt).

## <a name="radius-proxy"></a>RADIUS-Proxy

Ein RADIUS-Server kann als Proxy Client für andere RADIUS-Server fungieren. In diesen Fällen übergibt der vom NAS angewandte RADIUS-Server die Authentifizierungs-oder Buchhaltungs Anforderung an einen anderen RADIUS-Server, der die Authentifizierung oder die Buchhaltungs Aufgabe ausführt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Internet Authentifizierungsdienst und Netzwerk Richtlinien Server](internet-authentication-service-vs-network-policy-server.md)
</dt> <dt>

[RADIUS-Buchhaltungs Pakete](/windows/desktop/Nps/ias-radius-accounting-packets)
</dt> <dt>

[Arbeiten mit einem Zustands Server](/windows/desktop/Nps/ias-working-with-a-state-server)
</dt> </dl>

 

 