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
# <a name="how-to-process-comboboxex-notifications"></a><span data-ttu-id="1dae0-103">Verarbeiten von ComboBoxEx-Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="1dae0-103">How to Process ComboBoxEx Notifications</span></span>

<span data-ttu-id="1dae0-104">In diesem Thema wird veranschaulicht, wie ComboBoxEx-Benachrichtigungs Meldungen verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="1dae0-104">This topic demonstrates how to process ComboBoxEx notification messages.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="1dae0-105">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="1dae0-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="1dae0-106">Technologien</span><span class="sxs-lookup"><span data-stu-id="1dae0-106">Technologies</span></span>

-   [<span data-ttu-id="1dae0-107">Windows-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="1dae0-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="1dae0-108">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="1dae0-108">Prerequisites</span></span>

-   <span data-ttu-id="1dae0-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="1dae0-109">C/C++</span></span>
-   <span data-ttu-id="1dae0-110">Programmieren der Windows-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="1dae0-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="1dae0-111">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="1dae0-111">Instructions</span></span>


<span data-ttu-id="1dae0-112">Ein ComboBoxEx-Steuerelement benachrichtigt das übergeordnete Fenster von Ereignissen durch das Senden von [**WM- \_ Benachrichtigungs**](wm-notify.md) Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="1dae0-112">A ComboBoxEx control notifies its parent window of events by sending [**WM\_NOTIFY**](wm-notify.md) messages.</span></span> <span data-ttu-id="1dae0-113">Außerdem werden die von ihm empfangenen [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Benachrichtigungs Meldungen aus dem darin enthaltenen Kombinations Feld an das übergeordnete Fenster weitergeleitet, das verarbeitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1dae0-113">It also passes the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) notification messages that it receives from the combo box contained within it to the parent window to be processed.</span></span> <span data-ttu-id="1dae0-114">Daher muss Ihre Anwendung darauf vorbereitet sein, **WM- \_ Benachrichtigungs** Meldungen von den ComboBoxEx-und **WM- \_ Befehls** Meldungen zu verarbeiten, die vom untergeordneten Kombinations Feld-Steuerelement ComboBoxEx weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="1dae0-114">Therefore, your application must be prepared to process **WM\_NOTIFY** messages from the ComboBoxEx and **WM\_COMMAND** messages that are forwarded from the ComboBoxEx child combo box control.</span></span>

<span data-ttu-id="1dae0-115">Im Beispiel in diesem Abschnitt werden die [**WM \_ Notify**](wm-notify.md) -und [**WM \_ Command**](/windows/desktop/menurc/wm-command) -Meldungen eines ComboBoxEx-Steuer Elements behandelt, indem eine entsprechende Anwendungs definierte Funktion aufgerufen wird, um diese Nachrichten zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="1dae0-115">The example in this section handles the [**WM\_NOTIFY**](wm-notify.md) and [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) messages from a ComboBoxEx control by calling a corresponding application-defined function to process these messages.</span></span>

## <a name="complete-example"></a><span data-ttu-id="1dae0-116">Vollständiges Beispiel</span><span class="sxs-lookup"><span data-stu-id="1dae0-116">Complete example</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="1dae0-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1dae0-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1dae0-118">Informationen zu ComboBoxEx-Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="1dae0-118">About ComboBoxEx Controls</span></span>](comboboxex-controls.md)
</dt> <dt>

[<span data-ttu-id="1dae0-119">ComboBoxEx-Steuerelement Verweis</span><span class="sxs-lookup"><span data-stu-id="1dae0-119">ComboBoxEx Control Reference</span></span>](bumper-comboboxex-comboboxex-control-reference.md)
</dt> <dt>

[<span data-ttu-id="1dae0-120">Verwenden von ComboBoxEx-Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="1dae0-120">Using ComboBoxEx Controls</span></span>](/windows/desktop/Controls/using-comboboxex)
</dt> <dt>

[<span data-ttu-id="1dae0-121">ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="1dae0-121">ComboBoxEx</span></span>](comboboxex-control-reference.md)
</dt> </dl>

 

 