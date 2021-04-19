---
title: Ribbon. applicationmenu (Eigenschaft)
description: Stellt das Anwendungsmenü dar. | Ribbon. applicationmenu (Eigenschaft)
ms.assetid: 6945e976-8ac8-40fa-8e71-31812871b496
keywords:
- Menüband. applicationmenu-Eigenschaften Fenster (Menüband)
topic_type:
- apiref
api_name:
- Ribbon.ApplicationMenu
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71263a19057d3f66747b1a40aaa2d0a46528e9b6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106357212"
---
# <a name="ribbonapplicationmenu-property"></a>Ribbon. applicationmenu (Eigenschaft)

Stellt das Anwendungsmenü dar.

## <a name="usage"></a>Verbrauch

``` syntax
<Ribbon.ApplicationMenu>
  child elements
</Ribbon.ApplicationMenu>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                     | BESCHREIBUNG                                    |
|-----------------------------------------------------------------------------|------------------------------------------------|
| [**Applicationmenu**](windowsribbon-element-applicationmenu.md)<br/> | Muss genau einmal auftreten<br/> <br/> |



## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                   |
|-----------------------------------------------------------|
| [**Menüband**](windowsribbon-element-ribbon.md)<br/> |



## <a name="remarks"></a>Bemerkungen

Erforderlich.

Kann höchstens einmal für jedes [**Menüband**](windowsribbon-element-ribbon.md)auftreten.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird das grundlegende Markup für das **Ribbon. applicationmenu** -Element veranschaulicht.

In diesem Code Abschnitt wird die Deklaration des **Ribbon. applicationmenu** -Steuer Elements angezeigt.


```XML
<!-- Control declarations for Application Menu items. -->
<Ribbon.ApplicationMenu>
  <ApplicationMenu CommandName="cmdFileMenu">
    <!-- Most recently used items collection. -->
    <ApplicationMenu.RecentItems>
      <RecentItems CommandName="cmdMRUItems"/>
    </ApplicationMenu.RecentItems>
    <!-- Menu items collection. -->
    <MenuGroup>
      <Button CommandName="cmdNew" />
      <Button CommandName="cmdOpen" />
      <Button CommandName="cmdSave" />
    </MenuGroup>
    <MenuGroup>
      <Button CommandName="cmdPrint" />
      <Button CommandName="cmdExit" />
    </MenuGroup>
  </ApplicationMenu>
</Ribbon.ApplicationMenu>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/> |



 

 





