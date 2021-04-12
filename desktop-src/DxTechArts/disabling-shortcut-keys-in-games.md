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
# <a name="disabling-shortcut-keys-in-games"></a>Deaktivieren von Tastenkombinationen in spielen

In diesem Artikel wird beschrieben, wie Tastenkombinationen in Microsoft Windows vorübergehend deaktiviert werden, um die Unterbrechung von Spiel spielen bei voll Bild spielen zu verhindern. Die UMSCHALTTASTE und die STRG-Taste werden häufig als Feuer-oder Run-Schaltflächen in Spielen verwendet. Wenn Benutzer versehentlich die Windows-Taste drücken (in der Nähe dieser Tasten), können Sie dazu führen, dass Sie plötzlich aus der Anwendung herausspringt, was die Spiel Darstellung ruiniert. Wenn Sie einfach die Umschalttaste als Spiel Schaltfläche verwenden, kann die Tastenkombination "StickyKeys" versehentlich ausgeführt werden. Um diese Probleme zu vermeiden, sollten Sie diese Schlüssel bei der Ausführung im Vollbildmodus deaktivieren und die Schlüssel bei der Ausführung im Fenstermodus wieder für Ihre Standard Handler aktivieren oder die Anwendung beenden.

In diesem Artikel wird beschrieben, wie Sie die folgenden Schritte ausführen:

-   [Windows-Taste mit einem Tastatur Hook deaktivieren](#disable-the-windows-key-with-a-keyboard-hook)
-   [Deaktivieren der Tastenkombinationen für Barrierefreiheit](#disable-the-accessibility-shortcut-keys)

## <a name="disable-the-windows-key-with-a-keyboard-hook"></a>Windows-Taste mit einem Tastatur Hook deaktivieren

Verwenden Sie einen Tastatur Hook auf niedriger Ebene, um das Verarbeiten der Windows-Taste zu filtern. Der in Beispiel 1 angezeigte Tastatur Hook auf niedriger Ebene bleibt auch dann wirksam, wenn ein Benutzer das Fenster minimiert oder zu einer anderen Anwendung wechselt. Dies bedeutet, dass Sie darauf achten müssen, dass die Windows-Taste nicht deaktiviert ist, wenn die Anwendung deaktiviert wird. Der Code in Beispiel 1 bewirkt dies, indem die WM \_ activateapp-Nachricht verarbeitet wird.

> [!Note]  
> Diese Methode funktioniert unter Windows 2000 und neueren Versionen von Windows. Diese Methode funktioniert auch mit den Benutzerkonten mit den geringsten Rechten (auch als eingeschränkte Benutzerkonten bezeichnet).

 

Diese Methode wird von dxut verwendet und wird im folgenden Codebeispiel veranschaulicht.

**Beispiel 1. Verwenden eines Tastatur Hooks auf niedriger Ebene zum Deaktivieren der Windows-Taste**


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



## <a name="disable-the-accessibility-shortcut-keys"></a>Deaktivieren der Tastenkombinationen für Barrierefreiheit

Windows umfasst Barrierefreiheits Features wie z. b. "StickyKeys", "Filter Keys" und "degglekeys" (siehe [Windows-Barrierefreiheit](/previous-versions/visualstudio/visual-studio-6.0/aa227589(v=vs.60))). Jede dieser Dienste dient einem anderen Zweck: "StickyKeys" ist z. b. für Personen konzipiert, die Schwierigkeiten haben, zwei oder mehr Schlüssel gleichzeitig zu halten. Jede dieser Barrierefreiheits Features verfügt auch über eine Tastenkombination, mit der die Funktion aktiviert oder deaktiviert werden kann. Die Tastenkombination "StickyKeys" wird beispielsweise durch das fünfmal drücken der Umschalttaste ausgelöst. Wenn die Umschalttaste auch im Spiel verwendet wird, könnte der Benutzer diese Verknüpfung während der Spiel Wiedergabe versehentlich auslöst. Wenn die Verknüpfung ausgelöst wird, zeigt Windows (standardmäßig) eine Warnung in einem Dialogfeld an, das dazu führen würde, dass Windows ein Spiel im Vollbildmodus minimiert. Dies kann natürlich eine drastische Auswirkung auf Spiele spielen.

Die Barrierefreiheits Funktionen sind für einige Kunden erforderlich und stören sich nicht selbst durch voll Bild Spiele. Daher sollten Sie die Barrierefreiheits Einstellungen nicht ändern. Da die Verknüpfungen für Barrierefreiheits Features das Spielen von spielen unterbrechen können, wenn Sie versehentlich ausgelöst werden, sollten Sie eine Eingabe Hilfen nur dann deaktivieren, wenn diese Funktion nicht durch Aufrufen von [**SystemParametersInfo**](/previous-versions/visualstudio/visual-studio-6.0/aa227580(v=vs.60))aktiviert wird.

Eine von [**SystemParametersInfo**](/previous-versions/visualstudio/visual-studio-6.0/aa227580(v=vs.60)) deaktivierte Barrierefreiheits Verknüpfung bleibt deaktiviert, auch nachdem die Anwendung beendet wurde. Dies bedeutet, dass Sie die Einstellungen wiederherstellen müssen, bevor Sie die Anwendung beenden. Da es möglich ist, dass die Anwendung nicht ordnungsgemäß beendet wird, sollten Sie diese Einstellungen in den persistenten Speicher schreiben, damit Sie wieder hergestellt werden können, wenn die Anwendung erneut ausgeführt wird. Sie können auch einen Ausnahmehandler verwenden, um diese Einstellungen wiederherzustellen, wenn ein Absturz auftritt.

**So deaktivieren Sie diese Tastenkombinationen**

1.  Erfassen Sie die aktuellen Barrierefreiheits Einstellungen, bevor Sie Sie deaktivieren.
2.  Deaktivieren Sie die Barrierefreiheits Verknüpfung, wenn die Anwendung in den Vollbildmodus wechselt, wenn die Barrierefreiheits Funktion deaktiviert ist.
3.  Stellen Sie die Barrierefreiheits Einstellungen wieder her, wenn die Anwendung in den Fenstermodus wechselt oder beendet wird.

Diese Methode wird in dxut verwendet und wird im folgenden Codebeispiel veranschaulicht.

> [!Note]  
> Diese Methode funktioniert, wenn Sie mit einem eingeschränkten Benutzerkonto ausgeführt wird.

 

**Beispiel 2: Deaktivieren von Barrierefreiheits-Tastenkombinationen**


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



 

 