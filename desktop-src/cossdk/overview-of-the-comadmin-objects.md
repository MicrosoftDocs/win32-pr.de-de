---
description: Die COMAdmin-Objekte bieten ein einfaches Objektmodell, das Ihnen den Zugriff auf den com+-Katalog ermöglicht.
ms.assetid: 84cee7a7-f7a6-41a0-afd5-fae56365612e
title: Übersicht über die COMAdmin-Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22837cbe0548b623463234d1a03d17288eba2149
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127789"
---
# <a name="overview-of-the-comadmin-objects"></a><span data-ttu-id="1e8e0-103">Übersicht über die COMAdmin-Objekte</span><span class="sxs-lookup"><span data-stu-id="1e8e0-103">Overview of the COMAdmin Objects</span></span>

<span data-ttu-id="1e8e0-104">Die COMAdmin-Objekte bieten ein einfaches Objektmodell, das Ihnen den Zugriff auf den com+-Katalog ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="1e8e0-104">The COMAdmin objects offer a simple object model that provides you with access to the COM+ catalog.</span></span> <span data-ttu-id="1e8e0-105">Auf diese Weise werden alle Funktionen des Verwaltungs Programms Komponenten Dienste modelliert.</span><span class="sxs-lookup"><span data-stu-id="1e8e0-105">In doing so, they serve to model all the functionality provided by the Component Services administrative tool.</span></span> <span data-ttu-id="1e8e0-106">Jedes Mal, wenn Sie eine com+-Verwaltung durchführen, interagieren Sie mit dem com+-Katalog.</span><span class="sxs-lookup"><span data-stu-id="1e8e0-106">Whenever you do any kind of COM+ administration, you are interacting with the COM+ catalog.</span></span> <span data-ttu-id="1e8e0-107">Eine Beschreibung des Katalogs finden Sie unter [zugreifen auf den com+-Katalog](accessing-the-com--catalog.md).</span><span class="sxs-lookup"><span data-stu-id="1e8e0-107">For a description of the catalog, see [Accessing the COM+ Catalog](accessing-the-com--catalog.md).</span></span>

<span data-ttu-id="1e8e0-108">Die Informationen, die Sie entweder über das Verwaltungs Programmkomponenten Dienste oder mithilfe der COMAdmin-Objekte erhalten, sind ähnlich strukturiert, und die Aktionen, die Sie in einem der beiden Kontext ausführen, sind analog.</span><span class="sxs-lookup"><span data-stu-id="1e8e0-108">The information you obtain either from the Component Services administrative tool or by using the COMAdmin objects is structured similarly, and the actions you perform in either context are analogous.</span></span> <span data-ttu-id="1e8e0-109">Die grundlegende Korrelation zwischen der Verwendung des Komponenten Dienste-Snap-Ins und der programmgesteuerten Verwaltung besteht darin, dass Ordner in der Konsolen Struktur des Snap-Ins den Sammlungen im com+-Katalog entsprechen.</span><span class="sxs-lookup"><span data-stu-id="1e8e0-109">The basic correlation between using the Component Services snap-in and programmatic administration is that folders in the console tree of the snap-in correspond to collections in the COM+ catalog.</span></span> <span data-ttu-id="1e8e0-110">Das heißt, genauso wie jeder Ordner im Snap-in Elemente enthält alle Elemente. Beispielsweise enthält **com+-Anwendungen** installierte COM+-Anwendungen – jede Sammlung im com+-Katalog enthält Elemente mit einheitlicher Art.</span><span class="sxs-lookup"><span data-stu-id="1e8e0-110">That is, just as each folder in the snap-in contains items all of a kind; for example, **COM+ Applications** holds installed COM+ applications—each collection in the COM+ catalog holds items of a uniform kind.</span></span> <span data-ttu-id="1e8e0-111">Ebenso wie jedes Element in einem Ordner über Eigenschaften verfügt, die Sie für ein Eigenschaften Blatt festlegen können, werden von jedem Element in einer Sammlung Eigenschaften verfügbar gemacht, die Sie festlegen können.</span><span class="sxs-lookup"><span data-stu-id="1e8e0-111">Further, just as each item in a folder has properties that you can set on a property sheet, each item in a collection exposes properties that you can set.</span></span>

<span data-ttu-id="1e8e0-112">Damit Sie Objekte innerhalb dieser Struktur konfigurieren können, bieten die COMAdmin-Objekte Ihnen die Möglichkeit, die folgenden Aufgaben durchzuführen:</span><span class="sxs-lookup"><span data-stu-id="1e8e0-112">To enable you to configure objects within this structure, the COMAdmin objects provide you with the means to do the following:</span></span>

-   <span data-ttu-id="1e8e0-113">Zugreifen auf den com+-Katalog</span><span class="sxs-lookup"><span data-stu-id="1e8e0-113">Access the COM+ catalog</span></span>
-   <span data-ttu-id="1e8e0-114">Zugreifen auf Auflistungen im Katalog</span><span class="sxs-lookup"><span data-stu-id="1e8e0-114">Access collections in the catalog</span></span>
-   <span data-ttu-id="1e8e0-115">Zugreifen auf Elemente in Auflistungen</span><span class="sxs-lookup"><span data-stu-id="1e8e0-115">Access items in collections</span></span>
-   <span data-ttu-id="1e8e0-116">Zugreifen auf Eigenschaften für die Elemente in den Auflistungen</span><span class="sxs-lookup"><span data-stu-id="1e8e0-116">Access properties on the items in the collections</span></span>

<span data-ttu-id="1e8e0-117">Zur Unterstützung dieser Aktionen bietet die COMAdmin-Bibliothek die folgenden drei Klassen:</span><span class="sxs-lookup"><span data-stu-id="1e8e0-117">To support these actions, the COMAdmin Library provides the following three classes:</span></span>

-   <span data-ttu-id="1e8e0-118">[**Comadmincatalog**](comadmincatalog.md), das den Katalog selbst darstellt.</span><span class="sxs-lookup"><span data-stu-id="1e8e0-118">[**COMAdminCatalog**](comadmincatalog.md), which represents the catalog itself.</span></span>
-   <span data-ttu-id="1e8e0-119">[**Comadmincatalogcollection**](comadmincatalogcollection.md), die eine beliebige Sammlung darstellt.</span><span class="sxs-lookup"><span data-stu-id="1e8e0-119">[**COMAdminCatalogCollection**](comadmincatalogcollection.md), which represents any collection.</span></span>
-   <span data-ttu-id="1e8e0-120">[**COMAdminCatalogObject**](comadmincatalogobject.md), das jedes Element in einer Sammlung darstellt.</span><span class="sxs-lookup"><span data-stu-id="1e8e0-120">[**COMAdminCatalogObject**](comadmincatalogobject.md), which represents any item in a collection.</span></span>

<span data-ttu-id="1e8e0-121">Ausführlichere Beschreibungen dieser Klassen finden Sie unter [Zusammenfassungs Beschreibung der COMAdmin-Klassen](summary-description-of-the-comadmin-classes.md) in diesem Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="1e8e0-121">For fuller descriptions of these classes, see [Summary Description of the COMAdmin Classes](summary-description-of-the-comadmin-classes.md) in this section.</span></span>

<span data-ttu-id="1e8e0-122">Einen kurzen Überblick über typische Aktionen, die Sie in der programmgesteuerten Verwaltung durchführen, finden Sie unter [Einführ Endes Beispiel mithilfe des com+-Verwaltungs Katalogs](introductory-example-using-the-com--administration-catalog.md).</span><span class="sxs-lookup"><span data-stu-id="1e8e0-122">To get a quick idea of typical actions you perform in programmatic administration, see [Introductory Example Using the COM+ Administration Catalog](introductory-example-using-the-com--administration-catalog.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1e8e0-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1e8e0-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e8e0-124">Com+-Verwaltungsvorgänge in Transaktionen</span><span class="sxs-lookup"><span data-stu-id="1e8e0-124">COM+ Administration Operations Within Transactions</span></span>](com--administration-operations-within-transactions.md)
</dt> <dt>

[<span data-ttu-id="1e8e0-125">Behandeln von com+-Verwaltungsfehlern</span><span class="sxs-lookup"><span data-stu-id="1e8e0-125">Handling COM+ Administration Errors</span></span>](handling-com--administration-errors.md)
</dt> <dt>

[<span data-ttu-id="1e8e0-126">Einführ Endes Beispiel mit dem com+-Verwaltungs Katalog</span><span class="sxs-lookup"><span data-stu-id="1e8e0-126">Introductory Example Using the COM+ Administration Catalog</span></span>](introductory-example-using-the-com--administration-catalog.md)
</dt> <dt>

[<span data-ttu-id="1e8e0-127">Abrufen von Auflistungen im com+-Katalog</span><span class="sxs-lookup"><span data-stu-id="1e8e0-127">Retrieving Collections on the COM+ Catalog</span></span>](retrieving-collections-on-the-com--catalog.md)
</dt> <dt>

[<span data-ttu-id="1e8e0-128">Festlegen von Eigenschaften und Speichern von Änderungen am com+-Katalog</span><span class="sxs-lookup"><span data-stu-id="1e8e0-128">Setting Properties and Saving Changes to the COM+ Catalog</span></span>](setting-properties-and-saving-changes-to-the-com--catalog.md)
</dt> </dl>

 

 



