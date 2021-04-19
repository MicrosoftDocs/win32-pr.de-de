---
description: In der WMI-Infrastruktur ist der WMI-Dienst (Winmgmt) die Betriebssystem Komponente, die als Vermittler zwischen Verwaltungs Anwendungen und WMI-Datenanbietern fungiert. Das WMI-Repository ist ein Speicherbereich für WMI-bezogene statische Daten.
ms.assetid: 6ef157be-fb75-4453-bc20-4568a3dc18c0
ms.tgt_platform: multiple
title: WMI-Infrastruktur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4370af9ec062ffa845d54eafda054357a76dc07c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348544"
---
# <a name="wmi-infrastructure"></a>WMI-Infrastruktur

In der WMI-Infrastruktur ist der WMI-Dienst (Winmgmt) die Betriebssystem Komponente, die als Vermittler zwischen Verwaltungs Anwendungen und WMI-Daten [*Anbietern*](gloss-p.md)fungiert. Das [*WMI-Repository*](gloss-w.md) ist ein Speicherbereich für WMI-bezogene statische Daten.

Der WMI-Dienst wird als Dienst Prozess innerhalb eines gemeinsamen Dienst Host Prozesses (SVCHOST) implementiert. Weitere Informationen finden Sie unter [Anbieter Hosting und-Sicherheit](provider-hosting-and-security.md).

Der WMI-Dienst wird gestartet, wenn die erste Verwaltungs Anwendung oder das erste Skript eine Verbindung mit einem WMI-Namespace herstellt. Abhängig von der Einrichtung wird der WMI-Dienst möglicherweise heruntergefahren oder zu einem Profil mit geringem Speicherplatz wechseln, wenn er nicht von einer Verwaltungs Anwendung aufgerufen wird.

Der WMI-Dienst interagiert mit Verwaltungs Anwendungen über die COM-Schnittstelle. Wenn eine Anwendung über die-Schnittstelle eine Anforderung sendet, bestimmt WMI, ob die Anforderung für statische oder dynamische Daten ist. Wenn die Anforderung statische Daten (z. b. den Namen eines verwalteten Objekts) umfasst, ruft WMI die Daten aus dem Repository ab. Wenn die Anforderung dynamische Daten umfasst, z. b. die Menge an Arbeitsspeicher, die ein verwaltetes Objekt zurzeit verwendet, übergibt WMI die Anforderung an einen Anbieter.

Anbieter registrieren ihren Speicherort beim WMI-Dienst, der WMI das Weiterleiten von Datenanforderungen ermöglicht. Ein Anbieter registriert auch die Unterstützung für bestimmte Vorgänge, z. b. Datenabruf, Änderung, Löschung, Enumeration oder Abfrage Verarbeitung. Der WMI-Dienst verwendet die Anbieter Registrierungsinformationen, um Anwendungsanforderungen mit dem entsprechenden Anbieter abzugleichen. WMI verwendet die Registrierungsinformationen auch, um Anbieter nach Bedarf zu laden und zu entladen. Wenn ein Anbieter die Verarbeitung einer Anforderung abschließt, gibt der Anbieter das Ergebnis an den WMI-Dienst zurück. WMI leitet das Ergebnis dann über die COM-Schnittstelle an die Anwendung weiter. Weitere Informationen finden Sie unter [Bereitstellen von Daten für WMI](providing-data-to-wmi.md).

WMI verwendet die [Ereignis Ablauf Verfolgung](/windows/desktop/ETW/event-tracing-portal) (ETW), um die WMI-Dienst Aktivität aufzuzeichnen.

Da die-Infrastruktur den gesamten Datenverkehr zwischen den Anbietern und den Verwaltungs Anwendungen verarbeitet, bietet die-Infrastruktur die folgenden Features:

-   Unterstützung für Ereignis Benachrichtigungen

    Weitere Informationen finden Sie unter über [Wachen von Ereignissen](monitoring-events.md).

-   Unterstützung der Abfragesprache

    Weitere Informationen finden Sie unter [Abfragen mit WQL](querying-with-wql.md).

-   Sicherheitsunterstützung

    Weitere Informationen finden Sie unter Verwalten der [WMI-Sicherheit](maintaining-wmi-security.md).

-   Skripterstellung für den Zugriff auf Leistungsdaten

    Weitere Informationen finden Sie unter über [Wachen von Leistungsdaten](monitoring-performance-data.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WMI-Architektur](wmi-architecture.md)
</dt> </dl>

 

 
