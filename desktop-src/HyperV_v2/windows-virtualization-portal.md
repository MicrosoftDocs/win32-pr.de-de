---
description: Microsoft Hyper-V Server bietet eine skalierbare, zuverlässige und hoch verfügbare Verwaltungs Umgebung für virtuelle Computer. Software für virtuelle Hyper-V-Computer konsolidiert Server und Entwicklungs-und Testumgebungen.
ms.assetid: 3359A33F-528B-4955-8B37-30523B8AD33A
title: Hyper-V-WMI-Anbieter (v2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 555fd3cd1e8420c59bb5f1b8ef16480b3ddfcf4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368063"
---
# <a name="hyper-v-wmi-provider-v2"></a>Hyper-V-WMI-Anbieter (v2)

## <a name="purpose"></a>Zweck

Hyper-V bietet eine skalierbare, zuverlässige und hochverfügbare virtualisierte Server Computerumgebung. Ein oder mehrere Gast Betriebssysteme können gleichzeitig auf einem einzelnen physischen Computer ausgeführt werden. Zu den wichtigsten Verwendungsmöglichkeiten für die Technologie virtueller Computer zählen die folgenden:

-   Serverkonsolidierung
-   Konsolidierung der Entwicklungs-und Testumgebungen
-   Vereinfachte Notfall Wiederherstellung

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                 | BESCHREIBUNG                                                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Informationen zum Hyper-V-WMI-Anbieter](about-the-virtualization-wmi-provider.md)<br/>                | Der WMI-Anbieter für Hyper-V ermöglicht Entwicklern und skriskriptern, schnell benutzerdefinierte Tools, Hilfsprogramme und Erweiterungen für die Virtualisierungsplattform zu erstellen. Die WMI-Schnittstellen können alle Aspekte der Hyper-V-Dienste verwalten.<br/> |
| [Verwenden des Hyper-V-WMI-Anbieters](using-the-virtualization-wmi-provider.md)<br/>                | In den folgenden Themen wird beschrieben, wie der Hyper-V-WMI-Anbieter verwendet wird.<br/>                                                                                                                                                            |
| [Hyper-V-WMI-Klassen](hyper-v-wmi-classes.md)<br/>                                             | Im folgenden finden Sie die Hyper-V-WMI-Klassen.<br/>                                                                                                                                                                                    |
| [Hyper-V-anwendungsintegritätsüberwachungs-API](hyper-v-application-health-monitoring-api.md)<br/> | Die Hyper-V-Anwendungs Integritäts Überwachungs-API wird zum Überwachen des Integritäts Status von Anwendungen verwendet, die auf einem virtuellen Computer ausgeführt werden.<br/>                                                                                               |
| [HyperV-Replikations-API](hyper-v-replication-api.md)<br/>                                     | Die Hyper-V-Replikations-API wird zum Steuern der Replikation virtueller Computer und Failover verwendet.<br/>                                                                                                                             |
| [Hyper-V-Metrik-API](hyper-v-metrics-api.md)<br/>                                             | Die Hyper-V-Metrik-API wird zum Überwachen des Integritäts Status von Anwendungen verwendet, die auf einem virtuellen Computer ausgeführt werden.<br/>                                                                                                                     |
| [Hyper-V-Netzwerk-API](hyper-v-networking-api.md)<br/>                                       | Die Hyper-v-Netzwerk-API wird zum Steuern von Netzwerken in Hyper-v verwendet.<br/>                                                                                                                                                          |
| [Hyper-V-Migrations-API](hyper-v-storage-migration-api.md)<br/>                                 | Die Hyper-v-Migrations-API wird zum Steuern der Speicherung und Live Migration in Hyper-v verwendet.<br/>                                                                                                                                           |
| [Virtuelle Hyper-V-Fibre Channel-API](hyper-v-virtual-fiber-channels-api.md)<br/>                | Die virtuelle Hyper-v-Fibre Channel-API wird zum Steuern von virtuellen Fibre Channel Adaptern in Hyper-v verwendet.<br/>                                                                                                                           |
| [Hyper-V-VM-Platzierungs-API](hyper-v-vm-placement-api.md)<br/>                                   | Die Platzierungs-API des virtuellen Hyper-V-Computers (Virtual Machine, VM) enthält Kompatibilitätsinformationen für die VMs oder das hostingcomputersystem.<br/>                                                                                                        |
| [Schwellenwert Klassen](threshold-classes.md)<br/>                                                 | Enthält die Klassen, die in Windows 10 eingeführt wurden.<br/>                                                                                                                                                                                |
| [RS2-Klassen](redstone-classes.md)<br/>                                                        | Enthält die neuen Klassen für Windows 10, Version 1703.<br/>                                                                                                                                                                        |
| [RS3-Klassen](rs3-classes.md)<br/>                                                             | Enthält die neuen Klassen für Windows 10, Version 1709.<br/>                                                                                                                                                                        |
| [Hyper-V-Glossar](virtualization-glossary.md)<br/>                                            | Glossar der Begriffe, die in der Dokumentation zum Windows Virtualization SDK verwendet werden.<br/>                                                                                                                                                       |



 

## <a name="run-time-requirements"></a>Laufzeitanforderungen

Hyper-v-Dienste erfordern ein x64-basiertes System, das die Hardware gestützte Virtualisierung mit Hyper-v unterstützt. Programme, die mit den Hyper-V-WMI-Schnittstellen interagieren, können jedoch Remote auf jedem System ausgeführt werden, das WMI unterstützt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Hyper-V (Technische Bibliothek zu Windows Server 2008 R2)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc753637(v=ws.10))
</dt> <dt>

[Windows-Verwaltungsinstrumentation](/windows/desktop/WmiSdk/wmi-start-page)
</dt> <dt>

[Windows Server-Virtualisierung](https://www.microsoft.com/windowsserver2008/virtualization/default.mspx)
</dt> </dl>

 

