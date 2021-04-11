---
description: Definiert eine Gruppe, die einen Satz gruppierter Inhalte in einer Journal Notiz enthält.
ms.assetid: e2561be1-03ce-41f7-9ad4-197d75411c48
title: Gruppe "contentgroup"
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fbbc13a3dee796646b6d61ac9ba0bde50880f12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042622"
---
# <a name="contentgroup-group"></a><span data-ttu-id="ac4f7-103">Gruppe "contentgroup"</span><span class="sxs-lookup"><span data-stu-id="ac4f7-103">ContentGroup Group</span></span>

<span data-ttu-id="ac4f7-104">Definiert eine Gruppe, die einen Satz gruppierter Inhalte in einer Journal Notiz enthält.</span><span class="sxs-lookup"><span data-stu-id="ac4f7-104">Defines a group that contains a set of grouped content in a Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="ac4f7-105">Definition</span><span class="sxs-lookup"><span data-stu-id="ac4f7-105">Definition</span></span>

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

## <a name="child-elements"></a><span data-ttu-id="ac4f7-106">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ac4f7-106">Child Elements</span></span>

[<span data-ttu-id="ac4f7-107">**-Gruppenknoten**</span><span class="sxs-lookup"><span data-stu-id="ac4f7-107">**GroupNode**</span></span>](groupnode-element.md)

[<span data-ttu-id="ac4f7-108">**Paragraph**</span><span class="sxs-lookup"><span data-stu-id="ac4f7-108">**Paragraph**</span></span>](paragraph-element.md)

[<span data-ttu-id="ac4f7-109">**InkWord**</span><span class="sxs-lookup"><span data-stu-id="ac4f7-109">**InkWord**</span></span>](inkword-element.md)

[<span data-ttu-id="ac4f7-110">**Zeichnung**</span><span class="sxs-lookup"><span data-stu-id="ac4f7-110">**Drawing**</span></span>](drawing-element.md)

[<span data-ttu-id="ac4f7-111">**Text**</span><span class="sxs-lookup"><span data-stu-id="ac4f7-111">**Text**</span></span>](text-element.md)

[<span data-ttu-id="ac4f7-112">**Image**</span><span class="sxs-lookup"><span data-stu-id="ac4f7-112">**Image**</span></span>](docimage-element.md)

[<span data-ttu-id="ac4f7-113">**Flag**</span><span class="sxs-lookup"><span data-stu-id="ac4f7-113">**Flag**</span></span>](flag-element.md)

## <a name="attributes"></a><span data-ttu-id="ac4f7-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="ac4f7-114">Attributes</span></span>



| <span data-ttu-id="ac4f7-115">Attribut</span><span class="sxs-lookup"><span data-stu-id="ac4f7-115">Attribute</span></span>  | <span data-ttu-id="ac4f7-116">type</span><span class="sxs-lookup"><span data-stu-id="ac4f7-116">Type</span></span>                      | <span data-ttu-id="ac4f7-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="ac4f7-117">Required</span></span> | <span data-ttu-id="ac4f7-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ac4f7-118">Description</span></span>                                                                                        | <span data-ttu-id="ac4f7-119">PossibleValues</span><span class="sxs-lookup"><span data-stu-id="ac4f7-119">PossibleValues</span></span>                       |
|------------|---------------------------|----------|----------------------------------------------------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="ac4f7-120">**Left**</span><span class="sxs-lookup"><span data-stu-id="ac4f7-120">**Left**</span></span>   | <span data-ttu-id="ac4f7-121">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="ac4f7-121">**xs:integer**</span></span>            | <span data-ttu-id="ac4f7-122">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="ac4f7-122">Required</span></span> | <span data-ttu-id="ac4f7-123">Der Abstand zwischen dem Ursprung und dem äußersten äußersten linken Punkt im umgebenden Feld des Elements.</span><span class="sxs-lookup"><span data-stu-id="ac4f7-123">The distance from the origin to the leftmost point in the bounding box for the element.</span></span><br/> | <span data-ttu-id="ac4f7-124">Eine beliebige ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="ac4f7-124">Any integer.</span></span><br/>              |
| <span data-ttu-id="ac4f7-125">**Top**</span><span class="sxs-lookup"><span data-stu-id="ac4f7-125">**Top**</span></span>    | <span data-ttu-id="ac4f7-126">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="ac4f7-126">**xs:integer**</span></span>            | <span data-ttu-id="ac4f7-127">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="ac4f7-127">Required</span></span> | <span data-ttu-id="ac4f7-128">Der Abstand zwischen dem Ursprung und dem obersten Punkt im umgebenden Feld für das Element.</span><span class="sxs-lookup"><span data-stu-id="ac4f7-128">The distance from the origin to the topmost point in the bounding box for the element.</span></span><br/>  | <span data-ttu-id="ac4f7-129">Eine beliebige ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="ac4f7-129">Any integer.</span></span><br/>              |
| <span data-ttu-id="ac4f7-130">**Width**</span><span class="sxs-lookup"><span data-stu-id="ac4f7-130">**Width**</span></span>  | <span data-ttu-id="ac4f7-131">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="ac4f7-131">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="ac4f7-132">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="ac4f7-132">Required</span></span> | <span data-ttu-id="ac4f7-133">Die Breite des Begrenzungs Rahmens für das Element.</span><span class="sxs-lookup"><span data-stu-id="ac4f7-133">The width of the bounding box for the element.</span></span><br/>                                          | <span data-ttu-id="ac4f7-134">Eine beliebige nicht negative ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="ac4f7-134">Any non-negative integer.</span></span><br/> |
| <span data-ttu-id="ac4f7-135">**Height**</span><span class="sxs-lookup"><span data-stu-id="ac4f7-135">**Height**</span></span> | <span data-ttu-id="ac4f7-136">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="ac4f7-136">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="ac4f7-137">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="ac4f7-137">Required</span></span> | <span data-ttu-id="ac4f7-138">Die Höhe des umgebenden Felds für das Element.</span><span class="sxs-lookup"><span data-stu-id="ac4f7-138">The height of the bounding box for the element.</span></span><br/>                                         | <span data-ttu-id="ac4f7-139">Eine beliebige nicht negative ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="ac4f7-139">Any non-negative integer.</span></span><br/> |



 

## <a name="type-information"></a><span data-ttu-id="ac4f7-140">Typinformationen</span><span class="sxs-lookup"><span data-stu-id="ac4f7-140">Type Information</span></span>



|             |                                            |
|-------------|--------------------------------------------|
| <span data-ttu-id="ac4f7-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="ac4f7-141">Namespace</span></span>   | <span data-ttu-id="ac4f7-142">urn: Schemas-Microsoft-com: TabletPC: RichInk</span><span class="sxs-lookup"><span data-stu-id="ac4f7-142">urn:schemas-microsoft-com:tabletpc:richink</span></span> |
| <span data-ttu-id="ac4f7-143">Schemaname</span><span class="sxs-lookup"><span data-stu-id="ac4f7-143">Schema name</span></span> | <span data-ttu-id="ac4f7-144">Journal Leser</span><span class="sxs-lookup"><span data-stu-id="ac4f7-144">Journal Reader</span></span>                             |



 

 

 




