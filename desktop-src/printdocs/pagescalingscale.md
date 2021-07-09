---
description: Hier finden Sie Informationen zum PageScalingScale-Parameter. Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: 49a60a94-fb65-4439-bebf-3f77ea0861fe
title: PageScalingScale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8c6cee5fc46568e3cf7f15ecd43c07c6584c856
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548828"
---
# <a name="pagescalingscale"></a>PageScalingScale

Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

Gibt den Skalierungsfaktor für die benutzerdefinierte quadratische Skalierung an.

-   [Elementinformationen](#element-information)
-   [Strukturieren von Inhalt](#structure-content)

## <a name="element-information"></a>Elementinformationen



| Name | Wert |
|----------------------------|---------------------------------------------------------|
| Elementtyp <br/>   | ParameterDef<br/>                                 |
| Bereichspräfix <br/> | Seite<br/>                                         |
| Hinweise <br/>          | Mit PageScaling-Element verknüpft, Option "Benutzerdefiniert"<br/> |



 

## <a name="structure-content"></a>Strukturieren von Inhalt

Die XML-Struktur dieses Elements ist:

``` syntax
<psf:ParameterDef name="psk:PageScalingScale">
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
    <psf:Value xsi:type="xs:integer">1</psf:Value>
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
| DefaultValue<br/> | integer<br/> | nicht definiert<br/>       |
| MaxValue<br/>     | integer<br/> | nicht definiert<br/>       |
| Minvalue<br/>     | integer<br/> | 1<br/>               |
| Obligatorisch.<br/>    | Zeichenfolge<br/>  | psk:Conditional<br/> |
| Mehrere<br/>     | integer<br/> | 1<br/>               |
| Unittype<br/>     | Zeichenfolge<br/>  | Prozent<br/>         |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




