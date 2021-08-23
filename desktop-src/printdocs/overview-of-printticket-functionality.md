---
description: In dieser Übersicht über die PrintTicket-Funktionalität wird das Format für das Ausdrücken von Gerätekonfigurationsinformationen und die Verwendung eines PrintTickets beschrieben.
ms.assetid: c48b9821-9194-47d9-a3ec-b10dbbdf14cc
title: Übersicht über die PrintTicket-Funktionalität
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edd01e7247de83e8f378dbcff8e99c32abacd448f436ad69af1f99a1566655b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119718970"
---
# <a name="overview-of-printticket-functionality"></a>Übersicht über die PrintTicket-Funktionalität

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

PrintTicket verwendet ein XML-basiertes Format zum Ausdrücken von Gerätekonfigurationsinformationen mithilfe der Feature-/Options- und Parameterkonstrukte des Druckschemaframeworks. Dies umfasst alle Standardelementtypen sowie die Erweiterbarkeitsfunktionen des Druckschemaframeworks. Ein PrintTicket wird als eigenständige Beschreibung der Verarbeitung einer einzelnen Seite angenommen. Die Schritte zum Extrahieren und Erstellen eines solchen PrintTickets aus einem bestimmten Dokumentformat werden hier nicht behandelt.

Ein PrintTicket kann verwendet werden, um ein PrintCapabilities-Dokument abzurufen, das die Merkmale des Geräts für eine bestimmte Konfiguration beschreibt. Alternativ kann das PrintTicket mit einer Reihe von Renderinganweisungen übermittelt werden, um eine Ausgabeseite zu erzeugen, die gemäß der im PrintTicket angegebenen Konfiguration gerendert und verarbeitet wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



