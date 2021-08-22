---
title: Überwachen von Konfigurationsfunktionen
description: Überwachen von Konfigurationsfunktionen
ms.assetid: e9a00792-f471-47a4-93d7-25400e27f13f
keywords:
- monitor,functions
- Monitor,Funktionen auf hoher Ebene
- Monitor,Low-Level-Funktionen
- Monitor,Enumerationsfunktionen
- Funktionen auf hoher Ebene
- Low-Level-Funktionen
- Enumerationsfunktionen
- Überwachen der Konfiguration,Funktionen
- Überwachen der Konfiguration,Funktionen auf hoher Ebene
- Überwachen der Konfiguration,Funktionen auf niedriger Ebene
- Überwachen der Konfiguration,Enumerationsfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b8b4eca3e18b5a5254ef9adc8cd55e123c26a773149d323caf517c5429d972f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013438"
---
# <a name="monitor-configuration-functions"></a>Überwachen von Konfigurationsfunktionen

Die folgenden Funktionen werden verwendet, um Informationen von einem Monitor zu erhalten und die Einstellungen eines Monitors zu ändern. Monitorkonfigurationsfunktionen werden in Funktionen auf hoher Ebene, Funktionen auf niedriger Ebene und Enumerationsfunktionen kategorisiert. Weitere Informationen finden Sie unter [Verwenden der Monitorkonfiguration.](using-monitor-configuration.md)

## <a name="high-level-functions"></a>High-Level Functions



| Funktion                                                                         | Beschreibung                                                                          |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**DeungenssMonitor**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-degaussmonitor)                                         | Entschärft einen Monitor.                                                                 |
| [**GetMonitorBrightness**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitorbrightness)                             | Ruft die Minimal-, Höchst- und aktuellen Helligkeitseinstellungen eines Monitors ab.             |
| [**GetMonitorCapabilities**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitorcapabilities)                         | Ruft die Konfigurationsfunktionen eines Monitors ab.                               |
| [**GetMonitorColorTemperature**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitorcolortemperature)                 | Ruft die aktuelle Farbtemperatur eines Monitors ab.                                     |
| [**GetMonitorContrast**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitorcontrast)                                 | Ruft die minimalen, maximalen und aktuellen Kontrasteinstellungen eines Monitors ab.               |
| [**GetMonitorDisplayAreaPosition**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitordisplayareaposition)           | Ruft die minimale, maximale und aktuelle horizontale oder vertikale Position eines Monitors ab. |
| [**GetMonitorDisplayAreaSize**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitordisplayareasize)                   | Ruft die minimale, maximale und aktuelle Breite oder Höhe eines Monitors ab.                 |
| [**GetMonitorRedGreenOrBlueDrive**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitorredgreenorbluedrive)           | Ruft den Wert des roten, grünen oder blauen Laufwerks eines Monitors ab.                               |
| [**GetMonitorRedGreenOrBlueGain**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitorredgreenorbluegain)             | Ruft den Gewinnwert eines Monitors in Rot, Grün oder Blau ab.                                |
| [**GetMonitorTechnologyType**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitortechnologytype)                     | Ruft den Typ der von einem Monitor verwendeten Technologie ab.                                  |
| [**RestoreMonitorFactoryColorDefaults**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-restoremonitorfactorycolordefaults) | Stellt die Farbeinstellungen eines Monitors auf die Werkseinstellungen wieder zurück.                       |
| [**RestoreMonitorFactoryDefaults**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-restoremonitorfactorydefaults)           | Stellt die Einstellungen eines Monitors auf die Werkseinstellungen wieder zurück.                             |
| [**SaveCurrentMonitorSettings**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-savecurrentmonitorsettings)                 | Speichert die aktuellen Monitoreinstellungen im nicht unwillingsfreien Speicher der Anzeige.             |
| [**SetMonitorBrightness**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-setmonitorbrightness)                             | Legt den Helligkeitswert eines Monitors fest.                                                   |
| [**SetMonitorColorTemperature**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-setmonitorcolortemperature)                 | Legt die Farbtemperatur eines Monitors fest.                                                  |
| [**SetMonitorContrast**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-setmonitorcontrast)                                 | Legt den Kontrastwert eines Monitors fest.                                                     |
| [**SetMonitorDisplayAreaPosition**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-setmonitordisplayareaposition)           | Legt die horizontale oder vertikale Position des Anzeigebereichs eines Monitors fest.                |
| [**SetMonitorDisplayAreaSize**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-setmonitordisplayareasize)                   | Legt die Breite oder Höhe des Anzeigebereichs eines Monitors fest.                                |
| [**SetMonitorRedGreenOrBlueDrive**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-setmonitorredgreenorbluedrive)           | Legt den Wert des roten, grünen oder blauen Laufwerks eines Monitors fest.                                    |
| [**SetMonitorRedGreenOrBlueGain**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-setmonitorredgreenorbluegain)             | Legt den Gewinnwert eines Monitors für Rot, Grün oder Blau fest.                                     |



 

## <a name="low-level-functions"></a>Low-Level Functions



| Funktion                                                                                   | Beschreibung                                                                                                    |
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**CapabilitiesRequestAndCapabilitiesReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-capabilitiesrequestandcapabilitiesreply) | Ruft eine Zeichenfolge ab, die die Funktionen eines Monitors beschreibt.                                                        |
| [**GetCapabilitiesStringLength**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getcapabilitiesstringlength)                         | Ruft die Länge der Funktionenzeichenfolge eines Monitors ab.                                                       |
| [**GetTimingReport**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-gettimingreport)                                                 | Ruft die horizontalen und vertikalen Synchronisierungshäufigkeiten eines Monitors ab.                                     |
| [**GetVCPFeatureAndVCPFeatureReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getvcpfeatureandvcpfeaturereply)                 | Ruft den aktuellen Wert, den maximal zulässigen Wert und den Codetyp eines VCP-Codes (Virtual Systemsteuerung) für einen Monitor ab. |
| [**SaveCurrentSettings**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-savecurrentsettings)                                         | Speichert die aktuellen Monitoreinstellungen im nicht unwillingsfreien Speicher der Anzeige.                                       |
| [**SetVCPFeature**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-setvcpfeature)                                                     | Legt den Wert eines VCP-Codes (Virtual Systemsteuerung) für einen Monitor fest.                                            |



 

## <a name="enumeration-functions"></a>Enumerationsfunktionen



| Funktion                                                                                                   | Beschreibung                                                                               |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [**DestroyPhysicalMonitor**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-destroyphysicalmonitor)                                                   | Schließt ein Handle für einen physischen Monitor.                                                    |
| [**DestroyPhysicalMonitors**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-destroyphysicalmonitors)                                                 | Schließt ein Array physischer Monitorhandles.                                              |
| [**GetNumberOfPhysicalMonitorsFromHMONITOR**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getnumberofphysicalmonitorsfromhmonitor)                 | Ruft die Anzahl der physischen Monitore ab, die einem **HMONITOR-Monitorhandpunkt** zugeordnet sind. |
| [**GetNumberOfPhysicalMonitorsFromIDirect3DDevice9**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getnumberofphysicalmonitorsfromidirect3ddevice9) | Ruft die Anzahl der physischen Monitore ab, die einem Direct3D-Gerät zugeordnet sind.              |
| [**GetPhysicalMonitorsFromHMONITOR**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor)                                 | Ruft die physischen Monitore ab, die einem **HMONITOR-Monitorhandpunkt** zugeordnet sind.           |
| [**GetPhysicalMonitorsFromIDirect3DDevice9**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromidirect3ddevice9)                 | Ruft die physischen Monitore ab, die einem Direct3D-Gerät zugeordnet sind.                        |



 

## <a name="internal-functions"></a>Interne Funktionen

Die folgenden Funktionen werden von der Api für die Monitorkonfiguration verwendet, um auf die Funktionalität im Anzeigetreiber zuzugreifen. Anwendungen sollten diese Funktionen nicht aufrufen.

-   [**DDCCIGetCapabilitiesString**](ddccigetcapabilitiesstring.md)
-   [**DDCCIGetCapabilitiesStringLength**](ddccigetcapabilitiesstringlength.md)
-   [**DDCCIGetTimingReport**](ddccigettimingreport.md)
-   [**DDCCIGetVCPFeature**](ddccigetvcpfeature.md)
-   [**DDCCISaveCurrentSettings**](ddccisavecurrentsettings.md)
-   [**DDCCISetVCPFeature**](ddccisetvcpfeature.md)
-   [**DestroyPhysicalMonitorInternal**](destroyphysicalmonitorinternal.md)
-   [**GetNumberOfPhysicalMonitors**](getnumberofphysicalmonitors.md)
-   [**GetPhysicalMonitorDescription**](getphysicalmonitordescription.md)
-   [**GetPhysicalMonitors**](getphysicalmonitors.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Referenz zur Monitorkonfiguration](monitor-configuration-reference.md)
</dt> </dl>

 

 




