---
description: Eine Fensterklasse wird von einer Fensterprozedur unterstützt. Ihre Anwendung kann eine Fensterklasse entweder mit RegisterClassA oder RegisterClassW registrieren. Neue Anwendungen sollten in der Regel RegisterClassW verwenden.
ms.assetid: 016296ce-6151-4673-ad59-c69a2138a05a
title: Registrieren von Fensterklassen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f508ebdbfa35f2551d723b3ef9a1ffd807917dfe71e503f9d77b2e8fdb136f2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040450"
---
# <a name="registering-window-classes"></a>Registrieren von Fensterklassen

Eine Fensterklasse wird von einer Fensterprozedur unterstützt. Ihre Anwendung kann eine Fensterklasse registrieren, indem sie [**entweder RegisterClassA**](/windows/win32/api/winuser/nf-winuser-registerclassa) oder [**RegisterClassW verwendet.**](/windows/win32/api/winuser/nf-winuser-registerclassa) Neue Anwendungen sollten in der Regel **RegisterClassW verwenden.**

Wenn die Anwendung die Fensterklasse mit [**RegisterClassA**](/windows/win32/api/winuser/nf-winuser-registerclassa)registriert, informiert die Funktion das Betriebssystem darüber, dass die Fenster der erstellten Klasse Nachrichten mit Text- oder Zeichenparametern erwarten, um einen Windows-Codepagezeichensatz [(ANSI)](code-pages.md) zu verwenden. Bei der [**Registrierung mit RegisterClassW**](/windows/win32/api/winuser/nf-winuser-registerclassa) kann die Anwendung vom Betriebssystem anfordern, dass Textparameter von Nachrichten als Unicode übergeben [werden.](unicode.md) Mit [**der IsWindowUnicode-Funktion**](/windows/win32/api/winuser/nf-winuser-iswindowunicode) kann eine Anwendung die Art der einzelnen Fenster abfragen.

Das folgende Beispiel zeigt, wie sie eine Windows-Codepage-Fensterklasse und eine Unicode-Fensterklasse registrieren und die Fensterverfahren für beide Fälle schreiben. Für dieses Beispiel werden alle Funktionen und Strukturen mit den spezifischen Datentypen "A" (ANSI) oder "W" (breit, Unicode) angezeigt. Mithilfe der [](using-generic-data-types.md)unter Verwenden generischer Datentypen erläuterten Verfahren können Sie alternativ dieses Beispiel schreiben, um generische Datentypen zu verwenden, sodass es für die Verwendung von Windows-Codepages oder Unicode kompiliert werden kann, je nachdem, ob "UNICODE" definiert ist.


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



Das folgende Beispiel zeigt den Unterschied zwischen der Behandlung der [**WM \_ CHAR-Meldung**](../inputdev/wm-char.md) in Windows Codepagefensterprozedur und einer Unicode-Fensterprozedur.


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



Der text in Nachrichten, die **von AnsiWndProc** empfangen werden, besteht aus Windows Codepagezeichen. Der text in Nachrichten, die **von UniWndProc empfangen** werden, besteht aus Unicode-Zeichen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Unicode und Zeichensätzen](using-unicode-and-character-sets.md)
</dt> </dl>

 

 
