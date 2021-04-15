---
title: Implementieren von Quick Infos für Status leisten Symbole
description: Eine nicht eindringliche Möglichkeit, eine erklärende Meldung für ein Status leisten Symbol anzuzeigen, ist die Implementierung einer QuickInfo. Die QuickInfo wird beim Klicken nicht mehr angezeigt, Sie können aber auch einen Timeout Wert angeben.
ms.assetid: AA7F17F2-63A4-4954-9DAB-788B73984628
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 277fb8d15654ae51565c1a461a9a8414d3e9213c
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104474397"
---
# <a name="how-to-implement-tooltips-for-status-bar-icons"></a><span data-ttu-id="54a22-104">Implementieren von Quick Infos für Status leisten Symbole</span><span class="sxs-lookup"><span data-stu-id="54a22-104">How to Implement Tooltips for Status Bar Icons</span></span>

<span data-ttu-id="54a22-105">Eine nicht eindringliche Möglichkeit, eine erklärende Meldung für ein Status leisten Symbol anzuzeigen, ist die Implementierung einer QuickInfo.</span><span class="sxs-lookup"><span data-stu-id="54a22-105">A nonintrusive way to display an explanatory message for a status bar icon is to implement a tooltip.</span></span> <span data-ttu-id="54a22-106">Die QuickInfo wird beim Klicken nicht mehr angezeigt, Sie können aber auch einen Timeout Wert angeben.</span><span class="sxs-lookup"><span data-stu-id="54a22-106">The tooltip disappears when clicked, but you can also specify a time-out value.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="54a22-107">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="54a22-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="54a22-108">Technologien</span><span class="sxs-lookup"><span data-stu-id="54a22-108">Technologies</span></span>

-   [<span data-ttu-id="54a22-109">Windows-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="54a22-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="54a22-110">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="54a22-110">Prerequisites</span></span>

-   <span data-ttu-id="54a22-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="54a22-111">C/C++</span></span>
-   <span data-ttu-id="54a22-112">Programmieren der Windows-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="54a22-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="54a22-113">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="54a22-113">Instructions</span></span>

### <a name="implement-tooltips-for-status-bar-icons"></a><span data-ttu-id="54a22-114">Tooltips für StatusBar-Symbole implementieren</span><span class="sxs-lookup"><span data-stu-id="54a22-114">Implement Tooltips for Status Bar Icons</span></span>

<span data-ttu-id="54a22-115">Im folgenden Code Fragment wird veranschaulicht, wie einem Status leisten Symbol eine QuickInfo-Sprechblase hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="54a22-115">The following code fragment illustrates how to add a balloon tooltip to a status bar icon.</span></span>


```C++
#define ARRAYSIZE(a) (sizeof(a)/sizeof(a[0]))

NOTIFYICONDATA IconData = {0};

IconData.cbSize = sizeof(IconData);
IconData.hWnd   = hwndNI;
IconData.uFlags = NIF_INFO;

HRESULT hr = StringCchCopy(IconData.szInfo, 
                           ARRAYSIZE(IconData.szInfo), 
                           TEXT("Your message text goes here."));

if(FAILED(hr))
{
  // TODO: Write an error handler in case the call to StringCchCopy fails.
}
IconData.uTimeout = 15000; // in milliseconds

Shell_NotifyIcon(NIM_MODIFY, &IconData);
            
```



## <a name="remarks"></a><span data-ttu-id="54a22-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="54a22-116">Remarks</span></span>

<span data-ttu-id="54a22-117">Eine ausführliche Erläuterung der Statusleiste finden Sie in [der Taskleiste](/windows/desktop/shell/taskbar).</span><span class="sxs-lookup"><span data-stu-id="54a22-117">For a detailed discussion of the status bar, see [The Taskbar](/windows/desktop/shell/taskbar).</span></span>

<span data-ttu-id="54a22-118">Zum Anzeigen einer QuickInfo-Sprechblase müssen Sie das NIF- \_ infoflag in der [**notifyiendata**](/windows/desktop/api/shellapi/ns-shellapi-notifyicondataa) -Struktur festlegen und die Elemente **szinfo** und **utimeout** verwenden, um den QuickInfo-Text und die Timeout Dauer anzugeben.</span><span class="sxs-lookup"><span data-stu-id="54a22-118">To display a balloon tooltip, you need to set the NIF\_INFO flag in the [**NOTIFYICONDATA**](/windows/desktop/api/shellapi/ns-shellapi-notifyicondataa) structure, and use the **szInfo** and **uTimeout** members to specify the tooltip text and time-out duration.</span></span>

## <a name="related-topics"></a><span data-ttu-id="54a22-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="54a22-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54a22-120">Verwenden von Quick Infos</span><span class="sxs-lookup"><span data-stu-id="54a22-120">Using Tooltip Controls</span></span>](using-tooltip-contro.md)
</dt> </dl>

 

 