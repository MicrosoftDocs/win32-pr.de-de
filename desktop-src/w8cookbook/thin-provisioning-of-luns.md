---
title: Schlanke Speicherzuweisung logischer Einheiten
description: Schlanke Speicherzuweisung logischer Einheiten
ms.assetid: D64ECA7B-62AC-4C14-BE4B-84DA2E20C16B
keywords:
- LUN
- LBA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4abb6fa3cec112737b23e3cd658a48984cb0fcd1
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "104039745"
---
# <a name="thin-provisioning-of-logical-units"></a>Schlanke Speicherzuweisung logischer Einheiten

## <a name="platforms"></a>Plattformen

**Clients** – Windows 8  
**Server** – Windows Server 2012  


## <a name="description"></a>BESCHREIBUNG

Die schlanke Windows-Bereitstellung ist eine Schnittstelle zur Lösung für die End-to-End-Speicher Bereitstellung. Zum Bereitstellen eines hoch verfügbaren, skalierbaren und benutzerfreundlichen Speicher Bereitstellungs Diensts sind robuste Implementierungen vom Server Host zum Speicher Zielgerät erforderlich. Das Windows-Feature für die schlanke Speicherzuweisung bietet dem Systemadministrator, dem IT-Manager und dem Speicher Administrator eine synchrone Ansicht der Speichergeräte für die schlanke Speicherzuweisung für den Systemadministrator, den IT-Manager und den Speicher Administrator, indem es die (LUN)-Identifikation der logischen Einheit (LUN), Schwellenwert Benachrichtigung, Ressourcen Auslastungs Behandlung, Speicherplatz Rückgewinnung und Das Windows-Feature für die schlanke Speicherzuweisung stellt ein stabiles Speicher Bereitstellungs Dienstmodell dar, das auf Client-Server-Speichersysteme, virtualisierungsspeicher und cloudspeicherdienste angewendet werden kann. Microsoft gewährleistet die hohe Qualität des Features für die schlanke Speicherzuweisung durch erzwingen der Anforderungen an das Hardware-zertifizierungskit für Windows Thin Bereitstellung für Speicher Array Produkte.

Die Speicherlösung für die Bereitstellung von Windows schlank:

-   Ermöglicht Speicher Administratoren das Erstellen einer größeren LUN mit weniger physischen Datenträger Ressourcen.
-   Fügt physische Datenträger Ressource hinzu oder entfernt Sie, ohne den Speicher Bereitstellungs Dienst zu unterbrechen.
-   Benachrichtigt Benutzer über die Schwellenwert Einstellung auf die Auslastung des Speichervolumes.
-   Unterstützt die Speicher Bereitstellung über die freigegebene Speicherpool Konfiguration
-   Erhöht oder verringert die Größe des Speicherpools entsprechend der Nachfrage und Verwendung von Speicherplatz.

Zusammenfassung der Features der Windows-Thin Bereitstellung:

-   LUN-Identifikation der schlank Bereitstellung
-   Handles für Schwellenwert Benachrichtigung, temporäre Ressourcenauslastung und permanente Ressourcenauslastung
-   Speicherplatz Rückgewinnung
-   Zuordnung von Zustands Abfragen logischer Blöcke

## <a name="manifestation"></a>Ausstrahlung

Ohne das richtige Verständnis der Windows-Handles für die LUN mit schlanker Speicherzuweisung kann die APP mit unerwartetem Verhalten oder aus unbekannter Ursache fehlschlagen.

## <a name="using-thin-provisioning-luns"></a>Verwenden von LUNs mit schlanker Speicherzuweisung

Zur Verwendung von schlank bereitgestellten LUNs in Windows 8 oder Windows Server 2012 sollten System-und Speicher Administratoren Folgendes beachten:

-   LUN-Identifikation der Thin Bereitstellung; Systemadministratoren oder Endbenutzer können Defrag und das Dienstprogramm für den Speicher Optimierer verwenden, um den Medientyp des Speichergeräts zu identifizieren.
-   Wenn ein Schwellenwert oder ein dauerhaftes Ressourcen Auslastungs Ereignis erreicht wird, protokolliert Windows ein System Ereignis, um den Systemadministrator zu benachrichtigen.
-   Die Speicherplatz Rückgewinnung kann manuell oder automatisch durch Datei Lösch Benachrichtigung oder den Scheduler des Speicher Optimierers ausgeführt werden.
-   Der Speicher Administrator sollte die Schwellenwert Benachrichtigung für Warnungs Systemadministrator oder Endbenutzer implementieren und unerwartete Speicherdienst Unterbrechungen vermeiden.

## <a name="tests"></a>Tests

-   Das Speicher Array muss ein Zertifikat für die schlanke Windows 8-Bereitstellung erhalten, um die Windows Thin Provisioning-Funktionen
-   Das Hardware-zertifizierungskit für die Windows-schlanke Speicherzuweisung für das Speicher Array ist ein nützliches Testtool zum Überprüfen der Funktion von Speicherarrays für die Unterstützung von Windows schlank
-   Windows erwartet, dass die LUN mit schlanker Speicherzuweisung und die LUN für die vollständige Bereitstellung ohne Probleme in demselben System funktionieren.

## <a name="resources"></a>Ressourcen

-   [T10-SCSI-Block-Befehls Spezifikation (SBC3r27)](https://www.t10.org/cgi-bin/ac.pl?t=f&f=sbc3r27.pdf)
-   [Hardware-Dashboard-Dienste](/windows-hardware/drivers/dashboard/)

 

 