---
title: SplitButton.ButtonItem-Eigenschaft
description: Stellt einen Container für eine Schaltfläche oder umschaltfläche dar, der den Standardbefehl einer unterteilten Schaltfläche verfügbar macht.
ms.assetid: 3d46d606-238d-46d4-b92e-dfd759951770
keywords:
- SplitButton.ButtonItem-Eigenschaft Windows Menüband
topic_type:
- apiref
api_name:
- SplitButton.ButtonItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f49f316f7c740b434f761bbe4c00906c8f76b5027af9fcc87317af2a51960dab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119840690"
---
# <a name="splitbuttonbuttonitem-property"></a>SplitButton.ButtonItem-Eigenschaft

Stellt einen Container für eine [Schaltfläche](windowsribbon-controls-button.md) oder [umschaltfläche](windowsribbon-controls-togglebutton.md) dar, der den Standardbefehl einer [geteilten Schaltfläche](windowsribbon-controls-splitbutton.md)verfügbar macht.

## <a name="usage"></a>Verbrauch

``` syntax
<SplitButton.ButtonItem>
  child elements
</SplitButton.ButtonItem>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                               | BESCHREIBUNG                                   |
|-----------------------------------------------------------------------|-----------------------------------------------|
| [**Schaltfläche**](windowsribbon-element-button.md)<br/>             | Kann höchstens einmal auftreten.<br/> <br/> |
| [**ToggleButton**](windowsribbon-element-togglebutton.md)<br/> | Kann höchstens einmal auftreten.<br/> <br/> |



## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                             |
|---------------------------------------------------------------------|
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/> |



## <a name="remarks"></a>Hinweise

Optional.

Kann höchstens einmal für jede [**SplitButton-Datei**](windowsribbon-element-splitbutton.md)auftreten.

Jedes **SplitButton.ButtonItem-Element** kann nur ein [**untergeordnetes Button-**](windowsribbon-element-button.md) oder [**ToggleButton-Element**](windowsribbon-element-togglebutton.md) enthalten.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird das grundlegende Markup für die [Geteilte Schaltfläche](windowsribbon-controls-splitbutton.md)veranschaulicht.

Dieser Codeabschnitt zeigt die Befehlsdeklarationen [**SplitButton**](windowsribbon-element-splitbutton.md) und **SplitButton.ButtonItem** mit einer zugeordneten [**Gruppe,**](windowsribbon-element-group.md) die als übergeordneter Container für das **SplitButton-Element** fungiert.


```XML
<!-- SplitButton -->
<Command Name="cmdSplitButtonGroup"
         Symbol="cmdSplitButtonGroup"
         Comment="SplitButton Group"
         LabelTitle="SplitButton"/>
<Command Name="cmdSplitButton"
         Symbol="cmdSplitButton"
         Comment="SplitButton"
         LabelTitle="SplitButton"/>
<Command Name="cmdSBButtonItem"
         Symbol="cmdSBButtonItem"
         Comment="SBButtonItem"
         LabelTitle="SB ButtonItem"/>
<Command Name="cmdSBButton1"
         Symbol="cmdSBButton1"
         Comment="SBButton1"
         LabelTitle="SB Button">
  <Command.LargeImages>
    <Image Source="res/copyL_32.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/copyS_16.bmp"/>
  </Command.SmallImages>
  <Command.LargeHighContrastImages>
    <Image Source="res/copyLHC_32.bmp"/>
  </Command.LargeHighContrastImages>
  <Command.SmallHighContrastImages>
    <Image Source="res/copySHC_16.bmp"/>
  </Command.SmallHighContrastImages>
</Command>
<Command Name="cmdSBMajorItems"
         Comment="Major Items Category"
         LabelTitle="Major Items"/>
<Command Name="cmdSBStandardItems"
         Comment="Standard Items Category"
         LabelTitle="Standard Items"/>
```



Dieser Codeabschnitt zeigt die [**Steuerelementdeklarationen SplitButton**](windowsribbon-element-splitbutton.md) und **SplitButton.ButtonItem.**


```XML
<Group CommandName="cmdSplitButtonGroup">
  <SplitButton CommandName="cmdSplitButton">
    <SplitButton.ButtonItem>
      <Button CommandName="cmdSBButtonItem"/>
    </SplitButton.ButtonItem>
    <SplitButton.MenuGroups>
      <MenuGroup CommandName="cmdSBMajorItems" 
                 Class="MajorItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
      <MenuGroup CommandName="cmdSBStandardItems"
                 Class="StandardItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
      <MenuGroup Class="StandardItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
    </SplitButton.MenuGroups>
  </SplitButton>
</Group>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Steuerelement "Schaltfläche teilen"](windowsribbon-controls-splitbutton.md)
</dt> </dl>

 

 





