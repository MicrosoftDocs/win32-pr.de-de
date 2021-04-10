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
# <a name="how-to-create-rich-edit-controls"></a><span data-ttu-id="517e7-103">Erstellen von Rich-Edit-Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="517e7-103">How to Create Rich Edit Controls</span></span>

<span data-ttu-id="517e7-104">Zum Erstellen eines Rich-Edit-Steuer Elements rufen Sie die Funktion " [**kreatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) " auf, und geben Sie die Rich-Bearbeitungsfenster Klasse an</span><span class="sxs-lookup"><span data-stu-id="517e7-104">To create a rich edit control, call the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function, specifying the rich edit window class.</span></span> <span data-ttu-id="517e7-105">Geben Sie für Microsoft Rich Edit 4,1 (Msftedit.dll) die MSF- \_ Klasse als Fenster Klasse an.</span><span class="sxs-lookup"><span data-stu-id="517e7-105">For Microsoft Rich Edit 4.1 (Msftedit.dll), specify MSFTEDIT\_CLASS as the window class.</span></span> <span data-ttu-id="517e7-106">Geben Sie für alle früheren Versionen die RichEdit- \_ Klasse an.</span><span class="sxs-lookup"><span data-stu-id="517e7-106">For all previous versions, specify RICHEDIT\_CLASS.</span></span> <span data-ttu-id="517e7-107">Weitere Informationen finden Sie unter [Versionen von Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="517e7-107">For more information, see [Versions of Rich Edit](about-rich-edit-controls.md).</span></span>

<span data-ttu-id="517e7-108">Rich Edit-Steuerelemente unterstützen die meisten Fenster Stile, die mit Bearbeitungs Steuerelementen und zusätzlichen Stilen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="517e7-108">Rich edit controls support most of the window styles used with edit controls as well as additional styles.</span></span> <span data-ttu-id="517e7-109">Wenn Sie mehr als eine Textzeile im Steuerelement zulassen möchten, sollten Sie das mehr [**\_ zeilige**](edit-control-styles.md) Fenster Format angeben.</span><span class="sxs-lookup"><span data-stu-id="517e7-109">You should specify the [**ES\_MULTILINE**](edit-control-styles.md) window style if you want to allow more than one line of text in the control.</span></span> <span data-ttu-id="517e7-110">Weitere Informationen finden Sie unter [Rich Edit-Steuerelement Stile](rich-edit-control-styles.md).</span><span class="sxs-lookup"><span data-stu-id="517e7-110">For more information, see [Rich Edit Control Styles](rich-edit-control-styles.md).</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="517e7-111">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="517e7-111">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="517e7-112">Technologien</span><span class="sxs-lookup"><span data-stu-id="517e7-112">Technologies</span></span>

-   [<span data-ttu-id="517e7-113">Windows-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="517e7-113">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="517e7-114">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="517e7-114">Prerequisites</span></span>

-   <span data-ttu-id="517e7-115">C/C++</span><span class="sxs-lookup"><span data-stu-id="517e7-115">C/C++</span></span>
-   <span data-ttu-id="517e7-116">Programmieren der Windows-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="517e7-116">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="517e7-117">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="517e7-117">Instructions</span></span>

### <a name="create-a-rich-edit-control"></a><span data-ttu-id="517e7-118">Erstellen eines Rich-Edit-Steuer Elements</span><span class="sxs-lookup"><span data-stu-id="517e7-118">Create a Rich Edit Control</span></span>

<span data-ttu-id="517e7-119">Die folgende Beispiel Funktion erstellt ein Rich-Edit-Steuerelement und initialisiert es mit Text.</span><span class="sxs-lookup"><span data-stu-id="517e7-119">The following example function creates a rich edit control and initializes it with some text.</span></span>


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



<span data-ttu-id="517e7-120">In Microsoft Visual Studio 2005 und höher ist es möglich, ein umfangreiches Bearbeitungs Steuerelement zu einer Dialogfeld Vorlage hinzuzufügen, indem Sie das Steuerelement aus der Toolbox ziehen.</span><span class="sxs-lookup"><span data-stu-id="517e7-120">In Microsoft Visual Studio 2005 and later, it is possible to add a rich edit control into a dialog template by dragging the control from the toolbox.</span></span> <span data-ttu-id="517e7-121">Dadurch wird jedoch nicht sichergestellt, dass die erforderliche Bibliothek geladen wird, bevor das Steuerelement erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="517e7-121">However, doing this in the dialog editor does not ensure that the required library will be loaded before the control is created.</span></span> <span data-ttu-id="517e7-122">Die [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion muss aufgerufen werden, um Riched32.dll, Riched20.dll oder Msftedit.dll zu laden, bevor das Dialogfeld erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="517e7-122">It is necessary to call the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) function to load Riched32.dll, Riched20.dll, or Msftedit.dll before the dialog is created.</span></span>

## <a name="remarks"></a><span data-ttu-id="517e7-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="517e7-123">Remarks</span></span>

<span data-ttu-id="517e7-124">Um visuelle Stile mit diesen Steuerelementen zu verwenden, muss eine Anwendung ein Manifest einschließen und die [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) -Funktion am Anfang des Programms aufruft.</span><span class="sxs-lookup"><span data-stu-id="517e7-124">To use visual styles with these controls, an application must include a manifest and must call the [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) function at the beginning of the program.</span></span> <span data-ttu-id="517e7-125">Weitere Informationen zu visuellen Stilen finden Sie unter [visuelle Stile](themes-overview.md).</span><span class="sxs-lookup"><span data-stu-id="517e7-125">For information on visual styles, see [Visual Styles](themes-overview.md).</span></span> <span data-ttu-id="517e7-126">Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="517e7-126">For information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="517e7-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="517e7-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="517e7-128">Verwenden von Rich Edit-Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="517e7-128">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="517e7-129">[Demo zu allgemeinen Windows-Steuerelementen (cppwindowscommoncontrols)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="517e7-129">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 