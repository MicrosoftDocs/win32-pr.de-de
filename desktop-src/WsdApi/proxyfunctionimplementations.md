---
description: Generiert Implementierungen für Proxyfunktionen für Porttypvorgänge.
ms.assetid: 9505ee5f-fdb9-41b8-9537-0c5d29f90168
title: proxyFunctionImplementations-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e9f03834ca59ede41f2f3c3dff00d7dacdd54db
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995757"
---
# <a name="proxyfunctionimplementations-element"></a><span data-ttu-id="10add-103">proxyFunctionImplementations-Element</span><span class="sxs-lookup"><span data-stu-id="10add-103">proxyFunctionImplementations element</span></span>

<span data-ttu-id="10add-104">Generiert Implementierungen für Proxyfunktionen für Porttypvorgänge.</span><span class="sxs-lookup"><span data-stu-id="10add-104">Generates implementations for proxy functions for port type operations.</span></span>

## <a name="usage"></a><span data-ttu-id="10add-105">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="10add-105">Usage</span></span>

``` syntax
<proxyFunctionImplementations>
  child elements
</proxyFunctionImplementations>
```

## <a name="attributes"></a><span data-ttu-id="10add-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="10add-106">Attributes</span></span>

<span data-ttu-id="10add-107">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="10add-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="10add-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="10add-108">Child elements</span></span>



| <span data-ttu-id="10add-109">Element</span><span class="sxs-lookup"><span data-stu-id="10add-109">Element</span></span>                                     | <span data-ttu-id="10add-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="10add-110">Description</span></span>                                                                                                             |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="10add-111">**async**</span><span class="sxs-lookup"><span data-stu-id="10add-111">**async**</span></span>](async.md)<br/>           | <span data-ttu-id="10add-112">Gibt an, ob asynchrone Vorgänge in den generierten Proxyfunktionen enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="10add-112">Specifies whether asynchronous operations are included in the generated proxy functions.</span></span><br/> <br/>         |
| [<span data-ttu-id="10add-113">**Ereignisse**</span><span class="sxs-lookup"><span data-stu-id="10add-113">**events**</span></span>](events.md)<br/>         | <span data-ttu-id="10add-114">Gibt an, ob verwandte Ereignisse in den generierten Funktionen enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="10add-114">Specifies whether related events are included in the generated functions.</span></span><br/> <br/>                        |
| [<span data-ttu-id="10add-115">**faultInfo**</span><span class="sxs-lookup"><span data-stu-id="10add-115">**faultInfo**</span></span>](faultinfo.md)<br/>   | <span data-ttu-id="10add-116">Gibt an, ob Parameter, die zum Übergeben von Fehlerinformationen verwendet werden, in generierten Funktionen enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="10add-116">Specifies whether parameters used to pass fault information are included in generated functions.</span></span><br/> <br/> |
| [<span data-ttu-id="10add-117">**Vorgang**</span><span class="sxs-lookup"><span data-stu-id="10add-117">**operation**</span></span>](operation.md)<br/>   | <span data-ttu-id="10add-118">Gibt einen Vorgang an, für den Code generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="10add-118">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                                        |
| [<span data-ttu-id="10add-119">**Porttype**</span><span class="sxs-lookup"><span data-stu-id="10add-119">**portType**</span></span>](porttype.md)<br/>     | <span data-ttu-id="10add-120">Gibt den Porttyp an, für den Code generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="10add-120">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                                       |
| [<span data-ttu-id="10add-121">**proxyClass**</span><span class="sxs-lookup"><span data-stu-id="10add-121">**proxyClass**</span></span>](proxyclass.md)<br/> | <span data-ttu-id="10add-122">Gibt den Namen der clientseitigen Proxyklasse an.</span><span class="sxs-lookup"><span data-stu-id="10add-122">Specifies the name of the client-side proxy class.</span></span><br/> <br/>                                               |



### <a name="child-element-sequence"></a><span data-ttu-id="10add-123">Sequenz untergeordneter Elemente</span><span class="sxs-lookup"><span data-stu-id="10add-123">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  proxyClass?, 
  events?, 
  async?, 
  faultInfo?
)
```

## <a name="parent-elements"></a><span data-ttu-id="10add-124">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="10add-124">Parent elements</span></span>



| <span data-ttu-id="10add-125">Element</span><span class="sxs-lookup"><span data-stu-id="10add-125">Element</span></span>                         | <span data-ttu-id="10add-126">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="10add-126">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="10add-127">**Datei**</span><span class="sxs-lookup"><span data-stu-id="10add-127">**file**</span></span>](file.md)<br/> | <span data-ttu-id="10add-128">Gibt eine Datei aus dem Codegenerator aus.</span><span class="sxs-lookup"><span data-stu-id="10add-128">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="10add-129">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="10add-129">Element information</span></span>



| <span data-ttu-id="10add-130">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="10add-130">Label</span></span> | <span data-ttu-id="10add-131">Wert</span><span class="sxs-lookup"><span data-stu-id="10add-131">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="10add-132">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="10add-132">Minimum supported system</span></span><br/> | <span data-ttu-id="10add-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="10add-133">Windows Vista</span></span> |
| <span data-ttu-id="10add-134">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="10add-134">Can be empty</span></span>                        | <span data-ttu-id="10add-135">Ja</span><span class="sxs-lookup"><span data-stu-id="10add-135">Yes</span></span>           |



 

 




