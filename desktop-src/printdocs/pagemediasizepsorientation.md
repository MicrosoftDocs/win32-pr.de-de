---
description: Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification(Spezifikation des Druckschemas).
ms.assetid: b091c250-66f2-47cc-a012-1526c0ed02c9
title: PageMediaSizePSOrientation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d16a9a2e59ebffb41ad7c9a9c16eaf41497ade62
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997557"
---
# <a name="pagemediasizepsorientation"></a>PageMediaSizePSOrientation

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

Gibt die Ausrichtung relativ zur Richtung der Feedausrichtung an (Referenz zur Spezifikation des [PostScript-Druckerbeschreibungsdateiformats).](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)

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

## <a name="structure-properties"></a>Struktureigenschaften

In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.



| Eigenschaft                | xsi:type           | Wert                        |
|-------------------------|--------------------|------------------------------|
| DataType<br/>     | Zeichenfolge<br/>  | xs:integer<br/>        |
| DefaultValue<br/> | integer<br/> | 0<br/>                 |
| MaxValue<br/>     | integer<br/> | 3<br/>                 |
| Minvalue<br/>     | integer<br/> | 0<br/>                 |
| Obligatorisch.<br/>    | Zeichenfolge<br/>  | psk:Conditional<br/>   |
| Mehrere<br/>     | integer<br/> | 1<br/>                 |
| Unittype<br/>     | Zeichenfolge<br/>  | PageMediaSizeEnum<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des PostScript-Druckerbeschreibungsdateiformats](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)
</dt> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




