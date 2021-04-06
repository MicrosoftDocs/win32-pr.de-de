---
title: ScalingPolicy-Element
description: Stellt einen Container für die Skalierung von Spezifikationen dar.
ms.assetid: 133e7994-9901-43e8-82b0-3d910cf8758e
keywords:
- Fenster "scalingpolicy-Element Windows"
topic_type:
- apiref
api_name:
- ScalingPolicy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7f0d0f484ebded1233e3c64f6c7830882395b90a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718803"
---
# <a name="scalingpolicy-element"></a><span data-ttu-id="ad2e4-104">ScalingPolicy-Element</span><span class="sxs-lookup"><span data-stu-id="ad2e4-104">ScalingPolicy element</span></span>

<span data-ttu-id="ad2e4-105">Stellt einen Container für die Skalierung von Spezifikationen dar.</span><span class="sxs-lookup"><span data-stu-id="ad2e4-105">Represents a container for scaling specifications.</span></span>

## <a name="usage"></a><span data-ttu-id="ad2e4-106">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="ad2e4-106">Usage</span></span>

``` syntax
<ScalingPolicy>
  child elements
</ScalingPolicy>
```

## <a name="attributes"></a><span data-ttu-id="ad2e4-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="ad2e4-107">Attributes</span></span>

<span data-ttu-id="ad2e4-108">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="ad2e4-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="ad2e4-109">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ad2e4-109">Child elements</span></span>



| <span data-ttu-id="ad2e4-110">Element</span><span class="sxs-lookup"><span data-stu-id="ad2e4-110">Element</span></span>                                                                                       | <span data-ttu-id="ad2e4-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ad2e4-111">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="ad2e4-112">**Migen**</span><span class="sxs-lookup"><span data-stu-id="ad2e4-112">**Scale**</span></span>](windowsribbon-element-scale.md)<br/>                                       | <span data-ttu-id="ad2e4-113">Kann ein-oder mehrmals vorkommen</span><span class="sxs-lookup"><span data-stu-id="ad2e4-113">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="ad2e4-114">**Scalingpolicy. ideal sizes**</span><span class="sxs-lookup"><span data-stu-id="ad2e4-114">**ScalingPolicy.IdealSizes**</span></span>](windowsribbon-element-scalingpolicy-idealsizes.md)<br/> | <span data-ttu-id="ad2e4-115">Kann höchstens einmal vorkommen</span><span class="sxs-lookup"><span data-stu-id="ad2e4-115">May occur at most once</span></span><br/> <br/>      |



## <a name="parent-elements"></a><span data-ttu-id="ad2e4-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ad2e4-116">Parent elements</span></span>



| <span data-ttu-id="ad2e4-117">Element</span><span class="sxs-lookup"><span data-stu-id="ad2e4-117">Element</span></span>                                                                         |
|---------------------------------------------------------------------------------|
| [<span data-ttu-id="ad2e4-118">**Tab. scalingpolicy**</span><span class="sxs-lookup"><span data-stu-id="ad2e4-118">**Tab.ScalingPolicy**</span></span>](windowsribbon-element-tab-scalingpolicy.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="ad2e4-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ad2e4-119">Remarks</span></span>

<span data-ttu-id="ad2e4-120">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ad2e4-120">Required.</span></span>

<span data-ttu-id="ad2e4-121">Muss für jede [**Tab. scalingpolicy**](windowsribbon-element-tab-scalingpolicy.md)einmal auftreten.</span><span class="sxs-lookup"><span data-stu-id="ad2e4-121">Must occur once for each [**Tab.ScalingPolicy**](windowsribbon-element-tab-scalingpolicy.md).</span></span>

<span data-ttu-id="ad2e4-122">Das **scalingpolicy** -Element enthält ein Manifest der [**scalingpolicy. ideal sizes**](windowsribbon-element-scalingpolicy-idealsizes.md) -und [**Scale**](windowsribbon-element-scale.md) -Deklarationen, die Adaptive Layouteinstellungen für ein oder mehrere [**Gruppen**](windowsribbon-element-group.md) Elemente angeben, wenn die Größe des Menübands geändert wird.</span><span class="sxs-lookup"><span data-stu-id="ad2e4-122">The **ScalingPolicy** element contains a manifest of [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) and [**Scale**](windowsribbon-element-scale.md) declarations that specify adaptive layout preferences for one or more [**Group**](windowsribbon-element-group.md) elements when the Ribbon is resized.</span></span>

<span data-ttu-id="ad2e4-123">Die Liste der [**Skalierungs**](windowsribbon-element-scale.md) Deklarationen muss in absteigender Reihenfolge gültiger Größen (groß, Mittel, klein, Popup) für die [**sizedefinition**](windowsribbon-element-sizedefinition.md) sein, die dem [**Group**](windowsribbon-element-group.md) -Element zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="ad2e4-123">The list of [**Scale**](windowsribbon-element-scale.md) declarations must be in descending order of valid sizes (Large, Medium, Small, Popup) for the [**SizeDefinition**](windowsribbon-element-sizedefinition.md) associated with the [**Group**](windowsribbon-element-group.md) element.</span></span>

> [!Note]  
> <span data-ttu-id="ad2e4-124">Es wird dringend empfohlen, dass ausreichend Details zur Skalierungs Richtlinie angegeben werden, sodass ein Menüband ohne Bild Lauf leisten ohne Bild Lauf leisten dargestellt werden kann, wenn die Größe auf eine Breite von 300 Pixel bei 96 Punkten pro Zoll (dpi) geändert wird.</span><span class="sxs-lookup"><span data-stu-id="ad2e4-124">It is highly recommended that adequate scaling policy detail be specified such that a Ribbon is able to render without scroll bars when resized to a width of 300 pixels at 96 dots per inch (dpi).</span></span>

 

## <a name="examples"></a><span data-ttu-id="ad2e4-125">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ad2e4-125">Examples</span></span>

<span data-ttu-id="ad2e4-126">Im folgenden Beispiel wird veranschaulicht, wie die Darstellung von Steuerelementen in einer [**Gruppe**](windowsribbon-element-group.md) durch die Adaptive Layoutfunktionalität von Menüband- [**sizedefinition**](windowsribbon-element-sizedefinition.md) -Vorlagen angepasst werden kann.</span><span class="sxs-lookup"><span data-stu-id="ad2e4-126">The following example demonstrates how the appearance of controls in a [**Group**](windowsribbon-element-group.md) can be customized through the adaptive layout functionality of Ribbon [**SizeDefinition**](windowsribbon-element-sizedefinition.md) templates.</span></span>

<span data-ttu-id="ad2e4-127">Das **scalingpolicy** -Manifest in diesem Beispiel gibt für jede der vier Gruppen von Steuerelementen auf einer Registerkarte **Home** die Einstellung [**scalingpolicy. ideal sizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**sizedefinition**](windowsribbon-element-sizedefinition.md) an. Außerdem werden [**Skalierungs**](windowsribbon-element-scale.md) Elemente angegeben, um das reduzierende Verhalten der einzelnen Gruppen in absteigender Reihenfolge zu beeinflussen.</span><span class="sxs-lookup"><span data-stu-id="ad2e4-127">The **ScalingPolicy** manifest in this example specifies a [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**SizeDefinition**](windowsribbon-element-sizedefinition.md) preference for each of four groups of controls on a **Home** tab. In addition, [**Scale**](windowsribbon-element-scale.md) elements are specified to influence the collapsing behavior, in descending size order, of each group.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="ad2e4-128">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="ad2e4-128">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="ad2e4-129">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="ad2e4-129">Minimum supported system</span></span><br/> | <span data-ttu-id="ad2e4-130">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ad2e4-130">Windows 7</span></span> |
| <span data-ttu-id="ad2e4-131">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="ad2e4-131">Can be empty</span></span>                        | <span data-ttu-id="ad2e4-132">Nein</span><span class="sxs-lookup"><span data-stu-id="ad2e4-132">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="ad2e4-133">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ad2e4-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad2e4-134">Anpassen eines Menübands durch Größen Definitionen und Skalierungs Richtlinien</span><span class="sxs-lookup"><span data-stu-id="ad2e4-134">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 





