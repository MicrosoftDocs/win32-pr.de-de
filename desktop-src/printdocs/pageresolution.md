---
description: Erfahren Sie mehr über das vom Benutzer konfigurierbare PageResolution-Element. Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification (Spezifikation des Druckschemas).
ms.assetid: 88f9a9a3-520e-4044-9ab2-961de03878fa
title: Pageresolution
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c7f8768c7edbdb650e068734302add4dfa843b8b16db404bea5fbc50cb37e9e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112290"
---
# <a name="pageresolution"></a>Pageresolution

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

Definiert die Seitenauflösung der Druckerausgabe durch einen qualitativen Wert, durch einen DPI-Wert (Dots per Inch, Punkte pro Zoll) oder durch beide Angaben.

-   [Elementinformationen](#element-information)
-   [Strukturell](#structural-content)
-   [Extensible Markup Language -Inhalt (XML)](#extensible-markup-language-xml-content)

## <a name="element-information"></a>Elementinformationen



| Name | Wert |
|----------------------------|--------------------|
| Elementtyp <br/>   | Komponente<br/> |
| Bereichspräfix <br/> | Seite<br/>    |
| Hinweise <br/>          | Keine<br/>    |



 

## <a name="structural-content"></a>Strukturell

Die XML-Struktur dieses Elements lautet:

``` syntax
<psf:Feature name="psk:PageResolution">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:ResolutionX">
      <psf:Value xsi:type="xs:integer">_ResolutionXValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:ResolutionY">
      <psf:Value xsi:type="xs:integer">_ResolutionYValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:QualitativeResolution">
      <psf:Value xsi:type="xs:string">_QualitativeResolutionValue_</psf:Value>
    </psf:ScoredProperty> 
  </psf:Option>
</psf:Feature>      
```

## <a name="structure-variables"></a>Strukturvariablen

In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.



| Name                                      | Datentyp          | Einheit                  | Unterstützte Werte                                                                                                                                                                      | Zusammenfassung                                                                                                                                                          |
|-------------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_Optionname\_<br/>                 | Zeichenfolge<br/>  | Buchstaben<br/> | Gültiger vollqualifizierte Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert. Wenn kein Namespace angegeben wird, wird der Standardnamespace angenommen.<br/> | Der Name der Option.<br/>                                                                                                                               |
| \_IdentityOptionValue\_<br/>        | Zeichenfolge<br/>  | –<br/>        | TRUE, FALSE<br/>                                                                                                                                                               | Definiert eine Option, die diese Funktion deaktiviert, wenn sie ausgewählt wird.<br/>                                                                                     |
| \_ResolutionXValue\_<br/>           | integer<br/> | DPI<br/>        | Größer 0<br/>                                                                                                                                                            | Gibt die x-Komponente der Auflösung relativ zu PageImageableSize in DPI (relativ zur PageMediaSize- und Feedrichtung des Mediums) an.<br/> |
| \_ResolutionYValue\_<br/>           | integer<br/> | DPI<br/>        | Größer 0<br/>                                                                                                                                                            | Gibt die y-Komponente der Auflösung relativ zum PageImageableSize in DPI (relativ zur PageMediaSize- und Feedrichtung des Mediums) an.<br/> |
| \_QualitativeResolutionValue\_<br/> | Zeichenfolge<br/>  | –<br/>        | Default, Draft, High, Normal, Other.<br/>                                                                                                                                       | Gibt eine Qualitätsbezeichnung für die Auflösung an.<br/>                                                                                                         |



 

## <a name="extensible-markup-language-xml-content"></a>Extensible Markup Language -Inhalt (XML)

Die Schlüsselwörter für das öffentliche Druckschema werden im https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords -Namespace definiert. Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:

``` syntax
<psf:Feature name="psk:PageResolution">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
    <!-- The horizontal resolution in dots per inch -->
    <psf:ScoredProperty name="psk:ResolutionX">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <!-- The vertical resolution in dots per inch -->
    <psf:ScoredProperty name="psk:ResolutionY">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <!-- Value representing the resolution -->
    <psf:ScoredProperty name="psk:QualitativeResolution">
      <psf:Value xsi:type="xs:string">Other</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>    
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




