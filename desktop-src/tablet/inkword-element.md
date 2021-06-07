---
description: Enthält Informationen zu einem bestimmten Ink-Wort in der Journalnotiz, einschließlich Position, Alternativen und der tatsächlichen Ink-Daten.
ms.assetid: 1e197716-bf6c-4a28-ae66-38aa59d7371d
title: InkWord-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8dc9baea7cda0346e82c11331c45f453e61f192
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432392"
---
# <a name="inkword-element"></a><span data-ttu-id="f95db-103">InkWord-Element</span><span class="sxs-lookup"><span data-stu-id="f95db-103">InkWord Element</span></span>

<span data-ttu-id="f95db-104">Enthält Informationen zu einem bestimmten Ink-Wort in der Journalnotiz, einschließlich Position, Alternativen und der tatsächlichen Ink-Daten.</span><span class="sxs-lookup"><span data-stu-id="f95db-104">Contains information about a given ink word in the Journal note, including position, alternates, and the actual ink data.</span></span>

## <a name="definition"></a><span data-ttu-id="f95db-105">Definition</span><span class="sxs-lookup"><span data-stu-id="f95db-105">Definition</span></span>

``` syntax
<xs:element name="InkWord" type="InkWordType" />
```

## <a name="parent-elements"></a><span data-ttu-id="f95db-106">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f95db-106">Parent Elements</span></span>

[<span data-ttu-id="f95db-107">**GroupNode**</span><span class="sxs-lookup"><span data-stu-id="f95db-107">**GroupNode**</span></span>](groupnode-element.md)

[<span data-ttu-id="f95db-108">**Linie**</span><span class="sxs-lookup"><span data-stu-id="f95db-108">**Line**</span></span>](line-element.md)

## <a name="child-elements"></a><span data-ttu-id="f95db-109">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f95db-109">Child Elements</span></span>

[<span data-ttu-id="f95db-110">**ScalarTransform**</span><span class="sxs-lookup"><span data-stu-id="f95db-110">**ScalarTransform**</span></span>](scalartransform-element.md)

[<span data-ttu-id="f95db-111">**AlternateList**</span><span class="sxs-lookup"><span data-stu-id="f95db-111">**AlternateList**</span></span>](alternatelist-element.md)

[<span data-ttu-id="f95db-112">**CanReClassify**</span><span class="sxs-lookup"><span data-stu-id="f95db-112">**CanReClassify**</span></span>](canreclassify-element.md)

[<span data-ttu-id="f95db-113">**Vertrauen**</span><span class="sxs-lookup"><span data-stu-id="f95db-113">**Confidence**</span></span>](confidence-element.md)

[<span data-ttu-id="f95db-114">**InkObject**</span><span class="sxs-lookup"><span data-stu-id="f95db-114">**InkObject**</span></span>](inkobject-element.md)

## <a name="attributes"></a><span data-ttu-id="f95db-115">Attribute</span><span class="sxs-lookup"><span data-stu-id="f95db-115">Attributes</span></span>



| <span data-ttu-id="f95db-116">attribute</span><span class="sxs-lookup"><span data-stu-id="f95db-116">Attribute</span></span>  | <span data-ttu-id="f95db-117">Typ</span><span class="sxs-lookup"><span data-stu-id="f95db-117">Type</span></span>                      | <span data-ttu-id="f95db-118">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="f95db-118">Required</span></span> | <span data-ttu-id="f95db-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f95db-119">Description</span></span>                                                                             | <span data-ttu-id="f95db-120">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="f95db-120">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="f95db-121">**Left**</span><span class="sxs-lookup"><span data-stu-id="f95db-121">**Left**</span></span>   | <span data-ttu-id="f95db-122">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="f95db-122">**xs:integer**</span></span>            | <span data-ttu-id="f95db-123">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="f95db-123">Required</span></span> | <span data-ttu-id="f95db-124">Der Abstand zwischen dem Ursprung und dem äußersten linken Punkt im Begrenzungsfeld für das Element.</span><span class="sxs-lookup"><span data-stu-id="f95db-124">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="f95db-125">Eine beliebige ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="f95db-125">Any integer.</span></span>              |
| <span data-ttu-id="f95db-126">**Top**</span><span class="sxs-lookup"><span data-stu-id="f95db-126">**Top**</span></span>    | <span data-ttu-id="f95db-127">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="f95db-127">**xs:integer**</span></span>            | <span data-ttu-id="f95db-128">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="f95db-128">Required</span></span> | <span data-ttu-id="f95db-129">Der Abstand zwischen dem Ursprung und dem obersten Punkt im Begrenzungsfeld für das Element.</span><span class="sxs-lookup"><span data-stu-id="f95db-129">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="f95db-130">Eine beliebige ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="f95db-130">Any integer.</span></span>              |
| <span data-ttu-id="f95db-131">**Width**</span><span class="sxs-lookup"><span data-stu-id="f95db-131">**Width**</span></span>  | <span data-ttu-id="f95db-132">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="f95db-132">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="f95db-133">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="f95db-133">Required</span></span> | <span data-ttu-id="f95db-134">Die Breite des Begrenzungsfelds für das Element.</span><span class="sxs-lookup"><span data-stu-id="f95db-134">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="f95db-135">Eine nicht negative ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="f95db-135">Any non-negative integer.</span></span> |
| <span data-ttu-id="f95db-136">**Height**</span><span class="sxs-lookup"><span data-stu-id="f95db-136">**Height**</span></span> | <span data-ttu-id="f95db-137">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="f95db-137">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="f95db-138">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="f95db-138">Required</span></span> | <span data-ttu-id="f95db-139">Die Höhe des Begrenzungsfelds für das Element.</span><span class="sxs-lookup"><span data-stu-id="f95db-139">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="f95db-140">Eine nicht negative ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="f95db-140">Any non-negative integer.</span></span> |



 

> [!WARNING]
> <span data-ttu-id="f95db-141">Die interne Koordinatenzuordnung des Ink-Worts ist Englische Metrikeinheiten, und ein Multiplikator von 2,54 muss von Ihrer Anwendung verwendet werden, um die Werte für Breite und Höhe in die HIMETRIC-Einheiten zu konvertieren, die von den Plattform-APIs des Tablet-PCs verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f95db-141">The ink word's internal coordinate mapping is English Metric Units and a multiplier of 2.54 will need to be used by your application to convert the Width and Height values to the HIMETRIC units used by the Tablet PC platform APIs.</span></span>

 

## <a name="element-information"></a><span data-ttu-id="f95db-142">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="f95db-142">Element Information</span></span>



|  <span data-ttu-id="f95db-143">Element</span><span class="sxs-lookup"><span data-stu-id="f95db-143">Element</span></span>     | <span data-ttu-id="f95db-144">Wert</span><span class="sxs-lookup"><span data-stu-id="f95db-144">Value</span></span>                                                     |
|--------------|-------------------------------------------------------------|
| <span data-ttu-id="f95db-145">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="f95db-145">Element type</span></span> | <span data-ttu-id="f95db-146">[**ComplexType: InkWordType**](inkwordtype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="f95db-146">[**InkWordType**](inkwordtype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="f95db-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="f95db-147">Namespace</span></span>    | <span data-ttu-id="f95db-148">urn:schemas-microsoft-com:tabletpc:richink</span><span class="sxs-lookup"><span data-stu-id="f95db-148">urn:schemas-microsoft-com:tabletpc:richink</span></span>                  |
| <span data-ttu-id="f95db-149">Schemaname</span><span class="sxs-lookup"><span data-stu-id="f95db-149">Schema name</span></span>  | <span data-ttu-id="f95db-150">Journalreader</span><span class="sxs-lookup"><span data-stu-id="f95db-150">Journal Reader</span></span>                                              |



 

 

 



