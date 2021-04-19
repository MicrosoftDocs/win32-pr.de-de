---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 8169b74f-13e0-4f6b-81e2-1824d932ee50
title: Wichtige Eigenschaften Instanzen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ad3f58c099913b129ee7be0337ecab3343a5e5e
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106353645"
---
# <a name="important-property-instances"></a>Wichtige Eigenschaften Instanzen

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Damit ein Printworks-Client ein vernünftiges PrintTicket erstellen kann, muss das Printworks-Dokument bestimmte Eigenschaften von Funktions Instanzen sowie Options Instanzen innerhalb des Features bereitstellen. Ein generisches Benutzeroberflächen Modul benötigt solche Informationen, um eine Benutzeroberfläche zu erstellen. Dies erfordert wiederum, dass die Schlüsselwörter des Druck Schemas einige Eigenschaften Instanzen definieren, die als untergeordnete Elemente von Feature-und Option-Elementen angezeigt werden.

Funktionselemente können die folgende Eigenschaft enthalten.



| Eigenschaft                  | Werte                                 | Zweck                                                                                                                                                                                                                                                                                                       |
|---------------------------|----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SelectionType <br/> | Pickone<br/> Pickmany<br/> | Gibt die Anzahl der Optionen an, die für diese Funktion zu einem bestimmten Zeitpunkt ausgewählt werden können, entweder eine (pickone) oder mehr als eine (pickmany). Der Client kann diese Informationen verwenden, um ein Print Ticket zu erstellen. Diese Informationen betreffen das Verhalten der Benutzeroberfläche sowie die PrintTicket-Validierung durch den Anbieter.<br/> |



 

Options Elemente können die folgende Eigenschaft enthalten.



| Eigenschaft                   | Werte                           | Zweck                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identityoption <br/> | Richtig<br/> False<br/> | Das Auswählen der identityoption-Eigenschaft wird so interpretiert, dass diese Funktion deaktiviert wird. Eine Funktion, die eine SelectionType-Eigenschaft enthält, deren Wert pickmany ist, muss auch eine Option enthalten, die über eine identityoption-Eigenschaft verfügt. Der UI-Code (oder der Client, der ein Print Ticket erstellt) muss alle anderen Optionen deaktivieren, wenn die identityoption-Eigenschaft ausgewählt ist.<br/> |



 

Die Elemente "Feature", "Option" und "ParameterDef" können die folgende Eigenschaft enthalten.



| Eigenschaft              | Werte                          | Zweck                                                                                                                                                                                                                                                                                                                                     |
|-----------------------|---------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DisplayUI <br/> | Anzeigen<br/> Ausblenden<br/> | Gibt an, ob das übergeordnete Element in der Benutzeroberfläche angezeigt werden soll. Anzeigen gibt an, dass das Element in der Benutzeroberfläche angezeigt werden soll. Hide gibt an, dass das Element nicht in der Benutzeroberfläche angezeigt werden soll. Wenn diese Eigenschaft nicht für ein Element definiert ist, wird die Standardinterpretation angezeigt, was bedeutet, dass das Element angezeigt wird.<br/> |



 

Die Elemente "Feature", "Option" und "ParameterDef" können die folgende Eigenschaft enthalten.



| Eigenschaft                | Wert             | Zweck                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DisplayName <br/> | Zeichenfolge<br/> | Gibt die Anzeige Zeichenfolge für das übergeordnete Element an und überschreibt den Standard anzeigen Amen. Kann von printfunktionalitäten-Anbietern verwendet werden, um einen lokalisierten und benutzerfreundlichen anzeigen Amen zu präsentieren. Der Standardwert für den anzeigen Amen ist das Name-Attribut für das übergeordnete Element. <br/> Im Fall von Option-Elementen muss die Display Name-Eigenschaft vorhanden sein, wenn das Name-Attribut nicht angegeben wird.<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Druck Schema Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




