---
description: Enthält den Hintergrund für ein journaldocument-Element oder journalpage-Element.
ms.assetid: 48527c4e-50fb-4800-ac87-1646234783ba
title: Background-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e58a836c7cfd13130779c1cd6b017105bcaa6321
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368905"
---
# <a name="background-element"></a><span data-ttu-id="e4c3a-103">Background-Element</span><span class="sxs-lookup"><span data-stu-id="e4c3a-103">Background Element</span></span>

<span data-ttu-id="e4c3a-104">Enthält den Hintergrund für ein [**journaldocument**](journaldocument-element.md) -Element oder [**journalpage**](journalpage-element.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="e4c3a-104">Contains the background for a [**JournalDocument**](journaldocument-element.md) element or [**JournalPage**](journalpage-element.md) element.</span></span>

## <a name="definition"></a><span data-ttu-id="e4c3a-105">Definition</span><span class="sxs-lookup"><span data-stu-id="e4c3a-105">Definition</span></span>

``` syntax
<xs:element name="Background" type="BackgroundType" minOccurs="0" />
```

## <a name="parent-elements"></a><span data-ttu-id="e4c3a-106">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e4c3a-106">Parent Elements</span></span>

[<span data-ttu-id="e4c3a-107">**Schreib**</span><span class="sxs-lookup"><span data-stu-id="e4c3a-107">**Stationery**</span></span>](stationery-element.md)

## <a name="child-elements"></a><span data-ttu-id="e4c3a-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e4c3a-108">Child Elements</span></span>

[<span data-ttu-id="e4c3a-109">**Image**</span><span class="sxs-lookup"><span data-stu-id="e4c3a-109">**Image**</span></span>](image-element.md)

## <a name="attributes"></a><span data-ttu-id="e4c3a-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="e4c3a-110">Attributes</span></span>



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
<th><span data-ttu-id="e4c3a-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="e4c3a-111">Attribute</span></span></th>
<th><span data-ttu-id="e4c3a-112">type</span><span class="sxs-lookup"><span data-stu-id="e4c3a-112">Type</span></span></th>
<th><span data-ttu-id="e4c3a-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="e4c3a-113">Required</span></span></th>
<th><span data-ttu-id="e4c3a-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e4c3a-114">Description</span></span></th>
<th><span data-ttu-id="e4c3a-115">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="e4c3a-115">Possible Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e4c3a-116"><strong>Stil</strong></span><span class="sxs-lookup"><span data-stu-id="e4c3a-116"><strong>Style</strong></span></span></td>
<td><span data-ttu-id="e4c3a-117"><strong>xs:string</strong></span><span class="sxs-lookup"><span data-stu-id="e4c3a-117"><strong>xs:string</strong></span></span></td>
<td><span data-ttu-id="e4c3a-118">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="e4c3a-118">Required</span></span></td>
<td><span data-ttu-id="e4c3a-119">Gibt die Art des Hintergrunds an.</span><span class="sxs-lookup"><span data-stu-id="e4c3a-119">Specifies the style of the background.</span></span></td>
<td><ul>
<li><span data-ttu-id="e4c3a-120">Keine</span><span class="sxs-lookup"><span data-stu-id="e4c3a-120">None</span></span></li>
<li><span data-ttu-id="e4c3a-121">Basis</span><span class="sxs-lookup"><span data-stu-id="e4c3a-121">Solid</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e4c3a-122"><strong>Farbe</strong></span><span class="sxs-lookup"><span data-stu-id="e4c3a-122"><strong>Color</strong></span></span></td>
<td><span data-ttu-id="e4c3a-123"><a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType</span><span class="sxs-lookup"><span data-stu-id="e4c3a-123"><a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="e4c3a-124">Optional</span><span class="sxs-lookup"><span data-stu-id="e4c3a-124">Optional</span></span></td>
<td><span data-ttu-id="e4c3a-125">Gibt die Hintergrundfarbe an.</span><span class="sxs-lookup"><span data-stu-id="e4c3a-125">Specifies the color of the background.</span></span></td>
<td><span data-ttu-id="e4c3a-126">Siehe <a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType.</span><span class="sxs-lookup"><span data-stu-id="e4c3a-126">See <a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a><span data-ttu-id="e4c3a-127">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="e4c3a-127">Element Information</span></span>



|              |                                                                   |
|--------------|-------------------------------------------------------------------|
| <span data-ttu-id="e4c3a-128">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="e4c3a-128">Element type</span></span> | <span data-ttu-id="e4c3a-129">ComplexType für [**BackgroundType**](backgroundtype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="e4c3a-129">[**BackgroundType**](backgroundtype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="e4c3a-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="e4c3a-130">Namespace</span></span>    | <span data-ttu-id="e4c3a-131">urn: Schemas-Microsoft-com: TabletPC: RichInk</span><span class="sxs-lookup"><span data-stu-id="e4c3a-131">urn:schemas-microsoft-com:tabletpc:richink</span></span>                        |
| <span data-ttu-id="e4c3a-132">Schemaname</span><span class="sxs-lookup"><span data-stu-id="e4c3a-132">Schema name</span></span>  | <span data-ttu-id="e4c3a-133">Journal Leser</span><span class="sxs-lookup"><span data-stu-id="e4c3a-133">Journal Reader</span></span>                                                    |



 

 

 



