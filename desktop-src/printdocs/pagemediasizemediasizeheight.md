---
description: Abrufen von Informationen zum PageMediaSizeMediaSizeHeight-Parameter. Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification (Spezifikation des Druckschemas).
ms.assetid: 209b3024-60cf-47e0-8738-cd7795e38c2a
title: PageMediaSizeMediaSizeHeight
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 547077e7a63d91d6db43e8ebf6225a771bf237d8
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395795"
---
# <a name="pagemediasizemediasizeheight"></a>PageMediaSizeMediaSizeHeight

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

Gibt die MediaSizeHeight-Dimensionsrichtung für die Option Custom MediaSize an.

-   [Elementinformationen](#element-information)
-   [Strukturieren von Inhalt](#structure-content)

## <a name="element-information"></a>Elementinformationen



| Name | Wert |
|----------------------------|-----------------------------------------------------------|
| Elementtyp <br/>   | ParameterDef<br/>                                   |
| Bereichspräfix <br/> | Seite<br/>                                           |
| Hinweise <br/>          | Mit PageMediaSize-Element verknüpft, Option "Benutzerdefiniert"<br/> |



 

## <a name="structure-content"></a>Strukturieren von Inhalt

Die XML-Struktur dieses Elements lautet:

``` syntax
<psf:ParameterDef name="psk:PageMediaSizeMediaSizeHeight">
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
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
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

In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.



| Eigenschaft                | xsi:type           | Wert                      |
|-------------------------|--------------------|----------------------------|
| DataType<br/>     | Zeichenfolge<br/>  | xs:integer<br/>      |
| DefaultValue<br/> | integer<br/> | nicht definiert<br/>       |
| MaxValue<br/>     | integer<br/> | nicht definiert<br/>       |
| Minvalue<br/>     | integer<br/> | nicht definiert<br/>       |
| Obligatorisch.<br/>    | Zeichenfolge<br/>  | psk:Conditional<br/> |
| Mehrere<br/>     | integer<br/> | 1<br/>               |
| Unittype<br/>     | Zeichenfolge<br/>  | Mikron<br/>         |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




