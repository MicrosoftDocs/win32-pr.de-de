---
description: Gibt an, ob Parameter, die zum Übergeben von Fehlerinformationen verwendet werden, in generierte Funktionen eingeschlossen werden
ms.assetid: aba78d50-f884-416a-b022-bb03416aad11
title: faultinfo-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f0fd65a7214f61a0b2fa6bb8f44d9a8cadbef07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216513"
---
# <a name="faultinfo-element"></a><span data-ttu-id="a3f5b-103">faultinfo-Element</span><span class="sxs-lookup"><span data-stu-id="a3f5b-103">faultInfo element</span></span>

<span data-ttu-id="a3f5b-104">Gibt an, ob Parameter, die zum Übergeben von Fehlerinformationen verwendet werden, in generierte Funktionen eingeschlossen werden</span><span class="sxs-lookup"><span data-stu-id="a3f5b-104">Specifies whether parameters used to pass fault information are included in generated functions.</span></span>

## <a name="usage"></a><span data-ttu-id="a3f5b-105">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="a3f5b-105">Usage</span></span>

``` syntax
<faultInfo/>
```

## <a name="attributes"></a><span data-ttu-id="a3f5b-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="a3f5b-106">Attributes</span></span>

<span data-ttu-id="a3f5b-107">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="a3f5b-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="a3f5b-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a3f5b-108">Child elements</span></span>

<span data-ttu-id="a3f5b-109">Es gibt keine untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="a3f5b-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="a3f5b-110">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a3f5b-110">Parent elements</span></span>



| <span data-ttu-id="a3f5b-111">Element</span><span class="sxs-lookup"><span data-stu-id="a3f5b-111">Element</span></span>                                                                         | <span data-ttu-id="a3f5b-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a3f5b-112">Description</span></span>                                                                                                |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a3f5b-113">**functiondeklarationen**</span><span class="sxs-lookup"><span data-stu-id="a3f5b-113">**functionDeclarations**</span></span>](functiondeclarations.md)<br/>                 | <span data-ttu-id="a3f5b-114">Generiert Implementierungs Deklarationen für Proxy Funktionen für Porttyp Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="a3f5b-114">Generates implementation declarations for proxy functions for port type operations.</span></span><br/> <br/> |
| [<span data-ttu-id="a3f5b-115">**idlfunctiondeklarationen**</span><span class="sxs-lookup"><span data-stu-id="a3f5b-115">**idlFunctionDeclarations**</span></span>](idlfunctiondeclarations.md)<br/>           | <span data-ttu-id="a3f5b-116">Generiert IDL-Deklarationen für Proxy Funktionen für Porttyp Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="a3f5b-116">Generates IDL declarations for proxy functions for port type operations.</span></span><br/> <br/>            |
| [<span data-ttu-id="a3f5b-117">**proxyfunctionimplementierungen**</span><span class="sxs-lookup"><span data-stu-id="a3f5b-117">**proxyFunctionImplementations**</span></span>](proxyfunctionimplementations.md)<br/> | <span data-ttu-id="a3f5b-118">Generiert Implementierungen für Proxy Funktionen für Porttyp Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="a3f5b-118">Generates implementations for proxy functions for port type operations.</span></span><br/> <br/>             |
| [<span data-ttu-id="a3f5b-119">**stubdefinitionen**</span><span class="sxs-lookup"><span data-stu-id="a3f5b-119">**stubDefinitions**</span></span>](stubdefinitions.md)<br/>                           | <span data-ttu-id="a3f5b-120">Generiert Implementierungen für Stub-Funktionen für Porttyp Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="a3f5b-120">Generates implementations for stub functions for port type operations.</span></span><br/> <br/>              |



## <a name="remarks"></a><span data-ttu-id="a3f5b-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a3f5b-121">Remarks</span></span>

<span data-ttu-id="a3f5b-122">Mögliche Werte sind 1 (Fehler Parameter eingeschlossen) und 0 (Fehler Parameter ausgeschlossen).</span><span class="sxs-lookup"><span data-stu-id="a3f5b-122">Possible values are 1 (fault parameters included) and 0 (fault parameters excluded).</span></span> <span data-ttu-id="a3f5b-123">Standardmäßig werden Fehler Parameter ausgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="a3f5b-123">By default, fault parameters are excluded.</span></span>

## <a name="element-information"></a><span data-ttu-id="a3f5b-124">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="a3f5b-124">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="a3f5b-125">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="a3f5b-125">Minimum supported system</span></span><br/> | <span data-ttu-id="a3f5b-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a3f5b-126">Windows Vista</span></span> |
| <span data-ttu-id="a3f5b-127">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="a3f5b-127">Can be empty</span></span>                        | <span data-ttu-id="a3f5b-128">Ja</span><span class="sxs-lookup"><span data-stu-id="a3f5b-128">Yes</span></span>           |



 

 




