---
title: VerticalMenuLayout-Element
description: Stellt ein vertikales Layout für Elemente in einem Katalog dar.
ms.assetid: 4124c639-c078-4eb0-9d36-37d1ffcebac0
keywords:
- VerticalMenuLayout-Element Windows-Menüband
topic_type:
- apiref
api_name:
- VerticalMenuLayout
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5e6f3e4a691c9691b9bc6c8c6d760bb10635d8d8
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444051"
---
# <a name="verticalmenulayout-element"></a><span data-ttu-id="54724-104">VerticalMenuLayout-Element</span><span class="sxs-lookup"><span data-stu-id="54724-104">VerticalMenuLayout element</span></span>

<span data-ttu-id="54724-105">Stellt ein vertikales Layout für Elemente in einem Katalog dar.</span><span class="sxs-lookup"><span data-stu-id="54724-105">Represents a vertical layout for items in a gallery.</span></span>

## <a name="usage"></a><span data-ttu-id="54724-106">Verwendung</span><span class="sxs-lookup"><span data-stu-id="54724-106">Usage</span></span>

``` syntax
<VerticalMenuLayout
  Rows = "xs:integer"
  IsMultipleHighlightingEnabled = "xs:boolean"
  Gripper = "xs:string"/>
```

## <a name="attributes"></a><span data-ttu-id="54724-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="54724-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="54724-108">attribute</span><span class="sxs-lookup"><span data-stu-id="54724-108">Attribute</span></span></th>
<th><span data-ttu-id="54724-109">Typ</span><span class="sxs-lookup"><span data-stu-id="54724-109">Type</span></span></th>
<th><span data-ttu-id="54724-110">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="54724-110">Required</span></span></th>
<th><span data-ttu-id="54724-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="54724-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="54724-112"><strong>Greifer</strong></span><span class="sxs-lookup"><span data-stu-id="54724-112"><strong>Gripper</strong></span></span><br/></td>
<td><span data-ttu-id="54724-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="54724-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="54724-114">Nein</span><span class="sxs-lookup"><span data-stu-id="54724-114">No</span></span><br/></td>
<td><span data-ttu-id="54724-115">Ein Anfügehandle für die Größenänderung, das an die Dropdown-Dropdown-Datei des Katalogs angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="54724-115">A resizing handle attached to the gallery drop down.</span></span> <br/> <img src="images/controls/gripper.png" alt="Screen shot of a vertical gripper." /><br/> <span data-ttu-id="54724-116">Beschränkt auf einen der folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="54724-116">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="54724-117">
<dt><span></span><span></span><strong></strong> (Keine)</span><span class="sxs-lookup"><span data-stu-id="54724-117">
<dt><span></span><span></span><strong></strong> (None)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="54724-118"><dt><span></span><span></span><strong></strong> (Vertikal)</span><span class="sxs-lookup"><span data-stu-id="54724-118"><dt><span></span><span></span><strong></strong> (Vertical)</span></span><br/> </dt> <dd> <span data-ttu-id="54724-119">Standard.</span><span class="sxs-lookup"><span data-stu-id="54724-119">Default.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="54724-120"><strong>IsMultipleHighlightingEnabled</strong></span><span class="sxs-lookup"><span data-stu-id="54724-120"><strong>IsMultipleHighlightingEnabled</strong></span></span><br/></td>
<td><span data-ttu-id="54724-121">xs:boolean</span><span class="sxs-lookup"><span data-stu-id="54724-121">xs:boolean</span></span><br/></td>
<td><span data-ttu-id="54724-122">Nein</span><span class="sxs-lookup"><span data-stu-id="54724-122">No</span></span><br/></td>
<td><span data-ttu-id="54724-123"><strong>Windows 8 und neuer</strong></span><span class="sxs-lookup"><span data-stu-id="54724-123"><strong>Windows 8 and newer</strong></span></span><br/> <span data-ttu-id="54724-124">Hebt alle Elemente in der Liste bis einschließlich des aktuellen Mauszeigerelements hervor (anstatt nur des Mauszeigerelements).</span><span class="sxs-lookup"><span data-stu-id="54724-124">Highlights all items in the list up to, and including, the current mouseover item (instead of the mouseover item only).</span></span> <span data-ttu-id="54724-125">Wird in der Regel für mehrere <strong>Rückgängig-</strong> und <strong>Wiederholungsfunktionen</strong> verwendet.</span><span class="sxs-lookup"><span data-stu-id="54724-125">Typically used for multiple <strong>Undo</strong> and <strong>Redo</strong> functionality.</span></span><br/> <br/><span data-ttu-id="54724-126">
<dt><span></span><span></span><strong></strong> (true)</span><span class="sxs-lookup"><span data-stu-id="54724-126">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="54724-127"><dt><span></span><span></span><strong></strong> (false)</span><span class="sxs-lookup"><span data-stu-id="54724-127"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd> <span data-ttu-id="54724-128">Standard.</span><span class="sxs-lookup"><span data-stu-id="54724-128">Default.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="54724-129"><strong>Zeilen</strong></span><span class="sxs-lookup"><span data-stu-id="54724-129"><strong>Rows</strong></span></span><br/></td>
<td><span data-ttu-id="54724-130">xs:integer</span><span class="sxs-lookup"><span data-stu-id="54724-130">xs:integer</span></span><br/></td>
<td><span data-ttu-id="54724-131">Nein</span><span class="sxs-lookup"><span data-stu-id="54724-131">No</span></span><br/></td>
<td><span data-ttu-id="54724-132">Gibt die Anzahl der Elementzeilen an, die ohne Bildlauf sichtbar sein sollen.</span><span class="sxs-lookup"><span data-stu-id="54724-132">Specifies the number of item rows to be visible without scrolling.</span></span> <br/> <br/><span data-ttu-id="54724-133">
<dt><span></span><span></span><strong></strong> (xs:integer)</span><span class="sxs-lookup"><span data-stu-id="54724-133">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="54724-134">Eine beliebige positive oder negative ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="54724-134">Any positive or negative integer.</span></span> <br/> <span data-ttu-id="54724-135">Der Standardwert ist <strong>-1,</strong> der angibt, dass so viele Elementzeilen wie möglich angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="54724-135">The default is <strong>-1</strong> which specifies to display as many item rows as possible.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="54724-136">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="54724-136">Child elements</span></span>

<span data-ttu-id="54724-137">Es gibt keine untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="54724-137">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="54724-138">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="54724-138">Parent elements</span></span>



| <span data-ttu-id="54724-139">Element</span><span class="sxs-lookup"><span data-stu-id="54724-139">Element</span></span>                                                                                                 |
|---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="54724-140">**DropDownGallery.MenuLayout**</span><span class="sxs-lookup"><span data-stu-id="54724-140">**DropDownGallery.MenuLayout**</span></span>](windowsribbon-element-dropdowngallery-menulayout.md)<br/>       |
| [<span data-ttu-id="54724-141">**InRibbonGallery.MenuLayout**</span><span class="sxs-lookup"><span data-stu-id="54724-141">**InRibbonGallery.MenuLayout**</span></span>](windowsribbon-element-inribbongallery-menulayout.md)<br/>       |
| [<span data-ttu-id="54724-142">**SplitButtonGallery.MenuLayout**</span><span class="sxs-lookup"><span data-stu-id="54724-142">**SplitButtonGallery.MenuLayout**</span></span>](windowsribbon-element-splitbuttongallery-menulayout.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="54724-143">Hinweise</span><span class="sxs-lookup"><span data-stu-id="54724-143">Remarks</span></span>

<span data-ttu-id="54724-144">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="54724-144">Required.</span></span>

<span data-ttu-id="54724-145">Das **VerticalMenuLayout-Element** oder das [**FlowMenuLayout-Element**](windowsribbon-element-flowmenulayout.md) muss einmal für jedes [**DropDownGallery.MenuLayout-,**](windowsribbon-element-dropdowngallery-menulayout.md) [**InRibbonGallery.MenuLayout-**](windowsribbon-element-inribbongallery-menulayout.md)oder [**SplitButtonGallery.MenuLayout-Element**](windowsribbon-element-splitbuttongallery-menulayout.md) auftreten.</span><span class="sxs-lookup"><span data-stu-id="54724-145">Either the **VerticalMenuLayout** or the [**FlowMenuLayout**](windowsribbon-element-flowmenulayout.md) element must occur one time for each [**DropDownGallery.MenuLayout**](windowsribbon-element-dropdowngallery-menulayout.md), [**InRibbonGallery.MenuLayout**](windowsribbon-element-inribbongallery-menulayout.md), or [**SplitButtonGallery.MenuLayout**](windowsribbon-element-splitbuttongallery-menulayout.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="54724-146">Beispiele</span><span class="sxs-lookup"><span data-stu-id="54724-146">Examples</span></span>

<span data-ttu-id="54724-147">Im folgenden Beispiel wird das grundlegende Markup für ein **VerticalMenuLayout-Element** veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="54724-147">The following example demonstrates the basic markup for an **VerticalMenuLayout** element.</span></span>

<span data-ttu-id="54724-148">Dieser Codeabschnitt zeigt die [**InRibbonGallery-Steuerelementdeklarationen.**](windowsribbon-element-inribbongallery.md)</span><span class="sxs-lookup"><span data-stu-id="54724-148">This section of code shows the [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) control declarations.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="54724-149">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="54724-149">Element information</span></span>


- <span data-ttu-id="54724-150">**Unterstütztes Mindestsystem:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="54724-150">**Minimum supported system**: Windows 7</span></span> 
- <span data-ttu-id="54724-151">**Kann leer sein:** Ja</span><span class="sxs-lookup"><span data-stu-id="54724-151">**Can be empty**: Yes</span></span>



 

 





