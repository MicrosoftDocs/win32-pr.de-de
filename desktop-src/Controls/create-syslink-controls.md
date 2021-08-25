---
title: Erstellen von SysLink-Steuerelementen
description: Sie implementieren die Links des SysLink-Steuerelements über Markup in der Initialisierungszeichenfolge des Steuerelements oder durch Senden einer LM \_ SETITEM-Nachricht.
ms.assetid: CEE02A87-D85A-4F4D-931D-2B1371320814
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b2b50e364a2701d52aa0ed62222b0901a66b6c4073891b7f9348fffc8997fdc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119878510"
---
# <a name="how-to-create-syslink-controls"></a>Erstellen von SysLink-Steuerelementen

Sie implementieren die Links des SysLink-Steuerelements über Markup in der Initialisierungszeichenfolge des Steuerelements oder durch Senden einer [**LM \_ SETITEM-Nachricht.**](lm-setitem.md)

> [!Note]  
> Vor dem Erstellen von SysLink-Steuerelementen müssen Sie die [**InitCommonControlsEx-Funktion**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) aufrufen und dabei die LINKS \_ LINK CLASS \_ angeben.

 

Um einen SysLink zu erstellen, rufen Sie die [**CreateWindow-**](/windows/desktop/api/winuser/nf-winuser-createwindowa) oder [**CreateWindowEx-Funktion**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) auf und geben die [**WC \_ LINK-Fensterklasse**](common-control-window-classes.md) an. Der *lpWindowName-Parameter,* der diesen Funktionen gemeinsam ist, gibt einen Zeiger auf eine auf null endende Zeichenfolge an, die den anzuzeigenden markierten Text enthält. Spezifische Fensterstile für SysLink-Steuerelemente finden Sie unter [SysLink-Steuerelementstile.](syslink-control-styles.md)

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   [Windows Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Windows Benutzeroberfläche-Programmierung

## <a name="instructions"></a>Anweisungen

### <a name="create-a-syslink-control"></a>Erstellen eines SysLink-Steuerelements

Der folgende Beispielcode erstellt ein SysLink-Steuerelement, das zwei Links anzeigt. Der erste Link ist eine Internet-URL, der zweite ist anwendungsdefiniert.


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



## <a name="remarks"></a>Hinweise

Es wird davon ausgegangen, dass [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) bereits aufgerufen wurde.

Die Angabe des [**WS \_ TABSTOP-Stils**](/windows/desktop/winmsg/window-styles) stellt sicher, dass der Benutzer einen Link auswählen kann, indem er mit der TAB-TASTE darauf klickt und die EINGABETASTE drückt.

Version 6 von ComCtl32.dll unterstützt nur Unicode. Daher können Sie keine ANSI-Versionen von SysLink-Steuerelementen erstellen– nur Unicode.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von SysLink-Steuerelementen](/windows/desktop/Controls/using-syslink-controls)
</dt> <dt>

[Demo Windows allgemeinen Steuerelementen (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 