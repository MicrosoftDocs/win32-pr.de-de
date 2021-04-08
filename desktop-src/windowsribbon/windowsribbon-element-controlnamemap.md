---
title: Controlnamemap-Element
description: Stellt einen Container für Steuerelement Namen in einer benutzerdefinierten sizedefinition-Layoutvorlage dar.
ms.assetid: b4bceb90-a9a3-42d7-a85b-bf6e4e02784b
keywords:
- Controlnamemap-Element Windows-Menüband
topic_type:
- apiref
api_name:
- ControlNameMap
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7ca5338978be7f9ddf3432cbe1a0fb8d243d8c00
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103857419"
---
# <a name="controlnamemap-element"></a><span data-ttu-id="62cf9-104">Controlnamemap-Element</span><span class="sxs-lookup"><span data-stu-id="62cf9-104">ControlNameMap element</span></span>

<span data-ttu-id="62cf9-105">Stellt einen Container für Steuerelement Namen in einer benutzerdefinierten [**sizedefinition**](windowsribbon-element-sizedefinition.md) -Layoutvorlage dar.</span><span class="sxs-lookup"><span data-stu-id="62cf9-105">Represents a container for control names in a custom [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout template.</span></span>

## <a name="usage"></a><span data-ttu-id="62cf9-106">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="62cf9-106">Usage</span></span>

``` syntax
<ControlNameMap>
  child elements
</ControlNameMap>
```

## <a name="attributes"></a><span data-ttu-id="62cf9-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="62cf9-107">Attributes</span></span>

<span data-ttu-id="62cf9-108">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="62cf9-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="62cf9-109">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="62cf9-109">Child elements</span></span>



| <span data-ttu-id="62cf9-110">Element</span><span class="sxs-lookup"><span data-stu-id="62cf9-110">Element</span></span>                                                                                 | <span data-ttu-id="62cf9-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="62cf9-111">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="62cf9-112">**Controlnamedefinition**</span><span class="sxs-lookup"><span data-stu-id="62cf9-112">**ControlNameDefinition**</span></span>](windowsribbon-element-controlnamedefinition.md)<br/> | <span data-ttu-id="62cf9-113">Kann ein-oder mehrmals vorkommen</span><span class="sxs-lookup"><span data-stu-id="62cf9-113">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="62cf9-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="62cf9-114">Parent elements</span></span>



| <span data-ttu-id="62cf9-115">Element</span><span class="sxs-lookup"><span data-stu-id="62cf9-115">Element</span></span>                                                                   |
|---------------------------------------------------------------------------|
| [<span data-ttu-id="62cf9-116">**Sizedefinition**</span><span class="sxs-lookup"><span data-stu-id="62cf9-116">**SizeDefinition**</span></span>](windowsribbon-element-sizedefinition.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="62cf9-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="62cf9-117">Remarks</span></span>

<span data-ttu-id="62cf9-118">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="62cf9-118">Optional.</span></span>

<span data-ttu-id="62cf9-119">Kann höchstens einmal für jedes [**sizedefinition**](windowsribbon-element-sizedefinition.md) -Element auftreten.</span><span class="sxs-lookup"><span data-stu-id="62cf9-119">May occur at most once for each [**SizeDefinition**](windowsribbon-element-sizedefinition.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="62cf9-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="62cf9-120">Examples</span></span>

<span data-ttu-id="62cf9-121">Im folgenden Codebeispiel wird das grundlegende Markup für eine benutzerdefinierte [**sizedefinition**](windowsribbon-element-sizedefinition.md) -Layoutvorlage mit vier Schaltflächen mit einem **controlnamemap** -Element veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="62cf9-121">The following code example demonstrates the basic markup for a custom four-button [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout template with a **ControlNameMap** element.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="62cf9-122">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="62cf9-122">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="62cf9-123">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="62cf9-123">Minimum supported system</span></span><br/> | <span data-ttu-id="62cf9-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="62cf9-124">Windows 7</span></span> |
| <span data-ttu-id="62cf9-125">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="62cf9-125">Can be empty</span></span>                        | <span data-ttu-id="62cf9-126">Nein</span><span class="sxs-lookup"><span data-stu-id="62cf9-126">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="62cf9-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="62cf9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62cf9-128">Anpassen eines Menübands durch Größen Definitionen und Skalierungs Richtlinien</span><span class="sxs-lookup"><span data-stu-id="62cf9-128">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 





