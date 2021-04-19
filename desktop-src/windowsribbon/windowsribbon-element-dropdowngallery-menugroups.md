---
title: Dropdowngallery. menugroups (Eigenschaft)
description: Stellt einen Container für einen Satz von Dropdown Menü Elementen in einem Drop-Down-Katalog Steuerelement dar.
ms.assetid: 594f6ae5-760e-456d-98cd-04ecae0bae99
keywords:
- Dropdowngallery. menugroups-Eigenschaften Fenster (Menüband)
topic_type:
- apiref
api_name:
- DropDownGallery.MenuGroups
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67fcaeb81020cf4c317bf065c25a770d2a77e21f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346756"
---
# <a name="dropdowngallerymenugroups-property"></a>Dropdowngallery. menugroups (Eigenschaft)

Stellt einen Container für einen Satz von Dropdown Menü Elementen in einem [Dropdown-](windowsribbon-controls-dropdowngallery.md) Katalog Steuerelement dar.

## <a name="usage"></a>Verbrauch

``` syntax
<DropDownGallery.MenuGroups>
  child elements
</DropDownGallery.MenuGroups>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                         | BESCHREIBUNG                                     |
|-----------------------------------------------------------------|-------------------------------------------------|
| [**MenuGroup**](windowsribbon-element-menugroup.md)<br/> | Muss mindestens einmal vorkommen<br/> <br/> |



## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                                     |
|-----------------------------------------------------------------------------|
| [**Dropdown Gallery**](windowsribbon-element-dropdowngallery.md)<br/> |



## <a name="remarks"></a>Bemerkungen

Erforderlich.

Muss für jedes [**dropdowngallery**](windowsribbon-element-dropdowngallery.md) -Element genau einmal auftreten.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird das grundlegende Markup für das **dropdowngallery. menugroups** -Element veranschaulicht.

In diesem Code Abschnitt wird die Deklaration des **dropdowngallery. menugroups** -Steuer Elements in einem [Dropdown-](windowsribbon-controls-dropdowngallery.md) Katalog Befehlsbereich veranschaulicht.


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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Dropdown-Katalog-Steuerelement**](windowsribbon-element-dropdowngallery.md)
</dt> <dt>

[Arbeiten mit Galerien](ribbon-controls-galleries.md)
</dt> </dl>

 

 





