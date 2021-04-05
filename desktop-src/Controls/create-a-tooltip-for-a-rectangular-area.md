---
title: Erstellen einer QuickInfo für einen rechteckigen Bereich
description: Im folgenden Beispiel wird veranschaulicht, wie ein Standardmäßiges QuickInfo-Steuerelement für den gesamten Client Bereich eines Fensters erstellt wird.
ms.assetid: 6AF1CE6E-AD63-4F84-9759-14FE4F16092B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f8daf62bf2ba85c8750fd07a1b9122b0360fc11
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708652"
---
# <a name="how-to-create-a-tooltip-for-a-rectangular-area"></a>Erstellen einer QuickInfo für einen rechteckigen Bereich

Im folgenden Beispiel wird veranschaulicht, wie ein Standardmäßiges QuickInfo-Steuerelement für den gesamten Client Bereich eines Fensters erstellt wird.

Die folgende Abbildung zeigt die QuickInfo, die angezeigt wird, wenn sich der Mauszeiger innerhalb des Client Fensters eines Dialog Felds befindet. Das Handle des Dialog Felds wurde an die im vorherigen Beispiel gezeigte Funktion weitergeleitet.

![Screenshot eines Dialog Felds der Mauszeiger befindet sich innerhalb des Client Fensters, und eine QuickInfo ist sichtbar.](images/tt-rectangle.png)

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche

## <a name="instructions"></a>Anweisungen

### <a name="create-a-tooltip-for-a-rectangular-area"></a>Erstellen einer QuickInfo für einen rechteckigen Bereich

Im folgenden Beispiel wird veranschaulicht, wie ein Standardmäßiges QuickInfo-Steuerelement für den gesamten Client Bereich eines Fensters erstellt wird.


```C++
void CreateToolTipForRect(HWND hwndParent)
{
    // Create a tooltip.
    HWND hwndTT = CreateWindowEx(WS_EX_TOPMOST, TOOLTIPS_CLASS, NULL, 
                                 WS_POPUP | TTS_NOPREFIX | TTS_ALWAYSTIP, 
                                 CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, 
                                 hwndParent, NULL, g_hInst,NULL);

    SetWindowPos(hwndTT, HWND_TOPMOST, 0, 0, 0, 0, 
                 SWP_NOMOVE | SWP_NOSIZE | SWP_NOACTIVATE);

    // Set up "tool" information. In this case, the "tool" is the entire parent window.
    
    TOOLINFO ti = { 0 };
    ti.cbSize   = sizeof(TOOLINFO);
    ti.uFlags   = TTF_SUBCLASS;
    ti.hwnd     = hwndParent;
    ti.hinst    = g_hInst;
    ti.lpszText = TEXT("This is your tooltip string.");;
    
    GetClientRect (hwndParent, &ti.rect);

    // Associate the tooltip with the "tool" window.
    SendMessage(hwndTT, TTM_ADDTOOL, 0, (LPARAM) (LPTOOLINFO) &ti); 
} 
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Quick Infos](using-tooltip-contro.md)
</dt> </dl>

 

 




