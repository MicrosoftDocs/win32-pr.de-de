---
title: Desktopfenster-Manager ist immer eingeschaltet
description: Desktopfenster-Manager ist immer eingeschaltet
ms.assetid: 36E2DD1B-E480-47A9-850B-3057119641C0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b256b4270ab0bbeba588a4beff9bd1bd2bbe1c8166b40cd527f8b48a4f897df0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057360"
---
# <a name="desktop-window-manager-is-always-on"></a>Desktopfenster-Manager ist immer eingeschaltet

## <a name="platforms"></a>Plattformen

**Clients** – Windows 8  
**Server** – Windows Server 2012  


## <a name="description"></a>BESCHREIBUNG

In Windows 8 ist Desktopfenster-Manager (DWM) immer ON und kann von Endbenutzern und Apps nicht deaktiviert werden. Wie in Windows 7 wird DWM zum Erstellen des Desktops verwendet. Zusätzlich zu den in Windows 7 aktivierten Funktionen ermöglicht die DWM-Desktopkomposition jetzt die Desktopkomposition für alle Designs, unterstützung für Stereoskopisches 3D sowie Verwaltung, Trennung und Schutz der Benutzeroberfläche mit Windows Store Apps.

**Desktopkomposition für alle Designs**

In Windows Vista und Windows 7 ist die Desktopkomposition nur mit dem GLASS-Design aktiviert. Benutzer von Windows klassischen Designs und Designs mit hohem Kontrast können daher keine Funktionen verwenden, die durch die Desktopkomposition aktiviert werden, z. B. Windows Flip, automatische Skalierung für die Skalierung mit hoher Auflösung (DPI), Vorschauminiaturansicht und Vollbildlupe. Darüber hinaus müssen App-Entwickler in diesen früheren Versionen von Windows mehrere Codepfade schreiben und verwalten: einen, in dem die Desktopkomposition aktiviert ist, und einen anderen, in dem die Desktopkomposition deaktiviert ist.

Mit Windows 8 ist die Desktopkomposition für alle Designs aktiviert. Benutzer von Windows klassischen Designs und Designs mit hohem Kontrast können die Funktionen nutzen, die durch die Desktopkomposition ermöglicht werden, z. B. Windows Flip, automatische Skalierung für die Skalierung mit hoher Auflösung (High Resolution, DPI), Miniaturansichtsvorschau und Vollbildlupe. Darüber hinaus müssen Entwickler nicht mehrere Codepfade schreiben und verwalten, wodurch die Entwicklung vereinfacht wird.

**Unterstützung für stereokopiertes 3D**

Die DWM-Desktopkomposition unterstützt das Rendern und die Darstellung von 3D-App-Inhalten mit Stereoton und Vollbild.

**Verwaltung, Trennung und Schutz der Benutzeroberfläche mit Windows Store-Apps**

Die DWM-Desktopkomposition ermöglicht die Trennung und den Schutz von Desktop-App-Fenstern von den neuen Windows Store App-Fenstern, indem die Desktop-App-Fenster von den Windows Store App-Fenstern verwaltet und getrennt werden. Da die Desktopkomposition für die Verwaltung aller App-Fenster zuständig ist, kann das Deaktivieren der Desktopkomposition zu unerwartetem Verhalten führen. Darüber hinaus ist die Desktopkomposition für das Komponieren der neuen Startmenü sowie für zusätzliche Fensteranimationen verantwortlich, die die Kernpersonalisierung des neuen Windows Betriebssystems bilden.

## <a name="controlling-desktop-composition"></a>Steuern der Desktopkomposition

In Windows Vista und Windows 7 ist die Desktopkomposition in einer Reihe von Szenarien deaktiviert. In Windows 8 ist die DWM-Desktopkomposition eine Kernkomponente des Betriebssystems und kann nicht deaktiviert werden. Mit einigen Ausnahmen ist die Desktopkomposition immer eingeschaltet. sie wird vor der Benutzeranmeldung gestartet und bleibt für die Dauer einer Sitzung aktiv. In diesem Abschnitt wird beschrieben, wie Windows 8 die Szenarien in Windows 7 behandelt, in denen die Desktopkomposition deaktiviert ist.

**Server-SKU und bestimmte Client-SKUs**

In Windows 8 ist die Desktopkomposition für alle Server- und Client-SKUs aktiviert. Dadurch wird sichergestellt, dass Serveradministratoren und Benutzer von den Funktionen profitieren können, die durch die Desktopkomposition ermöglicht werden.

**Grundlegende Anforderungen für die Desktopkomposition**

Windows 8 stellt sicher, dass die Anforderungen an die Grafikadapter- und Systemfarbtiefe durch WDDM-Treiberunterstützung und Systemfarbtiefe erfüllt werden.

**WDDM-Treiberunterstützung**

Wenn ein System nicht über einen WDDM-kompatiblen Grafiktreiber verfügt, verwendet Windows 8 den Microsoft Basic-Anzeigeadapter als Standardadapter. Da DWM immer auf dem Standardadapter ausgeführt wird, wird der Microsoft Basic-Anzeigeadapter ausgewählt, um den Desktop zusammenzustellen, wenn ein WDDM-kompatibler Grafiktreiber auf dem System nicht verfügbar ist (unabhängig davon, ob er installiert oder deaktiviert ist).

Microsoft Basic Display Adapter ist ein Softwarerasterizer, der die CPU anstelle der GPU verwendet, um alle Zeichnungen auszuführen. Beachten Sie, dass die Leistung der Desktopkomposition auf dem Microsoft Basic-Anzeigeadapter (insbesondere Animationen) möglicherweise nicht so reibungslos ist wie bei der Ausführung der Desktopkomposition auf einer GPU.

**Systemfarbtiefe**

Die Desktopkomposition kann nur ausgeführt werden, wenn die Farbtiefe auf 32 Bits pro Pixel festgelegt ist. In Windows 7 kann die Farbtiefe des Systems in folgenden Szenarien geändert werden:

-   Ein Endbenutzer verwendet die Windows Systemsteuerung anzeigen oder eine Systemsteuerung eines Drittanbieters, um die Systemfarbe zu ändern.
-   Ein Endbenutzer führt eine App aus, die die Farbtiefe des Systems über eine öffentliche API ändert.

Im Gegensatz zu Windows 7 unterstützt Windows 8 keine andere Farbtiefe als 32 Bits pro Pixel. Der Benutzer kann die Farbtiefe des Systems nicht mehr über die Systemsteuerung ändern.

Darüber hinaus können App-Entwickler keine APIs verwenden, um die Farbtiefe des Systems zu ändern. Windows 8 erkennt Apps, die versuchen, die Farbtiefe des Systems in weniger als 32 Bits pro Pixel zu ändern, und informiert den Benutzer, dass ein App-Kompatibilitätss shim angewendet werden muss, um die Apps auszuführen. Nach der Bestätigung durch den Benutzer wird der App-Kompatibilitätss shim angewendet, und der Shim virtualisiert den Modus mit niedriger Farbe in die App, während das System bei 32 Bits pro Pixel ausgeführt wird.

**WinSAT**

In Windows 8 hängt die Desktopkomposition nicht von WinSAT-Bewertungen ab. Darüber hinaus umfasst WinSAT keine DWM-Bewertung mehr.

**App-Kompatibilität und Benutzeraktion**

In Windows 8:

-   Alle Optionen zum Deaktivieren der Desktopkomposition, die in Fenster 7 vorhanden sind, werden entfernt.
-   Die Desktopkomposition ist für das Verfassen aller Designs verantwortlich.
-   Apps können DwmEnableComposition nicht verwenden, um die Desktopkomposition zu deaktivieren. Um die Abwärtskompatibilität zu gewährleisten, gibt ein Aufruf dieser API den Erfolg zurück. Die Desktopkomposition ist jedoch nicht deaktiviert.
-   Der Shim "Desktopkomposition deaktivieren" wird entfernt.
-   Die Option "Desktopkomposition deaktivieren" auf der Registerkarte "Kompatibilität" des Dialogfelds Anwendungseigenschaften wird entfernt.

**Eine App verwendet einen Spiegelungstreiber für Remoting.**

In Windows 8:

-   Unterstützt keine Spiegeltreiber für Remotingszenarien. Während die meisten vorhandenen Apps, die Spiegeltreiber verwenden, weiterhin funktionieren sollten, funktionieren einige Features oder Apps, die Spiegeltreiber verwenden, aufgrund der Infrastrukturänderung, die erforderlich ist, um vorhandene Spiegeltreiber in Windows 8 mit DWM ON zu unterstützen.
-   Unterstützt Desktopduplizierungs-APIs für App-Entwickler, die Spiegeltreiber für Remotingszenarien verwenden.
-   Unterstützt keine vorhandenen Barrierefreiheitsspiegelungstreiber.
-   Vorhandene Spiegeltreiber müssen aktualisiert werden, um sicherzustellen, dass sie mit Windows 8

**Remotedesktopverbindung**

In Windows 8 ist die Desktopkomposition immer für eine Remotedesktopverbindung aktiviert. Für einen Clientcomputer, der eine Verbindung mit einem Windows 8 Remotecomputer herstellt, wird die Desktopkomposition für die Remotedesktopsitzung unabhängig von der Windows Clientversion immer aktiviert. Die Desktopkomposition wird für mehrere Monitore auf dem Clientcomputer sowie für die Remote-App-Sitzung unterstützt.

Darüber hinaus werden beim Herstellen einer Verbindung mit einem Windows 8 Remotecomputer diese Einstellungen im Remotedesktopverbindung-Client nicht wirksam:

-   Farbtiefe
-   Kontrollkästchen "Komposition aktivieren"

Die Farbtiefe der Verbindung wird immer auf 32 Bits pro Pixel festgelegt, und die Desktopkomposition ist immer aktiviert.

 

 




