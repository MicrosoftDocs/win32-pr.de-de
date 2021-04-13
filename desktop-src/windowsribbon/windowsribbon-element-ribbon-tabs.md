---
title: Ribbon. Tabs (Eigenschaft)
description: Stellt einen Container für alle Kern Registerkarten in einem Menüband dar.
ms.assetid: b43d0544-c110-4785-85d7-935842b8f03e
keywords:
- Menüband. Registerkarten-Eigenschaften Fenster
topic_type:
- apiref
api_name:
- Ribbon.Tabs
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4300a2385b6ada64e05e16671802460930cc2a7b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475417"
---
# <a name="ribbontabs-property"></a>Ribbon. Tabs (Eigenschaft)

Stellt einen Container für alle Kern Registerkarten in einem Menüband dar.

## <a name="usage"></a>Verbrauch

``` syntax
<Ribbon.Tabs>
  child elements
</Ribbon.Tabs>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                             | BESCHREIBUNG                                     |
|-----------------------------------------------------|-------------------------------------------------|
| [**Registerkarte**](windowsribbon-element-tab.md)<br/> | Muss mindestens einmal vorkommen<br/> <br/> |



## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                   |
|-----------------------------------------------------------|
| [**Menüband**](windowsribbon-element-ribbon.md)<br/> |



## <a name="remarks"></a>Bemerkungen

Erforderlich.

Kann für jedes [**Menüband**](windowsribbon-element-ribbon.md)einmal oder mehrmals vorkommen.

## <a name="examples"></a>Beispiele

Das folgende Beispiel veranschaulicht das einfache Markup für ein **Ribbon. Tabs** -Element mit einer Registerkarten Deklaration der [**Registerkarte**](windowsribbon-element-tab.md) **Home** .


```C++
<Ribbon Name="ScenicRibbonSampleApp">
  <Ribbon.QuickAccessToolbar>
  ...
  </Ribbon.QuickAccessToolbar>
  <Ribbon.ApplicationMenu>
  ...
  </Ribbon.ApplicationMenu>
  <Ribbon.SizeDefinitions>
  ...
  </Ribbon.SizeDefinitions>
  <Ribbon.Tabs>
  ...
```




```C++
<Tab CommandName="cmdHomeTab">
  <Group CommandName="cmdClipboardGroup" 
         SizeDefinition="ThreeButtons">
    <Button CommandName="cmdCopy"/>
    <Button CommandName="cmdPaste"/>
    <ToggleButton CommandName="cmdMinimize"/>
  </Group>
</Tab>
```




```C++
  ...
  </Ribbon.Tabs>
  <Ribbon.ContextualTabs>
  ...
  </Ribbon.ContextualTabs>
  <Ribbon.HelpButton>
  ...
  </Ribbon.HelpButton>
</Ribbon>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Menüband. contextualtabs**](windowsribbon-element-ribbon-contextualtabs.md)
</dt> </dl>

 

 





