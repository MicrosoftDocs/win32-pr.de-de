---
description: Authentifizierung ist der Prozess, bei dem ermittelt wird, ob Aufrufer tatsächlich die Person sind, die sie als&\# 8212 bezeichnen. Dabei wird die Authentizität eines Identitätsanspruchs überprüft.
ms.assetid: c1b11f58-5bab-45d9-a686-86c95415990e
title: Clientauthentifizierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 472f16e32cb99f9f2c89c21012f1faa7f96af17878c34d16400f7d505c324398
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119638990"
---
# <a name="client-authentication"></a>Clientauthentifizierung

Authentifizierung ist der Prozess, bei dem ermittelt wird, ob Aufrufer tatsächlich die Person sind, die sie sagen, und die Authentizität eines Identitätsanspruchs zu überprüfen. Im Allgemeinen kann dies sowohl vom Server als auch vom Client erfolgen, wobei jeder den anderen authentifiziert. Es ist jedoch besonders wichtig für eine Serveranwendung, die Clients autorisiert, wie bei der rollenbasierten Sicherheit auch die Authentifizierung durchzuführen. Die Authentifizierung von Clients ist eine Voraussetzung für eine sinnvolle Autorisierungsrichtlinie. Sie können alle gewünschten Rollenüberprüfungen durchführen. Wenn Sie jedoch nicht sicher sind, ob die von Ihnen überprüfte Clientidentität authentifiziert ist, verlässt sich Ihre Anwendung im Grunde auf das Honor-System.

Bei COM+-Anwendungen können Sie die Authentifizierung aktivieren und administrativ konfigurieren. Danach funktioniert sie für die Anwendung transparent. Sie können eine Authentifizierungsebene mithilfe des Verwaltungstools Komponentendienste oder der Verwaltungsfunktionen administrativ angeben. Ausführliche Informationen zum Festlegen der Authentifizierung finden Sie unter [Festlegen einer Authentifizierungsebene für eine Serveranwendung](setting-an-authentication-level-for-a-server-application.md) und [Aktivieren der Authentifizierung für eine Bibliotheksanwendung.](enabling-authentication-for-a-library-application.md)

Das Festlegen der Authentifizierung bedeutet unterschiedliche Dinge, je nachdem, ob es sich bei dem Anwendungstyp um eine Server- oder Bibliotheksanwendung handelt.

## <a name="setting-authentication-for-com-server-applications"></a>Festlegen der Authentifizierung für COM+-Serveranwendungen

Für eine COM+-Serveranwendung legen Sie eine Authentifizierungsebene fest, die bestimmt, wie die Authentifizierung ausgeführt wird, wenn Clients Komponenten innerhalb der Anwendung aufrufen. Sie können aus mehreren Authentifizierungsebenen wählen, die unterschiedliche Sicherheitsstufen bieten, von keiner Authentifizierung bis hin zur Verschlüsselung jedes Pakets und aller Methodenaufrufparameter. Weitere Informationen finden Sie unter [Festlegen einer Authentifizierungsebene für eine Serveranwendung.](setting-an-authentication-level-for-a-server-application.md)

Höhere Sicherheit bringt jedoch einige Leistungskosten mit sich, die Sie beim Konfigurieren Ihrer Anwendung berücksichtigen sollten. COM+ handelt zwischen der von Client und Server angegebenen Authentifizierungsebene aus. Die Art und Weise, wie diese Aushandlung durchgeführt wird, hat den Vorteil, dass Sie die Authentifizierung von der Serverseite aus allein administrativ steuern können. Weitere Informationen finden Sie unter [Aushandlung der Authentifizierungsebene](negotiation-of-authentication-level.md).

> [!Note]  
> Sie sollten niemals programmgesteuert eine Authentifizierungsebene angeben, indem Sie [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) in einer COM+-Anwendung verwenden. COM+ ruft **CoInitializeSecurity** für Sie auf, und dies kann nur einmal pro Prozess aufgerufen werden.

 

Die zugrunde liegenden Authentifizierungsdienste werden von COM und Microsoft Windows bereitgestellt. In einem Authentifizierungsdienst stellt ein Drittanbieter ein Zertifikat für einen Benutzer bereit, das die Authentizität der Identität des Benutzers bestätigt. Diese Zertifizierung ist so vertrauenswürdig wie die Zertifizierungsstelle und hängt – ähnlich wie eine Fahrerlizenz oder ein Passport als Zertifizierendes Dokument – von der Autorität des Ausstellers ab. Ausführlichere Informationen zu Authentifizierungsdiensten finden Sie unter [COM und Sicherheitspakete](/windows/desktop/com/com-and-security-packages) in der COM-Dokumentation.

## <a name="setting-authentication-for-com-library-applications"></a>Festlegen der Authentifizierung für COM+-Bibliotheksanwendungen

Bei einer COM+-Bibliotheksanwendung aktivieren oder deaktivieren Sie die Authentifizierung, um zu bestimmen, ob die Anwendung der vom Hostingprozess durchgeführten Authentifizierung unterliegt. Obwohl die Authentifizierung für eine COM+-Bibliotheksanwendung größtenteils durch den Hostingprozess gesteuert wird, können Sie die Bibliotheksanwendung so konfigurieren, dass sie nicht an der Authentifizierung teilnimmt. Das heißt, Aufrufe der Anwendung können authentifiziert oder nicht authentifiziert werden, und im letzteren Fall ist die "Authentifizierung" von Clients immer erfolgreich. Weitere Informationen finden Sie unter [Aktivieren der Authentifizierung für eine Bibliotheksanwendung.](enabling-authentication-for-a-library-application.md)

Darüber hinaus kann es sinnvoll sein, den Client in der Datenbank oder in einer Downstreamanwendung zu authentifizieren. Die Authentifizierung von Clients bei der COM+-Anwendung allein reicht möglicherweise nicht aus. In diesem Fall müssen Sie die Identität des Clients annehmen, damit die Identität des Clients nachgeschaltet wird. Ausführliche Informationen zum Identitätswechsel finden Sie unter [Clientidentitätswechsel und Delegierung.](client-impersonation-and-delegation.md) Eine Erläuterung der Probleme bei der Entscheidung, ob die Authentifizierung auf der Datenebene erfolgt, finden Sie unter [Anwendungssicherheit mit mehreren Ebenen.](multi-tier-application-security.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Clientidentitätswechsel und -delegierung](client-impersonation-and-delegation.md)
</dt> <dt>

[Bibliotheksanwendungssicherheit](library-application-security.md)
</dt> <dt>

[Anwendungssicherheit mit mehreren Ebenen](multi-tier-application-security.md)
</dt> <dt>

[Programmgesteuerte Komponentensicherheit](programmatic-component-security.md)
</dt> <dt>

[Rollenbasierte Sicherheitsverwaltung](role-based-security-administration.md)
</dt> <dt>

[Verwenden der Softwareeinschränkungsrichtlinie in COM+](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 
