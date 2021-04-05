---
title: Verticalmenulayout-Element
description: Stellt ein vertikales Layout für Elemente in einem Katalog dar.
ms.assetid: 4124c639-c078-4eb0-9d36-37d1ffcebac0
keywords:
- Windows-Menüband für verticalmenulayout-Element
topic_type:
- apiref
api_name:
- VerticalMenuLayout
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7fb848edcc8ab5ddff1405f35d5abd414ae40d15
ms.sourcegitcommit: 2387bc0339a1764564c1509e72ed5f2e8ae60b36
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/30/2020
ms.locfileid: "103724344"
---
# <a name="verticalmenulayout-element"></a><span data-ttu-id="e7217-104">Verticalmenulayout-Element</span><span class="sxs-lookup"><span data-stu-id="e7217-104">VerticalMenuLayout element</span></span>

<span data-ttu-id="e7217-105">Stellt ein vertikales Layout für Elemente in einem Katalog dar.</span><span class="sxs-lookup"><span data-stu-id="e7217-105">Represents a vertical layout for items in a gallery.</span></span>

## <a name="usage"></a><span data-ttu-id="e7217-106">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="e7217-106">Usage</span></span>

``` syntax
<VerticalMenuLayout
  Rows = "xs:integer"
  IsMultipleHighlightingEnabled = "xs:boolean"
  Gripper = "xs:string"/>
```

## <a name="attributes"></a><span data-ttu-id="e7217-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="e7217-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e7217-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="e7217-108">Attribute</span></span></th>
<th><span data-ttu-id="e7217-109">type</span><span class="sxs-lookup"><span data-stu-id="e7217-109">Type</span></span></th>
<th><span data-ttu-id="e7217-110">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="e7217-110">Required</span></span></th>
<th><span data-ttu-id="e7217-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e7217-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e7217-112"><strong>Zieh Elements</strong></span><span class="sxs-lookup"><span data-stu-id="e7217-112"><strong>Gripper</strong></span></span><br/></td>
<td><span data-ttu-id="e7217-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="e7217-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="e7217-114">Nein</span><span class="sxs-lookup"><span data-stu-id="e7217-114">No</span></span><br/></td>
<td><span data-ttu-id="e7217-115">Ein an den Katalog-Dropdown angefügtes Handle zur Anpassung der Größe.</span><span class="sxs-lookup"><span data-stu-id="e7217-115">A resizing handle attached to the gallery drop down.</span></span> <br/> <img src="images/controls/gripper.png" alt="Screen shot of a vertical gripper." /><br/> <span data-ttu-id="e7217-116">Beschränkt auf einen der folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="e7217-116">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="e7217-117">
<dt><span></span><span></span><strong></strong> Gar</span><span class="sxs-lookup"><span data-stu-id="e7217-117">
<dt><span></span><span></span><strong></strong> (None)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="e7217-118"><dt><span></span><span></span><strong></strong> Rechtes</span><span class="sxs-lookup"><span data-stu-id="e7217-118"><dt><span></span><span></span><strong></strong> (Vertical)</span></span><br/> </dt> <dd> <span data-ttu-id="e7217-119">Standard.</span><span class="sxs-lookup"><span data-stu-id="e7217-119">Default.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e7217-120"><strong>Ismultiplehighlightingenabled</strong></span><span class="sxs-lookup"><span data-stu-id="e7217-120"><strong>IsMultipleHighlightingEnabled</strong></span></span><br/></td>
<td><span data-ttu-id="e7217-121">xs:boolean</span><span class="sxs-lookup"><span data-stu-id="e7217-121">xs:boolean</span></span><br/></td>
<td><span data-ttu-id="e7217-122">Nein</span><span class="sxs-lookup"><span data-stu-id="e7217-122">No</span></span><br/></td>
<td><span data-ttu-id="e7217-123"><strong>Windows 8 und höher</strong></span><span class="sxs-lookup"><span data-stu-id="e7217-123"><strong>Windows 8 and newer</strong></span></span><br/> <span data-ttu-id="e7217-124">Hebt alle Elemente in der Liste bis einschließlich des aktuellen Mouseover-Elements hervor (anstelle des Mouseover-Elements).</span><span class="sxs-lookup"><span data-stu-id="e7217-124">Highlights all items in the list up to, and including, the current mouseover item (instead of the mouseover item only).</span></span> <span data-ttu-id="e7217-125">Wird normalerweise für mehrere Funktionen zum Rückgängigmachen und wieder <strong>holen</strong> <strong></strong></span><span class="sxs-lookup"><span data-stu-id="e7217-125">Typically used for multiple <strong>Undo</strong> and <strong>Redo</strong> functionality.</span></span><br/> <br/><span data-ttu-id="e7217-126">
<dt><span></span><span></span><strong></strong> Fall</span><span class="sxs-lookup"><span data-stu-id="e7217-126">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="e7217-127"><dt><span></span><span></span><strong></strong> Alarm</span><span class="sxs-lookup"><span data-stu-id="e7217-127"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd> <span data-ttu-id="e7217-128">Standard.</span><span class="sxs-lookup"><span data-stu-id="e7217-128">Default.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e7217-129"><strong>Zeilen</strong></span><span class="sxs-lookup"><span data-stu-id="e7217-129"><strong>Rows</strong></span></span><br/></td>
<td><span data-ttu-id="e7217-130">xs:integer</span><span class="sxs-lookup"><span data-stu-id="e7217-130">xs:integer</span></span><br/></td>
<td><span data-ttu-id="e7217-131">Nein</span><span class="sxs-lookup"><span data-stu-id="e7217-131">No</span></span><br/></td>
<td><span data-ttu-id="e7217-132">Gibt die Anzahl der Element Zeilen an, die ohne Scrollen sichtbar sein sollen.</span><span class="sxs-lookup"><span data-stu-id="e7217-132">Specifies the number of item rows to be visible without scrolling.</span></span> <br/> <br/><span data-ttu-id="e7217-133">
<dt><span></span><span></span><strong></strong> (xs: Integer)</span><span class="sxs-lookup"><span data-stu-id="e7217-133">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="e7217-134">Eine positive oder negative ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="e7217-134">Any positive or negative integer.</span></span> <br/> <span data-ttu-id="e7217-135">Der Standardwert ist <strong>-1</strong> . dieser gibt an, dass so viele Element Zeilen wie möglich angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="e7217-135">The default is <strong>-1</strong> which specifies to display as many item rows as possible.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="e7217-136">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e7217-136">Child elements</span></span>

<span data-ttu-id="e7217-137">Es gibt keine untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="e7217-137">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="e7217-138">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e7217-138">Parent elements</span></span>



| <span data-ttu-id="e7217-139">Element</span><span class="sxs-lookup"><span data-stu-id="e7217-139">Element</span></span>                                                                                                 |
|---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e7217-140">**Dropdowngallery. menulayout**</span><span class="sxs-lookup"><span data-stu-id="e7217-140">**DropDownGallery.MenuLayout**</span></span>](windowsribbon-element-dropdowngallery-menulayout.md)<br/>       |
| [<span data-ttu-id="e7217-141">**Inribbongallery. menulayout**</span><span class="sxs-lookup"><span data-stu-id="e7217-141">**InRibbonGallery.MenuLayout**</span></span>](windowsribbon-element-inribbongallery-menulayout.md)<br/>       |
| [<span data-ttu-id="e7217-142">**Splitbuttongallery. menulayout**</span><span class="sxs-lookup"><span data-stu-id="e7217-142">**SplitButtonGallery.MenuLayout**</span></span>](windowsribbon-element-splitbuttongallery-menulayout.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="e7217-143">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e7217-143">Remarks</span></span>

<span data-ttu-id="e7217-144">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e7217-144">Required.</span></span>

<span data-ttu-id="e7217-145">Entweder das **verticalmenulayout** -oder das [**flowmenulayout**](windowsribbon-element-flowmenulayout.md) -Element muss für jedes [**dropdowngallery. menulayout**](windowsribbon-element-dropdowngallery-menulayout.md)-, [**inribbongallery. menulayout**](windowsribbon-element-inribbongallery-menulayout.md)-oder [**splitbuttongallery. menulayout**](windowsribbon-element-splitbuttongallery-menulayout.md) -Element einmal vorkommen.</span><span class="sxs-lookup"><span data-stu-id="e7217-145">Either the **VerticalMenuLayout** or the [**FlowMenuLayout**](windowsribbon-element-flowmenulayout.md) element must occur one time for each [**DropDownGallery.MenuLayout**](windowsribbon-element-dropdowngallery-menulayout.md), [**InRibbonGallery.MenuLayout**](windowsribbon-element-inribbongallery-menulayout.md), or [**SplitButtonGallery.MenuLayout**](windowsribbon-element-splitbuttongallery-menulayout.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="e7217-146">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e7217-146">Examples</span></span>

<span data-ttu-id="e7217-147">Im folgenden Beispiel wird das grundlegende Markup für ein **verticalmenulayout** -Element veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="e7217-147">The following example demonstrates the basic markup for an **VerticalMenuLayout** element.</span></span>

<span data-ttu-id="e7217-148">In diesem Code Abschnitt werden die Deklarationen des [**inribbongallery**](windowsribbon-element-inribbongallery.md) -Steuer Elements veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="e7217-148">This section of code shows the [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) control declarations.</span></span>


```XML
<!-- InRibbonGallery -->
<Group CommandName="cmdInRibbonGalleryGroup" SizeDefinition="OneInRibbonGallery">
  <InRibbonGallery CommandName="cmdInRibbonGallery"
                   MaxColumns="10"
                   MaxColumnsMedium="5"
                   MinColumnsLarge="5"
                   MinColumnsMedium="3"
                   Type="Items">
    <InRibbonGallery.MenuLayout>
      <VerticalMenuLayout Rows="2"
                          Gripper="Vertical"/>
    </InRibbonGallery.MenuLayout>
    <InRibbonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </InRibbonGallery.MenuGroups>            
  </InRibbonGallery>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="e7217-149">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="e7217-149">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="e7217-150">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="e7217-150">Minimum supported system</span></span><br/> | <span data-ttu-id="e7217-151">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e7217-151">Windows 7</span></span> |
| <span data-ttu-id="e7217-152">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="e7217-152">Can be empty</span></span>                        | <span data-ttu-id="e7217-153">Ja</span><span class="sxs-lookup"><span data-stu-id="e7217-153">Yes</span></span>       |



 

 





