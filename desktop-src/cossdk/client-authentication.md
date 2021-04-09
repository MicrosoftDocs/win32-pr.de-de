---
description: Die Authentifizierung ist der Prozess, bei dem die Aufrufer tatsächlich&8212 werden, um \# die Authentizität eines Identitäts Anspruchs zu überprüfen.
ms.assetid: c1b11f58-5bab-45d9-a686-86c95415990e
title: Clientauthentifizierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd24edf341fc2033807587b01fd37420d781d5f8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958466"
---
# <a name="client-authentication"></a>Clientauthentifizierung

Bei der Authentifizierung wird festgestellt, dass Aufrufer tatsächlich die Benutzer sind, die Sie sagen – Überprüfen der Echtheit eines Identitäts Anspruchs. Im Allgemeinen kann dies sowohl von Server als auch vom Client durchgeführt werden, von denen jede die andere authentifiziert. Es ist jedoch besonders wichtig für eine Serveranwendung, die Clients autorisiert, wie bei Rollen basierter Sicherheit, auch für die Authentifizierung. Das Authentifizieren von Clients ist eine Voraussetzung für eine sinnvolle Autorisierungs Richtlinie. Sie können die gesamte gewünschte Rollen Überprüfung ausführen. Wenn Sie jedoch nicht sicher sind, dass die überprüfende Client Identität authentisch ist, verlässt sich Ihre Anwendung im Grunde auf das-Anspruchs System.

Für COM+-Anwendungen ist die Authentifizierung etwas, das Sie in administrativer Weise aktivieren und konfigurieren können. danach funktioniert es transparent mit der Anwendung. Sie geben eine Authentifizierungs Ebene administrativ mithilfe des Verwaltungs Programms Komponenten Dienste oder der administrativen Funktionen an. Ausführliche Informationen zum Festlegen der Authentifizierung finden Sie unter [Festlegen einer Authentifizierungs Ebene für eine Server Anwendung](setting-an-authentication-level-for-a-server-application.md) und [Aktivieren der Authentifizierung für eine Bibliotheks Anwendung](enabling-authentication-for-a-library-application.md).

Das Festlegen der Authentifizierung bedeutet verschiedene Dinge, abhängig davon, ob es sich beim Anwendungstyp um eine Server-oder Bibliotheks Anwendung handelt.

## <a name="setting-authentication-for-com-server-applications"></a>Festlegen der Authentifizierung für com+-Server Anwendungen

Für eine COM+-Serveranwendung legen Sie eine Authentifizierungs Stufe fest, mit der bestimmt wird, wie die Authentifizierung erfolgt, wenn Clients Komponenten innerhalb der Anwendung aufzurufen. Sie können zwischen verschiedenen Authentifizierungs Ebenen wählen, die unterschiedliche Sicherheitsstufen bieten, von denen keine Authentifizierung für die Verschlüsselung der einzelnen Pakete und alle Methoden aufrufungsparameter besteht. Weitere Informationen finden Sie unter [Festlegen einer Authentifizierungs Ebene für eine Server Anwendung](setting-an-authentication-level-for-a-server-application.md).

Höhere Sicherheit beinhaltet jedoch einige Leistungseinbußen, die Sie beim Konfigurieren Ihrer Anwendung berücksichtigen sollten. Com+ aushandelt zwischen der von Client und Server angegebenen Authentifizierungs Ebene. Die Art und Weise, wie diese Aushandlung durchgeführt wird, bietet den Vorteil, dass Sie die Authentifizierung nur von der Serverseite aus verwalten können. Weitere Informationen finden Sie unter [Aushandlung der Authentifizierungs Ebene](negotiation-of-authentication-level.md).

> [!Note]  
> Sie sollten eine Authentifizierungs Ebene niemals Programm gesteuert angeben, indem Sie [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) innerhalb einer COM+-Anwendung verwenden. Com+ Ruft **CoInitializeSecurity** für Sie auf, und dies kann nur einmal pro Prozess aufgerufen werden.

 

Die zugrunde liegenden Authentifizierungsdienste werden von com und Microsoft Windows bereitgestellt. Bei einem Authentifizierungsdienst wird von einem Drittanbieter ein Zertifikat für einen Benutzer bereitstellt, bei dem die Echtheit der Identität des Benutzers bestätigt wird. Diese Zertifizierung ist so glaubwürdig wie die Zertifizierungsstelle, und – auf die gleiche Weise wie die Lizenz eines Treibers, oder ein Passport fungiert als Zertifizierungsdokument – Sie hängt von der Autorität des Ausstellers ab. Ausführlichere Informationen zu Authentifizierungsdiensten finden Sie unter [com-und Sicherheitspakete](/windows/desktop/com/com-and-security-packages) in der com-Dokumentation.

## <a name="setting-authentication-for-com-library-applications"></a>Festlegen der Authentifizierung für COM+-Bibliotheksanwendungen

Für eine COM+-Bibliotheks Anwendung aktivieren oder deaktivieren Sie die Authentifizierung, um zu bestimmen, ob die Anwendung der Authentifizierung unterliegt, die vom Hostingprozess ausgeführt wird. Obwohl die Authentifizierung für eine COM+-Bibliotheks Anwendung größtenteils durch den Hostingprozess gesteuert wird, können Sie die Bibliotheks Anwendung so konfigurieren, dass Sie nicht an der Authentifizierung teilnimmt. Das heißt, dass Aufrufe der Anwendung authentifiziert oder nicht authentifiziert werden können, und in letzterem Fall ist die Authentifizierung von Clients immer erfolgreich. Weitere Informationen finden Sie unter [Aktivieren der Authentifizierung für eine Bibliotheks Anwendung](enabling-authentication-for-a-library-application.md).

Außerdem ist es möglich, dass Sie den Client bei der Datenbank oder bei einer downstreamanwendung authentifizieren müssen – bei der Authentifizierung von Clients bei der com+-Anwendung ist es möglicherweise nicht ausreichend. Wenn dies der Fall ist, müssen Sie die Identität des Clients annehmen, damit die Identität des Clients nach unten weitergegeben wird. Ausführliche Informationen zum Identitätswechsel finden Sie unter [Client Identitätswechsel und Delegierung](client-impersonation-and-delegation.md). Eine Erörterung der Probleme bei der Entscheidung, ob die Authentifizierung auf der Datenebene durchgeführt werden soll, finden Sie unter [Multi-Tier Application Security](multi-tier-application-security.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Client Identitätswechsel und Delegierung](client-impersonation-and-delegation.md)
</dt> <dt>

[Sicherheit der Bibliothek Anwendungen](library-application-security.md)
</dt> <dt>

[Multi-Tier-Anwendungssicherheit](multi-tier-application-security.md)
</dt> <dt>

[Sicherheit für programmgesteuerte Komponenten](programmatic-component-security.md)
</dt> <dt>

[Rollenbasierte Sicherheitsverwaltung](role-based-security-administration.md)
</dt> <dt>

[Verwenden der Richtlinie für Software Einschränkung in com+](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 
