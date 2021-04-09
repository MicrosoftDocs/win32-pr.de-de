---
title: Verwenden von Buddy-Fenstern
description: Wenn Sie andere Steuerelemente als Buddy-Fenster für eine TrackBar festlegen, können Sie diese Steuerelemente an den Enden der TrackBar als Bezeichnungen automatisch positionieren.
ms.assetid: 5797AA55-BD8D-407A-8896-08EE0DDC7E30
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8eca9a4e3b3049f8d4cf7515879d91a096f5a9e3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036796"
---
# <a name="how-to-use-buddy-windows"></a><span data-ttu-id="1f78d-103">Verwenden von Buddy-Fenstern</span><span class="sxs-lookup"><span data-stu-id="1f78d-103">How to Use Buddy Windows</span></span>

<span data-ttu-id="1f78d-104">Wenn Sie andere Steuerelemente als Buddy-Fenster für eine TrackBar festlegen, können Sie diese Steuerelemente an den Enden der TrackBar als Bezeichnungen automatisch positionieren.</span><span class="sxs-lookup"><span data-stu-id="1f78d-104">By setting other controls as buddy windows for a trackbar, you can automatically position those controls at the ends of the trackbar as labels.</span></span>

<span data-ttu-id="1f78d-105">Die folgende Abbildung zeigt eine horizontale und eine vertikale Trackleiste, beide mit statischen Steuerelementen als "Buddy-Fenster".</span><span class="sxs-lookup"><span data-stu-id="1f78d-105">The following illustration shows a horizontal and a vertical trackbar, both with static controls as buddy windows.</span></span>

![Screenshot mit einem Dialogfeld mit einer horizontalen Trackleiste und einer vertikalen Trackleiste](images/tkb-buddy.png)

## <a name="what-you-need-to-know"></a><span data-ttu-id="1f78d-107">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="1f78d-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="1f78d-108">Technologien</span><span class="sxs-lookup"><span data-stu-id="1f78d-108">Technologies</span></span>

-   [<span data-ttu-id="1f78d-109">Windows-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="1f78d-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="1f78d-110">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="1f78d-110">Prerequisites</span></span>

-   <span data-ttu-id="1f78d-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="1f78d-111">C/C++</span></span>
-   <span data-ttu-id="1f78d-112">Programmieren der Windows-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="1f78d-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="1f78d-113">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="1f78d-113">Instructions</span></span>

### <a name="use-buddy-windows"></a><span data-ttu-id="1f78d-114">Verwenden von Buddy-Fenstern</span><span class="sxs-lookup"><span data-stu-id="1f78d-114">Use Buddy Windows</span></span>

<span data-ttu-id="1f78d-115">Im folgenden Codebeispiel werden die in der Abbildung gezeigten Buddy-Fenster erstellt.</span><span class="sxs-lookup"><span data-stu-id="1f78d-115">The following code example creates the buddy windows shown in the illustration.</span></span>


```
void LabelTrackbarsWithBuddies(HWND hDlg)
{
    HWND hwndTrackbar;
    HWND hwndBuddy;
    
    const int staticWidth   = 50;
    const int staticHeight  = 20;

//======================================================
// For horizontal Trackbar.

    hwndTrackbar = GetDlgItem(hDlg, IDC_SLIDER1);

    hwndBuddy = CreateWindowEx(0, L"STATIC", L"Left", SS_RIGHT | WS_CHILD | WS_VISIBLE, 
                                    0, 0, staticWidth, staticHeight, hDlg, NULL, g_hInst, NULL);
                                    
    SendMessage(hwndTrackbar, TBM_SETBUDDY, (WPARAM)TRUE, (LPARAM)hwndBuddy);
    
    //-------------------------------------------------

    hwndBuddy = CreateWindowEx(0, L"STATIC", L"Right", SS_LEFT | WS_CHILD | WS_VISIBLE, 
                               0, 0, staticWidth, staticHeight, hDlg, NULL, g_hInst, NULL);
                                
    SendMessage(hwndTrackbar, TBM_SETBUDDY, (WPARAM)FALSE, (LPARAM)hwndBuddy);
    
//======================================================    
// For vertical Trackbar.
    
    hwndTrackbar = GetDlgItem(hDlg, IDC_SLIDER2);

    hwndBuddy = CreateWindowEx(0, L"STATIC", L"Top", SS_CENTER | WS_CHILD | WS_VISIBLE, 
                               0, 0, staticWidth, staticHeight, hDlg, NULL, g_hInst, NULL);
                               
    SendMessage(hwndTrackbar, TBM_SETBUDDY, (WPARAM)TRUE, (LPARAM)hwndBuddy);

    //-------------------------------------------------

    hwndBuddy = CreateWindowEx(0, L"STATIC", L"Bottom", SS_CENTER | WS_CHILD | WS_VISIBLE, 
                               0, 0, staticWidth, staticHeight, hDlg, NULL, g_hInst, NULL);
                               
    SendMessage(hwndTrackbar, TBM_SETBUDDY, (WPARAM)FALSE, (LPARAM)hwndBuddy);
}
```



## <a name="remarks"></a><span data-ttu-id="1f78d-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1f78d-116">Remarks</span></span>

<span data-ttu-id="1f78d-117">**IDC \_ SLIDER1** und **IDC \_ SLIDER2** sind trackbars, die im Ressourcen-Editor erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="1f78d-117">**IDC\_SLIDER1** and **IDC\_SLIDER2** are trackbars created in the resource editor.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1f78d-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1f78d-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f78d-119">Verwenden von TrackBar-Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="1f78d-119">Using Trackbar Controls</span></span>](using-trackbar-controls.md)
</dt> </dl>

 

 




