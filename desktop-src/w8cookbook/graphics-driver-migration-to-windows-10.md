---
title: Migration von Grafiktreibern zu Windows 10
description: Windows 10 Media und Windows 10 (wie der Vorgänger, Windows 8.1) verfügen über keine Grafiktreiber von Drittanbietern im Windows Media Kit oder in Box.
ms.assetid: E6240CF0-5A65-4A66-98AE-856C783EB320
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a23d8ae341172223955fcc781f95b7615bcfc867
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341470"
---
# <a name="graphics-driver-migration-to-windows-10"></a>Migration von Grafiktreibern zu Windows 10

Windows 10 Media und Windows 10 (wie der Vorgänger, Windows 8.1) verfügen über keine Grafiktreiber von Drittanbietern im Windows Media Kit oder in Box. Stattdessen werden die Grafiktreiber für eine große Bandbreite von Geräten auf Wu bereitgestellt, sodass Hardwarehersteller Treiber aktualisieren können, ohne dass eine Änderung des Betriebssystem Abbilds erforderlich ist. Außerdem werden vorhandene Treiber bei einem Betriebssystem Upgrade auf Windows 10 von Windows 7, Windows 8 oder Windows 8.1 nicht zu Windows 10 migriert. Dies wirkt sich auch auf Upgrades von Windows Server 2012 aus.

## <a name="upgrades-and-installation"></a>Upgrades und Installation

Bei Upgrades und Neuinstallationen müssen die Grafiktreiber von Windows Update (Wu) oder der IHV/OEM-Website für die relevante Hardware abgerufen werden. Dies erfordert eine Internetverbindung. Die Treiber in Wu werden durch dynamisches Update (du) in das Betriebssystem Setup eingefügt, wenn ein Benutzer Ihr Windows 7-oder Windows 8. x-System auf Windows 10 aktualisiert.

> [!Note]  
> Dies gilt nicht für Systeme, die im Lieferumfang von vorinstalliertem Windows enthalten sind, z. b. Computer, die in einem Einzelhandelsgeschäft erworben wurden. Diese Systeme verfügen bereits über die Grafiktreiber, die vom OEM installiert wurden. Der OEM stellt möglicherweise auch eine DVD (für die Neuinstallation des Betriebssystems) bereit, die die Treiber enthält.

 

Nach dem Upgrade auf Windows 10 stellen Benutzer möglicherweise fest, dass auf Ihrem PC keine Grafiktreiber installiert sind. Dies kann folgende Ursachen haben:

-   Der Benutzer hat sich für eine Neuinstallation entschieden, d. h. kein Upgrade.
-   Der Benutzer hat die Option zum Suchen nach Updates während des Upgrades deaktiviert, d. h., das dynamische Update (du) wurde deaktiviert.
-   Die Internet Verbindung funktionierte während des Upgrades nicht.
-   Die Treiberinstallation ist fehlgeschlagen.

Nach einer Ordnungs losen Installation des Betriebssystems werden keine Grafiktreiber auf dem PC angezeigt, solange der Wu-Client nicht automatisch ausgeführt wird und die anwendbaren Treiber heruntergeladen werden. In der Zwischenzeit führt der PC den Microsoft Basic Display Adapter (msbda) mit eingeschränkten Funktionen aus, z. b. keine Unterstützung für mehrere Monitore, und der Benutzer kann im Vergleich zu einem Hardwaretreiber auch eine schlechte Leistung erleben, z. b. langsame Framerate oder Risse bei der Videowiedergabe.

## <a name="manifestations"></a>Kundgebungen

Bei älteren PCs (in der Regel vor Windows 7 erstellt) ist es möglich, dass keine Treiber für Windows 10 auf Wu vorhanden sind, da die Grafikkarten das Ende des Lebenszyklus erreicht haben und von den Hardwareanbietern nicht mehr unterstützt werden. Sogar Systeme, die derzeit Windows 7 oder 8. x ausführen, wurden möglicherweise von einem früheren Betriebssystem aktualisiert und können über EOL-Grafikadapter verfügen.

Für neuere PCs sind möglicherweise keine Treiber verfügbar, da der Grafikadapter von einem älteren Computer übertragen wurde, z. b. während eines Hardware Upgrades. Dies tritt am häufigsten bei Computern mit mehreren Grafikadaptern auf, bei denen der Benutzer beim Erwerb eines neuen Computers eine alte Grafikkarte aufbewahrt hat, um mehrere Anzeige Vorgänge zu verwenden.

Eine weitere Möglichkeit für einen kleinen Prozentsatz an Computern besteht darin, dass Windows Update nur über "Coverage"-Treiber verfügt. Dabei handelt es sich um generische Treiber, die keine OEM-Anpassungen haben. Ein Benutzer, der nach dem Upgrade auf Windows 10 einen dieser Treiber übermittelt, kann sehen, dass einige Funktionen fehlen, z. b. funktionieren Funktionstasten zum Steuern der Bildschirmhelligkeit nicht mehr.

## <a name="mitigations"></a>Gegenmaßnahmen

-   Geeignete Grafiktreiber sollten bei der Aktualisierung entweder während des Upgradevorgangs oder nach Abschluss des Upgrades direkt nach dem Upgrade übermittelt werden. OEMs müssen sicherstellen, dass die entsprechenden Grafiktreiber in den System Abbildern enthalten sind, die für die Hersteller Installation von Windows 10 auf ihren Computern verwendet werden.
-   Nach einem Upgrade kann der Benutzer die Einstellungen Windows Update für Treiber explizit überprüfen, \\ obwohl dies nicht erforderlich sein sollte. Benutzer, die eine Überprüfung erzwingen, während ein Treiber automatisch im Hintergrund installiert wird, sehen möglicherweise einen Fehler bei der Treiberinstallation, wenn die automatische Installation zuerst abgeschlossen wird. Sie können diese Warnmeldung ignorieren.
-   Benutzer, die eine Neuinstallation von Windows 10 durchführen möchten, sollten die relevanten Treiber vor der Installation abrufen oder darauf verlassen, dass Windows Update die Treiber später bereitstellt. in diesem Fall müssen Sie sicherstellen, dass Ihre Internet Verbindung funktioniert.
-   Für Computer, die einen Abdeckungs Treiber empfangen, gibt es keine Entschärfung für fehlende Funktionalität. Dies sollte jedoch nur in Fällen auftreten, in denen der Hardwarelieferant die Treiber nicht mehr verwaltet, d. h. Computer, die mehrere Jahre alt sind.

> [!Note]  
> Für Systeme mit einer einzelnen Anzeige, z. b. einem Laptop, werden viele Benutzer feststellen, dass msbda akzeptabel ist, und dass der Mangel an Hardware Treibern nicht auffindbar ist. In diesem Fall ist keine Entschärfung erforderlich.

 

## <a name="solutions"></a>Lösungen

Es ist wichtig, dass IHVs und OEMs Ihre Windows 10-Grafiktreiber für alle Hardware, die Sie unterstützen möchten, in Wu hochladen.

Benutzer sollten beim Upgrade die Option "nach Updates suchen" ausgewählt haben (Standardeinstellung). Abhängig von der Geschwindigkeit der Netzwerkverbindung und der Auslastung der Wu-Server kann dies bedeuten, dass die Treiber erst installiert werden, nachdem OOBE abgeschlossen ist und sich der Benutzer zum ersten Mal angemeldet hat. In der Zwischenzeit hat der Benutzer möglicherweise einige eingeschränkte Funktionen oder eine schlechte Leistung bemerkt.

Benutzer müssen sicherstellen, dass Ihre Internet Verbindung funktioniert, bevor Sie ein Upgrade starten, auch wenn Sie mithilfe von Medien (DVD oder Flash Laufwerk) aktualisiert werden.

-   Wenn der PC mit dem Internet verbunden ist, sollten die entsprechenden Treiber automatisch heruntergeladen und installiert werden. Der Benutzer muss keine Maßnahmen ergreifen.
-   Wenn der PC nicht mit dem Internet verbunden ist, müssen die Treiber mithilfe eines mit dem Internet verbundenen Computers von der IHV-oder OEM-Website heruntergeladen werden. wird mithilfe eines Flash Laufwerks oder einer CD/DVD auf den Zielcomputer übertragen. und dann manuell installiert.

 

 




