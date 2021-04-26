---
description: Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: c10da176-946a-4439-8ad7-037013b39e41
title: DocumentBannerSheet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7ef61001e45178989d6f89e17d8cc38b82c1354
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996307"
---
# <a name="documentbannersheet"></a>DocumentBannerSheet

Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

Beschreibt das Bannerblatt, das für ein bestimmtes Dokument ausgegeben werden soll. Das Bannerblatt sollte unter Verwendung des Standardmäßigen PageMediaType auf der Standardseite "PageMediaSize" ausgegeben werden. Das Bannerblatt sollte auch vom Rest des Dokuments isoliert werden. Dies bedeutet, dass alle Optionen zum Beenden oder Verarbeiten von Dokumenten (z. B. DocumentDuplex, DocumentStaple oder DocumentBinding) das Bannerblatt nicht enthalten sollten. Das Bannerblatt kann vom Rest des Auftrags isoliert werden. Dies bedeutet, dass alle Optionen zum Beenden oder Verarbeiten von Aufgaben das Dokumentbannerblatt enthalten können. Das Bannerblatt sollte als erstes Blatt des Dokuments angezeigt werden.

-   [Elementinformationen](#element-information)
-   [Strukturelle Inhalte](#structural-content)

## <a name="element-information"></a>Elementinformationen



| Name | Wert |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Elementtyp <br/>   | Funktion<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Bereichspräfix <br/> | Dokument<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Hinweise <br/>          | XPS-kompatible Benutzer MÜSSEN erzwingen, dass ein URI-Verweis auf eine Ressource, z. B. ein Bild oder Farbprofil, entweder in einem Druckfunktionendokument oder printTicket auf einen Teilenamen (einen relativen URI zum Paketstamm) innerhalb desselben XPS-Dokumentpakets verweisen muss, das das resultierende PrintTicket enthält. Ein kompatibler XPS-Consumer DARF KEINEN URI verwenden, der nicht mit der Partnamenssyntax kompatibel ist. Diese Einstellungen sind XPS-spezifisch. <br/> URIs, auf die entweder in einem Druckfunktionendokument oder printTicket verwiesen wird, DÜRFEN NICHT als URLs aufgelöst werden. Dies ist unsicher, da sie möglicherweise nicht wie beabsichtigt gelöst werden und zu schädlichen Sicherheitsrisiken für treiber und betriebssystem könnten.<br/> |



 

## <a name="structural-content"></a>Strukturell

Die XML-Struktur dieses Elements lautet:

``` syntax
<psf:Feature name="psk:DocumentBannerSheet">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <!-- Specifies the XPS specific part name -->
    <psf:ScoredProperty name="psk:BannerSheetSource">
      <psf:ParameterRef name="psk:DocumentBannerSheetSource" />
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="structure-variables"></a>Strukturvariablen

In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.



| Name                               | Datentyp         | Einheit                   | Unterstützte Werte                                                                                                                                                                      | Zusammenfassung                                                                      |
|------------------------------------|-------------------|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| \_Optionname\_<br/>          | Zeichenfolge<br/> | Buchstaben <br/> | Gültiger vollqualifizierte Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert. Wenn kein Namespace angegeben ist, wird der Standardnamespace angenommen.<br/> | Der Name der Option<br/>                                            |
| \_IdentityOptionValue\_<br/> | Zeichenfolge<br/> | –<br/>         | TRUE, FALSE<br/>                                                                                                                                                                | Definiert eine Option, die diese Funktion deaktiviert, wenn sie ausgewählt wird.<br/> |



 

## <a name="extensible-markup-language-xml-content"></a>Extensible Markup Language -Inhalt (XML)

Die Schlüsselwörter für das öffentliche Druckschema werden im https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords -Namespace definiert. Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:

``` syntax
<psf:Feature name="psk:DocumentBannerSheet">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies a custom banner sheet should be output. If a DocumentBannerSheetSource 
     ParameterInit element is not specified, this Option should be ignored. -->
  <psf:Option name="psk:Custom">
    <psf:ScoredProperty name="psk:BannerSheetSource">
      <psf:ParameterRef name="psk:DocumentBannerSheetSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies no banner sheet should be output. -->
  <psf:Option name="psk:None" />
  <!-- Specifies the standard (device defined) banner sheet should be output. -->
  <psf:Option name="psk:Standard" />
</psf:Feature>
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




