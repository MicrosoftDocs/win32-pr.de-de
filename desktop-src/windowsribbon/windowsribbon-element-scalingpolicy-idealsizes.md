---
title: Scalingpolicy. idealsizes (Eigenschaft)
description: Stellt einen Container mit Skalierungs Spezifikationen für die bevorzugte sizedefinition-Vorlage basierend auf der Menü Band Größe dar.
ms.assetid: a4aa2642-160d-4d81-9df9-29277911aa5a
keywords:
- Skingpolicy. idealsizes-Eigenschaften Fenster (Menüband)
topic_type:
- apiref
api_name:
- ScalingPolicy.IdealSizes
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7bf62cd0388b523f444c4a9cca226b58187212b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346525"
---
# <a name="scalingpolicyidealsizes-property"></a><span data-ttu-id="e03dc-104">Scalingpolicy. idealsizes (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="e03dc-104">ScalingPolicy.IdealSizes property</span></span>

<span data-ttu-id="e03dc-105">Stellt einen Container mit Skalierungs Spezifikationen für die bevorzugte [**sizedefinition**](windowsribbon-element-sizedefinition.md) -Vorlage basierend auf der Menü Band Größe dar.</span><span class="sxs-lookup"><span data-stu-id="e03dc-105">Represents a container of scaling specifications for the preferred [**SizeDefinition**](windowsribbon-element-sizedefinition.md) template, based on Ribbon size.</span></span>

## <a name="usage"></a><span data-ttu-id="e03dc-106">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="e03dc-106">Usage</span></span>

``` syntax
<ScalingPolicy.IdealSizes>
  child elements
</ScalingPolicy.IdealSizes>
```

## <a name="attributes"></a><span data-ttu-id="e03dc-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="e03dc-107">Attributes</span></span>

<span data-ttu-id="e03dc-108">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="e03dc-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="e03dc-109">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e03dc-109">Child elements</span></span>



| <span data-ttu-id="e03dc-110">Element</span><span class="sxs-lookup"><span data-stu-id="e03dc-110">Element</span></span>                                                 | <span data-ttu-id="e03dc-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e03dc-111">Description</span></span>                                        |
|---------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="e03dc-112">**Migen**</span><span class="sxs-lookup"><span data-stu-id="e03dc-112">**Scale**</span></span>](windowsribbon-element-scale.md)<br/> | <span data-ttu-id="e03dc-113">Kann ein-oder mehrmals vorkommen</span><span class="sxs-lookup"><span data-stu-id="e03dc-113">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="e03dc-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e03dc-114">Parent elements</span></span>



| <span data-ttu-id="e03dc-115">Element</span><span class="sxs-lookup"><span data-stu-id="e03dc-115">Element</span></span>                                                                 |
|-------------------------------------------------------------------------|
| [<span data-ttu-id="e03dc-116">**ScalingPolicy**</span><span class="sxs-lookup"><span data-stu-id="e03dc-116">**ScalingPolicy**</span></span>](windowsribbon-element-scalingpolicy.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="e03dc-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e03dc-117">Remarks</span></span>

<span data-ttu-id="e03dc-118">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="e03dc-118">Optional.</span></span>

<span data-ttu-id="e03dc-119">Kann höchstens einmal für jede [**scalingpolicy**](windowsribbon-element-scalingpolicy.md)auftreten.</span><span class="sxs-lookup"><span data-stu-id="e03dc-119">May occur at most once for each [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md).</span></span>

<span data-ttu-id="e03dc-120">Wenn **scalingpolicy. ideal sizes** definiert ist, muss für jedes [**Group**](windowsribbon-element-group.md) -Element in einem [**Tab**](windowsribbon-element-tab.md) -Element ein [**Skalierungs**](windowsribbon-element-scale.md) Eintrag vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="e03dc-120">If **ScalingPolicy.IdealSizes** is defined, then a [**Scale**](windowsribbon-element-scale.md) entry for each [**Group**](windowsribbon-element-group.md) element in a [**Tab**](windowsribbon-element-tab.md) element must be present.</span></span>

<span data-ttu-id="e03dc-121">**Scalingpolicy. ideal sizes** sind die bevorzugten [**sizedefinition**](windowsribbon-element-sizedefinition.md) -Layouts für eine [**Gruppe**](windowsribbon-element-group.md) von Steuerelementen.</span><span class="sxs-lookup"><span data-stu-id="e03dc-121">**ScalingPolicy.IdealSizes** are the preferred [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layouts for a [**Group**](windowsribbon-element-group.md) of controls.</span></span>

## <a name="examples"></a><span data-ttu-id="e03dc-122">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e03dc-122">Examples</span></span>

<span data-ttu-id="e03dc-123">Im folgenden Beispiel wird veranschaulicht, wie die Darstellung von Steuerelementen in einer [**Gruppe**](windowsribbon-element-group.md) durch die Adaptive Layoutfunktionalität von Menüband- [**sizedefinition**](windowsribbon-element-sizedefinition.md) -Vorlagen angepasst werden kann.</span><span class="sxs-lookup"><span data-stu-id="e03dc-123">The following example demonstrates how the appearance of controls in a [**Group**](windowsribbon-element-group.md) can be customized through the adaptive layout functionality of Ribbon [**SizeDefinition**](windowsribbon-element-sizedefinition.md) templates.</span></span>

<span data-ttu-id="e03dc-124">Das [**scalingpolicy**](windowsribbon-element-scalingpolicy.md) -Manifest in diesem Beispiel gibt für jede der vier Gruppen von Steuerelementen auf einer Registerkarte **Home** die Einstellung **scalingpolicy. ideal sizes** [**sizedefinition**](windowsribbon-element-sizedefinition.md) an. Außerdem werden [**Skalierungs**](windowsribbon-element-scale.md) Elemente angegeben, um das reduzierende Verhalten der einzelnen Gruppen in absteigender Reihenfolge zu beeinflussen.</span><span class="sxs-lookup"><span data-stu-id="e03dc-124">The [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) manifest in this example specifies a **ScalingPolicy.IdealSizes** [**SizeDefinition**](windowsribbon-element-sizedefinition.md) preference for each of four groups of controls on a **Home** tab. In addition, [**Scale**](windowsribbon-element-scale.md) elements are specified to influence the collapsing behavior, in descending size order, of each group.</span></span>


```C++
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



## <a name="requirements"></a><span data-ttu-id="e03dc-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e03dc-125">Requirements</span></span>



| <span data-ttu-id="e03dc-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e03dc-126">Requirement</span></span> | <span data-ttu-id="e03dc-127">Wert</span><span class="sxs-lookup"><span data-stu-id="e03dc-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="e03dc-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e03dc-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e03dc-129">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e03dc-129">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="e03dc-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e03dc-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e03dc-131">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e03dc-131">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e03dc-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e03dc-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e03dc-133">Anpassen eines Menübands durch Größen Definitionen und Skalierungs Richtlinien</span><span class="sxs-lookup"><span data-stu-id="e03dc-133">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 





