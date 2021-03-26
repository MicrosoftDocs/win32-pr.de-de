---
description: Verwenden Sie die GetDC-Funktion, um das Zeichnen auszuführen, das unmittelbar statt bei der Verarbeitung einer WM-Zeichnungs Nachricht ausgeführt werden muss \_ .
ms.assetid: 75525e26-72f5-4a58-a663-0bbdc2034759
title: Verwenden der GetDC-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98c018228eccbce7b487444341481165e24214b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979376"
---
# <a name="using-the-getdc-function"></a>Verwenden der GetDC-Funktion

Verwenden Sie die [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) -Funktion, um das Zeichnen auszuführen, das unmittelbar statt bei der Verarbeitung einer WM-Zeichnungs Nachricht ausgeführt werden muss. [**\_**](wm-paint.md) Diese Zeichnung wird in der Regel als Reaktion auf eine Aktion durch den Benutzer ausgeführt, z. b. das Treffen einer Auswahl oder Zeichnung mit der Maus. In solchen Fällen sollte der Benutzer sofortiges Feedback erhalten und darf nicht gezwungen werden, die Auswahl oder Zeichnung aufzuheben, damit die Anwendung das Ergebnis anzeigt. In den folgenden Abschnitten wird gezeigt, wie Sie GetDC zum Zeichnen in einem Fenster verwenden:

-   [Zeichnen mit der Maus](drawing-with-the-mouse.md)
-   [Zeichnen in zeitgesteuerten Intervallen](drawing-at-timed-intervals.md)

 

 



