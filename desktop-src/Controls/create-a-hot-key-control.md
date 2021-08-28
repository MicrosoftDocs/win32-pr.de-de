---
title: Erstellen eines Hot Key-Steuerelements
description: In diesem Thema wird veranschaulicht, wie Sie ein Hot-Key-Steuerelement erstellen. Sie erstellen ein Hot-Key-Steuerelement, indem Sie die CreateWindowEx-Funktion verwenden und die \_ HOTKEY CLASS-Fensterklasse angeben.
ms.assetid: A6723D4E-B8F6-4365-8FCD-99B73D2C0470
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 081db39f07e8d80fcbb5a437bc8cbe83473b4299282c8b2437d95acda02b2db9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119577041"
---
# <a name="how-to-create-a-hot-key-control"></a>Erstellen eines Hot Key-Steuerelements

In diesem Thema wird veranschaulicht, wie Sie ein Hot-Key-Steuerelement erstellen. Sie erstellen ein Hot-Key-Steuerelement, indem Sie die [**CreateWindowEx-Funktion**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) verwenden und die \_ HOTKEY CLASS-Fensterklasse angeben.

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   [Windows Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Windows Benutzeroberfläche-Programmierung

## <a name="instructions"></a>Anweisungen


Stellen Sie vor dem Erstellen des Hot-Key-Steuerelements sicher, dass die DLL der allgemeinen Steuerelemente geladen ist.

Im folgenden C++-Codebeispiel ruft die anwendungsdefinierte Funktion die [**InitCommonControlsEx-Funktion**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) auf, um die allgemeine Steuerelement-DLL zu laden. Anschließend ruft sie die [**CreateWindowEx-Funktion**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) auf und gibt die **HOTKEY \_ CLASS-Fensterklasse** an, um ein Hot-Key-Steuerelement zu erstellen. Er verwendet die [**HKM \_ SETRULES-**](hkm-setrules.md) und [**HKM \_ SETHOTKEY-Meldungen,**](hkm-sethotkey.md) um das Steuerelement zu initialisieren, und gibt ein Handle an das Steuerelement zurück.

Mit diesem Hot Key-Steuerelement kann der Benutzer weder einen hot-Schlüssel auswählen, bei dem es sich um einen einzelnen unveränderten Schlüssel handelt, noch erlaubt es dem Benutzer, nur UMSCHALTTASTE und einen Schlüssel auszuwählen. Diese Regeln verhindern effektiv, dass der Benutzer einen Hot-Key auswählt, der beim Eingeben von Text versehentlich eingegeben wird.



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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Referenz zum Hot-Key-Steuerelement](bumper-hot-key-hot-key-control-reference.md)
</dt> <dt>

[Informationen zu Hot-Key-Steuerelementen](hot-key-controls.md)
</dt> <dt>

[Verwenden von Hot-Key-Steuerelementen](using-hot-key-controls.md)
</dt> </dl>

 

 