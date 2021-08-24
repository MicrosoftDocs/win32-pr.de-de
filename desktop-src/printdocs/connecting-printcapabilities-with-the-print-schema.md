---
description: Erfahren Sie mehr über das allgemeine PrintCapabilities-Schema, das die Struktur, den Zweck und die Verwendung der verschiedenen Elementtypen abdeckt.
ms.assetid: 2f6c51a3-003c-4d68-9e4d-9be5d325a477
title: Verbinden von PrintCapabilities mit dem Druckschema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65b82efc36798cc39439ff1dcf30d10c02b33aaa7ca4b0e92be5ce3e305875dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119720150"
---
# <a name="connecting-printcapabilities-with-the-print-schema"></a>Verbinden von PrintCapabilities mit dem Druckschema

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

Das allgemeine PrintCapabilities-Schema deckt die Struktur, den Zweck und die Verwendung der verschiedenen Elementtypen ab. Sie gibt das Namensattribut an, das zum Definieren bestimmter Instanzen jedes Elementtyps verwendet wird. Es gibt an, dass PrintCapabilities-Autoren Instanzen von Elementen verwenden können, die durch die Schlüsselwörter des Druckschemas definiert sind, oder sie können ihre eigenen privat definierten Instanzen einführen, solange diese privat definierten Instanzen in einem Namespace definiert sind, der eindeutig als ihre eigenen identifiziert wird. (PrintCapabilities-Autoren können auch Instanzen verwenden, die zuvor in einem anderen privaten Namespace definiert wurden.)

Das Dokument Print Schema Keywords definiert die spezifischen Instanzen der einzelnen Elementtypen, die in PrintCapabilities-Dokumenten und in PrintTickets verwendet werden können. Außerdem werden deren Zweck und Verwendung dokumentiert. Das Dokument Print Schema Keywords definiert auch Instanzen mehrerer Elementtypen wie folgt:

-   Eigenschaften- und Untereigenschafteninstanzen, die sich im Stammverzeichnis des PrintCapabilities-Dokuments befinden

    -   Diese Elemente beschreiben die verschiedenen Aspekte und Funktionen des Geräts und stellen ein allgemeines Vokabular für die Beschreibung von Geräten bereit.

-   Eigenschaften- und Untereigenschafteninstanzen, die untergeordnete Elemente von Feature-Elementen sind

    -   Diese Elemente beschreiben verschiedene Aspekte im Zusammenhang mit einem bestimmten Feature.

-   Eigenschaften- und Untereigenschafteninstanzen, die untergeordnete Elemente von Option-Elementen sind

    -   Diese Elemente beschreiben die verschiedenen Aspekte und Funktionen des Geräts, die von der für ein bestimmtes Feature ausgewählten Option abhängig sind. Diese können durch Eigenschafteninstanzen ersetzt werden, die sich im Stammverzeichnis des PrintCapabilities-Dokuments befinden, bieten jedoch in einigen Fällen zusätzlichen Komfort. Weitere Informationen finden Sie unter [Hinzufügen von Eigenschafteninstanzen.](adding-property-instances.md)

<!-- -->

-   ScoredProperty-Instanzen

    -   ScoredProperty-Instanzen definieren die Sprache, die zum Charakterisieren einer Option verwendet wird. Die in den Druckschemaschlüsselwörtern definierten ScoredProperty-Instanzen ermöglichen es, dass Optionsinstanzen, die von vielen verschiedenen Parteien geschrieben wurden, für viele Geräte portierbar und von jedem anderen Gerätetreiber, PrintCapabilities- oder PrintTicket-Anbieter verstanden werden können.

-   ScoredProperty Value-Instanzen

    -   Diese Value-Instanzen werden aus demselben Grund bereitgestellt, aus dem Auch ScoredProperty-Instanzen bereitgestellt werden.

-   Funktionsinstanzen

    -   Jede Option muss zu einem bestimmten Feature gehören, sodass das Feature selbst definiert werden muss.

-   ParameterDef-Instanzen

    -   Eine parameterDef-Instanz, die mit Schlüsselwörtern für Druckschemas bereitgestellt wird, definiert auch einen Wert für jede darin enthaltene Eigenschaft. Der PrintCapabilities-Anbieter kann die Value-Instanzen für die Eigenschafteninstanzen ändern, die geändert werden können. Informationen dazu, welche Eigenschafteninstanzen geändert werden können und welche nicht geändert werden können (sind unveränderlich), finden Sie unter [ParameterDef- und ParameterInit-Elemente.](parameterdef-and-parameterinit-elements.md)

Beachten Sie unbedingt, dass das PrintCapabilities-Schema keine Option-Instanzen benennt. Optionsinstanzen sind ausschließlich durch ihre ScoredProperty-Instanzen gekennzeichnet, die als Ganzes übernommen werden. Ein häufiges Missverständnis besteht darin, dass die Verwendung des Attributs "name" zum Definieren einer Option Optionsinstanzen identifiziert, dies ist jedoch falsch. Optionselemente müssen für gleichgeordnete Optionsinstanzen nicht eindeutig sein, und es wird auch nicht das Attribut "name" verwendet, um eine erforderliche Option zu definieren.

Das Dokument Print Schema Keywords definiert einen Standardnamespace, zu dem alle Instanznamenattribute in den PrintCapabilities- und PrintTicket-Schemas gehören. Alle Elementtyptags und XML-Attribute, die von den Elementtypen verwendet werden, gehören ebenfalls zu diesem Namespace.

Für jede im PrintCapabilities-Schema definierte Instanz gibt das PrintCapabilities-Schema sowohl das Name-Attribut als auch den Speicherort der Instanz an. Der Anbieter und der Client müssen beide beibehalten, wenn diese Instanz im PrintCapabilities-Dokument oder im PrintTicket verwendet wird.

Im Dokument Print Schema Keywords (Schlüsselwörter des Druckschemas) werden einige Instanzen als obligatorisch gekennzeichnet. Diese Instanzen müssen in jedem PrintCapabilities-Dokument angezeigt werden und ordnungsgemäß mit gültigen Werten initialisiert werden. Alle Instanzen in den Druckschemaschlüsselwörtern, die nicht als obligatorisch festgelegt sind, sind optional.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



