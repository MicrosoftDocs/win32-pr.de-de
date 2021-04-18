---
description: Enthält Informationen über ein bestimmtes frei Hand Wort in der Journal Notiz, einschließlich Position, Alternativen und der eigentlichen frei Hand Daten.
ms.assetid: 1e197716-bf6c-4a28-ae66-38aa59d7371d
title: InkWord-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 179fb5e2bcce2e01f684f0b39d662e8538c7d27e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358526"
---
# <a name="inkword-element"></a><span data-ttu-id="17bde-103">InkWord-Element</span><span class="sxs-lookup"><span data-stu-id="17bde-103">InkWord Element</span></span>

<span data-ttu-id="17bde-104">Enthält Informationen über ein bestimmtes frei Hand Wort in der Journal Notiz, einschließlich Position, Alternativen und der eigentlichen frei Hand Daten.</span><span class="sxs-lookup"><span data-stu-id="17bde-104">Contains information about a given ink word in the Journal note, including position, alternates, and the actual ink data.</span></span>

## <a name="definition"></a><span data-ttu-id="17bde-105">Definition</span><span class="sxs-lookup"><span data-stu-id="17bde-105">Definition</span></span>

``` syntax
<xs:element name="InkWord" type="InkWordType" />
```

## <a name="parent-elements"></a><span data-ttu-id="17bde-106">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="17bde-106">Parent Elements</span></span>

[<span data-ttu-id="17bde-107">**-Gruppenknoten**</span><span class="sxs-lookup"><span data-stu-id="17bde-107">**GroupNode**</span></span>](groupnode-element.md)

[<span data-ttu-id="17bde-108">**Stimmen**</span><span class="sxs-lookup"><span data-stu-id="17bde-108">**Line**</span></span>](line-element.md)

## <a name="child-elements"></a><span data-ttu-id="17bde-109">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="17bde-109">Child Elements</span></span>

[<span data-ttu-id="17bde-110">**Scalartransform**</span><span class="sxs-lookup"><span data-stu-id="17bde-110">**ScalarTransform**</span></span>](scalartransform-element.md)

[<span data-ttu-id="17bde-111">**Alternative ist**</span><span class="sxs-lookup"><span data-stu-id="17bde-111">**AlternateList**</span></span>](alternatelist-element.md)

[<span data-ttu-id="17bde-112">**Canreclassify**</span><span class="sxs-lookup"><span data-stu-id="17bde-112">**CanReClassify**</span></span>](canreclassify-element.md)

[<span data-ttu-id="17bde-113">**Confidence**</span><span class="sxs-lookup"><span data-stu-id="17bde-113">**Confidence**</span></span>](confidence-element.md)

[<span data-ttu-id="17bde-114">**Inkobject**</span><span class="sxs-lookup"><span data-stu-id="17bde-114">**InkObject**</span></span>](inkobject-element.md)

## <a name="attributes"></a><span data-ttu-id="17bde-115">Attribute</span><span class="sxs-lookup"><span data-stu-id="17bde-115">Attributes</span></span>



| <span data-ttu-id="17bde-116">Attribut</span><span class="sxs-lookup"><span data-stu-id="17bde-116">Attribute</span></span>  | <span data-ttu-id="17bde-117">type</span><span class="sxs-lookup"><span data-stu-id="17bde-117">Type</span></span>                      | <span data-ttu-id="17bde-118">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="17bde-118">Required</span></span> | <span data-ttu-id="17bde-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="17bde-119">Description</span></span>                                                                             | <span data-ttu-id="17bde-120">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="17bde-120">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="17bde-121">**Left**</span><span class="sxs-lookup"><span data-stu-id="17bde-121">**Left**</span></span>   | <span data-ttu-id="17bde-122">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="17bde-122">**xs:integer**</span></span>            | <span data-ttu-id="17bde-123">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="17bde-123">Required</span></span> | <span data-ttu-id="17bde-124">Der Abstand zwischen dem Ursprung und dem äußersten äußersten linken Punkt im umgebenden Feld des Elements.</span><span class="sxs-lookup"><span data-stu-id="17bde-124">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="17bde-125">Eine beliebige ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="17bde-125">Any integer.</span></span>              |
| <span data-ttu-id="17bde-126">**Top**</span><span class="sxs-lookup"><span data-stu-id="17bde-126">**Top**</span></span>    | <span data-ttu-id="17bde-127">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="17bde-127">**xs:integer**</span></span>            | <span data-ttu-id="17bde-128">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="17bde-128">Required</span></span> | <span data-ttu-id="17bde-129">Der Abstand zwischen dem Ursprung und dem obersten Punkt im umgebenden Feld für das Element.</span><span class="sxs-lookup"><span data-stu-id="17bde-129">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="17bde-130">Eine beliebige ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="17bde-130">Any integer.</span></span>              |
| <span data-ttu-id="17bde-131">**Width**</span><span class="sxs-lookup"><span data-stu-id="17bde-131">**Width**</span></span>  | <span data-ttu-id="17bde-132">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="17bde-132">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="17bde-133">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="17bde-133">Required</span></span> | <span data-ttu-id="17bde-134">Die Breite des Begrenzungs Rahmens für das Element.</span><span class="sxs-lookup"><span data-stu-id="17bde-134">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="17bde-135">Eine beliebige nicht negative ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="17bde-135">Any non-negative integer.</span></span> |
| <span data-ttu-id="17bde-136">**Height**</span><span class="sxs-lookup"><span data-stu-id="17bde-136">**Height**</span></span> | <span data-ttu-id="17bde-137">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="17bde-137">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="17bde-138">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="17bde-138">Required</span></span> | <span data-ttu-id="17bde-139">Die Höhe des umgebenden Felds für das Element.</span><span class="sxs-lookup"><span data-stu-id="17bde-139">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="17bde-140">Eine beliebige nicht negative ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="17bde-140">Any non-negative integer.</span></span> |



 

> [!WARNING]
> <span data-ttu-id="17bde-141">Die interne Koordinaten Zuordnung des frei Hand Worts ist eine englische metrikeinheit, und ein Multiplikator von 2,54 muss von Ihrer Anwendung verwendet werden, um die Width-und Height-Werte in die von den Tablet PC Platform-APIs verwendeten HIMETRIC-Einheiten zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="17bde-141">The ink word's internal coordinate mapping is English Metric Units and a multiplier of 2.54 will need to be used by your application to convert the Width and Height values to the HIMETRIC units used by the Tablet PC platform APIs.</span></span>

 

## <a name="element-information"></a><span data-ttu-id="17bde-142">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="17bde-142">Element Information</span></span>



|              |                                                             |
|--------------|-------------------------------------------------------------|
| <span data-ttu-id="17bde-143">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="17bde-143">Element type</span></span> | <span data-ttu-id="17bde-144">ComplexType " [**inkwordtype**](inkwordtype-complex-type.md) "</span><span class="sxs-lookup"><span data-stu-id="17bde-144">[**InkWordType**](inkwordtype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="17bde-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="17bde-145">Namespace</span></span>    | <span data-ttu-id="17bde-146">urn: Schemas-Microsoft-com: TabletPC: RichInk</span><span class="sxs-lookup"><span data-stu-id="17bde-146">urn:schemas-microsoft-com:tabletpc:richink</span></span>                  |
| <span data-ttu-id="17bde-147">Schemaname</span><span class="sxs-lookup"><span data-stu-id="17bde-147">Schema name</span></span>  | <span data-ttu-id="17bde-148">Journal Leser</span><span class="sxs-lookup"><span data-stu-id="17bde-148">Journal Reader</span></span>                                              |



 

 

 



