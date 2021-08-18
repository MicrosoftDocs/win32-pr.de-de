---
description: Vor dem Zeichnen muss das System das Anzeigegerät für Zeichnungsvorgänge vorbereiten.
ms.assetid: a3802aa7-deec-4151-b1b1-4cd38f769864
title: Anzeigen von Geräten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd71b943d294bf89e932f965b023ecbce7f4e594044fe96b70bb84d41a27f777
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119038118"
---
# <a name="display-devices"></a>Anzeigen von Geräten

Vor dem Zeichnen muss das System das Anzeigegerät für Zeichnungsvorgänge vorbereiten. Ein Anzeigegerätekontext definiert eine Reihe von Grafikobjekten und den zugehörigen Attributen sowie die Grafikmodi, die sich auf die Ausgabe auswirken. Das System bereitet jeden Anzeigegerätekontext für die Ausgabe in einem Fenster vor, wobei die Zeichnungsobjekte, Farben und Modi für das Fenster anstelle des Anzeigegeräts festgelegt werden. Wenn die Anwendung den Anzeigegerätekontext über Aufrufe von GDI-Funktionen angibt, verwendet GDI die Informationen im Kontext, um ausgaben im angegebenen Fenster zu generieren, ohne in andere Fenster oder andere Teile des Bildschirms einzudringen.

Das System stellt fünf Arten von Anzeigegerätekontexten bereit.



| type                                           | Bedeutung                                                                                                                                                          |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [gemeinsam](common-display-device-contexts.md)   | Ermöglicht das Zeichnen im Clientbereich eines angegebenen Fensters.                                                                                                        |
| [class](class-display-device-contexts.md)     | Ermöglicht das Zeichnen im Clientbereich eines angegebenen Fensters.                                                                                                        |
| [parent](parent-display-device-contexts.md)   | Ermöglicht das Zeichnen an einer beliebigen Stelle im Fenster. Obwohl der Kontext des übergeordneten Geräts auch das Zeichnen im übergeordneten Fenster zulässt, ist er auf diese Weise nicht vorgesehen. |
| [private](private-display-device-contexts.md) | Ermöglicht das Zeichnen im Clientbereich eines angegebenen Fensters.                                                                                                        |
| [Fenster](window-display-device-contexts.md)   | Ermöglicht das Zeichnen an einer beliebigen Stelle im Fenster.                                                                                                                          |



 

Das System stellt einen allgemeinen, Klassen-, übergeordneten oder privaten Gerätekontext für ein Fenster basierend auf dem Typ des Anzeigegerätekontexts bereit, der im Klassenstil dieses Fensters angegeben ist. Das System stellt einen Fenstergerätekontext nur dann zur Verfügung, wenn die Anwendung explizit einen anfordert, z. B. durch Aufrufen der [**GetWindowDC-**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc) oder [**GetDCEx-Funktion.**](/windows/desktop/api/Winuser/nf-winuser-getdcex) In allen Fällen kann eine Anwendung die [**WindowFromDC-Funktion**](/windows/desktop/api/Winuser/nf-winuser-windowfromdc) verwenden, um zu bestimmen, welches Fenster ein Anzeigedomänencontroller derzeit darstellt.

Dieser Abschnitt enthält Informationen zu den folgenden Themen.

-   [Anzeigen des Gerätekontextcaches](display-device-context-cache.md)
-   [Anzeigen von Gerätekontextstandardeinstellungen](display-device-context-defaults.md)
-   [Allgemeine Anzeigegerätekontexte](common-display-device-contexts.md)
-   [Private Anzeigegerätekontexte](private-display-device-contexts.md)
-   [Übergeordnete Anzeigegerätekontexte](parent-display-device-contexts.md)
-   [Klassenanzeigegerätekontexte](class-display-device-contexts.md)
-   [Anzeigen von Gerätekontexten im Fenster](window-display-device-contexts.md)
-   [Übergeordnete Anzeigegerätekontexte](parent-display-device-contexts.md)

 

 



