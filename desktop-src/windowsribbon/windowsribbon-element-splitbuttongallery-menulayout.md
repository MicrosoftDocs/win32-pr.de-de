---
title: SplitButtonGallery.MenuLayout-Eigenschaft
description: Stellt einen Container für Dropdownmenülayouts für den Katalog mit geteilten Schaltflächen dar.
ms.assetid: 4bebdff6-16ea-4cf3-adc7-9b86ea200e81
keywords:
- SplitButtonGallery.MenuLayout-Eigenschaft Windows Menüband
topic_type:
- apiref
api_name:
- SplitButtonGallery.MenuLayout
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f40cf184d6122fc40041cfb77953bba2b7950d9d1a957d99aae659633ee5c194
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118706898"
---
# <a name="splitbuttongallerymenulayout-property"></a>SplitButtonGallery.MenuLayout-Eigenschaft

Stellt einen Container für Dropdownmenülayouts für den Katalog mit [geteilten Schaltflächen](windowsribbon-controls-splitbuttongallery.md) dar.

## <a name="usage"></a>Verbrauch

``` syntax
<SplitButtonGallery.MenuLayout>
  child elements
</SplitButtonGallery.MenuLayout>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                           | Beschreibung                                    |
|-----------------------------------------------------------------------------------|------------------------------------------------|
| [**FlowMenuLayout**](windowsribbon-element-flowmenulayout.md)<br/>         | Muss genau einmal auftreten<br/> <br/> |
| [**VerticalMenuLayout**](windowsribbon-element-verticalmenulayout.md)<br/> | Muss genau einmal auftreten<br/> <br/> |



## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                                           |
|-----------------------------------------------------------------------------------|
| [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a>Hinweise

Optional.

Kann höchstens einmal für jedes [**SplitButtonGallery-Element**](windowsribbon-element-splitbuttongallery.md) auftreten.

> [!Note]  
> Maximal ein untergeordnetes Element ([**VerticalMenuLayout**](windowsribbon-element-verticalmenulayout.md) oder [**FlowMenuLayout**](windowsribbon-element-flowmenulayout.md)) ist zulässig.

 

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird das grundlegende Markup für den Katalog mit geteilten [Schaltflächen](windowsribbon-controls-splitbuttongallery.md)veranschaulicht.

Dieser Codeabschnitt zeigt die **SplitButtonGallery.MenuLayout-Steuerelementdeklaration.**


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
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Steuerelement "Katalog mit geteilten Schaltflächen"](windowsribbon-controls-splitbuttongallery.md)
</dt> <dt>

[Arbeiten mit Katalogen](ribbon-controls-galleries.md)
</dt> </dl>

 

 





