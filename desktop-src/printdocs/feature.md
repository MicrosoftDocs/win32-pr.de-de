---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 5a6553c2-f322-47e2-bbc8-44f6541f1288
title: Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad89655181563e2da3a8d4841b1d90ecd4e6ac07
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106366568"
---
# <a name="feature"></a>Funktion

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Ein Feature-Element enthält eine vollständige Liste der Optionen und Eigenschaften Elemente, die ein Geräte Attribut, eine Einstellung für die Auftrags Formatierung oder ein anderes relevantes Merkmal vollständig beschreiben.

## <a name="element-tag"></a>Elementtag

<Feature>

## <a name="xml-attributes"></a>XML-Attribute

In der folgenden Tabelle werden die XML-Attribute aufgelistet, die sich möglicherweise auf dieses Element beziehen.



| XML-Attribut   | Details                                                                                              |
|-----------------|------------------------------------------------------------------------------------------------------|
| name<br/> | Enthält den Namen der Funktion, entweder ein Standard Feature oder eine privat definierte Funktion. <br/> |



 

Weitere Informationen finden Sie im Abschnitt [XML-Attribute](xml-attributes.md) .

## <a name="element-information"></a>Elementinformationen

In der folgenden Tabelle werden die Elemente aufgelistet, die übergeordnete Elemente dieses Elements sein können, die Elemente, die möglicherweise untergeordnete Elemente dieses Elements sind, sowie alle Einschränkungen für das Element selbst.



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
<li><em>Feature</em> (0 (null) oder mehr)<br/></li>
<li><em>Option</em> (mindestens eine)<br/></li>
<li><em>Property</em> (0 (null) oder mehr)<br/></li>
</ul>
oder <br/>
<ul>
<li><em>Feature</em> (mindestens ein Element)<br/></li>
<li><em>Option</em> (0 (null) oder mehr)<br/></li>
<li><em>Property</em> (0 (null) oder mehr)<br/></li>
</ul></td>
</tr>
<tr class="odd">
<td>Dieses Element<br/></td>
<td>Es sind keine Zeichendaten zulässig.<br/> Doppelte untergeordnete Options Elemente, die gleich geordnete Elemente sind, sind zulässig. Doppelte namens Verknüpfungen sind zulässig. <br/></td>
</tr>
</tbody>
</table>



 

## <a name="configuration-dependencies"></a>Konfigurations Abhängigkeiten

Funktionselemente verfügen möglicherweise nicht über Konfigurations Abhängigkeiten.

## <a name="element-usage"></a>Element Verwendung

### <a name="relationship-to-xml-attributes"></a>Beziehung zu XML-Attributen

In der Funktions-/Option-Darstellung wird ein Geräte Attribut durch ein Feature-Element dargestellt. Das Device-Attribut wird durch das Name-Attribut im Feature-Element des Geräte Attributs eindeutig identifiziert, wie im folgenden Beispiel gezeigt. In diesem Beispiel ist das Geräte Attribut "Resolution".

``` syntax
<Feature name="Resolution" />
```

Das Druck Schema definiert einen Satz von namens Attributen für bestimmte Funktions Instanzen. Diese namens Attribute dienen zum Identifizieren eines Satzes von vordefinierten Funktions Instanzen, die bestimmten konfigurierbaren Geräte Attributen zugeordnet sind. Diese featureinstanznamen sollten immer dann verwendet werden, wenn Sie die Portabilität Ihres printfunktionalitäten-Dokuments und der von ihnen abgeleiteten PrintTickets erhöhen. Instanzen von Privat definierten Funktionen können eingeführt werden, wenn bestimmte Geräte Attribute keiner der Schema definierten Funktions Instanzen entsprechen. Weitere Informationen über die Syntax für namens Attribute und die Konventionen, die für Schema definierte und privat definierte Namen gelten, finden Sie unter [XML-Attribute](xml-attributes.md).

### <a name="relationship-to-option-element"></a>Beziehung zu Option-Element

Jeder der möglichen Zustände wird durch ein Option-Element dargestellt. Jede Options Definition enthält ein oder mehrere ScoredProperty-Elemente, die den dargestellten Zustand eindeutig beschreiben oder charakterisieren. Das Verfahren, das zum Erstellen von Options Definitionen verwendet wird, wird in [options Definitionen](option-definitions.md)beschrieben. Alle Options Elemente, die einem bestimmten Feature-Element zugeordnet sind, befinden sich als untergeordnete Elemente des Feature-Elements.

### <a name="subfeatures"></a>Unter Features

Das Print Schema-Framework ermöglicht außerdem, dass Featureelemente hierarchisch gruppiert werden. Das heißt, ein Feature-Element kann ein oder mehrere untergeordnete Funktionselemente (unter Funktionen) enthalten. Dies kann nützlich sein, um verwandte Funktionselemente zu organisieren, oder für Featureelemente, die die Aspekte eines Geräte Features steuern. Ein Beispiel hierfür ist ein Gerät, das Heften unterstützt. Ein solches Gerät bietet dem Benutzer möglicherweise die Wahl, wo der Stapel zu suchen ist, z. b. in der oberen linken Ecke oder in der oberen rechten Ecke oder am oberen Rand oder entlang des linken Rands. Die Benutzeroberfläche (User Interface, UI) für dieses Gerät sollte dem Benutzer die höchste verfügbare Auswahl präsentieren können. in diesem Fall ist es in diesem Fall, ob Heften verwendet werden soll. Erst nachdem der Benutzer sich für die Verwendung von Heften entschieden hat, sollte er eine zweite Ebene von Auswahlmöglichkeiten haben. Eine Funktions Hierarchie fügt die zusätzliche Struktur hinzu, die eine solche Benutzeroberfläche ermöglicht. Das Print Schema-Framework ermöglicht es, dass untergeordnete Funktionen über eigene untergeordnete unter Features verfügen, wodurch eine unbegrenzte Schachtelungs Ebene ermöglicht wird.

Das Print Schema Framework ermöglicht außerdem, dass Options Elemente auf derselben Ebene wie unter Funktionen angezeigt werden. Das heißt, als gleich geordnete Elemente innerhalb desselben übergeordneten Funktions Elements. Dadurch kann der Benutzer die allgemeine Entscheidung treffen (unabhängig davon, ob das Heften verwendet wird), bevor die Auswahl der untergeordneten Funktion aktiviert wird. In diesem Beispiel enthält das Root-Funktionselement "Staple" möglicherweise zwei Options Elemente: "on" und "Off" sowie eine Unterfunktion mit dem Namen "stapleloation".

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

[Druck Schema Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




