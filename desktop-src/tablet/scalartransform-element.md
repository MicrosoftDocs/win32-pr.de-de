---
description: Skalartransformation, die vom Zeichnen oder InkWord verwendet wird.
ms.assetid: 88fc3b90-9ec6-41c0-9267-ed5b585ea07b
title: ScalarTransform-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91ed5f7d3b44456522b45c7243b15390b7c52433
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432432"
---
# <a name="scalartransform-element"></a><span data-ttu-id="8bf5b-103">ScalarTransform-Element</span><span class="sxs-lookup"><span data-stu-id="8bf5b-103">ScalarTransform Element</span></span>

<span data-ttu-id="8bf5b-104">Skalartransformation, die von [**der Zeichnung oder**](drawing-element.md) von [**InkWord verwendet wird.**](inkword-element.md)</span><span class="sxs-lookup"><span data-stu-id="8bf5b-104">Scalar transform used by the [**Drawing**](drawing-element.md) or [**InkWord**](inkword-element.md).</span></span>

## <a name="definition"></a><span data-ttu-id="8bf5b-105">Definition</span><span class="sxs-lookup"><span data-stu-id="8bf5b-105">Definition</span></span>

``` syntax
<xs:element name="ScalarTransform" minOccurs="0" type="ScalarTransformType" />
```

## <a name="parent-elements"></a><span data-ttu-id="8bf5b-106">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8bf5b-106">Parent Elements</span></span>

[<span data-ttu-id="8bf5b-107">**Zeichnung**</span><span class="sxs-lookup"><span data-stu-id="8bf5b-107">**Drawing**</span></span>](drawing-element.md)

[<span data-ttu-id="8bf5b-108">**InkWord**</span><span class="sxs-lookup"><span data-stu-id="8bf5b-108">**InkWord**</span></span>](inkword-element.md)

## <a name="child-elements"></a><span data-ttu-id="8bf5b-109">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8bf5b-109">Child Elements</span></span>

<span data-ttu-id="8bf5b-110">Keine</span><span class="sxs-lookup"><span data-stu-id="8bf5b-110">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="8bf5b-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="8bf5b-111">Attributes</span></span>



| <span data-ttu-id="8bf5b-112">attribute</span><span class="sxs-lookup"><span data-stu-id="8bf5b-112">Attribute</span></span> | <span data-ttu-id="8bf5b-113">Typ</span><span class="sxs-lookup"><span data-stu-id="8bf5b-113">Type</span></span>           | <span data-ttu-id="8bf5b-114">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="8bf5b-114">Required</span></span> | <span data-ttu-id="8bf5b-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8bf5b-115">Description</span></span> | <span data-ttu-id="8bf5b-116">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="8bf5b-116">Possible Values</span></span>     |
|-----------|----------------|----------|-------------|---------------------|
| <span data-ttu-id="8bf5b-117">**Mat1**</span><span class="sxs-lookup"><span data-stu-id="8bf5b-117">**Mat1**</span></span>  | <span data-ttu-id="8bf5b-118">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="8bf5b-118">**xs:decimal**</span></span> | <span data-ttu-id="8bf5b-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="8bf5b-119">Required</span></span> |             | <span data-ttu-id="8bf5b-120">Eine beliebige Dezimalzahl.</span><span class="sxs-lookup"><span data-stu-id="8bf5b-120">Any decimal number.</span></span> |
| <span data-ttu-id="8bf5b-121">**Mat2**</span><span class="sxs-lookup"><span data-stu-id="8bf5b-121">**Mat2**</span></span>  | <span data-ttu-id="8bf5b-122">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="8bf5b-122">**xs:decimal**</span></span> | <span data-ttu-id="8bf5b-123">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="8bf5b-123">Required</span></span> |             | <span data-ttu-id="8bf5b-124">Eine beliebige Dezimalzahl.</span><span class="sxs-lookup"><span data-stu-id="8bf5b-124">Any decimal number.</span></span> |
| <span data-ttu-id="8bf5b-125">**Mat3**</span><span class="sxs-lookup"><span data-stu-id="8bf5b-125">**Mat3**</span></span>  | <span data-ttu-id="8bf5b-126">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="8bf5b-126">**xs:decimal**</span></span> | <span data-ttu-id="8bf5b-127">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="8bf5b-127">Required</span></span> |             | <span data-ttu-id="8bf5b-128">Eine beliebige Dezimalzahl.</span><span class="sxs-lookup"><span data-stu-id="8bf5b-128">Any decimal number.</span></span> |
| <span data-ttu-id="8bf5b-129">**Mat4**</span><span class="sxs-lookup"><span data-stu-id="8bf5b-129">**Mat4**</span></span>  | <span data-ttu-id="8bf5b-130">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="8bf5b-130">**xs:decimal**</span></span> | <span data-ttu-id="8bf5b-131">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="8bf5b-131">Required</span></span> |             | <span data-ttu-id="8bf5b-132">Eine beliebige Dezimalzahl.</span><span class="sxs-lookup"><span data-stu-id="8bf5b-132">Any decimal number.</span></span> |
| <span data-ttu-id="8bf5b-133">**Mat5**</span><span class="sxs-lookup"><span data-stu-id="8bf5b-133">**Mat5**</span></span>  | <span data-ttu-id="8bf5b-134">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="8bf5b-134">**xs:decimal**</span></span> | <span data-ttu-id="8bf5b-135">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="8bf5b-135">Required</span></span> |             | <span data-ttu-id="8bf5b-136">Eine beliebige Dezimalzahl.</span><span class="sxs-lookup"><span data-stu-id="8bf5b-136">Any decimal number.</span></span> |
| <span data-ttu-id="8bf5b-137">**Mat6**</span><span class="sxs-lookup"><span data-stu-id="8bf5b-137">**Mat6**</span></span>  | <span data-ttu-id="8bf5b-138">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="8bf5b-138">**xs:decimal**</span></span> | <span data-ttu-id="8bf5b-139">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="8bf5b-139">Required</span></span> |             | <span data-ttu-id="8bf5b-140">Eine beliebige Dezimalzahl.</span><span class="sxs-lookup"><span data-stu-id="8bf5b-140">Any decimal number.</span></span> |
| <span data-ttu-id="8bf5b-141">**Mat7**</span><span class="sxs-lookup"><span data-stu-id="8bf5b-141">**Mat7**</span></span>  | <span data-ttu-id="8bf5b-142">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="8bf5b-142">**xs:decimal**</span></span> | <span data-ttu-id="8bf5b-143">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="8bf5b-143">Required</span></span> |             | <span data-ttu-id="8bf5b-144">Eine beliebige Dezimalzahl.</span><span class="sxs-lookup"><span data-stu-id="8bf5b-144">Any decimal number.</span></span> |
| <span data-ttu-id="8bf5b-145">**Mat8**</span><span class="sxs-lookup"><span data-stu-id="8bf5b-145">**Mat8**</span></span>  | <span data-ttu-id="8bf5b-146">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="8bf5b-146">**xs:decimal**</span></span> | <span data-ttu-id="8bf5b-147">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="8bf5b-147">Required</span></span> |             | <span data-ttu-id="8bf5b-148">Eine beliebige Dezimalzahl.</span><span class="sxs-lookup"><span data-stu-id="8bf5b-148">Any decimal number.</span></span> |
| <span data-ttu-id="8bf5b-149">**Mat9**</span><span class="sxs-lookup"><span data-stu-id="8bf5b-149">**Mat9**</span></span>  | <span data-ttu-id="8bf5b-150">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="8bf5b-150">**xs:decimal**</span></span> | <span data-ttu-id="8bf5b-151">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="8bf5b-151">Required</span></span> |             | <span data-ttu-id="8bf5b-152">Eine beliebige Dezimalzahl.</span><span class="sxs-lookup"><span data-stu-id="8bf5b-152">Any decimal number.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="8bf5b-153">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="8bf5b-153">Element Information</span></span>



| <span data-ttu-id="8bf5b-154">Element</span><span class="sxs-lookup"><span data-stu-id="8bf5b-154">Element</span></span>      | <span data-ttu-id="8bf5b-155">Wert</span><span class="sxs-lookup"><span data-stu-id="8bf5b-155">Value</span></span>                                                                       |
|--------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="8bf5b-156">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="8bf5b-156">Element type</span></span> | <span data-ttu-id="8bf5b-157">[**complexType: ScalarTransformType**](scalartransformtype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="8bf5b-157">[**ScalarTransformType**](scalartransformtype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="8bf5b-158">Namespace</span><span class="sxs-lookup"><span data-stu-id="8bf5b-158">Namespace</span></span>    | <span data-ttu-id="8bf5b-159">urn:schemas-microsoft-com:tabletpc:richink</span><span class="sxs-lookup"><span data-stu-id="8bf5b-159">urn:schemas-microsoft-com:tabletpc:richink</span></span>                                  |
| <span data-ttu-id="8bf5b-160">Schemaname</span><span class="sxs-lookup"><span data-stu-id="8bf5b-160">Schema name</span></span>  | <span data-ttu-id="8bf5b-161">Journalreader</span><span class="sxs-lookup"><span data-stu-id="8bf5b-161">Journal Reader</span></span>                                                              |



 

 

 



