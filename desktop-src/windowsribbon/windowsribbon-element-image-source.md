---
title: Image.Source-Eigenschaft
description: Stellt den Verzeichnispfad eines Bilds dar.
ms.assetid: 174a518a-e9a3-4461-a9a3-d61b62d2b718
keywords:
- Image.Source-Eigenschaft Windows Menüband
topic_type:
- apiref
api_name:
- Image.Source
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20612f0d25f914cb4c80ae77bb001a678af79e4605c3e1358ed7e33f6b19d805
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118202405"
---
# <a name="imagesource-property"></a>Image.Source-Eigenschaft

Stellt den Verzeichnispfad eines Bilds dar.

## <a name="usage"></a>Verbrauch

``` syntax
<Image.Source/>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente

Es gibt keine untergeordneten Elemente.

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                 |
|---------------------------------------------------------|
| [**Image**](windowsribbon-element-image.md)<br/> |



## <a name="remarks"></a>Hinweise

Optional.

Kann höchstens einmal für jedes [**Image**](windowsribbon-element-image.md)auftreten.

Dieses Element enthält einen Wert vom Typ *xs:anyURI* oder eine beliebige Zeichenfolge, die einen Uniform Resource Identifier (URI) darstellt. Der URI-Wert ist ein absoluter oder relativer Verzeichnispfad (zur Menübandmarkupdatei) einer Bildressource vom Typ Bitmap (BMP).

## <a name="examples"></a>Beispiele

Das folgende Codebeispiel zeigt das Markup, das zum Deklarieren einer Sammlung von Bildressourcen durch eine Reihe von [**Bildelementen**](windowsribbon-element-image.md) erforderlich ist, die vier spezifische Bildschirm-DPI-Einstellungen unterstützen. Die **Image.Source-Eigenschaft** wird verwendet, um den Pfad zur Imageressource anzugeben.


```C++
<Command Name="cmdSizeAndColor" Symbol="IDR_CMD_SIZEANDCOLOR">
  <Command.LabelTitle>
    <String Id="250">Size and Color</String>
  </Command.LabelTitle>
  <Command.LargeImages>
    <Image Id="251" MinDPI="96">
      <Image.Source>res/sizeAndColor_96.bmp</Image.Source>
    </Image>
    <Image Id="252" MinDPI="120">
      <Image.Source>res/sizeAndColor_120.bmp</Image.Source>
    </Image>
    <Image Id="253" MinDPI="144">
      <Image.Source>res/sizeAndColor_144.bmp</Image.Source>
    </Image>
    <Image Id="254" MinDPI="192">
      <Image.Source>res/sizeAndColor_192.bmp</Image.Source>
    </Image>
  </Command.LargeImages>
</Command>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/> |



 

 





