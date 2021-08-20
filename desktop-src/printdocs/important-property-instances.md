---
description: Damit ein Client ein PrintTicket erstellen kann, muss das PrintCapabilities-Dokument Eigenschaften von Featureinstanzen und Optionsinstanzen im Feature bereitstellen.
ms.assetid: 8169b74f-13e0-4f6b-81e2-1824d932ee50
title: Wichtige Eigenschafteninstanzen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df644c44bc1c9c0c0b4c5bf457bdb253f5b91969c55dd26833c0e05dc66cc558
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119100551"
---
# <a name="important-property-instances"></a>Wichtige Eigenschafteninstanzen

Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

Damit ein PrintCapabilities-Client ein angemessenes PrintTicket erstellen kann, muss das PrintCapabilities-Dokument bestimmte Eigenschaften von Featureinstanzen sowie Optionsinstanzen innerhalb des Features bereitstellen. Ein generisches Benutzeroberflächenmodul erfordert solche Informationen, um eine Benutzeroberfläche zu erstellen. Dies erfordert wiederum, dass die Druckschemaschlüsselwörter einige Eigenschafteninstanzen definieren, die als untere Elemente der Elemente Feature und Option angezeigt werden.

Featureelemente können die folgende Eigenschaft enthalten.



| Eigenschaft                  | Werte                                 | Zweck                                                                                                                                                                                                                                                                                                       |
|---------------------------|----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SelectionType <br/> | PickOne<br/> PickMany<br/> | Gibt die Anzahl der Optionen an, die für dieses Feature zu einem bestimmten Zeitpunkt ausgewählt werden können, entweder eine (PickOne) oder mehrere (PickMany). Der Client kann diese Informationen verwenden, um ein PrintTicket zu erstellen. Diese Informationen wirken sich auf das Verhalten der Benutzeroberfläche sowie auf die PrintTicket-Überprüfung durch den Anbieter aus.<br/> |



 

Optionselemente können die folgende Eigenschaft enthalten.



| Eigenschaft                   | Werte                           | Zweck                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IdentityOption <br/> | Richtig<br/> Falsch<br/> | Die Auswahl der IdentityOption-Eigenschaft wird so interpretiert, dass sie "diese Funktion deaktivieren" bedeutet. Ein Feature, das eine SelectionType-Eigenschaft enthält, deren Wert PickMany ist, muss auch eine Option mit einer IdentityOption-Eigenschaft enthalten. Der Benutzeroberflächencode (oder der Client, der ein PrintTicket erstellt) muss die Auswahl einer anderen Option aufheben, wenn die IdentityOption-Eigenschaft ausgewählt ist.<br/> |



 

Feature-, Option- und ParameterDef-Elemente können die folgende Eigenschaft enthalten.



| Eigenschaft              | Werte                          | Zweck                                                                                                                                                                                                                                                                                                                                     |
|-----------------------|---------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DisplayUI <br/> | Anzeigen<br/> Ausblenden<br/> | Gibt an, ob das übergeordnete Element auf der Benutzeroberfläche angezeigt werden soll. Anzeigen gibt an, dass das Element auf der Benutzeroberfläche angezeigt werden soll. Ausblenden gibt an, dass das Element nicht auf der Benutzeroberfläche angezeigt werden soll. Wenn diese Eigenschaft für ein Element nicht definiert ist, ist die Standardinterpretation Show, was bedeutet, dass das Element angezeigt wird.<br/> |



 

Feature-, Option- und ParameterDef-Elemente können die folgende Eigenschaft enthalten.



| Eigenschaft                | Wert             | Zweck                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DisplayName <br/> | Zeichenfolge<br/> | Gibt die Anzeigezeichenfolge für das übergeordnete Element an und überschreiben den Standardanzeigenamen. Kann von PrintCapabilities-Anbietern verwendet werden, um einen lokalisierten und benutzerfreundlichen Anzeigenamen anzuzeigen. Der Standardwert des Anzeigenamens ist das Namensattribut für das übergeordnete Element. <br/> Wenn im Fall von Option-Elementen das Name-Attribut nicht angegeben wird, muss die DisplayName-Eigenschaft vorhanden sein.<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




