---
description: Enthält eine Base64-codierte Bitmap eines Flags, das dem Abschnitt einer Journalnotiz zugeordnet ist.
ms.assetid: 612f8814-ab3c-4a3e-9791-525788d4cc72
title: Flag-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46508f9821379fbedb3291ba45d16dbdd0fb316f
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432327"
---
# <a name="flag-element"></a><span data-ttu-id="82e38-103">Flag-Element</span><span class="sxs-lookup"><span data-stu-id="82e38-103">Flag Element</span></span>

<span data-ttu-id="82e38-104">Enthält eine Base64-codierte Bitmap eines Flags, das dem Abschnitt einer Journalnotiz zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="82e38-104">Contains a base64 encoded bitmap of a flag associated with section of a Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="82e38-105">Definition</span><span class="sxs-lookup"><span data-stu-id="82e38-105">Definition</span></span>

``` syntax
<xs:element name="Flag" type="FlagType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a><span data-ttu-id="82e38-106">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="82e38-106">Parent Elements</span></span>

[<span data-ttu-id="82e38-107">**Inhalt**</span><span class="sxs-lookup"><span data-stu-id="82e38-107">**Content**</span></span>](content-element--journal-reader.md)

[<span data-ttu-id="82e38-108">**GroupNode**</span><span class="sxs-lookup"><span data-stu-id="82e38-108">**GroupNode**</span></span>](groupnode-element.md)

## <a name="child-elements"></a><span data-ttu-id="82e38-109">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="82e38-109">Child Elements</span></span>

<span data-ttu-id="82e38-110">Keine</span><span class="sxs-lookup"><span data-stu-id="82e38-110">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="82e38-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="82e38-111">Attributes</span></span>



| <span data-ttu-id="82e38-112">attribute</span><span class="sxs-lookup"><span data-stu-id="82e38-112">Attribute</span></span>  | <span data-ttu-id="82e38-113">Typ</span><span class="sxs-lookup"><span data-stu-id="82e38-113">Type</span></span>                      | <span data-ttu-id="82e38-114">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="82e38-114">Required</span></span> | <span data-ttu-id="82e38-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="82e38-115">Description</span></span>                                                                             | <span data-ttu-id="82e38-116">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="82e38-116">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="82e38-117">**Left**</span><span class="sxs-lookup"><span data-stu-id="82e38-117">**Left**</span></span>   | <span data-ttu-id="82e38-118">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="82e38-118">**xs:integer**</span></span>            | <span data-ttu-id="82e38-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="82e38-119">Required</span></span> | <span data-ttu-id="82e38-120">Der Abstand vom Ursprung zum äußersten linken Punkt im Begrenzungsfeld für das Element.</span><span class="sxs-lookup"><span data-stu-id="82e38-120">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="82e38-121">Eine beliebige ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="82e38-121">Any integer.</span></span>              |
| <span data-ttu-id="82e38-122">**Top**</span><span class="sxs-lookup"><span data-stu-id="82e38-122">**Top**</span></span>    | <span data-ttu-id="82e38-123">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="82e38-123">**xs:integer**</span></span>            | <span data-ttu-id="82e38-124">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="82e38-124">Required</span></span> | <span data-ttu-id="82e38-125">Der Abstand vom Ursprung zum obersten Punkt im begrenzungsfeld für das Element.</span><span class="sxs-lookup"><span data-stu-id="82e38-125">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="82e38-126">Eine beliebige ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="82e38-126">Any integer.</span></span>              |
| <span data-ttu-id="82e38-127">**Width**</span><span class="sxs-lookup"><span data-stu-id="82e38-127">**Width**</span></span>  | <span data-ttu-id="82e38-128">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="82e38-128">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="82e38-129">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="82e38-129">Required</span></span> | <span data-ttu-id="82e38-130">Die Breite des Begrenzungsfelds für das Element.</span><span class="sxs-lookup"><span data-stu-id="82e38-130">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="82e38-131">Eine beliebige nicht negative ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="82e38-131">Any non-negative integer.</span></span> |
| <span data-ttu-id="82e38-132">**Height**</span><span class="sxs-lookup"><span data-stu-id="82e38-132">**Height**</span></span> | <span data-ttu-id="82e38-133">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="82e38-133">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="82e38-134">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="82e38-134">Required</span></span> | <span data-ttu-id="82e38-135">Die Höhe des Begrenzungsfelds für das Element.</span><span class="sxs-lookup"><span data-stu-id="82e38-135">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="82e38-136">Eine beliebige nicht negative ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="82e38-136">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="82e38-137">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="82e38-137">Element Information</span></span>



|  <span data-ttu-id="82e38-138">Element</span><span class="sxs-lookup"><span data-stu-id="82e38-138">Element</span></span>     | <span data-ttu-id="82e38-139">Wert</span><span class="sxs-lookup"><span data-stu-id="82e38-139">Value</span></span>                                                     |
|--------------|-------------------------------------------------------|
| <span data-ttu-id="82e38-140">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="82e38-140">Element type</span></span> | <span data-ttu-id="82e38-141">[**complexType: FlagType**](flagtype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="82e38-141">[**FlagType**](flagtype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="82e38-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="82e38-142">Namespace</span></span>    | <span data-ttu-id="82e38-143">urn:schemas-microsoft-com:tabletpc:richink</span><span class="sxs-lookup"><span data-stu-id="82e38-143">urn:schemas-microsoft-com:tabletpc:richink</span></span>            |
| <span data-ttu-id="82e38-144">Schemaname</span><span class="sxs-lookup"><span data-stu-id="82e38-144">Schema name</span></span>  | <span data-ttu-id="82e38-145">Journalreader</span><span class="sxs-lookup"><span data-stu-id="82e38-145">Journal Reader</span></span>                                        |



 

 

 



