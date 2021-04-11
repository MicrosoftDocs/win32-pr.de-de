---
description: Gibt den Typ der dezuweisung an, der von einer stubfunktion verwendet werden soll.
ms.assetid: 58228dfd-1d4b-41e5-b423-a54525021c22
title: enzuordcator-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3604f0efb366c3f88e2e0828c02344ee75606079
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215434"
---
# <a name="deallocator-element"></a><span data-ttu-id="1d815-103">enzuordcator-Element</span><span class="sxs-lookup"><span data-stu-id="1d815-103">deallocator element</span></span>

<span data-ttu-id="1d815-104">Gibt den Typ der dezuweisung an, der von einer stubfunktion verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1d815-104">Specifies the type of deallocator to be used by a stub function.</span></span>

## <a name="usage"></a><span data-ttu-id="1d815-105">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="1d815-105">Usage</span></span>

``` syntax
<deallocator/>
```

## <a name="attributes"></a><span data-ttu-id="1d815-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="1d815-106">Attributes</span></span>

<span data-ttu-id="1d815-107">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="1d815-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="1d815-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1d815-108">Child elements</span></span>

<span data-ttu-id="1d815-109">Es gibt keine untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="1d815-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="1d815-110">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1d815-110">Parent elements</span></span>



| <span data-ttu-id="1d815-111">Element</span><span class="sxs-lookup"><span data-stu-id="1d815-111">Element</span></span>                                               | <span data-ttu-id="1d815-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1d815-112">Description</span></span>                                                                                   |
|-------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1d815-113">**stubdefinitionen**</span><span class="sxs-lookup"><span data-stu-id="1d815-113">**stubDefinitions**</span></span>](stubdefinitions.md)<br/> | <span data-ttu-id="1d815-114">Generiert Implementierungen für Stub-Funktionen für Porttyp Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="1d815-114">Generates implementations for stub functions for port-type operations.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="1d815-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1d815-115">Remarks</span></span>

<span data-ttu-id="1d815-116">Der dezuordnertyp sollte in ein Tagpaar eingeschlossen werden <deallocator></deallocator> .</span><span class="sxs-lookup"><span data-stu-id="1d815-116">The deallocator type should be enclosed in a pair of <deallocator></deallocator> tags.</span></span> <span data-ttu-id="1d815-117">Die folgenden Zeichen folgen sind gültige Freigabe Werte:</span><span class="sxs-lookup"><span data-stu-id="1d815-117">The following strings are valid deallocator values:</span></span>

-   <span data-ttu-id="1d815-118">none</span><span class="sxs-lookup"><span data-stu-id="1d815-118">none</span></span>
-   <span data-ttu-id="1d815-119">Wsdfreelinkedmemory</span><span class="sxs-lookup"><span data-stu-id="1d815-119">WSDFreeLinkedMemory</span></span>
-   <span data-ttu-id="1d815-120">CoTaskMemFree</span><span class="sxs-lookup"><span data-stu-id="1d815-120">CoTaskMemFree</span></span>
-   <span data-ttu-id="1d815-121">free</span><span class="sxs-lookup"><span data-stu-id="1d815-121">free</span></span>
-   <span data-ttu-id="1d815-122">delete</span><span class="sxs-lookup"><span data-stu-id="1d815-122">delete</span></span>
-   <span data-ttu-id="1d815-123">deletearray</span><span class="sxs-lookup"><span data-stu-id="1d815-123">deleteArray</span></span>
-   <span data-ttu-id="1d815-124">Release</span><span class="sxs-lookup"><span data-stu-id="1d815-124">Release</span></span>

## <a name="element-information"></a><span data-ttu-id="1d815-125">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="1d815-125">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="1d815-126">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="1d815-126">Minimum supported system</span></span><br/> | <span data-ttu-id="1d815-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1d815-127">Windows Vista</span></span> |
| <span data-ttu-id="1d815-128">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="1d815-128">Can be empty</span></span>                        | <span data-ttu-id="1d815-129">Ja</span><span class="sxs-lookup"><span data-stu-id="1d815-129">Yes</span></span>           |



 

 




