---
title: Einschränken des Wiedergabe Bereichs
description: Einschränken des Wiedergabe Bereichs
ms.assetid: 080ab96f-1cb5-48d4-ac0a-8fd9ba68a31a
keywords:
- Mciwndplayfrom-Makro
- Mciwndplayto-Makro
- Mciwndplayfromto-Makro
- MCI-Wiedergabe Befehle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 465bcf7a7b6b5811de8413a1c89f7befcf81037f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855875"
---
# <a name="limiting-the-playback-scope"></a><span data-ttu-id="c127c-107">Einschränken des Wiedergabe Bereichs</span><span class="sxs-lookup"><span data-stu-id="c127c-107">Limiting the Playback Scope</span></span>

<span data-ttu-id="c127c-108">Das Steuern der Wiedergabe beginnt mit dem [**mciwndplay**](/windows/desktop/api/Vfw/nf-vfw-mciwndplay) -Makro, das den Inhalt oder die Datei wieder gibt, der mit einem mciwnd-Fenster von der aktuellen Wiedergabe Position bis zum Ende des Inhalts verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="c127c-108">Controlling playback begins with the [**MCIWndPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndplay) macro, which plays the content or file associated with an MCIWnd window from the current playback position to the end of the content.</span></span> <span data-ttu-id="c127c-109">Wenn Sie die Wiedergabe auf einen bestimmten Teil des Inhalts oder der Datei beschränken möchten, können Sie zwischen den anderen Wiedergabe-mciwnd-Makros wählen: [**mciwndplayfrom**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfrom), [**mciwndplayto**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto)und [**mciwndplayfromto**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto).</span><span class="sxs-lookup"><span data-stu-id="c127c-109">If you want to limit playback to a specific portion of the content or file, you can choose from the other playback MCIWnd macros: [**MCIWndPlayFrom**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfrom), [**MCIWndPlayTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto), and [**MCIWndPlayFromTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto).</span></span>

<span data-ttu-id="c127c-110">Außerdem müssen Sie ein geeignetes Zeitformat festlegen.</span><span class="sxs-lookup"><span data-stu-id="c127c-110">You also need to set an appropriate time format.</span></span> <span data-ttu-id="c127c-111">Das Zeitformat bestimmt, ob der Inhalt in Frames, Millisekunden, Spuren oder anderen Einheiten gemessen wird.</span><span class="sxs-lookup"><span data-stu-id="c127c-111">The time format determines whether the content is measured in frames, milliseconds, tracks, or some other units.</span></span>

<span data-ttu-id="c127c-112">Im folgenden Beispiel wird ein mciwnd-Fenster erstellt und Menübefehle bereitstellt, um das letzte Dritte, erste Dritte oder mittlere dritte des Inhalts wiederzugeben.</span><span class="sxs-lookup"><span data-stu-id="c127c-112">The following example creates an MCIWnd window and provides menu commands to play the last third, first third, or middle third of the content.</span></span> <span data-ttu-id="c127c-113">Diese Menübefehle verwenden **mciwndplayfrom**, **mciwndplayto** und **mciwndplayfromto** zum Wiedergeben der Inhalts Segmente.</span><span class="sxs-lookup"><span data-stu-id="c127c-113">These menu commands use **MCIWndPlayFrom**, **MCIWndPlayTo**, and **MCIWndPlayFromTo** to play the content segments.</span></span> <span data-ttu-id="c127c-114">Das Beispiel verwendet auch die Makros " [**mciwndgetstart**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstart) " und " [**mciwndgetend**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend) ", um den Anfang und das Ende des Inhalts zu identifizieren, und verwendet das [**mciwndhome**](/windows/desktop/api/Vfw/nf-vfw-mciwndhome) -Makro, um die Wiedergabe Position an den Anfang des Inhalts zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="c127c-114">The example also uses the [**MCIWndGetStart**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstart) and [**MCIWndGetEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend) macros to identify the beginning and end of the content, and it uses the [**MCIWndHome**](/windows/desktop/api/Vfw/nf-vfw-mciwndhome) macro to move the playback position to the beginning of the content.</span></span>

<span data-ttu-id="c127c-115">Die [**mciwndcreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) -Funktion verwendet \_ zusätzlich zu den Standardfenster Stilen die WS-Beschriftung und mciwndf- \_ ShowAll-Stile, um den Dateinamen, den Modus und die aktuelle Wiedergabe Position in der Titelleiste des mciwnd-Fensters anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="c127c-115">The [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) function uses the WS\_CAPTION and MCIWNDF\_SHOWALL styles in addition to the standard window styles to display the filename, mode, and current playback position in the title bar of the MCIWnd window.</span></span>


```C++
case WM_COMMAND: 
    switch (wParam) 
    { 
        case IDM_CREATEMCIWND: 
            g_hwndMCIWnd = MCIWndCreate(hwnd, 
                g_hinst, 
                WS_CHILD | WS_VISIBLE | WS_CAPTION | 
                MCIWNDF_SHOWALL, 
                "sample.avi"); 
            break;
        case IDM_PLAYFROM:                // plays last third of clip 
            MCIWndUseTime(g_hwndMCIWnd);  // millisecond format 
 
        // Get media start and end positions. 
            lStart = MCIWndGetStart(g_hwndMCIWnd); 
            lEnd = MCIWndGetEnd(g_hwndMCIWnd); 
 
        // Determine playback end position. 
            lPlayStart = 2 * (lEnd - lStart) / 3 + lStart; 
 
            MCIWndPlayFrom(g_hwndMCIWnd, lPlayStart); 
            break; 
        case IDM_PLAYTO:                  // plays first third of clip 
            MCIWndUseTime(g_hwndMCIWnd);  // millisecond format 
 
        // Get media start and end positions. 
            lStart = MCIWndGetStart(g_hwndMCIWnd); 
            lEnd = MCIWndGetEnd(g_hwndMCIWnd); 
 
        // Determine playback start position. 
            lPlayEnd = (lEnd - lStart) / 3 + lStart;
 
            MCIWndHome(g_hwndMCIWnd); 
            MCIWndPlayTo(g_hwndMCIWnd, lPlayEnd); 
            break; 
        case IDM_PLAYSOME:               // plays middle third of clip 
            MCIWndUseTime(g_hwndMCIWnd); // millisecond format 
 
        // Get media start and end positions. 
            lStart = MCIWndGetStart(g_hwndMCIWnd); 
            lEnd = MCIWndGetEnd(g_hwndMCIWnd); 
 
        // Determine playback start and end positions. 
            lPlayStart = (lEnd - lStart) / 3 + lStart;
            lPlayEnd = 2 * (lEnd - lStart) / 3 + lStart; 
 
            MCIWndPlayFromTo(g_hwndMCIWnd, lPlayStart, lPlayEnd); 
            break; 
    
    // Handle other commands here. 
    } 
```



 

 




