---
title: ControlSizeDefinition-Element
description: Stellt den Layoutstil einer Gruppe von Steuerelementen in einer benutzerdefinierten Vorlage dar.
ms.assetid: f9b875f4-e0cf-4823-81b5-ed19c201dcbb
keywords:
- ControlSizeDefinition-Element Windows-Menüband
topic_type:
- apiref
api_name:
- ControlSizeDefinition
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0ff5217c08b4ea6da1931b0c65501f912f2cc5dc
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443411"
---
# <a name="controlsizedefinition-element"></a><span data-ttu-id="92353-104">ControlSizeDefinition-Element</span><span class="sxs-lookup"><span data-stu-id="92353-104">ControlSizeDefinition element</span></span>

<span data-ttu-id="92353-105">Stellt den Layoutstil einer Gruppe von Steuerelementen in einer benutzerdefinierten Vorlage dar.</span><span class="sxs-lookup"><span data-stu-id="92353-105">Represents the layout style of a group of controls in a custom template.</span></span>

## <a name="usage"></a><span data-ttu-id="92353-106">Verwendung</span><span class="sxs-lookup"><span data-stu-id="92353-106">Usage</span></span>

``` syntax
<ControlSizeDefinition
  ImageSize = "xs:string"
  IsLabelVisible = "Boolean"
  IsImageVisible = "Boolean"
  IsPopup = "Boolean"
  ControlName = "xs:positiveInteger or xs:string"/>
```

## <a name="attributes"></a><span data-ttu-id="92353-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="92353-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="92353-108">attribute</span><span class="sxs-lookup"><span data-stu-id="92353-108">Attribute</span></span></th>
<th><span data-ttu-id="92353-109">Typ</span><span class="sxs-lookup"><span data-stu-id="92353-109">Type</span></span></th>
<th><span data-ttu-id="92353-110">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="92353-110">Required</span></span></th>
<th><span data-ttu-id="92353-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="92353-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="92353-112"><strong>ControlName</strong></span><span class="sxs-lookup"><span data-stu-id="92353-112"><strong>ControlName</strong></span></span><br/></td>
<td><span data-ttu-id="92353-113">xs:positiveInteger oder xs:string</span><span class="sxs-lookup"><span data-stu-id="92353-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="92353-114">Nein</span><span class="sxs-lookup"><span data-stu-id="92353-114">No</span></span><br/></td>
<td><span data-ttu-id="92353-115"><dt><span></span><span></span><strong></strong> (xs:positiveInteger oder xs:string)</span><span class="sxs-lookup"><span data-stu-id="92353-115"><dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="92353-116">Eine Zeichenfolge, ein ganzzahliger Wert zwischen 2 und 59999 einschließlich oder ein Hexadezimalwert zwischen 0x2 und 0xea5f einschließlich.</span><span class="sxs-lookup"><span data-stu-id="92353-116">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="92353-117">Der Wert muss innerhalb des Menüband-XML-Dokuments eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="92353-117">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="92353-118">Maximale Länge: 100 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="92353-118">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="92353-119"><strong>Imagesize</strong></span><span class="sxs-lookup"><span data-stu-id="92353-119"><strong>ImageSize</strong></span></span><br/></td>
<td><span data-ttu-id="92353-120">xs:string</span><span class="sxs-lookup"><span data-stu-id="92353-120">xs:string</span></span><br/></td>
<td><span data-ttu-id="92353-121">Nein</span><span class="sxs-lookup"><span data-stu-id="92353-121">No</span></span><br/></td>
<td><span data-ttu-id="92353-122">Beschränkt auf einen der folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="92353-122">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="92353-123">
<dt><span></span><span></span><strong></strong> (Groß)</span><span class="sxs-lookup"><span data-stu-id="92353-123">
<dt><span></span><span></span><strong></strong> (Large)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="92353-124"><dt><span></span><span></span><strong></strong> (Klein)</span><span class="sxs-lookup"><span data-stu-id="92353-124"><dt><span></span><span></span><strong></strong> (Small)</span></span><br/> </dt> <dd> <span data-ttu-id="92353-125">Standard.</span><span class="sxs-lookup"><span data-stu-id="92353-125">Default.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="92353-126"><strong>IsImageVisible</strong></span><span class="sxs-lookup"><span data-stu-id="92353-126"><strong>IsImageVisible</strong></span></span><br/></td>
<td><span data-ttu-id="92353-127">Boolesch</span><span class="sxs-lookup"><span data-stu-id="92353-127">Boolean</span></span><br/></td>
<td><span data-ttu-id="92353-128">Nein</span><span class="sxs-lookup"><span data-stu-id="92353-128">No</span></span><br/></td>
<td><span data-ttu-id="92353-129">Beschränkt auf einen der folgenden Werte (0 und 1 sind ungültig):</span><span class="sxs-lookup"><span data-stu-id="92353-129">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="92353-130">
<dt><span></span><span></span><strong></strong> (true)</span><span class="sxs-lookup"><span data-stu-id="92353-130">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="92353-131">Standard.</span><span class="sxs-lookup"><span data-stu-id="92353-131">Default.</span></span> <br/> </dd> <span data-ttu-id="92353-132"><dt><span></span><span></span><strong></strong> (false)</span><span class="sxs-lookup"><span data-stu-id="92353-132"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="92353-133"><strong>IsLabelVisible</strong></span><span class="sxs-lookup"><span data-stu-id="92353-133"><strong>IsLabelVisible</strong></span></span><br/></td>
<td><span data-ttu-id="92353-134">Boolesch</span><span class="sxs-lookup"><span data-stu-id="92353-134">Boolean</span></span><br/></td>
<td><span data-ttu-id="92353-135">Nein</span><span class="sxs-lookup"><span data-stu-id="92353-135">No</span></span><br/></td>
<td><span data-ttu-id="92353-136">Beschränkt auf einen der folgenden Werte (0 und 1 sind ungültig):</span><span class="sxs-lookup"><span data-stu-id="92353-136">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="92353-137">
<dt><span></span><span></span><strong></strong> (true)</span><span class="sxs-lookup"><span data-stu-id="92353-137">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="92353-138">Standard.</span><span class="sxs-lookup"><span data-stu-id="92353-138">Default.</span></span> <br/> </dd> <span data-ttu-id="92353-139"><dt><span></span><span></span><strong></strong> (false)</span><span class="sxs-lookup"><span data-stu-id="92353-139"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="92353-140"><strong>IsPopup</strong></span><span class="sxs-lookup"><span data-stu-id="92353-140"><strong>IsPopup</strong></span></span><br/></td>
<td><span data-ttu-id="92353-141">Boolesch</span><span class="sxs-lookup"><span data-stu-id="92353-141">Boolean</span></span><br/></td>
<td><span data-ttu-id="92353-142">Nein</span><span class="sxs-lookup"><span data-stu-id="92353-142">No</span></span><br/></td>
<td><span data-ttu-id="92353-143">Beschränkt auf einen der folgenden Werte (0 und 1 sind ungültig):</span><span class="sxs-lookup"><span data-stu-id="92353-143">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="92353-144">
<dt><span></span><span></span><strong></strong> (true)</span><span class="sxs-lookup"><span data-stu-id="92353-144">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="92353-145"><dt><span></span><span></span><strong></strong> (false)</span><span class="sxs-lookup"><span data-stu-id="92353-145"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="92353-146">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="92353-146">Child elements</span></span>

<span data-ttu-id="92353-147">Es gibt keine untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="92353-147">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="92353-148">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="92353-148">Parent elements</span></span>



| <span data-ttu-id="92353-149">Element</span><span class="sxs-lookup"><span data-stu-id="92353-149">Element</span></span>                                                                             |
|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="92353-150">**ControlGroup**</span><span class="sxs-lookup"><span data-stu-id="92353-150">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>               |
| [<span data-ttu-id="92353-151">**GroupSizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="92353-151">**GroupSizeDefinition**</span></span>](windowsribbon-element-groupsizedefinition.md)<br/> |
| [<span data-ttu-id="92353-152">**Zeile**</span><span class="sxs-lookup"><span data-stu-id="92353-152">**Row**</span></span>](windowsribbon-element-row.md)<br/>                                 |



## <a name="remarks"></a><span data-ttu-id="92353-153">Hinweise</span><span class="sxs-lookup"><span data-stu-id="92353-153">Remarks</span></span>

<span data-ttu-id="92353-154">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="92353-154">Optional.</span></span>

<span data-ttu-id="92353-155">Kann ein oder mehrere Male für jedes [**ControlGroup-,**](windowsribbon-element-controlgroup.md) [**Row-**](windowsribbon-element-row.md)oder [**SizeDefinition-Element**](windowsribbon-element-sizedefinition.md) auftreten.</span><span class="sxs-lookup"><span data-stu-id="92353-155">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**Row**](windowsribbon-element-row.md), or [**SizeDefinition**](windowsribbon-element-sizedefinition.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="92353-156">Beispiele</span><span class="sxs-lookup"><span data-stu-id="92353-156">Examples</span></span>

<span data-ttu-id="92353-157">Im folgenden Codebeispiel wird das grundlegende Markup für eine benutzerdefinierte [**SizeDefinition-Layoutvorlage**](windowsribbon-element-sizedefinition.md) mit vier Schaltflächen mit verschiedenen **ControlSizeDefinition-Elementen** veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="92353-157">The following code example demonstrates the basic markup for a custom four-button [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout template with various **ControlSizeDefinition** elements.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="92353-158">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="92353-158">Element information</span></span>

* <span data-ttu-id="92353-159">**Unterstütztes Mindestsystem:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="92353-159">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="92353-160">**Kann leer sein:** Ja</span><span class="sxs-lookup"><span data-stu-id="92353-160">**Can be empty**: Yes</span></span>



## <a name="see-also"></a><span data-ttu-id="92353-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="92353-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92353-162">Anpassen eines Menübands durch Größendefinitionen und Skalierungsrichtlinien</span><span class="sxs-lookup"><span data-stu-id="92353-162">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 





