---
title: Erstellen eines Eigenschaftenblatts
description: Im Beispiel in diesem Abschnitt wird ein Eigenschaften Blatt mit zwei Seiten \ 8212 erstellt; eines zum Festlegen der Schriftart Eigenschaften einer Zelle in einer Kalkulations Tabelle und ein weiteres zum Festlegen der Rahmen Eigenschaften der Zelle.
ms.assetid: 61ACF87A-938C-4487-ACEB-484FCB677C6A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d15abd44f3a583afd99c5d943b9105c8734b73c1
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/19/2021
ms.locfileid: "106350743"
---
# <a name="how-to-create-a-property-sheet"></a>Erstellen eines Eigenschaftenblatts

Im Beispiel in diesem Abschnitt wird ein Eigenschaften Blatt erstellt, das zwei Seiten enthält – eine zum Festlegen der Schriftart Eigenschaften einer Zelle in einer Kalkulations Tabelle und eine weitere zum Festlegen der Rahmen Eigenschaften der Zelle.

Im Beispiel werden die Seiten definiert, indem ein paar von [**PROPSHEETPAGE**](pss-propsheetpage.md) -Strukturen gefüllt und die Adresse in der [**propsheetheiader**](pss-propsheetheader.md) -Struktur angegeben wird, die an die [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) -Funktion übermittelt wird.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche

## <a name="instructions"></a>Anweisungen

### <a name="create-a-property-sheet"></a>Erstellen eines Eigenschaften Blatts

Im folgenden Codebeispiel wird veranschaulicht, wie ein zwei – Page-Eigenschaften Blatt erstellt wird.


```C++
// DoPropertySheet - creates a property sheet that contains two pages.
//
// hwndOwner - handle to the owner window of the property sheet.
//
// Global variables
//     g_hinst - instance handle

extern HINSTANCE g_hinst;

VOID DoPropertySheet(HWND hwndOwner)
{
    PROPSHEETPAGE psp[2];
    
    PROPSHEETHEADER psh;
    
    psp[0].dwSize      = sizeof(PROPSHEETPAGE);
    psp[0].dwFlags     = PSP_USEICONID | PSP_USETITLE;
    psp[0].hInstance   = g_hinst;
    psp[0].pszTemplate = MAKEINTRESOURCE(DLG_FONT);
    psp[0].pszIcon     = MAKEINTRESOURCE(IDI_FONT);
    psp[0].pfnDlgProc  = FontDialogProc;
    psp[0].pszTitle    = MAKEINTRESOURCE(IDS_FONT)
    psp[0].lParam      = 0;
    psp[0].pfnCallback = NULL;
    psp[1].dwSize      = sizeof(PROPSHEETPAGE);
    psp[1].dwFlags     = PSP_USEICONID | PSP_USETITLE;
    psp[1].hInstance   = g_hinst;
    psp[1].pszTemplate = MAKEINTRESOURCE(DLG_BORDER);
    psp[1].pszIcon     = MAKEINTRESOURCE(IDI_BORDER);
    psp[1].pfnDlgProc  = BorderDialogProc;
    psp[1].pszTitle    = MAKEINTRESOURCE(IDS_BORDER);
    psp[1].lParam      = 0;
    psp[1].pfnCallback = NULL;
    
    psh.dwSize      = sizeof(PROPSHEETHEADER);
    psh.dwFlags     = PSH_USEICONID | PSH_PROPSHEETPAGE;
    psh.hwndParent  = hwndOwner;
    psh.hInstance   = g_hinst;
    psh.pszIcon     = MAKEINTRESOURCE(IDI_CELL_PROPERTIES);
    psh.pszCaption  = (LPSTR) "Cell Properties";
    psh.nPages      = sizeof(psp) / sizeof(PROPSHEETPAGE);
    psh.nStartPage  = 0;
    psh.ppsp        = (LPCPROPSHEETPAGE) &psp;
    psh.pfnCallback = NULL;
    
    PropertySheet(&psh);
    
    return;
}
```



## <a name="remarks"></a>Bemerkungen

Die Dialogfeld Vorlagen, Symbole und Bezeichnungen für die Seiten werden aus den Ressourcen geladen, die in der ausführbaren Datei der Anwendung enthalten sind. Das Symbol für das Eigenschaften Blatt wird auch aus den Ressourcen der Anwendung geladen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Eigenschaften Blättern](using-property-sheets.md)
</dt> <dt>

[Eigenschafts Beispiel](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/controls/common/property)
</dt> </dl>

 

 




