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
# <a name="how-to-create-an-animation-control"></a>Erstellen eines Animations Steuer Elements

In diesem Thema wird veranschaulicht, wie ein Animations Steuerelement erstellt wird. Das dazugehörige C++-Codebeispiel erstellt ein Animations Steuerelement in einem Dialogfeld. Sie positioniert das Animations Steuerelement unterhalb eines angegebenen Steuer Elements und legt die Dimensionen des Animations Steuer Elements auf der Grundlage der Abmessungen eines Frames im Audio-Video Interleaved (AVI)-Clip fest.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche
-   AVI-Dateien

## <a name="instructions"></a>Anweisungen

### <a name="step-1-create-an-instance-of-the-animation-control"></a>Schritt 1: Erstellen Sie eine Instanz des Animations Steuer Elements.

Verwenden Sie das [**animieren \_ Create**](/windows/desktop/api/Commctrl/nf-commctrl-animate_create) -Makro, um eine Instanz des Animations Steuer Elements zu erstellen.


```C++
// IDC_ANIMATE - identifier of the animation control. 
// hwndDlg - handle to the dialog box.
RECT rc;
hwndAnim = Animate_Create(hwndDlg, IDC_ANIMATE, 
    WS_BORDER | WS_CHILD, g_hinst); 
```



### <a name="step-2-position-the-animation-control"></a>Schritt 2: Positionieren Sie das Animations Steuerelement.

Die Bildschirm Koordinaten der angegebenen Steuerelement Schaltfläche werden angezeigt.


```C++
// nIDCtl - identifier of the control below which the animation control is to be positioned.
GetWindowRect(GetDlgItem(hwndDlg, nIDCtl), &rc); 
```



Die Koordinaten der unteren linken Ecke werden in Client Koordinaten konvertiert.


```C++
POINT pt;
pt.x = rc.left; 
pt.y = rc.bottom; 
ScreenToClient(hwndDlg, &pt); 
```



Positionieren Sie das Animations Steuerelement unterhalb der angegebenen Steuerelement Schaltfläche.


```C++
// CX_FRAME, CY_FRAME - width and height of the frames in the AVI clip.      
SetWindowPos(hwndAnim, 0, pt.x, pt.y + 20, 
    CX_FRAME, CY_FRAME, 
    SWP_NOZORDER | SWP_DRAWFRAME);
```



### <a name="step-3-open-the-avi-clip"></a>Schritt 3: Öffnen Sie den AVI-Clip.

Aufrufen Sie das Makro [**animieren \_ Open**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open) , um den AVI-Clip zu öffnen und den ersten Frame im Animations Steuerelement anzuzeigen. Ruft die **ShowWindow** -Funktion auf, um das Animations Steuerelement sichtbar zu machen.


```C++
Animate_Open(hwndAnim, "SEARCH.AVI"); 
ShowWindow(hwndAnim, SW_SHOW); 
```



## <a name="complete-example"></a>Vollständiges Beispiel


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu Animations Steuerelementen](animation-control-overview.md)
</dt> <dt>

[Referenz zum Animations Steuerelement](bumper-animation-animation-control-reference.md)
</dt> <dt>

[Verwenden von Animations Steuerelementen](using-animation-control.md)
</dt> <dt>

[Animation](animation-control-reference.md)
</dt> </dl>

 

 




