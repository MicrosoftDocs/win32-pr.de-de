---
title: Schlanke Bereitstellung logischer Einheiten
description: Schlanke Bereitstellung logischer Einheiten
ms.assetid: D64ECA7B-62AC-4C14-BE4B-84DA2E20C16B
keywords:
- LUN
- Lba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64ed5385322601e633f79755fb192f1dce578f2bec0f944fa2f4f412c32d69a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119935050"
---
# <a name="thin-provisioning-of-logical-units"></a>Schlanke Bereitstellung logischer Einheiten

## <a name="platforms"></a>Plattformen

**Clients** – Windows 8  
**Server** – Windows Server 2012  


## <a name="description"></a>BESCHREIBUNG

Windows Thin Provisioning ist eine Schnittstelle zur End-to-End-Speicherbereitstellungslösung. Für die Bereitstellung eines hoch verfügbaren, skalierbaren und benutzerfreundlichen Speicherbereitstellungsdiensts sind stabile Implementierungen vom Serverhost zum Speicherzielgerät erforderlich. Die Windows Thin Provisioning-Funktion bietet dem Systemadministrator, IT-Manager und Speicheradministrator eine synchrone Ansicht der Speichergeräte für die schlanke Speicherbereitstellung über die Identifikation der logischen Einheit (LUNs), die Schwellenwertbenachrichtigung, die Verarbeitung der Ressourcenerschöpfung, die Speicherplatzwiederherstellung und den Abruf des Zustands der logischen Blockadressierung (Logical Block Addressing, LBA). Die Windows Schlanke Bereitstellungsfunktion stellt ein robustes Speicherbereitstellungsdienstmodell dar, das auf Client-Server-Speichersysteme, Virtualisierungsspeicher und Cloudspeicherdienste angewendet werden kann. Microsoft stellt die hohe Qualität des Thin Provisioning-Features sicher, indem die Windows Hardware Certification Kit-Anforderungen für Thin Provisioning für Speicherarrayprodukte erzwungen werden.

Die Windows Thin Provisioning-Speicherlösung:

-   Ermöglicht Speicheradministratoren das Erstellen einer größeren LUN mit weniger physischen Datenträgerressourcen.
-   Fügt eine physische Datenträgerressource hinzu oder entfernt sie, ohne den Speicherbereitstellungsdienst zu unterbrechen.
-   Warnung der Benutzer zur Speichervolumenutzung über die Schwellenwerteinstellung
-   Unterstützt die Speicherbereitstellung über die Konfiguration des freigegebenen Speicherpools.
-   Erhöht oder verringert die Größe des Speicherpools entsprechend dem Bedarf und der Nutzung des Speicherplatzes.

Zusammenfassung der Features der Windows Thin Provisioning:

-   LUN-Identifikation für die schlanke Bereitstellung
-   Handles für Schwellenwertbenachrichtigungen, temporäre Ressourcenerschöpfung und dauerhafte Ressourcenüberschöpfung
-   Storage Leerraumrückruf
-   Zuordnen von Zustandsabfragen logischer Blöcke

## <a name="manifestation"></a>Manifestation

Ohne das richtige Verständnis der Windows Handles für die LUN für die schlanke Bereitstellung kann die App mit unerwartetem Verhalten oder aus unbekannter Ursache fehlschlagen.

## <a name="using-thin-provisioning-luns"></a>Verwenden von LUNs für die schlanke Bereitstellung

Um lunsierte LUNs mit schlanker Speicherbereitstellung in Windows 8 oder Windows Server 2012 verwenden zu können, sollten System- und Speicheradministratoren folgende Aspekte beachten:

-   LUN-Identifikation mit schlanker Bereitstellung; Systemadministratoren oder Endbenutzer können defrag und das hilfsprogramm Storage Optimizer verwenden, um den Medientyp des Speichergeräts zu identifizieren.
-   Wenn ein Schwellenwert oder ein permanentes Ressourcenerschöpfungsereignis erreicht wird, protokolliert Windows ein Systemereignis, um den Systemadministrator zu benachrichtigen.
-   Storage Speicherplatzaufbewahrung kann manuell oder automatisch über eine Dateilöschbenachrichtigung oder den Planer des Speicheroptimierers ausgeführt werden.
-   Storage Administrator sollte die Schwellenwertbenachrichtigung implementieren, um den Systemadministrator oder Endbenutzer zu warnen und unerwartete Speicherdienstunterbrechungen zu vermeiden.

## <a name="tests"></a>Tests

-   Storage Array muss Windows 8 Thin Provisioning-Zertifikat empfangen, um Windows Thin Provisioning-Features zu unterstützen.
-   Windows Das Thin Provisioning Hardware Certification Kit für Speicherarray ist ein nützliches Testtool, um die Funktion des Speicherarrays für die Unterstützung Windows Thin Provisioning-Features zu überprüfen.
-   Windows erwartet, dass die LUN für die schlanke Bereitstellung und die LUN für die vollständige Bereitstellung ohne Probleme im selben System funktionieren.

## <a name="resources"></a>Ressourcen

-   [T10-SCSI-Blockbefehlsspezifikation (SBC3r27)](https://www.t10.org/cgi-bin/ac.pl?t=f&f=sbc3r27.pdf)
-   [Hardwaredashboarddienste](/windows-hardware/drivers/dashboard/)

 

 