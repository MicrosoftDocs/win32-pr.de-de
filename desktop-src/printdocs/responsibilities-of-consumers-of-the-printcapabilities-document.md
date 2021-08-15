---
description: Consumer von PrintCapabilities-Dokumenten haben bestimmte Verpflichtungen, die sie erfüllen müssen, bevor sie ein PrintCapabilities-Dokument verwenden können.
ms.assetid: 2377763b-9b3b-49ec-ab6c-476b8009ddcb
title: Verantwortlichkeiten der Consumer des PrintCapabilities-Dokuments
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f49cd8f843bfa39a4313b0958fe9874f1263403e3fb3b2f22e2c965927bf6f25
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118470252"
---
# <a name="responsibilities-of-consumers-of-the-printcapabilities-document"></a>Verantwortlichkeiten der Consumer des PrintCapabilities-Dokuments

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

Consumer von PrintCapabilities-Dokumenten haben bestimmte Verpflichtungen, die sie erfüllen müssen, bevor sie ein PrintCapabilities-Dokument verwenden können. Die folgenden Anforderungen gelten für Clients eines PrintCapabilities-Dokuments.

-   Sie dürfen keine syntaktisch gültigen PrintCapabilities ablehnen oder nicht verarbeiten. Das heißt, jedes PrintCapabilities-Dokument, das dem PrintCapabilities-Schema entspricht.

-   Sie müssen in der Lage sein, das unerwartete Vorhandensein oder Fehlen von privat definierten Inhalten zu umgehen. Dies schließt privat definierten Inhalt ein, der in Instanzen von durch das Druckschema definierten Elementen angezeigt wird.

-   Sie müssen in der Lage sein, optionalen Inhalt des Druckschemas zu umgehen, der nicht vorhanden ist.

-   Sie müssen wissen, wann ein neues Dokument angefordert werden soll.

    -   Werte von Eigenschafteninstanzen sind konfigurationsabhängig (also momentaufnahmeabhängig). Sie müssen die Momentaufnahme aktualisieren, wenn Sie auf eine Eigenschaftsinstanz zugreifen.

    -   Funktions-, Options- und ScoredProperty-Instanzen, die in ein PrintTicket kopiert werden sollen, sind definitionsgemäß statisch. Das heißt, sie sind nicht (und dürfen nicht) von der Gerätekonfiguration abhängig sein. Wenn Sie auf Instanzen dieser Typen zugreifen, müssen Sie kein neues PrintCapabilities-Dokument abrufen, wenn sich die Konfiguration ändert.

-   Consumer von PrintCapabilities, bei denen es sich um Benutzeroberflächenclients handelt, müssen in der Lage sein, Informationen in einem PrintCapabilities-Dokument zu verwenden, um eine Benutzeroberfläche zu erstellen und ein gültiges PrintTicket aus der Benutzerauswahl zu erstellen. Dazu gehört das Wissen, welche ParameterInit-Instanzen angegeben werden müssen, und das Überprüfen der angegebenen Instanzen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



