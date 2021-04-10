---
title: Erstellen einer Schaltfläche
description: Um Schaltflächen dynamisch zu erstellen, verwenden Sie die Funktion "up Window" oder "kreatewindowex". In diesem Thema wird veranschaulicht, wie Sie mit der Funktion "up Window" eine standardmäßige pushschaltfläche erstellen.
ms.assetid: A8C56D09-90A3-4C70-9907-61390521D1DA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dadc53f91f773e5fce9e29bdf1ae50cc59bfdfd
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104039870"
---
# <a name="how-to-create-a-button"></a><span data-ttu-id="738da-104">Erstellen einer Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="738da-104">How to Create a Button</span></span>

<span data-ttu-id="738da-105">Um Schaltflächen dynamisch zu erstellen, verwenden Sie die Funktion "up [**Window**](/windows/desktop/api/winuser/nf-winuser-createwindowa) " oder " [**kreatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) ".</span><span class="sxs-lookup"><span data-stu-id="738da-105">To create buttons dynamically, you use the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) or [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function.</span></span> <span data-ttu-id="738da-106">In diesem Thema wird veranschaulicht, wie Sie mit der Funktion "up **Window** " eine standardmäßige pushschaltfläche erstellen.</span><span class="sxs-lookup"><span data-stu-id="738da-106">This topic demonstrates how to use the **CreateWindow** function to create a default push button.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="738da-107">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="738da-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="738da-108">Technologien</span><span class="sxs-lookup"><span data-stu-id="738da-108">Technologies</span></span>

-   [<span data-ttu-id="738da-109">Windows-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="738da-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="738da-110">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="738da-110">Prerequisites</span></span>

-   <span data-ttu-id="738da-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="738da-111">C/C++</span></span>
-   <span data-ttu-id="738da-112">Programmieren der Windows-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="738da-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="738da-113">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="738da-113">Instructions</span></span>


<span data-ttu-id="738da-114">Verwenden Sie [**die Funktion**](/windows/desktop/api/winuser/nf-winuser-createwindowa) "Funktion", um ein Schaltflächen-Steuerelement zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="738da-114">Use the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) function to create a button control.</span></span>

<span data-ttu-id="738da-115">Im folgenden C++-Beispiel ist der *m- \_ HWND* -Parameter das Handle für das übergeordnete Fenster.</span><span class="sxs-lookup"><span data-stu-id="738da-115">In the following C++ example, the *m\_hwnd* parameter is the handle to the parent window.</span></span> <span data-ttu-id="738da-116">Der [**\_ DEFPUSHBUTTON**](button-styles.md) -Stil von "bin" gibt an, dass eine Standard Schaltfläche "Push" erstellt wird</span><span class="sxs-lookup"><span data-stu-id="738da-116">The [**BS\_DEFPUSHBUTTON**](button-styles.md) style specifies that a default push button should be created.</span></span> <span data-ttu-id="738da-117">Beachten Sie, dass die Größen-und Positionswerte angegeben werden müssen, da bei Verwendung von **CW \_ usedefault** für eine Schaltfläche die Werte auf NULL festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="738da-117">Note that the size and position values must be specified because using **CW\_USEDEFAULT** for a button sets the values to zero.</span></span>


```C++
HWND hwndButton = CreateWindow( 
    L"BUTTON",  // Predefined class; Unicode assumed 
    L"OK",      // Button text 
    WS_TABSTOP | WS_VISIBLE | WS_CHILD | BS_DEFPUSHBUTTON,  // Styles 
    10,         // x position 
    10,         // y position 
    100,        // Button width
    100,        // Button height
    m_hwnd,     // Parent window
    NULL,       // No menu.
    (HINSTANCE)GetWindowLongPtr(m_hwnd, GWLP_HINSTANCE), 
    NULL);      // Pointer not needed.
```



## <a name="related-topics"></a><span data-ttu-id="738da-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="738da-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="738da-119">Informationen zu Schaltflächen</span><span class="sxs-lookup"><span data-stu-id="738da-119">About Buttons</span></span>](about-buttons.md)
</dt> <dt>

[<span data-ttu-id="738da-120">Button-Steuerelement Verweis</span><span class="sxs-lookup"><span data-stu-id="738da-120">Button Control Reference</span></span>](bumper-button-button-control-reference.md)
</dt> <dt>

[<span data-ttu-id="738da-121">Verwenden von Schaltflächen</span><span class="sxs-lookup"><span data-stu-id="738da-121">Using Buttons</span></span>](using-buttons.md)
</dt> <dt>

[<span data-ttu-id="738da-122">Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="738da-122">Button</span></span>](buttons.md)
</dt> </dl>

 

 