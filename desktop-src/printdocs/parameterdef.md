---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: cb00edc9-2c8a-446d-989b-a4429ee8f544
title: ParameterDef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 697d8ff89f9aa3c9c95bea9995e18e521a17596c
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106350599"
---
# <a name="parameterdef"></a>ParameterDef

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Ein ParameterDef-Element definiert die gültigen Merkmale von Parameter Eingaben. Der Wert wird mithilfe eines parameterinit-Elements eingegeben.

## <a name="element-tag"></a>Elementtag

<ParameterDef>

## <a name="xml-attributes"></a>XML-Attribute

In der folgenden Tabelle werden die XML-Attribute aufgelistet, die sich möglicherweise auf dieses Element beziehen.



| XML-Attribut   | Details                                                                                                                                                                          |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| name<br/> | Definiert einen eindeutigen Namen für den Parameter im Kontext des aktuellen Dokuments. Doppelte ParameterDef-namens Attribute renderdas printfunktionalitäten-Dokument ist ungültig.<br/> |



 

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
<td>PrintCapabilities <br/></td>
</tr>
<tr class="even">
<td>Untergeordnete Elemente<br/></td>
<td>Eigenschaft (ein oder mehrere Elemente)<br/> Die folgenden Standard Eigenschafts Elemente müssen als Inhalt eines ParameterDef-Elements angezeigt werden. <br/>
<ul>
<li>DataType <br/></li>
<li>DefaultValue <br/></li>
<li>Obligatorisch. <br/></li>
<li>MaxLength oder MaxValue<br/></li>
<li>MinLength oder MinValue<br/></li>
<li>Mehr <br/></li>
<li>UnitType <br/></li>
</ul></td>
</tr>
<tr class="odd">
<td>Dieses Element<br/></td>
<td>Es sind keine Zeichendaten zulässig.<br/> Doppelte untergeordnete gleich geordnete Elemente sind nicht zulässig.<br/></td>
</tr>
</tbody>
</table>



 

\*Erforderlich, wenn DataType Integer oder Decimal ist. Optional, wenn DataType eine Zeichenfolge ist.

## <a name="configuration-dependencies"></a>Konfigurations Abhängigkeiten

Ein ParameterDef und der zugehörige Inhalt einer beliebigen Schachtelungs Ebene verfügen möglicherweise nicht über Konfigurations Abhängigkeiten.

## <a name="example"></a>Beispiel

Im folgenden Beispiel werden alle erforderlichen Eigenschaften Elemente für diesen Parameter festgelegt. Das Beispiel in [parameterinit](parameterinit.md) veranschaulicht, wie dieser Parameter initialisiert wird.

``` syntax
<psf:ParameterDef name="psk:PageMediaSizeMediaSizeHeight">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">microns</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">594106</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">152400</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">152400</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Optional</psf:Value>
  </psf:Property>
</psf:ParameterDef>
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Druck Schema Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




