---
title: Flowmenulayout-Element
description: Stellt ein horizontales Layout mit Zeilenumbrüchen für Elemente in einem Katalog dar.
ms.assetid: 40c3a2e1-e58a-4d34-a237-b1bea116c82e
keywords:
- Flowmenulayout-Element Windows-Menüband
topic_type:
- apiref
api_name:
- FlowMenuLayout
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8ec9690dd9839755a90abee4c8649c32eae4db6b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106341901"
---
# <a name="flowmenulayout-element"></a><span data-ttu-id="82898-104">Flowmenulayout-Element</span><span class="sxs-lookup"><span data-stu-id="82898-104">FlowMenuLayout element</span></span>

<span data-ttu-id="82898-105">Stellt ein horizontales Layout mit Zeilenumbrüchen für Elemente in einem Katalog dar.</span><span class="sxs-lookup"><span data-stu-id="82898-105">Represents a horizontal layout with line breaks for items in a gallery.</span></span>

## <a name="usage"></a><span data-ttu-id="82898-106">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="82898-106">Usage</span></span>

``` syntax
<FlowMenuLayout
  Rows = "xs:integer"
  Columns = "xs:integer"
  Gripper = "xs:string"/>
```

## <a name="attributes"></a><span data-ttu-id="82898-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="82898-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="82898-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="82898-108">Attribute</span></span></th>
<th><span data-ttu-id="82898-109">type</span><span class="sxs-lookup"><span data-stu-id="82898-109">Type</span></span></th>
<th><span data-ttu-id="82898-110">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="82898-110">Required</span></span></th>
<th><span data-ttu-id="82898-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="82898-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="82898-112"><strong>Spalten</strong></span><span class="sxs-lookup"><span data-stu-id="82898-112"><strong>Columns</strong></span></span><br/></td>
<td><span data-ttu-id="82898-113">xs:integer</span><span class="sxs-lookup"><span data-stu-id="82898-113">xs:integer</span></span><br/></td>
<td><span data-ttu-id="82898-114">Nein</span><span class="sxs-lookup"><span data-stu-id="82898-114">No</span></span><br/></td>
<td><span data-ttu-id="82898-115">Gibt die Anzahl der Elemente an, die in einer einzelnen Zeile angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="82898-115">Specifies the number of items to display in a single row.</span></span><br/> <br/><span data-ttu-id="82898-116">
<dt><span></span><span></span><strong></strong> (xs: Integer)</span><span class="sxs-lookup"><span data-stu-id="82898-116">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="82898-117">Eine positive oder negative ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="82898-117">Any positive or negative integer.</span></span> <br/> <span data-ttu-id="82898-118">Der Standardwert ist <strong>2</strong>.</span><span class="sxs-lookup"><span data-stu-id="82898-118">The default is <strong>2</strong>.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="82898-119"><strong>Zieh Elements</strong></span><span class="sxs-lookup"><span data-stu-id="82898-119"><strong>Gripper</strong></span></span><br/></td>
<td><span data-ttu-id="82898-120">xs:string</span><span class="sxs-lookup"><span data-stu-id="82898-120">xs:string</span></span><br/></td>
<td><span data-ttu-id="82898-121">Nein</span><span class="sxs-lookup"><span data-stu-id="82898-121">No</span></span><br/></td>
<td><span data-ttu-id="82898-122">Ein an den Katalog-Dropdown angefügtes Handle zur Anpassung der Größe.</span><span class="sxs-lookup"><span data-stu-id="82898-122">A resizing handle attached to the gallery drop down.</span></span> <br/> <img src="images/controls/gripper.png" alt="Screen shot of a vertical gripper." /><br/> <span data-ttu-id="82898-123">Beschränkt auf einen der folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="82898-123">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="82898-124">
<dt><span></span><span></span><strong></strong> Gar</span><span class="sxs-lookup"><span data-stu-id="82898-124">
<dt><span></span><span></span><strong></strong> (None)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="82898-125"><dt><span></span><span></span><strong></strong> Rechtes</span><span class="sxs-lookup"><span data-stu-id="82898-125"><dt><span></span><span></span><strong></strong> (Vertical)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="82898-126"><dt><span></span><span></span><strong></strong> Eckpfeiler</span><span class="sxs-lookup"><span data-stu-id="82898-126"><dt><span></span><span></span><strong></strong> (Corner)</span></span><br/> </dt> <dd> <span data-ttu-id="82898-127">Standard.</span><span class="sxs-lookup"><span data-stu-id="82898-127">Default.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="82898-128"><strong>Zeilen</strong></span><span class="sxs-lookup"><span data-stu-id="82898-128"><strong>Rows</strong></span></span><br/></td>
<td><span data-ttu-id="82898-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="82898-129">xs:integer</span></span><br/></td>
<td><span data-ttu-id="82898-130">Nein</span><span class="sxs-lookup"><span data-stu-id="82898-130">No</span></span><br/></td>
<td><span data-ttu-id="82898-131">Gibt die Anzahl der Element Zeilen an, die ohne Scrollen sichtbar sein sollen.</span><span class="sxs-lookup"><span data-stu-id="82898-131">Specifies the number of item rows to be visible without scrolling.</span></span> <br/> <br/><span data-ttu-id="82898-132">
<dt><span></span><span></span><strong></strong> (xs: Integer)</span><span class="sxs-lookup"><span data-stu-id="82898-132">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="82898-133">Eine positive oder negative ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="82898-133">Any positive or negative integer.</span></span> <br/> <span data-ttu-id="82898-134">Der Standardwert ist <strong>-1</strong> . dieser gibt an, dass so viele Element Zeilen wie möglich angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="82898-134">The default is <strong>-1</strong> which specifies to display as many item rows as possible.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="82898-135">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="82898-135">Child elements</span></span>

<span data-ttu-id="82898-136">Es gibt keine untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="82898-136">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="82898-137">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="82898-137">Parent elements</span></span>



| <span data-ttu-id="82898-138">Element</span><span class="sxs-lookup"><span data-stu-id="82898-138">Element</span></span>                                                                                                 |
|---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="82898-139">**Dropdowngallery. menulayout**</span><span class="sxs-lookup"><span data-stu-id="82898-139">**DropDownGallery.MenuLayout**</span></span>](windowsribbon-element-dropdowngallery-menulayout.md)<br/>       |
| [<span data-ttu-id="82898-140">**Inribbongallery. menulayout**</span><span class="sxs-lookup"><span data-stu-id="82898-140">**InRibbonGallery.MenuLayout**</span></span>](windowsribbon-element-inribbongallery-menulayout.md)<br/>       |
| [<span data-ttu-id="82898-141">**Splitbuttongallery. menulayout**</span><span class="sxs-lookup"><span data-stu-id="82898-141">**SplitButtonGallery.MenuLayout**</span></span>](windowsribbon-element-splitbuttongallery-menulayout.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="82898-142">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="82898-142">Remarks</span></span>

<span data-ttu-id="82898-143">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="82898-143">Required.</span></span>

<span data-ttu-id="82898-144">Entweder das [**verticalmenulayout**](windowsribbon-element-verticalmenulayout.md) -oder das **flowmenulayout** -Element muss für jedes [**dropdowngallery. menulayout**](windowsribbon-element-dropdowngallery-menulayout.md)-, [**inribbongallery. menulayout**](windowsribbon-element-inribbongallery-menulayout.md)-oder [**splitbuttongallery. menulayout**](windowsribbon-element-splitbuttongallery-menulayout.md) -Element einmal vorkommen.</span><span class="sxs-lookup"><span data-stu-id="82898-144">Either the [**VerticalMenuLayout**](windowsribbon-element-verticalmenulayout.md) or the **FlowMenuLayout** element must occur one time for each [**DropDownGallery.MenuLayout**](windowsribbon-element-dropdowngallery-menulayout.md), [**InRibbonGallery.MenuLayout**](windowsribbon-element-inribbongallery-menulayout.md), or [**SplitButtonGallery.MenuLayout**](windowsribbon-element-splitbuttongallery-menulayout.md) element.</span></span>

<span data-ttu-id="82898-145">Elemente werden entsprechend den Zeilenumbruch Eigenschaften angeordnet, die *den Zeilen-und* *Spalten* Attributen unterliegen.</span><span class="sxs-lookup"><span data-stu-id="82898-145">Elements are arranged according to the line-break properties inherent to the *row* and *column* attributes.</span></span> <span data-ttu-id="82898-146">Wenn Inhalt die Länge einer einzelnen Zeile überschreitet, unterbricht das Menü Zeilen, umschließt Zeilen und richtet Inhalte entsprechend aus.</span><span class="sxs-lookup"><span data-stu-id="82898-146">When content exceeds the length of a single line, the menu breaks lines, wraps lines, and aligns content appropriately.</span></span>

## <a name="examples"></a><span data-ttu-id="82898-147">Beispiele</span><span class="sxs-lookup"><span data-stu-id="82898-147">Examples</span></span>

<span data-ttu-id="82898-148">Im folgenden Beispiel wird das grundlegende Markup für [**dropdowngallery**](windowsribbon-element-dropdowngallery.md)veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="82898-148">The following example demonstrates the basic markup for the [**DropDownGallery**](windowsribbon-element-dropdowngallery.md).</span></span>

<span data-ttu-id="82898-149">In diesem Code Abschnitt wird die [**dropdowngallery. menulayout**](windowsribbon-element-dropdowngallery-menulayout.md) -Steuerelement Deklaration mit einer **flowmenulayout** -Spezifikation veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="82898-149">This section of code shows the [**DropDownGallery.MenuLayout**](windowsribbon-element-dropdowngallery-menulayout.md) control declaration with a **FlowMenuLayout** specification.</span></span>


```XML
<!-- DropDownGallery -->
<Group CommandName="cmdDropDownGalleryGroup">
  <DropDownGallery CommandName="cmdDropDownGallery"
                   TextPosition="Hide"
                   Type="Commands"
                   ItemHeight="32"
                   ItemWidth="32">
    <DropDownGallery.MenuLayout>
      <FlowMenuLayout Rows="2"
                      Columns="3"
                      Gripper="None"/>
    </DropDownGallery.MenuLayout>
    <DropDownGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
       </MenuGroup>
       <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </DropDownGallery.MenuGroups>
  </DropDownGallery>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="82898-150">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="82898-150">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="82898-151">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="82898-151">Minimum supported system</span></span><br/> | <span data-ttu-id="82898-152">Windows 7</span><span class="sxs-lookup"><span data-stu-id="82898-152">Windows 7</span></span> |
| <span data-ttu-id="82898-153">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="82898-153">Can be empty</span></span>                        | <span data-ttu-id="82898-154">Ja</span><span class="sxs-lookup"><span data-stu-id="82898-154">Yes</span></span>       |



 

 





