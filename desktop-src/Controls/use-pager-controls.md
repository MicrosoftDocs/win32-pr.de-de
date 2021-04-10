---
title: Verwenden von Pager-Steuerelementen
description: In diesem Abschnitt wird beschrieben, wie Sie das Pager-Steuerelement in Ihrer Anwendung implementieren.
ms.assetid: 5703FE4B-987E-49DA-9741-F8B45AD26467
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 586bfff0c8d8097c4b0e861506bb73f55467b711
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104039690"
---
# <a name="how-to-use-pager-controls"></a><span data-ttu-id="38748-103">Verwenden von Pager-Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="38748-103">How to Use Pager Controls</span></span>

<span data-ttu-id="38748-104">In diesem Abschnitt wird beschrieben, wie Sie das Pager-Steuerelement in Ihrer Anwendung implementieren.</span><span class="sxs-lookup"><span data-stu-id="38748-104">This section describes how to implement the pager control in your application.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="38748-105">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="38748-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="38748-106">Technologien</span><span class="sxs-lookup"><span data-stu-id="38748-106">Technologies</span></span>

-   [<span data-ttu-id="38748-107">Windows-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="38748-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="38748-108">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="38748-108">Prerequisites</span></span>

-   <span data-ttu-id="38748-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="38748-109">C/C++</span></span>
-   <span data-ttu-id="38748-110">Programmieren der Windows-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="38748-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="38748-111">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="38748-111">Instructions</span></span>

### <a name="initialize-a-pager-control"></a><span data-ttu-id="38748-112">Pager-Steuerelement initialisieren</span><span class="sxs-lookup"><span data-stu-id="38748-112">Initialize a Pager Control</span></span>

<span data-ttu-id="38748-113">Um das Pager-Steuerelement zu verwenden, müssen Sie die [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) -Funktion mit dem \_ \_ im **dwicc** -Member der [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) -Struktur festgelegten Flag für die-Klasse "pagescroller Class" aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="38748-113">To use the pager control, you must call the [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) function with the ICC\_PAGESCROLLER\_CLASS flag set in the **dwICC** member of the [**INITCOMMONCONTROLSEX**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) structure.</span></span>

### <a name="create-a-pager-control"></a><span data-ttu-id="38748-114">Erstellen eines Pager-Steuer Elements</span><span class="sxs-lookup"><span data-stu-id="38748-114">Create a Pager Control</span></span>

<span data-ttu-id="38748-115">Verwenden Sie die API " [**kreatewindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) " oder " [**kreatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) ", um ein Pager-Steuerelement zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="38748-115">Use the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) or the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) API to create a pager control.</span></span> <span data-ttu-id="38748-116">Der Klassenname für das Steuerelement ist " [**WC \_ pagescroller**](common-control-window-classes.md)", das in "kommctrl. h" definiert ist.</span><span class="sxs-lookup"><span data-stu-id="38748-116">The class name for the control is [**WC\_PAGESCROLLER**](common-control-window-classes.md), which is defined in Commctrl.h.</span></span> <span data-ttu-id="38748-117">Der [**PGS- \_ Horz**](pager-control-styles.md) -Stil wird zum Erstellen eines horizontalen Pager verwendet, und der PGS-Format " [**\_ Vert**](pager-control-styles.md) " wird zum Erstellen eines vertikalen Pager verwendet.</span><span class="sxs-lookup"><span data-stu-id="38748-117">The [**PGS\_HORZ**](pager-control-styles.md) style is used to create a horizontal pager, and the [**PGS\_VERT**](pager-control-styles.md) style is used to create a vertical pager.</span></span> <span data-ttu-id="38748-118">Da es sich hierbei um ein untergeordnetes Steuerelement handelt, sollte auch der untergeordnete [**WS \_**](/windows/desktop/winmsg/window-styles) -Stil verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="38748-118">Because this is a child control, the [**WS\_CHILD**](/windows/desktop/winmsg/window-styles) style should also be used.</span></span>

<span data-ttu-id="38748-119">Nachdem das Pager-Steuerelement erstellt wurde, möchten Sie wahrscheinlich ein enthaltenes Fenster zuweisen.</span><span class="sxs-lookup"><span data-stu-id="38748-119">After the pager control is created, you will most likely want to assign a contained window to it.</span></span> <span data-ttu-id="38748-120">Wenn das enthaltene Fenster ein untergeordnetes Fenster ist, sollten Sie das untergeordnete Fenster als untergeordnetes Element des Pager-Steuer Elements festlegen, sodass Größe und Position ordnungsgemäß berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="38748-120">If the contained window is a child window, you should make the child window a child of the pager control so that the size and position will be calculated correctly.</span></span> <span data-ttu-id="38748-121">Anschließend weisen Sie das Fenster dem Pager-Steuerelement mit der [**PGM- \_ setchild**](pgm-setchild.md) -Nachricht zu.</span><span class="sxs-lookup"><span data-stu-id="38748-121">You then assign the window to the pager control with the [**PGM\_SETCHILD**](pgm-setchild.md) message.</span></span> <span data-ttu-id="38748-122">Beachten Sie, dass diese Meldung das übergeordnete Fenster des enthaltenen Fensters nicht tatsächlich ändert. Er weist lediglich das enthaltene Fenster zu.</span><span class="sxs-lookup"><span data-stu-id="38748-122">Be aware that this message does not actually change the parent window of the contained window; it simply assigns the contained window.</span></span> <span data-ttu-id="38748-123">Wenn das enthaltene Fenster eines der allgemeinen Steuerelemente ist, muss es den [**CCS \_ NORESIZE**](common-control-styles.md) -Stil aufweisen, um zu verhindern, dass das Steuerelement versucht, die Größe der Größe des Pager-Steuer Elements zu ändern.</span><span class="sxs-lookup"><span data-stu-id="38748-123">If the contained window is one of the common controls, it must have the [**CCS\_NORESIZE**](common-control-styles.md) style to prevent the control from attempting to resize itself to the pager control's size.</span></span>

### <a name="process-pager-control-notifications"></a><span data-ttu-id="38748-124">Pager-Steuerelement Benachrichtigungen verarbeiten</span><span class="sxs-lookup"><span data-stu-id="38748-124">Process Pager Control Notifications</span></span>

<span data-ttu-id="38748-125">Es ist mindestens erforderlich, dass die [PGN \_ calcsize](pgn-calcsize.md) -Benachrichtigung verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="38748-125">At a minimum, it is necessary to process the [PGN\_CALCSIZE](pgn-calcsize.md) notification.</span></span> <span data-ttu-id="38748-126">Wenn Sie diese Benachrichtigung nicht verarbeiten und einen Wert für die Breite oder Höhe eingeben, werden die Bild Lauf Pfeile im Pager-Steuerelement nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="38748-126">If you do not process this notification and enter a value for the width or height, the scroll arrows in the pager control will not be displayed.</span></span> <span data-ttu-id="38748-127">Dies liegt daran, dass das Pager-Steuerelement die Breite oder Höhe verwendet, die in der PGN \_ calcsize-Benachrichtigung angegeben ist, um die "ideale" Größe des enthaltenen Fensters zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="38748-127">This is because the pager control uses the width or height supplied in the PGN\_CALCSIZE notification to determine the "ideal" size of the contained window.</span></span>

<span data-ttu-id="38748-128">Im folgenden Beispiel wird veranschaulicht, wie die [PGN \_ calcsize](pgn-calcsize.md) -Benachrichtigungs Fälle verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="38748-128">The following example demonstrates how to process the [PGN\_CALCSIZE](pgn-calcsize.md) notification case.</span></span> <span data-ttu-id="38748-129">In diesem Beispiel ist das enthaltene Fenster ein Symbolleisten-Steuerelement, das eine unbekannte Anzahl von Schaltflächen mit einer unbekannten Größe enthält.</span><span class="sxs-lookup"><span data-stu-id="38748-129">In this example, the contained window is a toolbar control that contains an unknown number of buttons at an unknown size.</span></span> <span data-ttu-id="38748-130">Im Beispiel wird gezeigt, wie die [**TB \_ getmaxsize**](tb-getmaxsize.md) -Nachricht verwendet wird, um die Größe aller Elemente in der Symbolleiste zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="38748-130">The example shows how to use the [**TB\_GETMAXSIZE**](tb-getmaxsize.md) message to determine the size of all of the items in the toolbar.</span></span> <span data-ttu-id="38748-131">Im Beispiel wird dann die Breite aller Elemente in den **iWidth** -Member der [**nmpgcalcsize**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgcalcsize) -Struktur eingefügt, die an die Benachrichtigung übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="38748-131">The example then places the width of all of the items into the **iWidth** member of the [**NMPGCALCSIZE**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgcalcsize) structure that is passed to the notification.</span></span>


```C++
case PGN_SCROLL:{

    LPNMPGSCROLL pScroll = (LPNMPGSCROLL)lParam;
 
    switch(pScroll->iDir){
     
        case PGF_SCROLLLEFT:
        case PGF_SCROLLRIGHT:
        case PGF_SCROLLUP:
        case PGF_SCROLLDOWN:
     
            pScroll->iScroll = 20;
        
            break;
        }
    }
  
return 0;
```



## <a name="related-topics"></a><span data-ttu-id="38748-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="38748-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="38748-133">Verwenden von Pager-Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="38748-133">Using Pager Controls</span></span>](using-pager-controls.md)
</dt> <dt>

<span data-ttu-id="38748-134">[Demo zu allgemeinen Windows-Steuerelementen (cppwindowscommoncontrols)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="38748-134">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 