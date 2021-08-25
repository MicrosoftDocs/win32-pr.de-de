---
title: Scale-Element
description: Stellt die Größe und Layoutpräferenz einer Gruppe von Steuerelementen über ein Group- und SizeDefinition-Paar dar.
ms.assetid: feef3721-c779-4c64-96c6-9d951ac32277
keywords:
- Scale-Element Windows Menüband
topic_type:
- apiref
api_name:
- Scale
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 580cfad910a727f7e4392489adc8cb8baec9a0bc
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122630201"
---
# <a name="scale-element"></a>Scale-Element

Stellt die Größe und Layoutpräferenz einer [**Gruppe**](windowsribbon-element-group.md) von Steuerelementen durch ein **{Group**-, [**SizeDefinition**](windowsribbon-element-sizedefinition.md)}-Paar dar.

## <a name="usage"></a>Verwendung

``` syntax
<Scale
  Size = "xs:string"
  Group = "xs:positiveInteger or xs:string"
/>
```

## <a name="attributes"></a>Attribute



<table>
<colgroup>
<col  />
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Attribut</th>
<th>Typ</th>
<th>Erforderlich</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Gruppe</strong><br/></td>
<td>xs:positiveInteger oder xs:string<br/></td>
<td>Ja<br/></td>
<td>Muss einem vorhandenen <a href="windowsribbon-element-group.md"><strong></strong></a> <em>Gruppenbefehlsnamen</em>entsprechen.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:positiveInteger oder xs:string)<br/> </dt> <dd> Eine Zeichenfolge oder ein ganzzahliger Wert zwischen 2 und 59999, einschließlich oder 0x2 und 0xea5f hexadezimal, einschließlich. <br/> Der Wert muss innerhalb des Menüband-XML-Dokuments eindeutig sein. <br/> Maximale Länge: 100 Zeichen. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Größe</strong><br/></td>
<td>xs:string<br/></td>
<td>Ja<br/></td>
<td>Dieser Wert sollte einer der gültigen Größen für das <em>SizeDefinition-Attribut</em> der zugeordneten <a href="windowsribbon-element-group.md"><strong>Gruppe</strong></a> von Steuerelementen entsprechen, die in <em>Gruppe</em>angegeben sind. <br/> Beschränkt auf einen der folgenden Werte: <br/> <br/>
<dt><span></span><span></span><strong></strong> (Popup)<br/> </dt> <dd> Identisches Steuerelementlayout, <code>Large</code> das in einem Popup- oder Dropdownbereich gehostet wird.<br/> </dd> <dt><span></span><span></span><strong></strong> (Klein)<br/> </dt> <dd> Small <a href="windowsribbon-element-sizedefinition.md"><strong>SizeDefinition-Vorlage.</strong></a><br/> </dd> <dt><span></span><span></span><strong></strong> (Mittel)<br/> </dt> <dd> Vorlage "Medium <a href="windowsribbon-element-sizedefinition.md"><strong>SizeDefinition".</strong></a><br/> </dd> <dt><span></span><span></span><strong></strong> (Groß)<br/> </dt> <dd> Large <a href="windowsribbon-element-sizedefinition.md"><strong>SizeDefinition-Vorlage.</strong></a><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Untergeordnete Elemente

Es gibt keine untergeordneten Elemente.

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                                                       |
|-----------------------------------------------------------------------------------------------|
| [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md)<br/>                       |
| [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md)<br/> |



## <a name="remarks"></a>Hinweise

Optional.

Kann ein oder mehrere Male für jede [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) oder [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md)auftreten.

Jedes Attributpaar (*Gruppe*, *Größe*) muss eindeutig sein.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird veranschaulicht, wie die Darstellung von Steuerelementen in einer [**Gruppe**](windowsribbon-element-group.md) mithilfe der adaptiven Layoutfunktionalität von [**Menübandgrößendefinitionsvorlagen**](windowsribbon-element-sizedefinition.md) angepasst werden kann.

Das [**ScalingPolicy-Manifest**](windowsribbon-element-scalingpolicy.md) in diesem Beispiel gibt eine [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**SizeDefinition-Einstellung**](windowsribbon-element-sizedefinition.md) für jede von vier Gruppen von Steuerelementen auf einer Registerkarte **Home** an. Darüber hinaus werden **Skalierungselemente** angegeben, um das Reduzierungsverhalten jeder Gruppe in absteigender Größenreihenfolge zu beeinflussen.


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



* **Unterstütztes Mindestsystem:** Windows 7
* **Kann leer sein:** Ja



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[Anpassen eines Menübands durch Größendefinitionen und Skalierungsrichtlinien](windowsribbon-templates.md)
</dt> </dl>

 

 





