---
description: In dieser Übersicht über die PrintTicket-Funktionalität wird das Format für das Ausdrücken von Gerätekonfigurationsinformationen und die Verwendung eines PrintTickets beschrieben.
ms.assetid: c48b9821-9194-47d9-a3ec-b10dbbdf14cc
title: Übersicht über die PrintTicket-Funktionalität
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e90aa6f967f5fce25977b52a4d0bec7e9e1ea705
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408543"
---
# <a name="overview-of-printticket-functionality"></a>Übersicht über die PrintTicket-Funktionalität

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

PrintTicket verwendet ein XML-basiertes Format zum Ausdrücken von Gerätekonfigurationsinformationen mithilfe der Feature-/Options- und Parameterkonstrukte des Druckschemaframeworks. Dies umfasst alle Standardelementtypen sowie die Erweiterbarkeitsfunktionen des Druckschemaframeworks. Ein PrintTicket wird als eigenständige Beschreibung der Verarbeitung einer einzelnen Seite angenommen. Die Schritte zum Extrahieren und Erstellen eines solchen PrintTickets aus einem bestimmten Dokumentformat werden hier nicht behandelt.

Ein PrintTicket kann verwendet werden, um ein PrintCapabilities-Dokument abzurufen, das die Merkmale des Geräts für eine bestimmte Konfiguration beschreibt. Alternativ kann das PrintTicket mit einer Reihe von Renderinganweisungen übermittelt werden, um eine Ausgabeseite zu erzeugen, die gemäß der im PrintTicket angegebenen Konfiguration gerendert und verarbeitet wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



