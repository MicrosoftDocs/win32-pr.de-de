---
title: Erstellen eines Tree-View-Steuer Elements
description: Um ein Strukturansicht-Steuerelement zu erstellen, verwenden Sie die Funktion "kreatewindowex", die den WC- \_ TreeView-Wert für die Fenster Klasse angibt.
ms.assetid: FEC3BF62-3085-47D4-B82E-7BD7B34B397D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 136ec22cc4f3f88e57266a4c2ac88df542a39429
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104102431"
---
# <a name="how-to-create-a-tree-view-control"></a>Erstellen eines Tree-View-Steuer Elements

Um ein Strukturansicht-Steuerelement zu erstellen, verwenden Sie die Funktion " [**kreatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) ", die den [**WC- \_ TreeView**](common-control-window-classes.md) -Wert für die Fenster Klasse angibt. Die Strukturansicht-Fenster Klasse wird beim Laden der allgemeinen Steuerelement-DLL im Adressraum der Anwendung registriert. Um sicherzustellen, dass die dll geladen wird, verwenden Sie die Funktion [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) .

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche

## <a name="instructions"></a>Anweisungen

### <a name="create-an-instance-of-a-tree-view-control"></a>Erstellen einer Instanz eines Tree-View-Steuer Elements

Im folgenden Beispiel wird ein Strukturansicht-Steuerelement erstellt, dessen Größenanpassung an den Client Bereich des übergeordneten Fensters erfolgt. Außerdem werden Anwendungs definierte Funktionen verwendet, um dem Steuerelement eine Bildliste zuzuordnen und dem Steuerelement Elemente hinzuzufügen.


```C++
// Create a tree-view control. 
// Returns the handle to the new control if successful,
// or NULL otherwise. 
// hwndParent - handle to the control's parent window. 
// lpszFileName - name of the file to parse for tree-view items.
// g_hInst - the global instance handle.
// ID_TREEVIEW - the resource ID of the control.

HWND CreateATreeView(HWND hwndParent)
{ 
    RECT rcClient;  // dimensions of client area 
    HWND hwndTV;    // handle to tree-view control 

    // Ensure that the common control DLL is loaded. 
    InitCommonControls(); 

    // Get the dimensions of the parent window's client area, and create 
    // the tree-view control. 
    GetClientRect(hwndParent, &rcClient); 
    hwndTV = CreateWindowEx(0,
                            WC_TREEVIEW,
                            TEXT("Tree View"),
                            WS_VISIBLE | WS_CHILD | WS_BORDER | TVS_HASLINES, 
                            0, 
                            0, 
                            rcClient.right, 
                            rcClient.bottom,
                            hwndParent, 
                            (HMENU)ID_TREEVIEW, 
                            g_hInst, 
                            NULL); 

    // Initialize the image list, and add items to the control. 
    // InitTreeViewImageLists and InitTreeViewItems are application- 
    // defined functions, shown later. 
    if (!InitTreeViewImageLists(hwndTV) || 
                !InitTreeViewItems(hwndTV))
    { 
        DestroyWindow(hwndTV); 
        return FALSE; 
    } 
    return hwndTV;
} 
```



## <a name="remarks"></a>Bemerkungen

Wenn Sie ein Strukturansicht-Steuerelement erstellen, können Sie ihm auch eine [**WM- \_ setFont**](/windows/desktop/winmsg/wm-setfont) -Nachricht senden, um die Schriftart festzulegen, die für den Text verwendet werden soll. Sie sollten diese Nachricht vor dem Einfügen von Elementen senden. Standardmäßig wird in einer Strukturansicht die Symbol Titel Schriftart verwendet. Obwohl Sie die Schriftart pro Element mithilfe von [benutzerdefiniertem zeichnen](custom-draw.md)anpassen können, verwendet das Strukturansicht-Steuerelement die Dimensionen der Schriftart, die von der **WM- \_ setFont** -Nachricht angegeben werden, um den Abstand und das Layout zu bestimmen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Tree-View Steuerelementen](using-treeview.md)
</dt> <dt>

[Custdtv-Beispiel veranschaulicht benutzerdefiniertes Zeichnen in einem Tree-View-Steuerelement](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 