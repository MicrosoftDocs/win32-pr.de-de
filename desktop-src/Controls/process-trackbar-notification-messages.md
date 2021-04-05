---
title: Verarbeiten von TrackBar-Benachrichtigungs Meldungen
description: Trackbars Benachrichtigen das übergeordnete Fenster von Benutzeraktionen, indem das übergeordnete Element eine WM \_ HScroll-oder WM- \_ VScroll-Nachricht sendet.
ms.assetid: 83F47A3E-E607-49C2-A8B5-BC8A321D90BB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c723ad1bebb5c9f3ec8c4e7aefdc658e0881aef6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709006"
---
# <a name="how-to-process-trackbar-notification-messages"></a><span data-ttu-id="c330b-103">Verarbeiten von TrackBar-Benachrichtigungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="c330b-103">How to Process Trackbar Notification Messages</span></span>

<span data-ttu-id="c330b-104">Trackbars Benachrichtigen das übergeordnete Fenster von Benutzeraktionen, indem das übergeordnete Element eine [**WM \_ HScroll**](wm-hscroll.md) -oder [**WM- \_ VScroll**](wm-vscroll.md) -Nachricht sendet.</span><span class="sxs-lookup"><span data-stu-id="c330b-104">Trackbars notify their parent window of user actions by sending the parent a [**WM\_HSCROLL**](wm-hscroll.md) or [**WM\_VSCROLL**](wm-vscroll.md) message.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="c330b-105">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="c330b-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="c330b-106">Technologien</span><span class="sxs-lookup"><span data-stu-id="c330b-106">Technologies</span></span>

-   [<span data-ttu-id="c330b-107">Windows-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="c330b-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="c330b-108">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="c330b-108">Prerequisites</span></span>

-   <span data-ttu-id="c330b-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="c330b-109">C/C++</span></span>
-   <span data-ttu-id="c330b-110">Programmieren der Windows-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="c330b-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="c330b-111">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="c330b-111">Instructions</span></span>

### <a name="process-trackbar-notification-messages"></a><span data-ttu-id="c330b-112">Verarbeiten von TrackBar-Benachrichtigungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="c330b-112">Process Trackbar Notification Messages</span></span>

<span data-ttu-id="c330b-113">Das folgende Codebeispiel ist eine Funktion, die aufgerufen wird, wenn das übergeordnete Fenster der TrackBar eine [**WM- \_ HScroll**](wm-hscroll.md) -Nachricht empfängt.</span><span class="sxs-lookup"><span data-stu-id="c330b-113">The following code example is a function that is called when the trackbar's parent window receives a [**WM\_HSCROLL**](wm-hscroll.md) message.</span></span> <span data-ttu-id="c330b-114">Die TrackBar in diesem Beispiel hat den [**TSB-Stil " \_ enableselrange**](trackbar-control-styles.md) ".</span><span class="sxs-lookup"><span data-stu-id="c330b-114">The trackbar in this example has the [**TBS\_ENABLESELRANGE**](trackbar-control-styles.md) style.</span></span> <span data-ttu-id="c330b-115">Die Position des Schiebereglers wird mit dem Auswahlbereich verglichen, und der Schieberegler wird bei Bedarf an die Anfangs-oder Endposition des Auswahl Bereichs verschoben.</span><span class="sxs-lookup"><span data-stu-id="c330b-115">The position of the slider is compared to the selection range, and the slider is moved to the starting or ending position of the selection range when necessary.</span></span>


```
// TBNotifications - handles trackbar notifications received 
// in the wParam parameter of WM_HSCROLL. This function simply 
// ensures that the slider remains within the selection range. 

VOID WINAPI TBNotifications( 
    WPARAM wParam,  // wParam of WM_HSCROLL message 
    HWND hwndTrack, // handle of trackbar window 
    UINT iSelMin,   // minimum value of trackbar selection 
    UINT iSelMax)   // maximum value of trackbar selection 
    { 
    DWORD dwPos;    // current position of slider 

    switch (LOWORD(wParam)) { 
    
        case TB_ENDTRACK:
          
            dwPos = SendMessage(hwndTrack, TBM_GETPOS, 0, 0); 
            
            if (dwPos > iSelMax) 
                SendMessage(hwndTrack, TBM_SETPOS, 
                    (WPARAM) TRUE,       // redraw flag 
                    (LPARAM) iSelMax); 
                    
            else if (dwPos < iSelMin) 
                SendMessage(hwndTrack, TBM_SETPOS, 
                    (WPARAM) TRUE,       // redraw flag 
                    (LPARAM) iSelMin); 
            
            break; 

        default: 
        
            break; 
        } 
} 
```



## <a name="remarks"></a><span data-ttu-id="c330b-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c330b-116">Remarks</span></span>

<span data-ttu-id="c330b-117">Ein Dialogfeld, das eine TrackBar im TSB-Format " [**\_ Vert**](trackbar-control-styles.md) " enthält, kann diese Funktion verwenden, wenn Sie eine [**WM- \_ VScroll**](wm-vscroll.md) -Nachricht empfängt.</span><span class="sxs-lookup"><span data-stu-id="c330b-117">A dialog box that contains a [**TBS\_VERT**](trackbar-control-styles.md) style trackbar can use this function when it receives a [**WM\_VSCROLL**](wm-vscroll.md) message.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c330b-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c330b-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c330b-119">Verwenden von TrackBar-Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="c330b-119">Using Trackbar Controls</span></span>](using-trackbar-controls.md)
</dt> </dl>

 

 




