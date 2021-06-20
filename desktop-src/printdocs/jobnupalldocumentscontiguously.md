---
description: Erfahren Sie mehr über das JobNUpAllDocumentsContiguously-Element, das die Ausgabe mehrerer logischer Seiten für ein einzelnes physisches Blatt beschreibt.
ms.assetid: e73e1736-9be5-4831-8277-23a62658b7b5
title: JobNUpAllDocumentsContiguously
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9106259c80a7efb89cc4481780bfb55af4f07e23
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408863"
---
# <a name="jobnupalldocumentscontiguously"></a>JobNUpAllDocumentsContiguously

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

Beschreibt die Ausgabe mehrerer logischer Seiten für ein einzelnes physisches Blatt. Alle Dokumente im Auftrag werden zusammenhängend kompiliert. JobNUpAllDocumentsContiguously und DocumentNUp schließen sich gegenseitig aus. Es obliegt dem Treiber, die Einschränkungsbehandlung zwischen diesen Schlüsselwörtern zu bestimmen.

Das folgende Diagramm veranschaulicht ein Beispiel mit Dokument 1 mit 3 Seiten und Dokument 2 mit 2 Seiten. Jedes Dokument im Auftrag ist zusammenhängend duplexgedupligt. Die im Beispiel gezeigten Präsentationsrichtungen sind die RightBottom-Option.

![Diagramm, das zeigt, wie Dokumentseiten basierend auf der DocumentNup-Einstellung auf einem einzelnen Blatt angeordnet werden](images/local-1242234459-jobduplexpics.gif)

-   [Elementinformationen](#element-information)
-   [Strukturell](#structural-content)
-   [xml-Inhalt (Extensible Markup Language)](#extensible-markup-language-xml-content)

## <a name="element-information"></a>Elementinformationen



| Name | Wert |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| Elementtyp <br/>   | Funktion<br/>                                                                                                                             |
| Bereichspräfix <br/> | Auftrag<br/>                                                                                                                                 |
| Hinweise <br/>          | Top, Bottom, Left und Right sind relativ zu PageImageableSize, wobei TopLeft durch den Ursprung der Höhe und Breite gekennzeichnet ist.<br/> |



 

## <a name="structural-content"></a>Strukturell

Die XML-Struktur dieses Elements lautet:

``` syntax
<psf:Feature name="psk:JobNUpAllDocumentsContiguously">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
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
| \_Optionname\_<br/>                      | Zeichenfolge<br/>  | Buchstaben<br/>    | Gültiger vollqualifizierte Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert. Wenn kein Namespace angegeben ist, wird der Standardnamespace angenommen.<br/> | Der Name der Option.<br/>                                                                                                   |
| \_IdentityOptionValue\_<br/>             | Zeichenfolge<br/>  | –<br/>           | TRUE, FALSE<br/>                                                                                                                                                               | Definiert eine Option, die diese Funktion deaktiviert, wenn sie ausgewählt wird.<br/>                                                         |
| \_PagesPerSheetValue\_<br/>              | integer<br/> | Logische Seiten<br/> | Alle ganzen Zahlen (größer als null).<br/>                                                                                                                                          | Gibt die Anzahl der logischen Seiten pro physischem Blatt an. Der unterstützte Satz kann ein beliebiger Satz von ganzen Zahlen sein, z. B. {1,2,4,6,8,9,16}.<br/> |
| \_PresentationDirectionOptionName\_<br/> | Zeichenfolge<br/>  | Buchstaben<br/>    | Gültiger vollqualifizierte Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert. Wenn kein Namespace angegeben ist, wird der Standardnamespace angenommen.<br/> | Der Name der Option.<br/>                                                                                                   |



 

## <a name="extensible-markup-language-xml-content"></a>xml-Inhalt (Extensible Markup Language)

Die Schlüsselwörter für das öffentliche Druckschema werden im https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords -Namespace definiert. Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:

``` syntax
<psf:Feature name="psk:JobNUpAllDocumentsContiguously">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
    <psf:ScoredProperty name="psk:PagesPerSheet">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Feature name="psk:PresentationDirection">
    <!-- Specifies left to right, top to bottom. -->
    <psf:Option name="psk:RightBottom" />
    <!-- Specifies top to bottom, left to right. -->
    <psf:Option name="psk:BottomRight" />
    <!-- Specifies right to left, top to bottom. -->
    <psf:Option name="psk:LeftBottom" />
    <!-- Specifies top to bottom, right to left. -->
    <psf:Option name="psk:BottomLeft" />
    <!-- Specifies left to right, bottom to top. -->
    <psf:Option name="psk:RightTop" />
    <!-- Specifies bottom to top, left to right. -->
    <psf:Option name="psk:TopRight" />
    <!-- Specifies right to left, bottom to top. -->
    <psf:Option name="psk:LeftTop" />
    <!-- Specifies bottom to top, right to left. -->
    <psf:Option name="psk:TopLeft" />
  </psf:Feature>
</psf:Feature>
    
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




