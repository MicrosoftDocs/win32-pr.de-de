---
description: Jedes Element in einer Auflistung macht Eigenschaften verfügbar.
ms.assetid: d9af57ea-c5b3-4017-bdc2-e43b86b3ddcd
title: Bearbeiten von Eigenschaften im com+-Katalog
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94ed2bade8886fe08bb7ed1ece179b35677569f1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748273"
---
# <a name="editing-properties-in-the-com-catalog"></a><span data-ttu-id="67db9-103">Bearbeiten von Eigenschaften im com+-Katalog</span><span class="sxs-lookup"><span data-stu-id="67db9-103">Editing Properties in the COM+ Catalog</span></span>

<span data-ttu-id="67db9-104">Jedes Element in einer Auflistung macht Eigenschaften verfügbar.</span><span class="sxs-lookup"><span data-stu-id="67db9-104">Each item in a collection exposes properties.</span></span> <span data-ttu-id="67db9-105">Diese Eigenschaften dienen zum Speichern von Konfigurationsdaten für jedes Element, das das Element darstellt.</span><span class="sxs-lookup"><span data-stu-id="67db9-105">These properties serve to hold configuration data for whatever element the item represents.</span></span> <span data-ttu-id="67db9-106">Diese Eigenschaften werden im Verwaltungs Programmkomponenten Dienste auf einer Eigenschaften Seite angezeigt, auf die Sie zugreifen können, indem Sie mit der rechten Maustaste auf ein Element in einem Ordner klicken.</span><span class="sxs-lookup"><span data-stu-id="67db9-106">In the Component Services administrative tool, these properties appear on a property page that you access by right-clicking an item in a folder.</span></span>

<span data-ttu-id="67db9-107">Da die Elemente in einer bestimmten Auflistung alle dieselbe Art darstellen, machen diese Elemente einen Satz von Eigenschaften verfügbar, der in der gesamten Auflistung konsistent ist.</span><span class="sxs-lookup"><span data-stu-id="67db9-107">Because the items in a given collection all represent the same kind of thing, those items expose a set of properties that is consistent across the collection.</span></span> <span data-ttu-id="67db9-108">Beispielsweise macht die [**Anwendungs**](applications.md) Auflistung eine Name-Eigenschaft, eine AppID-Eigenschaft usw. verfügbar.</span><span class="sxs-lookup"><span data-stu-id="67db9-108">For example, the [**Applications**](applications.md) collection exposes a Name property, an AppID property, and so forth.</span></span> <span data-ttu-id="67db9-109">Dies entspricht der Art und Weise, wie die einzelnen Anwendungen im Verwaltungs Programmkomponenten Dienste eine einheitlich strukturierte Eigenschaften Seite für die Anwendung bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="67db9-109">This is analogous to how each application in the Component Services administrative tool has a consistently structured property page available for it.</span></span> <span data-ttu-id="67db9-110">Eine Liste der Eigenschaften, die für die **Anwendungs** Sammlung verfügbar sind, finden Sie unter **Anwendungen**.</span><span class="sxs-lookup"><span data-stu-id="67db9-110">For a list of properties available to the **Applications** collection, see **Applications**.</span></span> <span data-ttu-id="67db9-111">Eine Liste der Eigenschaften, die für die [**Komponenten**](components.md) Auflistung verfügbar sind, finden Sie unter **Komponenten**.</span><span class="sxs-lookup"><span data-stu-id="67db9-111">For a list of properties available to the [**Components**](components.md) collection, see **Components**.</span></span>

<span data-ttu-id="67db9-112">Eine umfassende Liste der Eigenschaften, die von Elementen in jeder Sammlung verfügbar gemacht werden, finden Sie unter [com+-Verwaltungs Sammlungen](com--administration-collections.md).</span><span class="sxs-lookup"><span data-stu-id="67db9-112">For a complete list of properties exposed by items in each collection, see [COM+ Administration Collections](com--administration-collections.md).</span></span>

<span data-ttu-id="67db9-113">Sie stellen ein Element in einer Auflistung dar, indem Sie ein Objekt verwenden, das aus der [**COMAdminCatalogObject**](comadmincatalogobject.md) -Klasse erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="67db9-113">You represent an item in a collection by using an object created from the [**COMAdminCatalogObject**](comadmincatalogobject.md) class.</span></span> <span data-ttu-id="67db9-114">Mit diesem Objekt können Sie alle Eigenschaften, die vom Element verfügbar gemacht werden, festlegen und erhalten.</span><span class="sxs-lookup"><span data-stu-id="67db9-114">This object enables you to set and get any of the properties exposed by the item.</span></span> <span data-ttu-id="67db9-115">Beim Festlegen von Eigenschaften ist es auch möglich, dass Sie mit einem anderen Writer mit dem com+-Katalog in Konflikt stehen.</span><span class="sxs-lookup"><span data-stu-id="67db9-115">When setting properties, it is also possible that you might be contending with another writer to the COM+ catalog.</span></span> <span data-ttu-id="67db9-116">Weitere Informationen finden Sie unter " [erhalten und Festlegen von Eigenschaften](getting-and-setting-properties.md)".</span><span class="sxs-lookup"><span data-stu-id="67db9-116">For more information, see [Getting and Setting Properties](getting-and-setting-properties.md).</span></span>

<span data-ttu-id="67db9-117">Nachdem Sie die Eigenschaften festgelegt haben, wird tatsächlich ein Commit für die Änderungen ausgeführt, bis Sie die Änderungen explizit speichern.</span><span class="sxs-lookup"><span data-stu-id="67db9-117">After you have set properties, no changes are actually committed until you explicitly save changes.</span></span> <span data-ttu-id="67db9-118">Weitere Informationen finden Sie unter [Speichern oder Verwerfen von Änderungen](saving-or-discarding-changes.md).</span><span class="sxs-lookup"><span data-stu-id="67db9-118">For more information, see [Saving or Discarding Changes](saving-or-discarding-changes.md).</span></span>

<span data-ttu-id="67db9-119">Wenn Sie Änderungen speichern, erzwingt der com+-Katalog einige Konfigurations Logik, um sicherzustellen, dass keine inkompatiblen Konfigurationen festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="67db9-119">When you save changes, the COM+ catalog enforces some configuration logic to ensure that you don't set things to incompatible configurations.</span></span> <span data-ttu-id="67db9-120">Außerdem werden einige Eigenschaften geändert, wenn Sie bestimmte andere Eigenschaften explizit ändern.</span><span class="sxs-lookup"><span data-stu-id="67db9-120">It also changes some properties for you when you explicitly change certain other properties.</span></span> <span data-ttu-id="67db9-121">Weitere Informationen finden Sie unter Abhängigkeiten [zwischen Eigenschaften](interdependencies-between-properties.md).</span><span class="sxs-lookup"><span data-stu-id="67db9-121">For more information, see [Interdependencies Between Properties](interdependencies-between-properties.md).</span></span>

<span data-ttu-id="67db9-122">Außerdem verfügt com+ über eine Funktion, mit der Sie dynamisch Abfragen können, um festzustellen, welche Eigenschaften für die Elemente in einer bestimmten Sammlung verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="67db9-122">Additionally, COM+ has a facility that enables you to dynamically query to see what properties are available for the items in a given collection.</span></span> <span data-ttu-id="67db9-123">Weitere Informationen finden Sie unter [Abfragen von verfügbaren Eigenschaften](querying-for-available-properties.md).</span><span class="sxs-lookup"><span data-stu-id="67db9-123">For details, see [Querying for Available Properties](querying-for-available-properties.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="67db9-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="67db9-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="67db9-125">Com+-Verwaltungsvorgänge in Transaktionen</span><span class="sxs-lookup"><span data-stu-id="67db9-125">COM+ Administration Operations Within Transactions</span></span>](com--administration-operations-within-transactions.md)
</dt> <dt>

[<span data-ttu-id="67db9-126">Behandeln von com+-Verwaltungsfehlern</span><span class="sxs-lookup"><span data-stu-id="67db9-126">Handling COM+ Administration Errors</span></span>](handling-com--administration-errors.md)
</dt> <dt>

[<span data-ttu-id="67db9-127">Einführ Endes Beispiel mit dem com+-Verwaltungs Katalog</span><span class="sxs-lookup"><span data-stu-id="67db9-127">Introductory Example Using the COM+ Administration Catalog</span></span>](introductory-example-using-the-com--administration-catalog.md)
</dt> <dt>

[<span data-ttu-id="67db9-128">Übersicht über die COMAdmin-Objekte</span><span class="sxs-lookup"><span data-stu-id="67db9-128">Overview of the COMAdmin Objects</span></span>](overview-of-the-comadmin-objects.md)
</dt> <dt>

[<span data-ttu-id="67db9-129">Abrufen von Auflistungen im com+-Katalog</span><span class="sxs-lookup"><span data-stu-id="67db9-129">Retrieving Collections on the COM+ Catalog</span></span>](retrieving-collections-on-the-com--catalog.md)
</dt> </dl>

 

 



