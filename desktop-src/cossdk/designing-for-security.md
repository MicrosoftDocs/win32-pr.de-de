---
description: Entwerfen für Sicherheit
ms.assetid: 436f9d86-fbfa-4d5a-8580-fa1d4065c0aa
title: Entwerfen für Sicherheit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69bc59b06cfcb7432806e548cc9808199b194e6e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346645"
---
# <a name="designing-for-security"></a>Entwerfen für Sicherheit

Ihre End-to-End-Strategie für die Sicherheit hängt offensichtlich von der Art der verteilten Anwendung ab, die Sie entwickeln. Im folgenden finden Sie einige Vorschläge zur Adressierung der Sicherheit in Bezug auf die Anwendungslogik der mittleren Ebene:

-   Um Effizienz und Leistung zu erzielen, authentifizieren Sie sich so nah wie möglich bei dem Benutzer. Wenn Ihre Anwendung eine Browser-zu-Geschäftslogik-zu-Datenbankarchitektur umfasst, sollten Sie die Browser Clients den Domänen Identitäten zuordnet, die COM+-Anwendung unter Identitäten für jede Anwendung ausführen und Tabellen in der Datenebene so konfigurieren, dass Sie nur über eine bestimmte Anwendungs Identität zugänglich sind. Dieses vertrauenswürdige Server Szenario ist skalierbarer und weniger problematisch als die Verwendung des DBMS für die Authentifizierung.
-   Wenn Sie eine Komponente entwerfen, die in einer verteilten Anwendung mithilfe der rollenbasierten Sicherheit verwendet wird, können Sie die [com+-Sicherheits](com--security.md) Funktionen verwenden. Diese Funktion ermöglicht Ihnen das Aufrufen von Methoden wie [**IObjectContext:: isCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-iscallerinrole) und [**IObjectContext:: issecurityaktivi,**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-issecurityenabled) um Code Blöcke vor nicht autorisiertem Zugriff zu schützen. Sie können auch den Sicherheits Aufruf Kontext verwenden, um Informationen zu den Aufrufern eines Objekts abzurufen.
-   Wenn Sie eine Komponente entwerfen, die in einer verteilten Anwendung verwendet wird, ohne rollenbasierte Sicherheit zu verwenden, wird die Sicherheit automatisch nur auf Prozessebene geprüft. Prozess Zugriffsberechtigungen bestimmen, wer Zugriff auf die Anwendung erhält. Wenn Sie beim Prozess oder auf der Schnittstellen Ebene eine präzisere Steuerung der Sicherheitseinstellungen benötigen, verwenden Sie die von com bereitgestellte programmgesteuerte Sicherheitsfunktionalität.
-   Wenn eine Komponente, die die programmgesteuerte com+-Sicherheit verwendet, ohne Integration in eine COM+-Anwendung ausgeführt wird, werden Ausnahmen ausgelöst. Wenn eine solche Komponente erfolgreich in eine Anwendung integriert werden soll, die nicht Teil der com+-Umgebung ist, müssen Sie daher alle Ausnahmen entsprechend behandeln.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Entwerfen für Verfügbarkeit](designing-for-availability.md)
</dt> <dt>

[Entwerfen für die Bereitstellung](designing-for-deployment.md)
</dt> <dt>

[Entwerfen von Skalierbarkeit](designing-for-scalability.md)
</dt> <dt>

[Sicherheit für programmgesteuerte Komponenten](programmatic-component-security.md)
</dt> </dl>

 

 



