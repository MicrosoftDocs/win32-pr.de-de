---
title: Verwenden von Windows
description: Indem Sie andere Steuerelemente als Fenster für eine Trackleiste festlegen, können Sie diese Steuerelemente automatisch als Bezeichnungen an den Enden der Trackleiste positionieren.
ms.assetid: 5797AA55-BD8D-407A-8896-08EE0DDC7E30
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6819e0f37f07a90ae08a623f14c6c26d1d67f55ea81143834dfd10816f74396
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829055"
---
# <a name="how-to-use-buddy-windows"></a>Verwenden von Windows

Indem Sie andere Steuerelemente als Fenster für eine Trackleiste festlegen, können Sie diese Steuerelemente automatisch als Bezeichnungen an den Enden der Trackleiste positionieren.

Die folgende Abbildung zeigt eine horizontale und eine vertikale Trackleiste, die beide statische Steuerelemente als Fenster verwenden.

![Screenshot eines Dialogfelds mit einer horizontalen Trackleiste und einer vertikalen Trackleiste](images/tkb-buddy.png)

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   [Windows Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Windows Benutzeroberfläche-Programmierung

## <a name="instructions"></a>Anweisungen

### <a name="use-buddy-windows"></a>Verwenden von Windows

Im folgenden Codebeispiel werden die in der Abbildung gezeigten Fenster erstellt.


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



## <a name="remarks"></a>Hinweise

**IDC \_ SLIDER1 und** **IDC \_ SLIDER2 sind** Trackbars, die im Ressourcen-Editor erstellt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Trackbar-Steuerelementen](using-trackbar-controls.md)
</dt> </dl>

 

 




