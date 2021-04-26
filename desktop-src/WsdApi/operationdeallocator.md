---
description: Gibt den Typdelocator an, der von einer Stubfunktion für Vorgänge verwendet werden soll.
ms.assetid: 52e6235d-90e6-4559-b17c-14ca3be896ff
title: operationDeallocator-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe3ae0d9f1d37a478ceca0895806ade6a011747e
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994287"
---
# <a name="operationdeallocator-element"></a><span data-ttu-id="fd0ea-103">operationDeallocator-Element</span><span class="sxs-lookup"><span data-stu-id="fd0ea-103">operationDeallocator element</span></span>

<span data-ttu-id="fd0ea-104">Gibt den Typdelocator an, der von der Stubfunktion eines Vorgangs verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="fd0ea-104">Specifies the type deallocator to be used by an operation's stub function.</span></span>

## <a name="usage"></a><span data-ttu-id="fd0ea-105">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="fd0ea-105">Usage</span></span>

``` syntax
<operationDeallocator
  operation = "character_string"
  deallocator = "character_string"/>
```

## <a name="attributes"></a><span data-ttu-id="fd0ea-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="fd0ea-106">Attributes</span></span>



| <span data-ttu-id="fd0ea-107">Attribut</span><span class="sxs-lookup"><span data-stu-id="fd0ea-107">Attribute</span></span>                  | <span data-ttu-id="fd0ea-108">type</span><span class="sxs-lookup"><span data-stu-id="fd0ea-108">Type</span></span>                         | <span data-ttu-id="fd0ea-109">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="fd0ea-109">Required</span></span>       | <span data-ttu-id="fd0ea-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fd0ea-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------------------|------------------------------|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd0ea-111">**Deallocator**</span><span class="sxs-lookup"><span data-stu-id="fd0ea-111">**deallocator**</span></span><br/> | <span data-ttu-id="fd0ea-112">\_Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="fd0ea-112">character\_string</span></span><br/> | <span data-ttu-id="fd0ea-113">Ja</span><span class="sxs-lookup"><span data-stu-id="fd0ea-113">Yes</span></span><br/> | <span data-ttu-id="fd0ea-114">Der für den Vorgang zu verwendende Deallocator.</span><span class="sxs-lookup"><span data-stu-id="fd0ea-114">The deallocator to use for the operation.</span></span><br/> <br/> <span data-ttu-id="fd0ea-115">Die folgenden Zeichenfolgen sind gültige Werte.</span><span class="sxs-lookup"><span data-stu-id="fd0ea-115">The following strings are valid values.</span></span><br/> <br/> <dl><span data-ttu-id="fd0ea-116"><span id="none"></span><span id="NONE"></span><dt>"None"</dt> <span id="WSDFreeLinkedMemory"></span> <span id="wsdfreelinkedmemory"></span> <span id="WSDFREELINKEDMEMORY"></span> <dt>"WSDFreeLinkedMemory".</dt> <span id="CoTaskMemFree"></span> <span id="cotaskmemfree"></span> <span id="COTASKMEMFREE"></span> <dt>"CoTaskMemFree".</dt> <span id="free"></span> <span id="FREE"></span> <dt>"Free"</dt> <span id="delete"></span> <span id="DELETE"></span> <dt>"delete"</dt> <span id="deleteArray"></span> <span id="deletearray"></span> <span id="DELETEARRAY"></span> <dt>"deleteArray"</dt> <span id="Release"></span> <span id="release"></span> <span id="RELEASE"></span> <dt>"Release"</dt></span><span class="sxs-lookup"><span data-stu-id="fd0ea-116"><span id="none"></span><span id="NONE"></span><dt>\*\*\*\*none\*\*\*\*</dt><span id="WSDFreeLinkedMemory"></span><span id="wsdfreelinkedmemory"></span><span id="WSDFREELINKEDMEMORY"></span><dt>\*\*\*\*WSDFreeLinkedMemory\*\*\*\*</dt><span id="CoTaskMemFree"></span><span id="cotaskmemfree"></span><span id="COTASKMEMFREE"></span><dt>\*\*\*\*CoTaskMemFree\*\*\*\*</dt><span id="free"></span><span id="FREE"></span><dt>\*\*\*\*free\*\*\*\*</dt><span id="delete"></span><span id="DELETE"></span><dt>\*\*\*\*delete\*\*\*\*</dt><span id="deleteArray"></span><span id="deletearray"></span><span id="DELETEARRAY"></span><dt>\*\*\*\*deleteArray\*\*\*\*</dt><span id="Release"></span><span id="release"></span><span id="RELEASE"></span><dt>\*\*\*\*Release\*\*\*\*</dt></span></span> </dl> |
| <span data-ttu-id="fd0ea-117">**operation**</span><span class="sxs-lookup"><span data-stu-id="fd0ea-117">**operation**</span></span><br/>   | <span data-ttu-id="fd0ea-118">\_Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="fd0ea-118">character\_string</span></span><br/> | <span data-ttu-id="fd0ea-119">Ja</span><span class="sxs-lookup"><span data-stu-id="fd0ea-119">Yes</span></span><br/> | <span data-ttu-id="fd0ea-120">Der Name des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="fd0ea-120">The name of the operation.</span></span><br/> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



## <a name="child-elements"></a><span data-ttu-id="fd0ea-121">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fd0ea-121">Child elements</span></span>

<span data-ttu-id="fd0ea-122">Es gibt keine untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="fd0ea-122">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="fd0ea-123">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fd0ea-123">Parent elements</span></span>



| <span data-ttu-id="fd0ea-124">Element</span><span class="sxs-lookup"><span data-stu-id="fd0ea-124">Element</span></span>                                               | <span data-ttu-id="fd0ea-125">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fd0ea-125">Description</span></span>                                                                                   |
|-------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fd0ea-126">**stubDefinitions**</span><span class="sxs-lookup"><span data-stu-id="fd0ea-126">**stubDefinitions**</span></span>](stubdefinitions.md)<br/> | <span data-ttu-id="fd0ea-127">Generiert Implementierungen für Stubfunktionen für Porttypvorgänge.</span><span class="sxs-lookup"><span data-stu-id="fd0ea-127">Generates implementations for stub functions for port type operations.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="fd0ea-128">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="fd0ea-128">Element information</span></span>



| <span data-ttu-id="fd0ea-129">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="fd0ea-129">Label</span></span> | <span data-ttu-id="fd0ea-130">Wert</span><span class="sxs-lookup"><span data-stu-id="fd0ea-130">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="fd0ea-131">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="fd0ea-131">Minimum supported system</span></span><br/> | <span data-ttu-id="fd0ea-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fd0ea-132">Windows Vista</span></span> |
| <span data-ttu-id="fd0ea-133">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="fd0ea-133">Can be empty</span></span>                        | <span data-ttu-id="fd0ea-134">Ja</span><span class="sxs-lookup"><span data-stu-id="fd0ea-134">Yes</span></span>           |



 

 




