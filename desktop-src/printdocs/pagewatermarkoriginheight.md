---
description: Hier finden Sie Informationen zum PageWatermarkOriginHeight-Parameter. Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: ef429727-d881-408b-95ce-2acce667654a
title: PageWatermarkOriginHeight
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d59e9336088d44cef1941df03319519ae69af1c3
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395985"
---
# <a name="pagewatermarkoriginheight"></a>PageWatermarkOriginHeight

Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

Gibt den Ursprung eines Wasserzeichens relativ zum Ursprung von PageImageableSize an.

-   [Elementinformationen](#element-information)
-   [Strukturieren von Inhalt](#structure-content)

## <a name="element-information"></a>Elementinformationen



| Name | Wert |
|----------------------------|--------------------------------------------|
| Elementtyp <br/>   | ParameterDef<br/>                    |
| Bereichspräfix <br/> | Seite<br/>                            |
| Hinweise <br/>          | Mit PageWatermark-Element verknüpft<br/> |



 

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

## <a name="structure-properties"></a>Struktureigenschaften

In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.



| Eigenschaft                | xsi:type           | Wert                                                                   |
|-------------------------|--------------------|-------------------------------------------------------------------------|
| DataType<br/>     | Zeichenfolge<br/>  | xs:integer<br/>                                                   |
| DefaultValue<br/> | integer<br/> | nicht definiert<br/>                                                    |
| MaxValue<br/>     | integer<br/> | Kleiner als oder gleich PageImageableSize– ExtentHeight-Wert<br/> |
| Minvalue<br/>     | integer<br/> | 0<br/>                                                            |
| Mehrere<br/>     | integer<br/> | 1<br/>                                                            |
| Obligatorisch.<br/>    | Zeichenfolge<br/>  | psk:Conditional<br/>                                              |
| Unittype<br/>     | Zeichenfolge<br/>  | Mikron<br/>                                                      |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




