---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: ba62f902-9bc9-4492-ab53-4a4ddbc23530
title: "\"Pgeblackgenerationprocessinggraycomponentreplacementextent\""
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58c71700b23459c087361e9e28ac0c43120aff90
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "103869656"
---
# <a name="pageblackgenerationprocessinggraycomponentreplacementextent"></a>"Pgeblackgenerationprocessinggraycomponentreplacementextent"

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Beschreibt die übergeordneten Objekte (in den Farben), für die GCR gilt. 0% = Uniform Component Replace, 100% = graue Komponenten Ersetzung.

-   [Elementinformationen](#element-information)
-   [Strukturieren von Inhalt](#structure-content)

## <a name="element-information"></a>Elementinformationen



| Name                       |                                                            |
|----------------------------|------------------------------------------------------------|
| Elementtyp <br/>   | ParameterDef<br/>                                    |
| Bereichs Präfix <br/> | Seite<br/>                                            |
| Notizen <br/>          | Verknüpft mit dem Element "pgeblackgenerationprocessing"<br/> |



 

## <a name="structure-content"></a>Strukturieren von Inhalt

Die XML-Struktur dieses Elements lautet:

``` syntax
<psf:ParameterDef name="psk:PageBlackGenerationProcessingGrayComponentReplacementExtent">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">100</psf:Value>
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
    <psf:Value xsi:type="xs:string">percent</psf:Value>
  </psf:Property>
</psf:ParameterDef>
```

## <a name="structure-properties"></a>Struktur Eigenschaften

In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.



| Eigenschaft                | xsi:type           | Wert                      |
|-------------------------|--------------------|----------------------------|
| DataType<br/>     | Zeichenfolge<br/>  | xs:integer<br/>      |
| DefaultValue<br/> | Zeichenfolge<br/>  | nicht definiert<br/>       |
| MaxValue<br/>     | integer<br/> | 100<br/>             |
| MinValue<br/>     | integer<br/> | 0<br/>               |
| Mehrere<br/>     | integer<br/> | 1<br/>               |
| Obligatorisch.<br/>    | Zeichenfolge<br/>  | PSK: bedingt<br/> |
| UnitType<br/>     | Zeichenfolge<br/>  | Prozent<br/>         |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Druck Schema Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




