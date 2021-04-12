---
description: Integration Services sind Software Dienste, die auf dem Gast Betriebssystem innerhalb eines untergeordneten virtuellen Computers ausgeführt werden, und als Teil des Virtualisierungsstapels im Verwaltungs Betriebssystem, um ein gewisses Maß an Integration mit dem Verwaltungs Betriebssystem zu ermöglichen.
ms.assetid: 7A8E9EF2-AC67-47CB-81A5-BF4C8A55D710
title: Integration Services-Klassen
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04d60a913159c49387848b5e18a3e37b942f3e7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528202"
---
# <a name="integration-services-classes"></a>Integration Services-Klassen

Integration Services sind Software Dienste, die auf dem Gast Betriebssystem innerhalb eines untergeordneten virtuellen Computers ausgeführt werden, und als Teil des Virtualisierungsstapels im Verwaltungs Betriebssystem, um ein gewisses Maß an Integration mit dem Verwaltungs Betriebssystem zu ermöglichen. Sie werden verwendet, um Probleme zu beheben, die sich aus dem hohen Maß an Isolation ergeben, die von virtuellen Maschinen bereitgestellt wird.

Im folgenden finden Sie WMI-virtualisierungsklassen, die sich auf die Integration Services beziehen.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                                | BESCHREIBUNG                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MSVM \_ copyfilein guestjob**](msvm-copyfiletoguestjob.md)<br/>                                               | Stellt einen Gast Datei Dienst-Vorgangs Auftrag dar. <br/>                                                                                                                                                                                                            |
| [**MSVM \_ copyfilein guestsettingdata**](msvm-copyfiletoguestsettingdata.md)<br/>                               | Stellt die Parameter zum Kopieren einer Datei vom Host in den Gast dar. <br/>                                                                                                                                                                                |
| [**MSVM \_ guestfileservice**](msvm-guestfileservice.md)<br/>                                                   | [**MSVM \_ Guestfileservice**](msvm-guestfileservice.md) enthält eine Methode, die verwendet werden kann, um eine Datei auf einen virtuellen Computer vom Hyper-V-Host zu kopieren. <br/>                                                                                                     |
| [**MSVM- \_ guestservice**](msvm-guestservice.md)<br/>                                                           | [**MSVM \_ Guestservice**](msvm-guestservice.md) ist die abstrakte Basisklasse für Dienste im Gast, auf die vom Host zugegriffen werden kann. <br/>                                                                                                                  |
| [**MSVM \_ guestserviczuterfacecomponent**](msvm-guestserviceinterfacecomponent.md)<br/>                       | Stellt den Status der Komponente der Gast Dienst Schnittstelle dar, die einen Mechanismus zum interagieren mit der virtuellen Maschine über die Verwaltungs Schnittstellen auf dem Host System bereitstellt. <br/>                                                                         |
| [**MSVM \_ guestserviceinterfacemeentsettingdata**](msvm-guestserviceinterfacecomponentsettingdata.md)<br/> | Stellt den konfigurierten Status der Komponente der Gast Dienst Schnittstelle dar. <br/>                                                                                                                                                                                 |
| [**MSVM \_ kvpexchangecomponent**](msvm-kvpexchangecomponent.md)<br/>                                           | Stellt den Status des Schlüssel-Wert-Paar-Exchange-Dienstanbieter dar, der einen Mechanismus zum Austauschen von Daten zwischen dem virtuellen Computer und dem Betriebssystem bereitstellt, das unter dem Verwaltungs Betriebssystem ausgeführt wird.<br/>                                                  |
| [**MSVM \_ kvpexchangecomponentsettingdata**](msvm-kvpexchangecomponentsettingdata.md)<br/>                     | Stellt den konfigurierten Status des Schlüssel-Wert-Paar-Exchange-Dienstanbieter dar.<br/>                                                                                                                                                                                    |
| [**MSVM \_ kvpexchangedataitem**](msvm-kvpexchangedataitem.md)<br/>                                             | Stellt ein Schlüssel-Wert-Paar dar.<br/>                                                                                                                                                                                                                               |
| [**MSVM \_ registeredguestservice**](msvm-registeredguestservice.md)<br/>                                       | Stellt eine Zuordnung zwischen einer Instanz von [**MSVM \_ guestserviceinterfacecomponent**](msvm-guestserviceinterfacecomponent.md) und einer Instanz von [**MSVM \_ guestservice**](msvm-guestservice.md)dar, die einen Dienst darstellt, der im Gast Betriebssystem ausgeführt wird. <br/> |
| [**MSVM \_ shutdowncomponent**](msvm-shutdowncomponent.md)<br/>                                                 | Stellt den Status des Diensts für das Herunterfahren dar, der einen Mechanismus zum Herunterfahren des Betriebssystems des virtuellen Computers von den Verwaltungs Schnittstellen auf dem Host System bereitstellt.<br/>                                                                       |
| [**MSVM \_ shutdowncomponentsettingdata**](msvm-shutdowncomponentsettingdata.md)<br/>                           | Stellt den konfigurierten Status des herunter Fahr Dienstanbieter dar.<br/>                                                                                                                                                                                                   |
| [**MSVM \_ timesynccomponent**](msvm-timesynccomponent.md)<br/>                                                 | Stellt den Status des Zeit Synchronisierungs dienstanens dar, der für die Synchronisierung der Systemzeit eines virtuellen Computers mit der Systemzeit des Betriebssystems im Verwaltungs Betriebssystem zuständig ist.<br/>                             |
| [**MSVM \_ timesynccomponentsettingdata**](msvm-timesynccomponentsettingdata.md)<br/>                           | Stellt den konfigurierten Status des Zeit Synchronisierungs dienstants dar.<br/>                                                                                                                                                                                       |
| [**MSVM \_ vsscomponent**](msvm-vsscomponent.md)<br/>                                                           | Stellt den Status des Volumeschattenkopie-Dienst-Diensts (VSS) dar, der die VSS-Anforderer im Gast Betriebssystem implementiert.<br/>                                                                                                                    |
| [**MSVM \_ vsscomponentsettingdata**](msvm-vsscomponentsettingdata.md)<br/>                                     | Stellt den konfigurierten Status des Volumeschattenkopie-Dienst-Diensts (VSS) dar.<br/>                                                                                                                                                                           |



 

 

 




