---
description: Erfahren Sie mehr über das Property-Element in Dokumenten und beim Drucken. Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification(Spezifikation des Druckschemas).
ms.assetid: 14631336-adfc-4edf-81ef-63e426d41c87
title: Eigenschaft (Dokumente und Drucken)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e43b52c054972ee0ee2b8a535021581c05e7d96
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120295"
---
# <a name="property-documents-and-printing"></a>Eigenschaft (Dokumente und Drucken)

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

Ein Property-Element deklariert ein Gerät, eine Auftragsformatierung oder eine andere relevante Eigenschaft, deren Name durch das Name-Attribut angegeben wird. Ein Value-Element wird verwendet, um der Eigenschaft einen Wert zuzuweisen.

Eine Eigenschaft kann komplex sein und möglicherweise mehrere Untereigenschaften enthalten. Untereigenschaften werden auch durch Property-Elemente dargestellt.

## <a name="element-tag"></a>Elementtag

<Property>

## <a name="xml-attributes"></a>XML-Attribute

In der folgenden Tabelle sind die XML-Attribute aufgeführt, die möglicherweise zu diesem Element gehören.



| XML-Attribut   | Details                                                                                                                    |
|-----------------|----------------------------------------------------------------------------------------------------------------------------|
| name<br/> | Enthält das Namensattribut der Eigenschaft, bei der es sich entweder um eine Standardeigenschaft oder eine privat definierte Eigenschaft handelt. <br/> |



 

Weitere Informationen finden Sie im Abschnitt [XML-Attribute.](xml-attributes.md)

## <a name="element-information"></a>Elementinformationen

In der folgenden Tabelle sind die Elemente aufgeführt, die möglicherweise die untergeordneten Elemente dieses Elements sind, sowie alle Einschränkungen für das Element selbst.



| Category                   | Details                                                                                                                                                                                                                                                                                                                      |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Übergeordnete Elemente<br/> | PrintCapabilities <br/> Funktion<br/> PrintTicket<br/> Option<br/> ParameterDef<br/> Eigenschaft<br/> ScoredProperty<br/>                                                                                                                                                              |
| Untergeordnete Elemente<br/>  | Das System weist der Reihenfolge der Elemente keine Bedeutung zu. Wenn Clients sich dafür entscheiden, eine gewisse Bedeutung in der Reihenfolge der Elemente zuzuordnen, können sie dies auch tun. <br/> *Eigenschaftswert* (mindestens ein *Wert)* (null oder mehr)<br/> oder <br/> *Eigenschaftswert* (null oder mehr) (mindestens ein *Wert)*<br/> |
| Dieses Element<br/>    | Es sind keine Zeichendaten zulässig.<br/> Doppelte untergeordnete Value-Elemente, die gleichgeordnete Elemente sind, sind zulässig.<br/>                                                                                                                                                                                                        |



 

## <a name="configuration-dependencies"></a>Konfigurationsabhängigkeiten

Eine Eigenschaft kann Konfigurationsabhängigkeiten aufweisen, es sei denn, sie wird in einem ParameterDef-Element angezeigt.

## <a name="element-usage"></a>Elementverwendung

Zusätzlich zum Erscheinen in Feature- und Optionselementen können Eigenschaftselemente auf der Stammebene der jeweiligen zugrunde liegenden Technologien angezeigt werden. Das Druckschema definiert einen Satz von Eigenschaftselementen, die verwendet werden können, um ein Gerät auf portable Weise zu beschreiben. Wenn diese Eigenschaften jedoch nicht ihren Anforderungen als PrintCapabilities-Anbieter entsprechen (in der Regel weil das unterstützte Gerät neue Aspekte aufweist, die vom Druckschema nicht erwartet werden), können Sie Ihre eigenen privaten Property-Elemente einführen. Sie können die von einer öffentlichen Eigenschaft bereitgestellten Informationen erweitern oder erweitern, indem Sie eine oder mehrere private Untereigenschaften als Elementinhalt der öffentlichen Eigenschaft hinzufügen.

Eigenschaftselemente werden mithilfe eines XML-Elementtags <Property> definiert. Jeder Eigenschaft wird anhand ihres Namensattributs ein Name zugewiesen. Der Name muss ein XML-QName sein und der Namespacekonvention entsprechen. Weitere Informationen finden Sie unter [XML-Attribute.](xml-attributes.md) Das Eigenschaftsnamenattribut und seine Position innerhalb der Hierarchie übergeordneter Property-Elemente (wenn es sich um eine Untereigenschaft handelt) identifizieren die Eigenschaft eindeutig im PrintCapabilities-Dokument oder printTicket.

Eine Eigenschaft kann ein oder mehrere Value-Elemente oder mindestens ein untergeordnetes Property-Element (als Untereigenschaften bezeichnet) oder eine Kombination aus beiden enthalten. Untereigenschaften sind nützlich, wenn die Eigenschaft selbst aus mehreren Komponenten besteht. Beispielsweise kann eine "ConsumableColor"-Eigenschaft über die Komponenten "C", "M" und "Y" verfügen.

## <a name="example"></a>Beispiel

``` syntax
<psf:Property name="psk:DisplayName">
  <psf:Value xsi:type="xs:string">6</psf:Value>
</psf:Property>
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




