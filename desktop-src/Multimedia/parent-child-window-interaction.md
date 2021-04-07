---
title: Interaktion mit Parent-Child Fenster
description: Interaktion mit Parent-Child Fenster
ms.assetid: de10bf12-4ba4-4c6b-be56-489e4e2b26b1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da43ab5ebe1aa24d8d67b8c901cd3302d8db48ae
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725864"
---
# <a name="parent-child-window-interaction"></a>Interaktion mit Parent-Child Fenster

Einige Meldungen auf Systemebene, z. b. " [**WM \_ palettechanged**](/windows/desktop/gdi/wm-palettechanged) " und " [**WM \_ querynewpalette**](/windows/desktop/gdi/wm-querynewpalette)", werden nur an die Fenster der obersten Ebene und überlappende Fenster gesendet. Wenn ein Erfassungsfenster ein untergeordnetes Fenster ist, muss das übergeordnete Element diese Nachrichten weiterleiten.

Wenn die Größe des übergeordneten Fensters geändert wird, müssen möglicherweise Benachrichtigungs Meldungen an das Aufzeichnungs Fenster gesendet werden. Wenn sich die Dimensionen des aufgezeichneten Videos umgekehrt, muss das Aufzeichnungs Fenster möglicherweise Benachrichtigungs Meldungen an das übergeordnete Fenster senden. Die einfachste Möglichkeit, dies zu verwalten, besteht darin, die Größe des Aufzeichnungs Fensters immer der Größe des aufgezeichneten Videostreams zu überlassen, wobei das übergeordnete Element benachrichtigt wird, wenn sich diese Dimensionen ändern.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erfassungsfenster](capture-windows.md)
</dt> </dl>

 

 