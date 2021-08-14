---
description: Erfahren Sie mehr über den PageDestinationColorProfileEmbedded-Parameter. Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification (Spezifikation des Druckschemas).
ms.assetid: b360f870-bfaa-4d4d-adce-17fcfc48b6a6
title: PageDestinationColorProfileEmbedded
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f1a66daa2ed8cc4db9cbcc390030dde05b034808f9326fee73f1fe28e3d91cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118732643"
---
# <a name="pagedestinationcolorprofileembedded"></a>PageDestinationColorProfileEmbedded

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

Gibt das eingebettete Zielfarbprofil an.

-   [Elementinformationen](#element-information)
-   [Strukturieren von Inhalt](#structure-content)

## <a name="element-information"></a>Elementinformationen



| Name | Wert |
|----------------------------|----------------------------------------------------------|
| Elementtyp <br/>   | ParameterDef<br/>                                  |
| Bereichspräfix <br/> | Seite<br/>                                          |
| Hinweise <br/>          | Verknüpft mit dem PageDestinationColorProfile-Element<br/> |



 

## <a name="structure-content"></a>Strukturieren von Inhalt

Die XML-Struktur dieses Elements lautet:

``` syntax
<psf:ParameterDef name="psk:PageDestinationColorProfileEmbedded">
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

 

 




