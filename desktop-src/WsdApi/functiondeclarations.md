---
description: Generiert Implementierungsdeklarationen für Proxyfunktionen für Porttypvorgänge.
ms.assetid: 6ba7dbb6-6598-4569-97e1-d703e4b896c7
title: functionDeclarations-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 508cbac6d220c0ebdee0c6306d5f8a8ab5f26770
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998817"
---
# <a name="functiondeclarations-element"></a><span data-ttu-id="05a3e-103">functionDeclarations-Element</span><span class="sxs-lookup"><span data-stu-id="05a3e-103">functionDeclarations element</span></span>

<span data-ttu-id="05a3e-104">Generiert Implementierungsdeklarationen für Proxyfunktionen für Porttypvorgänge.</span><span class="sxs-lookup"><span data-stu-id="05a3e-104">Generates implementation declarations for proxy functions for port type operations.</span></span>

## <a name="usage"></a><span data-ttu-id="05a3e-105">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="05a3e-105">Usage</span></span>

``` syntax
<functionDeclarations>
  child elements
</functionDeclarations>
```

## <a name="attributes"></a><span data-ttu-id="05a3e-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="05a3e-106">Attributes</span></span>

<span data-ttu-id="05a3e-107">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="05a3e-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="05a3e-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="05a3e-108">Child elements</span></span>



| <span data-ttu-id="05a3e-109">Element</span><span class="sxs-lookup"><span data-stu-id="05a3e-109">Element</span></span>                                   | <span data-ttu-id="05a3e-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="05a3e-110">Description</span></span>                                                                                                             |
|-------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="05a3e-111">**async**</span><span class="sxs-lookup"><span data-stu-id="05a3e-111">**async**</span></span>](async.md)<br/>         | <span data-ttu-id="05a3e-112">Gibt an, ob asynchrone Vorgänge in den generierten Proxyfunktionen enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="05a3e-112">Specifies whether asynchronous operations are included in the generated proxy functions.</span></span><br/> <br/>         |
| [<span data-ttu-id="05a3e-113">**Ereignisse**</span><span class="sxs-lookup"><span data-stu-id="05a3e-113">**events**</span></span>](events.md)<br/>       | <span data-ttu-id="05a3e-114">Gibt an, ob verwandte Ereignisse in den generierten Funktionen enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="05a3e-114">Specifies whether related events are included in the generated functions.</span></span><br/> <br/>                        |
| [<span data-ttu-id="05a3e-115">**faultInfo**</span><span class="sxs-lookup"><span data-stu-id="05a3e-115">**faultInfo**</span></span>](faultinfo.md)<br/> | <span data-ttu-id="05a3e-116">Gibt an, ob Parameter, die zum Übergeben von Fehlerinformationen verwendet werden, in generierten Funktionen enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="05a3e-116">Specifies whether parameters used to pass fault information are included in generated functions.</span></span><br/> <br/> |
| [<span data-ttu-id="05a3e-117">**Vorgang**</span><span class="sxs-lookup"><span data-stu-id="05a3e-117">**operation**</span></span>](operation.md)<br/> | <span data-ttu-id="05a3e-118">Gibt einen Vorgang an, für den Code generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="05a3e-118">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                                        |
| [<span data-ttu-id="05a3e-119">**Porttype**</span><span class="sxs-lookup"><span data-stu-id="05a3e-119">**portType**</span></span>](porttype.md)<br/>   | <span data-ttu-id="05a3e-120">Gibt den Porttyp an, für den Code generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="05a3e-120">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                                       |



### <a name="child-element-sequence"></a><span data-ttu-id="05a3e-121">Sequenz untergeordneter Elemente</span><span class="sxs-lookup"><span data-stu-id="05a3e-121">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  events?, 
  async?, 
  faultInfo?
)
```

## <a name="parent-elements"></a><span data-ttu-id="05a3e-122">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="05a3e-122">Parent elements</span></span>



| <span data-ttu-id="05a3e-123">Element</span><span class="sxs-lookup"><span data-stu-id="05a3e-123">Element</span></span>                         | <span data-ttu-id="05a3e-124">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="05a3e-124">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="05a3e-125">**Datei**</span><span class="sxs-lookup"><span data-stu-id="05a3e-125">**file**</span></span>](file.md)<br/> | <span data-ttu-id="05a3e-126">Gibt eine Datei aus dem Codegenerator aus.</span><span class="sxs-lookup"><span data-stu-id="05a3e-126">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="05a3e-127">Hinweise</span><span class="sxs-lookup"><span data-stu-id="05a3e-127">Remarks</span></span>

<span data-ttu-id="05a3e-128">Dieses Element generiert Deklarationen von Memberfunktionen, die vorgängen entsprechen, die vom Vertrag aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="05a3e-128">This element generates declarations of member functions corresponding to operations called out by the contract.</span></span> <span data-ttu-id="05a3e-129">Diese Deklarationen sind in einer Form, die für die Verwendung durch einen C++-Compiler geeignet ist, und werden im Allgemeinen in CPP-Dateien verwendet.</span><span class="sxs-lookup"><span data-stu-id="05a3e-129">These declarations are in a form appropriate for consumption by a C++ compiler and are generally used in .cpp files.</span></span>

<span data-ttu-id="05a3e-130">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="05a3e-130">Example:</span></span>

``` syntax
<functionDeclarations events = "true"/>
```

## <a name="element-information"></a><span data-ttu-id="05a3e-131">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="05a3e-131">Element information</span></span>



| <span data-ttu-id="05a3e-132">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="05a3e-132">Label</span></span> | <span data-ttu-id="05a3e-133">Wert</span><span class="sxs-lookup"><span data-stu-id="05a3e-133">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="05a3e-134">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="05a3e-134">Minimum supported system</span></span><br/> | <span data-ttu-id="05a3e-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="05a3e-135">Windows Vista</span></span> |
| <span data-ttu-id="05a3e-136">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="05a3e-136">Can be empty</span></span>                        | <span data-ttu-id="05a3e-137">Ja</span><span class="sxs-lookup"><span data-stu-id="05a3e-137">Yes</span></span>           |



 

 




