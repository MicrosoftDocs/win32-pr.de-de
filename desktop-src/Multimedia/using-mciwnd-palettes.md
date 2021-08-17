---
title: Verwenden von MCIWnd-Paletten
description: Verwenden von MCIWnd-Paletten
ms.assetid: 2b99ca57-f321-4286-8ebf-ae3344d8d2c9
keywords:
- MCIWndGetPalette-Makro
- MCIWndSetPalette-Makro
- MCIWndRealize-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 074dece2c1dac95e24a465413cae686acea5a8e9055913bfb832341efdb12c1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117801119"
---
# <a name="using-mciwnd-palettes"></a>Verwenden von MCIWnd-Paletten

Zum Wiedergeben von Videoclips mit 8-Bit-Farbtiefe (256 Farbkapazität) ist eine Palette erforderlich, um die verwendeten Farben zu definieren. Manchmal ist die in einem Videoclip enthaltene Palette nicht die am besten geeignete Palette für die Wiedergabe. In diesem Fall bietet MCIWnd drei Möglichkeiten zum Verwalten von Paletten für die Wiedergabe:

-   Rufen Sie mithilfe des [**MCIWndGetPalette-Makros**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpalette) ein Handle für die Palette ab, die einem MCIWnd-Fenster zugeordnet ist. Die Palette ist nicht unbedingt ausschließlich dem MCIWnd-Fenster zugeordnet. Andere Anwendungen können auf das Palettenhandle zugreifen und es sogar für ungültig erklären. Daher sollte Ihre Anwendung die globale Verwendung der Palette antizipieren und nach Abschluss der Palette nicht freigeben.
-   Geben Sie mithilfe des [**MCIWndSetPalette-Makros**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetpalette) eine neue Palette an, die mit dem Videoclip verwendet werden soll, der einem MCIWnd-Fenster zugeordnet ist.
-   Erkennen Sie die Palette, die einem MCIWnd-Fenster zugeordnet ist, mithilfe des [**MCIWndRealize-Makros**](/windows/desktop/api/Vfw/nf-vfw-mciwndrealize) der Systempalette. Dieses Makro ruft die [**Funktion RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette) mit der Palette auf, die dem MCIWnd-Fenster zugeordnet ist. Wenn Ihre Anwendungsmeldungshandler für [**WM \_ PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) und [**WM \_ QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) nur **RealizePalette** oder **MCIWndRealize** aufrufen, müssen Sie diese Nachrichten an MCIWnd weiterleiten, wenn Sie sie nicht selbst verarbeiten.

> [!Note]  
> Wenn ein Videoclip mit 8-Bit-Farbtiefe in das MCIWnd-Fenster geladen wird, ersetzt die in diesem Clip enthaltene Palette die Palette, die dem MCIWnd-Fenster zugeordnet ist.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verbesserungen bei der Wiedergabe](playback-enhancements.md)
</dt> </dl>

 

 