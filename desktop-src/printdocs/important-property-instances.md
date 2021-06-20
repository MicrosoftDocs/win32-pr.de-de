---
description: Damit ein Client ein PrintTicket erstellen kann, muss das PrintCapabilities-Dokument Eigenschaften von Featureinstanzen und Optionsinstanzen im Feature bereitstellen.
ms.assetid: 8169b74f-13e0-4f6b-81e2-1824d932ee50
title: Wichtige Eigenschafteninstanzen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4691b73b1206ee092c171b213a3815925b7f53c6
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409123"
---
# <a name="important-property-instances"></a>Wichtige Eigenschafteninstanzen

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

Damit ein PrintCapabilities-Client ein angemessenes PrintTicket erstellen kann, muss das PrintCapabilities-Dokument bestimmte Eigenschaften von Featureinstanzen sowie Optionsinstanzen innerhalb des Features bereitstellen. Ein generisches Benutzeroberflächenmodul erfordert solche Informationen, um eine Benutzeroberfläche zu erstellen. Dies erfordert wiederum, dass die Druckschemaschlüsselwörter einige Eigenschafteninstanzen definieren, die als untergeordnete Elemente von Feature- und Optionselementen angezeigt werden.

Featureelemente können die folgende Eigenschaft enthalten.



| Eigenschaft                  | Werte                                 | Zweck                                                                                                                                                                                                                                                                                                       |
|---------------------------|----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SelectionType <br/> | PickOne<br/> PickMany<br/> | Gibt die Anzahl der Optionen an, die für dieses Feature zu einem bestimmten Zeitpunkt ausgewählt werden können, entweder eine (PickOne) oder mehrere Optionen (PickMany). Der Client kann diese Informationen verwenden, um ein PrintTicket zu erstellen. Diese Informationen wirken sich auf das Benutzeroberflächenverhalten und die PrintTicket-Überprüfung durch den Anbieter aus.<br/> |



 

Optionselemente können die folgende Eigenschaft enthalten.



| Eigenschaft                   | Werte                           | Zweck                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IdentityOption <br/> | True<br/> Falsch<br/> | Das Auswählen der IdentityOption-Eigenschaft wird so interpretiert, dass diese Funktion deaktiviert wird. Ein Feature, das eine SelectionType-Eigenschaft enthält, deren Wert PickMany ist, muss auch eine Option mit einer IdentityOption-Eigenschaft enthalten. Der Benutzeroberflächencode (oder der Client, der ein PrintTicket erstellt) muss jede andere Option deaktivieren, wenn die IdentityOption-Eigenschaft ausgewählt ist.<br/> |



 

Die Elemente Feature, Option und ParameterDef können die folgende Eigenschaft enthalten.



| Eigenschaft              | Werte                          | Zweck                                                                                                                                                                                                                                                                                                                                     |
|-----------------------|---------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DisplayUI <br/> | Anzeigen<br/> Ausblenden<br/> | Gibt an, ob das übergeordnete Element auf der Benutzeroberfläche angezeigt werden soll. Show gibt an, dass das Element auf der Benutzeroberfläche angezeigt werden soll. Ausblenden gibt an, dass das Element nicht auf der Benutzeroberfläche angezeigt werden soll. Wenn diese Eigenschaft nicht für ein Element definiert ist, lautet die Standardinterpretation Show, was bedeutet, dass das Element angezeigt wird.<br/> |



 

Die Elemente Feature, Option und ParameterDef können die folgende Eigenschaft enthalten.



| Eigenschaft                | Wert             | Zweck                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DisplayName <br/> | Zeichenfolge<br/> | Gibt die Anzeigezeichenfolge für das übergeordnete Element an und überschreibt den Standardanzeigenamen. Kann von PrintCapabilities-Anbietern verwendet werden, um einen lokalisierten und benutzerfreundlichen Anzeigenamen darzustellen. Der Standardwert für den Anzeigenamen ist das Name-Attribut für das übergeordnete Element. <br/> Wenn bei Option-Elementen das Name-Attribut nicht angegeben wird, muss die DisplayName-Eigenschaft vorhanden sein.<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




