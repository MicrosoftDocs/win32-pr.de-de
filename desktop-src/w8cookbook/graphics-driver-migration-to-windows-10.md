---
title: Grafiktreibermigration zu Windows 10
description: Windows 10 Medien und Windows 10 verfügen wie ihr Vorgänger Windows 8.1 über keine Grafiktreiber von Drittanbietern im Windows Media Kit oder "In Box".
ms.assetid: E6240CF0-5A65-4A66-98AE-856C783EB320
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b1703210318f55dad3e50f4dcdd7e143434275b7ef3b41203f41792262a53e5a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119882710"
---
# <a name="graphics-driver-migration-to-windows-10"></a>Grafiktreibermigration zu Windows 10

Windows 10 Medien und Windows 10 verfügen wie ihr Vorgänger Windows 8.1 über keine Grafiktreiber von Drittanbietern im Windows Media Kit oder "In Box". Stattdessen werden die Grafiktreiber für eine vielzahl von Geräten auf WU bereitgestellt, wodurch Hardwarehersteller Treiber aktualisieren können, ohne dass eine Änderung des Betriebssystemimages erforderlich ist. Darüber hinaus werden vorhandene Treiber während eines Betriebssystemupgrades von Windows 10 Windows Windows 10 7, Windows 8 oder Windows 8.1. Dies wirkt sich auch auf Upgrades von Windows Server 2012.

## <a name="upgrades-and-installation"></a>Upgrades und Installation

Für Upgrades und neue Installationen müssen die Grafiktreiber von Windows Update (WU) oder der IHV/OEM-Website für die relevante Hardware erhalten werden. Dies erfordert eine Internetverbindung. Die Treiber auf WU werden durch dynamisches Update (Dynamic Update, DU) in das Betriebssystemsetup eingefügt, wenn ein Benutzer ein Upgrade des Windows 7- oder Windows 8.x-Systems auf Windows 10.

> [!Note]  
> Dies gilt nicht für Systeme, Windows vorinstalliert sind, z. B. in einem Einzelhandelsgeschäft erworbene Standardcomputer. Auf diesen Systemen sind die Grafiktreiber bereits vom OEM installiert. Der OEM kann auch eine DVD (für die Neuinstallierung des Betriebssystems) mit den Treibern liefern.

 

Nach dem Upgrade auf Windows 10 können Benutzer feststellen, dass auf ihrem PC keine Grafiktreiber installiert sind. Dies kann folgende Ursachen haben:

-   Der Benutzer hat eine neu installierte Installation vorgenommen, d. h. kein Upgrade.
-   Der Benutzer hat die Option zum Suchen nach Updates während des Upgrades deaktiviert, d. h. das dynamische Update (Dynamic Update, DU) wurde effektiv deaktiviert.
-   Die Internetverbindung funktionierte während des Upgrades nicht.
-   Fehler bei der Treiberinstallation.

Nach einer bereinigten Installation des Betriebssystems sind keine Grafiktreiber auf dem PC vorhanden, bis der WU-Client automatisch ausgeführt wird und die entsprechenden Treiber herunterlädt. In der Zwischenzeit wird auf dem PC der Microsoft Basic Display Adapter (MSBDA) ausgeführt, der über eingeschränkte Funktionen verfügt, z. B. keine Unterstützung für mehrere Monitore, und der Benutzer kann im Vergleich zu einem Hardwaretreiber auch eine schlechte Leistung haben, z. B. langsame Bildfrequenz oder Tränkung bei der Videowiedergabe.

## <a name="manifestations"></a>Manifestationen

Bei älteren PCs (in der Regel vor Windows 7 erstellt) ist es möglich, dass keine Treiber für Windows 10 auf WU installiert sind, da die Grafikkarten das Ende der Lebensdauer (End-Of-Life, EOL) erreicht haben und von den Hardwareanbietern nicht mehr unterstützt werden. Selbst Systeme, auf denen Windows 7 oder 8.x ausgeführt wird, wurden möglicherweise von einem früheren Betriebssystem aktualisiert und verfügen möglicherweise über EOL-Grafikkarten.

Neuere PCs verfügen möglicherweise nicht über Treiber, da die Grafikkarte von einem älteren Computer übertragen wurde, z. B. während eines Hardwareupgrades. Dies geschieht am häufigsten bei Computern mit mehreren Grafikkarten, bei denen der Benutzer beim Kauf eines neuen Computers eine alte Grafikkarte aufbewahrt hat, um mehrere Anzeigen zu verwenden.

Eine weitere Möglichkeit für einen kleinen Prozentsatz der Computer ist, dass Windows Update nur "Abdeckungstreiber" hat. Hierbei handelt es sich um generische Treiber ohne OEM-Anpassungen. Ein Benutzer, der nach dem Upgrade auf Windows 10 einen dieser Treiber geliefert hat, kann erkennen, dass einige Funktionen fehlen, z. B. Funktionstasten zum Steuern der Bildschirmhelligkeit funktionieren nicht mehr.

## <a name="mitigations"></a>Gegenmaßnahmen

-   Geeignete Grafiktreiber sollten entweder vom DU während des Upgradevorgangs oder von WU kurz nach Abschluss des Upgrades bereitgestellt werden. OEMs müssen sicherstellen, dass die entsprechenden Grafiktreiber in den Systemabbildern enthalten sind, die für die Factoryinstallation von Windows 10 auf ihren Computern verwendet werden.
-   Nach einem Upgrade kann der Benutzer das Update für Treiber Einstellungen Windows, obwohl dies \\ nicht erforderlich sein sollte. Benutzer, die eine Überprüfung erzwingen, während ein Treiber automatisch im Hintergrund installiert wird, sehen möglicherweise einen Treiberinstallationsfehler, wenn die automatische Installation zuerst abgeschlossen wird. Sie können diese Warnmeldung ignorieren.
-   Benutzer, die eine Bereinigung von Windows 10 planen, sollten die relevanten Treiber vor der Installation abrufen oder sich auf Windows Update verlassen, um die Treiber später zur Verfügung zu stellen. In diesem Fall müssen sie sicherstellen, dass ihre Internetverbindung funktioniert.
-   Für Computer, die einen Abdeckungstreiber erhalten, gibt es keine Entschärfung für fehlende Funktionalität. Dies sollte jedoch nur in Fällen geschehen, in denen der Hardwareanbieter die Treiber nicht mehr verwaltet, d. h. Computer, die mehrere Jahre alt sind.

> [!Note]  
> Bei Systemen mit einem einzelnen Display, z. B. einem Laptop, stellen viele Benutzer fest, dass MSBDA akzeptabel ist, und bemerken das Fehlen eines Hardwaretreibers nicht. In diesem Fall ist keine Entschärfung erforderlich.

 

## <a name="solutions"></a>Lösungen

Es ist wichtig, dass IHVs und OEMs ihre Windows 10-Grafiktreiber für jede Hardware, die sie unterstützen möchten, in WU hochladen.

Benutzer sollten beim Upgrade die Option "Nach Updates suchen" (Standardeinstellung) ausgewählt lassen. Abhängig von der Geschwindigkeit der Netzwerkverbindung und der Last auf den WU-Servern kann dies bedeuten, dass die Treiber erst installiert werden, nachdem OOBE abgeschlossen wurde und sich der Benutzer zum ersten Mal angemeldet hat. In der Zwischenzeit kann es sein, dass dem Benutzer einige eingeschränkte Funktionen oder eine schlechte Leistung aufgefallen sind.

Benutzer müssen sicherstellen, dass ihre Internetverbindung funktioniert, bevor sie ein Upgrade starten, auch wenn sie ein Upgrade mithilfe von Medien (DVD oder Flashlaufwerk) durchführen.

-   Wenn der PC mit dem Internet verbunden ist, sollten die entsprechenden Treiber automatisch heruntergeladen und installiert werden. Der Benutzer muss keine Maßnahmen ergreifen.
-   Wenn der PC nicht mit dem Internet verbunden ist, müssen die Treiber über einen Computer mit Internetverbindung von der IHV- oder OEM-Website heruntergeladen werden. wird mithilfe eines Flashlaufwerks oder einer CD/DVD auf den Zielcomputer übertragen. und werden dann manuell installiert.

 

 




