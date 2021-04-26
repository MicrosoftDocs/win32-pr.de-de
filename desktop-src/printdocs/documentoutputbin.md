---
description: Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: 73840548-f68b-4af8-acb4-6f7faa2e8879
title: DocumentOutputBin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96f6d16ca000e76b01cd2c3165054d7acc81351b
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997137"
---
# <a name="documentoutputbin"></a>DocumentOutputBin

Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

Beschreibt die vollständige Liste der unterstützten Behälter für das Gerät. Ermöglicht die Angabe des Ausgabebehälters pro Dokument. Die Schlüsselwörter JobOutputBin, DocumentOutputBin und PageOutputBin schließen sich gegenseitig aus, nur eines sollte in einem PrintTicket- oder Druckfunktionen-Dokument angegeben werden.

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
<psf:Feature name="psk:DocumentOutputBin">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:BinType">
      <psf:Value xsi:type="xs:string">_BinTypeValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSheetCapacity">
      <psf:Value xsi:type="xs:integer">_MediaSheetCapacityValue_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a>Strukturvariablen

In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.



| Name                                   | Datentyp          | Einheit                  | Unterstützte Werte                                                                                                                                                             | Zusammenfassung                                                                             |
|----------------------------------------|--------------------|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| \_Optionname\_<br/>              | Zeichenfolge<br/>  | Buchstaben<br/> | Gültiger vollqualifizierter Name, wie durch https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname definiert. Wenn kein Namespace angegeben wird, wird der Standardnamespace angenommen.<br/> | Der Name der Option.<br/>                                                  |
| \_IdentityOptionValue\_<br/>     | Zeichenfolge<br/>  | –<br/>        | TRUE, FALSE<br/>                                                                                                                                                      | Definiert eine Option, durch die diese Funktion deaktiviert wird, wenn sie ausgewählt wird.<br/>        |
| \_BinTypeValue\_<br/>            | Zeichenfolge<br/>  | –<br/>        | MailBox, Sorter, Stacker, Finisher, None.<br/>                                                                                                                         | Gibt den allgemeinen Typ des Papierkorbs an.<br/>                                   |
| \_MediaSheetCapacityValue\_<br/> | integer<br/> | Blätter<br/>     | Größer 0<br/>                                                                                                                                                   | Gibt die Medienkapazität in der Anzahl der Seiten (vollständige Ebene) des Papierkorbs an.<br/> |



 

## <a name="extensible-markup-language-xml-content"></a>Extensible Markup Language -Inhalt (XML)

Die Schlüsselwörter für das öffentliche Druckschema werden im https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords -Namespace definiert. Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:

``` syntax
<psf:Feature name="psk:DocumentOutputBin">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
    <!--Specifies type of output bin-->
    <psf:ScoredProperty name="psk:BinType">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <!--Specifies media capacity for output bin-->
    <psf:ScoredProperty name="psk:MediaSheetCapacity">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>    
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




