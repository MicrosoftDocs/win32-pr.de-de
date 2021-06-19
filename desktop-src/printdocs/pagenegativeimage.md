---
description: Erfahren Sie mehr über das benutzerkonfigurierbare PageNegativeImage-Element. Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: 4f6ff85c-8cad-4b9b-8a1d-ce41ed7dfbed
title: PageNegativeImage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a1e1a9de2d82135adb82c68f45785ee3763e41a
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395655"
---
# <a name="pagenegativeimage"></a>PageNegativeImage

Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

Beschreibt die negative Einstellung der Ausgabe.

-   [Elementinformationen](#element-information)
-   [Strukturelle Inhalte](#structural-content)
-   [Extensible Markup Language (XML)-Inhalt](#extensible-markup-language-xml-content)

## <a name="element-information"></a>Elementinformationen



| Name | Wert |
|----------------------------|--------------------|
| Elementtyp <br/>   | Funktion<br/> |
| Bereichspräfix <br/> | Seite<br/>    |
| Hinweise <br/>          | Keine<br/>    |



 

## <a name="structural-content"></a>Strukturelle Inhalte

Die XML-Struktur dieses Elements ist:

``` syntax
<psf:Feature name="psk:PageNegativeImage">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a>Strukturvariablen

In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.



| Name                               | Datentyp         | Einheit                  | Unterstützte Werte                                                                                                                                                                      | Zusammenfassung                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| \_Optionname\_<br/>          | Zeichenfolge<br/> | Buchstaben<br/> | Gültiger vollqualifizierter Name, wie durch [Namespaces in XML definiert.](https://www.w3.org/TR/1999/REC-xml-names-19990114/) Wenn kein Namespace angegeben wird, wird der Standardnamespace angenommen.<br/> | Der Name der Option.<br/>                                           |
| \_IdentityOptionValue\_<br/> | Zeichenfolge<br/> | –<br/>        | TRUE, FALSE<br/>                                                                                                                                                               | Definiert eine Option, durch die diese Funktion deaktiviert wird, wenn sie ausgewählt wird.<br/> |



 

## <a name="extensible-markup-language-xml-content"></a>Extensible Markup Language (XML)-Inhalt

Die Schlüsselwörter des öffentlichen Druckschemas werden im -Namespace https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords definiert. Der öffentliche Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:

``` syntax
<psf:Feature name="psk:PageNegativeImage">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies the output should be the negative image. -->
  <psf:Option name="psk:Negative" />
  <!-- Specifies the output should be the non-negative image. -->
  <psf:Option name="psk:None" />
</psf:Feature>
    
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




