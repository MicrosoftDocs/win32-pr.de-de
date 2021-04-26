---
description: Gibt an, ob asynchrone Vorgänge in den generierten Proxyfunktionen enthalten sind.
ms.assetid: 7b57d5c6-589b-4e03-bfcf-1faa671ebd77
title: async-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6cbc68d0a5dea30f4b4d179a54539ac3f9516a4
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994957"
---
# <a name="async-element"></a><span data-ttu-id="6c735-103">async-Element</span><span class="sxs-lookup"><span data-stu-id="6c735-103">async element</span></span>

<span data-ttu-id="6c735-104">Gibt an, ob asynchrone Vorgänge in den generierten Proxyfunktionen enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="6c735-104">Specifies whether asynchronous operations are included in the generated proxy functions.</span></span>

## <a name="usage"></a><span data-ttu-id="6c735-105">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="6c735-105">Usage</span></span>

``` syntax
<async/>
```

## <a name="attributes"></a><span data-ttu-id="6c735-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="6c735-106">Attributes</span></span>

<span data-ttu-id="6c735-107">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="6c735-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="6c735-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6c735-108">Child elements</span></span>

<span data-ttu-id="6c735-109">Es gibt keine untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="6c735-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="6c735-110">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6c735-110">Parent elements</span></span>



| <span data-ttu-id="6c735-111">Element</span><span class="sxs-lookup"><span data-stu-id="6c735-111">Element</span></span>                                                                         | <span data-ttu-id="6c735-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6c735-112">Description</span></span>                                                                                                |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6c735-113">**functionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="6c735-113">**functionDeclarations**</span></span>](functiondeclarations.md)<br/>                 | <span data-ttu-id="6c735-114">Generiert Implementierungsdeklarationen für Proxyfunktionen für Porttypvorgänge.</span><span class="sxs-lookup"><span data-stu-id="6c735-114">Generates implementation declarations for proxy functions for port type operations.</span></span><br/> <br/> |
| [<span data-ttu-id="6c735-115">**idlFunctionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="6c735-115">**idlFunctionDeclarations**</span></span>](idlfunctiondeclarations.md)<br/>           | <span data-ttu-id="6c735-116">Generiert IDL-Deklarationen für Proxyfunktionen für Porttypvorgänge.</span><span class="sxs-lookup"><span data-stu-id="6c735-116">Generates IDL declarations for proxy functions for port type operations.</span></span><br/> <br/>            |
| [<span data-ttu-id="6c735-117">**proxyFunctionImplementations**</span><span class="sxs-lookup"><span data-stu-id="6c735-117">**proxyFunctionImplementations**</span></span>](proxyfunctionimplementations.md)<br/> | <span data-ttu-id="6c735-118">Generiert Implementierungen für Proxyfunktionen für Porttypvorgänge.</span><span class="sxs-lookup"><span data-stu-id="6c735-118">Generates implementations for proxy functions for port type operations.</span></span><br/> <br/>             |



## <a name="remarks"></a><span data-ttu-id="6c735-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6c735-119">Remarks</span></span>

<span data-ttu-id="6c735-120">Mögliche Werte sind 1 (asynchrone Vorgänge eingeschlossen) und 0 (Standard, asynchrone Vorgänge ausgeschlossen).</span><span class="sxs-lookup"><span data-stu-id="6c735-120">Possible values are 1 (asynchronous operations included) and 0 (default, asynchronous operations excluded).</span></span>

<span data-ttu-id="6c735-121">Ein Proxy kann sowohl asynchrone als auch synchrone Versionen der gleichen Vorgänge haben.</span><span class="sxs-lookup"><span data-stu-id="6c735-121">A proxy can have both asynchronous and synchronous versions of the same operations.</span></span>

## <a name="element-information"></a><span data-ttu-id="6c735-122">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="6c735-122">Element information</span></span>



| <span data-ttu-id="6c735-123">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="6c735-123">Label</span></span> | <span data-ttu-id="6c735-124">Wert</span><span class="sxs-lookup"><span data-stu-id="6c735-124">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="6c735-125">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="6c735-125">Minimum supported system</span></span><br/> | <span data-ttu-id="6c735-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6c735-126">Windows Vista</span></span> |
| <span data-ttu-id="6c735-127">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="6c735-127">Can be empty</span></span>                        | <span data-ttu-id="6c735-128">Ja</span><span class="sxs-lookup"><span data-stu-id="6c735-128">Yes</span></span>           |



 

 




