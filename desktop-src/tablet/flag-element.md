---
description: Enthält eine Base64-codierte Bitmap eines Flags, das einem Abschnitt eines Journal Hinweises zugeordnet ist.
ms.assetid: 612f8814-ab3c-4a3e-9791-525788d4cc72
title: Flag-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b6eda9aeb29c07c0de05eadffb8ba8d60f81954
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345742"
---
# <a name="flag-element"></a><span data-ttu-id="2adc9-103">Flag-Element</span><span class="sxs-lookup"><span data-stu-id="2adc9-103">Flag Element</span></span>

<span data-ttu-id="2adc9-104">Enthält eine Base64-codierte Bitmap eines Flags, das einem Abschnitt eines Journal Hinweises zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="2adc9-104">Contains a base64 encoded bitmap of a flag associated with section of a Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="2adc9-105">Definition</span><span class="sxs-lookup"><span data-stu-id="2adc9-105">Definition</span></span>

``` syntax
<xs:element name="Flag" type="FlagType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a><span data-ttu-id="2adc9-106">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2adc9-106">Parent Elements</span></span>

[<span data-ttu-id="2adc9-107">**Inhalt**</span><span class="sxs-lookup"><span data-stu-id="2adc9-107">**Content**</span></span>](content-element--journal-reader.md)

[<span data-ttu-id="2adc9-108">**-Gruppenknoten**</span><span class="sxs-lookup"><span data-stu-id="2adc9-108">**GroupNode**</span></span>](groupnode-element.md)

## <a name="child-elements"></a><span data-ttu-id="2adc9-109">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2adc9-109">Child Elements</span></span>

<span data-ttu-id="2adc9-110">Keine</span><span class="sxs-lookup"><span data-stu-id="2adc9-110">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="2adc9-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="2adc9-111">Attributes</span></span>



| <span data-ttu-id="2adc9-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="2adc9-112">Attribute</span></span>  | <span data-ttu-id="2adc9-113">type</span><span class="sxs-lookup"><span data-stu-id="2adc9-113">Type</span></span>                      | <span data-ttu-id="2adc9-114">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="2adc9-114">Required</span></span> | <span data-ttu-id="2adc9-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2adc9-115">Description</span></span>                                                                             | <span data-ttu-id="2adc9-116">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="2adc9-116">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="2adc9-117">**Left**</span><span class="sxs-lookup"><span data-stu-id="2adc9-117">**Left**</span></span>   | <span data-ttu-id="2adc9-118">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="2adc9-118">**xs:integer**</span></span>            | <span data-ttu-id="2adc9-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="2adc9-119">Required</span></span> | <span data-ttu-id="2adc9-120">Der Abstand zwischen dem Ursprung und dem äußersten äußersten linken Punkt im umgebenden Feld des Elements.</span><span class="sxs-lookup"><span data-stu-id="2adc9-120">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="2adc9-121">Eine beliebige ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="2adc9-121">Any integer.</span></span>              |
| <span data-ttu-id="2adc9-122">**Top**</span><span class="sxs-lookup"><span data-stu-id="2adc9-122">**Top**</span></span>    | <span data-ttu-id="2adc9-123">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="2adc9-123">**xs:integer**</span></span>            | <span data-ttu-id="2adc9-124">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="2adc9-124">Required</span></span> | <span data-ttu-id="2adc9-125">Der Abstand zwischen dem Ursprung und dem obersten Punkt im umgebenden Feld für das Element.</span><span class="sxs-lookup"><span data-stu-id="2adc9-125">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="2adc9-126">Eine beliebige ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="2adc9-126">Any integer.</span></span>              |
| <span data-ttu-id="2adc9-127">**Width**</span><span class="sxs-lookup"><span data-stu-id="2adc9-127">**Width**</span></span>  | <span data-ttu-id="2adc9-128">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="2adc9-128">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="2adc9-129">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="2adc9-129">Required</span></span> | <span data-ttu-id="2adc9-130">Die Breite des Begrenzungs Rahmens für das Element.</span><span class="sxs-lookup"><span data-stu-id="2adc9-130">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="2adc9-131">Eine beliebige nicht negative ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="2adc9-131">Any non-negative integer.</span></span> |
| <span data-ttu-id="2adc9-132">**Height**</span><span class="sxs-lookup"><span data-stu-id="2adc9-132">**Height**</span></span> | <span data-ttu-id="2adc9-133">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="2adc9-133">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="2adc9-134">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="2adc9-134">Required</span></span> | <span data-ttu-id="2adc9-135">Die Höhe des umgebenden Felds für das Element.</span><span class="sxs-lookup"><span data-stu-id="2adc9-135">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="2adc9-136">Eine beliebige nicht negative ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="2adc9-136">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="2adc9-137">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="2adc9-137">Element Information</span></span>



|              |                                                       |
|--------------|-------------------------------------------------------|
| <span data-ttu-id="2adc9-138">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="2adc9-138">Element type</span></span> | <span data-ttu-id="2adc9-139">ComplexType " [**FlagType**](flagtype-complex-type.md) "</span><span class="sxs-lookup"><span data-stu-id="2adc9-139">[**FlagType**](flagtype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="2adc9-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="2adc9-140">Namespace</span></span>    | <span data-ttu-id="2adc9-141">urn: Schemas-Microsoft-com: TabletPC: RichInk</span><span class="sxs-lookup"><span data-stu-id="2adc9-141">urn:schemas-microsoft-com:tabletpc:richink</span></span>            |
| <span data-ttu-id="2adc9-142">Schemaname</span><span class="sxs-lookup"><span data-stu-id="2adc9-142">Schema name</span></span>  | <span data-ttu-id="2adc9-143">Journal Leser</span><span class="sxs-lookup"><span data-stu-id="2adc9-143">Journal Reader</span></span>                                        |



 

 

 



