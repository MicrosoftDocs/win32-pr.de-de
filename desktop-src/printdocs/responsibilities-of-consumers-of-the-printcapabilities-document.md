---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 2377763b-9b3b-49ec-ab6c-476b8009ddcb
title: Zuständigkeiten von Kunden des Printworks-Dokuments
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b74cfc1885ecc5599365bc6eadcef30ef4c4ae3
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106366381"
---
# <a name="responsibilities-of-consumers-of-the-printcapabilities-document"></a>Zuständigkeiten von Kunden des Printworks-Dokuments

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Consumer von printfähigkeiten-Dokumenten haben bestimmte Verpflichtungen, die Sie einhalten müssen, bevor Sie ein Printworks-Dokument verwenden können. Die folgenden Anforderungen gelten für Clients eines Printworks-Dokuments.

-   Sie dürfen keine syntaktisch gültigen Print-Funktionen ablehnen oder nicht verarbeiten. Das heißt, alle printfunktionalitäten-Dokumente, die dem printfunktionalitäten-Schema entsprechen.

-   Sie müssen in der Lage sein, das unerwartete vorhanden sein oder Fehlen von Privat definierten Inhalten zu umgehen. Dies schließt privat definierte Inhalte ein, die in Instanzen von Schema definierten Elementen vom Druck Schema angezeigt werden.

-   Sie müssen den optionalen Inhalt des Druck Schemas umgehen können, der nicht vorhanden ist.

-   Sie müssen wissen, wann ein neues Dokument angefordert werden muss.

    -   Werte von Eigenschaften Instanzen sind Konfigurations abhängig (daher von der Momentaufnahme abhängig). Sie müssen die Momentaufnahme aktualisieren, wenn Sie auf eine Eigenschaften Instanz zugreifen.

    -   Feature-, Option-und ScoredProperty-Instanzen, die in ein Print Ticket kopiert werden sollen, sind definitionsgemäß statisch. Das heißt, Sie sind nicht (und dürfen nicht sein), abhängig von der Gerätekonfiguration. Wenn Sie auf Instanzen dieser Art zugreifen, ist es nicht erforderlich, dass Sie ein neues printfunktionalitäten-Dokument erhalten, wenn sich die Konfiguration ändert.

-   Consumer von Print-Funktionen, die Benutzeroberflächen Clients sind, müssen in der Lage sein, Informationen in einem printfunktionalitäten-Dokument zu verwenden, um eine Benutzeroberfläche zu erstellen und ein gültiges PrintTicket aus der Benutzer Auswahl zu erstellen. Dazu gehört das wissen, welche parameterinit-Instanzen angegeben werden müssen, und die Überprüfung der angegebenen Instanzen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Druck Schema Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



