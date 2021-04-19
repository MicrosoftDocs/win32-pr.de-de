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
# <a name="designing-for-security"></a><span data-ttu-id="73a01-103">Entwerfen für Sicherheit</span><span class="sxs-lookup"><span data-stu-id="73a01-103">Designing for Security</span></span>

<span data-ttu-id="73a01-104">Ihre End-to-End-Strategie für die Sicherheit hängt offensichtlich von der Art der verteilten Anwendung ab, die Sie entwickeln.</span><span class="sxs-lookup"><span data-stu-id="73a01-104">Your end-to-end strategy for security obviously depends on the type of distributed application you are developing.</span></span> <span data-ttu-id="73a01-105">Im folgenden finden Sie einige Vorschläge zur Adressierung der Sicherheit in Bezug auf die Anwendungslogik der mittleren Ebene:</span><span class="sxs-lookup"><span data-stu-id="73a01-105">Following are several suggestions for addressing security with respect to middle-tier application logic:</span></span>

-   <span data-ttu-id="73a01-106">Um Effizienz und Leistung zu erzielen, authentifizieren Sie sich so nah wie möglich bei dem Benutzer.</span><span class="sxs-lookup"><span data-stu-id="73a01-106">For efficiency and performance, authenticate as close to the user as you can.</span></span> <span data-ttu-id="73a01-107">Wenn Ihre Anwendung eine Browser-zu-Geschäftslogik-zu-Datenbankarchitektur umfasst, sollten Sie die Browser Clients den Domänen Identitäten zuordnet, die COM+-Anwendung unter Identitäten für jede Anwendung ausführen und Tabellen in der Datenebene so konfigurieren, dass Sie nur über eine bestimmte Anwendungs Identität zugänglich sind.</span><span class="sxs-lookup"><span data-stu-id="73a01-107">If your application involves a browser-to-business-logic-to-database architecture, consider mapping the browser clients to domain identities, run the COM+ application under identities specific to each application, and configure tables in the data tier to be accessible only by a particular application identity.</span></span> <span data-ttu-id="73a01-108">Dieses vertrauenswürdige Server Szenario ist skalierbarer und weniger problematisch als die Verwendung des DBMS für die Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="73a01-108">This trusted server scenario is more scalable and less problematic than using the DBMS for authenticating.</span></span>
-   <span data-ttu-id="73a01-109">Wenn Sie eine Komponente entwerfen, die in einer verteilten Anwendung mithilfe der rollenbasierten Sicherheit verwendet wird, können Sie die [com+-Sicherheits](com--security.md) Funktionen verwenden.</span><span class="sxs-lookup"><span data-stu-id="73a01-109">If you are designing a component that will be used in a distributed application using role-based security, you can use the [COM+ security](com--security.md) functionality.</span></span> <span data-ttu-id="73a01-110">Diese Funktion ermöglicht Ihnen das Aufrufen von Methoden wie [**IObjectContext:: isCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-iscallerinrole) und [**IObjectContext:: issecurityaktivi,**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-issecurityenabled) um Code Blöcke vor nicht autorisiertem Zugriff zu schützen.</span><span class="sxs-lookup"><span data-stu-id="73a01-110">This functionality allows you to call methods such as [**IObjectContext::IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-iscallerinrole) and [**IObjectContext::IsSecurityEnabled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-issecurityenabled) to help protect blocks of code from unauthorized access.</span></span> <span data-ttu-id="73a01-111">Sie können auch den Sicherheits Aufruf Kontext verwenden, um Informationen zu den Aufrufern eines Objekts abzurufen.</span><span class="sxs-lookup"><span data-stu-id="73a01-111">You can also use the security call context to get information about an object's callers.</span></span>
-   <span data-ttu-id="73a01-112">Wenn Sie eine Komponente entwerfen, die in einer verteilten Anwendung verwendet wird, ohne rollenbasierte Sicherheit zu verwenden, wird die Sicherheit automatisch nur auf Prozessebene geprüft.</span><span class="sxs-lookup"><span data-stu-id="73a01-112">If you are designing a component that will be used in a distributed application without using role-based security, security is automatically checked only at the process level.</span></span> <span data-ttu-id="73a01-113">Prozess Zugriffsberechtigungen bestimmen, wer Zugriff auf die Anwendung erhält.</span><span class="sxs-lookup"><span data-stu-id="73a01-113">Process access permissions determine who is given access to the application.</span></span> <span data-ttu-id="73a01-114">Wenn Sie beim Prozess oder auf der Schnittstellen Ebene eine präzisere Steuerung der Sicherheitseinstellungen benötigen, verwenden Sie die von com bereitgestellte programmgesteuerte Sicherheitsfunktionalität.</span><span class="sxs-lookup"><span data-stu-id="73a01-114">If you need finer grain control over security settings at the process or at the interface level, use the programmatic security functionality provided by COM.</span></span>
-   <span data-ttu-id="73a01-115">Wenn eine Komponente, die die programmgesteuerte com+-Sicherheit verwendet, ohne Integration in eine COM+-Anwendung ausgeführt wird, werden Ausnahmen ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="73a01-115">If a component using COM+ programmatic security is run without being integrated into a COM+ application, exceptions will be thrown.</span></span> <span data-ttu-id="73a01-116">Wenn eine solche Komponente erfolgreich in eine Anwendung integriert werden soll, die nicht Teil der com+-Umgebung ist, müssen Sie daher alle Ausnahmen entsprechend behandeln.</span><span class="sxs-lookup"><span data-stu-id="73a01-116">Therefore, if you want such a component to be successfully integrated into an application that is not part of the COM+ environment, you must handle all exceptions appropriately.</span></span>

## <a name="related-topics"></a><span data-ttu-id="73a01-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="73a01-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73a01-118">Entwerfen für Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="73a01-118">Designing for Availability</span></span>](designing-for-availability.md)
</dt> <dt>

[<span data-ttu-id="73a01-119">Entwerfen für die Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="73a01-119">Designing for Deployment</span></span>](designing-for-deployment.md)
</dt> <dt>

[<span data-ttu-id="73a01-120">Entwerfen von Skalierbarkeit</span><span class="sxs-lookup"><span data-stu-id="73a01-120">Designing for Scalability</span></span>](designing-for-scalability.md)
</dt> <dt>

[<span data-ttu-id="73a01-121">Sicherheit für programmgesteuerte Komponenten</span><span class="sxs-lookup"><span data-stu-id="73a01-121">Programmatic Component Security</span></span>](programmatic-component-security.md)
</dt> </dl>

 

 



