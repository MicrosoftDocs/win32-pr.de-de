---
description: Die Jugendschutzkontrollen können mithilfe der Einstellungs- und Protokollierungs-APIs erweitert werden.
ms.assetid: f0fc1b11-6de4-48f6-afc9-f05c8812d2bd
title: Übersicht über Erweiterbarkeitsfunktionen für Jugendschutz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bf609c08a4114d7d96ae600744879bda53ac483d90bcd25def3dd0d5f9e3c26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971719"
---
# <a name="parental-controls-extensibility-features-overview"></a>Übersicht über Erweiterbarkeitsfunktionen für Jugendschutz

Die Jugendschutzkontrollen können mithilfe der Einstellungs- und Protokollierungs-APIs erweitert werden.

-   [Protokollierung – Hintergrund](/windows)
-   [Erweiterbarkeit der Protokollierung](#logging-extensibility)
-   [Bereich "Jugendschutz" Allgemeine Erweiterungslinkerweiterung der Benutzeroberfläche](#parental-controls-panel-general-ui-extensibility-link-addition)
-   [Ersetzen von Webinhaltsfiltern](#web-content-filter-replacement)

## <a name="loggingbackground"></a>Protokollierung – Hintergrund

Microsoft hat eine Reihe von Standardereignissen für allgemeine Aktivitäten definiert:

-   System: Änderungen an Einstellungen der Jugendschutzeinstellungen, Kontoänderungen, Systemuhränderungen, fehlgeschlagene Anmeldeversuche.
-   User:
    -   System-/Zeitlimits: Anmeldezeiten, Abmeldezeit, Anwendungslaufversuche und Ausführungsdauer der Anwendung (siehe Hinweis).
    -   Webeinschränkungen: Besuchte und blockierte Websites, Dateidownloadversuche. Webbrowser und browserbasierte Anwendungen müssen diese nicht protokollieren, da der Webinhaltsfilter-LSP dies tut. Ersetzungswebfilter müssen diese Ereignisse generieren.
    -   Spiele: Spiele spielten und blockiert, Spielende (Ereignisse zusammen bieten die Dauer der Spiele).
    -   Bestimmte Programme zulassen und blockieren: Ausführungsversuch, Herunterfahren, durch allgemeine Anwendungseinschränkungen blockiert.
    -   Instant Messaging: Konvertierungsinitiierungsversuch, Konversationseinführungsversuch, Konversationsabbruch, Video/Audio/Spiel/Kurznachrichtendienst/Dateiübertragung/URL-Austauschfunktion, Änderungsversuch der Kontaktliste.
    -   E-Mail: Empfangen oder Empfangen blockiert, Sendeversuch, Änderungsversuch der Kontaktliste.
    -   Medien: Medien, die abgespielt und versucht wurden.

Nicht alle vorherigen Ereignisse sind für die Verwendung durch Anwendungen geeignet. Kontoänderungen, die Systemuhränderung und die Protokollierung von Anmelde- und Abmeldeereignis werden nur vom Betriebssystem implementiert und daher nicht öffentlich verfügbar gemacht.

> [!Note]  
> Die Instrumentierung von Anwendungseintritts- und -beendigungsereignissen ist in Windows Vista verfügbar und wird von der Jugendschutz-Verwaltung zum Protokollieren dieser Daten konfiguriert.

 

## <a name="logging-extensibility"></a>Erweiterbarkeit der Protokollierung

Ein generisches benutzerdefiniertes Ereignis wird auch mit drei verfügbaren Tags/Werten definiert, sodass ISVs in der Regel keine eigenen Tags/Werte in einem Manifest definieren müssen. Der Protokoll-Viewer erkennt und zeigt die Tagheader und -werte an, wenn die Anzahl der verwendeten Felder (1 bis 3) und Überschriften für jedes Feld mithilfe der WMI-API registriert werden. Die generische Ereignisanzeige kann auch zum Anzeigen benutzerdefinierter Ereignisse verwendet werden.

Wenn das generische benutzerdefinierte Ereignis nicht geeignet ist, kann ein ISV sein eigenes mithilfe eines Anwendungsmanifests definieren und Header für bis zu drei Felder mit der gleichen WMI-API registrieren.

ISVs können ihre eigenen Ereignisse definieren und unabhängig vom Protokoll-Viewer über öffentliche Windows nutzen. Dies hat nicht den Vorteil einer vollständigen Protokollzentralisierung.

## <a name="parental-controls-panel-general-ui-extensibility-link-addition"></a>Bereich "Jugendschutz" Allgemeine Erweiterungslinkerweiterung der Benutzeroberfläche

Eine allgemeine Benutzeroberflächen-Erweiterbarkeitsverknüpfung wird durch Den Zugriff auf Einstellungen über WMI verfügbar gemacht, indem eine Erweiterungsinstanz aus übergebenen Ressourcen-DLL-Pfad und -ID, Imagepfad (Bitmap), Pfad für deaktivierte Statusbilder (Bitmap), Dll-Pfad und ID der Untertitelressource sowie Spezifikationen für ausführbare Pfade erstellt werden. Nach der Registrierung wird der Link im Bereich Weitere Einstellungen des Bereichs "Jugendschutz" angezeigt. Wenn Sie darauf klicken, wird die angegebene ausführbare Datei aufgerufen.

Die ausführbare Pfadzeichenfolge kann optional ein Token für die SID des aktuellen Benutzers enthalten, das vor dem Aufruf ersetzt werden soll. Dadurch kann die Linkausführung im Kontext des Benutzers ausgeführt werden, für den die Hubseite gerade angezeigt wird, wenn die ausführbare Datei die SID kennen muss.

## <a name="web-content-filter-replacement"></a>Ersetzen von Webinhaltsfiltern

Wie im Thema Jugendschutz In-Box Einschränkungen und Benutzeroberflächen [erwähnt,](parental-controls-in-box-restrictions-and-user-interfaces.md)kann der im Feld enthaltene Webinhaltsfilter durch einen vom Anbieter bereitgestellten Filter ersetzt werden. Dies erfolgt durch Den Zugriff auf Einstellungen über WMI, um eine GUID und einen Namen für die Filterung zu festlegen.

Der allgemeine Erweiterbarkeitsmechanismus der Benutzeroberfläche wird verwendet, um einen Drittanbieterfilter verfügbar zu machen. Dies ist derselbe Mechanismus wie für alle Erweiterungen, die im Abschnitt Weitere Einstellungen der obersten Ebene der Systemsteuerung. Wenn Sie den zusätzlichen Schritt zum Festlegen der gleichen GUID und eines entsprechenden Namens für ressourcenbasierte DLL-Pfad und -ID in die Filtereinstellungen auf Systemebene vornehmen, wird der im Feld angezeigte Filterlink ausgeblendet, und der Eintrag des Drittanbieters wird oben im Abschnitt Weitere Einstellungen angezeigt. Der für den Filter registrierte Name wird im Zusammenfassungsabschnitt angezeigt.

Das Zurücksetzen der Filter-GUID und der Namenspfad-/ID-Einstellungen führt dazu, dass sich der im Feld enthaltene Webinhaltsfilter als aktiver Filter erneut einbilden und erneut im abschnitt Windows Einstellungen wird.

Beachten Sie, dass Filter von Drittanbietern nicht in den Technologien eingeschränkt sind, die zum Verbinden mit Windows werden. Ein Filter muss lediglich seine Einstellungen über einen Erweiterbarkeitslink verfügbar machen und die entsprechenden Einstellungen der Jugendschutz-Steuerungen verwenden.

 

 
