---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 14631336-adfc-4edf-81ef-63e426d41c87
title: Eigenschaft (Dokumente und Drucken)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9fb4a057b2cf7795262b595c59f9da0343fdf12
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "104351868"
---
# <a name="property-documents-and-printing"></a>Eigenschaft (Dokumente und Drucken)

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Ein Property-Element deklariert ein Gerät, eine Auftrags Formatierung oder eine andere relevante Eigenschaft, deren Name durch das Name-Attribut angegeben wird. Ein Value-Element wird verwendet, um der Eigenschaft einen Wert zuzuweisen.

Eine Eigenschaft kann komplex sein und möglicherweise mehrere untergeordnete Eigenschaften enthalten. Unter Eigenschaften werden auch durch Eigenschafts Elemente dargestellt.

## <a name="element-tag"></a>Elementtag

<Property>

## <a name="xml-attributes"></a>XML-Attribute

In der folgenden Tabelle werden die XML-Attribute aufgelistet, die sich möglicherweise auf dieses Element beziehen.



| XML-Attribut   | Details                                                                                                                    |
|-----------------|----------------------------------------------------------------------------------------------------------------------------|
| name<br/> | Enthält das Name-Attribut der Eigenschaft, bei der es sich entweder um eine Standard Eigenschaft oder eine privat definierte Eigenschaft handelt. <br/> |



 

Weitere Informationen finden Sie im Abschnitt [XML-Attribute](xml-attributes.md) .

## <a name="element-information"></a>Elementinformationen

In der folgenden Tabelle werden die Elemente aufgelistet, die übergeordnete Elemente dieses Elements sein können, die Elemente, die möglicherweise untergeordnete Elemente dieses Elements sind, sowie alle Einschränkungen für das Element selbst.



| Category                   | Details                                                                                                                                                                                                                                                                                                                      |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Übergeordnete Elemente<br/> | PrintCapabilities <br/> Funktion<br/> PrintTicket<br/> Option<br/> ParameterDef<br/> Eigenschaft<br/> ScoredProperty<br/>                                                                                                                                                              |
| Untergeordnete Elemente<br/>  | Das System weist der Reihenfolge der Elemente keine Bedeutung zu. Wenn Clients eine gewisse Bedeutung in der Reihenfolge der Elemente festlegen möchten, können Sie dies tun. <br/> *Eigenschaft* (mindestens ein *Wert* ) (0 (null) oder mehr)<br/> oder <br/> *Eigenschafts* Wert (null oder mehr) (mindestens ein *Wert* )<br/> |
| Dieses Element<br/>    | Es sind keine Zeichendaten zulässig.<br/> Doppelte untergeordnete Element Elemente, die gleich geordnete Elemente sind, sind zulässig.<br/>                                                                                                                                                                                                        |



 

## <a name="configuration-dependencies"></a>Konfigurations Abhängigkeiten

Eine Eigenschaft kann Konfigurations Abhängigkeiten aufweisen, außer wenn Sie in einem ParameterDef-Element angezeigt wird.

## <a name="element-usage"></a>Element Verwendung

Eigenschaften Elemente können nicht nur innerhalb von Funktions-und Options Elementen angezeigt werden, sondern auch auf der Stamm Ebene der jeweiligen zugrunde liegenden Technologien. Das Druck Schema definiert einen Satz von Eigenschaften Elementen, die verwendet werden können, um ein Gerät portabel zu beschreiben. Wenn diese Eigenschaften jedoch nicht Ihren Anforderungen als Print-Funktions Anbieter genügt (in der Regel, weil das Gerät, das unterstützt wird, über neue Aspekte verfügt, die vom Druck Schema nicht erwartet werden), können Sie eigene private Eigenschaften Elemente einführen. Sie können die von einer öffentlichen Eigenschaft bereitgestellten Informationen verbessern oder vertiefen, indem Sie eine oder mehrere private unter Eigenschaften als Element Inhalt der Public-Eigenschaft hinzufügen.

Eigenschafts Elemente werden mithilfe eines XML-Element Tags definiert <Property> . Jeder Eigenschaft wird anhand des Namens Attributs ein Name zugewiesen. Der Name muss ein XML-QName sein und muss der Namespace Konvention entsprechen. Weitere Informationen finden Sie unter [XML-Attribute](xml-attributes.md). Das Eigenschaftsnamen Attribut und seine Position in der Hierarchie der übergeordneten Eigenschaften Elemente (wenn es sich um eine untergeordnete Eigenschaft handelt) identifizieren die Eigenschaft innerhalb des Printworks-Dokuments oder des PrintTicket eindeutig.

Eine Eigenschaft kann ein oder mehrere value-Elemente oder ein oder mehrere untergeordnete Eigenschaften Elemente (als untergeordnete Eigenschaften bezeichnet) oder eine Kombination aus beidem enthalten. Unter Eigenschaften sind nützlich, wenn die Eigenschaft selbst aus mehreren Komponenten besteht. Beispielsweise kann eine "consumablecolor"-Eigenschaft "C"-, "M"-und "Y"-Komponenten enthalten.

## <a name="example"></a>Beispiel

``` syntax
<psf:Property name="psk:DisplayName">
  <psf:Value xsi:type="xs:string">6</psf:Value>
</psf:Property>
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Druck Schema Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




