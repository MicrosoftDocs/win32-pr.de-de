---
description: Der WMI-Kern Anbieter definiert Klassen, die die Kernfunktionen von WMI bilden.
ms.assetid: 6EEA4284-CCFE-4206-9EAA-B4BCF988DE03
title: WMI-Kern Anbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9927be7208d9133d65257292950913972e96483
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217610"
---
# <a name="wmi-core-provider"></a>WMI-Kern Anbieter

Der WMI-Kern Anbieter definiert Klassen, die die Kernfunktionen von WMI bilden.

Die Mehrzahl der WMI-Kern Anbieter Klassen enthalten vom [WDM-Anbieter](wdm-provider.md)bereitgestellte Daten und beschreiben Anzeige Monitore. Die Klassen werden in der Datei "WMI. mof" definiert und befinden sich im \\ Namespace "root WMI".

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                           | BESCHREIBUNG                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MSMonitorClass**](msmonitorclass.md)<br/>                                             | ist eine abstrakte WMI-Basisklasse. Die Klassen, die die Videoanzeige Monitore beschreiben, erben von dieser [**MSMonitorClass**](msmonitorclass.md).<br/>                                                                         |
| [MSMCA-Klassen](msmca-classes.md)<br/>                                                   | eine Reihe von WMI-Klassen, die die Machine Check-Architektur (MCA) verfügbar machen. Die System Abstraktionsschicht (SAL) stellt alle Ereignisse bereit, die in der MSMCA-Klasse gemeldet werden. Die Intel Corporation entwickelt und besitzt die MCA.<br/>         |
| [**Frequencyrangedescriptor**](frequencyrangedescriptor.md)<br/>                         | stellt einen Container für Merkmale eines unterstützten Häufigkeits Bereichs dar.<br/>                                                                                                                                          |
| [**Supporteddisplayfeaturesdescriptor**](supporteddisplayfeaturesdescriptor.md)<br/>     | stellt die unterstützten Anzeigefunktionen des Monitors dar.<br/>                                                                                                                                                           |
| [**Videomodebug Descriptor**](videomodedescriptor.md)<br/>                                   | enthält modusdeskriptorelemente für das **monitorsourcemodes** -Array in der [**wmimonitorlistedsupportedsourcemodes**](wmimonitorlistedsupportedsourcemodes.md) -Klasse.<br/>                                           |
| [**WMIEvent**](wmievent.md)<br/>                                                         | Die [**wmievent**](wmievent.md) -Klasse ist eine Basisklasse, von der alle WMI-Ereignis Klassen abgeleitet werden.<br/>                                                                                                                |
| [**Wmimonitoranalog gvideoinputparameams**](wmimonitoranalogvideoinputparams.md)<br/>         | stellt die analogen Videoeingabe Parameter eines Computermonitors dar.<br/>                                                                                                                                                 |
| [**Wmimonitorbasicdisplaypara**](wmimonitorbasicdisplayparams.md)<br/>                 | stellt die grundlegenden Anzeigefunktionen eines Computermonitors dar.<br/>                                                                                                                                                        |
| [**Wmimonitorhelligkeit**](wmimonitorbrightness.md)<br/>                                 | stellt die Parameter für die Helligkeit eines Computermonitors dar.<br/>                                                                                                                                                         |
| [**Wmimonitorbrightnesabvent**](wmimonitorbrightnessevent.md)<br/>                       | stellt eine Änderung der Helligkeit eines Monitors dar.<br/>                                                                                                                                                                 |
| [**Wmimonitorbrightnessmethods**](wmimonitorbrightnessmethods.md)<br/>                   | enthält Methoden, mit denen die Monitor Helligkeit verwaltet wird.<br/>                                                                                                                                                                    |
| [**Wmimonitorcolorcharacteristics**](wmimonitorcolorcharacteristics.md)<br/>             | stellt die Farbmerkmale der International Commission on Illumination (CIE) eines Computermonitors dar.<br/>                                                                                                          |
| [**Wmimonitorconnectionpara**](wmimonitorconnectionparams.md)<br/>                     | enthält den Verbindungstyp des Monitors.<br/>                                                                                                                                                                        |
| [**Wmimonitordescriptormethods**](wmimonitordescriptormethods.md)<br/>                   | enthält Methoden, die den unformatierten Inhalt der Videoeingabe Definition von (VESA) erweiterten erweiterten Display Identification Data (E-EDID) v. 1. x-Standard-128-Byte-Datenblöcken abrufen.<br/> |
| [**Wmimonitordigitalvideoinputparameter.**](wmimonitordigitalvideoinputparams.md)<br/>       | stellt Eingabeparameter für digitales Video dar.<br/>                                                                                                                                                                      |
| [**Wmimonitorid**](wmimonitorid.md)<br/>                                                 | stellt die identifizierenden Informationen zu einem Videomonitor dar, z. b. Herstellername, Jahr der Fertigung oder Seriennummer.<br/>                                                                                     |
| [**Wmimonitorlistedfrequencyranges**](wmimonitorlistedfrequencyranges.md)<br/>           | Listet die vom Monitor unterstützten Häufigkeits Bereiche auf.<br/>                                                                                                                                                                |
| [**Wmimonitorlistedsupportedsourcemodes**](wmimonitorlistedsupportedsourcemodes.md)<br/> | Listet die unterstützten Quell Modi für einen Videomonitor in seinem Monitor Deskriptor auf, sofern vorhanden.<br/>                                                                                                                       |
| [**WmiMonitorRawEEdidV1Block**](wmimonitorraweedidv1block.md)<br/>                       | stellt die unformatierten Daten aus einer durch VESA erweiterten, erweiterten Display Identification Data (E-EDID)-Struktur dar.<br/>                                                                      |
| [**Xyzincie**](xyzincie.md)<br/>                                                         | enthält die Koordinaten der Anzeige im Bereich der International Commission on Illumination (CIE) XYZ-Farbraum.<br/>                                                                                                      |



 

 

 




