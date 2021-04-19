---
description: Generiert IDL-Deklarationen für Proxy Funktionen für Porttyp Vorgänge.
ms.assetid: e56fdd68-b72d-4167-9e4c-b5bbf103880b
title: idlfunction-Deklarationen-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1afa43676898231f739804185b8bf5d6e2b4faf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358816"
---
# <a name="idlfunctiondeclarations-element"></a><span data-ttu-id="cc186-103">idlfunction-Deklarationen-Element</span><span class="sxs-lookup"><span data-stu-id="cc186-103">idlFunctionDeclarations element</span></span>

<span data-ttu-id="cc186-104">Generiert IDL-Deklarationen für Proxy Funktionen für Porttyp Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="cc186-104">Generates IDL declarations for proxy functions for port type operations.</span></span>

## <a name="usage"></a><span data-ttu-id="cc186-105">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="cc186-105">Usage</span></span>

``` syntax
<idlFunctionDeclarations>
  child elements
</idlFunctionDeclarations>
```

## <a name="attributes"></a><span data-ttu-id="cc186-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="cc186-106">Attributes</span></span>

<span data-ttu-id="cc186-107">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="cc186-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="cc186-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cc186-108">Child elements</span></span>



| <span data-ttu-id="cc186-109">Element</span><span class="sxs-lookup"><span data-stu-id="cc186-109">Element</span></span>                                   | <span data-ttu-id="cc186-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cc186-110">Description</span></span>                                                                                                             |
|-------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cc186-111">**async**</span><span class="sxs-lookup"><span data-stu-id="cc186-111">**async**</span></span>](async.md)<br/>         | <span data-ttu-id="cc186-112">Gibt an, ob asynchrone Vorgänge in den generierten Proxy Funktionen enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="cc186-112">Specifies whether asynchronous operations are included in the generated proxy functions.</span></span><br/> <br/>         |
| [<span data-ttu-id="cc186-113">**EventArg**</span><span class="sxs-lookup"><span data-stu-id="cc186-113">**eventArg**</span></span>](eventarg.md)<br/>   | <span data-ttu-id="cc186-114">Gibt an, ob Verwandte Ereignis Argumente in den generierten Funktionen enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="cc186-114">Specifies whether related event arguments are included in the generated functions.</span></span><br/> <br/>               |
| [<span data-ttu-id="cc186-115">**Fall**</span><span class="sxs-lookup"><span data-stu-id="cc186-115">**events**</span></span>](events.md)<br/>       | <span data-ttu-id="cc186-116">Gibt an, ob verwandte Ereignisse in den generierten Funktionen enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="cc186-116">Specifies whether related events are included in the generated functions.</span></span><br/> <br/>                        |
| [<span data-ttu-id="cc186-117">**faultinfo**</span><span class="sxs-lookup"><span data-stu-id="cc186-117">**faultInfo**</span></span>](faultinfo.md)<br/> | <span data-ttu-id="cc186-118">Gibt an, ob Parameter, die zum Übergeben von Fehlerinformationen verwendet werden, in generierte Funktionen eingeschlossen werden</span><span class="sxs-lookup"><span data-stu-id="cc186-118">Specifies whether parameters used to pass fault information are included in generated functions.</span></span><br/> <br/> |
| [<span data-ttu-id="cc186-119">**Betriebs**</span><span class="sxs-lookup"><span data-stu-id="cc186-119">**operation**</span></span>](operation.md)<br/> | <span data-ttu-id="cc186-120">Gibt einen Vorgang an, für den Code generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="cc186-120">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                                        |
| [<span data-ttu-id="cc186-121">**PortType**</span><span class="sxs-lookup"><span data-stu-id="cc186-121">**portType**</span></span>](porttype.md)<br/>   | <span data-ttu-id="cc186-122">Gibt den Porttyp an, für den Code generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="cc186-122">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                                       |



### <a name="child-element-sequence"></a><span data-ttu-id="cc186-123">Sequenz untergeordneter Elemente</span><span class="sxs-lookup"><span data-stu-id="cc186-123">Child element sequence</span></span>

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

## <a name="parent-elements"></a><span data-ttu-id="cc186-124">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cc186-124">Parent elements</span></span>



| <span data-ttu-id="cc186-125">Element</span><span class="sxs-lookup"><span data-stu-id="cc186-125">Element</span></span>                         | <span data-ttu-id="cc186-126">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cc186-126">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="cc186-127">**Datei**</span><span class="sxs-lookup"><span data-stu-id="cc186-127">**file**</span></span>](file.md)<br/> | <span data-ttu-id="cc186-128">Gibt eine Datei aus dem Code-Generator aus.</span><span class="sxs-lookup"><span data-stu-id="cc186-128">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="cc186-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cc186-129">Remarks</span></span>

<span data-ttu-id="cc186-130">Dieses Element generiert Deklarationen von Element Funktionen, die den Vorgängen entsprechen, die durch den Vertrag aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="cc186-130">This element generates declarations of member functions corresponding to operations called out by the contract.</span></span> <span data-ttu-id="cc186-131">Diese Deklarationen sind in einer für die Verwendung durch den Mittel l-Compiler geeigneten Form und werden im Allgemeinen in IDL-Dateien verwendet.</span><span class="sxs-lookup"><span data-stu-id="cc186-131">These declarations are in a form appropriate for consumption by the MIDL compiler and are generally used in .idl files.</span></span>

<span data-ttu-id="cc186-132">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="cc186-132">Example:</span></span>

``` syntax
<idlFunctionDeclarations events = "true"/>
```

## <a name="element-information"></a><span data-ttu-id="cc186-133">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="cc186-133">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="cc186-134">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="cc186-134">Minimum supported system</span></span><br/> | <span data-ttu-id="cc186-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cc186-135">Windows Vista</span></span> |
| <span data-ttu-id="cc186-136">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="cc186-136">Can be empty</span></span>                        | <span data-ttu-id="cc186-137">Ja</span><span class="sxs-lookup"><span data-stu-id="cc186-137">Yes</span></span>           |



 

 




