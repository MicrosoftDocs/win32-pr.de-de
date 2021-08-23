---
description: Übersicht über die Jugendschutz-API
ms.assetid: 647e5df8-7c6d-466a-a3d4-eac13efa797d
title: Übersicht über die Jugendschutz-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc2dc1995db834aa206dea1a4f657565ac3e38b35766ca6a83ac495c4f1734af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119712580"
---
# <a name="parental-controls-api-overview"></a>Übersicht über die Jugendschutz-API

APIs, die für die Jugendschutz-Api verwendet werden, machen die Einstellungen für Richtlinien- und In-Box-Einschränkungen sowie protokollierungsfunktionen verfügbar.

## <a name="settings"></a>Einstellungen

Es werden zwei öffentliche APIs bereitgestellt:

-   Eine einfache COM-basierte Mindestkonformitäts-API (als Compliance-API bezeichnet) in erster Linie für Anwendungen, um zu bestimmen, ob die Protokollierung aktiviert werden soll. Darüber hinaus werden einfache Methoden für:
    -   Abrufen des Einschränkungsstatus für Webeinschränkungen, Zeitlimits, Spieleeinschränkungen und Anwendungseinschränkungen.
    -   Abrufen der ID des aktiven Webinhaltsfilters.
    -   Bestimmen, ob Benutzeroberflächenelemente des Anbieters angezeigt werden sollen, und dies in Übereinstimmung mit dem in-box-Hiding beim Beitritt zu einer Domäne.
    -   Abrufen des letzten Zeitpunkts, zu dem eine Einstellung für einen Benutzer geändert wurde.
    -   Abrufen, ob browserbasierte oder browserbasierte Dateidownloads für einen Benutzer blockiert werden müssen, und die Möglichkeit, eine URL an fordern zu können, die speziell vom Webinhaltsfilter für diesen Benutzer zugelassen wird.
    -   Bestimmen, ob ein bestimmtes Spiel für einen Benutzer blockiert wird.
-   Windows WMI-API-Zugriff (Management Instrumentation, Verwaltungsinstrumentation) auf einen Namespace der Jugendschutzverwaltung für vollständigen Schreib- und Lesezugriff auf alle verfügbar gemachten Einstellungen. Die Jugendschutzverwaltung stellt einen WMI-Anbieter zum Verwalten von Lese-/Schreibberechtigungen für den zugrunde liegenden Einstellungsspeicher mit ordnungsgemäßer Erzwingung von Berechtigungen für Administratoren und kontrollierte Benutzer zur Verfügung.

ISVs werden aufgefordert, die Kompatibilitäts-API und die WMI-API nach Bedarf zu verwenden, um Einschränkungen entsprechend der untergeordneten Sicherheit basierend auf der Funktionalität der Anwendung oder Lösung zu steuern.

## <a name="logging"></a>Protokollierung

-   Windows standardmäßige Ereignisveröffentlichungs- und -verbrauch-APIs werden für die Aktivitätsüberwachung der Elternkontrolle verwendet. Das Windows Vista-Ereignisberichterstellungs- und -Ablaufverfolgungssystem hat die Leistung gegenüber früheren ETW-Funktionen (Event Tracing for Windows) verbessert. Jugendschutz definiert einen eindeutigen Kanal für seine Daten in ETW.
-   ISVs werden aufgefordert, die Ereignisveröffentlichungs-API zu verwenden, um Benutzeraktivitäten zu protokollieren, wie im Abschnitt Verwenden von Jugendschutz-APIs angegeben.

 

 



