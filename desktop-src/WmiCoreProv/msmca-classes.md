---
description: Eine Reihe von WMI-Klassen, die die Machine Check-Architektur (MCA) verfügbar machen. Die System Abstraktionsschicht (SAL) stellt alle Ereignisse bereit, die in der MSMCA-Klasse gemeldet werden. Die Intel Corporation entwickelt und besitzt die MCA.
ms.assetid: 4e35f871-5bce-49ed-a3e8-d2d967e6e2dc
title: MSMCA-Klassen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 461d4c5c50ae5316c96c3dffc18af7b729cfa6e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347058"
---
# <a name="msmca-classes"></a>MSMCA-Klassen

Bei den MSMCA-Klassen (Microsoft Machine Check Architecture) handelt es sich um einen Satz von WMI-Klassen, die die MCA (Machine Check Architecture) verfügbar machen. Die System Abstraktionsschicht (SAL) stellt alle Ereignisse bereit, die in der MSMCA-Klasse gemeldet werden. Die Intel Corporation entwickelt und besitzt die MCA.



| Klasse                                                                               | BESCHREIBUNG                                                                                            |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**Msmcaevent \_ cpuerror**](msmcaevent-cpuerror.md)                                 | Stellt ein CPU-Fehler Ereignis dar.                                                                          |
| [**Msmcaevent- \_ Header**](msmcaevent-header.md)                                     | Stellt den allgemeinen Header dar, der von allen msmcaevent-Klassen verwendet wird.                                          |
| [**Msmcaevent \_ invaliderror**](msmcaevent-invaliderror.md)                         | Stellt einen ungültigen Fehler in der Speicher Prüf Architektur (MCA) dar.                                            |
| [**Msmcaevent \_ MemoryError**](msmcaevent-memoryerror.md)                           | Stellt ein MCA-Speicherfehler Ereignis dar.                                                                  |
| [**Msmcaevent \_ memorypageremoved**](msmcaevent-memorypageremoved.md)               | Gibt an, dass das Betriebssystem eine physische Seite des Arbeitsspeichers entfernt hat.                                 |
| [**Msmcaevent \_ pcibuserror**](msmcaevent-pcibuserror.md)                           | Stellt einen MCA PCI-Busfehler dar.                                                                       |
| [**Msmcaevent \_ pcicomponendterror**](msmcaevent-pcicomponenterror.md)               | Stellt einen MCA-PCI-Komponenten Fehler dar.                                                                 |
| [**Msmcaevent \_ platformspecificerror**](msmcaevent-platformspecificerror.md)       | Stellt einen plattformspezifischen MCA-Fehler dar.                                                             |
| [**Msmcaevent \_ smbioserror**](msmcaevent-smbioserror.md)                           | Stellt einen MCA-System-BIOS-Fehler dar.                                                                   |
| [**Msmcaevent \_ switchumcmcabruf**](msmcaevent-switchtocmcpolling.md)             | Gibt an, dass die korrigierte Verarbeitung der Computer Überprüfung zum Abrufen gewechselt wird.                            |
| [**Msmcaevent \_ systemeventerror**](msmcaevent-systemeventerror.md)                 | Stellt einen MCA-System Ereignis Fehler dar.                                                                  |
| [**Msmcainfo**](msmcainfo.md)                                                      | Eine abstrakte Basisklasse, von der alle Daten Klassen für MCA-Anbieter (Machine Check Architecture) abgeleitet werden. |
| [**Msmcainfo- \_ Eintrag**](msmcainfo-entry.md)                                         | Stellt einen MCA-, korrigierten Computer Überprüfung (CMC)-oder CPE-Informations Eintrag (korrigiert Platform Error) dar. |
| [**Msmcainfo \_ rawcmcevent**](msmcainfo-rawcmcevent.md)                             | Enthält ein CMC-Ereignis.                                                                                  |
| [**Msmcainfo \_ rawcorrectedplatformevent**](msmcainfo-rawcorrectedplatformevent.md) | Enthält ein korrigiertes Platt Form Ereignis.                                                                   |
| [**Msmcainfo \_ rawmcadata**](msmcainfo-rawmcadata.md)                               | Gibt die unformatierten MCA-Protokolle an.                                                                            |
| [**Msmcainfo \_ rawmcaevent**](msmcainfo-rawmcaevent.md)                             | Enthält ein MCA-Ereignis.                                                                                  |
| [**WmiEvent**](wmievent.md)                                                        | Abstrakte Basisklasse, von der alle MCA-Anbieter Ereignis Klassen abgeleitet werden.                             |



 

 

 



