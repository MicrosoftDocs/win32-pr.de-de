---
title: Image-Element (Windows-Menüband-Framework)
description: Stellt ein Bild dar.
ms.assetid: 2c71bb16-93ac-484f-b81b-1b95842472b3
keywords:
- Windows-Menüband für Bildelement
topic_type:
- apiref
api_name:
- Image
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1d33f6710da2261a359aa7fd0a3b493871155cf4
ms.sourcegitcommit: 40a1246849dba8ececf54c716b2794b99c96ad50
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/12/2019
ms.locfileid: "104101050"
---
# <a name="image-element"></a>Image-Element

Stellt ein Bild dar.

## <a name="usage"></a>Verbrauch

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
<th>Attribut</th>
<th>type</th>
<th>Erforderlich</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Id</strong><br/></td>
<td>xs: positivan teger Union xs: String<br/></td>
<td>Nein<br/></td>
<td>Die eindeutige Ressourcen-ID. <br/> <br/>
<dt><span></span><span></span><strong></strong> (Die Vereinigung von xs: positiveingeteger und xs: String)<br/> </dt> <dd> Ein ganzzahliger Wert zwischen 2 und 59999, einschließlich, oder 0x2 und 0xea5f in Hexadezimal (einschließlich). <br/> Die maximale Länge beträgt 10 Zeichen, einschließlich optionaler führender Nullen. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Mindpi</strong><br/></td>
<td>xs:positiveInteger<br/></td>
<td>Nein<br/></td>
<td><dt><span></span><span></span><strong></strong> (xs: positivin teger)<br/> </dt> <dd> Eine beliebige Sequenz von Ziffern mit einem Minimalwert von 96. <br/> Wenn mindpi weggelassen wird, ist der Standardwert 96. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>Quelle</strong><br/></td>
<td>xs:anyURI<br/></td>
<td>Nein<br/></td>
<td><dt><span></span><span></span><strong></strong> (xs: anyURI)<br/> </dt> <dd> Eine beliebige Sequenz von Zeichen, die einen URI darstellt. Der URI-Wert ist eine absolute oder relative (für den Menüband-Markup Datei) Pfad zu einer Bildressource des Typs BMP. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Symbol</strong><br/></td>
<td>xs:string<br/></td>
<td>Nein<br/></td>
<td>Das Ressourcen Symbol für das Bild.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: String)<br/> </dt> <dd> Eine Zeichenfolge, die aus einem Buchstaben oder einem Unterstrich gefolgt von einer beliebigen Folge von Buchstaben, Ziffern oder unterstrichen mit maximal 100 Zeichen besteht. <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                               | BESCHREIBUNG                                   |
|-----------------------------------------------------------------------|-----------------------------------------------|
| [**Image. Source**](windowsribbon-element-image-source.md)<br/> | Kann höchstens einmal vorkommen<br/> <br/> |



## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                                                                     |
|-------------------------------------------------------------------------------------------------------------|
| [**Command. largehighkontra stimages**](windowsribbon-element-command-largehighcontrastimages.md)<br/> |
| [**Command. largeimages**](windowsribbon-element-command-largeimages.md)<br/>                         |
| [**Command. smallhighkontra stimages**](windowsribbon-element-command-smallhighcontrastimages.md)<br/> |
| [**Command. smallimages**](windowsribbon-element-command-smallimages.md)<br/>                         |



## <a name="remarks"></a>Bemerkungen

Dies ist optional.

Kann für jeden Befehl einmal oder mehrmals vorkommen [**. smallimages**](windowsribbon-element-command-smallimages.md), [**Command. smallhighkontra stimages**](windowsribbon-element-command-smallhighcontrastimages.md), [**Command. largeimages**](windowsribbon-element-command-largeimages.md)oder [**Command. largehighkontra stimages**](windowsribbon-element-command-largehighcontrastimages.md) .

Wenn eine Auflistung von Bild Ressourcen, die für die Unterstützung bestimmter Bildschirmpunkte pro Zoll (dpi) entwickelt wurden, über einen Satz von **Bild** Elementen an das Menüband-Framework übergeben wird, verwendet das Framework das **Bild** mit einem *mindpi* -Attribut Wert, der mit der aktuellen Bildschirm-dpi-Einstellung übereinstimmt.

Wenn kein **Bild** Element mit einem *mindpi* -Wert deklariert wird, der mit der aktuellen Bildschirm dpi-Einstellung übereinstimmt, wählt das Framework das **Bild** aus, das den nächstgelegenen *mindpi* -Wert aufweist, der kleiner ist als die aktuelle Bildschirm dpi-Einstellung, und skaliert die Bildressource Wenn kein **Bild** Element mit einem *mindpi* -Attribut Wert, der kleiner als die aktuelle Bildschirm dpi-Einstellung ist, deklariert ist, wählt das Framework den nächsten *mindpi* -Wert aus, der größer als die aktuelle Bildschirm dpi-Einstellung ist, und skaliert die Bildressource nach unten.

## <a name="examples"></a>Beispiele

Das folgende Codebeispiel zeigt das Markup, das zum Deklarieren von über einen Satz von **Bild** Elementen erforderlich ist, eine Auflistung von Bild Ressourcen, die für die Unterstützung von vier bestimmten Bildschirm DPI-Einstellungen entworfen wurden.


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



|                                     |           |
|-------------------------------------|-----------|
| Unterstützte Mindestversion (System)<br/> | Windows 7 |
| Kann leer bleiben                        | Nein        |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Angeben von Menüband-Bild Ressourcen](windowsribbon-imageformats.md)
</dt> </dl>

 

 





