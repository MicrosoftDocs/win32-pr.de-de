---
title: Abrufen und Festlegen eines heißen Schlüssels
description: In diesem Thema wird veranschaulicht, wie die Tastenkombination für ein Hot Key-Steuerelement abgerufen oder festgelegt wird.
ms.assetid: F3643196-F847-4EE4-97ED-75AF52D4FF8D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fac5d0bab71fea11fe3d2aba23405f6d7ee7fb1ed8c78f2578f034ae9c84cad8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119079494"
---
# <a name="how-to-retrieve-and-set-a-hot-key"></a>Abrufen und Festlegen eines heißen Schlüssels

In diesem Thema wird veranschaulicht, wie die Tastenkombination für ein Hot Key-Steuerelement abgerufen oder festgelegt wird. Die [**Meldung HKM \_ SETHOTKEY**](hkm-sethotkey.md) ermöglicht einer Anwendung das Festlegen der Hot Key-Kombination für ein Hot Key-Steuerelement. Anwendungen verwenden die [**HKM \_ GETHOTKEY-Nachricht,**](hkm-gethotkey.md) um den virtuellen Schlüsselcode und die Modifiziererflags des hot-Schlüssels abzurufen, die vom Benutzer ausgewählt werden.

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   [Windows Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Windows Benutzeroberfläche-Programmierung

## <a name="instructions"></a>Anweisungen


Verwenden Sie [**die HKM \_ GETHOTKEY-Nachricht,**](hkm-gethotkey.md) um den Code des virtuellen Schlüssels und die Modifiziererschlüssel abzurufen, die einen vom Benutzer gewählten hot-Schlüssel beschreiben. Verwenden Sie die [**\_ HKM-Nachricht SETHOTKEY,**](hkm-sethotkey.md) um diese Werte für einen hot-Schlüssel zu setzen.

Im folgenden C++-Codebeispiel verwendet die anwendungsdefinierte Funktion die [**HKM \_ GETHOTKEY-Nachricht,**](hkm-gethotkey.md) um eine Tastenkombination aus einem Hot Key-Steuerelement abzurufen, und verwendet dann die [**WM \_ SETHOTKEY-Nachricht,**](/windows/desktop/inputdev/wm-sethotkey) um einen globalen hot-Schlüssel festzulegen. Beachten Sie, dass Sie keinen globalen hot-Schlüssel für ein Fenster mit dem [**WS \_ CHILD-Fensterstil**](/windows/desktop/winmsg/window-styles) festlegen können.



```C++
// Retrieves the hot key from the hot key control and sets it as
// the hot key for the application's main window. 
//
// Parameters 
//     hwndHot  - Handle of the hot key control. 
//     hwndMain - Handle of the main window. 

BOOL WINAPI ProcessHotkey(HWND hwndHot, HWND hwndMain) 
{ 
    WORD wHotkey;  

    // Retrieve the hot key (virtual key code and modifiers). 
    wHotkey = (WORD) SendMessage(hwndHot, HKM_GETHOTKEY, 0, 0); 
    
    // Use the result as wParam for WM_SETHOTKEY. 
    SendMessage(hwndMain, WM_SETHOTKEY, wHotkey, 0); 
    return TRUE;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Referenz zum Hot Key-Steuerelement](bumper-hot-key-hot-key-control-reference.md)
</dt> <dt>

[Informationen zu Hot Key-Steuerelementen](hot-key-controls.md)
</dt> <dt>

[Verwenden von Hot Key-Steuerelementen](using-hot-key-controls.md)
</dt> </dl>

 

 