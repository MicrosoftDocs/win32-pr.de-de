---
description: Eine COM+-Anwendung ist die primäre Verwaltungs-und Sicherheitseinheit für Komponenten Dienste und besteht aus einer Gruppe von COM-Komponenten, die im allgemeinen verwandte Funktionen ausführen.
ms.assetid: 82e94acb-e7ce-4423-a720-26ee65d0d7b4
title: Übersicht über die COM+-Anwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3365e0c0e7598d8f1eb2f466e8a2cea2d93edf4
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2021
ms.locfileid: "106349753"
---
# <a name="com-application-overview"></a><span data-ttu-id="9e4f4-103">Übersicht über die COM+-Anwendung</span><span class="sxs-lookup"><span data-stu-id="9e4f4-103">COM+ Application Overview</span></span>

<span data-ttu-id="9e4f4-104">Eine COM+-Anwendung ist die primäre Verwaltungs-und Sicherheitseinheit für Komponenten Dienste und besteht aus einer Gruppe von COM-Komponenten, die im allgemeinen verwandte Funktionen ausführen.</span><span class="sxs-lookup"><span data-stu-id="9e4f4-104">A COM+ application is the primary unit of administration and security for Component Services and consists of a group of COM components that generally perform related functions.</span></span> <span data-ttu-id="9e4f4-105">Diese Komponenten bestehen weiter aus Schnittstellen und Methoden, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="9e4f4-105">These components further consist of interfaces and methods, as shown in the following illustration.</span></span>

![Diagramm, das Schnittstellen und Methoden innerhalb von Feldern anzeigt, in der Reihenfolge der Methode innerhalb der Komponente innerhalb der com+-Anwendung.](images/487518b4-0460-4b2d-a834-c4ea57755ffd.png)

<span data-ttu-id="9e4f4-107">Mit dem Verwaltungs Programmkomponenten Dienste können Sie neue COM+-Anwendungen erstellen, Anwendungen Komponenten hinzufügen und die Attribute für eine Anwendung und deren Komponenten festlegen.</span><span class="sxs-lookup"><span data-stu-id="9e4f4-107">You can use the Component Services administrative tool to create new COM+ applications, add components to applications, and set the attributes for an application and its components.</span></span>

<span data-ttu-id="9e4f4-108">Indem Sie logische Gruppen von COM-Komponenten als com+-Anwendungen erstellen, können Sie die folgenden Vorteile von com+ nutzen:</span><span class="sxs-lookup"><span data-stu-id="9e4f4-108">By creating logical groups of COM components as COM+ applications, you can take advantage of the following benefits of COM+:</span></span>

-   <span data-ttu-id="9e4f4-109">Einen Bereitstellungs Bereich für COM-Komponenten.</span><span class="sxs-lookup"><span data-stu-id="9e4f4-109">A deployment scope for COM components.</span></span>
-   <span data-ttu-id="9e4f4-110">Einen allgemeinen Konfigurationsbereich für COM-Komponenten, einschließlich Sicherheitsgrenzen und Warteschlangen.</span><span class="sxs-lookup"><span data-stu-id="9e4f4-110">A common configuration scope for COM components, including security boundaries and queuing.</span></span>
-   <span data-ttu-id="9e4f4-111">Speicherung von Komponenten Attributen, die nicht vom Komponenten Entwickler bereitgestellt werden (z. b. Transaktionen und Synchronisierung).</span><span class="sxs-lookup"><span data-stu-id="9e4f4-111">Storage of component attributes not provided by the component developer (for example, transactions and synchronization).</span></span>
-   <span data-ttu-id="9e4f4-112">Komponenten-DLLs (Dynamic-Link Libraries), die bei Bedarf in Prozesse (DLLHost.exe) geladen werden.</span><span class="sxs-lookup"><span data-stu-id="9e4f4-112">Component dynamic-link libraries (DLLs) loaded into processes (DLLHost.exe) on demand.</span></span>
-   <span data-ttu-id="9e4f4-113">Verwaltete Server Prozesse zum Hosten von-Komponenten.</span><span class="sxs-lookup"><span data-stu-id="9e4f4-113">Managed server processes to host components.</span></span>
-   <span data-ttu-id="9e4f4-114">Erstellung und Verwaltung von Threads, die von-Komponenten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9e4f4-114">Creation and management of threads used by components.</span></span>
-   <span data-ttu-id="9e4f4-115">Zugriff auf das Kontext Objekt für Ressourcen Spender, sodass die zugeordneten Ressourcen automatisch dem Kontext zugeordnet werden können.</span><span class="sxs-lookup"><span data-stu-id="9e4f4-115">Access to the context object for resource dispensers, allowing acquired resources to be automatically associated with the context.</span></span> <span data-ttu-id="9e4f4-116">(Weitere Informationen zu COM-Komponenten und Kontexten finden Sie unter [com+-Kontexte](com--contexts.md).)</span><span class="sxs-lookup"><span data-stu-id="9e4f4-116">(For more information on COM components and contexts, see [COM+ Contexts](com--contexts.md).)</span></span>

## <a name="related-topics"></a><span data-ttu-id="9e4f4-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9e4f4-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9e4f4-118">Entwickeln von com+-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="9e4f4-118">Developing COM+ Applications</span></span>](developing-com--applications.md)
</dt> <dt>

[<span data-ttu-id="9e4f4-119">Teile einer COM+-Anwendung</span><span class="sxs-lookup"><span data-stu-id="9e4f4-119">Parts of a COM+ Application</span></span>](parts-of-a-com--application.md)
</dt> <dt>

[<span data-ttu-id="9e4f4-120">Typen von com+-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="9e4f4-120">Types of COM+ Applications</span></span>](types-of-com--applications.md)
</dt> </dl>

 

 



