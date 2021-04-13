---
description: Eltern Steuerelemente können mithilfe der APIs für Einstellungen und Protokollierung erweitert werden.
ms.assetid: f0fc1b11-6de4-48f6-afc9-f05c8812d2bd
title: Übersicht über die Erweiterbarkeits Features für Eltern Steuerelemente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fe150c5955881b8038cdca9a1e4562ee28093f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349108"
---
# <a name="parental-controls-extensibility-features-overview"></a>Übersicht über die Erweiterbarkeits Features für Eltern Steuerelemente

Eltern Steuerelemente können mithilfe der APIs für Einstellungen und Protokollierung erweitert werden.

-   [Protokollierung – Hintergrund](/windows)
-   [Protokollierungs Erweiterbarkeit](#logging-extensibility)
-   [Steuerelement "Jugendschutz" allgemeine Benutzeroberflächen-Erweiterbarkeits Link Addition](#parental-controls-panel-general-ui-extensibility-link-addition)
-   [Ersetzung von Webinhalts Filtern](#web-content-filter-replacement)

## <a name="loggingbackground"></a>Protokollierung – Hintergrund

Microsoft hat eine Reihe von Standard Ereignissen definiert, um allgemeine Aktivitäten zu behandeln:

-   System: Eltern Steuerungseinstellungen Änderungen, Kontoänderungen, Änderungen an der Systemuhr, fehlgeschlagene Anmeldeversuche.
-   User:
    -   System-/uhrzeitlimits: Anmeldezeiten, Abmeldung, Anwendungs Ausführungs Versuche und Ausführungsdauer der Anwendung (siehe Hinweis).
    -   Webeinschränkungen: besuchte und blockierte Websites, Datei Download Versuche. Webbrowser und Browser ähnliche Anwendungen müssen diese nicht protokollieren, wie es der Webinhalts Filter-LSP tut. Ersetzungs-Webfilter müssen diese Ereignisse generieren.
    -   Spiele: Spiele und Blockierung, Spiel Ende (Ereignisse, die eine Dauer spielen).
    -   Zulassen und Blockieren bestimmter Programme: Ausführen des Versuchs, Herunterfahren, blockiert durch allgemeine Anwendungs Einschränkungen.
    -   Instant Messaging: Umwandlungs Initiierungs Versuch, konverterjoinversuch, Konversations Versuch, Video-/Audio-/Spiel-/Kurznachrichtendienst/Dateiübertragung/URL-Swap-Feature, Kontaktlisten-Änderungs Versuch.
    -   E-Mail: der Empfangs-oder Empfangsport wurde blockiert, der Sende Versuch war der Änderungs Versuch der Kontaktliste
    -   Medium: Medien wurden wiedergegeben und versucht.

Nicht alle vorherigen Ereignisse sind für die Verwendung durch Anwendungen geeignet. Kontoänderungen, die Änderung der Systemuhr und die Protokollierung von Anmelde-und Abmelde Ereignissen werden nur vom Betriebssystem implementiert und daher nicht öffentlich verfügbar gemacht.

> [!Note]  
> Die Instrumentierung von Anwendungs Eintrags-und Beendigungs Ereignissen ist in Windows Vista verfügbar und wird von Eltern Steuerelementen konfiguriert, um diese Daten zu protokollieren.

 

## <a name="logging-extensibility"></a>Protokollierungs Erweiterbarkeit

Ein generisches benutzerdefiniertes Ereignis ist auch mit 3 verfügbaren Tags/Werten definiert, sodass ISVs in der Regel keine eigenen in einem Manifest definieren müssen. Der Protokoll-Viewer erkennt und zeigt die Tagheader und-Werte an, wenn die Anzahl der verwendeten Felder (1 bis 3) und die Überschriften für jedes Feld mithilfe der WMI-API registriert werden. Der generische Ereignisanzeige kann auch verwendet werden, um benutzerdefinierte Ereignisse anzuzeigen.

Wenn das generische benutzerdefinierte Ereignis nicht geeignet ist, kann ein ISV seine eigenen mithilfe eines Anwendungs Manifests definieren und mithilfe derselben WMI-API Header für bis zu drei Felder registrieren.

ISVs können Ihre eigenen Ereignisse definieren und unabhängig vom Protokoll-Viewer über öffentliche Windows-APIs nutzen. Dies hat nicht den Vorteil der vollständigen Protokoll Zentralisierung.

## <a name="parental-controls-panel-general-ui-extensibility-link-addition"></a>Steuerelement "Jugendschutz" allgemeine Benutzeroberflächen-Erweiterbarkeits Link Addition

Ein allgemeiner Link zur Erweiterbarkeit der Benutzeroberfläche wird durch den Zugriff auf Einstellungen über WMI verfügbar gemacht. dabei wird eine Erweiterungs Instanz aus dem Namen Ressourcen-DLL-Pfad und ID, dem Image (Bitmap)-Pfad, dem deaktivierten Status Image (Bitmap), dem Untertitel Ressourcen-DLL-Pfad und der ID und den Spezifikationen für ausführbare Pfade Nach der Registrierung wird der Link im Bereich Weitere Einstellungen der Jugend Steuerungs Bereich angezeigt, und durch Klicken auf den Link wird die angegebene ausführbare Datei aufgerufen.

Die ausführbare Pfad Zeichenfolge kann optional ein Token für die SID des aktuellen Benutzers enthalten, die vor dem Aufruf ersetzt werden soll. Dies ermöglicht die Ausführung der Link Ausführung im Kontext des Benutzers, für den die Hub-Seite derzeit angezeigt wird, wenn die ausführbare Datei die SID kennen muss.

## <a name="web-content-filter-replacement"></a>Ersetzung von Webinhalts Filtern

Wie in diesem Thema erwähnt [In-Box](parental-controls-in-box-restrictions-and-user-interfaces.md), kann der in-Box-Webinhalts Filter durch einen vom Hersteller bereitgestellten Filter ersetzt werden. Dies erfolgt durch den Zugriff auf Einstellungen über WMI, um eine GUID und den Namen für die Filterung festzulegen.

Der allgemeine Erweiterbarkeits Mechanismus für die Benutzeroberfläche wird zum verfügbar machen eines Drittanbieter Filters verwendet. Dies ist derselbe Mechanismus, der für jede Erweiterung verwendet wird, die im Abschnitt Weitere Einstellungen der Systemsteuerung der obersten Ebene der Ebene angezeigt werden soll. Wenn Sie die gleiche GUID und den entsprechenden Pfad und die ID der namens Ressourcen-DLL in den Filtereinstellungen auf Systemebene festlegen, wird der im Feld angezeigte filterlink ausgeblendet, und der Eintrag von Drittanbietern wird oben im Abschnitt Weitere Einstellungen angezeigt. Der für den Filter registrierte Name wird im Abschnitt Zusammenfassung angezeigt.

Das Zurücksetzen der Filter-GUID und der namens Pfad-/ID-Einstellungen führt dazu, dass sich der in-Box-Webinhalts Filter als aktiver Filter wiederherstellt und im Abschnitt "Windows-Einstellungen" erneut angezeigt wird.

Beachten Sie, dass Filter von Drittanbietern in den Technologien, die zum Einbinden der Windows-Kommunikation verwendet werden, nicht eingeschränkt werden. Ein Filter muss seine Einstellungen nur über einen Erweiterbarkeits Link verfügbar machen und die entsprechenden Einstellungen für Eltern Steuerelemente berücksichtigen.

 

 
