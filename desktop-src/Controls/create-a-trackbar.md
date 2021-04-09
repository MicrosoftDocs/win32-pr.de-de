---
title: Erstellen einer TrackBar
description: Wenn die TrackBar erstellt wird, werden sowohl der Bereich als auch der zugehörige Auswahlbereich initialisiert. Die Seitengröße wird auch zu diesem Zeitpunkt festgelegt.
ms.assetid: FA110B4A-D3D7-49D8-A3DC-368099F6DA1E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9468ff044b94837f54d04cda4a9105f15410692
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036538"
---
# <a name="how-to-create-a-trackbar"></a><span data-ttu-id="a6c54-104">Erstellen einer TrackBar</span><span class="sxs-lookup"><span data-stu-id="a6c54-104">How to Create a Trackbar</span></span>

<span data-ttu-id="a6c54-105">Wenn die TrackBar erstellt wird, werden sowohl der Bereich als auch der zugehörige Auswahlbereich initialisiert.</span><span class="sxs-lookup"><span data-stu-id="a6c54-105">When the trackbar is created, both its range and its selection range are initialized.</span></span> <span data-ttu-id="a6c54-106">Die Seitengröße wird auch zu diesem Zeitpunkt festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a6c54-106">The page size is also set at this time.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="a6c54-107">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="a6c54-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="a6c54-108">Technologien</span><span class="sxs-lookup"><span data-stu-id="a6c54-108">Technologies</span></span>

-   [<span data-ttu-id="a6c54-109">Windows-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="a6c54-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="a6c54-110">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="a6c54-110">Prerequisites</span></span>

-   <span data-ttu-id="a6c54-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="a6c54-111">C/C++</span></span>
-   <span data-ttu-id="a6c54-112">Programmieren der Windows-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="a6c54-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="a6c54-113">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="a6c54-113">Instructions</span></span>

### <a name="create-a-trackbar"></a><span data-ttu-id="a6c54-114">Erstellen einer TrackBar</span><span class="sxs-lookup"><span data-stu-id="a6c54-114">Create a Trackbar</span></span>

<span data-ttu-id="a6c54-115">Im folgenden Beispiel wird gezeigt, wie Sie eine TrackBar mit den Formaten [**TSB \_ autoticks**](trackbar-control-styles.md) und [**TB \_ enableselrange**](trackbar-control-styles.md) erstellen.</span><span class="sxs-lookup"><span data-stu-id="a6c54-115">The following example shows how to create a trackbar with the [**TBS\_AUTOTICKS**](trackbar-control-styles.md) and [**TBS\_ENABLESELRANGE**](trackbar-control-styles.md) styles.</span></span>


```
// CreateTrackbar - creates and initializes a trackbar. 
// 
// Global variable
//     g_hinst - instance handle
//
HWND WINAPI CreateTrackbar( 
    HWND hwndDlg,  // handle of dialog box (parent window) 
    UINT iMin,     // minimum value in trackbar range 
    UINT iMax,     // maximum value in trackbar range 
    UINT iSelMin,  // minimum value in trackbar selection 
    UINT iSelMax)  // maximum value in trackbar selection 
{ 

    InitCommonControls(); // loads common control's DLL 

    hwndTrack = CreateWindowEx( 
        0,                               // no extended styles 
        TRACKBAR_CLASS,                  // class name 
        "Trackbar Control",              // title (caption) 
        WS_CHILD | 
        WS_VISIBLE | 
        TBS_AUTOTICKS | 
        TBS_ENABLESELRANGE,              // style 
        10, 10,                          // position 
        200, 30,                         // size 
        hwndDlg,                         // parent window 
        ID_TRACKBAR,                     // control identifier 
        g_hinst,                         // instance 
        NULL                             // no WM_CREATE parameter 
        ); 

    SendMessage(hwndTrack, TBM_SETRANGE, 
        (WPARAM) TRUE,                   // redraw flag 
        (LPARAM) MAKELONG(iMin, iMax));  // min. & max. positions
        
    SendMessage(hwndTrack, TBM_SETPAGESIZE, 
        0, (LPARAM) 4);                  // new page size 

    SendMessage(hwndTrack, TBM_SETSEL, 
        (WPARAM) FALSE,                  // redraw flag 
        (LPARAM) MAKELONG(iSelMin, iSelMax)); 
        
    SendMessage(hwndTrack, TBM_SETPOS, 
        (WPARAM) TRUE,                   // redraw flag 
        (LPARAM) iSelMin); 

    SetFocus(hwndTrack); 

    return hwndTrack; 
} 
```



## <a name="related-topics"></a><span data-ttu-id="a6c54-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a6c54-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6c54-117">Verwenden von TrackBar-Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="a6c54-117">Using Trackbar Controls</span></span>](using-trackbar-controls.md)
</dt> </dl>

 

 




