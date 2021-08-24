---
title: Erstellen eines ComboBoxEx-Steuerelements
description: In diesem Thema wird das Erstellen eines ComboBoxEx-Steuerelements veranschaulicht.
ms.assetid: E3D577AF-3290-431E-AA6C-1E9A9ED6448C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d051c668e95667948d11a8ec86ed41236f84ff78325911e008c65ad787b958fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119576130"
---
# <a name="how-to-create-a-comboboxex-control"></a>Erstellen eines ComboBoxEx-Steuerelements

In diesem Thema wird das Erstellen eines ComboBoxEx-Steuerelements veranschaulicht.

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   [Windows Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Windows Benutzeroberfläche-Programmierung

## <a name="instructions"></a>Anweisungen


Um ein ComboBoxEx-Steuerelement zu erstellen, rufen Sie die [**CreateWindowEx-Funktion**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) auf, indem Sie [**WC \_ COMBOBOXEX**](common-control-window-classes.md) als Fensterklasse verwenden. Sie müssen zuerst die Window-Klasse registrieren, indem Sie die [**InitCommonControlsEx-Funktion**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) aufrufen, während Sie das BIT FÜR DIE BENUTZEREX-KLASSEN des BENUTZERS INITCOMMONCONTROLSEX in der zugehörigen \_ \_ [**INITCOMMONCONTROLSEX-Struktur**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) angeben.

## <a name="complete-example"></a>Vollständiges Beispiel

Die folgende anwendungsdefinierte Funktion erstellt ein ComboBoxEx-Steuerelement mit dem [**\_ CBS-DROPDOWN-Stil**](combo-box-styles.md) im Hauptfenster.


```C++
// CreateComboEx - Registers the ComboBoxEx window class and creates
// a ComboBoxEx control in the client area of the main window.
//
// g_hwndMain - A handle to the main window.
// g_hinst    - A handle to the program instance.
HWND WINAPI CreateComboEx(void)
{
    HWND hwnd;
    INITCOMMONCONTROLSEX icex;

    icex.dwSize = sizeof(INITCOMMONCONTROLSEX);
    icex.dwICC = ICC_USEREX_CLASSES;

    InitCommonControlsEx(&icex);

    hwnd = CreateWindowEx(0, WC_COMBOBOXEX, NULL,
                    WS_BORDER | WS_VISIBLE |
                    WS_CHILD | CBS_DROPDOWN,
                    // No size yet--resize after setting image list.
                    0,      // Vertical position of Combobox
                    0,      // Horizontal position of Combobox
                    0,      // Sets the width of Combobox
                    100,    // Sets the height of Combobox
                    g_hwndMain,
                    NULL,
                    g_hinst,
                    NULL);

    return (hwnd);
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu ComboBoxEx-Steuerelementen](comboboxex-controls.md)
</dt> <dt>

[ComboBoxEx-Steuerelementreferenz](bumper-comboboxex-comboboxex-control-reference.md)
</dt> <dt>

[Verwenden von ComboBoxEx-Steuerelementen](/windows/desktop/Controls/using-comboboxex)
</dt> <dt>

[ComboBoxEx](comboboxex-control-reference.md)
</dt> </dl>

 

 