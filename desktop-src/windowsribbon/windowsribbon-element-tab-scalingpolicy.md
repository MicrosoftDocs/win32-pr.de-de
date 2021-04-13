---
title: Tab. scalingpolicy (Eigenschaft)
description: Stellt einen Container für Spezifikationen der Registerkarten Skala dar.
ms.assetid: cc1e4a35-9348-459b-a2f1-25c34d49e5e8
keywords:
- Tab. scalingpolicy-Eigenschaft, Windows-Menüband
topic_type:
- apiref
api_name:
- Tab.ScalingPolicy
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c46528e7b5957415db55f1a51dd6dafed7e1da98
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478606"
---
# <a name="tabscalingpolicy-property"></a><span data-ttu-id="3c065-104">Tab. scalingpolicy (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="3c065-104">Tab.ScalingPolicy property</span></span>

<span data-ttu-id="3c065-105">Stellt einen Container für Spezifikationen der [Register](windowsribbon-controls-tab.md) kartenskala dar.</span><span class="sxs-lookup"><span data-stu-id="3c065-105">Represents a container for [Tab](windowsribbon-controls-tab.md) scaling specifications.</span></span>

## <a name="usage"></a><span data-ttu-id="3c065-106">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="3c065-106">Usage</span></span>

``` syntax
<Tab.ScalingPolicy>
  child elements
</Tab.ScalingPolicy>
```

## <a name="attributes"></a><span data-ttu-id="3c065-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="3c065-107">Attributes</span></span>

<span data-ttu-id="3c065-108">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="3c065-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="3c065-109">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3c065-109">Child elements</span></span>



| <span data-ttu-id="3c065-110">Element</span><span class="sxs-lookup"><span data-stu-id="3c065-110">Element</span></span>                                                                 | <span data-ttu-id="3c065-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3c065-111">Description</span></span>                                    |
|-------------------------------------------------------------------------|------------------------------------------------|
| [<span data-ttu-id="3c065-112">**ScalingPolicy**</span><span class="sxs-lookup"><span data-stu-id="3c065-112">**ScalingPolicy**</span></span>](windowsribbon-element-scalingpolicy.md)<br/> | <span data-ttu-id="3c065-113">Muss genau einmal auftreten</span><span class="sxs-lookup"><span data-stu-id="3c065-113">Must occur exactly once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="3c065-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3c065-114">Parent elements</span></span>



| <span data-ttu-id="3c065-115">Element</span><span class="sxs-lookup"><span data-stu-id="3c065-115">Element</span></span>                                             |
|-----------------------------------------------------|
| [<span data-ttu-id="3c065-116">**Registerkarte**</span><span class="sxs-lookup"><span data-stu-id="3c065-116">**Tab**</span></span>](windowsribbon-element-tab.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="3c065-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3c065-117">Remarks</span></span>

<span data-ttu-id="3c065-118">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="3c065-118">Optional.</span></span>

<span data-ttu-id="3c065-119">Kann höchstens einmal für jede [**Registerkarte**](windowsribbon-element-tab.md)auftreten.</span><span class="sxs-lookup"><span data-stu-id="3c065-119">May occur at most once for each [**Tab**](windowsribbon-element-tab.md).</span></span>

<span data-ttu-id="3c065-120">Skalierungs Spezifikationen beschreiben das Größen-und Layoutverhalten für die Steuerelemente auf einer [Registerkarte](windowsribbon-controls-tab.md) , wenn die Größe des Menübands geändert wird.</span><span class="sxs-lookup"><span data-stu-id="3c065-120">Scaling specifications describe the size and layout behavior for the controls in a [Tab](windowsribbon-controls-tab.md) when the Ribbon is resized.</span></span>

## <a name="examples"></a><span data-ttu-id="3c065-121">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3c065-121">Examples</span></span>

<span data-ttu-id="3c065-122">Das folgende Codebeispiel veranschaulicht ein [**scalingpolicy**](windowsribbon-element-scalingpolicy.md) -Manifest, das eine [**scalingpolicy. ideal sizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**sizedefinition**](windowsribbon-element-sizedefinition.md) -Einstellung für jede von vier Gruppen von Steuerelementen auf einer Registerkarte **Home** angibt. Außerdem werden [**Skalierungs**](windowsribbon-element-scale.md) Elemente angegeben, um das reduzierende Verhalten der einzelnen Gruppen in absteigender Reihenfolge zu beeinflussen.</span><span class="sxs-lookup"><span data-stu-id="3c065-122">The following code example demonstrates a [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) manifest that specifies a [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**SizeDefinition**](windowsribbon-element-sizedefinition.md) preference for each of four groups of controls on a **Home** tab. In addition, [**Scale**](windowsribbon-element-scale.md) elements are specified to influence the collapsing behavior, in descending size order, of each group.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="3c065-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3c065-123">Requirements</span></span>



| <span data-ttu-id="3c065-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3c065-124">Requirement</span></span> | <span data-ttu-id="3c065-125">Wert</span><span class="sxs-lookup"><span data-stu-id="3c065-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="3c065-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3c065-126">Minimum supported client</span></span><br/> | <span data-ttu-id="3c065-127">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3c065-127">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="3c065-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3c065-128">Minimum supported server</span></span><br/> | <span data-ttu-id="3c065-129">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3c065-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3c065-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3c065-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c065-131">Anpassen eines Menübands durch Größen Definitionen und Skalierungs Richtlinien</span><span class="sxs-lookup"><span data-stu-id="3c065-131">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 





