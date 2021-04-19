---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: fe6bd921-cbf3-4cca-afae-82d3822206ba
title: PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3d2e225eb38584e290db55c33594be80d0d7999
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106370363"
---
# <a name="printticket"></a>PrintTicket

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Ein PrintTicket-Element ist das Stamm Element des PrintTicket-Dokuments. Ein PrintTicket-Element enthält alle Auftrags Formatierungsinformationen, die für die Ausgabe eines Auftrags erforderlich sind.

## <a name="element-tag"></a>Elementtag

<PrintTicket>

## <a name="xml-attributes"></a>XML-Attribute

In der folgenden Tabelle werden die XML-Attribute aufgelistet, die sich möglicherweise auf dieses Element beziehen.



| XML-Attribut      | Details                                                                                                                                                                                   |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| version<br/> | Gibt die Version des Schemas an, das Elementtypen und deren Struktur definiert, ein Literaltyp vom Typ Integer. Die aktuelle Schema Version ist "1". Dieses Attribut ist erforderlich. <br/> |



 

Weitere Informationen finden Sie im Abschnitt [XML-Attribute](xml-attributes.md) .

## <a name="element-information"></a>Elementinformationen

In der folgenden Tabelle werden die Elemente aufgelistet, die übergeordnete Elemente dieses Elements sein können, die Elemente, die möglicherweise untergeordnete Elemente dieses Elements sind, sowie alle Einschränkungen für das Element selbst.



| Category                   | Details                                                                                                            |
|----------------------------|--------------------------------------------------------------------------------------------------------------------|
| Übergeordnete Elemente<br/> | Nur Dokument Stamm.<br/>                                                                                     |
| Untergeordnete Elemente<br/>  | *Feature* (0 (null) oder mehr)<br/> *Parameterinit* (0 (null) oder mehr)<br/> *Property* (0 (null) oder mehr)<br/> |
| Dieses Element<br/>    | Es sind keine Zeichendaten zulässig.<br/> Doppelte untergeordnete gleich geordnete Elemente sind nicht zulässig.<br/>                  |



 

## <a name="configuration-dependencies"></a>Konfigurations Abhängigkeiten

Konfigurations Abhängigkeiten gelten nur für Elemente in einem printfunktionalitäten-Dokument.

## <a name="example"></a>Beispiel

Siehe [PrintTicket-Beispiel](printticket-example.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Druck Schema Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




