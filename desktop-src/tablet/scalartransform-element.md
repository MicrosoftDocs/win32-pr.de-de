---
description: Skalare Transformation, die von der Zeichnung oder InkWord verwendet wird.
ms.assetid: 88fc3b90-9ec6-41c0-9267-ed5b585ea07b
title: Scalartransform-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f5853c0fab76cd5a4857ae0235127a2fe103872
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355338"
---
# <a name="scalartransform-element"></a><span data-ttu-id="ac6aa-103">Scalartransform-Element</span><span class="sxs-lookup"><span data-stu-id="ac6aa-103">ScalarTransform Element</span></span>

<span data-ttu-id="ac6aa-104">Skalare Transformation, die von der [**Zeichnung**](drawing-element.md) oder [**InkWord**](inkword-element.md)verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ac6aa-104">Scalar transform used by the [**Drawing**](drawing-element.md) or [**InkWord**](inkword-element.md).</span></span>

## <a name="definition"></a><span data-ttu-id="ac6aa-105">Definition</span><span class="sxs-lookup"><span data-stu-id="ac6aa-105">Definition</span></span>

``` syntax
<xs:element name="ScalarTransform" minOccurs="0" type="ScalarTransformType" />
```

## <a name="parent-elements"></a><span data-ttu-id="ac6aa-106">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ac6aa-106">Parent Elements</span></span>

[<span data-ttu-id="ac6aa-107">**Zeichnung**</span><span class="sxs-lookup"><span data-stu-id="ac6aa-107">**Drawing**</span></span>](drawing-element.md)

[<span data-ttu-id="ac6aa-108">**InkWord**</span><span class="sxs-lookup"><span data-stu-id="ac6aa-108">**InkWord**</span></span>](inkword-element.md)

## <a name="child-elements"></a><span data-ttu-id="ac6aa-109">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ac6aa-109">Child Elements</span></span>

<span data-ttu-id="ac6aa-110">Keine</span><span class="sxs-lookup"><span data-stu-id="ac6aa-110">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="ac6aa-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="ac6aa-111">Attributes</span></span>



| <span data-ttu-id="ac6aa-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="ac6aa-112">Attribute</span></span> | <span data-ttu-id="ac6aa-113">type</span><span class="sxs-lookup"><span data-stu-id="ac6aa-113">Type</span></span>           | <span data-ttu-id="ac6aa-114">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="ac6aa-114">Required</span></span> | <span data-ttu-id="ac6aa-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ac6aa-115">Description</span></span> | <span data-ttu-id="ac6aa-116">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="ac6aa-116">Possible Values</span></span>     |
|-----------|----------------|----------|-------------|---------------------|
| <span data-ttu-id="ac6aa-117">**Mat1**</span><span class="sxs-lookup"><span data-stu-id="ac6aa-117">**Mat1**</span></span>  | <span data-ttu-id="ac6aa-118">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="ac6aa-118">**xs:decimal**</span></span> | <span data-ttu-id="ac6aa-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="ac6aa-119">Required</span></span> |             | <span data-ttu-id="ac6aa-120">Eine beliebige Dezimalzahl.</span><span class="sxs-lookup"><span data-stu-id="ac6aa-120">Any decimal number.</span></span> |
| <span data-ttu-id="ac6aa-121">**Mat2**</span><span class="sxs-lookup"><span data-stu-id="ac6aa-121">**Mat2**</span></span>  | <span data-ttu-id="ac6aa-122">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="ac6aa-122">**xs:decimal**</span></span> | <span data-ttu-id="ac6aa-123">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="ac6aa-123">Required</span></span> |             | <span data-ttu-id="ac6aa-124">Eine beliebige Dezimalzahl.</span><span class="sxs-lookup"><span data-stu-id="ac6aa-124">Any decimal number.</span></span> |
| <span data-ttu-id="ac6aa-125">**Mat3**</span><span class="sxs-lookup"><span data-stu-id="ac6aa-125">**Mat3**</span></span>  | <span data-ttu-id="ac6aa-126">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="ac6aa-126">**xs:decimal**</span></span> | <span data-ttu-id="ac6aa-127">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="ac6aa-127">Required</span></span> |             | <span data-ttu-id="ac6aa-128">Eine beliebige Dezimalzahl.</span><span class="sxs-lookup"><span data-stu-id="ac6aa-128">Any decimal number.</span></span> |
| <span data-ttu-id="ac6aa-129">**Mat4**</span><span class="sxs-lookup"><span data-stu-id="ac6aa-129">**Mat4**</span></span>  | <span data-ttu-id="ac6aa-130">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="ac6aa-130">**xs:decimal**</span></span> | <span data-ttu-id="ac6aa-131">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="ac6aa-131">Required</span></span> |             | <span data-ttu-id="ac6aa-132">Eine beliebige Dezimalzahl.</span><span class="sxs-lookup"><span data-stu-id="ac6aa-132">Any decimal number.</span></span> |
| <span data-ttu-id="ac6aa-133">**Mat5**</span><span class="sxs-lookup"><span data-stu-id="ac6aa-133">**Mat5**</span></span>  | <span data-ttu-id="ac6aa-134">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="ac6aa-134">**xs:decimal**</span></span> | <span data-ttu-id="ac6aa-135">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="ac6aa-135">Required</span></span> |             | <span data-ttu-id="ac6aa-136">Eine beliebige Dezimalzahl.</span><span class="sxs-lookup"><span data-stu-id="ac6aa-136">Any decimal number.</span></span> |
| <span data-ttu-id="ac6aa-137">**Mat6**</span><span class="sxs-lookup"><span data-stu-id="ac6aa-137">**Mat6**</span></span>  | <span data-ttu-id="ac6aa-138">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="ac6aa-138">**xs:decimal**</span></span> | <span data-ttu-id="ac6aa-139">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="ac6aa-139">Required</span></span> |             | <span data-ttu-id="ac6aa-140">Eine beliebige Dezimalzahl.</span><span class="sxs-lookup"><span data-stu-id="ac6aa-140">Any decimal number.</span></span> |
| <span data-ttu-id="ac6aa-141">**Mat7**</span><span class="sxs-lookup"><span data-stu-id="ac6aa-141">**Mat7**</span></span>  | <span data-ttu-id="ac6aa-142">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="ac6aa-142">**xs:decimal**</span></span> | <span data-ttu-id="ac6aa-143">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="ac6aa-143">Required</span></span> |             | <span data-ttu-id="ac6aa-144">Eine beliebige Dezimalzahl.</span><span class="sxs-lookup"><span data-stu-id="ac6aa-144">Any decimal number.</span></span> |
| <span data-ttu-id="ac6aa-145">**Mat8**</span><span class="sxs-lookup"><span data-stu-id="ac6aa-145">**Mat8**</span></span>  | <span data-ttu-id="ac6aa-146">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="ac6aa-146">**xs:decimal**</span></span> | <span data-ttu-id="ac6aa-147">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="ac6aa-147">Required</span></span> |             | <span data-ttu-id="ac6aa-148">Eine beliebige Dezimalzahl.</span><span class="sxs-lookup"><span data-stu-id="ac6aa-148">Any decimal number.</span></span> |
| <span data-ttu-id="ac6aa-149">**Mat9**</span><span class="sxs-lookup"><span data-stu-id="ac6aa-149">**Mat9**</span></span>  | <span data-ttu-id="ac6aa-150">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="ac6aa-150">**xs:decimal**</span></span> | <span data-ttu-id="ac6aa-151">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="ac6aa-151">Required</span></span> |             | <span data-ttu-id="ac6aa-152">Eine beliebige Dezimalzahl.</span><span class="sxs-lookup"><span data-stu-id="ac6aa-152">Any decimal number.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="ac6aa-153">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="ac6aa-153">Element Information</span></span>



|              |                                                                             |
|--------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="ac6aa-154">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="ac6aa-154">Element type</span></span> | <span data-ttu-id="ac6aa-155">ComplexType " [**scalartransformtype**](scalartransformtype-complex-type.md) "</span><span class="sxs-lookup"><span data-stu-id="ac6aa-155">[**ScalarTransformType**](scalartransformtype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="ac6aa-156">Namespace</span><span class="sxs-lookup"><span data-stu-id="ac6aa-156">Namespace</span></span>    | <span data-ttu-id="ac6aa-157">urn: Schemas-Microsoft-com: TabletPC: RichInk</span><span class="sxs-lookup"><span data-stu-id="ac6aa-157">urn:schemas-microsoft-com:tabletpc:richink</span></span>                                  |
| <span data-ttu-id="ac6aa-158">Schemaname</span><span class="sxs-lookup"><span data-stu-id="ac6aa-158">Schema name</span></span>  | <span data-ttu-id="ac6aa-159">Journal Leser</span><span class="sxs-lookup"><span data-stu-id="ac6aa-159">Journal Reader</span></span>                                                              |



 

 

 



