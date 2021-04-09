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
# <a name="how-to-create-a-hot-key-control"></a>Erstellen eines Steuer Elements für ein Hot Key

In diesem Thema wird veranschaulicht, wie Sie ein Steuerelement für den Hot Key erstellen Sie erstellen ein Hot Key-Steuerelement, indem Sie [**die Funktion "" der**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) Klasse "Hotkey" angeben und die Fenster Klasse "Hotkey Class" angeben \_ .

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche

## <a name="instructions"></a>Anweisungen


Vergewissern Sie sich, dass die DLL für allgemeine Steuerelemente geladen ist, bevor Sie das Steuerelement für den Hot Key erstellen

Im folgenden C++-Codebeispiel ruft die Anwendungs definierte Funktion die [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) -Funktion auf, um die allgemeine Steuerelement-DLL zu laden. Anschließend wird die Funktion " [**roatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) " aufgerufen, die die Klasse " **Hotkey \_ Class** Window" angibt, um ein Steuerelement für den Hot Key zu erstellen. Er verwendet die [**HKM \_**](hkm-setrules.md) -Meldungen "SKM" und " [**HKM \_**](hkm-sethotkey.md) ", um das Steuerelement zu initialisieren, und gibt ein Handle für das Steuerelement zurück.

Mit diesem Hot Key-Steuerelement kann der Benutzer keine heiße Taste auswählen, bei der es sich um eine einzelne nicht geänderte Taste handelt, und es ist auch nicht möglich, die UMSCHALTTASTE und eine Taste auszuwählen. Diese Regeln verhindern effektiv, dass der Benutzer eine heiße Taste wählt, die bei der Eingabe von Text versehentlich eingegeben werden kann.



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

[Referenz zur Hot Key-Steuerung](bumper-hot-key-hot-key-control-reference.md)
</dt> <dt>

[Informationen zu Hot Key-Steuerelementen](hot-key-controls.md)
</dt> <dt>

[Verwenden von Hot Key-Steuerelementen](using-hot-key-controls.md)
</dt> </dl>

 

 