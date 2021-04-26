---
description: Gibt an, ob verwandte Ereignisse in den generierten Funktionen enthalten sind.
ms.assetid: 23ca463c-b305-496b-a1e3-58dbb793f17e
title: events-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6883f1bcca9b62c3d8b60ca86f47b0e688d513c2
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995928"
---
# <a name="events-element"></a><span data-ttu-id="a210e-103">events-Element</span><span class="sxs-lookup"><span data-stu-id="a210e-103">events element</span></span>

<span data-ttu-id="a210e-104">Gibt an, ob verwandte Ereignisse in den generierten Funktionen enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="a210e-104">Specifies whether related events are included in the generated functions.</span></span>

## <a name="usage"></a><span data-ttu-id="a210e-105">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="a210e-105">Usage</span></span>

``` syntax
<events/>
```

## <a name="attributes"></a><span data-ttu-id="a210e-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="a210e-106">Attributes</span></span>

<span data-ttu-id="a210e-107">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="a210e-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="a210e-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a210e-108">Child elements</span></span>

<span data-ttu-id="a210e-109">Es gibt keine untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="a210e-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="a210e-110">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a210e-110">Parent elements</span></span>



| <span data-ttu-id="a210e-111">Element</span><span class="sxs-lookup"><span data-stu-id="a210e-111">Element</span></span>                                                                         | <span data-ttu-id="a210e-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a210e-112">Description</span></span>                                                                                                |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a210e-113">**functionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="a210e-113">**functionDeclarations**</span></span>](functiondeclarations.md)<br/>                 | <span data-ttu-id="a210e-114">Generiert Implementierungsdeklarationen für Proxyfunktionen für Porttypvorgänge.</span><span class="sxs-lookup"><span data-stu-id="a210e-114">Generates implementation declarations for proxy functions for port type operations.</span></span><br/> <br/> |
| [<span data-ttu-id="a210e-115">**idlFunctionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="a210e-115">**idlFunctionDeclarations**</span></span>](idlfunctiondeclarations.md)<br/>           | <span data-ttu-id="a210e-116">Generiert IDL-Deklarationen für Proxyfunktionen für Porttypvorgänge.</span><span class="sxs-lookup"><span data-stu-id="a210e-116">Generates IDL declarations for proxy functions for port type operations.</span></span><br/> <br/>            |
| [<span data-ttu-id="a210e-117">**proxyFunctionImplementations**</span><span class="sxs-lookup"><span data-stu-id="a210e-117">**proxyFunctionImplementations**</span></span>](proxyfunctionimplementations.md)<br/> | <span data-ttu-id="a210e-118">Generiert Implementierungen für Proxyfunktionen für Porttypvorgänge.</span><span class="sxs-lookup"><span data-stu-id="a210e-118">Generates implementations for proxy functions for port type operations.</span></span><br/> <br/>             |
| [<span data-ttu-id="a210e-119">**stubDeclarations**</span><span class="sxs-lookup"><span data-stu-id="a210e-119">**stubDeclarations**</span></span>](stubdeclarations.md)<br/>                         | <span data-ttu-id="a210e-120">Generiert Deklarationen für Stubfunktionen für Porttypvorgänge.</span><span class="sxs-lookup"><span data-stu-id="a210e-120">Generates declarations for stub functions for port type operations.</span></span><br/> <br/>                 |
| [<span data-ttu-id="a210e-121">**stubDefinitions**</span><span class="sxs-lookup"><span data-stu-id="a210e-121">**stubDefinitions**</span></span>](stubdefinitions.md)<br/>                           | <span data-ttu-id="a210e-122">Generiert Implementierungen für Stubfunktionen für Porttypvorgänge.</span><span class="sxs-lookup"><span data-stu-id="a210e-122">Generates implementations for stub functions for port type operations.</span></span><br/> <br/>              |



## <a name="remarks"></a><span data-ttu-id="a210e-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a210e-123">Remarks</span></span>

<span data-ttu-id="a210e-124">Mögliche Werte sind 1 (ereignisse eingeschlossen) und 0 (Standard, ausgeschlossene Ereignisse).</span><span class="sxs-lookup"><span data-stu-id="a210e-124">Possible values are 1 (events included) and 0 (default, events excluded).</span></span>

## <a name="element-information"></a><span data-ttu-id="a210e-125">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="a210e-125">Element information</span></span>



| <span data-ttu-id="a210e-126">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="a210e-126">Label</span></span> | <span data-ttu-id="a210e-127">Wert</span><span class="sxs-lookup"><span data-stu-id="a210e-127">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="a210e-128">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="a210e-128">Minimum supported system</span></span><br/> | <span data-ttu-id="a210e-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a210e-129">Windows Vista</span></span> |
| <span data-ttu-id="a210e-130">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="a210e-130">Can be empty</span></span>                        | <span data-ttu-id="a210e-131">Ja</span><span class="sxs-lookup"><span data-stu-id="a210e-131">Yes</span></span>           |



 

 




