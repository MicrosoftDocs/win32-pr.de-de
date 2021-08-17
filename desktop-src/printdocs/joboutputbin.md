---
description: Erfahren Sie mehr über das JobOutputBin-Element, das den installierten Ausgabebehälter auf einem Gerät oder die vollständige Liste der unterstützten Container für ein Gerät beschreibt.
ms.assetid: 324ec426-b7c8-43af-96b9-74929358e262
title: JobOutputBin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35a1322a75ac7aef5ff2c5d30f9dd63a64beb00a147f8eb4cf7529a3f9582d96
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119447460"
---
# <a name="joboutputbin"></a>JobOutputBin

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

Beschreibt den installierten Ausgabebehälter auf einem Gerät oder die vollständige Liste der unterstützten Container für ein Gerät. Die Schlüsselwörter JobOutputBin, DocumentOutputBin und PageOutputBin schließen sich gegenseitig aus, nur eines sollte in einem PrintTicket- oder Print Capabilities-Dokument angegeben werden.

-   [Elementinformationen](#element-information)
-   [Strukturell](#structural-content)
-   [Extensible Markup Language (XML)-Inhalt](#extensible-markup-language-xml-content)

## <a name="element-information"></a>Elementinformationen



| Name | Wert |
|----------------------------|--------------------|
| Elementtyp <br/>   | Komponente<br/> |
| Bereichspräfix <br/> | Auftrag<br/>     |
| Hinweise <br/>          | Keine<br/>    |



 

## <a name="structural-content"></a>Strukturell

Die XML-Struktur dieses Elements lautet:

``` syntax
<psf:Feature name="psk:JobOutputBin">
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

In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.



| Name                                   | Datentyp          | Einheit                  | Unterstützte Werte                                                                                                                                                                      | Zusammenfassung                                                                             |
|----------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| \_Optionname\_<br/>              | Zeichenfolge<br/>  | Buchstaben<br/> | Gültiger vollqualifizierte Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert. Wenn kein Namespace angegeben wird, wird der Standardnamespace angenommen.<br/> | Der Name der Option.<br/>                                                  |
| \_IdentityOptionValue\_<br/>     | Zeichenfolge<br/>  | –<br/>        | TRUE, FALSE<br/>                                                                                                                                                               | Definiert eine Option, die diese Funktion deaktiviert, wenn sie ausgewählt wird.<br/>        |
| \_BinTypeValue\_<br/>            | Zeichenfolge<br/>  | –<br/>        | MailBox, Sorter, Stacker, Finisher, None.<br/>                                                                                                                                  | Gibt den allgemeinen Typ des Papierkorbs an.<br/>                                   |
| \_MediaSheetCapacityValue\_<br/> | integer<br/> | Blätter<br/>     | Maximal zulässige ganzzahlige Einschränkung des Geräts.<br/>                                                                                                                              | Gibt die Medienkapazität in der Anzahl der Seiten (vollständige Ebene) des Papierkorbs an.<br/> |



 

## <a name="extensible-markup-language-xml-content"></a>Extensible Markup Language (XML)-Inhalt

Die Schlüsselwörter für das öffentliche Druckschema werden im https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords -Namespace definiert. Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:

``` syntax
<psf:Feature name="psk:JobOutputBin">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
    <psf:ScoredProperty name="psk:BinType">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>  
    </psf:ScoredProperty>
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

 

 




