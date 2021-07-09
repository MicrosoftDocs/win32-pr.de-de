---
description: Erfahren Sie mehr über das vom Benutzer konfigurierbare PageMirrorImage-Element. Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification (Spezifikation des Druckschemas).
ms.assetid: a05357c0-6a82-42ff-b4f8-d3e0ee089055
title: PageMirrorImage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fe917d6973fbd074111a5da7b6fe5620e7251e9
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549093"
---
# <a name="pagemirrorimage"></a>PageMirrorImage

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

Beschreibt die Spiegelungseinstellung der Ausgabe.

-   [Elementinformationen](#element-information)
-   [Strukturell](#structural-content)
-   [xml-Inhalt (Extensible Markup Language)](#extensible-markup-language-xml-content)

## <a name="element-information"></a>Elementinformationen



| Name | Wert |
|----------------------------|--------------------|
| Elementtyp <br/>   | Funktion<br/> |
| Bereichspräfix <br/> | Seite<br/>    |
| Hinweise <br/>          | Keine<br/>    |



 

## <a name="structural-content"></a>Strukturell

Die XML-Struktur dieses Elements lautet:

``` syntax
<psf:Feature name="psk:PageMirrorImage">
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

In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.



| Name                               | Datentyp         | Einheit                  | Unterstützte Werte                                                                                                                                                                      | Zusammenfassung                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| \_Optionname\_<br/>          | Zeichenfolge<br/> | Buchstaben<br/> | Gültiger vollqualifizierte Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert. Wenn kein Namespace angegeben wird, wird der Standardnamespace angenommen.<br/> | Der Name der Option.<br/>                                           |
| \_IdentityOptionValue\_<br/> | Zeichenfolge<br/> | n/v<br/>        | TRUE, FALSE<br/>                                                                                                                                                               | Definiert eine Option, die diese Funktion deaktiviert, wenn sie ausgewählt wird.<br/> |



 

## <a name="extensible-markup-language-xml-content"></a>xml-Inhalt (Extensible Markup Language)

Die Schlüsselwörter für das öffentliche Druckschema werden im https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords -Namespace definiert. Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:

``` syntax
<psf:Feature name="psk:PageMirrorImage">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies the output should be mirrored parallel to the MediaSizeWidth direction. -->
  <psf:Option name="psk:MirrorImageWidth" />
  <!-- Specifies the output should be mirrored parallel to the MediaSizeHeight direction. -->
  <psf:Option name="psk:MirrorImageHeight" />
  <!-- Specifies the output should not be mirrored. -->
  <psf:Option name="psk:None" />
</psf:Feature>
    
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




