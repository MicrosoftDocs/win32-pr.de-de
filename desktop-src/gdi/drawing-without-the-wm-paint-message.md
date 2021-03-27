---
description: Obwohl Anwendungen die meisten Zeichnungsvorgänge ausführen, während die WM-Zeichnungs \_ Nachricht verarbeitet wird, ist es manchmal effizienter, wenn eine Anwendung direkt in einem Fenster gezeichnet wird, ohne auf die WM-Zeichnungs Nachricht zu vertrauen \_ .
ms.assetid: 2d015879-58d2-4cbe-b1cc-445f2e8fd316
title: Zeichnen ohne die WM_PAINT Meldung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66695e85b700de6f62366dedb6fe082f410d4385
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863647"
---
# <a name="drawing-without-the-wm_paint-message"></a>Zeichnen ohne die WM-Zeichnungs \_ Nachricht

Obwohl Anwendungen die meisten Zeichnungsvorgänge ausführen, während [**die \_ WM**](wm-paint.md) -Zeichnungs Nachricht verarbeitet wird, ist es manchmal effizienter, wenn eine Anwendung direkt in einem Fenster gezeichnet wird, ohne auf die WM-Zeichnungs Nachricht zu vertrauen. **\_** Dies kann hilfreich sein, wenn der Benutzer sofortiges Feedback benötigt, z. b. beim Auswählen von Text und ziehen oder Anpassen eines Objekts. In solchen Fällen zeichnet die Anwendung normalerweise bei der Verarbeitung von Tastatur-oder Maus Nachrichten.

Um in einem Fenster zu zeichnen, ohne eine [**WM \_ Paint**](wm-paint.md) -Meldung zu verwenden, verwendet die Anwendung die [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) -Funktion oder die [**getdcex**](/windows/desktop/api/Winuser/nf-winuser-getdcex) -Funktion, um einen Anzeigegeräte Kontext für das Fenster abzurufen. Beim Anzeigen des Geräte Kontexts kann die Anwendung im Fenster zeichnen und das Eindringen in andere Fenster vermeiden. Nachdem die Anwendung das Zeichnen abgeschlossen hat, ruft Sie die [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) -Funktion auf, um den Anzeigegeräte Kontext zur Verwendung durch andere Anwendungen freizugeben.

Wenn Sie ohne eine [**WM \_ Paint**](wm-paint.md) -Meldung zeichnen, wird das Fenster in der Regel nicht für ungültig erklärt. Stattdessen wird es so gezeichnet, dass das Fenster problemlos wieder hergestellt und die Zeichnung entfernt werden kann. Wenn der Benutzer z. b. Text oder ein Objekt auswählt, zeichnet die Anwendung normalerweise die Auswahl, indem Sie alle bereits im Fenster vorhandenen Objekte umkehren. Die Anwendung kann die Auswahl entfernen und den ursprünglichen Inhalt des Fensters wiederherstellen, indem Sie einfach wieder umkehren.

Die Anwendung ist für die sorgfältige Verwaltung von Änderungen zuständig, die Sie an diesem Fenster vornimmt. Insbesondere, wenn eine Anwendung eine Auswahl zeichnet und eine dazwischenliegende WM-Zeichnungs Meldung auftritt, muss die Anwendung sicherstellen, dass jede während der Nachricht durchgeführte Zeichnung die Auswahl nicht beschädigt. [**\_**](wm-paint.md) Um dies zu vermeiden, entfernen viele Anwendungen die Auswahl, führen normale Zeichnungsvorgänge durch und stellen dann die Auswahl wieder her, wenn die Zeichnung vollständig ist.

 

 



