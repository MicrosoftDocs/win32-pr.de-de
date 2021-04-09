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
# <a name="using-mciwnd-palettes"></a><span data-ttu-id="0f89e-106">Verwenden von mciwnd-Paletten</span><span class="sxs-lookup"><span data-stu-id="0f89e-106">Using MCIWnd Palettes</span></span>

<span data-ttu-id="0f89e-107">Die Wiedergabe von Videoclips mit 8-Bit-Farbtiefe (256-Color-Kapazität) erfordert eine Palette, um die verwendeten Farben zu definieren.</span><span class="sxs-lookup"><span data-stu-id="0f89e-107">Playing video clips with 8-bit color depth (256-color capacity) requires a palette to define the colors being used.</span></span> <span data-ttu-id="0f89e-108">Manchmal ist die Palette, die in einem Video Clip enthalten ist, nicht die geeignetste Palette, die während der Wiedergabe verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="0f89e-108">Sometimes, the palette included with a video clip is not the most appropriate palette to use during playback.</span></span> <span data-ttu-id="0f89e-109">In diesem Fall bietet mciwnd drei Möglichkeiten zum Verwalten von Paletten für die Wiedergabe:</span><span class="sxs-lookup"><span data-stu-id="0f89e-109">In this case, MCIWnd provides three ways to manage palettes for playback:</span></span>

-   <span data-ttu-id="0f89e-110">Rufen Sie ein Handle für die Palette ab, die einem mciwnd-Fenster zugeordnet ist, indem Sie das [**mciwndgetpalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpalette) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="0f89e-110">Retrieve a handle to the palette associated with an MCIWnd window by using the [**MCIWndGetPalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpalette) macro.</span></span> <span data-ttu-id="0f89e-111">Die Palette ist nicht notwendigerweise ausschließlich dem mciwnd-Fenster zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="0f89e-111">The palette is not necessarily associated exclusively with the MCIWnd window.</span></span> <span data-ttu-id="0f89e-112">Andere Anwendungen können den Palettenhandle aufrufen und sogar für ungültig erklären.</span><span class="sxs-lookup"><span data-stu-id="0f89e-112">Other applications can access, and even invalidate, the palette handle.</span></span> <span data-ttu-id="0f89e-113">Folglich sollte Ihre Anwendung die globale Verwendung der Palette vorhersehen und sollte Sie, wenn Sie mit der Palette fertig ist, nicht freigeben.</span><span class="sxs-lookup"><span data-stu-id="0f89e-113">Consequently, your application should anticipate the global use of the palette and, when finished with the palette, should not free it.</span></span>
-   <span data-ttu-id="0f89e-114">Geben Sie eine neue Palette an, die mit dem Video Clip verwendet werden soll, der einem mciwnd-Fenster zugeordnet ist, indem Sie das [**mciwndsetpalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetpalette) -Makro verwenden</span><span class="sxs-lookup"><span data-stu-id="0f89e-114">Specify a new palette to use with the video clip associated with an MCIWnd window by using the [**MCIWndSetPalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetpalette) macro.</span></span>
-   <span data-ttu-id="0f89e-115">Erkennen Sie die Palette, die einem mciwnd-Fenster zugeordnet ist, mit der Systempalette, indem Sie das [**mciwndrealize**](/windows/desktop/api/Vfw/nf-vfw-mciwndrealize) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="0f89e-115">Realize the palette associated with an MCIWnd window to the system palette by using the [**MCIWndRealize**](/windows/desktop/api/Vfw/nf-vfw-mciwndrealize) macro.</span></span> <span data-ttu-id="0f89e-116">Dieses Makro ruft die [**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette) -Funktion mit der Palette auf, die dem mciwnd-Fenster zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="0f89e-116">This macro calls the [**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette) function with the palette associated with the MCIWnd window.</span></span> <span data-ttu-id="0f89e-117">Wenn Ihre Anwendungs Nachrichten Handler für [**WM \_ palettechanged**](/windows/desktop/gdi/wm-palettechanged) und [**WM \_ querynewpalette**](/windows/desktop/gdi/wm-querynewpalette) nur **RealizePalette** oder **mciwndrealize** aufzurufen, müssen Sie diese Nachrichten an mciwnd weiterleiten, wenn Sie Sie nicht selbst behandeln.</span><span class="sxs-lookup"><span data-stu-id="0f89e-117">If your application message handlers for [**WM\_PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) and [**WM\_QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) call only **RealizePalette** or **MCIWndRealize**, you must forward these messages to MCIWnd if you do not handle them yourself.</span></span>

> [!Note]  
> <span data-ttu-id="0f89e-118">Wenn ein Videoclip mit 8-Bit-Farbtiefe in das mciwnd-Fenster geladen wird, ersetzt die in diesem Clip enthaltene Palette die Palette, die dem mciwnd-Fenster zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="0f89e-118">When a video clip with 8-bit color depth is loaded into the MCIWnd window, the palette included with that clip replaces the palette associated with the MCIWnd window.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="0f89e-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0f89e-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f89e-120">Wiedergabe Verbesserungen</span><span class="sxs-lookup"><span data-stu-id="0f89e-120">Playback Enhancements</span></span>](playback-enhancements.md)
</dt> </dl>

 

 