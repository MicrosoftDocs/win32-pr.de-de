---
title: Application-Element
description: Stellt das Element der obersten Ebene in der Markup Spezifikation des Windows-Menü Band Frameworks dar.
ms.assetid: 05396d8b-fbd1-40bb-8d0f-8ac11506e7db
keywords:
- Windows-Menüband für Anwendungs Element
topic_type:
- apiref
api_name:
- Application
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9b116879a918ca0437c7f2bdd201ef4ffd6d3c61
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "103734713"
---
# <a name="application-element"></a><span data-ttu-id="7dc32-104">Application-Element</span><span class="sxs-lookup"><span data-stu-id="7dc32-104">Application element</span></span>

<span data-ttu-id="7dc32-105">Stellt das Element der obersten Ebene in der Markup Spezifikation des Windows-Menü Band Frameworks dar.</span><span class="sxs-lookup"><span data-stu-id="7dc32-105">Represents the top-level element in the Windows Ribbon framework markup specification.</span></span>

## <a name="usage"></a><span data-ttu-id="7dc32-106">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="7dc32-106">Usage</span></span>

``` syntax
<Application
  xmlns = "xs:string">
  child elements
</Application>
```

## <a name="attributes"></a><span data-ttu-id="7dc32-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="7dc32-107">Attributes</span></span>



| <span data-ttu-id="7dc32-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="7dc32-108">Attribute</span></span>            | <span data-ttu-id="7dc32-109">type</span><span class="sxs-lookup"><span data-stu-id="7dc32-109">Type</span></span>                 | <span data-ttu-id="7dc32-110">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="7dc32-110">Required</span></span>       | <span data-ttu-id="7dc32-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7dc32-111">Description</span></span>                                                                                                                                                                                                       |
|----------------------|----------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7dc32-112">**xmlns**</span><span class="sxs-lookup"><span data-stu-id="7dc32-112">**xmlns**</span></span><br/> | <span data-ttu-id="7dc32-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="7dc32-113">xs:string</span></span><br/> | <span data-ttu-id="7dc32-114">Ja</span><span class="sxs-lookup"><span data-stu-id="7dc32-114">Yes</span></span><br/> | <dt>`http://schemas.microsoft.com/windows/2009/Ribbon`<br/> </dt> <dd> <span data-ttu-id="7dc32-115">Der URI für die Markup-Namespace Bindung des Menübands.</span><span class="sxs-lookup"><span data-stu-id="7dc32-115">The URI for the Ribbon markup namespace binding.</span></span> <br/> </dd> </dl> |



## <a name="child-elements"></a><span data-ttu-id="7dc32-116">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7dc32-116">Child elements</span></span>



| <span data-ttu-id="7dc32-117">Element</span><span class="sxs-lookup"><span data-stu-id="7dc32-117">Element</span></span>                                                                               | <span data-ttu-id="7dc32-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7dc32-118">Description</span></span>                                    |
|---------------------------------------------------------------------------------------|------------------------------------------------|
| [<span data-ttu-id="7dc32-119">**Application. Commands**</span><span class="sxs-lookup"><span data-stu-id="7dc32-119">**Application.Commands**</span></span>](windowsribbon-element-application-commands.md)<br/> | <span data-ttu-id="7dc32-120">Kann höchstens einmal vorkommen</span><span class="sxs-lookup"><span data-stu-id="7dc32-120">May occur at most once</span></span><br/> <br/>  |
| [<span data-ttu-id="7dc32-121">**Application. views**</span><span class="sxs-lookup"><span data-stu-id="7dc32-121">**Application.Views**</span></span>](windowsribbon-element-application-views.md)<br/>       | <span data-ttu-id="7dc32-122">Muss genau einmal auftreten</span><span class="sxs-lookup"><span data-stu-id="7dc32-122">Must occur exactly once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="7dc32-123">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7dc32-123">Parent elements</span></span>

<span data-ttu-id="7dc32-124">Es gibt keine übergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="7dc32-124">There are no parent elements.</span></span>

## <a name="remarks"></a><span data-ttu-id="7dc32-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7dc32-125">Remarks</span></span>

<span data-ttu-id="7dc32-126">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7dc32-126">Required.</span></span>

<span data-ttu-id="7dc32-127">Muss genau einmal als Container für alle Menü Band Markup vorkommen.</span><span class="sxs-lookup"><span data-stu-id="7dc32-127">Must occur exactly once as the container for all of the Ribbon markup.</span></span>

<span data-ttu-id="7dc32-128">Die untergeordneten Elemente des **Application** -Elements müssen in der angegebenen Reihenfolge vorkommen:</span><span class="sxs-lookup"><span data-stu-id="7dc32-128">The child elements of the **Application** element must occur in the specified order:</span></span>

1.  [<span data-ttu-id="7dc32-129">**Application. Commands**</span><span class="sxs-lookup"><span data-stu-id="7dc32-129">**Application.Commands**</span></span>](windowsribbon-element-application-commands.md)
2.  [<span data-ttu-id="7dc32-130">**Application. views**</span><span class="sxs-lookup"><span data-stu-id="7dc32-130">**Application.Views**</span></span>](windowsribbon-element-application-views.md)

## <a name="examples"></a><span data-ttu-id="7dc32-131">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7dc32-131">Examples</span></span>

<span data-ttu-id="7dc32-132">Das folgende Beispiel zeigt eine Deklaration eines **Anwendungs** Elements.</span><span class="sxs-lookup"><span data-stu-id="7dc32-132">The following example shows an **Application** element declaration.</span></span>


```XML
<Application xmlns="http://schemas.microsoft.com/windows/2009/Ribbon">
...
</Application>
```



## <a name="element-information"></a><span data-ttu-id="7dc32-133">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="7dc32-133">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="7dc32-134">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="7dc32-134">Minimum supported system</span></span><br/> | <span data-ttu-id="7dc32-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7dc32-135">Windows 7</span></span> |
| <span data-ttu-id="7dc32-136">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="7dc32-136">Can be empty</span></span>                        | <span data-ttu-id="7dc32-137">Nein</span><span class="sxs-lookup"><span data-stu-id="7dc32-137">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="7dc32-138">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="7dc32-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7dc32-139">Deklarieren von Befehlen und Steuerelementen mit Menüband-Markup</span><span class="sxs-lookup"><span data-stu-id="7dc32-139">Declaring Commands and Controls with Ribbon Markup</span></span>](windowsribbon-schema.md)
</dt> </dl>

 

 





