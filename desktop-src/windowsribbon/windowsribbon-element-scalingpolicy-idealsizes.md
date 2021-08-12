---
title: ScalingPolicy.IdealSizes-Eigenschaft
description: Stellt einen Container mit Skalierungsspezifikationen für die bevorzugte SizeDefinition-Vorlage basierend auf der Größe des Menübands dar.
ms.assetid: a4aa2642-160d-4d81-9df9-29277911aa5a
keywords:
- ScalingPolicy.IdealSizes-Eigenschaft Windows Menüband
topic_type:
- apiref
api_name:
- ScalingPolicy.IdealSizes
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 500f6193411ed72b8858506816d9af4f82b1219680fa0537bf54b3daa7735211
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118439525"
---
# <a name="scalingpolicyidealsizes-property"></a>ScalingPolicy.IdealSizes-Eigenschaft

Stellt einen Container mit Skalierungsspezifikationen für die bevorzugte [**SizeDefinition-Vorlage**](windowsribbon-element-sizedefinition.md) basierend auf der Größe des Menübands dar.

## <a name="usage"></a>Verbrauch

``` syntax
<ScalingPolicy.IdealSizes>
  child elements
</ScalingPolicy.IdealSizes>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                 | BESCHREIBUNG                                        |
|---------------------------------------------------------|----------------------------------------------------|
| [**Skalieren**](windowsribbon-element-scale.md)<br/> | Kann ein oder mehrere Male auftreten.<br/> <br/> |



## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                                 |
|-------------------------------------------------------------------------|
| [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md)<br/> |



## <a name="remarks"></a>Hinweise

Optional.

Kann höchstens einmal für jede [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md)auftreten.

Wenn **ScalingPolicy.IdealSizes** definiert ist, muss ein [**Scale-Eintrag**](windowsribbon-element-scale.md) für jedes [**Group-Element**](windowsribbon-element-group.md) in einem [**Tab-Element**](windowsribbon-element-tab.md) vorhanden sein.

**ScalingPolicy.IdealSizes** sind die bevorzugten [**SizeDefinition-Layouts**](windowsribbon-element-sizedefinition.md) für eine [**Gruppe**](windowsribbon-element-group.md) von Steuerelementen.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird veranschaulicht, wie die Darstellung von Steuerelementen in einer [**Gruppe**](windowsribbon-element-group.md) mithilfe der adaptiven Layoutfunktionalität von [**Menübandgrößendefinitionsvorlagen**](windowsribbon-element-sizedefinition.md) angepasst werden kann.

Das [**ScalingPolicy-Manifest**](windowsribbon-element-scalingpolicy.md) in diesem Beispiel gibt eine **ScalingPolicy.IdealSizes** [**SizeDefinition-Einstellung**](windowsribbon-element-sizedefinition.md) für jede von vier Gruppen von Steuerelementen auf einer Registerkarte **Home** an. Darüber hinaus werden [**Skalierungselemente**](windowsribbon-element-scale.md) angegeben, um das Reduzierungsverhalten jeder Gruppe in absteigender Größenreihenfolge zu beeinflussen.


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
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[Anpassen eines Menübands durch Größendefinitionen und Skalierungsrichtlinien](windowsribbon-templates.md)
</dt> </dl>

 

 





