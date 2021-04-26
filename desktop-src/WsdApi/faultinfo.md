---
description: Gibt an, ob Parameter, die zum Übergeben von Fehlerinformationen verwendet werden, in generierten Funktionen enthalten sind.
ms.assetid: aba78d50-f884-416a-b022-bb03416aad11
title: faultInfo-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3788af9aeb31d1ed84522bc6b177143ec0607b2
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995857"
---
# <a name="faultinfo-element"></a><span data-ttu-id="2739a-103">faultInfo-Element</span><span class="sxs-lookup"><span data-stu-id="2739a-103">faultInfo element</span></span>

<span data-ttu-id="2739a-104">Gibt an, ob Parameter, die zum Übergeben von Fehlerinformationen verwendet werden, in generierten Funktionen enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="2739a-104">Specifies whether parameters used to pass fault information are included in generated functions.</span></span>

## <a name="usage"></a><span data-ttu-id="2739a-105">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="2739a-105">Usage</span></span>

``` syntax
<faultInfo/>
```

## <a name="attributes"></a><span data-ttu-id="2739a-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="2739a-106">Attributes</span></span>

<span data-ttu-id="2739a-107">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="2739a-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="2739a-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2739a-108">Child elements</span></span>

<span data-ttu-id="2739a-109">Es gibt keine untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="2739a-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="2739a-110">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2739a-110">Parent elements</span></span>



| <span data-ttu-id="2739a-111">Element</span><span class="sxs-lookup"><span data-stu-id="2739a-111">Element</span></span>                                                                         | <span data-ttu-id="2739a-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2739a-112">Description</span></span>                                                                                                |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2739a-113">**functionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="2739a-113">**functionDeclarations**</span></span>](functiondeclarations.md)<br/>                 | <span data-ttu-id="2739a-114">Generiert Implementierungsdeklarationen für Proxyfunktionen für Porttypvorgänge.</span><span class="sxs-lookup"><span data-stu-id="2739a-114">Generates implementation declarations for proxy functions for port type operations.</span></span><br/> <br/> |
| [<span data-ttu-id="2739a-115">**idlFunctionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="2739a-115">**idlFunctionDeclarations**</span></span>](idlfunctiondeclarations.md)<br/>           | <span data-ttu-id="2739a-116">Generiert IDL-Deklarationen für Proxyfunktionen für Porttypvorgänge.</span><span class="sxs-lookup"><span data-stu-id="2739a-116">Generates IDL declarations for proxy functions for port type operations.</span></span><br/> <br/>            |
| [<span data-ttu-id="2739a-117">**proxyFunctionImplementations**</span><span class="sxs-lookup"><span data-stu-id="2739a-117">**proxyFunctionImplementations**</span></span>](proxyfunctionimplementations.md)<br/> | <span data-ttu-id="2739a-118">Generiert Implementierungen für Proxyfunktionen für Porttypvorgänge.</span><span class="sxs-lookup"><span data-stu-id="2739a-118">Generates implementations for proxy functions for port type operations.</span></span><br/> <br/>             |
| [<span data-ttu-id="2739a-119">**stubDefinitions**</span><span class="sxs-lookup"><span data-stu-id="2739a-119">**stubDefinitions**</span></span>](stubdefinitions.md)<br/>                           | <span data-ttu-id="2739a-120">Generiert Implementierungen für Stubfunktionen für Porttypvorgänge.</span><span class="sxs-lookup"><span data-stu-id="2739a-120">Generates implementations for stub functions for port type operations.</span></span><br/> <br/>              |



## <a name="remarks"></a><span data-ttu-id="2739a-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2739a-121">Remarks</span></span>

<span data-ttu-id="2739a-122">Mögliche Werte sind 1 (Fehlerparameter eingeschlossen) und 0 (Fehlerparameter ausgeschlossen).</span><span class="sxs-lookup"><span data-stu-id="2739a-122">Possible values are 1 (fault parameters included) and 0 (fault parameters excluded).</span></span> <span data-ttu-id="2739a-123">Standardmäßig werden Fehlerparameter ausgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="2739a-123">By default, fault parameters are excluded.</span></span>

## <a name="element-information"></a><span data-ttu-id="2739a-124">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="2739a-124">Element information</span></span>



| <span data-ttu-id="2739a-125">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="2739a-125">Label</span></span> | <span data-ttu-id="2739a-126">Wert</span><span class="sxs-lookup"><span data-stu-id="2739a-126">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="2739a-127">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="2739a-127">Minimum supported system</span></span><br/> | <span data-ttu-id="2739a-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2739a-128">Windows Vista</span></span> |
| <span data-ttu-id="2739a-129">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="2739a-129">Can be empty</span></span>                        | <span data-ttu-id="2739a-130">Ja</span><span class="sxs-lookup"><span data-stu-id="2739a-130">Yes</span></span>           |



 

 




