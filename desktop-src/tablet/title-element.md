---
description: Enthält Titelinformationen über die Journal Notiz.
ms.assetid: efeed3a6-de5e-4698-9dc3-d0acb3d13dee
title: Title-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2362e286482b329c50788b8eae4b4a30cbd1a125
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351558"
---
# <a name="title-element"></a><span data-ttu-id="e45f0-103">Title-Element</span><span class="sxs-lookup"><span data-stu-id="e45f0-103">Title Element</span></span>

<span data-ttu-id="e45f0-104">Enthält Titelinformationen über die Journal Notiz.</span><span class="sxs-lookup"><span data-stu-id="e45f0-104">Contains title information about the Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="e45f0-105">Definition</span><span class="sxs-lookup"><span data-stu-id="e45f0-105">Definition</span></span>

``` syntax
<xs:element name="Title" type="TitleType" minOccurs="0" />
```

## <a name="parent-elements"></a><span data-ttu-id="e45f0-106">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e45f0-106">Parent Elements</span></span>

[<span data-ttu-id="e45f0-107">**Schreib**</span><span class="sxs-lookup"><span data-stu-id="e45f0-107">**Stationery**</span></span>](stationery-element.md)

## <a name="child-elements"></a><span data-ttu-id="e45f0-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e45f0-108">Child Elements</span></span>

[<span data-ttu-id="e45f0-109">**TitleArea**</span><span class="sxs-lookup"><span data-stu-id="e45f0-109">**TitleArea**</span></span>](titlearea-element.md)

## <a name="attributes"></a><span data-ttu-id="e45f0-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="e45f0-110">Attributes</span></span>



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
<th><span data-ttu-id="e45f0-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="e45f0-111">Attribute</span></span></th>
<th><span data-ttu-id="e45f0-112">type</span><span class="sxs-lookup"><span data-stu-id="e45f0-112">Type</span></span></th>
<th><span data-ttu-id="e45f0-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="e45f0-113">Required</span></span></th>
<th><span data-ttu-id="e45f0-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e45f0-114">Description</span></span></th>
<th><span data-ttu-id="e45f0-115">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="e45f0-115">Possible Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e45f0-116"><strong>Stil</strong></span><span class="sxs-lookup"><span data-stu-id="e45f0-116"><strong>Style</strong></span></span></td>
<td><span data-ttu-id="e45f0-117"><strong>xs:string</strong></span><span class="sxs-lookup"><span data-stu-id="e45f0-117"><strong>xs:string</strong></span></span></td>
<td><span data-ttu-id="e45f0-118">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="e45f0-118">Required</span></span></td>
<td><span data-ttu-id="e45f0-119">Gibt den Typ des Rahmens an, der den Titel des Notiz Rahmens umgibt.</span><span class="sxs-lookup"><span data-stu-id="e45f0-119">Specifies the type of border surrounding the title of the note.</span></span></td>
<td><ul>
<li><span data-ttu-id="e45f0-120">Keine</span><span class="sxs-lookup"><span data-stu-id="e45f0-120">None</span></span></li>
<li><span data-ttu-id="e45f0-121">Solidsquare</span><span class="sxs-lookup"><span data-stu-id="e45f0-121">SolidSquare</span></span></li>
<li><span data-ttu-id="e45f0-122">Outlinesquare</span><span class="sxs-lookup"><span data-stu-id="e45f0-122">OutlineSquare</span></span></li>
<li><span data-ttu-id="e45f0-123">"Solidroundrecrect"</span><span class="sxs-lookup"><span data-stu-id="e45f0-123">SolidRoundRect</span></span></li>
<li><span data-ttu-id="e45f0-124">Outlineroundrect</span><span class="sxs-lookup"><span data-stu-id="e45f0-124">OutlineRoundRect</span></span></li>
<li><span data-ttu-id="e45f0-125">"Solidroundrectdottedbaseline"</span><span class="sxs-lookup"><span data-stu-id="e45f0-125">SolidRoundRectDottedBaseline</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e45f0-126"><strong>DateStyle</strong></span><span class="sxs-lookup"><span data-stu-id="e45f0-126"><strong>DateStyle</strong></span></span></td>
<td><span data-ttu-id="e45f0-127"><strong>xs:string</strong></span><span class="sxs-lookup"><span data-stu-id="e45f0-127"><strong>xs:string</strong></span></span></td>
<td><span data-ttu-id="e45f0-128">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="e45f0-128">Required</span></span></td>
<td><span data-ttu-id="e45f0-129">Definiert, ob der Titel ein Datum enthält.</span><span class="sxs-lookup"><span data-stu-id="e45f0-129">Defines whether the title includes a date or not.</span></span></td>
<td><ul>
<li><span data-ttu-id="e45f0-130">Keine</span><span class="sxs-lookup"><span data-stu-id="e45f0-130">None</span></span></li>
<li><span data-ttu-id="e45f0-131">Short</span><span class="sxs-lookup"><span data-stu-id="e45f0-131">Short</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e45f0-132"><strong>Farbe</strong></span><span class="sxs-lookup"><span data-stu-id="e45f0-132"><strong>Color</strong></span></span></td>
<td><span data-ttu-id="e45f0-133"><a href="colortype-simple-type.md"><strong>ColorType simpleType</strong></a></span><span class="sxs-lookup"><span data-stu-id="e45f0-133"><a href="colortype-simple-type.md"><strong>ColorType simpleType</strong></a></span></span></td>
<td><span data-ttu-id="e45f0-134">Optional</span><span class="sxs-lookup"><span data-stu-id="e45f0-134">Optional</span></span></td>
<td><span data-ttu-id="e45f0-135">Gibt die Hintergrundfarbe an.</span><span class="sxs-lookup"><span data-stu-id="e45f0-135">Specifies the color of the background.</span></span></td>
<td><span data-ttu-id="e45f0-136">Siehe <a href="colortype-simple-type.md"><strong>ColorType simpleType</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="e45f0-136">See <a href="colortype-simple-type.md"><strong>ColorType simpleType</strong></a>.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a><span data-ttu-id="e45f0-137">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="e45f0-137">Element Information</span></span>



|              |                                                         |
|--------------|---------------------------------------------------------|
| <span data-ttu-id="e45f0-138">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="e45f0-138">Element type</span></span> | <span data-ttu-id="e45f0-139">ComplexType für [**titletype**](titletype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="e45f0-139">[**TitleType**](titletype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="e45f0-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="e45f0-140">Namespace</span></span>    | <span data-ttu-id="e45f0-141">urn: Schemas-Microsoft-com: TabletPC: RichInk</span><span class="sxs-lookup"><span data-stu-id="e45f0-141">urn:schemas-microsoft-com:tabletpc:richink</span></span>              |
| <span data-ttu-id="e45f0-142">Schemaname</span><span class="sxs-lookup"><span data-stu-id="e45f0-142">Schema name</span></span>  | <span data-ttu-id="e45f0-143">Journal Leser</span><span class="sxs-lookup"><span data-stu-id="e45f0-143">Journal Reader</span></span>                                          |



 

 

 



