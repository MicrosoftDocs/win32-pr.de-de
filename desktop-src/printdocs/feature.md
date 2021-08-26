---
description: Überprüfen Sie Featureelemente, die eine Liste von Option- und Property-Elementen enthalten, die ein Geräteattribut, eine Auftragsformatierungseinstellung oder ein anderes relevantes Merkmal beschreiben.
ms.assetid: 5a6553c2-f322-47e2-bbc8-44f6541f1288
title: Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3d35686674d08ea0ea4030648b06803919e5d07
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882499"
---
# <a name="feature"></a>Funktion

Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

Ein Feature-Element enthält eine vollständige Liste der Option- und Property-Elemente, die ein Geräteattribut, eine Auftragsformatierungseinstellung oder ein anderes relevantes Merkmal vollständig beschreiben.

## <a name="element-tag"></a>Elementtag

&lt;Feature&gt;

## <a name="xml-attributes"></a>XML-Attribute

In der folgenden Tabelle sind die XML-Attribute aufgeführt, die für dieses Element gelten können.



| XML-Attribut   | Details                                                                                              |
|-----------------|------------------------------------------------------------------------------------------------------|
| name<br/> | Enthält den Namen des Features, entweder ein Standardfeature oder ein privat definiertes Feature. <br/> |



 

Weitere Informationen finden Sie im Abschnitt [XML-Attribute.](xml-attributes.md)

## <a name="element-information"></a>Elementinformationen

In der folgenden Tabelle sind die Elemente, die diesem Element unter Umständen über- und unteren Elementen liegen können, die Elemente, die diesem Element unter umständen unter stehen, und alle Einschränkungen für das Element selbst aufgeführt.




| Category | Details | 
|----------|---------|
| Übergeordnete Elemente<br /> | PrintCapabilities <br /> PrintTicket <br /> Funktion<br /> | 
| Untergeordnete Elemente<br /> | Eine der folgenden Gruppen:<br /><ul><li><em>Feature</em> (null oder mehr)<br /></li><li><em>Option</em> (mindestens eine)<br /></li><li><em>Eigenschaft</em> (null oder mehr)<br /></li></ul>oder <br /><ul><li><em>Feature</em> (mindestens ein Feature)<br /></li><li><em>Option</em> (null oder mehr)<br /></li><li><em>Eigenschaft</em> (null oder mehr)<br /></li></ul> | 
| Dieses Element<br /> | Zeichendaten sind nicht zulässig.<br /> Doppelte untergeordnete Optionselemente, die gleichgeordnete Elemente sind, sind zulässig. Doppelte Namensattributverknüpfungen sind zulässig. <br /> | 




 

## <a name="configuration-dependencies"></a>Konfigurationsabhängigkeiten

Featureelemente verfügen möglicherweise nicht über Konfigurationsabhängigkeiten.

## <a name="element-usage"></a>Elementverwendung

### <a name="relationship-to-xml-attributes"></a>Beziehung zu XML-Attributen

In der Feature-/Optionsdarstellung wird ein Geräteattribut durch ein Feature-Element dargestellt. Das Geräteattribut wird wie im folgenden Beispiel durch das Name-Attribut im Feature-Element des Geräteattributs eindeutig identifiziert. In diesem Beispiel ist das Geräteattribut Resolution.

``` syntax
<Feature name="Resolution" />
```

Das Druckschema definiert einen Satz von Namensattributen für bestimmte Featureinstanzen. Diese Namensattribute dienen dazu, eine Reihe vordefinierter Featureinstanzen zu identifizieren, die bestimmten konfigurierbaren Geräteattributen zugeordnet sind. Diese Funktionsinstanznamen sollten nach Möglichkeit verwendet werden, da sie die Portabilität Ihres PrintCapabilities-Dokuments und der von ihnen abgeleiteten PrintTickets erhöhen. Privat definierte Featureinstanzen können eingeführt werden, wenn bestimmte Geräteattribute keinen der schemadefinierten Featureinstanzen entsprechen. Informationen zur Syntax für Namensattribute und zu den Konventionen, die für schemadefinierte und privat definierte Namen gelten, finden Sie unter [XML-Attribute](xml-attributes.md).

### <a name="relationship-to-option-element"></a>Beziehung zum Option-Element

Jeder der möglichen Zustände wird durch ein Option-Element dargestellt. Jede Optionsdefinition enthält ein oder mehrere ScoredProperty-Elemente, die zusammen den dargestellten Zustand eindeutig beschreiben oder charakterisieren. Das Verfahren zum Erstellen von Optionsdefinitionen wird unter [Optionsdefinitionen beschrieben.](option-definitions.md) Alle Optionselemente, die einem bestimmten Feature-Element zugeordnet sind, befinden sich als untergeordnete Elemente des Feature-Elements.

### <a name="subfeatures"></a>Unterfeatures

Das Druckschemaframework ermöglicht auch, Featureelemente hierarchisch zu gruppieren. Das heißt, ein Feature-Element kann selbst ein oder mehrere untergeordnete Feature-Elemente (Unterfeatures) enthalten. Dies kann nützlich sein, um verwandte Featureelemente zu organisieren, oder für Featureelemente, die Aspekte eines Gerätefeatures steuern. Ein Beispiel ist ein Gerät, das die Heftung unterstützt. Ein solches Gerät kann dem Benutzer die Wahl bieten, wo sich die Klammer befindet, z. B. in der oberen linken Ecke oder in der oberen rechten Ecke, am oberen Rand oder am linken Rand. Die Benutzeroberfläche (UI) für dieses Gerät sollte in der Lage sein, dem Benutzer zuerst die höchsten Auswahlmöglichkeiten zu bieten. In diesem Fall ist dies die Entscheidung, ob die Heftung verwendet werden soll. Erst nachdem sich der Benutzer entschieden hat, die Heftung zu verwenden, sollte ihm eine zweite Auswahlebene angezeigt werden, z. B. der Standort des Hefts. Eine Featurehierarchie fügt die zusätzliche Struktur hinzu, die eine solche Benutzeroberfläche ermöglicht. Das Druckschemaframework ermöglicht es Unterfeatures, über eigene untergeordnete Unterfeatures zu verfügen, wodurch eine unbegrenzte Schachtelungsebene ermöglicht wird.

Das Druckschemaframework ermöglicht auch, dass Options-Elemente auf der gleichen Ebene wie Unterfeatures angezeigt werden. das heißt, als gleichgeordnete Elemente innerhalb des gleichen übergeordneten Feature-Elements. Auf diese Weise kann der Benutzer die Entscheidung auf hoher Ebene treffen (ob die Heftung verwendet werden soll), bevor er die Unterfeatureauswahl treffen kann. In diesem Beispiel kann das Stammfeatureelement "Heft" die beiden Option-Elemente "On" und "Off" sowie ein Unterfeature namens "Solllocation" enthalten.

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

 

 




