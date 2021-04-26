---
description: Gibt den Typ des Deallocators an, der von einer Stubfunktion verwendet werden soll.
ms.assetid: 58228dfd-1d4b-41e5-b423-a54525021c22
title: deallocator-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 692ed2e57b3e649c0ee7af171f205c949496f9b4
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994937"
---
# <a name="deallocator-element"></a><span data-ttu-id="25a76-103">deallocator-Element</span><span class="sxs-lookup"><span data-stu-id="25a76-103">deallocator element</span></span>

<span data-ttu-id="25a76-104">Gibt den Typ des Deallocators an, der von einer Stubfunktion verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="25a76-104">Specifies the type of deallocator to be used by a stub function.</span></span>

## <a name="usage"></a><span data-ttu-id="25a76-105">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="25a76-105">Usage</span></span>

``` syntax
<deallocator/>
```

## <a name="attributes"></a><span data-ttu-id="25a76-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="25a76-106">Attributes</span></span>

<span data-ttu-id="25a76-107">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="25a76-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="25a76-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="25a76-108">Child elements</span></span>

<span data-ttu-id="25a76-109">Es gibt keine untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="25a76-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="25a76-110">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="25a76-110">Parent elements</span></span>



| <span data-ttu-id="25a76-111">Element</span><span class="sxs-lookup"><span data-stu-id="25a76-111">Element</span></span>                                               | <span data-ttu-id="25a76-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="25a76-112">Description</span></span>                                                                                   |
|-------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="25a76-113">**stubDefinitions**</span><span class="sxs-lookup"><span data-stu-id="25a76-113">**stubDefinitions**</span></span>](stubdefinitions.md)<br/> | <span data-ttu-id="25a76-114">Generiert Implementierungen für Stubfunktionen für Porttypvorgänge.</span><span class="sxs-lookup"><span data-stu-id="25a76-114">Generates implementations for stub functions for port-type operations.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="25a76-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="25a76-115">Remarks</span></span>

<span data-ttu-id="25a76-116">Der Deallocator-Typ sollte in ein Tagpaar eingeschlossen <deallocator></deallocator> werden.</span><span class="sxs-lookup"><span data-stu-id="25a76-116">The deallocator type should be enclosed in a pair of <deallocator></deallocator> tags.</span></span> <span data-ttu-id="25a76-117">Die folgenden Zeichenfolgen sind gültige Deallocator-Werte:</span><span class="sxs-lookup"><span data-stu-id="25a76-117">The following strings are valid deallocator values:</span></span>

-   <span data-ttu-id="25a76-118">Keine</span><span class="sxs-lookup"><span data-stu-id="25a76-118">none</span></span>
-   <span data-ttu-id="25a76-119">WSDFreeLinkedMemory</span><span class="sxs-lookup"><span data-stu-id="25a76-119">WSDFreeLinkedMemory</span></span>
-   <span data-ttu-id="25a76-120">CoTaskMemFree</span><span class="sxs-lookup"><span data-stu-id="25a76-120">CoTaskMemFree</span></span>
-   <span data-ttu-id="25a76-121">free</span><span class="sxs-lookup"><span data-stu-id="25a76-121">free</span></span>
-   <span data-ttu-id="25a76-122">delete</span><span class="sxs-lookup"><span data-stu-id="25a76-122">delete</span></span>
-   <span data-ttu-id="25a76-123">deleteArray</span><span class="sxs-lookup"><span data-stu-id="25a76-123">deleteArray</span></span>
-   <span data-ttu-id="25a76-124">Release</span><span class="sxs-lookup"><span data-stu-id="25a76-124">Release</span></span>

## <a name="element-information"></a><span data-ttu-id="25a76-125">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="25a76-125">Element information</span></span>



| <span data-ttu-id="25a76-126">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="25a76-126">Label</span></span> | <span data-ttu-id="25a76-127">Wert</span><span class="sxs-lookup"><span data-stu-id="25a76-127">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="25a76-128">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="25a76-128">Minimum supported system</span></span><br/> | <span data-ttu-id="25a76-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="25a76-129">Windows Vista</span></span> |
| <span data-ttu-id="25a76-130">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="25a76-130">Can be empty</span></span>                        | <span data-ttu-id="25a76-131">Ja</span><span class="sxs-lookup"><span data-stu-id="25a76-131">Yes</span></span>           |



 

 




