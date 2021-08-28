---
description: Erfahren Sie mehr über einige der Funktionen und Informationen, die das PrintCapabilities-Dokument nicht bereitstellen soll.
ms.assetid: 87a897cd-d3aa-488a-b129-9837d3500d0d
title: Was ein PrintCapabilities-Dokument nicht ist
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 180c303a21dbed39908d87831a1e01e2965b09a68e1e23a6e1f8793e247556f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119718540"
---
# <a name="what-a-printcapabilities-document-is-not"></a>Was ein PrintCapabilities-Dokument nicht ist

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

Es lohnt sich, einige der Funktionen und Informationen aufzulisten, die das PrintCapabilities-Dokument nicht bereitstellen soll.

Ein PrintCapabilities-Dokument:

-   Stellt keine mehrwertigen (konfigurationsabhängigen) Daten dar.

    Jedes PrintCapabilities-Dokument wird für eine bestimmte Konfiguration erstellt. Keine Eigenschaft oder ScoredProperty im Dokument kann einen Wert aufweisen, der von der jeweiligen Konfiguration abhängt. In der anfänglichen Schemaversion muss der PrintCapabilities-Anbieter die Eingabe PrintTicket verarbeiten und ein PrintCapabilities-Dokument erstellen, das Eigenschaftswerte enthält, die für die im PrintTicket angegebene Konfiguration geeignet sind.

-   Enthält keine Einschränkungsinformationen.

    Das PrintCapabilities-Dokument gibt nicht an, welche Konfigurationen zulässig und welche nicht zulässig sind. In der anfänglichen Schemaversion muss der PrintCapabilities-Anbieter alle Informationen speichern, die zum Überprüfen von Konfigurationen erforderlich sind, eine Methode bereitstellen, die die Eingabe printTicket überprüft, und ein korrigiertes PrintTicket zurückgeben, falls das angegebene PrintTicket gegen eine oder mehrere Einschränkungen verstößt.

-   Enthält keine dynamischen Geräteinformationen.

    Es ist zu viel Aufwand beim Erstellen des PrintCapabilities-Dokuments erforderlich, damit es verwendet werden kann, um sich schnell ändernde Statusinformationen wie Freihandebenen, verbleibendes Papier in jeder Leiste oder Papierstaus zu speichern.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



