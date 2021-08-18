---
description: Erfahren Sie mehr über das DocumentCollate-Element, das die Sortierungsmerkmale der Ausgabe beschreibt.
ms.assetid: 752cccf7-1f95-4597-b0e2-a96fd22ffeef
title: DocumentCollate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4accbba3bf309ef9eaec251c5877ee7965f984ed63670a50ebf5e870406acb92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971589"
---
# <a name="documentcollate"></a>DocumentCollate

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

Beschreibt die Sortiermerkmale der Ausgabe. Alle Seiten in jedem einzelnen Dokument werden sortiert. DocumentCollate und JobCollateAlldocuments schließen sich gegenseitig aus. Das Verhalten und die Implementierung, ob beide oder nur eines dieser Schlüsselwörter implementiert ist, bleibt dem Treiber überlassen.

Im Folgenden finden Sie die Regeln, die für die Collate-Implementierung befolgt werden sollten.

## <a name="element-definition-and-rules"></a>Elementdefinition und Regeln

Sie müssen zuerst die Regeln für JobCollateAllDocument befolgen und dann Regeln für DocumentCollate anwenden, damit die Szenarien funktionieren. Beachten Sie, dass in einer Konvertierungseinstellung von PrintTicket in Devmode, bei der JobCollateAllDocuments vom Treiber nicht unterstützt wird, der Treiber das geeignete Verhalten auswählen muss (JobCollateAllDocuments = ON oder OFF). Außerdem kann die Auswahl abhängig von anderen PrintTicket-Einstellungen geändert werden.

### <a name="jobcollatealldocuments"></a>JobCollateAllDocuments

EIN: Drucken Sie (DocumentCopiesAllPages) Kopien jedes Dokuments, und wiederholen Sie die Zeiten von JobCopiesAllDocuments.

OFF: Für jedes Dokument werden Druckkopien (JobCopiesAllDocuments x DocumentCopiesAllPages) zusammen kopiert.

### <a name="documentcollate"></a>DocumentCollate

ON: Für alle Kopien (JobCopiesAllDocuments x DocumentCopiesAllPages) eines Dokuments, die zusammenhängend gedruckt werden, sortieren Sie blätter in diesem Dokument.

OFF: Drucken Sie für alle Kopien (JobCopiesAllDocuments x DocumentCopiesAllPages), die zusammenhängend gedruckt werden, alle Kopien (JobCopiesAllDocuments x DocumentCopiesAllPages) jedes Blatts zusammen.

-   [Elementinformationen](#element-information)

-   [Strukturell](#structural-content)

-   [XML-Inhalt](#extensible-markup-language-xml-content)

## <a name="element-information"></a>Elementinformationen



| Name | Wert |
|----------------------------|---------------------|
| Elementtyp <br/>   | Komponente<br/>  |
| Bereichspräfix <br/> | Dokument<br/> |
| Hinweise <br/>          | Keine<br/>     |



 

## <a name="structural-content"></a>Strukturell

Die XML-Struktur dieses Elements lautet:

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

In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.



| Name                               | Datentyp         | Einheit                  | Unterstützte Werte                                                                                                                                                                      | Zusammenfassung                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| \_Optionname\_<br/>          | Zeichenfolge<br/> | Buchstaben<br/> | Gültiger vollqualifizierte Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert. Wenn kein Namespace angegeben wird, wird der Standardnamespace angenommen.<br/> | Der Name der Option.<br/>                                           |
| \_IdentityOptionValue\_<br/> | Zeichenfolge<br/> | –<br/>        | TRUE, FALSE<br/>                                                                                                                                                               | Definiert eine Option, die diese Funktion deaktiviert, wenn sie ausgewählt wird.<br/> |



 

## <a name="extensible-markup-language-xml-content"></a>Extensible Markup Language (XML)-Inhalt

Die Schlüsselwörter für das öffentliche Druckschema werden im https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords -Namespace definiert. Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:

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

 

 




