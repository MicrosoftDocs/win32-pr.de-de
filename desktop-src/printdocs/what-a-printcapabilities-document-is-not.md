---
description: Erfahren Sie mehr über einige der Funktionen und Informationen, die das PrintCapabilities-Dokument nicht bereitstellen soll.
ms.assetid: 87a897cd-d3aa-488a-b129-9837d3500d0d
title: Was ein PrintCapabilities-Dokument nicht ist
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bcd5dbedf6ee3a7e2713bd3591b182c606cfb0c
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409893"
---
# <a name="what-a-printcapabilities-document-is-not"></a>Was ein PrintCapabilities-Dokument nicht ist

Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

Es lohnt sich, einige der Funktionen und Informationen auflisten, die das PrintCapabilities-Dokument nicht bereitstellen soll.

Ein PrintCapabilities-Dokument:

-   Stellt keine mehrwertigen (konfigurationsabhängigen) Daten dar.

    Jedes PrintCapabilities-Dokument wird für eine bestimmte Konfiguration erstellt. Keine Eigenschaft oder ScoredProperty im Dokument kann einen Wert haben, der von der jeweiligen Konfiguration abhängt. In der anfänglichen Schemaversion muss der PrintCapabilities-Anbieter die Eingabe PrintTicket verarbeiten und ein PrintCapabilities-Dokument erstellen, das Eigenschaftswerte enthält, die für die im PrintTicket angegebene Konfiguration geeignet sind.

-   Enthält keine Einschränkungsinformationen.

    Das PrintCapabilities-Dokument gibt nicht an, welche Konfigurationen zulässig und welche nicht zulässig sind. In der anfänglichen Schemaversion muss der PrintCapabilities-Anbieter alle Informationen speichern, die zum Überprüfen von Konfigurationen erforderlich sind, eine Methode zur Überprüfung der PrintTicket-Eingabe angeben und ein korrigiertes PrintTicket zurückgeben, wenn das angegebene PrintTicket gegen eine oder mehrere Einschränkungen verstößt.

-   Enthält keine dynamischen Geräteinformationen.

    Es ist zu viel Aufwand für die Konstruktion des PrintCapabilities-Dokuments verbunden, damit es für sich schnell ändernde Statusinformationen verwendet werden kann, z. B. Freidruckebenen, Papier, das in jeder Tablettleiste verbleibt, oder Papierstaustatus.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



