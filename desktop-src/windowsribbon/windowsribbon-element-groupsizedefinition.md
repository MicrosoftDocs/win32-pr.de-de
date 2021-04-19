---
title: Groupsizedefinition-Element
description: Stellt eine Layoutgröße für eine Gruppe von Steuerelementen in einer benutzerdefinierten Vorlage dar.
ms.assetid: c0e20c80-16af-41d5-81e1-0dc32e92e3fa
keywords:
- Groupsizedefinition-Element Windows-Menüband
topic_type:
- apiref
api_name:
- GroupSizeDefinition
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5cf166dbf428c9d17beb148887cc94be73dc11a0
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106339461"
---
# <a name="groupsizedefinition-element"></a><span data-ttu-id="55c51-104">Groupsizedefinition-Element</span><span class="sxs-lookup"><span data-stu-id="55c51-104">GroupSizeDefinition element</span></span>

<span data-ttu-id="55c51-105">Stellt eine Layoutgröße für eine Gruppe von Steuerelementen in einer benutzerdefinierten Vorlage dar.</span><span class="sxs-lookup"><span data-stu-id="55c51-105">Represents a layout size for a group of controls in a custom template.</span></span>

## <a name="usage"></a><span data-ttu-id="55c51-106">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="55c51-106">Usage</span></span>

``` syntax
<GroupSizeDefinition
  Size = "xs:string">
  child elements
</GroupSizeDefinition>
```

## <a name="attributes"></a><span data-ttu-id="55c51-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="55c51-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="55c51-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="55c51-108">Attribute</span></span></th>
<th><span data-ttu-id="55c51-109">type</span><span class="sxs-lookup"><span data-stu-id="55c51-109">Type</span></span></th>
<th><span data-ttu-id="55c51-110">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="55c51-110">Required</span></span></th>
<th><span data-ttu-id="55c51-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="55c51-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="55c51-112"><strong>Größe</strong></span><span class="sxs-lookup"><span data-stu-id="55c51-112"><strong>Size</strong></span></span><br/></td>
<td><span data-ttu-id="55c51-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="55c51-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="55c51-114">Nein</span><span class="sxs-lookup"><span data-stu-id="55c51-114">No</span></span><br/></td>
<td><span data-ttu-id="55c51-115">Beschränkt auf einen der folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="55c51-115">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="55c51-116">
<dt><span></span><span></span><strong></strong> Viele</span><span class="sxs-lookup"><span data-stu-id="55c51-116">
<dt><span></span><span></span><strong></strong> (Large)</span></span><br/> </dt> <dd> <span data-ttu-id="55c51-117">Standard.</span><span class="sxs-lookup"><span data-stu-id="55c51-117">Default.</span></span> <br/> </dd> <span data-ttu-id="55c51-118"><dt><span></span><span></span><strong></strong> Mittelalter</span><span class="sxs-lookup"><span data-stu-id="55c51-118"><dt><span></span><span></span><strong></strong> (Medium)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="55c51-119"><dt><span></span><span></span><strong></strong> Zuletzt</span><span class="sxs-lookup"><span data-stu-id="55c51-119"><dt><span></span><span></span><strong></strong> (Small)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="55c51-120">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="55c51-120">Child elements</span></span>



| <span data-ttu-id="55c51-121">Element</span><span class="sxs-lookup"><span data-stu-id="55c51-121">Element</span></span>                                                                                 | <span data-ttu-id="55c51-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="55c51-122">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="55c51-123">**Columnbreak**</span><span class="sxs-lookup"><span data-stu-id="55c51-123">**ColumnBreak**</span></span>](windowsribbon-element-columnbreak.md)<br/>                     | <span data-ttu-id="55c51-124">Kann ein-oder mehrmals vorkommen</span><span class="sxs-lookup"><span data-stu-id="55c51-124">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="55c51-125">**Controlgroup**</span><span class="sxs-lookup"><span data-stu-id="55c51-125">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>                   | <span data-ttu-id="55c51-126">Kann ein-oder mehrmals vorkommen</span><span class="sxs-lookup"><span data-stu-id="55c51-126">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="55c51-127">**Controlsizedefinition**</span><span class="sxs-lookup"><span data-stu-id="55c51-127">**ControlSizeDefinition**</span></span>](windowsribbon-element-controlsizedefinition.md)<br/> | <span data-ttu-id="55c51-128">Kann ein-oder mehrmals vorkommen</span><span class="sxs-lookup"><span data-stu-id="55c51-128">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="55c51-129">**Zeile**</span><span class="sxs-lookup"><span data-stu-id="55c51-129">**Row**</span></span>](windowsribbon-element-row.md)<br/>                                     | <span data-ttu-id="55c51-130">Kann ein-oder mehrmals vorkommen</span><span class="sxs-lookup"><span data-stu-id="55c51-130">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="55c51-131">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="55c51-131">Parent elements</span></span>



| <span data-ttu-id="55c51-132">Element</span><span class="sxs-lookup"><span data-stu-id="55c51-132">Element</span></span>                                                                   |
|---------------------------------------------------------------------------|
| [<span data-ttu-id="55c51-133">**Sizedefinition**</span><span class="sxs-lookup"><span data-stu-id="55c51-133">**SizeDefinition**</span></span>](windowsribbon-element-sizedefinition.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="55c51-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="55c51-134">Remarks</span></span>

<span data-ttu-id="55c51-135">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="55c51-135">Optional.</span></span>

<span data-ttu-id="55c51-136">Kann für jedes [**sizedefinition**](windowsribbon-element-sizedefinition.md) -Element (einmal pro *Größe*) bis zu drei mal vorkommen.</span><span class="sxs-lookup"><span data-stu-id="55c51-136">May occur up to three times for each [**SizeDefinition**](windowsribbon-element-sizedefinition.md) element (one time for each *Size*).</span></span>

## <a name="examples"></a><span data-ttu-id="55c51-137">Beispiele</span><span class="sxs-lookup"><span data-stu-id="55c51-137">Examples</span></span>

<span data-ttu-id="55c51-138">Im folgenden Codebeispiel wird eine grundlegende benutzerdefinierte Vorlage veranschaulicht, die die drei Gruppen layoutgrößen enthält, die beim Erstellen einer benutzerdefinierten Vorlage mit dem **groupsizedefinition** -Element definiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="55c51-138">The following code example illustrates a basic custom template that includes the three group layout sizes that must be defined with the **GroupSizeDefinition** element when creating a custom template.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="55c51-139">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="55c51-139">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="55c51-140">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="55c51-140">Minimum supported system</span></span><br/> | <span data-ttu-id="55c51-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="55c51-141">Windows 7</span></span> |
| <span data-ttu-id="55c51-142">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="55c51-142">Can be empty</span></span>                        | <span data-ttu-id="55c51-143">Nein</span><span class="sxs-lookup"><span data-stu-id="55c51-143">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="55c51-144">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="55c51-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55c51-145">Anpassen eines Menübands durch Größen Definitionen und Skalierungs Richtlinien</span><span class="sxs-lookup"><span data-stu-id="55c51-145">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 





