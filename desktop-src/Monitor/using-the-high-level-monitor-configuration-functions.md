---
title: Verwenden der High-Level Monitor-Konfigurationsfunktionen
description: Verwenden der High-Level Monitor-Konfigurationsfunktionen
ms.assetid: 23e5d45d-a924-4119-b21d-b24764b53a94
keywords:
- monitor,functions
- Monitor, high-level configuration functions (Überwachen, Konfigurationsfunktionen auf hoher Ebene)
- Überwachen,Aufzählen physischer Monitore
- Überwachen, kontinuierliche Einstellungen
- Überwachen der Konfiguration, übergeordnete Konfigurationsfunktionen
- Überwachen der Konfiguration, Funktionen
- Überwachen der Konfiguration, Aufzählen physischer Monitore
- Überwachen der Konfiguration, kontinuierliche Einstellungen
- Aufzählen physischer Monitore
- Konfigurationsfunktionen auf hoher Ebene
- Einstellungen für fortlaufende Überwachung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 827d19ef0006dc89208061c18ef34c28c8f993c3e0d6ebd0d1c1005daf2cd640
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066600"
---
# <a name="using-the-high-level-monitor-configuration-functions"></a>Verwenden der High-Level Monitor-Konfigurationsfunktionen

## <a name="enumerating-physical-monitors"></a>Aufzählen physischer Monitore

Es gibt mehrere Funktionen, die Anzeigegeräte aufzählen, einschließlich [**EnumDisplayMonitors**](/windows/desktop/api/winuser/nf-winuser-enumdisplaymonitors) und [**MonitorFromWindow.**](/windows/desktop/api/winuser/nf-winuser-monitorfromwindow) Diese Funktionen sind in der Windows GDI-Dokumentation unter dem Thema [Multiple Display Monitors](/windows/desktop/gdi/multiple-display-monitors)dokumentiert. Diese Funktionen geben **HMONITOR-Handles** zurück. Trotz des Namens kann ein **HMONITOR-Handle** jedoch mehreren physischen Monitoren zugeordnet werden. Um die Einstellungen auf einem Monitor zu konfigurieren, muss die Anwendung ein eindeutiges Handle für den physischen Monitor abrufen, indem [**Sie GetPhysicalMonitorsFromHMONITOR**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor)aufrufen.

Wenn Ihre Anwendung Direct3D verwendet, können Sie ein Monitorhandle von einem Direct3D-Gerät abrufen, indem [**Sie GetPhysicalMonitorsFromIDirect3DDevice9**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromidirect3ddevice9)aufrufen.

## <a name="supported-functions"></a>Unterstützte Funktionen

Ein Monitor unterstützt möglicherweise nicht alle Monitorkonfigurationsfunktionen. Um herauszufinden, welche Funktionen ein Monitor unterstützt, rufen [**Sie GetMonitorCapabilities auf.**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitorcapabilities)

## <a name="continuous-monitor-settings"></a>Continuous Monitor-Einstellungen

Eine *Kontinuierliche* Überwachungseinstellung kann zwischen einem minimalen und einem maximalen Wert liegen. Die meisten der übergeordneten Monitorkonfigurationsfunktionen steuern einstellungen für fortlaufende Monitore. Helligkeit und Kontrast sind beispielsweise kontinuierliche Einstellungen.

Kontinuierliche Überwachungseinstellungen verfügen nicht über definierte reale Einheiten. Die Einheiten sind willkürlich und können von Hersteller zu Hersteller variieren. Wenn zwei Monitore z. B. den gleichen Helligkeitswert aufweisen, sieht ein Monitor möglicherweise viel besser aus als ein anderer. In der Regel stellt eine Anwendung dem Benutzer Schieberegler- oder Nach-unten-Steuerelemente bereit. Der Benutzer kann dann die Einstellungen anpassen, um die beste subjektive Qualität zu bieten.

## <a name="changes-in-monitor-state"></a>Änderungen im Überwachungsstatus

Ein Monitor kann Zustände aus verschiedenen Gründen ändern, z. B.:

-   Der Benutzer ändert die Einstellungen mit den Frontpanel-Steuerelementen des Monitors.
-   Der Benutzer ändert die Bildschirmauflösung, Aktualisierungsrate oder Bittiefe des Monitors.
-   Die Anwendung verwendet die Monitorfunktionen auf niedriger Ebene, um eine Einstellung zu ändern, auf die von den funktionen auf hoher Ebene nicht zugegriffen werden kann.
-   Die Anwendung ruft [**RestoreMonitorFactoryColorDefaults**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-restoremonitorfactorycolordefaults) oder [**RestoreMonitorFactoryDefaults auf.**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-restoremonitorfactorydefaults)

Alle diese Ereignisse können die Überwachungseinstellungen ändern. Sie können auch den Minimal- und Höchstwert einer Einstellung ändern.

## <a name="dependencies-among-monitor-settings"></a>Abhängigkeiten zwischen Monitor-Einstellungen

Das Ändern der Farbtemperatur kann das aktuelle Laufwerk ändern und einstellungen gewinnen, und das Gegenteil ist ebenfalls der Fall. Dies sind die einzigen Abhängigkeiten zwischen den übergeordneten Monitorkonfigurationsfunktionen. Auf andere Einstellungen kann nur über die Monitorfunktionen auf niedriger Ebene zugegriffen werden. Möglicherweise bestehen Abhängigkeiten zwischen diesen Einstellungen und den einstellungen auf hoher Ebene. Diese Abhängigkeiten sind herstellerspezifisch. Eine Anwendung kann dieses Problem auf verschiedene Weise behandeln:

-   Verwenden Sie nur funktionen auf hoher Ebene.
-   Rufen Sie nach dem Aufrufen einer Funktion auf niedriger Ebene den aktuellen Wert jeder Überwachungseinstellung ab. Leider kann dieser Ansatz langsam sein, da das Abrufen jeder Einstellung etwa 40 Millisekunden dauert.
-   Verwenden Sie Funktionen auf niedriger Ebene nur mit bestimmten Überwachungsmodellen, deren Verhalten Sie verstehen.

## <a name="disabled-monitor-settings"></a>Deaktivierte monitor-Einstellungen

Eine Anwendung kann keine Monitoreinstellungen deaktivieren, indem sie die übergeordneten Monitorfunktionen aufruft. Eine Anwendung kann jedoch versehentlich eine Einstellung deaktivieren, wenn sie die Funktionen auf niedriger Ebene verwendet, um eine Überwachungseinstellung zu ändern, die von den funktionen auf hoher Ebene nicht unterstützt wird. Darüber hinaus kann ein Benutzer eine Einstellung mithilfe des Front-Panel-Steuerelements deaktivieren. Diese Verhaltensweisen sind herstellerspezifisch.

Wenn eine Überwachungseinstellung deaktiviert wird, schlägt jede Funktion, die diese Einstellung festlegt oder abruft, fehl und legt den Code für den letzten Fehler auf ERROR \_ DISABLED \_ MONITOR SETTING \_ fest. In diesem Fall kann die Anwendung eine der folgenden Schritte ausführen:

-   Zeigen Sie eine Fehlermeldung an, und schlagen Sie dem Benutzer vor, die Einstellung mithilfe des Frontpanel-Steuerelements anzupassen.
-   Rufen Sie die [**RestoreMonitorFactoryDefaults-Funktion auf.**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-restoremonitorfactorydefaults) Wenn ein Monitor über das \_ Funktionsflag MC RESTORE \_ FACTORY \_ DEFAULTS ENABLES MONITOR SETTINGS \_ \_ \_ verfügt, aktiviert diese Funktion alle Monitoreinstellungen, die von den übergeordneten Monitorfunktionen unterstützt werden. Leider setzt die Funktion auch die Monitoreinstellungen auf die Werkseinstellungen zurück.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden der Monitorkonfiguration](using-monitor-configuration.md)
</dt> </dl>

 

 