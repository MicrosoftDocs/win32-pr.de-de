---
description: Sie können die WM- \_ Zeichnungs Nachricht verwenden, um die zum Anzeigen von Informationen erforderliche Zeichnung auszuführen.
ms.assetid: cc56745f-95d0-4607-a206-1e7ed7109bf0
title: Verwenden der WM_PAINT Nachricht
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba77246e04effc74de8158aef9bfc4aaf27471c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215646"
---
# <a name="using-the-wm_paint-message"></a>Verwenden der WM-Zeichnungs \_ Meldung

Sie können die [**WM- \_**](wm-paint.md) Zeichnungs Nachricht verwenden, um die zum Anzeigen von Informationen erforderliche Zeichnung auszuführen. Da das System WM- \_ Paint-Meldungen an Ihre Anwendung sendet, wenn Ihr Fenster aktualisiert werden muss oder wenn Sie explizit ein Update anfordern, können Sie den Code zum Zeichnen in der Fenster Prozedur Ihrer Anwendung konsolidieren. Sie können diesen Code dann immer dann verwenden, wenn Ihre Anwendung entweder neue oder vorhandene Informationen zeichnen muss.

In den folgenden Abschnitten werden verschiedene Möglichkeiten zum Verwenden der WM- \_ Zeichnungs Nachricht zum Zeichnen in einem Fenster gezeigt:

-   [Zeichnen im Client Bereich](drawing-in-the-client-area.md)
-   [Neuzeichnen des gesamten Client Bereichs](redrawing-the-entire-client-area.md)
-   [Neuzeichnen in der Aktualisierungs Region](redrawing-in-the-update-region.md)
-   [Der Client Bereich wird ungültig gemacht.](invalidating-the-client-area.md)
-   [Zeichnen eines minimierten Fensters](drawing-a-minimized-window.md)
-   [Zeichnen eines benutzerdefinierten Fenster Hintergrunds](drawing-a-custom-window-background.md)

 

 



