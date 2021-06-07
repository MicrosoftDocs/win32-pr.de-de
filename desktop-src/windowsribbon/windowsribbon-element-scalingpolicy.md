---
title: ScalingPolicy-Element
description: Stellt einen Container zum Skalieren von Spezifikationen dar.
ms.assetid: 133e7994-9901-43e8-82b0-3d910cf8758e
keywords:
- ScalingPolicy-Element im Windows-Menüband
topic_type:
- apiref
api_name:
- ScalingPolicy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 812256b0ff329073eb516c6ab2eb7501db8de40d
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444991"
---
# <a name="scalingpolicy-element"></a><span data-ttu-id="a119d-104">ScalingPolicy-Element</span><span class="sxs-lookup"><span data-stu-id="a119d-104">ScalingPolicy element</span></span>

<span data-ttu-id="a119d-105">Stellt einen Container zum Skalieren von Spezifikationen dar.</span><span class="sxs-lookup"><span data-stu-id="a119d-105">Represents a container for scaling specifications.</span></span>

## <a name="usage"></a><span data-ttu-id="a119d-106">Verwendung</span><span class="sxs-lookup"><span data-stu-id="a119d-106">Usage</span></span>

``` syntax
<ScalingPolicy>
  child elements
</ScalingPolicy>
```

## <a name="attributes"></a><span data-ttu-id="a119d-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="a119d-107">Attributes</span></span>

<span data-ttu-id="a119d-108">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="a119d-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="a119d-109">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a119d-109">Child elements</span></span>



| <span data-ttu-id="a119d-110">Element</span><span class="sxs-lookup"><span data-stu-id="a119d-110">Element</span></span>                                                                                       | <span data-ttu-id="a119d-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a119d-111">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="a119d-112">**Skalieren**</span><span class="sxs-lookup"><span data-stu-id="a119d-112">**Scale**</span></span>](windowsribbon-element-scale.md)<br/>                                       | <span data-ttu-id="a119d-113">Kann ein oder mehrere Male auftreten.</span><span class="sxs-lookup"><span data-stu-id="a119d-113">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="a119d-114">**ScalingPolicy.IdealSizes**</span><span class="sxs-lookup"><span data-stu-id="a119d-114">**ScalingPolicy.IdealSizes**</span></span>](windowsribbon-element-scalingpolicy-idealsizes.md)<br/> | <span data-ttu-id="a119d-115">Kann nur einmal auftreten.</span><span class="sxs-lookup"><span data-stu-id="a119d-115">May occur at most once</span></span><br/> <br/>      |



## <a name="parent-elements"></a><span data-ttu-id="a119d-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a119d-116">Parent elements</span></span>



| <span data-ttu-id="a119d-117">Element</span><span class="sxs-lookup"><span data-stu-id="a119d-117">Element</span></span>                                                                         |
|---------------------------------------------------------------------------------|
| [<span data-ttu-id="a119d-118">**Tab.ScalingPolicy**</span><span class="sxs-lookup"><span data-stu-id="a119d-118">**Tab.ScalingPolicy**</span></span>](windowsribbon-element-tab-scalingpolicy.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="a119d-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a119d-119">Remarks</span></span>

<span data-ttu-id="a119d-120">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a119d-120">Required.</span></span>

<span data-ttu-id="a119d-121">Muss einmal für jedes [**Tab.ScalingPolicy-Objekt auftreten.**](windowsribbon-element-tab-scalingpolicy.md)</span><span class="sxs-lookup"><span data-stu-id="a119d-121">Must occur once for each [**Tab.ScalingPolicy**](windowsribbon-element-tab-scalingpolicy.md).</span></span>

<span data-ttu-id="a119d-122">Das **ScalingPolicy-Element** enthält ein Manifest von [**ScalingPolicy.IdealSizes-**](windowsribbon-element-scalingpolicy-idealsizes.md) und Scale-Deklarationen, die adaptive Layouteinstellungen für mindestens ein [**Group-Element**](windowsribbon-element-group.md) angeben, wenn die Größe des Menübands geändert wird. [](windowsribbon-element-scale.md)</span><span class="sxs-lookup"><span data-stu-id="a119d-122">The **ScalingPolicy** element contains a manifest of [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) and [**Scale**](windowsribbon-element-scale.md) declarations that specify adaptive layout preferences for one or more [**Group**](windowsribbon-element-group.md) elements when the Ribbon is resized.</span></span>

<span data-ttu-id="a119d-123">Die Liste [](windowsribbon-element-scale.md) der Skalierungsdeklarationen muss in absteigender Reihenfolge gültiger Größen (Groß, Mittel, Klein, Popup) für die [**SizeDefinition**](windowsribbon-element-sizedefinition.md) sein, die dem [**Group-Element zugeordnet**](windowsribbon-element-group.md) ist.</span><span class="sxs-lookup"><span data-stu-id="a119d-123">The list of [**Scale**](windowsribbon-element-scale.md) declarations must be in descending order of valid sizes (Large, Medium, Small, Popup) for the [**SizeDefinition**](windowsribbon-element-sizedefinition.md) associated with the [**Group**](windowsribbon-element-group.md) element.</span></span>

> [!Note]  
> <span data-ttu-id="a119d-124">Es wird dringend empfohlen, geeignete Skalierungsrichtliniedetails so anzugeben, dass ein Menüband ohne Bildlaufleisten gerendert werden kann, wenn die Größe auf eine Breite von 300 Pixel bei 96 DPI-Punkten (Dots per Inch) geändert wird.</span><span class="sxs-lookup"><span data-stu-id="a119d-124">It is highly recommended that adequate scaling policy detail be specified such that a Ribbon is able to render without scroll bars when resized to a width of 300 pixels at 96 dots per inch (dpi).</span></span>

 

## <a name="examples"></a><span data-ttu-id="a119d-125">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a119d-125">Examples</span></span>

<span data-ttu-id="a119d-126">Im folgenden Beispiel wird veranschaulicht, wie [](windowsribbon-element-group.md) die Darstellung von Steuerelementen in einer Gruppe mithilfe der Adaptive Layout-Funktionalität von [**Ribbon SizeDefinition-Vorlagen angepasst werden**](windowsribbon-element-sizedefinition.md) kann.</span><span class="sxs-lookup"><span data-stu-id="a119d-126">The following example demonstrates how the appearance of controls in a [**Group**](windowsribbon-element-group.md) can be customized through the adaptive layout functionality of Ribbon [**SizeDefinition**](windowsribbon-element-sizedefinition.md) templates.</span></span>

<span data-ttu-id="a119d-127">Das **ScalingPolicy-Manifest** in diesem Beispiel gibt eine [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**SizeDefinition-Einstellung**](windowsribbon-element-sizedefinition.md) für jede von vier Gruppen von Steuerelementen auf einer Registerkarte **Start** an. Darüber hinaus werden [**Skalierungselemente**](windowsribbon-element-scale.md) angegeben, um das Reduzierungsverhalten jeder Gruppe in absteigender Reihenfolge zu beeinflussen.</span><span class="sxs-lookup"><span data-stu-id="a119d-127">The **ScalingPolicy** manifest in this example specifies a [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**SizeDefinition**](windowsribbon-element-sizedefinition.md) preference for each of four groups of controls on a **Home** tab. In addition, [**Scale**](windowsribbon-element-scale.md) elements are specified to influence the collapsing behavior, in descending size order, of each group.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="a119d-128">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="a119d-128">Element information</span></span>

- <span data-ttu-id="a119d-129">**Unterstütztes Mindestsystem:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="a119d-129">**Minimum supported system**: Windows 7</span></span> 
- <span data-ttu-id="a119d-130">**Kann leer sein:** Nein</span><span class="sxs-lookup"><span data-stu-id="a119d-130">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="a119d-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a119d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a119d-132">Anpassen eines Menübands durch Größendefinitionen und Skalierungsrichtlinien</span><span class="sxs-lookup"><span data-stu-id="a119d-132">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 





