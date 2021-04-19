---
title: Splitbuttongallery. menulayout (Eigenschaft)
description: Stellt einen Container für Dropdown-Menü Layouts für unterteilte Schaltflächen Katalog dar.
ms.assetid: 4bebdff6-16ea-4cf3-adc7-9b86ea200e81
keywords:
- Splitbuttongallery. menulayout-Eigenschaften Fenster (Menüband)
topic_type:
- apiref
api_name:
- SplitButtonGallery.MenuLayout
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04428c14b5e47795da47e5c03970610cd08a6e8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341998"
---
# <a name="splitbuttongallerymenulayout-property"></a>Splitbuttongallery. menulayout (Eigenschaft)

Stellt einen Container für Dropdown-Menü Layouts für unter [teilte Schalt](windowsribbon-controls-splitbuttongallery.md) Flächen Katalog dar.

## <a name="usage"></a>Verbrauch

``` syntax
<SplitButtonGallery.MenuLayout>
  child elements
</SplitButtonGallery.MenuLayout>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                           | BESCHREIBUNG                                    |
|-----------------------------------------------------------------------------------|------------------------------------------------|
| [**Flowmenulayout**](windowsribbon-element-flowmenulayout.md)<br/>         | Muss genau einmal auftreten<br/> <br/> |
| [**Verticalmenulayout**](windowsribbon-element-verticalmenulayout.md)<br/> | Muss genau einmal auftreten<br/> <br/> |



## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                                           |
|-----------------------------------------------------------------------------------|
| [**Splitbuttongallery**](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a>Bemerkungen

Dies ist optional.

Kann höchstens einmal für jedes [**splitbuttongallery**](windowsribbon-element-splitbuttongallery.md) -Element auftreten.

> [!Note]  
> Maximal ein untergeordnetes Element ([**verticalmenulayout**](windowsribbon-element-verticalmenulayout.md) oder [**flowmenulayout**](windowsribbon-element-flowmenulayout.md)) ist zulässig.

 

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird das grundlegende Markup für den Katalog mit unter [teilten Schalt](windowsribbon-controls-splitbuttongallery.md)Flächen veranschaulicht.

In diesem Code Abschnitt wird die Deklaration **splitbuttongallery. menulayout** -Steuerelement gezeigt.


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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Steuerelement "Split Button Gallery"](windowsribbon-controls-splitbuttongallery.md)
</dt> <dt>

[Arbeiten mit Galerien](ribbon-controls-galleries.md)
</dt> </dl>

 

 





