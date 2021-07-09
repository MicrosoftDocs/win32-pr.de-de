---
description: Erfahren Sie mehr über das benutzerkonfigurierbare PageMediaColor-Element. Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: 3e0e2cb2-cb51-446d-a6ff-f76aa8c305f6
title: PageMediaColor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3041c8954048f60f52e9324f0c6565396d7fafe2
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549158"
---
# <a name="pagemediacolor"></a>PageMediaColor

Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

Beschreibt die Medienfarboptionen und die Merkmale der einzelnen Optionen.

-   [Elementinformationen](#element-information)
-   [Strukturelle Inhalte](#structural-content)
-   [Extensible Markup Language (XML) Content](#extensible-markup-language-xml-content)

## <a name="element-information"></a>Elementinformationen



| Name | Wert |
|----------------------------|--------------------|
| Elementtyp <br/>   | Funktion<br/> |
| Bereichspräfix <br/> | Seite<br/>    |
| Hinweise <br/>          | Keine<br/>    |



 

## <a name="structural-content"></a>Strukturelle Inhalte

Die XML-Struktur dieses Elements ist:

``` syntax
<psf:Feature name="psk:PageMediaColor">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">_MediaColorsRGBValue_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a>Strukturvariablen

In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.



| Name                               | Datentyp         | Einheit                  | Unterstützte Werte                                                                                                                                                                      | Zusammenfassung                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| \_Optionname\_<br/>          | Zeichenfolge<br/> | Buchstaben<br/> | Gültiger vollqualifizierter Name, wie durch [Namespaces in XML definiert.](https://www.w3.org/TR/1999/REC-xml-names-19990114/) Wenn kein Namespace angegeben wird, wird der Standardnamespace angenommen.<br/> | Der Name der Option.<br/>                                           |
| \_IdentityOptionValue\_<br/> | Zeichenfolge<br/> | n/v<br/>        | TRUE, FALSE<br/>                                                                                                                                                               | Definiert eine Option, durch die diese Funktion deaktiviert wird, wenn sie ausgewählt wird.<br/> |
| \_MediaColorsRGBValue\_<br/> | Zeichenfolge<br/> | sRGB-Farbe<br/> | \#AARRGGBB, wobei A, R, G, B Hexadezimalziffern darstellen.<br/>                                                                                                                  | Definiert die sRGB-Farbe für das physische Medienblatt. <br/>             |



 

## <a name="extensible-markup-language-xml-content"></a>Extensible Markup Language (XML) Content

Die Schlüsselwörter des öffentlichen Druckschemas werden im -Namespace `https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords` definiert. Der öffentliche Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:

``` syntax
<psf:Feature name="psk:PageMediaColor">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:Black">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FF000000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Blue">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FF0000FF</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Brown">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFA52A2A</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Gold">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFFFD700</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:GoldenRod">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFDAA520</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Gray">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FF808080</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Green">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FF008000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Ivory">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFFFFFF0</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NoColor">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Orange">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFFFA500</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Pink">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFFFC0CB</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Red">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFFF0000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Silver">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFC0C0C0</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Turquoise">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FF40E0D0</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Violet">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFEE82EE</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:White">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFFFFFFF</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Yellow">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFFFFF00</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a custom page color. -->
  <psf:Option name="psk:Custom">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>
