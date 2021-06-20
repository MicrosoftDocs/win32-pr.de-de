---
description: Erfahren Sie mehr über das DocumentCollate-Element, das die Sortierungsmerkmale der Ausgabe beschreibt.
ms.assetid: 752cccf7-1f95-4597-b0e2-a96fd22ffeef
title: DocumentCollate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4c3036cc64265ea8f88bfcc46aea0149f8af5ad
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409453"
---
# <a name="documentcollate"></a>DocumentCollate

Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

Beschreibt die Sortierungsmerkmale der Ausgabe. Alle Seiten in jedem einzelnen Dokument werden sortiert. DocumentCollate und JobCollateAlldocuments schließen sich gegenseitig aus. Das Verhalten und die Implementierung, ob beide oder nur eines dieser Schlüsselwörter implementiert wird, bleiben dem Treiber erhalten.

Im Folgenden finden Sie die Regeln, die für die Collate-Implementierung befolgt werden sollten.

## <a name="element-definition-and-rules"></a>Elementdefinition und Regeln

Sie müssen zuerst die Regeln für JobCollateAllDocument befolgen und dann Regeln für DocumentCollate anwenden, damit die Szenarien funktionieren. Beachten Sie, dass es in einer Konvertierungseinstellung "PrintTicket in Devmode", bei der JobCollateAllDocuments vom Treiber nicht unterstützt wird, Aufgabe des Treibers ist, das geeignete Verhalten zu wählen (JobCollateAllDocuments = ON oder OFF). Außerdem kann die Auswahl abhängig von anderen PrintTicket-Einstellungen geändert werden.

### <a name="jobcollatealldocuments"></a>JobCollateAllDocuments

ON: Drucken Sie (DocumentCopiesAllPages)-Kopien jedes Dokuments, wiederholen Sie JobCopiesAllDocuments-Zeiten.

OFF: Für jedes Dokument kopiert print (JobCopiesAllDocuments x DocumentCopiesAllPages) zusammen.

### <a name="documentcollate"></a>DocumentCollate

ON: Für alle Kopien (JobCopiesAllDocuments x DocumentCopiesAllPages) eines zusammenhängend gedruckten Dokuments werden die Blätter in diesem Dokument sortiert.

OFF: Für alle Kopien (JobCopiesAllDocuments x DocumentCopiesAllPages), die zusammenhängend gedruckt werden, drucken Sie alle Kopien (JobCopiesAllDocuments x DocumentCopiesAllPages) jedes Blatts zusammen.

-   [Elementinformationen](#element-information)

-   [Strukturelle Inhalte](#structural-content)

-   [XML-Inhalt](#extensible-markup-language-xml-content)

## <a name="element-information"></a>Elementinformationen



| Name | Wert |
|----------------------------|---------------------|
| Elementtyp <br/>   | Funktion<br/>  |
| Bereichspräfix <br/> | Dokument<br/> |
| Hinweise <br/>          | Keine<br/>     |



 

## <a name="structural-content"></a>Strukturelle Inhalte

Die XML-Struktur dieses Elements ist:

``` syntax
<psf:Feature name="psk:DocumentCollate">
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
<psf:Feature name="psk:DocumentCollate">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies collating.  -->
  <psf:Option name="psk:Collated" />
  <!-- Specifies no collating. -->
  <psf:Option name="psk:Uncollated" />
</psf:Feature>
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




