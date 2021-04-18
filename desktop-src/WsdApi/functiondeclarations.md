---
description: Generiert Implementierungs Deklarationen für Proxy Funktionen für Porttyp Vorgänge.
ms.assetid: 6ba7dbb6-6598-4569-97e1-d703e4b896c7
title: functiondeklarationen-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b82aca30f94fc8fcec80701a74b56e83ab674c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216168"
---
# <a name="functiondeclarations-element"></a><span data-ttu-id="6a53c-103">functiondeklarationen-Element</span><span class="sxs-lookup"><span data-stu-id="6a53c-103">functionDeclarations element</span></span>

<span data-ttu-id="6a53c-104">Generiert Implementierungs Deklarationen für Proxy Funktionen für Porttyp Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="6a53c-104">Generates implementation declarations for proxy functions for port type operations.</span></span>

## <a name="usage"></a><span data-ttu-id="6a53c-105">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="6a53c-105">Usage</span></span>

``` syntax
<functionDeclarations>
  child elements
</functionDeclarations>
```

## <a name="attributes"></a><span data-ttu-id="6a53c-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="6a53c-106">Attributes</span></span>

<span data-ttu-id="6a53c-107">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="6a53c-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="6a53c-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6a53c-108">Child elements</span></span>



| <span data-ttu-id="6a53c-109">Element</span><span class="sxs-lookup"><span data-stu-id="6a53c-109">Element</span></span>                                   | <span data-ttu-id="6a53c-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6a53c-110">Description</span></span>                                                                                                             |
|-------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6a53c-111">**async**</span><span class="sxs-lookup"><span data-stu-id="6a53c-111">**async**</span></span>](async.md)<br/>         | <span data-ttu-id="6a53c-112">Gibt an, ob asynchrone Vorgänge in den generierten Proxy Funktionen enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="6a53c-112">Specifies whether asynchronous operations are included in the generated proxy functions.</span></span><br/> <br/>         |
| [<span data-ttu-id="6a53c-113">**Fall**</span><span class="sxs-lookup"><span data-stu-id="6a53c-113">**events**</span></span>](events.md)<br/>       | <span data-ttu-id="6a53c-114">Gibt an, ob verwandte Ereignisse in den generierten Funktionen enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="6a53c-114">Specifies whether related events are included in the generated functions.</span></span><br/> <br/>                        |
| [<span data-ttu-id="6a53c-115">**faultinfo**</span><span class="sxs-lookup"><span data-stu-id="6a53c-115">**faultInfo**</span></span>](faultinfo.md)<br/> | <span data-ttu-id="6a53c-116">Gibt an, ob Parameter, die zum Übergeben von Fehlerinformationen verwendet werden, in generierte Funktionen eingeschlossen werden</span><span class="sxs-lookup"><span data-stu-id="6a53c-116">Specifies whether parameters used to pass fault information are included in generated functions.</span></span><br/> <br/> |
| [<span data-ttu-id="6a53c-117">**Betriebs**</span><span class="sxs-lookup"><span data-stu-id="6a53c-117">**operation**</span></span>](operation.md)<br/> | <span data-ttu-id="6a53c-118">Gibt einen Vorgang an, für den Code generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="6a53c-118">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                                        |
| [<span data-ttu-id="6a53c-119">**PortType**</span><span class="sxs-lookup"><span data-stu-id="6a53c-119">**portType**</span></span>](porttype.md)<br/>   | <span data-ttu-id="6a53c-120">Gibt den Porttyp an, für den Code generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="6a53c-120">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                                       |



### <a name="child-element-sequence"></a><span data-ttu-id="6a53c-121">Sequenz untergeordneter Elemente</span><span class="sxs-lookup"><span data-stu-id="6a53c-121">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  events?, 
  async?, 
  faultInfo?
)
```

## <a name="parent-elements"></a><span data-ttu-id="6a53c-122">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6a53c-122">Parent elements</span></span>



| <span data-ttu-id="6a53c-123">Element</span><span class="sxs-lookup"><span data-stu-id="6a53c-123">Element</span></span>                         | <span data-ttu-id="6a53c-124">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6a53c-124">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="6a53c-125">**Datei**</span><span class="sxs-lookup"><span data-stu-id="6a53c-125">**file**</span></span>](file.md)<br/> | <span data-ttu-id="6a53c-126">Gibt eine Datei aus dem Code-Generator aus.</span><span class="sxs-lookup"><span data-stu-id="6a53c-126">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="6a53c-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6a53c-127">Remarks</span></span>

<span data-ttu-id="6a53c-128">Dieses Element generiert Deklarationen von Element Funktionen, die den Vorgängen entsprechen, die durch den Vertrag aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="6a53c-128">This element generates declarations of member functions corresponding to operations called out by the contract.</span></span> <span data-ttu-id="6a53c-129">Diese Deklarationen sind in einer für die Verwendung durch einen C++-Compiler geeigneten Form und werden im Allgemeinen in cpp-Dateien verwendet.</span><span class="sxs-lookup"><span data-stu-id="6a53c-129">These declarations are in a form appropriate for consumption by a C++ compiler and are generally used in .cpp files.</span></span>

<span data-ttu-id="6a53c-130">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="6a53c-130">Example:</span></span>

``` syntax
<functionDeclarations events = "true"/>
```

## <a name="element-information"></a><span data-ttu-id="6a53c-131">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="6a53c-131">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="6a53c-132">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="6a53c-132">Minimum supported system</span></span><br/> | <span data-ttu-id="6a53c-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6a53c-133">Windows Vista</span></span> |
| <span data-ttu-id="6a53c-134">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="6a53c-134">Can be empty</span></span>                        | <span data-ttu-id="6a53c-135">Ja</span><span class="sxs-lookup"><span data-stu-id="6a53c-135">Yes</span></span>           |



 

 




