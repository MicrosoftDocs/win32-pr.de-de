---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 64fcd03f-8e0a-498d-82ea-0c69be0a3886
title: JobCollateAllDocuments
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0406a5f9106cbe4cd2a8ccb0986a1bfacc95b916
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "104351909"
---
# <a name="jobcollatealldocuments"></a>JobCollateAllDocuments

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Beschreibt die Sortierungs Merkmale der Ausgabe. Alle Dokumente in jedem einzelnen Auftrag werden sortiert. DocumentCollate und JobCollateAllDocuments schließen sich gegenseitig aus. Das Verhalten und die Implementierung, ob sowohl als auch nur eines dieser Schlüsselwörter implementiert ist, wird dem Treiber überlassen.

Im folgenden finden Sie die Regeln, die für die COLLATE-Implementierung befolgt werden sollten.

## <a name="element-definition-and-rules"></a>Element Definition und-Regeln

Sie müssen zuerst die Regeln für jobcollatealldocument befolgen und dann Regeln für DocumentCollate anwenden, damit die Szenarien funktionieren. Beachten Sie, dass in einer Konvertierungs Einstellung von PrintTicket zu DEVMODE, in der JobCollateAllDocuments nicht vom Treiber unterstützt wird, der Treiber das geeignete Verhalten auswählen muss (JobCollateAllDocuments = on oder Off). Die Auswahl kann auch abhängig von anderen PrintTicket-Einstellungen geändert werden.

### <a name="jobcollatealldocuments"></a>JobCollateAllDocuments

Auf: Print (DocumentCopiesAllPages)-Kopien der einzelnen Dokumente, wiederholen Sie die JobCopiesAllDocuments-Zeiten.

Aus: für jedes Dokument wird Print (JobCopiesAllDocuments x DocumentCopiesAllPages) zusammen kopiert.

### <a name="documentcollate"></a>DocumentCollate

Auf: für alle Kopien (JobCopiesAllDocuments x DocumentCopiesAllPages) eines Dokuments, das zusammenhängend gedruckt wird, werden in diesem Dokument COLLATE-Blätter angezeigt.

Aus: für alle Kopien (JobCopiesAllDocuments x DocumentCopiesAllPages), die zusammenhängend gedruckt werden, werden alle Kopien (JobCopiesAllDocuments x DocumentCopiesAllPages) jedes Blatts zusammen gedruckt.

-   [Elementinformationen](#element-information)
-   [Strukturelle Inhalte](#structural-content)
-   [Inhalt der Extensible Markup Language (XML)](#extensible-markup-language-xml-content)

### <a name="element-information"></a>Elementinformationen



| Name                       |                    |
|----------------------------|--------------------|
| Elementtyp <br/>   | Funktion<br/> |
| Bereichs Präfix <br/> | Auftrag<br/>     |
| Hinweise <br/>          | Keine<br/>    |



 

### <a name="structural-content"></a>Strukturelle Inhalte

Die XML-Struktur dieses Elements lautet:

``` syntax
<psf:Feature name="psk:JobCollateAllDocuments">
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

### <a name="structure-variables"></a>Strukturvariablen

In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.



| Name                               | Datentyp         | Einheit                  | Unterstützte Werte                                                                                                                                                                      | Zusammenfassung                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| \_Optionsname\_<br/>          | Zeichenfolge<br/> | Buchstaben<br/> | Gültiger, voll qualifizierter Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert. Wenn kein Namespace angegeben wird, wird der Standard Namespace angenommen.<br/> | Der Name der Option.<br/>                                           |
| \_Identityoptionvalue\_<br/> | Zeichenfolge<br/> | –<br/>        | TRUE, FALSE<br/>                                                                                                                                                               | Definiert eine Option, die diese Funktion deaktiviert, wenn Sie ausgewählt wird.<br/> |



 

### <a name="extensible-markup-language-xml-content"></a>Inhalt der Extensible Markup Language (XML)

Die Schlüsselwörter der öffentlichen Druck Schemas werden im- https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords Namespace definiert. Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort wird unten definiert:

``` syntax
<psf:Feature name="psk:JobCollateAllDocuments">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies collating.  -->
  <psf:Option name="psk:Collated" />
  <!-- Specifies no collating. -->
  <psf:Option name="psk:Uncollated" />
</psf:Feature>
```

 

 




