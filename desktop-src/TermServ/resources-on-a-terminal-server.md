---
title: Ressourcen auf einem Remotedesktop-Sitzungshost Server
description: Mehrere Benutzer können sich gleichzeitig bei einem einzelnen Remotedesktop-Sitzungshost -Server (RD-Sitzungshost) anmelden, wobei die Hardware- und Softwareressourcen des Servers gemeinsam verwendet werden.
ms.assetid: ab193a9f-7424-42bf-8cea-28628096edc6
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46ba87ea7569b8ef9daeccb54890bb8882d423621b414fdd8df28c0c4e67b750
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120009190"
---
# <a name="resources-on-a-remote-desktop-session-host-server"></a>Ressourcen auf einem Remotedesktop-Sitzungshost Server

In einer Remotedesktopdienste-Umgebung können sich mehrere Benutzer gleichzeitig bei einem einzelnen Remotedesktop-Sitzungshost -Server (RD-Sitzungshost) anmelden (früher als Terminalserver bezeichnet). Folglich teilen sich die Benutzer die Hardware- und Softwareressourcen des Servers, wodurch die folgenden Bereiche von Inhalten entstehen können:

-   CPU-Zeit. Jeder Benutzer verfügt über eine Desktopumgebung und kann alle anwendungen ausführen, die für diesen Desktop verfügbar sind. Alle Anwendungen, die von allen Benutzern ausgeführt werden, ringen jedoch um die zentralen CPU-Ressourcen, die auf dem RD-Sitzungshost-Server verfügbar sind. Wenn ein Benutzer eine schlecht geschriebene, CPU-intensive Anwendung ausführt, kann es bei anderen Benutzern zu einem sichtbaren Leistungsverlust kommen.
-   Datenträgerzugriff. Benutzer ringen um den Zugriff auf Anwendungen und zugehörige Programmdateien. Darüber hinaus ringen Benutzer um Datenträgerzugriffe durch das Serverbetriebssystem, z. B. das Laden von DLLs oder das Austauschen des Arbeitsspeichers zwischen der Auslagerungsdatei und dem physischen Speicher.
-   Arbeitsspeicher für zufälligen Zugriff (RAM). Jede Anwendung, die von jedem Benutzer ausgeführt wird, ringt um die ram-Ressourcen, die auf dem RD-Sitzungshost-Server verfügbar sind. Wenn ein Benutzer eine speicherintensive Anwendung ausführt, kann es bei anderen Benutzern zu Leistungseinbußen kommen.
-   Netzwerkzugriff. Der Netzwerkzugriff ist in einer Remotedesktopdienste Umgebung unerlässlich, da alle Desktopaktivitäten – grafische Ausgabe und Maus-/Tastatureingabe – über die Netzwerkverbindungen zwischen dem Clientdesktop und dem Server fließen. Darüber hinaus ringen die Anwendungen der Benutzer, die auf dem RD-Sitzungshost Server ausgeführt werden, um den Zugriff auf andere Netzwerkressourcen.
-   Serverhardware. Hardwarekomponenten wie CD-ROMs, Diskettenlaufwerke, serielle Anschlüsse und parallele Ports sind häufig serverbasiert und nicht clientbasiert. Die Gemeinsame Nutzung dieser traditionell nicht freigegebenen Komponenten führt zu neuen Überlegungen für Benutzer und Anwendungen, die auf diese Hardwarekomponenten zugreifen. Weitere Informationen finden Sie unter [Peripheriehardwarerichtlinien.](peripheral-hardware-guidelines.md)
-   Zugriff auf globale Objekte und Ressourcen. In einer Remotedesktopdienste-Umgebung führen Benutzer keine einzelnen Kopien von Windows aus– einige der Kernmodule werden geklont, aber die verbleibenden Module werden von den Benutzern gemeinsam genutzt. Daher konkurrieren Benutzer um den Zugriff auf die Registrierung, die Auslagerungsdatei, Systemdienste und andere globale Objekte und Ressourcen.

Viele der oben genannten Punkte können entschärft werden, indem sie die Größe des RD-Sitzungshost-Servers mit ausreichendEN CPU-, Arbeitsspeicher- und Datenträgerressourcen für die Verarbeitung des Clientbedarfs verringern. Beispielsweise kann eine Konfiguration mit mehreren Prozessoren die CPU-Verfügbarkeit maximieren. Die Speicherverfügbarkeit kann maximiert werden, indem zusätzlicher physischer Arbeitsspeicher installiert wird (die erhöhten Arbeitsspeicherlimits für die Enterprise, Datacenter oder 64-Bit-Editionen von Windows Server können hilfreich sein). Schließlich kann die Leistung des Datenträgerzugriffs maximiert werden, indem mehrere Kanäle konfiguriert und Ihre Betriebssystem- und Anwendungslasten auf verschiedene physische Laufwerke verteilt werden. Die ordnungsgemäße Konfiguration eines RD-Sitzungshost Servers ist ein wichtiges Element der wahrgenommenen Anwendungsleistung.

Obwohl die Hardware dimensionierung ein wichtiger Bestandteil der Erstellung einer skalierbaren Remotedesktopdienste Umgebung ist, sind die Überlegungen zur Software ebenso wichtig. Tatsächlich kann die Feinabstimmung einer Anwendung häufig viel tun, um den Ressourcenkonkurrenz zu verringern und die wahrgenommene Anwendungsleistung zu verbessern.

Weitere Informationen zur Remotedesktopdienste-Umgebung finden Sie in den folgenden Themen:

-   [Remotedesktopdienste Programmierrichtlinien](terminal-services-programming-guidelines.md)
-   [Erkennen der Remotedesktopdienste-Umgebung](detecting-the-terminal-services-environment.md)
-   [Ermitteln, ob die Remotedesktopdienste-Rolle installiert ist](detecting-whether-terminal-services-is-installed.md)
-   [Remotedesktopdienste Sitzungen](terminal-services-sessions.md)

 

 




