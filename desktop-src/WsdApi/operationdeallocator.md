---
description: Gibt den typdezuweisung an, der von einer vorlagenstub-Funktion verwendet werden soll.
ms.assetid: 52e6235d-90e6-4559-b17c-14ca3be896ff
title: operationenzuordcator-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c214b5dbc3245f63797c55880fe052d5c3ced15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358923"
---
# <a name="operationdeallocator-element"></a><span data-ttu-id="fd3ab-103">operationenzuordcator-Element</span><span class="sxs-lookup"><span data-stu-id="fd3ab-103">operationDeallocator element</span></span>

<span data-ttu-id="fd3ab-104">Gibt den typdezuweisung an, der von der Stub-Funktion eines Vorgangs verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="fd3ab-104">Specifies the type deallocator to be used by an operation's stub function.</span></span>

## <a name="usage"></a><span data-ttu-id="fd3ab-105">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="fd3ab-105">Usage</span></span>

``` syntax
<operationDeallocator
  operation = "character_string"
  deallocator = "character_string"/>
```

## <a name="attributes"></a><span data-ttu-id="fd3ab-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="fd3ab-106">Attributes</span></span>



| <span data-ttu-id="fd3ab-107">Attribut</span><span class="sxs-lookup"><span data-stu-id="fd3ab-107">Attribute</span></span>                  | <span data-ttu-id="fd3ab-108">type</span><span class="sxs-lookup"><span data-stu-id="fd3ab-108">Type</span></span>                         | <span data-ttu-id="fd3ab-109">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="fd3ab-109">Required</span></span>       | <span data-ttu-id="fd3ab-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fd3ab-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------------------|------------------------------|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd3ab-111">**deallokator**</span><span class="sxs-lookup"><span data-stu-id="fd3ab-111">**deallocator**</span></span><br/> | <span data-ttu-id="fd3ab-112">Zeichen \_ Folge</span><span class="sxs-lookup"><span data-stu-id="fd3ab-112">character\_string</span></span><br/> | <span data-ttu-id="fd3ab-113">Ja</span><span class="sxs-lookup"><span data-stu-id="fd3ab-113">Yes</span></span><br/> | <span data-ttu-id="fd3ab-114">Der für den Vorgang zu verwendende dezuweiser.</span><span class="sxs-lookup"><span data-stu-id="fd3ab-114">The deallocator to use for the operation.</span></span><br/> <br/> <span data-ttu-id="fd3ab-115">Die folgenden Zeichen folgen sind gültige Werte.</span><span class="sxs-lookup"><span data-stu-id="fd3ab-115">The following strings are valid values.</span></span><br/> <br/> <dl><span data-ttu-id="fd3ab-116"><span id="none"></span><span id="NONE"></span><dt>\* \* \* \* keine *</dt> <span id="WSDFreeLinkedMemory"></span> <span id="wsdfreelinkedmemory"></span> <span id="WSDFREELINKEDMEMORY"></span> \* \* \* <dt>* \* \* \* Wsdfreelinkedmemory \* *</dt> <span id="CoTaskMemFree"></span> <span id="cotaskmemfree"></span> <span id="COTASKMEMFREE"></span> \* \* <dt>* \* \* \* CoTaskMemFree \* \* \* *</dt> <span id="free"></span> <span id="FREE"></span> <dt>* \* \* \* Free \* \* \* *</dt> <span id="delete"></span> <span id="DELETE"></span> <dt>* \* \* \* Delete \* \* \* *</dt> <span id="deleteArray"></span> <span id="deletearray"></span> <span id="DELETEARRAY"></span> <dt>* \* \* \* deletearray \* \* \* *</dt> <span id="Release"></span> <span id="release"></span> <span id="RELEASE"></span> <dt>* \* \* \* Release \* \* \*</dt> \*</span><span class="sxs-lookup"><span data-stu-id="fd3ab-116"><span id="none"></span><span id="NONE"></span><dt>\*\*\*\*none\*\*\*\*</dt><span id="WSDFreeLinkedMemory"></span><span id="wsdfreelinkedmemory"></span><span id="WSDFREELINKEDMEMORY"></span><dt>\*\*\*\*WSDFreeLinkedMemory\*\*\*\*</dt><span id="CoTaskMemFree"></span><span id="cotaskmemfree"></span><span id="COTASKMEMFREE"></span><dt>\*\*\*\*CoTaskMemFree\*\*\*\*</dt><span id="free"></span><span id="FREE"></span><dt>\*\*\*\*free\*\*\*\*</dt><span id="delete"></span><span id="DELETE"></span><dt>\*\*\*\*delete\*\*\*\*</dt><span id="deleteArray"></span><span id="deletearray"></span><span id="DELETEARRAY"></span><dt>\*\*\*\*deleteArray\*\*\*\*</dt><span id="Release"></span><span id="release"></span><span id="RELEASE"></span><dt>\*\*\*\*Release\*\*\*\*</dt></span></span> </dl> |
| <span data-ttu-id="fd3ab-117">**operation**</span><span class="sxs-lookup"><span data-stu-id="fd3ab-117">**operation**</span></span><br/>   | <span data-ttu-id="fd3ab-118">Zeichen \_ Folge</span><span class="sxs-lookup"><span data-stu-id="fd3ab-118">character\_string</span></span><br/> | <span data-ttu-id="fd3ab-119">Ja</span><span class="sxs-lookup"><span data-stu-id="fd3ab-119">Yes</span></span><br/> | <span data-ttu-id="fd3ab-120">Der Name des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="fd3ab-120">The name of the operation.</span></span><br/> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



## <a name="child-elements"></a><span data-ttu-id="fd3ab-121">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fd3ab-121">Child elements</span></span>

<span data-ttu-id="fd3ab-122">Es gibt keine untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="fd3ab-122">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="fd3ab-123">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fd3ab-123">Parent elements</span></span>



| <span data-ttu-id="fd3ab-124">Element</span><span class="sxs-lookup"><span data-stu-id="fd3ab-124">Element</span></span>                                               | <span data-ttu-id="fd3ab-125">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fd3ab-125">Description</span></span>                                                                                   |
|-------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fd3ab-126">**stubdefinitionen**</span><span class="sxs-lookup"><span data-stu-id="fd3ab-126">**stubDefinitions**</span></span>](stubdefinitions.md)<br/> | <span data-ttu-id="fd3ab-127">Generiert Implementierungen für Stub-Funktionen für Porttyp Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="fd3ab-127">Generates implementations for stub functions for port type operations.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="fd3ab-128">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="fd3ab-128">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="fd3ab-129">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="fd3ab-129">Minimum supported system</span></span><br/> | <span data-ttu-id="fd3ab-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fd3ab-130">Windows Vista</span></span> |
| <span data-ttu-id="fd3ab-131">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="fd3ab-131">Can be empty</span></span>                        | <span data-ttu-id="fd3ab-132">Ja</span><span class="sxs-lookup"><span data-stu-id="fd3ab-132">Yes</span></span>           |



 

 




