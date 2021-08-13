---
title: SplitButtonGallery.MenuGroups (Eigenschaft)
description: Stellt einen Container für einen Satz von Dropdownmenüelementen in einem SplitButtonGallery-Steuerelement dar.
ms.assetid: e30fcf9a-488b-423a-8bc4-fccbc78f74de
keywords:
- SplitButtonGallery.MenuGroups-Eigenschaft Windows Menüband
topic_type:
- apiref
api_name:
- SplitButtonGallery.MenuGroups
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 931a66ffca192a1655f3eeffc405c4c02c8e298c28fe9cb9d0d8c6612e29d793
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119441719"
---
# <a name="splitbuttongallerymenugroups-property"></a>SplitButtonGallery.MenuGroups (Eigenschaft)

Stellt einen Container für einen Satz von Dropdownmenüelementen in einem [**SplitButtonGallery-Steuerelement**](windowsribbon-element-splitbuttongallery.md) dar.

## <a name="usage"></a>Verbrauch

``` syntax
<SplitButtonGallery.MenuGroups>
  child elements
</SplitButtonGallery.MenuGroups>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                         | Beschreibung                                     |
|-----------------------------------------------------------------|-------------------------------------------------|
| [**Menugroup**](windowsribbon-element-menugroup.md)<br/> | Muss mindestens einmal auftreten<br/> <br/> |



## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                                           |
|-----------------------------------------------------------------------------------|
| [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a>Hinweise

Erforderlich.

Muss genau einmal für jedes [**SplitButtonGallery-Element**](windowsribbon-element-splitbuttongallery.md) auftreten.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird das grundlegende Markup für das **SplitButtonGallery.MenuGroups-Element** veranschaulicht.

Dieser Codeabschnitt zeigt die **Steuerelementdeklaration SplitButtonGallery.MenuGroups.**


```XML
<!-- SplitButtonGallery -->
<Group CommandName="cmdSplitButtonGalleryGroup">
  <SplitButtonGallery CommandName="cmdSplitButtonGallery">
    <SplitButtonGallery.MenuLayout>
      <FlowMenuLayout Rows="2"
                      Columns="3"
                      Gripper="None"/>
    </SplitButtonGallery.MenuLayout>
    <SplitButtonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </SplitButtonGallery.MenuGroups>
  </SplitButtonGallery>
</Group>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[Split Button Gallery-Steuerelement](windowsribbon-controls-splitbuttongallery.md)
</dt> <dt>

[Arbeiten mit Katalogen](ribbon-controls-galleries.md)
</dt> </dl>

 

 





