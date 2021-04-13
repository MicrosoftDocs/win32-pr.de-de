---
description: Enthält eine Liste der Computer im Ordner Computer des Verwaltungs Tools Komponenten Dienste. Sie enthält ein-Objekt für jeden Computer.
ms.assetid: 56e32b47-a9f5-4888-b727-71ad0499da00
title: Sammlung von Computer Listen
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ComputerList
api_type:
- COM
api_location: ''
ms.openlocfilehash: 379e5e07a86d06961de3f8f3936a260451bf43ae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483222"
---
# <a name="computerlist-collection"></a><span data-ttu-id="99b41-104">Sammlung von Computer Listen</span><span class="sxs-lookup"><span data-stu-id="99b41-104">ComputerList collection</span></span>

<span data-ttu-id="99b41-105">Enthält eine Liste der Computer im Ordner **Computer** des Verwaltungs Tools Komponenten Dienste.</span><span class="sxs-lookup"><span data-stu-id="99b41-105">Contains a list of the computers in the **Computers** folder of the Component Services administration tool.</span></span> <span data-ttu-id="99b41-106">Sie enthält ein-Objekt für jeden Computer.</span><span class="sxs-lookup"><span data-stu-id="99b41-106">It contains an object for each computer.</span></span>

<span data-ttu-id="99b41-107">Diese Auflistung unterstützt die [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) -und [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) -Methoden des [**comadmincatalogcollection**](comadmincatalogcollection.md) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="99b41-107">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="99b41-108">Member</span><span class="sxs-lookup"><span data-stu-id="99b41-108">Members</span></span>

<span data-ttu-id="99b41-109">Die Sammlung " **Computer List** " erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle, verfügt jedoch nicht über zusätzliche Mitglieder.</span><span class="sxs-lookup"><span data-stu-id="99b41-109">The **ComputerList** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="99b41-110">Verwandte Auflistungen</span><span class="sxs-lookup"><span data-stu-id="99b41-110">Related Collections</span></span>

<span data-ttu-id="99b41-111">Sie können von dieser Sammlung zu einer der folgenden Sammlungen navigieren:</span><span class="sxs-lookup"><span data-stu-id="99b41-111">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="99b41-112">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="99b41-112">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="99b41-113">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="99b41-113">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="99b41-114">**Relatedcollectioninfo**</span><span class="sxs-lookup"><span data-stu-id="99b41-114">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="99b41-115">Sie können von den folgenden Sammlungen aus zu dieser Sammlung navigieren:</span><span class="sxs-lookup"><span data-stu-id="99b41-115">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="99b41-116">**Fasst**</span><span class="sxs-lookup"><span data-stu-id="99b41-116">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="99b41-117">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="99b41-117">Properties</span></span>

<span data-ttu-id="99b41-118">Die folgenden Eigenschaften werden vom [**COMAdminCatalogObject**](comadmincatalogobject.md) -Objekt in der-Auflistung unterstützt:</span><span class="sxs-lookup"><span data-stu-id="99b41-118">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="99b41-119">Name</span><span class="sxs-lookup"><span data-stu-id="99b41-119">Name</span></span>](#name)

### <a name="name"></a><span data-ttu-id="99b41-120">Name</span><span class="sxs-lookup"><span data-stu-id="99b41-120">Name</span></span>



| <span data-ttu-id="99b41-121">Eingabe</span><span class="sxs-lookup"><span data-stu-id="99b41-121">Entry</span></span> | <span data-ttu-id="99b41-122">Wert</span><span class="sxs-lookup"><span data-stu-id="99b41-122">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99b41-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="99b41-123">Description</span></span>    | <span data-ttu-id="99b41-124">Der Name des Computers.</span><span class="sxs-lookup"><span data-stu-id="99b41-124">The name of the computer.</span></span> <span data-ttu-id="99b41-125">Zusätzliche Leerzeichen am Anfang und Ende der Zeichenfolge werden entfernt. Diese Eigenschaft wird zurückgegeben, wenn die [**Schlüssel**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) -oder [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) -Eigenschaften Methode für ein Objekt dieser Auflistung aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="99b41-125">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="99b41-126">Access</span><span class="sxs-lookup"><span data-stu-id="99b41-126">Access</span></span>         | <span data-ttu-id="99b41-127">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="99b41-127">WriteOnce</span></span>                                                                                                                                                                                                                                                              |
| <span data-ttu-id="99b41-128">type</span><span class="sxs-lookup"><span data-stu-id="99b41-128">Type</span></span>           | <span data-ttu-id="99b41-129">String</span><span class="sxs-lookup"><span data-stu-id="99b41-129">String</span></span>                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="99b41-130">Standard</span><span class="sxs-lookup"><span data-stu-id="99b41-130">Default</span></span>        | <span data-ttu-id="99b41-131">"Neuer Computer"</span><span class="sxs-lookup"><span data-stu-id="99b41-131">"New Computer"</span></span>                                                                                                                                                                                                                                                         |
| <span data-ttu-id="99b41-132">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="99b41-132">Minimum system</span></span> | <span data-ttu-id="99b41-133">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="99b41-133">Windows 2000</span></span>                                                                                                                                                                                                                                                           |



 

## <a name="see-also"></a><span data-ttu-id="99b41-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="99b41-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99b41-135">Com+-Verwaltungs Sammlungen</span><span class="sxs-lookup"><span data-stu-id="99b41-135">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
