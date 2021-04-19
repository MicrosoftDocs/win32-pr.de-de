---
title: Columnbreak-Element
description: Stellt ein vertikales Trennzeichen (sichtbar oder ausgeblendet) in benutzerdefinierten sizedefinition-Layoutvorlagen dar.
ms.assetid: 5979d3e6-366b-4c47-810f-90fb8039af8d
keywords:
- Windows-Menüband für columnbreak-Element
topic_type:
- apiref
api_name:
- ColumnBreak
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 00257783c0c8a7919251004a4b1996ab4d994c3c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106342099"
---
# <a name="columnbreak-element"></a><span data-ttu-id="91d90-104">Columnbreak-Element</span><span class="sxs-lookup"><span data-stu-id="91d90-104">ColumnBreak element</span></span>

<span data-ttu-id="91d90-105">Stellt ein vertikales Trennzeichen (sichtbar oder ausgeblendet) in benutzerdefinierten [**sizedefinition**](windowsribbon-element-sizedefinition.md) -Layoutvorlagen dar.</span><span class="sxs-lookup"><span data-stu-id="91d90-105">Represents a vertical separator (visible or hidden) in custom [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout templates.</span></span>

## <a name="usage"></a><span data-ttu-id="91d90-106">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="91d90-106">Usage</span></span>

``` syntax
<ColumnBreak
  ShowSeparator = "Boolean"/>
```

## <a name="attributes"></a><span data-ttu-id="91d90-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="91d90-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="91d90-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="91d90-108">Attribute</span></span></th>
<th><span data-ttu-id="91d90-109">type</span><span class="sxs-lookup"><span data-stu-id="91d90-109">Type</span></span></th>
<th><span data-ttu-id="91d90-110">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="91d90-110">Required</span></span></th>
<th><span data-ttu-id="91d90-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="91d90-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="91d90-112"><strong>Showseparator</strong></span><span class="sxs-lookup"><span data-stu-id="91d90-112"><strong>ShowSeparator</strong></span></span><br/></td>
<td><span data-ttu-id="91d90-113">Boolesch</span><span class="sxs-lookup"><span data-stu-id="91d90-113">Boolean</span></span><br/></td>
<td><span data-ttu-id="91d90-114">Nein</span><span class="sxs-lookup"><span data-stu-id="91d90-114">No</span></span><br/></td>
<td><span data-ttu-id="91d90-115">Beschränkt auf einen der folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="91d90-115">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="91d90-116">
<dt><span></span><span></span><strong></strong> Fall</span><span class="sxs-lookup"><span data-stu-id="91d90-116">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="91d90-117">Standard.</span><span class="sxs-lookup"><span data-stu-id="91d90-117">Default.</span></span> <br/> </dd> <span data-ttu-id="91d90-118"><dt><span></span><span></span><strong></strong> Alarm</span><span class="sxs-lookup"><span data-stu-id="91d90-118"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="91d90-119">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="91d90-119">Child elements</span></span>

<span data-ttu-id="91d90-120">Es gibt keine untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="91d90-120">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="91d90-121">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="91d90-121">Parent elements</span></span>



| <span data-ttu-id="91d90-122">Element</span><span class="sxs-lookup"><span data-stu-id="91d90-122">Element</span></span>                                                                             |
|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="91d90-123">**Groupsizedefinition**</span><span class="sxs-lookup"><span data-stu-id="91d90-123">**GroupSizeDefinition**</span></span>](windowsribbon-element-groupsizedefinition.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="91d90-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="91d90-124">Remarks</span></span>

<span data-ttu-id="91d90-125">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="91d90-125">Optional.</span></span>

<span data-ttu-id="91d90-126">Kann für jedes [**groupsizedefinition**](windowsribbon-element-groupsizedefinition.md) -Element einmal oder mehrmals vorkommen.</span><span class="sxs-lookup"><span data-stu-id="91d90-126">May occur one or more times for each [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="91d90-127">Beispiele</span><span class="sxs-lookup"><span data-stu-id="91d90-127">Examples</span></span>

<span data-ttu-id="91d90-128">Im folgenden Beispiel wird das grundlegende Markup für ein **columnbreak** -Element in einer benutzerdefinierten [**sizedefinition**](windowsribbon-element-sizedefinition.md) -Layoutvorlage mit vier Schaltflächen veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="91d90-128">The following example demonstrates the basic markup for a **ColumnBreak** element in a custom four-button [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout template.</span></span> <span data-ttu-id="91d90-129">Der **columnbreak** -Wert wird nur für die `Large` Vorlage angegeben.</span><span class="sxs-lookup"><span data-stu-id="91d90-129">The **ColumnBreak** is only specified for the `Large` template.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="91d90-130">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="91d90-130">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="91d90-131">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="91d90-131">Minimum supported system</span></span><br/> | <span data-ttu-id="91d90-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="91d90-132">Windows 7</span></span> |
| <span data-ttu-id="91d90-133">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="91d90-133">Can be empty</span></span>                        | <span data-ttu-id="91d90-134">Ja</span><span class="sxs-lookup"><span data-stu-id="91d90-134">Yes</span></span>       |



## <a name="see-also"></a><span data-ttu-id="91d90-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="91d90-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91d90-136">Anpassen eines Menübands durch Größen Definitionen und Skalierungs Richtlinien</span><span class="sxs-lookup"><span data-stu-id="91d90-136">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 





