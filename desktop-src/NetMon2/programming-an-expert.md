---
description: Das Netzwerkmonitor SDK umfasst die Funktionen und den Beispielcode, die Sie zum Erstellen von Experten benötigen. Sie können jedoch auch vorhandene Tools verwenden, einschließlich eines Dialog-Editors.
ms.assetid: 6a3834b7-753f-42cc-986f-3d7e8bf79fd9
title: Programmieren eines Experten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df633d971558f9b14374680b09a22771e10ea0d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131461"
---
# <a name="programming-an-expert"></a>Programmieren eines Experten

Das Netzwerkmonitor SDK umfasst die Funktionen und den Beispielcode, die Sie zum Erstellen von Experten benötigen. Sie können jedoch auch vorhandene Tools verwenden, einschließlich eines Dialog-Editors.

## <a name="minimum-requirements-to-run-an-expert"></a>Mindestanforderungen für das Ausführen eines Experten

In der folgenden Tabelle sind die DLL-Einstiegspunkte und die Expertenfunktionen aufgelistet, die Sie zum Erstellen eines Experten verwenden müssen.



| Name                                                 | type               | Erforderlich?                                       |
|------------------------------------------------------|--------------------|-------------------------------------------------|
| [**DllMain**](dllmain-expert.md)                    | DLL-Einstiegs Funktion | Ja                                             |
| [**Experte registrieren**](register-expert.md)           | DLL-Einstiegs Funktion | Ja                                             |
| [**Ausführen**](run.md)                                   | DLL-Einstiegs Funktion | Ja                                             |
| [**Konfigurieren**](configure.md)                       | DLL-Einstiegs Funktion | Nur, wenn der Experte die Benutzerkonfiguration bereitstellt. |
| [**Profil Status**](expertindicatestatus.md) | Expertenfunktion    | Ja                                             |
| [**ExpertSubmitEvent**](expertsubmitevent.md)       | Expertenfunktion    | Ja                                             |



 

Sehen Sie sich die Referenz Themen für Experten und Parser im Netzwerkmonitor SDK an, um den Quellcode zu aktualisieren, und verwenden Sie dann den Beispielcode und die in den folgenden Themen aufgeführten Prozeduren:

-   [Entwickeln eines Experten](building-an-expert.md)
-   [Installieren eines Experten](installing-an-expert-to-network-monitor-2-1.md)
-   [Debuggen eines Experten](debugging-an-expert.md)

Experten-DLLs benötigen C, nicht die C++-Aufruf Konvention, da Funktionen über eine Überlagerung durch Funktionszeiger aufgerufen werden. Durch eine Reihe von spezialisierten Expertenfunktionen hat der Experte Zugriff auf die Frames in der Erfassung. Der Experte kann den größten Teil der Netzwerkmonitor-API verwenden, um die zurückgegebenen Daten zu bearbeiten. Wenn ein Experte Informationen findet, die an den Benutzer gesendet werden, werden die Informationen in einer Ereignisdaten Struktur verpackt und an Netzwerkmonitor gesendet, die dann die Informationen in einem expertenausgabe Fenster anzeigt. Der Experte muss Netzwerkmonitor in regelmäßigen Abständen mit Statusinformationen für den Prozentsatz aktualisieren, die von [**der Funktion "**](expertindicatestatus.md) Funktion" von "-Funktion" bereitgestellt werden.

Die exportierten Funktionen des Experten werden wie folgt aufgerufen:

-   Wenn Netzwerkmonitor die Liste der Experten erstellt, die dem Benutzer präsentiert werden sollen, ruft Netzwerkmonitor die [**Register-expertenfunktion**](register-expert.md) auf.
-   Wenn der Experte nach dem Aufruf von " **Register**" konfigurierbar ist, wird Netzwerkmonitor die Funktion " [**configure**](configure.md) " aufrufen.
-   Wenn der Netzwerkmonitor Benutzer auf " **Experte ausführen**" klickt, ruft Netzwerkmonitor die Funktion " [**Run**](run.md) " auf.

Wenn Experten die angeforderten Frames analysieren und ein Problem finden, verwenden Sie " [**ExpertSubmitEvent**](expertsubmitevent.md) ", um ein Ereignis zu senden, das Informationen zum Problem enthält. Netzwerkmonitor verteilt das Ereignis entweder an den standardmäßigen (freigegebenen) Ereignisanzeige oder (sofern der Experte für das Ereignis registriert) für eine private Ereignisanzeige.

 

 



