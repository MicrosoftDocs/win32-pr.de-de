---
title: Einbetten von nicht-Schaltflächen-Steuerelementen in Symbolleisten
description: Symbolleisten unterstützen nur Schaltflächen. Daher müssen Sie, wenn Ihre Anwendung eine andere Art von Kontrolle erfordert, ein untergeordnetes Fenster erstellen. Die folgende Abbildung zeigt eine Symbolleiste mit einem eingebetteten Bearbeitungs Steuerelement.
ms.assetid: 7B4DACEF-96BB-447E-AE8F-F55401C665E9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb8ae2189350b9ea2f4aaa0c3ea0b49727bd3415
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2020
ms.locfileid: "103858102"
---
# <a name="how-to-embed-nonbutton-controls-in-toolbars"></a>Einbetten von nicht-Schaltflächen-Steuerelementen in Symbolleisten

Symbolleisten unterstützen nur Schaltflächen. Daher müssen Sie, wenn Ihre Anwendung eine andere Art von Kontrolle erfordert, ein untergeordnetes Fenster erstellen. Die folgende Abbildung zeigt eine Symbolleiste mit einem eingebetteten Bearbeitungs Steuerelement.

![Screenshot eines Dialog Felds mit einem Bearbeitungs Steuerelement auf der Symbolleiste, vorangehenden drei Symbolleisten Symbolen](images/tb-withedit.png)

> [!Note]  
> Erwägen Sie die Verwendung von Grund leisten-Steuer [Elementen](rebar-controls.md) anstelle von Steuerelementen in Symbolleisten.

 

Jeder Fenstertyp kann auf einer Symbolleiste platziert werden. Im folgenden Beispielcode wird ein Bearbeitungs Steuerelement als untergeordnetes Element des Fensters Symbolleisten-Steuerelement hinzugefügt. Da die Symbolleiste erstellt und dann das Bearbeitungs Steuerelement hinzugefügt wurde, müssen Sie Platz für das Bearbeitungs Steuerelement bereitstellen. Eine Möglichkeit besteht darin, ein Trennzeichen als Platzhalter in der Symbolleiste hinzuzufügen und die Breite des Trenn Zeichens auf die Anzahl der Pixel festzulegen, die Sie reservieren möchten.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche

## <a name="instructions"></a>Anweisungen

### <a name="embed-a-nonbutton-control-in-a-toolbar"></a>Einbetten eines nonbutton-Steuer Elements in einer Symbolleiste

Der folgende Code Ausschnitt erstellt die Symbolleiste in der obigen Abbildung.


```C++
// IDM_NEW, IDM_OPEN, and IDM_SAVE are application-defined command constants.

HIMAGELIST g_hImageList = NULL;

HWND CreateToolbarWithEdit(HWND hWndParent)
{
    const int ImageListID = 0;    // Define some constants.
    const int bitmapSize  = 16;
    
    const int cx_edit = 100;      // Dimensions of edit control.
    const int cy_edit = 35;  

    TBBUTTON tbButtons[] =        // Toolbar buttons.
    {
        // The separator is set to the width of the edit control. 
        
        {cx_edit, 0, TBSTATE_ENABLED, BTNS_SEP, {0}, 0, -1},
        {STD_FILENEW, IDM_NEW, TBSTATE_ENABLED, BTNS_BUTTON, {0}, 0, 0},
        {STD_FILEOPEN, IDM_OPEN, TBSTATE_ENABLED, BTNS_BUTTON, {0}, 0, 0},
        {STD_FILESAVE, IDM_SAVE, TBSTATE_ENABLED, BTNS_BUTTON, {0}, 0, 0},
        {0, 0, TBSTATE_ENABLED, BTNS_SEP, {0}, 0, 0},
    };

    // Create the toolbar.
    HWND hWndToolbar = CreateWindowEx(0, TOOLBARCLASSNAME, L"Toolbar", 
                                      WS_CHILD | WS_VISIBLE | WS_BORDER, 
                                      0, 0, 0, 0,
                                      hWndParent, NULL, HINST_COMMCTRL, NULL);

    if (!hWndToolbar)
        return NULL;
    
    int numButtons = sizeof(tbButtons) / sizeof(TBBUTTON);

    // Create the image list.
    g_hImageList = ImageList_Create(bitmapSize, bitmapSize, // Dimensions of individual bitmaps.
                                    0,                      // Flags.
                                    numButtons, 0);

    // Set the image list.
    SendMessage(hWndToolbar, TB_SETIMAGELIST, (WPARAM)ImageListID, (LPARAM)g_hImageList);

    // Load the button images.
    SendMessage(hWndToolbar, TB_LOADIMAGES, (WPARAM)IDB_STD_SMALL_COLOR, (LPARAM)HINST_COMMCTRL);

    // Add buttons.
    SendMessage(hWndToolbar, TB_BUTTONSTRUCTSIZE, (WPARAM)sizeof(TBBUTTON), 0);
    SendMessage(hWndToolbar, TB_ADDBUTTONS,       (WPARAM)numButtons,       (LPARAM)&tbButtons);

    // Create the edit control child window.    
    HWND hWndEdit = CreateWindowEx(0L, L"Edit", NULL, 
                                   WS_CHILD | WS_BORDER | WS_VISIBLE | ES_LEFT | ES_AUTOVSCROLL | ES_MULTILINE, 
                                   0, 0, cx_edit, cy_edit, 
                                   hWndToolbar, (HMENU) IDM_EDIT, g_hInst, 0 );
    
    if (!hWndEdit)
    {
        DestroyWindow(hWndToolbar);
        ImageList_Destroy(g_hImageList);
        
        return NULL;
    }
    
    return hWndToolbar;    // Return the toolbar with the embedded edit control.
}
```



In diesem Beispiel werden die Dimensionen des untergeordneten Fensters hart codiert. Wenn Sie jedoch eine stabilere Anwendung erstellen möchten, ermitteln Sie die Größe der Symbolleiste, und legen Sie das Bearbeitungs Steuerelement Fenster an.

Möglicherweise möchten Sie, dass die Bearbeitungs Steuerelement-Benachrichtigungen zu einem anderen Fenster, z. b. dem übergeordneten Symbol der Symbolleiste Erstellen Sie hierzu das Bearbeitungs Steuerelement als untergeordnetes Element des übergeordneten Fensters der Symbolleiste. Ändern Sie dann das übergeordnete Element des Bearbeitungs Steuer Elements wie folgt in die Symbolleiste.


```
SetParent (hWndEdit, hWndToolbar);
```



Benachrichtigungen gelangen zum ursprünglichen übergeordneten Element. Aus diesem Grund werden die Bearbeitungs Steuerelement Meldungen an das übergeordnete Element der Symbolleiste gesendet, auch wenn sich das Bearbeitungsfenster im Symbolleisten Fenster befindet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Symbolleisten](using-toolbar-controls.md)
</dt> <dt>

[Demo zu allgemeinen Windows-Steuerelementen (cppwindowscommoncontrols)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




