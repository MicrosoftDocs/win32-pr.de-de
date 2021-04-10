---
title: Inribbongallery. menulayout (Eigenschaft)
description: Stellt einen Container für In-Ribbon Katalog-Dropdown Menü Layouts dar.
ms.assetid: 89e0eb39-2790-4571-a661-ab3ebafbb13f
keywords:
- Inribbongallery. menulayout-Eigenschaften Fenster (Menüband)
topic_type:
- apiref
api_name:
- InRibbonGallery.MenuLayout
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d2fc5e0eab5d8dbc35cd9cb3be96e5d5d351416
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040192"
---
# <a name="inribbongallerymenulayout-property"></a>Inribbongallery. menulayout (Eigenschaft)

Stellt einen Container für [in-Ribbon-](windowsribbon-controls-inribbongallery.md) Katalog-Dropdown Menü Layouts dar.

## <a name="usage"></a>Verbrauch

``` syntax
<InRibbonGallery.MenuLayout>
  child elements
</InRibbonGallery.MenuLayout>
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
| [**Inribbongallery**](windowsribbon-element-inribbongallery.md)<br/> |



## <a name="remarks"></a>Bemerkungen

Dies ist optional.

Kann höchstens einmal für jedes [**inribbongallery**](windowsribbon-element-inribbongallery.md) -Element auftreten.

> [!Note]  
> Maximal ein untergeordnetes Element ([**verticalmenulayout**](windowsribbon-element-verticalmenulayout.md) oder [**flowmenulayout**](windowsribbon-element-flowmenulayout.md)) ist zulässig.

 

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird das grundlegende Markup für den [in-Ribbon-](windowsribbon-controls-inribbongallery.md)Katalog veranschaulicht.

In diesem Code Abschnitt wird die Deklaration des **inribbongallery. menulayout** -Steuer Elements veranschaulicht.


```XML
<!-- InRibbonGallery -->
<Group CommandName="cmdInRibbonGalleryGroup" SizeDefinition="OneInRibbonGallery">
  <InRibbonGallery CommandName="cmdInRibbonGallery"
                   MaxColumns="10"
                   MaxColumnsMedium="5"
                   MinColumnsLarge="5"
                   MinColumnsMedium="3"
                   Type="Items">
    <InRibbonGallery.MenuLayout>
      <VerticalMenuLayout Rows="2"
                          Gripper="Vertical"/>
    </InRibbonGallery.MenuLayout>
    <InRibbonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </InRibbonGallery.MenuGroups>            
  </InRibbonGallery>
</Group>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[In-Ribbon Gallery-Steuerelement](windowsribbon-controls-inribbongallery.md)
</dt> <dt>

[Arbeiten mit Galerien](ribbon-controls-galleries.md)
</dt> </dl>

 

 





