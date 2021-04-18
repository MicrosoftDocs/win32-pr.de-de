---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: b091c250-66f2-47cc-a012-1526c0ed02c9
title: Pagemediasizepsorientation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a188c61d3bb3c47286b887406174a3fc41f3c58a
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106365008"
---
# <a name="pagemediasizepsorientation"></a>Pagemediasizepsorientation

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Gibt die Ausrichtung in Relation zur Richtung der Feed-Ausrichtung an (Reference [PostScript Printer Description File Format Specification](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).

-   [Elementinformationen](#element-information)
-   [Strukturieren von Inhalt](#structure-content)

## <a name="element-information"></a>Elementinformationen



| Name                       |                                                             |
|----------------------------|-------------------------------------------------------------|
| Elementtyp <br/>   | ParameterDef<br/>                                     |
| Bereichs Präfix <br/> | Seite<br/>                                             |
| Notizen <br/>          | Verknüpft mit PageMediaSize-Element, customps-Option<br/> |



 

## <a name="structure-content"></a>Strukturieren von Inhalt

Die XML-Struktur dieses Elements lautet:

``` syntax
<psf:ParameterDef name="psk:PageMediaSizePSOrientation">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">0</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">3</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">0</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">PageMediaSizeEnum</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a>Struktur Eigenschaften

In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.



| Eigenschaft                | xsi:type           | Wert                        |
|-------------------------|--------------------|------------------------------|
| DataType<br/>     | Zeichenfolge<br/>  | xs:integer<br/>        |
| DefaultValue<br/> | integer<br/> | 0<br/>                 |
| MaxValue<br/>     | integer<br/> | 3<br/>                 |
| MinValue<br/>     | integer<br/> | 0<br/>                 |
| Obligatorisch.<br/>    | Zeichenfolge<br/>  | PSK: bedingt<br/>   |
| Mehrere<br/>     | integer<br/> | 1<br/>                 |
| UnitType<br/>     | Zeichenfolge<br/>  | Pagemediasizeaufumum<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Datei Format Spezifikation für PostScript-Drucker Beschreibung](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)
</dt> <dt>

[Druck Schema Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




