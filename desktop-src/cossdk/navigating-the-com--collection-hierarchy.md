---
description: Navigieren in der com+-Sammlungs Hierarchie
ms.assetid: bd72effe-898f-40a6-973c-a26e7fe2478f
title: Navigieren in der com+-Sammlungs Hierarchie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06fc4cde6c56bc08b0326e892409067759e91be6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106339689"
---
# <a name="navigating-the-com-collection-hierarchy"></a><span data-ttu-id="150bb-103">Navigieren in der com+-Sammlungs Hierarchie</span><span class="sxs-lookup"><span data-stu-id="150bb-103">Navigating the COM+ Collection Hierarchy</span></span>

<span data-ttu-id="150bb-104">Einige Auflistungen, die Sie problemlos abrufen können, indem Sie die [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) -Methode für das [**comadmincatalog**](comadmincatalog.md) -Objekt verwenden.</span><span class="sxs-lookup"><span data-stu-id="150bb-104">Some collections you can retrieve easily by using the [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) method on the [**COMAdminCatalog**](comadmincatalog.md) object.</span></span> <span data-ttu-id="150bb-105">Diese Methode ruft eine Auflistung der obersten Ebene ab. Das heißt, eine Auflistung, z. b. [**Anwendungen**](applications.md), die eigenständig ist und eindeutig und in keiner anderen Auflistung logisch unterteilt ist.</span><span class="sxs-lookup"><span data-stu-id="150bb-105">This method retrieves a "top-level" collection; that is, a collection such as [**Applications**](applications.md), which stands on its own and which is unique and not logically subsumed under another collection.</span></span>

<span data-ttu-id="150bb-106">Viele Auflistungen werden jedoch in einer anderen Auflistung logisch unterteilt, weil Sie Elemente enthalten, die Teil einer größeren Struktur sind.</span><span class="sxs-lookup"><span data-stu-id="150bb-106">Many collections, however, are logically subsumed under another collection because they contain elements that are part of some larger structure.</span></span> <span data-ttu-id="150bb-107">Beispielsweise wird die [**Komponenten**](components.md) Auflistung mit der [**Anwendungs**](applications.md) Auflistung subsumed oder verknüpft, da Sie die Komponenten enthält, die in einer bestimmten COM+-Anwendung installiert sind, die wiederum einem Element in der **Anwendungs** Auflistung entspricht.</span><span class="sxs-lookup"><span data-stu-id="150bb-107">For example, the [**Components**](components.md) collection is subsumed, or related, to the [**Applications**](applications.md) collection because it contains the components installed in a particular COM+ application, which itself corresponds to an item in the **Applications** collection.</span></span> <span data-ttu-id="150bb-108">Verwandte Auflistungen wie diese sind nicht eindeutig. für jede einzelne Anwendung gibt es eine **Komponenten** Sammlung.</span><span class="sxs-lookup"><span data-stu-id="150bb-108">Related collections such as this are not unique; there is a **Components** collection for each distinct application.</span></span>

<span data-ttu-id="150bb-109">Daher werden Auflistungen in einer hierarchischen Struktur angeordnet, die auf natürliche Weise den logischen Beziehungen zwischen den darin enthaltenen Elementen entspricht.</span><span class="sxs-lookup"><span data-stu-id="150bb-109">Therefore, collections are arranged in a hierarchical structure that corresponds naturally to the logical relationships between the items they contain.</span></span> <span data-ttu-id="150bb-110">Ein Diagramm der Sammlungs Hierarchie finden Sie unter [com+-Verwaltungs Sammlungen](com--administration-collections.md).</span><span class="sxs-lookup"><span data-stu-id="150bb-110">A diagram of the collection hierarchy can be found at [COM+ Administration Collections](com--administration-collections.md).</span></span> <span data-ttu-id="150bb-111">Für viele der Elemente, die Sie mit den COMAdmin-Objekten konfigurieren möchten, müssen Sie durch einen Teil der Sammlungs Hierarchie navigieren, um das entsprechende Element abzurufen.</span><span class="sxs-lookup"><span data-stu-id="150bb-111">For many of the elements that you want to configure using the COMAdmin objects, you need to navigate through some portion of the collection hierarchy to retrieve the appropriate item.</span></span>

<span data-ttu-id="150bb-112">Dies bedeutet in der Praxis, dass Sie, wenn Sie ein Element in einer verknüpften Auflistung erhalten möchten, alle erforderlichen höheren Ebenen durchlaufen müssen.</span><span class="sxs-lookup"><span data-stu-id="150bb-112">What this means in practice is that if you want to get an item in a related collection, you need to go through all the necessary higher level, subsuming collections first.</span></span> <span data-ttu-id="150bb-113">Zum Abrufen einer verknüpften Auflistung müssen Sie das spezifische Element in der übergeordneten Auflistung abrufen, mit der die untergeordnete Auflistung verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="150bb-113">And to retrieve a related collection, you need to retrieve the specific item in the parent collection to which the child collection is related.</span></span> <span data-ttu-id="150bb-114">Wenn Sie z. b. ein Element konfigurieren möchten, das einer Komponente in einer bestimmten COM+-Anwendung entspricht, müssen Sie die folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="150bb-114">For example, if you want to configure an item corresponding to a component in a particular COM+ application, you must perform the following steps:</span></span>

1.  <span data-ttu-id="150bb-115">Holen Sie sich die [**Anwendungs**](applications.md) Auflistung, und füllen Sie Sie auf.</span><span class="sxs-lookup"><span data-stu-id="150bb-115">Get the [**Applications**](applications.md) collection and populate it.</span></span>
2.  <span data-ttu-id="150bb-116">Durchlaufen Sie den Inhalt der [**Anwendungs**](applications.md) Auflistung, bis Sie zu dem Element gelangen, das der richtigen COM+-Anwendung entspricht.</span><span class="sxs-lookup"><span data-stu-id="150bb-116">Enumerate through the contents of the [**Applications**](applications.md) collection until you get to the item corresponding to the correct COM+ application.</span></span>
3.  <span data-ttu-id="150bb-117">Rufen Sie die [**Komponenten**](components.md) Auflistung für die jeweilige COM+-Anwendung ab, und füllen Sie Sie auf.</span><span class="sxs-lookup"><span data-stu-id="150bb-117">Get and populate the [**Components**](components.md) collection for that particular COM+ application.</span></span>
4.  <span data-ttu-id="150bb-118">Durchlaufen Sie den Inhalt der [**Komponenten**](components.md) Auflistung, bis Sie zu dem Element gelangen, das der richtigen Komponente entspricht.</span><span class="sxs-lookup"><span data-stu-id="150bb-118">Enumerate through the contents of the [**Components**](components.md) collection until you get to the item corresponding to the correct component.</span></span>

<span data-ttu-id="150bb-119">Im folgenden Microsoft Visual Basic Beispiel wird gezeigt, wie die vorangegangenen Schritte ausgeführt werden:</span><span class="sxs-lookup"><span data-stu-id="150bb-119">The following Microsoft Visual Basic example shows how to perform the preceding steps:</span></span>


```VB
On Error GoTo My_Error_Handler

Dim Catalog As COMAdminCatalog 
Set Catalog = CreateObject("COMAdmin.COMAdminCatalog")

' Get the Applications collection and populate it.
Dim Applications As COMAdminCatalogCollection 
Set Applications = Catalog.GetCollection("Applications") 
Applications.Populate

' Get the correct application, "My Application".
Dim AppObject As COMAdminCatalogObject 
For Each AppObject in Applications 
    If AppObject.Name = "My Application" Then 
        Exit For 
    End If
Next 

' Get and populate the Components collection for "My Application".
Dim Components As COMAdminCatalogCollection 
Set Components = Applications.GetCollection("Components", AppObject.Key) 
Components.Populate

' Get the correct component, "My Component".
Dim CompObject As COMAdminCatalogObject 
For Each CompObject in Components 
    If CompObject.Name = "My Component" Then 
        Exit For 
    End If
Next 

```



<span data-ttu-id="150bb-120">Im vorherigen Beispiel werden zwei unterschiedliche **GetCollection** -Methoden verwendet.</span><span class="sxs-lookup"><span data-stu-id="150bb-120">Two distinct **GetCollection** methods are used in the preceding example.</span></span> <span data-ttu-id="150bb-121">Der erste wird durch [**comadmincatalog**](comadmincatalog.md) verfügbar gemacht und wird verwendet, um eine Sammlung der obersten Ebene zu erhalten – in diesem Fall "Applications".</span><span class="sxs-lookup"><span data-stu-id="150bb-121">The first is exposed by [**COMAdminCatalog**](comadmincatalog.md) and is used to get a top-level collection—in this case, "Applications".</span></span> <span data-ttu-id="150bb-122">Die zweite wird durch [**comadmincatalogcollection**](comadmincatalogcollection.md) verfügbar gemacht und wird verwendet, um eine Auflistung zu erhalten, die mit der aktuellen Auflistung verknüpft ist. Sie geben genau die gewünschte Auflistung an, indem Sie den Namen "Components" und den Schlüssel Eigenschafts Wert des übergeordneten Objekts übergeben.</span><span class="sxs-lookup"><span data-stu-id="150bb-122">The second is exposed by [**COMAdminCatalogCollection**](comadmincatalogcollection.md) and is used to get a collection related to the present collection; you indicate precisely which collection you want by passing in the name "Components" and the Key property value of the parent object.</span></span> <span data-ttu-id="150bb-123">Der Schlüssel Eigenschafts Wert ist oft ein Name oder eine GUID, die das Objekt eindeutig identifiziert. Dieser Wert wird in der Dokumentation für jede Sammlung identifiziert.</span><span class="sxs-lookup"><span data-stu-id="150bb-123">The Key property value is often a name or a GUID that uniquely identifies the object; this value is identified in the documentation for each collection.</span></span>

<span data-ttu-id="150bb-124">In den meisten Fällen müssen Sie verwandte Auflistungen iterativ in der Sammlungs Hierarchie abrufen, bis Sie die gewünschte Sammlung abrufen.</span><span class="sxs-lookup"><span data-stu-id="150bb-124">In the most general case, you need to get related collections iteratively down the collection hierarchy until you retrieve the collection you want.</span></span> <span data-ttu-id="150bb-125">Die Schritte, die Sie durchführen würden, folgen dem gleichen allgemeinen Modell, wiederholt.</span><span class="sxs-lookup"><span data-stu-id="150bb-125">The steps you would take follow the same general model, repetitively.</span></span> <span data-ttu-id="150bb-126">Eine komplette Liste der Sammlungen finden Sie unter [com+-Verwaltungs Sammlungen](com--administration-collections.md).</span><span class="sxs-lookup"><span data-stu-id="150bb-126">For a complete list of collections, see [COM+ Administration Collections](com--administration-collections.md).</span></span>

<span data-ttu-id="150bb-127">In einigen Fällen möchten Sie möglicherweise eine Verknüpfungs Methode verwenden, wenn Sie ein zweites Mal einen Pfad über die Auflistungs Hierarchie befolgen.</span><span class="sxs-lookup"><span data-stu-id="150bb-127">In some cases, you might want to use a shortcut method the second time you follow a path through the collection hierarchy.</span></span> <span data-ttu-id="150bb-128">Diese Methode kann nur verwendet werden, nachdem Sie bereits alle dazwischen liegenden Schlüsselwerte zwischengespeichert haben.</span><span class="sxs-lookup"><span data-stu-id="150bb-128">You can use this method only after you have already cached all the intervening Key values.</span></span> <span data-ttu-id="150bb-129">Weitere Informationen finden Sie unter [**icomadmincatalog:: getcollectionbyquery**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollectionbyquery).</span><span class="sxs-lookup"><span data-stu-id="150bb-129">For details, see [**ICOMAdminCatalog::GetCollectionByQuery**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollectionbyquery).</span></span>

## <a name="related-topics"></a><span data-ttu-id="150bb-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="150bb-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="150bb-131">Com+-Sammlungen werden aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="150bb-131">Populating COM+ Collections</span></span>](populating-com--collections.md)
</dt> <dt>

[<span data-ttu-id="150bb-132">Abfragen von verfügbaren verwandten Sammlungen</span><span class="sxs-lookup"><span data-stu-id="150bb-132">Querying for Available Related Collections</span></span>](querying-for-available-related-collections.md)
</dt> <dt>

[<span data-ttu-id="150bb-133">Abrufen von Auflistungen im com+-Katalog</span><span class="sxs-lookup"><span data-stu-id="150bb-133">Retrieving Collections on the COM+ Catalog</span></span>](retrieving-collections-on-the-com--catalog.md)
</dt> </dl>

 

 



