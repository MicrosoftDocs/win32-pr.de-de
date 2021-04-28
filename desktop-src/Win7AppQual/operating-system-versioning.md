---
description: Betriebssystemversionsierung
ms.assetid: 974650d9-504a-4f19-bc71-90fbc92672d9
title: Betriebssystemversionsierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43b2b8c60994eaee7a3becfa9acc03fe2c61fb12
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088038"
---
# <a name="operating-system-versioning"></a>Betriebssystemversionsierung

## <a name="affected-platforms"></a>Betroffene Plattformen

**Clients** – Windows 7  
**Server** – Windows Server 2008 R2  









## <a name="feature-impact"></a>Auswirkung von Features

**Schweregrad:** Hoch  
**Häufigkeit** – Hoch  









## <a name="description"></a>BESCHREIBUNG

Die interne Versionsnummer für Windows 7 und Windows Server 2008 R2 ist 6.1. Die GetVersion-Funktion gibt diese Versionsnummer jetzt an Anwendungen zurück, wenn sie abgefragt wird. Dies ist besonders wichtig für Anti Antivirus, Sicherung, Hilfsprogrammanwendungen und Kopierschutz.

## <a name="manifestation-of-impact"></a>Auswirkungen

Der Grund für diese Änderung ist anwendungsspezifisch. Dies bedeutet, dass jede Anwendung, die speziell nach der Betriebssystemversion sucht, eine höhere Versionsnummer erhalten, was zu einer oder mehreren der folgenden Situationen führen kann:

-   Anwendungsinstallationsprogramme können die Anwendung möglicherweise nicht installieren, und Anwendungen können möglicherweise nicht gestartet werden.
-   Anwendungen können instabil werden oder abstürzen
-   Anwendungen generieren möglicherweise Fehlermeldungen, funktionieren aber weiterhin ordnungsgemäß.

## <a name="mitigation"></a>Minderung

Die meisten Anwendungen funktionieren unter Windows 7 und Windows Server 2008 R2 ordnungsgemäß, da die Anwendungskompatibilität in Windows 7 und Windows Server 2008 R2 sehr hoch ist. Windows 7 und Windows Server 2008 R2 enthalten jedoch eine Kompatibilitätsansicht für Installationsprogramme und Anwendungen, die nach Betriebssystemversionen überprüfen.

Um die Kompatibilitätsansicht zu aktivieren, können Benutzer mit der rechten Maustaste auf die Verknüpfung oder die ausführbare Datei klicken und dann die Windows XP SP2- oder Windows Vista-Kompatibilitätsansicht auf der Registerkarte Kompatibilität anwenden. In den meisten Fällen sollte dies der Anwendung ermöglichen, ordnungsgemäß zu arbeiten, ohne dass Änderungen an der Anwendung erforderlich sind.

IT-Experten können auch alle anwendbaren Versionskompatibilitätskorrekturen anwenden, indem sie das Kompatibilitätsadministratortool verwenden, das mit dem Application Compatibility Toolkit (ACT) installiert wird. Wenn eine Anwendung z. B. nicht funktioniert, weil sie die Windows XP® mit Sp2-Versionsinformationen (Service Pack 2) überprüft, aber nicht gefunden hat, kann winXPSP2VersionLie angewendet werden, um die richtigen Versionsnummerninformationen an die Anwendung zurückzugeben, unabhängig von der tatsächlichen Betriebssystemversion, die auf dem Computer ausgeführt wird. Die verfügbaren Versionslie-Kompatibilitätskorrekturen sind:

-   Win95VersionLie
-   Win98VersionLie
-   WinNT4SP5VersionLie
-   Win2000VersionLie
-   Win2000SP1VersionLie
-   Win2000SP2VersionLie
-   Win2000SP3VersionLie
-   WinXPVersionLie
-   WinXPSP1VersionLie
-   WinXPSP2VersionLie
-   VistaRTMVersionLie
-   VistaSP1VersionLie
-   VistaSP2VersionLie
-   Win2K3RTMVersionLie
-   Win2K3SP1VersionLie

## <a name="solution"></a>Lösung

Im Allgemeinen sollten Anwendungen keine Überprüfungen der Betriebssystemversion durchführen. Wenn eine Anwendung ein bestimmtes Feature benötigt, ist es besser zu versuchen, das Feature zu finden, und schlägt nur fehl, wenn das erforderliche Feature fehlt. Anwendungen sollten immer Versionsnummern akzeptieren, die größer oder gleich der niedrigsten unterstützten Version des Betriebssystems sind. Ausnahmen sollten nur auftreten, wenn eine bestimmte rechtliche, geschäftliche oder Systemkomponentenanforderung besteht.

## <a name="links-to-other-resources"></a>Links zu anderen Ressourcen

-   [Download des Anwendungskompatibilitätstoolkits](/windows-hardware/get-started/adk-install)
-   [Bekannte Kompatibilitätskorrekturen, Kompatibilitätsmodi und AppHelp-Meldungen](/previous-versions/windows/it-pro/windows-7/cc765984(v=ws.10))

 

 
