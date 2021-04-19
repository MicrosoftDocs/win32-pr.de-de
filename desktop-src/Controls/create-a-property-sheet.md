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
# <a name="how-to-create-a-property-sheet"></a><span data-ttu-id="343d0-103">Erstellen eines Eigenschaftenblatts</span><span class="sxs-lookup"><span data-stu-id="343d0-103">How to Create a Property Sheet</span></span>

<span data-ttu-id="343d0-104">Im Beispiel in diesem Abschnitt wird ein Eigenschaften Blatt erstellt, das zwei Seiten enthält – eine zum Festlegen der Schriftart Eigenschaften einer Zelle in einer Kalkulations Tabelle und eine weitere zum Festlegen der Rahmen Eigenschaften der Zelle.</span><span class="sxs-lookup"><span data-stu-id="343d0-104">The example in this section creates a property sheet that contains two pages—one for setting the font properties of a cell in a spreadsheet, and another for setting the border properties of the cell.</span></span>

<span data-ttu-id="343d0-105">Im Beispiel werden die Seiten definiert, indem ein paar von [**PROPSHEETPAGE**](pss-propsheetpage.md) -Strukturen gefüllt und die Adresse in der [**propsheetheiader**](pss-propsheetheader.md) -Struktur angegeben wird, die an die [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) -Funktion übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="343d0-105">The example defines the pages by filling a pair of [**PROPSHEETPAGE**](pss-propsheetpage.md) structures and specifying the address in the [**PROPSHEETHEADER**](pss-propsheetheader.md) structure that is passed to the [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) function.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="343d0-106">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="343d0-106">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="343d0-107">Technologien</span><span class="sxs-lookup"><span data-stu-id="343d0-107">Technologies</span></span>

-   [<span data-ttu-id="343d0-108">Windows-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="343d0-108">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="343d0-109">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="343d0-109">Prerequisites</span></span>

-   <span data-ttu-id="343d0-110">C/C++</span><span class="sxs-lookup"><span data-stu-id="343d0-110">C/C++</span></span>
-   <span data-ttu-id="343d0-111">Programmieren der Windows-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="343d0-111">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="343d0-112">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="343d0-112">Instructions</span></span>

### <a name="create-a-property-sheet"></a><span data-ttu-id="343d0-113">Erstellen eines Eigenschaften Blatts</span><span class="sxs-lookup"><span data-stu-id="343d0-113">Create a Property Sheet</span></span>

<span data-ttu-id="343d0-114">Im folgenden Codebeispiel wird veranschaulicht, wie ein zwei – Page-Eigenschaften Blatt erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="343d0-114">The following code example demonstrates how to create a two–page property sheet.</span></span>


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



## <a name="remarks"></a><span data-ttu-id="343d0-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="343d0-115">Remarks</span></span>

<span data-ttu-id="343d0-116">Die Dialogfeld Vorlagen, Symbole und Bezeichnungen für die Seiten werden aus den Ressourcen geladen, die in der ausführbaren Datei der Anwendung enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="343d0-116">The dialog box templates, icons, and labels for the pages are loaded from the resources contained in the application's executable file.</span></span> <span data-ttu-id="343d0-117">Das Symbol für das Eigenschaften Blatt wird auch aus den Ressourcen der Anwendung geladen.</span><span class="sxs-lookup"><span data-stu-id="343d0-117">The icon for the property sheet is also loaded from the application's resources.</span></span>

## <a name="related-topics"></a><span data-ttu-id="343d0-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="343d0-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="343d0-119">Verwenden von Eigenschaften Blättern</span><span class="sxs-lookup"><span data-stu-id="343d0-119">Using Property Sheets</span></span>](using-property-sheets.md)
</dt> <dt>

[<span data-ttu-id="343d0-120">Eigenschafts Beispiel</span><span class="sxs-lookup"><span data-stu-id="343d0-120">Property sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/controls/common/property)
</dt> </dl>

 

 




