---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 92e9bce1-d58e-40a4-9721-832d7c3bc2b2
title: Zuständigkeiten von printfunktionalitäten-Anbietern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 586bbf355f7b62f8f9c8b3f3b0c59714cdd6ade5
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106370357"
---
# <a name="responsibilities-of-printcapabilities-providers"></a>Zuständigkeiten von printfunktionalitäten-Anbietern

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Printfunktionalitäten-Anbieter müssen einen minimalen Satz von Funktionen unterstützen, die von der PrintTicket/printfunktionalitäten-Anbieter Schnittstelle impliziert werden. Diese Funktionen sind hier aufgeführt.

-   Sie müssen die Richtung der propagieren? XML-Attribut, wenn es im entsprechenden Kontext angezeigt wird und einen gültigen Wert für diesen Kontext enthält.

-   Sie müssen ein printfunktionalitäten-Dokument generieren, das dem printfunktionalitäten-Schema entspricht und die im Druck Schema angegebenen Anforderungen erfüllt.

-   Sie müssen in der Lage sein, ein gültiges PrintTicket zu erkennen.

-   Sie müssen in der Lage sein, ein Print Ticket zu interpretieren und die spezifische Konfiguration zu verstehen, die Sie repräsentiert.

-   Sie müssen in der Lage sein, zu bestimmen, ob diese Konfiguration Einschränkungs Konflikte enthält.

-   Sie müssen in der Lage sein, ein ungültiges oder in Konflikt stehender PrintTicket zu ändern, indem Sie die am wenigsten bedeutende Änderung vornehmen, damit Sie sowohl gültig als auch ohne Konflikte ist.

-   Sie müssen in der Lage sein, ein printfunktionalitäten-Dokument für eine bestimmte Gerätekonfiguration zu generieren.

-   Sie müssen in der Lage sein, eine Standardkonfiguration oder PrintTicket zu generieren.

-   Sie müssen in der Lage sein, ein printfunktionalitäten-Dokument zu generieren, das der Standardkonfiguration entspricht.

-   Sie müssen einen vom Gerätetreiber definierten Prozess zur Durchführung von Optionen implementieren, der die Übereinstimmung der Übereinstimmung zwischen zwei Options Instanzen, die zu derselben Funktion gehören, bestimmen können. Dieser Algorithmus wird in der PrintTicket-Überprüfung verwendet.

Zusätzlich zu den vorstehenden Anforderungen muss das printfunktionalitäten-Dokument gültige und korrekte Werte für jedes XML-Attribut (z. b. "eingeschränkt") jeder Option enthalten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Druck Schema Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



