---
title: Sizedefinition-Element
description: Stellt eine benutzerdefinierte Layoutvorlage von Menü Band Steuerelementen dar.
ms.assetid: f90bb469-aee2-4bba-9efe-142a39a8c1ae
keywords:
- Fenster "sizedefinition-Element Windows"
topic_type:
- apiref
api_name:
- SizeDefinition
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7bfab87f01700f8f4d36f76cbcbfe3696acfbec2
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2020
ms.locfileid: "106340883"
---
# <a name="sizedefinition-element"></a><span data-ttu-id="59af3-104">Sizedefinition-Element</span><span class="sxs-lookup"><span data-stu-id="59af3-104">SizeDefinition element</span></span>

<span data-ttu-id="59af3-105">Stellt eine benutzerdefinierte Layoutvorlage von Menü Band Steuerelementen dar.</span><span class="sxs-lookup"><span data-stu-id="59af3-105">Represents a custom layout template of Ribbon controls.</span></span>

## <a name="usage"></a><span data-ttu-id="59af3-106">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="59af3-106">Usage</span></span>

``` syntax
<SizeDefinition
  Name = "xs:positiveInteger or xs:string or xs:token">
  child elements
</SizeDefinition>
```

## <a name="attributes"></a><span data-ttu-id="59af3-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="59af3-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="59af3-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="59af3-108">Attribute</span></span></th>
<th><span data-ttu-id="59af3-109">type</span><span class="sxs-lookup"><span data-stu-id="59af3-109">Type</span></span></th>
<th><span data-ttu-id="59af3-110">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="59af3-110">Required</span></span></th>
<th><span data-ttu-id="59af3-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="59af3-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="59af3-112"><strong>Name</strong></span><span class="sxs-lookup"><span data-stu-id="59af3-112"><strong>Name</strong></span></span><br/></td>
<td><span data-ttu-id="59af3-113">xs: positiveInteger oder xs: String oder xs: Token</span><span class="sxs-lookup"><span data-stu-id="59af3-113">xs:positiveInteger or xs:string or xs:token</span></span><br/></td>
<td><span data-ttu-id="59af3-114">Ja</span><span class="sxs-lookup"><span data-stu-id="59af3-114">Yes</span></span><br/></td>
<td><span data-ttu-id="59af3-115">, Wenn <a href="windowsribbon-element-ribbon-sizedefinitions.md"><strong>Menüband. sizedefinitions</strong></a> das übergeordnete Element ist, andernfalls optional.</span><span class="sxs-lookup"><span data-stu-id="59af3-115">When <a href="windowsribbon-element-ribbon-sizedefinitions.md"><strong>Ribbon.SizeDefinitions</strong></a> is the parent, otherwise optional.</span></span><br/> <br/><span data-ttu-id="59af3-116">
<dt><span></span><span></span><strong></strong> (xs: positiveInteger oder xs: String oder xs: Token)</span><span class="sxs-lookup"><span data-stu-id="59af3-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string or xs:token)</span></span><br/> </dt> <dd> <span data-ttu-id="59af3-117">Eine Zeichenfolge oder ein ganzzahliger Wert zwischen 2 und 59999, einschließlich, oder 0x2 und 0xea5f in Hexadezimal (einschließlich).</span><span class="sxs-lookup"><span data-stu-id="59af3-117">A string or an integer value between 2 and 59999, inclusive, or 0x2 and 0xea5f in hexadecimal, inclusive.</span></span> <br/> <span data-ttu-id="59af3-118">Der Wert muss innerhalb des Menüband-XML-Dokuments eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="59af3-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="59af3-119">Maximale Länge: 100 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="59af3-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="59af3-120">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="59af3-120">Child elements</span></span>



| <span data-ttu-id="59af3-121">Element</span><span class="sxs-lookup"><span data-stu-id="59af3-121">Element</span></span>                                                                             | <span data-ttu-id="59af3-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="59af3-122">Description</span></span>                                     |
|-------------------------------------------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="59af3-123">**Controlnamemap**</span><span class="sxs-lookup"><span data-stu-id="59af3-123">**ControlNameMap**</span></span>](windowsribbon-element-controlnamemap.md)<br/>           | <span data-ttu-id="59af3-124">Kann höchstens einmal vorkommen</span><span class="sxs-lookup"><span data-stu-id="59af3-124">May occur at most once</span></span><br/> <br/>   |
| [<span data-ttu-id="59af3-125">**Groupsizedefinition**</span><span class="sxs-lookup"><span data-stu-id="59af3-125">**GroupSizeDefinition**</span></span>](windowsribbon-element-groupsizedefinition.md)<br/> | <span data-ttu-id="59af3-126">Muss mindestens einmal vorkommen</span><span class="sxs-lookup"><span data-stu-id="59af3-126">Must occur at least once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="59af3-127">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="59af3-127">Parent elements</span></span>



| <span data-ttu-id="59af3-128">Element</span><span class="sxs-lookup"><span data-stu-id="59af3-128">Element</span></span>                                                                                   |
|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="59af3-129">**Gruppe**</span><span class="sxs-lookup"><span data-stu-id="59af3-129">**Group**</span></span>](windowsribbon-element-group.md)<br/>                                   |
| [<span data-ttu-id="59af3-130">**Ribbon. sizedefinitions**</span><span class="sxs-lookup"><span data-stu-id="59af3-130">**Ribbon.SizeDefinitions**</span></span>](windowsribbon-element-ribbon-sizedefinitions.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="59af3-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="59af3-131">Remarks</span></span>

<span data-ttu-id="59af3-132">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="59af3-132">Optional.</span></span>

<span data-ttu-id="59af3-133">Kann höchstens einmal für jedes [**Group**](windowsribbon-element-group.md) -Element auftreten.</span><span class="sxs-lookup"><span data-stu-id="59af3-133">May occur at most once for each [**Group**](windowsribbon-element-group.md) element.</span></span>

<span data-ttu-id="59af3-134">Kann für jedes [**Ribbon. sizedefinitions**](windowsribbon-element-ribbon-sizedefinitions.md) -Element einmal oder mehrmals vorkommen.</span><span class="sxs-lookup"><span data-stu-id="59af3-134">May occur one or more times for each [**Ribbon.SizeDefinitions**](windowsribbon-element-ribbon-sizedefinitions.md) element.</span></span>

<span data-ttu-id="59af3-135">Vordefinierte [Layoutvorlagen](windowsribbon-templates.md) für das Menüband-Framework werden mit dem *sizedefinition* -Attribut des [**Group**](windowsribbon-element-group.md) -Elements angegeben.</span><span class="sxs-lookup"><span data-stu-id="59af3-135">Predefined Ribbon framework [layout templates](windowsribbon-templates.md) are specified with the *SizeDefinition* attribute of the [**Group**](windowsribbon-element-group.md) element.</span></span>

<span data-ttu-id="59af3-136">Wenn ein entsprechendes [**scalingpolicy. ideal sizes**](windowsribbon-element-scalingpolicy-idealsizes.md) -Element nicht für jedes [**Group**](windowsribbon-element-group.md) -Element in einem [**Register**](windowsribbon-element-tab.md) Kartenelement deklariert wird, tritt ein Validierungs Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="59af3-136">If a corresponding [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) element is not declared for each [**Group**](windowsribbon-element-group.md) element in a [**Tab**](windowsribbon-element-tab.md) element, a validation error will occur.</span></span>

## <a name="examples"></a><span data-ttu-id="59af3-137">Beispiele</span><span class="sxs-lookup"><span data-stu-id="59af3-137">Examples</span></span>

<span data-ttu-id="59af3-138">Im folgenden Codebeispiel wird eine grundlegende benutzerdefinierte Vorlage veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="59af3-138">The following code example illustrates a basic custom template.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="59af3-139">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="59af3-139">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="59af3-140">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="59af3-140">Minimum supported system</span></span><br/> | <span data-ttu-id="59af3-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="59af3-141">Windows 7</span></span> |
| <span data-ttu-id="59af3-142">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="59af3-142">Can be empty</span></span>                        | <span data-ttu-id="59af3-143">Nein</span><span class="sxs-lookup"><span data-stu-id="59af3-143">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="59af3-144">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="59af3-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59af3-145">Anpassen eines Menübands durch Größen Definitionen und Skalierungs Richtlinien</span><span class="sxs-lookup"><span data-stu-id="59af3-145">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 





