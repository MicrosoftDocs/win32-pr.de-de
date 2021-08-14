---
title: Ribbon.QuickAccessToolbar-Eigenschaft
description: Stellt einen Container für die Quick Access Toolbar (QAT) dar.
ms.assetid: 8a873a48-4f8b-439d-acad-7da2081fbf40
keywords:
- Ribbon.QuickAccessToolbar-Eigenschaft Windows Menüband
topic_type:
- apiref
api_name:
- Ribbon.QuickAccessToolbar
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83e1fa4cb5de43be2b7316d4ed1786c2a1325fa4468538e2ffea41d5d8c9ef0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118202317"
---
# <a name="ribbonquickaccesstoolbar-property"></a>Ribbon.QuickAccessToolbar-Eigenschaft

Stellt einen Container für die Quick Access Toolbar (QAT) dar.

## <a name="usage"></a>Verbrauch

``` syntax
<Ribbon.QuickAccessToolbar>
  child elements
</Ribbon.QuickAccessToolbar>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                           | BESCHREIBUNG                                    |
|-----------------------------------------------------------------------------------|------------------------------------------------|
| [**QuickAccessToolbar**](windowsribbon-element-quickaccesstoolbar.md)<br/> | Muss genau einmal auftreten<br/> <br/> |



## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                   |
|-----------------------------------------------------------|
| [**Menüband**](windowsribbon-element-ribbon.md)<br/> |



## <a name="remarks"></a>Hinweise

Erforderlich.

Kann ein oder mehrere Male für jedes [**Menüband**](windowsribbon-element-ribbon.md)auftreten.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird das grundlegende Markup für das **Ribbon.QuickAccessToolbar-Element** veranschaulicht.


```XML
      <Ribbon.QuickAccessToolbar>
        <QuickAccessToolbar CommandName="cmdQAT"
                            CustomizeCommandName="cmdCustomizeQAT">
          <QuickAccessToolbar.ApplicationDefaults>
            <Button CommandName="cmdButton1"/>
            <ToggleButton CommandName="cmdMinimize"
                          ApplicationDefaults.IsChecked="false"/>
          </QuickAccessToolbar.ApplicationDefaults>
        </QuickAccessToolbar>
      </Ribbon.QuickAccessToolbar>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/> |



 

 





