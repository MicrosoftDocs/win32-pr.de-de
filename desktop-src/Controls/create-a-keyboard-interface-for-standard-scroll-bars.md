---
title: Erstellen einer Tastaturschnittstelle für Standard-Scrollleisten
description: Obwohl ein Bildlaufleisten-Steuerelement eine integrierte Tastaturschnittstelle bereitstellt, ist dies bei einer Standardbildlaufleiste nicht der DerEinführungsschutz.
ms.assetid: 249D0077-6E61-479A-91D5-A4BD9752B82E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f25994639a40a6380bbf2f9cc0075e8a78b9e15787dbdf1babf0e6a15550faf1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119698740"
---
# <a name="how-to-create-a-keyboard-interface-for-standard-scroll-bars"></a>Erstellen einer Tastaturschnittstelle für Standard-Scrollleisten

Obwohl ein Bildlaufleisten-Steuerelement eine integrierte Tastaturschnittstelle bereitstellt, ist dies bei einer Standardbildlaufleiste nicht der DerEinführungsschutz. Um eine Tastaturschnittstelle für eine Standardschiebeleiste zu implementieren, muss eine Fensterprozedur die [**WM \_ KEYDOWN-Meldung**](/windows/desktop/inputdev/wm-keydown) verarbeiten und den durch den *wParam-Parameter* angegebenen Code mit virtuellen Schlüsseln untersuchen. Wenn der Code des virtuellen Schlüssels einer Pfeiltaste entspricht, sendet sich die Fensterprozedur selbst eine [**WM \_ HSCROLL-**](wm-hscroll.md) oder [**WM \_ VSCROLL-Nachricht,**](wm-vscroll.md) wobei das Wort in niedriger Reihenfolge des *wParam-Parameters* auf den entsprechenden Code für die Scrollleistenanforderung festgelegt ist.

Wenn der Benutzer beispielsweise die NACH-OBEN-TASTE drückt, empfängt die Fensterprozedur eine [**WM \_ KEYDOWN-Meldung**](/windows/desktop/inputdev/wm-keydown) mit *wParam* gleich VK \_ UP. Als Antwort sendet sich die Fensterprozedur selbst eine [**\_ WM-VSCROLL-Nachricht,**](wm-vscroll.md) wobei das Wort *wParam* in niedriger Reihenfolge auf den SB \_ LINEUP-Anforderungscode festgelegt ist.

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   [Windows Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Windows Benutzeroberfläche-Programmierung

## <a name="instructions"></a>Anweisungen

### <a name="create-a-keyboard-interface-for-a-standard-scroll-bar"></a>Erstellen einer Tastaturschnittstelle für eine Standardbildlaufleiste

Im folgenden Codebeispiel wird veranschaulicht, wie Sie eine Tastaturschnittstelle für eine Standard-Scrollleiste einschließen.


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

[Verwenden von Bildlaufleisten](using-scroll-bars.md)
</dt> <dt>

[Demo zu Windows allgemeinen Steuerelementen (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 