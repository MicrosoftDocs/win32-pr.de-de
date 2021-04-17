---
title: Desktopfenster-Manager ist immer on.
description: Desktopfenster-Manager ist immer on.
ms.assetid: 36E2DD1B-E480-47A9-850B-3057119641C0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f855635615dee734b9a719d4e51d3ead663d144e
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "104316592"
---
# <a name="desktop-window-manager-is-always-on"></a>Desktopfenster-Manager ist immer on.

## <a name="platforms"></a>Plattformen

**Clients** – Windows 8  
**Server** – Windows Server 2012  


## <a name="description"></a>BESCHREIBUNG

In Windows 8 ist Desktopfenster-Manager (DWM) immer aktiviert und kann nicht von Endbenutzern und apps deaktiviert werden. Wie in Windows 7 wird DWM verwendet, um den Desktop zu verfassen. Zusätzlich zu den in Windows 7 aktivierten Oberflächen ermöglicht die DWM-Desktop Komposition die Desktop Komposition für alle Designs, die Unterstützung für Stereotyp-3D und die Verwaltung, Trennung und den Schutz der Erfahrung mit Windows Store-Apps.

**Desktop Komposition für alle Designs**

In Windows Vista und Windows 7 ist die Desktop Komposition nur mit dem Aero Glass-Design aktiviert. Daher können Benutzer von Windows Classic-und High-Contrast-Designs keine Umgebungen verwenden, die von der Desktop Komposition aktiviert werden, wie z. b. Windows Flip, automatische Skalierung für die Skalierung mit hoher Auflösung, Vorschau Vorschau und Vollbild Bildschirm Außerdem müssen App-Entwickler in diesen früheren Versionen von Windows mehrere Codepfade schreiben und verwalten – eine, bei der die Desktop Komposition aktiviert ist, und eine andere, bei der die Desktop Komposition deaktiviert ist.

Mit Windows 8 ist die Desktop Komposition für alle Designs aktiviert. Benutzer von Windows Classic-und High-Contrast-Designs können die von der Desktop Komposition aktivierten Oberflächen wie Windows Flip, die automatische Skalierung für die Skalierung mit hoher Auflösung, die Vorschau der Miniaturansichten und die Vollbild Bildschirmlupe verwenden. Außerdem müssen Entwickler nicht mehrere Codepfade schreiben und verwalten, um so die Entwicklung zu vereinfachen.

**Unterstützung für stereoskopisch 3D**

Die DWM-Desktop Komposition unterstützt das Rendering und die Darstellung von Fenster-und voll Bildinhalt-3D-App-Inhalt.

**Verwaltung, Trennung und Schutz der Funktionen mit Windows Store-Apps**

Die DWM-Desktop Komposition ermöglicht die Trennung und den Schutz von Desktop-App-Fenstern aus den neuen Windows Store-App-Fenstern durch verwalten und Trennen der Desktop-App-Fenster von Windows Store-App-Fenstern. Da die Desktop Komposition für die Verwaltung aller App-Fenster zuständig ist, kann die Deaktivierung der Desktop Komposition zu unerwartetem Verhalten führen. Außerdem ist die Desktop Komposition dafür verantwortlich, das neue Startmenü sowie weitere Fenster Animationen zu erstellen, die die Kern Persönlichkeit des neuen Windows-Betriebssystems bilden.

## <a name="controlling-desktop-composition"></a>Steuern der Desktop Komposition

In Windows Vista und Windows 7 ist die Desktop Komposition in einer Reihe von Szenarien deaktiviert. In Windows 8 ist die DWM-Desktop Komposition eine zentrale Betriebssystem Komponente und kann nicht deaktiviert werden. Mit wenigen Ausnahmen ist die Desktop Komposition immer on. Sie wird gestartet, bevor der Benutzer sich Anmeldungs-und verbleibt, während eine Sitzung aktiv ist. In diesem Abschnitt wird beschrieben, wie Windows 8 die Szenarien in Windows 7 behandelt, bei denen die Desktop Komposition deaktiviert ist.

**Server-SKU und bestimmte Client-SKUs**

In Windows 8 ist die Desktop Komposition für alle Server-und Client-SKUs aktiviert. Dadurch wird sichergestellt, dass Server Administratoren und Benutzer von den Erfahrungen profitieren können, die von der Desktop Komposition aktiviert werden.

**Grundlegende Anforderungen für die Desktop Komposition**

Windows 8 stellt sicher, dass die Anforderungen an Grafikkarten und System Farbtiefe durch die Unterstützung von WDDM-Treibern und die System Farbtiefe erfüllt werden.

**Unterstützung für WDDM-Treiber**

Wenn ein System keinen WDDM-kompatiblen Grafiktreiber hat, verwendet Windows 8 den Microsoft Basic-Anzeige Adapter als Standard Adapter. Da DWM immer auf dem Standard Adapter ausgeführt wird, wählt es den Microsoft Basic-Anzeige Adapter aus, um den Desktop zu verfassen, wenn ein WDDM-kompatibler Grafiktreiber nicht verfügbar ist (ob nicht installiert oder deaktiviert).

Beim Microsoft Basic-Anzeige Adapter handelt es sich um einen Software-Raster, der die CPU anstelle der GPU verwendet, um die gesamte Zeichnung auszuführen. Beachten Sie, dass die Leistung der Desktop Komposition auf dem Microsoft Basic-Anzeige Adapter (insbesondere Animationen) möglicherweise nicht so reibungslos ist, wie bei der Ausführung der Desktop Komposition auf einer GPU.

**System Farbtiefe**

Die Desktop Komposition kann nur ausgeführt werden, wenn die Farbtiefe auf 32 Bits pro Pixel festgelegt ist. In Windows 7 kann die Farb Tiefe des Systems in den folgenden Szenarien geändert werden:

-   Ein Endbenutzer verwendet die Windows-Systemsteuerung oder die Systemsteuerung von Drittanbietern, um die System Farbe zu ändern.
-   Ein Endbenutzer führt eine APP aus, die die Farbtiefe des Systems über eine öffentliche API ändert.

Anders als bei Windows 7 unterstützt Windows 8 keine Farbtiefe von höchstens 32 Bits pro Pixel. Der Benutzer kann die Farb Tiefe des Systems nicht mehr über die Systemsteuerung ändern.

Darüber hinaus können App-Entwickler keine APIs verwenden, um die Farbtiefe des Systems zu ändern. Windows 8 erkennt apps, die versuchen, die Farbtiefe des Systems auf weniger als 32 Bits pro Pixel zu ändern, und informiert den Benutzer darüber, dass ein Anwendungskompatibilitäts-Shim angewendet werden muss, um die apps auszuführen. Nach der Bestätigung durch den Benutzer wird der Anwendungskompatibilitäts-Shim angewendet, und das Shim virtualisiert den Modus mit niedriger Farbe für die APP, wobei das System auf 32 Bits pro Pixel ausgeführt wird.

**WinSAT**

In Windows 8 ist die Desktop Komposition nicht von WinSAT-Bewertungen abhängig. Darüber hinaus enthält WinSAT keine DWM-Bewertung mehr.

**APP-Kompatibilität und Benutzeraktion**

In Windows 8:

-   Alle Optionen zum Deaktivieren der Desktop Komposition, die in Windows 7 vorhanden sind, werden entfernt.
-   Die Desktop Komposition ist für das Verfassen aller Designs verantwortlich.
-   Apps können DwmEnableComposition nicht verwenden, um die Desktop Komposition zu deaktivieren. Um die Abwärtskompatibilität zu gewährleisten, wird ein Rückruf dieser API erfolgreich zurückgegeben. die Desktop Komposition ist jedoch nicht deaktiviert.
-   Das Shim "Desktop Komposition deaktivieren" wird entfernt.
-   Die Option zum Deaktivieren der Desktop Komposition auf der Registerkarte Kompatibilität im Dialogfeld Anwendungseigenschaften wird entfernt.

**Eine APP verwendet einen Spiegelungs Treiber für Remoting.**

In Windows 8:

-   Unterstützt keine Spiegel Treiber für Remoting-Szenarien. Obwohl die meisten der vorhandenen apps, die Spiegel Treiber verwenden, weiterhin funktionieren sollten. aufgrund der Infrastruktur Änderung, die zur Unterstützung vorhandener Spiegel Treiber in Windows 8 mit DWM unter erforderlich ist, funktionieren einige Features oder apps, die Spiegel Treiber verwenden, möglicherweise nicht.
-   Unterstützt Desktop Duplizierungs-APIs für App-Entwickler, die Spiegel Treiber für Remoting-Szenarien verwenden.
-   Vorhandene Barrierefreiheits Spiegel Treiber werden von nicht unterstützt.
-   Vorhandene Spiegel Treiber müssen aktualisiert werden, um sicherzustellen, dass Sie mit Windows 8 kompatibel sind.

**Remote Desktop Verbindung**

In Windows 8 ist die Desktop Komposition für eine Remote Desktop Verbindung immer aktiviert. Ein Client Computer, der eine Verbindung mit einem Windows 8-Remote Computer herstellt, erhält unabhängig von der Windows-Client Version immer die Desktop Komposition für die Remote Desktop Sitzung. Die Desktop Komposition wird für mehrere Monitore auf dem Client Computer sowie für die Remote-App-Sitzung unterstützt.

Wenn eine Verbindung mit einem Remote Computer mit Windows 8 hergestellt wird, werden die folgenden Einstellungen im Remotedesktopverbindung Client nicht wirksam:

-   Farbtiefe
-   Kontrollkästchen "Komposition aktivieren"

Die Farbtiefe der Verbindung ist immer auf 32 Bits pro Pixel festgelegt, und die Desktop Komposition ist immer aktiviert.

 

 




