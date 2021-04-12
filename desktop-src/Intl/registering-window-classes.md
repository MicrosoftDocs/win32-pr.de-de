---
description: Eine Fenster Klasse wird von einer Fenster Prozedur unterstützt. Die Anwendung kann eine Fenster Klasse entweder mithilfe von registerclassa oder registerclassw registrieren. Neue Anwendungen sollten in der Regel registerclassw verwenden.
ms.assetid: 016296ce-6151-4673-ad59-c69a2138a05a
title: Registrieren von Fensterklassen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57c82e9daead566e5bcb5419fccc234014005f6f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104132041"
---
# <a name="registering-window-classes"></a>Registrieren von Fensterklassen

Eine Fenster Klasse wird von einer Fenster Prozedur unterstützt. Die Anwendung kann eine Fenster Klasse entweder mithilfe von [**registerclassa**](/windows/win32/api/winuser/nf-winuser-registerclassa) oder [**registerclassw**](/windows/win32/api/winuser/nf-winuser-registerclassa)registrieren. Neue Anwendungen sollten in der Regel **registerclassw** verwenden.

Wenn die Anwendung die Fenster Klasse mithilfe von [**registerclassa**](/windows/win32/api/winuser/nf-winuser-registerclassa)registriert, informiert die Funktion das Betriebssystem darüber, dass die Fenster der erstellten Klasse Nachrichten mit Text-oder Zeichen Parametern erwarten, um einen [Windows (ANSI)-Codepage](code-pages.md) -Zeichensatz zu verwenden. Die Registrierung mithilfe von [**registerclassw**](/windows/win32/api/winuser/nf-winuser-registerclassa) ermöglicht der Anwendung, das Betriebssystem aufzufordern, Text Parameter von Nachrichten als [Unicode](unicode.md)zu übergeben. Die [**iswindowunicode**](/windows/win32/api/winuser/nf-winuser-iswindowunicode) -Funktion ermöglicht es einer Anwendung, die Art der einzelnen Fenster abzufragen.

Im folgenden Beispiel wird gezeigt, wie Sie eine Windows-Codepage-Fenster Klasse und eine Unicode-Fenster Klasse registrieren und wie Sie die Fenster Prozeduren für beide Fälle schreiben. Im Rahmen dieses Beispiels werden alle Funktionen und Strukturen mit den spezifischen Datentypen "A" (ANSI) oder "W" (Wide, Unicode) angezeigt. Mithilfe der in der [Verwendung von generischen Datentypen](using-generic-data-types.md)erläuterten Verfahren können Sie dieses Beispiel auch für die Verwendung von generischen Datentypen schreiben, sodass es für die Verwendung von Windows-Codepages oder Unicode kompiliert werden kann, je nachdem, ob "Unicode" definiert ist.


```C++
// Register a Windows code page window class.

WNDCLASSA AnsiWndCls;

AnsiWndCls.style         = CS_DBLCLKS | CS_PARENTDC;
AnsiWndCls.lpfnWndProc   = (WNDPROC)AnsiWndProc;
AnsiWndCls.cbClsExtra    = 0;
AnsiWndCls.cbWndExtra    = 0;
AnsiWndCls.hInstance     = hInstance;
AnsiWndCls.hIcon         = NULL;
AnsiWndCls.hCursor       = LoadCursor(NULL, (LPTSTR)IDC_IBEAM);
AnsiWndCls.hbrBackground = NULL;
AnsiWndCls.lpszMenuName  = NULL;
AnsiWndCls.lpszClassName = "TestAnsi";

RegisterClassA(&AnsiWndCls);

// Register a Unicode window class.

WNDCLASSW UnicodeWndCls;

UnicodeWndCls.style         = CS_DBLCLKS | CS_PARENTDC;
UnicodeWndCls.lpfnWndProc   = (WNDPROC)UniWndProc;
UnicodeWndCls.cbClsExtra    = 0;
UnicodeWndCls.cbWndExtra    = 0;
UnicodeWndCls.hInstance     = hInstance;
UnicodeWndCls.hIcon         = NULL;
UnicodeWndCls.hCursor       = LoadCursor(NULL,(LPTSTR)IDC_IBEAM);
UnicodeWndCls.hbrBackground = NULL;
UnicodeWndCls.lpszMenuName  = NULL;
UnicodeWndCls.lpszClassName = L"TestUnicode";

RegisterClassW(&UnicodeWndCls);
```



Das folgende Beispiel zeigt den Unterschied zwischen der Verarbeitung der [**WM- \_ char**](../inputdev/wm-char.md) -Nachricht in einer Windows-Codepage-Fenster Prozedur und einer Unicode-Fenster Prozedur.


```C++
// "ANSI" Window Procedure

LRESULT CALLBACK AnsiWndProc(HWND hWnd, UINT message,
                             WPARAM wParam, LPARAM lParam)
{

    // Dispatch the messages that can be received.

    switch (message)
    {
        case WM_CHAR:

            // wParam - the value of the key
            // lParam - (not used in this example)

            if (lstrcmpA("Q", (LPCSTR) wParam))
            {
                // ...
            }
            else
            {
                // ...
            }
            break;
        // Process other messages.
    default:
        return DefWindowProc(hWnd, message, wParam, lParam);
    }
    return 0;
}

// Unicode Window Procedure

LRESULT CALLBACK UniWndProc(HWND hWnd, UINT message,
                            WPARAM wParam, LPARAM lParam)
{

    // Dispatch the messages that can be received.

    switch (message)
    {
        case WM_CHAR:

            // wParam - the value of the key
            // lParam - (not used in this example)

            if (lstrcmpW(L"Q", (LPCWSTR) wParam))
            {
                // ...
            }
            else
            {
                // ...
            }
            break;
        // Process other messages.
    default:
        return DefWindowProc(hWnd, message, wParam, lParam);
    }
    return 0;
}
```



Der gesamte Text in den von **ansiwndproc** empfangenen Nachrichten besteht aus Windows-Code Page Zeichen. Der gesamte Text in Nachrichten, die von **uniwndproc** empfangen werden, besteht aus Unicode-Zeichen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Unicode und Zeichensätzen](using-unicode-and-character-sets.md)
</dt> </dl>

 

 
