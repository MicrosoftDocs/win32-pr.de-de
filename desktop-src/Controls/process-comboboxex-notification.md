---
title: Verarbeiten von ComboBoxEx-Benachrichtigungen
description: In diesem Thema wird veranschaulicht, wie ComboBoxEx-Benachrichtigungs Meldungen verarbeitet werden.
ms.assetid: 375634BC-CDD6-4D72-A41E-FCBFCBFE7F03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a9787e22aa01d51478ca55f0dde5d7ac944decb
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "103949262"
---
# <a name="how-to-process-comboboxex-notifications"></a>Verarbeiten von ComboBoxEx-Benachrichtigungen

In diesem Thema wird veranschaulicht, wie ComboBoxEx-Benachrichtigungs Meldungen verarbeitet werden.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche

## <a name="instructions"></a>Anweisungen


Ein ComboBoxEx-Steuerelement benachrichtigt das übergeordnete Fenster von Ereignissen durch das Senden von [**WM- \_ Benachrichtigungs**](wm-notify.md) Nachrichten. Außerdem werden die von ihm empfangenen [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Benachrichtigungs Meldungen aus dem darin enthaltenen Kombinations Feld an das übergeordnete Fenster weitergeleitet, das verarbeitet werden soll. Daher muss Ihre Anwendung darauf vorbereitet sein, **WM- \_ Benachrichtigungs** Meldungen von den ComboBoxEx-und **WM- \_ Befehls** Meldungen zu verarbeiten, die vom untergeordneten Kombinations Feld-Steuerelement ComboBoxEx weitergeleitet werden.

Im Beispiel in diesem Abschnitt werden die [**WM \_ Notify**](wm-notify.md) -und [**WM \_ Command**](/windows/desktop/menurc/wm-command) -Meldungen eines ComboBoxEx-Steuer Elements behandelt, indem eine entsprechende Anwendungs definierte Funktion aufgerufen wird, um diese Nachrichten zu verarbeiten.

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

[ComboBoxEx-Steuerelement Verweis](bumper-comboboxex-comboboxex-control-reference.md)
</dt> <dt>

[Verwenden von ComboBoxEx-Steuerelementen](/windows/desktop/Controls/using-comboboxex)
</dt> <dt>

[ComboBoxEx](comboboxex-control-reference.md)
</dt> </dl>

 

 