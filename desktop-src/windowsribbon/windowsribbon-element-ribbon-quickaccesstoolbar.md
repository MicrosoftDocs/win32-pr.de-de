---
title: Ribbon. quickaccesstoolbar (Eigenschaft)
description: Stellt einen Container für die Symbolleiste für den schnell Zugriff (QAT) dar.
ms.assetid: 8a873a48-4f8b-439d-acad-7da2081fbf40
keywords:
- Menüband. quickaccesstoolbar-Eigenschaften Fenster (Menüband)
topic_type:
- apiref
api_name:
- Ribbon.QuickAccessToolbar
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad0e09b220bd60b60ccbb8ee05c2da9c4317ba78
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391552"
---
# <a name="ribbonquickaccesstoolbar-property"></a>Ribbon. quickaccesstoolbar (Eigenschaft)

Stellt einen Container für die Symbolleiste für den schnell Zugriff (QAT) dar.

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
| [**Quickaccesstoolbar**](windowsribbon-element-quickaccesstoolbar.md)<br/> | Muss genau einmal auftreten<br/> <br/> |



## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                   |
|-----------------------------------------------------------|
| [**Menüband**](windowsribbon-element-ribbon.md)<br/> |



## <a name="remarks"></a>Bemerkungen

Erforderlich.

Kann für jedes [**Menüband**](windowsribbon-element-ribbon.md)einmal oder mehrmals vorkommen.

## <a name="examples"></a>Beispiele

Das folgende Beispiel veranschaulicht das einfache Markup für das **Ribbon. quickaccesstoolbar** -Element.


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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/> |



 

 





