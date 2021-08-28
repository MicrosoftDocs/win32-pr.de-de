---
title: Verarbeiten von ComboBoxEx-Benachrichtigungen
description: In diesem Thema wird veranschaulicht, wie ComboBoxEx-Benachrichtigungsmeldungen verarbeitet werden.
ms.assetid: 375634BC-CDD6-4D72-A41E-FCBFCBFE7F03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4ec73c31020283afe5876567a57fc1fbd8a23cee123e9dc417c14c57a86709a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119575490"
---
# <a name="how-to-process-comboboxex-notifications"></a>Verarbeiten von ComboBoxEx-Benachrichtigungen

In diesem Thema wird veranschaulicht, wie ComboBoxEx-Benachrichtigungsmeldungen verarbeitet werden.

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   [Windows Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Windows Benutzeroberfläche-Programmierung

## <a name="instructions"></a>Anweisungen


Ein ComboBoxEx-Steuerelement benachrichtigt sein übergeordnetes Fenster über Ereignisse, indem [**WM \_ NOTIFY-Nachrichten**](wm-notify.md) gesendet werden. Außerdem werden die [**WM COMMAND-Benachrichtigungsmeldungen, \_**](/windows/desktop/menurc/wm-command) die vom darin enthaltenen Kombinationsfeld empfangen werden, an das übergeordnete Fenster übergeben, das verarbeitet werden soll. Daher muss Ihre Anwendung darauf vorbereitet sein, **WM \_ NOTIFY-Nachrichten** aus den ComboBoxEx- und **WM \_ COMMAND-Nachrichten** zu verarbeiten, die vom untergeordneten ComboBoxEx-Kombinationsfeld-Steuerelement weitergeleitet werden.

Im Beispiel in diesem Abschnitt werden die [**WM \_ NOTIFY-**](wm-notify.md) und [**WM \_ COMMAND-Meldungen**](/windows/desktop/menurc/wm-command) eines ComboBoxEx-Steuerelements verarbeitet, indem eine entsprechende anwendungsdefinierte Funktion aufgerufen wird, um diese Nachrichten zu verarbeiten.

## <a name="complete-example"></a>Vollständiges Beispiel


```C++
LRESULT CALLBACK WndProc (HWND hwnd, UINT msg, WPARAM wParam, LPARAM lParam)
{
    switch(msg){

        case WM_COMMAND: // notification from the child ComboBox within the ComboBoxEx control.
            if((HWND)lParam == g_hwndCB)
                DoOldNotify(hwnd,  wParam);  
            break;

        case WM_NOTIFY: // notification from the ComboBoxEx control
            return (DoCBEXNotify(hwnd, lParam));

        case WM_PAINT:
            hdc = BeginPaint(hwnd, &ps);
            EndPaint(hwnd, &ps);
            break;

        case WM_DESTROY:
            PostQuitMessage(0);
            break;

        default:
            return DefWindowProc(hwnd, msg, wParam, lParam);
            break;
    }

    return FALSE;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu ComboBoxEx-Steuerelementen](comboboxex-controls.md)
</dt> <dt>

[ComboBoxEx-Steuerelementreferenz](bumper-comboboxex-comboboxex-control-reference.md)
</dt> <dt>

[Verwenden von ComboBoxEx-Steuerelementen](/windows/desktop/Controls/using-comboboxex)
</dt> <dt>

[ComboBoxEx](comboboxex-control-reference.md)
</dt> </dl>

 

 