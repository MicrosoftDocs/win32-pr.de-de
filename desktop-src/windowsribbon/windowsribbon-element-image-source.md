---
title: Image. Source (Eigenschaft)
description: Stellt den Verzeichnispfad eines Bilds dar.
ms.assetid: 174a518a-e9a3-4461-a9a3-d61b62d2b718
keywords:
- Bild. Quell Eigenschaft (Windows-Menüband)
topic_type:
- apiref
api_name:
- Image.Source
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ace2a907280a11c54452b54bfb6172539980e38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741000"
---
# <a name="imagesource-property"></a>Image. Source (Eigenschaft)

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



## <a name="remarks"></a>Bemerkungen

Dies ist optional.

Kann höchstens einmal für jedes [**Image**](windowsribbon-element-image.md)auftreten.

Dieses Element enthält einen Wert vom Typ *xs: anyURI* oder eine beliebige Sequenz von Zeichen, die einen Uniform Resource Identifier (URI) darstellt. Der URI-Wert ist eine absolute oder relative (für den Menü Band Markup Datei) Verzeichnispfad einer Bildressource des Typs Bitmap (BMP).

## <a name="examples"></a>Beispiele

Das folgende Codebeispiel zeigt das Markup, das zum Deklarieren von über einen Satz von [**Bild**](windowsribbon-element-image.md) Elementen erforderlich ist, eine Auflistung von Bild Ressourcen, die für die Unterstützung von vier bestimmten Bildschirm DPI-Einstellungen entworfen wurden. Die **Image. Source** -Eigenschaft wird verwendet, um den Pfad zur Bildressource anzugeben.


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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/> |



 

 





