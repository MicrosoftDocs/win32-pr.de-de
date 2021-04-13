---
title: Scale-Element
description: Stellt die Größe und Layouteinstellung einer Gruppe von Steuerelementen über eine Gruppe, sizedefinition-Paar, dar.
ms.assetid: feef3721-c779-4c64-96c6-9d951ac32277
keywords:
- Menüband für Fenster Skalierungs Element
topic_type:
- apiref
api_name:
- Scale
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3832d36a48b330b036fa287499f9db387335f87b
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2020
ms.locfileid: "104389805"
---
# <a name="scale-element"></a><span data-ttu-id="91d15-104">Scale-Element</span><span class="sxs-lookup"><span data-stu-id="91d15-104">Scale element</span></span>

<span data-ttu-id="91d15-105">Stellt die Größe und die Layouteinstellung einer [**Gruppe**](windowsribbon-element-group.md) von Steuerelementen durch ein {**Group**, [**sizedefinition**](windowsribbon-element-sizedefinition.md)}-Paar dar.</span><span class="sxs-lookup"><span data-stu-id="91d15-105">Represents the size and layout preference of a [**Group**](windowsribbon-element-group.md) of controls through a {**Group**, [**SizeDefinition**](windowsribbon-element-sizedefinition.md)} pair.</span></span>

## <a name="usage"></a><span data-ttu-id="91d15-106">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="91d15-106">Usage</span></span>

``` syntax
<Scale
  Size = "xs:string"
  Group = "xs:positiveInteger or xs:string"
/>
```

## <a name="attributes"></a><span data-ttu-id="91d15-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="91d15-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="91d15-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="91d15-108">Attribute</span></span></th>
<th><span data-ttu-id="91d15-109">type</span><span class="sxs-lookup"><span data-stu-id="91d15-109">Type</span></span></th>
<th><span data-ttu-id="91d15-110">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="91d15-110">Required</span></span></th>
<th><span data-ttu-id="91d15-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="91d15-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="91d15-112"><strong>Gruppieren</strong></span><span class="sxs-lookup"><span data-stu-id="91d15-112"><strong>Group</strong></span></span><br/></td>
<td><span data-ttu-id="91d15-113">xs: positiveingeteger oder xs: String</span><span class="sxs-lookup"><span data-stu-id="91d15-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="91d15-114">Ja</span><span class="sxs-lookup"><span data-stu-id="91d15-114">Yes</span></span><br/></td>
<td><span data-ttu-id="91d15-115">Muss einem vorhandenen <em>CommandName</em>der <a href="windowsribbon-element-group.md"><strong>Gruppe</strong></a> entsprechen.</span><span class="sxs-lookup"><span data-stu-id="91d15-115">Must correspond to an existing <a href="windowsribbon-element-group.md"><strong>Group</strong></a> <em>CommandName</em>.</span></span><br/> <br/><span data-ttu-id="91d15-116">
<dt><span></span><span></span><strong></strong> (xs: positiveingeteger oder xs: String)</span><span class="sxs-lookup"><span data-stu-id="91d15-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="91d15-117">Eine Zeichenfolge oder ein ganzzahliger Wert zwischen 2 und 59999, einschließlich, oder 0x2 und 0xea5f in Hexadezimal (einschließlich).</span><span class="sxs-lookup"><span data-stu-id="91d15-117">A string or an integer value between 2 and 59999, inclusive, or 0x2 and 0xea5f in hexadecimal, inclusive.</span></span> <br/> <span data-ttu-id="91d15-118">Der Wert muss innerhalb des Menüband-XML-Dokuments eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="91d15-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="91d15-119">Maximale Länge: 100 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="91d15-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="91d15-120"><strong>Größe</strong></span><span class="sxs-lookup"><span data-stu-id="91d15-120"><strong>Size</strong></span></span><br/></td>
<td><span data-ttu-id="91d15-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="91d15-121">xs:string</span></span><br/></td>
<td><span data-ttu-id="91d15-122">Ja</span><span class="sxs-lookup"><span data-stu-id="91d15-122">Yes</span></span><br/></td>
<td><span data-ttu-id="91d15-123">Dieser Wert sollte einer der gültigen Größen für das <em>sizedefinition</em> -Attribut der zugeordneten <a href="windowsribbon-element-group.md"><strong>Gruppe</strong></a> von Steuerelementen entsprechen, die in der <em>Gruppe</em>angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="91d15-123">This value should correspond to one of the valid sizes for the <em>SizeDefinition</em> attribute of the associated <a href="windowsribbon-element-group.md"><strong>Group</strong></a> of controls specified in <em>Group</em>.</span></span> <br/> <span data-ttu-id="91d15-124">Beschränkt auf einen der folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="91d15-124">Restricted to one of the following values:</span></span> <br/> <br/><span data-ttu-id="91d15-125">
<dt><span></span><span></span><strong></strong> Up</span><span class="sxs-lookup"><span data-stu-id="91d15-125">
<dt><span></span><span></span><strong></strong> (Popup)</span></span><br/> </dt> <dd> <span data-ttu-id="91d15-126">Identisches Steuerelement Layout, das <code>Large</code> jedoch in einem Popup-oder Dropdown Bereich gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="91d15-126">Identical control layout to <code>Large</code> but hosted in a pop-up or a drop-down pane.</span></span><br/> </dd> <span data-ttu-id="91d15-127"><dt><span></span><span></span><strong></strong> Zuletzt</span><span class="sxs-lookup"><span data-stu-id="91d15-127"><dt><span></span><span></span><strong></strong> (Small)</span></span><br/> </dt> <dd> <span data-ttu-id="91d15-128">Kleine <a href="windowsribbon-element-sizedefinition.md"><strong>sizedefinition</strong></a> -Vorlage.</span><span class="sxs-lookup"><span data-stu-id="91d15-128">Small <a href="windowsribbon-element-sizedefinition.md"><strong>SizeDefinition</strong></a> template.</span></span><br/> </dd> <span data-ttu-id="91d15-129"><dt><span></span><span></span><strong></strong> Mittelalter</span><span class="sxs-lookup"><span data-stu-id="91d15-129"><dt><span></span><span></span><strong></strong> (Medium)</span></span><br/> </dt> <dd> <span data-ttu-id="91d15-130">Mittlere <a href="windowsribbon-element-sizedefinition.md"><strong>sizedefinition</strong></a> -Vorlage.</span><span class="sxs-lookup"><span data-stu-id="91d15-130">Medium <a href="windowsribbon-element-sizedefinition.md"><strong>SizeDefinition</strong></a> template.</span></span><br/> </dd> <span data-ttu-id="91d15-131"><dt><span></span><span></span><strong></strong> Viele</span><span class="sxs-lookup"><span data-stu-id="91d15-131"><dt><span></span><span></span><strong></strong> (Large)</span></span><br/> </dt> <dd> <span data-ttu-id="91d15-132">Große <a href="windowsribbon-element-sizedefinition.md"><strong>sizedefinition</strong></a> -Vorlage.</span><span class="sxs-lookup"><span data-stu-id="91d15-132">Large <a href="windowsribbon-element-sizedefinition.md"><strong>SizeDefinition</strong></a> template.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="91d15-133">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="91d15-133">Child elements</span></span>

<span data-ttu-id="91d15-134">Es gibt keine untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="91d15-134">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="91d15-135">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="91d15-135">Parent elements</span></span>



| <span data-ttu-id="91d15-136">Element</span><span class="sxs-lookup"><span data-stu-id="91d15-136">Element</span></span>                                                                                       |
|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="91d15-137">**ScalingPolicy**</span><span class="sxs-lookup"><span data-stu-id="91d15-137">**ScalingPolicy**</span></span>](windowsribbon-element-scalingpolicy.md)<br/>                       |
| [<span data-ttu-id="91d15-138">**Scalingpolicy. ideal sizes**</span><span class="sxs-lookup"><span data-stu-id="91d15-138">**ScalingPolicy.IdealSizes**</span></span>](windowsribbon-element-scalingpolicy-idealsizes.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="91d15-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="91d15-139">Remarks</span></span>

<span data-ttu-id="91d15-140">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="91d15-140">Optional.</span></span>

<span data-ttu-id="91d15-141">Kann einmal oder mehrmals für jede [**scalingpolicy**](windowsribbon-element-scalingpolicy.md) oder [**scalingpolicy. ideal sizes**](windowsribbon-element-scalingpolicy-idealsizes.md)auftreten.</span><span class="sxs-lookup"><span data-stu-id="91d15-141">May occur one or more times for each [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) or [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md).</span></span>

<span data-ttu-id="91d15-142">Jedes Attribut Paar (*Gruppe*, *Größe*) muss eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="91d15-142">Each (*Group*, *Size*) attribute pair must be unique.</span></span>

## <a name="examples"></a><span data-ttu-id="91d15-143">Beispiele</span><span class="sxs-lookup"><span data-stu-id="91d15-143">Examples</span></span>

<span data-ttu-id="91d15-144">Im folgenden Beispiel wird veranschaulicht, wie die Darstellung von Steuerelementen in einer [**Gruppe**](windowsribbon-element-group.md) durch die Adaptive Layoutfunktionalität von Menüband- [**sizedefinition**](windowsribbon-element-sizedefinition.md) -Vorlagen angepasst werden kann.</span><span class="sxs-lookup"><span data-stu-id="91d15-144">The following example demonstrates how the appearance of controls in a [**Group**](windowsribbon-element-group.md) can be customized through the adaptive layout functionality of Ribbon [**SizeDefinition**](windowsribbon-element-sizedefinition.md) templates.</span></span>

<span data-ttu-id="91d15-145">Das [**scalingpolicy**](windowsribbon-element-scalingpolicy.md) -Manifest in diesem Beispiel gibt für jede der vier Gruppen von Steuerelementen auf einer Registerkarte **Home** die Einstellung [**scalingpolicy. ideal sizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**sizedefinition**](windowsribbon-element-sizedefinition.md) an. Außerdem werden **Skalierungs** Elemente angegeben, um das reduzierende Verhalten der einzelnen Gruppen in absteigender Reihenfolge zu beeinflussen.</span><span class="sxs-lookup"><span data-stu-id="91d15-145">The [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) manifest in this example specifies a [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**SizeDefinition**](windowsribbon-element-sizedefinition.md) preference for each of four groups of controls on a **Home** tab. In addition, **Scale** elements are specified to influence the collapsing behavior, in descending size order, of each group.</span></span>


```XML
<Tab CommandName="Home">
  <Tab.ScalingPolicy>
    <ScalingPolicy>
      <ScalingPolicy.IdealSizes>
        <Scale Group="GroupClipboard" Size="Medium"/>
        <Scale Group="GroupView" Size="Large"/>
        <Scale Group="GroupFont" Size="Large"/>
        <Scale Group="GroupParagraph" Size="Large"/>
      </ScalingPolicy.IdealSizes>
      <Scale Group="GroupClipboard" Size="Small"/>
      <Scale Group="GroupClipboard" Size="Popup"/>
      <Scale Group="GroupFont" Size="Medium"/>
      <Scale Group="GroupParagraph" Size="Medium"/>
      <!-- 
        GroupView group is associated with the OneButton SizeDefinition.
        Since this template is constrained to one size (Large) there
        is no need to declare further scaling preferences.
      -->
    </ScalingPolicy>
  </Tab.ScalingPolicy>

  <Group CommandName="GroupClipboard" SizeDefinition="FourButtons">
    <Button CommandName="Paste"/>
    <Button CommandName="Cut"/>
    <Button CommandName="Copy"/>
    <Button CommandName="SelectAll"/>
  </Group>

  <Group CommandName="GroupFont"  ApplicationModes="1">
    <FontControl CommandName="Font" FontType="FontWithColor" />
  </Group>

  <Group CommandName="GroupParagraph"  ApplicationModes="1" SizeDefinition="ButtonGroups">
    <ControlGroup>
      <ControlGroup>
        <ToggleButton CommandName="Numbered" />
        <ToggleButton CommandName="Bulleted" />
      </ControlGroup>
    </ControlGroup>
    <ControlGroup>
      <ControlGroup>
        <ToggleButton CommandName="LeftJustify" />
        <ToggleButton CommandName="CenterJustify" />
        <ToggleButton CommandName="RightJustify" />
      </ControlGroup>
      <ControlGroup/>
      <ControlGroup>
        <Button CommandName="Outdent" />
        <Button CommandName="Indent" />
      </ControlGroup>
    </ControlGroup>
  </Group>

  <Group CommandName="GroupView" SizeDefinition="OneButton" >
    <ToggleButton CommandName="ViewSource"/>
  </Group>

</Tab>
```



## <a name="element-information"></a><span data-ttu-id="91d15-146">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="91d15-146">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="91d15-147">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="91d15-147">Minimum supported system</span></span><br/> | <span data-ttu-id="91d15-148">Windows 7</span><span class="sxs-lookup"><span data-stu-id="91d15-148">Windows 7</span></span> |
| <span data-ttu-id="91d15-149">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="91d15-149">Can be empty</span></span>                        | <span data-ttu-id="91d15-150">Ja</span><span class="sxs-lookup"><span data-stu-id="91d15-150">Yes</span></span>       |



## <a name="see-also"></a><span data-ttu-id="91d15-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="91d15-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91d15-152">Anpassen eines Menübands durch Größen Definitionen und Skalierungs Richtlinien</span><span class="sxs-lookup"><span data-stu-id="91d15-152">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 





