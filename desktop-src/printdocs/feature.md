---
description: Überprüfen Sie Featureelemente, die eine Liste von Options- und Property-Elementen enthalten, die ein Geräteattribut, eine Auftragsformatierungseinstellung oder ein anderes relevantes Merkmal beschreiben.
ms.assetid: 5a6553c2-f322-47e2-bbc8-44f6541f1288
title: Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b28ab7e8cc69ecc9ba3956fbae3c5278baace8cf
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120635"
---
# <a name="feature"></a>Funktion

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

Ein Feature-Element enthält eine vollständige Liste der Option- und Property-Elemente, die ein Geräteattribut, eine Auftragsformatierungseinstellung oder ein anderes relevantes Merkmal vollständig beschreiben.

## <a name="element-tag"></a>Elementtag

<Feature>

## <a name="xml-attributes"></a>XML-Attribute

In der folgenden Tabelle sind die XML-Attribute aufgeführt, die zu diesem Element gehören können.



| XML-Attribut   | Details                                                                                              |
|-----------------|------------------------------------------------------------------------------------------------------|
| name<br/> | Enthält den Namen des Features, entweder ein Standardfeature oder ein privat definiertes Feature. <br/> |



 

Weitere Informationen finden Sie im Abschnitt [XML-Attribute.](xml-attributes.md)

## <a name="element-information"></a>Elementinformationen

In der folgenden Tabelle sind die Elemente aufgeführt, die möglicherweise die untergeordneten Elemente dieses Elements sind, sowie alle Einschränkungen für das Element selbst.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Category</th>
<th>Details</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Übergeordnete Elemente<br/></td>
<td>PrintCapabilities <br/> PrintTicket <br/> Funktion<br/></td>
</tr>
<tr class="even">
<td>Untergeordnete Elemente<br/></td>
<td>Eine der folgenden Gruppen:<br/>
<ul>
<li><em>Feature</em> (null oder mehr)<br/></li>
<li><em>Option</em> (mindestens eine Option)<br/></li>
<li><em>Eigenschaft</em> (null oder mehr)<br/></li>
</ul>
oder <br/>
<ul>
<li>Feature (mindestens ein <em>Feature)</em><br/></li>
<li><em>Option</em> (null oder mehr)<br/></li>
<li><em>Eigenschaft</em> (null oder mehr)<br/></li>
</ul></td>
</tr>
<tr class="odd">
<td>Dieses Element<br/></td>
<td>Es sind keine Zeichendaten zulässig.<br/> Doppelte untergeordnete Optionselemente, die gleichgeordnete Elemente sind, sind zulässig. Doppelte Namensattributverknüpfungen zulässig. <br/></td>
</tr>
</tbody>
</table>



 

## <a name="configuration-dependencies"></a>Konfigurationsabhängigkeiten

Featureelemente weisen möglicherweise keine Konfigurationsabhängigkeiten auf.

## <a name="element-usage"></a>Elementverwendung

### <a name="relationship-to-xml-attributes"></a>Beziehung zu XML-Attributen

In der Feature-/Optionsdarstellung wird ein Geräteattribut durch ein Feature-Element dargestellt. Das Geräteattribut wird durch das Name-Attribut im Feature-Element des Geräteattributs eindeutig identifiziert, wie im folgenden Beispiel. In diesem Beispiel lautet das Geräteattribut Auflösung.

``` syntax
<Feature name="Resolution" />
```

Das Druckschema definiert einen Satz von Namensattributen für bestimmte Featureinstanzen. Diese Namensattribute dienen zum Identifizieren eines Satzes vordefinierter Featureinstanzen, die bestimmten konfigurierbaren Geräteattributen zugeordnet sind. Diese Funktionsinstanznamen sollten nach Möglichkeit verwendet werden, da sie die Portabilität Ihres PrintCapabilities-Dokuments und der von ihnen abgeleiteten PrintTickets erhöhen. Privat definierte Featureinstanzen können eingeführt werden, wenn bestimmte Geräteattribute keiner der schemadefinierte Featureinstanzen entsprechen. Informationen zur Syntax für Namensattribute und zu den Konventionen, die für schemadefinierte und private Namen gelten, finden Sie unter [XML-Attribute.](xml-attributes.md)

### <a name="relationship-to-option-element"></a>Beziehung zum Option-Element

Jeder der möglichen Zustände wird durch ein Option-Element dargestellt. Jede Option-Definition enthält mindestens ein ScoredProperty-Element, das den dargestellten Zustand eindeutig beschreibt oder kennzeichnet. Das Verfahren zum Erstellen von Optionsdefinitionen wird unter [Optionsdefinitionen](option-definitions.md)beschrieben. Alle Option-Elemente, die einem bestimmten Feature-Element zugeordnet sind, befinden sich als untergeordnete Elemente des Feature-Elements.

### <a name="subfeatures"></a>Unterfeatures

Das Druckschemaframework ermöglicht auch die hierarchische Gruppierung von Featureelementen. Das heißt, ein Feature-Element kann selbst ein oder mehrere untergeordnete Feature-Elemente (Unterfeatures) enthalten. Dies kann nützlich sein, um verwandte Featureelemente zu organisieren, oder für Featureelemente, die Aspekte eines Gerätefeatures steuern. Ein Beispiel ist ein Gerät, das Das Stapling unterstützt. Ein solches Gerät kann dem Benutzer die Wahl geben, wo sich die Klammer befindet, z. B. in der oberen linken Ecke, in der oberen rechten Ecke oder am oberen Rand oder am linken Rand. Die Benutzeroberfläche für dieses Gerät sollte dem Benutzer zuerst die höchsten Auswahlmöglichkeiten bieten können. In diesem Fall ist dies die Verwendung von Stapling. Erst nachdem sich der Benutzer für die Verwendung von Stapling entschieden hat, sollte ihm eine zweite Auswahlebene angezeigt werden, also einen festen Standort. Eine Featurehierarchie fügt die zusätzliche Struktur hinzu, die eine solche Benutzeroberfläche ermöglicht. Das Druckschemaframework ermöglicht untergeordneten Features ihre eigenen untergeordneten Features, wodurch eine unbegrenzte Schachtelungsebene ermöglicht wird.

Mit dem Druckschemaframework können Option-Elemente auch auf der gleichen Ebene wie Unterfeatures angezeigt werden. das heißt, als gleichgeordnete Elemente innerhalb desselben übergeordneten Feature-Elements. Dadurch kann der Benutzer die übergeordnete Entscheidung treffen (ob stapling verwendet werden soll), bevor er die Teilfeatureauswahl trifft. In diesem Beispiel enthält das Feature-Stammelement "Klammer" möglicherweise zwei Optionselemente, "On" und "Off", sowie ein Unterfeature mit dem Namen "Location".

## <a name="example"></a>Beispiel

``` syntax
<psf:Feature name="psk:JobOutputBin">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option constrained="psk:None">
    <psf:ScoredProperty name="psk:Bin">
      <psf:Value xsi:type="xs:string">SorterBin</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSheetCapacity">
      <psf:Value xsi:type="xs:integer">100</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




