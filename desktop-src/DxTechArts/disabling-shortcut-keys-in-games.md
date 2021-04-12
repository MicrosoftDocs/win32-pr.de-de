---
title: Deaktivieren von Tastenkombinationen in spielen
description: In diesem Artikel wird beschrieben, wie Tastenkombinationen in Microsoft Windows vorübergehend deaktiviert werden, um die Unterbrechung von Spiel spielen bei voll Bild spielen zu verhindern.
ms.assetid: 732523f9-ecff-c6c2-646d-1bc3443232ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aff426e0d728150cf5f6ac3cd8d46a711c9b4f8b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473525"
---
# <a name="disabling-shortcut-keys-in-games"></a><span data-ttu-id="4c555-103">Deaktivieren von Tastenkombinationen in spielen</span><span class="sxs-lookup"><span data-stu-id="4c555-103">Disabling Shortcut Keys in Games</span></span>

<span data-ttu-id="4c555-104">In diesem Artikel wird beschrieben, wie Tastenkombinationen in Microsoft Windows vorübergehend deaktiviert werden, um die Unterbrechung von Spiel spielen bei voll Bild spielen zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="4c555-104">This articles describes how to temporarily disable keyboard shortcuts in Microsoft Windows to prevent disruption of game play for full screen games.</span></span> <span data-ttu-id="4c555-105">Die UMSCHALTTASTE und die STRG-Taste werden häufig als Feuer-oder Run-Schaltflächen in Spielen verwendet.</span><span class="sxs-lookup"><span data-stu-id="4c555-105">The SHIFT key and the CTRL key are often used as fire or run buttons in games.</span></span> <span data-ttu-id="4c555-106">Wenn Benutzer versehentlich die Windows-Taste drücken (in der Nähe dieser Tasten), können Sie dazu führen, dass Sie plötzlich aus der Anwendung herausspringt, was die Spiel Darstellung ruiniert.</span><span class="sxs-lookup"><span data-stu-id="4c555-106">If users accidentally press the Windows key (located near these keys), they can cause themselves to suddenly jump out of the application, which ruins the game experience.</span></span> <span data-ttu-id="4c555-107">Wenn Sie einfach die Umschalttaste als Spiel Schaltfläche verwenden, kann die Tastenkombination "StickyKeys" versehentlich ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="4c555-107">Simply using the SHIFT key as a game button can inadvertently execute the StickyKeys shortcut which may display a warning dialog.</span></span> <span data-ttu-id="4c555-108">Um diese Probleme zu vermeiden, sollten Sie diese Schlüssel bei der Ausführung im Vollbildmodus deaktivieren und die Schlüssel bei der Ausführung im Fenstermodus wieder für Ihre Standard Handler aktivieren oder die Anwendung beenden.</span><span class="sxs-lookup"><span data-stu-id="4c555-108">To avoid these issues, you should disable these keys when running in full-screen mode, and either enable the keys back to their default handlers when running in windowed mode or exit the application.</span></span>

<span data-ttu-id="4c555-109">In diesem Artikel wird beschrieben, wie Sie die folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="4c555-109">This article describes how to do the following:</span></span>

-   [<span data-ttu-id="4c555-110">Windows-Taste mit einem Tastatur Hook deaktivieren</span><span class="sxs-lookup"><span data-stu-id="4c555-110">Disable the Windows Key with a Keyboard Hook</span></span>](#disable-the-windows-key-with-a-keyboard-hook)
-   [<span data-ttu-id="4c555-111">Deaktivieren der Tastenkombinationen für Barrierefreiheit</span><span class="sxs-lookup"><span data-stu-id="4c555-111">Disable the Accessibility Shortcut Keys</span></span>](#disable-the-accessibility-shortcut-keys)

## <a name="disable-the-windows-key-with-a-keyboard-hook"></a><span data-ttu-id="4c555-112">Windows-Taste mit einem Tastatur Hook deaktivieren</span><span class="sxs-lookup"><span data-stu-id="4c555-112">Disable the Windows Key with a Keyboard Hook</span></span>

<span data-ttu-id="4c555-113">Verwenden Sie einen Tastatur Hook auf niedriger Ebene, um das Verarbeiten der Windows-Taste zu filtern.</span><span class="sxs-lookup"><span data-stu-id="4c555-113">Use a low-level keyboard hook to filter out the Windows key from being processed.</span></span> <span data-ttu-id="4c555-114">Der in Beispiel 1 angezeigte Tastatur Hook auf niedriger Ebene bleibt auch dann wirksam, wenn ein Benutzer das Fenster minimiert oder zu einer anderen Anwendung wechselt.</span><span class="sxs-lookup"><span data-stu-id="4c555-114">The low-level keyboard hook shown in Example 1 remains in effect even if a user minimizes the window or switches to another application.</span></span> <span data-ttu-id="4c555-115">Dies bedeutet, dass Sie darauf achten müssen, dass die Windows-Taste nicht deaktiviert ist, wenn die Anwendung deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="4c555-115">This means that you must be careful to ensure that the Windows key is not disabled when the application is deactivated.</span></span> <span data-ttu-id="4c555-116">Der Code in Beispiel 1 bewirkt dies, indem die WM \_ activateapp-Nachricht verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="4c555-116">The code in Example 1 does this by handling the WM\_ACTIVATEAPP message.</span></span>

> [!Note]  
> <span data-ttu-id="4c555-117">Diese Methode funktioniert unter Windows 2000 und neueren Versionen von Windows.</span><span class="sxs-lookup"><span data-stu-id="4c555-117">This method works on Windows 2000 and later versions of Windows.</span></span> <span data-ttu-id="4c555-118">Diese Methode funktioniert auch mit den Benutzerkonten mit den geringsten Rechten (auch als eingeschränkte Benutzerkonten bezeichnet).</span><span class="sxs-lookup"><span data-stu-id="4c555-118">This method also works with least-privileged user accounts (also known as limited-user accounts).</span></span>

 

<span data-ttu-id="4c555-119">Diese Methode wird von dxut verwendet und wird im folgenden Codebeispiel veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="4c555-119">This method is used by DXUT and is illustrated in the following code example.</span></span>

<span data-ttu-id="4c555-120">**Beispiel 1. Verwenden eines Tastatur Hooks auf niedriger Ebene zum Deaktivieren der Windows-Taste**</span><span class="sxs-lookup"><span data-stu-id="4c555-120">**Example 1. Using a low-level keyboard hook to disable the Windows key**</span></span>


```C++
HHOOK g_hKeyboardHook;
BOOL g_bFullscreen;
 
INT WINAPI WinMain( HINSTANCE, HINSTANCE, LPSTR, int )
{
    // Initialization
    g_hKeyboardHook = SetWindowsHookEx( WH_KEYBOARD_LL,  LowLevelKeyboardProc, GetModuleHandle(NULL), 0 );
 
    // 
    // main application code here
    // 
 
    // Cleanup before shutdown
    UnhookWindowsHookEx( g_hKeyboardHook );
}
 
 
LRESULT CALLBACK LowLevelKeyboardProc( int nCode, WPARAM wParam, LPARAM lParam )
{
    if (nCode < 0 || nCode != HC_ACTION )  // do not process message 
        return CallNextHookEx( g_hKeyboardHook, nCode, wParam, lParam); 
 
    bool bEatKeystroke = false;
    KBDLLHOOKSTRUCT* p = (KBDLLHOOKSTRUCT*)lParam;
    switch (wParam) 
    {
        case WM_KEYDOWN:  
        case WM_KEYUP:    
        {
            bEatKeystroke = (g_bFullscreen && g_bWindowActive && ((p->vkCode == VK_LWIN) || (p->vkCode == VK_RWIN)));
            break;
        }
    }
 
    if( bEatKeystroke )
        return 1;
    else
        return CallNextHookEx( g_hKeyboardHook, nCode, wParam, lParam );
}
 
 
LRESULT CALLBACK WndProc( HWND hWnd, UINT uMsg, WPARAM wParam, LPARAM lParam )
{
    switch( uMsg )
    {
       case WM_ACTIVATEAPP:
            // g_bWindowActive is used to control if the Windows key is filtered by the keyboard hook or not.
            if( wParam == TRUE )
                g_bWindowActive  = true;           
            else 
                g_bWindowActive  = false;           
            break;
    }
}
```



## <a name="disable-the-accessibility-shortcut-keys"></a><span data-ttu-id="4c555-121">Deaktivieren der Tastenkombinationen für Barrierefreiheit</span><span class="sxs-lookup"><span data-stu-id="4c555-121">Disable the Accessibility Shortcut Keys</span></span>

<span data-ttu-id="4c555-122">Windows umfasst Barrierefreiheits Features wie z. b. "StickyKeys", "Filter Keys" und "degglekeys" (siehe [Windows-Barrierefreiheit](/previous-versions/visualstudio/visual-studio-6.0/aa227589(v=vs.60))).</span><span class="sxs-lookup"><span data-stu-id="4c555-122">Windows includes accessibility features such as StickyKeys, FilterKeys, and ToggleKeys (see [Windows Accessibility](/previous-versions/visualstudio/visual-studio-6.0/aa227589(v=vs.60))).</span></span> <span data-ttu-id="4c555-123">Jede dieser Dienste dient einem anderen Zweck: "StickyKeys" ist z. b. für Personen konzipiert, die Schwierigkeiten haben, zwei oder mehr Schlüssel gleichzeitig zu halten.</span><span class="sxs-lookup"><span data-stu-id="4c555-123">Each of these serves a different purpose; StickyKeys for example, is designed for people who have difficulty holding down two or more keys simultaneously.</span></span> <span data-ttu-id="4c555-124">Jede dieser Barrierefreiheits Features verfügt auch über eine Tastenkombination, mit der die Funktion aktiviert oder deaktiviert werden kann.</span><span class="sxs-lookup"><span data-stu-id="4c555-124">Each of these accessibility features also has a keyboard shortcut that allows the feature to be turned on or off.</span></span> <span data-ttu-id="4c555-125">Die Tastenkombination "StickyKeys" wird beispielsweise durch das fünfmal drücken der Umschalttaste ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="4c555-125">For example, the StickyKeys shortcut is triggered by pressing the SHIFT key five times.</span></span> <span data-ttu-id="4c555-126">Wenn die Umschalttaste auch im Spiel verwendet wird, könnte der Benutzer diese Verknüpfung während der Spiel Wiedergabe versehentlich auslöst.</span><span class="sxs-lookup"><span data-stu-id="4c555-126">If the SHIFT key is also used in the game, the user could accidentally trigger this shortcut during game play.</span></span> <span data-ttu-id="4c555-127">Wenn die Verknüpfung ausgelöst wird, zeigt Windows (standardmäßig) eine Warnung in einem Dialogfeld an, das dazu führen würde, dass Windows ein Spiel im Vollbildmodus minimiert.</span><span class="sxs-lookup"><span data-stu-id="4c555-127">When the shortcut is triggered, Windows (by default) presents a warning in a dialog box, which would cause Windows to minimize a game running in full-screen mode.</span></span> <span data-ttu-id="4c555-128">Dies kann natürlich eine drastische Auswirkung auf Spiele spielen.</span><span class="sxs-lookup"><span data-stu-id="4c555-128">This, of course, can have a drastic effect on game play.</span></span>

<span data-ttu-id="4c555-129">Die Barrierefreiheits Funktionen sind für einige Kunden erforderlich und stören sich nicht selbst durch voll Bild Spiele. Daher sollten Sie die Barrierefreiheits Einstellungen nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="4c555-129">The accessibility features are required for some customers and do not themselves interfere with full-screen games; therefore, you should not change the accessibility settings.</span></span> <span data-ttu-id="4c555-130">Da die Verknüpfungen für Barrierefreiheits Features das Spielen von spielen unterbrechen können, wenn Sie versehentlich ausgelöst werden, sollten Sie eine Eingabe Hilfen nur dann deaktivieren, wenn diese Funktion nicht durch Aufrufen von [**SystemParametersInfo**](/previous-versions/visualstudio/visual-studio-6.0/aa227580(v=vs.60))aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="4c555-130">However, because the shortcuts for accessibility features can disrupt game play if triggered accidentally, you should turn off an accessibility shortcut only when that feature is not enabled by calling [**SystemParametersInfo**](/previous-versions/visualstudio/visual-studio-6.0/aa227580(v=vs.60)).</span></span>

<span data-ttu-id="4c555-131">Eine von [**SystemParametersInfo**](/previous-versions/visualstudio/visual-studio-6.0/aa227580(v=vs.60)) deaktivierte Barrierefreiheits Verknüpfung bleibt deaktiviert, auch nachdem die Anwendung beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="4c555-131">An accessibility shortcut that is turned off by [**SystemParametersInfo**](/previous-versions/visualstudio/visual-studio-6.0/aa227580(v=vs.60)) remains turned off even after the application has exited.</span></span> <span data-ttu-id="4c555-132">Dies bedeutet, dass Sie die Einstellungen wiederherstellen müssen, bevor Sie die Anwendung beenden.</span><span class="sxs-lookup"><span data-stu-id="4c555-132">This means that you must restore the settings before exiting the application.</span></span> <span data-ttu-id="4c555-133">Da es möglich ist, dass die Anwendung nicht ordnungsgemäß beendet wird, sollten Sie diese Einstellungen in den persistenten Speicher schreiben, damit Sie wieder hergestellt werden können, wenn die Anwendung erneut ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4c555-133">Because it is possible for the application to fail to exit correctly, you should write these settings to persistent storage so that they can be restored when the application is run again.</span></span> <span data-ttu-id="4c555-134">Sie können auch einen Ausnahmehandler verwenden, um diese Einstellungen wiederherzustellen, wenn ein Absturz auftritt.</span><span class="sxs-lookup"><span data-stu-id="4c555-134">You could also use an exception handler to restore these settings if a crash occurs.</span></span>

<span data-ttu-id="4c555-135">**So deaktivieren Sie diese Tastenkombinationen**</span><span class="sxs-lookup"><span data-stu-id="4c555-135">**To turn off these shortcuts**</span></span>

1.  <span data-ttu-id="4c555-136">Erfassen Sie die aktuellen Barrierefreiheits Einstellungen, bevor Sie Sie deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="4c555-136">Capture the current accessibility settings before disabling them.</span></span>
2.  <span data-ttu-id="4c555-137">Deaktivieren Sie die Barrierefreiheits Verknüpfung, wenn die Anwendung in den Vollbildmodus wechselt, wenn die Barrierefreiheits Funktion deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="4c555-137">Disable the accessibility shortcut when the application goes into full-screen mode if the accessibility feature is off.</span></span>
3.  <span data-ttu-id="4c555-138">Stellen Sie die Barrierefreiheits Einstellungen wieder her, wenn die Anwendung in den Fenstermodus wechselt oder beendet wird.</span><span class="sxs-lookup"><span data-stu-id="4c555-138">Restore the accessibility settings when the application goes into windowed mode or exits.</span></span>

<span data-ttu-id="4c555-139">Diese Methode wird in dxut verwendet und wird im folgenden Codebeispiel veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="4c555-139">This method is used in DXUT, and is illustrated in the following code example.</span></span>

> [!Note]  
> <span data-ttu-id="4c555-140">Diese Methode funktioniert, wenn Sie mit einem eingeschränkten Benutzerkonto ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4c555-140">This method works when running on a limited user account.</span></span>

 

<span data-ttu-id="4c555-141">**Beispiel 2: Deaktivieren von Barrierefreiheits-Tastenkombinationen**</span><span class="sxs-lookup"><span data-stu-id="4c555-141">**Example 2. Disabling accessibility shortcut keys**</span></span>


```C++
STICKYKEYS g_StartupStickyKeys = {sizeof(STICKYKEYS), 0};
TOGGLEKEYS g_StartupToggleKeys = {sizeof(TOGGLEKEYS), 0};
FILTERKEYS g_StartupFilterKeys = {sizeof(FILTERKEYS), 0};    
 
 
INT WINAPI WinMain( HINSTANCE, HINSTANCE, LPSTR, int )
{
    // Save the current sticky/toggle/filter key settings so they can be restored them later
    SystemParametersInfo(SPI_GETSTICKYKEYS, sizeof(STICKYKEYS), &g_StartupStickyKeys, 0);
    SystemParametersInfo(SPI_GETTOGGLEKEYS, sizeof(TOGGLEKEYS), &g_StartupToggleKeys, 0);
    SystemParametersInfo(SPI_GETFILTERKEYS, sizeof(FILTERKEYS), &g_StartupFilterKeys, 0);
 
    // Disable when full screen
    AllowAccessibilityShortcutKeys( true );
 
    // Restore back when going to windowed or shutting down
    AllowAccessibilityShortcutKeys( false );
}
 
 
void AllowAccessibilityShortcutKeys( bool bAllowKeys )
{
    if( bAllowKeys )
    {
        // Restore StickyKeys/etc to original state and enable Windows key      
        STICKYKEYS sk = g_StartupStickyKeys;
        TOGGLEKEYS tk = g_StartupToggleKeys;
        FILTERKEYS fk = g_StartupFilterKeys;
        
        SystemParametersInfo(SPI_SETSTICKYKEYS, sizeof(STICKYKEYS), &g_StartupStickyKeys, 0);
        SystemParametersInfo(SPI_SETTOGGLEKEYS, sizeof(TOGGLEKEYS), &g_StartupToggleKeys, 0);
        SystemParametersInfo(SPI_SETFILTERKEYS, sizeof(FILTERKEYS), &g_StartupFilterKeys, 0);
    }
    else
    {
        // Disable StickyKeys/etc shortcuts but if the accessibility feature is on, 
        // then leave the settings alone as its probably being usefully used
 
        STICKYKEYS skOff = g_StartupStickyKeys;
        if( (skOff.dwFlags & SKF_STICKYKEYSON) == 0 )
        {
            // Disable the hotkey and the confirmation
            skOff.dwFlags &= ~SKF_HOTKEYACTIVE;
            skOff.dwFlags &= ~SKF_CONFIRMHOTKEY;
 
            SystemParametersInfo(SPI_SETSTICKYKEYS, sizeof(STICKYKEYS), &skOff, 0);
        }
 
        TOGGLEKEYS tkOff = g_StartupToggleKeys;
        if( (tkOff.dwFlags & TKF_TOGGLEKEYSON) == 0 )
        {
            // Disable the hotkey and the confirmation
            tkOff.dwFlags &= ~TKF_HOTKEYACTIVE;
            tkOff.dwFlags &= ~TKF_CONFIRMHOTKEY;
 
            SystemParametersInfo(SPI_SETTOGGLEKEYS, sizeof(TOGGLEKEYS), &tkOff, 0);
        }
 
        FILTERKEYS fkOff = g_StartupFilterKeys;
        if( (fkOff.dwFlags & FKF_FILTERKEYSON) == 0 )
        {
            // Disable the hotkey and the confirmation
            fkOff.dwFlags &= ~FKF_HOTKEYACTIVE;
            fkOff.dwFlags &= ~FKF_CONFIRMHOTKEY;
 
            SystemParametersInfo(SPI_SETFILTERKEYS, sizeof(FILTERKEYS), &fkOff, 0);
        }
    }
}
```



 

 