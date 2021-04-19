---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: c7abb657-6c9d-435a-a700-2eb0f14707c0
title: Joburi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bb06148438b0fd6715370c56ff9efe54d512219
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106355116"
---
# <a name="joburi"></a>Joburi

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Gibt einen URI (Uniform Resource Identifier) für das Dokument an.

-   [Elementinformationen](#element-information)
-   [Strukturelle Inhalte](#structural-content)
-   [Inhalt der Extensible Markup Language (XML)](#extensible-markup-language-xml-content)

## <a name="element-information"></a>Elementinformationen



| Name                       |                     |
|----------------------------|---------------------|
| Elementtyp <br/>   | Eigenschaft<br/> |
| Bereichs Präfix <br/> | Auftrag<br/>      |
| Hinweise <br/>          | Keine<br/>     |



 

## <a name="structural-content"></a>Strukturelle Inhalte

Die XML-Struktur dieses Elements lautet wie folgt:

``` syntax
<psf:Property name="psk:JobURI">
    <psf:Value xsi:type="xs:string">_JobURIValue_</psf:Value>
</psf:Property>
      
```

## <a name="structure-variables"></a>Strukturvariablen

In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.



| Name                       | Datentyp         | Einheit | Unterstützte Werte | Zusammenfassung |
|----------------------------|-------------------|------|------------------|---------|
| \_Joburivalue\_<br/> | Zeichenfolge<br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a>Inhalt der Extensible Markup Language (XML)

``` syntax
<psf:Property name="psk:JobURI">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Druck Schema Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




