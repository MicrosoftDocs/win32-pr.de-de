---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: edbdd2c7-da04-49fb-a0f8-31a7df88f8ef
title: "\"Pgewatermarktextcolor\""
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be77e76dd1b304a46b2760565a09fe0134d3f0b5
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "104530578"
---
# <a name="pagewatermarktextcolor"></a>"Pgewatermarktextcolor"

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Definiert die sRGB-Farbe für den Wasserzeichen Text. Das Format ist "ARGB: \# aarrggbb".

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
<psf:ParameterDef name="psk:PageWatermarkTextColor">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:string</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxLength">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinLength">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">sRGB</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a>Struktur Eigenschaften

In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.



| Eigenschaft                | xsi:type           | Wert                      |
|-------------------------|--------------------|----------------------------|
| DataType<br/>     | Zeichenfolge<br/>  | xs:string<br/>       |
| DefaultValue<br/> | integer<br/> | nicht definiert<br/>       |
| MaxValue<br/>     | integer<br/> | nicht definiert<br/>       |
| MinValue<br/>     | integer<br/> | nicht definiert<br/>       |
| Obligatorisch.<br/>    | Zeichenfolge<br/>  | PSK: bedingt<br/> |
| UnitType<br/>     | Zeichenfolge<br/>  | sRGB<br/>            |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Druck Schema Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




