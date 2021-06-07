---
description: Windows Image Acquisition (WIA) ist die Plattform für die Imageerfassung in der Windows-Betriebssystemfamilie, die mit Windows Edition (Windows Me) und Windows XP beginnt.
ms.assetid: 8f32422e-25ec-48bc-9d79-57dbb3b53e93
title: Windows-Bilderfassung (WIA)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 664b5accaa1312eae3baf6161e41c9c65e718c69
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443091"
---
# <a name="windows-image-acquisition-wia"></a>Windows-Bilderfassung (WIA)

Windows Image Acquisition (WIA) ist die Plattform für die Imageerfassung in der Windows-Betriebssystemfamilie, die mit Windows Edition (Windows Me) und Windows XP beginnt.

-   [Introduction (Einführung)](#introduction)
-   [Vorteile der Windows-Imageerfassung 2.0](#benefits-of-windows-image-acquisition-20)
    -   [Für Anwendungsautoren](#for-application-writers)
    -   [Für Gerätehersteller](#for-device-manufactures)
    -   [Für Scannerbenutzer](#for-scanner-users)
-   [Entwicklung der Windows-Imageerfassung](#development-of-windows-image-acquisition)
-   [Übersicht über die Windows-Imageerfassung](#overview-of-windows-image-acquisition)
-   [Fakten zur Windows-Imageerfassung 2.0](#facts-about-windows-image-acquisition-20)
-   [Entwicklergruppe](#developer-audience)
-   [Laufzeitanforderungen](#run-time-requirements)
-   [WIA-Themen](#wia-topics)

## <a name="introduction"></a>Einführung

Die WIA-Plattform ermöglicht Bildverarbeitungs-/Grafikanwendungen die Interaktion mit Imaginghardware und standardisiert die Interaktion zwischen verschiedenen Anwendungen und Scannern. Dies ermöglicht es diesen verschiedenen Anwendungen, mit diesen verschiedenen Scannern zu kommunizieren und mit ihnen zu interagieren, ohne dass die Anwendungsautoren und Scannerhersteller ihre Anwendungen oder Treiber für jede Kombination aus Anwendung und Gerät anpassen müssen.

![Grafik, die die grundlegende Architektur von wia als bidirektionle Ebene zwischen imagegebenden Anwendungen und Geräten zeigt. ](images/wia-diagram1.png)

## <a name="benefits-of-windows-image-acquisition-20"></a>Vorteile der Windows-Imageerfassung 2.0

WIA bietet Vorteile für Anwendungsentwickler, Gerätehersteller und Scannerbenutzer, die mit der Imageerstellungshardware interagieren müssen.

### <a name="for-application-writers"></a>Für Anwendungsautoren

-   Windows führt einen Zertifizierungsprozess für WIA-Treiber aus, sodass WIA-Anwendungen garantiert mit allen WIA-basierten Scannern kompatibel sind.
-   WIA-Treiber werden in den WIA-Dienstprozess geladen und bieten somit eine stabilere Treiberumgebung.
-   Anwendungen können über die Überprüfungsschaltfläche über Pushereignisse initiiert werden, die vom WIA-Subsystem unterstützt werden.
-   Die WIA enthält einen Standardsegmentierungsfilter, den alle Treiber nutzen können. Auf diese Weise müssen Anwendungen keinen Code für die Überprüfung in mehreren Regionen schreiben, um beispielsweise eine große Anzahl von Fotos zu trennen, die über einen Flatbedscanner verteilt sind.

### <a name="for-device-manufactures"></a>Für Gerätehersteller

-   Der WIA-Treiberzertifizierungsprozess hilft Treiberentwicklern bei der Einrichtung, dass ihr Treiber WIA-konform ist.
-   WIA-Treiber können einen integrierten Segmentierungsfilter, einen Bildverarbeitungsfilter und einen Fehlerhandler nutzen, wenn sie sich dafür entscheiden.
-   WIA-basierte Scanner funktionieren direkt unter Windows mit Windows-Scananwendungen wie Windows-Fax und -Scan und Paint.
-   WIA-Treiber bieten eine bessere Integration in Windows, z. B. die vollständige Geräteerfahrung.
-   Die Windows Vista-Version enthält einen WSD-WIA-Klassentreiber, der allen Geräten, die mit dem WS-Scan-Protokoll (Web Services for Scanner) kompatibel sind, die Arbeit mit WIA-Anwendungen ohne zusätzlichen Treiber oder software ermöglicht.

### <a name="for-scanner-users"></a>Für Scannerbenutzer

-   WIA-basierte Scanner können von Windows-Anwendungen wie Windows-Fax und -Scan und Paint verwendet werden, ohne dass zusätzliche Software erforderlich ist.
-   WIA-basierte Anwendungen und Scanner können auch WIA-Add-Ons wie den Segmentierungsfilter nutzen, der Funktionen wie die Verarbeitung einer Reihe von Bildern auf dem Scanner und das Scannen aller Bilder in einzelnen Dateien ohne Benutzereingriff ermöglicht.
-   WIA-basierte Geräte bieten eine viel bessere Integration in andere Windows-Features, z. B. das feature Device Stage für Windows 7.
-   WIA bietet eine stabilere, stabilere und zuverlässigere Überprüfungserfahrung durch Isolieren des Treibers und der Anwendung.

## <a name="development-of-windows-image-acquisition"></a>Entwicklung der Windows-Imageerfassung

Die Bildverarbeitungsarchitektur in Windows 2000 und Windows 95 oder höher bestand aus einer low-level-Hardwareabstraktion, Still Image Architecture (STI) und einem hohen Satz von APIs, die als TWAIN bezeichnet werden. In Windows XP und Windows Me wurde WIA eingeführt. WIA ist eine Imagearchitektur, die auf STI aufbaut und TWAIN nicht erfordert, obwohl TWAIN weiterhin zusammen mit WIA unterstützt wird.

WIA 1.0 wurde in Windows Me und Windows XP eingeführt und unterstützt Scanner, Digitalkameras und digitale Videogeräte. WIA 2.0 wurde mit Windows Vista veröffentlicht. WIA 2.0 ist für Scanner vorgesehen, bietet aber weiterhin Unterstützung für ältere WIA 1.0-Anwendungen und -Geräte über eine vom WIA-Dienst bereitgestellte WIA 1.0-zu-WIA 2.0-Kompatibilitätsschicht. Die Unterstützung von Videoinhalten wurde jedoch aus WIA für Windows Vista entfernt. Wir empfehlen die WPD-API (Windows Portable Devices) für Digitalkameras und digitale Videogeräte in Zukunft. WIA 1.0- und STI-TWAIN-Treiber werden neben nativen WIA 2.0-Gerätetreibern und Imageerstellungsanwendungen weiterhin direkt unter Windows Vista und Windows 7 unterstützt.

## <a name="overview-of-windows-image-acquisition"></a>Übersicht über die Windows-Imageerfassung

WIA bietet ein Framework, das es einem Gerät ermöglicht, seine einzigartigen Funktionen dem Betriebssystem zu präsentieren, und ermöglicht es Imageerstellungsanwendungen, diese einzigartigen Funktionen aufzurufen.

Die WIA-Plattform umfasst ein Datenerfassungsprotokoll, ein Gerätetreibermodell und eine Geräteschnittstelle (Device Driver Model and Interface, DDI), eine API und einen dedizierten WIA-Dienst. Die Plattform enthält auch eine Reihe integrierter Kernelmodustreiber, die die Kommunikation mit Imageerstellungsgeräten unterstützen, die lokal über USB-, serielle/parallele, SCSI- und FireWire-Schnittstellen verbunden sind. Das WIA-Subsystem enthält auch eine transparente Kompatibilitätsebene, die es TWAIN-kompatiblen Anwendungen ermöglicht, WIA-treiberbasierte Geräte zu verwenden und zu verwenden.

Mit dem Netzwerk verbundene Imageerstellungsgeräte, die das WSD-Protokoll (Web Services for Devices) unterstützen, können auch von WIA-kompatiblen Imaginganwendungen unter Windows Vista und Windows 7 über einen WSD-WIA-Klassentreiber verwendet werden, der als Teil von Windows Vista ausgeliefert wurde. Der Klassentreiber konvertiert WIA-Aufrufe in WSD-Aufrufe und umgekehrt und sorgt dafür, dass bereits vorhandene WIA-Anwendungen ohne zusätzlichen Treiber mit WSD-basierten Scannern funktionieren.

WIA-Treiber bestehen aus einer Komponente der Benutzeroberfläche (UI) und einer Kerntreiberkomponente, die in zwei verschiedene Prozessräume geladen werden: die Benutzeroberfläche im Anwendungsbereich und der Treiberkern im WIA-Dienstbereich. Der Dienst wird in Windows XP im Kontext des lokalen Systems und ab Windows Server 2003 und Windows Vista im Kontext des lokalen Diensts ausgeführt, um die Sicherheit vor fehlerhaften oder böswilligen Treibern zu erhöhen.

![Grafik, die die Architektur von wia und deren Funktionsweise als Dienst zeigt.](images/wia-arch.png)

Der WIA-API-Satz macht Imageerstellungsanwendungen für Hardwarefunktionen für die Imageerfassung verfügbar, indem Folgendes unterstützt wird:

-   Enumeration der verfügbaren Bilderfassungsgeräte.
-   Gleichzeitiges Erstellen von Verbindungen mit mehreren Geräten.
-   Abfragen von Eigenschaften von Geräten auf standard- und erweiterbare Weise.
-   Abrufen von Gerätedaten mithilfe von Standard- und Hochleistungsübertragungsmechanismen.
-   Verwalten von Imageeigenschaften über Datenübertragungen hinweg.
-   Benachrichtigung über den Gerätestatus und die Behandlung von Überprüfungsereignissen.

Windows hat WIA Skriptunterstützung hinzugefügt, indem die WIA Automation Library im Jahr 2002 veröffentlicht wurde, die in Windows Vista als Windows Image Acquisition (WIA) Automation Layer integriert wurde und weiterhin Teil von Windows 7 ist. Die WIA Automation Library bietet End-to-End-Imageerfassungsfunktionen für automatisierungsfähige Anwendungsentwicklungsumgebungen und Programmiersprachen wie Microsoft Visual Basic 6.0, Active Server Pages (ASP), VBScript und \# C.

Für Windows 7 verfügen WIA-APIs über zusätzliche Unterstützung, um die bereits vorhandene Unterstützung für Pushscans zu ergänzen.

-   Automatisch konfigurierte, vom Gerät initiierte Überprüfung mit Scanparametern, die auf dem Scanner im Geräte-Frontpanel konfiguriert sind.
-   Automatische Quellauswahl für vom Gerät initiierte Überprüfung.

## <a name="facts-about-windows-image-acquisition-20"></a>Fakten zur Windows-Imageerfassung 2.0

-   Der Datenübertragungsmechanismus in WIA 2.0 basiert auf Datenströmen. Die Streamabstraktion entfernt die Unterscheidung zwischen verschiedenen Übertragungstypen und ermöglicht auch den Austausch gegenseitig vereinbarter Metadaten zwischen Gerät und Anwendung.
-   Das WIA 2.0-Subsystem enthält auch ein einfaches Bildverarbeitungsfilter-Treiber-Add-On, das optional vom Scannertreiber ersetzt werden kann, wenn der Treiber einen benutzerdefinierten Bildverarbeitungsfilter bereitstellt. Der integrierte Filter ermöglicht die Nachverarbeitung von Bildern, die über den Scanner erfasst wurden. Der Filter für die Bildverarbeitung ermöglicht auch Live-Softwarevorschau, wenn kleine Einstellungen wie Helligkeit und Kontrast angepasst werden.
-   Der Segmentierungsfilter ist eine weitere praktische WIA-Komponente, die durch einen angepassteren Filter durch den Scannertreiber ersetzt werden kann. Der Segmentierungsfilter kann für die Überprüfung in mehreren Regionen verwendet werden. Beispielsweise ermöglicht die Überprüfung in mehreren Regionen einer Anwendung die automatische Erkennung verschiedener Scanregionen ohne Benutzereingriff, z. B. die Identifizierung einer Reihe von Fotos, die zufällig auf dem Flatbed des Scanners zu finden sind.
-   WIA 2.0 bietet einen ersetzbaren/erweiterbaren Fehlerhandler, um Software-, Hardware- und Konfigurationsfehler sowie Verzögerungen ordnungsgemäß zu behandeln und ggf. zu beheben. Der Fehlerhandler ist eine weitere WIA-Komponente, die vom Scannertreiber durch eine angepasstere Version ersetzt werden kann. Diese Erweiterung stellt Status- und Fehlermeldungen während der Datenerfassung bereit, z. B. "Lampe wird aufgewärmt", "Cover open", "Paper jam" usw. Diese Erweiterung ermöglicht auch eine übersichtlichere Unterstützung für "Cancel-Vorgänge".

## <a name="developer-audience"></a>Entwicklerzielgruppe

Die WIA-API ist für die Verwendung durch C/C++-Programmierer konzipiert. Kenntnisse über die Windows-GUI und die COM-Schnittstellen (Component Object Model) sind erforderlich.

Für Entwickler, die mit Microsoft Visual Basic 6.0, Active Server Pages (ASP) oder skripting vertraut sind, bietet WIA eine Automatisierungsebene für Windows XP Service Pack 1 (SP1) oder höher, die auf der Grundlage von C/C++ basiert und den Zugriff auf die von C/C++ bereitgestellte Grundlage vereinfacht. Informationen zur Automatisierungsebene finden Sie unter [Windows Image Acquisition Automation Layer](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).

> [!Note]  
> Die WIA Automation Layer ersetzt die Wia 1.0-Skripterstellung (Windows Image Acquisition).

 

## <a name="run-time-requirements"></a>Laufzeitanforderungen

Anwendungen, die die WIA-API verwenden, benötigen Windows XP oder höher.

## <a name="wia-topics"></a>WIA-Themen

Die WIA-Themen sind wie in der folgenden Tabelle dargestellt organisiert.



|  Thema                                                                                                                            | BESCHREIBUNG                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [Informationen zum Erwerb von Windows-Images](-wia-about-windows-image-acquisition.md)                                                  | Allgemeine Informationen zu WIA                                                                     |
| [Treiber für die Windows-Imageerfassung](/windows-hardware/drivers/image/windows-image-acquisition-drivers)                  | WIA-Treiberentwicklung                                                                            |
| [Automatisierungsebene für die Windows-Imageerfassung](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage) | WIA-Automatisierungsebene                                                                              |
| [WIA-Tutorial](-wia-wia-tutorial.md)                                                                                        | Exemplarische Vorgehensweise für Code im Software Development Kit (SDK), der sich auf bestimmte Aufgaben konzentriert |
| [Referenz](-wia-reference.md)                                                                                              | Informationen zu WIA-Schnittstellen, -Methoden, -Objekten und -Datentypen, die in C/C++ und Skripts verwendet werden.      |



 

 

 
