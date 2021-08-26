---
description: Enthält die neuen Klassen für Windows 10 Version 1703.
ms.assetid: 33F993F0-2B20-49F7-9DAC-1D682633420C
title: Redstone-Klassen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d6a61f2b79cc9739cff7a3643096592186e42a257fbb101549cd6719b75fc7b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119980190"
---
# <a name="redstone-classes"></a>Redstone-Klassen

Enthält die neuen Klassen für Windows 10 Version 1703.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                                | Beschreibung                                                                                                                                                                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Msvm \_ AssignableDeviceDismountSettingData**](msvm-assignabledevicedismountsettingdata.md)<br/>             | Stellt die Einstellungen eines zu importierenden virtuellen Systems dar. Wird von der [**Dismount-Methode**](msvm-assignabledeviceservice-dismountassignabledevice.md) der [**Msvm \_ AssignableDeviceService-Klasse**](msvm-assignabledeviceservice.md) verwendet.<br/>                                                        |
| [**Msvm \_ AssignableDeviceService**](msvm-assignabledeviceservice.md)<br/>                                     | Verwaltet die zu weisenden Geräte auf einem Hostcomputersystem.<br/>                                                                                                                                                                                                                                      |
| [**Msvm \_ CollectionReferencePointExportJob**](msvm-collectionreferencepointexportjob.md)<br/>                 | Diese Klasse stellt einen Exportvorgangauftrag für einen Auflistungsverweispunkt dar.<br/>                                                                                                                                                                                                                       |
| [**Msvm \_ EthernetSwitchHardwareOffloadSettingData**](msvm-ethernetswitchhardwareoffloadsettingdata.md)<br/>   | Stellt die Einstellungen für die Switch-Ausladung dar.<br/>                                                                                                                                                                                                                                                        |
| [**Msvm \_ EthernetSwitchPortMigrationQosSettingData**](msvm-ethernetswitchportmigrationqossettingdata.md)<br/> | Stellt die VFP-QOS-Einstellungen dar.<br/>                                                                                                                                                                                                                                                               |
| [**Msvm \_ EthernetSwitchPortRdmaSettingData**](msvm-ethernetswitchportrdmasettingdata.md)<br/>                 | Stellt die RdMA-Featureeinstellungsdaten des Ports dar.<br/>                                                                                                                                                                                                                                                 |
| [**Msvm \_ EthernetSwitchPortTeamMappingSettingData**](msvm-ethernetswitchportteammappingsettingdata.md)<br/>   | Stellt die Einstellungsdaten der Portteamzuordnungsfunktion dar.<br/>                                                                                                                                                                                                                                         |
| [**Msvm \_ GpuPartition**](msvm-gpupartition.md)<br/>                                                           | Stellt den Zustand der GPU-Partition dar.<br/>                                                                                                                                                                                                                                                     |
| [**Msvm \_ GpuPartitionSettingData**](msvm-gpupartitionsettingdata.md)<br/>                                     | Stellt den konfigurierten Zustand eines GPU-Partitionsgeräts dar.<br/>                                                                                                                                                                                                                                     |
| [**Msvm \_ NetworkConnectionDiagnosticInformation**](msvm-networkconnectiondiagnosticinformation.md)<br/>       | Stellt Informationen zur Netzwerkkonnektivität für einen virtuellen Computer zur Verfügung.<br/>                                                                                                                                                                                                                     |
| [**Msvm \_ NetworkConnectionDiagnosticSettingData**](msvm-networkconnectiondiagnosticsettingdata.md)<br/>       | Stellt die Einstellungen dar, die zum Testen der Netzwerkkonnektivität eines virtuellen Computers verwendet werden. <br/>                                                                                                                                                                                                           |
| [**Msvm \_ PartitionableGpu**](msvm-partitionablegpu.md)<br/>                                                   | Stellt eine partitionierbare GPU dar. Jede GPU kann in eine Reihe von GPU-Partitionen aufgeteilt werden, die einem virtuellen Computer als vGPU zugewiesen werden können.<br/>                                                                                                                                                  |
| [**Msvm \_ PciExpress**](msvm-pciexpress.md)<br/>                                                               | Stellt den Zustand des PCI Express-Ports dar.<br/>                                                                                                                                                                                                                                                  |
| [**Msvm \_ PciExpressSettingData**](msvm-pciexpresssettingdata.md)<br/>                                         | Stellt den konfigurierten Zustand eines PCI Express-Ports dar.<br/>                                                                                                                                                                                                                                         |
| [**Msvm \_ SecurityElement**](msvm-securityelement.md)<br/>                                                     | Stellt die Laufzeitsicherheitseinstellungen eines [**\_ CIM-Computersystems dar.**](cim-computersystem.md)<br/>                                                                                                                                                                                               |
| [**Msvm \_ SecurityService**](msvm-securityservice.md)<br/>                                                     | Stellt den Sicherheitsdienst dar. Es wird zum Konfigurieren der Sicherheitseinstellungen des virtuellen Systems verwendet.<br/>                                                                                                                                                                                                  |
| [**Msvm \_ SecuritySettingData**](msvm-securitysettingdata.md)<br/>                                             | Stellt den konfigurierten Status der Sicherheitseinstellungen für dar. <br/>                                                                                                                                                                                                                                  |
| [**Msvm \_ StorageSettingData**](msvm-storagesettingdata.md)<br/>                                               | Stellt die speicherspezifischen Einstellungen für ein virtuelles System dar.<br/>                                                                                                                                                                                                                                 |
| [**Msvm \_ SummaryInformationBase**](msvm-summaryinformationbase.md)<br/>                                       | Wird in der [**GetSummaryInformation-Methode**](getsummaryinformation-msvm-virtualsystemmanagementservice.md) in der [**Msvm \_ VirtualSystemManagementService-Klasse**](msvm-virtualsystemmanagementservice.md) verwendet, um schnell allgemeine Informationen zu einem virtuellen System oder einer Momentaufnahme abzurufen.<br/> |
| [**Msvm \_ SystemComponentSettingData**](msvm-systemcomponentsettingdata.md)<br/>                               | Eine generische Basisklasse zum Festlegen von Datenklassen, die Komponenten eines virtuellen Systems darstellen.<br/>                                                                                                                                                                                                     |
| [**Msvm \_ VirtualSystemReferencePointExportJob**](msvm-virtualsystemreferencepointexportjob.md)<br/>           | Diese Klasse stellt einen Exportvorgangauftrag für den Virtuellen Systemverweispunkt dar.<br/>                                                                                                                                                                                                                   |



 

 

 




