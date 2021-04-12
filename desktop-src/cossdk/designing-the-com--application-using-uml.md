---
description: Zum Entwickeln einer erfolgreichen com+-Anwendung ist ein vorab Anwendungsarchitektur Entwurf erforderlich.
ms.assetid: 6a7cc610-e09a-4097-bc31-4e53db0ee152
title: Entwerfen der com+-Anwendung mithilfe von UML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48526623df5bc929daa4d8ce9cbe4d7592d6b30c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393049"
---
# <a name="designing-the-com-application-using-uml"></a><span data-ttu-id="a4fb7-103">Entwerfen der com+-Anwendung mithilfe von UML</span><span class="sxs-lookup"><span data-stu-id="a4fb7-103">Designing the COM+ Application Using UML</span></span>

<span data-ttu-id="a4fb7-104">Zum Entwickeln einer erfolgreichen com+-Anwendung ist ein vorab Anwendungsarchitektur Entwurf erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a4fb7-104">Developing a successful COM+ application requires up-front application architectural design.</span></span> <span data-ttu-id="a4fb7-105">Der Unified Modeling Language (UML) ist entscheidend für diese Entwurfsentwicklung.</span><span class="sxs-lookup"><span data-stu-id="a4fb7-105">The Unified Modeling Language (UML) is key to this design development.</span></span> <span data-ttu-id="a4fb7-106">UML ist eine Modellierungs Notation für Anwendungsdaten und Prozesse, die die bewährten Methoden der Softwarebranche kombiniert.</span><span class="sxs-lookup"><span data-stu-id="a4fb7-106">The UML is a modeling notation for application data and processes that combines the best practices of the software industry.</span></span> <span data-ttu-id="a4fb7-107">Da die UML-Anwendung die Anwendung in drei Ansichten unterteilt, die die Anwendung sowie deren Verpackung und Implementierung widerspiegeln, ist die Modellierungs Notation gut für die Unterstützung von Enterprise Modeling.</span><span class="sxs-lookup"><span data-stu-id="a4fb7-107">Because the UML breaks the application into three views that reflect the application as well as its packaging and implementation, the modeling notation extends well to support enterprise modeling.</span></span>

<span data-ttu-id="a4fb7-108">Die UML behandelt drei Ansichten der Anwendung wie folgt:</span><span class="sxs-lookup"><span data-stu-id="a4fb7-108">The UML addresses three views of the application, as follows:</span></span>

-   <span data-ttu-id="a4fb7-109">Die statische Ansicht, die anhand von Informationen modelliert wird, die aus Benutzer Szenarien und Klassendiagrammen entnommen wurden.</span><span class="sxs-lookup"><span data-stu-id="a4fb7-109">The static view, which is modeled by information taken from user scenarios and class diagrams.</span></span>
-   <span data-ttu-id="a4fb7-110">Die dynamische Ansicht, die mithilfe von Sequenz-, Zusammenarbeits-und Zustands Übergangs Diagrammen modelliert wird.</span><span class="sxs-lookup"><span data-stu-id="a4fb7-110">The dynamic view, which is modeled using sequence, collaboration, and state transition diagrams.</span></span>
-   <span data-ttu-id="a4fb7-111">Die funktionale Ansicht, bei der es sich um die herkömmliche beschreibende Darstellung mit Pseudo Code und Spezifikationen handelt.</span><span class="sxs-lookup"><span data-stu-id="a4fb7-111">The functional view, which is the more traditional descriptive narrative using pseudocode and specifications.</span></span>

<span data-ttu-id="a4fb7-112">Die Informationen für diese Sichten können durch die folgenden drei Entwurfs Schritte erfasst werden, die für die UML-Arbeit geeignet sind.</span><span class="sxs-lookup"><span data-stu-id="a4fb7-112">The information for these views can be gathered by following three design steps that work well with the UML.</span></span> <span data-ttu-id="a4fb7-113">Bevor Sie eine einzelne Codezeile schreiben, müssen Sie die folgenden Modelle erstellen:</span><span class="sxs-lookup"><span data-stu-id="a4fb7-113">Before writing a single line of code, you need to create the following models:</span></span>

<dl> <dt>

<span data-ttu-id="a4fb7-114"><span id="Conceptual_model"></span><span id="conceptual_model"></span><span id="CONCEPTUAL_MODEL"></span>Konzeptionelles Modell</span><span class="sxs-lookup"><span data-stu-id="a4fb7-114"><span id="Conceptual_model"></span><span id="conceptual_model"></span><span id="CONCEPTUAL_MODEL"></span>Conceptual model</span></span>
</dt> <dd>

<span data-ttu-id="a4fb7-115">Entscheiden Sie, welche Komponenten und Dienste erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="a4fb7-115">Decide what components and services are required.</span></span>

</dd> <dt>

<span data-ttu-id="a4fb7-116"><span id="Logical_model"></span><span id="logical_model"></span><span id="LOGICAL_MODEL"></span>Logisches Modell</span><span class="sxs-lookup"><span data-stu-id="a4fb7-116"><span id="Logical_model"></span><span id="logical_model"></span><span id="LOGICAL_MODEL"></span>Logical model</span></span>
</dt> <dd>

<span data-ttu-id="a4fb7-117">Bestimmen Sie, welcher logische Entwurfs Ebene Sie angehören.</span><span class="sxs-lookup"><span data-stu-id="a4fb7-117">Determine which logical design tier they belong in.</span></span>

</dd> <dt>

<span data-ttu-id="a4fb7-118"><span id="Physical_model"></span><span id="physical_model"></span><span id="PHYSICAL_MODEL"></span>Physisches Modell</span><span class="sxs-lookup"><span data-stu-id="a4fb7-118"><span id="Physical_model"></span><span id="physical_model"></span><span id="PHYSICAL_MODEL"></span>Physical model</span></span>
</dt> <dd>

<span data-ttu-id="a4fb7-119">Legen Sie fest, wo sich die Komponenten physisch befinden und wie Sie codiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a4fb7-119">Determine where the components reside physically and how they are to be coded.</span></span>

</dd> </dl>

<span data-ttu-id="a4fb7-120">Diese Modelle können dann mit UML-basierten Case-Tools verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a4fb7-120">These models can then be used with UML-based CASE tools.</span></span> <span data-ttu-id="a4fb7-121">Weitere Informationen zu diesen drei Entwurfs Modellen finden Sie in den folgenden Themen in diesem Abschnitt:</span><span class="sxs-lookup"><span data-stu-id="a4fb7-121">For more information on these three design models, see the following topics in this section:</span></span>

-   [<span data-ttu-id="a4fb7-122">Das konzeptionelle Modell: Anwendungsanforderungen</span><span class="sxs-lookup"><span data-stu-id="a4fb7-122">The Conceptual Model: Application Requirements</span></span>](the-conceptual-model--application-requirements.md)
-   [<span data-ttu-id="a4fb7-123">Das logische Modell: Anwendungs Definition und-Planung</span><span class="sxs-lookup"><span data-stu-id="a4fb7-123">The Logical Model: Application Definition and Planning</span></span>](the-logical-model--application-definition-and-planning.md)
-   [<span data-ttu-id="a4fb7-124">Das physische Modell: Anwendungsarchitektur</span><span class="sxs-lookup"><span data-stu-id="a4fb7-124">The Physical Model: Application Architecture</span></span>](the-physical-model--application-architecture.md)

## <a name="related-topics"></a><span data-ttu-id="a4fb7-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a4fb7-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4fb7-126">Com+-Entwurfs Annahmen und-Prinzipien</span><span class="sxs-lookup"><span data-stu-id="a4fb7-126">COM+ Design Assumptions and Principles</span></span>](com--design-assumptions-and-principles.md)
</dt> <dt>

[<span data-ttu-id="a4fb7-127">Allgemeine Entwurfs Tipps für die Verwendung von com+</span><span class="sxs-lookup"><span data-stu-id="a4fb7-127">General Design Tips for Using COM+</span></span>](general-design-tips-for-using-com-.md)
</dt> <dt>

[<span data-ttu-id="a4fb7-128">Optimieren von Interaktionen mit der com+-Geschäftslogik Ebene</span><span class="sxs-lookup"><span data-stu-id="a4fb7-128">Optimizing Interactions with the COM+ Business Logic Tier</span></span>](optimizing-interactions-with-the-com--business-logic-tier.md)
</dt> <dt>

[<span data-ttu-id="a4fb7-129">Weitere Microsoft-Tools zum entwickeln verteilter Anwendungen</span><span class="sxs-lookup"><span data-stu-id="a4fb7-129">Other Microsoft Tools for Building Distributed Applications</span></span>](other-microsoft-tools-for-building-distributed-applications.md)
</dt> </dl>

 

 



