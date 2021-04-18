---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: b49e20b7-bd9e-4b8f-bb4a-bb1e99b0c417
title: Erstellen eines printfunktionalitäten-Dokuments
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ccb1adf4626254ba9f71c706ad7d4556a23aeb6
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106354919"
---
# <a name="creating-a-printcapabilities-document"></a>Erstellen eines printfunktionalitäten-Dokuments

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Nachdem ein Print Ticket überprüft wurde, kann es verwendet werden, um eine Momentaufnahme der Print-Funktionen zu erstellen. Der Anbieter muss über eine interne Darstellung für jede Eigenschaft verfügen, deren Wert von der Gerätekonfiguration abhängig ist. Wenn z. b. "spotpulse" eine Eigenschaft ist, die sowohl von der Auflösung als auch von den MediaType-Features abhängig ist, wird eine interne Darstellung von "spotpulse", die sich auf die verschiedenen Werte für "Resolution" und "MediaType" bezieht, in der folgenden Tabelle



| Lösung      | MediaType         | Spot-Durchmesser   |
|-----------------|-------------------|----------------|
| 300<br/>  | Kauf<br/>   | 520<br/> |
| 300<br/>  | Glanz<br/> | 350<br/> |
| 600<br/>  | Kauf<br/>   | 330<br/> |
| 600<br/>  | Glanz<br/> | 180<br/> |
| 1200<br/> | Kauf<br/>   | 250<br/> |
| 1200<br/> | Glanz<br/> | 100<br/> |



 

In diesem Beispiel muss der printfunktionalitäten-Anbieter das angegebene PrintTicket verwenden, um den richtigen Eintrag aus der internen Tabelle auszuwählen und diesen als Wert für die Eigenschaft "Spot-Durchmesser" zu melden. Dieser Vorgang wird für jede mehrwertige Eigenschaft (für jede Eigenschaft, deren Wert abhängig von der Konfiguration ist) wiederholt. Im Abschnitt [printfunktionalitäten-Schema und Dokument](printcapabilities-schema-and-document-construction.md) Erstellung werden die anderen Schritte beschrieben, die zum Erstellen einer Momentaufnahme der Print-Funktionen erforderlich sind.

Um eine Momentaufnahme des Standard Dokuments printfunktionalitäten zu erstellen, geben Sie der Methode, mit der printfunktionalitäten-Dokumente erstellt werden, ein Standardmäßiges Print Ticket (anstelle eines beliebigen PrintTicket).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Druck Schema Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




