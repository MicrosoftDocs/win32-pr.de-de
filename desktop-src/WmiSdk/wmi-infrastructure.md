---
description: In der WMI-Infrastruktur ist der WMI-Dienst (Winmgmt) die Betriebssystemkomponente, die als Vermittler zwischen Verwaltungsanwendungen und WMI-Datenanbietern fungiert. Das WMI-Repository ist ein Speicherbereich für WMI-bezogene statische Daten.
ms.assetid: 6ef157be-fb75-4453-bc20-4568a3dc18c0
ms.tgt_platform: multiple
title: WMI-Infrastruktur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a2bc4492c7d26f422705863609a2e0ec19af5eb930e0aa80f4fd8bb8c26bea4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757330"
---
# <a name="wmi-infrastructure"></a>WMI-Infrastruktur

In der WMI-Infrastruktur ist der WMI-Dienst (Winmgmt) die Betriebssystemkomponente, die [](gloss-p.md)als Vermittler zwischen Verwaltungsanwendungen und WMI-Datenanbietern fungiert. Das [*WMI-Repository*](gloss-w.md) ist ein Speicherbereich für WMI-bezogene statische Daten.

Der WMI-Dienst wird als Dienstprozess innerhalb eines Shared Service Host-Prozesses (SVCHOST) implementiert. Weitere Informationen finden Sie unter [Anbieterhosting und Sicherheit.](provider-hosting-and-security.md)

Der WMI-Dienst wird gestartet, wenn die erste Verwaltungsanwendung oder das erste Verwaltungsskript einen Aufruf zum Herstellen einer Verbindung mit einem WMI-Namespace vornimmt. Je nach Setup kann der WMI-Dienst heruntergefahren werden oder in ein Profil mit wenig Arbeitsspeicher wechseln, wenn er nicht von einer Verwaltungsanwendung aufgerufen wird.

Der WMI-Dienst interagiert über die COM-Schnittstelle mit Verwaltungsanwendungen. Wenn eine Anwendung eine Anforderung über die -Schnittstelle vornimmt, bestimmt WMI, ob es sich bei der Anforderung um statische oder dynamische Daten handelt. Wenn die Anforderung statische Daten umfasst, z. B. den Namen eines verwalteten Objekts, ruft WMI die Daten aus dem Repository ab. Wenn die Anforderung dynamische Daten umfasst, z. B. die Menge an Arbeitsspeicher, die ein verwaltetes Objekt derzeit verwendet, übergibt WMI die Anforderung an einen Anbieter.

Anbieter registrieren ihren Standort beim WMI-Dienst, der es WMI ermöglicht, Datenanforderungen weiterzuleiten. Ein Anbieter registriert auch Unterstützung für bestimmte Vorgänge, z. B. Datenabruf, Änderung, Löschung, Enumeration oder Abfrageverarbeitung. Der WMI-Dienst verwendet die Anbieterregistrierungsinformationen, um Anwendungsanforderungen mit dem entsprechenden Anbieter abzugleichen. WMI verwendet bei Bedarf auch die Registrierungsinformationen, um Anbieter zu laden und zu entladen. Wenn ein Anbieter die Verarbeitung einer Anforderung beendet, gibt der Anbieter das Ergebnis an den WMI-Dienst zurück. WMI leitet das Ergebnis dann über die COM-Schnittstelle an die Anwendung weiter. Weitere Informationen finden Sie unter [Bereitstellen von Daten für WMI.](providing-data-to-wmi.md)

WMI verwendet [die Ereignisablaufverfolgung](/windows/desktop/ETW/event-tracing-portal) (Event Tracing, ETW), um WMI-Dienstaktivitäten aufzuzeichnen.

Da die Infrastruktur den gesamten Datenverkehr zwischen den Anbietern und den Verwaltungsanwendungen verarbeitet, bietet die Infrastruktur die folgenden Features:

-   Unterstützung für Ereignisbenachrichtigungen

    Weitere Informationen finden Sie unter [Überwachen von Ereignissen.](monitoring-events.md)

-   Unterstützung der Abfragesprache

    Weitere Informationen finden Sie unter [Abfragen mit WQL.](querying-with-wql.md)

-   Sicherheitsunterstützung

    Weitere Informationen finden Sie unter [Verwalten der WMI-Sicherheit.](maintaining-wmi-security.md)

-   Skriptzugriff auf Leistungsindikatordaten

    Weitere Informationen finden Sie unter [Überwachen von Leistungsdaten.](monitoring-performance-data.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WMI-Architektur](wmi-architecture.md)
</dt> </dl>

 

 
