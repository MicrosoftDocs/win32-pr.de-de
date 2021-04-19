---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: d746bdd1-96c2-41f5-ad99-0b51c8ee8731
title: Ältere Druck Schema Referenz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 881e986501950108c06e1e92303d13dc06265aae
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106363900"
---
# <a name="legacy-print-schema-reference"></a>Ältere Druck Schema Referenz

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Das Druck Schema und zugehörige Technologien sind in den Microsoft .NET Framework 3,0, Microsoft Windows Vista und späteren Versionen verfügbar.

Das Druck Schema bietet ein XML-basiertes Format zum Ausdrücken und organisieren eines großen Satzes von Eigenschaften, die entweder ein Auftrags Format oder Print-Funktionen hierarchisch strukturiert beschreiben.

Beim Druck Schema handelt es sich um einen Oberbegriff, der zwei Komponenten, die Schlüsselwörter des Druck Schemas und das Druck Schema Framework umfasst. Das Schlüsselwort des Print Schema-Schlüssel Worts ist ein öffentliches Schema, das einen Satz von Element Instanzen definiert, die zum Beschreiben von Geräte Attributen und zum Formatieren von Druckaufträgen verwendet werden können. Das Print Schema-Framework ist ein öffentliches Schema, das eine hierarchisch strukturierte Auflistung von XML-Elementtypen definiert, und gibt an, wie die Elementtypen gleichzeitig verwendet werden können.

Die Druck Schema Schlüsselwörter und das Druck Schema-Framework bilden die Grundlage für zwei Druck Schema bezogene Technologien, das printforms-Schema und das PrintTicket-Schema.

Beachten Sie, dass eines der Ziele des Druck Schemas darin besteht, Schema Erweiterungen durch Anbieter zu unterstützen. Das heißt, die Anbieter sind nicht auf die Verwendung von Eigenschaften, Features, Optionen oder parameterinit-Instanzen beschränkt, die in den Schlüsselwörtern des Print-Schemas in den Technologien definiert sind, die auf dem Print Schema-Framework basieren. Anbieterspezifische Element Instanzen können innerhalb von Element Instanzen, die in den Schlüsselwörtern des Print-Schemas definiert sind, frei durchsucht werden. Die einzige Voraussetzung ist, dass anbieterspezifische (private) Eigenschaften Instanzen zu einem Namespace gehören müssen, der dem Anbieter eindeutig zugeordnet ist.

-   [Hintergrund des Druck Schemas](print-schema-background.md)

-   [Druck Schema-Related Technologien](print-schema-related-technologies.md)

-   [Begriffe, die im Druck Schema verwendet werden](terms-used-in-the-print-schema.md)

-   [Syntax des Druck Schemas](syntax-of-the-print-schema.md)

-   [Zusammenfassung der Element Typen](summary-of-element-types.md)

-   [Print Schema Framework](print-schema-framework.md)

-   [Öffentliche Schlüsselwörter des Druck Schemas](print-schema-public-keywords.md)

-   [Printfunktionalitäten-Schema und Dokument Erstellung](printcapabilities-schema-and-document-construction.md)

-   [PrintTicket-Schema und Dokument Erstellung](printticket-schema-and-document-construction.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Druck Schema Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



