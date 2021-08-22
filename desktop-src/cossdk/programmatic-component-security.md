---
description: Wenn Sie die rollenbasierte Sicherheit in der COM+-Anwendung verwenden, die Ihre Komponente enthält, haben Sie Zugriff auf programmgesteuerte Sicherheitsfunktionen innerhalb Ihrer Komponente.
ms.assetid: 6117970c-5dbd-485e-978e-3aa96e42b359
title: Programmgesteuerte Komponentensicherheit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b3fc8813b6aff98f19e7c051067f3246c25b336ea7a99a2371f03c7f3f50883
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119462110"
---
# <a name="programmatic-component-security"></a>Programmgesteuerte Komponentensicherheit

Wenn Sie die rollenbasierte Sicherheit in der COM+-Anwendung verwenden, die Ihre Komponente enthält, haben Sie Zugriff auf programmgesteuerte Sicherheitsfunktionen innerhalb Ihrer Komponente. Sie können die Rollenmitgliedschaft überprüfen, um zu bestimmen, ob bestimmte Codeabschnitte ausgeführt werden. Sie können mithilfe des Kontextobjekts für Sicherheitsaufrufe auf Sicherheitsinformationen zugreifen und bestimmen, ob die Sicherheit für den aktuellen Aufruf aktiviert ist. Sie können alle diese Aufgaben ausführen, indem Sie einen Verweis auf ein [**SecurityCallContext-Objekt**](securitycallcontext.md) (für Microsoft Visual Basic-Anwendungen) oder einen Zeiger auf die [**ISecurityCallContext-Schnittstelle**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) (für C- und Microsoft Visual C++-Anwendungen) verwenden.

Weitere Informationen zur programmgesteuerten rollenbasierten Sicherheit finden Sie in den folgenden Themen in diesem Abschnitt:

-   [Überprüfen der Rollenmitgliedschaft](checking-role-membership.md)
-   [Bestimmen, ob Role-Based Sicherheit aktiviert ist](determining-whether-role-based-security-is-enabled.md)
-   [Zugreifen auf Kontextinformationen für Sicherheitsaufrufe](accessing-security-call-context-information.md)

## <a name="impersonation-and-com-security-features"></a>Identitätswechsel und COM-Sicherheitsfeatures

Wenn Ihre Komponente in einer COM+-Anwendung verwendet wird, die keine rollenbasierte Sicherheit verwendet, sind die programmgesteuerte Rollenüberprüfung und Die Kontextinformationen für Sicherheitsaufrufe nicht verfügbar. Sie können jedoch die programmgesteuerte Sicherheitsfunktionalität von COM verwenden. Weitere Informationen finden Sie unter [Sicherheit in COM.](/windows/desktop/com/security-in-com)

Sie können zwar einen Großteil der von COM bereitgestellten Sicherheitsfunktionen verwenden, aber Sie können [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) nicht von einer Komponente aufrufen, die Teil einer COM+-Anwendung ist, da **CoInitializeSecurity** vom Ersatzzeichen aufgerufen wird, in dem die COM+-Anwendung ausgeführt wird. Sie können jedoch andere Sicherheitsfunktionen aufrufen, z. B. [**CoQueryClientBlanket,**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryclientblanket)die Informationen zum Client abrufen.

Insbesondere wenn Sie die Identität des Clients verwenden müssen, um auf eine Ressource zuzugreifen , z. B. auf eine Datei, die durch eine Sicherheitsbeschreibung geschützt ist, oder die Identität des Clients an eine Datenbank weiterzuverbreiten, können Sie den Identitätswechsel programmgesteuert ausführen. Weitere Informationen dazu, wann und wie dies geschieht, finden Sie unter [Clientidentitätswechsel und Delegierung.](client-impersonation-and-delegation.md)

## <a name="testing-security-functionality"></a>Testen der Sicherheitsfunktionalität

Wenn Sie die programmgesteuerte COM+-Sicherheit in Ihrer Komponente verwenden, müssen Sie die Komponente in eine COM+-Anwendung integrieren, wenn Sie bereit sind, die Sicherheitsfunktionalität der Komponente zu testen. Wenn eine Komponente mit com+-programmgesteuerter Sicherheit ausgeführt wird, ohne in eine COM+-Anwendung integriert zu werden, werden Ausnahmen ausgelöst. Wenn Sie also sicherstellen möchten, dass eine solche Komponente auch erfolgreich in eine Anwendung integriert werden kann, die nicht Teil der COM+-Umgebung ist, müssen Sie sicherstellen, dass diese Ausnahmen ordnungsgemäß behandelt werden.

## <a name="documenting-security-requirements"></a>Dokumentieren von Sicherheitsanforderungen

Wenn Sie eine eigenständige Komponente für COM+-Anwendungen schreiben, die rollenbasierte Sicherheit verwenden, müssen Sie die Komponente dokumentieren, damit die Sicherheit entsprechend konfiguriert werden kann, wenn die Komponente in eine COM+-Anwendung integriert ist. Beispielsweise sollten Sie die Rollen identifizieren, die hinzugefügt werden müssen, und erläutern, welche Methoden und Schnittstellen den einzelnen Rollen zugewiesen werden sollen. Darüber hinaus sollten Sie, wenn eine Methode wie IsCallerInRole("Sollen") aufgerufen wird, die Funktionalität beschreiben, auf die nur Vonser Zugriff haben. Sie sollten auch angeben, ob eine Rolle erforderlich ist, um den Zugriff auf die gesamte Komponente zu schützen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Clientauthentifizierung](client-authentication.md)
</dt> <dt>

[Clientidentitätswechsel und -delegierung](client-impersonation-and-delegation.md)
</dt> <dt>

[Bibliotheksanwendungssicherheit](library-application-security.md)
</dt> <dt>

[Anwendungssicherheit mit mehreren Ebenen](multi-tier-application-security.md)
</dt> <dt>

[Rollenbasierte Sicherheitsverwaltung](role-based-security-administration.md)
</dt> <dt>

[Verwenden der Softwareeinschränkungsrichtlinie in COM+](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 
