---
description: Enthält Formatierungsinformationen für die horizontalen Linien, die für die Schreibweise in einem Journal Hinweis verwendet werden.
ms.assetid: e3c9e7a8-8de6-4871-b386-2186883f2ee7
title: Horizontales Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0e380ca35f86ce1012084d31de732cd66c79363
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751896"
---
# <a name="horizontal-element"></a><span data-ttu-id="48286-103">Horizontales Element</span><span class="sxs-lookup"><span data-stu-id="48286-103">Horizontal Element</span></span>

<span data-ttu-id="48286-104">Enthält Formatierungsinformationen für die horizontalen Linien, die für die Schreibweise in einem Journal Hinweis verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="48286-104">Contains formatting information for the horizontal lines used for the stationery in a Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="48286-105">Definition</span><span class="sxs-lookup"><span data-stu-id="48286-105">Definition</span></span>

``` syntax
<xs:element name="Horizontal" type="HorizontalType" minOccurs="0" />
```

## <a name="parent-elements"></a><span data-ttu-id="48286-106">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="48286-106">Parent Elements</span></span>

[<span data-ttu-id="48286-107">**Linelayout**</span><span class="sxs-lookup"><span data-stu-id="48286-107">**LineLayout**</span></span>](linelayout-element.md)

## <a name="child-elements"></a><span data-ttu-id="48286-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="48286-108">Child Elements</span></span>

<span data-ttu-id="48286-109">Keine</span><span class="sxs-lookup"><span data-stu-id="48286-109">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="48286-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="48286-110">Attributes</span></span>



<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="48286-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="48286-111">Attribute</span></span></th>
<th><span data-ttu-id="48286-112">type</span><span class="sxs-lookup"><span data-stu-id="48286-112">Type</span></span></th>
<th><span data-ttu-id="48286-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="48286-113">Required</span></span></th>
<th><span data-ttu-id="48286-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="48286-114">Description</span></span></th>
<th><span data-ttu-id="48286-115">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="48286-115">Possible Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="48286-116"><strong>Stil</strong></span><span class="sxs-lookup"><span data-stu-id="48286-116"><strong>Style</strong></span></span></td>
<td><span data-ttu-id="48286-117"><a href="linelayoutstyletype-simple-type.md"><strong>Linelayoutstyletype</strong></a> simpleType</span><span class="sxs-lookup"><span data-stu-id="48286-117"><a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="48286-118">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="48286-118">Required</span></span></td>
<td><span data-ttu-id="48286-119">Gibt den Typ der zu Zeichenden Zeile an.</span><span class="sxs-lookup"><span data-stu-id="48286-119">Specifies the type of line to be drawn.</span></span></td>
<td><ul>
<li><span data-ttu-id="48286-120">Keine</span><span class="sxs-lookup"><span data-stu-id="48286-120">None</span></span></li>
<li><span data-ttu-id="48286-121">Basis</span><span class="sxs-lookup"><span data-stu-id="48286-121">Solid</span></span></li>
<li><span data-ttu-id="48286-122">Strich</span><span class="sxs-lookup"><span data-stu-id="48286-122">Dash</span></span></li>
<li><span data-ttu-id="48286-123">Punkt</span><span class="sxs-lookup"><span data-stu-id="48286-123">Dot</span></span></li>
<li><span data-ttu-id="48286-124">DashDot</span><span class="sxs-lookup"><span data-stu-id="48286-124">DashDot</span></span></li>
<li><span data-ttu-id="48286-125">DashDotDot</span><span class="sxs-lookup"><span data-stu-id="48286-125">DashDotDot</span></span></li>
<li><span data-ttu-id="48286-126">Double</span><span class="sxs-lookup"><span data-stu-id="48286-126">Double</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48286-127"><strong>Farbe</strong></span><span class="sxs-lookup"><span data-stu-id="48286-127"><strong>Color</strong></span></span></td>
<td><span data-ttu-id="48286-128"><a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType</span><span class="sxs-lookup"><span data-stu-id="48286-128"><a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="48286-129">Optional</span><span class="sxs-lookup"><span data-stu-id="48286-129">Optional</span></span></td>
<td><span data-ttu-id="48286-130">Farbe des Elements.</span><span class="sxs-lookup"><span data-stu-id="48286-130">Color of the element.</span></span></td>
<td><span data-ttu-id="48286-131">Ein Hexadezimal-RGB-Wert.</span><span class="sxs-lookup"><span data-stu-id="48286-131">A hexadecimal RGB value.</span></span> <span data-ttu-id="48286-132">Entspricht dem folgenden regulären Ausdruck: # [0-9a-zA-Z] {6} .</span><span class="sxs-lookup"><span data-stu-id="48286-132">Matches the following regular expression: #[0-9a-zA-Z]{6}.</span></span> <span data-ttu-id="48286-133">Beispielsweise #4a79B5.</span><span class="sxs-lookup"><span data-stu-id="48286-133">For example, #4a79B5.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48286-134"><strong>SpacingBefore</strong></span><span class="sxs-lookup"><span data-stu-id="48286-134"><strong>SpacingBefore</strong></span></span></td>
<td><span data-ttu-id="48286-135"><strong>xs:nonNegativeInteger</strong></span><span class="sxs-lookup"><span data-stu-id="48286-135"><strong>xs:nonNegativeInteger</strong></span></span></td>
<td><span data-ttu-id="48286-136">Optional</span><span class="sxs-lookup"><span data-stu-id="48286-136">Optional</span></span></td>
<td><span data-ttu-id="48286-137">Abstand vor dem Element.</span><span class="sxs-lookup"><span data-stu-id="48286-137">Spacing before the element.</span></span></td>
<td><span data-ttu-id="48286-138">Eine beliebige nicht negative ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="48286-138">Any non-negative integer.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48286-139"><strong>Abstand zwischen</strong></span><span class="sxs-lookup"><span data-stu-id="48286-139"><strong>SpacingBetween</strong></span></span></td>
<td><span data-ttu-id="48286-140"><strong>xs:nonNegativeInteger</strong></span><span class="sxs-lookup"><span data-stu-id="48286-140"><strong>xs:nonNegativeInteger</strong></span></span></td>
<td><span data-ttu-id="48286-141">Optional</span><span class="sxs-lookup"><span data-stu-id="48286-141">Optional</span></span></td>
<td><span data-ttu-id="48286-142">Abstand zwischen diesem Element und umgebenden Elementen.</span><span class="sxs-lookup"><span data-stu-id="48286-142">Spacing between this element and surrounding elements.</span></span></td>
<td><span data-ttu-id="48286-143">Eine beliebige nicht negative ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="48286-143">Any non-negative integer.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a><span data-ttu-id="48286-144">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="48286-144">Element Information</span></span>



|              |                                                                   |
|--------------|-------------------------------------------------------------------|
| <span data-ttu-id="48286-145">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="48286-145">Element type</span></span> | [<span data-ttu-id="48286-146">**ComplexType "horizontaltype"**</span><span class="sxs-lookup"><span data-stu-id="48286-146">**HorizontalType complexType**</span></span>](horizontaltype-complex-type.md) |
| <span data-ttu-id="48286-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="48286-147">Namespace</span></span>    | <span data-ttu-id="48286-148">urn: Schemas-Microsoft-com: TabletPC: RichInk</span><span class="sxs-lookup"><span data-stu-id="48286-148">urn:schemas-microsoft-com:tabletpc:richink</span></span>                        |
| <span data-ttu-id="48286-149">Schemaname</span><span class="sxs-lookup"><span data-stu-id="48286-149">Schema name</span></span>  | <span data-ttu-id="48286-150">Journal Leser</span><span class="sxs-lookup"><span data-stu-id="48286-150">Journal Reader</span></span>                                                    |



 

 

 




