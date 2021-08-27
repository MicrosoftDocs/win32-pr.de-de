---
title: Image-Element (Windows Menübandframework)
description: Stellt ein Bild dar.
ms.assetid: 2c71bb16-93ac-484f-b81b-1b95842472b3
keywords:
- Bildelement Windows Menüband
topic_type:
- apiref
api_name:
- Image
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b05f7c93ea1597d2dde4724ff0b24b53769cd9ea
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122631678"
---
# <a name="image-element"></a>Image-Element

Stellt ein Bild dar.

## <a name="usage"></a>Verwendung

``` syntax
<Image
  Source = "xs:anyURI"
  MinDPI = "xs:positiveInteger"
  Symbol = "xs:string"
  Id = "xs:positiveInteger union xs:string">
  child elements
</Image>
```

## <a name="attributes"></a>Attribute



<table>
<colgroup>
<col  />
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Attribut</th>
<th>Typ</th>
<th>Erforderlich</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Id</strong><br/></td>
<td>xs:positiveInteger union xs:string<br/></td>
<td>Nein<br/></td>
<td>Die eindeutige Ressourcen-ID. <br/> <br/>
<dt><span></span><span></span><strong></strong> (Die Vereinigung von xs:positiveInteger und xs:string)<br/> </dt> <dd> Ein ganzzahliger Wert zwischen 2 und 59999, einschließlich oder 0x2 und 0xea5f in Hexadezimal, einschließlich. <br/> Die maximale Länge beträgt 10 Zeichen, einschließlich optionaler führender Nullen. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>MinDPI</strong><br/></td>
<td>xs:positiveInteger<br/></td>
<td>Nein<br/></td>
<td><dt><span></span><span></span><strong></strong> (xs:positiveInteger)<br/> </dt> <dd> Jede Sequenz von Ziffern mit einem Mindestwert von 96. <br/> Wenn MinDPI ausgelassen wird, ist der Standardwert 96. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>Quelle</strong><br/></td>
<td>xs:anyURI<br/></td>
<td>Nein<br/></td>
<td><dt><span></span><span></span><strong></strong> (xs:anyURI)<br/> </dt> <dd> Jede Zeichensequenz, die einen URI darstellt. Der URI-Wert ist ein absoluter oder relativer Pfad (zur Menüband-Markupdatei) zu einer Bildressource vom Typ BMP. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Symbol</strong><br/></td>
<td>xs:string<br/></td>
<td>Nein<br/></td>
<td>Das Ressourcensymbol für das Bild.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:string)<br/> </dt> <dd> Eine Zeichenfolge, die aus einem Buchstaben oder Unterstrich besteht, gefolgt von einer beliebigen Sequenz von Buchstaben, Ziffern oder Unterstrichen bis zu maximal 100 Zeichen. <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                               | Beschreibung                                   |
|-----------------------------------------------------------------------|-----------------------------------------------|
| [**Image.Source**](windowsribbon-element-image-source.md)<br/> | Kann höchstens einmal auftreten.<br/> <br/> |



## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                                                                     |
|-------------------------------------------------------------------------------------------------------------|
| [**Command.LargeHighContrastImages**](windowsribbon-element-command-largehighcontrastimages.md)<br/> |
| [**Command.LargeImages**](windowsribbon-element-command-largeimages.md)<br/>                         |
| [**Command.SmallHighContrastImages**](windowsribbon-element-command-smallhighcontrastimages.md)<br/> |
| [**Command.SmallImages**](windowsribbon-element-command-smallimages.md)<br/>                         |



## <a name="remarks"></a>Hinweise

Optional.

Kann ein oder mehrere Male für jedes [**Command.SmallImages-,**](windowsribbon-element-command-smallimages.md) [**Command.SmallHighContrastImages-,**](windowsribbon-element-command-smallhighcontrastimages.md) [**Command.LargeImages-**](windowsribbon-element-command-largeimages.md)oder [**Command.LargeHighContrastImages-Element**](windowsribbon-element-command-largehighcontrastimages.md) auftreten.

Wenn eine Sammlung von Bildressourcen, die bestimmte Bildschirmpunkte pro Zoll (dpi) unterstützen sollen, über eine Reihe von **Bildelementen** an das Menübandframework übermittelt wird, verwendet das Framework das **Bild** mit einem *MinDPI-Attributwert,* der der aktuellen Bildschirm-DPI-Einstellung entspricht.

Wenn kein **Image-Element** mit einem *MinDPI-Wert* deklariert wird, der der aktuellen Bildschirm-DPI-Einstellung entspricht, wählt das Framework das **Bild** aus, das den nächsten *MinDPI-Wert* kleiner als die aktuelle Bildschirm-DPI-Einstellung hat, und skaliert die Bildressource nach oben. Wenn kein **Image-Element** mit einem *MinDPI-Attributwert* deklariert wird, der kleiner als die aktuelle Bildschirm-DPI-Einstellung ist, wählt das Framework den nächsten *MinDPI-Wert* aus, der größer als die aktuelle Bildschirm-DPI-Einstellung ist, und skaliert die Bildressource herunter.

## <a name="examples"></a>Beispiele

Das folgende Codebeispiel zeigt das Markup, das zum Deklarieren einer Sammlung von Bildressourcen durch eine Reihe von **Bildelementen** erforderlich ist, die vier spezifische Bildschirm-DPI-Einstellungen unterstützen.


```XML
<Command Name="cmdSizeAndColor" Symbol="IDR_CMD_SIZEANDCOLOR">
  <Command.LabelTitle>
    <String Id="250">Size and Color</String>
  </Command.LabelTitle>
  <Command.LargeImages>
    <Image Id="251" MinDPI="96">res/sizeAndColor_96.bmp</Image>
    <Image Id="252" MinDPI="120">res/sizeAndColor_120.bmp</Image>
    <Image Id="253" MinDPI="144">res/sizeAndColor_144.bmp</Image>
    <Image Id="254" MinDPI="192">res/sizeAndColor_192.bmp</Image>
  </Command.LargeImages>
</Command>
```



## <a name="element-information"></a>Elementinformationen

* **Unterstütztes Mindestsystem:** Windows 7
* **Kann leer sein:** Nein



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[Angeben von Menübandbildressourcen](windowsribbon-imageformats.md)
</dt> </dl>

 

 





