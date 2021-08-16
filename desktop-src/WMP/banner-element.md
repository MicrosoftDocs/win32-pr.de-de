---
title: BANNER-Element
description: Das BANNER-Element definiert eine URL zu einer Grafikdatei, die im Anzeigebereich angezeigt wird.
ms.assetid: 8b4a3369-a687-40a8-b5df-afb0e0518cd1
keywords:
- BANNER-Element Windows Media Player
topic_type:
- apiref
api_name:
- BANNER Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 91b3de50c1360337c1344a1af1a0696361614dbc293390470e7c196e53528a1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135963"
---
# <a name="banner-element"></a>BANNER-Element

Das **BANNER-Element** definiert eine URL zu einer Grafikdatei, die im Anzeigebereich angezeigt wird.

``` syntax
<BANNER
   HREF = "URL"
>
</BANNER>
```

## <a name="attributes"></a>Attribute

**HREF** (erforderlich)

URL zu einer Grafikdatei, die im Anzeigebereich angezeigt wird.

## <a name="parentchild-elements"></a>Übergeordnete/untergeordnete Elemente



| Hierarchy       | Elemente                   |
|-----------------|----------------------------|
| Übergeordnete Elemente | **ASX**, **ENTRY**         |
| Untergeordnete Elemente  | **ABSTRACT**, **MOREINFO** |



 

## <a name="remarks"></a>Hinweise

Dieses Element definiert eine URL zu einer Grafikdatei, die im Windows Media Player unterhalb des Videoinhalts angezeigt wird. Wenn es sich bei dem Medium nur um Audiodaten handelt, wird die Bannergrafik allein angezeigt. Windows Media Player reserviert einen Abstand von 32 Pixeln hoch bis 194 Pixel breit (Bannerleiste) für die Grafik. Wenn die in der URL definierte Grafik kleiner als diese ist, wird sie in ihrer ursprünglichen Größe angezeigt. Wenn die Grafik größer als der reservierte Speicherplatz ist, Windows Media Player das Bild an den Platz zuschneiden.

Sie können ein **ABSTRACT-Element** innerhalb des Bereichs des **BANNER-Elements** verwenden, um Text als QuickInfo anzuzeigen, wenn der Benutzer den Mauszeiger über der Bannergrafik hält. Ein **MOREINFO-Element** innerhalb **eines BANNER-Elements** definiert eine URL, zu der der Benutzer gehört, wenn er auf die Bannergrafik klickt. (Die URL kann ein beliebiger Pfad oder ein beliebiges Protokoll sein, z. B. ein E-Mail-Link, eine HTTP-URL (Hypertext Transfer Protocol) zu einer Website oder sogar ein Microsoft JScript-Befehl.) Wenn der Zeiger über die Grafik bewegt wird, wird die Grafik eingebettet und sieht wie eine Schaltfläche aus.

Ein **BANNER-Element,** das für ein **ASX-Element** definiert ist, wird angezeigt, während alle Clips in der Wiedergabeliste abspielt werden. Ein  BANNER-Element, das in einem **ENTRY-Element** definiert ist, wird nur angezeigt, während dieser Clip abspielt, und überschreibt während dieser Zeit alle Banner, die im übergeordneten **ASX-Element definiert** sind. Sie können angeben, Windows Media Player Speicherplatz für das Banner reserviert, indem Sie das **BANNERBAR-Attribut** des **ASX-Elements** festlegen.

Bannerbilder werden nicht mit DRM-Dateien unterstützt, oder wenn Windows Media Player in eine Webseite eingebettet ist.

## <a name="examples"></a>Beispiele

Im Folgenden finden Sie ein Beispiel für ein **BANNER-Element** ohne untergeordnete Elemente:


```XML
<BANNER HREF="https://sample.microsoft.com/art/banner1.bmp" />
```



Im Folgenden finden Sie ein Beispiel für ein **BANNER-Element,** das **ABSTRACT-** und **MOREINFO-Elemente** enthält.


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
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Windows Referenz zu Medienmetadateielementen**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Referenz zur Medienmetadatei**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





