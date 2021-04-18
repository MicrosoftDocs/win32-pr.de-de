---
description: Wenn Sie die rollenbasierte Sicherheit in der com+-Anwendung verwenden, die die Komponente enthält, haben Sie Zugriff auf programmgesteuerte Sicherheitsfunktionen innerhalb der Komponente.
ms.assetid: 6117970c-5dbd-485e-978e-3aa96e42b359
title: Sicherheit für programmgesteuerte Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31622608e4d4f54aeb53b403b5d8711ff9c6a9af
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345444"
---
# <a name="programmatic-component-security"></a>Sicherheit für programmgesteuerte Komponenten

Wenn Sie die rollenbasierte Sicherheit in der com+-Anwendung verwenden, die die Komponente enthält, haben Sie Zugriff auf programmgesteuerte Sicherheitsfunktionen innerhalb der Komponente. Sie können die Rollen Mitgliedschaft überprüfen, um zu bestimmen, ob bestimmte Code Abschnitte ausgeführt werden. Sie können mithilfe des Kontext Objekts für den Sicherheits Rückruf auf Sicherheitsinformationen zugreifen, und Sie können ermitteln, ob die Sicherheit für den aktuellen-Befehl aktiviert ist. Sie können all diese Aufgaben durchführen, indem Sie einen Verweis auf ein [**SecurityCallContext**](securitycallcontext.md) -Objekt (für Microsoft Visual Basic-Anwendungen) oder einen Zeiger auf die [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) -Schnittstelle (für C-und Microsoft Visual C++-Anwendungen) verwenden.

Weitere Informationen zur programmgesteuerten rollenbasierten Sicherheit finden Sie in den folgenden Themen in diesem Abschnitt:

-   [Überprüfen der Rollen Mitgliedschaft](checking-role-membership.md)
-   [Bestimmen, ob Role-Based Sicherheit aktiviert ist](determining-whether-role-based-security-is-enabled.md)
-   [Aufrufen von Kontextinformationen für den Sicherheitskontext](accessing-security-call-context-information.md)

## <a name="impersonation-and-com-security-features"></a>Identitätswechsel und com-Sicherheits Features

Wenn die Komponente in einer COM+-Anwendung verwendet wird, für die keine rollenbasierte Sicherheit verwendet wird, sind keine programmatischen Rollen Überprüfung und keine Kontextinformationen zum Sicherheitsgespräch verfügbar. Sie können jedoch die von com bereitgestellte programmgesteuerte Sicherheitsfunktion verwenden. Weitere Informationen finden Sie unter [Sicherheit in com](/windows/desktop/com/security-in-com).

Obwohl Sie die meisten von com bereitgestellten Sicherheitsfunktionen verwenden können, können Sie [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) nicht aus einer Komponente aufrufen, die Teil einer COM+-Anwendung ist, da **CoInitializeSecurity** von dem Ersatz Zeichen aufgerufen wird, in dem die COM+-Anwendung ausgeführt wird. Sie können jedoch auch andere Sicherheitsfunktionen, wie z. b. [**coqueryclientblanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryclientblanket), abrufen, die Informationen über den Client abrufen.

Insbesondere, wenn Sie die Identität des Clients für den Zugriff auf eine Ressource verwenden müssen – z. b. durch den Zugriff auf eine Datei, die durch eine Sicherheits Beschreibung geschützt ist, oder über die Weitergabe der Identität des Clients an eine Datenbank – können Sie den Identitätswechsel Programm gesteuert ausführen. Weitere Details dazu, wann und wie Sie vorgehen, finden Sie unter Client Identitätswechsel [und Delegierung](client-impersonation-and-delegation.md).

## <a name="testing-security-functionality"></a>Testen von Sicherheitsfunktionen

Wenn Sie in Ihrer Komponente die programmgesteuerte com+-Sicherheit verwenden, müssen Sie die Komponente in eine COM+-Anwendung integrieren, wenn Sie bereit sind, die Sicherheitsfunktionen der Komponente zu testen. Wenn eine Komponente, die die programmgesteuerte com+-Sicherheit verwendet, ohne Integration in eine COM+-Anwendung ausgeführt wird, werden Ausnahmen ausgelöst. Wenn Sie also sicherstellen möchten, dass eine solche Komponente auch erfolgreich in eine Anwendung integriert werden kann, die nicht Teil der com+-Umgebung ist, müssen Sie sicherstellen, dass diese Ausnahmen ordnungsgemäß behandelt werden.

## <a name="documenting-security-requirements"></a>Dokumentieren von Sicherheitsanforderungen

Wenn Sie eine eigenständige Komponente für COM+-Anwendungen schreiben, die rollenbasierte Sicherheit verwenden, müssen Sie die Komponente dokumentieren, damit die Sicherheit entsprechend konfiguriert werden kann, wenn die Komponente in eine COM+-Anwendung integriert ist. Sie sollten z. b. die Rollen ermitteln, die hinzugefügt werden müssen, und erläutern, welchen Methoden und Schnittstellen die einzelnen Rollen zugewiesen werden sollen. Außerdem sollten Sie, wenn eine Methode wie isCallerInRole ("Teller") aufgerufen wird, die Funktionalität beschreiben, auf die nur der Kassierer zugreifen kann. Außerdem sollten Sie angeben, ob eine Rolle erforderlich ist, um den Zugriff auf die gesamte Komponente zu schützen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Clientauthentifizierung](client-authentication.md)
</dt> <dt>

[Client Identitätswechsel und Delegierung](client-impersonation-and-delegation.md)
</dt> <dt>

[Sicherheit der Bibliothek Anwendungen](library-application-security.md)
</dt> <dt>

[Multi-Tier-Anwendungssicherheit](multi-tier-application-security.md)
</dt> <dt>

[Rollenbasierte Sicherheitsverwaltung](role-based-security-administration.md)
</dt> <dt>

[Verwenden der Richtlinie für Software Einschränkung in com+](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 
