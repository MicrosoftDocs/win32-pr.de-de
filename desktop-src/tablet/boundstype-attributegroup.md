---
description: Definiert eine Attribut Gruppe, die von einer Vielzahl von Elementen in einer Journal-XML-Datei verwendet wird. Sie enthält Attribute, mit denen die Begrenzungen (Links, oben, Höhe und Breite) eines Elements im Dokument definiert werden.
ms.assetid: 7841aa65-fb35-4909-a34e-3c883555f764
title: Boundstype-Attribut Gruppe
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 411a9d3ec30363e5c405cf27654330a0886f8946
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749105"
---
# <a name="boundstype-attribute-group"></a><span data-ttu-id="5ef0e-104">Boundstype-Attribut Gruppe</span><span class="sxs-lookup"><span data-stu-id="5ef0e-104">BoundsType Attribute Group</span></span>

<span data-ttu-id="5ef0e-105">Definiert eine Attribut Gruppe, die von einer Vielzahl von Elementen in einer Journal-XML-Datei verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5ef0e-105">Defines an attribute group that is used by a variety of elements in a Journal XML file.</span></span> <span data-ttu-id="5ef0e-106">Sie enthält Attribute, mit denen die Begrenzungen (Links, oben, Höhe und Breite) eines Elements im Dokument definiert werden.</span><span class="sxs-lookup"><span data-stu-id="5ef0e-106">It contains attributes used to define the bounds (left, top, height, and width) of an element in the document.</span></span>

## <a name="definition"></a><span data-ttu-id="5ef0e-107">Definition</span><span class="sxs-lookup"><span data-stu-id="5ef0e-107">Definition</span></span>

``` syntax
<xs:attributeGroup name="BoundsType">
  <xs:attribute name="Left" use="required" type="xs:integer" />
  <xs:attribute name="Top" use="required" type="xs:integer" />
  <xs:attribute name="Width" use="required" type="xs:nonNegativeInteger" />
  <xs:attribute name="Height" use="required" type="xs: nonNegativeInteger" />
</xs:attributeGroup>
```

## <a name="child-elements"></a><span data-ttu-id="5ef0e-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5ef0e-108">Child Elements</span></span>

<span data-ttu-id="5ef0e-109">Keine</span><span class="sxs-lookup"><span data-stu-id="5ef0e-109">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="5ef0e-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="5ef0e-110">Attributes</span></span>



| <span data-ttu-id="5ef0e-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="5ef0e-111">Attribute</span></span>  | <span data-ttu-id="5ef0e-112">type</span><span class="sxs-lookup"><span data-stu-id="5ef0e-112">Type</span></span>                      | <span data-ttu-id="5ef0e-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="5ef0e-113">Required</span></span> | <span data-ttu-id="5ef0e-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5ef0e-114">Description</span></span>                                                                                        | <span data-ttu-id="5ef0e-115">PossibleValues</span><span class="sxs-lookup"><span data-stu-id="5ef0e-115">PossibleValues</span></span>                       |
|------------|---------------------------|----------|----------------------------------------------------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="5ef0e-116">**Left**</span><span class="sxs-lookup"><span data-stu-id="5ef0e-116">**Left**</span></span>   | <span data-ttu-id="5ef0e-117">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="5ef0e-117">**xs:integer**</span></span>            | <span data-ttu-id="5ef0e-118">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="5ef0e-118">Required</span></span> | <span data-ttu-id="5ef0e-119">Der Abstand zwischen dem Ursprung und dem äußersten äußersten linken Punkt im umgebenden Feld des Elements.</span><span class="sxs-lookup"><span data-stu-id="5ef0e-119">The distance from the origin to the leftmost point in the bounding box for the element.</span></span><br/> | <span data-ttu-id="5ef0e-120">Eine beliebige ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="5ef0e-120">Any integer.</span></span><br/>              |
| <span data-ttu-id="5ef0e-121">**Top**</span><span class="sxs-lookup"><span data-stu-id="5ef0e-121">**Top**</span></span>    | <span data-ttu-id="5ef0e-122">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="5ef0e-122">**xs:integer**</span></span>            | <span data-ttu-id="5ef0e-123">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="5ef0e-123">Required</span></span> | <span data-ttu-id="5ef0e-124">Der Abstand zwischen dem Ursprung und dem obersten Punkt im umgebenden Feld für das Element.</span><span class="sxs-lookup"><span data-stu-id="5ef0e-124">The distance from the origin to the topmost point in the bounding box for the element.</span></span><br/>  | <span data-ttu-id="5ef0e-125">Eine beliebige ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="5ef0e-125">Any integer.</span></span><br/>              |
| <span data-ttu-id="5ef0e-126">**Width**</span><span class="sxs-lookup"><span data-stu-id="5ef0e-126">**Width**</span></span>  | <span data-ttu-id="5ef0e-127">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="5ef0e-127">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="5ef0e-128">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="5ef0e-128">Required</span></span> | <span data-ttu-id="5ef0e-129">Die Breite des Begrenzungs Rahmens für das Element.</span><span class="sxs-lookup"><span data-stu-id="5ef0e-129">The width of the bounding box for the element.</span></span><br/>                                          | <span data-ttu-id="5ef0e-130">Eine beliebige nicht negative ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="5ef0e-130">Any non-negative integer.</span></span><br/> |
| <span data-ttu-id="5ef0e-131">**Height**</span><span class="sxs-lookup"><span data-stu-id="5ef0e-131">**Height**</span></span> | <span data-ttu-id="5ef0e-132">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="5ef0e-132">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="5ef0e-133">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="5ef0e-133">Required</span></span> | <span data-ttu-id="5ef0e-134">Die Höhe des umgebenden Felds für das Element.</span><span class="sxs-lookup"><span data-stu-id="5ef0e-134">The height of the bounding box for the element.</span></span><br/>                                         | <span data-ttu-id="5ef0e-135">Eine beliebige nicht negative ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="5ef0e-135">Any non-negative integer.</span></span><br/> |



 

## <a name="type-information"></a><span data-ttu-id="5ef0e-136">Typinformationen</span><span class="sxs-lookup"><span data-stu-id="5ef0e-136">Type Information</span></span>



|             |                                            |
|-------------|--------------------------------------------|
| <span data-ttu-id="5ef0e-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="5ef0e-137">Namespace</span></span>   | <span data-ttu-id="5ef0e-138">urn: Schemas-Microsoft-com: TabletPC: RichInk</span><span class="sxs-lookup"><span data-stu-id="5ef0e-138">urn:schemas-microsoft-com:tabletpc:richink</span></span> |
| <span data-ttu-id="5ef0e-139">Schemaname</span><span class="sxs-lookup"><span data-stu-id="5ef0e-139">Schema name</span></span> | <span data-ttu-id="5ef0e-140">Journal Leser</span><span class="sxs-lookup"><span data-stu-id="5ef0e-140">Journal Reader</span></span>                             |



 

## <a name="remarks"></a><span data-ttu-id="5ef0e-141">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5ef0e-141">Remarks</span></span>

<span data-ttu-id="5ef0e-142">" **Left** " und " **Top** " können negativ sein, da der Ursprung durch die Ränder definiert wird, nicht die Seite.</span><span class="sxs-lookup"><span data-stu-id="5ef0e-142">**Left** and **Top** can be negative because the origin is defined by the margins, not the page.</span></span>

 

 




