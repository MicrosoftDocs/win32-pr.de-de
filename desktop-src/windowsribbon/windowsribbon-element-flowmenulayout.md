---
title: FlowMenuLayout-Element
description: Stellt ein horizontales Layout mit Zeilenumbrüchen für Elemente in einem Katalog dar.
ms.assetid: 40c3a2e1-e58a-4d34-a237-b1bea116c82e
keywords:
- FlowMenuLayout-Element Im Windows-Menüband
topic_type:
- apiref
api_name:
- FlowMenuLayout
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 31a040fb51ad46feb30147fea97c19210cc16094
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111442881"
---
# <a name="flowmenulayout-element"></a><span data-ttu-id="c74d6-104">FlowMenuLayout-Element</span><span class="sxs-lookup"><span data-stu-id="c74d6-104">FlowMenuLayout element</span></span>

<span data-ttu-id="c74d6-105">Stellt ein horizontales Layout mit Zeilenumbrüchen für Elemente in einem Katalog dar.</span><span class="sxs-lookup"><span data-stu-id="c74d6-105">Represents a horizontal layout with line breaks for items in a gallery.</span></span>

## <a name="usage"></a><span data-ttu-id="c74d6-106">Verwendung</span><span class="sxs-lookup"><span data-stu-id="c74d6-106">Usage</span></span>

``` syntax
<FlowMenuLayout
  Rows = "xs:integer"
  Columns = "xs:integer"
  Gripper = "xs:string"/>
```

## <a name="attributes"></a><span data-ttu-id="c74d6-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="c74d6-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c74d6-108">attribute</span><span class="sxs-lookup"><span data-stu-id="c74d6-108">Attribute</span></span></th>
<th><span data-ttu-id="c74d6-109">Typ</span><span class="sxs-lookup"><span data-stu-id="c74d6-109">Type</span></span></th>
<th><span data-ttu-id="c74d6-110">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="c74d6-110">Required</span></span></th>
<th><span data-ttu-id="c74d6-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c74d6-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c74d6-112"><strong>Spalten</strong></span><span class="sxs-lookup"><span data-stu-id="c74d6-112"><strong>Columns</strong></span></span><br/></td>
<td><span data-ttu-id="c74d6-113">xs:integer</span><span class="sxs-lookup"><span data-stu-id="c74d6-113">xs:integer</span></span><br/></td>
<td><span data-ttu-id="c74d6-114">Nein</span><span class="sxs-lookup"><span data-stu-id="c74d6-114">No</span></span><br/></td>
<td><span data-ttu-id="c74d6-115">Gibt die Anzahl der Elemente an, die in einer einzelnen Zeile angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="c74d6-115">Specifies the number of items to display in a single row.</span></span><br/> <br/><span data-ttu-id="c74d6-116">
<dt><span></span><span></span><strong></strong> (xs:integer)</span><span class="sxs-lookup"><span data-stu-id="c74d6-116">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="c74d6-117">Eine positive oder negative ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="c74d6-117">Any positive or negative integer.</span></span> <br/> <span data-ttu-id="c74d6-118">Der Standardwert ist <strong>2.</strong></span><span class="sxs-lookup"><span data-stu-id="c74d6-118">The default is <strong>2</strong>.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c74d6-119"><strong>Greifer</strong></span><span class="sxs-lookup"><span data-stu-id="c74d6-119"><strong>Gripper</strong></span></span><br/></td>
<td><span data-ttu-id="c74d6-120">xs:string</span><span class="sxs-lookup"><span data-stu-id="c74d6-120">xs:string</span></span><br/></td>
<td><span data-ttu-id="c74d6-121">Nein</span><span class="sxs-lookup"><span data-stu-id="c74d6-121">No</span></span><br/></td>
<td><span data-ttu-id="c74d6-122">Ein größenverfingendes Handle, das an die Dropdownliste des Katalogs angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="c74d6-122">A resizing handle attached to the gallery drop down.</span></span> <br/> <img src="images/controls/gripper.png" alt="Screen shot of a vertical gripper." /><br/> <span data-ttu-id="c74d6-123">Auf einen der folgenden Werte beschränkt:</span><span class="sxs-lookup"><span data-stu-id="c74d6-123">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="c74d6-124">
<dt><span></span><span></span><strong></strong> (Keine)</span><span class="sxs-lookup"><span data-stu-id="c74d6-124">
<dt><span></span><span></span><strong></strong> (None)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="c74d6-125"><dt><span></span><span></span><strong></strong> (Vertikal)</span><span class="sxs-lookup"><span data-stu-id="c74d6-125"><dt><span></span><span></span><strong></strong> (Vertical)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="c74d6-126"><dt><span></span><span></span><strong></strong> (Ecke)</span><span class="sxs-lookup"><span data-stu-id="c74d6-126"><dt><span></span><span></span><strong></strong> (Corner)</span></span><br/> </dt> <dd> <span data-ttu-id="c74d6-127">Standard.</span><span class="sxs-lookup"><span data-stu-id="c74d6-127">Default.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c74d6-128"><strong>Zeilen</strong></span><span class="sxs-lookup"><span data-stu-id="c74d6-128"><strong>Rows</strong></span></span><br/></td>
<td><span data-ttu-id="c74d6-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="c74d6-129">xs:integer</span></span><br/></td>
<td><span data-ttu-id="c74d6-130">Nein</span><span class="sxs-lookup"><span data-stu-id="c74d6-130">No</span></span><br/></td>
<td><span data-ttu-id="c74d6-131">Gibt die Anzahl der Elementzeilen an, die ohne Scrollen sichtbar sein sollen.</span><span class="sxs-lookup"><span data-stu-id="c74d6-131">Specifies the number of item rows to be visible without scrolling.</span></span> <br/> <br/><span data-ttu-id="c74d6-132">
<dt><span></span><span></span><strong></strong> (xs:integer)</span><span class="sxs-lookup"><span data-stu-id="c74d6-132">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="c74d6-133">Eine positive oder negative ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="c74d6-133">Any positive or negative integer.</span></span> <br/> <span data-ttu-id="c74d6-134">Der Standardwert ist <strong>-1,</strong> der angibt, dass so viele Elementzeilen wie möglich angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="c74d6-134">The default is <strong>-1</strong> which specifies to display as many item rows as possible.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="c74d6-135">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c74d6-135">Child elements</span></span>

<span data-ttu-id="c74d6-136">Es gibt keine untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="c74d6-136">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="c74d6-137">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c74d6-137">Parent elements</span></span>



| <span data-ttu-id="c74d6-138">Element</span><span class="sxs-lookup"><span data-stu-id="c74d6-138">Element</span></span>                                                                                                 |
|---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c74d6-139">**DropDownGallery.MenuLayout**</span><span class="sxs-lookup"><span data-stu-id="c74d6-139">**DropDownGallery.MenuLayout**</span></span>](windowsribbon-element-dropdowngallery-menulayout.md)<br/>       |
| [<span data-ttu-id="c74d6-140">**InRibbonGallery.MenuLayout**</span><span class="sxs-lookup"><span data-stu-id="c74d6-140">**InRibbonGallery.MenuLayout**</span></span>](windowsribbon-element-inribbongallery-menulayout.md)<br/>       |
| [<span data-ttu-id="c74d6-141">**SplitButtonGallery.MenuLayout**</span><span class="sxs-lookup"><span data-stu-id="c74d6-141">**SplitButtonGallery.MenuLayout**</span></span>](windowsribbon-element-splitbuttongallery-menulayout.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="c74d6-142">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c74d6-142">Remarks</span></span>

<span data-ttu-id="c74d6-143">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c74d6-143">Required.</span></span>

<span data-ttu-id="c74d6-144">Entweder [**das VerticalMenuLayout-**](windowsribbon-element-verticalmenulayout.md) oder **das FlowMenuLayout-Element** muss einmal für jedes [**DropDownGallery.MenuLayout-,**](windowsribbon-element-dropdowngallery-menulayout.md) [**InRibbonGallery.MenuLayout-**](windowsribbon-element-inribbongallery-menulayout.md)oder [**SplitButtonGallery.MenuLayout-Element**](windowsribbon-element-splitbuttongallery-menulayout.md) auftreten.</span><span class="sxs-lookup"><span data-stu-id="c74d6-144">Either the [**VerticalMenuLayout**](windowsribbon-element-verticalmenulayout.md) or the **FlowMenuLayout** element must occur one time for each [**DropDownGallery.MenuLayout**](windowsribbon-element-dropdowngallery-menulayout.md), [**InRibbonGallery.MenuLayout**](windowsribbon-element-inribbongallery-menulayout.md), or [**SplitButtonGallery.MenuLayout**](windowsribbon-element-splitbuttongallery-menulayout.md) element.</span></span>

<span data-ttu-id="c74d6-145">Elemente werden entsprechend den Zeilenumbrucheigenschaften angeordnet, die den Zeilen- *und* *Spaltenattributen inhärent* sind.</span><span class="sxs-lookup"><span data-stu-id="c74d6-145">Elements are arranged according to the line-break properties inherent to the *row* and *column* attributes.</span></span> <span data-ttu-id="c74d6-146">Wenn inhalt die Länge einer einzelnen Zeile überschreitet, unterbricht das Menü Zeilen, umbricht Zeilen und richtet den Inhalt entsprechend aus.</span><span class="sxs-lookup"><span data-stu-id="c74d6-146">When content exceeds the length of a single line, the menu breaks lines, wraps lines, and aligns content appropriately.</span></span>

## <a name="examples"></a><span data-ttu-id="c74d6-147">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c74d6-147">Examples</span></span>

<span data-ttu-id="c74d6-148">Im folgenden Beispiel wird das grundlegende Markup für [**die DropDownGallery veranschaulicht.**](windowsribbon-element-dropdowngallery.md)</span><span class="sxs-lookup"><span data-stu-id="c74d6-148">The following example demonstrates the basic markup for the [**DropDownGallery**](windowsribbon-element-dropdowngallery.md).</span></span>

<span data-ttu-id="c74d6-149">Dieser Codeabschnitt zeigt die [**DropDownGallery.MenuLayout-Steuerelementdeklaration**](windowsribbon-element-dropdowngallery-menulayout.md) mit einer **FlowMenuLayout-Spezifikation.**</span><span class="sxs-lookup"><span data-stu-id="c74d6-149">This section of code shows the [**DropDownGallery.MenuLayout**](windowsribbon-element-dropdowngallery-menulayout.md) control declaration with a **FlowMenuLayout** specification.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="c74d6-150">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="c74d6-150">Element information</span></span>

* <span data-ttu-id="c74d6-151">**Unterstütztes Mindestsystem:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="c74d6-151">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="c74d6-152">**Kann leer sein:** Ja</span><span class="sxs-lookup"><span data-stu-id="c74d6-152">**Can be empty**: Yes</span></span>


 

 





