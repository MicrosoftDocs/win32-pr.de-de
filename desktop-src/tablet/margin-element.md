---
description: Definiert die Rand Linien, die auf der Seite gezeichnet werden.
ms.assetid: c3047706-affd-4feb-9d48-cfb4c7dd6fa0
title: Margin-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0500d4db165012393cb600c1e118089b68c76695
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218361"
---
# <a name="margin-element"></a><span data-ttu-id="31222-103">Margin-Element</span><span class="sxs-lookup"><span data-stu-id="31222-103">Margin Element</span></span>

<span data-ttu-id="31222-104">Definiert die Rand Linien, die auf der Seite gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="31222-104">Defines the margin lines drawn on the page.</span></span>

## <a name="definition"></a><span data-ttu-id="31222-105">Definition</span><span class="sxs-lookup"><span data-stu-id="31222-105">Definition</span></span>

``` syntax
<xs:complexType name="MarginType">
   <xs:attribute name="Style" use="required" type="LineLayoutStyleType" />
   <xs:attribute name="Color" type="ColorType" />
   <xs:attribute name="Type" type="MarginTypeType" />
   <xs:attribute name="Spacing" type="xs:positiveInteger" />
</xs:complexType>
```

## <a name="parent-elements"></a><span data-ttu-id="31222-106">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="31222-106">Parent Elements</span></span>

<span data-ttu-id="31222-107">Keine</span><span class="sxs-lookup"><span data-stu-id="31222-107">None.</span></span>

## <a name="child-elements"></a><span data-ttu-id="31222-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="31222-108">Child Elements</span></span>

<span data-ttu-id="31222-109">Keine...</span><span class="sxs-lookup"><span data-stu-id="31222-109">None..</span></span>

## <a name="attributes"></a><span data-ttu-id="31222-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="31222-110">Attributes</span></span>



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
<th><span data-ttu-id="31222-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="31222-111">Attribute</span></span></th>
<th><span data-ttu-id="31222-112">type</span><span class="sxs-lookup"><span data-stu-id="31222-112">Type</span></span></th>
<th><span data-ttu-id="31222-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="31222-113">Required</span></span></th>
<th><span data-ttu-id="31222-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="31222-114">Description</span></span></th>
<th><span data-ttu-id="31222-115">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="31222-115">Possible Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="31222-116"><strong>Stil</strong></span><span class="sxs-lookup"><span data-stu-id="31222-116"><strong>Style</strong></span></span></td>
<td><span data-ttu-id="31222-117"><a href="linelayoutstyletype-simple-type.md"><strong>Linelayoutstyletype</strong></a> simpleType</span><span class="sxs-lookup"><span data-stu-id="31222-117"><a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="31222-118">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="31222-118">Required</span></span></td>
<td><span data-ttu-id="31222-119">Gibt den Typ der zu Zeichenden Zeile an.</span><span class="sxs-lookup"><span data-stu-id="31222-119">Specifies the type of line to be drawn.</span></span></td>
<td><ul>
<li><span data-ttu-id="31222-120">Keine</span><span class="sxs-lookup"><span data-stu-id="31222-120">None</span></span></li>
<li><span data-ttu-id="31222-121">Basis</span><span class="sxs-lookup"><span data-stu-id="31222-121">Solid</span></span></li>
<li><span data-ttu-id="31222-122">Strich</span><span class="sxs-lookup"><span data-stu-id="31222-122">Dash</span></span></li>
<li><span data-ttu-id="31222-123">Punkt</span><span class="sxs-lookup"><span data-stu-id="31222-123">Dot</span></span></li>
<li><span data-ttu-id="31222-124">DashDot</span><span class="sxs-lookup"><span data-stu-id="31222-124">DashDot</span></span></li>
<li><span data-ttu-id="31222-125">DashDotDot</span><span class="sxs-lookup"><span data-stu-id="31222-125">DashDotDot</span></span></li>
<li><span data-ttu-id="31222-126">Double</span><span class="sxs-lookup"><span data-stu-id="31222-126">Double</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="31222-127"><strong>Farbe</strong></span><span class="sxs-lookup"><span data-stu-id="31222-127"><strong>Color</strong></span></span></td>
<td><span data-ttu-id="31222-128"><a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType</span><span class="sxs-lookup"><span data-stu-id="31222-128"><a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="31222-129">Optional</span><span class="sxs-lookup"><span data-stu-id="31222-129">Optional</span></span></td>
<td><span data-ttu-id="31222-130">Farbe des Elements.</span><span class="sxs-lookup"><span data-stu-id="31222-130">Color of the element.</span></span></td>
<td><span data-ttu-id="31222-131">Ein Hexadezimal-RGB-Wert.</span><span class="sxs-lookup"><span data-stu-id="31222-131">A hexadecimal RGB value.</span></span> <span data-ttu-id="31222-132">Entspricht dem folgenden regulären Ausdruck: # [0-9a-zA-Z] {6} .</span><span class="sxs-lookup"><span data-stu-id="31222-132">Matches the following regular expression: #[0-9a-zA-Z]{6}.</span></span> <span data-ttu-id="31222-133">Beispielsweise #4a79B5.</span><span class="sxs-lookup"><span data-stu-id="31222-133">For example, #4a79B5.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="31222-134"><strong>Type</strong></span><span class="sxs-lookup"><span data-stu-id="31222-134"><strong>Type</strong></span></span></td>
<td><span data-ttu-id="31222-135"><a href="margintypetype-simple-type.md"><strong>Margintypetype</strong></a> simpleType</span><span class="sxs-lookup"><span data-stu-id="31222-135"><a href="margintypetype-simple-type.md"><strong>MarginTypeType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="31222-136">Optional</span><span class="sxs-lookup"><span data-stu-id="31222-136">Optional</span></span></td>
<td><span data-ttu-id="31222-137">Gibt den linken oder rechten Rand an.</span><span class="sxs-lookup"><span data-stu-id="31222-137">Indicates Left or Right margin.</span></span></td>
<td><ul>
<li><span data-ttu-id="31222-138">Left</span><span class="sxs-lookup"><span data-stu-id="31222-138">Left</span></span></li>
<li><span data-ttu-id="31222-139">Right</span><span class="sxs-lookup"><span data-stu-id="31222-139">Right</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="31222-140"><strong>Abstand</strong></span><span class="sxs-lookup"><span data-stu-id="31222-140"><strong>Spacing</strong></span></span></td>
<td><span data-ttu-id="31222-141"><strong>xs:nonNegativeInteger</strong></span><span class="sxs-lookup"><span data-stu-id="31222-141"><strong>xs:nonNegativeInteger</strong></span></span></td>
<td><span data-ttu-id="31222-142">Optional</span><span class="sxs-lookup"><span data-stu-id="31222-142">Optional</span></span></td>
<td><span data-ttu-id="31222-143">Abstand zwischen dem Rand der Seite und dem Rand.</span><span class="sxs-lookup"><span data-stu-id="31222-143">Spacing between edge of page and margin.</span></span></td>
<td><span data-ttu-id="31222-144">Eine beliebige nicht negative ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="31222-144">Any non-negative integer.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a><span data-ttu-id="31222-145">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="31222-145">Element Information</span></span>



|              |                                                           |
|--------------|-----------------------------------------------------------|
| <span data-ttu-id="31222-146">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="31222-146">Element type</span></span> | <span data-ttu-id="31222-147">ComplexType ' [**margintype**](margintype-complex-type.md) '</span><span class="sxs-lookup"><span data-stu-id="31222-147">[**MarginType**](margintype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="31222-148">Namespace</span><span class="sxs-lookup"><span data-stu-id="31222-148">Namespace</span></span>    | <span data-ttu-id="31222-149">urn: Schemas-Microsoft-com: TabletPC: RichInk</span><span class="sxs-lookup"><span data-stu-id="31222-149">urn:schemas-microsoft-com:tabletpc:richink</span></span>                |
| <span data-ttu-id="31222-150">Schemaname</span><span class="sxs-lookup"><span data-stu-id="31222-150">Schema name</span></span>  | <span data-ttu-id="31222-151">Journal Leser</span><span class="sxs-lookup"><span data-stu-id="31222-151">Journal Reader</span></span>                                            |



 

 

 




