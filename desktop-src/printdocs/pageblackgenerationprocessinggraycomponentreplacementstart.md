---
description: Erfahren Sie mehr über das PageBlackGenerationProcessingGrayComponentReplacementStart-Element, das den Punkt beschreibt, an dem GCR gestartet werden soll.
ms.assetid: 28ea95a2-e602-4f71-9488-48525e995814
title: PageBlackGenerationProcessingGrayComponentReplacementStart
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3323f3aa910673b5e35d660cf59b9f30fb0380711d053db314167a9f93c3dd3b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112320"
---
# <a name="pageblackgenerationprocessinggraycomponentreplacementstart"></a>PageBlackGenerationProcessingGrayComponentReplacementStart

Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

Beschreibt den Punkt im Bereich "Hervorhebung bis Schatten", an dem GCR beginnen soll (100 % dunkelster Schatten).

-   [Elementinformationen](#element-information)
-   [Strukturieren von Inhalt](#structure-content)

## <a name="element-information"></a>Elementinformationen



| Name | Wert |
|----------------------------|------------------------------------------------------------|
| Elementtyp <br/>   | ParameterDef<br/>                                    |
| Bereichspräfix <br/> | Seite<br/>                                            |
| Hinweise <br/>          | Mit PageBlackGenerationProcessing-Element verknüpft<br/> |



 

## <a name="structure-content"></a>Strukturieren von Inhalt

Die XML-Struktur dieses Elements ist:

``` syntax
<psf:ParameterDef name="psk:PageBlackGenerationProcessingGrayComponentReplacementStart">
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

## <a name="structure-properties"></a>Struktureigenschaften

In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.



| Eigenschaft                | xsi:type           | Wert                      |
|-------------------------|--------------------|----------------------------|
| DataType<br/>     | Zeichenfolge<br/>  | xs:integer<br/>      |
| DefaultValue<br/> | Zeichenfolge<br/>  | nicht definiert<br/>       |
| MaxValue<br/>     | integer<br/> | 100<br/>             |
| Minvalue<br/>     | integer<br/> | 0<br/>               |
| Mehrere<br/>     | integer<br/> | 1<br/>               |
| Obligatorisch.<br/>    | Zeichenfolge<br/>  | psk:Conditional<br/> |
| Unittype<br/>     | Zeichenfolge<br/>  | Prozent<br/>         |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




