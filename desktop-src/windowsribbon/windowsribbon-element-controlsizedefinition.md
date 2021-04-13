---
title: Controlsizedefinition-Element
description: Stellt den Layoutstil einer Gruppe von Steuerelementen in einer benutzerdefinierten Vorlage dar.
ms.assetid: f9b875f4-e0cf-4823-81b5-ed19c201dcbb
keywords:
- Windows-Menüband "controlsizedefinition-Element"
topic_type:
- apiref
api_name:
- ControlSizeDefinition
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e35fe159bf5bafa1ebfa6119215a4265ee900ef0
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312660"
---
# <a name="controlsizedefinition-element"></a><span data-ttu-id="07b4f-104">Controlsizedefinition-Element</span><span class="sxs-lookup"><span data-stu-id="07b4f-104">ControlSizeDefinition element</span></span>

<span data-ttu-id="07b4f-105">Stellt den Layoutstil einer Gruppe von Steuerelementen in einer benutzerdefinierten Vorlage dar.</span><span class="sxs-lookup"><span data-stu-id="07b4f-105">Represents the layout style of a group of controls in a custom template.</span></span>

## <a name="usage"></a><span data-ttu-id="07b4f-106">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="07b4f-106">Usage</span></span>

``` syntax
<ControlSizeDefinition
  ImageSize = "xs:string"
  IsLabelVisible = "Boolean"
  IsImageVisible = "Boolean"
  IsPopup = "Boolean"
  ControlName = "xs:positiveInteger or xs:string"/>
```

## <a name="attributes"></a><span data-ttu-id="07b4f-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="07b4f-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="07b4f-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="07b4f-108">Attribute</span></span></th>
<th><span data-ttu-id="07b4f-109">type</span><span class="sxs-lookup"><span data-stu-id="07b4f-109">Type</span></span></th>
<th><span data-ttu-id="07b4f-110">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="07b4f-110">Required</span></span></th>
<th><span data-ttu-id="07b4f-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="07b4f-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="07b4f-112"><strong>ControlName</strong></span><span class="sxs-lookup"><span data-stu-id="07b4f-112"><strong>ControlName</strong></span></span><br/></td>
<td><span data-ttu-id="07b4f-113">xs: positiveingeteger oder xs: String</span><span class="sxs-lookup"><span data-stu-id="07b4f-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="07b4f-114">Nein</span><span class="sxs-lookup"><span data-stu-id="07b4f-114">No</span></span><br/></td>
<td><span data-ttu-id="07b4f-115"><dt><span></span><span></span><strong></strong> (xs: positiveingeteger oder xs: String)</span><span class="sxs-lookup"><span data-stu-id="07b4f-115"><dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="07b4f-116">Eine Zeichenfolge, ein ganzzahliger Wert zwischen 2 und 59999, einschließlich, oder ein Hexadezimalwert zwischen 0x2 und 0xea5f (einschließlich).</span><span class="sxs-lookup"><span data-stu-id="07b4f-116">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="07b4f-117">Der Wert muss innerhalb des Menüband-XML-Dokuments eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="07b4f-117">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="07b4f-118">Maximale Länge: 100 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="07b4f-118">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="07b4f-119"><strong>ImageSize</strong></span><span class="sxs-lookup"><span data-stu-id="07b4f-119"><strong>ImageSize</strong></span></span><br/></td>
<td><span data-ttu-id="07b4f-120">xs:string</span><span class="sxs-lookup"><span data-stu-id="07b4f-120">xs:string</span></span><br/></td>
<td><span data-ttu-id="07b4f-121">Nein</span><span class="sxs-lookup"><span data-stu-id="07b4f-121">No</span></span><br/></td>
<td><span data-ttu-id="07b4f-122">Beschränkt auf einen der folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="07b4f-122">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="07b4f-123">
<dt><span></span><span></span><strong></strong> Viele</span><span class="sxs-lookup"><span data-stu-id="07b4f-123">
<dt><span></span><span></span><strong></strong> (Large)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="07b4f-124"><dt><span></span><span></span><strong></strong> Zuletzt</span><span class="sxs-lookup"><span data-stu-id="07b4f-124"><dt><span></span><span></span><strong></strong> (Small)</span></span><br/> </dt> <dd> <span data-ttu-id="07b4f-125">Standard.</span><span class="sxs-lookup"><span data-stu-id="07b4f-125">Default.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="07b4f-126"><strong>Isimagevisible</strong></span><span class="sxs-lookup"><span data-stu-id="07b4f-126"><strong>IsImageVisible</strong></span></span><br/></td>
<td><span data-ttu-id="07b4f-127">Boolesch</span><span class="sxs-lookup"><span data-stu-id="07b4f-127">Boolean</span></span><br/></td>
<td><span data-ttu-id="07b4f-128">Nein</span><span class="sxs-lookup"><span data-stu-id="07b4f-128">No</span></span><br/></td>
<td><span data-ttu-id="07b4f-129">Auf einen der folgenden Werte beschränkt (0 und 1 sind ungültig):</span><span class="sxs-lookup"><span data-stu-id="07b4f-129">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="07b4f-130">
<dt><span></span><span></span><strong></strong> Fall</span><span class="sxs-lookup"><span data-stu-id="07b4f-130">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="07b4f-131">Standard.</span><span class="sxs-lookup"><span data-stu-id="07b4f-131">Default.</span></span> <br/> </dd> <span data-ttu-id="07b4f-132"><dt><span></span><span></span><strong></strong> Alarm</span><span class="sxs-lookup"><span data-stu-id="07b4f-132"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="07b4f-133"><strong>Islabelvisible</strong></span><span class="sxs-lookup"><span data-stu-id="07b4f-133"><strong>IsLabelVisible</strong></span></span><br/></td>
<td><span data-ttu-id="07b4f-134">Boolesch</span><span class="sxs-lookup"><span data-stu-id="07b4f-134">Boolean</span></span><br/></td>
<td><span data-ttu-id="07b4f-135">Nein</span><span class="sxs-lookup"><span data-stu-id="07b4f-135">No</span></span><br/></td>
<td><span data-ttu-id="07b4f-136">Auf einen der folgenden Werte beschränkt (0 und 1 sind ungültig):</span><span class="sxs-lookup"><span data-stu-id="07b4f-136">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="07b4f-137">
<dt><span></span><span></span><strong></strong> Fall</span><span class="sxs-lookup"><span data-stu-id="07b4f-137">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="07b4f-138">Standard.</span><span class="sxs-lookup"><span data-stu-id="07b4f-138">Default.</span></span> <br/> </dd> <span data-ttu-id="07b4f-139"><dt><span></span><span></span><strong></strong> Alarm</span><span class="sxs-lookup"><span data-stu-id="07b4f-139"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="07b4f-140"><strong>Ispopup</strong></span><span class="sxs-lookup"><span data-stu-id="07b4f-140"><strong>IsPopup</strong></span></span><br/></td>
<td><span data-ttu-id="07b4f-141">Boolesch</span><span class="sxs-lookup"><span data-stu-id="07b4f-141">Boolean</span></span><br/></td>
<td><span data-ttu-id="07b4f-142">Nein</span><span class="sxs-lookup"><span data-stu-id="07b4f-142">No</span></span><br/></td>
<td><span data-ttu-id="07b4f-143">Auf einen der folgenden Werte beschränkt (0 und 1 sind ungültig):</span><span class="sxs-lookup"><span data-stu-id="07b4f-143">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="07b4f-144">
<dt><span></span><span></span><strong></strong> Fall</span><span class="sxs-lookup"><span data-stu-id="07b4f-144">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="07b4f-145"><dt><span></span><span></span><strong></strong> Alarm</span><span class="sxs-lookup"><span data-stu-id="07b4f-145"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="07b4f-146">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="07b4f-146">Child elements</span></span>

<span data-ttu-id="07b4f-147">Es gibt keine untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="07b4f-147">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="07b4f-148">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="07b4f-148">Parent elements</span></span>



| <span data-ttu-id="07b4f-149">Element</span><span class="sxs-lookup"><span data-stu-id="07b4f-149">Element</span></span>                                                                             |
|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="07b4f-150">**Controlgroup**</span><span class="sxs-lookup"><span data-stu-id="07b4f-150">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>               |
| [<span data-ttu-id="07b4f-151">**Groupsizedefinition**</span><span class="sxs-lookup"><span data-stu-id="07b4f-151">**GroupSizeDefinition**</span></span>](windowsribbon-element-groupsizedefinition.md)<br/> |
| [<span data-ttu-id="07b4f-152">**Zeile**</span><span class="sxs-lookup"><span data-stu-id="07b4f-152">**Row**</span></span>](windowsribbon-element-row.md)<br/>                                 |



## <a name="remarks"></a><span data-ttu-id="07b4f-153">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="07b4f-153">Remarks</span></span>

<span data-ttu-id="07b4f-154">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="07b4f-154">Optional.</span></span>

<span data-ttu-id="07b4f-155">Kann für jedes [**controlgroup**](windowsribbon-element-controlgroup.md)-, [**Row**](windowsribbon-element-row.md)-oder [**sizedefinition**](windowsribbon-element-sizedefinition.md) -Element einmal oder mehrmals vorkommen.</span><span class="sxs-lookup"><span data-stu-id="07b4f-155">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**Row**](windowsribbon-element-row.md), or [**SizeDefinition**](windowsribbon-element-sizedefinition.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="07b4f-156">Beispiele</span><span class="sxs-lookup"><span data-stu-id="07b4f-156">Examples</span></span>

<span data-ttu-id="07b4f-157">Im folgenden Codebeispiel wird das grundlegende Markup für eine benutzerdefinierte [**sizedefinition**](windowsribbon-element-sizedefinition.md) -Layoutvorlage mit vier Schaltflächen mit verschiedenen **controlsizedefinition** -Elementen veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="07b4f-157">The following code example demonstrates the basic markup for a custom four-button [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout template with various **ControlSizeDefinition** elements.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="07b4f-158">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="07b4f-158">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="07b4f-159">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="07b4f-159">Minimum supported system</span></span><br/> | <span data-ttu-id="07b4f-160">Windows 7</span><span class="sxs-lookup"><span data-stu-id="07b4f-160">Windows 7</span></span> |
| <span data-ttu-id="07b4f-161">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="07b4f-161">Can be empty</span></span>                        | <span data-ttu-id="07b4f-162">Ja</span><span class="sxs-lookup"><span data-stu-id="07b4f-162">Yes</span></span>       |



## <a name="see-also"></a><span data-ttu-id="07b4f-163">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="07b4f-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07b4f-164">Anpassen eines Menübands durch Größen Definitionen und Skalierungs Richtlinien</span><span class="sxs-lookup"><span data-stu-id="07b4f-164">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 





