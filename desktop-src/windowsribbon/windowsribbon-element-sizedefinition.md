---
title: SizeDefinition-Element
description: Stellt eine benutzerdefinierte Layoutvorlage von Menüband-Steuerelementen dar.
ms.assetid: f90bb469-aee2-4bba-9efe-142a39a8c1ae
keywords:
- SizeDefinition-Element Windows-Menüband
topic_type:
- apiref
api_name:
- SizeDefinition
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cc68ac032459bed77d402ebd860886398748c874
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444801"
---
# <a name="sizedefinition-element"></a><span data-ttu-id="2924c-104">SizeDefinition-Element</span><span class="sxs-lookup"><span data-stu-id="2924c-104">SizeDefinition element</span></span>

<span data-ttu-id="2924c-105">Stellt eine benutzerdefinierte Layoutvorlage von Menüband-Steuerelementen dar.</span><span class="sxs-lookup"><span data-stu-id="2924c-105">Represents a custom layout template of Ribbon controls.</span></span>

## <a name="usage"></a><span data-ttu-id="2924c-106">Verwendung</span><span class="sxs-lookup"><span data-stu-id="2924c-106">Usage</span></span>

``` syntax
<SizeDefinition
  Name = "xs:positiveInteger or xs:string or xs:token">
  child elements
</SizeDefinition>
```

## <a name="attributes"></a><span data-ttu-id="2924c-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="2924c-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2924c-108">attribute</span><span class="sxs-lookup"><span data-stu-id="2924c-108">Attribute</span></span></th>
<th><span data-ttu-id="2924c-109">Typ</span><span class="sxs-lookup"><span data-stu-id="2924c-109">Type</span></span></th>
<th><span data-ttu-id="2924c-110">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="2924c-110">Required</span></span></th>
<th><span data-ttu-id="2924c-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2924c-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2924c-112"><strong>Name</strong></span><span class="sxs-lookup"><span data-stu-id="2924c-112"><strong>Name</strong></span></span><br/></td>
<td><span data-ttu-id="2924c-113">xs:positiveInteger oder xs:string oder xs:token</span><span class="sxs-lookup"><span data-stu-id="2924c-113">xs:positiveInteger or xs:string or xs:token</span></span><br/></td>
<td><span data-ttu-id="2924c-114">Ja</span><span class="sxs-lookup"><span data-stu-id="2924c-114">Yes</span></span><br/></td>
<td><span data-ttu-id="2924c-115">Wenn <a href="windowsribbon-element-ribbon-sizedefinitions.md"><strong>Ribbon.SizeDefinitions</strong></a> das übergeordnete Element ist, andernfalls optional.</span><span class="sxs-lookup"><span data-stu-id="2924c-115">When <a href="windowsribbon-element-ribbon-sizedefinitions.md"><strong>Ribbon.SizeDefinitions</strong></a> is the parent, otherwise optional.</span></span><br/> <br/><span data-ttu-id="2924c-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger oder xs:string oder xs:token)</span><span class="sxs-lookup"><span data-stu-id="2924c-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string or xs:token)</span></span><br/> </dt> <dd> <span data-ttu-id="2924c-117">Eine Zeichenfolge oder ein ganzzahliger Wert zwischen 2 und 59999, einschließlich oder 0x2 und 0xea5f hexadezimal, einschließlich.</span><span class="sxs-lookup"><span data-stu-id="2924c-117">A string or an integer value between 2 and 59999, inclusive, or 0x2 and 0xea5f in hexadecimal, inclusive.</span></span> <br/> <span data-ttu-id="2924c-118">Der Wert muss innerhalb des Menüband-XML-Dokuments eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="2924c-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="2924c-119">Maximale Länge: 100 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="2924c-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="2924c-120">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2924c-120">Child elements</span></span>



| <span data-ttu-id="2924c-121">Element</span><span class="sxs-lookup"><span data-stu-id="2924c-121">Element</span></span>                                                                             | <span data-ttu-id="2924c-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2924c-122">Description</span></span>                                     |
|-------------------------------------------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="2924c-123">**ControlNameMap**</span><span class="sxs-lookup"><span data-stu-id="2924c-123">**ControlNameMap**</span></span>](windowsribbon-element-controlnamemap.md)<br/>           | <span data-ttu-id="2924c-124">Kann höchstens einmal auftreten.</span><span class="sxs-lookup"><span data-stu-id="2924c-124">May occur at most once</span></span><br/> <br/>   |
| [<span data-ttu-id="2924c-125">**GroupSizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="2924c-125">**GroupSizeDefinition**</span></span>](windowsribbon-element-groupsizedefinition.md)<br/> | <span data-ttu-id="2924c-126">Muss mindestens einmal auftreten</span><span class="sxs-lookup"><span data-stu-id="2924c-126">Must occur at least once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="2924c-127">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2924c-127">Parent elements</span></span>



| <span data-ttu-id="2924c-128">Element</span><span class="sxs-lookup"><span data-stu-id="2924c-128">Element</span></span>                                                                                   |
|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2924c-129">**Gruppe**</span><span class="sxs-lookup"><span data-stu-id="2924c-129">**Group**</span></span>](windowsribbon-element-group.md)<br/>                                   |
| [<span data-ttu-id="2924c-130">**Ribbon.SizeDefinitions**</span><span class="sxs-lookup"><span data-stu-id="2924c-130">**Ribbon.SizeDefinitions**</span></span>](windowsribbon-element-ribbon-sizedefinitions.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="2924c-131">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2924c-131">Remarks</span></span>

<span data-ttu-id="2924c-132">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="2924c-132">Optional.</span></span>

<span data-ttu-id="2924c-133">Kann höchstens einmal für jedes [**Group-Element**](windowsribbon-element-group.md) auftreten.</span><span class="sxs-lookup"><span data-stu-id="2924c-133">May occur at most once for each [**Group**](windowsribbon-element-group.md) element.</span></span>

<span data-ttu-id="2924c-134">Kann ein oder mehrere Male für jedes [**Ribbon.SizeDefinitions-Element**](windowsribbon-element-ribbon-sizedefinitions.md) auftreten.</span><span class="sxs-lookup"><span data-stu-id="2924c-134">May occur one or more times for each [**Ribbon.SizeDefinitions**](windowsribbon-element-ribbon-sizedefinitions.md) element.</span></span>

<span data-ttu-id="2924c-135">Vordefinierte [Menüband-Frameworklayoutvorlagen](windowsribbon-templates.md) werden mit dem *SizeDefinition-Attribut* des [**Group-Elements**](windowsribbon-element-group.md) angegeben.</span><span class="sxs-lookup"><span data-stu-id="2924c-135">Predefined Ribbon framework [layout templates](windowsribbon-templates.md) are specified with the *SizeDefinition* attribute of the [**Group**](windowsribbon-element-group.md) element.</span></span>

<span data-ttu-id="2924c-136">Wenn ein [**entsprechendes ScalingPolicy.IdealSizes-Element**](windowsribbon-element-scalingpolicy-idealsizes.md) nicht für jedes [**Group-Element**](windowsribbon-element-group.md) in einem [**Tab-Element**](windowsribbon-element-tab.md) deklariert wird, tritt ein Validierungsfehler auf.</span><span class="sxs-lookup"><span data-stu-id="2924c-136">If a corresponding [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) element is not declared for each [**Group**](windowsribbon-element-group.md) element in a [**Tab**](windowsribbon-element-tab.md) element, a validation error will occur.</span></span>

## <a name="examples"></a><span data-ttu-id="2924c-137">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2924c-137">Examples</span></span>

<span data-ttu-id="2924c-138">Das folgende Codebeispiel veranschaulicht eine einfache benutzerdefinierte Vorlage.</span><span class="sxs-lookup"><span data-stu-id="2924c-138">The following code example illustrates a basic custom template.</span></span>


```XML
<Group CommandName="cmdButtonGroup2">
  <SizeDefinition>
    <ControlNameMap>
      <ControlNameDefinition Name="button1"/>
      <ControlNameDefinition Name="button2"/>
      <ControlNameDefinition Name="button3"/>
      <ControlNameDefinition Name="button4"/>
    </ControlNameMap>
    <GroupSizeDefinition Size="Large">
      <ControlGroup>
        <ControlSizeDefinition ControlName="button1"
                               ImageSize="Large"
                               IsLabelVisible="true" />
        <ControlSizeDefinition ControlName="button2"
                               ImageSize="Large"
                               IsLabelVisible="true" />
      </ControlGroup>
      <ColumnBreak ShowSeparator="true"/>
      <ControlGroup>
        <ControlSizeDefinition ControlName="button3"
                               ImageSize="Large"
                              IsLabelVisible="true" />
        <ControlSizeDefinition ControlName="button4"
                              ImageSize="Large"
                              IsLabelVisible="true" />
      </ControlGroup>
    </GroupSizeDefinition>
    <GroupSizeDefinition Size="Medium">
      <Row>
        <ControlSizeDefinition ControlName="button1"
                               ImageSize="Small"
                               IsLabelVisible="true" />
        <ControlSizeDefinition ControlName="button3"
                               ImageSize="Small"
                               IsLabelVisible="true" />
      </Row>
      <Row>
        <ControlSizeDefinition ControlName="button2"
                               ImageSize="Small"
                               IsLabelVisible="true" />
        <ControlSizeDefinition ControlName="button4"
                               ImageSize="Small"
                               IsLabelVisible="true" />
      </Row>
    </GroupSizeDefinition>
    <GroupSizeDefinition Size="Small">
      <Row>
        <ControlSizeDefinition ControlName="button1"
                               ImageSize="Small"
                               IsLabelVisible="true" />
        <ControlSizeDefinition ControlName="button3"
                               ImageSize="Small"
                               IsLabelVisible="false" />
      </Row>
      <Row>
        <ControlSizeDefinition ControlName="button2"
                               ImageSize="Small"
                               IsLabelVisible="true" />
        <ControlSizeDefinition ControlName="button4"
                               ImageSize="Small"
                               IsLabelVisible="false" />
      </Row>
    </GroupSizeDefinition>
  </SizeDefinition>
  <Button CommandName="cmdButtonG21"></Button>
  <Button CommandName="cmdButtonG22"></Button>
  <Button CommandName="cmdButtonG23"></Button>
  <Button CommandName="cmdButtonG24"></Button>
</Group>
<Group CommandName="cmdCheckBoxGroup">
  <CheckBox CommandName="cmdCheckBox"></CheckBox>
</Group>
<Group CommandName="cmdToggleButtonGroup"
       SizeDefinition="OneButton">
  <ToggleButton CommandName="cmdToggleButton"></ToggleButton>
</Group>
<Group CommandName="cmdButtonGroup"
       SizeDefinition="ThreeButtons">
  <Button CommandName="cmdButton1"></Button>
  <Button CommandName="cmdButton2"></Button>
  <Button CommandName="cmdButton3"></Button>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="2924c-139">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="2924c-139">Element information</span></span>


- <span data-ttu-id="2924c-140">**Unterstütztes Mindestsystem:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="2924c-140">**Minimum supported system**: Windows 7</span></span> 
- <span data-ttu-id="2924c-141">**Kann leer sein:** Nein</span><span class="sxs-lookup"><span data-stu-id="2924c-141">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="2924c-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2924c-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2924c-143">Anpassen eines Menübands durch Größendefinitionen und Skalierungsrichtlinien</span><span class="sxs-lookup"><span data-stu-id="2924c-143">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 





