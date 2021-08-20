---
description: Sie können die WM PAINT-Nachricht verwenden, um die zum Anzeigen von Informationen \_ erforderliche Zeichnung zu erstellen.
ms.assetid: cc56745f-95d0-4607-a206-1e7ed7109bf0
title: Verwenden der WM_PAINT Nachricht
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1969d5aae7e64ad74d8070c7515daa6e9e782135ce0af54b49c7faab07f5d34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119037448"
---
# <a name="using-the-wm_paint-message"></a>Verwenden der WM \_ PAINT-Nachricht

Sie können die [**WM \_ PAINT-Nachricht verwenden,**](wm-paint.md) um die zum Anzeigen von Informationen erforderliche Zeichnung zu erstellen. Da das System WM PAINT-Nachrichten an Ihre Anwendung sendet, wenn Das Fenster aktualisiert werden muss oder Wenn Sie explizit eine Aktualisierung anfordern, können Sie den Code zum Zeichnen in der Fensterprozedur Ihrer \_ Anwendung konsolidieren. Sie können diesen Code dann immer dann verwenden, wenn Ihre Anwendung neue oder vorhandene Informationen zeichnen muss.

In den folgenden Abschnitten werden verschiedene Möglichkeiten zum Verwenden der WM PAINT-Nachricht zum \_ Zeichnen in einem Fenster gezeigt:

-   [Zeichnen im Clientbereich](drawing-in-the-client-area.md)
-   [Neudrawing the Entire Client Area (Neuzeichnung des gesamten Clientbereichs)](redrawing-the-entire-client-area.md)
-   [Neuzeichnung im Updatebereich](redrawing-in-the-update-region.md)
-   [Ungültig machen des Clientbereichs](invalidating-the-client-area.md)
-   [Zeichnen eines minimierten Fensters](drawing-a-minimized-window.md)
-   [Zeichnen eines benutzerdefinierten Fensterhintergrunds](drawing-a-custom-window-background.md)

 

 



