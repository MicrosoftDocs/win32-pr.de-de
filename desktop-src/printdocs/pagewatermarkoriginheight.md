---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: ef429727-d881-408b-95ce-2acce667654a
title: "\"Pgewatermarkoriginheight\""
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1d3e12591f6c648e6e636e1bb72f4df694d0d13
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "103961263"
---
# <a name="pagewatermarkoriginheight"></a>"Pgewatermarkoriginheight"

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Gibt den Ursprung eines Wasserzeichens relativ zum Ursprung von PageImageableSize an.

-   [Elementinformationen](#element-information)
-   [Strukturieren von Inhalt](#structure-content)

## <a name="element-information"></a>Elementinformationen



| Name                       |                                            |
|----------------------------|--------------------------------------------|
| Elementtyp <br/>   | ParameterDef<br/>                    |
| Bereichs Präfix <br/> | Seite<br/>                            |
| Notizen <br/>          | Mit dem Element "pgewatermark" verknüpft<br/> |



 

## <a name="structure-content"></a>Strukturieren von Inhalt

Die XML-Struktur dieses Elements lautet wie folgt:

``` syntax
<psf:ParameterDef name="psk:PageWatermarkOriginHeight">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
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
    <psf:Value xsi:type="xs:string">microns</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a>Struktur Eigenschaften

In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.



| Eigenschaft                | xsi:type           | Wert                                                                   |
|-------------------------|--------------------|-------------------------------------------------------------------------|
| DataType<br/>     | Zeichenfolge<br/>  | xs:integer<br/>                                                   |
| DefaultValue<br/> | integer<br/> | nicht definiert<br/>                                                    |
| MaxValue<br/>     | integer<br/> | Kleiner oder gleich dem PageImageableSize-ExtentHeight-Wert<br/> |
| MinValue<br/>     | integer<br/> | 0<br/>                                                            |
| Mehrere<br/>     | integer<br/> | 1<br/>                                                            |
| Obligatorisch.<br/>    | Zeichenfolge<br/>  | PSK: bedingt<br/>                                              |
| UnitType<br/>     | Zeichenfolge<br/>  | Mikrometern<br/>                                                      |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Druck Schema Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




