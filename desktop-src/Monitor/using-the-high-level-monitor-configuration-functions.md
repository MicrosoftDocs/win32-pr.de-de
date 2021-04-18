---
title: Verwenden der High-Level Monitor-Konfigurationsfunktionen
description: Verwenden der High-Level Monitor-Konfigurationsfunktionen
ms.assetid: 23e5d45d-a924-4119-b21d-b24764b53a94
keywords:
- überwachen, Funktionen
- Überwachen von Konfigurationsfunktionen auf hoher Ebene
- überwachen und auflisten physischer Monitore
- überwachen, fortlaufende Einstellungen
- Überwachen der Konfiguration, allgemeine Konfigurationsfunktionen
- Monitor Konfiguration, Funktionen
- Überwachen der Konfiguration, auflisten physischer Monitore
- Monitor Konfiguration, kontinuierliche Einstellungen
- Auflisten physischer Monitore
- Allgemeine Konfigurationsfunktionen
- fortlaufende Monitoreinstellungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff494388aac91d8aacd92ed4fe345722ea18659f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106337426"
---
# <a name="using-the-high-level-monitor-configuration-functions"></a>Verwenden der High-Level Monitor-Konfigurationsfunktionen

## <a name="enumerating-physical-monitors"></a>Auflisten physischer Monitore

Es gibt mehrere Funktionen, die Anzeigegeräte aufzählen, einschließlich " [**enumdisplaymonitors**](/windows/desktop/api/winuser/nf-winuser-enumdisplaymonitors) " und " [**monitorfromwindow**](/windows/desktop/api/winuser/nf-winuser-monitorfromwindow)". Diese Funktionen sind in der Dokumentation zu Windows GDI unter dem Thema [Multiple Display Monitors](/windows/desktop/gdi/multiple-display-monitors)dokumentiert. Diese Funktionen geben **Hmonitor** -Handles zurück. Trotz des Namens kann ein **Hmonitor** -handle jedoch mehr als einem physischen Monitor zugeordnet werden. Um die Einstellungen für einen Monitor zu konfigurieren, muss die Anwendung einen eindeutigen Handle für den physischen Monitor abrufen, indem [**getphysicalmonitorsfromhmonitor**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor)aufgerufen wird.

Wenn Ihre Anwendung Direct3D verwendet, können Sie ein Monitor Handle von einem Direct3D-Gerät abrufen, indem Sie [**GetPhysicalMonitorsFromIDirect3DDevice9**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromidirect3ddevice9)aufrufen.

## <a name="supported-functions"></a>Unterstützte Funktionen

Ein Monitor unterstützt möglicherweise nicht alle Monitor Konfigurationsfunktionen. Um herauszufinden, welche Funktionen von einem Monitor unterstützt werden, können Sie [**getmonitorfunctions**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitorcapabilities)aufrufen.

## <a name="continuous-monitor-settings"></a>Fortlaufende Monitor Einstellungen

Eine *kontinuierliche* Monitor Einstellung kann zwischen einem minimalen und einem maximalen Wert liegen. Die meisten der Monitor Konfigurationsfunktionen auf hoher Ebene steuern die kontinuierlichen Monitoreinstellungen. Beispielsweise sind "Helligkeit" und "Kontrast" kontinuierliche Einstellungen.

Die Einstellungen des kontinuierlichen Monitors haben nicht definierte reale Einheiten. Die Einheiten sind willkürlich und können von einem Hersteller zu einem anderen abweichen. Wenn beispielsweise zwei Monitore denselben Wert für die Helligkeit aufweisen, kann ein Monitor viel heller aussehen als ein anderer. In der Regel werden dem Benutzer in einer Anwendung Schieberegler-Steuerelemente oder auf-ab-Steuerelemente angezeigt. Der Benutzer kann die Einstellungen dann anpassen, um die beste subjektive Qualität zu erhalten.

## <a name="changes-in-monitor-state"></a>Änderungen im Monitor Status

Ein Monitor kann sich aus verschiedenen Gründen wie folgt ändern:

-   Der Benutzer ändert die Einstellungen mit den Front-Panel-Steuerelementen des Monitors.
-   Der Benutzer ändert die Bildschirmauflösung, die Aktualisierungsrate oder die Bittiefe des Monitors.
-   Die Anwendung verwendet die Monitor Funktionen auf niedriger Ebene, um eine Einstellung zu ändern, auf die von den Funktionen auf hoher Ebene aus nicht zugegriffen werden kann.
-   Die Anwendung ruft [**restoremonitorfactorycolordefaults**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-restoremonitorfactorycolordefaults) oder [**restoremonitorfactorydefaults**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-restoremonitorfactorydefaults)auf.

Alle diese Ereignisse können die Monitoreinstellungen ändern. Sie können auch den minimalen und maximalen Wert einer Einstellung ändern.

## <a name="dependencies-among-monitor-settings"></a>Abhängigkeiten zwischen den Monitor Einstellungen

Wenn Sie die Farbtemperatur ändern, kann das aktuelle Laufwerk geändert und Einstellungen abgerufen werden. das Gegenteil gilt auch für das Gegenteil. Dies sind die einzigen Abhängigkeiten zwischen den Monitor Konfigurationsfunktionen auf hoher Ebene. Andere Einstellungen sind möglicherweise nur über die Low-Level-Monitor Funktion verfügbar. Möglicherweise sind Abhängigkeiten zwischen diesen Einstellungen und den Einstellungen auf hoher Ebene vorhanden. Diese Abhängigkeiten sind Anbieter spezifisch. Eine Anwendung kann dieses Problem auf verschiedene Weise behandeln:

-   Verwenden Sie nur Funktionen auf hoher Ebene.
-   Nachdem Sie eine Funktion auf niedriger Ebene aufgerufen haben, rufen Sie den aktuellen Wert jeder Monitor Einstellung ab. Leider kann dieser Ansatz langsam sein, da das erzielen der einzelnen Einstellungen ungefähr 40 Millisekunden dauert.
-   Verwenden Sie Funktionen auf niedriger Ebene nur mit bestimmten überwachungsmodellen, deren Verhalten Sie verstehen.

## <a name="disabled-monitor-settings"></a>Deaktivierte Monitor Einstellungen

Eine Anwendung kann keine Monitoreinstellungen deaktivieren, indem Sie die übergeordneten Monitor Funktionen aufrufen. Allerdings kann eine Anwendung versehentlich eine Einstellung deaktivieren, wenn Sie die Funktionen auf niedriger Ebene verwendet, um eine Monitor Einstellung zu ändern, die von den Funktionen auf hoher Ebene nicht unterstützt wird. Außerdem kann ein Benutzer eine Einstellung mithilfe des Front-Panel-Steuer Elements deaktivieren. Diese Verhalten sind Anbieter spezifisch.

Wenn eine Monitor Einstellung deaktiviert wird, schlagen alle Funktionen, die diese Einstellung festlegen oder abrufen, fehl, und legen Sie den letzten Fehlercode auf Fehler \_ deaktivierte \_ Monitor \_ Einstellungen fest. In diesem Fall kann die Anwendung eine der folgenden Aktionen ausführen:

-   Zeigen Sie eine Fehlermeldung an, und zeigen Sie dem Benutzer an, dass er die Einstellung mithilfe des Front-Panel-Steuer Elements anpassen soll.
-   Der [**restoremonitorfactorydefaults**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-restoremonitorfactorydefaults) -Funktion wird aufgerufen. Wenn für einen Monitor das Flag "MC \_ Restore Factory-Standardeinstellungen" \_ aktiviert ist \_ \_ \_ \_ , werden von dieser Funktion alle Monitoreinstellungen aktiviert, die von den übergeordneten Monitor Funktionen unterstützt werden. Leider setzt die Funktion auch die Monitoreinstellungen auf ihren standardmäßigen Werkseinstellungen zurück.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden der Monitor Konfiguration](using-monitor-configuration.md)
</dt> </dl>

 

 