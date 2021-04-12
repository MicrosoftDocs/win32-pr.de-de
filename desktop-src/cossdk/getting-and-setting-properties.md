---
description: Eigenschaften werden erhalten und festgelegt
ms.assetid: 259612e7-70df-4f0f-90bc-766008dfdce7
title: Festlegen und Festlegen von Eigenschaften (Komponenten Dienste)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d151b08293cd32a35cd27bdba4dd3a37cdebfa4f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483446"
---
# <a name="getting-and-setting-properties-component-services"></a><span data-ttu-id="b932c-103">Festlegen und Festlegen von Eigenschaften (Komponenten Dienste)</span><span class="sxs-lookup"><span data-stu-id="b932c-103">Getting and Setting Properties (Component Services)</span></span>

<span data-ttu-id="b932c-104">Bevor Sie bestimmte Eigenschaften lesen oder schreiben können, die von einem Element in einer Sammlung verfügbar gemacht werden, müssen Sie die folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="b932c-104">Before you can read or write particular properties exposed by an item in a collection, you must take the following steps:</span></span>

1.  <span data-ttu-id="b932c-105">Rufen Sie die-Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="b932c-105">Retrieve the collection.</span></span>
2.  <span data-ttu-id="b932c-106">Füllen Sie die Sammlung aus, um Daten aus dem com+-Katalog einzulesen.</span><span class="sxs-lookup"><span data-stu-id="b932c-106">Populate the collection to read in data for it from the COM+ catalog.</span></span>
3.  <span data-ttu-id="b932c-107">Rufen Sie das spezifische Element in der Auflistung ab, das es mit einem Objekt aus der [**COMAdminCatalogObject**](comadmincatalogobject.md) -Klasse darstellt.</span><span class="sxs-lookup"><span data-stu-id="b932c-107">Retrieve the specific item in the collection, representing it with an object from the [**COMAdminCatalogObject**](comadmincatalogobject.md) class.</span></span>

<span data-ttu-id="b932c-108">Ein Beispiel, das diese Schritte veranschaulicht, finden Sie unter [Navigieren in der com+](navigating-the-com--collection-hierarchy.md)-Auflistungs Hierarchie.</span><span class="sxs-lookup"><span data-stu-id="b932c-108">For an example that illustrates these steps, see [Navigating the COM+ Collection Hierarchy](navigating-the-com--collection-hierarchy.md).</span></span>

<span data-ttu-id="b932c-109">Da die jeweils verfügbaren Eigenschaften variieren können, hängt davon ab, was das Element darstellt. Das heißt, ein Element, das eine Komponente darstellt, verfügt über andere Eigenschaften als eine, die eine COM+-Anwendung darstellt.</span><span class="sxs-lookup"><span data-stu-id="b932c-109">Because the particular properties exposed can vary depending on what the item represents; that is, an item representing a component has different properties than one representing a COM+ application.</span></span> <span data-ttu-id="b932c-110">Legen Sie eine dieser Eigenschaften mithilfe einer einzelnen generischen Eigenschaft (der Wert-Eigenschaft) für [**COMAdminCatalogObject**](comadmincatalogobject.md)fest.</span><span class="sxs-lookup"><span data-stu-id="b932c-110">Set any of these properties using a single generic property, the Value property, on [**COMAdminCatalogObject**](comadmincatalogobject.md).</span></span>

<span data-ttu-id="b932c-111">Die Value-Eigenschaft ermöglicht es Ihnen, eine bestimmte benannte Eigenschaft, die von einem Element verfügbar gemacht wird, zu erhalten oder festzulegen, bei der Erstellung einen Wert für eine benannte Eigenschaft zurückzugeben und beim Festlegen einen Namen und einen Wert zu nehmen.</span><span class="sxs-lookup"><span data-stu-id="b932c-111">The Value property enables you to get or set any specific named property exposed by an item, returning a value for a named property when getting, and taking a name and value when setting.</span></span>

<span data-ttu-id="b932c-112">Es werden erst dann Änderungen im com+-Katalog aufgezeichnet, wenn Sie die Änderungen mithilfe der [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) -Methode für das [**comadmincatalogcollection**](comadmincatalogcollection.md) -Objekt explizit speichern.</span><span class="sxs-lookup"><span data-stu-id="b932c-112">No changes are actually recorded to the COM+ catalog until you explicitly save changes using the [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) method on the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span> <span data-ttu-id="b932c-113">Ausstehende Änderungen für alle Eigenschaften in allen Elementen in einer bestimmten Sammlung werden gleichzeitig gespeichert.</span><span class="sxs-lookup"><span data-stu-id="b932c-113">Pending changes for all properties on all items in a given collection are saved all at once.</span></span> <span data-ttu-id="b932c-114">Weitere Informationen finden Sie unter [Speichern oder Verwerfen von Änderungen](saving-or-discarding-changes.md).</span><span class="sxs-lookup"><span data-stu-id="b932c-114">For details, see [Saving or Discarding Changes](saving-or-discarding-changes.md).</span></span>

<span data-ttu-id="b932c-115">Nicht alle Änderungen, die Sie vornehmen, werden akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="b932c-115">Not all changes that you make will be accepted.</span></span> <span data-ttu-id="b932c-116">Der com+-Katalog erzwingt eine gewisse Konsistenz Logik, um sicherzustellen, dass Sie die Dinge auf sinnvolle Weise konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="b932c-116">The COM+ catalog enforces some coherency logic to ensure that you configure things in a reasonable way.</span></span> <span data-ttu-id="b932c-117">Wenn Sie einige Eigenschaften ändern, können sich außerdem andere automatisch durch die gleiche Konsistenz Logik ändern.</span><span class="sxs-lookup"><span data-stu-id="b932c-117">Additionally, when you change some properties, others might change automatically by the same coherency logic.</span></span> <span data-ttu-id="b932c-118">Diese Effekte werden angezeigt, wenn Sie versuchen, Änderungen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="b932c-118">These effects show up when you attempt to save changes.</span></span>

> [!Note]  
> <span data-ttu-id="b932c-119">Es ist möglich, dass Sie mit einem anderen Writer im com+-Katalog in Konflikt stehen.</span><span class="sxs-lookup"><span data-stu-id="b932c-119">It is possible for you to be in contention with another writer to the COM+ catalog.</span></span> <span data-ttu-id="b932c-120">Zwischen Aufrufen von "Auffüllen [**" und "**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) " für eine bestimmte Sammlung verfügen Sie nicht über eine Sperre für diese Daten im Katalog.</span><span class="sxs-lookup"><span data-stu-id="b932c-120">Between calls to [**Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) and [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) for a given collection, you do not have a lock on any of that data in the catalog.</span></span> <span data-ttu-id="b932c-121">Mehrere Parteien können gleichzeitig Elemente in einer bestimmten Sammlung konfigurieren und können Konflikte aufweisen, wenn Sie Änderungen speichern.</span><span class="sxs-lookup"><span data-stu-id="b932c-121">Multiple parties may simultaneously be configuring items in a given collection and could be contending when they save changes.</span></span> <span data-ttu-id="b932c-122">Dies bedeutet, dass eine andere Person die Einstellungen eines Objekts vor oder nach dem Ausführen ändern kann, entweder mithilfe der COMAdmin-Objekte oder mithilfe des Verwaltungs Programms Komponenten Dienste entweder lokal oder Remote.</span><span class="sxs-lookup"><span data-stu-id="b932c-122">This means that someone else might change settings on an object before or after you do, either running some kind of program using the COMAdmin objects or using the Component Services administrative tool, either locally or remotely.</span></span> <span data-ttu-id="b932c-123">Die allgemeine Regel, bei der Objekte im Katalog geschrieben werden, besteht darin, dass alle Eigenschaften eines Objekts gleichzeitig geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="b932c-123">The general rule with writing objects on the catalog is that all properties on an object are written at once.</span></span> <span data-ttu-id="b932c-124">Das heißt, der letzte Writer gewinnt – das Objekt wird im Katalog genau so gespeichert, wie es vom letzten Writer konfiguriert wurde.</span><span class="sxs-lookup"><span data-stu-id="b932c-124">That is, the last writer wins—the object is saved in the catalog precisely as the last writer configured it.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="b932c-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b932c-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b932c-126">Abhängigkeiten zwischen Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b932c-126">Interdependencies Between Properties</span></span>](interdependencies-between-properties.md)
</dt> <dt>

[<span data-ttu-id="b932c-127">Abfragen von verfügbaren Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b932c-127">Querying for Available Properties</span></span>](querying-for-available-properties.md)
</dt> <dt>

[<span data-ttu-id="b932c-128">Speichern oder Verwerfen von Änderungen</span><span class="sxs-lookup"><span data-stu-id="b932c-128">Saving or Discarding Changes</span></span>](saving-or-discarding-changes.md)
</dt> </dl>

 

 



