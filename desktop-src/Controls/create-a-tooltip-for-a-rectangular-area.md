---
title: Erstellen einer QuickInfo für einen rechteckigen Bereich
description: Im folgenden Beispiel wird veranschaulicht, wie Sie ein standardmäßiges QuickInfo-Steuerelement für den gesamten Clientbereich eines Fensters erstellen.
ms.assetid: 6AF1CE6E-AD63-4F84-9759-14FE4F16092B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9be19be187e8c09b3aeb618e1c3518c7c15ca66816cbbb751abe43aa0b9172a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119920694"
---
# <a name="how-to-create-a-tooltip-for-a-rectangular-area"></a>Erstellen einer QuickInfo für einen rechteckigen Bereich

Im folgenden Beispiel wird veranschaulicht, wie Sie ein standardmäßiges QuickInfo-Steuerelement für den gesamten Clientbereich eines Fensters erstellen.

Die folgende Abbildung zeigt die QuickInfo, die angezeigt wird, wenn sich der Mauszeiger im Clientfenster eines Dialogfelds befindet. Das Handle des Dialogfelds wurde an die im vorherigen Beispiel gezeigte Funktion übergeben.

![Screenshot eines Dialogfelds Der Mauszeiger befindet sich im Clientfenster, und eine QuickInfo ist sichtbar.](images/tt-rectangle.png)

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   [Windows Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Windows Benutzeroberfläche-Programmierung

## <a name="instructions"></a>Anweisungen

### <a name="create-a-tooltip-for-a-rectangular-area"></a>Erstellen einer QuickInfo für einen rechteckigen Bereich

Im folgenden Beispiel wird veranschaulicht, wie Sie ein standardmäßiges QuickInfo-Steuerelement für den gesamten Clientbereich eines Fensters erstellen.


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

[Verwenden von QuickInfo-Steuerelementen](using-tooltip-contro.md)
</dt> </dl>

 

 




