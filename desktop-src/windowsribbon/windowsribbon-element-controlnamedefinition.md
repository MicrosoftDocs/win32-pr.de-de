---
title: ControlNameDefinition-Element
description: Stellt einen Namen eines Steuerelements in einer benutzerdefinierten SizeDefinition-Layoutvorlage dar.
ms.assetid: 94b724bd-a4e3-40e0-9cf0-3cc6a71100d2
keywords:
- ControlNameDefinition-Element Im Windows-Menüband
topic_type:
- apiref
api_name:
- ControlNameDefinition
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6b2dc1db251d4d657c3793d2a66a9add1d324c37
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443441"
---
# <a name="controlnamedefinition-element"></a><span data-ttu-id="9bece-104">ControlNameDefinition-Element</span><span class="sxs-lookup"><span data-stu-id="9bece-104">ControlNameDefinition element</span></span>

<span data-ttu-id="9bece-105">Stellt einen Namen eines Steuerelements in einer benutzerdefinierten [**SizeDefinition-Layoutvorlage**](windowsribbon-element-sizedefinition.md) dar.</span><span class="sxs-lookup"><span data-stu-id="9bece-105">Represents a name of a control in a custom [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout template.</span></span>

## <a name="usage"></a><span data-ttu-id="9bece-106">Verwendung</span><span class="sxs-lookup"><span data-stu-id="9bece-106">Usage</span></span>

``` syntax
<ControlNameDefinition
  Name = "xs:positiveInteger or xs:string">
  child elements
</ControlNameDefinition>
```

## <a name="attributes"></a><span data-ttu-id="9bece-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="9bece-107">Attributes</span></span>



| <span data-ttu-id="9bece-108">attribute</span><span class="sxs-lookup"><span data-stu-id="9bece-108">Attribute</span></span>           | <span data-ttu-id="9bece-109">Typ</span><span class="sxs-lookup"><span data-stu-id="9bece-109">Type</span></span>                                       | <span data-ttu-id="9bece-110">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="9bece-110">Required</span></span>      | <span data-ttu-id="9bece-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9bece-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                           |
|---------------------|--------------------------------------------|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9bece-112">**Name**</span><span class="sxs-lookup"><span data-stu-id="9bece-112">**Name**</span></span><br/> | <span data-ttu-id="9bece-113">xs:positiveInteger oder xs:string</span><span class="sxs-lookup"><span data-stu-id="9bece-113">xs:positiveInteger or xs:string</span></span><br/> | <span data-ttu-id="9bece-114">Nein</span><span class="sxs-lookup"><span data-stu-id="9bece-114">No</span></span><br/> | <span data-ttu-id="9bece-115"><dt> (xs:positiveInteger oder xs:string)</span><span class="sxs-lookup"><span data-stu-id="9bece-115"><dt> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="9bece-116">Eine Zeichenfolge, ein ganzzahliger Wert zwischen 2 und 59999, einschließlich, oder ein Hexadezimalwert zwischen 0x2 und 0xea5f einschließlich.</span><span class="sxs-lookup"><span data-stu-id="9bece-116">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="9bece-117">Der Wert muss innerhalb des Menüband-XML-Dokuments eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="9bece-117">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="9bece-118">Maximale Länge: 100 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="9bece-118">Maximum length: 100 characters.</span></span> <br/> </dd> </dl> |



## <a name="child-elements"></a><span data-ttu-id="9bece-119">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9bece-119">Child elements</span></span>



| <span data-ttu-id="9bece-120">Element</span><span class="sxs-lookup"><span data-stu-id="9bece-120">Element</span></span>                              | <span data-ttu-id="9bece-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9bece-121">Description</span></span>                                        |
|--------------------------------------|----------------------------------------------------|
| <span data-ttu-id="9bece-122">**ControlNameDefinition**</span><span class="sxs-lookup"><span data-stu-id="9bece-122">**ControlNameDefinition**</span></span><br/> | <span data-ttu-id="9bece-123">Kann ein oder mehrere Male auftreten.</span><span class="sxs-lookup"><span data-stu-id="9bece-123">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="9bece-124">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9bece-124">Parent elements</span></span>



| <span data-ttu-id="9bece-125">Element</span><span class="sxs-lookup"><span data-stu-id="9bece-125">Element</span></span>                                                                   |
|---------------------------------------------------------------------------|
| [<span data-ttu-id="9bece-126">**ControlNameMap**</span><span class="sxs-lookup"><span data-stu-id="9bece-126">**ControlNameMap**</span></span>](windowsribbon-element-controlnamemap.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="9bece-127">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9bece-127">Remarks</span></span>

<span data-ttu-id="9bece-128">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="9bece-128">Optional.</span></span>

<span data-ttu-id="9bece-129">Kann ein oder mehrere Male für jedes [**ControlNameMap-Element**](windowsribbon-element-controlnamemap.md) auftreten.</span><span class="sxs-lookup"><span data-stu-id="9bece-129">May occur one or more times for each [**ControlNameMap**](windowsribbon-element-controlnamemap.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="9bece-130">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9bece-130">Examples</span></span>

<span data-ttu-id="9bece-131">Im folgenden Codebeispiel wird das grundlegende Markup für eine benutzerdefinierte [**SizeDefinition-Layoutvorlage**](windowsribbon-element-sizedefinition.md) mit vier Schaltflächen mit vier **ControlNameDefinition-Elementen** veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="9bece-131">The following code example demonstrates the basic markup for a custom four-button [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout template with four **ControlNameDefinition** elements.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="9bece-132">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="9bece-132">Element information</span></span>

* <span data-ttu-id="9bece-133">**Unterstütztes Mindestsystem:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="9bece-133">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="9bece-134">**Kann leer sein:** Nein</span><span class="sxs-lookup"><span data-stu-id="9bece-134">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="9bece-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9bece-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bece-136">Anpassen eines Menübands durch Größendefinitionen und Skalierungsrichtlinien</span><span class="sxs-lookup"><span data-stu-id="9bece-136">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 





