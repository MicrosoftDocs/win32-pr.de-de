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
# <a name="registering-window-classes"></a><span data-ttu-id="ef817-105">Registrieren von Fensterklassen</span><span class="sxs-lookup"><span data-stu-id="ef817-105">Registering Window Classes</span></span>

<span data-ttu-id="ef817-106">Eine Fenster Klasse wird von einer Fenster Prozedur unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ef817-106">A window class is supported by a window procedure.</span></span> <span data-ttu-id="ef817-107">Die Anwendung kann eine Fenster Klasse entweder mithilfe von [**registerclassa**](/windows/win32/api/winuser/nf-winuser-registerclassa) oder [**registerclassw**](/windows/win32/api/winuser/nf-winuser-registerclassa)registrieren.</span><span class="sxs-lookup"><span data-stu-id="ef817-107">Your application can register a window class by using either [**RegisterClassA**](/windows/win32/api/winuser/nf-winuser-registerclassa) or [**RegisterClassW**](/windows/win32/api/winuser/nf-winuser-registerclassa).</span></span> <span data-ttu-id="ef817-108">Neue Anwendungen sollten in der Regel **registerclassw** verwenden.</span><span class="sxs-lookup"><span data-stu-id="ef817-108">New applications should typically use **RegisterClassW**.</span></span>

<span data-ttu-id="ef817-109">Wenn die Anwendung die Fenster Klasse mithilfe von [**registerclassa**](/windows/win32/api/winuser/nf-winuser-registerclassa)registriert, informiert die Funktion das Betriebssystem darüber, dass die Fenster der erstellten Klasse Nachrichten mit Text-oder Zeichen Parametern erwarten, um einen [Windows (ANSI)-Codepage](code-pages.md) -Zeichensatz zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="ef817-109">If the application registers the window class using [**RegisterClassA**](/windows/win32/api/winuser/nf-winuser-registerclassa), the function informs the operating system that the windows of the created class expect messages with text or character parameters to use a [Windows (ANSI) code page](code-pages.md) character set.</span></span> <span data-ttu-id="ef817-110">Die Registrierung mithilfe von [**registerclassw**](/windows/win32/api/winuser/nf-winuser-registerclassa) ermöglicht der Anwendung, das Betriebssystem aufzufordern, Text Parameter von Nachrichten als [Unicode](unicode.md)zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="ef817-110">Registration using [**RegisterClassW**](/windows/win32/api/winuser/nf-winuser-registerclassa) allows the application to request the operating system to pass text parameters of messages as [Unicode](unicode.md).</span></span> <span data-ttu-id="ef817-111">Die [**iswindowunicode**](/windows/win32/api/winuser/nf-winuser-iswindowunicode) -Funktion ermöglicht es einer Anwendung, die Art der einzelnen Fenster abzufragen.</span><span class="sxs-lookup"><span data-stu-id="ef817-111">The [**IsWindowUnicode**](/windows/win32/api/winuser/nf-winuser-iswindowunicode) function enables an application to query the nature of each window.</span></span>

<span data-ttu-id="ef817-112">Im folgenden Beispiel wird gezeigt, wie Sie eine Windows-Codepage-Fenster Klasse und eine Unicode-Fenster Klasse registrieren und wie Sie die Fenster Prozeduren für beide Fälle schreiben.</span><span class="sxs-lookup"><span data-stu-id="ef817-112">The following example shows how to register a Windows code page window class and a Unicode window class and how to write the window procedures for both cases.</span></span> <span data-ttu-id="ef817-113">Im Rahmen dieses Beispiels werden alle Funktionen und Strukturen mit den spezifischen Datentypen "A" (ANSI) oder "W" (Wide, Unicode) angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ef817-113">For the purposes of this example, all functions and structures are shown with the specific "A" (ANSI) or "W" (wide, Unicode) data types.</span></span> <span data-ttu-id="ef817-114">Mithilfe der in der [Verwendung von generischen Datentypen](using-generic-data-types.md)erläuterten Verfahren können Sie dieses Beispiel auch für die Verwendung von generischen Datentypen schreiben, sodass es für die Verwendung von Windows-Codepages oder Unicode kompiliert werden kann, je nachdem, ob "Unicode" definiert ist.</span><span class="sxs-lookup"><span data-stu-id="ef817-114">Using the techniques explained in [Using Generic Data Types](using-generic-data-types.md), you can alternatively write this example to use generic data types, so that it can be compiled to use either Windows code pages or Unicode, depending on whether "UNICODE" is defined.</span></span>


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



<span data-ttu-id="ef817-115">Das folgende Beispiel zeigt den Unterschied zwischen der Verarbeitung der [**WM- \_ char**](../inputdev/wm-char.md) -Nachricht in einer Windows-Codepage-Fenster Prozedur und einer Unicode-Fenster Prozedur.</span><span class="sxs-lookup"><span data-stu-id="ef817-115">The following example shows the difference between handling the [**WM\_CHAR**](../inputdev/wm-char.md) message in a Windows code page window procedure and a Unicode window procedure.</span></span>


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



<span data-ttu-id="ef817-116">Der gesamte Text in den von **ansiwndproc** empfangenen Nachrichten besteht aus Windows-Code Page Zeichen.</span><span class="sxs-lookup"><span data-stu-id="ef817-116">All text in messages received by **AnsiWndProc** is composed of Windows code page characters.</span></span> <span data-ttu-id="ef817-117">Der gesamte Text in Nachrichten, die von **uniwndproc** empfangen werden, besteht aus Unicode-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="ef817-117">All text in messages received by **UniWndProc** is composed of Unicode characters.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ef817-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ef817-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ef817-119">Verwenden von Unicode und Zeichensätzen</span><span class="sxs-lookup"><span data-stu-id="ef817-119">Using Unicode and Character Sets</span></span>](using-unicode-and-character-sets.md)
</dt> </dl>

 

 
