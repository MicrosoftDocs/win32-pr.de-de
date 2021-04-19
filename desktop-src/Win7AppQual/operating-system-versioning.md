---
description: .
ms.assetid: 974650d9-504a-4f19-bc71-90fbc92672d9
title: Versionsverwaltung des Betriebssystems
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44e71cb671e19463ca6137c9b0ce7af04c2793e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357051"
---
# <a name="operating-system-versioning"></a>Versionsverwaltung des Betriebssystems

## <a name="affected-platforms"></a>Betroffene Plattformen

**Clients** -Windows 7  
**Server** -Windows Server 2008 R2  









## <a name="feature-impact"></a>Auswirkungen von Features

**Schweregrad** -hoch  
**Häufigkeit** -hoch  









## <a name="description"></a>BESCHREIBUNG

Die interne Versionsnummer für Windows 7 und Windows Server 2008 R2 ist 6,1. Diese Versionsnummer wird von der Funktion GetVersion nun bei der Abfrage an Anwendungen zurückgegeben. Dies ist insbesondere für Antivirus-, Sicherungs-, hilfsprogrammanwendungen und den Kopierschutz wichtig.

## <a name="manifestation-of-impact"></a>Erscheinung der Auswirkung

Die Manifestation dieser Änderung ist anwendungsspezifisch. Dies bedeutet, dass jede Anwendung, die speziell auf die Betriebssystemversion prüft, eine höhere Versionsnummer erhält, was zu einer oder mehreren der folgenden Situationen führen kann:

-   Anwendungs Installationsprogramme können die Anwendung möglicherweise nicht installieren, und Anwendungen können möglicherweise nicht gestartet werden.
-   Anwendungen werden möglicherweise instabil oder abstürzen
-   Anwendungen generieren möglicherweise Fehlermeldungen, funktionieren jedoch weiterhin ordnungsgemäß.

## <a name="mitigation"></a>Minderung

Die meisten Anwendungen funktionieren ordnungsgemäß unter Windows 7 und Windows Server 2008 R2, da die Anwendungs Kompatibilität in Windows 7 und Windows Server 2008 R2 sehr hoch ist. Windows 7 und Windows Server 2008 R2 enthalten jedoch eine Kompatibilitäts Ansicht für Installationsprogramme und Anwendungen, die auf die Betriebssystemversion überprüfen.

Um die Kompatibilitäts Ansicht zu aktivieren, können Benutzer mit der rechten Maustaste auf die Verknüpfung oder die ausführbare Datei klicken und dann die Kompatibilitäts Ansicht von Windows XP SP2 oder Windows Vista auf der Registerkarte Kompatibilität anwenden. In den meisten Fällen sollte dadurch die Anwendung ordnungsgemäß ausgeführt werden können, ohne dass Änderungen an der Anwendung erforderlich sind.

IT-Fachleute können auch beliebige der anwendbaren versionlie-Kompatibilitäts Korrekturen mithilfe des Compatibility Administrator-Tools anwenden, das mit dem Anwendungskompatibilitäts-Toolkit (Application Compatibility Toolkit, Act) installiert wird. Wenn beispielsweise eine Anwendung nicht funktionsfähig ist, weil Sie die Versionsinformationen für Windows XP® mit Service Pack 2 (SP2) überprüft, aber nicht findet, kann WinXPSP2VersionLie angewendet werden, um die richtigen Versionsnummern Informationen unabhängig von der tatsächlichen Betriebssystemversion, die auf dem Computer ausgeführt wird, an die Anwendung zurückzugeben. Die verfügbaren versionlie-Kompatibilitäts Korrekturen lauten:

-   Win95VersionLie
-   Win98VersionLie
-   WinNT4SP5VersionLie
-   Win2000VersionLie
-   Win2000SP1VersionLie
-   Win2000SP2VersionLie
-   Win2000SP3VersionLie
-   Winxpversionlie
-   WinXPSP1VersionLie
-   WinXPSP2VersionLie
-   Vistartmversionlie
-   VistaSP1VersionLie
-   VistaSP2VersionLie
-   Win2K3RTMVersionLie
-   Win2K3SP1VersionLie

## <a name="solution"></a>Lösung

Im Allgemeinen sollten Anwendungen keine Überprüfungen auf Betriebssystemversionen durchführen. Wenn eine Anwendung eine bestimmte Funktion benötigt, empfiehlt es sich, das Feature zu finden, und es wird nur dann ein Fehler erzeugt, wenn die erforderliche Funktion fehlt. Anwendungen sollten mindestens Versionsnummern akzeptieren, die größer oder gleich der niedrigsten unterstützten Version des Betriebssystems sind. Ausnahmen sollten nur auftreten, wenn eine bestimmte gesetzliche, geschäftliche oder Systemkomponenten Anforderung vorliegt.

## <a name="links-to-other-resources"></a>Links zu anderen Ressourcen

-   [Anwendungskompatibilitäts-Toolkit Download](/windows-hardware/get-started/adk-install)
-   [Bekannte Kompatibilitäts Korrekturen, Kompatibilitäts Modi und AppHelp-Meldungen](/previous-versions/windows/it-pro/windows-7/cc765984(v=ws.10))

 

 
