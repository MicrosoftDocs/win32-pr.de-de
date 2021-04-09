---
title: Verwenden von mciwnd-Paletten
description: Verwenden von mciwnd-Paletten
ms.assetid: 2b99ca57-f321-4286-8ebf-ae3344d8d2c9
keywords:
- Mciwndgetpalette-Makro
- Mciwndsetpalette-Makro
- Mciwndrealize-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d970e0e33c9dd03c7f1133576f371b713f7174df
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948709"
---
# <a name="using-mciwnd-palettes"></a>Verwenden von mciwnd-Paletten

Die Wiedergabe von Videoclips mit 8-Bit-Farbtiefe (256-Color-Kapazität) erfordert eine Palette, um die verwendeten Farben zu definieren. Manchmal ist die Palette, die in einem Video Clip enthalten ist, nicht die geeignetste Palette, die während der Wiedergabe verwendet werden kann. In diesem Fall bietet mciwnd drei Möglichkeiten zum Verwalten von Paletten für die Wiedergabe:

-   Rufen Sie ein Handle für die Palette ab, die einem mciwnd-Fenster zugeordnet ist, indem Sie das [**mciwndgetpalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpalette) -Makro verwenden. Die Palette ist nicht notwendigerweise ausschließlich dem mciwnd-Fenster zugeordnet. Andere Anwendungen können den Palettenhandle aufrufen und sogar für ungültig erklären. Folglich sollte Ihre Anwendung die globale Verwendung der Palette vorhersehen und sollte Sie, wenn Sie mit der Palette fertig ist, nicht freigeben.
-   Geben Sie eine neue Palette an, die mit dem Video Clip verwendet werden soll, der einem mciwnd-Fenster zugeordnet ist, indem Sie das [**mciwndsetpalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetpalette) -Makro verwenden
-   Erkennen Sie die Palette, die einem mciwnd-Fenster zugeordnet ist, mit der Systempalette, indem Sie das [**mciwndrealize**](/windows/desktop/api/Vfw/nf-vfw-mciwndrealize) -Makro verwenden. Dieses Makro ruft die [**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette) -Funktion mit der Palette auf, die dem mciwnd-Fenster zugeordnet ist. Wenn Ihre Anwendungs Nachrichten Handler für [**WM \_ palettechanged**](/windows/desktop/gdi/wm-palettechanged) und [**WM \_ querynewpalette**](/windows/desktop/gdi/wm-querynewpalette) nur **RealizePalette** oder **mciwndrealize** aufzurufen, müssen Sie diese Nachrichten an mciwnd weiterleiten, wenn Sie Sie nicht selbst behandeln.

> [!Note]  
> Wenn ein Videoclip mit 8-Bit-Farbtiefe in das mciwnd-Fenster geladen wird, ersetzt die in diesem Clip enthaltene Palette die Palette, die dem mciwnd-Fenster zugeordnet ist.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Wiedergabe Verbesserungen](playback-enhancements.md)
</dt> </dl>

 

 