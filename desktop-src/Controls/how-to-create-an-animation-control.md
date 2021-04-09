---
title: Erstellen eines Animations Steuer Elements
description: In diesem Thema wird veranschaulicht, wie ein Animations Steuerelement erstellt wird.
ms.assetid: 5852B636-F3D0-47A4-82F6-8BE570013E1B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d4ff190617996e42e6580b82311fb51f4248000
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036584"
---
# <a name="how-to-create-an-animation-control"></a><span data-ttu-id="5e44f-103">Erstellen eines Animations Steuer Elements</span><span class="sxs-lookup"><span data-stu-id="5e44f-103">How to Create an Animation Control</span></span>

<span data-ttu-id="5e44f-104">In diesem Thema wird veranschaulicht, wie ein Animations Steuerelement erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="5e44f-104">This topic demonstrates how to create an animation control.</span></span> <span data-ttu-id="5e44f-105">Das dazugehörige C++-Codebeispiel erstellt ein Animations Steuerelement in einem Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="5e44f-105">The accompanying C++ code example creates an animation control in a dialog box.</span></span> <span data-ttu-id="5e44f-106">Sie positioniert das Animations Steuerelement unterhalb eines angegebenen Steuer Elements und legt die Dimensionen des Animations Steuer Elements auf der Grundlage der Abmessungen eines Frames im Audio-Video Interleaved (AVI)-Clip fest.</span><span class="sxs-lookup"><span data-stu-id="5e44f-106">It positions the animation control below a specified control, and sets the dimensions of the animation control based on the dimensions of a frame in the Audio-Video Interleaved (AVI) clip.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="5e44f-107">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="5e44f-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="5e44f-108">Technologien</span><span class="sxs-lookup"><span data-stu-id="5e44f-108">Technologies</span></span>

-   [<span data-ttu-id="5e44f-109">Windows-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="5e44f-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="5e44f-110">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="5e44f-110">Prerequisites</span></span>

-   <span data-ttu-id="5e44f-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="5e44f-111">C/C++</span></span>
-   <span data-ttu-id="5e44f-112">Programmieren der Windows-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="5e44f-112">Windows User Interface Programming</span></span>
-   <span data-ttu-id="5e44f-113">AVI-Dateien</span><span class="sxs-lookup"><span data-stu-id="5e44f-113">AVI files</span></span>

## <a name="instructions"></a><span data-ttu-id="5e44f-114">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="5e44f-114">Instructions</span></span>

### <a name="step-1-create-an-instance-of-the-animation-control"></a><span data-ttu-id="5e44f-115">Schritt 1: Erstellen Sie eine Instanz des Animations Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="5e44f-115">Step 1: Create an instance of the animation control.</span></span>

<span data-ttu-id="5e44f-116">Verwenden Sie das [**animieren \_ Create**](/windows/desktop/api/Commctrl/nf-commctrl-animate_create) -Makro, um eine Instanz des Animations Steuer Elements zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5e44f-116">Use the [**Animate\_Create**](/windows/desktop/api/Commctrl/nf-commctrl-animate_create) macro to create an instance of the animation control.</span></span>


```C++
// IDC_ANIMATE - identifier of the animation control. 
// hwndDlg - handle to the dialog box.
RECT rc;
hwndAnim = Animate_Create(hwndDlg, IDC_ANIMATE, 
    WS_BORDER | WS_CHILD, g_hinst); 
```



### <a name="step-2-position-the-animation-control"></a><span data-ttu-id="5e44f-117">Schritt 2: Positionieren Sie das Animations Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="5e44f-117">Step 2: Position the animation control.</span></span>

<span data-ttu-id="5e44f-118">Die Bildschirm Koordinaten der angegebenen Steuerelement Schaltfläche werden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5e44f-118">Get the screen coordinates of the specified control button.</span></span>


```C++
// nIDCtl - identifier of the control below which the animation control is to be positioned.
GetWindowRect(GetDlgItem(hwndDlg, nIDCtl), &rc); 
```



<span data-ttu-id="5e44f-119">Die Koordinaten der unteren linken Ecke werden in Client Koordinaten konvertiert.</span><span class="sxs-lookup"><span data-stu-id="5e44f-119">Convert the coordinates of the lower-left corner to client coordinates.</span></span>


```C++
POINT pt;
pt.x = rc.left; 
pt.y = rc.bottom; 
ScreenToClient(hwndDlg, &pt); 
```



<span data-ttu-id="5e44f-120">Positionieren Sie das Animations Steuerelement unterhalb der angegebenen Steuerelement Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="5e44f-120">Position the animation control below the specified control button.</span></span>


```C++
// CX_FRAME, CY_FRAME - width and height of the frames in the AVI clip.      
SetWindowPos(hwndAnim, 0, pt.x, pt.y + 20, 
    CX_FRAME, CY_FRAME, 
    SWP_NOZORDER | SWP_DRAWFRAME);
```



### <a name="step-3-open-the-avi-clip"></a><span data-ttu-id="5e44f-121">Schritt 3: Öffnen Sie den AVI-Clip.</span><span class="sxs-lookup"><span data-stu-id="5e44f-121">Step 3: Open the AVI clip.</span></span>

<span data-ttu-id="5e44f-122">Aufrufen Sie das Makro [**animieren \_ Open**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open) , um den AVI-Clip zu öffnen und den ersten Frame im Animations Steuerelement anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="5e44f-122">Call the [**Animate\_Open**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open) macro to open the AVI clip and display the first frame in the animation control.</span></span> <span data-ttu-id="5e44f-123">Ruft die **ShowWindow** -Funktion auf, um das Animations Steuerelement sichtbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="5e44f-123">Call the **ShowWindow** function to make the animation control visible.</span></span>


```C++
Animate_Open(hwndAnim, "SEARCH.AVI"); 
ShowWindow(hwndAnim, SW_SHOW); 
```



## <a name="complete-example"></a><span data-ttu-id="5e44f-124">Vollständiges Beispiel</span><span class="sxs-lookup"><span data-stu-id="5e44f-124">Complete example</span></span>


```C++
// CreateAnimationCtrl - creates an animation control, positions it 
//                       below the specified control in a dialog box, 
//                       and opens the AVI clip for the animation control. 
// Returns the handle to the animation control. 
// hwndDlg             - handle to the dialog box. 
// nIDCtl              - identifier of the control below which the animation control 
//                       is to be positioned. 
// 
// Constants 
//     IDC_ANIMATE - identifier of the animation control. 
//     CX_FRAME, CY_FRAME - width and height of the frames 
//     in the AVI clip. 

HWND CreateAnimationCtrl(HWND hwndDlg, int nIDCtl) 
{ 
    HWND hwndAnim = NULL;    
    
    // Create the animation control.
    // IDC_ANIMATE - identifier of the animation control. 
    // hwndDlg - handle to the dialog box.
    RECT rc;
    hwndAnim = Animate_Create(hwndDlg, IDC_ANIMATE, 
        WS_BORDER | WS_CHILD, g_hinst); 

    // Get the screen coordinates of the specified control button.
    // nIDCtl - identifier of the control below which the animation control is to be positioned.
    GetWindowRect(GetDlgItem(hwndDlg, nIDCtl), &rc); 

    // Convert the coordinates of the lower-left corner to 
    // client coordinates.
    POINT pt;
    pt.x = rc.left; 
    pt.y = rc.bottom; 
    ScreenToClient(hwndDlg, &pt); 

    // Position the animation control below the Stop button.
    // CX_FRAME, CY_FRAME - width and height of the frames in the AVI clip.      
    SetWindowPos(hwndAnim, 0, pt.x, pt.y + 20, 
        CX_FRAME, CY_FRAME, 
        SWP_NOZORDER | SWP_DRAWFRAME);

    // Open the AVI clip, and show the animation control.
    Animate_Open(hwndAnim, "SEARCH.AVI"); 
    ShowWindow(hwndAnim, SW_SHOW); 

    return hwndAnim; 
} 
```



## <a name="related-topics"></a><span data-ttu-id="5e44f-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5e44f-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5e44f-126">Informationen zu Animations Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="5e44f-126">About Animation Controls</span></span>](animation-control-overview.md)
</dt> <dt>

[<span data-ttu-id="5e44f-127">Referenz zum Animations Steuerelement</span><span class="sxs-lookup"><span data-stu-id="5e44f-127">Animation Control Reference</span></span>](bumper-animation-animation-control-reference.md)
</dt> <dt>

[<span data-ttu-id="5e44f-128">Verwenden von Animations Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="5e44f-128">Using Animation Controls</span></span>](using-animation-control.md)
</dt> <dt>

[<span data-ttu-id="5e44f-129">Animation</span><span class="sxs-lookup"><span data-stu-id="5e44f-129">Animation</span></span>](animation-control-reference.md)
</dt> </dl>

 

 




