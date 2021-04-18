---
title: Abrufen und Festlegen einer Abkürzungs Taste
description: In diesem Thema wird veranschaulicht, wie Sie die Tastenkombination für ein Hot Key-Steuerelement abrufen oder festlegen.
ms.assetid: F3643196-F847-4EE4-97ED-75AF52D4FF8D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d453433917c211bc787f70a5d9344f1a477858e
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "106340545"
---
# <a name="how-to-retrieve-and-set-a-hot-key"></a>Abrufen und Festlegen einer Abkürzungs Taste

In diesem Thema wird veranschaulicht, wie Sie die Tastenkombination für ein Hot Key-Steuerelement abrufen oder festlegen. Die [**HKM \_ SetHotKey**](hkm-sethotkey.md) -Nachricht ermöglicht einer Anwendung die Festlegung der Tastenkombination für ein Hot Key-Steuerelement. Anwendungen verwenden die [**HKM \_ GetHotKey**](hkm-gethotkey.md) -Nachricht, um den Code des virtuellen Schlüssels und die Modifiziererflags des vom Benutzer ausgewählten Hot Key abzurufen.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche

## <a name="instructions"></a>Anweisungen


Verwenden Sie die [**HKM \_ GetHotKey**](hkm-gethotkey.md) -Nachricht, um den Code des virtuellen Schlüssels und die modifiziererschlüssel abzurufen, die einen vom Benutzer ausgewählten Kürzungs Schlüssel beschreiben. Verwenden Sie die [**HKM \_ SetHotKey**](hkm-sethotkey.md) -Nachricht, um diese Werte für einen Hot Key festzulegen.

Im folgenden C++-Codebeispiel verwendet die Anwendungs definierte Funktion die [**HKM \_ GetHotKey**](hkm-gethotkey.md) -Nachricht, um eine Tastenkombination aus einem Abkürzungs Schlüssel-Steuerelement abzurufen, und verwendet dann die [**WM \_ SetHotKey**](/windows/desktop/inputdev/wm-sethotkey) -Nachricht, um eine globale Hot Key-Nachricht festzulegen. Beachten Sie, dass Sie keine globale Taste für ein Fenster mit dem untergeordneten Fenster Stil von [**WS \_**](/windows/desktop/winmsg/window-styles) festlegen können.



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

[Referenz zur Hot Key-Steuerung](bumper-hot-key-hot-key-control-reference.md)
</dt> <dt>

[Informationen zu Hot Key-Steuerelementen](hot-key-controls.md)
</dt> <dt>

[Verwenden von Hot Key-Steuerelementen](using-hot-key-controls.md)
</dt> </dl>

 

 