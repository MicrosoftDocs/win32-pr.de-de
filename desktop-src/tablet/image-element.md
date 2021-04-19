---
description: Enthält codierte Binärdaten für ein Bild im Journal Dokument, falls vorhanden.
ms.assetid: fbb86bef-68f7-4aad-8a98-1c68e79ea2de
title: Image-Element
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8437495a4c248a8e5bc68a0f7b75a2cf7d761387
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360680"
---
# <a name="image-element"></a><span data-ttu-id="09bcb-103">Image-Element</span><span class="sxs-lookup"><span data-stu-id="09bcb-103">Image Element</span></span>

<span data-ttu-id="09bcb-104">Enthält codierte Binärdaten für ein Bild im Journal Dokument, falls vorhanden.</span><span class="sxs-lookup"><span data-stu-id="09bcb-104">Contains encoded binary data for an image in the Journal document, if present.</span></span>

## <a name="definition"></a><span data-ttu-id="09bcb-105">Definition</span><span class="sxs-lookup"><span data-stu-id="09bcb-105">Definition</span></span>

``` syntax
 Copy Code<xs:element name="Image" type="ImageType" />
```

## <a name="parent-elements"></a><span data-ttu-id="09bcb-106">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="09bcb-106">Parent Elements</span></span>

[<span data-ttu-id="09bcb-107">**Inhalt**</span><span class="sxs-lookup"><span data-stu-id="09bcb-107">**Content**</span></span>](content-element--journal-reader.md)

[<span data-ttu-id="09bcb-108">**-Gruppenknoten**</span><span class="sxs-lookup"><span data-stu-id="09bcb-108">**GroupNode**</span></span>](groupnode-element.md)

## <a name="child-elements"></a><span data-ttu-id="09bcb-109">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="09bcb-109">Child Elements</span></span>

<span data-ttu-id="09bcb-110">Keine</span><span class="sxs-lookup"><span data-stu-id="09bcb-110">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="09bcb-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="09bcb-111">Attributes</span></span>



| <span data-ttu-id="09bcb-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="09bcb-112">Attribute</span></span>  | <span data-ttu-id="09bcb-113">type</span><span class="sxs-lookup"><span data-stu-id="09bcb-113">Type</span></span>                      | <span data-ttu-id="09bcb-114">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="09bcb-114">Required</span></span> | <span data-ttu-id="09bcb-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="09bcb-115">Description</span></span>                                                                             | <span data-ttu-id="09bcb-116">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="09bcb-116">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="09bcb-117">**Left**</span><span class="sxs-lookup"><span data-stu-id="09bcb-117">**Left**</span></span>   | <span data-ttu-id="09bcb-118">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="09bcb-118">**xs:integer**</span></span>            | <span data-ttu-id="09bcb-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="09bcb-119">Required</span></span> | <span data-ttu-id="09bcb-120">Der Abstand zwischen dem Ursprung und dem äußersten äußersten linken Punkt im umgebenden Feld des Elements.</span><span class="sxs-lookup"><span data-stu-id="09bcb-120">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="09bcb-121">Eine beliebige ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="09bcb-121">Any integer.</span></span>              |
| <span data-ttu-id="09bcb-122">**Top**</span><span class="sxs-lookup"><span data-stu-id="09bcb-122">**Top**</span></span>    | <span data-ttu-id="09bcb-123">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="09bcb-123">**xs:integer**</span></span>            | <span data-ttu-id="09bcb-124">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="09bcb-124">Required</span></span> | <span data-ttu-id="09bcb-125">Der Abstand zwischen dem Ursprung und dem obersten Punkt im umgebenden Feld für das Element.</span><span class="sxs-lookup"><span data-stu-id="09bcb-125">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="09bcb-126">Eine beliebige ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="09bcb-126">Any integer.</span></span>              |
| <span data-ttu-id="09bcb-127">**Width**</span><span class="sxs-lookup"><span data-stu-id="09bcb-127">**Width**</span></span>  | <span data-ttu-id="09bcb-128">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="09bcb-128">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="09bcb-129">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="09bcb-129">Required</span></span> | <span data-ttu-id="09bcb-130">Die Breite des Begrenzungs Rahmens für das Element.</span><span class="sxs-lookup"><span data-stu-id="09bcb-130">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="09bcb-131">Eine beliebige nicht negative ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="09bcb-131">Any non-negative integer.</span></span> |
| <span data-ttu-id="09bcb-132">**Height**</span><span class="sxs-lookup"><span data-stu-id="09bcb-132">**Height**</span></span> | <span data-ttu-id="09bcb-133">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="09bcb-133">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="09bcb-134">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="09bcb-134">Required</span></span> | <span data-ttu-id="09bcb-135">Die Höhe des umgebenden Felds für das Element.</span><span class="sxs-lookup"><span data-stu-id="09bcb-135">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="09bcb-136">Eine beliebige nicht negative ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="09bcb-136">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="09bcb-137">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="09bcb-137">Element Information</span></span>



|              |                                                         |
|--------------|---------------------------------------------------------|
| <span data-ttu-id="09bcb-138">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="09bcb-138">Element type</span></span> | <span data-ttu-id="09bcb-139">ComplexType " [**ImageType**](imagetype-complex-type.md) "</span><span class="sxs-lookup"><span data-stu-id="09bcb-139">[**ImageType**](imagetype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="09bcb-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="09bcb-140">Namespace</span></span>    | <span data-ttu-id="09bcb-141">urn: Schemas-Microsoft-com: TabletPC: RichInk</span><span class="sxs-lookup"><span data-stu-id="09bcb-141">urn:schemas-microsoft-com:tabletpc:richink</span></span>              |
| <span data-ttu-id="09bcb-142">Schemaname</span><span class="sxs-lookup"><span data-stu-id="09bcb-142">Schema name</span></span>  | <span data-ttu-id="09bcb-143">Journal Leser</span><span class="sxs-lookup"><span data-stu-id="09bcb-143">Journal Reader</span></span>                                          |



 

## <a name="see-also"></a><span data-ttu-id="09bcb-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="09bcb-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09bcb-145">**Hintergrund**</span><span class="sxs-lookup"><span data-stu-id="09bcb-145">**Background**</span></span>](background-element.md)
</dt> </dl>

 

 



