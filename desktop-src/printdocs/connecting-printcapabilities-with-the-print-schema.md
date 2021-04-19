---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 2f6c51a3-003c-4d68-9e4d-9be5d325a477
title: Verbinden von printfunktionen mit dem Druck Schema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17d2f5a34421dba2402bce1d6699f208fd58c799
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106366570"
---
# <a name="connecting-printcapabilities-with-the-print-schema"></a>Verbinden von printfunktionen mit dem Druck Schema

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Das allgemeine printfunktionalitäten-Schema deckt die Struktur, den Zweck und die Verwendung der verschiedenen Elementtypen ab. Sie gibt das Name-Attribut an, das verwendet wird, um bestimmte Instanzen der einzelnen Elementtypen zu definieren. Er gibt an, dass printfunktionalitäten-Autoren Instanzen von Elementen verwenden können, die durch die Schlüsselwörter des Print-Schemas definiert werden, oder Sie können Ihre eigenen privat definierten Instanzen einführen, sofern diese privat definierten Instanzen in einem Namespace definiert sind, der eindeutig als eigenständig identifiziert ist. (Printfunktionen-Autoren können auch Instanzen verwenden, die zuvor in einem anderen privaten Namespace definiert wurden.)

Das Dokument mit dem Schlüsselwort "Print Schema" definiert die spezifischen Instanzen der einzelnen Elementtypen, die in Printworks-Dokumenten und in PrintTickets verwendet werden können. Sie dokumentiert auch ihren Zweck und ihre Verwendung. Das Dokument mit den Schlüsselwörtern für den Druck Schema definiert auch Instanzen mehrerer Elementtypen wie folgt:

-   Eigenschaften-und unter Eigenschaften Instanzen, die sich im Stammverzeichnis des printfunktionalitäten-Dokuments befinden

    -   Diese Elemente beschreiben die verschiedenen Aspekte und Funktionen des Geräts und stellen ein gängiges Vokabular zum Beschreiben von Geräten bereit.

-   Eigenschaften-und unter Eigenschaften Instanzen, die untergeordnete Elemente von Funktions Elementen sind

    -   Diese Elemente beschreiben verschiedene Aspekte im Zusammenhang mit einer bestimmten Funktion.

-   Eigenschaften-und unter Eigenschaften Instanzen, die untergeordnete Elemente von Option-Elementen sind

    -   Diese Elemente beschreiben die verschiedenen Aspekte und Funktionen des Geräts, die von der Option abhängig sind, die für eine bestimmte Funktion ausgewählt ist. Diese können durch Eigenschaften Instanzen ersetzt werden, die sich im Stammverzeichnis des printfunktionalitäten-Dokuments befinden, aber in einigen Fällen zusätzliche Möglichkeiten bieten. Weitere Informationen finden Sie unter [Hinzufügen von Eigenschaften Instanzen](adding-property-instances.md).

<!-- -->

-   ScoredProperty-Instanzen

    -   ScoredProperty-Instanzen definieren die Sprache, die verwendet wird, um eine Option zu bezeichnen. Die in den Schlüsselwörtern "Print Schema" definierten ScoredProperty-Instanzen ermöglichen es, dass Options Instanzen, die von vielen verschiedenen Parteien geschrieben wurden, für viele Geräte portabel sind und von jedem anderen Gerätetreiber oder Print-Funktionen oder PrintTicket-Anbieter verstanden werden können.

-   ScoredProperty-Wert Instanzen

    -   Diese Wert Instanzen werden aus demselben Grund bereitgestellt, wie ScoredProperty-Instanzen bereitgestellt werden.

-   Funktions Instanzen

    -   Jede Option muss zu einer bestimmten Funktion gehören, sodass die Funktion selbst definiert werden muss.

-   ParameterDef-Instanzen

    -   Eine von einem Druck Schema-Schlüsselwort bereitgestellte ParameterDef-Instanz definiert auch einen Wert für jede darin enthaltene Eigenschaft. Der printfunktionalitäten-Anbieter kann die Wert Instanzen für die Eigenschaften Instanzen ändern, die geändert werden können. Informationen dazu, welche Eigenschaften Instanzen geändert werden können und welche nicht geändert werden können (sind unveränderlich), finden Sie unter [ParameterDef-und parameterinit-Elemente](parameterdef-and-parameterinit-elements.md).

Beachten Sie unbedingt, dass das printfunktionalitäten-Schema keine Options Instanzen nennt. Options Instanzen werden ausschließlich durch ihre ScoredProperty-Instanzen gekennzeichnet, die als Ganzes übernommen werden. Ein gängiges Missverständnis besteht darin, dass durch die Verwendung des "Name"-Attributs zum Definieren einer Option Options Instanzen identifiziert werden, dies jedoch nicht korrekt ist. Options Elemente müssen nicht eindeutig für gleich geordnete Options Instanzen sein, und es wird auch nicht das Attribut "Name" verwendet, um eine erforderliche Option zu definieren.

Das Dokument mit dem Schlüsselwort "Print Schema" definiert einen Standard Namespace, zu dem alle instanznamensattribute in den printfunktionalitäten-und PrintTicket-Schemas gehören. Alle Elementtyp Tags und XML-Attribute, die von den Elementtypen verwendet werden, gehören ebenfalls zu diesem Namespace.

Für jede Instanz, die im printfunktionalitäten-Schema definiert ist, gibt das printfunktionalitäten-Schema sowohl das Name-Attribut als auch den Speicherort der-Instanz an. Der Anbieter und der Client müssen beide beibehalten, wenn Sie diese Instanz in Ihrem Printworks-Dokument oder in PrintTicket verwenden.

Das Dokument mit dem Schlüsselwort "Print Schema" legt einige Instanzen als obligatorisch fest. Diese Instanzen müssen in jedem printfunktionalitäten-Dokument angezeigt werden und müssen ordnungsgemäß mit gültigen Werten initialisiert werden. Alle Instanzen in den Druck Schema Schlüsselwörtern, die nicht als obligatorisch gekennzeichnet sind, sind optional.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Druck Schema Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



