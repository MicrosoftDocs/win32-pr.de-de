---
title: Erstellen eines Steuer Elements für ein Hot Key
description: In diesem Thema wird veranschaulicht, wie Sie ein Steuerelement für den Hot Key erstellen Sie erstellen ein Hot Key-Steuerelement, indem Sie die Funktion "" der Klasse "Hotkey" angeben und die Fenster Klasse "Hotkey Class" angeben \_ .
ms.assetid: A6723D4E-B8F6-4365-8FCD-99B73D2C0470
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 498005efcdfbbf001283551bbeea4906ebc854cf
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "103858564"
---
# <a name="how-to-create-a-hot-key-control"></a><span data-ttu-id="670ea-104">Erstellen eines Steuer Elements für ein Hot Key</span><span class="sxs-lookup"><span data-stu-id="670ea-104">How to Create a Hot Key Control</span></span>

<span data-ttu-id="670ea-105">In diesem Thema wird veranschaulicht, wie Sie ein Steuerelement für den Hot Key erstellen</span><span class="sxs-lookup"><span data-stu-id="670ea-105">This topic demonstrates how to create a hot key control.</span></span> <span data-ttu-id="670ea-106">Sie erstellen ein Hot Key-Steuerelement, indem Sie [**die Funktion "" der**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) Klasse "Hotkey" angeben und die Fenster Klasse "Hotkey Class" angeben \_ .</span><span class="sxs-lookup"><span data-stu-id="670ea-106">You create a hot key control by using the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function, specifying the HOTKEY\_CLASS window class.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="670ea-107">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="670ea-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="670ea-108">Technologien</span><span class="sxs-lookup"><span data-stu-id="670ea-108">Technologies</span></span>

-   [<span data-ttu-id="670ea-109">Windows-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="670ea-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="670ea-110">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="670ea-110">Prerequisites</span></span>

-   <span data-ttu-id="670ea-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="670ea-111">C/C++</span></span>
-   <span data-ttu-id="670ea-112">Programmieren der Windows-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="670ea-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="670ea-113">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="670ea-113">Instructions</span></span>


<span data-ttu-id="670ea-114">Vergewissern Sie sich, dass die DLL für allgemeine Steuerelemente geladen ist, bevor Sie das Steuerelement für den Hot Key erstellen</span><span class="sxs-lookup"><span data-stu-id="670ea-114">Before you create the hot key control, ensure that the common controls DLL is loaded.</span></span>

<span data-ttu-id="670ea-115">Im folgenden C++-Codebeispiel ruft die Anwendungs definierte Funktion die [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) -Funktion auf, um die allgemeine Steuerelement-DLL zu laden.</span><span class="sxs-lookup"><span data-stu-id="670ea-115">In the following C++ code example, the application-defined function calls the [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) function to load the common control DLL.</span></span> <span data-ttu-id="670ea-116">Anschließend wird die Funktion " [**roatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) " aufgerufen, die die Klasse " **Hotkey \_ Class** Window" angibt, um ein Steuerelement für den Hot Key zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="670ea-116">Then it calls the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function, specifying the **HOTKEY\_CLASS** window class, to create a hot key control.</span></span> <span data-ttu-id="670ea-117">Er verwendet die [**HKM \_**](hkm-setrules.md) -Meldungen "SKM" und " [**HKM \_**](hkm-sethotkey.md) ", um das Steuerelement zu initialisieren, und gibt ein Handle für das Steuerelement zurück.</span><span class="sxs-lookup"><span data-stu-id="670ea-117">It uses the [**HKM\_SETRULES**](hkm-setrules.md) and [**HKM\_SETHOTKEY**](hkm-sethotkey.md) messages to initialize the control and returns a handle to the control.</span></span>

<span data-ttu-id="670ea-118">Mit diesem Hot Key-Steuerelement kann der Benutzer keine heiße Taste auswählen, bei der es sich um eine einzelne nicht geänderte Taste handelt, und es ist auch nicht möglich, die UMSCHALTTASTE und eine Taste auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="670ea-118">This hot key control does not allow the user to choose a hot key that is a single unmodified key, nor does it permit the user to choose only SHIFT and a key.</span></span> <span data-ttu-id="670ea-119">Diese Regeln verhindern effektiv, dass der Benutzer eine heiße Taste wählt, die bei der Eingabe von Text versehentlich eingegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="670ea-119">These rules effectively prevent the user from choosing a hot key that might be entered accidentally while typing text.</span></span>



```C++
// Creates a hot key control and sets rules and default settings for it.
// 
// Returns the handle of the hot key control. 
//
// Parameter
//     hwndDlg - Handle of the parent window (dialog box). 
// 
// Global variable 
//     g_hinst - Handle of the application instance. 

extern HINSTANCE g_hinst; 

HWND WINAPI InitializeHotkey(HWND hwndDlg) 
{ 
    HWND hwndHot = NULL;
    
    // Ensure that the common control DLL is loaded. 
    INITCOMMONCONTROLSEX icex;  //declare an INITCOMMONCONTROLSEX Structure
    icex.dwSize = sizeof(INITCOMMONCONTROLSEX);
    icex.dwICC = ICC_HOTKEY_CLASS;   //set dwICC member to ICC_HOTKEY_CLASS    
                                     // this loads the Hot Key control class.
    InitCommonControlsEx(&icex);  
 
    hwndHot = CreateWindowEx(0,                        // no extended styles 
                             HOTKEY_CLASS,             // class name 
                             TEXT(""),                 // no title (caption) 
                             WS_CHILD | WS_VISIBLE,    // style 
                             15, 10,                   // position 
                             200, 20,                  // size 
                             hwndDlg,                  // parent window 
                             NULL,                     // uses class menu 
                             g_hinst,                  // instance 
                             NULL);                    // no WM_CREATE parameter 
 
    SetFocus(hwndHot); 
 
    // Set rules for invalid key combinations. If the user does not supply a
    // modifier key, use ALT as a modifier. If the user supplies SHIFT as a 
    // modifier key, use SHIFT + ALT instead.
    SendMessage(hwndHot, 
                HKM_SETRULES, 
                (WPARAM) HKCOMB_NONE | HKCOMB_S,   // invalid key combinations 
                MAKELPARAM(HOTKEYF_ALT, 0));       // add ALT to invalid entries 
 
    // Set CTRL + ALT + A as the default hot key for this window. 
    // 0x41 is the virtual key code for 'A'. 
    SendMessage(hwndHot, 
                HKM_SETHOTKEY, 
                MAKEWORD(0x41, HOTKEYF_CONTROL | HOTKEYF_ALT), 
                0); 
 
    return hwndHot; 
}
```



## <a name="related-topics"></a><span data-ttu-id="670ea-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="670ea-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="670ea-121">Referenz zur Hot Key-Steuerung</span><span class="sxs-lookup"><span data-stu-id="670ea-121">Hot Key Control Reference</span></span>](bumper-hot-key-hot-key-control-reference.md)
</dt> <dt>

[<span data-ttu-id="670ea-122">Informationen zu Hot Key-Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="670ea-122">About Hot Key Controls</span></span>](hot-key-controls.md)
</dt> <dt>

[<span data-ttu-id="670ea-123">Verwenden von Hot Key-Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="670ea-123">Using Hot Key Controls</span></span>](using-hot-key-controls.md)
</dt> </dl>

 

 