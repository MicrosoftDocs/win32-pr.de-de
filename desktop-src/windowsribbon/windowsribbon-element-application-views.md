---
title: Application.Views-Eigenschaft
description: Stellt einen Container für jede Menübandframeworkansicht dar, insbesondere das Menüband und contextPopup.
ms.assetid: e7549b8b-0f95-477a-9024-1a99ee1412c2
keywords:
- Application.Views-Eigenschaft Windows Menüband
topic_type:
- apiref
api_name:
- Application.Views
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe063397698a74da0421cf0c9c3b2ef46861f1477e0f4ac99fe5d6e6063c7251
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964309"
---
# <a name="applicationviews-property"></a>Application.Views-Eigenschaft

Stellt einen Container für jede Menübandframeworkansicht dar, insbesondere [**das Menüband**](windowsribbon-element-ribbon.md) und [**den ContextPopup.**](windowsribbon-element-contextpopup.md)

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
| [**ContextPopup**](windowsribbon-element-contextpopup.md)<br/> | Kann ein oder mehrere Male auftreten.<br/> <br/> |
| [**Menüband**](windowsribbon-element-ribbon.md)<br/>             | Muss genau einmal auftreten<br/> <br/>     |



## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                             |
|---------------------------------------------------------------------|
| [**Anwendung**](windowsribbon-element-application.md)<br/> |



## <a name="remarks"></a>Hinweise

Erforderlich.

Muss genau einmal für jedes [**Application-Element**](windowsribbon-element-application.md) auftreten.

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt ein **Application.Views-Element,** das ein Manifest von Menübandsteuerelementen enthält, die jeweils einen Verweis auf einen Befehl enthalten, der im [**Application.Commands-Element deklariert**](windowsribbon-element-application-commands.md) ist.


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
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Application.Commands**](windowsribbon-element-application-commands.md)
</dt> </dl>

 

 





