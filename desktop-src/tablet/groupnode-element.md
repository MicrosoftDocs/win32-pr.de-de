---
description: Enthält eine Reihe von Elementen&\# 8212; Paragraph, InkWord, Drawing, Text, Image oder Flag&\# 8212;, die in der Journalnotiz gruppiert sind.
ms.assetid: 59ee3037-7178-41c8-84d5-d5c68fa2cf9b
title: GroupNode-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbc4d39a592b5b6328bd31ff37761cfd3f0138c0
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432571"
---
# <a name="groupnode-element"></a><span data-ttu-id="2b205-103">GroupNode-Element</span><span class="sxs-lookup"><span data-stu-id="2b205-103">GroupNode Element</span></span>

<span data-ttu-id="2b205-104">Enthält eine Reihe von Elementen –[**Absatz**](paragraph-element.md), [**InkWord**](inkword-element.md), [**Zeichnung**](drawing-element.md), [**Text**](text-element.md), [**Bild**](image-element.md)oder [**Flag**](flag-element.md)– die in der Journalnotiz zusammen bzw. niert sind.</span><span class="sxs-lookup"><span data-stu-id="2b205-104">Contains a set of elements—[**Paragraph**](paragraph-element.md), [**InkWord**](inkword-element.md), [**Drawing**](drawing-element.md), [**Text**](text-element.md), [**Image**](image-element.md), or [**Flag**](flag-element.md)—that are grouped together in the Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="2b205-105">Definition</span><span class="sxs-lookup"><span data-stu-id="2b205-105">Definition</span></span>

``` syntax
<xs:element name="GroupNode" type="GroupNodeType" />
```

## <a name="parent-elements"></a><span data-ttu-id="2b205-106">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2b205-106">Parent Elements</span></span>

[<span data-ttu-id="2b205-107">**Inhalt**</span><span class="sxs-lookup"><span data-stu-id="2b205-107">**Content**</span></span>](content-element--journal-reader.md)

## <a name="child-elements"></a><span data-ttu-id="2b205-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2b205-108">Child Elements</span></span>

[<span data-ttu-id="2b205-109">**Paragraph**</span><span class="sxs-lookup"><span data-stu-id="2b205-109">**Paragraph**</span></span>](paragraph-element.md)

[<span data-ttu-id="2b205-110">**InkWord**</span><span class="sxs-lookup"><span data-stu-id="2b205-110">**InkWord**</span></span>](inkword-element.md)

[<span data-ttu-id="2b205-111">**Zeichnung**</span><span class="sxs-lookup"><span data-stu-id="2b205-111">**Drawing**</span></span>](drawing-element.md)

[<span data-ttu-id="2b205-112">**Text**</span><span class="sxs-lookup"><span data-stu-id="2b205-112">**Text**</span></span>](text-element.md)

[<span data-ttu-id="2b205-113">**Image**</span><span class="sxs-lookup"><span data-stu-id="2b205-113">**Image**</span></span>](docimage-element.md)

[<span data-ttu-id="2b205-114">**Flag**</span><span class="sxs-lookup"><span data-stu-id="2b205-114">**Flag**</span></span>](flag-element.md)

## <a name="attributes"></a><span data-ttu-id="2b205-115">Attribute</span><span class="sxs-lookup"><span data-stu-id="2b205-115">Attributes</span></span>



| <span data-ttu-id="2b205-116">attribute</span><span class="sxs-lookup"><span data-stu-id="2b205-116">Attribute</span></span>  | <span data-ttu-id="2b205-117">Typ</span><span class="sxs-lookup"><span data-stu-id="2b205-117">Type</span></span>                      | <span data-ttu-id="2b205-118">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="2b205-118">Required</span></span> | <span data-ttu-id="2b205-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2b205-119">Description</span></span>                                                                             | <span data-ttu-id="2b205-120">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="2b205-120">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="2b205-121">**Left**</span><span class="sxs-lookup"><span data-stu-id="2b205-121">**Left**</span></span>   | <span data-ttu-id="2b205-122">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="2b205-122">**xs:integer**</span></span>            | <span data-ttu-id="2b205-123">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="2b205-123">Required</span></span> | <span data-ttu-id="2b205-124">Der Abstand zwischen dem Ursprung und dem äußersten linken Punkt im Begrenzungsfeld für das Element.</span><span class="sxs-lookup"><span data-stu-id="2b205-124">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="2b205-125">Eine beliebige ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="2b205-125">Any integer.</span></span>              |
| <span data-ttu-id="2b205-126">**Top**</span><span class="sxs-lookup"><span data-stu-id="2b205-126">**Top**</span></span>    | <span data-ttu-id="2b205-127">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="2b205-127">**xs:integer**</span></span>            | <span data-ttu-id="2b205-128">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="2b205-128">Required</span></span> | <span data-ttu-id="2b205-129">Der Abstand zwischen dem Ursprung und dem obersten Punkt im Begrenzungsfeld für das Element.</span><span class="sxs-lookup"><span data-stu-id="2b205-129">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="2b205-130">Eine beliebige ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="2b205-130">Any integer.</span></span>              |
| <span data-ttu-id="2b205-131">**Width**</span><span class="sxs-lookup"><span data-stu-id="2b205-131">**Width**</span></span>  | <span data-ttu-id="2b205-132">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="2b205-132">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="2b205-133">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="2b205-133">Required</span></span> | <span data-ttu-id="2b205-134">Die Breite des Begrenzungsfelds für das Element.</span><span class="sxs-lookup"><span data-stu-id="2b205-134">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="2b205-135">Eine nicht negative ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="2b205-135">Any non-negative integer.</span></span> |
| <span data-ttu-id="2b205-136">**Height**</span><span class="sxs-lookup"><span data-stu-id="2b205-136">**Height**</span></span> | <span data-ttu-id="2b205-137">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="2b205-137">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="2b205-138">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="2b205-138">Required</span></span> | <span data-ttu-id="2b205-139">Die Höhe des Begrenzungsfelds für das Element.</span><span class="sxs-lookup"><span data-stu-id="2b205-139">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="2b205-140">Eine nicht negative ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="2b205-140">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="2b205-141">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="2b205-141">Element Information</span></span>



|  <span data-ttu-id="2b205-142">Element</span><span class="sxs-lookup"><span data-stu-id="2b205-142">Element</span></span>     | <span data-ttu-id="2b205-143">Wert</span><span class="sxs-lookup"><span data-stu-id="2b205-143">Value</span></span>                                                     |
|--------------|-----------------------------------------------------------------|
| <span data-ttu-id="2b205-144">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="2b205-144">Element type</span></span> | <span data-ttu-id="2b205-145">[**complexType: GroupNodeType**](groupnodetype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="2b205-145">[**GroupNodeType**](groupnodetype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="2b205-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="2b205-146">Namespace</span></span>    | <span data-ttu-id="2b205-147">urn:schemas-microsoft-com:tabletpc:richink</span><span class="sxs-lookup"><span data-stu-id="2b205-147">urn:schemas-microsoft-com:tabletpc:richink</span></span>                      |
| <span data-ttu-id="2b205-148">Schemaname</span><span class="sxs-lookup"><span data-stu-id="2b205-148">Schema name</span></span>  | <span data-ttu-id="2b205-149">Journalreader</span><span class="sxs-lookup"><span data-stu-id="2b205-149">Journal Reader</span></span>                                                  |



 

 

 



