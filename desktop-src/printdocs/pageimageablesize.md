---
description: Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: 6b81814f-2d9e-4862-8633-6ba016c11dac
title: PageImageableSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1eef9012a7fda3eed6afd16add1d483c35c1111
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996107"
---
# <a name="pageimageablesize"></a>PageImageableSize

Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

Beschreibt den bildierten Zeichenbereich für Layout und Rendering. Dies wird basierend auf PageMediaSize und PageOrientation gemeldet.

Die folgenden Diagramme veranschaulichen die Verwendung von PageImageableSize-Variablen basierend auf PageOrientation.

![Diagramm, das Seitenmessungen zeigt](images/local-1641910626-image.png)

-   [Elementinformationen](#element-information)
-   [Strukturelle Inhalte](#structural-content)
-   [Extensible Markup Language (XML) Content](#extensible-markup-language-xml-content)

## <a name="element-information"></a>Elementinformationen



|                            |                     |
|----------------------------|---------------------|
| Name | Wert |
| Elementtyp<br/>    | Eigenschaft<br/> |
| Bereichspräfix <br/> | Seite<br/>     |
| Hinweise <br/>          | Keine<br/>     |



 

## <a name="structural-content"></a>Strukturelle Inhalte

Die XML-Struktur dieses Elements ist:

``` syntax
<psf:Property name="psk:PageImageableSize">
  <psf:Property name="psk:ImageableSizeWidth">
    <psf:Value xsi:type="xs:integer">_ImageableSizeWidthValue_</psf:Value>
  </psf:Property>
  <psf:Property name="psk:ImageableSizeHeight">
    <psf:Value xsi:type="xs:integer">_ImageableSizeHeightValue_</psf:Value>
  </psf:Property>
  <!--Specifies the imageable area within the logical page.  -->
  <psf:Property name="psk:ImageableArea">
    <psf:Property name="psk:OriginWidth">
      <psf:Value xsi:type="xs:integer">_OriginWidthValue_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:OriginHeight">
      <psf:Value xsi:type="xs:integer">_OriginHeightValue_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:ExtentWidth">
      <psf:Value xsi:type="xs:integer">_ExtentWidthValue_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:ExtentHeight">
      <psf:Value xsi:type="xs:integer">_ExtentHeightValue_</psf:Value>
    </psf:Property>
  </psf:Property>
</psf:Property>
```

## <a name="structure-variables"></a>Strukturvariablen

In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.



| Name                                    | Datentyp          | Einheit               | Unterstützte Werte                       | Zusammenfassung                                                                                                                    |
|-----------------------------------------|--------------------|--------------------|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| \_ImageableSizeWidthValue\_<br/>  | integer<br/> | Mikron<br/> | Größer 0<br/>             | Gibt die horizontale Dimension der Anwendungsmediengröße relativ zur PageOrientation an.<br/>               |
| \_ImageableSizeHeightValue\_<br/> | integer<br/> | Mikron<br/> | Größer 0<br/>             | Gibt die vertikale Dimension der Mediengröße der Anwendung relativ zur PageOrientation an.<br/>                 |
| \_OriginWidthValue\_<br/>         | integer<br/> | Mikron<br/> | Größer oder gleich 0.<br/> | Gibt den horizontalen Ursprung des bildbaren Bereichs relativ zur Größe der Anwendungsmedien an.<br/>                   |
| \_OriginHeightValue\_<br/>        | integer<br/> | Mikron<br/> | Größer oder gleich 0.<br/> | Gibt den vertikalen Ursprung des bildbaren Bereichs relativ zur Größe der Anwendungsmedien an.<br/>                     |
| \_ExtentWidthValue\_<br/>         | integer<br/> | Mikron<br/> | Größer 0<br/>             | Gibt den horizontalen Abstand zwischen dem Ursprung und der Begrenzungsgrenze der Größe der Anwendungsmedien an.<br/>      |
| \_ExtentHeightValue\_<br/>        | integer<br/> | Mikron<br/> | Größer 0<br/>             | Gibt den vertikalen Abstand zwischen dem Ursprung und der Begrenzungsgrenze der Mediengröße der Canvasanwendung an.<br/> |



 

## <a name="extensible-markup-language-xml-content"></a>Extensible Markup Language -Inhalt (XML)

Die Schlüsselwörter für das öffentliche Druckschema werden im https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords -Namespace definiert. Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:

``` syntax
<psf:Property name="psk:PageImageableSize">
  <psf:Property name="psk:ImageableSizeWidth">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psk:ImageableSizeHeight">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
    <psf:Property name="psk:ImageableArea">
      <psf:Property name="psk:OriginWidth">
        <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
      </psf:Property>
    <psf:Property name="psk:OriginHeight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:ExtentWidth">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:ExtentHeight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:Property>
  </psf:Property>
</psf:Property>
  
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




