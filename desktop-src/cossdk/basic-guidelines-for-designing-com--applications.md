---
description: Grundlegende Richtlinien zum Entwerfen von com+-Anwendungen
ms.assetid: 2d08bd05-5b0c-480c-91fd-b2bf321fc21e
title: Grundlegende Richtlinien zum Entwerfen von com+-Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b6552022c3a9c2f50172164d1ed60811c5272e0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127161"
---
# <a name="basic-guidelines-for-designing-com-applications"></a><span data-ttu-id="38f5b-103">Grundlegende Richtlinien zum Entwerfen von com+-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="38f5b-103">Basic Guidelines for Designing COM+ Applications</span></span>

<span data-ttu-id="38f5b-104">Um com+ in vollem Umfang nutzen zu können, gibt es einige grundlegende Richtlinien, die Sie beim Erstellen einer Anwendung verwenden können:</span><span class="sxs-lookup"><span data-stu-id="38f5b-104">To take full advantage of COM+, there are a few basic guidelines you can use when creating an application:</span></span>

-   <span data-ttu-id="38f5b-105">**Modellieren Sie Ihren permanenten Zustand als Datenbankschema, indem Sie das gewünschte Daten Bank Tool verwenden.**</span><span class="sxs-lookup"><span data-stu-id="38f5b-105">**Model your durable state as a database schema, using your database tool of choice.**</span></span> <span data-ttu-id="38f5b-106">Fast jede Anwendung muss einen permanenten Zustand aufrechterhalten.</span><span class="sxs-lookup"><span data-stu-id="38f5b-106">Almost every application needs to maintain durable state.</span></span> <span data-ttu-id="38f5b-107">Datenbanken stellen die Dienste bereit, die zum Erstellen dauerhafter und skalierbarer Speicher Zustands erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="38f5b-107">Databases provide the services needed to create durable and scalable storage of state.</span></span> <span data-ttu-id="38f5b-108">Der erste Schritt beim Erstellen einer COM+-Anwendung besteht daher darin, den permanenten Zustand Ihrer Anwendung als eine Art Datenbankschema zu modellieren.</span><span class="sxs-lookup"><span data-stu-id="38f5b-108">Therefore, the first step in creating a COM+ application is to model the durable state of your application as some sort of database schema.</span></span> <span data-ttu-id="38f5b-109">Es spielt keine Rolle, welche Datenbank Sie verwenden; die meisten kommerziellen Datenbanken sind mit com+ kompatibel.</span><span class="sxs-lookup"><span data-stu-id="38f5b-109">It doesn't really matter what database you use; most commercial databases are compatible with COM+.</span></span> <span data-ttu-id="38f5b-110">Microsoft SQL Server ist ein gutes Beispiel für eine Lösung, die Sie verwenden können.</span><span class="sxs-lookup"><span data-stu-id="38f5b-110">Microsoft SQL Server is a good example of one solution you could use.</span></span>

-   <span data-ttu-id="38f5b-111">**Modellieren Sie die Logik der com+-Anwendung als Satz von COM-Schnittstellen.**</span><span class="sxs-lookup"><span data-stu-id="38f5b-111">**Model the logic of your COM+ application as a set of COM interfaces.**</span></span> <span data-ttu-id="38f5b-112">Wenn Sie über ein Schema verfügen, das die Zustandsinformationen der Anwendung darstellt, modellieren Sie die Austausch Vorgänge in der Anwendung als COM-Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="38f5b-112">Once you have a schema that represents the state information of the application, model the interchanges that happen in the application as COM interfaces.</span></span> <span data-ttu-id="38f5b-113">Diese Schnittstellen modellieren das Verhalten der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="38f5b-113">These interfaces will model the behavior of the application.</span></span> <span data-ttu-id="38f5b-114">Dies ist auch die Entwicklungsphase, wenn Sie bestimmen möchten, welche com+-Dienste für Ihre Anwendung am besten geeignet sind.</span><span class="sxs-lookup"><span data-stu-id="38f5b-114">This is also the development stage when you should determine which COM+ services work best for your application.</span></span>

-   <span data-ttu-id="38f5b-115">**Buildkomponentendlls, die Komponenten enthalten, die das physische Datenschema verwenden, und eine logische Ansicht der Daten für andere Komponenten (das erste Element in dieser Liste) verfügbar machen, sowie Komponenten, die in Bezug auf das logische Datenmodell (das zweite Element in dieser Liste) implementiert werden.**</span><span class="sxs-lookup"><span data-stu-id="38f5b-115">**Build component DLLs that contain components that use the physical data schema and expose a logical view of the data to other components (the first item in this list), as well as components that are implemented in terms of the logical data model (the second item in this list).**</span></span> <span data-ttu-id="38f5b-116">Sobald Sie die Struktur der Logik und die Zustandsinformationen haben, können Sie mit dem Schreiben von Code beginnen und nun dll-basierte com-Komponenten schreiben, die die Schnittstellen im Hinblick auf das definierte Schema implementieren.</span><span class="sxs-lookup"><span data-stu-id="38f5b-116">Once you have the structure of the logic and the state information, you can begin to write code and can now write DLL-based COM components that implement the interfaces in terms of the defined schema.</span></span> <span data-ttu-id="38f5b-117">Ihre Komponenten fungieren einfach als Manipulatoren zum Arbeiten mit ihren Datenbankinformationen, und mit ihren Komponenten-DLLs können Sie eine COM+-Anwendung erstellen, die funktioniert und erfolgreich skaliert werden kann.</span><span class="sxs-lookup"><span data-stu-id="38f5b-117">Your components simply act as manipulators for working with your database information, and your component DLLs enable you build a COM+ application that works and that scales successfully.</span></span>

-   <span data-ttu-id="38f5b-118">**Stellen Sie die Komponenten in der com+-Umgebung mithilfe der com+-Dienste bereit, die Sie ausgewählt haben.**</span><span class="sxs-lookup"><span data-stu-id="38f5b-118">**Deploy the components in the COM+ environment using the COM+ services you've selected.**</span></span> <span data-ttu-id="38f5b-119">Nachdem Sie die Anwendung erstellt haben, können Sie die Anwendung in einem Netzwerk oder einem Server Cluster bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="38f5b-119">Once you have built the application, you can then deploy the application across a network or server cluster.</span></span> <span data-ttu-id="38f5b-120">Sie können jetzt auf der Grundlage der verfügbaren ressourcenentscheidungen treffen, und Sie können jede Komponente für maximale Leistung anpassen.</span><span class="sxs-lookup"><span data-stu-id="38f5b-120">You can now make decisions based on resources available, and you can tailor each component for maximum performance.</span></span>

## <a name="related-topics"></a><span data-ttu-id="38f5b-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="38f5b-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="38f5b-122">Com+-Entwurfs Annahmen und-Prinzipien</span><span class="sxs-lookup"><span data-stu-id="38f5b-122">COM+ Design Assumptions and Principles</span></span>](com--design-assumptions-and-principles.md)
</dt> <dt>

[<span data-ttu-id="38f5b-123">Entwerfen der com+-Anwendung mithilfe von UML</span><span class="sxs-lookup"><span data-stu-id="38f5b-123">Designing the COM+ Application Using UML</span></span>](designing-the-com--application-using-uml.md)
</dt> <dt>

[<span data-ttu-id="38f5b-124">Allgemeine Entwurfs Tipps für die Verwendung von com+</span><span class="sxs-lookup"><span data-stu-id="38f5b-124">General Design Tips for Using COM+</span></span>](general-design-tips-for-using-com-.md)
</dt> <dt>

[<span data-ttu-id="38f5b-125">Optimieren von Interaktionen mit der com+-Geschäftslogik Ebene</span><span class="sxs-lookup"><span data-stu-id="38f5b-125">Optimizing Interactions with the COM+ Business Logic Tier</span></span>](optimizing-interactions-with-the-com--business-logic-tier.md)
</dt> <dt>

[<span data-ttu-id="38f5b-126">Weitere Microsoft-Tools zum entwickeln verteilter Anwendungen</span><span class="sxs-lookup"><span data-stu-id="38f5b-126">Other Microsoft Tools for Building Distributed Applications</span></span>](other-microsoft-tools-for-building-distributed-applications.md)
</dt> </dl>

 

 



