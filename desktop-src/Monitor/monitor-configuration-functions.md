---
title: Überwachen von Konfigurationsfunktionen
description: Überwachen von Konfigurationsfunktionen
ms.assetid: e9a00792-f471-47a4-93d7-25400e27f13f
keywords:
- überwachen, Funktionen
- Überwachen von Funktionen auf hoher Ebene
- Überwachen von Funktionen auf niedriger Ebene
- überwachen, Enumerationsfunktionen
- Funktionen auf hoher Ebene
- Low-Level-Funktionen
- Enumerationsfunktionen
- Monitor Konfiguration, Funktionen
- Überwachen der Konfiguration, Funktionen auf hoher Ebene
- Überwachen der Konfiguration, Low-Level-Funktionen
- Monitor Konfiguration, Enumerationsfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86925cd25912c17b8fb1bdd339888e5429de135b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340450"
---
# <a name="monitor-configuration-functions"></a>Überwachen von Konfigurationsfunktionen

Die folgenden Funktionen werden verwendet, um Informationen von einem Monitor zu erhalten und die Einstellungen eines Monitors zu ändern. Monitor Konfigurationsfunktionen werden in Funktionen auf hoher Ebene, auf Low-Level-Funktionen und Enumerationsfunktionen kategorisiert. Weitere Informationen finden Sie unter [Verwenden der Monitor Konfiguration](using-monitor-configuration.md).

## <a name="high-level-functions"></a>High-Level Funktionen



| Funktion                                                                         | BESCHREIBUNG                                                                          |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**"Degaussmonitor"**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-degaussmonitor)                                         | Degauert einen Monitor.                                                                 |
| [**Getmonitorhelligkeit**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitorbrightness)                             | Ruft die minimalen, maximalen und aktuellen Helligkeitseinstellungen eines Monitors ab.             |
| [**Getmonitorfunktionalitäten**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitorcapabilities)                         | Ruft die Konfigurationsfunktionen eines Monitors ab.                               |
| [**Getmonitorcolortemperatur**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitorcolortemperature)                 | Ruft die aktuelle Farbtemperatur eines Monitors ab.                                     |
| [**Getmonitorcontrast**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitorcontrast)                                 | Ruft die minimalen, maximalen und aktuellen Kontrasteinstellungen eines Monitors ab.               |
| [**Getmonitordisplayareaposition**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitordisplayareaposition)           | Ruft die minimale, maximale und aktuelle horizontale oder vertikale Position eines Monitors ab. |
| [**Getmonitordisplayareasize**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitordisplayareasize)                   | Ruft den Minimalwert, den Höchstwert und die aktuelle Breite oder Höhe eines Monitors ab.                 |
| [**Getmonitorredgreenorbluedrive**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitorredgreenorbluedrive)           | Ruft den roten, grünen oder blauen Laufwerks Wert eines Monitors ab.                               |
| [**Getmonitorredgreenorbluegain**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitorredgreenorbluegain)             | Ruft den roten, grünen oder blauen Wert eines Monitors ab.                                |
| [**Getmonitortechnologytype**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitortechnologytype)                     | Ruft den Typ der von einem Monitor verwendeten Technologie ab.                                  |
| [**Restoremonitorfactoriycolordefaults**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-restoremonitorfactorycolordefaults) | Stellt die Farbeinstellungen eines Monitors in den Werk seitigen Standardeinstellungen wieder her.                       |
| [**Restoremonitorfactoriydefaults**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-restoremonitorfactorydefaults)           | Stellt die Einstellungen eines Monitors auf die Werk seitigen Standardeinstellungen wieder her.                             |
| [**Savecurrentmonitorsettings**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-savecurrentmonitorsettings)                 | Speichert die aktuellen Monitoreinstellungen im nicht flüchtigen Speicher der Anzeige.             |
| [**Setmonitorhelligkeit**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-setmonitorbrightness)                             | Legt den Wert für die Helligkeit eines Monitors fest.                                                   |
| [**Setmonitorcolortemperatur**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-setmonitorcolortemperature)                 | Legt die Farbtemperatur eines Monitors fest.                                                  |
| [**Setmonitorcontrast**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-setmonitorcontrast)                                 | Legt den Kontrastwert eines Monitors fest.                                                     |
| [**Setmonitordisplayareaposition**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-setmonitordisplayareaposition)           | Legt die horizontale oder vertikale Position des Anzeige Bereichs eines Monitors fest.                |
| [**Setmonitordisplayareasize**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-setmonitordisplayareasize)                   | Legt die Breite oder Höhe des Anzeige Bereichs eines Monitors fest.                                |
| [**Setmonitorredgreenorbluedrive**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-setmonitorredgreenorbluedrive)           | Legt den Wert eines roten, grünen oder blauen Laufwerks für den Monitor fest.                                    |
| [**Setmonitorredgreenorbluegain**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-setmonitorredgreenorbluegain)             | Legt den roten, grünen oder blauen Wert eines Monitors fest.                                     |



 

## <a name="low-level-functions"></a>Low-Level Funktionen



| Funktion                                                                                   | BESCHREIBUNG                                                                                                    |
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**Capabilitiesrequestandcapabilitiesreply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-capabilitiesrequestandcapabilitiesreply) | Ruft eine Zeichenfolge ab, die die Funktionen eines Monitors beschreibt.                                                        |
| [**Getcapabilitiesstringlength**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getcapabilitiesstringlength)                         | Ruft die Länge der Funktions Zeichenfolge eines Monitors ab.                                                       |
| [**Gettimingreport**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-gettimingreport)                                                 | Ruft die horizontale und vertikale Synchronisierungs Frequenz eines Monitors ab.                                     |
| [**Getvcpfeatureandvcpfeaturereply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getvcpfeatureandvcpfeaturereply)                 | Ruft den aktuellen Wert, den maximalen Wert und den Codetyp eines virtuellen System Steuerungs Codes (VCP) für einen Monitor ab. |
| [**Savecurrentsettings**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-savecurrentsettings)                                         | Speichert die aktuellen Monitoreinstellungen im nicht flüchtigen Speicher der Anzeige.                                       |
| [**Setvcpfeature**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-setvcpfeature)                                                     | Legt den Wert eines VCP-Codes (Virtual Control Panel) für einen Monitor fest.                                            |



 

## <a name="enumeration-functions"></a>Enumerationsfunktionen



| Funktion                                                                                                   | BESCHREIBUNG                                                                               |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [**Destroyphysicalmonitor**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-destroyphysicalmonitor)                                                   | Schließt ein Handle für einen physischen Monitor.                                                    |
| [**Destroyphysicalmonitors**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-destroyphysicalmonitors)                                                 | Schließt ein Array physischer Monitor Handles.                                              |
| [**Getnumofphysicalmonitorsfromhmonitor**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getnumberofphysicalmonitorsfromhmonitor)                 | Hiermit wird die Anzahl der physischen Monitore abgerufen, die einem **Hmonitor** -Monitor Handle zugeordnet sind. |
| [**GetNumberOfPhysicalMonitorsFromIDirect3DDevice9**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getnumberofphysicalmonitorsfromidirect3ddevice9) | Hiermit wird die Anzahl der physischen Monitore abgerufen, die einem Direct3D-Gerät zugeordnet sind.              |
| [**Getphysicalmonitorsfromhmonitor**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor)                                 | Hiermit werden die physischen Monitore abgerufen, die einem **Hmonitor** -Monitor Handle zugeordnet sind.           |
| [**GetPhysicalMonitorsFromIDirect3DDevice9**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromidirect3ddevice9)                 | Hiermit werden die physischen Monitore abgerufen, die einem Direct3D-Gerät zugeordnet sind.                        |



 

## <a name="internal-functions"></a>Interne Funktionen

Die folgenden Funktionen werden von der Monitor-Konfigurations-API verwendet, um auf die Funktionalität des Anzeige Treibers zuzugreifen. Anwendungen sollten diese Funktionen nicht aufzurufen.

-   [**Ddccigetcapabilitiesstring**](ddccigetcapabilitiesstring.md)
-   [**Ddccigetcapabilitiesstringlength**](ddccigetcapabilitiesstringlength.md)
-   [**Ddccigettimingreport**](ddccigettimingreport.md)
-   [**Ddccigetvcpfeature**](ddccigetvcpfeature.md)
-   [**Ddccisavecurrentsettings**](ddccisavecurrentsettings.md)
-   [**Ddccisetvcpfeature**](ddccisetvcpfeature.md)
-   [**Destroyphysicalmonitorinternal**](destroyphysicalmonitorinternal.md)
-   [**Getnumofphysicalmonitors**](getnumberofphysicalmonitors.md)
-   [**Getphysicalmonitordescription**](getphysicalmonitordescription.md)
-   [**Getphysicalmonitors**](getphysicalmonitors.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Monitor Konfigurations Referenz](monitor-configuration-reference.md)
</dt> </dl>

 

 




