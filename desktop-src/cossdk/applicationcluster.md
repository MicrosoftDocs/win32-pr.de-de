---
description: Enthält eine Liste der Server Computer im Anwendungs Cluster. Sie enthält ein-Objekt für jeden Server.
ms.assetid: 8722080a-cf95-4c29-9eb7-99c6df93611f
title: ApplicationCluster-Sammlung
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ApplicationCluster
api_type:
- COM
api_location: ''
ms.openlocfilehash: 00a54f5c79bcbaf4ef61b130db556fc27f264101
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126596"
---
# <a name="applicationcluster-collection"></a><span data-ttu-id="0531e-104">ApplicationCluster-Sammlung</span><span class="sxs-lookup"><span data-stu-id="0531e-104">ApplicationCluster collection</span></span>

<span data-ttu-id="0531e-105">Enthält eine Liste der Server Computer im Anwendungs Cluster.</span><span class="sxs-lookup"><span data-stu-id="0531e-105">Contains a list of the server computers in the application cluster.</span></span> <span data-ttu-id="0531e-106">Sie enthält ein-Objekt für jeden Server.</span><span class="sxs-lookup"><span data-stu-id="0531e-106">It contains an object for each server.</span></span> <span data-ttu-id="0531e-107">Dabei handelt es sich um eine Auflistung der obersten Ebene.</span><span class="sxs-lookup"><span data-stu-id="0531e-107">This is a top-level collection.</span></span>

<span data-ttu-id="0531e-108">Der Anwendungs Cluster wird für Zwecke des CLB-Dienstanbieter (Component Load Balancing, Komponenten Lastenausgleich) definiert.</span><span class="sxs-lookup"><span data-stu-id="0531e-108">The application cluster is defined for purposes of the component load balancing (CLB) service.</span></span> <span data-ttu-id="0531e-109">Damit die Anwendungs Cluster Sammlung verwendet werden kann, muss der CLB-Dienst auf dem Computer installiert sein.</span><span class="sxs-lookup"><span data-stu-id="0531e-109">For the application cluster collection to be used, the CLB service must be installed on the computer.</span></span>

<span data-ttu-id="0531e-110">Sie legen einen Router im Anwendungs Cluster mit der isrouter-Eigenschaft für das [**LocalComputer**](localcomputer.md) -Sammlungsobjekt fest, und Sie legen fest, dass für eine bestimmte [**Komponente ein Lasten**](components.md) Ausgleich mit der LoadBalancingSupported-Eigenschaft eines komponentenauflistungs Objekts ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0531e-110">You designate a router in the application cluster with the IsRouter property on the [**LocalComputer**](localcomputer.md) collection object, and you designate that a given component should be load balanced with the LoadBalancingSupported property on a [**Components**](components.md) collection object.</span></span>

<span data-ttu-id="0531e-111">Diese Auflistung unterstützt die [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) -und [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) -Methoden des [**comadmincatalogcollection**](comadmincatalogcollection.md) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="0531e-111">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="0531e-112">Member</span><span class="sxs-lookup"><span data-stu-id="0531e-112">Members</span></span>

<span data-ttu-id="0531e-113">Die **ApplicationCluster** -Auflistung erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle, verfügt jedoch nicht über zusätzliche Member.</span><span class="sxs-lookup"><span data-stu-id="0531e-113">The **ApplicationCluster** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="0531e-114">Verwandte Auflistungen</span><span class="sxs-lookup"><span data-stu-id="0531e-114">Related Collections</span></span>

<span data-ttu-id="0531e-115">Sie können von dieser Sammlung zu einer der folgenden Sammlungen navigieren:</span><span class="sxs-lookup"><span data-stu-id="0531e-115">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="0531e-116">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="0531e-116">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="0531e-117">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="0531e-117">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="0531e-118">**Relatedcollectioninfo**</span><span class="sxs-lookup"><span data-stu-id="0531e-118">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="0531e-119">Sie können von den folgenden Sammlungen aus zu dieser Sammlung navigieren:</span><span class="sxs-lookup"><span data-stu-id="0531e-119">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="0531e-120">**Fasst**</span><span class="sxs-lookup"><span data-stu-id="0531e-120">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="0531e-121">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0531e-121">Properties</span></span>

<span data-ttu-id="0531e-122">Die folgenden Eigenschaften werden vom [**COMAdminCatalogObject**](comadmincatalogobject.md) -Objekt in der-Auflistung unterstützt:</span><span class="sxs-lookup"><span data-stu-id="0531e-122">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="0531e-123">Name</span><span class="sxs-lookup"><span data-stu-id="0531e-123">Name</span></span>](#name)

### <a name="name"></a><span data-ttu-id="0531e-124">Name</span><span class="sxs-lookup"><span data-stu-id="0531e-124">Name</span></span>



| <span data-ttu-id="0531e-125">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0531e-125">Entry</span></span> | <span data-ttu-id="0531e-126">Wert</span><span class="sxs-lookup"><span data-stu-id="0531e-126">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0531e-127">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0531e-127">Description</span></span>    | <span data-ttu-id="0531e-128">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="0531e-128">The name of the server.</span></span> <span data-ttu-id="0531e-129">Zusätzliche Leerzeichen am Anfang und Ende der Zeichenfolge werden entfernt. Diese Eigenschaft wird zurückgegeben, wenn die [**Schlüssel**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) -oder [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) -Eigenschaften Methode für ein Objekt dieser Auflistung aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="0531e-129">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="0531e-130">Access</span><span class="sxs-lookup"><span data-stu-id="0531e-130">Access</span></span>         | <span data-ttu-id="0531e-131">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="0531e-131">WriteOnce</span></span>                                                                                                                                                                                                                                                            |
| <span data-ttu-id="0531e-132">type</span><span class="sxs-lookup"><span data-stu-id="0531e-132">Type</span></span>           | <span data-ttu-id="0531e-133">String</span><span class="sxs-lookup"><span data-stu-id="0531e-133">String</span></span>                                                                                                                                                                                                                                                               |
| <span data-ttu-id="0531e-134">Standard</span><span class="sxs-lookup"><span data-stu-id="0531e-134">Default</span></span>        | <span data-ttu-id="0531e-135">"Neuer Computer"</span><span class="sxs-lookup"><span data-stu-id="0531e-135">"New Computer"</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="0531e-136">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="0531e-136">Minimum system</span></span> | <span data-ttu-id="0531e-137">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="0531e-137">Windows 2000</span></span>                                                                                                                                                                                                                                                         |



 

## <a name="see-also"></a><span data-ttu-id="0531e-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0531e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0531e-139">Com+-Verwaltungs Sammlungen</span><span class="sxs-lookup"><span data-stu-id="0531e-139">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
