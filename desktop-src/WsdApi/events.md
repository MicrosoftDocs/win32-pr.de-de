---
description: Gibt an, ob verwandte Ereignisse in den generierten Funktionen enthalten sind.
ms.assetid: 23ca463c-b305-496b-a1e3-58dbb793f17e
title: Events-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2571cc8e9820ca38beb649b3c227fb1c01f61c50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215433"
---
# <a name="events-element"></a><span data-ttu-id="0dfb0-103">Events-Element</span><span class="sxs-lookup"><span data-stu-id="0dfb0-103">events element</span></span>

<span data-ttu-id="0dfb0-104">Gibt an, ob verwandte Ereignisse in den generierten Funktionen enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="0dfb0-104">Specifies whether related events are included in the generated functions.</span></span>

## <a name="usage"></a><span data-ttu-id="0dfb0-105">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="0dfb0-105">Usage</span></span>

``` syntax
<events/>
```

## <a name="attributes"></a><span data-ttu-id="0dfb0-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="0dfb0-106">Attributes</span></span>

<span data-ttu-id="0dfb0-107">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="0dfb0-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="0dfb0-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0dfb0-108">Child elements</span></span>

<span data-ttu-id="0dfb0-109">Es gibt keine untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="0dfb0-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="0dfb0-110">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0dfb0-110">Parent elements</span></span>



| <span data-ttu-id="0dfb0-111">Element</span><span class="sxs-lookup"><span data-stu-id="0dfb0-111">Element</span></span>                                                                         | <span data-ttu-id="0dfb0-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0dfb0-112">Description</span></span>                                                                                                |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0dfb0-113">**functiondeklarationen**</span><span class="sxs-lookup"><span data-stu-id="0dfb0-113">**functionDeclarations**</span></span>](functiondeclarations.md)<br/>                 | <span data-ttu-id="0dfb0-114">Generiert Implementierungs Deklarationen für Proxy Funktionen für Porttyp Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="0dfb0-114">Generates implementation declarations for proxy functions for port type operations.</span></span><br/> <br/> |
| [<span data-ttu-id="0dfb0-115">**idlfunctiondeklarationen**</span><span class="sxs-lookup"><span data-stu-id="0dfb0-115">**idlFunctionDeclarations**</span></span>](idlfunctiondeclarations.md)<br/>           | <span data-ttu-id="0dfb0-116">Generiert IDL-Deklarationen für Proxy Funktionen für Porttyp Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="0dfb0-116">Generates IDL declarations for proxy functions for port type operations.</span></span><br/> <br/>            |
| [<span data-ttu-id="0dfb0-117">**proxyfunctionimplementierungen**</span><span class="sxs-lookup"><span data-stu-id="0dfb0-117">**proxyFunctionImplementations**</span></span>](proxyfunctionimplementations.md)<br/> | <span data-ttu-id="0dfb0-118">Generiert Implementierungen für Proxy Funktionen für Porttyp Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="0dfb0-118">Generates implementations for proxy functions for port type operations.</span></span><br/> <br/>             |
| [<span data-ttu-id="0dfb0-119">**stubdeklarationen**</span><span class="sxs-lookup"><span data-stu-id="0dfb0-119">**stubDeclarations**</span></span>](stubdeclarations.md)<br/>                         | <span data-ttu-id="0dfb0-120">Generiert Deklarationen für Stub-Funktionen für Porttyp Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="0dfb0-120">Generates declarations for stub functions for port type operations.</span></span><br/> <br/>                 |
| [<span data-ttu-id="0dfb0-121">**stubdefinitionen**</span><span class="sxs-lookup"><span data-stu-id="0dfb0-121">**stubDefinitions**</span></span>](stubdefinitions.md)<br/>                           | <span data-ttu-id="0dfb0-122">Generiert Implementierungen für Stub-Funktionen für Porttyp Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="0dfb0-122">Generates implementations for stub functions for port type operations.</span></span><br/> <br/>              |



## <a name="remarks"></a><span data-ttu-id="0dfb0-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0dfb0-123">Remarks</span></span>

<span data-ttu-id="0dfb0-124">Mögliche Werte sind 1 (enthaltene Ereignisse) und 0 (Standard, ausgeschlossene Ereignisse).</span><span class="sxs-lookup"><span data-stu-id="0dfb0-124">Possible values are 1 (events included) and 0 (default, events excluded).</span></span>

## <a name="element-information"></a><span data-ttu-id="0dfb0-125">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="0dfb0-125">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="0dfb0-126">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="0dfb0-126">Minimum supported system</span></span><br/> | <span data-ttu-id="0dfb0-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0dfb0-127">Windows Vista</span></span> |
| <span data-ttu-id="0dfb0-128">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="0dfb0-128">Can be empty</span></span>                        | <span data-ttu-id="0dfb0-129">Ja</span><span class="sxs-lookup"><span data-stu-id="0dfb0-129">Yes</span></span>           |



 

 




