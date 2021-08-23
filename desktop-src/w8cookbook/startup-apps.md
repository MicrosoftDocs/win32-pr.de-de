---
title: Starten von Apps
description: Starten von Apps
ms.assetid: 3519CB52-A6EC-4819-87FE-C144801BDD9F
keywords:
- Start-App
- Hintergrundaufgabe
- Ausführen des Schlüssels
- RunOnce
- Startordner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbc2dc2a73a08c3aebd265c209b407646e50a6cb1b7cba630884cf719330b8dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815050"
---
# <a name="startup-apps"></a>Starten von Apps

## <a name="platform"></a>Plattform

**Clients** Windows 8     


## <a name="description"></a>Beschreibung

Einer der großen Windows ist die Möglichkeit, verschiedene Formfaktoren zu beleuchten, von herkömmlichen Desktops und Laptops bis hin zu low-powered Tablets. Um sicherzustellen, dass unsere gegenseitigen Kunden eine hervorragende Erfahrung mit jedem Formfaktor haben, den sie mit Windows auswählen, sind zwei wichtige Erfolgsmetriken, die berücksichtigt werden müssen, eine höhere Akkulaufzeit und eine hervorragende PC-Reaktionsfähigkeit. Um dies zu erreichen, wurden Verbesserungen in mehreren Bereichen von Windows vorgenommen, einschließlich Prozesslebenszyklus, Standbyzuständen und Start-Apps (Apps mit automatisiertem Start nach dem Start des Computers). Dieses Thema hebt einige der Auswirkungen hervor, die Start-Apps auf ein Windows Gerät haben, und bietet Entwicklern (ISV/IHV) und OEMs Anleitungen, um die Nutzungsmuster von Start-Apps zu überdenken, um die Akkulaufzeit und Reaktionsfähigkeit für unsere gemeinsamen Kunden zu verbessern. Außerdem werden die Änderungen in Windows beschrieben, mit denen Benutzer bestimmen können, welche der Start-Apps tatsächlich ausgeführt werden sollen.

Windows Store-Apps sind so konzipiert, dass sie neue Standards für Akkuverbrauch und Reaktionsfähigkeit einhalten, und Windows verwaltet ihren Lebenszyklus durch Anhalten und/oder Beenden. Desktop-Apps, die für frühere Windows Versionen entwickelt wurden, wurden jedoch nicht notwendigerweise so konzipiert, dass sie die Akkulaufzeit beibehalten oder auf Benutzeraktivitäten reagieren, und können sich auf die Reaktionsfähigkeit des Systems auswirken (z. B. wenn eine App einen regulären 1-Sekunden-Heartbeat sendet, um nach Updates zu suchen, oder vorab Arbeitsspeicher vorab zuweist, falls sie ihn später benötigt). Dies kann für den Benutzer, der einen Windows Tablet-PC mit einer langen Akkulebenserwartung und wochenlanger Standbydauer kauft, eine schlechte Erfahrung erzielen, aber ermittelt, dass die Akkulaufzeit des Tablets diese Ziele nicht erreicht. Da Start-Apps im Hintergrund ausgeführt werden, kann die Anzahl von Apps, die auf dem System ausgeführt werden, deutlich höher sein als das, was dem Benutzer bekannt ist, und sich auf die Reaktionsfähigkeit des Systems auswirken. Start-Apps sind so klassifiziert, dass sie diejenigen umfassen, die diese Mechanismen nutzen, um zu starten:

-   Ausführen von Registrierungsschlüsseln (HKLM, HKCU, Wow64-Knoten enthalten)
-   RunOnce-Registrierungsschlüssel
-   Startordner im Startmenü für benutzer- und öffentliche Speicherorte

Windows wurden neue Funktionen hinzugefügt, um sicherzustellen, dass Endbenutzer immer die Kontrolle über die Apps haben, die auf ihren Systemen ausgeführt werden. Auf der Registerkarte Start in Task-Manager wird eine Liste der Start-Apps sowie Steuerelemente angezeigt, mit denen Benutzer Start-Apps deaktivieren können. Damit Benutzer bestimmen können, was deaktiviert werden soll, zeigt Task-Manager ein Maß für die Auswirkungen der einzelnen Start-Apps an. Die Auswirkungen werden basierend auf der CPU- und Datenträgerauslastung einer App beim Start bewertet. Die Auswirkungswerte werden durch Anwenden der folgenden Kriterien bestimmt:

-   **Hohe Auswirkungen**   Apps, die mehr als eine Sekunde CPU-Zeit oder mehr als 3 MB Datenträger-E/A beim Start verwenden
-   **Mittlere Auswirkung**   Apps, die 300 ms – 1000 ms CPU-Zeit oder 300 KB – 3 MB Datenträger-E/A verwenden
-   **Geringe Auswirkung**   Apps mit weniger als 300 ms CPU-Zeit und weniger als 300 KB Datenträger-E/A

Microsoft stellt Tools bereit, mit denen App-Entwickler ihre Auswirkungen auf das Startverhalten bewerten, analysieren und Maßnahmen ergreifen können, um ihre Auswirkungen auf das Startverhalten zu verringern und die Benutzerfreundlichkeit zu verbessern. Das Assessment and Deployment Kit bietet die Möglichkeit, eine Startleistungsbewertung durchzuführen und die Auswirkungen von Apps zu messen, die beim Start ausgeführt werden. Die Bewertungsergebnisse enthalten ggf. detaillierte Analyse- und Wartungsinformationen für die wichtigsten Komponenten beim Start Windows. Mithilfe des Windows Leistungsanalyse können App-Entwickler eine umfassende Analyse durchführen, um die Grundursache der Leistungsbeeinträchtigung zu ermitteln und Windows Startleistung zu verbessern. Installieren Sie die Windows ADK [von hier](/previous-versions/windows/hh825494(v=win.10))aus.

## <a name="guidance"></a>Anleitung

Start-Apps umfassen mehrere Kategorien, wie in der folgenden Tabelle beschrieben. Eine Reihe von Empfehlungen für Entwickler wird den Kategorien von Start-Apps zugeordnet, die mit den oben beschriebenen Windows funktionalen Änderungen übereinstimmen.



Kategorien von Start-Apps

BESCHREIBUNG

Empfehlung

**Updater**

Überwachen und Aktualisieren von Benutzern auf Onlineupdates

**Wartungstask**

> [!Note]  
> Alle Updates sollten Wartungstasks ohne Anforderungen an die Benutzeroberflächeninteraktion sein. Apps sollten sich einfach nur still aktualisieren und bei Einem Fehler ein Rollback durchführen.

<br/>

${ROWSPAN2}$**Hardwareunterstützung**${REMOVE}$  

Alternative Zugriffspunkte

Bereitstellen des Zugriffs auf Windows Features und Apps, auf die über andere Zugriffspunkte in Windows

**Entfernen**

> [!Note]  
> Der Schlüssel besteht darin, doppelte Features zu reduzieren, die in Windows

<br/>

Antragsteller

Bereitstellen von Benachrichtigungen für Benutzer zu ihren Geräten

**Entfernen**

> [!Note]  
> Windows stellt Benutzern Benachrichtigungen zu ihren Geräten bereit.

<br/>

**Vorabstarts**

Einige vorläufige Aktivitäten, die von Apps benötigt werden, werden während der Benutzeranmeldung an eine Start-App ausgelagert.

**Entfernen**

> [!Note]  
> Windows 8 ist für eine schnelle Benutzeroberfläche für App-Starte optimiert.

<br/>

${ROWSPAN4}$**Hilfsprogramm**${REMOVE}$  

PC-Synchronisierung

Bereitstellen von Synchronisierungsfunktionen für mehrere Systeme

**Start** (Potenzielle Updates in der Betaversion)

Sicherung und Wiederherstellung

Einstiegspunkt zum Speichern und Wiederherstellen des Zustands von Dateien, Einstellungen oder ganzen Systemen

**Windows Store App für die Benutzerverknüpfung**

Telemetrie

Sammeln und Senden von Informationen zur Benutzeroberfläche und Umgebung

**Wartungstask**

PC-Überwachung

Bereitstellen nicht angeforderter Systemstatusüberwachung und Benachrichtigungen, die vorhandene Posteingangsfunktionen duplizieren

**Entfernen**

> [!Note]  
> Der Schlüssel besteht darin, doppelte Features zu reduzieren, die in Windows

<br/>

${ROWSPAN2}$**Sicherheit**${REMOVE}$  

Filter für die jugendschutz &

Erzwingen von Regeln und Einschränkungen für Internetzugriff und -nutzung

**Startup**

Konfiguration und Verwaltung

Benutzern das Steuern von Diagnose- und Wiederherstellungsoptionen für die Systemsicherheitsüberwachung erlauben Benachrichtigen von Benutzern über Ergebnisse und Sicherheitsaktionen

**Windows Store App für die Benutzerverknüpfung**

**Kommunikation & Internet** (IM & VoIP)

Senden und Empfangen von Nachrichten und Aufrufen

**Windows Store-App**

**Musik & MP3**

Wiedergeben, Speichern und Verwalten von Musik

**Windows Store-App**

**Foto & Video**

Erkennen, Aufzeichnen, Rendern, Speichern und Verwalten von Fotos und Videos

**Windows Store-App**

**PC Gaming**

Starten von Spielen in verschiedenen Domänen

**Windows Store-App**

**Upsell & Advertisement**

Aufmerksamkeit auf Waren und Dienstleistungen lenken, die zum Kauf verfügbar sind

**Entfernen**



 

> [!Note]  
> Richtlinien für Barrierefreiheits-Apps werden durch separate direkte Interaktionen mit ISVs abgedeckt. Weitere Informationen finden Sie [*unter Programmieren für Erleichterte Bedienung.*](../winauto/ease-of-access---assistive-technology-registration.md)

 

**Windows Store-Apps**

Windows Store-Apps verbessern die Benutzerfreundlichkeit, indem sie einen Windows-Raum mit neuen Koordinaten einführen: ein neues App-Modell, eine neue Benutzeroberfläche und eine Windows Store. Diese Sprach- und Präsentationsframeworkoptionen sind für die Entwicklung Windows Store verfügbar:

-   HTML/JavaScript/CSS
-   XAML/C #
-   XAML/C++

Aggregierte Informationen zum Entwickeln von Windows Store-Apps finden Sie unter [Windows Dev Center](https://msdn.microsoft.com/windows/apps/).

Beispiele:

-   [Entwickeln Windows Store Spielen](/previous-versions/windows/apps/hh452744(v=win.10))
-   [Entwickeln Windows Store-App, die Medien verwendet](/previous-versions/windows/apps/hh465132(v=win.10))

**Automatische Wartungsaufgaben**

Periodische Hintergrundaktivitäten sollten als Automatische Wartung entworfen werden. Diese werden zur Leerlaufzeit des Systems geplant, um die Reaktionsfähigkeit und Energieeffizienz Windows PCs zu erhöhen. Wartungsaufgaben können mithilfe des Desktop-SDK von einer Desktop-App zur Installationszeit erstellt und konfiguriert werden. Weitere Informationen Automatische Wartung im folgenden Thema.

## <a name="resources"></a>Ressourcen

-   [Richtlinien für die Barrierefreiheit](../winauto/ease-of-access---assistive-technology-registration.md)
-   [Windows Developer Center](https://msdn.microsoft.com/windows/apps/)
-   [Windows ADK](/previous-versions/windows/hh825494(v=win.10))

 

