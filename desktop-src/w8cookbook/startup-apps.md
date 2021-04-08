---
title: Start-apps
description: Start-apps
ms.assetid: 3519CB52-A6EC-4819-87FE-C144801BDD9F
keywords:
- Start-App
- Hintergrundaufgabe
- Taste ausführen
- RunOnce
- Startordner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75a12f01dac073712512206a5c432561b4a0b75e
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "103734632"
---
# <a name="startup-apps"></a>Start-apps

## <a name="platform"></a>Plattform

**Clients**   Windows 8  


## <a name="description"></a>BESCHREIBUNG

Eine der großen Wett-und Windows-Anwendungen ist die Möglichkeit, verschiedene Formfaktoren, von herkömmlichen Desktops und Laptops bis hin zu kleinen Tablets, zu untersuchen. Um sicherzustellen, dass unsere wechselseitigen Kunden eine gute Benutzeroberfläche für jeden von Ihnen gewählten Formfaktor haben, sind zwei wichtige Erfolgs Metriken, die berücksichtigt werden müssen, eine größere Akku Lebensdauer und eine ausgezeichnete PC-Reaktionsfähigkeit. Um dies zu erreichen, wurden Verbesserungen an mehreren Windows-Bereichen vorgenommen, einschließlich Prozess Lebenszyklus, Ruhezustand und Start-apps (Apps mit automatisiertem Start nach dem Starten des Computers). In diesem Thema werden einige der Auswirkungen von Start-apps auf einem Windows-Gerät hervorgehoben und Anleitungen für Entwickler (ISV/IHV) und OEMs bereitstellt, um die Verwendungs Muster von Start-apps zu überdenken, um die Akku Lebensdauer und Reaktionsfähigkeit unserer gegenseitigen Kunden zu verbessern. Außerdem werden die Änderungen in Windows beschrieben, mit denen Benutzer steuern können, welche der Start-apps tatsächlich ausgeführt werden.

Windows Store-Apps sind so konzipiert, dass Sie neuen Standards für den Akku Verbrauch und die Reaktionsfähigkeit entsprechen, und Windows verwaltet ihren Lebenszyklus, indem Sie angehalten und/oder beendet wird. Desktop-Apps, die für frühere Windows-Versionen entwickelt wurden, wurden jedoch nicht notwendigerweise so entworfen, dass Sie die Akku Lebensdauer beibehalten oder die Benutzeraktivität beeinträchtigen können. Sie können sich auch auf die Reaktionsfähigkeit des Systems auswirken (z. b. Wenn eine APP einen regulären 1-Sekunden-Takt sendet, um nach Updates zu suchen, oder den Arbeitsspeicher vorab bereitstellen). Dies kann für den Benutzer, der einen Windows-Tablet PC kauft, mit einer langen Akku Lebensdauer und Wochen im Standbymodus eine schlechte Benutzer Leistung schaffen, aber es wird feststellt, dass die Akku Lebensdauer des Tablets diese Ziele nicht erreicht. Da Start-apps im Hintergrund ausgeführt werden, kann die Anzahl von apps, die auf dem System ausgeführt werden, deutlich länger sein als das, was der Benutzer kennt, und sich auf die Reaktionsfähigkeit des Systems auswirken. Start-apps werden klassifiziert, um diejenigen zu berücksichtigen, die diese Mechanismen zum Starten nutzen:

-   Ausführen von Registrierungs Schlüsseln (HKLM, HKCU, WOW64-Knoten eingeschlossen)
-   RunOnce-Registrierungsschlüssel
-   Startordner im Startmenü für Benutzer-und öffentliche Speicherorte

Windows wurde eine neue Funktionalität hinzugefügt, um sicherzustellen, dass Endbenutzer immer die Kontrolle über die apps haben, die auf Ihren Systemen ausgeführt werden. Auf der Registerkarte "Start" im Task-Manager wird eine Liste der Start-apps angezeigt. Außerdem werden Steuerelemente angezeigt, mit denen Benutzer Start-apps deaktivieren Um Benutzern zu helfen, zu deaktivieren, was deaktiviert werden soll, zeigt der Task-Manager ein Measure für jede Auswirkung der Start-APP an Die Auswirkung wird basierend auf der CPU und der Datenträger Nutzung einer APP beim Start bewertet. Die Auswirkung von Werten wird durch Anwenden der folgenden Kriterien bestimmt:

-   **Hohe Auswirkung**   Apps, die mehr als eine Sekunde CPU-Zeit oder mehr als 3 MB Datenträger-e/a beim Start verwenden
-   **Mittlere Auswirkung**   Apps mit 300 MS-1000 ms CPU-Zeit oder 300 KB-3 MB Datenträger-e/a
-   **Geringe Auswirkung**   Apps, die weniger als 300 ms CPU-Zeit und weniger als 300 KB Datenträger-e/a verwenden

Microsoft stellt Tools bereit, die APP-Entwicklern bei der Bewertung, Analyse und Durchführung von Maßnahmen unterstützen, um die Auswirkungen auf den Start zu verringern und die Benutzer Das Assessment and Deployment Kit bietet die Möglichkeit, eine Start Leistungsbewertung auszuführen und die Auswirkungen von apps zu messen, die beim Start ausgeführt werden. Die Bewertungsergebnisse enthalten ggf. detaillierte Analyse-und Wiederherstellungs Informationen für die wichtigsten Komponenten beim Windows-Start. Mithilfe von Windows Performance Analyzer können App-Entwickler eine umfassende Analyse durchführen, um die Grundursache der Auswirkungen auf die Leistung zu ermitteln und die Windows-Startleistung zu verbessern. Installieren Sie das Windows ADK von [hier](/previous-versions/windows/hh825494(v=win.10)).

## <a name="guidance"></a>Leitfaden

Start-apps umfassen mehrere Kategorien, wie in der folgenden Tabelle beschrieben. Eine Reihe von Empfehlungen für Entwickler werden den Kategorien von Start-apps zugeordnet, um die oben beschriebenen Windows-Funktionsänderungen auszurichten.



Kategorien von Start-apps

BESCHREIBUNG

Empfehlung

**Aktualisierungen**

Überwachen und Aktualisieren von Benutzern für Online Updates

**Wartungs Task**

> [!Note]  
> Alle Updates sollten Wartungs Tasks sein, ohne dass Anforderungen an die UI-Interaktion bestehen. Apps sollten sich einfach selbst aktualisieren und bei einem Fehler ein Rollback durchführen.

<br/>

$ {ROWSPAN2} $**Hardware Unterstützung**$ {Remove} $  

Alternative Zugriffspunkte

Bereitstellen des Zugriffs auf Windows-Features und-apps, die über andere Zugriffspunkte in Windows zugänglich sind

**Remove**

> [!Note]  
> Der Schlüssel besteht darin, doppelte Features zu verringern, die in Windows vorhanden sind.

<br/>

Benachrichtigt

Benutzern Benachrichtigungen zu Ihren Geräten bereitstellen

**Remove**

> [!Note]  
> Windows stellt Benachrichtigungen für Benutzer über Ihre Geräte bereit.

<br/>

**Pre-Launcher**

Einige der für apps benötigten vorläufigen Aktivitäten werden bei der Benutzeranmeldung in eine Start-App verlagert.

**Remove**

> [!Note]  
> Windows 8 ist für eine schnelle Darstellung von App-Starts optimiert.

<br/>

$ {ROWSPAN4} $**Utility**$ {Remove} $  

PC-Synchronisierung

Bereitstellen von Synchronisierungs Funktionen über mehrere Systeme hinweg

**Start** (potenzielle Updates in der Beta Version)

Sicherung und Wiederherstellung

Einstiegspunkt zum Speichern und Wiederherstellen des Zustands von Dateien, Einstellungen oder ganzen Systemen

**Windows Store-App für die Schnittstellen mit den Benutzern**

Telemetrie

Sammeln und Senden von Informationen über die Benutzerumgebung und die Umgebung

**Wartungs Task**

PC-Überwachung

Bereitstellen von angeforderter Systemstatus Überwachung und Benachrichtigungen, die vorhandene Eingangsbox

**Remove**

> [!Note]  
> Der Schlüssel besteht darin, doppelte Features zu verringern, die in Windows vorhanden sind.

<br/>

$ {ROWSPAN2} $**Security**$ {Remove} $  

Eltern Steuerungs & Filter

Erzwingen von Regeln und Einschränkungen für den Zugriff auf das Internet und die Verwendung

**Startup**

Konfiguration und Verwaltung

Benutzern das Steuern von Diagnose-und Wiederherstellungsoptionen für die Überwachung der Systemsicherheit gestatten Benutzer über Ergebnisse und Sicherheitsaktionen Benachrichtigen

**Windows Store-App für die Schnittstellen mit den Benutzern**

**Kommunikation & Internet** (im & VoIP)

Senden und empfangen von Nachrichten und aufrufen

**Windows Store-App**

**Musik & MP3**

Spielen, speichern und Verwalten von Musik

**Windows Store-App**

**Foto & Video**

Erkennen, aufzeichnen, wiedergeben, speichern und Verwalten von Fotos und Videos

**Windows Store-App**

**PC-Gaming**

Spiele in verschiedenen Domänen starten

**Windows Store-App**

**Upsell-& Ankündigung**

Aufmerksamkeit auf waren und Dienste, die für den Kauf verfügbar sind

**Remove**



 

> [!Note]  
> Richtlinien für Barrierefreiheit-apps werden durch separate direkte Verpflichtungen mit ISVs abgedeckt. Weitere Informationen finden Sie [*unter Programmieren für den einfachen Zugriff*](../winauto/ease-of-access---assistive-technology-registration.md) .

 

**Windows Store-Apps**

Windows Store-Apps verbessern die Benutzeroberfläche durch die Einführung eines Windows-Raums mit neuen Koordinaten: ein neues app-Modell, eine neue Benutzeroberfläche und einen Windows Store. Diese sprach-und Präsentations Framework-Optionen sind für die Entwicklung von Windows Store-Apps verfügbar:

-   HTML/JavaScript/CSS
-   XAML/C #
-   XAML/C++

Aggregierte Informationen für die Entwicklung von Windows Store-Apps finden Sie im [Windows dev Center](https://msdn.microsoft.com/windows/apps/).

Beispiele:

-   [Entwickeln von Windows Store-spielen](/previous-versions/windows/apps/hh452744(v=win.10))
-   [Entwickeln einer Windows Store-App, die Medien verwendet](/previous-versions/windows/apps/hh465132(v=win.10))

**Automatische Wartungs Tasks**

Periodische Hintergrund Aktivitäten sollten als automatische Wartungs Tasks entworfen werden. Diese werden zur Leerlaufzeit des Systems geplant, um die Reaktionsfähigkeit und Energieeffizienz von Windows-PCs zu erhöhen. Wartungs Tasks können von einer Desktop-App zur Installationszeit mithilfe des Desktop SDK erstellt und konfiguriert werden. Weitere Informationen finden Sie im folgenden Thema zur automatischen Wartung.

## <a name="resources"></a>Ressourcen

-   [Richtlinien für Barrierefreiheit](../winauto/ease-of-access---assistive-technology-registration.md)
-   [Windows Developer Center](https://msdn.microsoft.com/windows/apps/)
-   [Windows ADK](/previous-versions/windows/hh825494(v=win.10))

 

