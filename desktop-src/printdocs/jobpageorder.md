---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 0c255d50-8b0e-4ecd-876d-eaaccdca7b27
title: Jobpage Order
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e554da890464afdaed033490def1a915f9d7d800
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "106350605"
---
# <a name="jobpageorder"></a>Jobpage Order

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Definiert die Reihenfolge physischer Seiten für die Ausgabe.

-   [Elementinformationen](#element-information)
-   [Strukturelle Inhalte](#structural-content)
-   [Inhalt der Extensible Markup Language (XML)](#extensible-markup-language-xml-content)

## <a name="element-information"></a>Elementinformationen



| Name                       |                    |
|----------------------------|--------------------|
| Elementtyp <br/>   | Funktion<br/> |
| Bereichs Präfix <br/> | Auftrag<br/>     |
| Hinweise <br/>          | Keine<br/>    |



 

## <a name="structural-content"></a>Strukturelle Inhalte

Die XML-Struktur dieses Elements lautet:

``` syntax
<psf:Feature name="psk:JobPageOrder">
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
| \_Optionsname\_<br/>          | Zeichenfolge<br/> | Buchstaben<br/> | Gültiger, voll qualifizierter Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert. Wenn kein Namespace angegeben wird, wird der Standard Namespace angenommen.<br/> | Der Name der Option.<br/>                                           |
| \_Identityoptionvalue\_<br/> | Zeichenfolge<br/> | –<br/>        | TRUE, FALSE<br/>                                                                                                                                                               | Definiert eine Option, die diese Funktion deaktiviert, wenn Sie ausgewählt wird.<br/> |



 

## <a name="extensible-markup-language-xml-content"></a>Inhalt der Extensible Markup Language (XML)

Die Schlüsselwörter der öffentlichen Druck Schemas werden im- https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords Namespace definiert. Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort wird unten definiert:

``` syntax
<psf:Feature name="psk:JobPageOrder">
  <psf:Property name="psf:SelectionType">
   <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies front to back page order. -->
  <psf:Option name="psk:Standard" />
  <!-- Specifies back to front page order. -->
  <psf:Option name="psk:Reverse" />
</psf:Feature>
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Druck Schema Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




