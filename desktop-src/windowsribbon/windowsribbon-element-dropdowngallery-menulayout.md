---
title: Dropdowngallery. menulayout (Eigenschaft)
description: Stellt einen Container für Dropdown Gallery-Dropdown Menü Layouts dar.
ms.assetid: 7251e889-377d-4d7f-b049-bd81a202774d
keywords:
- Dropdowngallery. menulayout-Eigenschaften Fenster (Menüband)
topic_type:
- apiref
api_name:
- DropDownGallery.MenuLayout
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d1b6ad3f07f369dfef90b1e6c52c34793e60520
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346755"
---
# <a name="dropdowngallerymenulayout-property"></a>Dropdowngallery. menulayout (Eigenschaft)

Stellt einen Container für [**Dropdown Gallery-Dropdown**](windowsribbon-element-dropdowngallery.md) Menü Layouts dar.

## <a name="usage"></a>Verbrauch

``` syntax
<DropDownGallery.MenuLayout>
  child elements
</DropDownGallery.MenuLayout>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                           | BESCHREIBUNG                                    |
|-----------------------------------------------------------------------------------|------------------------------------------------|
| [**Flowmenulayout**](windowsribbon-element-flowmenulayout.md)<br/>         | Muss genau einmal auftreten<br/> <br/> |
| [**Verticalmenulayout**](windowsribbon-element-verticalmenulayout.md)<br/> | Muss genau einmal auftreten<br/> <br/> |



## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                                     |
|-----------------------------------------------------------------------------|
| [**Dropdown Gallery**](windowsribbon-element-dropdowngallery.md)<br/> |



## <a name="remarks"></a>Bemerkungen

Dies ist optional.

Kann höchstens einmal für jedes [**dropdowngallery**](windowsribbon-element-dropdowngallery.md) -Element auftreten.

> [!Note]  
> Maximal ein untergeordnetes Element ([**verticalmenulayout**](windowsribbon-element-verticalmenulayout.md) oder [**flowmenulayout**](windowsribbon-element-flowmenulayout.md)) ist zulässig.

 

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird das grundlegende Markup für [**dropdowngallery**](windowsribbon-element-dropdowngallery.md)veranschaulicht.

In diesem Code Abschnitt wird die Deklaration des **dropdowngallery. menulayout** -Steuer Elements veranschaulicht.


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

 

 





