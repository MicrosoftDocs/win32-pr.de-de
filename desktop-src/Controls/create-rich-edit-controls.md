---
title: Erstellen von Rich-Edit-Steuerelementen
description: Zum Erstellen eines Rich-Edit-Steuer Elements rufen Sie die Funktion "kreatewindowex" auf, und geben Sie die Rich-Bearbeitungsfenster Klasse an
ms.assetid: E0F3E458-7907-42BD-841A-CB3D12628AA8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6585e606cc77b307bf41aa938ed49e8baecb1349
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104039658"
---
# <a name="how-to-create-rich-edit-controls"></a>Erstellen von Rich-Edit-Steuerelementen

Zum Erstellen eines Rich-Edit-Steuer Elements rufen Sie die Funktion " [**kreatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) " auf, und geben Sie die Rich-Bearbeitungsfenster Klasse an Geben Sie für Microsoft Rich Edit 4,1 (Msftedit.dll) die MSF- \_ Klasse als Fenster Klasse an. Geben Sie für alle früheren Versionen die RichEdit- \_ Klasse an. Weitere Informationen finden Sie unter [Versionen von Rich Edit](about-rich-edit-controls.md).

Rich Edit-Steuerelemente unterstützen die meisten Fenster Stile, die mit Bearbeitungs Steuerelementen und zusätzlichen Stilen verwendet werden. Wenn Sie mehr als eine Textzeile im Steuerelement zulassen möchten, sollten Sie das mehr [**\_ zeilige**](edit-control-styles.md) Fenster Format angeben. Weitere Informationen finden Sie unter [Rich Edit-Steuerelement Stile](rich-edit-control-styles.md).

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche

## <a name="instructions"></a>Anweisungen

### <a name="create-a-rich-edit-control"></a>Erstellen eines Rich-Edit-Steuer Elements

Die folgende Beispiel Funktion erstellt ein Rich-Edit-Steuerelement und initialisiert es mit Text.


```C++
HWND CreateRichEdit(HWND hwndOwner,        // Dialog box handle.
                    int x, int y,          // Location.
                    int width, int height, // Dimensions.
                    HINSTANCE hinst)       // Application or DLL instance.
{
    LoadLibrary(TEXT("Msftedit.dll"));
    
    HWND hwndEdit= CreateWindowEx(0, MSFTEDIT_CLASS, TEXT("Type here"),
        ES_MULTILINE | WS_VISIBLE | WS_CHILD | WS_BORDER | WS_TABSTOP, 
        x, y, width, height, 
        hwndOwner, NULL, hinst, NULL);
        
    return hwndEdit;
}
```



In Microsoft Visual Studio 2005 und höher ist es möglich, ein umfangreiches Bearbeitungs Steuerelement zu einer Dialogfeld Vorlage hinzuzufügen, indem Sie das Steuerelement aus der Toolbox ziehen. Dadurch wird jedoch nicht sichergestellt, dass die erforderliche Bibliothek geladen wird, bevor das Steuerelement erstellt wird. Die [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion muss aufgerufen werden, um Riched32.dll, Riched20.dll oder Msftedit.dll zu laden, bevor das Dialogfeld erstellt wird.

## <a name="remarks"></a>Bemerkungen

Um visuelle Stile mit diesen Steuerelementen zu verwenden, muss eine Anwendung ein Manifest einschließen und die [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) -Funktion am Anfang des Programms aufruft. Weitere Informationen zu visuellen Stilen finden Sie unter [visuelle Stile](themes-overview.md). Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Rich Edit-Steuerelementen](using-rich-edit-controls.md)
</dt> <dt>

[Demo zu allgemeinen Windows-Steuerelementen (cppwindowscommoncontrols)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 