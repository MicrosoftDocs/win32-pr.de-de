---
title: Tab.ScalingPolicy(Eigenschaft)
description: Stellt einen Container für Tabstoppskalierungsspezifikationen dar.
ms.assetid: cc1e4a35-9348-459b-a2f1-25c34d49e5e8
keywords:
- Tab.ScalingPolicy-Eigenschaft Windows Menüband
topic_type:
- apiref
api_name:
- Tab.ScalingPolicy
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11b98174ff5c3426a4805905f0aa7ada86d63a644f4245135bcede5c71d11e75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117850796"
---
# <a name="tabscalingpolicy-property"></a>Tab.ScalingPolicy(Eigenschaft)

Stellt einen Container für [Tabstoppskalierungsspezifikationen](windowsribbon-controls-tab.md) dar.

## <a name="usage"></a>Verbrauch

``` syntax
<Tab.ScalingPolicy>
  child elements
</Tab.ScalingPolicy>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                 | Beschreibung                                    |
|-------------------------------------------------------------------------|------------------------------------------------|
| [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md)<br/> | Muss genau einmal auftreten<br/> <br/> |



## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                             |
|-----------------------------------------------------|
| [**Registerkarte**](windowsribbon-element-tab.md)<br/> |



## <a name="remarks"></a>Hinweise

Optional.

Kann für jede Registerkarte nur einmal [**auftreten.**](windowsribbon-element-tab.md)

Skalierungsspezifikationen beschreiben die Größe und das Layoutverhalten für die Steuerelemente in einer [Registerkarte,](windowsribbon-controls-tab.md) wenn die Größe des Menübands geändert wird.

## <a name="examples"></a>Beispiele

Im folgenden Codebeispiel wird ein [**ScalingPolicy-Manifest**](windowsribbon-element-scalingpolicy.md) veranschaulicht, das eine [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**SizeDefinition-Einstellung**](windowsribbon-element-sizedefinition.md) für jede von vier Gruppen von Steuerelementen auf einer **Registerkarte Start angibt.** Darüber hinaus werden [**Skalierungselemente**](windowsribbon-element-scale.md) angegeben, um das Reduzierungsverhalten jeder Gruppe in absteigender Reihenfolge zu beeinflussen.


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



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Anpassen eines Menübands durch Größendefinitionen und Skalierungsrichtlinien](windowsribbon-templates.md)
</dt> </dl>

 

 





