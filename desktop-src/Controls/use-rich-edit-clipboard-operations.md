---
title: So verwenden Sie Rich-Edit-Zwischenablage Vorgänge
description: Eine Anwendung kann den Inhalt der Zwischenablage in ein Rich-Edit-Steuerelement einfügen, indem Sie entweder das beste verfügbare Zwischenablage Format oder ein bestimmtes Zwischenablage Format verwendet.
ms.assetid: 1FEFFD95-839B-4A26-A26E-B8429D5FF4C0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a46432054956914b484c9faeeeda78f2a18e132
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103949163"
---
# <a name="how-to-use-rich-edit-clipboard-operations"></a><span data-ttu-id="f5217-103">So verwenden Sie Rich-Edit-Zwischenablage Vorgänge</span><span class="sxs-lookup"><span data-stu-id="f5217-103">How to Use Rich Edit Clipboard Operations</span></span>

<span data-ttu-id="f5217-104">Eine Anwendung kann den Inhalt der Zwischenablage in ein Rich-Edit-Steuerelement einfügen, indem Sie entweder das beste verfügbare Zwischenablage Format oder ein bestimmtes Zwischenablage Format verwendet.</span><span class="sxs-lookup"><span data-stu-id="f5217-104">An application can paste the contents of the clipboard into a rich edit control by using either the best available clipboard format or a specific clipboard format.</span></span> <span data-ttu-id="f5217-105">Sie können auch bestimmen, ob ein Rich-Edit-Steuerelement in der Lage ist, ein Zwischenablage Format einzufügen.</span><span class="sxs-lookup"><span data-stu-id="f5217-105">You can also determine whether a rich edit control is capable of pasting a clipboard format.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="f5217-106">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="f5217-106">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="f5217-107">Technologien</span><span class="sxs-lookup"><span data-stu-id="f5217-107">Technologies</span></span>

-   [<span data-ttu-id="f5217-108">Windows-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="f5217-108">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="f5217-109">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="f5217-109">Prerequisites</span></span>

-   <span data-ttu-id="f5217-110">C/C++</span><span class="sxs-lookup"><span data-stu-id="f5217-110">C/C++</span></span>
-   <span data-ttu-id="f5217-111">Programmieren der Windows-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="f5217-111">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="f5217-112">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="f5217-112">Instructions</span></span>

### <a name="use-a-rich-edit-clipboard-operation"></a><span data-ttu-id="f5217-113">Verwenden eines Rich-Edit-Zwischenablage Vorgangs</span><span class="sxs-lookup"><span data-stu-id="f5217-113">Use a Rich Edit Clipboard Operation</span></span>

<span data-ttu-id="f5217-114">Wie bei einem Bearbeitungs Steuerelement können Sie den Inhalt der aktuellen Auswahl mithilfe der [**WM- \_ Kopier**](/windows/desktop/dataxchg/wm-copy) -oder der WM- [**\_ Ausschneide**](/windows/desktop/dataxchg/wm-cut) Nachricht kopieren oder Ausschneiden.</span><span class="sxs-lookup"><span data-stu-id="f5217-114">As with an edit control, you can copy or cut the contents of the current selection by using the [**WM\_COPY**](/windows/desktop/dataxchg/wm-copy) or [**WM\_CUT**](/windows/desktop/dataxchg/wm-cut) message.</span></span> <span data-ttu-id="f5217-115">Auf ähnliche Weise können Sie den Inhalt der Zwischenablage mithilfe der [**WM- \_ Einfüge**](/windows/desktop/dataxchg/wm-paste) Nachricht in ein Rich-Edit-Steuerelement einfügen.</span><span class="sxs-lookup"><span data-stu-id="f5217-115">Similarly, you can paste the contents of the clipboard into a rich edit control by using the [**WM\_PASTE**](/windows/desktop/dataxchg/wm-paste) message.</span></span> <span data-ttu-id="f5217-116">Das Steuerelement fügt das erste verfügbare Format, das es erkennt, ein, das vermutlich das beschreibende Format darstellt.</span><span class="sxs-lookup"><span data-stu-id="f5217-116">The control pastes the first available format that it recognizes, which presumably is the most descriptive format.</span></span>

<span data-ttu-id="f5217-117">Wenn Sie ein bestimmtes Zwischenablage Format einfügen möchten, können Sie die " [**EM \_ PasteSpecial**](em-pastespecial.md) "-Meldung verwenden.</span><span class="sxs-lookup"><span data-stu-id="f5217-117">To paste a specific clipboard format, you can use the [**EM\_PASTESPECIAL**](em-pastespecial.md) message.</span></span> <span data-ttu-id="f5217-118">Diese Meldung ist nützlich für Anwendungen mit einem **speziellen** Befehl zum Einfügen, mit dem Benutzer das Zwischenablage Format auswählen können.</span><span class="sxs-lookup"><span data-stu-id="f5217-118">This message is useful for applications with a **Paste Special** command that enables the user to select the clipboard format.</span></span> <span data-ttu-id="f5217-119">Sie können die [**EM \_ CanPaste**](em-canpaste.md) -Nachricht verwenden, um zu bestimmen, ob ein bestimmtes Format vom Steuerelement erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="f5217-119">You can use the [**EM\_CANPASTE**](em-canpaste.md) message to determine whether a given format is recognized by the control.</span></span>

<span data-ttu-id="f5217-120">Sie können auch die [**EM \_ CanPaste**](em-canpaste.md) -Nachricht verwenden, um zu bestimmen, ob ein verfügbares Zwischenablage Format von einem Rich Edit-Steuerelement erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="f5217-120">You can also use the [**EM\_CANPASTE**](em-canpaste.md) message to determine whether any available clipboard format is recognized by a rich edit control.</span></span> <span data-ttu-id="f5217-121">Diese Meldung ist nützlich, wenn die " [**WM \_ initmenupopup**](/windows/desktop/menurc/wm-initmenupopup) "-Meldung verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="f5217-121">This message is useful when processing the [**WM\_INITMENUPOPUP**](/windows/desktop/menurc/wm-initmenupopup) message.</span></span> <span data-ttu-id="f5217-122">Eine Anwendung kann den **Einfüge** Befehl in Abhängigkeit davon aktivieren oder grauen, ob das Steuerelement ein beliebiges verfügbares Format einfügen kann.</span><span class="sxs-lookup"><span data-stu-id="f5217-122">An application might enable or gray its **Paste** command depending on whether the control can paste any available format.</span></span>

<span data-ttu-id="f5217-123">Rich Edit-Steuerelemente registrieren zwei Zwischenablage Formate:</span><span class="sxs-lookup"><span data-stu-id="f5217-123">Rich edit controls register two clipboard formats:</span></span>

-   <span data-ttu-id="f5217-124">Rich Text Format</span><span class="sxs-lookup"><span data-stu-id="f5217-124">Rich Text Format</span></span>
-   <span data-ttu-id="f5217-125">Rich-Text-Format ohne Objekte</span><span class="sxs-lookup"><span data-stu-id="f5217-125">Rich Text Format Without Objects</span></span>
-   <span data-ttu-id="f5217-126">RichEdit-Text und-Objekte</span><span class="sxs-lookup"><span data-stu-id="f5217-126">RichEdit Text and Objects</span></span>

<span data-ttu-id="f5217-127">Eine Anwendung kann diese Formate mithilfe der [**RegisterClipboardFormat**](/windows/desktop/api/winuser/nf-winuser-registerclipboardformata) -Funktion registrieren und die Werte für die Werte "CF \_ RTF", "CF \_ RTF noobjs" und "CF \_ retextobj" angeben.</span><span class="sxs-lookup"><span data-stu-id="f5217-127">An application can register these formats by using the [**RegisterClipboardFormat**](/windows/desktop/api/winuser/nf-winuser-registerclipboardformata) function, specifying the CF\_RTF, CF\_RTFNOOBJS, and CF\_RETEXTOBJ values.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f5217-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f5217-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f5217-129">Verwenden von Rich Edit-Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="f5217-129">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="f5217-130">[Demo zu allgemeinen Windows-Steuerelementen (cppwindowscommoncontrols)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="f5217-130">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 