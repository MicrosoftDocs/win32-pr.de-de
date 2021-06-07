---
description: Definiert die Randlinien, die auf der Seite gezeichnet werden.
ms.assetid: c3047706-affd-4feb-9d48-cfb4c7dd6fa0
title: Margin-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 547177a10fc3724f3b9bf3dde65f857d03f0f2a4
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432132"
---
# <a name="margin-element"></a><span data-ttu-id="d54a3-103">Margin-Element</span><span class="sxs-lookup"><span data-stu-id="d54a3-103">Margin Element</span></span>

<span data-ttu-id="d54a3-104">Definiert die Randlinien, die auf der Seite gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="d54a3-104">Defines the margin lines drawn on the page.</span></span>

## <a name="definition"></a><span data-ttu-id="d54a3-105">Definition</span><span class="sxs-lookup"><span data-stu-id="d54a3-105">Definition</span></span>

``` syntax
<xs:complexType name="MarginType">
   <xs:attribute name="Style" use="required" type="LineLayoutStyleType" />
   <xs:attribute name="Color" type="ColorType" />
   <xs:attribute name="Type" type="MarginTypeType" />
   <xs:attribute name="Spacing" type="xs:positiveInteger" />
</xs:complexType>
```

## <a name="parent-elements"></a><span data-ttu-id="d54a3-106">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d54a3-106">Parent Elements</span></span>

<span data-ttu-id="d54a3-107">Keine</span><span class="sxs-lookup"><span data-stu-id="d54a3-107">None.</span></span>

## <a name="child-elements"></a><span data-ttu-id="d54a3-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d54a3-108">Child Elements</span></span>

<span data-ttu-id="d54a3-109">nichts..</span><span class="sxs-lookup"><span data-stu-id="d54a3-109">None..</span></span>

## <a name="attributes"></a><span data-ttu-id="d54a3-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="d54a3-110">Attributes</span></span>



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
<th><span data-ttu-id="d54a3-111">attribute</span><span class="sxs-lookup"><span data-stu-id="d54a3-111">Attribute</span></span></th>
<th><span data-ttu-id="d54a3-112">Typ</span><span class="sxs-lookup"><span data-stu-id="d54a3-112">Type</span></span></th>
<th><span data-ttu-id="d54a3-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="d54a3-113">Required</span></span></th>
<th><span data-ttu-id="d54a3-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d54a3-114">Description</span></span></th>
<th><span data-ttu-id="d54a3-115">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="d54a3-115">Possible Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d54a3-116"><strong>Stil</strong></span><span class="sxs-lookup"><span data-stu-id="d54a3-116"><strong>Style</strong></span></span></td>
<td><span data-ttu-id="d54a3-117"><a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a> simpleType</span><span class="sxs-lookup"><span data-stu-id="d54a3-117"><a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="d54a3-118">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="d54a3-118">Required</span></span></td>
<td><span data-ttu-id="d54a3-119">Gibt den Typ der zu zeichnenden Linie an.</span><span class="sxs-lookup"><span data-stu-id="d54a3-119">Specifies the type of line to be drawn.</span></span></td>
<td><ul>
<li><span data-ttu-id="d54a3-120">Keine</span><span class="sxs-lookup"><span data-stu-id="d54a3-120">None</span></span></li>
<li><span data-ttu-id="d54a3-121">Basis</span><span class="sxs-lookup"><span data-stu-id="d54a3-121">Solid</span></span></li>
<li><span data-ttu-id="d54a3-122">Strich</span><span class="sxs-lookup"><span data-stu-id="d54a3-122">Dash</span></span></li>
<li><span data-ttu-id="d54a3-123">Punkt</span><span class="sxs-lookup"><span data-stu-id="d54a3-123">Dot</span></span></li>
<li><span data-ttu-id="d54a3-124">DashDot</span><span class="sxs-lookup"><span data-stu-id="d54a3-124">DashDot</span></span></li>
<li><span data-ttu-id="d54a3-125">DashDotDot</span><span class="sxs-lookup"><span data-stu-id="d54a3-125">DashDotDot</span></span></li>
<li><span data-ttu-id="d54a3-126">Double</span><span class="sxs-lookup"><span data-stu-id="d54a3-126">Double</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d54a3-127"><strong>Farbe</strong></span><span class="sxs-lookup"><span data-stu-id="d54a3-127"><strong>Color</strong></span></span></td>
<td><span data-ttu-id="d54a3-128"><a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType</span><span class="sxs-lookup"><span data-stu-id="d54a3-128"><a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="d54a3-129">Optional</span><span class="sxs-lookup"><span data-stu-id="d54a3-129">Optional</span></span></td>
<td><span data-ttu-id="d54a3-130">Farbe des Elements.</span><span class="sxs-lookup"><span data-stu-id="d54a3-130">Color of the element.</span></span></td>
<td><span data-ttu-id="d54a3-131">Ein hexadezimaler RGB-Wert.</span><span class="sxs-lookup"><span data-stu-id="d54a3-131">A hexadecimal RGB value.</span></span> <span data-ttu-id="d54a3-132">Entspricht dem folgenden regulären Ausdruck: #[0-9a-zA-Z] {6} .</span><span class="sxs-lookup"><span data-stu-id="d54a3-132">Matches the following regular expression: #[0-9a-zA-Z]{6}.</span></span> <span data-ttu-id="d54a3-133">Beispiel: #4a79B5.</span><span class="sxs-lookup"><span data-stu-id="d54a3-133">For example, #4a79B5.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d54a3-134"><strong>Typ</strong></span><span class="sxs-lookup"><span data-stu-id="d54a3-134"><strong>Type</strong></span></span></td>
<td><span data-ttu-id="d54a3-135"><a href="margintypetype-simple-type.md"><strong>MarginTypeType</strong></a> simpleType</span><span class="sxs-lookup"><span data-stu-id="d54a3-135"><a href="margintypetype-simple-type.md"><strong>MarginTypeType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="d54a3-136">Optional</span><span class="sxs-lookup"><span data-stu-id="d54a3-136">Optional</span></span></td>
<td><span data-ttu-id="d54a3-137">Gibt den linken oder rechten Rand an.</span><span class="sxs-lookup"><span data-stu-id="d54a3-137">Indicates Left or Right margin.</span></span></td>
<td><ul>
<li><span data-ttu-id="d54a3-138">Left</span><span class="sxs-lookup"><span data-stu-id="d54a3-138">Left</span></span></li>
<li><span data-ttu-id="d54a3-139">Right</span><span class="sxs-lookup"><span data-stu-id="d54a3-139">Right</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d54a3-140"><strong>Abstand</strong></span><span class="sxs-lookup"><span data-stu-id="d54a3-140"><strong>Spacing</strong></span></span></td>
<td><span data-ttu-id="d54a3-141"><strong>xs:nonNegativeInteger</strong></span><span class="sxs-lookup"><span data-stu-id="d54a3-141"><strong>xs:nonNegativeInteger</strong></span></span></td>
<td><span data-ttu-id="d54a3-142">Optional</span><span class="sxs-lookup"><span data-stu-id="d54a3-142">Optional</span></span></td>
<td><span data-ttu-id="d54a3-143">Abstand zwischen Seitenrand und Rand.</span><span class="sxs-lookup"><span data-stu-id="d54a3-143">Spacing between edge of page and margin.</span></span></td>
<td><span data-ttu-id="d54a3-144">Eine beliebige nicht negative ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="d54a3-144">Any non-negative integer.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a><span data-ttu-id="d54a3-145">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="d54a3-145">Element Information</span></span>



|  <span data-ttu-id="d54a3-146">Element</span><span class="sxs-lookup"><span data-stu-id="d54a3-146">Element</span></span>     | <span data-ttu-id="d54a3-147">Wert</span><span class="sxs-lookup"><span data-stu-id="d54a3-147">Value</span></span>                                                     |
|--------------|-----------------------------------------------------------|
| <span data-ttu-id="d54a3-148">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="d54a3-148">Element type</span></span> | <span data-ttu-id="d54a3-149">[**complexType: MarginType**](margintype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="d54a3-149">[**MarginType**](margintype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="d54a3-150">Namespace</span><span class="sxs-lookup"><span data-stu-id="d54a3-150">Namespace</span></span>    | <span data-ttu-id="d54a3-151">urn:schemas-microsoft-com:tabletpc:richink</span><span class="sxs-lookup"><span data-stu-id="d54a3-151">urn:schemas-microsoft-com:tabletpc:richink</span></span>                |
| <span data-ttu-id="d54a3-152">Schemaname</span><span class="sxs-lookup"><span data-stu-id="d54a3-152">Schema name</span></span>  | <span data-ttu-id="d54a3-153">Journalreader</span><span class="sxs-lookup"><span data-stu-id="d54a3-153">Journal Reader</span></span>                                            |



 

 

 




