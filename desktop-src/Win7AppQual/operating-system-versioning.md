---
description: Betriebssystemversionsierung
ms.assetid: 974650d9-504a-4f19-bc71-90fbc92672d9
title: Betriebssystemversionsierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 707594f7e17b1518f56c0dc889911740f1bbddf50038c1908b7a47d7a0629b43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994870"
---
# <a name="operating-system-versioning"></a>Betriebssystemversionsierung

## <a name="affected-platforms"></a>Betroffene Plattformen

**Clients** – Windows 7  
**Server** – Windows Server 2008 R2  









## <a name="feature-impact"></a>Auswirkungen auf Features

**Schweregrad –** Hoch  
**Frequency** – High  









## <a name="description"></a>Beschreibung

Die interne Versionsnummer für Windows 7 und Windows Server 2008 R2 ist 6.1. Die GetVersion-Funktion gibt diese Versionsnummer jetzt an Anwendungen zurück, wenn sie abgefragt wird. Dies ist besonders wichtig für AntiViren, Sicherung, Hilfsprogrammanwendungen und Kopierschutz.

## <a name="manifestation-of-impact"></a>Auswirkungen

Diese Änderung ist anwendungsspezifisch. Dies bedeutet, dass jede Anwendung, die speziell nach der Betriebssystemversion sucht, eine höhere Versionsnummer erhält, was zu einer oder mehreren der folgenden Situationen führen kann:

-   Anwendungsinstallationsprogramme können die Anwendung möglicherweise nicht installieren, und Anwendungen können möglicherweise nicht gestartet werden.
-   Anwendungen können instabil werden oder abstürzen
-   Anwendungen generieren möglicherweise Fehlermeldungen, funktionieren aber weiterhin ordnungsgemäß.

## <a name="mitigation"></a>Minderung

Die meisten Anwendungen funktionieren auf Windows 7 und Windows Server 2008 R2 ordnungsgemäß, da die Anwendungskompatibilität in Windows 7 und Windows Server 2008 R2 sehr hoch ist. Allerdings enthalten Windows 7 und Windows Server 2008 R2 eine Kompatibilitätsansicht für Installationsprogramme und Anwendungen, die auf Betriebssystemversion prüfen.

Um die Kompatibilitätsansicht zu aktivieren, können Benutzer mit der rechten Maustaste auf die Verknüpfung oder die ausführbare Datei klicken und dann die Windows XP SP2- oder Windows Vista-Kompatibilitätsansicht auf der Registerkarte Kompatibilität anwenden. In den meisten Fällen sollte dies der Anwendung ermöglichen, ordnungsgemäß zu arbeiten, ohne dass Änderungen an der Anwendung erforderlich sind.

IT-Experten können auch alle anwendbaren Versionskompatibilitätskorrekturen anwenden, indem sie das Kompatibilitätsadministratortool verwenden, das mit dem Application Compatibility Toolkit (ACT) installiert wird. Wenn eine Anwendung beispielsweise nicht funktioniert, weil sie nach dem Windows XP® mit Sp2-Versionsinformationen (Service Pack 2) sucht, aber nicht gefunden wird, kann WinXPSP2VersionLie angewendet werden, um die richtigen Versionsnummerninformationen an die Anwendung zurückzugeben, unabhängig von der tatsächlichen Betriebssystemversion, die auf dem Computer ausgeführt wird. Die verfügbaren Versionslie-Kompatibilitätskorrekturen sind:

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

Im Allgemeinen sollten Anwendungen keine Überprüfungen der Betriebssystemversion durchführen. Wenn eine Anwendung ein bestimmtes Feature benötigt, ist es besser zu versuchen, das Feature zu finden, und schlägt nur fehl, wenn das erforderliche Feature fehlt. Anwendungen sollten immer Versionsnummern akzeptieren, die größer oder gleich der niedrigsten unterstützten Version des Betriebssystems sind. Ausnahmen sollten nur auftreten, wenn eine bestimmte rechtliche, geschäftliche oder Systemkomponentenanforderung vorliegt.

## <a name="links-to-other-resources"></a>Links zu anderen Ressourcen

-   [Herunterladen des Anwendungskompatibilitätstoolkits](/windows-hardware/get-started/adk-install)
-   [Bekannte Kompatibilitätskorrekturen, Kompatibilitätsmodi und AppHelp-Meldungen](/previous-versions/windows/it-pro/windows-7/cc765984(v=ws.10))

 

 
