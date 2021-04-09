---
description: Generiert Implementierungen für Proxy Funktionen für Porttyp Vorgänge.
ms.assetid: 9505ee5f-fdb9-41b8-9537-0c5d29f90168
title: proxyfunctionimplementierungen-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53a27e217cfa3d0a9efd204a1b18c7b2f0ca16f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867344"
---
# <a name="proxyfunctionimplementations-element"></a><span data-ttu-id="c2465-103">proxyfunctionimplementierungen-Element</span><span class="sxs-lookup"><span data-stu-id="c2465-103">proxyFunctionImplementations element</span></span>

<span data-ttu-id="c2465-104">Generiert Implementierungen für Proxy Funktionen für Porttyp Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="c2465-104">Generates implementations for proxy functions for port type operations.</span></span>

## <a name="usage"></a><span data-ttu-id="c2465-105">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="c2465-105">Usage</span></span>

``` syntax
<proxyFunctionImplementations>
  child elements
</proxyFunctionImplementations>
```

## <a name="attributes"></a><span data-ttu-id="c2465-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="c2465-106">Attributes</span></span>

<span data-ttu-id="c2465-107">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="c2465-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="c2465-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c2465-108">Child elements</span></span>



| <span data-ttu-id="c2465-109">Element</span><span class="sxs-lookup"><span data-stu-id="c2465-109">Element</span></span>                                     | <span data-ttu-id="c2465-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c2465-110">Description</span></span>                                                                                                             |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c2465-111">**async**</span><span class="sxs-lookup"><span data-stu-id="c2465-111">**async**</span></span>](async.md)<br/>           | <span data-ttu-id="c2465-112">Gibt an, ob asynchrone Vorgänge in den generierten Proxy Funktionen enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="c2465-112">Specifies whether asynchronous operations are included in the generated proxy functions.</span></span><br/> <br/>         |
| [<span data-ttu-id="c2465-113">**Fall**</span><span class="sxs-lookup"><span data-stu-id="c2465-113">**events**</span></span>](events.md)<br/>         | <span data-ttu-id="c2465-114">Gibt an, ob verwandte Ereignisse in den generierten Funktionen enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="c2465-114">Specifies whether related events are included in the generated functions.</span></span><br/> <br/>                        |
| [<span data-ttu-id="c2465-115">**faultinfo**</span><span class="sxs-lookup"><span data-stu-id="c2465-115">**faultInfo**</span></span>](faultinfo.md)<br/>   | <span data-ttu-id="c2465-116">Gibt an, ob Parameter, die zum Übergeben von Fehlerinformationen verwendet werden, in generierte Funktionen eingeschlossen werden</span><span class="sxs-lookup"><span data-stu-id="c2465-116">Specifies whether parameters used to pass fault information are included in generated functions.</span></span><br/> <br/> |
| [<span data-ttu-id="c2465-117">**Betriebs**</span><span class="sxs-lookup"><span data-stu-id="c2465-117">**operation**</span></span>](operation.md)<br/>   | <span data-ttu-id="c2465-118">Gibt einen Vorgang an, für den Code generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="c2465-118">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                                        |
| [<span data-ttu-id="c2465-119">**PortType**</span><span class="sxs-lookup"><span data-stu-id="c2465-119">**portType**</span></span>](porttype.md)<br/>     | <span data-ttu-id="c2465-120">Gibt den Porttyp an, für den Code generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="c2465-120">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                                       |
| [<span data-ttu-id="c2465-121">**proxyClass**</span><span class="sxs-lookup"><span data-stu-id="c2465-121">**proxyClass**</span></span>](proxyclass.md)<br/> | <span data-ttu-id="c2465-122">Gibt den Namen der Client seitigen Proxy Klasse an.</span><span class="sxs-lookup"><span data-stu-id="c2465-122">Specifies the name of the client-side proxy class.</span></span><br/> <br/>                                               |



### <a name="child-element-sequence"></a><span data-ttu-id="c2465-123">Sequenz untergeordneter Elemente</span><span class="sxs-lookup"><span data-stu-id="c2465-123">Child element sequence</span></span>

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

## <a name="parent-elements"></a><span data-ttu-id="c2465-124">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c2465-124">Parent elements</span></span>



| <span data-ttu-id="c2465-125">Element</span><span class="sxs-lookup"><span data-stu-id="c2465-125">Element</span></span>                         | <span data-ttu-id="c2465-126">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c2465-126">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="c2465-127">**Datei**</span><span class="sxs-lookup"><span data-stu-id="c2465-127">**file**</span></span>](file.md)<br/> | <span data-ttu-id="c2465-128">Gibt eine Datei aus dem Code-Generator aus.</span><span class="sxs-lookup"><span data-stu-id="c2465-128">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="c2465-129">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="c2465-129">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="c2465-130">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="c2465-130">Minimum supported system</span></span><br/> | <span data-ttu-id="c2465-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c2465-131">Windows Vista</span></span> |
| <span data-ttu-id="c2465-132">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="c2465-132">Can be empty</span></span>                        | <span data-ttu-id="c2465-133">Ja</span><span class="sxs-lookup"><span data-stu-id="c2465-133">Yes</span></span>           |



 

 




