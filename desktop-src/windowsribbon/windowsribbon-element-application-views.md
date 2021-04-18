---
title: Application. views (Eigenschaft)
description: Stellt einen Container für jede Menüband-frameworkansicht dar, insbesondere das Menüband und das contextpopup.
ms.assetid: e7549b8b-0f95-477a-9024-1a99ee1412c2
keywords:
- Application. views-Eigenschaften Fenster (Menüband)
topic_type:
- apiref
api_name:
- Application.Views
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57e7d106d346a790ee3bd8879b2367f38341f0a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339970"
---
# <a name="applicationviews-property"></a>Application. views (Eigenschaft)

Stellt einen Container für jede Menüband-frameworkansicht dar, insbesondere das [**Menüband**](windowsribbon-element-ribbon.md) und das [**contextpopup**](windowsribbon-element-contextpopup.md).

## <a name="usage"></a>Verbrauch

``` syntax
<Application.Views>
  child elements
</Application.Views>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                               | BESCHREIBUNG                                        |
|-----------------------------------------------------------------------|----------------------------------------------------|
| [**Contextpopup**](windowsribbon-element-contextpopup.md)<br/> | Kann ein-oder mehrmals vorkommen<br/> <br/> |
| [**Menüband**](windowsribbon-element-ribbon.md)<br/>             | Muss genau einmal auftreten<br/> <br/>     |



## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                             |
|---------------------------------------------------------------------|
| [**Application**](windowsribbon-element-application.md)<br/> |



## <a name="remarks"></a>Bemerkungen

Erforderlich.

Muss für jedes [**Anwendungs**](windowsribbon-element-application.md) Element genau einmal auftreten.

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt ein **Application. views** -Element, das ein Manifest von Menü Band Steuerelementen enthält, die jeweils über einen Verweis auf einen Befehl verfügen, der im [**Application. Commands**](windowsribbon-element-application-commands.md) -Element deklariert ist.


```C++
<Application.Views>
  <Ribbon Name="ScenicRibbonSampleApp">
    <Ribbon.Tabs>
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
    </Ribbon.Tabs>
  </Ribbon>
</Application.Views>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Application. Commands**](windowsribbon-element-application-commands.md)
</dt> </dl>

 

 





