---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 941515a8-ba3f-47b9-9f3f-08a48122661a
title: DocumentNUp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08fdf22fa557ce1da4fde20ad1d8ea14625a1b77
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "104219107"
---
# <a name="documentnup"></a>DocumentNUp

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Beschreibt die Ausgabe und das Format mehrerer logischer Seiten an ein einzelnes physisches Blatt. Jedes Dokument wird separat kompiliert. "DocumentNUp" und "jobnupalldocumentsangrenzende" schließen sich gegenseitig aus. Der Treiber kann die Einschränkungs Behandlung zwischen diesen Schlüsselwörtern bestimmen.

Das folgende Diagramm veranschaulicht ein Beispiel mit Dokument 1, das drei Seiten enthält, und Dokument 2, das zwei Seiten enthält. Jedes Dokument wird separat duplext. Die unten gezeigte Präsentations Richtung ist die Option RightBottom.

![ein Diagramm, das zeigt, wie Dokument Seiten basierend auf der DocumentNUp-Einstellung auf einem einzelnen Blatt angelegt werden](images/local-1663869164-docduplex1.gif)

-   [Elementinformationen](#element-information)
-   [Strukturelle Inhalte](#structural-content)
-   [Inhalt der Extensible Markup Language (XML)](#extensible-markup-language-xml-content)

## <a name="element-information"></a>Elementinformationen



| Name                       |                                                                                                                                                 |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| Elementtyp <br/>   | Funktion<br/>                                                                                                                              |
| Bereichs Präfix <br/> | Dokument<br/>                                                                                                                             |
| Notizen <br/>          | Top, Bottom, Left und Right sind relativ zu PageImageableSize, wobei TopLeft durch den Ursprung der x-Achse und der y-Achse gekennzeichnet wird.<br/> |



 

## <a name="structural-content"></a>Strukturelle Inhalte

Die XML-Struktur dieses Elements lautet wie folgt:

``` syntax
<psf:Feature name="psk:DocumentNUp">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:PagesPerSheet">
      <psf:Value xsi:type="xs:integer">_PagesPerSheetValue_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies the ordering direction of the pages.  First direction followed by second direction. -->
  <psf:Feature name="psk:PresentationDirection">
    <psf:Option name="psk:_PresentationDirectionOptionName_" />
  </psf:Feature>
</psf:Feature>
```

## <a name="structure-variables"></a>Strukturvariablen

In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.



| Name                                           | Datentyp          | Einheit                     | Unterstützte Werte                                                                                                                                                                      | Zusammenfassung                                                                                                                              |
|------------------------------------------------|--------------------|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| \_Optionsname\_<br/>                      | Zeichenfolge<br/>  | Buchstaben<br/>    | Gültiger, voll qualifizierter Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert. Wenn kein Namespace angegeben wird, wird der Standard Namespace angenommen.<br/> | Der Name der Option.<br/>                                                                                                   |
| \_Identityoptionvalue\_<br/>             | Zeichenfolge<br/>  | –<br/>           | TRUE, FALSE<br/>                                                                                                                                                               | Definiert eine Option, die diese Funktion deaktiviert, wenn Sie ausgewählt wird.<br/>                                                         |
| \_Pagespersheetvalue\_<br/>              | integer<br/> | Logische Seiten<br/> | Alle ganzzahligen Werte (größer als null).<br/>                                                                                                                                          | Gibt die Anzahl der logischen Seiten pro physikalischer Tabelle an. Die unterstützte Menge kann eine beliebige Gruppe von Ganzzahlen sein, z.b. {1,2,4,6,8,9,16}.<br/> |
| \_Presentationdirectionoptionname\_<br/> | Zeichenfolge<br/>  | Buchstaben<br/>    | Gültiger, voll qualifizierter Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert. Wenn kein Namespace angegeben wird, wird der Standard Namespace angenommen.<br/> | Der Name der Option.<br/>                                                                                                   |



 

## <a name="extensible-markup-language-xml-content"></a>Inhalt der Extensible Markup Language (XML)

Die Schlüsselwörter der öffentlichen Druck Schemas werden im- https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords Namespace definiert. Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort wird unten definiert:

``` syntax
<psf:Feature name="psk:DocumentNUp">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
    <psf:ScoredProperty name="psk:PagesPerSheet">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Feature name="psk:PresentationDirection">
    <!-- Specifies format left to right, top to bottom. -->
    <psf:Option name="psk:RightBottom" />
    <!-- Specifies format top to bottom, left to right. -->
    <psf:Option name="psk:BottomRight" />
    <!-- Specifies format right to left, top to bottom. -->
    <psf:Option name="psk:LeftBottom" />
    <!-- Specifies format top to bottom, right to left. -->
    <psf:Option name="psk:BottomLeft" />
    <!-- Specifies format left to right, bottom to top. -->
    <psf:Option name="psk:RightTop" />
    <!-- Specifies format bottom to top, left to right. -->
    <psf:Option name="psk:TopRight" />
    <!-- Specifies format right to left, bottom to top. -->
    <psf:Option name="psk:LeftTop" />
    <!-- Specifies format bottom to top, right to left. -->
    <psf:Option name="psk:TopLeft" />
  </psf:Feature>
</psf:Feature>
    
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Druck Schema Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




