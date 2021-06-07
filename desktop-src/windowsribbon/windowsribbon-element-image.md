---
title: Image-Element (Windows Ribbon Framework)
description: Stellt ein Bild dar.
ms.assetid: 2c71bb16-93ac-484f-b81b-1b95842472b3
keywords:
- Bildelement Windows-Menüband
topic_type:
- apiref
api_name:
- Image
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fe0b9afb51697d50de9cb80886cf829b90c81262
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111442891"
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
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>attribute</th>
<th>Typ</th>
<th>Erforderlich</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Id</strong><br/></td>
<td>xs:positiveInteger union xs:string<br/></td>
<td>Nein<br/></td>
<td>Die eindeutige Ressourcen-ID. <br/> <br/>
<dt><span></span><span></span><strong></strong> (Die Vereinigung von xs:positiveInteger und xs:string)<br/> </dt> <dd> Ein ganzzahliger Wert zwischen 2 und 59999, einschließlich oder 0x2 und 0xea5f hexadezimal, einschließlich. <br/> Die maximale Länge beträgt 10 Zeichen, einschließlich optionaler führender Nullen. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>MinDPI</strong><br/></td>
<td>xs:positiveInteger<br/></td>
<td>Nein<br/></td>
<td><dt><span></span><span></span><strong></strong> (xs:positiveInteger)<br/> </dt> <dd> Eine beliebige Sequenz von Ziffern mit einem Mindestwert von 96. <br/> Wenn MinDPI weggelassen wird, ist der Standardwert 96. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>Quelle</strong><br/></td>
<td>xs:anyURI<br/></td>
<td>Nein<br/></td>
<td><dt><span></span><span></span><strong></strong> (xs:anyURI)<br/> </dt> <dd> Jede Sequenz von Zeichen, die einen URI darstellt. Der URI-Wert ist ein absoluter oder relativer Pfad (zur Menübandmarkupdatei) zu einer Bildressource vom Typ BMP. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Symbol</strong><br/></td>
<td>xs:string<br/></td>
<td>Nein<br/></td>
<td>Das Ressourcensymbol für das Bild.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:string)<br/> </dt> <dd> Eine Zeichenfolge, die aus einem Buchstaben oder Unterstrich gefolgt von einer beliebigen Folge von Buchstaben, Ziffern oder Unterstrichen bis zu maximal 100 Zeichen besteht. <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                               | BESCHREIBUNG                                   |
|-----------------------------------------------------------------------|-----------------------------------------------|
| [**Image.Source**](windowsribbon-element-image-source.md)<br/> | Kann nur einmal auftreten.<br/> <br/> |



## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                                                                     |
|-------------------------------------------------------------------------------------------------------------|
| [**Command.LargeHighContrastImages**](windowsribbon-element-command-largehighcontrastimages.md)<br/> |
| [**Command.LargeImages**](windowsribbon-element-command-largeimages.md)<br/>                         |
| [**Command.SmallHighContrastImages**](windowsribbon-element-command-smallhighcontrastimages.md)<br/> |
| [**Command.SmallImages**](windowsribbon-element-command-smallimages.md)<br/>                         |



## <a name="remarks"></a>Hinweise

Dies ist optional.

Kann ein oder mehrere Male für jedes [**Command.SmallImages-,**](windowsribbon-element-command-smallimages.md) [**Command.SmallHighContrastImages-,**](windowsribbon-element-command-smallhighcontrastimages.md) [**Command.LargeImages-**](windowsribbon-element-command-largeimages.md)oder [**Command.LargeHighContrastImages-Element**](windowsribbon-element-command-largehighcontrastimages.md) auftreten.

Wenn eine Sammlung von Bildressourcen, die für die Unterstützung bestimmter DPI-Einstellungen (Screen Dots per Inch) entworfen  wurden, für das Menübandframework über eine Reihe von **Image-Elementen** bereitgestellt wird, verwendet das Framework das Image mit einem *MinDPI-Attributwert,* der der aktuellen DPI-Einstellung des Bildschirms entspricht.

Wenn kein **Image-Element** mit einem *MinDPI-Wert* deklariert wird, der der  aktuellen DPI-Einstellung des Bildschirms entspricht, wählt das Framework das Bild aus, das den nächstgelegenen *MinDPI-Wert* kleiner als die aktuelle DPI-Einstellung des Bildschirms hat, und skaliert die Bildressource hoch. Wenn andernfalls kein **Image-Element** mit einem *MinDPI-Attributwert* deklariert wird, der kleiner als die aktuelle DPI-Einstellung des Bildschirms ist, wählt das Framework den nächsten *MinDPI-Wert* aus, der größer als die aktuelle DPI-Einstellung des Bildschirms ist, und skaliert die Bildressource herunter.

## <a name="examples"></a>Beispiele

Das folgende Codebeispiel zeigt das Markup, das erforderlich ist, um über einen Satz von **Image-Elementen** eine Sammlung von Bildressourcen zu deklarieren, die zur Unterstützung von vier spezifischen DPI-Bildschirmeinstellungen entwickelt wurden.


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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Angeben von Menübandbildressourcen](windowsribbon-imageformats.md)
</dt> </dl>

 

 





