---
title: ColumnBreak-Element
description: Stellt ein vertikales Trennzeichen (sichtbar oder ausgeblendet) in benutzerdefinierten SizeDefinition-Layoutvorlagen dar.
ms.assetid: 5979d3e6-366b-4c47-810f-90fb8039af8d
keywords:
- ColumnBreak-Element Im Windows-Menüband
topic_type:
- apiref
api_name:
- ColumnBreak
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b5bff1682cdf55b44092a176abd6dc7e935220a7
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444841"
---
# <a name="columnbreak-element"></a><span data-ttu-id="45487-104">ColumnBreak-Element</span><span class="sxs-lookup"><span data-stu-id="45487-104">ColumnBreak element</span></span>

<span data-ttu-id="45487-105">Stellt ein vertikales Trennzeichen (sichtbar oder ausgeblendet) in benutzerdefinierten [**SizeDefinition-Layoutvorlagen**](windowsribbon-element-sizedefinition.md) dar.</span><span class="sxs-lookup"><span data-stu-id="45487-105">Represents a vertical separator (visible or hidden) in custom [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout templates.</span></span>

## <a name="usage"></a><span data-ttu-id="45487-106">Verwendung</span><span class="sxs-lookup"><span data-stu-id="45487-106">Usage</span></span>

``` syntax
<ColumnBreak
  ShowSeparator = "Boolean"/>
```

## <a name="attributes"></a><span data-ttu-id="45487-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="45487-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="45487-108">attribute</span><span class="sxs-lookup"><span data-stu-id="45487-108">Attribute</span></span></th>
<th><span data-ttu-id="45487-109">Typ</span><span class="sxs-lookup"><span data-stu-id="45487-109">Type</span></span></th>
<th><span data-ttu-id="45487-110">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="45487-110">Required</span></span></th>
<th><span data-ttu-id="45487-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="45487-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="45487-112"><strong>ShowSeparator</strong></span><span class="sxs-lookup"><span data-stu-id="45487-112"><strong>ShowSeparator</strong></span></span><br/></td>
<td><span data-ttu-id="45487-113">Boolesch</span><span class="sxs-lookup"><span data-stu-id="45487-113">Boolean</span></span><br/></td>
<td><span data-ttu-id="45487-114">Nein</span><span class="sxs-lookup"><span data-stu-id="45487-114">No</span></span><br/></td>
<td><span data-ttu-id="45487-115">Auf einen der folgenden Werte beschränkt:</span><span class="sxs-lookup"><span data-stu-id="45487-115">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="45487-116">
<dt><span></span><span></span><strong></strong> (true)</span><span class="sxs-lookup"><span data-stu-id="45487-116">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="45487-117">Standard.</span><span class="sxs-lookup"><span data-stu-id="45487-117">Default.</span></span> <br/> </dd> <span data-ttu-id="45487-118"><dt><span></span><span></span><strong></strong> (false)</span><span class="sxs-lookup"><span data-stu-id="45487-118"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="45487-119">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="45487-119">Child elements</span></span>

<span data-ttu-id="45487-120">Es gibt keine untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="45487-120">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="45487-121">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="45487-121">Parent elements</span></span>



| <span data-ttu-id="45487-122">Element</span><span class="sxs-lookup"><span data-stu-id="45487-122">Element</span></span>                                                                             |
|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="45487-123">**GroupSizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="45487-123">**GroupSizeDefinition**</span></span>](windowsribbon-element-groupsizedefinition.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="45487-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="45487-124">Remarks</span></span>

<span data-ttu-id="45487-125">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="45487-125">Optional.</span></span>

<span data-ttu-id="45487-126">Kann ein oder mehrere Male für jedes [**GroupSizeDefinition-Element**](windowsribbon-element-groupsizedefinition.md) auftreten.</span><span class="sxs-lookup"><span data-stu-id="45487-126">May occur one or more times for each [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="45487-127">Beispiele</span><span class="sxs-lookup"><span data-stu-id="45487-127">Examples</span></span>

<span data-ttu-id="45487-128">Im folgenden Beispiel wird das grundlegende Markup für ein **ColumnBreak-Element** in einer benutzerdefinierten [**SizeDefinition-Layoutvorlage**](windowsribbon-element-sizedefinition.md) mit vier Schaltflächen veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="45487-128">The following example demonstrates the basic markup for a **ColumnBreak** element in a custom four-button [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout template.</span></span> <span data-ttu-id="45487-129">**ColumnBreak** wird nur für die Vorlage `Large` angegeben.</span><span class="sxs-lookup"><span data-stu-id="45487-129">The **ColumnBreak** is only specified for the `Large` template.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="45487-130">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="45487-130">Element information</span></span>

* <span data-ttu-id="45487-131">**Unterstütztes Mindestsystem:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="45487-131">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="45487-132">**Kann leer sein:** Ja</span><span class="sxs-lookup"><span data-stu-id="45487-132">**Can be empty**: Yes</span></span>



## <a name="see-also"></a><span data-ttu-id="45487-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="45487-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45487-134">Anpassen eines Menübands durch Größendefinitionen und Skalierungsrichtlinien</span><span class="sxs-lookup"><span data-stu-id="45487-134">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 





