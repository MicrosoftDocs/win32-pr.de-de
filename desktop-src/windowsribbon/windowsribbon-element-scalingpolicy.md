---
title: ScalingPolicy-Element
description: Stellt einen Container für skalierungsspezifikationen dar.
ms.assetid: 133e7994-9901-43e8-82b0-3d910cf8758e
keywords:
- ScalingPolicy-Element Windows Menüband
topic_type:
- apiref
api_name:
- ScalingPolicy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 202112a24a74c9b20d429910fd0ee9447002ce7f2cb95133165fb968eaaf4f69
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007470"
---
# <a name="scalingpolicy-element"></a>ScalingPolicy-Element

Stellt einen Container für skalierungsspezifikationen dar.

## <a name="usage"></a>Verbrauch

``` syntax
<ScalingPolicy>
  child elements
</ScalingPolicy>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                                       | BESCHREIBUNG                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| [**Skalieren**](windowsribbon-element-scale.md)<br/>                                       | Kann ein oder mehrere Male auftreten.<br/> <br/> |
| [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md)<br/> | Kann nur einmal auftreten.<br/> <br/>      |



## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                                         |
|---------------------------------------------------------------------------------|
| [**Tab.ScalingPolicy**](windowsribbon-element-tab-scalingpolicy.md)<br/> |



## <a name="remarks"></a>Hinweise

Erforderlich.

Muss einmal für jedes [**Tab.ScalingPolicy-Objekt auftreten.**](windowsribbon-element-tab-scalingpolicy.md)

Das **ScalingPolicy-Element** enthält ein Manifest der [**Deklarationen ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) und [**Scale,**](windowsribbon-element-scale.md) die adaptive Layouteinstellungen für mindestens ein [**Group-Element**](windowsribbon-element-group.md) angeben, wenn die Größe des Menübands geändert wird.

Die Liste [](windowsribbon-element-scale.md) der Skalierungsdeklarationen muss in absteigender Reihenfolge gültiger Größen (Groß, Mittel, Klein, Popup) für die [**SizeDefinition**](windowsribbon-element-sizedefinition.md) sein, die dem [**Group-Element zugeordnet**](windowsribbon-element-group.md) ist.

> [!Note]  
> Es wird dringend empfohlen, geeignete Skalierungsrichtliniedetails so anzugeben, dass ein Menüband ohne Bildlaufleisten gerendert werden kann, wenn die Größe auf eine Breite von 300 Pixel bei 96 DPI(Dots per Inch) geändert wird.

 

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird veranschaulicht, wie [](windowsribbon-element-group.md) die Darstellung von Steuerelementen in einer Gruppe mithilfe der Adaptive Layout-Funktionalität von [**Ribbon SizeDefinition-Vorlagen angepasst werden**](windowsribbon-element-sizedefinition.md) kann.

Das **ScalingPolicy-Manifest** in diesem Beispiel gibt eine [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**SizeDefinition-Einstellung**](windowsribbon-element-sizedefinition.md) für jede von vier Gruppen von Steuerelementen auf einer Registerkarte **Start** an. Darüber hinaus werden [**Skalierungselemente**](windowsribbon-element-scale.md) angegeben, um das Reduzierungsverhalten jeder Gruppe in absteigender Reihenfolge zu beeinflussen.


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



## <a name="element-information"></a>Elementinformationen

- **Unterstütztes Mindestsystem:** Windows 7 
- **Kann leer sein:** Nein



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Anpassen eines Menübands durch Größendefinitionen und Skalierungsrichtlinien](windowsribbon-templates.md)
</dt> </dl>

 

 





