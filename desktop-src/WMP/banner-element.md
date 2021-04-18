---
title: Banner-Element
description: Das Banner Element definiert eine URL zu einer Grafikdatei, die im Anzeigebereich angezeigt wird.
ms.assetid: 8b4a3369-a687-40a8-b5df-afb0e0518cd1
keywords:
- Banner Element Windows Media Player
topic_type:
- apiref
api_name:
- BANNER Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8e257c14e5908482cdf8de458c259bc64a55c6d5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354705"
---
# <a name="banner-element"></a>Banner-Element

Das **Banner** Element definiert eine URL zu einer Grafikdatei, die im Anzeigebereich angezeigt wird.

``` syntax
<BANNER
   HREF = "URL"
>
</BANNER>
```

## <a name="attributes"></a>Attribute

**Href** (erforderlich)

URL zu einer Grafikdatei, die im Anzeigebereich angezeigt wird.

## <a name="parentchild-elements"></a>Über-/unterordnungselemente



| Hierarchy       | Elemente                   |
|-----------------|----------------------------|
| Übergeordnete Elemente | **ASX**, **Eintrag**         |
| Untergeordnete Elemente  | **abstract**, **moreingefo** |



 

## <a name="remarks"></a>Bemerkungen

Dieses Element definiert eine URL zu einer Grafikdatei, die im Windows-Media Player Anzeigebereich unterhalb des Video Inhalts angezeigt wird. Wenn das Medium nur Audiodaten ist, wird die Banner Grafik eigenständig angezeigt. Windows Media Player reserviert einen Bereich von 32 Pixel, der um 194 Pixel breit (die Banner Leiste) für die Grafik ist. Wenn die in der URL definierte Grafik kleiner als diese ist, wird Sie in ihrer ursprünglichen Größe angezeigt. Wenn die Grafik größer als der reservierte Platz ist, wird das Bild von Windows Media Player an den Platz angepasst.

Sie können ein **abstraktes** Element innerhalb des Gültigkeits Bereichs des **Banner** Elements verwenden, um Text als QuickInfo anzuzeigen, wenn der Benutzer den Mauszeiger über die Banner Grafik hält. Ein **Moran FO** -Element innerhalb eines **Banner** Elements definiert eine URL, auf die der Benutzer klickt, wenn der Benutzer auf die Banner Grafik klickt. (Die URL kann ein beliebiger Pfad oder Protokoll sein, z. b. ein e-Mail-Link, eine HTTP-URL (Hypertext Transfer Protocol) zu einer Website oder sogar ein Microsoft JScript-Befehl.) Wenn der Zeiger über die Grafik bewegt wird, wird die Grafik als geprägt und sieht wie eine Schaltfläche aus.

Ein für ein **ASX** -Element definiertes **Banner** Element wird angezeigt, während alle Clips in der Wiedergabeliste abgespielt werden. Ein **Banner** Element, das in einem **Entry** -Element definiert ist, wird nur angezeigt, während dieser Clip wiedergegeben wird, und während dieser Zeit überschreibt jedes Banner, das im übergeordneten **ASX** -Element definiert Sie können angeben, wie Windows Media Player Speicherplatz für das Banner reserviert, indem Sie das **bannerbar** -Attribut des **ASX** -Elements festlegen.

Banner Bilder werden bei DRM-Dateien nicht unterstützt, oder wenn Windows Media Player in eine Webseite eingebettet ist.

## <a name="examples"></a>Beispiele

Im folgenden finden Sie ein Beispiel für ein **Banner** Element ohne untergeordnete Elemente:


```XML
<BANNER HREF="https://sample.microsoft.com/art/banner1.bmp" />
```



Im folgenden finden Sie ein Beispiel für ein **Banner** -Element, das **abstrakte** und **morumfo** -Elemente enthält.


```XML
<BANNER HREF="https://www.proseware.com/logos/banner1.bmp">
    <ABSTRACT>Click here to go to our website.</ABSTRACT>
    <MOREINFO HREF="https://sample.microsoft.com" />
    <!-- The text in the Abstract element displays as a 
         ToolTip when the mouse hovers over the banner 
         graphic. When a user clicks the banner, the URL 
         given in the MoreInfo element opens in the 
         browser. -->
</BANNER>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Verweis auf Windows Media-Metadateielemente**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Referenz zu Windows Media-Metadateien**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





