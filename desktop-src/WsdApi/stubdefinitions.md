---
description: Generiert Implementierungen für Stubfunktionen für Porttypvorgänge.
ms.assetid: 69899302-db54-493b-90de-596750be566f
title: stubDefinitions-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42c60b071c901538122751f6e92cfd7049f7be88
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994687"
---
# <a name="stubdefinitions-element"></a><span data-ttu-id="ea1ae-103">stubDefinitions-Element</span><span class="sxs-lookup"><span data-stu-id="ea1ae-103">stubDefinitions element</span></span>

<span data-ttu-id="ea1ae-104">Generiert Implementierungen für Stubfunktionen für Porttypvorgänge.</span><span class="sxs-lookup"><span data-stu-id="ea1ae-104">Generates implementations for stub functions for port-type operations.</span></span>

## <a name="usage"></a><span data-ttu-id="ea1ae-105">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="ea1ae-105">Usage</span></span>

``` syntax
<stubDefinitions>
  child elements
</stubDefinitions>
```

## <a name="attributes"></a><span data-ttu-id="ea1ae-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="ea1ae-106">Attributes</span></span>

<span data-ttu-id="ea1ae-107">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="ea1ae-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="ea1ae-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ea1ae-108">Child elements</span></span>



| <span data-ttu-id="ea1ae-109">Element</span><span class="sxs-lookup"><span data-stu-id="ea1ae-109">Element</span></span>                                                         | <span data-ttu-id="ea1ae-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ea1ae-110">Description</span></span>                                                                                                             |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ea1ae-111">**Deallocator**</span><span class="sxs-lookup"><span data-stu-id="ea1ae-111">**deallocator**</span></span>](deallocator.md)<br/>                   | <span data-ttu-id="ea1ae-112">Gibt den Typ des Deallocators an, der von einer Stubfunktion verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ea1ae-112">Specifies the type of deallocator to be used by a stub function.</span></span><br/> <br/>                                 |
| [<span data-ttu-id="ea1ae-113">**eventArg**</span><span class="sxs-lookup"><span data-stu-id="ea1ae-113">**eventArg**</span></span>](eventarg.md)<br/>                         | <span data-ttu-id="ea1ae-114">Gibt an, ob verwandte Ereignisargumente in den generierten Funktionen enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="ea1ae-114">Specifies whether related event arguments are included in the generated functions.</span></span><br/> <br/>               |
| [<span data-ttu-id="ea1ae-115">**Ereignisse**</span><span class="sxs-lookup"><span data-stu-id="ea1ae-115">**events**</span></span>](events.md)<br/>                             | <span data-ttu-id="ea1ae-116">Gibt an, ob verwandte Ereignisse in den generierten Funktionen enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="ea1ae-116">Specifies whether related events are included in the generated functions.</span></span><br/> <br/>                        |
| [<span data-ttu-id="ea1ae-117">**faultInfo**</span><span class="sxs-lookup"><span data-stu-id="ea1ae-117">**faultInfo**</span></span>](faultinfo.md)<br/>                       | <span data-ttu-id="ea1ae-118">Gibt an, ob Parameter, die zum Übergeben von Fehlerinformationen verwendet werden, in generierten Funktionen enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="ea1ae-118">Specifies whether parameters used to pass fault information are included in generated functions.</span></span><br/> <br/> |
| [<span data-ttu-id="ea1ae-119">**Vorgang**</span><span class="sxs-lookup"><span data-stu-id="ea1ae-119">**operation**</span></span>](operation.md)<br/>                       | <span data-ttu-id="ea1ae-120">Gibt einen Vorgang an, für den Code generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="ea1ae-120">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                                        |
| [<span data-ttu-id="ea1ae-121">**operationDeallocator**</span><span class="sxs-lookup"><span data-stu-id="ea1ae-121">**operationDeallocator**</span></span>](operationdeallocator.md)<br/> | <span data-ttu-id="ea1ae-122">Gibt den Typ des Deallocators an, der von der Stubfunktion eines Vorgangs verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ea1ae-122">Specifies the type of deallocator to be used by an operation's stub function.</span></span><br/> <br/>                    |
| [<span data-ttu-id="ea1ae-123">**Porttype**</span><span class="sxs-lookup"><span data-stu-id="ea1ae-123">**portType**</span></span>](porttype.md)<br/>                         | <span data-ttu-id="ea1ae-124">Gibt den Porttyp an, für den Code generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="ea1ae-124">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                                       |
| [<span data-ttu-id="ea1ae-125">**serverClass**</span><span class="sxs-lookup"><span data-stu-id="ea1ae-125">**serverClass**</span></span>](serverclass.md)<br/>                   | <span data-ttu-id="ea1ae-126">Gibt den Namen der hostseitigen Serverklasse an.</span><span class="sxs-lookup"><span data-stu-id="ea1ae-126">Specifies the name of the host-side server class.</span></span><br/> <br/>                                                |



### <a name="child-element-sequence"></a><span data-ttu-id="ea1ae-127">Sequenz untergeordneter Elemente</span><span class="sxs-lookup"><span data-stu-id="ea1ae-127">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  serverClass, 
  eventArg?, 
  events?, 
  operationDeallocator*, 
  deallocator?, 
  faultInfo?
)
```

## <a name="parent-elements"></a><span data-ttu-id="ea1ae-128">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ea1ae-128">Parent elements</span></span>



| <span data-ttu-id="ea1ae-129">Element</span><span class="sxs-lookup"><span data-stu-id="ea1ae-129">Element</span></span>                         | <span data-ttu-id="ea1ae-130">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ea1ae-130">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="ea1ae-131">**Datei**</span><span class="sxs-lookup"><span data-stu-id="ea1ae-131">**file**</span></span>](file.md)<br/> | <span data-ttu-id="ea1ae-132">Gibt eine Datei aus dem Codegenerator aus.</span><span class="sxs-lookup"><span data-stu-id="ea1ae-132">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="ea1ae-133">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="ea1ae-133">Element information</span></span>



| <span data-ttu-id="ea1ae-134">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="ea1ae-134">Label</span></span> | <span data-ttu-id="ea1ae-135">Wert</span><span class="sxs-lookup"><span data-stu-id="ea1ae-135">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="ea1ae-136">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="ea1ae-136">Minimum supported system</span></span><br/> | <span data-ttu-id="ea1ae-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ea1ae-137">Windows Vista</span></span> |
| <span data-ttu-id="ea1ae-138">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="ea1ae-138">Can be empty</span></span>                        | <span data-ttu-id="ea1ae-139">Nein</span><span class="sxs-lookup"><span data-stu-id="ea1ae-139">No</span></span>            |



 

 




