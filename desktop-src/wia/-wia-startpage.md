---
description: Windows-Abbild Beschaffung (WIA) ist die noch immer Abbild Erfassungs Plattform in der Windows-Betriebssystem Familie, beginnend mit Windows Millennium Edition (Windows Me) und Windows XP.
ms.assetid: 8f32422e-25ec-48bc-9d79-57dbb3b53e93
title: Windows-Bilderfassung (WIA)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0ff1f3fb51a4c87d909637a90591336d9d2eb30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526420"
---
# <a name="windows-image-acquisition-wia"></a>Windows-Bilderfassung (WIA)

Windows-Abbild Beschaffung (WIA) ist die noch immer Abbild Erfassungs Plattform in der Windows-Betriebssystem Familie, beginnend mit Windows Millennium Edition (Windows Me) und Windows XP.

-   [Introduction (Einführung)](#introduction)
-   [Vorteile der Windows-Abbild Erfassung 2,0](#benefits-of-windows-image-acquisition-20)
    -   [Für Anwendungs Schreiber](#for-application-writers)
    -   [Für Gerätehersteller](#for-device-manufactures)
    -   [Für Scanner-Benutzer](#for-scanner-users)
-   [Entwicklung von Windows-Abbild Käufen](#development-of-windows-image-acquisition)
-   [Übersicht über die Windows-Abbild Erfassung](#overview-of-windows-image-acquisition)
-   [Fakten zur Windows-Abbild Erfassung 2,0](#facts-about-windows-image-acquisition-20)
-   [Entwickler Zielgruppe](#developer-audience)
-   [Lauf Zeitanforderungen](#run-time-requirements)
-   [Themen zu WIA](#wia-topics)

## <a name="introduction"></a>Einführung

Die WIA-Plattform ermöglicht Bild Verarbeitungs-/grafieanwendungen die Interaktion mit der Bildverarbeitungshardware und die Standardisierung der Interaktion zwischen verschiedenen Anwendungen und Scannern. Dadurch können die verschiedenen Anwendungen mit diesen unterschiedlichen Scannern kommunizieren und damit interagieren, ohne dass die Anwendungs Schreiber und Scanner Ihre Anwendung oder Treiber für jede Kombination aus Anwendungs Gerät anpassen müssen.

![Grafik, die die grundlegende Architektur von WIA als bidirektionale Schicht zwischen Bildverarbeitungsanwendungen und Geräten anzeigt. ](images/wia-diagram1.png)

## <a name="benefits-of-windows-image-acquisition-20"></a>Vorteile der Windows-Abbild Erfassung 2,0

WIA bietet Vorteile für Anwendungsentwickler, Gerätehersteller und Scanner, die mit der Bildverarbeitungshardware interagieren müssen.

### <a name="for-application-writers"></a>Für Anwendungs Schreiber

-   Windows führt einen Zertifizierungsprozess für WIA-Treiber aus, damit WIA-Anwendungen sicher mit allen WIA-basierten Scannern kompatibel sind.
-   WIA-Treiber werden in den WIA-Dienst Prozess geladen und bieten somit eine stabilere Treiber Umgebung.
-   Anwendungen können über die Schaltfläche Scanner Scan mithilfe von Push-Ereignissen initiiert werden, die vom WIA-Subsystem unterstützt werden.
-   Der WIA enthält einen standardmäßigen Segmentierungs Filter, den alle Treiber nutzen können. auf diese Weise müssen Anwendungen keinen Code für die Überprüfung in mehreren Regionen schreiben, wie z. b. das Aufteilen einer großen Anzahl von Fotos, die über einen flatlover-Scanner verteilt sind.

### <a name="for-device-manufactures"></a>Für Gerätehersteller

-   Der Prozess für die Erstellung eines WIA-Treibers unterstützt Entwickler bei der Einrichtung, dass der Treiber mit der Anwendung kompatibel ist.
-   WIA-Treiber können einen integrierten Segmentierungs Filter, Bild Verarbeitungs Filter und Fehlerhandler nutzen, wenn Sie sich dafür entscheiden.
-   WIA-basierte Scanner funktionieren direkt in Windows mit Windows-Scananwendungen wie Windows Fax und Scan und Paint.
-   WIA-Treiber bieten eine bessere Integration in Windows, z. b. die vollständige Geräteleistung.
-   Die Windows Vista-Version umfasst einen WSD-WIA-Klassen Treiber, mit dem alle Geräte, die mit dem WS-Scan-Protokoll (Web Services for Scanner) kompatibel sind, mit WIA-Anwendungen ohne zusätzlichen Treiber oder Software arbeiten können.

### <a name="for-scanner-users"></a>Für Scanner-Benutzer

-   WIA-basierte Scanner können von Windows-Anwendungen wie Windows Fax und Scan und Paint verwendet werden, ohne dass zusätzliche Software erforderlich ist.
-   WIA-basierte Anwendungen und Scanner können auch WIA-Add-ons nutzen, wie z. b. den Segmentierungs Filter, der Funktionen wie die Verarbeitung einer Reihe von Bildern auf dem Scanner und das Scannen aller Daten in einzelne Dateien ohne Benutzereingriff ermöglicht.
-   WIA-basierte Geräte bieten eine viel bessere Integration in andere Windows-Features, wie z. b. das Device Stage-Feature für Windows 7.
-   WIA bietet eine robustere, stabilere und zuverlässigere Scanfunktion, indem der Treiber und die Anwendung isoliert werden.

## <a name="development-of-windows-image-acquisition"></a>Entwicklung von Windows-Abbild Käufen

Die Imaging-Architektur in Windows 2000 und Windows 95 oder höher umfasste eine Hardware Abstraktion auf niedriger Ebene, noch Bildarchitektur (STI) und eine allgemeine Gruppe von APIs, die als TWAIN bezeichnet werden. In Windows XP und Windows Me wurde es eingeführt. WIA ist eine Image Erstellungs Architektur, die auf STI aufbaut und keinen TWAIN erfordert, obwohl TWAIN weiterhin zusammen mit WIA unterstützt wird.

WIA 1,0 wurde in Windows Me und Windows XP eingeführt und unterstützt Scanner, digitale Kameras und digitale Videogeräte. WIA 2,0 wurde mit Windows Vista veröffentlicht. WIA 2,0 ist auf Scanner ausgerichtet, bietet jedoch weiterhin Unterstützung für ältere WIA 1,0-Anwendungen und-Geräte über eine WIA 1,0 bis WIA 2,0-Kompatibilitätsschicht, die vom WIA-Dienst bereitgestellt wird. Allerdings wurde die Unterstützung von Videoinhalten aus WIA für Windows Vista entfernt. Es wird empfohlen, Windows Portable Devices (WPD) API für digitale Kameras und digitale Videogeräte zu einem späteren Zeitpunkt zu betreiben. WIA 1,0-und STI TWAIN-Treiber werden weiterhin direkt unter Windows Vista und Windows 7 unterstützt, zusammen mit nativen WIA 2,0-Gerätetreibern und Abbild Erstellungs Anwendungen.

## <a name="overview-of-windows-image-acquisition"></a>Übersicht über die Windows-Abbild Erfassung

WIA stellt ein Framework bereit, mit dem ein Gerät seine einzigartigen Funktionen für das Betriebssystem bereitstellen kann und es Abbild Erstellungs Anwendungen ermöglicht, diese eindeutigen Funktionen aufzurufen.

Die WIA-Plattform umfasst ein Daten Erfassungs Protokoll, ein Gerätetreiber Modell und eine Schnittstelle (DDI), eine API und einen dedizierten WIA-Dienst. Die Plattform umfasst auch eine Reihe integrierter Kernelmodustreiber, die die Kommunikation mit Abbild Erstellungs Geräten unterstützen, die über USB-, Serielle/parallele, SCSI-und FireWire-Schnittstellen verbunden sind. Das WIA-Subsystem umfasst auch eine transparente Kompatibilitätsschicht, mit der TWAIN-kompatible Anwendungen auf WIA-Treiber basierende Geräte anwenden und verwenden können.

Mit der Netzwerkverbindung verbundene Abbild Erstellungs Geräte, die das WSD-Protokoll (Web Services for Devices) unterstützen, können von WIA-kompatiblen Abbild Erstellungs Anwendungen unter Windows Vista und Windows 7 standardmäßig über einen WSD-WIA-Klassen Treiber verwendet werden, der als Teil von Windows Vista ausgeliefert wird. Der Klassen Treiber konvertiert WIA-Aufrufe von WSD-aufrufen und bewirkt, dass bereits vorhandene WIA-Anwendungen mit WSD-basierten Scannern ohne zusätzlichen Treiber funktionieren.

WIA-Treiber bestehen aus einer Komponente der Benutzeroberfläche (UI) und einer Kern Treiber Komponente, die in zwei unterschiedliche Prozess Räume geladen wurde: die Benutzeroberfläche im Anwendungsbereich und die treiberkerne im WIA-Dienstbereich. Der Dienst wird im Kontext des lokalen Systems in Windows XP ausgeführt und wird im Kontext des lokalen Diensts gestartet, beginnend mit Windows Server 2003 und Windows Vista, um die Sicherheit gegen fehlerhafte oder böswillige Treiber zu erhöhen.

![Grafik, die die Architektur von WIA und deren Funktionsweise als Dienst anzeigt.](images/wia-arch.png)

Der WIA-API-Satz stellt Abbild Erstellungs Anwendungen zum Abrufen von Hardwarefunktionen für die Image Beschaffung bereit

-   Enumeration der verfügbaren Abbild Erwerbs Geräte.
-   Gleichzeitiges Erstellen von Verbindungen mit mehreren Geräten.
-   Abfragen von Eigenschaften von Geräten in einer standardmäßigen und erweiterbaren Weise.
-   Gerätedaten werden mithilfe von Standard-und Hochleistungs Übertragungsmechanismen abgerufen.
-   Verwalten von Image-Eigenschaften über Datenübertragungen hinweg
-   Benachrichtigung über den Gerätestatus und die Verarbeitung von Scan Ereignissen.

Windows hat Skriptunterstützung für WIA hinzugefügt, indem die WIA-Automatisierungs Bibliothek in 2002 freigegeben wurde, die in Windows Vista als Windows-Abbild Erwerbs-Automatisierungs Schicht (WIA) integriert war und weiterhin Teil von Windows 7 ist. Die WIA Automation Library bietet End-to-End-Abbild Erfassungs Funktionen für Automatisierungs fähige Anwendungsentwicklungsumgebungen und Programmiersprachen wie Microsoft Visual Basic 6,0 Active Server Pages (ASP), VBScript und C \# .

Für Windows 7 verfügen WIA-APIs über zusätzliche Unterstützung, um die bereits vorhandene Unterstützung für pushscans zu ergänzen.

-   Automatisch konfiguriertes Gerät initiierte Überprüfung mit Überprüfungs Parametern, die bei der Überprüfung auf dem Geräte-Front-Panel konfiguriert sind.
-   Automatische Quell Auswahl für vom Gerät initiierte Überprüfung.

## <a name="facts-about-windows-image-acquisition-20"></a>Fakten zur Windows-Abbild Erfassung 2,0

-   Der Datenübertragungsmechanismus in WIA 2,0 ist Datenstrom basiert. Die streamabstraktion entfernt den Unterschied zwischen verschiedenen Übertragungs Typen und ermöglicht außerdem den Austausch von einvernehmlich vereinbarten Metadaten zwischen Gerät und Anwendung.
-   Das WIA 2,0-Subsystem enthält auch ein einfaches Bild Verarbeitungs Filter-Treiber-Add-on, das optional vom Scanner-Treiber ersetzbar ist, wenn der Treiber einen angepassten Bild Verarbeitungs Filter bereitstellt. Der integrierte Filter ermöglicht die nach Verarbeitung von Images, die über den Scanner abgerufen wurden. Der Bild Verarbeitungs Filter aktiviert auch Live-Software Vorschau, wenn kleine Einstellungen wie Helligkeit und Kontrast angepasst werden.
-   Der Segmentierungs Filter ist eine weitere praktische WIA-Komponente, die durch einen stärker angepassten Filter durch den Scanner ersetzt werden kann. Der Segmentierungs Filter kann für das Scannen in mehreren Regionen verwendet werden. Die Überprüfung in mehreren Regionen ermöglicht es einer Anwendung beispielsweise, unterschiedliche Überprüfungs Bereiche ohne Benutzereingriff automatisch zu erkennen, wie z. b. das Identifizieren einer Reihe von Fotos, die nach dem Zufallsprinzip auf dem Scanner angezeigt werden.
-   WIA 2,0 stellt einen ersetzbaren/erweiterbaren Fehlerhandler bereit, um Software-, Hardware-und Konfigurationsfehler und Verzögerungen ordnungsgemäß zu behandeln und ggf. wiederherzustellen. Der Fehlerhandler ist eine andere WIA-Komponente, die durch eine stärker angepasste Version des Scanner-Treibers ersetzt werden kann. Diese Erweiterung liefert Status-und Fehlermeldungen während der Daten übernahmen, z. b. "Lamp-Aufwärmphase", "Abdeckung offen", "Papierstau" usw. Diese Erweiterung ermöglicht außerdem eine saubere Unterstützung für "Abbruch Vorgänge".

## <a name="developer-audience"></a>Entwicklerzielgruppe

Die WIA-API ist für die Verwendung durch C/C++-Programmierer konzipiert. Vertrautheit mit der Windows-GUI und den Component Object Model-Schnittstellen (com) ist erforderlich.

Für Entwickler, die mit Microsoft Visual Basic 6,0, Active Server Pages (ASP) oder der Skripterstellung vertraut sind, bietet WIA eine Automatisierungs Schicht für Windows XP Service Pack 1 (SP1) oder höher, die auf der Grundlage von C/C++ basiert und den Zugriff vereinfacht. Weitere Informationen zur Automatisierungs Schicht finden Sie unter [Automatisierungs Schicht für Windows-Abbild Erfassung](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).

> [!Note]  
> Die WIA-Automatisierungs Schicht ersetzt die Windows-Abbild Erfassung (WIA) 1,0-Skripterstellung.

 

## <a name="run-time-requirements"></a>Laufzeitanforderungen

Für Anwendungen, die die WIA-API verwenden, ist Windows XP oder höher erforderlich.

## <a name="wia-topics"></a>Themen zu WIA

Die WIA-Themen sind so organisiert, wie in der folgenden Tabelle dargestellt.



|                                                                                                                              |                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [Informationen zur Windows-Abbild Erfassung](-wia-about-windows-image-acquisition.md)                                                  | Allgemeine Informationen zu WIA                                                                     |
| [Windows-Abbild Erfassungs Treiber](/windows-hardware/drivers/image/windows-image-acquisition-drivers)                  | WIA-Treiberentwicklung                                                                            |
| [Automatisierungs Schicht für Windows-Abbild Erfassung](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage) | WIA-Automatisierungs Schicht                                                                              |
| [WIA-Tutorial](-wia-wia-tutorial.md)                                                                                        | Exemplarische Vorgehensweise für Code, der im Software Development Kit (SDK) enthalten ist, der sich auf bestimmte Aufgaben konzentriert |
| [Verweis](-wia-reference.md)                                                                                              | Informationen zu WIA-Schnittstellen,-Methoden,-Objekten und-Datentypen, die in C/C++ und Skripterstellung verwendet werden.      |



 

 

 
