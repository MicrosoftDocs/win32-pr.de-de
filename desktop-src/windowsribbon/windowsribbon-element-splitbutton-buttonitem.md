---
title: SplitButton. buttonitem (Eigenschaft)
description: Stellt einen Container für eine Schaltfläche oder UMSCHALT Fläche dar, die den Standardbefehl einer unterteilten Schaltfläche verfügbar macht.
ms.assetid: 3d46d606-238d-46d4-b92e-dfd759951770
keywords:
- Fenster "SplitButton. buttonitem"-Eigenschaft (Fenster)
topic_type:
- apiref
api_name:
- SplitButton.ButtonItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bf1e1cb908ce9a86f23f75d17bf2e76797997db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475765"
---
# <a name="splitbuttonbuttonitem-property"></a>SplitButton. buttonitem (Eigenschaft)

Stellt einen Container für eine [Schalt](windowsribbon-controls-button.md) Fläche oder [UMSCHALT Fläche](windowsribbon-controls-togglebutton.md) dar, die den Standardbefehl einer unter [teilten Schaltfläche](windowsribbon-controls-splitbutton.md)verfügbar macht.

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
| [**Schaltfläche**](windowsribbon-element-button.md)<br/>             | Kann höchstens einmal vorkommen<br/> <br/> |
| [**ToggleButton**](windowsribbon-element-togglebutton.md)<br/> | Kann höchstens einmal vorkommen<br/> <br/> |



## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                             |
|---------------------------------------------------------------------|
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/> |



## <a name="remarks"></a>Bemerkungen

Dies ist optional.

Kann höchstens einmal für jedes [**SplitButton-Objekt**](windowsribbon-element-splitbutton.md)auftreten.

Jedes **SplitButton. buttonitem** -Element darf nur ein untergeordnetes [**Schalt**](windowsribbon-element-button.md) Flächen [**-oder-**](windowsribbon-element-togglebutton.md) Element enthalten.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird das grundlegende Markup für die [Trenn Schaltfläche](windowsribbon-controls-splitbutton.md)veranschaulicht.

Dieser Code Abschnitt zeigt die Befehls Deklarationen [**SplitButton**](windowsribbon-element-splitbutton.md) und **SplitButton. buttonitem** mit einer zugeordneten [**Gruppe**](windowsribbon-element-group.md) , die als übergeordneter Container für das **SplitButton** -Element fungiert.


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



In diesem Code Abschnitt werden die Deklarationen [**SplitButton**](windowsribbon-element-splitbutton.md) und **SplitButton. buttonitem** -Steuerelement gezeigt.


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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Steuerelement "Split Button](windowsribbon-controls-splitbutton.md)
</dt> </dl>

 

 





