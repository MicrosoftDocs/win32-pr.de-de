---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 87a897cd-d3aa-488a-b129-9837d3500d0d
title: Das Dokument "printfunktionalitäten" ist nicht
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd6e18082a5e551f3997dad8b9688d84ff2f824a
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106353274"
---
# <a name="what-a-printcapabilities-document-is-not"></a>Das Dokument "printfunktionalitäten" ist nicht

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Es lohnt sich, einige der Funktionen und Informationen aufzulisten, die das Dokument printfunktionalitäten nicht bereitstellen soll.

Ein printfunktionalitäten-Dokument:

-   Stellt keine mehrwertigen (Konfigurations abhängigen) Daten dar.

    Jedes Dokument "printfunktionen" wird für eine bestimmte Konfiguration erstellt. Keine Eigenschaft oder ScoredProperty im Dokument kann über einen Wert verfügen, der von der jeweiligen Konfiguration abhängt. In der anfänglichen Schema Version muss der PrintValues-Anbieter das PrintTicket-Eingabeverfahren verarbeiten und ein PrintValues-Dokument erstellen, das die für die im PrintTicket angegebenen Konfigurationen geeigneten Eigenschaftswerte enthält.

-   Enthält keine Einschränkungs Informationen.

    Das Dokument printfunktionalitäten gibt nicht an, welche Konfigurationen zulässig sind und welche nicht zulässig sind. In der ersten Schema Version muss der printfunktionalitäten-Anbieter alle Informationen speichern, die zum Überprüfen von Konfigurationen erforderlich sind, eine Methode bereitstellen, die das PrintTicket-Eingabe Element überprüft, und ein korrigiertes Print Ticket zurückgeben, wenn das angegebene PrintTicket gegen eine oder mehrere Einschränkungen verstößt.

-   Enthält keine dynamischen Geräteinformationen.

    Es ist zu viel mehr Aufwand bei der Erstellung des printfunktionalitäten-Dokuments, damit es für die schnelle Änderung von Statusinformationen verwendet werden kann, wie z. b. Freihand Ebenen, verbleibende Papier in jeder Info Leiste oder Papierstau Status.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Druck Schema Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



