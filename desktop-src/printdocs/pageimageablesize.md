---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 6b81814f-2d9e-4862-8633-6ba016c11dac
title: PageImageableSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26dca243defc08b43a79e897bfa91913a954bf37
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "104560731"
---
# <a name="pageimageablesize"></a>PageImageableSize

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Beschreibt das Abbild Canvas für Layout und Rendering. Dies wird auf der Grundlage von PageMediaSize und PageOrientation gemeldet.

Die folgenden Diagramme veranschaulichen die Verwendung der PageImageableSize-Variablen auf der Grundlage von PageOrientation.

![ein Diagramm, das Seiten Messungen anzeigt](images/local-1641910626-image.png)

-   [Elementinformationen](#element-information)
-   [Strukturelle Inhalte](#structural-content)
-   [Inhalt der Extensible Markup Language (XML)](#extensible-markup-language-xml-content)

## <a name="element-information"></a>Elementinformationen



|                            |                     |
|----------------------------|---------------------|
| Name                       |                     |
| Elementtyp<br/>    | Eigenschaft<br/> |
| Bereichs Präfix <br/> | Seite<br/>     |
| Hinweise <br/>          | Keine<br/>     |



 

## <a name="structural-content"></a>Strukturelle Inhalte

Die XML-Struktur dieses Elements lautet:

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
| \_Imageablesizewidthvalue\_<br/>  | integer<br/> | Mikrometern<br/> | Größer 0<br/>             | Gibt die horizontale Dimension der Anwendungs Mediengröße in Relation zur PageOrientation an.<br/>               |
| \_Imageablesizeheightvalue\_<br/> | integer<br/> | Mikrometern<br/> | Größer 0<br/>             | Gibt die vertikale Dimension der Anwendungs Mediengröße in Relation zur PageOrientation an.<br/>                 |
| \_Originwidthvalue\_<br/>         | integer<br/> | Mikrometern<br/> | Größer oder gleich 0 (null).<br/> | Gibt den horizontalen Ursprung des Druck Bereichs in Bezug auf die Größe des Anwendungs Mediums an.<br/>                   |
| \_Originheightvalue\_<br/>        | integer<br/> | Mikrometern<br/> | Größer oder gleich 0 (null).<br/> | Gibt den vertikalen Ursprung des Druck Bereichs in Bezug auf die Größe des Anwendungs Mediums an.<br/>                     |
| \_Extentwidthvalue\_<br/>         | integer<br/> | Mikrometern<br/> | Größer 0<br/>             | Gibt den horizontalen Abstand zwischen dem Ursprung und dem Begrenzungs Grenzwert der Größe der Anwendungs Medien an.<br/>      |
| \_Extentheightvalue\_<br/>        | integer<br/> | Mikrometern<br/> | Größer 0<br/>             | Gibt den vertikalen Abstand zwischen dem Ursprung und dem Begrenzungs Grenzwert der Mediengröße der Canvas-Anwendung an.<br/> |



 

## <a name="extensible-markup-language-xml-content"></a>Inhalt der Extensible Markup Language (XML)

Die Schlüsselwörter der öffentlichen Druck Schemas werden im- https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords Namespace definiert. Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort wird unten definiert:

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

[Druck Schema Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




