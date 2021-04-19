---
title: Row-Element
description: Stellt eine Zeile von Steuerelementen in einer benutzerdefinierten sizedefinition-Layoutvorlage dar.
ms.assetid: c3dac35f-3537-4eb7-b378-501ea88813f5
keywords:
- Windows-Menüband für Zeilen Element
topic_type:
- apiref
api_name:
- Row
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 83a0a5a9e7908cc1c8cff688b3fefc1e8910b6a4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106341271"
---
# <a name="row-element"></a><span data-ttu-id="85013-104">Row-Element</span><span class="sxs-lookup"><span data-stu-id="85013-104">Row element</span></span>

<span data-ttu-id="85013-105">Stellt eine Zeile von Steuerelementen in einer benutzerdefinierten sizedefinition-Layoutvorlage dar.</span><span class="sxs-lookup"><span data-stu-id="85013-105">Represents a row of controls in a custom SizeDefinition layout template.</span></span>

## <a name="usage"></a><span data-ttu-id="85013-106">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="85013-106">Usage</span></span>

``` syntax
<Row>
  child elements
</Row>
```

## <a name="attributes"></a><span data-ttu-id="85013-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="85013-107">Attributes</span></span>

<span data-ttu-id="85013-108">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="85013-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="85013-109">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="85013-109">Child elements</span></span>



| <span data-ttu-id="85013-110">Element</span><span class="sxs-lookup"><span data-stu-id="85013-110">Element</span></span>                                                                                 | <span data-ttu-id="85013-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="85013-111">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="85013-112">**Controlgroup**</span><span class="sxs-lookup"><span data-stu-id="85013-112">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>                   | <span data-ttu-id="85013-113">Kann ein-oder mehrmals vorkommen</span><span class="sxs-lookup"><span data-stu-id="85013-113">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="85013-114">**Controlsizedefinition**</span><span class="sxs-lookup"><span data-stu-id="85013-114">**ControlSizeDefinition**</span></span>](windowsribbon-element-controlsizedefinition.md)<br/> | <span data-ttu-id="85013-115">Kann ein-oder mehrmals vorkommen</span><span class="sxs-lookup"><span data-stu-id="85013-115">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="85013-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="85013-116">Parent elements</span></span>



| <span data-ttu-id="85013-117">Element</span><span class="sxs-lookup"><span data-stu-id="85013-117">Element</span></span>                                                                             |
|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="85013-118">**Groupsizedefinition**</span><span class="sxs-lookup"><span data-stu-id="85013-118">**GroupSizeDefinition**</span></span>](windowsribbon-element-groupsizedefinition.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="85013-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="85013-119">Remarks</span></span>

<span data-ttu-id="85013-120">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="85013-120">Optional.</span></span>

<span data-ttu-id="85013-121">Kann für jedes [**groupsizedefinition**](windowsribbon-element-groupsizedefinition.md) -Element einmal oder mehrmals vorkommen.</span><span class="sxs-lookup"><span data-stu-id="85013-121">May occur one or more times for each [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="85013-122">Beispiele</span><span class="sxs-lookup"><span data-stu-id="85013-122">Examples</span></span>

<span data-ttu-id="85013-123">Im folgenden Codebeispiel wird das grundlegende Markup für eine benutzerdefinierte [**sizedefinition**](windowsribbon-element-sizedefinition.md) -Layoutvorlage mit vier Schaltflächen mit verschiedenen **Zeilen** Elementen veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="85013-123">The following code example demonstrates the basic markup for a custom four-button [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout template with various **Row** elements.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="85013-124">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="85013-124">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="85013-125">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="85013-125">Minimum supported system</span></span><br/> | <span data-ttu-id="85013-126">Windows 7</span><span class="sxs-lookup"><span data-stu-id="85013-126">Windows 7</span></span> |
| <span data-ttu-id="85013-127">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="85013-127">Can be empty</span></span>                        | <span data-ttu-id="85013-128">Nein</span><span class="sxs-lookup"><span data-stu-id="85013-128">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="85013-129">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="85013-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85013-130">Anpassen eines Menübands durch Größen Definitionen und Skalierungs Richtlinien</span><span class="sxs-lookup"><span data-stu-id="85013-130">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 





