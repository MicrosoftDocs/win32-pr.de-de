---
description: Erfahren Sie mehr über das DocumentNUp-Element, das die Ausgabe und das Format mehrerer logischer Seiten auf einem einzelnen physischen Blatt beschreibt.
ms.assetid: 941515a8-ba3f-47b9-9f3f-08a48122661a
title: DocumentNUp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0804d38bdb60cd28ba88832b21abe8426d8aaf3b4fedf6ce5ad38f624f10c596
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119949725"
---
# <a name="documentnup"></a>DocumentNUp

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

Beschreibt die Ausgabe und das Format mehrerer logischer Seiten zu einem einzelnen physischen Blatt. Jedes Dokument wird separat kompiliert. DocumentNUp und JobNUpAllDocumentsContiguously schließen sich gegenseitig aus. Es liegt an dem Treiber, die Einschränkungsbehandlung zwischen diesen Schlüsselwörtern zu bestimmen.

Das folgende Diagramm veranschaulicht ein Beispiel mit Dokument 1 mit 3 Seiten und Dokument 2 mit 2 Seiten. Jedes Dokument ist separat duplexed. Die unten gezeigte Präsentationsrichtung ist die RightBottom-Option.

![Ein Diagramm, das zeigt, wie Dokumentseiten basierend auf der DocumentNup-Einstellung auf einem einzelnen Blatt angeordnet werden](images/local-1663869164-docduplex1.gif)

-   [Elementinformationen](#element-information)
-   [Strukturell](#structural-content)
-   [Extensible Markup Language -Inhalt (XML)](#extensible-markup-language-xml-content)

## <a name="element-information"></a>Elementinformationen



| Name | Wert |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| Elementtyp <br/>   | Komponente<br/>                                                                                                                              |
| Bereichspräfix <br/> | Dokument<br/>                                                                                                                             |
| Hinweise <br/>          | Top, Bottom, Left und Right sind relativ zu PageImageableSize, wobei TopLeft durch den Ursprung der x-Achse und der y-Achse gekennzeichnet ist.<br/> |



 

## <a name="structural-content"></a>Strukturell

Die XML-Struktur dieses Elements sieht wie folgt aus:

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

In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.



| Name                                           | Datentyp          | Einheit                     | Unterstützte Werte                                                                                                                                                                      | Zusammenfassung                                                                                                                              |
|------------------------------------------------|--------------------|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| \_Optionname\_<br/>                      | Zeichenfolge<br/>  | Buchstaben<br/>    | Gültiger vollqualifizierte Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert. Wenn kein Namespace angegeben wird, wird der Standardnamespace angenommen.<br/> | Der Name der Option.<br/>                                                                                                   |
| \_IdentityOptionValue\_<br/>             | Zeichenfolge<br/>  | –<br/>           | TRUE, FALSE<br/>                                                                                                                                                               | Definiert eine Option, die diese Funktion deaktiviert, wenn sie ausgewählt wird.<br/>                                                         |
| \_PagesPerSheetValue\_<br/>              | integer<br/> | Logische Seiten<br/> | Alle ganzen Zahlen (Größer als Null).<br/>                                                                                                                                          | Gibt die Anzahl logischer Seiten pro physischem Blatt an. Der unterstützte Satz kann ein beliebiger Satz von ganzen Zahlen sein, z. B. {1,2,4,6,8,9,16}.<br/> |
| \_PresentationDirectionOptionName\_<br/> | Zeichenfolge<br/>  | Buchstaben<br/>    | Gültiger vollqualifizierte Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert. Wenn kein Namespace angegeben wird, wird der Standardnamespace angenommen.<br/> | Der Name der Option.<br/>                                                                                                   |



 

## <a name="extensible-markup-language-xml-content"></a>Extensible Markup Language -Inhalt (XML)

Die Schlüsselwörter für das öffentliche Druckschema werden im https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords -Namespace definiert. Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:

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

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




