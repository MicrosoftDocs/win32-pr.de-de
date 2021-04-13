---
description: Enthält die Informationen, die die vertikale Komponente der Zeilen in der von der Journal Notiz verwendeten Schreibweise beschreiben. Wird beispielsweise verwendet, wenn der Hinweis Rasterlinien enthält.
ms.assetid: af6f485e-13df-41bb-b57a-10d8393b83e7
title: Vertikales Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 191a9c5cb3190cff9b1e379a68dbfab49ddc25a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343269"
---
# <a name="vertical-element"></a><span data-ttu-id="4af4e-104">Vertikales Element</span><span class="sxs-lookup"><span data-stu-id="4af4e-104">Vertical Element</span></span>

<span data-ttu-id="4af4e-105">Enthält die Informationen, die die vertikale Komponente der Zeilen in der von der Journal Notiz verwendeten Schreibweise beschreiben.</span><span class="sxs-lookup"><span data-stu-id="4af4e-105">Contains the information that describes the vertical component of the lines in the stationery used by the Journal note.</span></span> <span data-ttu-id="4af4e-106">Wird beispielsweise verwendet, wenn der Hinweis Rasterlinien enthält.</span><span class="sxs-lookup"><span data-stu-id="4af4e-106">Used, for example, when the note has grid lines.</span></span>

## <a name="definition"></a><span data-ttu-id="4af4e-107">Definition</span><span class="sxs-lookup"><span data-stu-id="4af4e-107">Definition</span></span>

``` syntax
<xs:element name="Vertical" type="VerticalType" minOccurs="0" />
```

## <a name="parent-elements"></a><span data-ttu-id="4af4e-108">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4af4e-108">Parent Elements</span></span>

[<span data-ttu-id="4af4e-109">**Linelayout**</span><span class="sxs-lookup"><span data-stu-id="4af4e-109">**LineLayout**</span></span>](linelayout-element.md)

## <a name="child-elements"></a><span data-ttu-id="4af4e-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4af4e-110">Child Elements</span></span>

<span data-ttu-id="4af4e-111">Keine</span><span class="sxs-lookup"><span data-stu-id="4af4e-111">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="4af4e-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="4af4e-112">Attributes</span></span>



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
<th><span data-ttu-id="4af4e-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="4af4e-113">Attribute</span></span></th>
<th><span data-ttu-id="4af4e-114">type</span><span class="sxs-lookup"><span data-stu-id="4af4e-114">Type</span></span></th>
<th><span data-ttu-id="4af4e-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="4af4e-115">Required</span></span></th>
<th><span data-ttu-id="4af4e-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4af4e-116">Description</span></span></th>
<th><span data-ttu-id="4af4e-117">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="4af4e-117">Possible Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4af4e-118"><strong>Stil</strong></span><span class="sxs-lookup"><span data-stu-id="4af4e-118"><strong>Style</strong></span></span></td>
<td><span data-ttu-id="4af4e-119"><a href="linelayoutstyletype-simple-type.md"><strong>Linelayoutstyletype</strong></a> simpleType</span><span class="sxs-lookup"><span data-stu-id="4af4e-119"><a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="4af4e-120">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="4af4e-120">Required</span></span></td>
<td><span data-ttu-id="4af4e-121">Gibt den Typ der zu Zeichenden Zeile an.</span><span class="sxs-lookup"><span data-stu-id="4af4e-121">Specifies the type of line to be drawn.</span></span></td>
<td><ul>
<li><span data-ttu-id="4af4e-122">Keine</span><span class="sxs-lookup"><span data-stu-id="4af4e-122">None</span></span></li>
<li><span data-ttu-id="4af4e-123">Basis</span><span class="sxs-lookup"><span data-stu-id="4af4e-123">Solid</span></span></li>
<li><span data-ttu-id="4af4e-124">Strich</span><span class="sxs-lookup"><span data-stu-id="4af4e-124">Dash</span></span></li>
<li><span data-ttu-id="4af4e-125">Punkt</span><span class="sxs-lookup"><span data-stu-id="4af4e-125">Dot</span></span></li>
<li><span data-ttu-id="4af4e-126">DashDot</span><span class="sxs-lookup"><span data-stu-id="4af4e-126">DashDot</span></span></li>
<li><span data-ttu-id="4af4e-127">DashDotDot</span><span class="sxs-lookup"><span data-stu-id="4af4e-127">DashDotDot</span></span></li>
<li><span data-ttu-id="4af4e-128">Double</span><span class="sxs-lookup"><span data-stu-id="4af4e-128">Double</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4af4e-129"><strong>Farbe</strong></span><span class="sxs-lookup"><span data-stu-id="4af4e-129"><strong>Color</strong></span></span></td>
<td><span data-ttu-id="4af4e-130"><a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType</span><span class="sxs-lookup"><span data-stu-id="4af4e-130"><a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="4af4e-131">Optional</span><span class="sxs-lookup"><span data-stu-id="4af4e-131">Optional</span></span></td>
<td><span data-ttu-id="4af4e-132">Farbe des Elements.</span><span class="sxs-lookup"><span data-stu-id="4af4e-132">Color of the element.</span></span></td>
<td><span data-ttu-id="4af4e-133">Ein Hexadezimal-RGB-Wert.</span><span class="sxs-lookup"><span data-stu-id="4af4e-133">A hexadecimal RGB value.</span></span> <span data-ttu-id="4af4e-134">Entspricht dem folgenden regulären Ausdruck: # [0-9a-zA-Z] {6} .</span><span class="sxs-lookup"><span data-stu-id="4af4e-134">Matches the following regular expression: #[0-9a-zA-Z]{6}.</span></span> <span data-ttu-id="4af4e-135">Beispielsweise #4a79B5.</span><span class="sxs-lookup"><span data-stu-id="4af4e-135">For example, #4a79B5.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4af4e-136"><strong>SpacingBefore</strong></span><span class="sxs-lookup"><span data-stu-id="4af4e-136"><strong>SpacingBefore</strong></span></span></td>
<td><span data-ttu-id="4af4e-137"><strong>xs:nonNegativeInteger</strong></span><span class="sxs-lookup"><span data-stu-id="4af4e-137"><strong>xs:nonNegativeInteger</strong></span></span></td>
<td><span data-ttu-id="4af4e-138">Optional</span><span class="sxs-lookup"><span data-stu-id="4af4e-138">Optional</span></span></td>
<td><span data-ttu-id="4af4e-139">Abstand vor dem Element.</span><span class="sxs-lookup"><span data-stu-id="4af4e-139">Spacing before the element.</span></span></td>
<td><span data-ttu-id="4af4e-140">Eine beliebige nicht negative ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="4af4e-140">Any non-negative integer.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4af4e-141"><strong>Abstand zwischen</strong></span><span class="sxs-lookup"><span data-stu-id="4af4e-141"><strong>SpacingBetween</strong></span></span></td>
<td><span data-ttu-id="4af4e-142"><strong>xs:nonNegativeInteger</strong></span><span class="sxs-lookup"><span data-stu-id="4af4e-142"><strong>xs:nonNegativeInteger</strong></span></span></td>
<td><span data-ttu-id="4af4e-143">Optional</span><span class="sxs-lookup"><span data-stu-id="4af4e-143">Optional</span></span></td>
<td><span data-ttu-id="4af4e-144">Abstand zwischen diesem Element und umgebenden Elementen.</span><span class="sxs-lookup"><span data-stu-id="4af4e-144">Spacing between this element and surrounding elements.</span></span></td>
<td><span data-ttu-id="4af4e-145">Eine beliebige nicht negative ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="4af4e-145">Any non-negative integer.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a><span data-ttu-id="4af4e-146">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="4af4e-146">Element Information</span></span>



|              |                                                               |
|--------------|---------------------------------------------------------------|
| <span data-ttu-id="4af4e-147">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="4af4e-147">Element type</span></span> | <span data-ttu-id="4af4e-148">ComplexType ' [**verticaltype**](verticaltype-complex-type.md) '</span><span class="sxs-lookup"><span data-stu-id="4af4e-148">[**VerticalType**](verticaltype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="4af4e-149">Namespace</span><span class="sxs-lookup"><span data-stu-id="4af4e-149">Namespace</span></span>    | <span data-ttu-id="4af4e-150">urn: Schemas-Microsoft-com: TabletPC: RichInk</span><span class="sxs-lookup"><span data-stu-id="4af4e-150">urn:schemas-microsoft-com:tabletpc:richink</span></span>                    |
| <span data-ttu-id="4af4e-151">Schemaname</span><span class="sxs-lookup"><span data-stu-id="4af4e-151">Schema name</span></span>  | <span data-ttu-id="4af4e-152">Journal Leser</span><span class="sxs-lookup"><span data-stu-id="4af4e-152">Journal Reader</span></span>                                                |



 

 

 




