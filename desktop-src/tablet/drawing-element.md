---
description: Enthält Inhalte, die vom Analyzer oder vom Benutzer als Zeichnung klassifiziert wurden.
ms.assetid: 566542f3-b824-442d-9d8b-0064ebcf9b68
title: Drawing-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe516a4ba33e6e597b17ce8365d792f19468c3b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350979"
---
# <a name="drawing-element"></a><span data-ttu-id="0f8ad-103">Drawing-Element</span><span class="sxs-lookup"><span data-stu-id="0f8ad-103">Drawing Element</span></span>

<span data-ttu-id="0f8ad-104">Enthält Inhalte, die vom Analyzer oder vom Benutzer als Zeichnung klassifiziert wurden.</span><span class="sxs-lookup"><span data-stu-id="0f8ad-104">Contains content that has been classified by the analyzer or the user as a drawing.</span></span>

## <a name="definition"></a><span data-ttu-id="0f8ad-105">Definition</span><span class="sxs-lookup"><span data-stu-id="0f8ad-105">Definition</span></span>

``` syntax
<xs:element name="Drawing" type="DrawingType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a><span data-ttu-id="0f8ad-106">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0f8ad-106">Parent Elements</span></span>

[<span data-ttu-id="0f8ad-107">**Inhalt**</span><span class="sxs-lookup"><span data-stu-id="0f8ad-107">**Content**</span></span>](content-element--journal-reader.md)

[<span data-ttu-id="0f8ad-108">**-Gruppenknoten**</span><span class="sxs-lookup"><span data-stu-id="0f8ad-108">**GroupNode**</span></span>](groupnode-element.md)

## <a name="child-elements"></a><span data-ttu-id="0f8ad-109">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0f8ad-109">Child Elements</span></span>

[<span data-ttu-id="0f8ad-110">**Scalartransform**</span><span class="sxs-lookup"><span data-stu-id="0f8ad-110">**ScalarTransform**</span></span>](scalartransform-element.md)

[<span data-ttu-id="0f8ad-111">**Canreclassify**</span><span class="sxs-lookup"><span data-stu-id="0f8ad-111">**CanReClassify**</span></span>](canreclassify-element.md)

[<span data-ttu-id="0f8ad-112">**Inkclass**</span><span class="sxs-lookup"><span data-stu-id="0f8ad-112">**InkClass**</span></span>](inkclass-element.md)

[<span data-ttu-id="0f8ad-113">**Inkobject**</span><span class="sxs-lookup"><span data-stu-id="0f8ad-113">**InkObject**</span></span>](inkobject-element.md)

## <a name="attributes"></a><span data-ttu-id="0f8ad-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="0f8ad-114">Attributes</span></span>



| <span data-ttu-id="0f8ad-115">Attribut</span><span class="sxs-lookup"><span data-stu-id="0f8ad-115">Attribute</span></span>  | <span data-ttu-id="0f8ad-116">type</span><span class="sxs-lookup"><span data-stu-id="0f8ad-116">Type</span></span>                      | <span data-ttu-id="0f8ad-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="0f8ad-117">Required</span></span> | <span data-ttu-id="0f8ad-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0f8ad-118">Description</span></span>                                                                             | <span data-ttu-id="0f8ad-119">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="0f8ad-119">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="0f8ad-120">**Left**</span><span class="sxs-lookup"><span data-stu-id="0f8ad-120">**Left**</span></span>   | <span data-ttu-id="0f8ad-121">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="0f8ad-121">**xs:integer**</span></span>            | <span data-ttu-id="0f8ad-122">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="0f8ad-122">Required</span></span> | <span data-ttu-id="0f8ad-123">Der Abstand zwischen dem Ursprung und dem äußersten äußersten linken Punkt im umgebenden Feld des Elements.</span><span class="sxs-lookup"><span data-stu-id="0f8ad-123">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="0f8ad-124">Eine beliebige ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="0f8ad-124">Any integer.</span></span>              |
| <span data-ttu-id="0f8ad-125">**Top**</span><span class="sxs-lookup"><span data-stu-id="0f8ad-125">**Top**</span></span>    | <span data-ttu-id="0f8ad-126">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="0f8ad-126">**xs:integer**</span></span>            | <span data-ttu-id="0f8ad-127">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="0f8ad-127">Required</span></span> | <span data-ttu-id="0f8ad-128">Der Abstand zwischen dem Ursprung und dem obersten Punkt im umgebenden Feld für das Element.</span><span class="sxs-lookup"><span data-stu-id="0f8ad-128">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="0f8ad-129">Eine beliebige ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="0f8ad-129">Any integer.</span></span>              |
| <span data-ttu-id="0f8ad-130">**Width**</span><span class="sxs-lookup"><span data-stu-id="0f8ad-130">**Width**</span></span>  | <span data-ttu-id="0f8ad-131">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="0f8ad-131">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="0f8ad-132">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="0f8ad-132">Required</span></span> | <span data-ttu-id="0f8ad-133">Die Breite des Begrenzungs Rahmens für das Element.</span><span class="sxs-lookup"><span data-stu-id="0f8ad-133">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="0f8ad-134">Eine beliebige nicht negative ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="0f8ad-134">Any non-negative integer.</span></span> |
| <span data-ttu-id="0f8ad-135">**Height**</span><span class="sxs-lookup"><span data-stu-id="0f8ad-135">**Height**</span></span> | <span data-ttu-id="0f8ad-136">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="0f8ad-136">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="0f8ad-137">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="0f8ad-137">Required</span></span> | <span data-ttu-id="0f8ad-138">Die Höhe des umgebenden Felds für das Element.</span><span class="sxs-lookup"><span data-stu-id="0f8ad-138">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="0f8ad-139">Eine beliebige nicht negative ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="0f8ad-139">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="0f8ad-140">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="0f8ad-140">Element Information</span></span>



|              |                                                             |
|--------------|-------------------------------------------------------------|
| <span data-ttu-id="0f8ad-141">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="0f8ad-141">Element type</span></span> | <span data-ttu-id="0f8ad-142">ComplexType für [**drawingtype**](drawingtype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="0f8ad-142">[**DrawingType**](drawingtype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="0f8ad-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="0f8ad-143">Namespace</span></span>    | <span data-ttu-id="0f8ad-144">urn: Schemas-Microsoft-com: TabletPC: RichInk</span><span class="sxs-lookup"><span data-stu-id="0f8ad-144">urn:schemas-microsoft-com:tabletpc:richink</span></span>                  |
| <span data-ttu-id="0f8ad-145">Schemaname</span><span class="sxs-lookup"><span data-stu-id="0f8ad-145">Schema name</span></span>  | <span data-ttu-id="0f8ad-146">Journal Leser</span><span class="sxs-lookup"><span data-stu-id="0f8ad-146">Journal Reader</span></span>                                              |



 

 

 



