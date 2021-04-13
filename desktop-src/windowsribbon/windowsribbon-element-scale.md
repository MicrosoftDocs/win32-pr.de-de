---
title: Scale-Element
description: Stellt die Größe und Layouteinstellung einer Gruppe von Steuerelementen über eine Gruppe, sizedefinition-Paar, dar.
ms.assetid: feef3721-c779-4c64-96c6-9d951ac32277
keywords:
- Menüband für Fenster Skalierungs Element
topic_type:
- apiref
api_name:
- Scale
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3832d36a48b330b036fa287499f9db387335f87b
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2020
ms.locfileid: "104389805"
---
# <a name="scale-element"></a>Scale-Element

Stellt die Größe und die Layouteinstellung einer [**Gruppe**](windowsribbon-element-group.md) von Steuerelementen durch ein {**Group**, [**sizedefinition**](windowsribbon-element-sizedefinition.md)}-Paar dar.

## <a name="usage"></a>Verbrauch

``` syntax
<Scale
  Size = "xs:string"
  Group = "xs:positiveInteger or xs:string"
/>
```

## <a name="attributes"></a>Attribute



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Attribut</th>
<th>type</th>
<th>Erforderlich</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Gruppieren</strong><br/></td>
<td>xs: positiveingeteger oder xs: String<br/></td>
<td>Ja<br/></td>
<td>Muss einem vorhandenen <em>CommandName</em>der <a href="windowsribbon-element-group.md"><strong>Gruppe</strong></a> entsprechen.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: positiveingeteger oder xs: String)<br/> </dt> <dd> Eine Zeichenfolge oder ein ganzzahliger Wert zwischen 2 und 59999, einschließlich, oder 0x2 und 0xea5f in Hexadezimal (einschließlich). <br/> Der Wert muss innerhalb des Menüband-XML-Dokuments eindeutig sein. <br/> Maximale Länge: 100 Zeichen. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Größe</strong><br/></td>
<td>xs:string<br/></td>
<td>Ja<br/></td>
<td>Dieser Wert sollte einer der gültigen Größen für das <em>sizedefinition</em> -Attribut der zugeordneten <a href="windowsribbon-element-group.md"><strong>Gruppe</strong></a> von Steuerelementen entsprechen, die in der <em>Gruppe</em>angegeben sind. <br/> Beschränkt auf einen der folgenden Werte: <br/> <br/>
<dt><span></span><span></span><strong></strong> Up<br/> </dt> <dd> Identisches Steuerelement Layout, das <code>Large</code> jedoch in einem Popup-oder Dropdown Bereich gehostet wird.<br/> </dd> <dt><span></span><span></span><strong></strong> Zuletzt<br/> </dt> <dd> Kleine <a href="windowsribbon-element-sizedefinition.md"><strong>sizedefinition</strong></a> -Vorlage.<br/> </dd> <dt><span></span><span></span><strong></strong> Mittelalter<br/> </dt> <dd> Mittlere <a href="windowsribbon-element-sizedefinition.md"><strong>sizedefinition</strong></a> -Vorlage.<br/> </dd> <dt><span></span><span></span><strong></strong> Viele<br/> </dt> <dd> Große <a href="windowsribbon-element-sizedefinition.md"><strong>sizedefinition</strong></a> -Vorlage.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Untergeordnete Elemente

Es gibt keine untergeordneten Elemente.

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                                                       |
|-----------------------------------------------------------------------------------------------|
| [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md)<br/>                       |
| [**Scalingpolicy. ideal sizes**](windowsribbon-element-scalingpolicy-idealsizes.md)<br/> |



## <a name="remarks"></a>Bemerkungen

Dies ist optional.

Kann einmal oder mehrmals für jede [**scalingpolicy**](windowsribbon-element-scalingpolicy.md) oder [**scalingpolicy. ideal sizes**](windowsribbon-element-scalingpolicy-idealsizes.md)auftreten.

Jedes Attribut Paar (*Gruppe*, *Größe*) muss eindeutig sein.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird veranschaulicht, wie die Darstellung von Steuerelementen in einer [**Gruppe**](windowsribbon-element-group.md) durch die Adaptive Layoutfunktionalität von Menüband- [**sizedefinition**](windowsribbon-element-sizedefinition.md) -Vorlagen angepasst werden kann.

Das [**scalingpolicy**](windowsribbon-element-scalingpolicy.md) -Manifest in diesem Beispiel gibt für jede der vier Gruppen von Steuerelementen auf einer Registerkarte **Home** die Einstellung [**scalingpolicy. ideal sizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**sizedefinition**](windowsribbon-element-sizedefinition.md) an. Außerdem werden **Skalierungs** Elemente angegeben, um das reduzierende Verhalten der einzelnen Gruppen in absteigender Reihenfolge zu beeinflussen.


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
| Kann leer bleiben                        | Ja       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Anpassen eines Menübands durch Größen Definitionen und Skalierungs Richtlinien](windowsribbon-templates.md)
</dt> </dl>

 

 





