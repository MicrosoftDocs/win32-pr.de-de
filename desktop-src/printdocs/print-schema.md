---
description: In dieser Übersicht werden das Druckschema und Links zu Referenzthemen zum Druckschema beschrieben. Das Druckschema enthält die Druckschemaschlüsselwörter und das Framework.
ms.assetid: d746bdd1-96c2-41f5-ad99-0b51c8ee8731
title: Legacy-Druckschemareferenz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81a8f417d20913563cfd4a52ba51d21b516e73f0
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407133"
---
# <a name="legacy-print-schema-reference"></a>Legacy-Druckschemareferenz

Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

Das Druckschema und die zugehörigen Technologien sind in Microsoft .NET Framework 3.0, Microsoft Windows Vista und späteren Versionen verfügbar.

Das Druckschema bietet ein XML-basiertes Format zum Ausdrücken und Organisieren einer großen Gruppe von Eigenschaften, die entweder ein Auftragsformat oder PrintCapabilities in einer hierarchisch strukturierten Weise beschreiben.

Das Druckschema ist ein Oberbegriff, der zwei Komponenten umfasst: die Print Schema Keywords und das Print Schema Framework. Das Dokument Print Schema Keywords ist ein öffentliches Schema, das einen Satz von Elementinstanzen definiert, die zum Beschreiben von Geräteattributen und zum Formatieren von Druckaufträgen verwendet werden können. Das Druckschemaframework ist ein öffentliches Schema, das eine hierarchisch strukturierte Auflistung von XML-Elementtypen definiert und angibt, wie die Elementtypen zusammen verwendet werden können.

Die Print Schema Keywords und das Print Schema Framework bilden die Grundlage für zwei Druckschema-bezogene Technologien, das PrintCapabilities-Schema und das PrintTicket-Schema.

Beachten Sie, dass eines der Ziele des Druckschemas die Unterstützung von Schemaerweiterungen durch Anbieter ist. Das heißt, anbieter sind nicht darauf beschränkt, nur die Eigenschaften-, Feature-, Options- oder ParameterInit-Instanzen zu verwenden, die in den Druckschemaschlüsselwörtern in den auf dem Druckschemaframework erstellten Technologien definiert sind. Anbieterspezifische Elementinstanzen können in Elementinstanzen, die in den Schlüsselwörtern für Druckschemas definiert sind, frei interspersiert werden. Die einzige Anforderung ist, dass anbieterspezifische (d. h. private) Eigenschafteninstanzen zu einem Namespace gehören müssen, der dem Anbieter eindeutig zugeordnet ist.

-   [Hintergrund des Druckschemas](print-schema-background.md)

-   [Print Schema-Related Technologies](print-schema-related-technologies.md)

-   [Im Druckschema verwendete Begriffe](terms-used-in-the-print-schema.md)

-   [Syntax des Druckschemas](syntax-of-the-print-schema.md)

-   [Zusammenfassung der Elementtypen](summary-of-element-types.md)

-   [Druckschemaframework](print-schema-framework.md)

-   [Öffentliche Schlüsselwörter für Das Schema drucken](print-schema-public-keywords.md)

-   [PrintCapabilities-Schema und Dokumentkonstruktion](printcapabilities-schema-and-document-construction.md)

-   [PrintTicket-Schema und Dokumentkonstruktion](printticket-schema-and-document-construction.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



