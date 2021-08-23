---
description: Ein Satz von WMI-Klassen, die die Machine Check Architecture (MCA) verfügbar machen. Die Systemabstraktionsschicht (System Abstraction Layer, SAL) stellt alle Ereignisse zur Verfügung, die in der MSMCA-Klasse gemeldet werden. Die Intel Corporation entwickelt und besitzt die MCA.
ms.assetid: 4e35f871-5bce-49ed-a3e8-d2d967e6e2dc
title: MSMCA-Klassen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea0f70bead9acbbb23fe0e2115ac12f967c7908f1f0eefa16d65cd1a57947e76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119641080"
---
# <a name="msmca-classes"></a>MSMCA-Klassen

Die MsMCA-Klassen (Microsoft Machine Check Architecture) sind eine Reihe von WMI-Klassen, die die Machine Check Architecture (MCA) verfügbar machen. Die Systemabstraktionsschicht (System Abstraction Layer, SAL) stellt alle Ereignisse zur Verfügung, die in der MSMCA-Klasse gemeldet werden. Die Intel Corporation entwickelt und besitzt die MCA.



| Klasse                                                                               | Beschreibung                                                                                            |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**MSMCAEvent \_ CPUError**](msmcaevent-cpuerror.md)                                 | Stellt ein CPU-Fehlerereignis dar.                                                                          |
| [**MSMCAEvent-Header \_**](msmcaevent-header.md)                                     | Stellt den allgemeinen Header dar, den alle MSMCAEvent-Klassen verwenden.                                          |
| [**MSMCAEvent \_ InvalidError**](msmcaevent-invaliderror.md)                         | Stellt einen ungültigen Fehler der Arbeitsspeicherüberprüfungsarchitektur (Memory Check Architecture, MCA) dar.                                            |
| [**MSMCAEvent \_ MemoryError**](msmcaevent-memoryerror.md)                           | Stellt ein MCA-Speicherfehlerereignis dar.                                                                  |
| [**MSMCAEvent \_ MemoryPageRemoved**](msmcaevent-memorypageremoved.md)               | Gibt an, dass das Betriebssystem eine physische Seite des Arbeitsspeichers entfernt hat.                                 |
| [**MSMCAEvent \_ PCIBusError**](msmcaevent-pcibuserror.md)                           | Stellt einen MCA-PCI-Busfehler dar.                                                                       |
| [**MSMCAEvent \_ PCIComponentError**](msmcaevent-pcicomponenterror.md)               | Stellt einen MCA-PCI-Komponentenfehler dar.                                                                 |
| [**MSMCAEvent \_ PlatformSpecificError**](msmcaevent-platformspecificerror.md)       | Stellt einen plattformspezifischen MCA-Fehler dar.                                                             |
| [**MSMCAEvent \_ SMBIOSError**](msmcaevent-smbioserror.md)                           | Stellt einen BIOS-Fehler des MCA-Systems dar.                                                                   |
| [**MSMCAEvent \_ SwitchToCMCPolling**](msmcaevent-switchtocmcpolling.md)             | Gibt an, dass die korrigierte Verarbeitung der Computerüberprüfung zum Abruf umgeschaltet wird.                            |
| [**MSMCAEvent \_ SystemEventError**](msmcaevent-systemeventerror.md)                 | Stellt einen MCA-Systemereignisfehler dar.                                                                  |
| [**MSMCAInfo**](msmcainfo.md)                                                      | Abstrakte Basisklasse, von der alle Datenklassen des Machine Check Architecture(MCA)-Anbieters abgeleitet werden. |
| [**MSMCAInfo-Eintrag \_**](msmcainfo-entry.md)                                         | Stellt einen MCA-, CMC- (Corrected Machine Check) oder CPE-Informationseintrag (Corrected Platform Error) dar. |
| [**MSMCAInfo \_ RawCMCEvent**](msmcainfo-rawcmcevent.md)                             | Enthält ein CMC-Ereignis.                                                                                  |
| [**MSMCAInfo \_ RawCorrectedPlatformEvent**](msmcainfo-rawcorrectedplatformevent.md) | Enthält ein korrigiertes Plattformereignis.                                                                   |
| [**MSMCAInfo \_ RawMCAData**](msmcainfo-rawmcadata.md)                               | Gibt die unformatten MCA-Protokolle an.                                                                            |
| [**MSMCAInfo \_ RawMCAEvent**](msmcainfo-rawmcaevent.md)                             | Enthält ein MCA-Ereignis.                                                                                  |
| [**WmiEvent**](wmievent.md)                                                        | Abstrakte Basisklasse, von der alle MCA-Anbieterereignisklassen abgeleitet werden.                             |



 

 

 



