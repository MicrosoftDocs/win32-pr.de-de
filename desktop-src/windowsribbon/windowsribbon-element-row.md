---
title: Row-Element
description: Stellt eine Zeile von Steuerelementen in einer benutzerdefinierten SizeDefinition-Layoutvorlage dar.
ms.assetid: c3dac35f-3537-4eb7-b378-501ea88813f5
keywords:
- Zeilenelement Im Windows-Menüband
topic_type:
- apiref
api_name:
- Row
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7d642cd209b3e00e2c63f7376e321132a1c0e686
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111445021"
---
# <a name="row-element"></a><span data-ttu-id="dbcf1-104">Row-Element</span><span class="sxs-lookup"><span data-stu-id="dbcf1-104">Row element</span></span>

<span data-ttu-id="dbcf1-105">Stellt eine Zeile von Steuerelementen in einer benutzerdefinierten SizeDefinition-Layoutvorlage dar.</span><span class="sxs-lookup"><span data-stu-id="dbcf1-105">Represents a row of controls in a custom SizeDefinition layout template.</span></span>

## <a name="usage"></a><span data-ttu-id="dbcf1-106">Verwendung</span><span class="sxs-lookup"><span data-stu-id="dbcf1-106">Usage</span></span>

``` syntax
<Row>
  child elements
</Row>
```

## <a name="attributes"></a><span data-ttu-id="dbcf1-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="dbcf1-107">Attributes</span></span>

<span data-ttu-id="dbcf1-108">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="dbcf1-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="dbcf1-109">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="dbcf1-109">Child elements</span></span>



| <span data-ttu-id="dbcf1-110">Element</span><span class="sxs-lookup"><span data-stu-id="dbcf1-110">Element</span></span>                                                                                 | <span data-ttu-id="dbcf1-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dbcf1-111">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="dbcf1-112">**ControlGroup**</span><span class="sxs-lookup"><span data-stu-id="dbcf1-112">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>                   | <span data-ttu-id="dbcf1-113">Kann ein oder mehrere Male auftreten.</span><span class="sxs-lookup"><span data-stu-id="dbcf1-113">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="dbcf1-114">**ControlSizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="dbcf1-114">**ControlSizeDefinition**</span></span>](windowsribbon-element-controlsizedefinition.md)<br/> | <span data-ttu-id="dbcf1-115">Kann ein oder mehrere Male auftreten.</span><span class="sxs-lookup"><span data-stu-id="dbcf1-115">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="dbcf1-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="dbcf1-116">Parent elements</span></span>



| <span data-ttu-id="dbcf1-117">Element</span><span class="sxs-lookup"><span data-stu-id="dbcf1-117">Element</span></span>                                                                             |
|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="dbcf1-118">**GroupSizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="dbcf1-118">**GroupSizeDefinition**</span></span>](windowsribbon-element-groupsizedefinition.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="dbcf1-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="dbcf1-119">Remarks</span></span>

<span data-ttu-id="dbcf1-120">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="dbcf1-120">Optional.</span></span>

<span data-ttu-id="dbcf1-121">Kann ein oder mehrere Male für jedes [**GroupSizeDefinition-Element**](windowsribbon-element-groupsizedefinition.md) auftreten.</span><span class="sxs-lookup"><span data-stu-id="dbcf1-121">May occur one or more times for each [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="dbcf1-122">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dbcf1-122">Examples</span></span>

<span data-ttu-id="dbcf1-123">Im folgenden Codebeispiel wird das grundlegende Markup für eine benutzerdefinierte [**SizeDefinition-Layoutvorlage**](windowsribbon-element-sizedefinition.md) mit vier Schaltflächen mit verschiedenen **Row-Elementen** veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="dbcf1-123">The following code example demonstrates the basic markup for a custom four-button [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout template with various **Row** elements.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="dbcf1-124">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="dbcf1-124">Element information</span></span>




* <span data-ttu-id="dbcf1-125">**Unterstütztes Mindestsystem:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="dbcf1-125">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="dbcf1-126">**Kann leer sein:** Nein</span><span class="sxs-lookup"><span data-stu-id="dbcf1-126">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="dbcf1-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dbcf1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbcf1-128">Anpassen eines Menübands durch Größendefinitionen und Skalierungsrichtlinien</span><span class="sxs-lookup"><span data-stu-id="dbcf1-128">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 





