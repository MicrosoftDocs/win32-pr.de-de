---
description: Microsoft Hyper-V Server bietet eine skalierbare, zuverlässige und hoch verfügbare Verwaltungsumgebung für virtuelle Computer. Die Software für virtuelle Hyper-V-Computer konsolidiert Server sowie Entwicklungs- und Testumgebungen.
ms.assetid: 3359A33F-528B-4955-8B37-30523B8AD33A
title: Hyper-V-WMI-Anbieter (V2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b82156754f085196eaece86bb4996c1b4a0bb8348e1566894ee78d4921676f96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014248"
---
# <a name="hyper-v-wmi-provider-v2"></a>Hyper-V-WMI-Anbieter (V2)

## <a name="purpose"></a>Zweck

Hyper-V bietet eine skalierbare, zuverlässige und hoch verfügbare virtualisierte Servercomputingumgebung. Sie ermöglicht es einem oder mehreren Gastbetriebssystemen, gleichzeitig auf einem einzelnen physischen Computer ausgeführt zu werden. Zu den wichtigsten Verwendungsmöglichkeiten für die Technologie virtueller Computer gehören die folgenden:

-   Serverkonsolidierung
-   Konsolidierung von Entwicklungs- und Testumgebungen
-   Vereinfachte Notfallwiederherstellung

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                 | Beschreibung                                                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Informationen zum Hyper-V-WMI-Anbieter](about-the-virtualization-wmi-provider.md)<br/>                | Mit dem WMI-Anbieter für Hyper-V können Entwickler und Skripter schnell benutzerdefinierte Tools, Hilfsprogramme und Erweiterungen für die Virtualisierungsplattform erstellen. Die WMI-Schnittstellen können alle Aspekte der Hyper-V-Dienste verwalten.<br/> |
| [Verwenden des Hyper-V-WMI-Anbieters](using-the-virtualization-wmi-provider.md)<br/>                | In den folgenden Themen wird die Verwendung des Hyper-V-WMI-Anbieters beschrieben.<br/>                                                                                                                                                            |
| [Hyper-V-WMI-Klassen](hyper-v-wmi-classes.md)<br/>                                             | Im Folgenden sind die Hyper-V-WMI-Klassen.<br/>                                                                                                                                                                                    |
| [Hyper-V-Anwendungsüberwachungs-API](hyper-v-application-health-monitoring-api.md)<br/> | Die Hyper-V-Anwendungsüberwachungs-API wird verwendet, um den Integritätsstatus von Anwendungen zu überwachen, die auf einem virtuellen Computer ausgeführt werden.<br/>                                                                                               |
| [Hyper-V-Replikations-API](hyper-v-replication-api.md)<br/>                                     | Die Hyper-V-Replikations-API wird verwendet, um die Replikation virtueller Computer und die Failoverwiederherstellung zu steuern.<br/>                                                                                                                             |
| [Hyper-V-Metrik-API](hyper-v-metrics-api.md)<br/>                                             | Die Hyper-V-Metrik-API wird verwendet, um den Integritätsstatus von Anwendungen zu überwachen, die auf einem virtuellen Computer ausgeführt werden.<br/>                                                                                                                     |
| [Hyper-V-Netzwerk-API](hyper-v-networking-api.md)<br/>                                       | Die Hyper-V-Netzwerk-API wird verwendet, um Netzwerke in Hyper-V zu steuern.<br/>                                                                                                                                                          |
| [Hyper-V-Migrations-API](hyper-v-storage-migration-api.md)<br/>                                 | Die Hyper-V-Migrations-API wird verwendet, um die Speicher- und Livemigration in Hyper-V zu steuern.<br/>                                                                                                                                           |
| [Virtuelle Hyper-V-Fibre Channel-API](hyper-v-virtual-fiber-channels-api.md)<br/>                | Die virtuelle Hyper-V-Fibre Channel-API wird verwendet, um virtuelle Fibre Channel-Adapter in Hyper-V zu steuern.<br/>                                                                                                                           |
| [Hyper-V-VM-Platzierungs-API](hyper-v-vm-placement-api.md)<br/>                                   | Die Platzierungs-API für virtuelle Hyper-V-Computer (VM) enthält die Kompatibilitätsinformationen für die virtuellen Computer oder das Hostcomputersystem.<br/>                                                                                                        |
| [Schwellenwertklassen](threshold-classes.md)<br/>                                                 | Enthält die in Windows 10 eingeführten Klassen.<br/>                                                                                                                                                                                |
| [RS2-Klassen](redstone-classes.md)<br/>                                                        | Enthält die neuen Klassen für Windows 10, Version 1703.<br/>                                                                                                                                                                        |
| [RS3-Klassen](rs3-classes.md)<br/>                                                             | Enthält die neuen Klassen für Windows 10, Version 1709.<br/>                                                                                                                                                                        |
| [Hyper-V-Glossar](virtualization-glossary.md)<br/>                                            | Glossar der Begriffe, die in der Dokumentation Windows Virtualization SDK verwendet werden.<br/>                                                                                                                                                       |



 

## <a name="run-time-requirements"></a>Laufzeitanforderungen

Hyper-V-Dienste erfordern ein x64-basiertes System, das hardwareunterstützte Virtualisierung mit Hyper-V unterstützt. Programme, die mit den Hyper-V-WMI-Schnittstellen interagieren, können jedoch remote auf jedem System ausgeführt werden, das WMI unterstützt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Hyper-V (Windows Server 2008 R2 Technical Library)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc753637(v=ws.10))
</dt> <dt>

[Windows-Verwaltungsinstrumentation](/windows/desktop/WmiSdk/wmi-start-page)
</dt> <dt>

[Windows Servervirtualisierung](https://www.microsoft.com/windowsserver2008/virtualization/default.mspx)
</dt> </dl>

 

