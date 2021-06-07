---
description: Enthält die Informationen, die die vertikale Komponente der Linien im Von der Journalnotiz verwendeten Stationery beschreiben. Wird z. B. verwendet, wenn die Notiz Gitternetzlinien hat.
ms.assetid: af6f485e-13df-41bb-b57a-10d8393b83e7
title: Vertical-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42565e6f2828c4ef27d1b28830502303a03e6f13
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432122"
---
# <a name="vertical-element"></a><span data-ttu-id="90667-104">Vertical-Element</span><span class="sxs-lookup"><span data-stu-id="90667-104">Vertical Element</span></span>

<span data-ttu-id="90667-105">Enthält die Informationen, die die vertikale Komponente der Linien im Von der Journalnotiz verwendeten Stationery beschreiben.</span><span class="sxs-lookup"><span data-stu-id="90667-105">Contains the information that describes the vertical component of the lines in the stationery used by the Journal note.</span></span> <span data-ttu-id="90667-106">Wird z. B. verwendet, wenn die Notiz Gitternetzlinien hat.</span><span class="sxs-lookup"><span data-stu-id="90667-106">Used, for example, when the note has grid lines.</span></span>

## <a name="definition"></a><span data-ttu-id="90667-107">Definition</span><span class="sxs-lookup"><span data-stu-id="90667-107">Definition</span></span>

``` syntax
<xs:element name="Vertical" type="VerticalType" minOccurs="0" />
```

## <a name="parent-elements"></a><span data-ttu-id="90667-108">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="90667-108">Parent Elements</span></span>

[<span data-ttu-id="90667-109">**LineLayout**</span><span class="sxs-lookup"><span data-stu-id="90667-109">**LineLayout**</span></span>](linelayout-element.md)

## <a name="child-elements"></a><span data-ttu-id="90667-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="90667-110">Child Elements</span></span>

<span data-ttu-id="90667-111">Keine</span><span class="sxs-lookup"><span data-stu-id="90667-111">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="90667-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="90667-112">Attributes</span></span>



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
<th><span data-ttu-id="90667-113">attribute</span><span class="sxs-lookup"><span data-stu-id="90667-113">Attribute</span></span></th>
<th><span data-ttu-id="90667-114">Typ</span><span class="sxs-lookup"><span data-stu-id="90667-114">Type</span></span></th>
<th><span data-ttu-id="90667-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="90667-115">Required</span></span></th>
<th><span data-ttu-id="90667-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="90667-116">Description</span></span></th>
<th><span data-ttu-id="90667-117">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="90667-117">Possible Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="90667-118"><strong>Stil</strong></span><span class="sxs-lookup"><span data-stu-id="90667-118"><strong>Style</strong></span></span></td>
<td><span data-ttu-id="90667-119"><a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a> simpleType</span><span class="sxs-lookup"><span data-stu-id="90667-119"><a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="90667-120">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="90667-120">Required</span></span></td>
<td><span data-ttu-id="90667-121">Gibt den Typ der zu zeichneten Linie an.</span><span class="sxs-lookup"><span data-stu-id="90667-121">Specifies the type of line to be drawn.</span></span></td>
<td><ul>
<li><span data-ttu-id="90667-122">Keine</span><span class="sxs-lookup"><span data-stu-id="90667-122">None</span></span></li>
<li><span data-ttu-id="90667-123">Basis</span><span class="sxs-lookup"><span data-stu-id="90667-123">Solid</span></span></li>
<li><span data-ttu-id="90667-124">Strich</span><span class="sxs-lookup"><span data-stu-id="90667-124">Dash</span></span></li>
<li><span data-ttu-id="90667-125">Punkt</span><span class="sxs-lookup"><span data-stu-id="90667-125">Dot</span></span></li>
<li><span data-ttu-id="90667-126">DashDot</span><span class="sxs-lookup"><span data-stu-id="90667-126">DashDot</span></span></li>
<li><span data-ttu-id="90667-127">DashDotDot</span><span class="sxs-lookup"><span data-stu-id="90667-127">DashDotDot</span></span></li>
<li><span data-ttu-id="90667-128">Double</span><span class="sxs-lookup"><span data-stu-id="90667-128">Double</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="90667-129"><strong>Farbe</strong></span><span class="sxs-lookup"><span data-stu-id="90667-129"><strong>Color</strong></span></span></td>
<td><span data-ttu-id="90667-130"><a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType</span><span class="sxs-lookup"><span data-stu-id="90667-130"><a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="90667-131">Optional</span><span class="sxs-lookup"><span data-stu-id="90667-131">Optional</span></span></td>
<td><span data-ttu-id="90667-132">Farbe des Elements.</span><span class="sxs-lookup"><span data-stu-id="90667-132">Color of the element.</span></span></td>
<td><span data-ttu-id="90667-133">Ein hexadezimaler RGB-Wert.</span><span class="sxs-lookup"><span data-stu-id="90667-133">A hexadecimal RGB value.</span></span> <span data-ttu-id="90667-134">Entspricht dem folgenden regulären Ausdruck: #[0-9a-zA-Z] {6} .</span><span class="sxs-lookup"><span data-stu-id="90667-134">Matches the following regular expression: #[0-9a-zA-Z]{6}.</span></span> <span data-ttu-id="90667-135">Beispiel: #4a79B5.</span><span class="sxs-lookup"><span data-stu-id="90667-135">For example, #4a79B5.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="90667-136"><strong>SpacingBefore</strong></span><span class="sxs-lookup"><span data-stu-id="90667-136"><strong>SpacingBefore</strong></span></span></td>
<td><span data-ttu-id="90667-137"><strong>xs:nonNegativeInteger</strong></span><span class="sxs-lookup"><span data-stu-id="90667-137"><strong>xs:nonNegativeInteger</strong></span></span></td>
<td><span data-ttu-id="90667-138">Optional</span><span class="sxs-lookup"><span data-stu-id="90667-138">Optional</span></span></td>
<td><span data-ttu-id="90667-139">Abstand vor dem Element.</span><span class="sxs-lookup"><span data-stu-id="90667-139">Spacing before the element.</span></span></td>
<td><span data-ttu-id="90667-140">Eine nicht negative ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="90667-140">Any non-negative integer.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="90667-141"><strong>SpacingBetween</strong></span><span class="sxs-lookup"><span data-stu-id="90667-141"><strong>SpacingBetween</strong></span></span></td>
<td><span data-ttu-id="90667-142"><strong>xs:nonNegativeInteger</strong></span><span class="sxs-lookup"><span data-stu-id="90667-142"><strong>xs:nonNegativeInteger</strong></span></span></td>
<td><span data-ttu-id="90667-143">Optional</span><span class="sxs-lookup"><span data-stu-id="90667-143">Optional</span></span></td>
<td><span data-ttu-id="90667-144">Abstand zwischen diesem Element und den umgebenden Elementen.</span><span class="sxs-lookup"><span data-stu-id="90667-144">Spacing between this element and surrounding elements.</span></span></td>
<td><span data-ttu-id="90667-145">Eine nicht negative ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="90667-145">Any non-negative integer.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a><span data-ttu-id="90667-146">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="90667-146">Element Information</span></span>



|  <span data-ttu-id="90667-147">Element</span><span class="sxs-lookup"><span data-stu-id="90667-147">Element</span></span>     | <span data-ttu-id="90667-148">Wert</span><span class="sxs-lookup"><span data-stu-id="90667-148">Value</span></span>                                                         |
|--------------|---------------------------------------------------------------|
| <span data-ttu-id="90667-149">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="90667-149">Element type</span></span> | <span data-ttu-id="90667-150">[**complexType: VerticalType**](verticaltype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="90667-150">[**VerticalType**](verticaltype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="90667-151">Namespace</span><span class="sxs-lookup"><span data-stu-id="90667-151">Namespace</span></span>    | <span data-ttu-id="90667-152">urn:schemas-microsoft-com:tabletpc:richink</span><span class="sxs-lookup"><span data-stu-id="90667-152">urn:schemas-microsoft-com:tabletpc:richink</span></span>                    |
| <span data-ttu-id="90667-153">Schemaname</span><span class="sxs-lookup"><span data-stu-id="90667-153">Schema name</span></span>  | <span data-ttu-id="90667-154">Journalreader</span><span class="sxs-lookup"><span data-stu-id="90667-154">Journal Reader</span></span>                                                |



 

 

 




