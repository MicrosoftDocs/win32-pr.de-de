---
title: ControlNameMap-Element
description: Stellt einen Container für Steuerelementnamen in einer benutzerdefinierten SizeDefinition-Layoutvorlage dar.
ms.assetid: b4bceb90-a9a3-42d7-a85b-bf6e4e02784b
keywords:
- ControlNameMap-Element Im Windows-Menüband
topic_type:
- apiref
api_name:
- ControlNameMap
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 42654af7f81730d01f9c699de7041ba24be185e9
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111442911"
---
# <a name="controlnamemap-element"></a><span data-ttu-id="33c83-104">ControlNameMap-Element</span><span class="sxs-lookup"><span data-stu-id="33c83-104">ControlNameMap element</span></span>

<span data-ttu-id="33c83-105">Stellt einen Container für Steuerelementnamen in einer benutzerdefinierten [**SizeDefinition-Layoutvorlage**](windowsribbon-element-sizedefinition.md) dar.</span><span class="sxs-lookup"><span data-stu-id="33c83-105">Represents a container for control names in a custom [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout template.</span></span>

## <a name="usage"></a><span data-ttu-id="33c83-106">Verwendung</span><span class="sxs-lookup"><span data-stu-id="33c83-106">Usage</span></span>

``` syntax
<ControlNameMap>
  child elements
</ControlNameMap>
```

## <a name="attributes"></a><span data-ttu-id="33c83-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="33c83-107">Attributes</span></span>

<span data-ttu-id="33c83-108">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="33c83-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="33c83-109">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="33c83-109">Child elements</span></span>



| <span data-ttu-id="33c83-110">Element</span><span class="sxs-lookup"><span data-stu-id="33c83-110">Element</span></span>                                                                                 | <span data-ttu-id="33c83-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="33c83-111">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="33c83-112">**ControlNameDefinition**</span><span class="sxs-lookup"><span data-stu-id="33c83-112">**ControlNameDefinition**</span></span>](windowsribbon-element-controlnamedefinition.md)<br/> | <span data-ttu-id="33c83-113">Kann ein oder mehrere Male auftreten.</span><span class="sxs-lookup"><span data-stu-id="33c83-113">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="33c83-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="33c83-114">Parent elements</span></span>



| <span data-ttu-id="33c83-115">Element</span><span class="sxs-lookup"><span data-stu-id="33c83-115">Element</span></span>                                                                   |
|---------------------------------------------------------------------------|
| [<span data-ttu-id="33c83-116">**SizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="33c83-116">**SizeDefinition**</span></span>](windowsribbon-element-sizedefinition.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="33c83-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="33c83-117">Remarks</span></span>

<span data-ttu-id="33c83-118">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="33c83-118">Optional.</span></span>

<span data-ttu-id="33c83-119">Kann für jedes [**SizeDefinition-Element mindestens einmal**](windowsribbon-element-sizedefinition.md) auftreten.</span><span class="sxs-lookup"><span data-stu-id="33c83-119">May occur at most once for each [**SizeDefinition**](windowsribbon-element-sizedefinition.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="33c83-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="33c83-120">Examples</span></span>

<span data-ttu-id="33c83-121">Im folgenden Codebeispiel wird das grundlegende Markup für eine benutzerdefinierte [**SizeDefinition-Layoutvorlage**](windowsribbon-element-sizedefinition.md) mit vier Schaltflächen mit einem **ControlNameMap-Element** veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="33c83-121">The following code example demonstrates the basic markup for a custom four-button [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout template with a **ControlNameMap** element.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="33c83-122">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="33c83-122">Element information</span></span>

* <span data-ttu-id="33c83-123">**Unterstütztes Mindestsystem:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="33c83-123">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="33c83-124">**Kann leer sein:** Nein</span><span class="sxs-lookup"><span data-stu-id="33c83-124">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="33c83-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="33c83-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33c83-126">Anpassen eines Menübands durch Größendefinitionen und Skalierungsrichtlinien</span><span class="sxs-lookup"><span data-stu-id="33c83-126">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 





