---
title: InRibbonGallery.MenuLayout (Eigenschaft)
description: Stellt einen Container für In-Ribbon Katalog-Dropdownmenülayouts dar.
ms.assetid: 89e0eb39-2790-4571-a661-ab3ebafbb13f
keywords:
- InRibbonGallery.MenuLayout-Eigenschaft Windows Menüband
topic_type:
- apiref
api_name:
- InRibbonGallery.MenuLayout
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f3748e35280972f115ae22792f28847df675b3aafe8ac91d29d930c9fd15bca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117850763"
---
# <a name="inribbongallerymenulayout-property"></a>InRibbonGallery.MenuLayout (Eigenschaft)

Stellt einen Container für [Dropdownmenülayouts](windowsribbon-controls-inribbongallery.md) im Menübandkatalog dar.

## <a name="usage"></a>Verbrauch

``` syntax
<InRibbonGallery.MenuLayout>
  child elements
</InRibbonGallery.MenuLayout>
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
| [**InRibbonGallery**](windowsribbon-element-inribbongallery.md)<br/> |



## <a name="remarks"></a>Hinweise

Optional.

Kann für jedes [**InRibbonGallery-Element mindestens einmal**](windowsribbon-element-inribbongallery.md) auftreten.

> [!Note]  
> Maximal ein untergeordnetes Element ([**VerticalMenuLayout**](windowsribbon-element-verticalmenulayout.md) oder [**FlowMenuLayout**](windowsribbon-element-flowmenulayout.md)) ist zulässig.

 

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird das grundlegende Markup für den [In-Ribbon Gallery veranschaulicht.](windowsribbon-controls-inribbongallery.md)

Dieser Codeabschnitt zeigt die **Steuerelementdeklaration InRibbonGallery.MenuLayout.**


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
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Steuerelement "Katalog im Menüband"](windowsribbon-controls-inribbongallery.md)
</dt> <dt>

[Arbeiten mit Katalogen](ribbon-controls-galleries.md)
</dt> </dl>

 

 





