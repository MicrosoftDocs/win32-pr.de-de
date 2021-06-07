---
description: Enthält codierte Binärdaten für ein Bild im Journaldokument, sofern vorhanden.
ms.assetid: fbb86bef-68f7-4aad-8a98-1c68e79ea2de
title: Image-Element
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9dd3b37a39ce45ee0294f46922fbab376523b64
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432582"
---
# <a name="image-element"></a><span data-ttu-id="018eb-103">Image-Element</span><span class="sxs-lookup"><span data-stu-id="018eb-103">Image Element</span></span>

<span data-ttu-id="018eb-104">Enthält codierte Binärdaten für ein Bild im Journaldokument, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="018eb-104">Contains encoded binary data for an image in the Journal document, if present.</span></span>

## <a name="definition"></a><span data-ttu-id="018eb-105">Definition</span><span class="sxs-lookup"><span data-stu-id="018eb-105">Definition</span></span>

``` syntax
 Copy Code<xs:element name="Image" type="ImageType" />
```

## <a name="parent-elements"></a><span data-ttu-id="018eb-106">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="018eb-106">Parent Elements</span></span>

[<span data-ttu-id="018eb-107">**Inhalt**</span><span class="sxs-lookup"><span data-stu-id="018eb-107">**Content**</span></span>](content-element--journal-reader.md)

[<span data-ttu-id="018eb-108">**GroupNode**</span><span class="sxs-lookup"><span data-stu-id="018eb-108">**GroupNode**</span></span>](groupnode-element.md)

## <a name="child-elements"></a><span data-ttu-id="018eb-109">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="018eb-109">Child Elements</span></span>

<span data-ttu-id="018eb-110">Keine</span><span class="sxs-lookup"><span data-stu-id="018eb-110">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="018eb-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="018eb-111">Attributes</span></span>



| <span data-ttu-id="018eb-112">attribute</span><span class="sxs-lookup"><span data-stu-id="018eb-112">Attribute</span></span>  | <span data-ttu-id="018eb-113">Typ</span><span class="sxs-lookup"><span data-stu-id="018eb-113">Type</span></span>                      | <span data-ttu-id="018eb-114">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="018eb-114">Required</span></span> | <span data-ttu-id="018eb-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="018eb-115">Description</span></span>                                                                             | <span data-ttu-id="018eb-116">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="018eb-116">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="018eb-117">**Left**</span><span class="sxs-lookup"><span data-stu-id="018eb-117">**Left**</span></span>   | <span data-ttu-id="018eb-118">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="018eb-118">**xs:integer**</span></span>            | <span data-ttu-id="018eb-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="018eb-119">Required</span></span> | <span data-ttu-id="018eb-120">Der Abstand vom Ursprung zum äußersten linken Punkt im Begrenzungsfeld für das Element.</span><span class="sxs-lookup"><span data-stu-id="018eb-120">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="018eb-121">Eine beliebige ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="018eb-121">Any integer.</span></span>              |
| <span data-ttu-id="018eb-122">**Top**</span><span class="sxs-lookup"><span data-stu-id="018eb-122">**Top**</span></span>    | <span data-ttu-id="018eb-123">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="018eb-123">**xs:integer**</span></span>            | <span data-ttu-id="018eb-124">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="018eb-124">Required</span></span> | <span data-ttu-id="018eb-125">Der Abstand vom Ursprung zum obersten Punkt im begrenzungsfeld für das Element.</span><span class="sxs-lookup"><span data-stu-id="018eb-125">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="018eb-126">Eine beliebige ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="018eb-126">Any integer.</span></span>              |
| <span data-ttu-id="018eb-127">**Width**</span><span class="sxs-lookup"><span data-stu-id="018eb-127">**Width**</span></span>  | <span data-ttu-id="018eb-128">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="018eb-128">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="018eb-129">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="018eb-129">Required</span></span> | <span data-ttu-id="018eb-130">Die Breite des Begrenzungsfelds für das Element.</span><span class="sxs-lookup"><span data-stu-id="018eb-130">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="018eb-131">Eine beliebige nicht negative ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="018eb-131">Any non-negative integer.</span></span> |
| <span data-ttu-id="018eb-132">**Height**</span><span class="sxs-lookup"><span data-stu-id="018eb-132">**Height**</span></span> | <span data-ttu-id="018eb-133">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="018eb-133">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="018eb-134">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="018eb-134">Required</span></span> | <span data-ttu-id="018eb-135">Die Höhe des Begrenzungsfelds für das Element.</span><span class="sxs-lookup"><span data-stu-id="018eb-135">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="018eb-136">Eine beliebige nicht negative ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="018eb-136">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="018eb-137">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="018eb-137">Element Information</span></span>



|  <span data-ttu-id="018eb-138">Element</span><span class="sxs-lookup"><span data-stu-id="018eb-138">Element</span></span>     | <span data-ttu-id="018eb-139">Wert</span><span class="sxs-lookup"><span data-stu-id="018eb-139">Value</span></span>                                                     |
|--------------|---------------------------------------------------------|
| <span data-ttu-id="018eb-140">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="018eb-140">Element type</span></span> | <span data-ttu-id="018eb-141">[**complexType: ImageType**](imagetype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="018eb-141">[**ImageType**](imagetype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="018eb-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="018eb-142">Namespace</span></span>    | <span data-ttu-id="018eb-143">urn:schemas-microsoft-com:tabletpc:richink</span><span class="sxs-lookup"><span data-stu-id="018eb-143">urn:schemas-microsoft-com:tabletpc:richink</span></span>              |
| <span data-ttu-id="018eb-144">Schemaname</span><span class="sxs-lookup"><span data-stu-id="018eb-144">Schema name</span></span>  | <span data-ttu-id="018eb-145">Journalreader</span><span class="sxs-lookup"><span data-stu-id="018eb-145">Journal Reader</span></span>                                          |



 

## <a name="see-also"></a><span data-ttu-id="018eb-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="018eb-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="018eb-147">**Hintergrund**</span><span class="sxs-lookup"><span data-stu-id="018eb-147">**Background**</span></span>](background-element.md)
</dt> </dl>

 

 



