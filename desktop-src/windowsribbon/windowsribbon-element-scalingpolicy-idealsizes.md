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
# <a name="scalingpolicyidealsizes-property"></a>Scalingpolicy. idealsizes (Eigenschaft)

Stellt einen Container mit Skalierungs Spezifikationen für die bevorzugte [**sizedefinition**](windowsribbon-element-sizedefinition.md) -Vorlage basierend auf der Menü Band Größe dar.

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
| [**Migen**](windowsribbon-element-scale.md)<br/> | Kann ein-oder mehrmals vorkommen<br/> <br/> |



## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                                 |
|-------------------------------------------------------------------------|
| [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md)<br/> |



## <a name="remarks"></a>Bemerkungen

Dies ist optional.

Kann höchstens einmal für jede [**scalingpolicy**](windowsribbon-element-scalingpolicy.md)auftreten.

Wenn **scalingpolicy. ideal sizes** definiert ist, muss für jedes [**Group**](windowsribbon-element-group.md) -Element in einem [**Tab**](windowsribbon-element-tab.md) -Element ein [**Skalierungs**](windowsribbon-element-scale.md) Eintrag vorhanden sein.

**Scalingpolicy. ideal sizes** sind die bevorzugten [**sizedefinition**](windowsribbon-element-sizedefinition.md) -Layouts für eine [**Gruppe**](windowsribbon-element-group.md) von Steuerelementen.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird veranschaulicht, wie die Darstellung von Steuerelementen in einer [**Gruppe**](windowsribbon-element-group.md) durch die Adaptive Layoutfunktionalität von Menüband- [**sizedefinition**](windowsribbon-element-sizedefinition.md) -Vorlagen angepasst werden kann.

Das [**scalingpolicy**](windowsribbon-element-scalingpolicy.md) -Manifest in diesem Beispiel gibt für jede der vier Gruppen von Steuerelementen auf einer Registerkarte **Home** die Einstellung **scalingpolicy. ideal sizes** [**sizedefinition**](windowsribbon-element-sizedefinition.md) an. Außerdem werden [**Skalierungs**](windowsribbon-element-scale.md) Elemente angegeben, um das reduzierende Verhalten der einzelnen Gruppen in absteigender Reihenfolge zu beeinflussen.


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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Anpassen eines Menübands durch Größen Definitionen und Skalierungs Richtlinien](windowsribbon-templates.md)
</dt> </dl>

 

 





