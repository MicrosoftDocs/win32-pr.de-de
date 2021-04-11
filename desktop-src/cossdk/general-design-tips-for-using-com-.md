---
description: Der Schlüssel für einen guten Entwurf ist die Planung. Wenn Sie mit dem Entwerfen einer Anwendung mit drei Ebenen nicht vertraut sind, finden Sie weitere Informationen im Abschnitt entwerfen der com+-Anwendung mithilfe von UML.
ms.assetid: 463f4154-92f6-46c3-95ff-8513963dcadd
title: Allgemeine Entwurfs Tipps für die Verwendung von com+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5765259f170b1a98f1abb2d097dfdaec2e09d47
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126584"
---
# <a name="general-design-tips-for-using-com"></a><span data-ttu-id="eed6e-104">Allgemeine Entwurfs Tipps für die Verwendung von com+</span><span class="sxs-lookup"><span data-stu-id="eed6e-104">General Design Tips for Using COM+</span></span>

<span data-ttu-id="eed6e-105">Der Schlüssel für einen guten Entwurf ist die Planung.</span><span class="sxs-lookup"><span data-stu-id="eed6e-105">The key to good design is planning.</span></span> <span data-ttu-id="eed6e-106">Wenn Sie mit dem Entwerfen einer Anwendung mit drei Ebenen nicht vertraut sind, finden Sie weitere Informationen im Abschnitt [Entwerfen der com+-Anwendung mithilfe von UML](designing-the-com--application-using-uml.md).</span><span class="sxs-lookup"><span data-stu-id="eed6e-106">If you are unfamiliar with designing a three-tier application, see the section entitled [Designing the COM+ Application Using UML](designing-the-com--application-using-uml.md).</span></span>

<span data-ttu-id="eed6e-107">Wie Sie die COM-Komponenten, die die mittlere Ebene der com+-Anwendung bilden, erstellen, kann sich erheblich auf die Leistung, Skalierbarkeit und einfache Bereitstellung auswirken.</span><span class="sxs-lookup"><span data-stu-id="eed6e-107">How you construct the COM components that make up the middle tier of your COM+ application can dramatically affect performance, scalability, and ease of deployment.</span></span> <span data-ttu-id="eed6e-108">Die folgenden Themen bieten Entwurfs Überlegungen und Implementierungs Tipps, die Sie beim Entwerfen von COM-Komponenten kennen sollten.</span><span class="sxs-lookup"><span data-stu-id="eed6e-108">The following topics provide design considerations and implementation tips you should know about when designing COM components.</span></span>



| <span data-ttu-id="eed6e-109">Thema</span><span class="sxs-lookup"><span data-stu-id="eed6e-109">Topic</span></span>                                                                   | <span data-ttu-id="eed6e-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eed6e-110">Description</span></span>                                                                                                                |
|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="eed6e-111">Entwerfen von Skalierbarkeit</span><span class="sxs-lookup"><span data-stu-id="eed6e-111">Designing for Scalability</span></span>](designing-for-scalability.md)<br/>   | <span data-ttu-id="eed6e-112">Schlägt Möglichkeiten vor, die Skalierbarkeit der com+-Anwendung zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="eed6e-112">Suggests ways to increase the scalability of your COM+ application.</span></span><br/>                                             |
| [<span data-ttu-id="eed6e-113">Entwerfen für Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="eed6e-113">Designing for Availability</span></span>](designing-for-availability.md)<br/> | <span data-ttu-id="eed6e-114">Erläutert Dienste, die Sie verwenden können, um die Verfügbarkeit der Funktionen der mittleren Ebene in com+-Anwendungen zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="eed6e-114">Discusses services you can use to improve the availability your middle-tier functionality in COM+ applications.</span></span><br/> |
| [<span data-ttu-id="eed6e-115">Entwerfen für Sicherheit</span><span class="sxs-lookup"><span data-stu-id="eed6e-115">Designing for Security</span></span>](designing-for-security.md)<br/>         | <span data-ttu-id="eed6e-116">Erläutert Möglichkeiten zur optimalen Einrichtung der Sicherheit für eine COM+-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="eed6e-116">Discusses ways to most efficiently set up security for a COM+ application.</span></span><br/>                                      |
| [<span data-ttu-id="eed6e-117">Entwerfen für die Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="eed6e-117">Designing for Deployment</span></span>](designing-for-deployment.md)<br/>     | <span data-ttu-id="eed6e-118">Erläutert Möglichkeiten, Bereitstellungs Probleme beim Entwerfen einer verteilten Anwendung zu minimieren.</span><span class="sxs-lookup"><span data-stu-id="eed6e-118">Discusses ways to minimize deployment headaches when designing a distributed application.</span></span><br/>                       |



 

<span data-ttu-id="eed6e-119">Stellen Sie außerdem sicher, dass Sie die [Leistung mit dem Objekt Pooling verbessern](improving-performance-with-object-pooling.md) , um die Verwendung von Objekt Pooling zu optimieren.</span><span class="sxs-lookup"><span data-stu-id="eed6e-119">Also, be sure to see [Improving Performance with Object Pooling](improving-performance-with-object-pooling.md) for ways to most effectively use object pooling.</span></span>

## <a name="related-topics"></a><span data-ttu-id="eed6e-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="eed6e-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eed6e-121">Com+-Entwurfs Annahmen und-Prinzipien</span><span class="sxs-lookup"><span data-stu-id="eed6e-121">COM+ Design Assumptions and Principles</span></span>](com--design-assumptions-and-principles.md)
</dt> <dt>

[<span data-ttu-id="eed6e-122">Entwerfen der com+-Anwendung mithilfe von UML</span><span class="sxs-lookup"><span data-stu-id="eed6e-122">Designing the COM+ Application Using UML</span></span>](designing-the-com--application-using-uml.md)
</dt> <dt>

[<span data-ttu-id="eed6e-123">Optimieren von Interaktionen mit der com+-Geschäftslogik Ebene</span><span class="sxs-lookup"><span data-stu-id="eed6e-123">Optimizing Interactions with the COM+ Business Logic Tier</span></span>](optimizing-interactions-with-the-com--business-logic-tier.md)
</dt> <dt>

[<span data-ttu-id="eed6e-124">Weitere Microsoft-Tools zum entwickeln verteilter Anwendungen</span><span class="sxs-lookup"><span data-stu-id="eed6e-124">Other Microsoft Tools for Building Distributed Applications</span></span>](other-microsoft-tools-for-building-distributed-applications.md)
</dt> </dl>

 

 




