---
description: Der Benutzer Computer hat möglicherweise Zugriff auf mehrere Geräte, die vom Benutzer ausgewählt und zur Durchführung interaktiver sprach Konversationen verwendet werden.
ms.assetid: cc7ad70a-157e-4db4-b5e4-00d25686a9dd
title: Festlegen eines Terminals für Telefon Konversationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75b12e772d8f941cb7c68e25136a843ec5f9a1f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350157"
---
# <a name="setting-a-terminal-for-phone-conversations"></a>Festlegen eines Terminals für Telefon Konversationen

Der Computer des Benutzers hat möglicherweise Zugriff auf mehrere Geräte, die vom Benutzer ausgewählt und zur Durchführung interaktiver sprach Konversationen verwendet werden. Zuerst ist das Telefongerät selbst mit den Lampen, den Schaltflächen, der Anzeige, dem ruftgerät und dem sprach-e/a-Gerät (Handy, Speakerphone, Headset) ausgestattet. Der Computer des Benutzers kann auch ein separates sprach-e/a-Gerät (z. b. ein Headset oder eine Mikrofon-/Sprecher-Kombination, das mit einer Soundkarte verbunden ist) für die Verwendung mit Telefon Konversationen haben

Mithilfe von TSPI kann der Benutzer auswählen, wohin die vom Switch gesendeten Informationen über die Zeile, die Adresse oder den Rückruf weitergeleitet werden sollen. Der Switch erwartet normalerweise, dass dies einer der Telefon Sätze ist, und sendet Ring Anforderungen, Lamp-Ereignisse (für Impuls Telefone), Anzeigedaten und sprach Daten nach Bedarf. Das Telefon sendet wiederum die Ereignisse "huokswitch", "Button Press-Ereignisse" (für "Impuls Telefone") und "Sprach Daten" zurück zum Switch.

Der *linienteil* von TSPI stellt Lamp-Ereignisse, Anzeige Ereignisse und Ring Ereignisse zur Verfügung, entweder als funktionale Rückgabecodes für die verschiedenen Zeilen Vorgänge in TSPI oder als nicht angeforderte Funktions Aufrufstatus Meldungen, die an den Anwendungs Rückruf gesendet werden. Die Dienstanbieter Implementierung ist für die Zuordnung zwischen der funktionalen TSPI-Ebene und den zugrunde liegenden oder funktionalen Nachrichten zuständig, die vom Telefonienetzwerk verwendet werden. In funktionalen Telefonieumgebungen werden TSPI-Funktionen dem funktionalen Protokoll zugeordnet.

Mithilfe der [**TSPI \_ linesetterminal**](/windows/win32/api/tspi/nf-tspi-tspi_linesetterminal) -Funktion kann TAPI das Routing von unterschiedlichen Ereignissen auf niedriger Ebene steuern, die zwischen dem Switch und der Station ausgetauscht werden. es kann auch festlegen, dass einige dieser Ereignisse auf niedriger Ebene nicht an ein Gerät weitergeleitet werden. Das Routing der verschiedenen Ereignis Klassen kann einzeln gesteuert werden. Beispielsweise kann der Mediendaten Strom eines Aufrufes (z. b. Voice) an ein beliebiges Übertragungs Gerät gesendet werden, wenn der Dienstanbieter und die Hardware dies tun können. Ring Ereignisse von der Umstellung auf das Telefon können einer visuellen Warnung auf dem Computerbildschirm zugeordnet werden, oder Sie können zu einem Telefongerät weitergeleitet werden. Lamp-Ereignisse und Anzeige Ereignisse können ignoriert oder an ein Telefongerät weitergeleitet werden (was sich als normales Telefon Satz verhält). Zum Schluss kann es sein, dass Schaltflächen auf einem Telefongerät an die Zeile weitergegeben werden. In jedem Fall wirkt sich dieses Routing von Signalen auf niedriger Ebene von der Zeile nicht auf die Ausführung des TSPI-Zeilen Teils aus, der immer die Low-Level-Ereignisse der funktionalen Entsprechung zuordnet. Anwendungen können sich die Gerätefunktionen einer Zeile ansehen, um die verfügbaren Terminals zu ermitteln.

Mit anderen Worten: die [**TSPI \_ linesetterminal**](/windows/win32/api/tspi/nf-tspi-tspi_linesetterminal) -Funktion gibt das Terminal Gerät an, an das die angegebene Zeile, die Adress Ereignisse oder die Ereignisse des aufrufungsmedienstreams weitergeleitet werden. Separate Terminals können für jede Ereignisklasse angegeben werden. Zu den Ereignis Klassen zählen Lampen, Schaltflächen, Anzeige, stumm, anokswitch und Mediendaten Strom.

 

 
