---
description: Enthält einen Absatz.
ms.assetid: 60322907-3902-49a9-91a9-e00b0a714c00
title: Paragraph-Element (Windows.ui.xaml.documents.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Paragraph
api_type:
- HeaderDef
api_location:
- windows.ui.xaml.documents.h
ms.openlocfilehash: 2f246294c80814ec809c0a1ca035fcb4741c30c5
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432232"
---
# <a name="paragraph-element"></a><span data-ttu-id="ebd11-103">Paragraph-Element</span><span class="sxs-lookup"><span data-stu-id="ebd11-103">Paragraph Element</span></span>

<span data-ttu-id="ebd11-104">Enthält einen Absatz.</span><span class="sxs-lookup"><span data-stu-id="ebd11-104">Contains a paragraph.</span></span>

## <a name="definition"></a><span data-ttu-id="ebd11-105">Definition</span><span class="sxs-lookup"><span data-stu-id="ebd11-105">Definition</span></span>

``` syntax
<xs:element name="Paragraph" type="ParagraphType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a><span data-ttu-id="ebd11-106">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ebd11-106">Parent Elements</span></span>

[<span data-ttu-id="ebd11-107">**Inhalt**</span><span class="sxs-lookup"><span data-stu-id="ebd11-107">**Content**</span></span>](content-element--journal-reader.md)

[<span data-ttu-id="ebd11-108">**GroupNode**</span><span class="sxs-lookup"><span data-stu-id="ebd11-108">**GroupNode**</span></span>](groupnode-element.md)

## <a name="child-elements"></a><span data-ttu-id="ebd11-109">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ebd11-109">Child Elements</span></span>

[<span data-ttu-id="ebd11-110">**Linie**</span><span class="sxs-lookup"><span data-stu-id="ebd11-110">**Line**</span></span>](line-element.md)

[<span data-ttu-id="ebd11-111">**ParagraphLineMetrics**</span><span class="sxs-lookup"><span data-stu-id="ebd11-111">**ParagraphLineMetrics**</span></span>](paragraphlinemetrics-element.md)

## <a name="attributes"></a><span data-ttu-id="ebd11-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="ebd11-112">Attributes</span></span>



| <span data-ttu-id="ebd11-113">attribute</span><span class="sxs-lookup"><span data-stu-id="ebd11-113">Attribute</span></span>       | <span data-ttu-id="ebd11-114">Typ</span><span class="sxs-lookup"><span data-stu-id="ebd11-114">Type</span></span>                      | <span data-ttu-id="ebd11-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="ebd11-115">Required</span></span> | <span data-ttu-id="ebd11-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ebd11-116">Description</span></span>                                                                             | <span data-ttu-id="ebd11-117">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="ebd11-117">Possible Values</span></span>           |
|-----------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="ebd11-118">**Left**</span><span class="sxs-lookup"><span data-stu-id="ebd11-118">**Left**</span></span>        | <span data-ttu-id="ebd11-119">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="ebd11-119">**xs:integer**</span></span>            | <span data-ttu-id="ebd11-120">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="ebd11-120">Required</span></span> | <span data-ttu-id="ebd11-121">Der Abstand zwischen dem Ursprung und dem äußersten linken Punkt im Begrenzungsfeld für das Element.</span><span class="sxs-lookup"><span data-stu-id="ebd11-121">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="ebd11-122">Eine beliebige ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="ebd11-122">Any integer.</span></span>              |
| <span data-ttu-id="ebd11-123">**Top**</span><span class="sxs-lookup"><span data-stu-id="ebd11-123">**Top**</span></span>         | <span data-ttu-id="ebd11-124">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="ebd11-124">**xs:integer**</span></span>            | <span data-ttu-id="ebd11-125">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="ebd11-125">Required</span></span> | <span data-ttu-id="ebd11-126">Der Abstand zwischen dem Ursprung und dem obersten Punkt im Begrenzungsfeld für das Element.</span><span class="sxs-lookup"><span data-stu-id="ebd11-126">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="ebd11-127">Eine beliebige ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="ebd11-127">Any integer.</span></span>              |
| <span data-ttu-id="ebd11-128">**Width**</span><span class="sxs-lookup"><span data-stu-id="ebd11-128">**Width**</span></span>       | <span data-ttu-id="ebd11-129">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="ebd11-129">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="ebd11-130">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="ebd11-130">Required</span></span> | <span data-ttu-id="ebd11-131">Die Breite des Begrenzungsfelds für das Element.</span><span class="sxs-lookup"><span data-stu-id="ebd11-131">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="ebd11-132">Eine nicht negative ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="ebd11-132">Any non-negative integer.</span></span> |
| <span data-ttu-id="ebd11-133">**Height**</span><span class="sxs-lookup"><span data-stu-id="ebd11-133">**Height**</span></span>      | <span data-ttu-id="ebd11-134">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="ebd11-134">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="ebd11-135">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="ebd11-135">Required</span></span> | <span data-ttu-id="ebd11-136">Die Höhe des Begrenzungsfelds für das Element.</span><span class="sxs-lookup"><span data-stu-id="ebd11-136">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="ebd11-137">Eine nicht negative ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="ebd11-137">Any non-negative integer.</span></span> |
| <span data-ttu-id="ebd11-138">**BlockNumber**</span><span class="sxs-lookup"><span data-stu-id="ebd11-138">**BlockNumber**</span></span> | <span data-ttu-id="ebd11-139">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="ebd11-139">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="ebd11-140">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="ebd11-140">Required</span></span> | <span data-ttu-id="ebd11-141">Blocknummer.</span><span class="sxs-lookup"><span data-stu-id="ebd11-141">Block number.</span></span>                                                                           | <span data-ttu-id="ebd11-142">Eine nicht negative ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="ebd11-142">Any non-negative integer.</span></span> |
| <span data-ttu-id="ebd11-143">**LineNumber**</span><span class="sxs-lookup"><span data-stu-id="ebd11-143">**LineNumber**</span></span>  | <span data-ttu-id="ebd11-144">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="ebd11-144">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="ebd11-145">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="ebd11-145">Required</span></span> | <span data-ttu-id="ebd11-146">Die Zeile, in der der Absatz beginnt.</span><span class="sxs-lookup"><span data-stu-id="ebd11-146">The line on which the paragraph begins.</span></span>                                                 | <span data-ttu-id="ebd11-147">Eine nicht negative ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="ebd11-147">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="ebd11-148">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="ebd11-148">Element Information</span></span>



|  <span data-ttu-id="ebd11-149">Element</span><span class="sxs-lookup"><span data-stu-id="ebd11-149">Element</span></span>     | <span data-ttu-id="ebd11-150">Wert</span><span class="sxs-lookup"><span data-stu-id="ebd11-150">Value</span></span>                                                     |
|--------------|-----------------------------------------------------------------|
| <span data-ttu-id="ebd11-151">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="ebd11-151">Element type</span></span> | <span data-ttu-id="ebd11-152">[**complexType: ParagraphType**](paragraphtype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="ebd11-152">[**ParagraphType**](paragraphtype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="ebd11-153">Namespace</span><span class="sxs-lookup"><span data-stu-id="ebd11-153">Namespace</span></span>    | <span data-ttu-id="ebd11-154">urn:schemas-microsoft-com:tabletpc:richink</span><span class="sxs-lookup"><span data-stu-id="ebd11-154">urn:schemas-microsoft-com:tabletpc:richink</span></span>                      |
| <span data-ttu-id="ebd11-155">Schemaname</span><span class="sxs-lookup"><span data-stu-id="ebd11-155">Schema name</span></span>  | <span data-ttu-id="ebd11-156">Journalreader</span><span class="sxs-lookup"><span data-stu-id="ebd11-156">Journal Reader</span></span>                                                  |



 

## <a name="requirements"></a><span data-ttu-id="ebd11-157">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="ebd11-157">Requirements</span></span>



| <span data-ttu-id="ebd11-158">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ebd11-158">Requirement</span></span> | <span data-ttu-id="ebd11-159">Wert</span><span class="sxs-lookup"><span data-stu-id="ebd11-159">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ebd11-160">Header</span><span class="sxs-lookup"><span data-stu-id="ebd11-160">Header</span></span><br/> | <dl> <span data-ttu-id="ebd11-161"><dt>Windows.ui.xaml.documents.h</dt></span><span class="sxs-lookup"><span data-stu-id="ebd11-161"><dt>Windows.ui.xaml.documents.h</dt></span></span> </dl> |



 

 




