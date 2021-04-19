---
description: Es werden verschiedene Implementierungs Implementierungen bereitgestellt.
ms.assetid: a00d9a3a-d052-492c-b9e7-3ecb1455a392
title: Steuerelement-Steuerelemente In-Box Einschränkungen & Benutzeroberflächen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e5f155f8323fd6b006e510d75865ea25e278c70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369048"
---
# <a name="parental-controls-in-box-restrictions--user-interfaces"></a>Steuerelement-Steuerelemente In-Box Einschränkungen & Benutzeroberflächen

Es werden verschiedene Implementierungs Implementierungen bereitgestellt.

-   [Webeinschränkungen](#web-restrictions)
-   [Zeit Limits](#time-limits)
-   [Spiele](#games)
-   [Zulassen und Blockieren bestimmter Programme](#allow-and-block-specific-programs)

## <a name="web-restrictions"></a>Webeinschränkungen

-   In-Box-Webinhalts Filter mithilfe eines kostenlosen dynamischen Bewertungs Diensts. Einzeln konfigurierbar pro kontrolliertem Benutzer.
-   Filtert bei Aktivierung den gesamten HTTP-Datenverkehr, gibt eine benutzerdefinierte formatierte Seite zurück Ermöglicht eine akzeptable Funktionalität bei allen wichtigen Browsern. Durch das Überwachen aller HTTP Get-und Post-Anforderungen für eine Seite können einzelne Webseiten Teile blockiert werden.
-   Hochgradig konfigurierbar mithilfe der Benutzeroberfläche, die URL-Listen zulässt oder blockiert, Voreinstellungen für eine vereinfachte Bewertungskategorie oder ActiveX-Steuerelement von 12 +-Kategorien sowie eine Richtlinie zum Blockieren von Dateidownloads.

> [!Note]  
> Die tatsächliche Blockierung von Dateidownloads erfordert, dass Anwendungen die Einschränkung implementieren, wobei die angegebene Einstellung eingehalten wird.

 

-   Wird als Windows-Filter Plattform (Windows Filtering Platform, WFP) implementiert, die mit dem in den Benutzersitzungen laufenden Prozess der Familien Sicherheitsüberwachung kommuniziert. Die Implementierung hat sich von einem LSP-Filter (geschichteter Dienstanbieter) zu einem Windows-Filter Plattform-Treiber (WFP) geändert, der mit dem in den Sitzungen der Benutzer ausgeführt wird.

    **Windows 7 und Windows Vista:** Wird als ein mehrstufiger Dienstanbieter (LSP) implementiert, der mit einem Dienst mit geringen Rechten für die allgemeine Verwaltung und Überwachung kommuniziert. Der Filter bleibt in der LSP-Kette, wenn er deaktiviert ist, übergibt aber den gesamten Datenverkehr über. Diese Implementierung wird nur für die aufgeführten Betriebssysteme unterstützt.

-   Anwendungen können eine Benutzeroberfläche bereitstellen, um die partielle Seiten Blockierung anzuzeigen, und die Richtlinie zum Blockieren von Dateidownloads beachten Sie können auch eine API aufrufen, um dem Benutzer zu gestatten, eine Berechtigung zum Anzeigen einer blockierten Seite anzufordern. Diese administrative außer Kraft Setzung Ruft eine kleine Anwendung auf, in der die versuchten URLs angezeigt werden und die Anmelde Informationen anfordern, um Sie zuzulassen.
-   Eine API wird für Sonderfälle bereitgestellt, in denen sich eine Anwendung registrieren muss, um die Filterung zu umgehen, oder bestimmte URLs sind immer zulässig.
-   Da jeweils nur ein Webinhalts Filter ausgeführt werden sollte, können sich Drittanbieter als aktiver Filter registrieren und den in-Box-Filter deaktivieren. Diese Erweiterbarkeit ist mit der Möglichkeit zum Anzeigen eines Drittanbieter Filters in der Benutzeroberfläche verbunden und ermöglicht eine einfache Ersetzung. Filter müssen Ihre Registrierung entfernen, wenn Sie deinstalliert werden.

## <a name="time-limits"></a>Zeit Limits

-   Die in-Box-Zeitbeschränkungen wurden durch die Möglichkeit zur Steuerung der Gesamtzeit pro Tag, mit der der Computer verwendet werden kann (Zeitkontingent), zusätzlich zur Steuerung der Zeiten, in denen der Computer verwendet werden kann (in früheren Versionen von Windows), verbessert.
-   Die Benutzeroberfläche für geschweiente Elemente ermöglicht die unabhängige Steuerung der einzelnen Wochentage mit einer halben Stunden Granularität.
-   Die Benutzeroberfläche für ein Zeitkontingent ermöglicht Steuerelemente für Wochentage und Wochenenden oder ein unabhängiges Steuerelement für jeden Wochentag mit einer Granularität von 15 Minuten.
-   Der-Mechanismus für schnelle Benutzer Switches wird nicht mehr verwendet, um die Anmeldung des kontrollierten Benutzers zu erzwingen oder zu blockieren, wenn der blockierte Zeitraum blockiert ist. Für diese Zwecke wird ein Wechsel zu einem separaten Desktop verwendet. Beachten Sie, dass der Benutzer den Status des Benutzers beibehält, wenn er gesperrt ist.

## <a name="games"></a>Spiele

-   Funktioniert in Verbindung mit dem Games Explorer.
-   Ermöglicht es Administratoren, zu steuern, welche Spiele durch eine umfangreiche Benutzeroberfläche zum Auswählen eines playerbewertungs-Systems und einer Ebene (plus Deskriptoren, falls vorhanden) und/oder durch das besondere zulassen oder Blockieren von Titeln gespielt werden können.
-   Metadaten für Spiele Bewertungen werden auf eine von zwei Arten abgerufen:
    -   Unterstützte Titel stellen ihre eigenen Spiel Definitions Dateien (DSFs) bereit.
    -   Ungefähr 2000 Legacy Titel werden durch eine in-Box-Datenbank abgedeckt.
-   Für die Durchsetzung werden drei Mechanismen verwendet:
    -   Verweigern Sie ACLs für kontrollierten Benutzer Schreibzugriff auf den Spiel Ordner.
    -   Prozess Beendigung für ältere Titel mithilfe von Anwendungskompatibilitäts-Shim-Technologie.
    -   Selbstüberprüfung der API-Verwendung durch unterstützte Titel zum Blockieren der Laufzeit.
-   Informationen zu Zeit Limits, die im obigen Abschnitt erläutert werden, werden empfohlen.
-   Die Dokumentation für dsfs und der Games Explorer wird hauptsächlich über DirectX SDK-Releases bereitgestellt.

## <a name="allow-and-block-specific-programs"></a>Zulassen und Blockieren bestimmter Programme

-   Diese werden auch als allgemeine Anwendungs Einschränkungen (überhaupt) bezeichnet.
-   Standardmäßig deaktiviert. Wenn diese Option aktiviert ist, kann ein kontrollierter Benutzer mit angemessenen Ausnahmen nur von einem Administrator genehmigte Anwendungen ausführen.
-   Die Benutzeroberfläche enthält eine Liste von Programmnamen mit entsprechenden Pfaden, von denen jede über das Kontrollkästchen Zulassen verfügt. Außerdem wird eine Schaltfläche zum Durchsuchen bereitgestellt.
-   Implementiert mithilfe von Richtlinien für Software Einschränkung (SRP), die auch als sicherer bezeichnet werden:
    -   Verhindert die Ausführung von allen Medien (USB-Schlüssel, Disketten usw.).
    -   Verwendet Pfad Regeln, um Programme anzugeben, die ausgeführt werden dürfen.
    -   NTFS-ACL-Schreibberechtigungen werden von allen Berechtigungen widerrufen, die der kontrollierte Benutzer ausführen darf.
    -   Wenn Sie blockiert und anschließend überschrieben werden, um zuzulassen, muss die Anwendung manuell neu gestartet werden.
-   Zu den Ausnahmen zählen:
    -   Alle Binärdateien, die erforderlich sind, damit eine einfache Teilmenge von Windows funktioniert.
    -   Alle ausführbaren Dateien, die mithilfe einer API registriert werden, sind für einen bestimmten Benutzer zulässig.
    -   Spiele, die als zulässig festgelegt sind, unterspielen Einschränkungen.
-   Beachten Sie, dass der RUNAS-Befehl für einen Benutzer blockiert wird, wenn überhaupt nicht auf ON fest steht.

 

 



