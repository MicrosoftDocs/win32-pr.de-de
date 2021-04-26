---
description: Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification(Spezifikation des Druckschemas).
ms.assetid: 4cd1b0f8-7f7e-40cc-8d19-d44187822cd1
title: DocumentPageRanges
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84ded7c18fc781fd4374feb8958a98b845d95546
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997177"
---
# <a name="documentpageranges"></a>DocumentPageRanges

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

Beschreibt den Ausgabebereich des Dokuments auf Seiten. Der Parameterwert muss der folgenden Struktur entsprechen:

-   PageRangeText: "*PageRange*" oder "*PageRange*,*PageRange*"

-   PageRange: "*PageNumber*" oder "*PageNumber* - *PageNumber*"

-   PageNumber: 1 bis N, wobei N die Anzahl der Seiten im Dokument ist. Wenn *PageNumber* > N, dann *PageNumber* = N.

Leerzeichen in der Zeichenfolge sollten ignoriert werden.

-   [Elementinformationen](#element-information)
-   [Strukturell](#structural-content)

## <a name="element-information"></a>Elementinformationen



| Name | Wert |
|----------------------------|-------------------------|
| Elementtyp <br/>   | ParameterDef<br/> |
| Bereichspräfix <br/> | Dokument<br/>     |
| Hinweise <br/>          | Keine<br/>         |



 

## <a name="structural-content"></a>Strukturell

Die XML-Struktur dieses Elements lautet:

``` syntax
<psf:ParameterDef name="psk:DocumentPageRanges">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:string</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxLength">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinLength">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">characters</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a>Struktureigenschaften

In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.



| Eigenschaft                | xsi:type           | Wert                      |
|-------------------------|--------------------|----------------------------|
| DataType<br/>     | Zeichenfolge<br/>  | xs:string<br/>       |
| DefaultValue<br/> | Zeichenfolge<br/>  | nicht definiert<br/>       |
| MaxLength<br/>    | integer<br/> | nicht definiert<br/>       |
| Minlength<br/>    | integer<br/> | 1<br/>               |
| Obligatorisch.<br/>    | Zeichenfolge<br/>  | psk:Conditional<br/> |
| Unittype<br/>     | Zeichenfolge<br/>  | Buchstaben<br/>      |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




