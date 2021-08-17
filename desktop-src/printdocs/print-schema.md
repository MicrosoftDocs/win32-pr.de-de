---
description: In dieser Übersicht werden das Druckschema und Links zu Referenzthemen zum Druckschema beschrieben. Das Druckschema enthält die Druckschemaschlüsselwörter und das Framework.
ms.assetid: d746bdd1-96c2-41f5-ad99-0b51c8ee8731
title: Legacydruckschemareferenz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 540496004534dff3e66ce1c30415ccec14c6d7b31c59ecf2f79905c25d5e7861
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118470857"
---
# <a name="legacy-print-schema-reference"></a>Legacydruckschemareferenz

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

Das Druckschema und verwandte Technologien sind in den Versionen Microsoft .NET Framework 3.0, Microsoft Windows Vista und höher verfügbar.

Das Druckschema stellt ein XML-basiertes Format zum Ausdrücken und Organisieren eines großen Satzes von Eigenschaften bereit, die entweder ein Auftragsformat oder PrintCapabilities in einer hierarchisch strukturierten Weise beschreiben.

Das Druckschema ist ein Oberbegriff, der zwei Komponenten umfasst: die Druckschemaschlüsselwörter und das Druckschemaframework. Das Dokument Print Schema Keywords (Druckschemaschlüsselwörter) ist ein öffentliches Schema, das eine Reihe von Elementinstanzen definiert, die zum Beschreiben von Geräteattributen und zum Formatieren von Druckauftragen verwendet werden können. Das Druckschemaframework ist ein öffentliches Schema, das eine hierarchisch strukturierte Auflistung von XML-Elementtypen definiert und angibt, wie die Elementtypen zusammen verwendet werden können.

Die Schlüsselwörter für Druckschema und das Druckschemaframework bilden die Grundlage für zwei Druckschematechnologien, das PrintCapabilities-Schema und das PrintTicket-Schema.

Es ist wichtig zu beachten, dass eines der Ziele des Druckschemas darin besteht, Schemaerweiterungen durch Anbieter zu unterstützen. Das heißt, Anbieter sind nicht darauf beschränkt, nur die Property-, Feature-, Option- oder ParameterInit-Instanzen zu verwenden, die in den Druckschemaschlüsselwörtern in den Technologien definiert sind, die auf dem Druckschemaframework basieren. Anbieterspezifische Elementinstanzen können innerhalb von Elementinstanzen, die in den Schlüsselwörtern für Druckschemas definiert sind, frei durchsetzt werden. Die einzige Anforderung besteht darin, dass anbieterspezifische (d. h. private) Eigenschafteninstanzen zu einem Namespace gehören müssen, der dem Anbieter eindeutig zugeordnet ist.

-   [Drucken des Schemahintergrunds](print-schema-background.md)

-   [Print Schema-Related Technologies](print-schema-related-technologies.md)

-   [Im Druckschema verwendete Begriffe](terms-used-in-the-print-schema.md)

-   [Syntax des Druckschemas](syntax-of-the-print-schema.md)

-   [Zusammenfassung der Elementtypen](summary-of-element-types.md)

-   [Druckschemaframework](print-schema-framework.md)

-   [Öffentliche Schlüsselwörter des Druckschemas](print-schema-public-keywords.md)

-   [PrintCapabilities-Schema und Dokumenterstellung](printcapabilities-schema-and-document-construction.md)

-   [PrintTicket-Schema und Dokumenterstellung](printticket-schema-and-document-construction.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



