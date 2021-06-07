---
description: Definiert eine Gruppe, die einen Satz gruppierter Inhalte in einer Journalnotiz enthält.
ms.assetid: e2561be1-03ce-41f7-9ad4-197d75411c48
title: ContentGroup-Gruppe
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02e4291da1912c43674871c06fb803e1936f7178
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432612"
---
# <a name="contentgroup-group"></a><span data-ttu-id="307fe-103">ContentGroup-Gruppe</span><span class="sxs-lookup"><span data-stu-id="307fe-103">ContentGroup Group</span></span>

<span data-ttu-id="307fe-104">Definiert eine Gruppe, die einen Satz gruppierter Inhalte in einer Journalnotiz enthält.</span><span class="sxs-lookup"><span data-stu-id="307fe-104">Defines a group that contains a set of grouped content in a Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="307fe-105">Definition</span><span class="sxs-lookup"><span data-stu-id="307fe-105">Definition</span></span>

``` syntax
<xs:group name="ContentGroup" >
  <xs:choice>
    <xs:element name="GroupNode" type="GroupNodeType" />
    <xs:element name="Paragraph" type="ParagraphType" />
    <xs:element name="InkWord" type="InkWordType" />
    <xs:element name="Drawing" type="DrawingType" />
    <xs:element name="Text" type="TextType" />
    <xs:element name="Image" type="ImageType" />
    <xs:element name="Flag" type="FlagType" />
    <xs:element name="Reflow" type="ReflowType" />
  </xs:choice>
</xs:group>
```

## <a name="child-elements"></a><span data-ttu-id="307fe-106">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="307fe-106">Child Elements</span></span>

[<span data-ttu-id="307fe-107">**GroupNode**</span><span class="sxs-lookup"><span data-stu-id="307fe-107">**GroupNode**</span></span>](groupnode-element.md)

[<span data-ttu-id="307fe-108">**Paragraph**</span><span class="sxs-lookup"><span data-stu-id="307fe-108">**Paragraph**</span></span>](paragraph-element.md)

[<span data-ttu-id="307fe-109">**InkWord**</span><span class="sxs-lookup"><span data-stu-id="307fe-109">**InkWord**</span></span>](inkword-element.md)

[<span data-ttu-id="307fe-110">**Zeichnung**</span><span class="sxs-lookup"><span data-stu-id="307fe-110">**Drawing**</span></span>](drawing-element.md)

[<span data-ttu-id="307fe-111">**Text**</span><span class="sxs-lookup"><span data-stu-id="307fe-111">**Text**</span></span>](text-element.md)

[<span data-ttu-id="307fe-112">**Image**</span><span class="sxs-lookup"><span data-stu-id="307fe-112">**Image**</span></span>](docimage-element.md)

[<span data-ttu-id="307fe-113">**Flag**</span><span class="sxs-lookup"><span data-stu-id="307fe-113">**Flag**</span></span>](flag-element.md)

## <a name="attributes"></a><span data-ttu-id="307fe-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="307fe-114">Attributes</span></span>



| <span data-ttu-id="307fe-115">attribute</span><span class="sxs-lookup"><span data-stu-id="307fe-115">Attribute</span></span>  | <span data-ttu-id="307fe-116">Typ</span><span class="sxs-lookup"><span data-stu-id="307fe-116">Type</span></span>                      | <span data-ttu-id="307fe-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="307fe-117">Required</span></span> | <span data-ttu-id="307fe-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="307fe-118">Description</span></span>                                                                                        | <span data-ttu-id="307fe-119">PossibleValues</span><span class="sxs-lookup"><span data-stu-id="307fe-119">PossibleValues</span></span>                       |
|------------|---------------------------|----------|----------------------------------------------------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="307fe-120">**Left**</span><span class="sxs-lookup"><span data-stu-id="307fe-120">**Left**</span></span>   | <span data-ttu-id="307fe-121">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="307fe-121">**xs:integer**</span></span>            | <span data-ttu-id="307fe-122">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="307fe-122">Required</span></span> | <span data-ttu-id="307fe-123">Der Abstand vom Ursprung zum äußersten linken Punkt im begrenzungsfeld für das Element.</span><span class="sxs-lookup"><span data-stu-id="307fe-123">The distance from the origin to the leftmost point in the bounding box for the element.</span></span><br/> | <span data-ttu-id="307fe-124">Eine beliebige ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="307fe-124">Any integer.</span></span><br/>              |
| <span data-ttu-id="307fe-125">**Top**</span><span class="sxs-lookup"><span data-stu-id="307fe-125">**Top**</span></span>    | <span data-ttu-id="307fe-126">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="307fe-126">**xs:integer**</span></span>            | <span data-ttu-id="307fe-127">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="307fe-127">Required</span></span> | <span data-ttu-id="307fe-128">Der Abstand vom Ursprung zum obersten Punkt im Begrenzungsfeld für das Element.</span><span class="sxs-lookup"><span data-stu-id="307fe-128">The distance from the origin to the topmost point in the bounding box for the element.</span></span><br/>  | <span data-ttu-id="307fe-129">Eine beliebige ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="307fe-129">Any integer.</span></span><br/>              |
| <span data-ttu-id="307fe-130">**Width**</span><span class="sxs-lookup"><span data-stu-id="307fe-130">**Width**</span></span>  | <span data-ttu-id="307fe-131">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="307fe-131">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="307fe-132">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="307fe-132">Required</span></span> | <span data-ttu-id="307fe-133">Die Breite des Begrenzungsfelds für das Element.</span><span class="sxs-lookup"><span data-stu-id="307fe-133">The width of the bounding box for the element.</span></span><br/>                                          | <span data-ttu-id="307fe-134">Eine beliebige nicht negative ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="307fe-134">Any non-negative integer.</span></span><br/> |
| <span data-ttu-id="307fe-135">**Height**</span><span class="sxs-lookup"><span data-stu-id="307fe-135">**Height**</span></span> | <span data-ttu-id="307fe-136">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="307fe-136">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="307fe-137">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="307fe-137">Required</span></span> | <span data-ttu-id="307fe-138">Die Höhe des Begrenzungsfelds für das Element.</span><span class="sxs-lookup"><span data-stu-id="307fe-138">The height of the bounding box for the element.</span></span><br/>                                         | <span data-ttu-id="307fe-139">Eine beliebige nicht negative ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="307fe-139">Any non-negative integer.</span></span><br/> |



 

## <a name="type-information"></a><span data-ttu-id="307fe-140">Typinformationen</span><span class="sxs-lookup"><span data-stu-id="307fe-140">Type Information</span></span>



|  <span data-ttu-id="307fe-141">Element</span><span class="sxs-lookup"><span data-stu-id="307fe-141">Element</span></span>     | <span data-ttu-id="307fe-142">Wert</span><span class="sxs-lookup"><span data-stu-id="307fe-142">Value</span></span>                                                     |
|-------------|--------------------------------------------|
| <span data-ttu-id="307fe-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="307fe-143">Namespace</span></span>   | <span data-ttu-id="307fe-144">urn:schemas-microsoft-com:tabletpc:richink</span><span class="sxs-lookup"><span data-stu-id="307fe-144">urn:schemas-microsoft-com:tabletpc:richink</span></span> |
| <span data-ttu-id="307fe-145">Schemaname</span><span class="sxs-lookup"><span data-stu-id="307fe-145">Schema name</span></span> | <span data-ttu-id="307fe-146">Journalreader</span><span class="sxs-lookup"><span data-stu-id="307fe-146">Journal Reader</span></span>                             |



 

 

 




