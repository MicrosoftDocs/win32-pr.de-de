---
title: Ressourcen auf einem Remotedesktop-Sitzungshost Server
description: Mehrere Benutzer können sich gleichzeitig bei einem einzelnen Remotedesktop-Sitzungshost (RD-Sitzungshost)-Server anmelden und die Hardware-und Software Ressourcen des Servers freigeben.
ms.assetid: ab193a9f-7424-42bf-8cea-28628096edc6
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81e099787ae3d0acd9028405b244f7fbc2e2117e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711418"
---
# <a name="resources-on-a-remote-desktop-session-host-server"></a>Ressourcen auf einem Remotedesktop-Sitzungshost Server

In einer Remotedesktopdienste Umgebung können sich mehrere Benutzer gleichzeitig bei einem einzelnen Remotedesktop-Sitzungshost (RD-Sitzungshost) (früher als Terminal Server bezeichnet) anmelden. Folglich werden die Hardware-und Software Ressourcen des Servers von den Benutzern gemeinsam genutzt, wodurch die folgenden Bereiche von Konflikten erstellt werden können:

-   CPU-Zeit. Jeder Benutzer verfügt über eine Desktopumgebung und kann alle Anwendungen ausführen, die für diesen Desktop verfügbar sind. Alle Anwendungen, die von allen Benutzern ausgeführt werden, sind jedoch für die zentralen CPU-Ressourcen, die auf dem RD-Sitzungshost Server verfügbar sind, in Konflikt. Wenn ein Benutzer eine schlecht geschriebene, CPU-intensive Anwendung ausführt, können andere Benutzer einen sichtbaren Leistungsverlust erleben.
-   Datenträger Zugriff. Benutzer haben Zugriff auf Anwendungen und zugehörige Programmdateien. Außerdem stellen die Benutzer einen Datenträger Zugriff durch das Server Betriebssystem her, z. b. das Laden von DLLs oder das Austauschen von Speicher zwischen der Auslagerungs Datei und dem physischen Speicher.
-   Arbeitsspeicher (Random Access Memory, RAM). Jede Anwendung, die von jedem Benutzer ausgeführt wird, ist ein Konflikt zwischen den RAM-Ressourcen, die auf dem RD-Sitzungshost Server verfügbar sind. Wenn ein Benutzer eine Arbeitsspeicher intensive Anwendung ausführt, treten bei anderen Benutzern möglicherweise Leistungseinbußen auf.
-   Netzwerkzugriff. Der Netzwerk Zugriff ist in einer Remotedesktopdienste Umgebung unverzichtbar, da alle Desktop Aktivitäten – grafische Ausgabe und Maus-/Tastatur Eingaben – über die Netzwerkverbindungen zwischen dem Client Desktop und dem Server fließen. Außerdem haben die Anwendungen der Benutzer, die auf dem RD-Sitzungshost-Server ausgeführt werden, Zugriff auf andere Netzwerkressourcen.
-   Server Hardware. Hardware Komponenten wie z. b. CD-ROMs, Diskettenlaufwerke, serielle Anschlüsse und parallele Ports sind häufig Server basiert, nicht Client basiert. Wenn Sie diese herkömmlichen, nicht freigegebenen Komponenten freigeben, werden Benutzer und Anwendungen, die auf diese Hardwarekomponenten zugreifen, neu Überlegungen erstellt. Weitere Informationen finden Sie unter [Richtlinien für die Peripherie Hardware](peripheral-hardware-guidelines.md).
-   Zugriff auf globale Objekte und Ressourcen. In einer Remotedesktopdienste Umgebung führen Benutzer keine einzelnen Kopien von Windows aus – einige der Kernmodule werden geklont, aber die restlichen Module werden von den Benutzern gemeinsam genutzt. Folglich konkurrieren Benutzer um den Zugriff auf die Registrierung, die Auslagerungs Datei, die Systemdienste und andere globale Objekte und Ressourcen.

Viele der vorangehenden Konflikte können verringert werden, indem der RD-Sitzungshost Server mit ausreichenden CPU-, Arbeitsspeicher-und Datenträger Ressourcen für die Client Nachfrage angepasst wird. Beispielsweise kann die CPU-Verfügbarkeit durch eine Konfiguration mit mehreren Prozessoren maximiert werden. Die Speicherverfügbarkeit kann maximiert werden, indem zusätzlicher physischer Arbeitsspeicher installiert wird (die zunehmenden Arbeitsspeicher Grenzwerte für die Enterprise-, Datacenter-oder 64-Bit-Editionen von Windows Server können dabei helfen). Schließlich kann die Leistung des Datenträger Zugriffs maximiert werden, indem mehrere Kanäle konfiguriert werden und das Betriebssystem und die Anwendungs Last auf verschiedene physische Laufwerke verteilt werden. Eine ordnungsgemäße Konfiguration eines RD-Sitzungshost Servers ist ein wichtiges Element der wahrgenommenen Anwendungsleistung.

Obwohl die Hardware Größe ein wichtiger Bestandteil der Erstellung einer skalierbaren Remotedesktopdienste Umgebung ist, sind die Überlegungen zur Software ebenso wichtig. Tatsächlich kann eine Feinabstimmung einer Anwendung häufig viel bewirken, den ressourcenwettbewerb zu reduzieren und die Leistung der erkannten Anwendungen zu verbessern.

Weitere Informationen zur Remotedesktopdienste-Umgebung finden Sie in den folgenden Themen:

-   [Programmier Richtlinien für Remotedesktopdienste](terminal-services-programming-guidelines.md)
-   [Erkennen der Remotedesktopdienste Umgebung](detecting-the-terminal-services-environment.md)
-   [Erkennen, ob die Remotedesktopdienste Rolle installiert ist](detecting-whether-terminal-services-is-installed.md)
-   [Remotedesktopdienste Sitzungen](terminal-services-sessions.md)

 

 




