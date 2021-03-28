---
description: Vor dem zeichnen muss das System das Anzeigegerät für Zeichnungsvorgänge vorbereiten.
ms.assetid: a3802aa7-deec-4151-b1b1-4cd38f769864
title: Geräte anzeigen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6df9e5e1746f309f402b31e736c58092d134d38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978657"
---
# <a name="display-devices"></a>Geräte anzeigen

Vor dem zeichnen muss das System das Anzeigegerät für Zeichnungsvorgänge vorbereiten. Ein Anzeigegeräte Kontext definiert eine Gruppe von Grafikobjekten und deren zugeordneten Attributen sowie die Grafikmodi, die die Ausgabe beeinflussen. Das System bereitet jeden Anzeigegeräte Kontext für die Ausgabe in einem Fenster vor, wobei die Zeichnungsobjekte, Farben und Modi für das Fenster anstelle des Anzeige Geräts festgelegt werden. Wenn die Anwendung den Anzeigegeräte Kontext über Aufrufe an GDI-Funktionen bereitstellt, verwendet GDI die Informationen im Kontext, um die Ausgabe im angegebenen Fenster zu generieren, ohne in andere Fenster oder andere Teile des Bildschirms einzugreifen.

Das System stellt fünf Arten von Anzeigegeräte Kontexten bereit.



| type                                           | Bedeutung                                                                                                                                                          |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [gewöhnliche](common-display-device-contexts.md)   | Lässt das Zeichnen im Client Bereich eines angegebenen Fensters zu.                                                                                                        |
| [class](class-display-device-contexts.md)     | Lässt das Zeichnen im Client Bereich eines angegebenen Fensters zu.                                                                                                        |
| [parent](parent-display-device-contexts.md)   | Ermöglicht das Zeichnen an beliebiger Stelle im-Fenster. Obwohl der übergeordnete Gerätekontext auch das Zeichnen im übergeordneten Fenster zulässt, ist er nicht für die Verwendung auf diese Weise vorgesehen. |
| [private](private-display-device-contexts.md) | Lässt das Zeichnen im Client Bereich eines angegebenen Fensters zu.                                                                                                        |
| [Fenster](window-display-device-contexts.md)   | Ermöglicht das Zeichnen an beliebiger Stelle im-Fenster.                                                                                                                          |



 

Das System stellt einen allgemeinen, Klassen-, übergeordneten oder privaten Gerätekontext für ein Fenster bereit, das auf dem Typ des Anzeigegeräte Kontexts basiert, der im Klassen Stil dieses Fensters angegeben ist. Das System stellt einen Fenster Gerätekontext nur dann bereit, wenn die Anwendung explizit eine Anforderung anfordert, indem Sie die [**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc) -oder [**getdcex**](/windows/desktop/api/Winuser/nf-winuser-getdcex) -Funktion aufrufen. In allen Fällen kann eine Anwendung die [**windowfromdc**](/windows/desktop/api/Winuser/nf-winuser-windowfromdc) -Funktion verwenden, um zu bestimmen, welches Fenster ein angezeigter DC zurzeit darstellt.

Dieser Abschnitt enthält Informationen zu den folgenden Themen.

-   [Gerätekontext Cache anzeigen](display-device-context-cache.md)
-   [Gerätekontext Standardwerte anzeigen](display-device-context-defaults.md)
-   [Gängige Anzeige von Geräte Kontexten](common-display-device-contexts.md)
-   [Private Anzeigegeräte Kontexte](private-display-device-contexts.md)
-   [Übergeordnete Geräte Kontexte anzeigen](parent-display-device-contexts.md)
-   [Klassen Anzeige von Geräte Kontexten](class-display-device-contexts.md)
-   [Fenster Geräte Kontexte anzeigen](window-display-device-contexts.md)
-   [Übergeordnete Geräte Kontexte anzeigen](parent-display-device-contexts.md)

 

 



