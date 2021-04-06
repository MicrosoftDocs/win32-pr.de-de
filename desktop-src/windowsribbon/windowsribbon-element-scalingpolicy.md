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
# <a name="scalingpolicy-element"></a>ScalingPolicy-Element

Stellt einen Container für die Skalierung von Spezifikationen dar.

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
| [**Migen**](windowsribbon-element-scale.md)<br/>                                       | Kann ein-oder mehrmals vorkommen<br/> <br/> |
| [**Scalingpolicy. ideal sizes**](windowsribbon-element-scalingpolicy-idealsizes.md)<br/> | Kann höchstens einmal vorkommen<br/> <br/>      |



## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                                         |
|---------------------------------------------------------------------------------|
| [**Tab. scalingpolicy**](windowsribbon-element-tab-scalingpolicy.md)<br/> |



## <a name="remarks"></a>Bemerkungen

Erforderlich.

Muss für jede [**Tab. scalingpolicy**](windowsribbon-element-tab-scalingpolicy.md)einmal auftreten.

Das **scalingpolicy** -Element enthält ein Manifest der [**scalingpolicy. ideal sizes**](windowsribbon-element-scalingpolicy-idealsizes.md) -und [**Scale**](windowsribbon-element-scale.md) -Deklarationen, die Adaptive Layouteinstellungen für ein oder mehrere [**Gruppen**](windowsribbon-element-group.md) Elemente angeben, wenn die Größe des Menübands geändert wird.

Die Liste der [**Skalierungs**](windowsribbon-element-scale.md) Deklarationen muss in absteigender Reihenfolge gültiger Größen (groß, Mittel, klein, Popup) für die [**sizedefinition**](windowsribbon-element-sizedefinition.md) sein, die dem [**Group**](windowsribbon-element-group.md) -Element zugeordnet ist.

> [!Note]  
> Es wird dringend empfohlen, dass ausreichend Details zur Skalierungs Richtlinie angegeben werden, sodass ein Menüband ohne Bild Lauf leisten ohne Bild Lauf leisten dargestellt werden kann, wenn die Größe auf eine Breite von 300 Pixel bei 96 Punkten pro Zoll (dpi) geändert wird.

 

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird veranschaulicht, wie die Darstellung von Steuerelementen in einer [**Gruppe**](windowsribbon-element-group.md) durch die Adaptive Layoutfunktionalität von Menüband- [**sizedefinition**](windowsribbon-element-sizedefinition.md) -Vorlagen angepasst werden kann.

Das **scalingpolicy** -Manifest in diesem Beispiel gibt für jede der vier Gruppen von Steuerelementen auf einer Registerkarte **Home** die Einstellung [**scalingpolicy. ideal sizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**sizedefinition**](windowsribbon-element-sizedefinition.md) an. Außerdem werden [**Skalierungs**](windowsribbon-element-scale.md) Elemente angegeben, um das reduzierende Verhalten der einzelnen Gruppen in absteigender Reihenfolge zu beeinflussen.


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



|                                     |           |
|-------------------------------------|-----------|
| Unterstützte Mindestversion (System)<br/> | Windows 7 |
| Kann leer bleiben                        | Nein        |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Anpassen eines Menübands durch Größen Definitionen und Skalierungs Richtlinien](windowsribbon-templates.md)
</dt> </dl>

 

 





