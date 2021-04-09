---
title: Verwenden der Low-Level Monitor-Konfigurationsfunktionen
description: Verwenden der Low-Level Monitor-Konfigurationsfunktionen
ms.assetid: 014a144b-d01a-4bc1-959d-08a643b3e1f5
keywords:
- überwachen, Funktionen
- Überwachen von Konfigurationsfunktionen auf niedriger Ebene
- überwachen, DDC/CI
- überwachen, Anzeigen der Datenkanal-Befehlsschnittstelle
- Überwachen der Konfiguration, Low-Level-Konfigurationsfunktionen
- Monitor Konfiguration, Funktionen
- Monitor Konfiguration, DDC/CI
- Überwachen der Konfiguration, Anzeigen der Datenkanal-Befehlsschnittstelle
- Konfigurationsfunktionen auf niedriger Ebene
- Anzeigen der Datenkanal-Befehlsschnittstelle
- DDC/CI
- VESA-Monitor-Steuerungs Befehlssatz (MCCS)
- Monitor Steuerungs-Befehlssatz (MCCS)
- MCCS (Befehlssatz der Überwachungs Steuerung)
- Virtuelle Systemsteuerung (VCP)
- VCP (virtuelle Systemsteuerung)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d98e2cd4d85cb972b6a13896e9c497e51e16f8d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948685"
---
# <a name="using-the-low-level-monitor-configuration-functions"></a>Verwenden der Low-Level Monitor-Konfigurationsfunktionen

Bevor Sie die Konfigurationsfunktionen auf niedriger Ebene verwenden, sollten Sie mit diesen Standards vertraut sein:

-   Datenkanal Befehlsschnittstelle anzeigen (DDC/CI)
-   VESA-Monitor-Steuerungs Befehlssatz (MCCS)

Die Low-Level-Funktionen funktionieren, indem Sie die Werte von VCP-Codes (Virtual Control Panel) erhalten und festlegen. Ein VCP-Code kann *kontinuierlich* oder *nicht fortlaufend* sein. Fortlaufende Codes können einen beliebigen Wert zwischen 0 (null) und einem anbieterspezifischen maximalen Wert annehmen. Nicht kontinuierliche Codes unterstützen einen definierten Satz von Werten, der auch für den Anbieter spezifisch ist.

Führen Sie die folgenden Schritte aus, um die Überwachungs Konfigurationsfunktionen auf niedriger Ebene zu verwenden:

1.  Rufen Sie ein **Hmonitor** -Handle durch Aufrufen von [**enumdisplaymonitors**](/windows/desktop/api/winuser/nf-winuser-enumdisplaymonitors) oder [**monitorfromwindow**](/windows/desktop/api/winuser/nf-winuser-monitorfromwindow)ab.
2.  Aufrufen von [**getnumofphysicalmonitorsfromhmonitor**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getnumberofphysicalmonitorsfromhmonitor) zum Abrufen der Anzahl der physischen Monitore, die dem **Hmonitor** -Handle zugeordnet sind.
3.  Aufrufen von [**getphysicalmonitorsfromhmonitor**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor) , um eine Liste von Handles für die physischen Monitore zu erhalten.
4.  Aufrufen von [**getcapabilitiesstringlength**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getcapabilitiesstringlength) zum Abrufen der Länge der DDC/CI-Funktions Zeichenfolge eines Monitors. Die Funktions Zeichenfolge ist eine ASCII-Zeichenfolge, die statische Informationen über den Monitor enthält. Ein Teil der Zeichenfolge listet die VCP-Codes auf, die der Monitor unterstützt. In der Zeichenfolge werden auch die unterstützten Werte der nicht kontinuierlichen VCP-Codes aufgelistet.
5.  Zuordnen eines Puffers zum Speichern der Funktions Zeichenfolge und Aufrufen von [**capabilitiesrequestandcapabilitiesreply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-capabilitiesrequestandcapabilitiesreply) zum Abrufen der Zeichenfolge.
6.  Analysieren Sie die Funktions Zeichenfolge, um zu bestimmen, welche VCP-Codes der Monitor unterstützt.
7.  Bei einem kontinuierlichen VCP-Code wird [**getvcpfeatureandvcpfeaturereply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getvcpfeatureandvcpfeaturereply) aufgerufen, um den aktuellen und den maximalen Wert des Codes zu erhalten. Analysieren Sie für einen nicht kontinuierlichen VCP-Code die Funktions Zeichenfolge, um die unterstützten Werte zu erhalten.
8.  Aufrufen von [**setvcpfeature**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-setvcpfeature) , um einen neuen Wert für einen VCP-Code festzulegen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Verwenden der Monitor Konfiguration**](using-monitor-configuration.md)
</dt> </dl>

 

 