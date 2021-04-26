---
description: Generiert IDL-Deklarationen für Proxyfunktionen für Porttypvorgänge.
ms.assetid: e56fdd68-b72d-4167-9e4c-b5bbf103880b
title: idlFunctionDeclarations-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf4d1648ac6d9c3ac6900826ebe90a64418822b6
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994737"
---
# <a name="idlfunctiondeclarations-element"></a><span data-ttu-id="5f57d-103">idlFunctionDeclarations-Element</span><span class="sxs-lookup"><span data-stu-id="5f57d-103">idlFunctionDeclarations element</span></span>

<span data-ttu-id="5f57d-104">Generiert IDL-Deklarationen für Proxyfunktionen für Porttypvorgänge.</span><span class="sxs-lookup"><span data-stu-id="5f57d-104">Generates IDL declarations for proxy functions for port type operations.</span></span>

## <a name="usage"></a><span data-ttu-id="5f57d-105">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="5f57d-105">Usage</span></span>

``` syntax
<idlFunctionDeclarations>
  child elements
</idlFunctionDeclarations>
```

## <a name="attributes"></a><span data-ttu-id="5f57d-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="5f57d-106">Attributes</span></span>

<span data-ttu-id="5f57d-107">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="5f57d-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="5f57d-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5f57d-108">Child elements</span></span>



| <span data-ttu-id="5f57d-109">Element</span><span class="sxs-lookup"><span data-stu-id="5f57d-109">Element</span></span>                                   | <span data-ttu-id="5f57d-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5f57d-110">Description</span></span>                                                                                                             |
|-------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5f57d-111">**async**</span><span class="sxs-lookup"><span data-stu-id="5f57d-111">**async**</span></span>](async.md)<br/>         | <span data-ttu-id="5f57d-112">Gibt an, ob asynchrone Vorgänge in den generierten Proxyfunktionen enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="5f57d-112">Specifies whether asynchronous operations are included in the generated proxy functions.</span></span><br/> <br/>         |
| [<span data-ttu-id="5f57d-113">**eventArg**</span><span class="sxs-lookup"><span data-stu-id="5f57d-113">**eventArg**</span></span>](eventarg.md)<br/>   | <span data-ttu-id="5f57d-114">Gibt an, ob verwandte Ereignisargumente in den generierten Funktionen enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="5f57d-114">Specifies whether related event arguments are included in the generated functions.</span></span><br/> <br/>               |
| [<span data-ttu-id="5f57d-115">**Ereignisse**</span><span class="sxs-lookup"><span data-stu-id="5f57d-115">**events**</span></span>](events.md)<br/>       | <span data-ttu-id="5f57d-116">Gibt an, ob verwandte Ereignisse in den generierten Funktionen enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="5f57d-116">Specifies whether related events are included in the generated functions.</span></span><br/> <br/>                        |
| [<span data-ttu-id="5f57d-117">**faultInfo**</span><span class="sxs-lookup"><span data-stu-id="5f57d-117">**faultInfo**</span></span>](faultinfo.md)<br/> | <span data-ttu-id="5f57d-118">Gibt an, ob Parameter, die zum Übergeben von Fehlerinformationen verwendet werden, in generierten Funktionen enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="5f57d-118">Specifies whether parameters used to pass fault information are included in generated functions.</span></span><br/> <br/> |
| [<span data-ttu-id="5f57d-119">**Vorgang**</span><span class="sxs-lookup"><span data-stu-id="5f57d-119">**operation**</span></span>](operation.md)<br/> | <span data-ttu-id="5f57d-120">Gibt einen Vorgang an, für den Code generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="5f57d-120">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                                        |
| [<span data-ttu-id="5f57d-121">**Porttype**</span><span class="sxs-lookup"><span data-stu-id="5f57d-121">**portType**</span></span>](porttype.md)<br/>   | <span data-ttu-id="5f57d-122">Gibt den Porttyp an, für den Code generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="5f57d-122">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                                       |



### <a name="child-element-sequence"></a><span data-ttu-id="5f57d-123">Sequenz untergeordneter Elemente</span><span class="sxs-lookup"><span data-stu-id="5f57d-123">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  eventArg?, 
  events?, 
  async?, 
  faultInfo?
)
```

## <a name="parent-elements"></a><span data-ttu-id="5f57d-124">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5f57d-124">Parent elements</span></span>



| <span data-ttu-id="5f57d-125">Element</span><span class="sxs-lookup"><span data-stu-id="5f57d-125">Element</span></span>                         | <span data-ttu-id="5f57d-126">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5f57d-126">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="5f57d-127">**Datei**</span><span class="sxs-lookup"><span data-stu-id="5f57d-127">**file**</span></span>](file.md)<br/> | <span data-ttu-id="5f57d-128">Gibt eine Datei aus dem Codegenerator aus.</span><span class="sxs-lookup"><span data-stu-id="5f57d-128">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="5f57d-129">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5f57d-129">Remarks</span></span>

<span data-ttu-id="5f57d-130">Dieses Element generiert Deklarationen von Memberfunktionen, die vorgängen entsprechen, die vom Vertrag aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="5f57d-130">This element generates declarations of member functions corresponding to operations called out by the contract.</span></span> <span data-ttu-id="5f57d-131">Diese Deklarationen sind in einer Für den MIDL-Compiler geeigneten Form und werden im Allgemeinen in IDL-Dateien verwendet.</span><span class="sxs-lookup"><span data-stu-id="5f57d-131">These declarations are in a form appropriate for consumption by the MIDL compiler and are generally used in .idl files.</span></span>

<span data-ttu-id="5f57d-132">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="5f57d-132">Example:</span></span>

``` syntax
<idlFunctionDeclarations events = "true"/>
```

## <a name="element-information"></a><span data-ttu-id="5f57d-133">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="5f57d-133">Element information</span></span>



| <span data-ttu-id="5f57d-134">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="5f57d-134">Label</span></span> | <span data-ttu-id="5f57d-135">Wert</span><span class="sxs-lookup"><span data-stu-id="5f57d-135">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="5f57d-136">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="5f57d-136">Minimum supported system</span></span><br/> | <span data-ttu-id="5f57d-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5f57d-137">Windows Vista</span></span> |
| <span data-ttu-id="5f57d-138">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="5f57d-138">Can be empty</span></span>                        | <span data-ttu-id="5f57d-139">Ja</span><span class="sxs-lookup"><span data-stu-id="5f57d-139">Yes</span></span>           |



 

 




