---
description: Abrufen von Informationen zum PageMediaSizePSHeight-Parameter. Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification (Spezifikation des Druckschemas).
ms.assetid: 857caf51-ccf6-415c-aab3-1fed50fa7b34
title: PageMediaSizePSHeight
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53af9494fe895c16fd884e06991b3072f320261e6a47d5fd7f2f06e029bff2d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117868205"
---
# <a name="pagemediasizepsheight"></a>PageMediaSizePSHeight

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

Gibt die Höhe der Seite parallel zur Ausrichtungsrichtung des Feeds an (Referenz PostScript Spezifikation für das Format der [Druckerbeschreibungsdatei).](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)

-   [Elementinformationen](#element-information)
-   [Strukturieren von Inhalt](#structure-content)

## <a name="element-information"></a>Elementinformationen



| Name | Wert |
|----------------------------|-------------------------------------------------------------|
| Elementtyp <br/>   | ParameterDef<br/>                                     |
| Bereichspräfix <br/> | Seite<br/>                                             |
| Hinweise <br/>          | Mit PageMediaSize-Element verknüpft, CustomPS-Option<br/> |



 

## <a name="structure-content"></a>Strukturieren von Inhalt

Die XML-Struktur dieses Elements lautet:

``` syntax
<psf:ParameterDef name="psk:PageMediaSizePSHeight">
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

[PostScript Spezifikation des Druckerbeschreibungsdateiformats](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)
</dt> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




