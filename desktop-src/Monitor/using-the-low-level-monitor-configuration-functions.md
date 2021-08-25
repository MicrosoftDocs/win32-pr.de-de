---
title: Verwenden der Low-Level Monitor-Konfigurationsfunktionen
description: Verwenden der Low-Level Monitor-Konfigurationsfunktionen
ms.assetid: 014a144b-d01a-4bc1-959d-08a643b3e1f5
keywords:
- Monitor, Funktionen
- Monitor,Low-Level-Konfigurationsfunktionen
- Monitor, DDC/CI
- monitor,Display Data Channel Command Interface
- Überwachen der Konfiguration,Konfigurationsfunktionen auf niedriger Ebene
- Überwachen der Konfiguration,Funktionen
- Überwachen der Konfiguration, DDC/CI
- Überwachen der Konfiguration, Anzeigen der Datenkanal-Befehlsschnittstelle
- Konfigurationsfunktionen auf niedriger Ebene
- Anzeigen der Datenkanalbefehlsschnittstelle
- DDC/CI
- VESA Monitor Control Command Set (MCCS)
- Monitor Control Command Set (MCCS)
- MCCS (Monitor Control Command Set)
- Virtual Systemsteuerung (VCP)
- VCP (Virtual Systemsteuerung)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3ffd21f0b232db71bb6023f968122271ce70f03b0a632dc33d9df1e7ee993bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119927390"
---
# <a name="using-the-low-level-monitor-configuration-functions"></a>Verwenden der Low-Level Monitor-Konfigurationsfunktionen

Bevor Sie die Low-Level-Monitorkonfigurationsfunktionen verwenden, sollten Sie mit diesen Standards vertraut sein:

-   Anzeigen der Datenkanal-Befehlsschnittstelle (DDC/CI)
-   VESA Monitor Control Command Set (MCCS)

Die Funktionen auf niedriger Ebene werden verwendet, indem sie die Werte von VCP-Codes (Virtual Systemsteuerung) abrufen und festlegen. Ein VCP-Code kann *kontinuierlich oder* nicht *fortlaufend sein.* Kontinuierliche Codes können einen beliebigen Wert zwischen 0 (null) und einem anbieterspezifischen Höchstwert annehmen. Nicht zusammenhängende Codes unterstützen einen definierten Satz von Werten, der auch für den Anbieter spezifisch ist.

Führen Sie die folgenden Schritte aus, um die Konfigurationsfunktionen des Low-Level-Monitors zu verwenden:

1.  Rufen Sie ein **HMONITOR-Handle** ab, indem [**Sie EnumDisplayMonitors**](/windows/desktop/api/winuser/nf-winuser-enumdisplaymonitors) oder [**MonitorFromWindow aufrufen.**](/windows/desktop/api/winuser/nf-winuser-monitorfromwindow)
2.  Rufen [**Sie GetNumberOfPhysicalMonitorsFromHMONITOR auf,**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getnumberofphysicalmonitorsfromhmonitor) um die Anzahl der physischen Monitore zu erhalten, die dem **HMONITOR-Handle zugeordnet** sind.
3.  Rufen [**Sie GetPhysicalMonitorsFromHMONITOR auf,**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor) um eine Liste der Handles für die physischen Monitore zu erhalten.
4.  Rufen [**Sie GetCapabilitiesStringLength**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getcapabilitiesstringlength) auf, um die Länge der DDC/CI-Funktionenzeichenfolge eines Monitors zu erhalten. Die Funktionenzeichenfolge ist eine ASCII-Zeichenfolge, die statische Informationen zum Monitor enthält. In einem Teil der Zeichenfolge werden die vom Monitor unterstützten VCP-Codes aufgeführt. Die Zeichenfolge listet auch die unterstützten Werte der nicht zusammenhängenden VCP-Codes auf.
5.  Ordnen Sie einen Puffer zu, der die Funktionenzeichenfolge enthält, und rufen [**Sie CapabilitiesRequestAndCapabilitiesReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-capabilitiesrequestandcapabilitiesreply) auf, um die Zeichenfolge zu erhalten.
6.  Analysieren Sie die Funktionenzeichenfolge, um zu bestimmen, welche VCP-Codes der Monitor unterstützt.
7.  Rufen Sie für einen kontinuierlichen VCP-Code [**GetVCPFeatureAndVCPFeatureReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getvcpfeatureandvcpfeaturereply) auf, um die aktuellen und maximalen Werte des Codes zu erhalten. Analysieren Sie für einen nicht zusammenhängenden VCP-Code die Funktionenzeichenfolge, um die unterstützten Werte zu erhalten.
8.  Rufen [**Sie SetVCPFeature auf,**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-setvcpfeature) um einen neuen Wert für einen VCP-Code zu festlegen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Verwenden der Monitorkonfiguration**](using-monitor-configuration.md)
</dt> </dl>

 

 