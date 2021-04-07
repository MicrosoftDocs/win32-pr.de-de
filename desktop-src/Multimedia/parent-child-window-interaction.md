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
# <a name="parent-child-window-interaction"></a><span data-ttu-id="e4e49-103">Interaktion mit Parent-Child Fenster</span><span class="sxs-lookup"><span data-stu-id="e4e49-103">Parent-Child Window Interaction</span></span>

<span data-ttu-id="e4e49-104">Einige Meldungen auf Systemebene, z. b. " [**WM \_ palettechanged**](/windows/desktop/gdi/wm-palettechanged) " und " [**WM \_ querynewpalette**](/windows/desktop/gdi/wm-querynewpalette)", werden nur an die Fenster der obersten Ebene und überlappende Fenster gesendet.</span><span class="sxs-lookup"><span data-stu-id="e4e49-104">Some system-level messages, such as [**WM\_PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) and [**WM\_QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette), are sent only to top-level and overlapped windows.</span></span> <span data-ttu-id="e4e49-105">Wenn ein Erfassungsfenster ein untergeordnetes Fenster ist, muss das übergeordnete Element diese Nachrichten weiterleiten.</span><span class="sxs-lookup"><span data-stu-id="e4e49-105">If a capture window is a child window, its parent must forward these messages.</span></span>

<span data-ttu-id="e4e49-106">Wenn die Größe des übergeordneten Fensters geändert wird, müssen möglicherweise Benachrichtigungs Meldungen an das Aufzeichnungs Fenster gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="e4e49-106">Similarly, if the parent window changes size, it might need to send notification messages to the capture window.</span></span> <span data-ttu-id="e4e49-107">Wenn sich die Dimensionen des aufgezeichneten Videos umgekehrt, muss das Aufzeichnungs Fenster möglicherweise Benachrichtigungs Meldungen an das übergeordnete Fenster senden.</span><span class="sxs-lookup"><span data-stu-id="e4e49-107">Conversely, if the dimensions of the captured video change, the capture window might need to send notification messages to the parent window.</span></span> <span data-ttu-id="e4e49-108">Die einfachste Möglichkeit, dies zu verwalten, besteht darin, die Größe des Aufzeichnungs Fensters immer der Größe des aufgezeichneten Videostreams zu überlassen, wobei das übergeordnete Element benachrichtigt wird, wenn sich diese Dimensionen ändern.</span><span class="sxs-lookup"><span data-stu-id="e4e49-108">The simplest way to manage this is to always keep the capture window dimensions equal to the size of the captured video stream, notifying the parent whenever these dimensions change.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e4e49-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e4e49-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4e49-110">Erfassungsfenster</span><span class="sxs-lookup"><span data-stu-id="e4e49-110">Capture Windows</span></span>](capture-windows.md)
</dt> </dl>

 

 