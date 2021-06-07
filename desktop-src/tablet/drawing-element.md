---
description: Enthält Inhalt, der vom Analysegerät oder vom Benutzer als Zeichnung klassifiziert wurde.
ms.assetid: 566542f3-b824-442d-9d8b-0064ebcf9b68
title: Drawing-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d87c0a3d8879fb5f3146c46c9c88d83a6e658d8
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432512"
---
# <a name="drawing-element"></a><span data-ttu-id="dd3a6-103">Drawing-Element</span><span class="sxs-lookup"><span data-stu-id="dd3a6-103">Drawing Element</span></span>

<span data-ttu-id="dd3a6-104">Enthält Inhalt, der vom Analysegerät oder vom Benutzer als Zeichnung klassifiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="dd3a6-104">Contains content that has been classified by the analyzer or the user as a drawing.</span></span>

## <a name="definition"></a><span data-ttu-id="dd3a6-105">Definition</span><span class="sxs-lookup"><span data-stu-id="dd3a6-105">Definition</span></span>

``` syntax
<xs:element name="Drawing" type="DrawingType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a><span data-ttu-id="dd3a6-106">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="dd3a6-106">Parent Elements</span></span>

[<span data-ttu-id="dd3a6-107">**Inhalt**</span><span class="sxs-lookup"><span data-stu-id="dd3a6-107">**Content**</span></span>](content-element--journal-reader.md)

[<span data-ttu-id="dd3a6-108">**GroupNode**</span><span class="sxs-lookup"><span data-stu-id="dd3a6-108">**GroupNode**</span></span>](groupnode-element.md)

## <a name="child-elements"></a><span data-ttu-id="dd3a6-109">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="dd3a6-109">Child Elements</span></span>

[<span data-ttu-id="dd3a6-110">**ScalarTransform**</span><span class="sxs-lookup"><span data-stu-id="dd3a6-110">**ScalarTransform**</span></span>](scalartransform-element.md)

[<span data-ttu-id="dd3a6-111">**CanReClassify**</span><span class="sxs-lookup"><span data-stu-id="dd3a6-111">**CanReClassify**</span></span>](canreclassify-element.md)

[<span data-ttu-id="dd3a6-112">**InkClass**</span><span class="sxs-lookup"><span data-stu-id="dd3a6-112">**InkClass**</span></span>](inkclass-element.md)

[<span data-ttu-id="dd3a6-113">**InkObject**</span><span class="sxs-lookup"><span data-stu-id="dd3a6-113">**InkObject**</span></span>](inkobject-element.md)

## <a name="attributes"></a><span data-ttu-id="dd3a6-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="dd3a6-114">Attributes</span></span>



| <span data-ttu-id="dd3a6-115">attribute</span><span class="sxs-lookup"><span data-stu-id="dd3a6-115">Attribute</span></span>  | <span data-ttu-id="dd3a6-116">Typ</span><span class="sxs-lookup"><span data-stu-id="dd3a6-116">Type</span></span>                      | <span data-ttu-id="dd3a6-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="dd3a6-117">Required</span></span> | <span data-ttu-id="dd3a6-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dd3a6-118">Description</span></span>                                                                             | <span data-ttu-id="dd3a6-119">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="dd3a6-119">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="dd3a6-120">**Left**</span><span class="sxs-lookup"><span data-stu-id="dd3a6-120">**Left**</span></span>   | <span data-ttu-id="dd3a6-121">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="dd3a6-121">**xs:integer**</span></span>            | <span data-ttu-id="dd3a6-122">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="dd3a6-122">Required</span></span> | <span data-ttu-id="dd3a6-123">Der Abstand zwischen dem Ursprung und dem äußersten linken Punkt im Begrenzungsfeld für das Element.</span><span class="sxs-lookup"><span data-stu-id="dd3a6-123">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="dd3a6-124">Eine beliebige ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="dd3a6-124">Any integer.</span></span>              |
| <span data-ttu-id="dd3a6-125">**Top**</span><span class="sxs-lookup"><span data-stu-id="dd3a6-125">**Top**</span></span>    | <span data-ttu-id="dd3a6-126">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="dd3a6-126">**xs:integer**</span></span>            | <span data-ttu-id="dd3a6-127">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="dd3a6-127">Required</span></span> | <span data-ttu-id="dd3a6-128">Der Abstand zwischen dem Ursprung und dem obersten Punkt im Begrenzungsfeld für das Element.</span><span class="sxs-lookup"><span data-stu-id="dd3a6-128">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="dd3a6-129">Eine beliebige ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="dd3a6-129">Any integer.</span></span>              |
| <span data-ttu-id="dd3a6-130">**Width**</span><span class="sxs-lookup"><span data-stu-id="dd3a6-130">**Width**</span></span>  | <span data-ttu-id="dd3a6-131">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="dd3a6-131">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="dd3a6-132">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="dd3a6-132">Required</span></span> | <span data-ttu-id="dd3a6-133">Die Breite des Begrenzungsfelds für das Element.</span><span class="sxs-lookup"><span data-stu-id="dd3a6-133">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="dd3a6-134">Eine nicht negative ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="dd3a6-134">Any non-negative integer.</span></span> |
| <span data-ttu-id="dd3a6-135">**Height**</span><span class="sxs-lookup"><span data-stu-id="dd3a6-135">**Height**</span></span> | <span data-ttu-id="dd3a6-136">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="dd3a6-136">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="dd3a6-137">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="dd3a6-137">Required</span></span> | <span data-ttu-id="dd3a6-138">Die Höhe des Begrenzungsfelds für das Element.</span><span class="sxs-lookup"><span data-stu-id="dd3a6-138">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="dd3a6-139">Eine nicht negative ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="dd3a6-139">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="dd3a6-140">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="dd3a6-140">Element Information</span></span>



|  <span data-ttu-id="dd3a6-141">Element</span><span class="sxs-lookup"><span data-stu-id="dd3a6-141">Element</span></span>     | <span data-ttu-id="dd3a6-142">Wert</span><span class="sxs-lookup"><span data-stu-id="dd3a6-142">Value</span></span>                                                     |
|--------------|-------------------------------------------------------------|
| <span data-ttu-id="dd3a6-143">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="dd3a6-143">Element type</span></span> | <span data-ttu-id="dd3a6-144">[**complexType: DrawingType**](drawingtype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="dd3a6-144">[**DrawingType**](drawingtype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="dd3a6-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="dd3a6-145">Namespace</span></span>    | <span data-ttu-id="dd3a6-146">urn:schemas-microsoft-com:tabletpc:richink</span><span class="sxs-lookup"><span data-stu-id="dd3a6-146">urn:schemas-microsoft-com:tabletpc:richink</span></span>                  |
| <span data-ttu-id="dd3a6-147">Schemaname</span><span class="sxs-lookup"><span data-stu-id="dd3a6-147">Schema name</span></span>  | <span data-ttu-id="dd3a6-148">Journalreader</span><span class="sxs-lookup"><span data-stu-id="dd3a6-148">Journal Reader</span></span>                                              |



 

 

 



