---
description: .
ms.assetid: 5d0188a5-ef5f-409e-9d2d-7639d99edc1d
title: nur 64-Bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d3178a15ec0a138a73789233dd2d787964a96b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218496"
---
# <a name="64-bit-only"></a>nur 64-Bit

## <a name="affected-platforms"></a>Betroffene Plattformen

**Server** -Windows Server 2008 R2  



## <a name="feature-impact"></a>Auswirkungen von Features

 **Schweregrad** -niedrig  
**Häufigkeit** -hoch  






## <a name="description"></a>BESCHREIBUNG

Windows Server 2008 R2 ist nur mit einer 64-Bit-SKU ausgeliefert. für die Server Version des Betriebssystems ist keine 32-Bit-SKU verfügbar. Für den Windows 7-Client ist jedoch weiterhin eine 32-Bit-SKU verfügbar.

## <a name="manifestation-of-impact"></a>Erscheinung der Auswirkung

Dies wirkt sich auf drei Bereiche aus:

-   32-Bit-Treiber
-   32-Bit-Plug-ins
-   ausführbare 16-Bit-Dateien

## <a name="solution-for-32-bit-drivers"></a>Lösung für 32-Bit-Treiber

Kompilieren Sie 32-Bit-Treiber als signierte 64-Bit-Treiber neu.

## <a name="solution-for-32-bit-plug-ins"></a>Lösung für 32-Bit-Plug-ins

WOW64, ein x86-Emulator, ermöglicht das nahtlose Ausführen von Windows-basierten 32-Bit-Anwendungen auf 64-Bit-Fenstern. WOW64 ist jetzt ein optionales Feature, das Sie installieren müssen, wenn es erforderlich ist, 32-Bit-Code auszuführen.

Das System isoliert 32-Bit-Anwendungen von 64-Bit-Anwendungen, einschließlich der Vermeidung von Datei-und Registrierungs Kollisionen. Konsolen-, GUI-und Dienst Anwendungen werden unterstützt. Das System stellt Interoperabilität zwischen der 32/64-Grenze für Szenarien wie Ausschneiden, einfügen und com bereit. Allerdings können 32-Bit-Prozesse keine 64-Bit-DLLs laden, und 64-Bit-Prozesse können keine 32-Bit-DLLs laden. Wir sehen dies häufig in Shell-Plug-ins, die für Windows Explorer geschrieben wurden.

Eine 32-Bit-Anwendung kann erkennen, ob Sie unter WOW64 durch Aufrufen der IsWow64Process-Funktion ausgeführt wird. Die Anwendung kann zusätzliche Informationen über den Prozessor mithilfe der GetNativeSystemInfo-Funktion abrufen.

Beachten Sie, dass 64-Bit-Windows die Ausführung von 16-Bit-Windows-basierten Anwendungen nicht unterstützt. Der Hauptgrund ist, dass Handles 32 signifikante Bits auf 64-Bit-Fenstern aufweisen. Daher können Handles nicht abgeschnitten und ohne Datenverlust an 16-Bit-Anwendungen übermittelt werden. Der Versuch, 16-Bit-Anwendungen zu starten, schlägt mit folgendem Fehler fehl: fehlerhafte \_ \_ exe- \_ Format.

## <a name="solution-for-16-bit-executables"></a>Lösung für ausführbare 16-Bit-Dateien

64-Bit-Windows erkennt eine begrenzte Anzahl spezifischer Programme mit 16-Bit-Installer und ersetzt eine portierte 32-Bit-Version. Die Liste der Substitutionen wird in der Registrierung unter folgendem Schlüssel gespeichert: HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ NtVdm64 es gibt integrierte Unterstützung für mehrere Installer-Engines, einschließlich InstallShield 5. x-Installer. Beachten Sie, dass der 64-Bit-Windows Installer die auf 32-Bit-MSI basierende Anwendungen nahtlos auf 64-Bit-Windows installieren kann.

## <a name="links-to-other-resources"></a>Links zu anderen Ressourcen

-   [Ausführen von 32-Bit-Anwendungen](/windows/desktop/WinProg64/running-32-bit-applications)
-   [Leistung und Arbeitsspeicher Verbrauch](/windows/desktop/WinProg64/performance-and-memory-consumption)
-   [WOW64-Implementierungs Details](/windows/desktop/WinProg64/wow64-implementation-details)
-   [Registrierungs Redirector](/windows/desktop/WinProg64/registry-redirector)
-   [Datei System-Redirector](/windows/desktop/WinProg64/file-system-redirector)
-   [Speicherverwaltung](/windows/desktop/WinProg64/memory-management)
-   [Prozessoraffinität](/windows/desktop/WinProg64/processor-affinity)
-   [Prozessübergreifende Kommunikation](/windows/desktop/WinProg64/interprocess-communication)
-   [Anwendungs Installation auf 64-Bit-Systemen](/windows/desktop/WinProg64/application-installation)
-   [Debuggen WOW64](/windows/desktop/WinProg64/debugging-wow64)
-   [**IsWow64Process-Funktion**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process)
-   [**GetNativeSystemInfo-Funktion**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getnativesysteminfo)

 

 
