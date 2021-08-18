---
title: Deaktivieren von Tastenkombinationen in Spielen
description: In diesem Artikel wird beschrieben, wie Tastenkombinationen in Microsoft Windows vorübergehend deaktiviert werden, um eine Unterbrechung des Spielspiels für Vollbild-Spiele zu verhindern.
ms.assetid: 732523f9-ecff-c6c2-646d-1bc3443232ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08eae2ee1b30e78b17440f2c6144c529de4e6d7b6272a5d497de5c5e631ac1c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119070520"
---
# <a name="disabling-shortcut-keys-in-games"></a>Deaktivieren von Tastenkombinationen in Spielen

In diesem Artikel wird beschrieben, wie Tastenkombinationen in Microsoft Windows vorübergehend deaktiviert werden, um eine Unterbrechung des Spielspiels für Vollbild-Spiele zu verhindern. Die UMSCHALTTASTE und die STRG-TASTE werden in Spielen häufig als Schaltflächen zum Starten oder Ausführen verwendet. Wenn Benutzer versehentlich die Windows Taste drücken (in der Nähe dieser Schlüssel), können sie dazu führen, dass sie plötzlich aus der Anwendung springen, was die Spielerfahrung verunfällt. Wenn Sie einfach die UMSCHALTTASTE als Spielschaltfläche verwenden, kann versehentlich die Tastenkombination StickyKeys ausgeführt werden, die möglicherweise ein Warndialogfeld anzeigt. Um diese Probleme zu vermeiden, sollten Sie diese Schlüssel bei der Ausführung im Vollbildmodus deaktivieren und die Schlüssel entweder wieder zu ihren Standardhandlern aktivieren, wenn sie im Fenstermodus ausgeführt werden, oder die Anwendung beenden.

In diesem Artikel wird folgende Vorgehensweise beschrieben:

-   [Deaktivieren der Windows-Taste mit einem Tastaturhook](#disable-the-windows-key-with-a-keyboard-hook)
-   [Deaktivieren der Tastenkombinationen für die Barrierefreiheit](#disable-the-accessibility-shortcut-keys)

## <a name="disable-the-windows-key-with-a-keyboard-hook"></a>Deaktivieren der Windows-Taste mit einem Tastaturhook

Verwenden Sie einen Low-Level-Tastaturhook, um die Windows Taste aus der Verarbeitung herauszufiltern. Der in Beispiel 1 gezeigte Tastaturhook auf niedriger Ebene bleibt auch dann wirksam, wenn ein Benutzer das Fenster minimiert oder zu einer anderen Anwendung wechselt. Dies bedeutet, dass Sie darauf achten müssen, dass der Windows Schlüssel nicht deaktiviert ist, wenn die Anwendung deaktiviert wird. Der Code in Beispiel 1 behandelt dazu die WM \_ ACTIVATEAPP-Meldung.

> [!Note]  
> Diese Methode funktioniert mit Windows 2000 und neueren Versionen von Windows. Diese Methode funktioniert auch mit Benutzerkonten mit den geringsten Berechtigungen (auch als Eingeschränkte Benutzerkonten bezeichnet).

 

Diese Methode wird von DXUT verwendet und im folgenden Codebeispiel veranschaulicht.

**Beispiel 1. Verwenden eines Tastaturhooks auf niedriger Ebene zum Deaktivieren der Windows-Taste**


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



## <a name="disable-the-accessibility-shortcut-keys"></a>Deaktivieren der Tastenkombinationen für die Barrierefreiheit

Windows enthält Barrierefreiheitsfunktionen wie StickyKeys, FilterKeys und ToggleKeys (siehe [Windows Accessibility](/previous-versions/visualstudio/visual-studio-6.0/aa227589(v=vs.60))). Jede dieser Ziele dient einem anderen Zweck. StickyKeys ist beispielsweise für Personen konzipiert, die Schwierigkeiten haben, zwei oder mehr Schlüssel gleichzeitig gedrückt zu halten. Jedes dieser Barrierefreiheitsfunktionen verfügt auch über eine Tastenkombination, mit der das Feature ein- oder ausgeschaltet werden kann. Beispielsweise wird die Tastenkombination StickyKeys ausgelöst, indem die UMSCHALTTASTE fünfmal gedrückt wird. Wenn die UMSCHALTTASTE auch im Spiel verwendet wird, könnte der Benutzer diese Verknüpfung versehentlich während des Spiels auslösen. Wenn die Verknüpfung ausgelöst wird, zeigt Windows (standardmäßig) eine Warnung in einem Dialogfeld an, was dazu führen würde, dass Windows ein Im Vollbildmodus ausgeführtes Spiel minimiert. Dies kann sich natürlich drastisch auf das Spiel auswirken.

Die Barrierefreiheitsfunktionen sind für einige Kunden erforderlich und beeinträchtigen nicht selbst Vollbildspiele. Daher sollten Sie die Barrierefreiheitseinstellungen nicht ändern. Da die Tastenkombinationen für Barrierefreiheitsfeatures jedoch die Spielwiedergabe unterbrechen können, wenn sie versehentlich ausgelöst werden, sollten Sie eine Tastenkombination für die Barrierefreiheit nur deaktivieren, wenn diese Funktion nicht aktiviert ist, indem [**Sie SystemParametersInfo**](/previous-versions/visualstudio/visual-studio-6.0/aa227580(v=vs.60))aufrufen.

Eine tastenkombination, die von [**SystemParametersInfo**](/previous-versions/visualstudio/visual-studio-6.0/aa227580(v=vs.60)) deaktiviert wird, bleibt auch nach dem Beenden der Anwendung deaktiviert. Dies bedeutet, dass Sie die Einstellungen wiederherstellen müssen, bevor Sie die Anwendung beenden. Da es möglich ist, dass die Anwendung nicht ordnungsgemäß beendet wird, sollten Sie diese Einstellungen in den persistenten Speicher schreiben, damit sie wiederhergestellt werden können, wenn die Anwendung erneut ausgeführt wird. Sie können auch einen Ausnahmehandler verwenden, um diese Einstellungen wiederherzustellen, wenn ein Absturz auftritt.

**So deaktivieren Sie diese Tastenkombinationen**

1.  Erfassen Sie die aktuellen Barrierefreiheitseinstellungen, bevor Sie sie deaktivieren.
2.  Deaktivieren Sie die Tastenkombination für die Barrierefreiheit, wenn die Anwendung in den Vollbildmodus wechselt, wenn die Barrierefreiheitsfunktion deaktiviert ist.
3.  Stellen Sie die Barrierefreiheitseinstellungen wieder her, wenn die Anwendung in den Fenstermodus wechselt oder beendet wird.

Diese Methode wird in DXUT verwendet und im folgenden Codebeispiel veranschaulicht.

> [!Note]  
> Diese Methode funktioniert bei der Ausführung in einem eingeschränkten Benutzerkonto.

 

**Beispiel 2. Deaktivieren von Tastenkombinationen für Barrierefreiheit**


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



 

 