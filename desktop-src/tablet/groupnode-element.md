---
description: Enthält einen Satz von Elementen&\# 8212; Absatz, InkWord, Zeichnung, Text, Bild oder Flag&\# 8212;, die in der Journal Notiz gruppiert sind.
ms.assetid: 59ee3037-7178-41c8-84d5-d5c68fa2cf9b
title: Groupnode-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ee141691ef58d14e6c08a49544e9cf3ecf7540b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346960"
---
# <a name="groupnode-element"></a><span data-ttu-id="99028-103">Groupnode-Element</span><span class="sxs-lookup"><span data-stu-id="99028-103">GroupNode Element</span></span>

<span data-ttu-id="99028-104">Enthält eine Reihe von Elementen –[**Absatz**](paragraph-element.md), [**InkWord**](inkword-element.md), [**Zeichnung**](drawing-element.md), [**Text**](text-element.md), [**Bild**](image-element.md)oder [**Flag**](flag-element.md)–, die in der Journal Notiz gruppiert sind.</span><span class="sxs-lookup"><span data-stu-id="99028-104">Contains a set of elements—[**Paragraph**](paragraph-element.md), [**InkWord**](inkword-element.md), [**Drawing**](drawing-element.md), [**Text**](text-element.md), [**Image**](image-element.md), or [**Flag**](flag-element.md)—that are grouped together in the Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="99028-105">Definition</span><span class="sxs-lookup"><span data-stu-id="99028-105">Definition</span></span>

``` syntax
<xs:element name="GroupNode" type="GroupNodeType" />
```

## <a name="parent-elements"></a><span data-ttu-id="99028-106">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="99028-106">Parent Elements</span></span>

[<span data-ttu-id="99028-107">**Inhalt**</span><span class="sxs-lookup"><span data-stu-id="99028-107">**Content**</span></span>](content-element--journal-reader.md)

## <a name="child-elements"></a><span data-ttu-id="99028-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="99028-108">Child Elements</span></span>

[<span data-ttu-id="99028-109">**Paragraph**</span><span class="sxs-lookup"><span data-stu-id="99028-109">**Paragraph**</span></span>](paragraph-element.md)

[<span data-ttu-id="99028-110">**InkWord**</span><span class="sxs-lookup"><span data-stu-id="99028-110">**InkWord**</span></span>](inkword-element.md)

[<span data-ttu-id="99028-111">**Zeichnung**</span><span class="sxs-lookup"><span data-stu-id="99028-111">**Drawing**</span></span>](drawing-element.md)

[<span data-ttu-id="99028-112">**Text**</span><span class="sxs-lookup"><span data-stu-id="99028-112">**Text**</span></span>](text-element.md)

[<span data-ttu-id="99028-113">**Image**</span><span class="sxs-lookup"><span data-stu-id="99028-113">**Image**</span></span>](docimage-element.md)

[<span data-ttu-id="99028-114">**Flag**</span><span class="sxs-lookup"><span data-stu-id="99028-114">**Flag**</span></span>](flag-element.md)

## <a name="attributes"></a><span data-ttu-id="99028-115">Attribute</span><span class="sxs-lookup"><span data-stu-id="99028-115">Attributes</span></span>



| <span data-ttu-id="99028-116">Attribut</span><span class="sxs-lookup"><span data-stu-id="99028-116">Attribute</span></span>  | <span data-ttu-id="99028-117">type</span><span class="sxs-lookup"><span data-stu-id="99028-117">Type</span></span>                      | <span data-ttu-id="99028-118">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="99028-118">Required</span></span> | <span data-ttu-id="99028-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="99028-119">Description</span></span>                                                                             | <span data-ttu-id="99028-120">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="99028-120">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="99028-121">**Left**</span><span class="sxs-lookup"><span data-stu-id="99028-121">**Left**</span></span>   | <span data-ttu-id="99028-122">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="99028-122">**xs:integer**</span></span>            | <span data-ttu-id="99028-123">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="99028-123">Required</span></span> | <span data-ttu-id="99028-124">Der Abstand zwischen dem Ursprung und dem äußersten äußersten linken Punkt im umgebenden Feld des Elements.</span><span class="sxs-lookup"><span data-stu-id="99028-124">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="99028-125">Eine beliebige ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="99028-125">Any integer.</span></span>              |
| <span data-ttu-id="99028-126">**Top**</span><span class="sxs-lookup"><span data-stu-id="99028-126">**Top**</span></span>    | <span data-ttu-id="99028-127">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="99028-127">**xs:integer**</span></span>            | <span data-ttu-id="99028-128">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="99028-128">Required</span></span> | <span data-ttu-id="99028-129">Der Abstand zwischen dem Ursprung und dem obersten Punkt im umgebenden Feld für das Element.</span><span class="sxs-lookup"><span data-stu-id="99028-129">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="99028-130">Eine beliebige ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="99028-130">Any integer.</span></span>              |
| <span data-ttu-id="99028-131">**Width**</span><span class="sxs-lookup"><span data-stu-id="99028-131">**Width**</span></span>  | <span data-ttu-id="99028-132">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="99028-132">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="99028-133">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="99028-133">Required</span></span> | <span data-ttu-id="99028-134">Die Breite des Begrenzungs Rahmens für das Element.</span><span class="sxs-lookup"><span data-stu-id="99028-134">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="99028-135">Eine beliebige nicht negative ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="99028-135">Any non-negative integer.</span></span> |
| <span data-ttu-id="99028-136">**Height**</span><span class="sxs-lookup"><span data-stu-id="99028-136">**Height**</span></span> | <span data-ttu-id="99028-137">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="99028-137">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="99028-138">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="99028-138">Required</span></span> | <span data-ttu-id="99028-139">Die Höhe des umgebenden Felds für das Element.</span><span class="sxs-lookup"><span data-stu-id="99028-139">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="99028-140">Eine beliebige nicht negative ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="99028-140">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="99028-141">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="99028-141">Element Information</span></span>



|              |                                                                 |
|--------------|-----------------------------------------------------------------|
| <span data-ttu-id="99028-142">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="99028-142">Element type</span></span> | <span data-ttu-id="99028-143">ComplexType " [**groupnodetype**](groupnodetype-complex-type.md) "</span><span class="sxs-lookup"><span data-stu-id="99028-143">[**GroupNodeType**](groupnodetype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="99028-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="99028-144">Namespace</span></span>    | <span data-ttu-id="99028-145">urn: Schemas-Microsoft-com: TabletPC: RichInk</span><span class="sxs-lookup"><span data-stu-id="99028-145">urn:schemas-microsoft-com:tabletpc:richink</span></span>                      |
| <span data-ttu-id="99028-146">Schemaname</span><span class="sxs-lookup"><span data-stu-id="99028-146">Schema name</span></span>  | <span data-ttu-id="99028-147">Journal Leser</span><span class="sxs-lookup"><span data-stu-id="99028-147">Journal Reader</span></span>                                                  |



 

 

 



