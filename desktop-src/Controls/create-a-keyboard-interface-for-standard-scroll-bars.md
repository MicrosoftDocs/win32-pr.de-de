---
title: Erstellen einer Tastaturschnittstelle für Standard Scrollleisten
description: Obwohl ein Schiebe leisten-Steuerelement eine integrierte Tastaturschnittstelle bereitstellt, ist dies für eine Standard Scrollleiste nicht der Standard.
ms.assetid: 249D0077-6E61-479A-91D5-A4BD9752B82E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43b739638d95d9f3e530718f8e9b9e6168069420
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103858496"
---
# <a name="how-to-create-a-keyboard-interface-for-standard-scroll-bars"></a>Erstellen einer Tastaturschnittstelle für Standard Scrollleisten

Obwohl ein Schiebe leisten-Steuerelement eine integrierte Tastaturschnittstelle bereitstellt, ist dies für eine Standard Scrollleiste nicht der Standard. Um eine Tastaturschnittstelle für eine Standard Scrollleiste zu implementieren, muss eine Fenster Prozedur die [**WM- \_ KeyDown**](/windows/desktop/inputdev/wm-keydown) -Nachricht verarbeiten und den durch den *wParam* -Parameter angegebenen Code des virtuellen Schlüssels überprüfen. Wenn der Code des virtuellen Schlüssels einer Pfeiltaste entspricht, sendet die Fenster Prozedur selbst eine [**WM \_ HScroll**](wm-hscroll.md) -oder [**WM \_ VScroll**](wm-vscroll.md) -Nachricht, bei der das nieder wertige Wort des *wParam* -Parameters auf den entsprechenden Anforderungs Code der Schiebe Leiste festgelegt ist.

Wenn der Benutzer z. b. die nach-oben-Taste drückt, empfängt die Fenster Prozedur eine [**WM- \_ KeyDown**](/windows/desktop/inputdev/wm-keydown) -Nachricht mit *wParam* , die der "VK up" entspricht \_ . Als Antwort sendet die Fenster Prozedur eine WM- [**\_ VScroll**](wm-vscroll.md) -Nachricht, bei der das nieder wertige Wort von *wParam* auf den SB-Anstellungs Anforderungs Code festgelegt ist \_ .

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche

## <a name="instructions"></a>Anweisungen

### <a name="create-a-keyboard-interface-for-a-standard-scroll-bar"></a>Erstellen einer Tastaturschnittstelle für eine Standard Scrollleiste

Im folgenden Codebeispiel wird veranschaulicht, wie Sie eine Tastaturschnittstelle für eine Standard Scrollleiste einschließen.


```C++
    case WM_KEYDOWN: 
    {
        WORD wScrollNotify = 0xFFFF;

        switch (wParam) 
        { 
            case VK_UP: 
                wScrollNotify = SB_LINEUP; 
                break; 
 
            case VK_PRIOR: 
                wScrollNotify = SB_PAGEUP; 
                break; 
 
            case VK_NEXT: 
                wScrollNotify = SB_PAGEDOWN; 
                break; 
 
            case VK_DOWN: 
                wScrollNotify = SB_LINEDOWN; 
                break; 
 
            case VK_HOME: 
                wScrollNotify = SB_TOP; 
                break; 
 
            case VK_END: 
                wScrollNotify = SB_BOTTOM; 
                break; 
        } 
 
        if (wScrollNotify != -1) 
            SendMessage(hwnd, WM_VSCROLL, MAKELONG(wScrollNotify, 0), 0L); 
 
        break; 
    }
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Scrollleisten](using-scroll-bars.md)
</dt> <dt>

[Demo zu allgemeinen Windows-Steuerelementen (cppwindowscommoncontrols)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 