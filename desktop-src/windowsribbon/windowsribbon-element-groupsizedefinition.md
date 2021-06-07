---
title: GroupSizeDefinition-Element
description: Stellt eine Layoutgröße für eine Gruppe von Steuerelementen in einer benutzerdefinierten Vorlage dar.
ms.assetid: c0e20c80-16af-41d5-81e1-0dc32e92e3fa
keywords:
- GroupSizeDefinition-Element im Windows-Menüband
topic_type:
- apiref
api_name:
- GroupSizeDefinition
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 650301a29ace2c6df9316a315d4cdbad448e5573
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443381"
---
# <a name="groupsizedefinition-element"></a><span data-ttu-id="d629e-104">GroupSizeDefinition-Element</span><span class="sxs-lookup"><span data-stu-id="d629e-104">GroupSizeDefinition element</span></span>

<span data-ttu-id="d629e-105">Stellt eine Layoutgröße für eine Gruppe von Steuerelementen in einer benutzerdefinierten Vorlage dar.</span><span class="sxs-lookup"><span data-stu-id="d629e-105">Represents a layout size for a group of controls in a custom template.</span></span>

## <a name="usage"></a><span data-ttu-id="d629e-106">Verwendung</span><span class="sxs-lookup"><span data-stu-id="d629e-106">Usage</span></span>

``` syntax
<GroupSizeDefinition
  Size = "xs:string">
  child elements
</GroupSizeDefinition>
```

## <a name="attributes"></a><span data-ttu-id="d629e-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="d629e-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d629e-108">attribute</span><span class="sxs-lookup"><span data-stu-id="d629e-108">Attribute</span></span></th>
<th><span data-ttu-id="d629e-109">Typ</span><span class="sxs-lookup"><span data-stu-id="d629e-109">Type</span></span></th>
<th><span data-ttu-id="d629e-110">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="d629e-110">Required</span></span></th>
<th><span data-ttu-id="d629e-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d629e-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d629e-112"><strong>Größe</strong></span><span class="sxs-lookup"><span data-stu-id="d629e-112"><strong>Size</strong></span></span><br/></td>
<td><span data-ttu-id="d629e-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="d629e-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="d629e-114">Nein</span><span class="sxs-lookup"><span data-stu-id="d629e-114">No</span></span><br/></td>
<td><span data-ttu-id="d629e-115">Auf einen der folgenden Werte beschränkt:</span><span class="sxs-lookup"><span data-stu-id="d629e-115">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="d629e-116">
<dt><span></span><span></span><strong></strong> (Groß)</span><span class="sxs-lookup"><span data-stu-id="d629e-116">
<dt><span></span><span></span><strong></strong> (Large)</span></span><br/> </dt> <dd> <span data-ttu-id="d629e-117">Standard.</span><span class="sxs-lookup"><span data-stu-id="d629e-117">Default.</span></span> <br/> </dd> <span data-ttu-id="d629e-118"><dt><span></span><span></span><strong></strong> (Mittel)</span><span class="sxs-lookup"><span data-stu-id="d629e-118"><dt><span></span><span></span><strong></strong> (Medium)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="d629e-119"><dt><span></span><span></span><strong></strong> (Klein)</span><span class="sxs-lookup"><span data-stu-id="d629e-119"><dt><span></span><span></span><strong></strong> (Small)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="d629e-120">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d629e-120">Child elements</span></span>



| <span data-ttu-id="d629e-121">Element</span><span class="sxs-lookup"><span data-stu-id="d629e-121">Element</span></span>                                                                                 | <span data-ttu-id="d629e-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d629e-122">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="d629e-123">**ColumnBreak**</span><span class="sxs-lookup"><span data-stu-id="d629e-123">**ColumnBreak**</span></span>](windowsribbon-element-columnbreak.md)<br/>                     | <span data-ttu-id="d629e-124">Kann ein oder mehrere Male auftreten.</span><span class="sxs-lookup"><span data-stu-id="d629e-124">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="d629e-125">**ControlGroup**</span><span class="sxs-lookup"><span data-stu-id="d629e-125">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>                   | <span data-ttu-id="d629e-126">Kann ein oder mehrere Male auftreten.</span><span class="sxs-lookup"><span data-stu-id="d629e-126">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="d629e-127">**ControlSizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="d629e-127">**ControlSizeDefinition**</span></span>](windowsribbon-element-controlsizedefinition.md)<br/> | <span data-ttu-id="d629e-128">Kann ein oder mehrere Male auftreten.</span><span class="sxs-lookup"><span data-stu-id="d629e-128">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="d629e-129">**Zeile**</span><span class="sxs-lookup"><span data-stu-id="d629e-129">**Row**</span></span>](windowsribbon-element-row.md)<br/>                                     | <span data-ttu-id="d629e-130">Kann ein oder mehrere Male auftreten.</span><span class="sxs-lookup"><span data-stu-id="d629e-130">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="d629e-131">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d629e-131">Parent elements</span></span>



| <span data-ttu-id="d629e-132">Element</span><span class="sxs-lookup"><span data-stu-id="d629e-132">Element</span></span>                                                                   |
|---------------------------------------------------------------------------|
| [<span data-ttu-id="d629e-133">**SizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="d629e-133">**SizeDefinition**</span></span>](windowsribbon-element-sizedefinition.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="d629e-134">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d629e-134">Remarks</span></span>

<span data-ttu-id="d629e-135">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="d629e-135">Optional.</span></span>

<span data-ttu-id="d629e-136">Kann bis zu dreimal für jedes [**SizeDefinition-Element**](windowsribbon-element-sizedefinition.md) auftreten (einmal für jede *Größe*).</span><span class="sxs-lookup"><span data-stu-id="d629e-136">May occur up to three times for each [**SizeDefinition**](windowsribbon-element-sizedefinition.md) element (one time for each *Size*).</span></span>

## <a name="examples"></a><span data-ttu-id="d629e-137">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d629e-137">Examples</span></span>

<span data-ttu-id="d629e-138">Das folgende Codebeispiel veranschaulicht eine einfache benutzerdefinierte Vorlage, die die drei Gruppenlayoutgrößen enthält, die beim Erstellen einer benutzerdefinierten Vorlage mit dem **GroupSizeDefinition-Element** definiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="d629e-138">The following code example illustrates a basic custom template that includes the three group layout sizes that must be defined with the **GroupSizeDefinition** element when creating a custom template.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="d629e-139">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="d629e-139">Element information</span></span>

* <span data-ttu-id="d629e-140">**Unterstütztes Mindestsystem:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="d629e-140">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="d629e-141">**Kann leer sein:** Nein</span><span class="sxs-lookup"><span data-stu-id="d629e-141">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="d629e-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d629e-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d629e-143">Anpassen eines Menübands durch Größendefinitionen und Skalierungsrichtlinien</span><span class="sxs-lookup"><span data-stu-id="d629e-143">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 





