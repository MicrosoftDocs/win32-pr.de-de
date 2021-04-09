---
title: Erstellen von Syslink-Steuerelementen
description: Sie implementieren die Hyperlinks des Syslink-Steuer Elements über das Markup in der Initialisierungs Zeichenfolge des Steuer Elements, oder indem Sie eine LM \_ SetItem-Nachricht senden.
ms.assetid: CEE02A87-D85A-4F4D-931D-2B1371320814
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77aa5c5ff3348f35f9c67cb34bea0cc495d403ef
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730656"
---
# <a name="how-to-create-syslink-controls"></a>Erstellen von Syslink-Steuerelementen

Sie implementieren die Hyperlinks des Syslink-Steuer Elements über das Markup in der Initialisierungs Zeichenfolge des Steuer Elements, oder indem Sie eine [**LM \_ SetItem**](lm-setitem.md) -Nachricht senden.

> [!Note]  
> Bevor Sie Syslink-Steuerelemente erstellen, müssen Sie die [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) -Funktion mit Angabe der "ICC Link"- \_ Klasse abrufen \_ .

 

Um einen Syslink zu erstellen, rufen Sie die Funktion "up [**Window**](/windows/desktop/api/winuser/nf-winuser-createwindowa) " oder " [**kreatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) " auf, und geben Sie die Fenster Klasse " [**WC- \_ Link**](common-control-window-classes.md) Der *lpWindowName* -Parameter, der diesen Funktionen gemeinsam ist, gibt einen Zeiger auf eine mit NULL endenden Zeichenfolge an, die den markierten Text enthält, der angezeigt werden soll. Informationen zu den in den Syslink-Steuerelementen spezifischen Fenster Formaten finden Sie unter [Syslink-Steuerelement Stile](syslink-control-styles.md)

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche

## <a name="instructions"></a>Anweisungen

### <a name="create-a-syslink-control"></a>Erstellen eines Syslink-Steuer Elements

Der folgende Beispielcode erstellt ein Syslink-Steuerelement, das zwei Hyperlinks anzeigt. Der erste Hyperlink ist eine Internet-URL, die zweite ist Anwendungs definiert.


```C++
HWND CreateSysLink(HWND hDlg, HINSTANCE hInst, RECT rect)
{
    return CreateWindowEx(0, WC_LINK, 
        L"For more information, <A HREF=\"https://www.microsoft.com\">click here</A> " \
        L"or <A ID=\"idInfo\">here</A>.", 
        WS_VISIBLE | WS_CHILD | WS_TABSTOP, 
        rect.left, rect.top, rect.right, rect.bottom, 
        hDlg, NULL, hInst, NULL);
}
```



## <a name="remarks"></a>Bemerkungen

Es wird davon ausgegangen, dass [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) bereits aufgerufen wurde.

Durch Angeben des [**WS- \_ Tabstopps**](/windows/desktop/winmsg/window-styles) -Stils wird sichergestellt, dass der Benutzer einen Link auswählen kann, indem er die Tab-Taste gedrückt und die EINGABETASTE drückt.

In Version 6 von ComCtl32.dll wird nur Unicode unterstützt. Daher können Sie keine ANSI-Versionen von Syslink-Steuerelementen erstellen – nur Unicode.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Syslink-Steuerelementen](/windows/desktop/Controls/using-syslink-controls)
</dt> <dt>

[Demo zu allgemeinen Windows-Steuerelementen (cppwindowscommoncontrols)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 