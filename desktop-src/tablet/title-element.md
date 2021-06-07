---
description: Enthält Titelinformationen zur Journalnotiz.
ms.assetid: efeed3a6-de5e-4698-9dc3-d0acb3d13dee
title: Title-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef687f809aae5c3722cdad84ee63d79c7bfcfb21
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432222"
---
# <a name="title-element"></a><span data-ttu-id="57de6-103">Title-Element</span><span class="sxs-lookup"><span data-stu-id="57de6-103">Title Element</span></span>

<span data-ttu-id="57de6-104">Enthält Titelinformationen zur Journalnotiz.</span><span class="sxs-lookup"><span data-stu-id="57de6-104">Contains title information about the Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="57de6-105">Definition</span><span class="sxs-lookup"><span data-stu-id="57de6-105">Definition</span></span>

``` syntax
<xs:element name="Title" type="TitleType" minOccurs="0" />
```

## <a name="parent-elements"></a><span data-ttu-id="57de6-106">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="57de6-106">Parent Elements</span></span>

[<span data-ttu-id="57de6-107">**Briefpapier**</span><span class="sxs-lookup"><span data-stu-id="57de6-107">**Stationery**</span></span>](stationery-element.md)

## <a name="child-elements"></a><span data-ttu-id="57de6-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="57de6-108">Child Elements</span></span>

[<span data-ttu-id="57de6-109">**TitleArea**</span><span class="sxs-lookup"><span data-stu-id="57de6-109">**TitleArea**</span></span>](titlearea-element.md)

## <a name="attributes"></a><span data-ttu-id="57de6-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="57de6-110">Attributes</span></span>



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
<th><span data-ttu-id="57de6-111">attribute</span><span class="sxs-lookup"><span data-stu-id="57de6-111">Attribute</span></span></th>
<th><span data-ttu-id="57de6-112">Typ</span><span class="sxs-lookup"><span data-stu-id="57de6-112">Type</span></span></th>
<th><span data-ttu-id="57de6-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="57de6-113">Required</span></span></th>
<th><span data-ttu-id="57de6-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="57de6-114">Description</span></span></th>
<th><span data-ttu-id="57de6-115">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="57de6-115">Possible Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="57de6-116"><strong>Stil</strong></span><span class="sxs-lookup"><span data-stu-id="57de6-116"><strong>Style</strong></span></span></td>
<td><span data-ttu-id="57de6-117"><strong>xs:string</strong></span><span class="sxs-lookup"><span data-stu-id="57de6-117"><strong>xs:string</strong></span></span></td>
<td><span data-ttu-id="57de6-118">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="57de6-118">Required</span></span></td>
<td><span data-ttu-id="57de6-119">Gibt den Typ des Rahmens um den Titel der Notiz an.</span><span class="sxs-lookup"><span data-stu-id="57de6-119">Specifies the type of border surrounding the title of the note.</span></span></td>
<td><ul>
<li><span data-ttu-id="57de6-120">Keine</span><span class="sxs-lookup"><span data-stu-id="57de6-120">None</span></span></li>
<li><span data-ttu-id="57de6-121">SolidSquare</span><span class="sxs-lookup"><span data-stu-id="57de6-121">SolidSquare</span></span></li>
<li><span data-ttu-id="57de6-122">OutlineSquare</span><span class="sxs-lookup"><span data-stu-id="57de6-122">OutlineSquare</span></span></li>
<li><span data-ttu-id="57de6-123">SolidRoundRect</span><span class="sxs-lookup"><span data-stu-id="57de6-123">SolidRoundRect</span></span></li>
<li><span data-ttu-id="57de6-124">OutlineRoundRect</span><span class="sxs-lookup"><span data-stu-id="57de6-124">OutlineRoundRect</span></span></li>
<li><span data-ttu-id="57de6-125">SolidRoundRectDottedBaseline</span><span class="sxs-lookup"><span data-stu-id="57de6-125">SolidRoundRectDottedBaseline</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="57de6-126"><strong>DateStyle</strong></span><span class="sxs-lookup"><span data-stu-id="57de6-126"><strong>DateStyle</strong></span></span></td>
<td><span data-ttu-id="57de6-127"><strong>xs:string</strong></span><span class="sxs-lookup"><span data-stu-id="57de6-127"><strong>xs:string</strong></span></span></td>
<td><span data-ttu-id="57de6-128">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="57de6-128">Required</span></span></td>
<td><span data-ttu-id="57de6-129">Definiert, ob der Titel ein Datum enthält oder nicht.</span><span class="sxs-lookup"><span data-stu-id="57de6-129">Defines whether the title includes a date or not.</span></span></td>
<td><ul>
<li><span data-ttu-id="57de6-130">Keine</span><span class="sxs-lookup"><span data-stu-id="57de6-130">None</span></span></li>
<li><span data-ttu-id="57de6-131">Short</span><span class="sxs-lookup"><span data-stu-id="57de6-131">Short</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="57de6-132"><strong>Farbe</strong></span><span class="sxs-lookup"><span data-stu-id="57de6-132"><strong>Color</strong></span></span></td>
<td><span data-ttu-id="57de6-133"><a href="colortype-simple-type.md"><strong>ColorType simpleType</strong></a></span><span class="sxs-lookup"><span data-stu-id="57de6-133"><a href="colortype-simple-type.md"><strong>ColorType simpleType</strong></a></span></span></td>
<td><span data-ttu-id="57de6-134">Optional</span><span class="sxs-lookup"><span data-stu-id="57de6-134">Optional</span></span></td>
<td><span data-ttu-id="57de6-135">Gibt die Hintergrundfarbe an.</span><span class="sxs-lookup"><span data-stu-id="57de6-135">Specifies the color of the background.</span></span></td>
<td><span data-ttu-id="57de6-136">Siehe <a href="colortype-simple-type.md"><strong>ColorType simpleType</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="57de6-136">See <a href="colortype-simple-type.md"><strong>ColorType simpleType</strong></a>.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a><span data-ttu-id="57de6-137">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="57de6-137">Element Information</span></span>



| <span data-ttu-id="57de6-138">Element</span><span class="sxs-lookup"><span data-stu-id="57de6-138">Element</span></span>      | <span data-ttu-id="57de6-139">Wert</span><span class="sxs-lookup"><span data-stu-id="57de6-139">Value</span></span>                                                   |
|--------------|---------------------------------------------------------|
| <span data-ttu-id="57de6-140">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="57de6-140">Element type</span></span> | <span data-ttu-id="57de6-141">[**complexType: TitleType**](titletype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="57de6-141">[**TitleType**](titletype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="57de6-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="57de6-142">Namespace</span></span>    | <span data-ttu-id="57de6-143">urn:schemas-microsoft-com:tabletpc:richink</span><span class="sxs-lookup"><span data-stu-id="57de6-143">urn:schemas-microsoft-com:tabletpc:richink</span></span>              |
| <span data-ttu-id="57de6-144">Schemaname</span><span class="sxs-lookup"><span data-stu-id="57de6-144">Schema name</span></span>  | <span data-ttu-id="57de6-145">Journalreader</span><span class="sxs-lookup"><span data-stu-id="57de6-145">Journal Reader</span></span>                                          |



 

 

 



