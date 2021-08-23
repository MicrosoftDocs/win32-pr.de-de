---
title: Erstellen eines Animationssteuerelements
description: In diesem Thema wird veranschaulicht, wie ein Animationssteuerelement erstellt wird.
ms.assetid: 5852B636-F3D0-47A4-82F6-8BE570013E1B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8117d7c9393a828786532bd3d3fbfcf4f4eaaf6bb1bfdccdc5a2f97fa1c5cb38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119435820"
---
# <a name="how-to-create-an-animation-control"></a>Erstellen eines Animationssteuerelements

In diesem Thema wird veranschaulicht, wie ein Animationssteuerelement erstellt wird. Im zugehörigen C++-Codebeispiel wird ein Animationssteuerelement in einem Dialogfeld erstellt. Es positioniert das Animationssteuerelement unter einem angegebenen Steuerelement und legt die Abmessungen des Animationssteuerelements basierend auf den Abmessungen eines Frames im clip Audio-Video Interleaved (AVI) fest.

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   [Windows Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Windows Benutzeroberfläche-Programmierung
-   AVI-Dateien

## <a name="instructions"></a>Anweisungen

### <a name="step-1-create-an-instance-of-the-animation-control"></a>Schritt 1: Erstellen Sie eine Instanz des Animationssteuerelements.

Verwenden Sie das Makro [**Animieren \_ erstellen,**](/windows/desktop/api/Commctrl/nf-commctrl-animate_create) um eine Instanz des Animationssteuerelements zu erstellen.


```C++
// IDC_ANIMATE - identifier of the animation control. 
// hwndDlg - handle to the dialog box.
RECT rc;
hwndAnim = Animate_Create(hwndDlg, IDC_ANIMATE, 
    WS_BORDER | WS_CHILD, g_hinst); 
```



### <a name="step-2-position-the-animation-control"></a>Schritt 2: Positionieren des Animationssteuerelements.

Abrufen der Bildschirmkoordinaten der angegebenen Steuerelementschaltfläche.


```C++
// nIDCtl - identifier of the control below which the animation control is to be positioned.
GetWindowRect(GetDlgItem(hwndDlg, nIDCtl), &rc); 
```



Konvertieren Sie die Koordinaten der unteren linken Ecke in Clientkoordinaten.


```C++
POINT pt;
pt.x = rc.left; 
pt.y = rc.bottom; 
ScreenToClient(hwndDlg, &pt); 
```



Positionieren Sie das Animationssteuerelement unterhalb der angegebenen Steuerelementschaltfläche.


```C++
// CX_FRAME, CY_FRAME - width and height of the frames in the AVI clip.      
SetWindowPos(hwndAnim, 0, pt.x, pt.y + 20, 
    CX_FRAME, CY_FRAME, 
    SWP_NOZORDER | SWP_DRAWFRAME);
```



### <a name="step-3-open-the-avi-clip"></a>Schritt 3: Öffnen Sie den AVI-Clip.

Rufen Sie das [**Makro Animieren \_ öffnen**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open) auf, um den AVI-Clip zu öffnen und den ersten Frame im Animationssteuerelement anzuzeigen. Rufen Sie die **ShowWindow-Funktion** auf, um das Animationssteuerelement sichtbar zu machen.


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

[Informationen zu Animationssteuerelementen](animation-control-overview.md)
</dt> <dt>

[Referenz zum Animationssteuerelement](bumper-animation-animation-control-reference.md)
</dt> <dt>

[Verwenden von Animationssteuerelementen](using-animation-control.md)
</dt> <dt>

[Animation](animation-control-reference.md)
</dt> </dl>

 

 




