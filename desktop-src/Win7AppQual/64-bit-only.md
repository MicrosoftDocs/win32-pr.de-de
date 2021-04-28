---
description: Nur 64-Bit
ms.assetid: 5d0188a5-ef5f-409e-9d2d-7639d99edc1d
title: Nur 64-Bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2d896fcaf4b8c4ebeadf7cfd5a5c22e511cb659
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088808"
---
# <a name="64-bit-only"></a>Nur 64-Bit

## <a name="affected-platforms"></a>Betroffene Plattformen

**Server** – Windows Server 2008 R2  



## <a name="feature-impact"></a>Auswirkung von Features

 **Schweregrad:** Niedrig  
**Häufigkeit** – Hoch  






## <a name="description"></a>BESCHREIBUNG

Windows Server 2008 R2 wird nur mit einer 64-Bit-SKU versendet. Für die Serverversion des Betriebssystems ist keine 32-Bit-SKU verfügbar. Eine 32-Bit-SKU ist jedoch weiterhin für den Windows 7-Client verfügbar.

## <a name="manifestation-of-impact"></a>Auswirkungen

Dies wirkt sich auf drei Bereiche aus:

-   32-Bit-Treiber
-   32-Bit-Plug-Ins
-   Ausführbare 16-Bit-Dateien

## <a name="solution-for-32-bit-drivers"></a>Lösung für 32-Bit-Treiber

Kompilieren Sie 32-Bit-Treiber als signierte 64-Bit-Treiber neu.

## <a name="solution-for-32-bit-plug-ins"></a>Lösung für 32-Bit-Plug-Ins

WoW64, ein x86-Emulator, ermöglicht die nahtlose Ausführung von Windows-basierten 32-Bit-Anwendungen unter 64-Bit-Windows. WoW64 ist jetzt ein optionales Feature, das Sie installieren müssen, wenn 32-Bit-Code ausgeführt werden muss.

Das System isoliert 32-Bit-Anwendungen von 64-Bit-Anwendungen, einschließlich der Verhinderung von Datei- und Registrierungskonflikten. Konsolen-, GUI- und Dienstanwendungen werden unterstützt. Das System bietet Interoperabilität über die 32/64-Grenze hinweg für Szenarien wie Ausschneiden und Einfügen und COM. 32-Bit-Prozesse können jedoch keine 64-Bit-DLLs laden, und 64-Bit-Prozesse können keine 32-Bit-DLLs laden. Dies wird häufig in Shell-Plug-Ins angezeigt, die für Windows-Explorer geschrieben wurden.

Eine 32-Bit-Anwendung kann erkennen, ob sie unter WOW64 ausgeführt wird, indem sie die IsWow64Process-Funktion aufruft. Die Anwendung kann mithilfe der GetNativeSystemInfo-Funktion zusätzliche Informationen zum Prozessor abrufen.

Beachten Sie, dass 64-Bit-Windows die Ausführung von 16-Bit-Windows-basierten Anwendungen nicht unterstützt. Der Hauptgrund dafür ist, dass Handles 32 signifikante Bits unter 64-Bit-Windows aufweisen. Daher können Handles nicht abgeschnitten und ohne Datenverlust an 16-Bit-Anwendungen übergeben werden. Beim Starten von 16-Bit-Anwendungen tritt folgender Fehler auf: ERROR \_ BAD \_ EXE \_ FORMAT.

## <a name="solution-for-16-bit-executables"></a>Lösung für ausführbare 16-Bit-Dateien

64-Bit-Windows erkennt eine begrenzte Anzahl bestimmter 16-Bit-Installationsprogrammprogramme und ersetzt eine portierte 32-Bit-Version. Die Liste der Ersetzungen wird in der Registrierung unter dem folgenden Schlüssel gespeichert: HKEY \_ LOCAL MACHINE Software Microsoft Windows NT \_ \\ \\ \\ \\ CurrentVersion \\ NtVdm64 Es gibt integrierte Unterstützung für mehrere Installer-Engines, einschließlich InstallShield 5.x-Installationsprogramme. Beachten Sie, dass der 64-Bit-Windows Installer nahtlos 32-Bit-MSI-basierte Anwendungen unter 64-Bit-Windows installieren kann.

## <a name="links-to-other-resources"></a>Links zu anderen Ressourcen

-   [Ausführen von 32-Bit-Anwendungen](/windows/desktop/WinProg64/running-32-bit-applications)
-   [Leistung und Arbeitsspeicherverbrauch](/windows/desktop/WinProg64/performance-and-memory-consumption)
-   [WOW64-Implementierungsdetails](/windows/desktop/WinProg64/wow64-implementation-details)
-   [Registrierungsumleitung](/windows/desktop/WinProg64/registry-redirector)
-   [Dateisystem-Redirector](/windows/desktop/WinProg64/file-system-redirector)
-   [Speicherverwaltung](/windows/desktop/WinProg64/memory-management)
-   [Prozessoraffinität](/windows/desktop/WinProg64/processor-affinity)
-   [Prozessübergreifende Kommunikation](/windows/desktop/WinProg64/interprocess-communication)
-   [Anwendungsinstallation auf 64-Bit-Systemen](/windows/desktop/WinProg64/application-installation)
-   [Debuggen von WOW64](/windows/desktop/WinProg64/debugging-wow64)
-   [**IsWow64Process-Funktion**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process)
-   [**GetNativeSystemInfo-Funktion**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getnativesysteminfo)

 

 
