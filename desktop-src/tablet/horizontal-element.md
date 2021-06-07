---
description: Enthält Formatierungsinformationen für die horizontalen Linien, die für das Stationery in einer Journalnotiz verwendet werden.
ms.assetid: e3c9e7a8-8de6-4871-b386-2186883f2ee7
title: Horizontales Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50de08008d0243d27f8a8c5f64d6aeac5ddbcc1c
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432376"
---
# <a name="horizontal-element"></a><span data-ttu-id="7f4f2-103">Horizontales Element</span><span class="sxs-lookup"><span data-stu-id="7f4f2-103">Horizontal Element</span></span>

<span data-ttu-id="7f4f2-104">Enthält Formatierungsinformationen für die horizontalen Linien, die für das Stationery in einer Journalnotiz verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7f4f2-104">Contains formatting information for the horizontal lines used for the stationery in a Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="7f4f2-105">Definition</span><span class="sxs-lookup"><span data-stu-id="7f4f2-105">Definition</span></span>

``` syntax
<xs:element name="Horizontal" type="HorizontalType" minOccurs="0" />
```

## <a name="parent-elements"></a><span data-ttu-id="7f4f2-106">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7f4f2-106">Parent Elements</span></span>

[<span data-ttu-id="7f4f2-107">**LineLayout**</span><span class="sxs-lookup"><span data-stu-id="7f4f2-107">**LineLayout**</span></span>](linelayout-element.md)

## <a name="child-elements"></a><span data-ttu-id="7f4f2-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7f4f2-108">Child Elements</span></span>

<span data-ttu-id="7f4f2-109">Keine</span><span class="sxs-lookup"><span data-stu-id="7f4f2-109">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="7f4f2-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="7f4f2-110">Attributes</span></span>



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
<th><span data-ttu-id="7f4f2-111">attribute</span><span class="sxs-lookup"><span data-stu-id="7f4f2-111">Attribute</span></span></th>
<th><span data-ttu-id="7f4f2-112">Typ</span><span class="sxs-lookup"><span data-stu-id="7f4f2-112">Type</span></span></th>
<th><span data-ttu-id="7f4f2-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="7f4f2-113">Required</span></span></th>
<th><span data-ttu-id="7f4f2-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7f4f2-114">Description</span></span></th>
<th><span data-ttu-id="7f4f2-115">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="7f4f2-115">Possible Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7f4f2-116"><strong>Stil</strong></span><span class="sxs-lookup"><span data-stu-id="7f4f2-116"><strong>Style</strong></span></span></td>
<td><span data-ttu-id="7f4f2-117"><a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a> simpleType</span><span class="sxs-lookup"><span data-stu-id="7f4f2-117"><a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="7f4f2-118">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="7f4f2-118">Required</span></span></td>
<td><span data-ttu-id="7f4f2-119">Gibt den Typ der zu zeichneten Linie an.</span><span class="sxs-lookup"><span data-stu-id="7f4f2-119">Specifies the type of line to be drawn.</span></span></td>
<td><ul>
<li><span data-ttu-id="7f4f2-120">Keine</span><span class="sxs-lookup"><span data-stu-id="7f4f2-120">None</span></span></li>
<li><span data-ttu-id="7f4f2-121">Basis</span><span class="sxs-lookup"><span data-stu-id="7f4f2-121">Solid</span></span></li>
<li><span data-ttu-id="7f4f2-122">Strich</span><span class="sxs-lookup"><span data-stu-id="7f4f2-122">Dash</span></span></li>
<li><span data-ttu-id="7f4f2-123">Punkt</span><span class="sxs-lookup"><span data-stu-id="7f4f2-123">Dot</span></span></li>
<li><span data-ttu-id="7f4f2-124">DashDot</span><span class="sxs-lookup"><span data-stu-id="7f4f2-124">DashDot</span></span></li>
<li><span data-ttu-id="7f4f2-125">DashDotDot</span><span class="sxs-lookup"><span data-stu-id="7f4f2-125">DashDotDot</span></span></li>
<li><span data-ttu-id="7f4f2-126">Double</span><span class="sxs-lookup"><span data-stu-id="7f4f2-126">Double</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7f4f2-127"><strong>Farbe</strong></span><span class="sxs-lookup"><span data-stu-id="7f4f2-127"><strong>Color</strong></span></span></td>
<td><span data-ttu-id="7f4f2-128"><a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType</span><span class="sxs-lookup"><span data-stu-id="7f4f2-128"><a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="7f4f2-129">Optional</span><span class="sxs-lookup"><span data-stu-id="7f4f2-129">Optional</span></span></td>
<td><span data-ttu-id="7f4f2-130">Farbe des Elements.</span><span class="sxs-lookup"><span data-stu-id="7f4f2-130">Color of the element.</span></span></td>
<td><span data-ttu-id="7f4f2-131">Ein hexadezimaler RGB-Wert.</span><span class="sxs-lookup"><span data-stu-id="7f4f2-131">A hexadecimal RGB value.</span></span> <span data-ttu-id="7f4f2-132">Entspricht dem folgenden regulären Ausdruck: #[0-9a-zA-Z] {6} .</span><span class="sxs-lookup"><span data-stu-id="7f4f2-132">Matches the following regular expression: #[0-9a-zA-Z]{6}.</span></span> <span data-ttu-id="7f4f2-133">Beispiel: #4a79B5.</span><span class="sxs-lookup"><span data-stu-id="7f4f2-133">For example, #4a79B5.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7f4f2-134"><strong>SpacingBefore</strong></span><span class="sxs-lookup"><span data-stu-id="7f4f2-134"><strong>SpacingBefore</strong></span></span></td>
<td><span data-ttu-id="7f4f2-135"><strong>xs:nonNegativeInteger</strong></span><span class="sxs-lookup"><span data-stu-id="7f4f2-135"><strong>xs:nonNegativeInteger</strong></span></span></td>
<td><span data-ttu-id="7f4f2-136">Optional</span><span class="sxs-lookup"><span data-stu-id="7f4f2-136">Optional</span></span></td>
<td><span data-ttu-id="7f4f2-137">Abstand vor dem Element.</span><span class="sxs-lookup"><span data-stu-id="7f4f2-137">Spacing before the element.</span></span></td>
<td><span data-ttu-id="7f4f2-138">Eine nicht negative ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="7f4f2-138">Any non-negative integer.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7f4f2-139"><strong>SpacingBetween</strong></span><span class="sxs-lookup"><span data-stu-id="7f4f2-139"><strong>SpacingBetween</strong></span></span></td>
<td><span data-ttu-id="7f4f2-140"><strong>xs:nonNegativeInteger</strong></span><span class="sxs-lookup"><span data-stu-id="7f4f2-140"><strong>xs:nonNegativeInteger</strong></span></span></td>
<td><span data-ttu-id="7f4f2-141">Optional</span><span class="sxs-lookup"><span data-stu-id="7f4f2-141">Optional</span></span></td>
<td><span data-ttu-id="7f4f2-142">Abstand zwischen diesem Element und den umgebenden Elementen.</span><span class="sxs-lookup"><span data-stu-id="7f4f2-142">Spacing between this element and surrounding elements.</span></span></td>
<td><span data-ttu-id="7f4f2-143">Eine nicht negative ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="7f4f2-143">Any non-negative integer.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a><span data-ttu-id="7f4f2-144">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="7f4f2-144">Element Information</span></span>



|  <span data-ttu-id="7f4f2-145">Element</span><span class="sxs-lookup"><span data-stu-id="7f4f2-145">Element</span></span>     | <span data-ttu-id="7f4f2-146">Wert</span><span class="sxs-lookup"><span data-stu-id="7f4f2-146">Value</span></span>                                                     |
|--------------|-------------------------------------------------------------------|
| <span data-ttu-id="7f4f2-147">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="7f4f2-147">Element type</span></span> | [<span data-ttu-id="7f4f2-148">**complexType: HorizontalType**</span><span class="sxs-lookup"><span data-stu-id="7f4f2-148">**HorizontalType complexType**</span></span>](horizontaltype-complex-type.md) |
| <span data-ttu-id="7f4f2-149">Namespace</span><span class="sxs-lookup"><span data-stu-id="7f4f2-149">Namespace</span></span>    | <span data-ttu-id="7f4f2-150">urn:schemas-microsoft-com:tabletpc:richink</span><span class="sxs-lookup"><span data-stu-id="7f4f2-150">urn:schemas-microsoft-com:tabletpc:richink</span></span>                        |
| <span data-ttu-id="7f4f2-151">Schemaname</span><span class="sxs-lookup"><span data-stu-id="7f4f2-151">Schema name</span></span>  | <span data-ttu-id="7f4f2-152">Journalreader</span><span class="sxs-lookup"><span data-stu-id="7f4f2-152">Journal Reader</span></span>                                                    |



 

 

 




