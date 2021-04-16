---
description: Verfügbarkeit ist die Fähigkeit einer Anwendung, Fehler in Server Ressourcen zu tolerieren.
ms.assetid: 5d9a8216-a568-4443-b94f-1b2f2827a4be
title: Entwerfen für Verfügbarkeit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 222583c9f53a1ccc88f2a4f984f445de02a2c976
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523547"
---
# <a name="designing-for-availability"></a><span data-ttu-id="7f30e-103">Entwerfen für Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="7f30e-103">Designing for Availability</span></span>

<span data-ttu-id="7f30e-104">Verfügbarkeit ist die Fähigkeit einer Anwendung, Fehler in Server Ressourcen zu tolerieren.</span><span class="sxs-lookup"><span data-stu-id="7f30e-104">Availability is the ability of an application to tolerate failures in server resources.</span></span> <span data-ttu-id="7f30e-105">Dies bedeutet, dass der Client weiterhin über den Fehler bedient wird und dass der Fehler im Idealfall für den Client transparent ist.</span><span class="sxs-lookup"><span data-stu-id="7f30e-105">This means that the client continues to be served through the failure and that, ideally, the failure is transparent to the client.</span></span> <span data-ttu-id="7f30e-106">Natürlich kann der Fehler entweder von Hardware-oder Software Quellen stammen, sodass Sie für beide Fälle entwickeln müssen.</span><span class="sxs-lookup"><span data-stu-id="7f30e-106">Obviously, the failure can come from either hardware or software sources, so you must develop for both cases.</span></span>

<span data-ttu-id="7f30e-107">Die Verfügbarkeit kann durch die folgenden Faktoren beeinträchtigt werden:</span><span class="sxs-lookup"><span data-stu-id="7f30e-107">Availability can be affected by the following factors:</span></span>

-   <span data-ttu-id="7f30e-108">Anwendungsmodell.</span><span class="sxs-lookup"><span data-stu-id="7f30e-108">Application model.</span></span> <span data-ttu-id="7f30e-109">Stellen Sie sicher, dass die kritische Anwendungslogik mit dem [com+-Transaktions](com--transactions.md) Dienst ausgeführt wird, um die höchste Verfügbarkeit sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="7f30e-109">For highest availability, ensure that the critical application logic is conducted using the [COM+ transactions](com--transactions.md) service.</span></span> <span data-ttu-id="7f30e-110">Außerdem kann die Verwendung eines Kompensierungs Mechanismus effektiv sein, um sicherzustellen, dass die Ressourcen nach Fehlern in einem fehlerfreien Zustand bleiben.</span><span class="sxs-lookup"><span data-stu-id="7f30e-110">In addition, using a compensation mechanism can be effective in ensuring that resources remain in a healthy state after failures.</span></span>
-   <span data-ttu-id="7f30e-111">Client Modell.</span><span class="sxs-lookup"><span data-stu-id="7f30e-111">Client model.</span></span> <span data-ttu-id="7f30e-112">Integrieren Sie die Logik "Wiederholungs Versuche bei Fehler" in die Client Anwendung, und suchen Sie nach einer ordnungsgemäßen Verschlechterung der Anwendung, wenn Ressourcen oder Dienste nicht verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="7f30e-112">Integrate "retry on failure" logic into the client application, and strive for a graceful degradation in the application if resources or services are unavailable.</span></span> <span data-ttu-id="7f30e-113">Verstehen Sie, was der Client von der Anwendung erwartet, und erstellen Sie einen Entwurf, der Alternativen ermöglicht, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="7f30e-113">Understand what the client is expecting from the application, and create a design that allows for alternatives when a failure occurs.</span></span>
-   <span data-ttu-id="7f30e-114">Daten-/statusverfügbarkeit.</span><span class="sxs-lookup"><span data-stu-id="7f30e-114">Data/state availability.</span></span> <span data-ttu-id="7f30e-115">Verwenden Sie zum konsistenten Zugriff auf persistente Daten die Windows-Cluster Unterstützung, um Failoverunterstützung bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="7f30e-115">For consistent access to persistent data, use Windows Clustering to provide failover support.</span></span>
-   <span data-ttu-id="7f30e-116">Dienst Verfügbarkeit.</span><span class="sxs-lookup"><span data-stu-id="7f30e-116">Service availability.</span></span> <span data-ttu-id="7f30e-117">Sie können den Netzwerk Lastenausgleich für den Lastenausgleich eingehender IP-Anforderungen in einem Cluster von Servern verwenden.</span><span class="sxs-lookup"><span data-stu-id="7f30e-117">You can use Network Load Balancing to load balance incoming IP requests across a cluster of servers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7f30e-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7f30e-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7f30e-119">Entwerfen für die Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="7f30e-119">Designing for Deployment</span></span>](designing-for-deployment.md)
</dt> <dt>

[<span data-ttu-id="7f30e-120">Entwerfen von Skalierbarkeit</span><span class="sxs-lookup"><span data-stu-id="7f30e-120">Designing for Scalability</span></span>](designing-for-scalability.md)
</dt> <dt>

[<span data-ttu-id="7f30e-121">Entwerfen für Sicherheit</span><span class="sxs-lookup"><span data-stu-id="7f30e-121">Designing for Security</span></span>](designing-for-security.md)
</dt> </dl>

 

 



