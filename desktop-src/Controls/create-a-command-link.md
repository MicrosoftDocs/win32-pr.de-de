---
title: Erstellen eines Befehls Links
description: In diesem Thema wird eine Möglichkeit zum Erstellen eines Befehls Links beschrieben.
ms.assetid: F342075B-2D3B-40E0-B657-E1C57EDC2E3A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8024a7f060a7bae3779b9ec9ebec40bd81c74bb
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104474461"
---
# <a name="how-to-create-a-command-link"></a><span data-ttu-id="77310-103">Erstellen eines Befehls Links</span><span class="sxs-lookup"><span data-stu-id="77310-103">How to Create a Command Link</span></span>

<span data-ttu-id="77310-104">In diesem Thema wird eine Möglichkeit zum Erstellen eines Befehls Links beschrieben.</span><span class="sxs-lookup"><span data-stu-id="77310-104">This topic describes one way to create a command link.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="77310-105">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="77310-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="77310-106">Technologien</span><span class="sxs-lookup"><span data-stu-id="77310-106">Technologies</span></span>

-   [<span data-ttu-id="77310-107">Windows-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="77310-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="77310-108">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="77310-108">Prerequisites</span></span>

-   <span data-ttu-id="77310-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="77310-109">C/C++</span></span>
-   <span data-ttu-id="77310-110">Programmieren der Windows-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="77310-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="77310-111">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="77310-111">Instructions</span></span>

### <a name="step-1-create-an-instance-of-the-command-link-button"></a><span data-ttu-id="77310-112">Schritt 1: Erstellen Sie eine Instanz der Befehls Link Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="77310-112">Step 1: Create an instance of the command link button.</span></span>

<span data-ttu-id="77310-113">Im folgenden C++-Codebeispiel gibt der "Format Bezeichner" ( [**\_ CommandLink**](button-styles.md) ) die Schaltfläche als Befehls Link Schaltfläche an.</span><span class="sxs-lookup"><span data-stu-id="77310-113">In the following C++ code example, the style constant [**BS\_COMMANDLINK**](button-styles.md) specifies the button as a command link button.</span></span>


```C++
HWND hwndCommandLink = CreateWindow(
    L"BUTTON",  // Predefined class; Unicode assumed
    L"",        // Text will be defined later
    WS_TABSTOP | WS_VISIBLE | WS_CHILD | BS_COMMANDLINK,  // Styles
    200,        // x position 
    10,         // y position 
    100,        // Button width
    100,        // Button height
    m_hwnd,     // Parent window
    NULL,       // No menu
    (HINSTANCE)GetWindowLongPtr(m_hwnd, GWLP_HINSTANCE), 
    NULL);      // Pointer not needed
```



### <a name="step-2-set-the-command-link-label-and-explanation-text"></a><span data-ttu-id="77310-114">Schritt 2: Festlegen der Bezeichnung für den Befehls Link und den Erläuterungstext</span><span class="sxs-lookup"><span data-stu-id="77310-114">Step 2: Set the command link label and explanation text</span></span>

<span data-ttu-id="77310-115">Verwenden Sie die [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) -Funktion, um die Bezeichnung für den Befehls Link und ergänzenden Text über die [**WM- \_ SetText**](/windows/desktop/winmsg/wm-settext) -Nachricht und die [**BCM- \_ setnote**](bcm-setnote.md) -Nachricht festzulegen.</span><span class="sxs-lookup"><span data-stu-id="77310-115">Use the [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) function to set the command link label and supplementary text via the [**WM\_SETTEXT**](/windows/desktop/winmsg/wm-settext) message and the [**BCM\_SETNOTE**](bcm-setnote.md) message, respectively.</span></span>


```C++
SendMessage(hwndCommandLink, WM_SETTEXT, 0, (LPARAM)L"Command link");
SendMessage(hwndCommandLink, BCM_SETNOTE, 0, (LPARAM)L"with note");
```



## <a name="related-topics"></a><span data-ttu-id="77310-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="77310-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77310-117">Informationen zu Schaltflächen</span><span class="sxs-lookup"><span data-stu-id="77310-117">About Buttons</span></span>](about-buttons.md)
</dt> <dt>

[<span data-ttu-id="77310-118">Button-Steuerelement Verweis</span><span class="sxs-lookup"><span data-stu-id="77310-118">Button Control Reference</span></span>](bumper-button-button-control-reference.md)
</dt> <dt>

[<span data-ttu-id="77310-119">Verwenden von Schaltflächen</span><span class="sxs-lookup"><span data-stu-id="77310-119">Using Buttons</span></span>](using-buttons.md)
</dt> <dt>

[<span data-ttu-id="77310-120">Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="77310-120">Button</span></span>](buttons.md)
</dt> </dl>

 

 