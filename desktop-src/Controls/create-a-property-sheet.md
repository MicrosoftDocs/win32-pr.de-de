---
title: Erstellen eines Eigenschaftenblatts
description: Im Beispiel in diesem Abschnitt wird ein Eigenschaftenblatt erstellt, das zwei Seiten \ 8212 enthält; eine zum Festlegen der Schriftarteigenschaften einer Zelle in einer Kalkulationstabelle und eine andere zum Festlegen der Rahmeneigenschaften der Zelle.
ms.assetid: 61ACF87A-938C-4487-ACEB-484FCB677C6A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fa99c3e678fa7d8e6aa70cd3f5c6e4c7bc514f94114c7bb7a411fa7df1caac3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117831846"
---
# <a name="how-to-create-a-property-sheet"></a>Erstellen eines Eigenschaftenblatts

Im Beispiel in diesem Abschnitt wird ein Eigenschaftenblatt erstellt, das zwei Seiten enthält: eine zum Festlegen der Schriftarteigenschaften einer Zelle in einer Kalkulationstabelle und eine andere zum Festlegen der Rahmeneigenschaften der Zelle.

Im Beispiel werden die Seiten definiert, indem ein Paar von [**PROPSHEETPAGE-Strukturen**](pss-propsheetpage.md) ausgefüllt und die Adresse in der [**PROPSHEETHEADER-Struktur**](pss-propsheetheader.md) angegeben wird, die an die [**PropertySheet-Funktion**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) übergeben wird.

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   [Windows Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Windows Benutzeroberfläche-Programmierung

## <a name="instructions"></a>Anweisungen

### <a name="create-a-property-sheet"></a>Erstellen eines Eigenschaftenblatts

Im folgenden Codebeispiel wird veranschaulicht, wie sie ein Eigenschaftenblatt mit zwei Seiten erstellen.


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



## <a name="remarks"></a>Hinweise

Die Dialogfeldvorlagen, Symbole und Bezeichnungen für die Seiten werden aus den Ressourcen geladen, die in der ausführbaren Datei der Anwendung enthalten sind. Das Symbol für das Eigenschaftenblatt wird auch aus den Ressourcen der Anwendung geladen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Eigenschaftenblättern](using-property-sheets.md)
</dt> <dt>

[Eigenschaftsbeispiel](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/controls/common/property)
</dt> </dl>

 

 




