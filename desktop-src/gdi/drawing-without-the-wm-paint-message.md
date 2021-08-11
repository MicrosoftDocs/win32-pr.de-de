---
description: Obwohl Anwendungen die meisten Zeichnungsvorgänge durchführen, während die WM PAINT-Nachricht verarbeitet wird, ist es manchmal effizienter, dass eine Anwendung direkt in einem Fenster zeichnet, ohne sich auf die \_ WM \_ PAINT-Nachricht verlassen zu müssen.
ms.assetid: 2d015879-58d2-4cbe-b1cc-445f2e8fd316
title: Zeichnen ohne WM_PAINT Nachricht
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36ff9a18e923feceb33f961c9427852b2c2daddfcfc4e093809e24cd42f32869
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118250339"
---
# <a name="drawing-without-the-wm_paint-message"></a>Zeichnen ohne DIE WM \_ PAINT-Nachricht

Obwohl Anwendungen die meisten Zeichnungsvorgänge durchführen, während die [**WM \_ PAINT-Nachricht**](wm-paint.md) verarbeitet wird, ist es manchmal effizienter, dass eine Anwendung direkt in einem Fenster zeichnet, ohne sich auf die **WM \_ PAINT-Nachricht verlassen zu** müssen. Dies kann nützlich sein, wenn der Benutzer sofortiges Feedback benötigt, z. B. beim Auswählen von Text und Ziehen oder Anpassen der Größe eines Objekts. In solchen Fällen zeichnet die Anwendung normalerweise während der Verarbeitung von Tastatur- oder Mausnachrichten.

Um in einem Fenster ohne [**WM \_ PAINT-Nachricht**](wm-paint.md) zu zeichnen, verwendet die Anwendung die [**GetDC-**](/windows/desktop/api/Winuser/nf-winuser-getdc) oder [**GetDCEx-Funktion,**](/windows/desktop/api/Winuser/nf-winuser-getdcex) um einen Anzeigegerätekontext für das Fenster abzurufen. Mit dem Anzeigegerätekontext kann die Anwendung im Fenster zeichnen und ein Eindringling in andere Fenster vermeiden. Wenn die Anwendung das Zeichnen abgeschlossen hat, ruft sie die [**ReleaseDC-Funktion**](/windows/desktop/api/Winuser/nf-winuser-releasedc) auf, um den Anzeigegerätekontext für die Verwendung durch andere Anwendungen frei zu geben.

Beim Zeichnen ohne VERWENDUNG einer [**WM \_ PAINT-Nachricht**](wm-paint.md) macht die Anwendung das Fenster in der Regel nicht ungültig. Stattdessen zeichnet es so, dass es das Fenster problemlos wiederherstellen und die Zeichnung entfernen kann. Wenn der Benutzer z. B. Text oder ein Objekt auswählt, zeichnet die Anwendung die Auswahl in der Regel, indem sie das zurückzieht, was sich bereits im Fenster befindet. Die Anwendung kann die Auswahl entfernen und den ursprünglichen Inhalt des Fensters wiederherstellen, indem sie einfach erneut zurückkehrt.

Die Anwendung ist für die sorgfältige Verwaltung von Änderungen am Fenster verantwortlich. Insbesondere wenn eine Anwendung eine Auswahl zeichnet und eine intervening [**WM \_ PAINT-Meldung**](wm-paint.md) auftritt, muss die Anwendung sicherstellen, dass jede während der Nachricht durchgeführte Zeichnung die Auswahl nicht beschädigt. Um dies zu vermeiden, entfernen viele Anwendungen die Auswahl, führen übliche Zeichnungsvorgänge aus und stellen die Auswahl dann wieder wieder auf, wenn das Zeichnen abgeschlossen ist.

 

 



