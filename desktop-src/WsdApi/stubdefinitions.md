---
description: Generiert Implementierungen für Stub-Funktionen für Porttyp Vorgänge.
ms.assetid: 69899302-db54-493b-90de-596750be566f
title: stubdefinitions-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6676cfc6cf55aa9c9961bd614506500d847def0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347620"
---
# <a name="stubdefinitions-element"></a><span data-ttu-id="080a8-103">stubdefinitions-Element</span><span class="sxs-lookup"><span data-stu-id="080a8-103">stubDefinitions element</span></span>

<span data-ttu-id="080a8-104">Generiert Implementierungen für Stub-Funktionen für Porttyp Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="080a8-104">Generates implementations for stub functions for port-type operations.</span></span>

## <a name="usage"></a><span data-ttu-id="080a8-105">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="080a8-105">Usage</span></span>

``` syntax
<stubDefinitions>
  child elements
</stubDefinitions>
```

## <a name="attributes"></a><span data-ttu-id="080a8-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="080a8-106">Attributes</span></span>

<span data-ttu-id="080a8-107">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="080a8-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="080a8-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="080a8-108">Child elements</span></span>



| <span data-ttu-id="080a8-109">Element</span><span class="sxs-lookup"><span data-stu-id="080a8-109">Element</span></span>                                                         | <span data-ttu-id="080a8-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="080a8-110">Description</span></span>                                                                                                             |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="080a8-111">**deallokator**</span><span class="sxs-lookup"><span data-stu-id="080a8-111">**deallocator**</span></span>](deallocator.md)<br/>                   | <span data-ttu-id="080a8-112">Gibt den Typ der dezuweisung an, der von einer stubfunktion verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="080a8-112">Specifies the type of deallocator to be used by a stub function.</span></span><br/> <br/>                                 |
| [<span data-ttu-id="080a8-113">**EventArg**</span><span class="sxs-lookup"><span data-stu-id="080a8-113">**eventArg**</span></span>](eventarg.md)<br/>                         | <span data-ttu-id="080a8-114">Gibt an, ob Verwandte Ereignis Argumente in den generierten Funktionen enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="080a8-114">Specifies whether related event arguments are included in the generated functions.</span></span><br/> <br/>               |
| [<span data-ttu-id="080a8-115">**Fall**</span><span class="sxs-lookup"><span data-stu-id="080a8-115">**events**</span></span>](events.md)<br/>                             | <span data-ttu-id="080a8-116">Gibt an, ob verwandte Ereignisse in den generierten Funktionen enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="080a8-116">Specifies whether related events are included in the generated functions.</span></span><br/> <br/>                        |
| [<span data-ttu-id="080a8-117">**faultinfo**</span><span class="sxs-lookup"><span data-stu-id="080a8-117">**faultInfo**</span></span>](faultinfo.md)<br/>                       | <span data-ttu-id="080a8-118">Gibt an, ob Parameter, die zum Übergeben von Fehlerinformationen verwendet werden, in generierte Funktionen eingeschlossen werden</span><span class="sxs-lookup"><span data-stu-id="080a8-118">Specifies whether parameters used to pass fault information are included in generated functions.</span></span><br/> <br/> |
| [<span data-ttu-id="080a8-119">**Betriebs**</span><span class="sxs-lookup"><span data-stu-id="080a8-119">**operation**</span></span>](operation.md)<br/>                       | <span data-ttu-id="080a8-120">Gibt einen Vorgang an, für den Code generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="080a8-120">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                                        |
| [<span data-ttu-id="080a8-121">**operationentzuordcator**</span><span class="sxs-lookup"><span data-stu-id="080a8-121">**operationDeallocator**</span></span>](operationdeallocator.md)<br/> | <span data-ttu-id="080a8-122">Gibt den Typ der dezuweisung an, der von der Stub-Funktion eines Vorgangs verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="080a8-122">Specifies the type of deallocator to be used by an operation's stub function.</span></span><br/> <br/>                    |
| [<span data-ttu-id="080a8-123">**PortType**</span><span class="sxs-lookup"><span data-stu-id="080a8-123">**portType**</span></span>](porttype.md)<br/>                         | <span data-ttu-id="080a8-124">Gibt den Porttyp an, für den Code generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="080a8-124">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                                       |
| [<span data-ttu-id="080a8-125">**Server Class**</span><span class="sxs-lookup"><span data-stu-id="080a8-125">**serverClass**</span></span>](serverclass.md)<br/>                   | <span data-ttu-id="080a8-126">Gibt den Namen der Host seitigen Serverklasse an.</span><span class="sxs-lookup"><span data-stu-id="080a8-126">Specifies the name of the host-side server class.</span></span><br/> <br/>                                                |



### <a name="child-element-sequence"></a><span data-ttu-id="080a8-127">Sequenz untergeordneter Elemente</span><span class="sxs-lookup"><span data-stu-id="080a8-127">Child element sequence</span></span>

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

## <a name="parent-elements"></a><span data-ttu-id="080a8-128">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="080a8-128">Parent elements</span></span>



| <span data-ttu-id="080a8-129">Element</span><span class="sxs-lookup"><span data-stu-id="080a8-129">Element</span></span>                         | <span data-ttu-id="080a8-130">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="080a8-130">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="080a8-131">**Datei**</span><span class="sxs-lookup"><span data-stu-id="080a8-131">**file**</span></span>](file.md)<br/> | <span data-ttu-id="080a8-132">Gibt eine Datei aus dem Code-Generator aus.</span><span class="sxs-lookup"><span data-stu-id="080a8-132">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="080a8-133">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="080a8-133">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="080a8-134">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="080a8-134">Minimum supported system</span></span><br/> | <span data-ttu-id="080a8-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="080a8-135">Windows Vista</span></span> |
| <span data-ttu-id="080a8-136">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="080a8-136">Can be empty</span></span>                        | <span data-ttu-id="080a8-137">Nein</span><span class="sxs-lookup"><span data-stu-id="080a8-137">No</span></span>            |



 

 




