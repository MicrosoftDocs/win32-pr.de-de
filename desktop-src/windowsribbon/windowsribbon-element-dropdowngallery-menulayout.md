---
title: DropDownGallery.MenuLayout-Eigenschaft
description: Stellt einen Container für DropDownGallery-Dropdownmenülayouts dar.
ms.assetid: 7251e889-377d-4d7f-b049-bd81a202774d
keywords:
- DropDownGallery.MenuLayout-Eigenschaft Windows Menüband
topic_type:
- apiref
api_name:
- DropDownGallery.MenuLayout
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b3fa4c0e2cca92aa2f95f73e0c817314bb71a8260db21a89cb40ec78fff7765
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810680"
---
# <a name="dropdowngallerymenulayout-property"></a>DropDownGallery.MenuLayout-Eigenschaft

Stellt einen Container für [**DropDownGallery-Dropdownmenülayouts**](windowsribbon-element-dropdowngallery.md) dar.

## <a name="usage"></a>Verwendung

``` syntax
<DropDownGallery.MenuLayout>
  child elements
</DropDownGallery.MenuLayout>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                           | Beschreibung                                    |
|-----------------------------------------------------------------------------------|------------------------------------------------|
| [**FlowMenuLayout**](windowsribbon-element-flowmenulayout.md)<br/>         | Muss genau einmal auftreten<br/> <br/> |
| [**VerticalMenuLayout**](windowsribbon-element-verticalmenulayout.md)<br/> | Muss genau einmal auftreten<br/> <br/> |



## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                                     |
|-----------------------------------------------------------------------------|
| [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)<br/> |



## <a name="remarks"></a>Hinweise

Optional.

Kann höchstens einmal für jedes [**DropDownGallery-Element**](windowsribbon-element-dropdowngallery.md) auftreten.

> [!Note]  
> Maximal ein untergeordnetes Element ([**VerticalMenuLayout**](windowsribbon-element-verticalmenulayout.md) oder [**FlowMenuLayout**](windowsribbon-element-flowmenulayout.md)) ist zulässig.

 

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird das grundlegende Markup für [**dropDownGallery**](windowsribbon-element-dropdowngallery.md)veranschaulicht.

Dieser Codeabschnitt zeigt die **DropDownGallery.MenuLayout-Steuerelementdeklaration.**


```XML
<!-- DropDownGallery -->
<Group CommandName="cmdDropDownGalleryGroup">
  <DropDownGallery CommandName="cmdDropDownGallery"
                   TextPosition="Hide"
                   Type="Commands"
                   ItemHeight="32"
                   ItemWidth="32">
    <DropDownGallery.MenuLayout>
      <FlowMenuLayout Rows="2"
                      Columns="3"
                      Gripper="None"/>
    </DropDownGallery.MenuLayout>
    <DropDownGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
       </MenuGroup>
       <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </DropDownGallery.MenuGroups>
  </DropDownGallery>
</Group>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Dropdownkatalog-Steuerelement**](windowsribbon-element-dropdowngallery.md)
</dt> <dt>

[Arbeiten mit Katalogen](ribbon-controls-galleries.md)
</dt> </dl>

 

 





