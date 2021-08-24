---
description: Integrationsdienste sind Softwaredienste, die auf dem Gastbetriebssystem innerhalb eines untergeordneten virtuellen Computers und als Teil des Virtualisierungsstapels im Verwaltungsbetriebssystem ausgeführt werden, um ein gewisses Maß an Integration in das Verwaltungsbetriebssystem zu ermöglichen.
ms.assetid: 7A8E9EF2-AC67-47CB-81A5-BF4C8A55D710
title: Integration Services-Klassen
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e4d833263298b88872cbf6eda71b953798897f3ff820d0ae831b818b9c92eaf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119694400"
---
# <a name="integration-services-classes"></a>Integration Services-Klassen

Integrationsdienste sind Softwaredienste, die auf dem Gastbetriebssystem innerhalb eines untergeordneten virtuellen Computers und als Teil des Virtualisierungsstapels im Verwaltungsbetriebssystem ausgeführt werden, um ein gewisses Maß an Integration in das Verwaltungsbetriebssystem zu ermöglichen. Sie werden verwendet, um Probleme zu beheben, die sich aus der hohen Isolationsstufe ergeben, die von virtuellen Computern bereitgestellt wird.

Im Folgenden finden Sie Virtualisierungs-WMI-Klassen, die sich auf die Integrationsdienste bezieht.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                                | Beschreibung                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Msvm \_ CopyFileToGuestJob**](msvm-copyfiletoguestjob.md)<br/>                                               | Stellt einen Vorgangsauftrag für den Gastdateidienst dar. <br/>                                                                                                                                                                                                            |
| [**Msvm \_ CopyFileToGuestSettingData**](msvm-copyfiletoguestsettingdata.md)<br/>                               | Stellt die Parameter zum Kopieren einer Datei vom Host in den Gast dar. <br/>                                                                                                                                                                                |
| [**Msvm \_ GuestFileService**](msvm-guestfileservice.md)<br/>                                                   | [**Msvm \_ GuestFileService enthält**](msvm-guestfileservice.md) eine Methode, mit der eine Datei vom Hyper-V-Host auf einen virtuellen Computer kopiert werden kann. <br/>                                                                                                     |
| [**Msvm \_ GuestService**](msvm-guestservice.md)<br/>                                                           | [**Msvm \_ GuestService**](msvm-guestservice.md) ist die abstrakte Basisklasse für Dienste im Gast, auf die vom Host aus zugegriffen werden kann. <br/>                                                                                                                  |
| [**Msvm \_ GuestServiceInterfaceComponent**](msvm-guestserviceinterfacecomponent.md)<br/>                       | Stellt den Zustand der Gastdienstschnittstellenkomponente dar, die einen Mechanismus für die Interaktion mit dem virtuellen Computer über die Verwaltungsschnittstellen auf dem Hostsystem bietet. <br/>                                                                         |
| [**Msvm \_ GuestServiceInterfaceComponentSettingData**](msvm-guestserviceinterfacecomponentsettingdata.md)<br/> | Stellt den konfigurierten Zustand der Gastdienstschnittstellenkomponente dar. <br/>                                                                                                                                                                                 |
| [**Msvm \_ KvpExchangeComponent**](msvm-kvpexchangecomponent.md)<br/>                                           | Stellt den Status des Schlüssel-Wert-Paaraustauschdiensts dar, der einen Mechanismus zum Austauschen von Daten zwischen dem virtuellen Computer und dem Betriebssystem bietet, das auf dem Verwaltungsbetriebssystem ausgeführt wird.<br/>                                                  |
| [**Msvm \_ KvpExchangeComponentSettingData**](msvm-kvpexchangecomponentsettingdata.md)<br/>                     | Stellt den konfigurierten Zustand des Schlüssel-Wert-Paaraustauschdiensts dar.<br/>                                                                                                                                                                                    |
| [**Msvm \_ KvpExchangeDataItem**](msvm-kvpexchangedataitem.md)<br/>                                             | Stellt ein Schlüssel-Wert-Paar dar.<br/>                                                                                                                                                                                                                               |
| [**Msvm \_ RegisteredGuestService**](msvm-registeredguestservice.md)<br/>                                       | Stellt eine Zuordnung zwischen einer Instanz von [**Msvm \_ GuestServiceInterfaceComponent**](msvm-guestserviceinterfacecomponent.md) und einer Instanz von [**Msvm \_ GuestService dar,**](msvm-guestservice.md)die einen im Gast ausgeführten Dienst darstellt. <br/> |
| [**Msvm \_ ShutdownComponent**](msvm-shutdowncomponent.md)<br/>                                                 | Stellt den Status des Diensts zum Herunterfahren dar, der einen Mechanismus zum Herunterfahren des Betriebssystems des virtuellen Computers über die Verwaltungsschnittstellen auf dem Hostsystem bietet.<br/>                                                                       |
| [**Msvm \_ ShutdownComponentSettingData**](msvm-shutdowncomponentsettingdata.md)<br/>                           | Stellt den konfigurierten Zustand des Diensts zum Herunterfahren dar.<br/>                                                                                                                                                                                                   |
| [**Msvm \_ TimeSyncComponent**](msvm-timesynccomponent.md)<br/>                                                 | Stellt den Status des Zeitsynchronisierungsdiensts dar, der für die Synchronisierung der Systemzeit eines virtuellen Computers mit der Systemzeit des Betriebssystems verantwortlich ist, das im Verwaltungsbetriebssystem ausgeführt wird.<br/>                             |
| [**Msvm \_ TimeSyncComponentSettingData**](msvm-timesynccomponentsettingdata.md)<br/>                           | Stellt den konfigurierten Zustand des Zeitsynchronisierungsdiensts dar.<br/>                                                                                                                                                                                       |
| [**Msvm \_ VssComponent**](msvm-vsscomponent.md)<br/>                                                           | Stellt den Zustand des diensts Volumeschattenkopie-Dienst (VSS) dar, der den VSS Requester im Gastbetriebssystem implementiert.<br/>                                                                                                                    |
| [**Msvm \_ VssComponentSettingData**](msvm-vsscomponentsettingdata.md)<br/>                                     | Stellt den konfigurierten Zustand des Volumeschattenkopie-Dienst (VSS) dar.<br/>                                                                                                                                                                           |



 

 

 




