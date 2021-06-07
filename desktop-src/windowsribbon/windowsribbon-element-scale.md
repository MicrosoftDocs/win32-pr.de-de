---
title: Scale-Element
description: Stellt die Größe und Layoutpräferenz einer Gruppe von Steuerelementen über ein Group,SizeDefinition-Paar dar.
ms.assetid: feef3721-c779-4c64-96c6-9d951ac32277
keywords:
- Skalierungselement Im Windows-Menüband
topic_type:
- apiref
api_name:
- Scale
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e3ba922b65525b92189673020f7155275bdf49f9
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111445011"
---
# <a name="scale-element"></a><span data-ttu-id="c1943-104">Scale-Element</span><span class="sxs-lookup"><span data-stu-id="c1943-104">Scale element</span></span>

<span data-ttu-id="c1943-105">Stellt die Größe und Layoutpräferenz einer [**Gruppe**](windowsribbon-element-group.md) von Steuerelementen über ein Paar {**Group**, [**SizeDefinition**](windowsribbon-element-sizedefinition.md)} dar.</span><span class="sxs-lookup"><span data-stu-id="c1943-105">Represents the size and layout preference of a [**Group**](windowsribbon-element-group.md) of controls through a {**Group**, [**SizeDefinition**](windowsribbon-element-sizedefinition.md)} pair.</span></span>

## <a name="usage"></a><span data-ttu-id="c1943-106">Verwendung</span><span class="sxs-lookup"><span data-stu-id="c1943-106">Usage</span></span>

``` syntax
<Scale
  Size = "xs:string"
  Group = "xs:positiveInteger or xs:string"
/>
```

## <a name="attributes"></a><span data-ttu-id="c1943-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="c1943-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c1943-108">attribute</span><span class="sxs-lookup"><span data-stu-id="c1943-108">Attribute</span></span></th>
<th><span data-ttu-id="c1943-109">Typ</span><span class="sxs-lookup"><span data-stu-id="c1943-109">Type</span></span></th>
<th><span data-ttu-id="c1943-110">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="c1943-110">Required</span></span></th>
<th><span data-ttu-id="c1943-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c1943-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c1943-112"><strong>Gruppe</strong></span><span class="sxs-lookup"><span data-stu-id="c1943-112"><strong>Group</strong></span></span><br/></td>
<td><span data-ttu-id="c1943-113">xs:positiveInteger oder xs:string</span><span class="sxs-lookup"><span data-stu-id="c1943-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="c1943-114">Ja</span><span class="sxs-lookup"><span data-stu-id="c1943-114">Yes</span></span><br/></td>
<td><span data-ttu-id="c1943-115">Muss einem vorhandenen <a href="windowsribbon-element-group.md"><strong>Gruppenbefehlsnamen</strong></a> <em>entsprechen.</em></span><span class="sxs-lookup"><span data-stu-id="c1943-115">Must correspond to an existing <a href="windowsribbon-element-group.md"><strong>Group</strong></a> <em>CommandName</em>.</span></span><br/> <br/><span data-ttu-id="c1943-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger oder xs:string)</span><span class="sxs-lookup"><span data-stu-id="c1943-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="c1943-117">Eine Zeichenfolge oder ein ganzzahliger Wert zwischen 2 und 59999, einschließlich oder 0x2 und 0xea5f hexadezimal, einschließlich.</span><span class="sxs-lookup"><span data-stu-id="c1943-117">A string or an integer value between 2 and 59999, inclusive, or 0x2 and 0xea5f in hexadecimal, inclusive.</span></span> <br/> <span data-ttu-id="c1943-118">Der Wert muss innerhalb des Menüband-XML-Dokuments eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="c1943-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="c1943-119">Maximale Länge: 100 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="c1943-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c1943-120"><strong>Größe</strong></span><span class="sxs-lookup"><span data-stu-id="c1943-120"><strong>Size</strong></span></span><br/></td>
<td><span data-ttu-id="c1943-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="c1943-121">xs:string</span></span><br/></td>
<td><span data-ttu-id="c1943-122">Ja</span><span class="sxs-lookup"><span data-stu-id="c1943-122">Yes</span></span><br/></td>
<td><span data-ttu-id="c1943-123">Dieser Wert sollte einer der gültigen Größen für das <em>SizeDefinition-Attribut</em> der zugeordneten <a href="windowsribbon-element-group.md"><strong>Gruppe</strong></a> von Steuerelementen entsprechen, die in Gruppe <em>angegeben ist.</em></span><span class="sxs-lookup"><span data-stu-id="c1943-123">This value should correspond to one of the valid sizes for the <em>SizeDefinition</em> attribute of the associated <a href="windowsribbon-element-group.md"><strong>Group</strong></a> of controls specified in <em>Group</em>.</span></span> <br/> <span data-ttu-id="c1943-124">Auf einen der folgenden Werte beschränkt:</span><span class="sxs-lookup"><span data-stu-id="c1943-124">Restricted to one of the following values:</span></span> <br/> <br/><span data-ttu-id="c1943-125">
<dt><span></span><span></span><strong></strong> (Popup)</span><span class="sxs-lookup"><span data-stu-id="c1943-125">
<dt><span></span><span></span><strong></strong> (Popup)</span></span><br/> </dt> <dd> <span data-ttu-id="c1943-126">Identisches Steuerelementlayout, <code>Large</code> das in einem Popup- oder Dropdownbereich gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="c1943-126">Identical control layout to <code>Large</code> but hosted in a pop-up or a drop-down pane.</span></span><br/> </dd> <span data-ttu-id="c1943-127"><dt><span></span><span></span><strong></strong> (Klein)</span><span class="sxs-lookup"><span data-stu-id="c1943-127"><dt><span></span><span></span><strong></strong> (Small)</span></span><br/> </dt> <dd> <span data-ttu-id="c1943-128">Small <a href="windowsribbon-element-sizedefinition.md"><strong>SizeDefinition-Vorlage.</strong></a></span><span class="sxs-lookup"><span data-stu-id="c1943-128">Small <a href="windowsribbon-element-sizedefinition.md"><strong>SizeDefinition</strong></a> template.</span></span><br/> </dd> <span data-ttu-id="c1943-129"><dt><span></span><span></span><strong></strong> (Mittel)</span><span class="sxs-lookup"><span data-stu-id="c1943-129"><dt><span></span><span></span><strong></strong> (Medium)</span></span><br/> </dt> <dd> <span data-ttu-id="c1943-130">Vorlage <a href="windowsribbon-element-sizedefinition.md"><strong>"Medium SizeDefinition".</strong></a></span><span class="sxs-lookup"><span data-stu-id="c1943-130">Medium <a href="windowsribbon-element-sizedefinition.md"><strong>SizeDefinition</strong></a> template.</span></span><br/> </dd> <span data-ttu-id="c1943-131"><dt><span></span><span></span><strong></strong> (Groß)</span><span class="sxs-lookup"><span data-stu-id="c1943-131"><dt><span></span><span></span><strong></strong> (Large)</span></span><br/> </dt> <dd> <span data-ttu-id="c1943-132">Large <a href="windowsribbon-element-sizedefinition.md"><strong>SizeDefinition-Vorlage.</strong></a></span><span class="sxs-lookup"><span data-stu-id="c1943-132">Large <a href="windowsribbon-element-sizedefinition.md"><strong>SizeDefinition</strong></a> template.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="c1943-133">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c1943-133">Child elements</span></span>

<span data-ttu-id="c1943-134">Es gibt keine untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="c1943-134">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="c1943-135">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c1943-135">Parent elements</span></span>



| <span data-ttu-id="c1943-136">Element</span><span class="sxs-lookup"><span data-stu-id="c1943-136">Element</span></span>                                                                                       |
|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c1943-137">**ScalingPolicy**</span><span class="sxs-lookup"><span data-stu-id="c1943-137">**ScalingPolicy**</span></span>](windowsribbon-element-scalingpolicy.md)<br/>                       |
| [<span data-ttu-id="c1943-138">**ScalingPolicy.IdealSizes**</span><span class="sxs-lookup"><span data-stu-id="c1943-138">**ScalingPolicy.IdealSizes**</span></span>](windowsribbon-element-scalingpolicy-idealsizes.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="c1943-139">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c1943-139">Remarks</span></span>

<span data-ttu-id="c1943-140">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="c1943-140">Optional.</span></span>

<span data-ttu-id="c1943-141">Kann ein oder mehrere Male für jedes [**ScalingPolicy-**](windowsribbon-element-scalingpolicy.md) oder [**ScalingPolicy.IdealSizes-Objekt auftreten.**](windowsribbon-element-scalingpolicy-idealsizes.md)</span><span class="sxs-lookup"><span data-stu-id="c1943-141">May occur one or more times for each [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) or [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md).</span></span>

<span data-ttu-id="c1943-142">Jedes *Attributpaar*( Group , *Size*) muss eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="c1943-142">Each (*Group*, *Size*) attribute pair must be unique.</span></span>

## <a name="examples"></a><span data-ttu-id="c1943-143">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c1943-143">Examples</span></span>

<span data-ttu-id="c1943-144">Im folgenden Beispiel wird veranschaulicht, wie [](windowsribbon-element-group.md) die Darstellung von Steuerelementen in einer Gruppe mithilfe der Adaptive Layout-Funktionalität von SizeDefinition-Vorlagen des [**Menübands angepasst werden**](windowsribbon-element-sizedefinition.md) kann.</span><span class="sxs-lookup"><span data-stu-id="c1943-144">The following example demonstrates how the appearance of controls in a [**Group**](windowsribbon-element-group.md) can be customized through the adaptive layout functionality of Ribbon [**SizeDefinition**](windowsribbon-element-sizedefinition.md) templates.</span></span>

<span data-ttu-id="c1943-145">Das [**ScalingPolicy-Manifest**](windowsribbon-element-scalingpolicy.md) in diesem Beispiel gibt eine [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**SizeDefinition-Einstellung**](windowsribbon-element-sizedefinition.md) für jede von vier Gruppen von Steuerelementen auf einer Registerkarte **Start** an. Darüber hinaus werden **Skalierungselemente** angegeben, um das Reduzierungsverhalten jeder Gruppe in absteigender Reihenfolge zu beeinflussen.</span><span class="sxs-lookup"><span data-stu-id="c1943-145">The [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) manifest in this example specifies a [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**SizeDefinition**](windowsribbon-element-sizedefinition.md) preference for each of four groups of controls on a **Home** tab. In addition, **Scale** elements are specified to influence the collapsing behavior, in descending size order, of each group.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="c1943-146">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="c1943-146">Element information</span></span>



* <span data-ttu-id="c1943-147">**Unterstütztes Mindestsystem:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="c1943-147">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="c1943-148">**Kann leer sein:** Ja</span><span class="sxs-lookup"><span data-stu-id="c1943-148">**Can be empty**: Yes</span></span>



## <a name="see-also"></a><span data-ttu-id="c1943-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c1943-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1943-150">Anpassen eines Menübands durch Größendefinitionen und Skalierungsrichtlinien</span><span class="sxs-lookup"><span data-stu-id="c1943-150">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 





