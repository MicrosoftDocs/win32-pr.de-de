---
description: Erfahren Sie mehr über das ParameterDef-Element, das die gültigen Merkmale der Parametereingabe definiert. Der Wert wird mithilfe eines ParameterInit-Elements eingegeben.
ms.assetid: cb00edc9-2c8a-446d-989b-a4429ee8f544
title: ParameterDef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4d7a0c8b86a8fef2d71cae1135eadca2c361e2062555d80a3a19f862f94ad7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119033978"
---
# <a name="parameterdef"></a>ParameterDef

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

Ein ParameterDef-Element definiert die gültigen Merkmale der Parametereingabe. Der Wert wird mithilfe eines ParameterInit-Elements eingegeben.

## <a name="element-tag"></a>Elementtag

<ParameterDef>

## <a name="xml-attributes"></a>XML-Attribute

In der folgenden Tabelle sind die XML-Attribute aufgeführt, die möglicherweise zu diesem Element gehören.



| XML-Attribut   | Details                                                                                                                                                                          |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| name<br/> | Definiert einen eindeutigen Namen für den Parameter im Kontext des aktuellen Dokuments. Doppelte ParameterDef-Namensattribute machen das PrintCapabilities-Dokument ungültig.<br/> |



 

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
<td>PrintCapabilities <br/></td>
</tr>
<tr class="even">
<td>Untergeordnete Elemente<br/></td>
<td>Eigenschaft (ein oder mehrere Elemente)<br/> Die folgenden Standardeigenschaftenelemente müssen als Inhalt eines ParameterDef-Elements angezeigt werden. <br/>
<ul>
<li>DataType <br/></li>
<li>DefaultValue <br/></li>
<li>Obligatorisch. <br/></li>
<li>MaxLength oder MaxValue<br/></li>
<li>MinLength oder MinValue<br/></li>
<li>Mehrere* <br/></li>
<li>Unittype <br/></li>
</ul></td>
</tr>
<tr class="odd">
<td>Dieses Element<br/></td>
<td>Es sind keine Zeichendaten zulässig.<br/> Doppelte untergeordnete gleichgeordnete Elemente sind nicht zulässig.<br/></td>
</tr>
</tbody>
</table>



 

\*Erforderlich, wenn DataType ganzzahlig oder dezimal ist. Optional, wenn DataType eine Zeichenfolge ist.

## <a name="configuration-dependencies"></a>Konfigurationsabhängigkeiten

Eine ParameterDef und ihr Inhalt auf einer beliebigen Schachtelungsebene weisen möglicherweise keine Konfigurationsabhängigkeiten auf.

## <a name="example"></a>Beispiel

Im folgenden Beispiel werden alle erforderlichen Property-Elemente für diesen Parameter festgelegt. Das Beispiel in [ParameterInit](parameterinit.md) veranschaulicht, wie dieser Parameter initialisiert wird.

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

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




