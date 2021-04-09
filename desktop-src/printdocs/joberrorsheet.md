---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: ad30df59-0051-4471-8c0e-3207bcc7bfbe
title: Joberrorsheet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ef9d613bf3b3af980b5cb8e916eac115cd1a0cb
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "103869668"
---
# <a name="joberrorsheet"></a>Joberrorsheet

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Beschreibt die Ausgabe des Fehler Blatts. Der gesamte Auftrag wird mit einem einzelnen Fehler Blatt angezeigt. Das Fehler Blatt sollte auf der Standardseite PageMediaSize ausgegeben werden und mithilfe des standardmäßigen PageMediaType verwendet werden. Das Fehler Blatt sollte vom Rest des Auftrags isoliert werden. Dies bedeutet, dass das Fehler Blatt bei allen Beendigungs-oder Verarbeitungsoptionen (z. b. jobduplex, jobstaple oder jobbinding) nicht enthalten sein sollte. Das Fehler Blatt sollte als abschließendes Blatt des Auftrags auftreten.

-   [Elementinformationen](#element-information)
-   [Strukturelle Inhalte](#structural-content)
-   [Inhalt der Extensible Markup Language (XML)](#extensible-markup-language-xml-content)

## <a name="element-information"></a>Elementinformationen



| Name                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Elementtyp <br/>   | Funktion<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Bereichs Präfix <br/> | Auftrag<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Notizen <br/>          | XPS-kompatible Consumer müssen erzwingen, dass ein URI-Verweis auf eine Ressource, z. b. ein Bild oder ein Farbprofil in einem Druck Funktions Dokument oder in PrintTicket, auf einen Teilnamen (ein relativer URI zum Paket Stamm) innerhalb desselben XPS-Dokument Pakets verweisen muss, das das resultierende PrintTicket enthält. Ein kompatibler XPS-Consumer darf keinen URI verwenden, der mit der Syntax für den Teilnamen nicht kompatibel ist. Diese Einstellungen sind XPS-spezifisch. <br/> URIs, auf die in einem Druck Funktions Dokument oder in PrintTicket verwiesen wird, dürfen nicht als URLs aufgelöst werden. Dies ist unsicher, da Sie möglicherweise nicht erwartungsgemäß aufgelöst werden und schädliche Sicherheitsrisiken für den Treiber und das Betriebssystem verursachen können.<br/> |



 

## <a name="structural-content"></a>Strukturelle Inhalte

Die XML-Struktur dieses Elements lautet:

``` syntax
<psf:Feature name="psk:JobErrorSheet">
  <!--Describes when an error sheet should be output. -->
  <psf:Feature name="psk:ErrorSheetWhen">
    <psf:Property name="psf:SelectionType">
      <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
    </psf:Property>
    <psf:Option name="psk:_ErrorSheetWhenOptionName_">
      <psf:Property name="psf:IdentityOption">
        <psf:Value xsi:type="xs:string">_ErrorSheetWhenIdentityOptionValue_</psf:Value>
      </psf:Property>
    </psf:Option>
  </psf:Feature>
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <!-- Specifies the XPS part name for the error sheet. -->
    <psf:ScoredProperty name="psk:ErrorSheetSource">
      <psf:ParameterRef name="psk:JobErrorSheetSource" />
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>      
```

## <a name="structure-variables"></a>Strukturvariablen

In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.



| Name                                             | Datentyp         | Einheit                  | Unterstützte Werte                                                                                                                                                                      | Zusammenfassung                                                                      |
|--------------------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| \_Errorsheetinstanoptionname\_<br/>          | Zeichenfolge<br/> | Buchstaben<br/> | Gültiger, voll qualifizierter Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert. Wenn kein Namespace angegeben wird, wird der Standard Namespace angenommen.<br/> | Der Name der Option.<br/>                                           |
| \_Errorsheet-identityoptionvalue\_<br/> | Zeichenfolge<br/> | –<br/>        | TRUE, FALSE<br/>                                                                                                                                                               | Definiert die Auswahlkriterien für die Benutzeroberfläche (UI).<br/>               |
| \_Optionsname\_<br/>                        | Zeichenfolge<br/> | –<br/>        | Gültiger voll qualifizierter Name, wie durch definiert https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname . Wenn kein Namespace angegeben wird, wird der Standard Namespace angenommen.<br/>          | Der Name der Option.<br/>                                           |
| \_Identityoptionvalue\_<br/>               | Zeichenfolge<br/> | –<br/>        | TRUE, FALSE<br/>                                                                                                                                                               | Definiert eine Option, die diese Funktion deaktiviert, wenn Sie ausgewählt wird.<br/> |



 

## <a name="extensible-markup-language-xml-content"></a>Inhalt der Extensible Markup Language (XML)

Die Schlüsselwörter der öffentlichen Druck Schemas werden im- https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords Namespace definiert. Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort wird unten definiert:

``` syntax
<psf:Feature name="psk:JobErrorSheet">
  <psf:Feature name="psk:ErrorSheetWhen">
    <psf:Property name="psf:SelectionType">
      <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
    </psf:Property>
    <!-- Specifies an error sheet will be output for every job. -->
    <psf:Option name="psk:Always" />
    <!-- Specifies an error sheet will be output only on error. -->
    <psf:Option name="psk:OnError" />
  </psf:Feature>
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies a custom error sheet should be output. If a JobErrorSheetSource 
     ParameterInit element is not specified, this Option should be ignored. -->
  <psf:Option name="psk:Custom">
    <psf:ScoredProperty name="psk:ErrorSheetSource">
      <psf:ParameterRef name="psk:JobErrorSheetSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies no error sheet should be output. -->
  <psf:Option name="psk:None" />
  <!-- Specifies the standard (device defined) error sheet should be output. -->
  <psf:Option name="psk:Standard" />
</psf:Feature>    
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Druck Schema Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




