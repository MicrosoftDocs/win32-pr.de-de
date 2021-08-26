---
description: Hier finden Sie Informationen zum PrintTicket-Element. Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification (Spezifikation des Druckschemas).
ms.assetid: fe6bd921-cbf3-4cca-afae-82d3822206ba
title: PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a38638083f6a6aabd0290fa3466a30fd50f7375
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884893"
---
# <a name="printticket"></a>PrintTicket

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

Ein PrintTicket-Element ist das Stammelement des PrintTicket-Dokuments. Ein PrintTicket-Element enthält alle Auftragsformatierungsinformationen, die zum Ausgeben eines Auftrags erforderlich sind.

## <a name="element-tag"></a>Elementtag

&lt;PrintTicket&gt;

## <a name="xml-attributes"></a>XML-Attribute

In der folgenden Tabelle sind die XML-Attribute aufgeführt, die möglicherweise zu diesem Element gehören.



| XML-Attribut      | Details                                                                                                                                                                                   |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| version<br/> | Gibt die Version des Schemas an, das Elementtypen und deren Struktur definiert, ein Literal vom Typ integer. Die aktuelle Schemaversion ist "1". Dieses Attribut ist erforderlich. <br/> |



 

Weitere Informationen finden Sie im Abschnitt [XML-Attribute.](xml-attributes.md)

## <a name="element-information"></a>Elementinformationen

In der folgenden Tabelle sind die Elemente aufgeführt, die möglicherweise die untergeordneten Elemente dieses Elements sind, sowie alle Einschränkungen für das Element selbst.



| Category                   | Details                                                                                                            |
|----------------------------|--------------------------------------------------------------------------------------------------------------------|
| Übergeordnete Elemente<br/> | Nur Dokumentstamm.<br/>                                                                                     |
| Untergeordnete Elemente<br/>  | *Feature* (null oder mehr)<br/> *ParameterInit* (null oder mehr)<br/> *Eigenschaft* (null oder mehr)<br/> |
| Dieses Element<br/>    | Es sind keine Zeichendaten zulässig.<br/> Doppelte untergeordnete gleichgeordnete Elemente sind nicht zulässig.<br/>                  |



 

## <a name="configuration-dependencies"></a>Konfigurationsabhängigkeiten

Konfigurationsabhängigkeiten gelten nur für Elemente in einem PrintCapabilities-Dokument.

## <a name="example"></a>Beispiel

Siehe [PrintTicket-Beispiel.](printticket-example.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




