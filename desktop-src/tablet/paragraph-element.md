---
description: Enthält einen Absatz.
ms.assetid: 60322907-3902-49a9-91a9-e00b0a714c00
title: Paragraph-Element (Windows.ui.xaml.doc. h)
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
ms.openlocfilehash: bfe3752541bb54571e9802f557e83dcc7632f845
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365169"
---
# <a name="paragraph-element"></a><span data-ttu-id="e029f-103">Paragraph-Element</span><span class="sxs-lookup"><span data-stu-id="e029f-103">Paragraph Element</span></span>

<span data-ttu-id="e029f-104">Enthält einen Absatz.</span><span class="sxs-lookup"><span data-stu-id="e029f-104">Contains a paragraph.</span></span>

## <a name="definition"></a><span data-ttu-id="e029f-105">Definition</span><span class="sxs-lookup"><span data-stu-id="e029f-105">Definition</span></span>

``` syntax
<xs:element name="Paragraph" type="ParagraphType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a><span data-ttu-id="e029f-106">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e029f-106">Parent Elements</span></span>

[<span data-ttu-id="e029f-107">**Inhalt**</span><span class="sxs-lookup"><span data-stu-id="e029f-107">**Content**</span></span>](content-element--journal-reader.md)

[<span data-ttu-id="e029f-108">**-Gruppenknoten**</span><span class="sxs-lookup"><span data-stu-id="e029f-108">**GroupNode**</span></span>](groupnode-element.md)

## <a name="child-elements"></a><span data-ttu-id="e029f-109">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e029f-109">Child Elements</span></span>

[<span data-ttu-id="e029f-110">**Stimmen**</span><span class="sxs-lookup"><span data-stu-id="e029f-110">**Line**</span></span>](line-element.md)

[<span data-ttu-id="e029f-111">**Knotenmetriken**</span><span class="sxs-lookup"><span data-stu-id="e029f-111">**ParagraphLineMetrics**</span></span>](paragraphlinemetrics-element.md)

## <a name="attributes"></a><span data-ttu-id="e029f-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="e029f-112">Attributes</span></span>



| <span data-ttu-id="e029f-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="e029f-113">Attribute</span></span>       | <span data-ttu-id="e029f-114">type</span><span class="sxs-lookup"><span data-stu-id="e029f-114">Type</span></span>                      | <span data-ttu-id="e029f-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="e029f-115">Required</span></span> | <span data-ttu-id="e029f-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e029f-116">Description</span></span>                                                                             | <span data-ttu-id="e029f-117">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="e029f-117">Possible Values</span></span>           |
|-----------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="e029f-118">**Left**</span><span class="sxs-lookup"><span data-stu-id="e029f-118">**Left**</span></span>        | <span data-ttu-id="e029f-119">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="e029f-119">**xs:integer**</span></span>            | <span data-ttu-id="e029f-120">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="e029f-120">Required</span></span> | <span data-ttu-id="e029f-121">Der Abstand zwischen dem Ursprung und dem äußersten äußersten linken Punkt im umgebenden Feld des Elements.</span><span class="sxs-lookup"><span data-stu-id="e029f-121">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="e029f-122">Eine beliebige ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="e029f-122">Any integer.</span></span>              |
| <span data-ttu-id="e029f-123">**Top**</span><span class="sxs-lookup"><span data-stu-id="e029f-123">**Top**</span></span>         | <span data-ttu-id="e029f-124">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="e029f-124">**xs:integer**</span></span>            | <span data-ttu-id="e029f-125">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="e029f-125">Required</span></span> | <span data-ttu-id="e029f-126">Der Abstand zwischen dem Ursprung und dem obersten Punkt im umgebenden Feld für das Element.</span><span class="sxs-lookup"><span data-stu-id="e029f-126">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="e029f-127">Eine beliebige ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="e029f-127">Any integer.</span></span>              |
| <span data-ttu-id="e029f-128">**Width**</span><span class="sxs-lookup"><span data-stu-id="e029f-128">**Width**</span></span>       | <span data-ttu-id="e029f-129">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="e029f-129">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="e029f-130">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="e029f-130">Required</span></span> | <span data-ttu-id="e029f-131">Die Breite des Begrenzungs Rahmens für das Element.</span><span class="sxs-lookup"><span data-stu-id="e029f-131">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="e029f-132">Eine beliebige nicht negative ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="e029f-132">Any non-negative integer.</span></span> |
| <span data-ttu-id="e029f-133">**Height**</span><span class="sxs-lookup"><span data-stu-id="e029f-133">**Height**</span></span>      | <span data-ttu-id="e029f-134">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="e029f-134">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="e029f-135">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="e029f-135">Required</span></span> | <span data-ttu-id="e029f-136">Die Höhe des umgebenden Felds für das Element.</span><span class="sxs-lookup"><span data-stu-id="e029f-136">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="e029f-137">Eine beliebige nicht negative ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="e029f-137">Any non-negative integer.</span></span> |
| <span data-ttu-id="e029f-138">**BlockNumber**</span><span class="sxs-lookup"><span data-stu-id="e029f-138">**BlockNumber**</span></span> | <span data-ttu-id="e029f-139">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="e029f-139">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="e029f-140">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="e029f-140">Required</span></span> | <span data-ttu-id="e029f-141">Block Nummer.</span><span class="sxs-lookup"><span data-stu-id="e029f-141">Block number.</span></span>                                                                           | <span data-ttu-id="e029f-142">Eine beliebige nicht negative ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="e029f-142">Any non-negative integer.</span></span> |
| <span data-ttu-id="e029f-143">**LineNumber**</span><span class="sxs-lookup"><span data-stu-id="e029f-143">**LineNumber**</span></span>  | <span data-ttu-id="e029f-144">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="e029f-144">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="e029f-145">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="e029f-145">Required</span></span> | <span data-ttu-id="e029f-146">Die Zeile, in der der Absatz beginnt.</span><span class="sxs-lookup"><span data-stu-id="e029f-146">The line on which the paragraph begins.</span></span>                                                 | <span data-ttu-id="e029f-147">Eine beliebige nicht negative ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="e029f-147">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="e029f-148">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="e029f-148">Element Information</span></span>



|              |                                                                 |
|--------------|-----------------------------------------------------------------|
| <span data-ttu-id="e029f-149">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="e029f-149">Element type</span></span> | <span data-ttu-id="e029f-150">ComplexType- [**Datentyp**](paragraphtype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="e029f-150">[**ParagraphType**](paragraphtype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="e029f-151">Namespace</span><span class="sxs-lookup"><span data-stu-id="e029f-151">Namespace</span></span>    | <span data-ttu-id="e029f-152">urn: Schemas-Microsoft-com: TabletPC: RichInk</span><span class="sxs-lookup"><span data-stu-id="e029f-152">urn:schemas-microsoft-com:tabletpc:richink</span></span>                      |
| <span data-ttu-id="e029f-153">Schemaname</span><span class="sxs-lookup"><span data-stu-id="e029f-153">Schema name</span></span>  | <span data-ttu-id="e029f-154">Journal Leser</span><span class="sxs-lookup"><span data-stu-id="e029f-154">Journal Reader</span></span>                                                  |



 

## <a name="requirements"></a><span data-ttu-id="e029f-155">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e029f-155">Requirements</span></span>



| <span data-ttu-id="e029f-156">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e029f-156">Requirement</span></span> | <span data-ttu-id="e029f-157">Wert</span><span class="sxs-lookup"><span data-stu-id="e029f-157">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e029f-158">Header</span><span class="sxs-lookup"><span data-stu-id="e029f-158">Header</span></span><br/> | <dl> <span data-ttu-id="e029f-159"><dt>Windows.ui.xaml.doc. h.</dt></span><span class="sxs-lookup"><span data-stu-id="e029f-159"><dt>Windows.ui.xaml.documents.h</dt></span></span> </dl> |



 

 




